---
title: Forum Aux Questions (FAQ)
description: Questions fréquentes sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063267"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Forum aux Questions sur le sous-système de Windows pour Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Quel est le sous-système Windows pour Linux (WSL) ?
Le sous-système Windows pour Linux (WSL) est une nouvelle fonctionnalité de Windows 10 qui vous permet d’exécuter des outils de ligne de commande Linux natifs directement sur Windows, applications du Windows store en même temps que votre ordinateur de bureau Windows traditionnel et modernes.

Consultez le [sur la page](./about.md) pour plus d’informations.

## <a name="who-is-wsl-for"></a>Qui est WSL pour ?
Il s’agit principalement d’un outil pour les développeurs, en particulier les développeurs web et ceux qui travaillent sur ou avec des projets open source. Ainsi, les personnes souhaitez/devez utiliser Bash, des outils Linux courants (`sed`, `awk`, etc.) et de nombreux outils Linux en premier (Ruby, Python, etc.) à utiliser leur chaîne d’outils sur Windows.

## <a name="what-can-i-do-with-wsl"></a>Que puis-je faire avec WSL ?
WSL fournit qu'une application appelée Bash.exe qui, au démarrage, ouvre une console Windows en cours d’exécution l’interpréteur de commandes Bash. À l’aide de Bash, vous pouvez exécuter des applications et des outils de ligne de commande Linux. Par exemple, tapez `lsb_release -a` et appuyez sur entrée ; vous allez voir les détails de la distribution Linux en cours d’exécution :

![Capture d’écran de détails de la distribution](media/distro.png)

Vous pouvez également accéder à du système de fichiers votre ordinateur local à partir de dans l’interpréteur de commandes d’interpréteur de commandes Linux : vous trouverez vos lecteurs locaux montés sous le `/mnt` dossier. Par exemple, votre `C:` lecteur est monté sous `/mnt/c`:  

![Capture d’écran du lecteur C monté](media/ls.png)

## <a name="what-is-bash"></a>Nouveautés de Bash ?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) est un interpréteur de textuel populaire et le langage de commande. Il est l’interpréteur de commandes par défaut inclus dans Ubuntu et d’autres distributions de Linux et macOS. Les utilisateurs tapent des commandes dans un interpréteur de commandes pour exécuter des scripts et/ou exécuter des commandes et des outils pour effectuer de nombreuses tâches.

## <a name="how-does-this-work"></a>Comment cela fonctionne-t-il ?
Découvrez notre [blog](https://blogs.msdn.microsoft.com/wsl/) où nous allons dans les détails de la technologie sous-jacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>Pourquoi utiliser WSL plutôt que Linux dans une machine virtuelle ?
WSL nécessite moins de ressources (processeur, mémoire et stockage) qu’une machine virtuelle complète. WSL vous permet également d’exécuter les outils de ligne de commande Linux et applications en même temps que vos applications bureau et store de la ligne de commande, Windows et à accéder à vos fichiers Windows à partir de Linux. Cela vous permet d’utiliser des applications de Windows et les outils de ligne de commande Linux sur le même ensemble de fichiers si vous le souhaitez.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>Pourquoi utiliser, par exemple, Ruby on Linux au lieu de sur Windows ?
Certains des outils multiplateformes ont été créés en supposant que l’environnement dans lequel ils s’exécutent se comporte comme Linux. Par exemple, certains outils supposent qu’ils sont en mesure d’accéder très longs chemins d’accès ou que des fichiers/dossiers spécifiques existent. Cela entraîne souvent des problèmes sur Windows qui souvent se comporte différemment à partir de Linux.

De nombreux langages tels que Ruby et nœud sont souvent portés à et s’exécutent très bien sur Windows. Toutefois, pas tous les propriétaires de bibliothèque de nœud/NPM ou Ruby Gem port leurs bibliothèques pour prendre en charge de Windows, et la plupart ont des dépendances spécifiques à Linux. Cela peut parfois produire des systèmes créés à l’aide de ces outils et les bibliothèques rencontre de build et parfois des erreurs d’exécution ou des comportements indésirables sur Windows.

Voici quelques-uns des problèmes qui ont provoqué des autres personnes à demander de Microsoft pour améliorer les outils de ligne de commande des Windows et ce qui nous a conduit à un partenariat avec Canonical pour activer les outils de ligne de commande Bash et Linux natifs pour s’exécuter sur Windows.

## <a name="what-does-this-mean-for-powershell"></a>Que cela signifie pour PowerShell ?
Lorsque vous travaillez avec les projets Open source, sont nombreux scénarios où il est extrêmement utile pour le déposer dans Bash à partir d’un PowerShell prompt. Prise en charge de l’interpréteur de commandes est complémentaire et renforce la valeur de la ligne de commande sur Windows, ce qui permet de PowerShell et la Communauté PowerShell pour tirer parti des autres technologies les plus courants.

En savoir plus sur le blog de l’équipe PowerShell-- [Bash pour Windows : Pourquoi c’est génial et ce que cela signifie pour PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>Puis-je exécuter Linux toutes les applications dans WSL ?
non ! WSL est un outil visant à permettre aux utilisateurs qui en ont besoin pour exécuter l’interpréteur de commandes et outils de ligne de commande de Linux sur Windows core. 

WSL est **pas** visent à prendre en charge des postes de travail de l’interface graphique utilisateur ou des applications (par exemple, Gnome, KDE, etc.)  

En outre, même si vous serez en mesure d’exécuter de nombreuses applications serveur les plus courants (par exemple, Redis), nous ne recommandons pas WSL pour l’hébergement des services de production, Microsoft propose un large éventail de solutions pour l’exécution des charges de travail Linux de production dans Azure, Hyper-V et Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>Les références (SKU) Windows WSL est inclus dans ?
Sous-système Windows pour Linux est disponible sur la bureau Windows pour Windows 10 anniversaire et les créateurs de mise à jour ou version ultérieure.

À compter de la Fall Creators update WSL sera disponible sur le bureau et le serveur de références (SKU) de Windows.

## <a name="what-processors-does-wsl-support"></a>Quels processeurs WSL prend en charge ?
WSL prend en charge x64 et les processeurs ARM.

## <a name="how-do-i-access-my-c-drive"></a>Comment accéder à mon lecteur C: ?
Points de montage pour les disques durs sur l’ordinateur local sont automatiquement créées et fournissent un accès facile au système de fichiers Windows. 
 
**/Mnt/\<lettre de lecteur > /**
 
Exemple d’utilisation `cd /mnt/c` pour accéder aux c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Comment utiliser un fichier Windows avec une application Linux ?

Un des avantages de WSL est de pouvoir accéder à vos fichiers via les applications Windows et Linux ou d’outils. 

WSL monte les lecteurs fixes de votre ordinateur sous le `/mnt/<drive>` dossier dans vos distributions Linux. Par exemple, votre `C:` lecteur est monté sous `/mnt/c/` 

Vos lecteurs montés, vous pouvez modifier le code, par exemple, `C:\dev\myproj\` à l’aide de [Visual Studio](https://visualstudio.microsoft.com/vs/) / ou [VS Code](https://code.visualstudio.com/)et que le code de Linux de génération/test en accédant aux mêmes fichiers via `\mnt\c\dev\myproj`.

> **REMARQUE IMPORTANTE**: Les principales limitations de l’utilisation de WSL est que l’accès à/modifier directement les fichiers du système de fichiers des vos distributions Linux à l’aide d’applications de Windows ou d’outils n’est pas pris en charge. Consultez : [Ne modifiez pas les fichiers de Linux à l’aide des outils et applications de Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Les fichiers sont dans le lecteur de Linux différents à partir du lecteur monté Windows ?

1. Fichiers sous la racine de Linux (par exemple, `/`) sont contrôlées par WSL qui reproduit le comportement spécifique de Linux, y compris mais sans limitation :
   * Fichiers qui contiennent des caractères de nom de fichier Windows non valides
   * Liens symboliques créé pour les utilisateurs non administrateurs
   * Modification des attributs de fichier via chmod et chown
   * Respecte la casse de fichier/dossier

2. Fichiers dans les lecteurs montés sont contrôlées par Windows et ont les comportements suivants :
   * Prise en charge de la casse
   * Toutes les autorisations sont définies pour mieux refléter les autorisations Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Pourquoi y a-t-il tant d’erreurs lors de l’exécution de la mise à niveau d’apt-get ?
Certains packages utilisent les fonctionnalités que nous n’avons pas encore implémentée. `udev`, par exemple, n’est pas encore pris en charge et empêche plusieurs `apt-get upgrade` erreurs.

Pour résoudre les problèmes liés à `udev`, suivez les étapes suivantes :

1. Écrivez le code suivant à `/usr/sbin/policy-rc.d` et enregistrez vos modifications.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Ajouter des autorisations d’exécution `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Exécutez les commandes suivantes

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Comment désinstaller une Distribution WSL ?

Sur les builds avant 1709 (16299) Ouvrez une invite de commandes et exécutez :
  ```batchfile
  lxrun /uninstall /full
  ```
  
Distributions WSL installées à partir du magasin peuvent être désinstallées comme toute autre application Windows, en cliquant sur la vignette de l’application et en cliquant sur la désinstallation, ou via PowerShell en utilisant le [ `Remove-AppxPackage` applet de commande](https://technet.microsoft.com/en-us/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>Pourquoi ping ne génère pas les erreurs de refus des autorisations ?
WSL builds < 14926, ping requis WSL exécuter via une Console avec élévation de privilèges. Ce problème a été résolu dans 14926 Build et version ultérieure.

## <a name="how-do-i-run-an-openssh-server"></a>Comment exécuter un serveur OpenSSH ?
Privilèges d’administrateur dans Windows sont requis pour exécuter OpenSSH dans WSL. Pour exécuter un serveur OpenSSH, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite CMD/PowerShell avec des privilèges d’administrateur.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>Pourquoi reçois-je « erreur : 0x80040306 » lorsque j’essaie d’installer ?
WSL ne prend pas en charge en cours d’exécution dans une console héritée. Pour désactiver l’ancienne console :

1. Ouvrez WSL, PowerShell ou Cmd
1. Cliquez avec le bouton droit sur titre de la barre -> Propriétés -> Décochez « Utiliser l’ancienne console »
1. Cliquez sur OK

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Pourquoi reçois-je « erreur : 0 x 80040154 » lors de l’exécution bash.exe après la mise à niveau de Windows ?
La fonctionnalité de « Sous-système Windows pour Linux » peut être désactivée pendant une mise à jour de Windows. Dans ce cas, la fonctionnalité de Windows doit être réactivée. Vous trouverez des instructions pour activer la fonctionnalité « Sous-système Windows pour Linux » dans le [Guide d’Installation](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Comment modifier la langue d’affichage de WSL ?
Installation WSL tente de modifier automatiquement les paramètres régionaux Ubuntu pour faire correspondre les paramètres régionaux de votre installation de Windows. Si vous ne souhaitez pas ce comportement, vous pouvez exécuter cette commande pour modifier les paramètres régionaux Ubuntu, une fois l’installation terminée. Vous devez relancer bash.exe pour que cette modification prenne effet.

Le ci-dessous exemple modifie les paramètres régionaux en-US :
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>Pourquoi avez pas accès à internet à partir de WSL ?
Certains utilisateurs ont signalé des problèmes avec les applications de pare-feu spécifiques bloque l’accès internet dans WSL. Les pare-feux signalés sont :

1. Kaspersky
1. AVG
1. Avast

Dans certains cas désactiver le pare-feu autorise l’accès. Dans certains cas le simple fait d’avoir le pare-feu installé recherche pour bloquer l’accès.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Comment accéder à un port à partir de WSL dans Windows ?
WSL partage l’adresse IP de Windows, comme il s’exécute sur Windows. Par conséquent vous pouvez accéder à tous les ports sur l’hôte local par exemple, si vous aviez un contenu web sur le port 1234, vous pourriez https://localhost:1234 dans votre navigateur Windows.

## <a name="where-can-i-provide-feedback"></a>Où puis-je fournir des commentaires ?

Vous pouvez partager vos commentaires et poser des questions via plusieurs canaux : Commentaires et questions doivent être orientées vers :
* Notre [suivi des problèmes GitHub](https://github.com/Microsoft/BashOnWindows/issues)
* Notre [de ligne de commande portail UserVoice](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Notre [blog de l’équipe de ligne de commande](https://blogs.msdn.microsoft.com/commandline/)
* Via Twitter. Veuillez suivre [ @richturn_ms ](https://twitter.com/richturn_MS) sur Twitter pour découvrir de nouvelles, mises à jour, etc.
