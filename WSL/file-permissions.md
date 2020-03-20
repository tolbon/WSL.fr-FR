---
title: Autorisations de fichiers
description: Comprendre comment WSL détermine les autorisations de fichiers dans Windows
keywords: BashOnWindows, bash, WSL, wsl2, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, fichier, autorisations
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520858"
---
# <a name="file-permissions-for-wsl"></a>Autorisations de fichier pour WSL

Cette page explique en détail comment les autorisations des fichiers Linux sont interprétées dans le sous-système Windows pour Linux, en particulier lors de l’accès à des ressources dans Windows sur le système de fichiers NT. Cette documentation suppose une connaissance élémentaire de la [structure des autorisations du système de fichiers Linux](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) . <!--TODO: Double check that it's okay to add these links--> et la [commande umask](https://en.wikipedia.org/wiki/Umask).

Lors de l’accès aux fichiers Windows à partir de WSL, les autorisations de fichiers sont calculées à partir des autorisations Windows ou lues à partir de métadonnées qui ont été ajoutées au fichier par WSL. Ces métadonnées ne sont pas activées par défaut. 

## <a name="wsl-metadata-on-windows-files"></a>WSL les métadonnées sur les fichiers Windows

Lorsque les métadonnées sont activées en tant qu’option de montage dans WSL, les attributs étendus des fichiers Windows NT peuvent être ajoutés et interprétés pour fournir des autorisations de système de fichiers Linux. 

WSL peut ajouter quatre attributs étendus NTFS :

| Nom de l’attribut | Description |
| --- | --- |
| $LXUID | ID du propriétaire de l’utilisateur |
| $LXGID | ID du propriétaire du groupe |
| $LXMOD | Mode de fichier (autorisations des systèmes de fichiers octaux et type, par exemple : 0777) |
| $LXDEV | Appareil, s’il s’agit d’un fichier d’appareil |

En outre, tout fichier qui n’est pas un fichier ou un répertoire normal (par exemple, liens symboliques, FIFO, Block Devices, les sockets Unix et les périphériques de caractères) a également un [point d’analyse](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)NTFS. Il est ainsi beaucoup plus rapide de déterminer le type de fichier dans un répertoire donné sans avoir à interroger ses attributs étendus. 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a>Scénarios d’accès aux fichiers

Vous trouverez ci-dessous une description de la façon dont les autorisations sont déterminées lors de l’accès aux fichiers de différentes manières à l’aide du sous-système Windows pour Linux.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Accès aux fichiers dans le système de fichiers du lecteur Windows (DrvFS) à partir de Linux

Ces scénarios se produisent lorsque vous accédez à vos fichiers Windows à partir de WSL, très probablement via `/mnt/c`. 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>Lecture des autorisations de fichier à partir d’un fichier Windows existant

Le résultat dépend de si le fichier a déjà des métadonnées existantes.

##### <a name="the-file-does-not-have-metadata-default"></a>**Le fichier ne contient pas de métadonnées (par défaut)**

Si le fichier n’a pas de métadonnées qui lui sont associées, nous traduisons les autorisations effectives de l’utilisateur Windows en lecture/écriture/exécution des bits et leur attribuons la même valeur pour l’utilisateur, le groupe et l’autre. Par exemple, si votre compte d’utilisateur Windows dispose d’un accès en lecture et en écriture, mais pas d’un accès en écriture au fichier, ce sera affiché comme `r-x` pour utilisateur, groupe et autre. Si l’attribut « lecture seule » du fichier est défini dans Windows, nous n’accordons pas d’accès en écriture dans Linux.

##### <a name="the-file-has-metadata"></a>Le fichier contient des métadonnées

Si le fichier contient des métadonnées, nous utilisons simplement ces valeurs de métadonnées au lieu de traduire les autorisations effectives de l’utilisateur Windows.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Modification des autorisations de fichier sur un fichier Windows existant à l’aide de chmod

Le résultat dépend de si le fichier a déjà des métadonnées existantes.

##### <a name="the-file-does-not-have-metadata-default"></a>**Le fichier ne contient pas de métadonnées (par défaut)**

Chmod n’aura qu’un seul effet. Si vous supprimez tous les attributs d’écriture d’un fichier, l’attribut « lecture seule » du fichier Windows est défini, car il s’agit du même comportement que CIFS (Common Internet File System) qui est le client SMB (Server Message Block) dans Linux.

##### <a name="the-file-has-metadata"></a>Le fichier contient des métadonnées

Chmod change ou ajoute des métadonnées en fonction des métadonnées existantes du fichier. 

N’oubliez pas que vous ne pouvez pas vous accorder plus d’accès que ce que vous avez sur Windows, même si les métadonnées indiquent que c’est le cas. Par exemple, vous pouvez définir les métadonnées pour qu’elles s’affichent pour que vous disposiez d’autorisations d’accès en écriture à un fichier à l’aide de `chmod 777`, mais si vous tentez d’accéder à ce fichier, vous ne pourrez toujours pas écrire dessus. Grâce à l’interopérabilité, les commandes de lecture ou d’écriture des fichiers Windows sont routées via vos autorisations d’utilisateur Windows.

#### <a name="creating-a-file-in-drivefs"></a>Création d’un fichier dans DriveFS

Le résultat dépend de si les métadonnées sont activées.

##### <a name="metadata-is-not-enabled-default"></a>Les métadonnées ne sont pas activées (par défaut)

Les autorisations Windows du fichier nouvellement créé sont les mêmes que si vous avez créé le fichier dans Windows sans un descripteur de sécurité spécifique, il hérite des autorisations du parent. 

##### <a name="metadata-is-enabled"></a>Les métadonnées sont activées

Les bits d’autorisation du fichier sont définis de façon à suivre l’umask Linux, et le fichier est enregistré avec les métadonnées.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>Quel utilisateur Linux et quel groupe Linux possède le fichier ? 

Le résultat dépend de si le fichier a déjà des métadonnées existantes.

##### <a name="the-file-does-not-have-metadata-default"></a>**Le fichier ne contient pas de métadonnées (par défaut)**
Dans le scénario par défaut, lors du montage automatique de lecteurs Windows, nous spécifions que l’ID d’utilisateur (UID) de tous les fichiers est défini sur l’ID d’utilisateur de votre utilisateur WSL et que l’ID de groupe (GID) est défini sur l’ID de groupe principal de votre utilisateur WSL. 

##### <a name="the-file-has-metadata"></a>Le fichier contient des métadonnées

L’UID et le GID spécifiés dans les métadonnées sont appliqués en tant que propriétaire de l’utilisateur et propriétaire du fichier. 

### <a name="accessing-linux-files-from-windows-using-wsl"></a>Accès aux fichiers Linux à partir de Windows à l’aide de `\\wsl$`

L’accès aux fichiers Linux via `\\wsl$` utilise l’utilisateur par défaut de votre distribution WSL. Par conséquent, toute application Windows accédant à des fichiers Linux aura les mêmes autorisations que l’utilisateur par défaut.

#### <a name="creating-a-new-file"></a>Création d’un nouveau fichier

L’umask par défaut est appliqué lors de la création d’un nouveau fichier à l’intérieur d’un WSL distribution à partir de Windows. L’umask par défaut est `022`, ou en d’autres termes, il autorise toutes les autorisations, à l’exception des autorisations d’écriture sur les groupes et autres. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Accès aux fichiers dans le système de fichiers racine Linux à partir de Linux

Tous les fichiers créés, modifiés ou consultés dans le système de fichiers racine Linux suivent les conventions Linux standard, telles que l’application de l’umask à un fichier nouvellement créé.

## <a name="configuring-file-permissions"></a>Configuration des autorisations de fichier

Vous pouvez configurer vos autorisations de fichier à l’intérieur de vos lecteurs Windows à l’aide des options de montage dans WSL. conf. Les options de montage vous permettent de définir des masques d’autorisations `umask`, `dmask` et `fmask`. Le `umask` est appliqué à tous les fichiers, le `dmask` est appliqué uniquement aux répertoires et le `fmask` est appliqué uniquement aux fichiers. Ces masques d’autorisation sont ensuite placés via une opération OR logique lorsqu’ils sont appliqués aux fichiers. par exemple, si vous avez une valeur `umask` de `023` et une valeur `fmask` de `022`, le masque des autorisations résultant pour les fichiers sera `023`. 

Pour obtenir des instructions sur la procédure à suivre, consultez la page [« gérer les distributions Linux »](./wsl-config.md) .
<!-- TODO: Add # to the link-->

