---
title: Notes de version de sous-système Windows pour Linux
description: Notes de publication pour le sous-système Windows pour Linux.  Mise à jour chaque semaine.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988260"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notes de version de sous-système Windows pour Linux

## <a name="build-18890"></a>Build 18890
Pour Windows général plus d’informations sur la build 18890 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Fuite de socket non bloquant [GH 2913]
* Entrée EOF à Terminal Server peut bloquer les lectures suivantes [GH 3421]
* Mettre à jour resolv.conf en-tête pour faire référence à wsl.conf [abordées dans GH 3928]
* Interblocage dans du code de suppression epoll [GH 3922]
* Gérer les espaces dans les arguments à--importer et – exporter [GH 3932]
* Extension mmap des fichiers ne fonctionne pas correctement [GH 3939]
* Résoudre un problème avec ARM64 \\accès de $ wsl ne fonctionne ne pas correctement
* Ajouter une meilleure icône par défaut pour wsl.exe

## <a name="build-18342"></a>Build 18342
Pour Windows général plus d’informations sur la build 18342 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans une distribution WSL à partir de Windows. Ces fichiers sont accessibles via la ligne de commande et également des applications Windows, comme l’Explorateur de fichiers, VSCode, etc. peuvent interagir avec ces fichiers. Accéder à vos fichiers en accédant à \\ \\wsl$\\< distro_name >, ou afficher la liste des distributions en cours d’exécution en accédant à \\ \\wsl$
* Ajouter des balises d’informations supplémentaires du processeur et de corriger les valeurs de Cpus_allowed [_liste] [GH 2234]
* Prend en charge exec de thread non leader [GH 3800]
* Traiter les échecs de mise à jour de configuration comme non irrécupérable [GH 3785]
* Mettre à jour binfmt pour gérer correctement les décalages [GH 3768]
* Activer le mappage des lecteurs réseau pour planifier 9 [GH 3854]
* Prise en charge Windows -> Linux et Linux -> traduction de chemin d’accès Windows pour les montages de liaisons
* Créer des sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule

## <a name="build-18334"></a>Build 18334
Pour Windows général plus d’informations sur la build 18334 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Redéfinir la façon que le fuseau horaire de Windows est mappé à un fuseau horaire de Linux [GH 3747]
* Corriger les fuites de mémoire et ajouter de nouvelles fonctions de traduction de chaîne [GH 3746]
* SIGCONT sur un threadgroup avec aucun thread n’est une absence d’opération [GH 3741] 
* Afficher correctement les descripteurs de fichier socket et epoll /proc/self/fd

## <a name="build-18305"></a>Build 18305
Pour Windows général plus d’informations sur la build 18305 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads perdre l’accès aux fichiers quand le thread principal s’arrête [GH 3589]
* TIOCSCTTY doit ignorer le paramètre « force », sauf si elle est nécessaire [GH 3652]
* améliorations de ligne de commande wsl.exe et ajout d’importation / exportation de fonctionnalités.
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a>Build 18277
Pour Windows général plus d’informations sur la build 18277 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Corriger l’erreur « interface non pris en charge » introduit dans la version 18272 [GH 3645]
* Ignorer l’indicateur MNT_FORCE pour syscall unmount [GH 3605]
* Interopérabilité WSL de commutateur à utiliser l’API CreatePseudoConsole officiel
* Mettre à jour aucune valeur de délai d’attente lorsque FUTEX_WAIT redémarre

## <a name="build-18272"></a>Build 18272
Pour Windows général plus d’informations sur la build 18272 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **AVERTISSEMENT :** Il existe un problème dans la génération qui rend WSL inutilisable. Lorsque vous tentez de lancer votre distribution, vous verrez une erreur « Interface non pris en charge ». Le problème a été résolu et sera dans la build de la semaine prochaine Insider rapide. Si vous avez installé cette build, vous pouvez revenir à la build précédente de Windows à l’aide de « Go revenir à la version précédente de Windows 10 » dans les paramètres -> mise à jour & sécurité -> Recovery.

## <a name="build-18267"></a>Build 18267
Pour Windows général plus d’informations sur la build 18267 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Corrigez le problème dans lequel les processus inactifs ne peuvent pas différentes et rester indéfiniment.
* WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]
* Autoriser fsync échoué pour les fichiers en lecture seule sur DrvFs [GH 3556]
* Vérifiez que les répertoires /bin et /sbin existent avant de créer des liens symboliques à l’intérieur de [GH 3584]
* Ajouter un mécanisme de délai d’attente d’arrêt instance pour les instances WSL. Le délai d’attente est actuellement définie sur 15 secondes, ce qui signifie que l’instance s’arrête dès que le dernier processus WSL quitte les 15 secondes. Pour mettre fin immédiatement à une distribution, utilisez :
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Build 17763 (1809)
Pour Windows général plus d’informations sur la build 17763 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Vérification des autorisations SetPriority syscall trop stricte pour modifier la priorité de thread même [GH 1838]
* Garantir que les temps d’interruption non biaisée est utilisé pour le démarrage pour éviter le renvoi des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Gérer les liens symboliques dans l’interpréteur de binfmt WSL [GH 3424]
* Meilleure gestion de nettoyage de descripteur de fichier de leader threadgroup.
* Commutateur WSL à utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter du afin d’éviter le dépassement de capacité [GH 3252]
* Ptrace attacher mai provoquer la mauvaise valeur de retour à partir des appels système [GH 1731]
* Correctif que relatif AF_UNIX plusieurs problèmes [GH 3371]
* Correction d’un problème qui provoquait interop WSL échoue si le répertoire de travail actuel est inférieur à 5 caractères [GH 3379]
* Éviter un délai deuxième échec des connexions de bouclage aux ports inexistant [GH 3286]
* Ajouter un fichier stub /proc/sys/fs/file-max [GH 2893]
* Informations de portée IPV6 plus précises.
* Prise en charge PR_SET_PTRACER [GH 3053]
* Canal de système de fichiers par inadvertance effacement epoll déclenchée par edge événement [GH 3276]
* Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]
* Prise en charge de zombie [GH 1353] améliorée
* Ajouter des entrées wsl.conf pour contrôler le comportement d’interopérabilité Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correctif pour getsockname pas toujours renvoyer le type de famille du socket UNIX [GH 1774]
* Ajouter la prise en charge pour TIOCSTI [GH 1863]
* Non bloquant de sockets en cours de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]
* Prendre en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]
* Corriger le problème sur le dossier racine [GH 3304] de vérification d’autorisation
* Prise en charge limitée TTY clavier ioctls KDGKBTYPE, KDGKBMODE et KDSKBMODE.
* Applications d’interface utilisateur Windows doivent s’exécuter même lorsque lancé en arrière-plan.
* Ajouter l’option -u ou--utilisateur wsl [GH 1203]
* Résoudre les problèmes de lancement WSL de démarrage rapide est activé [GH 2576]
* Sockets UNIX doivent conserver les informations d’identification homologue déconnectée [GH 3183]
* Sockets Unix de non bloquants indéfiniment échoué à cause d’EAGAIN [GH 3191]
* cas = off est de type [2937 GH 3212, 3328] de montage des nouvelle drvfs par défaut
    * Consultez [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) pour plus d’informations.
* Ajouter wslconfig / arrêter pour arrêter l’exécution des distributions.
* Résoudre les problème avec le contexte du shell WSL les entrées de menu qui ne gèrent pas correctement les chemins d’accès avec des espaces.
* Exposer par répertoire respecte la casse comme un attribut étendu
* ARM64 : Émuler des opérations de maintenance du cache. Résoudre [dotnet problème](https://github.com/dotnet/core/issues/1561).
* DrvFs : unescape uniquement des caractères dans la plage privées qui correspondent à un caractère d’échappement.
* Corriger désactivé par une erreur de validation de la longueur interpréteur ELF analyseur [GH 3154]
* Minuteurs d’absolu WSL avec une heure dans le passé ne déclenchent pas [GH 3091]
* Vérifiez qui vient d’être des points d’analyse créés sont répertoriés en tant que tel dans le répertoire parent.
* Créer atomiquement répertoires respecte la casse dans DrvFs.
* Correction d’un problème supplémentaire où les opérations multithread peut retourner ENOENT, même si le fichier existe. [GH 2712]
* Fixe WSL lancer échec lorsque UMCI est activé. [GH 3020]
* Ajouter un menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836]. Pour utiliser, maintenez la touche MAJ et avec le bouton droit dans une fenêtre d’Explorateur.
* Corriger le comportement Unix socket non bloquant [GH 2822, 3100]
* Correctif négatif de commande NETLINK comme indiqué dans GH 2026.
* Ajouter la prise en charge des indicateurs de propagation de montage [GH 2911].
* Résoudre le problème avec les événements inotify entraînant pas tronquer [GH 2978].
* Ajoutez--option exec pour wsl.exe appeler un fichier binaire unique sans un interpréteur de commandes.
* Ajoutez--option de distribution pour wsl.exe sélectionner une distribution spécifique.
* Prise en charge limitée dmesg. Les applications peuvent maintenant vous connecter à dmesg. Pilote WSL consigne des informations limitées dans dmesg. À l’avenir, cela peut être étendu pour effectuer d’autres informations/diagnostics à partir du pilote.
    * Remarque : dmesg actuellement pris en charge par le biais du `/dev/kmsg` interface de périphérique. `syslog` syscall interface n’est pas encore pris en charge. Et, par conséquent, certaines de la `dmesg` options de ligne de commande telles que `-S`, `-C` ne fonctionnent pas.
* Modifier les gid par défaut et périphériques série pour faire correspondre natif [GH 3042]
* DrvFs prend désormais en charge les attributs étendus.
    * Remarque: DrvFs présente certaines limitations sur le nom des attributs étendus. Certains caractères (comme '/', ' :' et '\*') ne sont pas autorisées et étendu les noms d’attributs ne sont pas sensible à la casse sur DrvFs

## <a name="build-18252-skip-ahead"></a>Build 18252 (passer à l’avance)
Pour Windows général plus d’informations sur la build 18252 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Déplacer des binaires init et bsdtar en dehors de la dll de lxssmanager et dans un dossier des outils distincts
* Corriger la concurrence autour de fermer le descripteur de fichier lors de l’utilisation de CLONE_FILES
* Gérer les champs facultatifs dans /proc/pid/mountinfo lors de la traduction des chemins d’accès DrvFs
* Autoriser mknod DrvFs de réussir sans prise en charge des métadonnées pour S_IFREG
* Fichiers en lecture seule créés sur DrvFs doivent avoir l’attribut en lecture seule définie [GH 3411]
* Ajouter d’assistance /sbin/mount.drvfs pour gérer le montage DrvFs
* Utilisez le changement de nom POSIX dans DrvFs.
* Permet la traduction de chemin d’accès sur les volumes sans GUID du volume.

## <a name="build-17738-fast"></a>Build 17738 (rapide)
Pour Windows général plus d’informations sur la build 17738 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Vérification des autorisations SetPriority syscall trop stricte pour modifier la priorité de thread même [GH 1838]
* Garantir que les temps d’interruption non biaisée est utilisé pour le démarrage pour éviter le renvoi des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Gérer les liens symboliques dans l’interpréteur de binfmt WSL [GH 3424]
* Meilleure gestion de nettoyage de descripteur de fichier de leader threadgroup.

## <a name="build-17728-fast"></a>Build 17728 (rapide)
Pour Windows général plus d’informations sur la build 17728 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Commutateur WSL à utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter du afin d’éviter le dépassement de capacité [GH 3252]
* Ptrace attacher mai provoquer la mauvaise valeur de retour à partir des appels système [GH 1731]
* Correctif que relatif d’un nombre de AF_UNIX émet [GH 3371]
* Correction d’un problème qui provoquait interop WSL échoue si le répertoire de travail actuel est inférieur à 5 caractères [GH 3379]

## <a name="build-18204-skip-ahead"></a>Build 18204 (passer à l’avance)
Pour Windows général plus d’informations sur la build 18204 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Diriger inadvertenly filesystem effacer événement epoll déclenchée par edge [GH 3276]
* Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]

## <a name="build-17723-fast"></a>Build 17723 (rapide)
Pour Windows général plus d’informations sur la build 17723 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Éviter un délai deuxième échec des connexions de bouclage aux ports inexistant [GH 3286]
* Ajouter un fichier stub /proc/sys/fs/file-max [GH 2893]
* Informations de portée IPV6 plus précises.
* Prise en charge PR_SET_PTRACER [GH 3053]
* Diriger inadvertenly filesystem effacer événement epoll déclenchée par edge [GH 3276]
* Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]

## <a name="build-17713"></a>Build 17713
Pour Windows général plus d’informations sur la build 17713 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Prise en charge de zombie [GH 1353] améliorée
* Ajouter des entrées wsl.conf pour contrôler le comportement d’interopérabilité Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correctif pour getsockname pas toujours renvoyer le type de famille du socket UNIX [GH 1774]
* Ajouter la prise en charge pour TIOCSTI [GH 1863]
* Non bloquant de sockets en cours de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]
* Prendre en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]
* Corriger le problème sur le dossier racine [GH 3304] de vérification d’autorisation
* Prise en charge limitée TTY clavier ioctls KDGKBTYPE, KDGKBMODE et KDSKBMODE.
* Applications d’interface utilisateur Windows doivent s’exécuter même lorsque lancé en arrière-plan.

## <a name="build-17704"></a>Build 17704
Pour Windows général plus d’informations sur la build 17704 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Ajouter l’option -u ou--utilisateur wsl [GH 1203]
* Résoudre les problèmes de lancement WSL de démarrage rapide est activé [GH 2576]
* Sockets UNIX doivent conserver les informations d’identification homologue déconnectée [GH 3183]
* Sockets Unix de non bloquants indéfiniment échoué à cause d’EAGAIN [GH 3191]
* cas = off est de type [2937 GH 3212, 3328] de montage des nouvelle drvfs par défaut
    * Consultez [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) pour plus d’informations.
* Ajouter wslconfig / arrêter pour arrêter l’exécution des distributions.

## <a name="build-17692"></a>Build 17692
Pour Windows général plus d’informations sur la build 17692 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Résoudre les problème avec le contexte du shell WSL les entrées de menu qui ne gèrent pas correctement les chemins d’accès avec des espaces.
* Exposer par répertoire respecte la casse comme un attribut étendu
* ARM64 : Émuler des opérations de maintenance du cache. Résoudre [dotnet problème](https://github.com/dotnet/core/issues/1561).
* DrvFs : unescape uniquement des caractères dans la plage privées qui correspondent à un caractère d’échappement.

## <a name="build-17686"></a>Build 17686
Pour Windows général plus d’informations sur la build 17686 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Corriger désactivé par une erreur de validation de la longueur interpréteur ELF analyseur [GH 3154]
* Minuteurs d’absolu WSL avec une heure dans le passé ne déclenchent pas [GH 3091]
* Vérifiez qui vient d’être des points d’analyse créés sont répertoriés en tant que tel dans le répertoire parent.
* Créer atomiquement répertoires respecte la casse dans DrvFs.

## <a name="build-17677"></a>Build 17677
Pour Windows général plus d’informations sur la build 17677 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Correction d’un problème supplémentaire où les opérations multithread peut retourner ENOENT, même si le fichier existe. [GH 2712]
* Fixe WSL lancer échec lorsque UMCI est activé. [GH 3020]

## <a name="build-17666"></a>Build 17666
Pour Windows général plus d’informations sur la build 17666 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>AVERTISSEMENT : Il existe un problème WSL empêche de s’exécuter sur certains chipsets AMD [GH 3134]. Un correctif est prêt et qu’il apporte sa méthode pour la branche de Build Insider.
* Ajouter un menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836]. Pour utiliser MAJ de blocage et avec le bouton droit dans une fenêtre d’Explorateur.
* Corriger le comportement unix socket non bloquant [GH 2822, 3100]
* Correctif négatif de commande NETLINK comme indiqué dans GH 2026.
* Ajouter la prise en charge des indicateurs de propagation de montage [GH 2911].
* Résoudre le problème avec les événements inotify entraînant pas tronquer [GH 2978].
* Ajoutez--option exec pour wsl.exe appeler un fichier binaire unique sans un interpréteur de commandes.
* Ajoutez--option de distribution pour wsl.exe sélectionner une distribution spécifique.

## <a name="build-17655-skip-ahead"></a>Build 17655 (passer à l’avance)
Pour Windows général plus d’informations sur la build 17655 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Prise en charge limitée dmesg. Les applications peuvent maintenant vous connecter à dmesg. Pilote WSL consigne des informations limitées dans dmesg. À l’avenir, cela peut être étendu pour effectuer d’autres informations/diagnostics à partir du pilote.
    * Remarque : dmesg actuellement pris en charge par le biais du `/dev/kmsg` interface de périphérique. `syslog` interface de sycall n’est pas encore pris en charge. Et, par conséquent, certaines de la `dmesg` options de ligne de commande telles que `-S`, `-C` ne fonctionnent pas.
* Correction d’un problème où les opérations multithread peut retourner ENOENT, même si le fichier existe. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Build 17639 (passer à l’avance)
Pour Windows général plus d’informations sur la build 17639 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Modifier les gid par défaut et périphériques série pour faire correspondre natif [GH 3042]
* DrvFs prend désormais en charge les attributs étendus.
    * Remarque: DrvFs présente certaines limitations sur le nom des attributs étendus. En particulier, certains caractères (comme '/', ' :' et '\*') ne sont pas autorisées et étendu les noms d’attributs ne sont pas sensible à la casse sur DrvFs

## <a name="build-17133-fast"></a>Build 17133 (rapide)
Pour Windows général plus d’informations sur la build 17133 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Correction d’un blocage dans WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Build 17128 (rapide)
Pour Windows général plus d’informations sur la build 17128 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Aucune

## <a name="build-17627-skip-ahead"></a>Build 17627 (passer à l’avance)
Pour Windows général plus d’informations sur la build 17627 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Ajouter la prise en charge pour les opérations prenant en charge les pi futex. [GH 1006]
    * Notez que les priorités ne sont pas actuellement une fonctionnalité WSL pris en charge par conséquent, il existe des limitations, mais l’utilisation standard doit être débloquée.
* Prise en charge des pare-feu Windows pour les processus WSL. [GH 1852]
    * Par exemple, pour autoriser la WSL python traite pour écouter sur n’importe quel port, utilisez la commande Windows élevée : ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respecter le shell par défaut de l’utilisateur lors de l’utilisation de wsl.exe. [GH 2372]
* Déclarer toutes les interfaces réseau ethernet. [GH 2996]
* Meilleure gestion du fichier de passwd endommagé. [GH 3001]

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17618-skip-ahead"></a>Build 17618 (passer à l’avance)
Pour Windows général plus d’informations sur la build 17618 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introduire une fonctionnalité pseudoconsole pour l’interopérabilité de NT [GH 988, 1366, 1433, 1542, 2370, 2406].
* Le mécanisme d’installation héritée (lxrun.exe) a été déconseillé. Le mécanisme pris en charge pour l’installation de distributions est via le Microsoft Store.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17110"></a>Build 17110
Pour Windows général plus d’informations sur la build 17110 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Autoriser /init à être arrêté à partir de Windows [GH 2928].
* DrvFs utilise désormais par répertoire respecte la casse par défaut (équivalent à la « cas = dir « option de montage).
    * À l’aide de « cas = force » (l’ancien comportement) requiert la définition d’une clé de Registre. Exécutez la commande suivante pour activer « cas = force » si vous avez besoin pour l’utiliser : reg ajouter HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui doivent respecter la casse, utiliser fsutil.exe pour les marquer comme respectant la casse : fsutil.exe fichier setcasesensitiveinfo <path> activer
* Les chaînes retournées par la syscall uname finissant par NULL.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17107"></a>Build 17107
Pour Windows général plus d’informations sur la build 17107 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Prend en charge TCSETSF et TCSETSW sur les points de terminaison maître pty [GH 2552].
* Démarrage des processus interop simultanées peut entraîner EINVAL [GH 2813].
* Corriger PTRACE_ATTACH pour afficher l’état de suivi approprié dans /proc/pid/status.
* Concurrence de correctif où le processus de courte durée clonés avec indicateurs CLEARTID et de SETTID pu quitter sans effacer l’adresse TID.
* Afficher un message lors de la mise à niveau les répertoires de système de fichiers Linux lors du déplacement d’une build de pre-17093. Pour plus d’informations sur les modifications de système de 17093 fichiers, consultez les notes de publication pour [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17101"></a>Build 17101
Pour Windows général plus d’informations sur la build 17101 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Prise en charge signalfd. [GH 129]
* Prend en charge les noms de fichier contenant des caractères NTFS non valides en les codant en tant que caractères Unicode privés. [GH 1514]
* Montage automatique utilisera en lecture seule lors de l’écriture n’est pas pris en charge. [GH 2603]
* Autoriser le collage des paires de substitution Unicode (comme les caractères emoji). [GH 2765]
* Fichiers pseudo-élément dans /proc et /sys doivent retourner la lecture et écrire des prêts à partir de select, interrogation, epoll, et al. [GH 2838]
* Corrigez le problème qui pouvait entraîner service passe en boucle infinie lorsque le Registre a été falsifié ou est endommagé.
* Résoudre les messages netlink pour travailler avec la nouvelle version (en amont 4.14) d’iproute2.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17093"></a>Build 17093
Pour Windows général plus d’informations sur la build 17093 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Important :
Lorsque vous démarrez WSL pour la première fois après la mise à niveau vers cette version, il doit effectuer un travail de la mise à niveau les répertoires de système de fichiers Linux. Cela peut prendre jusqu'à plusieurs minutes, donc WSL peut sembler démarrer lentement. Cela ne doit se produire une fois pour chaque distribution que vous avez installé à partir du magasin.
* Meilleure prise en charge de la casse dans DrvFs.
    * DrvFs prend désormais en charge par répertoire respecte la casse. Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme respectant la casse, ce qui permet de même des applications Windows ouvrir correctement les fichiers qui diffèrent uniquement par la casse.
    * DrvFs a de nouvelles options de montage contrôle respecte la casse sur une base par répertoire
        * cas = force : tous les répertoires sont traités comme respectant la casse (à l’exception de la racine du lecteur). Nouveaux répertoires créés avec WSL sont marqués comme respectant la casse. Il s’agit de l’ancien comportement à l’exception de marquage de nouveaux répertoires respecte la casse.
        * cas = dir : seuls les répertoires avec l’indicateur par répertoire respecte la casse sont traités comme respectant la casse ; autres répertoires respectent la casse. Nouveaux répertoires créés avec WSL sont marqués comme respectant la casse.
        * cas = off : seuls les répertoires avec l’indicateur par répertoire respecte la casse sont traités comme respectant la casse ; autres répertoires respectent la casse. Nouveaux répertoires créés avec WSL portent la mention de la casse.
    * Remarque : répertoires créés par WSL dans les versions précédentes n’ont pas cet indicateur défini, afin de ne pas être traités comme respectant la casse si vous utilisez le « cas = dir « option. Une façon de définir cet indicateur dans les répertoires existants sera bientôt disponible.
    * Exemple de montage avec ces options (pour les lecteurs existants, vous devez tout d’abord la démonter avant que vous pouvez monter avec des options différentes) : sudo mount -t drvfs C:/mnt/c -o cas = dir
    * Pour l’instant, cas = force est toujours l’option par défaut. Ce sera remplacé au cas = dir dans le futur.
* Vous pouvez maintenant utiliser des barres obliques dans les chemins d’accès de Windows lors du montage DrvFs, par exemple : sudo mount -t drvfs //server/share /mnt/share
* WSL traite désormais le fichier/etc/fstab pendant le démarrage de l’instance [GH 2636].
    * Cette opération est effectuée avant de monter automatiquement les lecteurs de DrvFs ; tous les lecteurs qui ont été déjà montés par fstab ne seront pas être remontées automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.
    * Ce comportement peut être désactivé à l’aide de wsl.conf.
* Les fichiers de montage, mountinfo et mountstats dans /proc échappement correctement les caractères spéciaux tels que des barres obliques inverses et les espaces [GH 2799]
* Fichiers spéciaux créés avec DrvFs tels que des liens symboliques WSL, ou file d’attente FIFO et les sockets lorsque les métadonnées sont activées, peuvent désormais être copiés et déplacés à partir de Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL est plus configurable avec wsl.conf
Nous avons ajouté une méthode vous permettant de configurer automatiquement certaines fonctionnalités dans WSL qui est appliqué chaque fois que vous lancez le sous-système. Cela inclut les options de montage automatique et de configuration du réseau. Pour en savoir plus à ce sujet à notre billet de blog : https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX autorise les connexions de socket entre les processus de Linux sur WSL et les processus natifs de Windows
Applications WSL et Windows peuvent désormais communiquer avec eux via des sockets Unix. Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible aux applications Windows et WSL. Maintenant, c’est possible avec les sockets Unix. Lecture de plus, consultez notre blog publiez au https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Mmap() prise en charge avec MAP_NORESERVE [GH 121, 2784]
* Prendre en charge CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]
* Gérer le signal d’arrêt non SIGCHLD clone [GH 121, 2781]
* Stub /proc/sys/fs/inotify/max_user_instances et /proc/sys/fs/inotify/max_user_watches [GH 1705]
* Erreur lors du chargement des fichiers binaires ELF qui contiennent des en-têtes de charge avec zéro décalages [GH 1884]
* Zéro octets de la page de fin lors du chargement d’images.
* Réduire les cas où execve en mode silencieux pour achever

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17083"></a>Build 17083
Pour Windows général plus d’informations sur la build 17083 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Vérification d’erreur fixe liée à epoll [2798 GH 2801, 2857]
* Fixe se bloque lors de la désactivation de l’ASLR [GH 1185, 2870]
* Vérifiez les opérations mmap apparaissent atomique [GH 2732]

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17074"></a>Build 17074
Pour Windows général plus d’informations sur la build 17074 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Format de stockage fixe de métadonnées DrvFs [GH 2777] </br>
**Important :** Métadonnées DrvFs créées avant cette build s’afficheront mal ou pas du tout. Pour résoudre les fichiers affectés, utilisez chmod et chown à réappliquer les métadonnées.
* Correction d’un problème avec plusieurs signaux et syscalls redémarrable.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17063"></a>Build 17063
Pour Windows général plus d’informations sur la build 17063 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs prend en charge des métadonnées supplémentaires de Linux. Cela permet de définir le propriétaire et le mode de fichiers à l’aide de chmod/chown, ainsi que la création de fichiers spéciaux tels que la file d’attente FIFO, les sockets unix et les fichiers de l’appareil. Cela est désactivée par défaut pour l’instant, car il est encore au stade expérimental.
**Remarque :**  Nous avons résolu un bogue dans le format de métadonnées utilisé par DrvFs. Bien que métadonnées fonctionnement sur cette génération pour l’expérimentation, builds futures correctement ne lira pas les métadonnées créées par cette build.  Vous devrez peut-être mettre à jour manuellement le propriétaire pour les fichiers modifiés et appareils avec un ID d’appareil personnalisé devront être recréés.

  Pour activer, DrvFs de montage avec l’option de métadonnées (pour l’activer sur un montage existant, vous devez tout d’abord la démonter) :

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Autorisations de Linux sont ajoutées en tant que métadonnées supplémentaires au fichier ; elles n’affectent pas les autorisations de Windows.  N’oubliez pas de modification d’un fichier à l’aide d’un éditeur Windows peut supprimer les métadonnées. Dans ce cas, le fichier reprendront ses autorisations par défaut.

* Options de montage ajouté à DrvFs pour contrôler les fichiers sans métadonnées.
  * UID : l’ID d’utilisateur utilisé pour le propriétaire de tous les fichiers.
  * GID : l’ID de groupe utilisé pour le propriétaire de tous les fichiers.
  * umask : un masque octal des autorisations à exclure pour tous les fichiers et répertoires.
  * cas : un masque octal des autorisations à exclure pour tous les fichiers régulières.
  * dmask : un masque octal des autorisations à exclure tous les répertoires.

  Exemple :
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combiner avec l’option de métadonnées pour spécifier les autorisations par défaut pour les fichiers sans métadonnées.

* A introduit une nouvelle variable d’environnement, `WSLENV`, pour configurer le flux des variables d’environnement entre WSL et Win32.

  Exemple :

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` est une liste délimitée par des deux-points de variables d’environnement qui peut être inclus lors du lancement du processus WSL à partir de Win32 ou Win32 à partir de WSL.  Chaque variable peut être suivi du suffixe par une barre oblique suivie d’indicateurs pour spécifier la façon dont elle est convertie.
  * p : La valeur est un chemin d’accès qui doit être convertis entre les chemins de Win32 et WSL.
  * L : La valeur est une liste de chemins d’accès. Dans WSL, il est une liste délimitée par des deux-points. Dans Win32, il est une liste délimitée par des points-virgules.
  * %U : La valeur doit être incluse uniquement lors de l’appel WSL à partir de Win32
  * w : La valeur doit être incluse uniquement lors de l’appel Win32 à partir de WSL

  Vous pouvez définir `WSLENV` dans .bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.

* drvfs montages conserve correctement les horodatages de tar, cp -p (1939 Hg)
* liens symboliques drvfs indiquent la taille correcte (2641 Hg)
* en lecture/écriture fonctionne pour les très grandes tailles d’e/s (2653 Hg)
* waitpid fonctionne avec le groupe de processus ID (2534 Hg)
* mmap amélioration significative des performances pour les régions de la réserve de grande taille ; améliore les performances de ghc (1671 Hg)
* prise en charge de la personnalité de READ_IMPLIES_EXEC ; résout les maxima et clisp (1185 Hg)
* mprotect prend en charge PROT_GROWSDOWN ; correctifs clisp (1128 Hg)
* page d’erreur correctifs dans sollicitation excessive du mode ; correctifs sbcl (1128 Hg)
* Clone prend en charge plusieurs combinaisons d’indicateurs
* Prend en charge select/epoll des fichiers epoll (précédemment une absence d’opération).
* Notifier ptrace de syscalls non implémentée.
* Ignorer les interfaces qui ne sont pas des lors de la génération des serveurs de noms resolv.conf [GH 2694]
* Énumérer les interfaces réseau avec aucune adresse physique. [GH 2685]
* Améliorations et correctifs de bogues supplémentaires.

### <a name="linux-tools-available-to-developers-on-windows"></a>Outils de Linux qui permettent aux développeurs sur Windows

* Ligne de commande de Windows chaîne d’outils inclut bsdtar (tar) et curl.
  Lecture [ce billet de blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et de voir comment ils vous mettre en forme l’expérience de développement sur Windows.

*   `AF_UNIX` est disponible dans le Kit de développement Windows Insider (17061 +).
  Lecture [ce billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus sur `AF_UNIX` et comment les développeurs sur Windows peuvent l’utiliser.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.


## <a name="build-17046"></a>Build 17046

Pour Windows général plus d’informations sur la build 17046 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Autoriser le processus à s’exécuter sans un Terminal Server actives. [GH 709, 1007, 1511, 2252, 2391, et al.]
- Mieux prendre en charge de CLONE_VFORK et CLONE_VM. [GH 1878, 2615]
- Ignorer les pilotes de filtre TDI pour WSL opérations de mise en réseau. [GH 1554]
- DrvFs crée des liens symboliques NT lorsque certaines conditions sont remplies. [GH 353, 1475, 2602]
    - La cible du lien doit être relative, ne doit pas traverser les points de montage ou les liens symboliques et doit exister.
    - L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela requiert généralement que vous lancez wsl.exe avec élévation de privilèges), sauf si le Mode développeur est activé.
    - Dans toutes les autres situations, DrvFs crée toujours des liens symboliques WSL.
- Autoriser en cours d’exécution avec élévation de privilèges et non élevés instances WSL simultanément.
- Support /proc/sys/kernel/yama/ptrace_scope
- Ajouter wslpath pour faire WSL <> – conversions de chemin d’accès de Windows. [GH 522, 1243, 1834, 2327, et al.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>Console
- Aucun correctif.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.


## <a name="build-17040"></a>Build 17040

Pour Windows général plus d’informations sur la build 17040 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Aucun correctif depuis 17035.

#### <a name="console"></a>Console
- Aucun correctif depuis 17035.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17035"></a>Build 17035

Pour Windows général plus d’informations sur la build 17035 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Accéder aux fichiers sur DrvFs peut parfois échouer avec EINVAL. [GH 2448]

#### <a name="console"></a>Console
- Une perte de couleur lors de l’insertion/suppression de lignes en mode de VT.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17025"></a>Version 17025

Pour Windows général plus d’informations sur la build 17025 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Démarrer le processus initiales dans un nouveau groupe de processus de premier plan [GH 1653, 2510].
- Remise SIGHUP résout [GH 2496].
- Générer un nom de pont virtuel par défaut si aucun ne fourni [GH 2497].
- Implémenter /proc/sys/kernel/random/boot_id [GH 2518].
- Résout les plus interop canal stdout/stderr.
- Appel de système de syncfs de stub.

#### <a name="console"></a>Console
- Corriger la traduction de VT d’entrée pour les consoles tiers [GH 111]

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="build-17017"></a>Build 17017

Pour Windows général plus d’informations sur la build 17017 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Ignorer les en-têtes de programme vides ELF [GH 330].
- Autoriser LxssManager créer des instances WSL pour les utilisateurs non interactifs (ssh et planifiée prise en charge de la tâche) [GH 777, 1602].
- Prise en charge WSL -> Win32 -> [GH 1228] les scénarios WSL (« début »).
- Prise en charge limitée pour l’arrêt des applications de console appelé via interop [GH 1614].
- Prise en charge les options de montage pour devpts [GH 1948].
- Ptrace blocage démarrage enfant [GH 2333].
- EPOLLET certains événements [GH 2462] manquants.
- Retourner plus de données pour PTRACE_GETSIGINFO.
- Getdents avec lseek donne des résultats incorrects.
- Corriger certains blocages d’application d’interopérabilité Win32, en attente d’entrée sur un canal qui n’a plus aucune donnée.
- O_ASYNC prend en charge pour les fichiers de tty/pty.
- Autres améliorations et correctifs de bogues

#### <a name="console"></a>Console
- Aucune Console les modifications n’associées dans cette version.

### <a name="ltp-results"></a>LTP résultats :
Test en cours d’exécution.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>Build 16288

Pour Windows général plus d’informations sur la build 16288 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Initialiser correctement et de signaler les uid et gid mode pour les descripteurs de fichier socket [GH 2490]
- Autres améliorations et correctifs de bogues

#### <a name="console"></a>Console
- Aucune Console les modifications n’associées dans cette version.

### <a name="ltp-results"></a>LTP résultats :
Aucune modification depuis 16273

## <a name="build-16278"></a>Build 16278

Pour Windows général plus d’informations sur la build 162738 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Explicitement annuler le mappage de vues mappées des sections de la sauvegarde de fichiers lors de la destruction de l’état LX MM [GH 2415]
- Autres améliorations et correctifs de bogues

#### <a name="console"></a>Console
- Aucune Console les modifications n’associées dans cette version.

### <a name="ltp-results"></a>LTP résultats :
Aucune modification depuis 16273

## <a name="build-16275"></a>Build 16275

Pour Windows général plus d’informations sur la build 162735 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Aucun WSL les modifications n’associées dans cette version.

#### <a name="console"></a>Console
- Aucune Console les modifications n’associées dans cette version.

### <a name="ltp-results"></a>LTP résultats :
Aucune modification depuis 16273

## <a name="build-16273"></a>Build 16273

Pour Windows général plus d’informations sur la build 16273 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Correction d’un problème où DrvFs parfois signalé le type de fichier incorrect pour les répertoires [GH 2392]
- Autoriser la création de sockets NETLINK_KOBJECT_UEVENT débloquer des programmes qui uevent utilisation [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Ajouter la prise en charge pour la connexion à non bloquant [GH 903, 1391, 1584 1585, 1829, 2290, 2314]
- Implémentez CLONE_FS cloner l’indicateur d’appel système [GH 2242]
- Résoudre les problèmes liés à la gère ne pas de tabulations ou guillemets correctement dans l’interopérabilité de NT [GH 1625, 2164]
- Résoudre l’erreur lorsque vous tentez de relancer WSL instances [GH 651, 2095] l’accès refusé
- Implémenter des opérations FUTEX_REQUEUE et FUTEX_CMP_REQUEUE futex [GH 2242]
- Corriger les autorisations pour les divers fichiers SysFs [GH 2214]
- Corriger le blocage de pile de Haskell pendant l’installation [GH 2290]
- Implémenter binfmt_misc « C » ' o ' et les indicateurs « P » [GH 2103]
- Ajouter /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- Ajouter la prise en charge partielle de l’appel de système d’ioprio_set [GH 498]
- Stub SO_REUSEPORT & Ajout de prise en charge pour SO_PASSCRED pour les sockets netlink [69 GH]
- Retourner différents codes d’erreur à partir de RegisterDistribuiton si une distribution est actuellement installée ou désinstallée.
- Autoriser la désinscription des distributions de WSL partiellement installées via wslconfig.exe
- Corriger le blocage de test de socket python à partir de udp::msg_peek
- Autres améliorations et correctifs de bogues

#### <a name="console"></a>Console
- Aucune Console les modifications n’associées dans cette version.

### <a name="ltp-results"></a>LTP résultats :
Nombre total de Tests : 1904<br/>
Total ignoré des Tests : 209<br/>
Nombre total d’échecs : 229<br/>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Build 16257

Pour Windows général plus d’informations sur la build 16257 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Implémenter l’appel du système prlimit64
- Ajouter la prise en charge pour ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Stub MSG_MORE pour les sockets TCP [GH 2351]
- Corriger comportement de vecteur auxiliaires AT_EXECFN non valide [GH 2133]
- Corriger le comportement de copier/coller pour console/tty et ajouter de la mémoire tampon saturée une meilleure gestion des [GH 2204, 2131]
- Définissez AT_SECURE dans un vecteur auxiliaire pour les programmes de set-user-ID et set-group-ID [GH 2031]
- Point de terminaison maître pseudo-périphérique-Terminal Server ne gère ne pas TIOCPGRP [GH 1063]
- Correctif lseek effectue pour rembobiner des répertoires dans LxFs [GH 2310]
- /dev/ptmx se bloque après une utilisation élevée [GH 1882]
- Autres améliorations et correctifs de bogues

#### <a name="console"></a>Console
- Correctif pour horizontal lignes/des traits de soulignement Everywhere [GH 2168]
- Correctif pour l’ordre de processus modifié NPM ce qui rend plus difficile à fermer [GH 2170]
- Ajouté à notre nouveau modèle de couleurs : https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP résultats :
Aucune modification depuis 16251

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`prlimit64`<br/>

### <a name="known-issues"></a>Problèmes connus
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[Problème GitHub 2392 : Dossiers de Windows n’est ne pas reconnu par WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
Dans la build 16257, WSL présente des problèmes lors de l’énumération des fichiers/dossiers de Windows via `/mnt/c/...`.
Ce problème a été résolu et doivent être libéré dans Insiders build pendant la semaine 14/8/2017.

<br/>

## <a name="build-16251"></a>Build 16251

Pour Windows général plus d’informations sur la build 16251 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Supprimer la balise de version bêta de composant facultatif WSL, consultez [billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) pour plus d’informations.
- Initialiser correctement enregistré-set uid et gid pour les fichiers binaires de set-user-ID et set-group-ID sur exec [962 GH 1415, 2072]
- Prise en charge ajoutée pour ptrace PTRACE_O_TRACEEXIT [GH 555]
- Prise en charge pour ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]
- Fixe ptrace pour arrêter des signaux ignoré
- Autres améliorations et correctifs de bogues

#### <a name="console"></a>Console
- Aucune Console les modifications n’associées dans cette version.

### <a name="ltp-results"></a>LTP résultats :
Nombre de Tests concluants : 768</br>
Nombre de Tests ayant échoué : 244</br>
Nombre de Tests ignorés : 96</br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Build 16241

Pour Windows général plus d’informations sur la build 16241 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Aucun WSL les modifications n’associées dans cette version.

#### <a name="console"></a>Console
- Correctif pour la sortie de caractères incorrect pour DEC lignes d’origine, signalé initialement [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Correctif pour aucun texte de sortie qui est affiché dans la page de codes 65001 (UTF-8)
- Ne transférez pas les modifications apportées à un seul valeurs RVB à d’autres parties de la palette de la modification de la sélection. Cela fera la feuille de propriétés de console beaucoup plus facile à utiliser.
- CTRL + S ne semble pas fonctionner correctement
- Non gras /-Dim complètement absent à partir des codes d’échappement ANSI [GH 2174]
- Console ne correctement prendre en charge des thèmes de couleurs Vim [GH 1706]
- Impossible de coller des caractères particuliers [GH 2149]
- Redimensionnement de redistribution interagit étrangement avec redimensionnement d’une fenêtre d’interpréteur de commandes lorsque les éléments se trouvent sur la ligne de commande/modifier [GH ConEmu 1123]
- CTRL-L quitte l’écran dirty [GH 1978]
- Bogue de rendu de console lors de l’affichage VT sur HDPI [GH 1907]
- Caractères de la version japonaise paraître étranges avec un caractère Unicode U + 30FB [GH 2146]
- Autres améliorations et correctifs de bogues

</br>

## <a name="build-16237"></a>Build 16237

Pour Windows général plus d’informations sur la build 16237 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fixe
- Utiliser des attributs par défaut pour les fichiers sans EAs dans lxfs (racine, racine, 0000)
- Prise en charge pour les distributions qui utilisent des attributs étendus
- Correctif de remplissage pour les entrées retournées par getdents et getdents64
- Corriger la vérification des autorisations pour l’appel de système SHM_STAT shmctl [GH 2068]
- État fixe epoll initiale incorrect pour les TTY ne [GH 2231]
- Corriger readdir DrvFs ne pas renvoie toutes les entrées [GH 2077]
- Corriger LxFs readdir lorsque les fichiers sont dissocié [GH 2077]
- Autoriser les fichiers drvfs non liés à être rouverte via la commande procfs
- Ajouté la substitution de clé de Registre global pour la désactivation des fonctionnalités WSL (interop / le montage du lecteur)
- Résoudre le nombre de blocs incorrect dans « stat » pour DrvFs (et LxFs) [GH 1894]
- Autres améliorations et correctifs de bogues

</br>

## <a name="build-16232"></a>Build 16232

Pour Windows général plus d’informations sur la build 16232 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Aucun WSL les modifications n’associées dans cette version.

</br>

## <a name="build-16226"></a>Build 16226

Pour Windows général plus d’informations sur la build 16226 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fixe
- xattr liés prise en charge syscalls (getxattr, setxattr, listxattr, removexattr).
- prise en charge de Security.capablity xattr.
- Une meilleure compatibilité avec certains systèmes de fichiers et les filtres, y compris les serveurs SMB non - MS. [GH #1952]
- Prise en charge améliorée pour les espaces réservés de OneDrive, des espaces réservés GVFS et du système d’exploitation Compact des fichiers compressés.
- Autres améliorations et correctifs de bogues

</br>

## <a name="build-16215"></a>Build 16215

Pour Windows général plus d’informations sur la build 16215 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fixe
- WSL ne requiert plus le mode développeur.
- Prend en charge les jonctions de répertoires dans drvfs.
- Gérer la désinstallation des packages appx de distribution WSL.
- Mise à jour de commande procfs pour afficher privés et partagés des mappages.
- Ajoutez la possibilité pour wslconfig.exe nettoyer les distributions qui sont partiellement installées ou désinstallées.
- Prise en charge ajoutée pour IP_MTU_DISCOVER pour les sockets TCP. [GH 1639, 2115, 2205]
- Déduire la famille de protocoles pour les itinéraires à AF_INADDR.
- Améliorations de l’appareil de série [GH 1929].

</br>

## <a name="build-16199"></a>Build 16199

Pour Windows général plus d’informations sur la build 16199 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Aucun WSL les modifications n’associées dans ces versions.

</br>

## <a name="build-16193"></a>Build 16193

Pour Windows général plus d’informations sur la build 16193 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Condition de concurrence entre les envois de SIGCONT et un threadgroup fin d’exécution [GH 1973]
- modifier les appareils tty et pty au rapport FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]
- Correctif SSH pour IP_OPTIONS
- Déplacé le montage DrvFs init démon [1862 Hg, 1968, 1767, 1933]
- Prise en charge dans DrvFs pour les liens symboliques de NT.

</br>

## <a name="build-16184"></a>Build 16184

Pour Windows général plus d’informations sur la build 16184 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Supprimer la tâche de maintenance de package apt (lxrun.exe /update)
- Sortie fixe ne s’affichent ne pas dans des processus Windows dans node.js [GH 1840]
- Assouplir les conditions d’alignement dans lxcore [GH 1794]
- Correction de la gestion de l’indicateur AT_EMPTY_PATH dans un nombre d’appels système.
- Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts provoquera le fichier un comportement non défini [GH 544,966,1357,1535,1615]
- / etc/hosts hérite désormais les entrées à partir du fichier d’hôtes Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Build 16179

Pour Windows général plus d’informations sur la build 16179 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Aucune modification WSL cette semaine.

</br>

## <a name="build-16176"></a>Build 16176

Pour Windows général plus d’informations sur la build 16176 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fixe

- [Prise en charge de la série est activée](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Option de socket ajoutée IP IP_OPTIONS [GH 1116]
- Implémenté pwritev (fonction) (lors du téléchargement du fichier à nginx/PHP-FPM) [GH 1506]
- Ajouté des options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- Prise en charge pour l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- Option de socket IP (V6) _MTU ajoutée pour le nœud applications, détermination d’itinéraire, dig, nslookup, hôte
- Option de socket ajoutée IP IPV6_UNICAST_HOPS
- [Améliorations du système de fichiers](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Autoriser le montage des chemins d’accès UNC
    * Activer la prise en charge CDFS dans drvfs
    * Gérer correctement les autorisations pour les systèmes de fichiers réseau dans drvfs
    * Ajouter la prise en charge pour les lecteurs à distance à drvfs
    * Activer FAT prennent en charge dans drvfs
- Autres correctifs et améliorations

### <a name="ltp-results"></a>Résultats LTP
Aucune modification depuis 15042

</br>

## <a name="build-16170"></a>Build 16170

Pour Windows général plus d’informations sur la build 16170 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Nous avons publié un nouveau [billet de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) traitant de nos efforts pour tester WSL.

### <a name="fixed"></a>Fixe

- Socket de prise en charge option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- Ajouter la prise en charge pour PTRACE_OLDSETOPTIONS. [GH 1692]
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>Résultats LTP
Aucune modification depuis 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Build 15046 vers Windows 10 Creators Update
Il existe plus aucune WSL correctifs ou les fonctionnalités prévues pour être inclus dans la mise à jour Windows 10 Creators. Notes de publication pour WSL reprendra dans les semaines à venir pour les ajouts de ciblage de la prochaine mise à jour Windows majeures. Pour Windows général plus d’informations sur la build 15046 et Insider futures versions visite le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Build 15042

Pour Windows général plus d’informations sur la build 15042 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fixe

- Correction d’un blocage lors de la suppression d’un chemin d’accès se terminant par «... »
- Correction d’un problème où FIONBIO ne pas retourner 0 en cas de réussite [GH 1683]
- Correction d’un problème avec des lectures de longueur nulle de sockets de datagramme inet
- Résoudre un blocage possible en raison d’une condition de concurrence dans drvfs inode recherche [GH 1675]
- Prise en charge pour les données connexes de socket unix ; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 737</br>
Nombre de cas d’échec (échec, ignoré, etc....) : 255

</br>

## <a name="build-15031"></a>Build 15031

Pour Windows général plus d’informations sur la build 15031 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction d’un bogue où time(2) est sporadique mener.
- Fixe et émettre où * SIGPROCMASK syscalls peut endommager le masque de signal.
- Maintenant retourner la longueur de ligne de commande complète dans la notification de la création de processus WSL. [GH 1632]
- WSL signale désormais la sortie du thread via ptrace pour les blocages GDB. [GH 1196]
- Correction du bogue où se bloquait ptys après tmux importante d’e/s. [GH 1358]
- Validation du délai d’expiration fixe dans un grand nombre d’appels système (futex, semtimedop, ppoll, sigtimewait, itimer, timer_create)
- Prise en charge EFD_SEMAPHORE eventfd ajout [GH 452]
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 737</br>
Nombre de cas d’échec (échec, ignoré, etc....) : 255 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Build 15025

Pour Windows général plus d’informations sur la build 15025 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correctif pour bogue que grep ne 2.27 [GH 1578]
- Indicateur EFD_SEMAPHORE implémentée pour syscall eventfd2 [GH 452]
- Implémenté/proc / [pid] / net/ipv6_route [GH 1608]
- Signal contrôlée par la prise en charge d’e/s pour les sockets de flux unix [GH 393, 68]
- Prendre en charge F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]
- Implémenter recvmmsg() syscall [GH 1531]
- Correction du bogue où les epoll_wait() n’a pas été en attente [GH 1609]
- Implement /proc/version_signature
- Tee syscall retourne maintenant échec si les deux descripteurs de fichier font référence au même canal
- Comportement correct implémentée pour SO_PEERCRED pour les sockets Unix
- Gestion des paramètres non valides de syscall tkill fixe
- Modifications pour augmenter la preformace de drvfs
- Correctif mineur pour le blocage des e/s de Ruby
- Fixe recvmsg() retour EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 732</br>
Nombre de cas d’échec (échec, ignoré, etc....) : 255 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Build 15019

Pour Windows général plus d’informations sur la build 15019 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction du bogue qui est signalé à tort l’utilisation du processeur dans commande procfs pour des outils comme htop (GH 823, 945, 971)
- Lors de l’appel open() avec O_TRUNC sur un fichier inotify génère désormais IN_MODIFY avant IN_OPEN
- Correctifs pour unix socket getsockopt SO_ERROR pour activer postgress [GH 61, 1354]
- Implémenter /proc/sys/net/core/somaxconn pour le langage GO
- Tâche d’arrière-plan apt-get package mise à jour s’exécute désormais masqué à partir de la vue
- Étendue clair pour ipv6 localhost (Spring-Framework(Java) échec).
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 714 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 249 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Build 15014

Pour Windows général plus d’informations sur la build 15014 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixe

- CTRL + C fonctionne désormais comme prévu
- htop et ps auxw maintenant afficher correct l’utilisation des ressources (GH #516)
- Traduction de base des exceptions de NT aux signaux. (GH #513)
- fallocate échoue avec ENOSPC alors EINVAL (GH #1571) au lieu de l’espace est insuffisant
- /Proc/sys/kernel/sem ajouté.
- Appels de système semop et semtimedop implémentées
- Erreurs nslookup fixe avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (69 Hg)
- Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 709 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 255 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Résumé de syscall
Syscalls total : 384 </br>
Total implémenté : 235 </br>
Nombre total de l’objet d’un stub : 22 </br>
Total non implémenté : 127 </br>
[Analyse détaillée](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Build 15007

Pour Windows général plus d’informations sur la build 15007 visitez le [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problème connu

- Il existe un bogue connu dans lequel la console ne reconnaît pas certains Ctrl + <key> d’entrée.  Cela inclut la commande ctrl-c qui agira comme un keypress « c » normal.

  - Solution : Mapper une autre clé à Ctrl + C. Par exemple, Ctrl + K, Ctrl + c faire pour mapper : `stty intr \^k`.  Ce mappage s’effectue par terminal et devra être fait *chaque* bash de temps est lancée. Les utilisateurs peuvent Explorer la possibilité d’inclure cela dans leurs `.bashrc`

### <a name="fixed"></a>Fixe

- Correction du problème où en cours d’exécution WSL consomme 100 % d’un cœur de processeur
- Option IP_PKTINFO, IPV6_RECVPKTINFO désormais pris en charge de socket. (GH #851, 987)
- Tronquer l’adresse d’interface réseau physique à 16 octets lxcore (GH #1452, 1414, 1343, 468, 308)
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 709 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 255 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Build 15002

Pour Windows général plus d’informations sur la build 15002 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problème connu

Deux problèmes connus :
- Il existe un bogue connu dans lequel la console ne reconnaît pas certains Ctrl + <key> d’entrée.  Cela inclut la commande ctrl-c qui agira comme un keypress « c » normal.

  - Solution : Mapper une autre clé à Ctrl + C. Par exemple, Ctrl + K, Ctrl + c faire pour mapper : `stty intr \^k`.  Ce mappage s’effectue par terminal et devra être fait *chaque* bash de temps est lancée. Les utilisateurs peuvent Explorer la possibilité d’inclure cela dans leurs `.bashrc`

- Pendant l’exécution de WSL un thread système consomme 100 % d’un cœur de processeur.  La cause racine a été adressée et fixe en interne.

### <a name="fixed"></a>Fixe

- Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.  Vous essayez de démarrer une session à un autre niveau sera bloquée.  Cela signifie que les consoles administrateur et non-administrateur ne peut pas s’exécuter en même temps. (#626 HG)
<br/>
- Implémenté les messages NETLINK_ROUTE suivants (exige un administrateur de Windows)
     - RTM_NEWADDR (prend en charge `ip addr add`)
     - RTM_NEWROUTE (prend en charge `ip route add`)
     - RTM_DELADDR (prend en charge `ip addr del`)
     - RTM_DELROUTE (prend en charge `ip route del`)
- Vérification des packages à mettre à jour de tâche planifiée ne s’est plus sur une connexion limitée (GH # 1 371)
- Correction d’erreur dans lequel tuyauterie obtient bloquée par exemple, c - bash « ls - alR / » | Bash -c « cat » (GH #1214)
- Option de socket TCP_KEEPCNT implémentée (GH #843)
- Option de socket IP_MTU_DISCOVER INET implémentée (GH #720, 717, 170, 69)
- Supprimé des fonctionnalités héritées pour exécuter des fichiers binaires de NT à partir d’init avec la recherche de chemin d’accès de NT. (#1325 HG)
- Corriger le mode de/dev/kmsg pour autoriser l’accès de lecture de groupe / autre (0644) (GH #1321)
- /Proc/sys/kernel/random/uuid implémentée (GH #1092)
- Correction d’erreur où l’heure de début de processus n’affiche qu’année 2432 (GH #974)
- Variable d’environnement terme par défaut commuté xterm-256color (GH #1446)
- Modifié la façon dont les processus de validation est calculée pendant la duplication du processus. (GH #1286)
- /Proc/sys/vm/overcommit_memory implémentée. (GH #1286)
- Fichier /proc/net/route implémentée (GH #69)
- Correction de l’erreur où nom raccourci a été correctement localisés (GH #696)
- Elf fixe logique qui est incorrectement la validation des en-têtes de programme d’analyse doit être inférieur (ou égal à) PATH_MAX. (GH #1048)
- Rappel statfs implémentée pour la commande procfs, sysfs cgroupfs et binfmtfs (GH #1378)
- Windows AptPackageIndexUpdate fixes qui ne se ferme pas (GH #1184, également abordées dans GH #1193)
- Prise en charge ADDR_NO_RANDOMIZE du personnalité ASLR ajouté. (GH #1148, 1128)
- PTRACE_GETSIGINFO améliorée, SIGSEGV, pour les traces de pile gdb appropriée pendant AV (875 de # Hg)
- ELF l’analyse n’est plus échoue pour les fichiers binaires patchelf. (#471 HG)
- VPN DNS propagées à /etc/resolv.conf (GH #416 1350)
- Améliorations apportées à TCP fermer pour le transfert de données plus fiable. (GH #610, 616, 1025, 1335)
- Code d’erreur correct retournent désormais lorsque trop de fichiers est ouverts (EMFILE). (GH #1126, 2090)
- Rapports d’Audit de Windows journal maintenant nom de l’image dans le processus de création d’audit.
- Échouer normalement lors du lancement bash.exe à partir d’une fenêtre d’interpréteur de commandes
- Message d’erreur ajoutés lorsque l’interopérabilité ne parvient pas à accéder à un répertoire de travail sous LxFs (par exemple, notepad.exe .bashrc)
- Résolution du problème où le chemin d’accès Windows a été tronquée dans WSL
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 690 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 274 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Build 14986

Pour Windows général plus d’informations sur la build 14986 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction de bogues avec Netlink et Pty IOCTL
- Version du noyau signale désormais 4.4.0-43 par souci de cohérence avec Xenial
- Bash.exe lance maintenant lorsque l’entrée dirigée vers ' nul :' (GH #1259)
- ID de thread signalés désormais correctement dans la commande procfs (#967 Hg)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Indicateurs IN_ISDIR désormais pris en charge dans inotify_add_watch() (GH #1280)
- Implémentez timer_create et les appels système associées.  Cela permet la prise en charge GHC (GH #307)
- Résolution du problème où ping retourné un temps de 0.000ms (GH #1296)
- Retourne le code d’erreur approprié lorsque trop de fichiers est ouverts.
- Résolution du problème dans WSL où demande Netlink pour les données de l’interface réseau échoue avec EINVAL si l’adresse matérielle de l’interface est de 32 octets (par exemple, l’interface Teredo)
   - Notez que l’utilitaire de Linux « ip » contient un bogue dans lequel il se bloque si WSL signale une adresse matérielle de 32 octets. Il s’agit d’un bogue dans « ip », pas WSL. Le « ip » utilitaire code en dur la longueur de la mémoire tampon de chaîne utilisée pour imprimer l’adresse de matériel, et cette mémoire tampon est trop petit pour imprimer une adresse matérielle de 32 octets.
- Améliorations et correctifs supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 669 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 258 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Build 14971

Pour Windows général plus d’informations sur la build 14971 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fixe

 - En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.  Mises à jour régulièrement planifiées reprendra à la prochaine version.

### <a name="ltp-results"></a>LTP résultats :
Inchangé depuis 14965 </br>
Nombre de Test réussi : 664 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Build 14965

Pour Windows général plus d’informations sur la build 14965 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fixe

- Prise en charge de Netlink des sockets du protocole NETLINK_ROUTE RTM_GETLINK et RTM_GETADDR (GH #468)
  - Permet aux commandes ifconfig et l’adresse ip pour l’énumération de réseau
  - Vous trouverez plus d’informations dans nos [WSL mise en réseau de billet de blog](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin est désormais dans le chemin de l’utilisateur par défaut
- Chemin d’accès de l’utilisateur NT maintenant ajouté pour le chemin d’accès WSL par défaut (par exemple, vous pouvez désormais taper notepad.exe sans ajouter System32 dans le chemin d’accès Linux)
- Prise en charge ajoutée pour /proc/sys/kernel/cap_last_cap
- Les fichiers binaires de NT peut maintenant être lancées depuis WSL lorsque le répertoire de travail actuel contient des caractères non-ansi (GH #1254)
- Autoriser l’arrêt sur un socket de flux de données déconnecté unix.
- Prise en charge ajoutée pour PR_GET_PDEATHSIG.
- Prise en charge ajoutée pour CLONE_PARENT
- Correction d’erreur dans lequel tuyauterie obtient bloquée par exemple, c - bash « ls - alR / » | Bash -c « cat » (GH #1214)
- Demandes de handle de connexion vers le terminal actuel.
- Marquer/proc /<pid>/oom_score_adj comme accessible en écriture.
- Ajouter un dossier de /sys/fs/cgroup.
- sched_setaffinity doit renvoyer le nombre de masque de bits d’affinité
- Corriger la logique de validation ELF qui incorrectement suppose de chemins d’accès de l’interpréteur doivent comporter moins de 64 caractères. (#743 HG)
- Descripteurs de fichiers ouverts peuvent conserver la fenêtre de console ouverte (GH #1187)
- Erreur Fixeed où rename() a échoué avec barre oblique sur le nom de la cible (GH #1008)
- Implémenter /proc/net/dev fichier
- 0.000ms fixe effectue un test ping en raison de la résolution du chronomètre.
- /Proc/self/environ implémentée (GH #730)
- Améliorations et correctifs de bogues supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 664 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Build 14959

Pour Windows général plus d’informations sur la build 14959 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fixe

- Notification Pico processus amélioré pour Windows.  Des informations supplémentaires disponibles sur le [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Stabilité améliorée avec l’interopérabilité de Windows
- Correction de l’erreur 0 x 80070057 lors du lancement bash.exe lorsque la Protection de données d’entreprise (EDP) est activée
- Améliorations et correctifs de bogues supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 665 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Build 14955

Pour Windows général plus d’informations sur la build 14955 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fixe

 - En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.  Mises à jour régulièrement planifiées reprendra à la prochaine version.

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 665 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Build 14951

Pour Windows général plus d’informations sur la build 14951 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Nouvelle fonctionnalité : Windows / Ubuntu interopérabilité
Les fichiers binaires Windows peuvent maintenant être appelées directement à partir de la ligne de commande WSL.  Cela permet aux utilisateurs d’interagir avec leur environnement de Windows et le système d’une manière qui n’a pas été possible.  Exemple rapide, il est désormais possible pour les utilisateurs à exécuter les commandes suivantes :

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Vous trouverez plus d’informations sur :

- [Blog de l’équipe WSL pour l’interopérabilité](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentation Interop MSDN](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Fixe

- Ubuntu 16.04 (Xenial) est maintenant installé pour toutes les nouvelles instances WSL.  Les utilisateurs avec des instances (fidèle) 14.04 existantes ne seront pas mis à niveau automatiquement.
- Paramètres régionaux définis lors de l’installation sont maintenant affichée.
- Améliorations de Terminal Server, y compris le bogue où rediriger un processus WSL vers un fichier ne pas toujours fonctionner
- Durée de vie de console doit être liée à la durée de vie bash.exe
- Taille de fenêtre de console doit utiliser la taille visible, taille de mémoire tampon pas
- Améliorations et correctifs de bogues supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 665 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Build 14946

Pour Windows général plus d’informations sur la build 14946 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fixe

- Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT qui contiennent des espaces ou des guillemets doubles. 
- Modification VolFs et DrvFs pour retourner 0 pour le nombre de liens de l’annuaire dans stat
- Prend en charge l’option de socket IPV6_MULTICAST_HOPS.
- Limiter à une seule console boucle d’e/s par tty. Exemple : la commande suivante est possible :
  - Bash -c « echo data » | Bash - c « ssh user@example.com ' cat > foo.txt » »

- Remplacez les espaces par des tabulations dans /proc/cpuinfo (GH #1115)
- DrvFs apparaît désormais dans mountinfo avec un nom qui correspond au volume de Windows monté
- /Home et/root apparaissent désormais dans mountinfo avec les noms corrects
- Améliorations et correctifs de bogues supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 665 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Build 14942

Pour Windows général plus d’informations sur la build 14942 visitez le [Windows Blog](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fixe

- Un nombre de bogues résolus, y compris la » a TENTÉ de s’exécuter de PasExécution ne peut être mémoire « incident qui a été blocage SSH de mise en réseau
- inotifiy prise en charge pour les notifications générées à partir d’applications Windows sur DrvFs est présent dans
- Implémenter TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod. (#695 HG)
- Implémenter l’appel système pivot_root
- Implémenter l’option de socket pour SO_DONTROUTE
- Améliorations et correctifs de bogues supplémentaires


### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 665 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 263 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Build 14936

Pour Windows général plus d’informations sur la build 14936 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Remarque: WSL va installer Ubuntu version 16.04 (Xenial) au lieu d’Ubuntu 14.04 (fidèle) dans une prochaine version.  Cette modification s’applique pour les Insiders installation de nouvelles instances (lxrun.exe /install ou première exécution de bash.exe).  Les instances existantes avec fidèle ne seront pas mis à niveau automatiquement. Les utilisateurs peuvent mettre à niveau leur image fidèle à Xenial à l’aide de la commande-version-mise à niveau.

### <a name="known-issue"></a>Problème connu
WSL rencontre un problème avec certaines implémentations de socket.  La vérification d’erreur se manifeste comme un incident avec l’erreur « A TENTÉ de s’exécuter de PasExécution ne peut être mémoire ».  La manifestation la plus commune de ce problème est un incident lors de l’utilisation de ssh.  La cause racine est fixe sur des versions internes et n’est adressée aux initiés dès que possible.

### <a name="fixed"></a>Fixe

- Implémentation de l’appel système chroot
- Améliorations dans inotify ~~, y compris la prise en charge pour les notifications générées à partir d’applications Windows sur DrvFs~~
  - Correction : Inotify prend en charge les modifications provenant d’applications Windows non disponibles pour l’instant.
- Liaison à IPV6 de socket ::<port n> prend désormais en charge IPV6_V6ONLY (GH #68 #157, #393, #460, #674, #740, #982, #996)
- Comportement WNOWAIT pour waitid systemcall implémenté (GH #638)
- Prise en charge des options de socket IP IP_HDRINCL et IP_TTL
- Read() de longueur nulle doit retourner immédiatement (GH #975)
- Gérer correctement les préfixes des noms de fichiers et le nom de fichier qui n’incluent pas une marque de fin NULL dans un fichier .tar.
- prise en charge d’epoll de/dev/null
- Corriger la source de temps /dev/alarm
- Bash -c maintenant en mesure de rediriger vers un fichier
- Améliorations et correctifs de bogues supplémentaires

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 664 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 264 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Build 14931

Pour Windows général plus d’informations sur la build 14931 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fixe

 - En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.  Mises à jour régulièrement planifiées reprendra dans la prochaine version.

<br/>

## <a name="build-14926"></a>Build 14926

Pour Windows général plus d’informations sur la build 14926 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fixe

- Ping fonctionne désormais dans les consoles qui n’ont pas de privilèges d’administrateur
- Ping6 maintenant également pris en charge, sans privilèges d’administrateur
- Inotify prise en charge pour les fichiers modifiés via WSL. (#216 HG)
  - Indicateurs pris en charge :
    - inotify_init1 : LX_O_CLOEXEC, LX_O_NONBLOCK
    - événements d’inotify_add_watch : LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - attributs d’inotify_add_watch : LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - lire la sortie : LX_IN_ISDIR, LX_IN_IGNORED
  - Problème connu : Modification des fichiers à partir d’applications de Windows ne génère pas d’événements
- Socket UNIX prend désormais en charge SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP résultats :
Nombre de Test réussi : 651 </br>
Nombre de cas d’échec (échec, ignoré, etc....) : 258 </br>
[Journaux de série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Build 14915

Pour Windows général plus d’informations sur la build 14915 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixe
-  Socketpair pour les sockets datagramme unix (GH #262)
- Prise en charge de socket UNIX pour SO_REUSEADDR
- Prise en charge de socket UNIX pour SO_BROADCAST (GH #568)
- Prise en charge de socket UNIX pour SOCK_SEQPACKET (758 GH #, #546)
- Ajout de prise en charge pour l’envoi de socket datagramme unix, reçues et d’arrêt
- Corriger la vérification d’erreur en raison de la validation de paramètre mmap non valide pour les adresses non fixe. (#847 HG)
- Prise en charge pour interrompre / reprendre des États de Terminal Server
- Prise en charge d’ioctl TIOCPKT débloquer l’utilitaire d’écran (GH #774)
    - Problème connu : Touches de fonction non opérationnels
- Correction d’une concurrence dans TimerFd qui peut entraîner un membre libéré 'ReaderReady' accessible par LxpTimerFdWorkerRoutine (GH #814)
- Activer le support d’appel système pouvant être redémarrées pour futex, interrogation et clock_nanosleep
- Prise en charge du montage de liaison ajouté
- Annuler le partage pour la prise en charge de l’espace de noms de montage
    - Problème connu : Lorsque vous créez un nouvel espace de noms de montage avec `unshare(CLONE_NEWNS)` le répertoire de travail continue à pointer vers l’ancien espace de noms
- Autres améliorations et correctifs de bogues

<br/>

## <a name="build-14905"></a>Build 14905

Pour Windows général plus d’informations sur la build 14905 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Système redémarrable appels sont désormais pris en charge (GH #349 GH #520)
- Liens symboliques vers des répertoires de fin dans / maintenant opérationnelle (GH #650)
- Implémenté RNDGETENTCNT ioctl pour/dev/Random
- Implémenté le/proc / [pid] / monte, / proc / [pid] / mountinfo et/proc / [pid] / mountstats fichiers
- Améliorations et correctifs de bogues supplémentaires

</br>

## <a name="build-14901"></a>Build 14901
Première Insider générer pour la publication de mise à jour anniversaire de Windows 10.

Pour Windows général plus d’informations sur la build 14901 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fixe
- Problème de barre oblique de fin fixe
    - Commandes telles que `$ mv a/c/ a/b/` fonctionne maintenant
- Installation invite désormais l’utilisateur si les paramètres régionaux Ubuntu doivent être défini sur les paramètres régionaux Windows
- Commande procfs prise en charge pour le dossier de ns
- Ajouté le montage et démontage pour tmpfs, commande procfs et systèmes de fichiers sysfs
- Corriger mknod [at] signature ABI de 32 bits
- Sockets UNIX déplacés pour distribuer le modèle
- Taille de mémoire tampon INET socket recv défini à l’aide de la setsockopt doit être respecté.
- Indicateur de message de réception de socket MSG_CMSG_CLOEXEC unix implémenter
- Redirection de canal de stdin/stdout de processus Linux (GH #2)
    - Permet de combinaison de l’interpréteur de commandes - c dans cmd.exe.  Exemple : > dir | Bash -c « foo grep »
- Bash peut désormais être installée sur les systèmes avec plusieurs fichiers d’échange (538 GH #, #358)
- Taille de mémoire tampon par défaut INET Socket doit correspondre à celle de l’installation d’Ubuntu par défaut
- Aligner syscalls xattr à listxattr
- Retourner uniquement les interfaces avec une adresse IPv4 valide provenant de SIOCGIFCONF
- Corriger l’action par défaut de signal lorsque injecté par ptrace
- implement /proc/sys/vm/min_free_kbytes
- Utilisez les valeurs de registres de contexte ordinateur lors de la restauration du contexte dans sigreturn
    - Cela résout le problème où java et javac ont été mise en suspens pour certains utilisateurs
- Implémenter /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Build 14388 à la mise à jour anniversaire Windows 10
Pour Windows général plus d’informations sur la build 14388 visitez le [Windows Blog](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fixe
- Correctifs pour vous préparer à la mise à jour anniversaire de Windows 10 sur 8/2
  - Vous trouverez plus d’informations sur WSL dans la mise à jour anniversaire sur notre [blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>Build 14376
Pour Windows général plus d’informations sur la build 14376 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fixe
- Supprimé certaines instances où apt-get bloque (GH #493)
- Correction d’un problème où les montages vides n’étaient pas gérées correctement
- Correction d’un problème où ramdisks n’étaient pas monté correctement
- Acceptation du socket d’unix de modification pour prendre en charge les indicateurs (partielle GH #451)
- Réseau commun fixe liés écran bleu
- Correction d’écran bleu lorsque vous accédez à/proc / [pid] / tâches (GH #523)
- Fixe utilisation élevée du processeur pour des scénarios de pty (488 GH #, #504)
- Améliorations et correctifs de bogues supplémentaires

<br/>

## <a name="build-14371"></a>Build 14371
Pour Windows général plus d’informations sur la build 14371 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fixe
- Corrigé concurrence de minutage avec SIGCHLD et wait() lors de l’utilisation de ptrace
- Correction d’un comportement lorsque les chemins d’accès ont une fin / (GH #432)
- Résolution du problème de changement de nom/dissocier des échouent en raison de descripteurs ouverts pour enfants
- Améliorations et correctifs de bogues supplémentaires

<br/>

## <a name="build-14366"></a>Build 14366
Pour Windows général plus d’informations sur la build 14366 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fixe
- Corriger dans la création de fichiers via les liens symboliques
-   Ajout de listxattr pour Python (385 Hg)
-   Améliorations et correctifs de bogues supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
-   Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Build 14361
Pour Windows général plus d’informations sur la build 14361 visitez le [Windows Blog](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fixe
- DrvFs est désormais sensible à la casse lors de l’exécution dans Bash sur Ubuntu sur Windows.
  - Les utilisateurs mai case.txt et cas. TXT sur leur c/mnt/lecteurs
  - Respecte la casse est uniquement pris en charge dans Bash sur Ubuntu sur Windows. Lorsque l’extérieur de NTFS Bash signale correctement les fichiers, mais un comportement inattendu peut se produire à interagir avec les fichiers à partir de Windows.
  - La racine de chaque volume (c'est-à-dire /mnt/c) n’est pas sensible à la casse
  - Vous pouvez trouver plus d’informations sur la gestion des ces fichiers dans Windows [ici](https://support.microsoft.com/en-us/kb/100625).
- Considérablement améliorée pty / tty prend en charge.  Les applications telles que TMUX désormais pris en charge que (# GH 40)
- Problème d’installation fixe où les comptes d’utilisateurs créés pas toujours
- Optimisé structure arg de ligne de commande permettant de liste d’arguments de très longs. (#153 HG)
- Maintenant en mesure de supprimer et chmod read_only les fichiers à partir de DrvFs
- Correction de certaines instances où les blocages de terminal sur Déconnecter (GH #43)
- chmod et chown fonctionnent désormais sur les appareils tty
- Autoriser la connexion à 0.0.0.0 et :: en tant que localhost (GH #388)
- Sendmsg/recvmsg gèrent maintenant une longueur de vecteur d’e/s de > 1 (partielle GH #376)
- Les utilisateurs peuvent désormais annulations du fichier généré automatiquement les ordinateurs hôtes (GH #398)
- Automatiquement en correspondance les paramètres régionaux de Linux pour les paramètres régionaux NT lors de l’installation (GH #11)
- Ajouté le fichier /proc/sys/vm/swappiness (GH #306)
- strace se ferme désormais correctement
- Autoriser les canaux être rouverte via /proc/self/fd (GH #222)
- Masquer les répertoires sous %LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)
- Meilleure gestion des bash.exe ~.  Commandes telles que « bash ~ ls - c » désormais pris en charge (GH #467)
- Sockets notifient maintenant epoll en lecture disponible lors de l’arrêt (GH #271)
- lxrun / désinstallation est plus efficace de la suppression des fichiers et dossiers
- Corrigé ps -f (GH #246)
- X11 prise en charge améliorée des applications telles que xEmacs (GH #481)
- Mise à jour de la taille de pile de thread initial au paramètre d’Ubuntu par défaut et de signalement de la taille correctement à la syscall get_rlimit (172 GH #, #258)
- Amélioration des rapports pico image noms de processus (par exemple, pour l’audit)
- /Proc/mountinfo implémentée pour la commande df
- Code d’erreur de lien symbolique fixe pour le nom de l’enfant. et...
- Améliorations et correctifs de bogues des améliorations supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Build 14352
Pour Windows général plus d’informations sur la build 14352 visitez le [Windows Blog](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fixe
- Correction d’un problème où des fichiers volumineux ont été téléchargés non / créées correctement.  Cela doit débloquer npm et autres scénarios (GH n ° 3, Hg #313)
- Supprimé certaines instances où sockets de blocage
- Correction des erreurs ptrace
- Correction d’un problème avec WSL autorisant les noms de fichiers plus de 255 caractères
- Prise en charge améliorée pour les caractères non anglais
- Ajoutez des données de fuseau horaire Windows actuelles et définissez comme valeur par défaut
- D’id appareil unique pour chaque point de montage (correctif jre – GH #49)
- Corriger le problème avec les chemins d’accès contenant «. » et «... »
- Prise en charge Fifo (GH #71)
- Format mis à jour de resolv.conf pour faire correspondre le format natif Ubuntu
- Un nettoyage des commande procfs
- Ping activé pour les consoles administrateur (GH #18)

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Build 14342
Pour Windows général plus d’informations sur build 14342 le [Windows Blog](https://aka.ms/wip14342). <br/>

Vous trouverez plus d’informations sur VolFs et DriveFs sur le [WSL Blog](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Fixe
- Résolu le problème d’installation lorsque l’utilisateur Windows avait des caractères Unicode dans le nom d’utilisateur
- La solution de contournement udev apt-get update dans le Forum aux questions est désormais fournie par défaut sur la première exécution
- Activé des liens symboliques dans DriveFs (/mnt/<drive>) répertoires
- Fonctionnent désormais de liens symboliques entre DriveFs et VolFs
- Adressée supérieur au niveau chemin d’accès de l’analyse du problème : %.ls. / / fonctionne désormais comme prévu
- npm installez-y DriveFs et les options -g sont maintenant opérationnelles.
- Correction d’un problème empêchant le lancement de serveur PHP
- Valeurs d’environnement par défaut de mise à jour, telles que $PATH pour rapprocher correspond à Ubuntu natif
- Ajouter une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache du package apt
- Correction du problème avec la validation de l’en-tête ELF, WSL prend désormais en charge toutes les options de Melkor
- Interpréteur de commandes Zsh est fonctionnel
- Les binaires précompilés Go sont donc compatibles
- Inviter sur Bash.exe tout d’abord exécuter est maintenant correctement localisé
- /proc/meminfo retourne désormais des informations correctes
- Sockets désormais pris en charge dans le système de fichiers virtuel
- /dev maintenant monté en tant que tempfs
- FIFO désormais pris en charge
- Des systèmes multicœurs montre maintenant correctement dans cpuinfo/proc /
- Améliorations supplémentaires et des messages d’erreur téléchargé au cours de la première exécution
- Syscall améliorations et correctifs de bogues. Syscall pris en charge de la liste ci-dessous.
- Améliorations et correctifs de bogues supplémentaires

### <a name="known-issues"></a>Problèmes connus
- Ne pas de résolution '..' correctement sur DriveFs dans certains cas

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL. Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a>Build 14332

Pour Windows général plus d’informations sur la build 14332 visitez le [Windows Blog](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fixe
- Meilleure génération resolv.conf, y compris la hiérarchisation des entrées DNS
- Problème avec le déplacement de fichiers et répertoires entre mnt et non- / mnt lecteurs
- Fichiers .tar peuvent maintenant être créés avec des liens symboliques
- Répertoire de /run/lock par défaut ajoutés lors de la création d’instance
- Mise à jour/dev/null pour retourner des informations statistiques appropriées
- Autres erreurs lors du téléchargement lors du premier démarrage
- Syscall améliorations et correctifs de bogues. Syscall pris en charge de la liste ci-dessous.
- Améliorations et correctifs de bogues des améliorations supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la nouvelle syscall qui a déjà une implémentation dans WSL. La syscall sur cette liste est pris en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Build 14328

Pour Windows général plus d’informations sur la build 14332 visitez le [Windows Blog](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Nouvelles fonctionnalités
* Prennent désormais en charge les utilisateurs de Linux.  L’installation de Bash sur Ubuntu sur Windows vous demande de la création d’un utilisateur Linux.  Pour plus d’informations, visitez https://aka.ms/wslusers
* Nom d’hôte est maintenant défini pour le nom d’ordinateur Windows, pas plus @localhost
* Pour plus d’informations sur build 14328, visitez : https://aka.ms/wip14328

### <a name="fixed"></a>Fixe
* Améliorations de lien symbolique pour /mnt/ non<drive> fichiers
    * npm installation fonctionne désormais correctement
    * JDK / jre installable maintenant à l’aide des instructions trouvées [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * problème connu : liens symboliques ne fonctionnent pas pour Windows monte.  Fonctionnalité sera disponible dans une version ultérieure
* haut et htop affichent désormais
* Messages d’erreur supplémentaires pour certains échecs de l’installation
* Syscall améliorations et correctifs de bogues.  Syscall pris en charge de la liste ci-dessous.
* Améliorations et correctifs de bogues des améliorations supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
Voici une liste d’appels qui ont une implémentation dans WSL.  Syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
