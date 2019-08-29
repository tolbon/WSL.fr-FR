---
title: Forum Aux Questions (FAQ)
description: Forum aux questions sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, Forum aux questions
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122762"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Forum aux questions sur le sous-système Windows pour Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Qu’est-ce que le sous-système Windows pour Linux (WSL)?
Le sous-système Windows pour Linux (WSL) est une nouvelle fonctionnalité de Windows 10 qui vous permet d’exécuter des outils en ligne de commande Linux natifs directement sur Windows, en même temps que votre bureau Windows traditionnel et vos applications modernes Store.

Pour plus d’informations, consultez la [page à propos](./about.md) .

## <a name="who-is-wsl-for"></a>À qui s’WSL?
Il s’agit principalement d’un outil destiné aux développeurs, en particulier les développeurs Web et ceux qui travaillent sur ou avec des projets open source. Cela permet à ceux qui souhaitent/doivent utiliser bash, les outils Linux courants`sed`( `awk`,, etc.) et de nombreux outils Linux (Ruby, Python, etc.) d’utiliser leurs chaîne d’outils sur Windows.

## <a name="what-can-i-do-with-wsl"></a>Que puis-je faire avec WSL?
WSL fournit une application appelée bash. exe qui, lorsqu’elle est démarrée, ouvre une console Windows exécutant l’interpréteur de commandes bash. Si vous utilisez bash, vous pouvez exécuter des applications et des outils Linux en ligne de commande. Par exemple, tapez `lsb_release -a` et appuyez sur entrée. vous verrez les détails de la distribution Linux en cours d’exécution:

![Capture d’écran des détails de distribution](media/distro.png)

Vous pouvez également accéder au système de fichiers de votre ordinateur local à partir de l’interpréteur de commandes bash Linux. vous trouverez `/mnt` vos lecteurs locaux montés sous le dossier. Par exemple, votre `C:` lecteur est monté sous `/mnt/c`:  

![Capture d’écran du lecteur C monté](media/ls.png)

## <a name="what-is-bash"></a>Qu’est-ce que bash?
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) est un interpréteur de commandes textuel et un langage de commande populaires. Il s’agit de l’interpréteur de commandes par défaut inclus dans Ubuntu et d’autres distributions Linux, et dans macOS. Les utilisateurs tapent des commandes dans un interpréteur de commandes pour exécuter des scripts et/ou exécuter des commandes et des outils pour accomplir de nombreuses tâches.

## <a name="how-does-this-work"></a>Comment cela fonctionne-t-il ?
Consultez notre [blog](https://blogs.msdn.microsoft.com/wsl/) pour en savoir plus sur la technologie sous-jacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>Pourquoi utiliser WSL plutôt que Linux sur une machine virtuelle?
WSL requiert moins de ressources (processeur, mémoire et stockage) qu’une machine virtuelle complète. WSL vous permet également d’exécuter des applications et des outils en ligne de commande Linux avec vos applications de ligne de commande, de bureau et de Windows Store, et d’accéder à vos fichiers Windows à partir de Linux. Cela vous permet d’utiliser des applications Windows et des outils en ligne de commande Linux sur le même jeu de fichiers, si vous le souhaitez.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>Pourquoi utiliser, par exemple, Ruby sur Linux plutôt que sur Windows?
Certains outils multiplateformes ont été créés en supposant que l’environnement dans lequel ils s’exécutent se comporte comme Linux. Par exemple, certains outils partent du principe qu’ils sont en mesure d’accéder à des chemins de fichiers très longs ou que des fichiers/dossiers spécifiques existent. Cela provoque souvent des problèmes sur Windows qui se comportent souvent différemment de Linux.

De nombreux langages tels que Ruby et Node sont souvent portés sur Windows et s’exécutent bien. Toutefois, tous les propriétaires de la bibliothèque de nœuds Ruby ou node/NPM ne prennent pas en charge les bibliothèques pour la prise en charge de Windows, et beaucoup ont des dépendances spécifiques à Linux. Cela peut souvent aboutir à des systèmes créés à l’aide de ces outils et bibliothèques souffrant de la génération, parfois des erreurs d’exécution ou des comportements indésirables sur Windows.

Il s’agit là d’un certain nombre de problèmes qui ont conduit de nombreuses personnes à demander à Microsoft d’améliorer les outils en ligne de commande de Windows et ce qui nous a amené à être partenaire avec Canonical pour permettre aux outils de ligne de commande Linux et de l’interpréteur de commandes natifs de s’exécuter sur Windows.

## <a name="what-does-this-mean-for-powershell"></a>Qu’est-ce que cela signifie pour PowerShell?
Lors de l’utilisation de projets OSS, il existe de nombreux scénarios dans lesquels il est très utile de supprimer bash d’une invite PowerShell. Le support bash est complémentaire et renforce la valeur de la ligne de commande sur Windows, ce qui permet à PowerShell et à la communauté PowerShell de tirer parti d’autres technologies populaires.

Pour en savoir plus, consultez le blog de [l’équipe PowerShell-bash pour Windows: Pourquoi c’est génial et ce qu’il signifie pour PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>Puis-je exécuter toutes les applications Linux dans WSL?
º! WSL est un outil destiné à permettre aux utilisateurs qui en ont besoin d’exécuter des outils en ligne de commande Linux bash et Core sur Windows. 

WSL n’a **pas** pour but de prendre en charge les applications ou les ordinateurs de bureau GUI (par exemple, GNOME, KDE, etc.)  

En outre, même si vous êtes en mesure d’exécuter de nombreuses applications serveur populaires (par exemple, Redims), nous vous déconseillons de WSL pour l’hébergement des services de production. Microsoft propose une variété de solutions pour l’exécution des charges de travail Linux de production dans Azure, Hyper-V et docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>À quelles références Windows WSL est-il inclus?
Le sous-système Windows pour Linux est disponible sur la version bureau de Windows pour Windows 10 anniversaire et Creators Update ou version ultérieure.

À partir de l’automne, les créateurs de mise à jour WSL seront disponibles sur les éditions bureau et serveur de Windows.

## <a name="what-processors-does-wsl-support"></a>Quels sont les processeurs pris en charge par WSL?
WSL prend en charge les processeurs x64 et ARM.

## <a name="how-do-i-access-my-c-drive"></a>Comment faire accéder au lecteur C:?
Les points de montage pour les disques durs sur l’ordinateur local sont créés automatiquement et offrent un accès facile au système de fichiers Windows. 
 
**lettre\<de lecteur/mnt/>/**
 
L’exemple `cd /mnt/c` d’utilisation serait d’accéder à c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Comment faire utiliser un fichier Windows avec une application Linux?

L’un des avantages de WSL est la possibilité d’accéder à vos fichiers via des applications ou des outils Windows et Linux. 

WSL monte les lecteurs fixes de votre ordinateur dans le `/mnt/<drive>` dossier de votre distributions Linux. Par exemple, votre `C:` lecteur est monté sous`/mnt/c/` 

À l’aide de vos lecteurs montés, vous pouvez modifier le code `C:\dev\myproj\` dans, par exemple, à l’aide de [Visual Studio](https://visualstudio.microsoft.com/vs/) /ou [vs code](https://code.visualstudio.com/), et générer/tester ce code dans `/mnt/c/dev/myproj`Linux en accédant aux mêmes fichiers via.

> **REMARQUE IMPORTANTE**: L’une des principales limitations de l’utilisation de WSL est que l’accès direct ou à la modification de fichiers dans le système de fichiers de votre distributions Linux à l’aide d’applications ou d’outils Windows n’est pas pris en charge. Consultez : [Ne pas modifier les fichiers Linux à l’aide des outils et des applications Windows](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Les fichiers du lecteur Linux sont-ils différents du lecteur Windows monté?

1. Les fichiers sous la racine Linux (c.-à-d `/`.) sont contrôlés par WSL, ce qui imite le comportement spécifique de Linux, y compris mais sans s’y limiter:
   * Fichiers qui contiennent des caractères de nom de fichier Windows non valides
   * Liens symboliques créés pour les utilisateurs non-administrateurs
   * Modification des attributs de fichier via chmod et chown
   * Respect de la casse des fichiers/dossiers

2. Les fichiers des lecteurs montés sont contrôlés par Windows et présentent les comportements suivants:
   * Respect de la casse
   * Toutes les autorisations sont définies pour mieux refléter les autorisations Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Pourquoi existe-t-il un grand nombre d’Erreurs lorsque j’exécute la mise à niveau de apt-obtien?
Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées. `udev`, par exemple, n’est pas encore pris en `apt-get upgrade` charge et provoque plusieurs erreurs.

Pour résoudre les problèmes liés `udev`à, procédez comme suit:

1. Écrivez les éléments suivants `/usr/sbin/policy-rc.d` dans et enregistrez vos modifications.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Ajouter des autorisations d’exécution à`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. Exécutez les commandes suivantes

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Comment faire désinstaller une distribution WSL?

Sur les builds antérieures à 1709 (16299), ouvrez une invite de commandes et exécutez:
  ```batchfile
  lxrun /uninstall /full
  ```
  
Les distributions WSL installées à partir du magasin peuvent être désinstallées comme n’importe quelle autre application Windows, en cliquant avec le bouton droit sur la vignette de l’application, puis en cliquant sur désinstaller ou via PowerShell à l’aide de l' [ `Remove-AppxPackage` applet](https://technet.microsoft.com/en-us/library/hh856038.aspx)de commande.

## <a name="why-does-ping-generate-permission-denied-errors"></a>Pourquoi ping génère-t-il des erreurs de refus d’autorisation?
Dans WSL builds < 14926, effectuez un test ping requis pour l’exécution de WSL via une console avec élévation de privilèges. Ce problème a été résolu dans la build 14926 et versions ultérieures.

## <a name="how-do-i-run-an-openssh-server"></a>Comment faire exécuter un serveur OpenSSH?
Les privilèges d’administrateur dans Windows sont requis pour exécuter OpenSSH dans WSL. Pour exécuter un serveur OpenSSH, exécutez bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash. exe à partir d’une invite de commandes CMD/PowerShell avec des privilèges d’administrateur.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>Pourquoi est-ce que j’obtiens le message d’erreur: 0x80040306» lorsque j’essaie de procéder à l’installation?
WSL ne prend pas en charge l’exécution dans une console héritée. Pour désactiver la console héritée:

1. Ouvrez WSL, PowerShell ou cmd
1. Cliquez avec le bouton droit sur la barre de titre-propriétés de >-> décochez la case «utiliser la console héritée».
1. Cliquez sur OK

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Pourquoi est-ce que j’obtiens le message d’erreur: 0x80040154» lorsque j’exécute bash. exe après la mise à niveau de Windows?
La fonctionnalité «sous-système Windows pour Linux» peut être désactivée au cours d’une mise à jour de Windows. Dans ce cas, la fonctionnalité Windows doit être réactivée. Vous trouverez des instructions sur l’activation de la fonctionnalité «sous-système Windows pour Linux» dans le [Guide d’installation](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Comment faire modifier la langue d’affichage de WSL?
WSL install va tenter de modifier automatiquement les paramètres régionaux Ubuntu afin qu’ils correspondent aux paramètres régionaux de votre installation Windows. Si vous ne souhaitez pas ce comportement, vous pouvez exécuter cette commande pour modifier les paramètres régionaux Ubuntu une fois l’installation terminée. Vous devrez relancer bash. exe pour que cette modification prenne effet.

L’exemple ci-dessous passe de paramètres régionaux à en-US:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>Pourquoi n’avez-vous pas accès à Internet à partir de WSL?
Certains utilisateurs ont signalé des problèmes avec des applications de pare-feu spécifiques qui bloquent l’accès à Internet dans WSL. Les pare-feu signalés sont:

1. Kaspersky
1. AVG
1. Avast

Dans certains cas, la désactivation du pare-feu autorise l’accès. Dans certains cas, l’installation du pare-feu semble bloquer l’accès.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Comment faire accéder à un port à partir de WSL dans Windows?
WSL partage l’adresse IP de Windows, car elle s’exécute sous Windows. Par conséquent, vous pouvez accéder à n’importe quel port sur localhost, par exemple, si vous aviez du https://localhost:1234 contenu Web sur le port 1234, vous pouviez dans votre navigateur Windows.

## <a name="how-can-i-back-up-my-wsl-distros"></a>Comment puis-je sauvegarder mes WSL distributions?

La meilleure façon de sauvegarder vos distributions est disponible dans la version 1809 et les versions ultérieures de Windows. Vous pouvez exporter l’intégralité de votre distribution vers un tarball `wsl --export` à l’aide de la commande. Vous pouvez ensuite importer ce distribution dans WSL à l’aide `wsl --import` de la commande, ce qui vous permet de sauvegarder et d’enregistrer les États de vos distributions WSL. 

Notez que les services de sauvegarde traditionnels qui sauvegardent les fichiers de vos dossiers AppData (comme la sauvegarde Windows) n’endommageront pas vos fichiers Linux. 



## <a name="where-can-i-provide-feedback"></a>Où puis-je fournir des commentaires?

Vous pouvez partager vos commentaires et poser des questions sur plusieurs canaux: Les commentaires et les questions doivent être dirigés vers:
* Notre [suivi des problèmes GitHub](https://github.com/Microsoft/BashOnWindows/issues)
* Notre [portail UserVoice en ligne de commande](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* Notre [blog de l’équipe en ligne de commande](https://blogs.msdn.microsoft.com/commandline/)
* Via Twitter. Veuillez suivre [@richturn_ms](https://twitter.com/richturn_MS) sur Twitter pour en savoir plus sur les actualités, les mises à jour, etc.
