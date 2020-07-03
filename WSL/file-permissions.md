---
title: Autorisations de fichier
description: Comprendre comment WSL détermine les autorisations de fichier dans Windows
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, fichier, autorisations
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.openlocfilehash: 81d4cfa1ae57cdd077ba8cbd614111881724718a
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336072"
---
# <a name="file-permissions-for-wsl"></a>Autorisations de fichier pour WSL

Cette page explique en détail comment les autorisations de fichier Linux sont interprétées dans le sous-système Windows pour Linux, en particulier lors de l’accès à des ressources dans Windows, dans le système de fichiers NT. Cette documentation suppose d’avoir compris les bases de la [structure des autorisations du système de fichiers Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) et de la [commande umask](https://en.wikipedia.org/wiki/Umask).

Lors de l’accès à des fichiers Windows à partir de WSL, les autorisations de fichier sont calculées à partir des autorisations Windows ou lues à partir des métadonnées qui ont été ajoutées au fichier par WSL. Ces métadonnées ne sont pas activées par défaut.

## <a name="wsl-metadata-on-windows-files"></a>Métadonnées WSL sur les fichiers Windows

Lorsque les métadonnées sont activées comme option de montage dans WSL, des attributs étendus sur les fichiers Windows NT peuvent être ajoutés et interprétés pour fournir des autorisations de système de fichiers Linux.

WSL peut ajouter quatre attributs étendus NTFS :

| Nom d’attribut | Description |
| --- | --- |
| $LXUID | ID d’utilisateur propriétaire |
| $LXGID | ID de groupe propriétaire |
| $LXMOD | Mode fichier (octaux et type d’autorisation des systèmes de fichiers, p. ex. : 0777) |
| $LXDEV | Appareil, s’il s’agit d’un fichier d’appareil |

De plus, tout fichier qui n’est pas un fichier ou un répertoire standard (p. ex. : liens symboliques, FIFO, périphériques de traitement par blocs, sockets Unix et périphériques d’entrée-sortie de caractères) a également un [point d’analyse](https://docs.microsoft.com/windows/win32/fileio/reparse-points) NTFS. Il est ainsi beaucoup plus rapide de déterminer le type de fichier figurant dans un répertoire donné sans avoir à interroger ses attributs étendus.

## <a name="file-access-scenarios"></a>Scénarios d’accès aux fichiers

Vous trouverez ci-dessous une description de la façon dont les autorisations sont déterminées lors de l’accès aux fichiers de différentes manières à l’aide du sous-système Windows pour Linux.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Accès aux fichiers dans le système de fichiers du lecteur Windows (DrvFS) à partir de Linux

Ces scénarios surviennent lorsque vous accédez à vos fichiers Windows à partir de WSL, probablement via `/mnt/c`.

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>Lecture des autorisations de fichier à partir d’un fichier Windows existant

Le résultat dépend du fait que le fichier a ou non déjà des métadonnées existantes.

##### <a name="drvfs-file-does-not-have-metadata-default"></a>Le fichier DrvFS n’a pas de métadonnées (par défaut)

Si le fichier n’a pas de métadonnées associées, nous traduisons les autorisations effectives de l’utilisateur Windows en bits de lecture/écriture/exécution et leur attribuons la même valeur pour l’utilisateur, le groupe et autre. Par exemple, si votre compte d’utilisateur Windows dispose d’un accès en lecture et exécution, mais pas d’un accès en écriture au fichier, cela sera indiqué sous la forme `r-x` pour l’utilisateur, le groupe et autre. Si l’attribut « Lecture seule » du fichier est défini dans Windows, nous n’accordons pas l’accès en écriture dans Linux.

##### <a name="the-file-has-metadata"></a>Le fichier a des métadonnées

Si le fichier a des métadonnées, nous utilisons simplement ces valeurs de métadonnées au lieu de traduire les autorisations effectives de l’utilisateur Windows.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Modification des autorisations de fichier d’un fichier Windows existant à l’aide de chmod

Le résultat dépend du fait que le fichier a ou non déjà des métadonnées existantes.

##### <a name="chmod-file-does-not-have-metadata-default"></a>Le fichier chmod n’a pas de métadonnées (par défaut)

Chmod aura un seul effet. Si vous supprimez tous les attributs d’écriture d’un fichier, l’attribut « lecture seule » du fichier Windows est défini, car il s’agit du même comportement que celui du système CIFS (Common Internet File System) qui est le client SMB (Server Message Block) dans Linux.

##### <a name="chmod-file-has-metadata"></a>Le fichier chmod a des métadonnées

Chmod change ou ajoute des métadonnées en fonction des métadonnées déjà existantes du fichier. 

N’oubliez pas que vous ne pouvez pas vous accorder plus d’accès que ce que vous avez sur Windows, même si les métadonnées indiquent que vous le pouvez. Par exemple, vous pouvez définir les métadonnées pour qu’elles affichent que vous disposez d’autorisations en écriture à un fichier à l’aide de `chmod 777`, mais si vous tentez d’accéder à ce fichier, vous ne pourrez toujours pas écrire dedans. Cela est dû à l’interopérabilité, car les commandes de lecture et d’écriture des fichiers Windows sont routées via vos autorisations d’utilisateur Windows.

#### <a name="creating-a-file-in-drivefs"></a>Création d’un fichier dans DriveFS

Le résultat dépend de l’activation ou non des métadonnées.

##### <a name="metadata-is-not-enabled-default"></a>Les métadonnées ne sont pas activées (par défaut)

Les autorisations Windows du fichier nouvellement créé sont les mêmes que si vous avez créé le fichier dans Windows sans un descripteur de sécurité spécifique. Il hérite des autorisations du parent.

##### <a name="metadata-is-enabled"></a>Les métadonnées sont activées

Les bits d’autorisation de fichier sont définis de façon à suivre le masque umask Linux, et le fichier est enregistré avec les métadonnées.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>Quel utilisateur Linux et quel groupe Linux le fichier détient-il ? 

Le résultat dépend du fait que le fichier a ou non déjà des métadonnées existantes.

##### <a name="user-file-does-not-have-metadata-default"></a>Le fichier utilisateur n’a pas de métadonnées (par défaut)

Dans le scénario par défaut, lors du montage automatique de lecteurs Windows, nous spécifions que l’ID d’utilisateur (UID) de tous les fichiers est défini sur l’ID d’utilisateur (UID) de votre utilisateur WSL et que l’ID de groupe (GID) est défini sur l’ID de groupe principal de votre utilisateur WSL.

##### <a name="user-file-has-metadata"></a>Le fichier utilisateur a des métadonnées

Les identificateurs UID et GID spécifiés dans les métadonnées sont appliqués en tant qu’utilisateur propriétaire et groupe propriétaire du fichier.

### <a name="accessing-linux-files-from-windows-using-wsl"></a>Accès aux fichiers Linux à partir de Windows à l’aide de `\\wsl$`

L’accès aux fichiers Linux via `\\wsl$` utilise l’utilisateur par défaut de votre distribution WSL. Par conséquent, toute application Windows accédant à des fichiers Linux aura les mêmes autorisations que l’utilisateur par défaut.

#### <a name="creating-a-new-file"></a>Création d’un nouveau fichier

Le masque umask par défaut est appliqué lors de la création d’un nouveau fichier à l’intérieur d’une distribution WSL à partir de Windows. Le masque umask par défaut est `022`. En d’autres termes, il autorise toutes les autorisations, à l’exception des autorisations en écriture sur les groupes et autres. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Accès aux fichiers dans le système de fichiers racine Linux à partir de Linux

Tous les fichiers créés, modifiés ou consultés dans le système de fichiers racine Linux suivent les conventions Linux standard, telles que l’application du masque umask à un fichier nouvellement créé.

## <a name="configuring-file-permissions"></a>Configuration des autorisations de fichier

Vous pouvez configurer vos autorisations de fichier à l’intérieur de vos lecteurs Windows à l’aide des options de montage figurant dans wsl.conf. Les options de montage vous permettent de définir des masques d’autorisations `umask`, `dmask` et `fmask`. Le masque `umask` est appliqué à tous les fichiers, le masque `dmask` est appliqué uniquement aux répertoires et le masque `fmask` est appliqué uniquement aux fichiers. Ces masques d’autorisations passent ensuite par une opération OR logique lorsqu’ils sont appliqués aux fichiers, p. ex. : Si vous avez une valeur `umask` de `023` et une valeur `fmask` de `022`, le masque d’autorisations résultant pour les fichiers sera `023`.

Pour obtenir des instructions sur la procédure à suivre, consultez l’article [Configurer les paramètres de lancement par distribution avec wslconf](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf).
