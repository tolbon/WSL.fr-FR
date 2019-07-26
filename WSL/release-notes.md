---
title: Notes de publication pour le sous-système Windows pour Linux
description: Notes de publication pour le sous-système Windows pour Linux.  Mise à jour hebdomadaire.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: d2d91db24c12fc674d695ccffc79eb5781a0721d
ms.sourcegitcommit: be00abbb170aa569e008b804f15949344b378999
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/25/2019
ms.locfileid: "68501583"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notes de publication pour le sous-système Windows pour Linux


## <a name="build-18947"></a>Build 18947
Pour obtenir des informations générales sur Windows sur la build 18947, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18947/).

### <a name="wsl"></a>WSL
* [WSL2] Autoriser l’accès des sockets TCP d’écoute dans WSL2 à partir de l’hôte à l’aide de localhost: port
* [WSL2] Correctifs pour les échecs d’installation/conversion et les Diagnostics supplémentaires pour suivre les problèmes futurs [GH 4105] 
* [WSL2] Améliorez les diagnostics des problèmes de réseau WSL2
* [WSL2] Mettre à jour la version du noyau vers 4.19.55
* [WSL2] Mise à jour du noyau avec les options de configuration requises pour l’ancrage [GH 4165]
* [WSL2] Augmentez le nombre de processeurs affectés à la machine virtuelle utilitaire légère pour qu’ils soient identiques à ceux de l’ordinateur hôte (précédemment plafonné à 8 par CONFIG_NR_CPUS dans la configuration du noyau) [GH 4137]
* [WSL2] Créer un fichier d’échange pour la machine virtuelle légère WSL2
* [WSL2] Autoriser l’affichage des montages utilisateur via \\ \\WSL $\\distribution (par exemple sshfs) [GH 4172]
* [WSL2] Améliorer les performances du système de fichiers 9P
* [WSL2] S’assurer que la liste ACL VHD n’augmente pas sans limite [GH 4126]
* [WSL2] Mise à jour de la configuration du noyau pour prendre en charge squashfs et xt_conntrack [GH 4107, 4123]
* [WSL2] Correctif pour Interop. option/etc/WSL.conf activée [GH 4140]
* [WSL2] Retourne ENOTSUP si le système de fichiers ne prend pas en charge EAs
* [WSL2] Corriger le blocage de \\CopyFile avec \\WSL $
* Changez l’umask par défaut en 0022 et ajoutez le paramètre FileSystem. umask à/etc/WSL.conf
* Corriger wslpath pour résoudre correctement liens symboliques, ceci a été régressé dans 19h1 [GH 4078]
* Introduire le fichier%\.UserProfile% wslconfig pour la modification des paramètres WSL2
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a>Build 18917
Pour obtenir des informations générales sur Windows sur la build 18917, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).

### <a name="wsl"></a>WSL
* WSL 2 est maintenant disponible! Pour plus d’informations, consultez le [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) .
* Corriger une régression où le lancement de processus Windows via liens symboliques ne fonctionnait pas correctement [GH 3999]
* Ajouter WSL. exe--List--verbose, WSL. exe--List--Quiet et WSL. exe--Import--options de version dans WSL. exe
* Ajouter WSL. exe--option d’arrêt
* Plan 9: Autoriser l’ouverture d’un répertoire pour que l’écriture aboutisse

## <a name="build-18890"></a>Build 18890
Pour obtenir des informations générales sur Windows sur la build 18890, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Fuite de socket non bloquant [GH 2913]
* L’entrée EOF du terminal peut bloquer les lectures suivantes [GH 3421]
* Mettez à jour l’en-tête resolv. conf pour faire référence à WSL. conf [abordé dans GH 3928]
* Blocage dans epoll supprimer le code [GH 3922]
* Gérer les espaces dans les arguments pour--import et – Export [GH 3932]
* L’extension des fichiers mmap ne fonctionne pas correctement [GH 3939]
* Résoudre le problème avec \\ARM64 WSL $ Access ne fonctionne pas correctement
* Ajouter une meilleure icône par défaut pour WSL. exe

## <a name="build-18342"></a>Build 18342
Pour obtenir des informations générales sur Windows sur la build 18342, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans un WSL distribution à partir de Windows. Ces fichiers sont accessibles par le biais de la ligne de commande, et les applications Windows, telles que l’Explorateur de fichiers, VSCode, etc., peuvent interagir avec ces fichiers. Accédez à vos fichiers en accédant \\à \\WSL\\$ < distro_name > ou consultez la liste des distributions en cours d’exécution en \\accédant à \\WSL $
* Ajouter des balises d’informations d’UC supplémentaires et corriger les valeurs Cpus_allowed [_list] [GH 2234]
* Prendre en charge exec à partir d’un thread non leader [GH 3800]
* Considérer les échecs de mise à jour de configuration comme non récupérables [GH 3785]
* Mettre à jour binfmt pour gérer correctement les décalages [GH 3768]
* Activer le mappage de lecteurs réseau pour le plan 9 [GH 3854]
* Prise en charge de Windows > Linux et Linux-> de la traduction de chemins d’accès Windows pour les montages de liaison
* Créer des sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule

## <a name="build-18334"></a>Build 18334
Pour obtenir des informations générales sur Windows sur la build 18334, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Remaniement de la façon dont le fuseau horaire Windows est mappé à un fuseau horaire Linux [GH 3747]
* Corriger les fuites de mémoire et ajouter de nouvelles fonctions de traduction de chaînes [GH 3746]
* SIGCONT sur un ThreadGroup sans threads est une absence d’opération [GH 3741] 
* Afficher correctement les descripteurs de fichiers socket et EPoll dans/proc/Self/FD

## <a name="build-18305"></a>Build 18305
Pour obtenir des informations générales sur Windows sur la build 18305, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads perdez l’accès aux fichiers lorsque le thread principal quitte [GH 3589]
* TIOCSCTTY doit ignorer le paramètre «force» à moins qu’il ne soit requis [GH 3652]
* améliorations de la ligne de commande WSL. exe et ajout de fonctionnalités d’importation/exportation.
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
Pour obtenir des informations générales sur Windows sur la build 18277, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Correction de l’erreur «aucune interface non prise en charge» introduite dans la build 18272 [GH 3645]
* Ignorer l’indicateur MNT_FORCE pour umount syscall [GH 3605]
* Basculer l’interopérabilité WSL pour utiliser l’API CreatePseudoConsole officielle
* Ne conserver aucune valeur de délai d’attente lors du redémarrage de FUTEX_WAIT

## <a name="build-18272"></a>Build 18272
Pour obtenir des informations générales sur Windows sur la build 18272, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **TRES** Il y a un problème dans cette Build qui rend WSL inopérant. Lors de la tentative de lancement de votre distribution, une erreur «aucune interface n’est prise en charge» s’affiche. Le problème a été résolu et sera intégré à la version d’Insider Fast de la semaine prochaine. Si vous avez installé cette Build, vous pouvez restaurer la version précédente de Windows à l’aide de «revenir à la version précédente de Windows 10» dans Paramètres-> Update & la récupération de la > de sécurité.

## <a name="build-18267"></a>Build 18267
Pour obtenir des informations générales sur Windows sur la build 18267, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Corrigez le problème où le processus zombie ne peut pas être récolté et rester indéfiniment.
* WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]
* Autoriser fsync à fonctionner correctement pour les fichiers en lecture seule sur DrvFs [GH 3556]
* Vérifiez que les répertoires/bin et/sbin existent avant de créer des liens symboliques dans [GH 3584]
* Ajout d’un mécanisme de délai d’attente d’arrêt d’instance pour les instances WSL. Le délai d’expiration est actuellement défini à 15 secondes, ce qui signifie que l’instance se termine 15 secondes après la fin du dernier processus WSL. Pour arrêter immédiatement une distribution, utilisez:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Build 17763 (1809)
Pour obtenir des informations générales sur Windows sur la build 17763, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* La vérification des autorisations de SetPriority syscall est trop stricte pour modifier la même priorité de thread [GH 1838]
* S’assurer que le temps d’interruption non biaisé est utilisé pour le temps de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime (CLOCK_BOOTTIME) [GH 3434]
* Handle liens symboliques dans l’interpréteur binfmt WSL [GH 3424]
* Meilleure gestion du nettoyage du descripteur de fichier ThreadGroup leader.
* Basculer WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter le dépassement de capacité [GH 3252]
* L’attachement ptrace peut provoquer une valeur de retour incorrecte dans les appels système [GH 1731]
* Correction de plusieurs problèmes liés à AF_UNIX [GH 3371]
* Résoudre le problème qui peut provoquer l’échec de WSL Interop si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]
* Éviter une seconde tentative de connexion de bouclage à des ports inexistants [GH 3286]
* Ajouter un fichier stub/proc/sys/FS/file-max [GH 2893]
* Informations d’étendue IPV6 plus précises.
* Prise en charge de PR_SET_PTRACER [GH 3053]
* Système de fichiers du canal effaçant par inadvertance l’événement epoll déclenché par le bord [GH 3276]
* L’exécutable Win32 lancé via un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]
* Prise en charge améliorée de Zombie [GH 1353]
* Ajouter des entrées WSL. conf pour contrôler le comportement de l’interopérabilité Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correctif pour GetSockName ne retournant pas toujours le type de famille de sockets UNIX [GH 1774]
* Ajout de la prise en charge de TIOCSTI [GH 1863]
* Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]
* Prise en charge de l’interopérabilité sur les disques durs virtuels montés [GH 3246, 3291]
* Résoudre le problème de vérification des autorisations sur le dossier racine [GH 3304]
* Prise en charge limitée des IOCTL du clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.
* Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.
* Ajouter WSL-u ou--User (option) [GH 1203]
* Résoudre les problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]
* Les sockets Unix doivent conserver les informations d’identification homologues déconnectées [GH 3183]
* Échec indéfiniment des sockets Unix non bloquants avec EAGAIN [GH 3191]
* case = OFF est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]
    * Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) .
* Ajoutez wslconfig/Terminate pour arrêter les distributions en cours d’exécution.
* Corrigez le problème avec les entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins d’accès avec des espaces.
* Exposer le respect de la casse par répertoire en tant qu’attribut étendu
* ARM64 Émule les opérations de maintenance du cache. Résolvez le [problème dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: seuls les caractères d’échappement de la plage privée qui correspondent à un caractère d’échappement.
* Correction de l’erreur de validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]
* Les minuteurs absolus WSL avec une heure dans le passé ne se déclenchent pas [GH 3091]
* Vérifiez que les points d’analyse nouvellement créés sont répertoriés comme tels dans le répertoire parent.
* Créez de manière atomique des répertoires sensibles à la casse dans DrvFs.
* Correction d’un problème supplémentaire où les opérations multithread pouvaient retourner ENOENT même si le fichier existe. [GH 2712]
* Correction de l’échec du lancement de WSL lorsque UMCI est activé. [GH 3020]
* Ajouter le menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836]. Pour utiliser, maintenez la touche Maj enfoncée et cliquez avec le bouton droit dans une fenêtre de l’Explorateur.
* Corriger le comportement non bloquant du socket Unix [GH 2822, 3100]
* Correction de la commande NetLink en suspens comme indiqué dans GH 2026.
* Ajoutez la prise en charge des indicateurs de propagation de montage [GH 2911].
* Résoudre le problème avec TRUNCATE not provoquant des événements inotify [GH 2978].
* Add--exec (option) pour WSL. exe afin d’appeler un seul binaire sans Shell.
* L’option Add--distribution de WSL. exe permet de sélectionner un distribution spécifique.
* Prise en charge limitée de dmesg. Les applications peuvent désormais se connecter à dmesg. Le pilote WSL journalise des informations limitées sur dmesg. À l’avenir, il peut être étendu pour transporter d’autres informations/Diagnostics à partir du pilote.
    * Remarque: dmesg est actuellement pris en charge `/dev/kmsg` par le biais de l’interface de l’appareil. `syslog`l’interface syscall n’est pas encore prise en charge. Et, par conséquent, certaines des `dmesg` options de ligne de commande `-S`, `-C` telles que, ne fonctionnent pas.
* Modifier le GID et le mode par défaut des appareils série pour qu’ils correspondent au mode natif [GH 3042]
* DrvFs prend désormais en charge les attributs étendus.
    * Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus. Certains caractères (tels que'/', ': 'et\*' ') ne sont pas autorisés, et les noms d’attributs étendus ne respectent pas la casse sur DrvFs

## <a name="build-18252-skip-ahead"></a>Build 18252 (avance)
Pour obtenir des informations générales sur Windows sur la build 18252, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Déplacer les fichiers binaires init et bsdtar hors de la dll lxssmanager et dans un dossier d’outils distinct
* Corriger la course à la fermeture du descripteur de fichier lors de l’utilisation de CLONE_FILES
* Gérer les champs facultatifs dans/proc/PID/mountinfo lors de la traduction de chemins d’accès DrvFs
* Autoriser DrvFs mknod à fonctionner sans la prise en charge des métadonnées pour S_IFREG
* Les fichiers ReadOnly créés sur DrvFs doivent avoir l’attribut ReadOnly défini [GH 3411]
* Ajouter/sbin/Mount.drvfs Helper pour gérer le montage DrvFs
* Utilisez POSIX Rename dans DrvFs.
* Autorisez la traduction de chemin sur les volumes sans GUID de volume.

## <a name="build-17738-fast"></a>Build 17738 (rapide)
Pour obtenir des informations générales sur Windows sur la build 17738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* La vérification des autorisations de SetPriority syscall est trop stricte pour modifier la même priorité de thread [GH 1838]
* S’assurer que le temps d’interruption non biaisé est utilisé pour le temps de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime (CLOCK_BOOTTIME) [GH 3434]
* Handle liens symboliques dans l’interpréteur binfmt WSL [GH 3424]
* Meilleure gestion du nettoyage du descripteur de fichier ThreadGroup leader.

## <a name="build-17728-fast"></a>Build 17728 (rapide)
Pour obtenir des informations générales sur Windows sur la build 17728, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Basculer WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter le dépassement de capacité [GH 3252]
* L’attachement ptrace peut provoquer une valeur de retour incorrecte dans les appels système [GH 1731]
* Résoudre un certain nombre de problèmes liés à AF_UNIX [GH 3371]
* Résoudre le problème qui peut provoquer l’échec de WSL Interop si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]

## <a name="build-18204-skip-ahead"></a>Build 18204 (avance)
Pour obtenir des informations générales sur Windows sur la build 18204, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Inadvertenly du système de fichiers du canal effacement du bord de l’événement epoll [GH 3276]
* L’exécutable Win32 lancé via un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]

## <a name="build-17723-fast"></a>Build 17723 (rapide)
Pour obtenir des informations générales sur Windows sur la build 17723, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Éviter une seconde tentative de connexion de bouclage à des ports inexistants [GH 3286]
* Ajouter un fichier stub/proc/sys/FS/file-max [GH 2893]
* Informations d’étendue IPV6 plus précises.
* Prise en charge de PR_SET_PTRACER [GH 3053]
* Inadvertenly du système de fichiers du canal effacement du bord de l’événement epoll [GH 3276]
* L’exécutable Win32 lancé via un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]

## <a name="build-17713"></a>Build 17713
Pour obtenir des informations générales sur Windows sur la build 17713, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Prise en charge améliorée de Zombie [GH 1353]
* Ajouter des entrées WSL. conf pour contrôler le comportement de l’interopérabilité Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correctif pour GetSockName ne retournant pas toujours le type de famille de sockets UNIX [GH 1774]
* Ajout de la prise en charge de TIOCSTI [GH 1863]
* Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]
* Prise en charge de l’interopérabilité sur les disques durs virtuels montés [GH 3246, 3291]
* Résoudre le problème de vérification des autorisations sur le dossier racine [GH 3304]
* Prise en charge limitée des IOCTL du clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.
* Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.

## <a name="build-17704"></a>Build 17704
Pour obtenir des informations générales sur Windows sur la build 17704, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Ajouter WSL-u ou--User (option) [GH 1203]
* Résoudre les problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]
* Les sockets Unix doivent conserver les informations d’identification homologues déconnectées [GH 3183]
* Échec indéfiniment des sockets Unix non bloquants avec EAGAIN [GH 3191]
* case = OFF est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]
    * Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) .
* Ajoutez wslconfig/Terminate pour arrêter les distributions en cours d’exécution.

## <a name="build-17692"></a>Build 17692
Pour obtenir des informations générales sur Windows sur la build 17692, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Corrigez le problème avec les entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins d’accès avec des espaces.
* Exposer le respect de la casse par répertoire en tant qu’attribut étendu
* ARM64 Émule les opérations de maintenance du cache. Résolvez le [problème dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs: seuls les caractères d’échappement de la plage privée qui correspondent à un caractère d’échappement.

## <a name="build-17686"></a>Build 17686
Pour obtenir des informations générales sur Windows sur la build 17686, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Correction de l’erreur de validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]
* Les minuteurs absolus WSL avec une heure dans le passé ne se déclenchent pas [GH 3091]
* Vérifiez que les points d’analyse nouvellement créés sont répertoriés comme tels dans le répertoire parent.
* Créez de manière atomique des répertoires sensibles à la casse dans DrvFs.

## <a name="build-17677"></a>Build 17677
Pour obtenir des informations générales sur Windows sur la build 17677, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Correction d’un problème supplémentaire où les opérations multithread pouvaient retourner ENOENT même si le fichier existe. [GH 2712]
* Correction de l’échec du lancement de WSL lorsque UMCI est activé. [GH 3020]

## <a name="build-17666"></a>Build 17666
Pour obtenir des informations générales sur Windows sur la build 17666, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>AVERTISSEMENT : Un problème empêche WSL de s’exécuter sur certains chipsets AMD [GH 3134]. Un correctif est prêt et fait de même pour la branche de génération Insider.
* Ajouter le menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836]. Pour utiliser maintenir la touche Maj et cliquer avec le bouton droit dans une fenêtre de l’Explorateur.
* Corriger le comportement non bloquant du socket Unix [GH 2822, 3100]
* Correction de la commande NetLink en suspens comme indiqué dans GH 2026.
* Ajoutez la prise en charge des indicateurs de propagation de montage [GH 2911].
* Résoudre le problème avec TRUNCATE not provoquant des événements inotify [GH 2978].
* Add--exec (option) pour WSL. exe afin d’appeler un seul binaire sans Shell.
* L’option Add--distribution de WSL. exe permet de sélectionner un distribution spécifique.

## <a name="build-17655-skip-ahead"></a>Build 17655 (avance)
Pour obtenir des informations générales sur Windows sur la build 17655, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Prise en charge limitée de dmesg. Les applications peuvent désormais se connecter à dmesg. Le pilote WSL journalise des informations limitées sur dmesg. À l’avenir, il peut être étendu pour transporter d’autres informations/Diagnostics à partir du pilote.
    * Remarque: dmesg est actuellement pris en charge `/dev/kmsg` par le biais de l’interface de l’appareil. `syslog`l’interface sycall n’est pas encore prise en charge. Et, par conséquent, certaines des `dmesg` options de ligne de commande `-S`, `-C` telles que, ne fonctionnent pas.
* Correction d’un problème où les opérations multithread pouvaient retourner ENOENT même si le fichier existe. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Build 17639 (avance)
Pour obtenir des informations générales sur Windows sur la build 17639, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Modifier le GID et le mode par défaut des appareils série pour qu’ils correspondent au mode natif [GH 3042]
* DrvFs prend désormais en charge les attributs étendus.
    * Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus. En particulier, certains caractères (tels que'/', ': 'et\*' ') ne sont pas autorisés, et les noms d’attributs étendus ne respectent pas la casse sur DrvFs

## <a name="build-17133-fast"></a>Build 17133 (rapide)
Pour obtenir des informations générales sur Windows sur la build 17133, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Correction du blocage dans WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Build 17128 (rapide)
Pour obtenir des informations générales sur Windows sur la build 17128, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Aucun

## <a name="build-17627-skip-ahead"></a>Build 17627 (avance)
Pour obtenir des informations générales sur Windows sur la build 17627, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Ajoutez la prise en charge des opérations compatibles Futex pi. [GH 1006]
    * Notez que les priorités ne sont actuellement pas une fonctionnalité de WSL prise en charge. il existe donc des limitations, mais l’utilisation standard doit être débloquée.
* Prise en charge du pare-feu Windows pour les processus WSL. [GH 1852]
    * Par exemple, pour autoriser le processus python WSL à écouter sur n’importe quel port, utilisez la commande Windows avec élévation de privilèges:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respectez le shell par défaut de l’utilisateur lors de l’utilisation de WSL. exe. [GH 2372]
* Signale toutes les interfaces réseau comme Ethernet. [GH 2996]
* Meilleure gestion des fichiers/etc/passwd endommagés. [GH 3001]

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17618-skip-ahead"></a>Build 17618 (avance)
Pour obtenir des informations générales sur Windows sur la build 17618, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introduisez la fonctionnalité pseudoconsole pour l’interopérabilité NT [GH 988, 1366, 1433, 1542, 2370, 2406].
* Le mécanisme d’installation hérité (lxrun. exe) est déconseillé. Le mécanisme pris en charge pour l’installation des distributions s’effectue via le Microsoft Store.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17110"></a>Build 17110
Pour obtenir des informations générales sur Windows sur la build 17110, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Autorisez l’arrêt de/init à partir de Windows [GH 2928].
* DrvFs utilise désormais le respect de la casse par répertoire par défaut (équivaut à l’option de montage «case = dir»).
    * L’utilisation de «case = force» (l’ancien comportement) requiert la définition d’une clé de registre. Exécutez la commande suivante pour activer «case = force» si vous devez l’utiliser: reg Add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui doivent respecter la casse, utilisez fsutil. exe pour les marquer comme respectant la casse: fsutil <path> . exe file setcasesensitiveinfo Enable
* Chaînes de fin NULL retournées par le commande uname syscall.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17107"></a>Build 17107
Pour obtenir des informations générales sur Windows sur la build 17107, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Prise en charge de TCSETSF et TCSETSW sur les points de terminaison du PTY maître [GH 2552].
* Le démarrage de processus d’interopérabilité simultanés peut entraîner la EINVAL [GH 2813].
* Corriger PTRACE_ATTACH pour afficher l’état de suivi approprié dans/proc/PID/Status.
* Corriger la concurrence où les processus de courte durée clonés avec les indicateurs CLEARTID et SETTID peuvent quitter sans effacer l’adresse TID.
* Affiche un message lors de la mise à niveau des répertoires du système de fichiers Linux lors du déplacement à partir d’une build antérieure à 17093. Pour plus d’informations sur les modifications du système de fichiers 17093, consultez les notes de publication de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17101"></a>Build 17101
Pour obtenir des informations générales sur Windows sur la build 17101, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Prise en charge de signalfd. [GH 129]
* Prennent en charge les noms de fichier contenant des caractères NTFS non conformes en les codant comme des caractères Unicode privés. [GH 1514]
* Le montage automatique est en lecture seule lorsque l’écriture n’est pas prise en charge. [GH 2603]
* Autoriser le collage de paires de substitution Unicode (comme les caractères Emoji). [GH 2765]
* Les Pseudo-fichiers dans/proc et/sys doivent retourner lecture et écriture prêts à partir de Select, Poll, epoll, et al. [GH 2838]
* Corrigez le problème qui peut amener le service à passer en boucle infinie lorsque le registre a été falsifié ou qu’il est endommagé.
* Corrigez les messages NetLink pour qu’ils fonctionnent avec la version plus récente (en amont 4,14) de iproute2.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17093"></a>Build 17093
Pour obtenir des informations générales sur Windows sur la build 17093, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Important :
Quand vous démarrez WSL pour la première fois après la mise à niveau vers cette Build, vous devez effectuer une mise à niveau des répertoires du système de fichiers Linux. Cela peut prendre plusieurs minutes. par conséquent, WSL peut sembler démarrer lentement. Cela ne doit se produire qu’une seule fois pour chaque distribution que vous avez installée à partir du magasin.
* Prise en charge améliorée du respect de la casse dans DrvFs.
    * DrvFs prend désormais en charge le respect de la casse par répertoire. Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme respectant la casse, ce qui permet même aux applications Windows d’ouvrir correctement les fichiers qui diffèrent uniquement par la casse.
    * DrvFs dispose de nouvelles options de montage contrôlant le respect de la casse par répertoire
        * case = force: tous les répertoires sont traités comme respectant la casse (à l’exception de la racine du lecteur). Les nouveaux répertoires créés avec WSL sont marqués en respectant la casse. Il s’agit du comportement hérité, à l’exception du marquage de nouveaux répertoires sensibles à la casse.
        * case = dir: seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme respectant la casse; les autres répertoires ne respectent pas la casse. Les nouveaux répertoires créés avec WSL sont marqués en respectant la casse.
        * case = OFF: seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme respectant la casse; les autres répertoires ne respectent pas la casse. Les nouveaux répertoires créés avec WSL sont marqués comme non sensibles à la casse.
    * Remarque: cet indicateur n’est pas défini pour les répertoires créés par WSL dans les versions précédentes, donc ils ne seront pas traités comme respectant la casse si vous utilisez l’option «case = dir». Un moyen de définir cet indicateur sur des répertoires existants sera bientôt disponible.
    * Exemple de montage avec ces options (pour les lecteurs existants, vous devez d’abord démonter avant de pouvoir monter avec des options différentes): sudo mount-t drvfs C:/mnt/c-o case = dir
    * Pour le moment, case = force est toujours l’option par défaut. Celui-ci sera remplacé par case = dir dans le futur.
* Vous pouvez maintenant utiliser des barres obliques dans les chemins d’accès Windows lors du montage de DrvFs, par exemple: sudo mount-t DrvFs//Server/Share/mnt/share
* WSL traite maintenant le fichier/etc/fstab au démarrage de l’instance [GH 2636].
    * Cette opération est effectuée avant le montage automatique des lecteurs DrvFs. les lecteurs déjà montés par fstab ne sont pas remontés automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.
    * Ce comportement peut être désactivé à l’aide de WSL. conf.
* Les fichiers Mount, mountinfo et mountstats dans/proc échappent correctement aux caractères spéciaux tels que les barres obliques inverses et les espaces [GH 2799]
* Les fichiers spéciaux créés avec DrvFs tels que les liens symboliques WSL, ou FIFO et sockets lorsque les métadonnées sont activées, peuvent maintenant être copiés et déplacés de Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL est plus configurable avec WSL. conf
Nous avons ajouté une méthode vous permettant de configurer automatiquement certaines fonctionnalités dans WSL qui seront appliquées chaque fois que vous lancerez le sous-système. Cela comprend les options de montage automatique et la configuration réseau. Pour en savoir plus, consultez notre billet de blog à l’adresse suivante: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX autorise les connexions de socket entre les processus Linux sur WSL et les processus natifs Windows
Les applications WSL et Windows peuvent désormais communiquer entre elles via des sockets Unix. Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible pour les applications Windows et WSL. Désormais, il est possible d’utiliser des sockets Unix. Pour en savoir plus, consultez notre billet de blog à l’adresse https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Prise en charge de mmap () avec MAP_NORESERVE [GH 121, 2784]
* Prise en charge de CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]
* Gérer le signal de fin non SIGCHLD dans le clone [GH 121, 2781]
* Stub/proc/sys/FS/inotify/max_user_instances et/proc/sys/FS/inotify/max_user_watches [GH 1705]
* Erreur lors du chargement des binaires ELF qui contiennent des en-têtes de charge avec des décalages non nuls [GH 1884]
* Zéro pour les octets de page de fin lors du chargement des images.
* Réduire les cas où execve arrête silencieusement le processus

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17083"></a>Build 17083
Pour obtenir des informations générales sur Windows sur la build 17083, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Correction de la vérification de bogue liée à epoll [GH 2798, 2801, 2857]
* Correction des blocages lors de la désactivation de ASLR [GH 1185, 2870]
* S’assurer que les opérations mmap apparaissent atomiques [GH 2732]

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17074"></a>Build 17074
Pour obtenir des informations générales sur Windows sur la build 17074, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Format de stockage fixe des métadonnées DrvFs [GH 2777] </br>
**Important :** Les métadonnées DrvFs créées avant cette génération s’affichent de manière incorrecte ou pas du tout. Pour corriger les fichiers affectés, utilisez chmod et chown pour réappliquer les métadonnées.
* Correction du problème avec plusieurs signaux et syscalls redémarrable.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17063"></a>Build 17063
Pour obtenir des informations générales sur Windows sur la build 17063, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs prend en charge des métadonnées Linux supplémentaires. Cela permet de définir le propriétaire et le mode des fichiers à l’aide de chmod/chown, ainsi que la création de fichiers spéciaux, tels que les FIFO, les sockets Unix et les fichiers d’appareil. Cela est désactivé par défaut pour le moment, car il est toujours expérimental.
**Remarque :**  Nous avons résolu un bogue dans le format de métadonnées utilisé par DrvFs. Bien que les métadonnées fonctionnent sur cette build pour l’expérimentation, les builds ultérieures ne lisent pas correctement les métadonnées créées par cette Build.  Vous devrez peut-être mettre à jour manuellement le propriétaire des fichiers et des appareils modifiés avec un ID d’appareil personnalisé doit être recréé.

  Pour activer, montez DrvFs avec l’option Metadata (pour l’activer sur un montage existant, vous devez d’abord le démonter):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Les autorisations Linux sont ajoutées en tant que métadonnées supplémentaires au fichier; ils n’affectent pas les autorisations Windows.  N’oubliez pas que la modification d’un fichier à l’aide d’un éditeur Windows peut supprimer les métadonnées. Dans ce cas, le fichier reprend ses autorisations par défaut.

* Ajout d’options de montage à DrvFs pour contrôler les fichiers sans métadonnées.
  * UID: ID utilisateur utilisé pour le propriétaire de tous les fichiers.
  * GID: ID de groupe utilisé pour le propriétaire de tous les fichiers.
  * umask: masque octal d’autorisations à exclure pour tous les fichiers et répertoires.
  * fmask: masque octal d’autorisations à exclure pour tous les fichiers normaux.
  * dmask: masque octal d’autorisations à exclure pour tous les répertoires.

  Exemple :
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combinez avec l’option de métadonnées pour spécifier des autorisations par défaut pour les fichiers sans métadonnées.

* A introduit une nouvelle variable d' `WSLENV`environnement,, pour configurer le mode de passage des variables d’environnement entre WSL et Win32.

  Exemple :

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`liste de variables d’environnement séparées par des virgules qui peuvent être incluses lors du lancement de processus WSL à partir de processus Win32 ou Win32 à partir de WSL.  Chaque variable peut être suivie d’un suffixe à l’aide d’une barre oblique suivie de balises pour spécifier la façon dont elle est traduite.
  * p La valeur est un chemin d’accès qui doit être traduit entre les chemins d’accès WSL et les chemins d’accès Win32.
  * budget La valeur est une liste de chemins d’accès. Dans WSL, il s’agit d’une liste délimitée par des points-virgules. Dans Win32, il s’agit d’une liste délimitée par des points-virgules.
  * GOUDJARATI La valeur doit être incluse uniquement lors de l’appel de WSL à partir de Win32
  * s La valeur doit être incluse uniquement lors de l’appel de Win32 à partir de WSL

  Vous pouvez définir `WSLENV` in. bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.

* les montages drvfs préservent correctement les horodateurs de tar, CP-p (GH 1939)
* drvfs liens symboliques signale la taille correcte (GH 2641)
* la lecture/écriture fonctionne pour les très grandes tailles d’e/s (GH 2653)
* waitpid fonctionne avec des ID de groupe de processus (GH 2534)
* amélioration significative des performances de mmap pour les régions de réserve volumineuses; améliore les performances de GHC (GH 1671)
* la personnalité prend en charge READ_IMPLIES_EXEC; corrige les maxima et les clisp (GH 1185)
* mprotect prend en charge PROT_GROWSDOWN; résout clisp (GH 1128)
* correction des erreurs de page en mode de survalidation; résout sbcl (GH 1128)
* le clone prend en charge davantage de combinaisons d’indicateurs
* Prend en charge Select/epoll de fichiers epoll (auparavant un non-op).
* Notifier ptrace des syscalls non implémentés.
* Ignorer les interfaces qui ne sont pas installées lors de la génération de noms de resolv. conf [GH 2694]
* Énumérer les interfaces réseau sans adresse physique. [GH 2685]
* Améliorations et correctifs de bogues supplémentaires.

### <a name="linux-tools-available-to-developers-on-windows"></a>Outils Linux disponibles pour les développeurs sur Windows

* La ligne de commande Windows chaîne d’outils comprend bsdtar (tar) et une boucle.
  Lisez [ce blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et découvrir comment ils conforment l’expérience des développeurs sur Windows.

*   `AF_UNIX`est disponible dans le kit de développement logiciel (SDK) Windows Insider (17061 +).
  Lisez [ce blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus `AF_UNIX` sur et sur la manière dont les développeurs sur Windows peuvent l’utiliser.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.


## <a name="build-17046"></a>Build 17046

Pour obtenir des informations générales sur Windows sur la build 17046, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Autoriser les processus à s’exécuter sans terminal actif. [GH 709, 1007, 1511, 2252, 2391, et al.]
- Meilleure prise en charge de CLONE_VFORK et CLONE_VM. [GH 1878, 2615]
- Ignorez les pilotes de filtre TDI pour les opérations de mise en réseau WSL. [GH 1554]
- DrvFs crée une liens symboliques NT lorsque certaines conditions sont remplies. [GH 353, 1475, 2602]
    - La cible du lien doit être relative, ne doit pas traverser les points de montage ou les liens symboliques et doit exister.
    - L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela nécessite normalement que vous lançiez WSL. exe avec élévation de privilèges), à moins que le mode développeur soit activé.
    - Dans toutes les autres situations, DrvFs crée toujours WSL liens symboliques.
- Autorisez l’exécution simultanée d’instances WSL avec élévation de privilèges et non élevées.
- Prise en charge/proc/sys/kernel/yama/ptrace_scope
- Ajoutez wslpath pour effectuer des conversions de chemins d’accès Windows > <. [GH 522, 1243, 1834, 2327, et al.]
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

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.


## <a name="build-17040"></a>Build 17040

Pour obtenir des informations générales sur Windows sur la build 17040, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Aucun correctif depuis 17035.

#### <a name="console"></a>Console
- Aucun correctif depuis 17035.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17035"></a>Build 17035

Pour obtenir des informations générales sur Windows sur la build 17035, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- L’accès aux fichiers sur DrvFs peut parfois échouer avec EINVAL. [GH 2448]

#### <a name="console"></a>Console
- Perte de couleur lors de l’insertion/suppression de lignes en mode VT.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17025"></a>Build 17025

Pour obtenir des informations générales sur Windows sur la build 17025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Démarrer les processus initiaux dans un nouveau groupe de processus de premier plan [GH 1653, 2510].
- Correctifs de remise SIGHUP [GH 2496].
- Générez un nom de pont virtuel par défaut s’il n’est pas fourni [GH 2497].
- Implémentez/proc/sys/kernel/Random/boot_id [GH 2518].
- Autres correctifs de canal stdout/stderr Interop.
- Appel système syncfs stub.

#### <a name="console"></a>Console
- Correction de la traduction VT d’entrée pour les consoles tierces [GH 111]

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="build-17017"></a>Build 17017

Pour obtenir des informations générales sur Windows sur la build 17017, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Ignorer les en-têtes de programme ELF vides [GH 330].
- Autoriser LxssManager à créer des instances WSL pour les utilisateurs non interactifs (SSH et prise en charge des tâches planifiées) [GH 777, 1602].
- Prise en charge des scénarios WSL-> Win32-> WSL («création») [GH 1228].
- Prise en charge limitée de l’arrêt des applications console appelées par le biais de l’interopérabilité [GH 1614].
- Options de montage de prise en charge pour devpts [GH 1948].
- Ptrace bloquant le démarrage enfant [GH 2333].
- EPOLLET manquant certains événements [GH 2462].
- Retourne plus de données pour PTRACE_GETSIGINFO.
- Getdents avec lseek donne des résultats incorrects.
- Corriger certaines interruptions de l’application d’interopérabilité Win32, en attente d’une entrée sur un canal qui n’a plus de données.
- Prise en charge O_ASYNC pour les fichiers TTY/Pty.
- Améliorations supplémentaires et correctifs de bogues

#### <a name="console"></a>Console
- Aucune modification de la console dans cette version.

### <a name="ltp-results"></a>Résultats de LTP:
Test en cours.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>Build 16288

Pour obtenir des informations générales sur Windows sur la build 16288, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Initialisez et signalez correctement uid, GID et mode pour les descripteurs de fichiers socket [GH 2490]
- Améliorations supplémentaires et correctifs de bogues

#### <a name="console"></a>Console
- Aucune modification de la console dans cette version.

### <a name="ltp-results"></a>Résultats de LTP:
Aucune modification depuis 16273

## <a name="build-16278"></a>Build 16278

Pour obtenir des informations générales sur Windows sur la build 162738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Annuler le mappage explicite des vues mappées des sections sauvegardées dans un fichier lors du déchirement de l’État LX MM [GH 2415]
- Améliorations supplémentaires et correctifs de bogues

#### <a name="console"></a>Console
- Aucune modification de la console dans cette version.

### <a name="ltp-results"></a>Résultats de LTP:
Aucune modification depuis 16273

## <a name="build-16275"></a>Build 16275

Pour obtenir des informations générales sur Windows sur la build 162735, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Aucune modification liée à WSL dans cette version.

#### <a name="console"></a>Console
- Aucune modification de la console dans cette version.

### <a name="ltp-results"></a>Résultats de LTP:
Aucune modification depuis 16273

## <a name="build-16273"></a>Build 16273

Pour obtenir des informations générales sur Windows sur la build 16273, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Résolution d’un problème où DrvFs a parfois signalé un type de fichier incorrect pour les répertoires [GH 2392]
- Autoriser la création de sockets NETLINK_KOBJECT_UEVENT pour débloquer des programmes qui utilisent UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Ajout de la prise en charge de la connexion non bloquante [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implémenter l’indicateur d’appel système CLONE_FS Clone [GH 2242]
- Résoudre les problèmes liés à la non-gestion des tabulations ou des guillemets correctement dans l’interopérabilité NT [GH 1625, 2164]
- Erreur de résolution de l’accès refusé lors de la tentative de redémarrage des instances WSL [GH 651, 2095]
- Implémenter des opérations Futex FUTEX_REQUEUE et FUTEX_CMP_REQUEUE [GH 2242]
- Corriger les autorisations pour différents fichiers SysFs [GH 2214]
- Corriger le blocage de la pile Haskell lors de l’installation [GH 2290]
- Implémenter les indicateurs binfmt_misc’C' 'O’et’P' [GH 2103]
- Add/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]
- Ajout de la prise en charge partielle de l’appel système ioprio_set [GH 498]
- Stub SO_REUSEPORT & ajout de la prise en charge de SO_PASSCRED pour les sockets NetLink [GH 69]
- Retourner des codes d’erreur différents à partir de RegisterDistribuiton si une distribution est en cours d’installation ou de désinstallation.
- Autoriser la désinscription des distributions WSL partiellement installées via wslconfig. exe
- Corriger le blocage du test de socket Python à partir de UDP:: MSG_PEEK
- Améliorations supplémentaires et correctifs de bogues

#### <a name="console"></a>Console
- Aucune modification de la console dans cette version.

### <a name="ltp-results"></a>Résultats de LTP:
Nombre total de tests: 1904<br/>
Nombre total de tests ignorés: 209<br/>
Nombre total d’échecs: 229<br/>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Build 16257

Pour obtenir des informations générales sur Windows sur la build 16257, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Implémenter un appel système prlimit64
- Ajout de la prise en charge de commande ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Stub MSG_MORE pour les sockets TCP [GH 2351]
- Corriger le comportement de vecteur auxiliaire AT_EXECFN non valide [GH 2133]
- Corriger le comportement de copier/coller pour console/TTY et ajouter une meilleure gestion de mémoire tampon complète [GH 2204, 2131]
- Définir AT_SECURE dans le vecteur auxiliaire pour les programmes Set-User-ID et Set-Group-ID [GH 2031]
- Psuedo-point de terminaison du contrôleur de terminal non géré TIOCPGRP [GH 1063]
- Fix lseek effectue le rembobinage des répertoires dans LxFs [GH 2310]
- /dev/ptmx se bloque après une utilisation intensive [GH 1882]
- Améliorations supplémentaires et correctifs de bogues

#### <a name="console"></a>Console
- Correction pour les lignes/traits de soulignement horizontaux partout [GH 2168]
- Correction de l’ordre du processus modification rendant la NPM plus difficile à fermer [GH 2170]
- Ajout de notre nouveau jeu de couleurs: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>Résultats de LTP:
Aucune modification depuis 16251

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`prlimit64`<br/>

### <a name="known-issues"></a>Problèmes connus
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub problème 2392: Dossiers Windows non reconnus par WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
Dans la build 16257, WSL rencontre des problèmes lors de l’énumération des `/mnt/c/...`fichiers/dossiers Windows via.
Ce problème a été résolu et doit être publié dans le cadre de la génération de la version de la semaine à partir de 8/14/2017.

<br/>

## <a name="build-16251"></a>Build 16251

Pour obtenir des informations générales sur Windows sur la build 16251, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Supprimez la balise bêta du composant facultatif WSL. pour plus d’informations, consultez le billet de [blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) .
- Initialisez correctement l’UID et le GID enregistrés pour les fichiers binaires Set-User-ID et Set-Group-ID sur exec [GH 962, 1415, 2072]
- Ajout de la prise en charge de ptrace PTRACE_O_TRACEEXIT [GH 555]
- Ajout de la prise en charge de ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]
- Correction des ptrace à arrêter sur les signaux ignorés
- Améliorations supplémentaires et correctifs de bogues

#### <a name="console"></a>Console
- Aucune modification de la console dans cette version.

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 768</br>
Nombre de tests ayant échoué: 244</br>
Nombre de tests ignorés: 96</br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Build 16241

Pour obtenir des informations générales sur Windows sur la build 16241, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Résolution
#### <a name="wsl"></a>WSL
- Aucune modification liée à WSL dans cette version.

#### <a name="console"></a>Console
- Correction pour la génération d’un mauvais caractère pour le franchissement des lignes DEC, initialement signalé [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- Correctif pour aucun texte de sortie affiché dans la page de codes 65001 (UTF8)
- Ne transférez pas les modifications apportées aux valeurs RVB d’une couleur vers d’autres parties de la palette lors de la modification de la sélection. Cela rendra la feuille de propriétés de la console beaucoup plus facile à utiliser.
- CTRL + S ne semble pas fonctionner correctement
- Non gras/-Dim totalement absent des codes d’échappement ANSI [GH 2174]
- La console ne prend pas en charge correctement les thèmes de couleur vim [GH 1706]
- Impossible de coller des caractères particuliers [GH 2149]
- Le redimensionnement du redimensionnement interagit de façon étrange avec le redimensionnement d’une fenêtre bash quand des éléments se trouvent sur la ligne de commande Edit/Command [GH ConEmu 1123]
- Ctrl-L laisse l’écran sale [GH 1978]
- Bogue de rendu de la console lors de l’affichage de VT sur HDPI [GH 1907]
- Les caractères Japansese semblent étranges avec le caractère Unicode U + 30FB [GH 2146]
- Améliorations supplémentaires et correctifs de bogues

</br>

## <a name="build-16237"></a>Build 16237

Pour obtenir des informations générales sur Windows sur la build 16237, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Résolution
- Utiliser des attributs par défaut pour les fichiers sans EAs dans lxfs (racine, racine, 0000)
- Ajout de la prise en charge des distributions qui utilisent des attributs étendus
- Correction du remplissage pour les entrées retournées par getdents et getdents64
- Correction des autorisations pour l’appel système shmctl SHM_STAT [GH 2068]
- Correction de l’État epoll initial incorrect pour les TTY ne [GH 2231]
- Fix DrvFs readdir ne retournant pas toutes les entrées [GH 2077]
- Corriger LxFs readdir lorsque des fichiers sont dissociés [GH 2077]
- Autoriser la réouverture des fichiers drvfs non liés via procfs
- Ajout d’un remplacement de clé de registre global pour la désactivation des fonctionnalités WSL (montage d’interopérabilité/lecteur)
- Correction du nombre de blocs incorrects dans «STAT» pour DrvFs (et LxFs) [GH 1894]
- Améliorations supplémentaires et correctifs de bogues

</br>

## <a name="build-16232"></a>Build 16232

Pour obtenir des informations générales sur Windows sur la build 16232, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Résolution
- Aucune modification liée à WSL dans cette version.

</br>

## <a name="build-16226"></a>Build 16226

Pour obtenir des informations générales sur Windows sur la build 16226, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Résolution
- prise en charge d’syscalls xattr associée (getxattr, setxattr, listxattr, removexattr).
- la prise en charge de Security. capablity xattr.
- Compatibilité améliorée avec certains filtres et systèmes de fichiers, y compris les serveurs SMB non-MS. [GH #1952]
- Prise en charge améliorée des espaces réservés OneDrive, des espaces réservés GVFS et des fichiers compressés compact OS.
- Améliorations supplémentaires et correctifs de bogues

</br>

## <a name="build-16215"></a>Build 16215

Pour obtenir des informations générales sur Windows sur la build 16215, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Résolution
- WSL ne requiert plus le mode développeur.
- Prendre en charge les jonctions de répertoires dans drvfs.
- Gérez la désinstallation des packages AppX de distribution WSL.
- Mettez à jour procfs pour afficher les mappages privés et partagés.
- Ajoutez la possibilité pour wslconfig. exe de nettoyer les distributions partiellement installées ou désinstallées.
- Ajout de la prise en charge de IP_MTU_DISCOVER pour les sockets TCP. [GH 1639, 2115, 2205]
- Déduire la famille de protocoles pour les itinéraires vers AF_INADDR.
- Améliorations des appareils série [GH 1929].

</br>

## <a name="build-16199"></a>Build 16199

Pour obtenir des informations générales sur Windows sur la build 16199, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Résolution
- Aucune modification liée à WSL dans ces versions.

</br>

## <a name="build-16193"></a>Build 16193

Pour obtenir des informations générales sur Windows sur la build 16193, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Résolution
- Condition de concurrence entre l’envoi de SIGCONT et l’arrêt d’un ThreadGroup [GH 1973]
- modifier les appareils TTY et Pty pour signaler FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]
- Correctif SSH pour IP_OPTIONS
- Montage DrvFs déplacé vers le démon init [GH 1862, 1968, 1767, 1933]
- Ajout de la prise en charge dans DrvFs pour NT liens symboliques suivant.

</br>

## <a name="build-16184"></a>Build 16184

Pour obtenir des informations générales sur Windows sur la build 16184, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Résolution
- Suppression de la tâche de maintenance de package APT (lxrun. exe/Update)
- Correction de la sortie non affichée dans à partir des processus Windows dans node. js [GH 1840]
- Assouplir les exigences d’alignement dans lxcore [GH 1794]
- Correction de la gestion de l’indicateur AT_EMPTY_PATH dans un nombre d’appels système.
- Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts entraînera un comportement non défini du fichier [GH 544, 966, 1357, 1535, 1615]
- /etc/hosts hérite désormais des entrées du fichier hosts Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Build 16179

Pour obtenir des informations générales sur Windows sur la build 16179, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Résolution
- Aucune modification de WSL cette semaine.

</br>

## <a name="build-16176"></a>Build 16176

Pour obtenir des informations générales sur Windows sur la build 16176, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Résolution

- [Prise en charge série activée](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Ajout de l’option de socket IP IP_OPTIONS [GH 1116]
- Mise en œuvre de la fonction pwritev (lors du chargement du fichier dans Nginx/PHP-FPM) [GH 1506]
- Ajout d’options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- Prise en charge de l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- Ajout de l’option de socket IP (V6) _MTU pour les applications nœud, traceroute, creuser, nslookup, hôte
- Ajout de l’option de socket IP IPV6_UNICAST_HOPS
- [Améliorations du système de fichiers](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Autoriser le montage de chemins d’accès UNC
    * Activer la prise en charge de CDFS dans drvfs
    * Gérer correctement les autorisations pour les systèmes de fichiers réseau dans drvfs
    * Ajouter la prise en charge des lecteurs distants à drvfs
    * Activer la prise en charge de FAT dans drvfs
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP
Aucune modification depuis 15042

</br>

## <a name="build-16170"></a>Build 16170

Pour obtenir des informations générales sur Windows sur la build 16170, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Nous avons publié un nouveau billet de [blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) traitant de nos efforts pour tester WSL.

### <a name="fixed"></a>Résolution

- Option de socket de support IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- Ajoutez la prise en charge de PTRACE_OLDSETOPTIONS. [GH 1692]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP
Aucune modification depuis 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Build 15046 pour Windows 10 Creators Update
Il n’y a plus de correctifs ou de fonctionnalités WSL prévus pour être inclus dans les créateurs de mise à jour de Windows 10. Les notes de publication pour WSL reprennent dans les semaines à venir pour les ajouts ciblant les Windows Update majeures suivantes. Pour obtenir des informations générales sur Windows sur la build 15046 et les versions ultérieures de l’Insider, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Build 15042

Pour obtenir des informations générales sur Windows sur la build 15042, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Résolution

- Correction d’un blocage lors de la suppression d’un chemin d’accès se terminant par «..»
- Correction d’un problème où FIONBIO ne retourne pas 0 en cas de réussite [GH 1683]
- Résolution du problème avec les lectures de longueur nulle des sockets de datagramme inet
- Résoudre le blocage possible en raison d’une condition de concurrence dans drvfs inode Lookup [GH 1675]
- Prise en charge étendue des données auxiliaires de socket Unix; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 737</br>
Nombre de non-passage (échec, ignoré, etc.): 255

</br>

## <a name="build-15031"></a>Build 15031

Pour obtenir des informations générales sur Windows sur la build 15031, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Résolution

- Correction d’un bogue où le point (2) se comporterait de façon sporadique.
- Correction et problème où * SIGPROCMASK syscalls peut corrompre un masque de signal.
- Retournez à présent la longueur de la ligne de commande dans la notification de création de processus WSL. [GH 1632]
- WSL signale désormais la sortie du thread via ptrace pour les blocages de GDB. [GH 1196]
- Correction du bogue où PTYs se bloque après des e/s tmux élevées. [GH 1358]
- Validation du délai d’attente fixe dans de nombreux appels système (Futex, SEMTIMEDOP, ppoll, sigtimedwait, itimer, timer_create)
- Ajout de la prise en charge de EFD_SEMAPHORE eventfd [GH 452]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 737</br>
Nombre de non-passage (échec, ignoré, etc.): 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Build 15025

Pour obtenir des informations générales sur Windows sur la build 15025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Résolution

- Correction du bogue qui a enfreint grep 2,27 [GH 1578]
- Implémentation de l’indicateur EFD_SEMAPHORE pour eventfd2 syscall [GH 452]
- Implemented/proc/[PID]/net/ipv6_route [GH 1608]
- Prise en charge des e/s par signal pour les sockets de flux UNIX [GH 393, 68]
- Prise en charge de F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]
- Implémenter recvmmsg () syscall [GH 1531]
- Correction du bogue où epoll_wait () n’attendait pas [GH 1609]
- Implémenter/proc/version_signature
- Tee syscall retourne désormais une erreur si les deux descripteurs de fichiers font référence au même canal
- Implémentation du comportement correct pour SO_PEERCRED pour les sockets Unix
- Correction de la gestion des paramètres non valides tkill syscall
- Modifications pour augmenter la preformace de drvfs
- Correctif mineur pour le blocage des e/s Ruby
- Fixed recvmsg () retournant EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 732</br>
Nombre de non-passage (échec, ignoré, etc.): 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Build 15019

Pour obtenir des informations générales sur Windows sur la build 15019, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Résolution

- Correction du bogue qui signalait incorrectement l’utilisation de l’UC dans procfs pour les outils tels que htop (GH 823, 945, 971)
- Lors de l’appel de Open () avec O_TRUNC sur un fichier existant, inotify génère désormais IN_MODIFY avant IN_OPEN
- Correctifs du socket Unix getsockopt SO_ERROR pour activer les postgres [GH 61, 1354]
- Implémenter/proc/sys/net/Core/SOMAXCONN pour le langage GO
- La tâche en arrière-plan apt-obtenir le package s’exécute désormais à partir de l’affichage
- Effacez l’étendue de l’hôte IPv6 localhost (défaillance de l’infrastructure à ressort (Java)).
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 714 </br>
Nombre de non-passage (échec, ignoré, etc.): 249 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Build 15014

Pour obtenir des informations générales sur Windows sur la build 15014, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Résolution

- Ctrl + C fonctionne à présent comme prévu
- htop et PS auxw affichent désormais une utilisation correcte des ressources (GH #516)
- Traduction de base des exceptions NT en signaux. (GH #513)
- fallocate échoue maintenant avec ENOSPC lorsque l’espace est insuffisant au lieu de EINVAL (GH #1571)
- Ajout de/proc/sys/kernel/sem.
- Implémentation des appels système semop et SEMTIMEDOP
- Correction des erreurs nslookup avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (GH 69)
- Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 709 </br>
Nombre de non-passage (échec, ignoré, etc.): 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Résumé de syscall
Nombre total de syscalls: 384 </br>
Total implémenté: 235 </br>
Nombre total de stubs: 22 </br>
Total non implémenté: 127 </br>
[Répartition détaillée](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Build 15007

Pour obtenir des informations générales sur Windows sur la build 15007, visitez le [blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problème connu

- Il existe un bogue connu dans lequel la console ne reconnaît pas une <key> entrée Ctrl +.  Cela comprend la commande Ctrl-c qui agit comme une touche «c» normale.

  - Solution de contournement : Mappez une autre clé à Ctrl + C. Par exemple, pour mapper Ctrl + K à Ctrl + C, procédez comme suit: `stty intr \^k`.  Ce mappage est par terminal et doit être effectué à *chaque* fois que bash est lancé. Les utilisateurs peuvent explorer l’option permettant de les inclure dans leur`.bashrc`

### <a name="fixed"></a>Résolution

- Correction du problème où l’exécution de WSL consomme 100% d’un cœur de processeur
- Option de socket IP_PKTINFO, IPV6_RECVPKTINFO désormais prise en charge. (GH #851, 987)
- Tronquer l’adresse physique de l’interface réseau à 16 octets dans lxcore (GH #1452, 1414, 1343, 468, 308)
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 709 </br>
Nombre de non-passage (échec, ignoré, etc.): 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Build 15002

Pour obtenir des informations générales sur Windows sur la build 15002, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problème connu

Deux problèmes connus:
- Il existe un bogue connu dans lequel la console ne reconnaît pas une <key> entrée Ctrl +.  Cela comprend la commande Ctrl-c qui agit comme une touche «c» normale.

  - Solution de contournement : Mappez une autre clé à Ctrl + C. Par exemple, pour mapper Ctrl + K à Ctrl + C, procédez comme suit: `stty intr \^k`.  Ce mappage est par terminal et doit être effectué à *chaque* fois que bash est lancé. Les utilisateurs peuvent explorer l’option permettant de les inclure dans leur`.bashrc`

- Pendant l’exécution de WSL, un thread système consomme 100% d’un cœur de processeur.  La cause initiale a été résolue et corrigée en interne.

### <a name="fixed"></a>Résolution

- Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.  Toute tentative de démarrage d’une session à un niveau différent est bloquée.  Cela signifie que les consoles Administrateur et non-administrateur ne peuvent pas s’exécuter en même temps. (GH #626)
<br/>
- Mise en œuvre des messages NETLINK_ROUTE suivants (nécessite l’administrateur Windows)
     - RTM_NEWADDR (prend `ip addr add`en charge)
     - RTM_NEWROUTE (prend `ip route add`en charge)
     - RTM_DELADDR (prend `ip addr del`en charge)
     - RTM_DELROUTE (prend `ip route del`en charge)
- La vérification des tâches planifiées pour les packages à mettre à jour ne s’exécutera plus sur une connexion limitée (GH #1371)
- Correction de l’erreur où le canaling est coincé, c.-à-d. bash-r «LS-alR/» | bash-c «Cat» (GH #1214)
- Implémentation de l’option de socket TCP_KEEPCNT (GH #843)
- Implémentation de l’option de socket IP_MTU_DISCOVER INET (GH #720, 717, 170, 69)
- Suppression des fonctionnalités héritées pour exécuter des binaires NT à partir de la recherche de chemin d’accès NT. (GH #1325)
- Mode de correction de/dev/kmsg pour autoriser l’accès de groupe/autre accès en lecture (0644) (GH #1321)
- Implemented/proc/sys/kernel/Random/UUID (GH #1092)
- Erreur corrigée où l’heure de début du processus s’est affichée sous la forme année 2432 (GH #974)
- Variable d’environnement de terme par défaut basculée vers xterm-256color (GH #1446)
- Modification de la façon dont la validation de processus est calculée pendant la duplication de processus. (GH #1286)
- /Proc/sys/VM/overcommit_memory. implémentée (GH #1286)
- Fichier/proc/net/route implémenté (GH #69)
- Correction de l’erreur où le nom du raccourci n’a pas été localisé correctement (GH #696)
- Correction de la logique d’analyse de Elf qui valide incorrectement les en-têtes de programme doit être inférieure ou égale à PATH_MAX. (GH #1048)
- Implémentation du rappel statfs pour procfs, sysfs, cgroupfs et binfmtfs (GH #1378)
- Correction des fenêtres AptPackageIndexUpdate qui ne sont pas fermées (GH #1184, également abordées dans GH #1193)
- Ajout de la prise en charge de la personnalité ASLR ADDR_NO_RANDOMIZE. (GH #1148, 1128)
- PTRACE_GETSIGINFO amélioré, SIGSEGV, pour les traces de pile gdb appropriées pendant l’AV (GH #875)
- L’analyse ELF n’échoue plus pour les fichiers binaires patchelf. (GH #471)
- DNS VPN propagé à/etc/resolv.conf (GH #416, 1350)
- Améliorations apportées à TCP Close pour un transfert de données plus fiable. (GH #610, 616, 1025, 1335)
- Retourne à présent un code d’erreur correct lorsque trop de fichiers sont ouverts (EMFILE). (GH #1126, 2090)
- Le journal d’audit Windows signale désormais le nom de l’image dans traiter créer un audit.
- Échouent à présent correctement lors du lancement de bash. exe à partir d’une fenêtre bash
- Ajout d’un message d’erreur lorsque l’interopérabilité n’est pas en mesure d’accéder à un répertoire de travail sous LxFs (c.-à-d. Notepad. exe. bashrc)
- Correction du problème où le chemin d’accès Windows était tronqué dans WSL
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 690 </br>
Nombre de non-passage (échec, ignoré, etc.): 274 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Build 14986

Pour obtenir des informations générales sur Windows sur la build 14986, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Résolution

- Correction de bugchecks avec des IOCTL NetLink et Pty
- La version du noyau signale 4.4.0-43 pour assurer la cohérence avec Xenial
- Bash. exe se lance maintenant quand l’entrée est dirigée vers «nul:» (GH #1259)
- Les ID de thread sont désormais signalés correctement dans procfs (GH #967)
- IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Indicateurs IN_ISDIR désormais pris en charge dans inotify_add_watch () (GH #1280)
- Implémentez timer_create et les appels système associés.  Cela permet la prise en charge de GHC (GH #307)
- Correction du problème où ping a retourné une heure de 0.000 MS (GH #1296)
- Retourne un code d’erreur correct lorsque trop de fichiers sont ouverts.
- Résolution d’un problème dans WSL où les données de l’interface réseau de l’interface réseau échouent avec EINVAL si l’adresse matérielle de l’interface est de 32 octets (par exemple, l’interface Teredo)
   - Notez que l’utilitaire «IP» Linux contient un bogue qui se bloque si WSL signale une adresse matérielle de 32 octets. Il s’agit d’un bogue dans «IP», et non WSL. L’utilitaire «IP» code en dur la longueur de la mémoire tampon de chaîne utilisée pour imprimer l’adresse matérielle, et cette mémoire tampon est trop petite pour imprimer une adresse matérielle de 32 octets.
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 669 </br>
Nombre de non-passage (échec, ignoré, etc.): 258 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Build 14971

Pour obtenir des informations générales sur Windows sur la build 14971, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Résolution

 - En dehors de notre contrôle, aucune mise à jour n’est apportée à cette version pour le sous-système Windows pour Linux.  Les mises à jour planifiées périodiquement reprendront à la prochaine version.

### <a name="ltp-results"></a>Résultats de LTP:
Non modifié à partir de 14965 </br>
Nombre de tests réussis: 664 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Build 14965

Pour obtenir des informations générales sur Windows sur la build 14965, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Résolution

- Prise en charge des RTM_GETLINK et RTM_GETADDR du protocole NETLINK_ROUTE (GH #468)
  - Active les commandes ifconfig et IP pour l’énumération de réseau
  - Pour plus d’informations, consultez notre billet de blog sur la [mise en réseau WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin est désormais dans le chemin d’accès de l’utilisateur par défaut
- Le chemin d’accès de l’utilisateur NT est maintenant ajouté au chemin d’accès WSL par défaut (par exemple, vous pouvez maintenant taper Notepad. exe sans ajouter system32 au chemin Linux)
- Ajout de la prise en charge de/proc/sys/kernel/cap_last_cap
- Les fichiers binaires NT peuvent maintenant être lancés à partir de WSL lorsque le répertoire de travail actuel contient des caractères non ANSI (GH #1254)
- Autoriser l’arrêt sur le socket de flux UNIX déconnecté.
- Ajout de la prise en charge de PR_GET_PDEATHSIG.
- Ajout de la prise en charge de CLONE_PARENT
- Correction de l’erreur où le canaling est coincé, c.-à-d. bash-r «LS-alR/» | bash-c «Cat» (GH #1214)
- Gérer les demandes de connexion au terminal actuel.
- Marquez<pid>/proc//oom_score_adj comme accessible en écriture.
- Ajoutez le dossier/sys/FS/cgroup.
- sched_setaffinity doit retourner le nombre de bits d’affinité Mask
- Corrigez la logique de validation ELF qui suppose que les chemins de l’interpréteur ne doivent pas dépasser 64 caractères. (GH #743)
- Les descripteurs de fichiers ouverts peuvent maintenir la fenêtre de console ouverte (GH #1187)
- Erreur fixe où Rename () a échoué avec la barre oblique de fin sur le nom de la cible (GH #1008)
- Implémenter le fichier/proc/net/dev
- Correction des 0.000 ms pings en raison de la résolution du minuteur.
- Implemented/proc/Self/environ (GH #730)
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 664 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Build 14959

Pour obtenir des informations générales sur Windows sur la build 14959, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Résolution

- Notification de processus de Pico améliorée pour Windows.  Informations supplémentaires disponibles sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Stabilité améliorée avec l’interopérabilité Windows
- Correction de l’erreur 0x80070057 lors du lancement de bash. exe lorsque la protection des données d’entreprise (EDP) est activée
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 665 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Build 14955

Pour obtenir des informations générales sur Windows sur la build 14955, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Résolution

 - En dehors de notre contrôle, aucune mise à jour n’est apportée à cette version pour le sous-système Windows pour Linux.  Les mises à jour planifiées périodiquement reprendront à la prochaine version.

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 665 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Build 14951

Pour obtenir des informations générales sur Windows sur la build 14951, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Nouvelle fonctionnalité: Interopérabilité Windows/Ubuntu
Les binaires Windows peuvent désormais être appelés directement à partir de la ligne de commande WSL.  Cela permet aux utilisateurs d’interagir avec leurs environnements et systèmes Windows d’une manière qui n’a pas été possible.  En guise d’exemple rapide, les utilisateurs peuvent désormais exécuter les commandes suivantes:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

Pour plus d’informations, consultez:

- [Blog de l’équipe WSL pour l’interopérabilité](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentation MSDN Interop](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Résolution

- Ubuntu 16,04 (Xenial) est maintenant installé pour toutes les nouvelles instances de WSL.  Les utilisateurs avec des instances 14,04 (Trusty) existantes ne seront pas automatiquement mis à niveau.
- Les paramètres régionaux définis lors de l’installation s’affichent maintenant
- Les améliorations des terminaux, y compris les bogues qui redirigent un processus WSL vers un fichier, ne fonctionnent pas toujours
- La durée de vie de la console doit être liée à bash. exe durée de vie
- La taille de la fenêtre de console doit utiliser la taille visible, pas la taille de la mémoire tampon
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 665 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Build 14946

Pour obtenir des informations générales sur Windows sur la build 14946, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Résolution

- Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT qui contiennent des espaces ou des guillemets. 
- Modifiez VolFs et DrvFs pour retourner 0 pour le nombre de liens du répertoire dans stat
- Prise en charge de l’option de socket IPV6_MULTICAST_HOPS.
- Limiter à une seule boucle d’e/s de console par TTY. Exemple: la commande suivante est possible:
  - bash-c "echo Data" | Chat-c «SSH user@example.com » > foo. txt»

- remplacer les espaces par des tabulations dans/proc/cpuinfo (GH #1115)
- DrvFs apparaît maintenant dans mountinfo avec un nom qui correspond au volume Windows monté
- /Home et/root s’affichent désormais dans mountinfo avec des noms corrects
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 665 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Build 14942

Pour obtenir des informations générales sur Windows sur la build 14942, visitez le [blog Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Résolution

- Un certain nombre de bugchecks adressés, y compris le blocage du réseau «tentative d’exécution de la mémoire noexecute», qui bloque SSH
- la prise en charge de inotifiy pour les notifications générées à partir d’applications Windows sur DrvFs est désormais
- Implémentez TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod. (GH #695)
- Implémenter l’appel système pivot_root
- Implémenter l’option de socket pour SO_DONTROUTE
- Correctifs et améliorations supplémentaires


### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 665 </br>
Nombre de non-passage (échec, ignoré, etc.): 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Build 14936

Pour obtenir des informations générales sur Windows sur la build 14936, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Remarque : WSL installe Ubuntu version 16,04 (Xenial) au lieu d’Ubuntu 14,04 (Trusty) dans une prochaine version.  Cette modification s’appliquera aux Insiders qui installent de nouvelles instances (lxrun. exe/install ou First Run. exe).  Les instances existantes avec l’approbation ne sont pas mises à niveau automatiquement. Les utilisateurs peuvent mettre à niveau leur image de confiance vers Xenial à l’aide de la commande do-Release-Upgrade.

### <a name="known-issue"></a>Problème connu
WSL rencontre un problème avec certaines implémentations de Socket.  La vérification de bogue se manifeste comme un blocage avec l’erreur «tentative d’exécution de la mémoire noexecute».  La manifestation la plus courante de ce problème est un blocage lors de l’utilisation de SSH.  L’origine du problème est résolue sur les builds internes et sera envoyée aux Insiders au plus tôt.

### <a name="fixed"></a>Résolution

- Implémentation de l’appel système mécanisme chroot
- Améliorations apportées à inotify ~~, notamment la prise en charge des notifications générées à partir d’applications Windows sur DrvFs~~
  - Correction La prise en charge de inotify pour les modifications provenant d’applications Windows non disponibles pour le moment.
- Liaison de socket à IPv6:<port n> : prend désormais en charge IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)
- Comportement WNOWAIT pour waitid systemcall implémenté (GH #638)
- Prise en charge des options de socket IP IP_HDRINCL et IP_TTL
- La lecture de longueur nulle () doit être renvoyée immédiatement (GH #975)
- Gérez correctement les noms de fichiers et les préfixes de noms de fichiers qui n’incluent pas de marque de fin NULL dans un fichier. tar.
- prise en charge de epoll pour/dev/null
- Corriger la source de temps/dev/Alarm
- Bash-c maintenant capable de rediriger vers un fichier
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 664 </br>
Nombre de non-passage (échec, ignoré, etc.): 264 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Build 14931

Pour obtenir des informations générales sur Windows sur la build 14931, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Résolution

 - En dehors de notre contrôle, aucune mise à jour n’est apportée à cette version pour le sous-système Windows pour Linux.  Les mises à jour planifiées périodiquement reprendront dans la prochaine version.

<br/>

## <a name="build-14926"></a>Build 14926

Pour obtenir des informations générales sur Windows sur la build 14926, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Résolution

- Ping fonctionne désormais dans les consoles qui ne disposent pas de privilèges d’administrateur
- Ping6 désormais pris en charge, sans privilèges d’administrateur
- Inotify la prise en charge des fichiers modifiés via WSL. (GH #216)
  - Indicateurs pris en charge:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - événements inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - attributs inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - lire la sortie: LX_IN_ISDIR, LX_IN_IGNORED
  - Problème connu: La modification de fichiers à partir d’applications Windows ne génère pas d’événements
- Le socket Unix prend désormais en charge SCM_CREDENTIALS

### <a name="ltp-results"></a>Résultats de LTP:
Nombre de tests réussis: 651 </br>
Nombre de non-passage (échec, ignoré, etc.): 258 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Build 14915

Pour obtenir des informations générales sur Windows sur la build 14915, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Résolution
-  Sockets de datagramme socketpair pour UNIX (GH #262)
- Prise en charge des sockets Unix pour SO_REUSEADDR
- Prise en charge des sockets UNIX pour SO_BROADCAST (GH #568)
- Prise en charge des sockets Unix pour SOCK_SEQPACKET (GH #758, #546)
- Ajout de la prise en charge de l’envoi, du recv et de l’arrêt du socket de datagramme UNIX
- Corrigez les Bugcheck en raison d’une validation de paramètre mmap non valide pour les adresses non fixes. (GH #847)
- Prise en charge de l’interruption/reprise des États des terminaux
- Prise en charge de TIOCPKT ioctl pour débloquer l’utilitaire Screen (GH #774)
    - Problème connu: Clés de fonction non opérationnelles
- Correction d’une course dans TimerFd qui pourrait provoquer l’accès d’un membre libéré’ReaderReady’par LxpTimerFdWorkerRoutine (GH #814)
- Activer la prise en charge des appels système pouvant être redémarrés pour Futex, Poll et clock_nanosleep
- Ajout de la prise en charge du montage bind
- annuler le partage pour la prise en charge des espaces de noms de montage
    - Problème connu: Lorsque vous créez un espace de noms `unshare(CLONE_NEWNS)` de montage avec le répertoire de travail actuel, vous pointez sur l’ancien espace de noms
- Améliorations supplémentaires et correctifs de bogues

<br/>

## <a name="build-14905"></a>Build 14905

Pour obtenir des informations générales sur Windows sur la build 14905, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Résolution
- Les appels système redémarrables sont désormais pris en charge (GH #349, GH #520)
- Liens symboliques vers les répertoires se terminant par/maintenant opérationnel (GH #650)
- RNDGETENTCNT IOCTL implémenté pour/dev/random
- Mise en œuvre des fichiers/proc/[PID]/Mounts,/proc/[PID]/mountinfo et/proc/[PID]/mountstats
- Correctifs et améliorations supplémentaires

</br>

## <a name="build-14901"></a>Build 14901
Première version d’Insider pour la publication de la mise à jour anniversaire Windows 10.

Pour obtenir des informations générales sur Windows sur la build 14901, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Résolution
- Correction de la barre oblique de fin
    - Les commandes telles `$ mv a/c/ a/b/` que fonctionnent maintenant
- Installation des invites maintenant si les paramètres régionaux Ubuntu doivent être définis sur les paramètres régionaux Windows
- Prise en charge procfs pour le dossier NS
- Ajout de montage et démontage pour les systèmes de fichiers tmpfs, procfs et sysfs
- Correction de la signature ABI 32 bits de la solution mknod [at]
- Sockets Unix déplacés vers le modèle de distribution
- La taille de la mémoire tampon de réception du socket INET à l’aide de setsockopt doit être respectée
- Implémenter l’indicateur de message de réception du socket Unix MSG_CMSG_CLOEXEC
- Redirection de canaux Linux process stdin/stdout (GH #2)
    - Permet le canalisation des commandes bash-c dans CMD.  Exemple: > dir | bash-c «grep foo»
- Bash peut désormais être installé sur des systèmes avec plusieurs infromages (GH #538, #358)
- La taille de la mémoire tampon du socket INET par défaut doit correspondre à celle du programme d’installation Ubuntu par défaut
- Aligner xattr syscalls sur listxattr
- Retourne uniquement les interfaces avec une adresse IPv4 valide à partir de SIOCGIFCONF
- Corriger l’action par défaut de signal quand elle est injectée par ptrace
- implémenter/proc/sys/VM/min_free_kbytes
- Utiliser des valeurs de registre de contexte d’ordinateur lors de la restauration du contexte dans sigreturn
    - Cela résout le problème où Java et javac étaient bloqués pour certains utilisateurs
- Implémenter/proc/sys/kernel/hostname

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Version 14388 de la mise à jour anniversaire de Windows 10
Pour obtenir des informations générales sur Windows sur la build 14388, visitez le [blog Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Résolution
- Correctifs pour préparer la mise à jour anniversaire Windows 10 sur 8/2
  - Vous trouverez plus d’informations sur WSL dans la mise à jour anniversaire sur notre [blog](https://blogs.msdn.microsoft.com/wsl/) .

<br/>

## <a name="build-14376"></a>Build 14376
Pour obtenir des informations générales sur Windows sur la build 14376, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Résolution
- Suppression de certaines instances où apt-obtien se bloque (GH #493)
- Résolution d’un problème où les montages vides n’étaient pas gérés correctement
- Correction d’un problème où les ramdisks n’étaient pas correctement montés
- Remplacer l’acceptation du socket UNIX par les indicateurs de prise en charge (GH #451 partiel)
- Résolution de l’écran bleu commun lié au réseau
- Correction de l’écran bleu lors de l’accès à/proc/[PID]/Task (GH #523)
- Correction de l’utilisation élevée du processeur pour certains cas de PTY (GH #488, #504)
- Correctifs et améliorations supplémentaires

<br/>

## <a name="build-14371"></a>Build 14371
Pour obtenir des informations générales sur Windows sur la build 14371, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Résolution
- Correction de la course temporelle avec SIGCHLD et attente () lors de l’utilisation de ptrace
- Correction de certains comportements lorsque les chemins d’accès ont une fin/(GH #432)
- Résolution du problème lié à l’échec de renommage/dissociation en raison de handles ouverts vers des enfants
- Correctifs et améliorations supplémentaires

<br/>

## <a name="build-14366"></a>Build 14366
Pour obtenir des informations générales sur Windows sur la build 14366, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Résolution
- Correction de la création de fichiers via liens symboliques
-   Ajout de listxattr pour Python (GH 385)
-   Correctifs et améliorations supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
-   Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Build 14361
Pour obtenir des informations générales sur Windows sur la build 14361, visitez le [blog Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Résolution
- DrvFs respecte désormais la casse lors de l’exécution dans bash sur Ubuntu sur Windows.
  - Les utilisateurs peuvent les cas. txt et CASE. TXT sur leurs lecteurs/mnt/c
  - Le respect de la casse est pris en charge uniquement dans bash sur Ubuntu sur Windows. En dehors du système NTFS bash signale les fichiers correctement, mais un comportement inattendu peut se produire lors de l’interaction avec les fichiers de Windows.
  - La racine de chaque volume (c.-à-d./mnt/c) n’est pas sensible à la casse
  - Vous trouverez plus d’informations sur la gestion de ces fichiers dans Windows [ici](https://support.microsoft.com/en-us/kb/100625).
- Prise en charge de PTY/TTY beaucoup améliorée.  Applications telles que TMUX désormais prises en charge (GH #40)
- Résolution d’un problème d’installation où les comptes d’utilisateurs n’ont pas toujours été créés
- Structure d’arguments de ligne de commande optimisée autorisant une liste d’arguments extrêmement longue. (GH #153)
- Possibilité de supprimer et chmod des fichiers READ_ONLY de DrvFs
- Correction de certaines instances où le terminal se bloque lors de la déconnexion (GH #43)
- chmod et chown fonctionnent désormais sur les appareils TTY
- Autoriser la connexion à 0.0.0.0 et:: en tant que localhost (GH #388)
- Sendmsg/recvmsg gère désormais une longueur de vecteur d’e/s de > 1 (à GH partiel #376)
- Les utilisateurs peuvent désormais désactiver le fichier des hôtes générés automatiquement (GH #398)
- Faire correspondre automatiquement les paramètres régionaux Linux aux paramètres régionaux NT lors de l’installation (GH #11)
- Ajout du fichier/proc/sys/VM/swappiness (GH #306)
- strace se ferme maintenant correctement
- Autoriser la réouverture des canaux via/proc/Self/FD (GH #222)
- Masquer les répertoires sous%LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)
- Meilleure gestion de bash. exe ~.  Les commandes telles que «bash ~-c ls» sont maintenant prises en charge (GH #467)
- Les sockets notifient désormais la lecture des epoll disponibles pendant l’arrêt (GH #271)
- lxrun/Uninstall est un meilleur travail de suppression des fichiers et des dossiers
- Correction de PS-f (GH #246)
- Prise en charge améliorée des applications X11 comme xEmacs (GH #481)
- Mise à jour de la taille de la pile des threads initiale pour qu’elle corresponde au paramètre Ubuntu par défaut et signale la taille correctement au get_rlimit syscall (GH #172, #258)
- Amélioration de la création de rapports sur les noms d’image de processus de Pico (par exemple, pour l’audit)
- Implémentation de/proc/mountinfo pour DF, commande
- Correction du code d’erreur symlink pour le nom de l’enfant. et.
- Améliorations supplémentaires correctifs et améliorations

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Build 14352
Pour obtenir des informations générales sur Windows sur la build 14352, visitez le [blog Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Résolution
- Résolution d’un problème où des fichiers volumineux n’ont pas été téléchargés/créés correctement.  Cela doit débloquer NPM et d’autres scénarios (GH #3, GH #313)
- Suppression de certaines instances où les sockets se bloquent
- Correction de certaines erreurs de ptrace
- Résolution d’un problème avec WSL autorisant les noms de fichiers de plus de 255 caractères
- Amélioration de la prise en charge des caractères non anglais
- Ajouter les données de fuseau horaire Windows actuelles et les définir par défaut
- ID d’appareil unique pour chaque point de montage (correctif JRE – GH #49)
- Corriger le problème avec les chemins d’accès contenant «.» et ".."
- Ajout de la prise en charge FIFO (GH #71)
- Format de resolv. conf mis à jour pour correspondre au format Ubuntu natif
- Certains nettoyages de procfs
- Activation du test ping pour les consoles Administrateur (GH #18)

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Build 14342
Pour obtenir des informations générales sur Windows sur la build 14342, le [blog Windows](https://aka.ms/wip14342). <br/>

Vous trouverez des informations sur VolFs et DriveFs sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Résolution
- Résolution du problème d’installation lorsque l’utilisateur Windows contenait des caractères Unicode dans le nom d’utilisateur
- La solution de contournement udev de mise à jour «apt-obtien» dans le Forum aux questions est désormais fournie par défaut lors de la première exécution
- Activation de liens symboliques dans les répertoires DriveFs (/MNT/<drive>)
- Liens symboliques fonctionne désormais entre DriveFs et VolFs
- Adressée supérieur au niveau chemin d’accès de l’analyse du problème : %.ls. / / fonctionne désormais comme prévu
- NPM install sur DriveFs et les options-g fonctionnent désormais
- Résolution du problème empêchant le lancement du serveur PHP
- Mise à jour des valeurs d’environnement par défaut, par exemple $PATH pour une correspondance plus proche d’Ubuntu natif
- Ajout d’une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache de packages APT
- Résolution du problème avec la validation d’en-tête ELF, WSL prend désormais en charge toutes les options Melkor
- L’interpréteur de commandes zsh est fonctionnel
- Les fichiers binaires Go précompilés sont désormais pris en charge
- L’invite de la première exécution de bash. exe est désormais localisée correctement
- /proc/meminfo retourne désormais des informations correctes
- Sockets pris en charge dans VFS
- /dev maintenant monté en tant que tempfs
- FIFO actuellement pris en charge
- Les systèmes multicœurs s’affichaient désormais correctement dans/proc/cpuinfo
- Améliorations supplémentaires et messages d’erreur téléchargés lors de la première exécution
- Améliorations de syscall et correctifs. Liste syscall prise en charge ci-dessous.
- Correctifs et améliorations supplémentaires

### <a name="known-issues"></a>Problèmes connus
- Impossible de résoudre'.. ' correctement sur DriveFs dans certains cas

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

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

Pour obtenir des informations générales sur Windows sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Résolution
- Meilleure génération de resolv. conf, y compris la hiérarchisation des entrées DNS
- Problème lié au déplacement de fichiers et de répertoires entre les lecteurs/mnt et non-/MNT
- Les fichiers tar peuvent maintenant être créés avec liens symboliques
- Ajout du répertoire/Run/Lock par défaut lors de la création de l’instance
- Mettre à jour/dev/null pour retourner les informations statistiques appropriées
- Erreurs supplémentaires lors du téléchargement lors de la première exécution
- Améliorations de syscall et correctifs. Liste syscall prise en charge ci-dessous.
- Améliorations supplémentaires correctifs et améliorations

### <a name="syscall-support"></a>Prise en charge de syscall
Voici le nouveau syscall qui a une implémentation dans WSL. Le syscall sur cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Build 14328

Pour obtenir des informations générales sur Windows sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Nouvelles fonctionnalités
* Prend désormais en charge les utilisateurs Linux.  L’installation de bash sur Ubuntu sur Windows vous invite à créer un utilisateur Linux.  Pour plus d’informations, visitez le site https://aka.ms/wslusers
* Hostname est maintenant défini sur le nom de l’ordinateur Windows, pas plus@localhost
* Pour plus d’informations sur la build 14328, visitez le site: https://aka.ms/wip14328

### <a name="fixed"></a>Résolution
* Améliorations des liens symboliques<drive> pour les fichiers non/MNT/
    * l’installation de NPM fonctionne maintenant
    * JDK/JRE s’installe maintenant à l’aide des instructions fournies [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * problème connu: liens symboliques ne fonctionne pas pour les montages Windows.  Les fonctionnalités seront disponibles dans une version ultérieure
* affichages haut et htop maintenant
* Messages d’erreur supplémentaires pour certains échecs d’installation
* Améliorations de syscall et correctifs.  Liste syscall prise en charge ci-dessous.
* Améliorations supplémentaires correctifs et améliorations

### <a name="syscall-support"></a>Prise en charge de syscall
Vous trouverez ci-dessous une liste des syscalls qui ont été implémentées dans WSL.  Les syscalls dans cette liste sont pris en charge dans au moins un scénario, mais ils peuvent ne pas avoir tous les paramètres pris en charge pour l’instant.

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
