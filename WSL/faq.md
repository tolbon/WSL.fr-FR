---
title: Forum Aux Questions (FAQ)
description: Forum aux questions sur le sous-système Windows pour Linux.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, FAQ
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 3c3681b0e0e8317917b4ec7c37c9bb2f0bbe9c95
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343898"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Forum aux questions sur le sous-système Windows pour Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Qu’est-ce que le sous-système Windows pour Linux (WSL) ?

Le sous-système Windows pour Linux (WSL) est une nouvelle fonctionnalité Windows 10 qui vous permet d’exécuter des outils en ligne de commande Linux natifs directement sur Windows, parallèlement à vos applications Windows de bureau classiques et du Store modernes.

Pour plus d’informations, consultez la [page À propos de](./about.md).

## <a name="who-is-wsl-for"></a>À qui WSL s’adresse-t-il ?

Il s’agit principalement d’un outil destiné aux développeurs, en particulier les développeurs web et ceux qui travaillent sur des projets open source ou les utilisent. Il permet à ceux qui souhaitent/doivent utiliser Bash, les outils Linux courants (`sed`, `awk`, etc.) et de nombreux premiers outils Linux (Ruby, Python, etc.) d’utiliser leur chaîne d’outils sur Windows.

## <a name="what-can-i-do-with-wsl"></a>Qu’est-ce que WSL me permet de faire ?

WSL fournit une application appelée Bash.exe qui, lorsqu’elle est démarrée, ouvre une console Windows exécutant l’interpréteur de commandes Bash. Bash vous permet d’exécuter des applications et des outils Linux en ligne de commande. Par exemple, tapez `lsb_release -a` et appuyez sur Entrée ; vous verrez les détails de la distribution Linux en cours d’exécution :

![Capture d’écran des détails de distribution](media/distro.png)

Vous pouvez également accéder au système de fichiers de votre ordinateur local à partir de l’interpréteur de commandes Bash Linux ; vous trouverez vos lecteurs locaux montés sous le dossier `/mnt`. Par exemple, votre lecteur `C:` est monté sous `/mnt/c` :  

![Capture d’écran du lecteur C monté](media/ls.png)

## <a name="what-is-bash"></a>Qu’est-ce que Bash ?

[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) est un interpréteur de commandes texte et un langage de commandes connues. Il s’agit de l’interpréteur de commandes par défaut inclus dans Ubuntu et d’autres distributions Linux ainsi que dans macOS. Les utilisateurs tapent des commandes dans un interpréteur de commandes pour exécuter des scripts et/ou des commandes et des outils pour accomplir de nombreuses tâches.

## <a name="how-does-this-work"></a>Comment cela fonctionne ?

Consultez notre [blog](https://blogs.msdn.microsoft.com/wsl/) pour en savoir plus sur la technologie sous-jacente.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>Pourquoi utiliser WSL plutôt que Linux dans une machine virtuelle ?

WSL demande moins de ressources (processeur, mémoire et stockage) qu’une machine virtuelle complète. WSL vous permet également d’exécuter des applications et des outils en ligne de commande Linux avec vos applications Windows en ligne de commande, de bureau et du Store, et d’accéder à vos fichiers Windows à partir de Linux. Cela vous permet d’utiliser des applications Windows et des outils en ligne de commande Linux sur le même ensemble de fichiers si vous le souhaitez.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>Pourquoi utiliser, par exemple, Ruby sur Linux plutôt que sur Windows ?

Certains outils multiplateformes ont été créés en supposant que l’environnement dans lequel ils s’exécutent se comporte comme Linux. Par exemple, certains outils partent du principe qu’ils sont en mesure d’accéder à des chemins de fichiers très longs ou que des fichiers/dossiers spécifiques existent. Cela provoque parfois des problèmes sur Windows qui se comporte souvent différemment de Linux.

De nombreux langages comme Ruby et Node sont souvent portés sur Windows et s’y exécutent très bien. Toutefois, les propriétaires de bibliothèques Ruby Gem ou Node/NPM ne portent pas tous leurs bibliothèques pour la prise en charge de Windows, et beaucoup ont des dépendances spécifiques à Linux. Cela peut souvent aboutir à des systèmes créés à l’aide de ces outils et bibliothèques qui font l’objet d’erreurs de build et parfois d’exécution ou de comportements indésirables sur Windows.

Il s’agit là de quelques-uns des problèmes qui ont conduit de nombreuses personnes à demander à Microsoft d’améliorer les outils en ligne de commande Windows et ce qui nous a amené à collaborer avec Canonical pour permettre aux outils en ligne de commande Linux et Bash natifs de s’exécuter sur Windows.

## <a name="what-does-this-mean-for-powershell"></a>Qu’est-ce que cela signifie pour PowerShell ?

Lors de l’utilisation de projets OSS, il existe de nombreux scénarios dans lesquels il est très utile de passer à Bash à partir d’une invite PowerShell. La prise en charge de Bash est complémentaire et valorise davantage la ligne de commande sur Windows, ce qui permet à PowerShell et à la communauté PowerShell de tirer parti d’autres technologies répandues.

Pour en savoir plus, accédez au blog de l’équipe PowerShell : [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>Puis-je exécuter TOUTES les applications Linux dans WSL ?

Non ! WSL est un outil destiné à permettre aux utilisateurs qui en ont besoin d’exécuter les principaux outils en ligne de commande Linux et Bash sur Windows.

WSL n’a **pas** pour but de prendre en charge les applications ou les ordinateurs de bureau GUI (par exemple, GNOME, KDE, etc.)  

De plus, même si vous pouvez exécuter de nombreuses applications serveur connues (par exemple, Redis), nous vous déconseillons WSL pour l’hébergement des services de production. Microsoft propose diverses solutions pour l’exécution des charges de travail Linux de production dans Azure, Hyper-V et Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>Dans quelles références SKU se trouve Windows WSL ?

Le sous-système Windows pour Linux est disponible sur la version bureau de Windows pour Mise à jour anniversaire Windows 10 et Windows 10 Creators Update ou version ultérieure.

À partir de Fall Creators Update, WSL sera disponible à la fois sur les références SKU bureau et serveur de Windows.

## <a name="what-processors-does-wsl-support"></a>Quels sont les processeurs pris en charge par WSL ?

WSL prend en charge les processeurs x64 et ARM.

## <a name="how-do-i-access-my-c-drive"></a>Comment accéder à mon lecteur C: ?

Des points de montage pour les disques durs sur l’ordinateur local sont créés automatiquement et offrent un accès facile au système de fichiers Windows.

**/mnt/\<lettre de lecteur>/**

Un exemple d’utilisation serait `cd /mnt/c` pour accéder à c:\

## <a name="how-do-i-set-up-git-credential-manager-how-do-i-use-my-windows-git-permissions-in-wsl"></a>Comment configurer Git Credential Manager ? (Comment utiliser mes autorisations Windows Git dans WSL ?) 

Git Credential Manager vous permet d’authentifier un serveur Git distant, même si vous disposez d’un modèle d’authentification complexe comme Azure Active Directory ou une authentification à deux facteurs. Git Credential Manager s’intègre au flux d’authentification des services tels que GitHub et, une fois que vous êtes authentifié auprès de votre fournisseur d’hébergement, demande un nouveau jeton d’authentification. Il stocke ensuite le jeton de façon sécurisée dans le gestionnaire d’informations d’identification Windows. Après la première fois, vous pouvez utiliser Git pour communiquer avec votre fournisseur d’hébergement sans avoir à vous réauthentifier. Il accède simplement au jeton dans le gestionnaire d’informations d’identification Windows.

Pour configurer Git Credential Manager en vue de l’utiliser avec une distribution WSL, ouvrez votre distribution et entrez cette commande :

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

À présent, toute opération git que vous effectuez dans votre distribution WSL utilise le gestionnaire d’informations d’identification. Si vous avez déjà mis en cache les informations d’identification d’un hôte, celui-ci y accède à partir du gestionnaire d’informations d’identification. Si ce n’est pas le cas, vous recevez une réponse de boîte de dialogue demandant vos informations d’identification, même si vous êtes dans une console Linux.

Cette prise en charge s’appuie sur l’[interopérabilité entre le sous-système Windows pour Linux et Windows lui-même](https://docs.microsoft.com/windows/wsl/interop).

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Comment utiliser un fichier Windows avec une application Linux ?

L’un des avantages de WSL est la possibilité d’accéder à vos fichiers via des applications ou des outils Windows et Linux. 

WSL monte les lecteurs fixes de votre ordinateur sous le dossier `/mnt/<drive>` de vos distributions Linux. Par exemple, votre lecteur `C:` est monté sous `/mnt/c/`

À l’aide de vos lecteurs montés, vous pouvez modifier le code dans, par exemple, `C:\dev\myproj\` à l’aide de [Visual Studio](https://visualstudio.microsoft.com/vs/) /ou [VS Code](https://code.visualstudio.com/) et générer/tester ce code dans Linux en accédant aux mêmes fichiers via `/mnt/c/dev/myproj`.

> **REMARQUE IMPORTANTE** : L’une des principales limitations de l’utilisation de WSL est que l’accès direct aux fichiers ou leur modification dans le système de fichiers des distributions Linux à l’aide d’applications ou d’outils Windows n’est pas pris en charge. Voir : [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Les fichiers du lecteur Linux sont-ils différents du lecteur Windows monté ?

1. Les fichiers sous la racine Linux (autrement dit, `/`) sont contrôlés par WSL, ce qui reproduit le comportement spécifique de Linux, notamment mais sans s’y limiter :
   * Fichiers qui contiennent des caractères de nom de fichier Windows non valides
   * Liens symboliques créés pour les utilisateurs non-administrateurs
   * Changement des attributs de fichier via chmod et chown
   * Respect de la casse des fichiers/dossiers

2. Les fichiers des lecteurs montés sont contrôlés par Windows et présentent les comportements suivants :
   * Prise en charge du respect de la casse
   * Toutes les autorisations sont définies pour mieux refléter les autorisations Windows

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Pourquoi autant d’erreurs sont retournées quand j’exécute apt-get upgrade ?

Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées. `udev`, par exemple, n’est pas encore pris en charge et provoque plusieurs erreurs avec `apt-get upgrade`.

Pour résoudre les problèmes liés à `udev`, procédez comme suit :

1. Écrivez le code suivant dans `/usr/sbin/policy-rc.d` et enregistrez vos modifications.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Ajoutez des autorisations d’exécution à `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
3. Exécutez les commandes suivantes

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Comment désinstaller une distribution WSL ?

Sur les builds antérieures à 1709 (16299), ouvrez une invite de commandes et exécutez :

  ```batchfile
  lxrun /uninstall /full
  ```
  
Les distributions WSL installées à partir du Store peuvent être désinstallées comme n’importe quelle autre application Windows, en cliquant avec le bouton droit sur la vignette de l’application et en cliquant sur Désinstaller ou via PowerShell à l’aide de l’[`Remove-AppxPackage`applet de commande ](https://technet.microsoft.com/library/hh856038.aspx).

## <a name="why-does-ping-generate-permission-denied-errors"></a>Pourquoi la commande ping génère des erreurs d’autorisation refusée ?

Dans les builds WSL antérieures à 14926, l’exécution de la commande ping via une console avec élévation de privilèges nécessitait WSL. Ce problème a été résolu dans la build 14926 et ultérieur.

## <a name="how-do-i-run-an-openssh-server"></a>Comment exécuter un serveur OpenSSH ?

L’exécution d’un serveur OpenSSH dans WSL nécessite des privilèges d’administrateur dans Windows. Pour exécuter un serveur OpenSSH, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite de commandes CMD/PowerShell avec des privilèges d’administrateur.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>Pourquoi est-ce que je reçois « Erreur : 0x80040306 » pendant l’installation ?

WSL ne prend pas en charge l’exécution dans une console héritée. Pour désactiver la console héritée :

1. Ouvrez WSL, PowerShell ou Cmd
1. Cliquez avec le bouton droit sur la barre de titre, sélectionnez Propriétés, puis décochez Utiliser la console héritée
1. Cliquez sur OK

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Pourquoi est-ce que je reçois « Erreur : 0x80040154 » quand j’exécute bash.exe après la mise à niveau de Windows ?

La fonctionnalité Sous-système Windows pour Linux peut être désactivée au cours d’une mise à jour de Windows. Dans ce cas, la fonctionnalité Windows doit être réactivée. Pour obtenir des instructions sur l’activation de la fonctionnalité Sous-système Windows pour Linux, consultez le [guide d’installation](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Comment changer la langue d’affichage de WSL ?

Le processus d’installation de WSL tente de changer automatiquement les paramètres régionaux d’Ubuntu de sorte qu’ils correspondent à ceux de votre installation Windows. Si vous souhaitez éviter ce comportement, vous pouvez exécuter cette commande pour changer les paramètres régionaux d’Ubuntu une fois l’installation terminée. Vous devrez relancer bash.exe pour que ce changement prenne effet.

L’exemple ci-dessous applique les paramètres régionaux en-US :

```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>Pourquoi est-ce que je n’ai pas d’accès Internet à partir de WSL ?

Des utilisateurs ont signalé des problèmes posés par certaines applications de pare-feu, qui bloquent l’accès Internet dans WSL. Les pare-feux signalés sont :

1. Kaspersky
1. AVG
1. Avast

Dans certains cas, la désactivation du pare-feu permet d’obtenir l’accès. Parfois, il semble que la simple installation du pare-feu bloque l’accès.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Comment accéder à un port à partir de WSL dans Windows ?
WSL partage l’adresse IP de Windows, car il s’exécute sur Windows. Par conséquent, vous pouvez accéder à n’importe quel port sur localhost ; par exemple, si vous avez du contenu web sur le port 1234, vous pouvez utiliser https://localhost:1234 dans votre navigateur Windows.

## <a name="how-can-i-back-up-my-wsl-distros-or-move-them-from-one-drive-to-another"></a>Comment sauvegarder mes distributions WSL ou les déplacer d’un lecteur à un autre ?

La meilleure façon de sauvegarder ou de déplacer vos distributions consiste à utiliser les commandes d’exportation/importation disponibles dans Windows version 1809 et ultérieure. Vous pouvez exporter l’intégralité de votre distribution vers un tarball à l’aide de la commande `wsl --export`. Vous pouvez ensuite réimporter cette distribution dans WSL à l’aide de la commande `wsl --import`, ce qui peut nommer un nouvel emplacement de lecteur pour l’importation. Vous pouvez ainsi sauvegarder et enregistrer les états de vos distributions WSL, ou déplacer ces dernières. 

Notez que les services de sauvegarde classiques qui sauvegardent les fichiers dans vos dossiers Appdata (comme la sauvegarde Windows) n’endommageront pas vos fichiers Linux.

## <a name="where-can-i-provide-feedback"></a>Où puis-je envoyer des commentaires ?

Vous pouvez partager vos commentaires et poser vos questions via plusieurs canaux.

Si vous rencontrez des problèmes techniques ou si vous voulez demander de nouvelles fonctionnalités, accédez à notre suivi des problèmes Github :

* [Outil de suivi des problèmes GitHub](https://github.com/Microsoft/BashOnWindows/issues)

Si vous voulez rester informé des dernières informations sur WSL, vous pouvez le faire sur :

* Notre [blog de l’équipe sur les lignes de commande](https://blogs.msdn.microsoft.com/commandline/)
* Twitter. Suivez [@craigaloewen](https://twitter.com/craigaloewen) sur Twitter pour être averti des nouveautés, mises à jour, etc.
