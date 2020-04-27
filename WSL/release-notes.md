---
title: Notes de publication pour le sous-système Windows pour Linux
description: Notes de publication pour le sous-système Windows pour Linux.  Mise à jour hebdomadaire.
keywords: BashOnWindows, bash, wsl, Windows, sous-système Windows pour Linux, sous-système windows, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 31bf975afb202a6cfd9a2879cff29a77b2969fce
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "76911703"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Notes de publication pour le sous-système Windows pour Linux

## <a name="build-19555"></a>Build 19555
Pour des informations Windows d’ordre général sur la build 19555, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).

* [WSL2] Utilisation d’un cgroup de mémoire pour limiter la quantité de mémoire utilisée par les opérations d’installation et de conversion [GH 4669]
* Ajout de la présence de wsl.exe quand le composant facultatif Sous-système Windows pour Linux n’est pas activé pour améliorer la découvertabilité des fonctionnalités.
* Changement de wsl.exe pour afficher le texte d’aide si le composant facultatif WSL n’est pas installé
* Correction de la condition de concurrence lors de la création d’instances
* Création de wslclient.dll qui contient toutes les fonctionnalités de ligne de commande
* Plus de plantage pendant l’arrêt du service LxssManagerUser
* Correction de l’échec rapide de wslapi.dll quand le paramètre distroName est NULL

## <a name="build-19041"></a>Build 19041
Pour des informations Windows d’ordre général sur la build 19041, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).

* [WSL2] Effacement du masque de signal avant de lancer les processus
* [WSL2] Mise à jour du noyau Linux vers 4.19.84
* Gestion de la création d’un lien symbolique /etc/resolv.conf quand le lien symbolique n’est pas relatif

## <a name="build-19028"></a>Build 19028
Pour des informations Windows d’ordre général sur la build 19028, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).

* [WSL2] Mise à jour du noyau Linux vers 4.19.81
* [WSL2] Remplacer l’autorisation par défaut de /dev/net/Tun par 0666 [GH 4629]
* [WSL2] Ajuster la quantité de mémoire par défaut affectée à la machine virtuelle Linux pour qu’elle soit à 80 % de mémoire hôte
* [WSL2] Correction du serveur Interop pour gérer les demandes avec un délai d’attente de sorte à empêcher les appelants incorrects de bloquer le serveur

## <a name="build-19018"></a>Build 19018
Pour des informations Windows d’ordre général sur la build 19018, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).

* [WSL2] Utilisation de cache=mmap comme valeur par défaut pour les montages 9p afin de corriger les applications dotnet
* [WSL2] Corrections pour le relais localhost [GH 4340]
* [WSL2] Introduction d’un montage tmpfs partagé multidistribution pour le partage de l’état entre plusieurs distributions
* Correction de la restauration d’un lecteur réseau persistant pour \\\\wsl$

## <a name="build-19013"></a>Build 19013
Pour des informations Windows d’ordre général sur la build 19013, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).

* [WSL2] Amélioration des performances de la mémoire de la machine virtuelle de l’utilitaire WSL. La mémoire qui n’est plus utilisée sera libérée et retournée à l’hôte.
* [WSL2] Mise à jour de la version du noyau vers 4.19.79. (ajout de CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK et CONFIG_BRIDGE_VLAN_FILTERING).
* [WSL2] Correction du relais d’entrée pour gérer les cas où stdin est un handle de canal qui n’est pas fermé [GH 4424]
* Vérification que \\\\wsl$ n’est pas sensible à la casse.
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a>Build 19002
Pour des informations Windows d’ordre général sur la build 19002, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).

* [WSL] Correction du problème de gestion de certains caractères Unicode : https://github.com/microsoft/terminal/issues/2770
* [WSL] Correction de cas rares où des distributions pouvaient être désinscrites si elles étaient lancées immédiatement après une mise à niveau build-à-build.
* [WSL] Correction d’un problème mineur avec wsl. exe --shutdown où les minuteurs inactifs d’instance n’étaient pas annulés.

## <a name="build-18995"></a>Build 18995
Pour des informations Windows d’ordre général sur la build 18995, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).

* [WSL2] Correction d’un problème où les montages DrvFs cessaient de fonctionner après l’interruption d’une opération (par ex. ctrl-c) [GH 4377]
* [WSL2] Correction de la gestion des très longs messages hvsocket [GH 4105]
* [WSL2] Correction du problème avec l’interopérabilité quand stdin est un fichier [GH 4475]
* [WSL2] Correction du plantage du service lors d’un état inattendu du réseau [GH 4474]
* [WSL2] Interrogation du nom de distribution du serveur d’interopérabilité si le processus actuel n’a pas la variable d’environnement
* [WSL2] Correction du problème avec l’interopérabilité quand stdin est un fichier
* [WSL2] Mise à jour de la version du noyau Linux vers 4.19.72
* [WSL2] Ajout de la possibilité de spécifier des paramètres de ligne de commande du noyau supplémentaires via .wslconfig
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a>Build 18990
Pour des informations Windows d’ordre général sur la build 18990, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).

* Améliorer les performances des listes de répertoires dans \\\\wsl$
* [WSL2] Injecter un entropie de démarrage supplémentaire [GH 4416]
* [WSL2] Correctif pour Windows Interop lors de l’utilisation de su / sudo [GH 4465]

## <a name="build-18980"></a>Build 18980
Pour obtenir des informations Windows d’ordre général sur la build 18980, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).

* Correction de la lecture des liens symboliques qui refusent FILE_READ_DATA. Sont inclus tous les liens symboliques créés par Windows à des fins de compatibilité descendante, comme « C:\Document et Settings » et un ensemble de liens symboliques dans le répertoire du profil de l’utilisateur.
* État de système de fichiers inattendu rendu récupérable [GH 4334, 4305]
* [WSL2] Ajout de la prise en charge d’arm64 si votre processeur/microprogramme prend en charge la virtualisation
* [WSL2] Autorisation des utilisateurs non privilégiés à afficher le journal du noyau
* [WSL2] Correction du relais de sortie quand les sockets stdout/stderr ont été fermés [GH 4375]
* [WSL2] Prise en charge du transfert de batterie et d’adaptateur secteur
* [WSL2] Mise à jour du noyau Linux vers 4.19.67
* Ajout de la possibilité de définir un nom d’utilisateur par défaut dans /etc/wsl.conf :
```
[user]
default=<string>
```

## <a name="build-18975"></a>Build 18975
Pour obtenir des informations Windows d’ordre général sur la Build 18975, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).

* [WSL2] Correction de plusieurs problèmes de fiabilité de localhost [GH 4340]

## <a name="build-18970"></a>Build 18970
Pour obtenir des informations Windows d’ordre général sur la Build 18970, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).

* [WSL2] Synchronisation de l’heure avec celle de l’hôte quand le système sort de l’état de veille [GH 4245]
* [WSL2] Création de liens symboliques NT sur les volumes Windows quand cela est possible.
* [WSL2] Création de distributions dans les espaces de noms UTS, IPC, PID et Mount.
* [WSL2] Correction du relais de port localhost quand le serveur est directement lié à localhost [GH 4353]
* [WSL2] Correction d’interop quand la sortie est redirigée [GH 4337]
* [WSL2] Prise en charge de la traduction des liens symboliques NT absolus.
* [WSL2] Mise à jour du noyau vers la version 4.19.59
* [WSL2] Définition correcte du masque de sous-réseau pour eth0.
* [WSL2] Changement de logique pour quitter la boucle de travail de la console lorsque l’événement de sortie est signalé.
* [WSL2] Éjection du disque dur virtuel de distribution lorsque la distribution n’est pas en cours d’exécution.
* [WSL2] Correction de la bibliothèque d’analyse de configuration pour gérer correctement les valeurs vides.
* [WSL2] Prise en charge de Docker Desktop en créant des montages entre les distributions. Une distribution peut adopter ce comportement en ajoutant la ligne suivante au fichier /etc/wsl.conf :
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a>Build 18945
Pour obtenir des informations Windows d’ordre général sur la build 18945, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).

### <a name="wsl"></a>WSL
* [WSL2] Autorisation des sockets tcp d’écoute dans WSL2 pour qu’ils soient accessibles à partir de l’hôte en utilisant localhost:port
* [WSL2] Correctifs pour les échecs d’installation/conversion et les diagnostics supplémentaires pour suivre les problèmes futurs [GH 4105] 
* [WSL2] Améliorations de la possibilité de diagnostiquer les problèmes de réseau WSL2
* [WSL2] Mise à jour de la version du noyau vers 4.19.55
* [WSL2] Mise à jour du noyau avec les options de configuration requises pour Docker [GH 4165]
* [WSL2] Augmentation du nombre de processeurs affecté à la machine virtuelle utilitaire légère pour qu’il soit identique à celui de l’hôte (précédemment plafonné à 8 par CONFIG_NR_CPUS dans la configuration du noyau) [GH 4137]
* [WSL2] Création d’un fichier d’échange pour la machine virtuelle légère WSL2
* [WSL2] Autorisation de la visibilité des montages utilisateur par le biais de \\\\wsl$\\distro (par exemple, sshfs) [GH 4172]
* [WSL2] Amélioration des performances du système de fichiers 9p
* [WSL2] Vérification que la liste ACL du disque dur virtuel n’augmente pas sans aucune limite [GH 4126]
* [WSL2] Mise à jour de la configuration du noyau pour prendre en charge squashfs et xt_conntrack [GH 4107, 4123]
* [WSL2] Correctif pour interop.enabled /etc/wsl.conf option [GH 4140]
* [WSL2] Renvoi de ENOTSUP si le système de fichiers ne prend pas en charge les EA
* [WSL2] Correction du blocage CopyFile avec \\\\wsl$
* Remplacement de l’umask par défaut par 0022 et ajout du paramètre filesystem.umask à /etc/wsl.conf
* Correction de wslpath pour résoudre correctement les liens symboliques (retour en arrière dans 19h1) [GH 4078]
* Introduction du fichier %UserProfile%\\.wslconfig pour modifier légèrement les paramètres WSL2
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

## <a name="build-18917"></a>Build 18917
Pour obtenir des informations Windows d’ordre général sur la build 18917, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).

### <a name="wsl"></a>WSL
* WSL 2 est maintenant disponible ! Pour plus d’informations, consultez le [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).
* Correction d’un retour en arrière où le lancement de processus Windows par le biais de liens symboliques ne fonctionnait pas correctement [GH 3999]
* Ajout des options wsl.exe --list --verbose, wsl.exe --list --quiet et wsl.exe --import --version à wsl.exe
* Ajout de l’option wsl.exe --shutdown
* Plan 9 : Autorisation de l’ouverture d’un répertoire pour que l’écriture aboutisse

## <a name="build-18890"></a>Build 18890
Pour obtenir des informations Windows d’ordre général sur la build 18890, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Fuite de socket non bloquante [GH 2913]
* L’entrée EOF du terminal peut bloquer les lectures consécutives [GH 3421]
* Mise à jour de l’en-tête resolv.conf pour faire référence à wsl.conf [description dans GH 3928]
* Blocage dans le code de suppression epoll [GH 3922]
* Gestion des espaces dans les arguments --import et –export [GH 3932]
* L’extension des fichiers mmap ne fonctionne pas correctement [GH 3939]
* Correction du problème où l’accès ARM64 \\\\wsl$ ne fonctionnait pas correctement
* Ajout d’une meilleure icône par défaut pour wsl.exe

## <a name="build-18342"></a>Build 18342
Pour obtenir des informations Windows d’ordre général sur la build 18342, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans une distribution WSL à partir de Windows. Ces fichiers sont accessibles par le biais de la ligne de commande. Des applications Windows, comme l’Explorateur de fichiers, VSCode, etc. peuvent aussi interagir avec ces fichiers. Accédez à vos fichiers en naviguant vers \\\\wsl$\\<nom_distribution> ou consultez la liste des distributions en cours d’exécution en naviguant vers \\\\wsl$.
* Ajout de balises d’informations de processeur supplémentaires et correction des valeurs Cpus_allowed[_list] [GH 2234]
* Prise en charge de l’exécution à partir d’un thread non-leader [GH 3800]
* Considération des échecs de mise à jour de configuration comme récupérables [GH 3785]
* Mise à jour de binfmt pour gérer correctement les décalages [GH 3768]
* Activation du mappage des lecteurs réseau pour le plan 9 [GH 3854]
* Prise en charge de la traduction de chemins Windows > Linux et Linux-> Windows pour les montages de liaison
* Création de sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule

## <a name="build-18334"></a>Build 18334
Pour obtenir des informations Windows d’ordre général sur la build 18334, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Nouvelle conception de la façon dont le fuseau horaire Windows est mappé à un fuseau horaire Linux [GH 3747]
* Correction des fuites de mémoire et ajout de nouvelles fonctions de traduction de chaînes [GH 3746]
* SIGCONT sur un groupe de threads sans aucun thread est un no-op [GH 3741] 
* Correction de l’affichage des descripteurs de fichiers socket et epoll dans /proc/self/fd

## <a name="build-18305"></a>Build 18305
Pour obtenir des informations Windows d’ordre général sur la build 18305, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* Perte d’accès des pthreads aux fichiers lors de la sortie du thread principal [GH 3589]
* TIOCSCTTY doit ignorer le paramètre « force » sauf s’il est obligatoire [GH 3652]
* Améliorations de la ligne de commande wsl.exe et ajout de fonctionnalités d’importation/exportation.
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

## <a name="build-18277"></a>Build 18277
Pour obtenir des informations Windows d’ordre général sur la build 18277, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Correction de l’erreur « Interface non prise en charge » introduite dans la build 18272 [GH 3645]
* Ignorance de l’indicateur MNT_FORCE pour umount syscall [GH 3605]
* Basculement d’interop WSL pour utiliser l’API CreatePseudoConsole officielle
* Non-conservation d’une valeur de délai d’expiration au redémarrage de FUTEX_WAIT

## <a name="build-18272"></a>Build 18272
Pour obtenir des informations Windows d’ordre général sur la build 18272, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **AVERTISSEMENT :** Un problème existant dans cette build rend WSL inopérable. Quand vous essayez de lancer votre distribution, une erreur « Interface non prise en charge » s’affiche. Le problème est résolu et sa résolution va être intégrée à la build Insider Fast de la semaine prochaine. Si vous avez installé cette build, vous pouvez revenir à la build Windows précédente en utilisant « Rétrograder vers la version précédente de Windows 10 » dans Paramètres->Mise à jour et sécurité->Récupération.

## <a name="build-18267"></a>Build 18267
Pour obtenir des informations Windows d’ordre général sur la build 18267, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Correction du problème où le processus zombie n’est pas recueilli et reste indéfiniment.
* WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]
* Autorisation de fsync à fonctionner correctement pour les fichiers en lecture seule sur DrvFs [GH 3556]
* Vérification que les répertoires /bin et /sbin existent avant de créer des liens symboliques dans [GH 3584]
* Ajout d’un mécanisme de délai d’expiration avant l’arrêt d’une instance pour les instances WSL. Le délai d’expiration est actuellement défini à 15 secondes, ce qui signifie que l’instance se termine 15 secondes après la fin du dernier processus WSL. Pour arrêter immédiatement une distribution, utilisez :
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Build 17763 (1809)
Pour obtenir des informations Windows d’ordre général sur la build 17763, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Vérification des autorisations de Setpriority syscall trop stricte pour modifier la priorité du même thread [GH 1838]
* Garantie que l’heure d’interruption non biaisée est utilisée pour l’heure de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Gestion des liens symboliques dans l’interpréteur binfmt WSL [GH 3424]
* Meilleure gestion du nettoyage du descripteur de fichier leader de groupe de threads.
* Basculement de WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter tout dépassement de capacité [GH 3252]
* Attachement ptrace à l’origine d’une valeur de retour incorrecte de la part des appels système [GH 1731]
* Correction de plusieurs problèmes liés à AF_UNIX [GH 3371]
* Correction du problème pouvant provoquer l’échec d’interop WSL si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]
* Évitement des connexions de boucle d’échec d’un délai d’une seconde à des ports inexistants [GH 3286]
* Ajout du fichier stub /proc/sys/fs/file-max [GH 2893]
* Informations d’étendue IPV6 plus précises.
* Prise en charge de PR_SET_PTRACER [GH 3053]
* Système de fichiers de canal effaçant par inadvertance l’événement epoll déclenché latéralement [GH 3276]
* L’exécutable Win32 lancé par le biais d’un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]
* Prise en charge améliorée de zombie [GH 1353]
* Ajout d’entrées wsl.conf pour contrôler le comportement d’interop Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correctif pour getsockname qui ne retourne pas toujours le type de famille des sockets UNIX [GH 1774]
* Ajout de la prise en charge de TIOCSTI [GH 1863]
* Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]
* Prise en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]
* Correction du problème de vérification des autorisations sur le dossier racine [GH 3304]
* Prise en charge limitée des commandes IOCTL de clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.
* Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.
* Ajout de l’option wsl -u ou --user [GH 1203]
* Correction des problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]
* Les sockets Unix ont besoin de conserver les informations d’identification des homologues déconnectés [GH 3183]
* Échec perpétuel des sockets Unix non bloquants avec EAGAIN [GH 3191]
* case=off est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]
    * Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).
* Ajout de wslconfig /terminate pour arrêter les distributions en cours d’exécution.
* Correction du problème lié aux entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins comportant des espaces.
* Exposition du respect de la casse par répertoire en tant qu’attribut étendu
* ARM64 : Émulation des opérations de maintenance du cache. Résolution du [problème dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs : uniquement les caractères de non-échappement de la plage privée qui correspondent à un caractère d’échappement.
* Correction de l’erreur « off-by-one » dans la validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]
* Les minuteurs absolus WSL avec une heure passée ne se déclenchent pas [GH 3091]
* Vérification que les points de nouvelle analyse récemment créés sont listés comme tels dans le répertoire parent.
* Création atomique de répertoires sensibles à la casse dans DrvFs.
* Correction d’un problème supplémentaire où les opérations multithread peuvent retourner ENOENT même si le fichier existe. [GH 2712]
* Correction de l’échec de lancement de WSL quand UMCI est activé. [GH 3020]
* Ajout du menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836]. Pour l’utiliser, maintenez la touche Maj enfoncée et cliquez avec le bouton droit dans une fenêtre de l’Explorateur.
* Correction du comportement non bloquant du socket Unix [GH 2822, 3100]
* Correction de la commande NetLink bloquée comme indiqué dans GH 2026.
* Ajout de la prise en charge des indicateurs de propagation de montage [GH 2911].
* Correction du problème lié à la troncation qui n’engendre pas d’événements inotify [GH 2978].
* Ajout de l’option --exec pour wsl.exe afin d’appeler un seul binaire sans shell.
* Ajout de l’option --distribution pour wsl.exe afin de sélectionner une distribution spécifique.
* Prise en charge limitée de dmesg. Les applications peuvent désormais se connecter à dmesg. Le pilote WSL journalise des informations limitées sur dmesg. À l’avenir, il sera développé pour transporter d’autres informations/diagnostics à partir du pilote.
    * Remarque : dmesg est actuellement pris en charge par le biais de l’interface d’appareil `/dev/kmsg`. L’interface syscall `syslog` n’est pas encore prise en charge. Et donc, certaines des options de ligne de commande `dmesg` comme `-S`, `-C`, ne fonctionnent pas.
* Changement du gid et du mode par défaut des appareils en série pour qu’ils correspondent aux natifs [GH 3042]
* DrvFs prend désormais en charge les attributs étendus.
    * Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus. Certains caractères (comme « / », « : » et « \* ») ne sont pas autorisés et les noms d’attributs étendus ne sont pas sensibles à la casse sur DrvFs

## <a name="build-18252-skip-ahead"></a>Build 18252 (Skip Ahead)
Pour obtenir des informations Windows d’ordre général sur la build 18252, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Déplacement des binaires init et bsdtar en dehors de la dll lxssmanager et dans un dossier d’outils distinct
* Correction de la concurrence autour du descripteur de fichier de fermeture lors de l’utilisation de CLONE_FILES
* Gestion des champs facultatifs dans /proc/pid/mountinfo lors de la traduction de chemins DrvFs
* Autorisation de la réussite de DrvFs mknod sans prise en charge des métadonnées de S_IFREG
* Les fichiers en lecture seule créés sur DrvFs doivent avoir l’attribut readonly défini [GH 3411]
* Ajout de l’assistance /sbin/mount.drvfs pour gérer le montage DrvFs
* Utilisation du renommage POSIX dans DrvFs.
* Autorisation de la traduction de chemins sur les volumes sans GUID de volume.

## <a name="build-17738-fast"></a>Build 17738 (Fast)
Pour obtenir des informations Windows d’ordre général sur la build 17738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Vérification des autorisations de Setpriority syscall trop stricte pour modifier la priorité du même thread [GH 1838]
* Garantie que l’heure d’interruption non biaisée est utilisée pour l’heure de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* Gestion des liens symboliques dans l’interpréteur binfmt WSL [GH 3424]
* Meilleure gestion du nettoyage du descripteur de fichier leader de groupe de threads.

## <a name="build-17728-fast"></a>Build 17728 (Fast)
Pour obtenir des informations Windows d’ordre général sur la build 17728, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Basculement de WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter tout dépassement de capacité [GH 3252]
* Attachement ptrace à l’origine d’une valeur de retour incorrecte de la part des appels système [GH 1731]
* Correction de plusieurs problèmes liés à AF_UNIX [GH 3371]
* Correction du problème pouvant provoquer l’échec d’interop WSL si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]

## <a name="build-18204-skip-ahead"></a>Build 18204 (Skip Ahead)
Pour obtenir des informations Windows d’ordre général sur la build 18204, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Système de fichiers de canal effaçant par inadvertance l’événement epoll déclenché latéralement [GH 3276]
* L’exécutable Win32 lancé par le biais d’un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]

## <a name="build-17723-fast"></a>Build 17723 (Fast)
Pour obtenir des informations Windows d’ordre général sur la build 17723, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Évitement des connexions de boucle d’échec d’un délai d’une seconde à des ports inexistants [GH 3286]
* Ajout du fichier stub /proc/sys/fs/file-max [GH 2893]
* Informations d’étendue IPV6 plus précises.
* Prise en charge de PR_SET_PTRACER [GH 3053]
* Système de fichiers de canal effaçant par inadvertance l’événement epoll déclenché latéralement [GH 3276]
* L’exécutable Win32 lancé par le biais d’un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]

## <a name="build-17713"></a>Build 17713
Pour obtenir des informations Windows d’ordre général sur la build 17713, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Prise en charge améliorée de zombie [GH 1353]
* Ajout d’entrées wsl.conf pour contrôler le comportement d’interop Windows [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Correctif pour getsockname qui ne retourne pas toujours le type de famille des sockets UNIX [GH 1774]
* Ajout de la prise en charge de TIOCSTI [GH 1863]
* Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]
* Prise en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]
* Correction du problème de vérification des autorisations sur le dossier racine [GH 3304]
* Prise en charge limitée des commandes IOCTL de clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.
* Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.

## <a name="build-17704"></a>Build 17704
Pour obtenir des informations Windows d’ordre général sur la build 17704, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Ajout de l’option wsl -u ou --user [GH 1203]
* Correction des problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]
* Les sockets Unix ont besoin de conserver les informations d’identification des homologues déconnectés [GH 3183]
* Échec perpétuel des sockets Unix non bloquants avec EAGAIN [GH 3191]
* case=off est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]
    * Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).
* Ajout de wslconfig /terminate pour arrêter les distributions en cours d’exécution.

## <a name="build-17692"></a>Build 17692
Pour obtenir des informations Windows d’ordre général sur la build 17692, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Correction du problème lié aux entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins comportant des espaces.
* Exposition du respect de la casse par répertoire en tant qu’attribut étendu
* ARM64 : Émulation des opérations de maintenance du cache. Résolution du [problème dotnet](https://github.com/dotnet/core/issues/1561).
* DrvFs : uniquement les caractères de non-échappement de la plage privée qui correspondent à un caractère d’échappement.

## <a name="build-17686"></a>Build 17686
Pour obtenir des informations Windows d’ordre général sur la build 17686, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Correction de l’erreur « off-by-one » dans la validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]
* Les minuteurs absolus WSL avec une heure passée ne se déclenchent pas [GH 3091]
* Vérification que les points de nouvelle analyse récemment créés sont listés comme tels dans le répertoire parent.
* Création atomique de répertoires sensibles à la casse dans DrvFs.

## <a name="build-17677"></a>Build 17677
Pour obtenir des informations Windows d’ordre général sur la build 17677, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Correction d’un problème supplémentaire où les opérations multithread peuvent retourner ENOENT même si le fichier existe. [GH 2712]
* Correction de l’échec de lancement de WSL quand UMCI est activé. [GH 3020]

## <a name="build-17666"></a>Build 17666
Pour obtenir des informations Windows d’ordre général sur la build 17666, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>AVERTISSEMENT : Un problème empêche WSL de s’exécuter sur certains chipsets AMD [GH 3134]. Un correctif est prêt et rejoint la branche de la build Insider.
* Ajout du menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836]. Pour l’utiliser, maintenez la touche Maj enfoncée et cliquez avec le bouton droit dans une fenêtre de l’Explorateur.
* Correction du comportement non bloquant du socket unix [GH 2822, 3100]
* Correction de la commande NetLink bloquée comme indiqué dans GH 2026.
* Ajout de la prise en charge des indicateurs de propagation de montage [GH 2911].
* Correction du problème lié à la troncation qui n’engendre pas d’événements inotify [GH 2978].
* Ajout de l’option --exec pour wsl.exe afin d’appeler un seul binaire sans shell.
* Ajout de l’option --distribution pour wsl.exe afin de sélectionner une distribution spécifique.

## <a name="build-17655-skip-ahead"></a>Build 17655 (Skip Ahead)
Pour obtenir des informations Windows d’ordre général sur la build 17655, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Prise en charge limitée de dmesg. Les applications peuvent désormais se connecter à dmesg. Le pilote WSL journalise des informations limitées sur dmesg. À l’avenir, il sera développé pour transporter d’autres informations/diagnostics à partir du pilote.
    * Remarque : dmesg est actuellement pris en charge par le biais de l’interface d’appareil `/dev/kmsg`. L’interface sycall `syslog` n’est pas encore prise en charge. Et donc, certaines des options de ligne de commande `dmesg` comme `-S`, `-C`, ne fonctionnent pas.
* Correction d’un problème où les opérations multithread peuvent retourner ENOENT même si le fichier existe. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Build 17639 (Skip Ahead)
Pour obtenir des informations Windows d’ordre général sur la build 17639, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Changement du gid et du mode par défaut des appareils en série pour qu’ils correspondent aux natifs [GH 3042]
* DrvFs prend désormais en charge les attributs étendus.
    * Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus. En particulier, certains caractères (comme « / », « : » et « \* ») ne sont pas autorisés et les noms d’attributs étendus ne sont pas sensibles à la casse sur DrvFs.

## <a name="build-17133-fast"></a>Build 17133 (Fast)
Pour obtenir des informations Windows d’ordre général sur la build 17133, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Correction du blocage dans WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Build 17128 (Fast)
Pour obtenir des informations Windows d’ordre général sur la build 17128, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Aucune

## <a name="build-17627-skip-ahead"></a>Build 17627 (Skip Ahead)
Pour obtenir des informations Windows d’ordre général sur la build 17627, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Ajout de la prise en charge des opérations futex pi-aware. [GH 1006]
    * Notez qu’actuellement, les priorités ne sont pas une fonctionnalité de WSL prise en charge. Il existe donc des limitations, mais l’utilisation standard doit être débloquée.
* Prise en charge du pare-feu Windows pour les processus WSL. [GH 1852]
    * Par exemple, pour autoriser le processus python WSL à écouter sur n’importe quel port, utilisez la commande Windows avec élévation de privilèges : ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Respectez le shell par défaut de l’utilisateur lors de l’utilisation de wsl.exe. [GH 2372]
* Signalisation de toutes les interfaces réseau en tant qu’Ethernet. [GH 2996]
* Meilleure gestion du fichier /etc/passwd endommagé. [GH 3001]

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17618-skip-ahead"></a>Build 17618 (Skip Ahead)
Pour obtenir des informations Windows d’ordre général sur la build 17618, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Introduction de la fonctionnalité de pseudoconsole pour interop NT [GH 988, 1366, 1433, 1542, 2370, 2406].
* Le mécanisme d’installation hérité (lxrun.exe) est déprécié. Le mécanisme pris en charge pour l’installation des distributions passe par Microsoft Store.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17110"></a>Build 17110
Pour obtenir des informations Windows d’ordre général sur la build 17110, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Autorisation de l’arrêt de /init à partir de Windows [GH 2928].
* DrvFs utilise désormais par défaut le respect de la casse par répertoire (ce qui équivaut à l’option de montage « case=dir »).
    * L’utilisation de « case=force » (ancien comportement) demande la définition d’une clé de Registre. Exécutez la commande suivante pour activer « case=force » si vous avez besoin de l’utiliser : reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui ont besoin d’être sensibles à la casse, utilisez fsutil.exe pour les marquer comme sensibles à la casse : fsutil.exe file setcasesensitiveinfo <path> enable
* Chaînes d’arrêt NULL retournées par uname syscall.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17107"></a>Build 17107
Pour obtenir des informations Windows d’ordre général sur la build 17107, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Prise en charge de TCSETSF et TCSETSW sur les points de terminaison pty maîtres [GH 2552].
* Le démarrage de processus interop simultanés peut entraîner EINVAL [GH 2813].
* Correction de PTRACE_ATTACH pour présenter l’état de suivi approprié dans /proc/pid/status.
* Correction de la concurrence où les processus de courte durée clonés avec des indicateurs CLEARTID et SETTID peuvent quitter sans effacer l’adresse TID.
* Affiche un message lors de la mise à niveau des répertoires du système de fichiers Linux à partir d’une build antérieure à 17093. Pour plus d’informations sur les changements du système de fichiers 17093, consultez les notes de publication de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17101"></a>Build 17101
Pour obtenir des informations Windows d’ordre général sur la build 17101, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Prise en charge de signalfd. [GH 129]
* Prise en charge des noms de fichiers contenant des caractères NTFS non conformes en les encodant en tant que caractères Unicode privés. [GH 1514]
* Le montage automatique repasse en lecture seule quand l’écriture n’est pas prise en charge. [GH 2603]
* Autorisation du collage de paires de substitution Unicode (comme les caractères Emoji). [GH 2765]
* Les pseudofichiers contenus dans /proc et /sys doivent revenir prêts pour la lecture et l’écriture à l’issue de select, poll, epoll et autres [GH 2838]
* Correction du problème qui peut amener le service à tourner infiniment en boucle quand le registre a été falsifié ou qu’il est endommagé.
* Correction des messages netlink pour qu’ils fonctionnent avec la version plus récente (4.14 en amont) de iproute2.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17093"></a>Build 17093
Pour obtenir des informations Windows d’ordre général sur la build 17093, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Important :
Quand vous démarrez WSL pour la première fois après la mise à niveau vers cette build, certaines tâches doivent être effectuées pour mettre à niveau les répertoires du système de fichiers Linux. Ces tâches peuvent prendre plusieurs minutes, c’est pourquoi WSL peut sembler démarrer lentement. Cette lenteur ne devrait se produire qu’une seule fois pour chaque distribution installée à partir du Store.
* Prise en charge améliorée du respect de la casse dans DrvFs.
    * DrvFs prend désormais en charge le respect de la casse par répertoire. Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme sensibles à la casse, ce qui permet même aux applications Windows d’ouvrir correctement les fichiers qui diffèrent uniquement par la casse.
    * DrvFs dispose de nouvelles options de montage contrôlant le respect de la casse par répertoire
        * case=force : tous les répertoires sont traités comme sensibles à la casse (à l’exception de la racine du lecteur). Les nouveaux répertoires créés avec WSL sont marqués comme sensibles à la casse. Il s’agit du comportement hérité, à l’exception du marquage de nouveaux répertoires sensibles à la casse.
        * case=dir : seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme sensibles à la casse ; les autres répertoires ne sont pas sensibles à la casse. Les nouveaux répertoires créés avec WSL sont marqués comme sensibles à la casse.
        * case=off : seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme sensibles à la casse ; les autres répertoires ne sont pas sensibles à la casse. Les nouveaux répertoires créés avec WSL sont marqués comme insensibles à la casse.
    * Remarque : cet indicateur n’est pas défini pour les répertoires créés par WSL dans les versions précédentes, donc ils ne sont pas traités comme sensibles à la casse si vous utilisez l’option « case=dir ». Un moyen de définir cet indicateur sur des répertoires existants sera bientôt disponible.
    * Exemple de montage avec ces options (pour les lecteurs existants, vous devez d’abord démonter avant de pouvoir monter avec des options différentes) : sudo mount -t drvfs C: /mnt/c -o case=dir
    * Pour le moment, case=force est toujours l’option par défaut. Celle-ci sera remplacée par case=dir à l’avenir.
* Vous pouvez maintenant utiliser des barres obliques dans les chemins Windows lors du montage de DrvFs, par exemple : sudo mount -t drvfs //server/share /mnt/share
* WSL traite maintenant le fichier /etc/fstab au démarrage de l’instance [GH 2636].
    * Cette opération est effectuée avant le montage automatique des lecteurs DrvFs. Tous les lecteurs déjà montés par fstab ne sont pas remontés automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.
    * Ce comportement peut être désactivé à l’aide de wsl.conf.
* Les fichiers mount, mountinfo et mountstats dans /proc échappent correctement les caractères spéciaux comme les barres obliques inverses et les espaces [GH 2799]
* Les fichiers spéciaux créés avec DrvFs, comme les liens symboliques WSL, les fichiers FIFO et les sockets quand les métadonnées sont activées, peuvent maintenant être copiés et déplacés à partir de Windows.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL est plus configurable avec wsl.conf
Nous avons ajouté une méthode pour vous permettre de configurer automatiquement certaines fonctionnalités dans WSL afin qu’elles soient appliquées chaque fois que vous lancez le sous-système. Cela comprend les options de montage automatique et la configuration réseau. Découvrez-en davantage dans notre billet de blog sur : https://aka.ms/wslconf

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX autorise les connexions de sockets entre les processus Linux sur WSL et les processus natifs Windows
Les applications WSL et Windows peuvent maintenant communiquer entre elles par le biais de sockets Unix. Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible aux applications à la fois Windows et WSL. Désormais, cela est possible avec des sockets Unix. Pour en savoir plus, consultez notre billet de blog sur https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* Prise en charge de mmap() avec MAP_NORESERVE [GH 121, 2784]
* Prise en charge de CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]
* Gestion du signal de fin non-SIGCHLD dans le clone [GH 121, 2781]
* Stub /proc/sys/fs/inotify/max_user_instances et /proc/sys/fs/inotify/max_user_watches [GH 1705]
* Erreur lors du chargement des binaires ELF qui contiennent des en-têtes de charge avec des décalages non nuls [GH 1884]
* Zéro pour les octets de page de fin lors du chargement des images.
* Réduction des cas où execve arrête silencieusement le processus

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17083"></a>Build 17083
Pour obtenir des informations Windows d’ordre général sur la build 17083, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Correction de la vérification d’erreur liée à epoll [GH 2798, 2801, 2857]
* Correction des blocages lors de la désactivation d’ASLR [GH 1185, 2870]
* Assurance que les opérations mmap apparaissent atomiques [GH 2732]

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17074"></a>Build 17074
Pour obtenir des informations Windows d’ordre général sur la build 17074, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Correction du format de stockage des métadonnées DrvFs [GH 2777] </br>
**Important :** Les métadonnées DrvFs créées avant cette build s’affichent de manière incorrecte ou pas du tout. Pour corriger les fichiers affectés, utilisez chmod et chown pour réappliquer les métadonnées.
* Correction du problème lié à de multiples signaux et syscalls redémarrables.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17063"></a>Build 17063
Pour obtenir des informations Windows d’ordre général sur la build 17063, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs prend en charge des métadonnées Linux supplémentaires. Cette prise en charge permet de définir le propriétaire et le mode des fichiers à l’aide de chmod/chown, ainsi que de créer des fichiers spéciaux, comme les FIFO, les sockets Unix et les fichiers d’appareil. Cette fonctionnalité est désactivée par défaut pour le moment, car elle est toujours expérimentale.
**Remarque :**  Nous avons corrigé un bogue dans le format des métadonnées utilisé par DrvFs. Bien que les métadonnées fonctionnent sur cette build à des fins d’expérimentation, les futures builds ne liront pas correctement les métadonnées créées par cette Build.  Vous devrez peut-être mettre à jour manuellement le propriétaire des fichiers modifiés et vous devrez recréer les appareils dont l’ID est personnalisé.

  Pour activer cette fonctionnalité, montez DrvFs avec l’option métadonnées (pour l’activer sur un montage existant, vous devez d’abord le démonter) :

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Les autorisations Linux sont ajoutées en tant que métadonnées supplémentaires au fichier ; elles n’affectent pas les autorisations Windows.  N’oubliez pas que la modification d’un fichier à l’aide d’un éditeur Windows risque de supprimer les métadonnées. Dans ce cas, le fichier reprend ses autorisations par défaut.

* Ajout d’options de montage à DrvFs pour contrôler les fichiers sans métadonnées.
  * uid : identifiant utilisateur utilisé pour le propriétaire de tous les fichiers.
  * gid : ID de groupe utilisé pour le propriétaire de tous les fichiers.
  * umask : masque octal des autorisations à exclure pour tous les fichiers et répertoires.
  * fmask : masque octal des autorisations à exclure pour tous les fichiers standard.
  * dmask : masque octal des autorisations à exclure pour tous les répertoires.

  Par exemple :
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Combinaison avec l’option de métadonnées pour spécifier des autorisations par défaut pour les fichiers sans métadonnées.

* Introduction d’une nouvelle variable d’environnement, `WSLENV`, pour configurer la façon dont les variables d’environnement circulent entre WSL et Win32.

  Par exemple :

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` est une liste de variables d’environnement séparées par des deux-points qui peuvent être incluses lors du lancement de processus WSL à partir de Win32 ou de processus Win32 à partir de WSL.  Chaque variable peut être suffixée à l’aide d’une barre oblique suivie d’indicateurs pour spécifier son mode de traduction.
  * p : La valeur est un chemin qui doit être traduit entre les chemins WSL et les chemins Win32.
  * l : La valeur est une liste de chemins. Dans WSL, il s’agit d’une liste délimitée par des deux-points. Dans Win32, il s’agit d’une liste délimitée par des points-virgules.
  * u : La valeur doit être incluse uniquement lors de l’appel de WSL à partir de Win32.
  * w : La valeur doit être incluse uniquement lors de l’appel de Win32 à partir de WSL.

  Vous pouvez définir `WSLENV` dans .bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.

* Les montages drvfs préservent correctement les horodatages de tar, cp -p (GH 1939)
* Les liens symboliques drvfs signale la taille correcte (GH 2641)
* La lecture/écriture fonctionne pour de très grandes tailles d’E/S (GH 2653)
* waitpid fonctionne avec des ID de groupe de processus (GH 2534)
* Amélioration significative des performances mmap pour les régions de réserve volumineuses ; amélioration des performances ghc (GH 1671)
* Prise en charge de la personnalité pour READ_IMPLIES_EXEC ; correction de maxima et clisp (GH 1185)
* Prise en charge par mprotect de PROT_GROWSDOWN ; correction de clisp (GH 1128)
* Correction des erreurs de page en mode de survalidation ; correction de sbcl (GH 1128)
* Prise en charge par le clone de davantage de combinaisons d’indicateurs
* Prise en charge select/epoll de fichiers epoll (auparavant un no-op).
* Notification de ptrace des syscalls non implémentés.
* Ignorance des interfaces absentes lors de la génération de serveurs de noms resolv.conf [GH 2694]
* Énumération des interfaces réseau sans adresse physique. [GH 2685]
* Correctifs de bogues et améliorations supplémentaires.

### <a name="linux-tools-available-to-developers-on-windows"></a>Outils Linux disponibles pour les développeurs sur Windows

* Inclusion par la chaîne d’outils de ligne de commande Windows de bsdtar (tar) et de curl.
  Lisez [ce blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et découvrir leur effet sur l’expérience des développeurs sur Windows.

*   `AF_UNIX` est disponible dans le SDK Windows Insider (17061+).
  Lisez [ce blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus sur `AF_UNIX` et sur la manière dont les développeurs sur Windows peuvent l’utiliser.

### <a name="console"></a>Console
* Aucun correctif.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.


## <a name="build-17046"></a>Build 17046

Pour obtenir des informations Windows d’ordre général sur la build 17046, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Autorisation des processus à s’exécuter sans terminal actif. [GH 709, 1007, 1511, 2252, 2391 et autres]
- Meilleure prise en charge de CLONE_VFORK et CLONE_VM. [GH 1878, 2615]
- Ignorance des pilotes de filtre TDI pour les opérations de mise en réseau WSL. [GH 1554]
- DrvFs crée des liens symboliques NT lorsque certaines conditions sont remplies. [GH 353, 1475, 2602]
    - La cible du lien doit être relative, ne doit pas traverser des points de montage ni des liens symboliques et doit exister.
    - L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela nécessite normalement que vous lançiez wsl.exe avec élévation de privilèges), à moins que le mode développeur ne soit activé.
    - Dans toutes les autres situations, DrvFs crée toujours des liens symboliques WSL.
- Autorisation de l’exécution simultanée d’instances WSL avec et sans élévation de privilèges.
- Support /proc/sys/kernel/yama/ptrace_scope
- Ajout de wslpath pour effectuer des conversions de chemins WSL<->Windows. [GH 522, 1243, 1834, 2327 et autres]
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

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.


## <a name="build-17040"></a>Build 17040

Pour obtenir des informations Windows d’ordre général sur la build 17040, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Aucun correctif depuis 17035.

#### <a name="console"></a>Console
- Aucun correctif depuis 17035.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17035"></a>Build 17035

Pour obtenir des informations Windows d’ordre général sur la build 17035, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- L’accès aux fichiers sur DrvFs peut parfois échouer avec EINVAL. [GH 2448]

#### <a name="console"></a>Console
- Perte de couleurs lors de l’insertion/la suppression de lignes en mode VT.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17025"></a>Build 17025

Pour obtenir des informations Windows d’ordre général sur la build 17025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Démarrage des processus initiaux dans un nouveau groupe de processus de premier plan [GH 1653, 2510].
- Correctifs de remise SIGHUP [GH 2496].
- Génération d’un nom de pont virtuel par défaut s’il n’est pas fourni [GH 2497].
- Implémentation de /proc/sys/kernel/random/boot_id [GH 2518].
- Autres correctifs de canal stdout/stderr Interop.
- Appel système syncfs stub.

#### <a name="console"></a>Console
- Correction de la traduction VT d’entrée pour les consoles tierces [GH 111]

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="build-17017"></a>Build 17017

Pour obtenir des informations Windows d’ordre général sur la build 17017, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Ignorance des en-têtes de programme ELF vides [GH 330].
- Autorisation de LxssManager à créer des instances WSL pour les utilisateurs non interactifs (prise en charge de ssh et des tâches planifiées) [GH 777, 1602].
- Prise en charge des scénarios WSL->Win32->WSL (« introduction ») [GH 1228].
- Prise en charge limitée de l’arrêt des applications console appelées par le biais d’Interop [GH 1614].
- Prise en charge d’options de montage pour devpts [GH 1948].
- Blocage du démarrage enfant par Ptrace [GH 2333].
- Événements manquants dans EPOLLET [GH 2462].
- Retour de données supplémentaires pour PTRACE_GETSIGINFO.
- Getdents avec lseek donne des résultats incorrects.
- Correction de certains blocages d’application interop Win32, en attente d’une entrée sur un canal qui n’a plus de données.
- Prise en charge O_ASYNC pour les fichiers tty/pty.
- Améliorations et correctifs de bogues supplémentaires

#### <a name="console"></a>Console
- Aucune modification liée à la console dans cette version.

### <a name="ltp-results"></a>Résultats LTP :
Test en cours.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>Build 16288

Pour obtenir des informations Windows d’ordre général sur la build 16288, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Lancement et signalement corrects des uid, gid et du mode pour les descripteurs de fichiers socket [GH 2490]
- Améliorations et correctifs de bogues supplémentaires

#### <a name="console"></a>Console
- Aucune modification liée à la console dans cette version.

### <a name="ltp-results"></a>Résultats LTP :
Aucune modification depuis 16273

## <a name="build-16278"></a>Build 16278

Pour obtenir des informations Windows d’ordre général sur la build 162738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Annulation explicite du mappage des vues mappées de sections sauvegardées dans un fichier lors du déchirement de l’état LX MM [GH 2415]
- Améliorations et correctifs de bogues supplémentaires

#### <a name="console"></a>Console
- Aucune modification liée à la console dans cette version.

### <a name="ltp-results"></a>Résultats LTP :
Aucune modification depuis 16273

## <a name="build-16275"></a>Build 16275

Pour obtenir des informations Windows d’ordre général sur la build 162735, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Aucune modification liée à WSL dans cette version.

#### <a name="console"></a>Console
- Aucune modification liée à la console dans cette version.

### <a name="ltp-results"></a>Résultats LTP :
Aucune modification depuis 16273

## <a name="build-16273"></a>Build 16273

Pour obtenir des informations Windows d’ordre général sur la build 16273, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Résolution d’un problème lié au signalement occasionnel par DrvFs d’un type de fichier incorrect pour les répertoires [GH 2392]
- Autorisation de la création de sockets NETLINK_KOBJECT_UEVENT pour débloquer des programmes qui utilisent uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Ajout de la prise en charge de la connexion non bloquante [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implémentation de l’indicateur d’appel système de clone CLONE_FS [GH 2242]
- Résolution des problèmes liés à la gestion incorrecte des tabulations ou des guillemets dans NT Interop [GH 1625, 2164]
- Correction de l’erreur d’accès refusé lors de la tentative de redémarrage des instances WSL [GH 651, 2095]
- Implémentation des opérations futex FUTEX_REQUEUE et FUTEX_CMP_REQUEUE [GH 2242]
- Correction des autorisations de divers fichiers SysFs [GH 2214]
- Correction du blocage de l’assemblage Haskell lors de l’installation [GH 2290]
- Implémentation des indicateurs binfmt_misc C, O et P [GH 2103]
- Ajout de /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- Ajout de la prise en charge partielle de l’appel système ioprio_set [GH 498]
- Stub SO_REUSEPORT & ajout de la prise en charge de SO_PASSCRED pour les sockets netlink [GH 69]
- Retour de différents codes d’erreur à partir de RegisterDistribuiton si une distribution est en cours d’installation ou de désinstallation.
- Autorisation de la désinscription des distributions WSL partiellement installées par le biais de wslconfig.exe
- Correction du blocage du test de socket Python à partir de udp::msg_peek
- Améliorations et correctifs de bogues supplémentaires

#### <a name="console"></a>Console
- Aucune modification liée à la console dans cette version.

### <a name="ltp-results"></a>Résultats LTP :
Nombre total de tests : 1904<br/>
Nombre total de tests ignorés : 209<br/>
Nombre total d’échecs : 229<br/>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Build 16257

Pour obtenir des informations Windows d’ordre général sur la build 16257, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Implémentation d’un appel système prlimit64
- Ajout de la prise en charge de ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Stub MSG_MORE pour les sockets TCP [GH 2351]
- Correction du comportement de vecteur auxiliaire AT_EXECFN non valide [GH 2133]
- Correction du comportement de copie/collage pour la console/tty et ajout d’une meilleure gestion du tampon complet [GH 2204, 2131]
- Définition d’AT_SECURE dans le vecteur auxiliaire pour des programmes set-user-ID et set-group-ID [GH 2031]
- Non-gestion de TIOCPGRP par le point de terminaison maître du pseudo-terminal [GH 1063]
- Correction d’lseek pour le rewind des répertoires dans LxFs [GH 2310]
- Verrouillage de /dev/ptmx après une utilisation intensive [GH 1882]
- Améliorations et correctifs de bogues supplémentaires

#### <a name="console"></a>Console
- Correction des lignes horizontales/traits de soulignement partout [GH 2168]
- Correction de l’ordre du processus modifié à l’origine d’une fermeture de NPM plus difficile [GH 2170]
- Ajout de notre nouveau jeu de couleurs : https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>Résultats LTP :
Aucune modification depuis 16251

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`prlimit64`<br/>

### <a name="known-issues"></a>Problèmes connus
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[Problème GitHub 2392 : Dossiers Windows non reconnus par WSL...](https://github.com/Microsoft/BashOnWindows/issues/2392)
Dans la build 16257, WSL rencontre des problèmes lors de l’énumération des fichiers/dossiers Windows par le biais de `/mnt/c/...`.
Ce problème a été résolu et publié dans la build Insiders la semaine démarrant le 14/08/2017.

<br/>

## <a name="build-16251"></a>Build 16251

Pour obtenir des informations Windows d’ordre général sur la build 16251, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Suppression de la balise bêta du composant facultatif WSL. Pour plus d’informations, consultez ce [billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).
- Lancement correct des uid et gid définis et enregistrés pour les binaires set-user-ID et set-group-ID sur exec [GH 962, 1415, 2072]
- Ajout de la prise en charge de ptrace PTRACE_O_TRACEEXIT [GH 555]
- Ajout de la prise en charge de ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]
- Correction de ptrace pour effectuer un arrêt sur les signaux ignorés
- Améliorations et correctifs de bogues supplémentaires

#### <a name="console"></a>Console
- Aucune modification liée à la console dans cette version.

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 768</br>
Nombre de tests ayant échoué : 244</br>
Nombre de tests ignorés : 96</br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Build 16241

Pour obtenir des informations Windows d’ordre général sur la build 16241, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fixe
#### <a name="wsl"></a>WSL
- Aucune modification liée à WSL dans cette version.

#### <a name="console"></a>Console
- Correction de la sortie d’un caractère incorrect pour la décimale des lignes croisées, signalée [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) à l’origine
- Correction de l’absence de texte de sortie affiché dans la page de codes 65001 (UTF8)
- Ne transférez pas les modifications apportées aux valeurs RVB d’une couleur vers d’autres parties de la palette lors de la modification de la sélection. La feuille de propriétés de la console sera ainsi beaucoup plus facile à utiliser.
- Ctrl+S ne semble pas fonctionner correctement
- Annuler la mise en gras/estomper totalement absent des codes d’échappement ANSI [GH 2174]
- La console ne prend pas en charge correctement les thèmes de couleur Vim [GH 1706]
- Impossible de coller des caractères particuliers [GH 2149]
- Le redimensionnement de l’ajustement dynamique interagit de façon étrange avec le redimensionnement d’une fenêtre bash quand des éléments se trouvent sur la ligne de commande/d’édition [GH ConEmu 1123]
- Ctrl-L laisse l’écran sale [GH 1978]
- Bogue de rendu de la console lors de l’affichage de VT sur HDPI [GH 1907]
- Apparence étrange des caractères japonais avec le caractère Unicode U+30FB [GH 2146]
- Améliorations et correctifs de bogues supplémentaires

</br>

## <a name="build-16237"></a>Build 16237

Pour obtenir des informations Windows d’ordre général sur la build 16237, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fixe
- Utilisation d’attributs par défaut pour les fichiers sans EA dans lxfs (racine, racine, 0000)
- Ajout de la prise en charge des distributions qui utilisent des attributs étendus
- Correction du remplissage pour les entrées retournées par getdents et getdents64
- Correction des autorisations pour l’appel système shmctl SHM_STAT [GH 2068]
- Correction de l’état epoll initial incorrect pour tty [GH 2231]
- Correction de DrvFs readdir qui ne retourne pas toutes les entrées [GH 2077]
- Correction de LxFs readdir quand des fichiers ne sont pas liés [GH 2077]
- Autorisation de la rouverture des fichiers drvfs non liés par le biais de procfs
- Ajout d’un remplacement de clé de Registre global pour la désactivation des fonctionnalités WSL (interop/montage de lecteur)
- Correction du nombre de blocs incorrects dans « stat » pour DrvFs (et LxFs) [GH 1894]
- Améliorations et correctifs de bogues supplémentaires

</br>

## <a name="build-16232"></a>Build 16232

Pour obtenir des informations Windows d’ordre général sur la build 16232, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Aucune modification liée à WSL dans cette version.

</br>

## <a name="build-16226"></a>Build 16226

Pour obtenir des informations Windows d’ordre général sur la build 16226, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fixe
- Prise en charge des syscalls liés à xattr (getxattr, setxattr, listxattr, removexattr).
- Prise en charge de security.capablity xattr.
- Amélioration de la compatibilité avec certains filtres et systèmes de fichiers, notamment les serveurs SMB non-MS. [GH #1952]
- Prise en charge améliorée des espaces réservés OneDrive, des espaces réservés GVFS et des fichiers compressés Compact OS.
- Améliorations et correctifs de bogues supplémentaires

</br>

## <a name="build-16215"></a>Build 16215

Pour obtenir des informations Windows d’ordre général sur la build 16215, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fixe
- WSL n’exige plus le mode développeur.
- Prise en charge des jonctions de répertoires dans drvfs.
- Gestion de la désinstallation des packages appx de distribution WSL.
- Mise à jour de procfs pour afficher les mappages privés et partagés.
- Ajout de la possibilité pour wslconfig.exe de nettoyer les distributions partiellement installées ou désinstallées.
- Ajout de la prise en charge de IP_MTU_DISCOVER pour les sockets TCP. [GH 1639, 2115, 2205]
- Déduction de la famille de protocoles pour les routes vers AF_INADDR.
- Améliorations des appareils série [GH 1929].

</br>

## <a name="build-16199"></a>Build 16199

Pour obtenir des informations Windows d’ordre général sur la Build 16199, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Aucune modification liée à WSL dans ces versions.

</br>

## <a name="build-16193"></a>Build 16193

Pour obtenir des informations Windows d’ordre général sur la Build 16193, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Condition de concurrence entre l’envoi de SIGCONT et un arrêt de groupe de threads [GH 1973]
- Modification des appareils tty et pty pour signaler FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]
- Correctif SSH pour IP_OPTIONS
- Déplacement du montage DrvFs vers le démon init [GH 1862, 1968, 1767, 1933]
- Ajout de la prise en charge dans DrvFs des liens symboliques NT suivants.

</br>

## <a name="build-16184"></a>Build 16184

Pour obtenir des informations Windows d’ordre général sur la Build 16184, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Suppression de la tâche de maintenance de package apt (lxrun.exe /update)
- Correction de la sortie qui ne s’affiche pas à partir des processus Windows dans node.js [GH 1840]
- Assouplissement des exigences d’alignement dans lxcore [GH 1794]
- Correction de la gestion de l’indicateur AT_EMPTY_PATH dans plusieurs appels système.
- Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts entraîne un comportement non défini du fichier [GH 544, 966, 1357, 1535, 1615]
- /etc/hosts hérite désormais des entrées du fichier hosts Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Build 16179

Pour obtenir des informations Windows d’ordre général sur la Build 16179, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Aucune modification de WSL cette semaine.

</br>

## <a name="build-16176"></a>Build 16176

Pour obtenir des informations Windows d’ordre général sur la Build 16176, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fixe

- [Prise en charge série activée](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- Ajout de l’option de socket IP IP_OPTIONS [GH 1116]
- Implémentation de la fonction pwritev (lors du chargement du fichier sur nginx/PHP-FPM) [GH 1506]
- Ajout des options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- Prise en charge de l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- Ajout de l’option de socket IP(V6)_MTU pour apps node, traceroute, dig, nslookup, host
- Ajout de l’option de socket IP IPV6_UNICAST_HOPS
- [Améliorations du système de fichiers](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * Autorisation du montage de chemins UNC
    * Activation de la prise en charge de CDFS dans drvfs
    * Gestion correcte des autorisations des systèmes de fichiers réseau dans drvfs
    * Ajout de la prise en charge des lecteurs distants à drvfs
    * Activation de la prise en charge de FAT dans drvfs
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP
Aucune modification depuis 15042

</br>

## <a name="build-16170"></a>Build 16170

Pour obtenir des informations Windows d’ordre général sur la Build 16170, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Nous avons publié un nouveau [billet de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) sur nos efforts pour tester WSL.

### <a name="fixed"></a>Fixe

- Prise en charge de l’option de socket IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- Ajout de la prise en charge de PTRACE_OLDSETOPTIONS. [GH 1692]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP
Aucune modification depuis 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Build 15046 vers Windows 10 Creators Update
Il n’y a plus de correctifs ou fonctionnalités WSL prévus pour être inclus dans Windows 10 Creators Update. Les notes de publication pour WSL reprennent dans les semaines à venir pour les ajouts ciblant la prochaine mise à jour majeure de Windows. Pour obtenir des informations Windows d’ordre général sur la build 15046 et sur les futures versions Insider, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Build 15042

Pour obtenir des informations Windows d’ordre général sur la Build 15042, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fixe

- Correction d’un blocage lors de la suppression d’un chemin se terminant par « .. »
- Résolution d’un problème où FIONBIO ne retourne pas 0 en cas de réussite [GH 1683]
- Résolution du problème avec les lectures de longueur nulle des sockets de datagramme inet
- Correction du blocage possible en raison d’une condition de concurrence dans une recherche drvfs inode [GH 1675]
- Prise en charge étendue des données auxiliaires de socket Unix ; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 737</br>
Nombre de non-réussites (échec, ignoré, etc.) : 255

</br>

## <a name="build-15031"></a>Build 15031

Pour obtenir des informations Windows d’ordre général sur la Build 15031, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction d’un bogue où time(2) se comporte de façon sporadique.
- Correction d’un problème où des syscalls *SIGPROCMASK peuvent corrompre un masque de signal.
- Retour à présent de la longueur de la ligne de commande complète dans la notification de création de processus WSL. [GH 1632]
- WSL signale désormais la sortie du thread par le biais de ptrace pour les blocages de GDB. [GH 1196]
- Correction du bogue où ptys se bloque suite à des E/S tmux lourdes. [GH 1358]
- Correction de la validation du délai d’expiration dans de nombreux appels système (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)
- Ajout de la prise en charge d’eventfd EFD_SEMAPHORE [GH 452]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 737</br>
Nombre de non-réussites (échec, ignoré, etc.) : 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Build 15025

Pour obtenir des informations Windows d’ordre général sur la Build 15025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction du bogue à l’origine de la rupture de grep 2.27 [GH 1578]
- Implémentation de l’indicateur EFD_SEMAPHORE pour eventfd2 syscall [GH 452]
- Implémentation de /proc/[pid]/net/ipv6_route [GH 1608]
- Prise en charge des E/S pilotées par signal pour les sockets de flux Unix [GH 393, 68]
- Prise en charge de F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]
- Implémentation de recvmmsg() syscall [GH 1531]
- Correction du bogue où epoll_wait() n’attendait pas [GH 1609]
- Implémentation de /proc/version_signature
- Tee syscall retourne désormais une erreur si les deux descripteurs de fichier font référence au même canal
- Implémentation du comportement correct pour SO_PEERCRED pour les sockets Unix
- Correction de la gestion du paramètre non valide tkill syscall
- Modifications pour augmenter les performances de drvfs
- Correctif mineur pour le blocage des E/S Ruby
- Correction de recvmsg() qui retourne EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 732</br>
Nombre de non-réussites (échec, ignoré, etc.) : 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Build 15019

Pour obtenir des informations Windows d’ordre général sur la Build 15019, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction du bogue qui signalait incorrectement l’utilisation du procfs dans procfs pour des outils comme htop (GH 823, 945, 971)
- Lors de l’appel de open() avec O_TRUNC sur un fichier existant, inotify génère désormais IN_MODIFY avant IN_OPEN
- Correctifs du socket Unix getsockopt SO_ERROR pour activer postgres [GH 61, 1354]
- Implémentation de /proc/sys/net/core/somaxconn pour le langage GO
- La tâche en arrière-plan de mise à jour du package apt-get s’exécute désormais de façon masquée
- Retrait de l’étendue pour IPv6 localhost (défaillance de Spring-Framework(Java)).
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 714 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 249 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Build 15014

Pour obtenir des informations Windows d’ordre général sur la Build 15014, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixe

- Ctrl+C fonctionne à présent comme prévu
- htop et ps auxw affichent désormais une utilisation correcte des ressources (GH #516)
- Traduction de base des exceptions NT en signaux. (GH #513)
- Échec de fallocate avec ENOSPC en cas d’espace insuffisant au lieu d’EINVAL (GH #1571)
- Ajout de /proc/sys/kernel/sem.
- Implémentation des appels système semop et semtimedop
- Correction des erreurs nslookup avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (GH 69)
- Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 709 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Résumé de syscall
Nombre total de syscalls : 384 </br>
Nombre total implémenté : 235 </br>
Nombre total de stubs : 22 </br>
Nombre total non implémenté : 127 </br>
[Répartition détaillée](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Build 15007

Pour obtenir des informations Windows d’ordre général sur la Build 15007, visitez le [blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Problème connu

- Il existe un bogue connu dans lequel la console ne reconnaît pas une entrée Ctrl+<key>.  Est concernée la commande Ctrl+C qui agit comme une touche « C » normale.

  - Solution : Mappez une autre touche à Ctrl+C. Par exemple, pour mapper Ctrl+K à Ctrl+C, procédez comme suit : `stty intr \^k`.  Ce mappage s’effectue par terminal et doit être effectué à *chaque* lancement de bash. Les utilisateurs peuvent explorer l’option permettant de l’inclure dans leur `.bashrc`

### <a name="fixed"></a>Fixe

- Correction du problème où l’exécution de WSL consomme 100 % d’un cœur de processeur
- Option de socket IP_PKTINFO, IPV6_RECVPKTINFO désormais prise en charge. (GH #851, 987)
- Adresse physique de l’interface réseau tronquée à 16 octets dans lxcore (GH #1452, 1414, 1343, 468, 308)
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 709 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 255 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Build 15002

Pour obtenir des informations Windows d’ordre général sur la Build 15002, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Problème connu

Deux problèmes connus :
- Il existe un bogue connu dans lequel la console ne reconnaît pas une entrée Ctrl+<key>.  Est concernée la commande Ctrl+C qui agit comme une touche « C » normale.

  - Solution : Mappez une autre touche à Ctrl+C. Par exemple, pour mapper Ctrl+K à Ctrl+C, procédez comme suit : `stty intr \^k`.  Ce mappage s’effectue par terminal et doit être effectué à *chaque* lancement de bash. Les utilisateurs peuvent explorer l’option permettant de l’inclure dans leur `.bashrc`

- Pendant l’exécution de WSL, un thread système consomme 100 % d’un cœur de processeur.  La cause racine a été traitée et corrigée en interne.

### <a name="fixed"></a>Fixe

- Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.  Toute tentative de démarrage d’une session à un niveau différent est bloquée.  Cela signifie que les consoles administrateur et non-administrateur ne peuvent pas s’exécuter en même temps. (GH #626)
<br/>
- Implémentation des messages NETLINK_ROUTE suivants (nécessite l’administrateur Windows)
     - RTM_NEWADDR (prend en charge `ip addr add`)
     - RTM_NEWROUTE (prend en charge `ip route add`)
     - RTM_DELADDR (prend en charge `ip addr del`)
     - RTM_DELROUTE (prend en charge `ip route del`)
- La vérification des tâches planifiées pour les packages à mettre à jour ne s’exécute plus sur une connexion limitée (GH #1371)
- Correction de l’erreur où la transmission est bloquée, c.-à-d. bash -c "ls -alR /" | bash -c "cat" (GH #1214)
- Implémentation de l’option de socket TCP_KEEPCNT (GH #843)
- Implémentation de l’option de socket IP_MTU_DISCOVER INET (GH #720, 717, 170, 69)
- Suppression des fonctionnalités héritées pour exécuter des binaires NT à partir du lancement avec recherche de chemin NT. (GH #1325)
- Correction du mode de /dev/kmsg pour autoriser l’accès en lecture au groupe ou autre (0644) (GH #1321)
- Implémentation de /proc/sys/kernel/random/uuid (GH #1092)
- Correction de l’erreur dans laquelle l’heure de début du processus affichée était l’année 2432 (GH #974)
- Basculement de la variable d’environnement TERM par défaut vers xterm-256color (GH #1446)
- Modification de la façon dont la validation de processus est calculée pendant la duplication de processus. (GH #1286)
- Implémentation de /proc/sys/vm/overcommit_memory. (GH #1286)
- Implémentation du fichier /proc/net/route (GH #69)
- Correction de l’erreur où le nom du raccourci n’est pas localisé correctement (GH #696)
- Correction de la logique d’analyse elf qui valide incorrectement les en-têtes de programme devant être inférieurs (ou égaux) à PATH_MAX. (GH #1048)
- Implémentation du rappel statfs pour procfs, sysfs, cgroupfs et binfmtfs (GH #1378)
- Correction des fenêtres AptPackageIndexUpdate qui ne se ferment pas (GH #1184, également décrit dans GH #1193)
- Ajout de la prise en charge de la personnalité ASLR ADDR_NO_RANDOMIZE. (GH #1148, 1128)
- Amélioration de PTRACE_GETSIGINFO, SIGSEGV, pour les arborescences des appels de procédure gdb appropriées pendant AV (GH #875)
- L’analyse elf n’échoue plus pour les binaires patchelf. (GH #471)
- DNS VPN propagé à /etc/resolv.conf (GH #416, 1350)
- Améliorations apportées à la fermeture de TCP pour un transfert de données plus fiable. (GH #610, 616, 1025, 1335)
- Retour d’un code d’erreur correct quand un nombre de fichiers trop élevé sont ouverts (EMFILE). (GH #1126, 2090)
- Le journal d’audit Windows signale désormais le nom de l’image dans le processus de création d’audit.
- Échec de bonne grâce lors du lancement de bash.exe à partir d’une fenêtre bash
- Ajout d’un message d’erreur quand interop n’est pas en mesure d’accéder à un répertoire de travail sous LxFs (c.-à-d. Bloc-notes.exe .bashrc)
- Correction du problème de troncation du chemin Windows dans WSL
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 690 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 274 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Build 14986

Pour obtenir des informations Windows d’ordre général sur la build 14986, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fixe

- Correction des vérifications d’erreurs avec des IOCTL Netlink et Pty
- La version du noyau signale maintenant 4.4.0-43 à des fins de cohérence avec Xenial
- Bash.exe se lance maintenant quand l’entrée est dirigée vers « nul: » (GH #1259)
- Les ID de thread sont désormais signalés correctement dans procfs (GH #967)
- Les indicateurs IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR sont désormais pris en charge dans inotify_add_watch() (GH #1280)
- Implémentation de timer_create et des appels système associés.  Cela permet la prise en charge de GHC (GH #307)
- Correction du problème où ping retourne une heure de 0.000ms (GH #1296)
- Retour d’un code d’erreur correct quand un nombre de fichiers trop élevé sont ouverts.
- Résolution d’un problème dans WSL où la demande Netlink de données d’interface réseau échoue avec EINVAL si l’adresse matérielle de l’interface correspond à 32 octets (comme l’interface Teredo)
   - Notez que l’utilitaire « ip » Linux contient un bogue qui entraîne un incident si WSL signale une adresse matérielle à 32 octets. Il s’agit d’un bogue dans « ip », et non WSL. L’utilitaire « ip » code en dur la longueur du tampon de chaîne utilisé pour imprimer l’adresse matérielle et ce tampon est trop petit pour imprimer une adresse matérielle à 32 octets.
- Correctifs et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 669 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 258 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Build 14971

Pour obtenir des informations Windows d’ordre général sur la build 14971, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fixe

 - En raison de circonstances hors de notre contrôle, il n’existe aucune mise à jour dans cette build pour le sous-système Windows pour Linux.  Les mises à jour planifiées régulièrement reprennent à la prochaine version.

### <a name="ltp-results"></a>Résultats LTP :
Inchangés par rapport à 14965 </br>
Nombre de tests réussis : 664 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Build 14965

Pour obtenir des informations Windows d’ordre général sur la build 14965, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fixe

- Prise en charge des sockets Netlink RTM_GETLINK et RTM_GETADDR du protocole NETLINK_ROUTE (GH #468)
  - Activation des commandes ifconfig et ip pour l’énumération réseau
  - Pour plus d’informations, consultez notre [billet de blog sur la mise en réseau WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- /sbin est désormais dans le chemin de l’utilisateur par défaut
- Le chemin de l’utilisateur NT est maintenant ajouté au chemin WSL par défaut (par exemple, vous pouvez maintenant taper Bloc-notes.exe sans ajouter System32 au chemin Linux)
- Ajout de la prise en charge de /proc/sys/kernel/cap_last_cap
- Les binaires NT peuvent maintenant être lancés à partir de WSL quand le répertoire de travail actuel contient des caractères non-ANSI (GH #1254)
- Autorisation de l’arrêt sur le socket de flux Unix déconnecté.
- Ajout de la prise en charge de PR_GET_PDEATHSIG.
- Ajout de la prise en charge de CLONE_PARENT
- Correction de l’erreur où la transmission est bloquée, c.-à-d. bash -c "ls -alR /" | bash -c "cat" (GH #1214)
- Gestion des requêtes de connexion au terminal actuel.
- Marquage de /proc/<pid>/oom_score_adj as writable.
- Ajout du dossier /sys/fs/cgroup.
- sched_setaffinity doit retourner le maque du nombre de bits d’affinité
- Correction de la logique de validation ELF qui suppose à tors que les chemins de l’interpréteur ne doivent pas comprendre plus de 64 caractères. (GH #743)
- Les descripteurs de fichiers ouverts peuvent maintenir la fenêtre de console ouverte (GH #1187)
- Correction d’une erreur liée à l’échec de rename() avec une barre oblique de fin sur le nom cible (GH #1008)
- Implémentation du fichier /proc/net/dev
- Correction de commandes ping 0.000ms dues à la résolution du minuteur.
- Implémentation de /proc/self/environ (GH #730)
- Corrections de bogues et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 664 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Build 14959

Pour obtenir des informations Windows d’ordre général sur la build 14959, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fixe

- Notification de processus Pico améliorée pour Windows.  Informations supplémentaires disponibles sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).
- Amélioration de la stabilité avec l’interopérabilité Windows
- Correction de l’erreur 0x80070057 lors du lancement de bash.exe quand la protection des données d’entreprise (PDE) est activée
- Corrections de bogues et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 665 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Build 14955

Pour obtenir des informations Windows d’ordre général sur la build 14955, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fixe

 - En raison de circonstances hors de notre contrôle, il n’existe aucune mise à jour dans cette build pour le sous-système Windows pour Linux.  Les mises à jour planifiées régulièrement reprennent à la prochaine version.

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 665 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Build 14951

Pour obtenir des informations Windows d’ordre général sur la build 14951, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Nouvelle fonctionnalité : Interopérabilité Windows/Ubuntu
Les binaires Windows peuvent désormais être appelés directement à partir de la ligne de commande WSL.  Cela permet aux utilisateurs d’interagir avec leurs environnement et système Windows d’une manière qui n’était auparavant pas possible.  En guise d’exemple rapide, il est maintenant possible pour les utilisateurs d’exécuter les commandes suivantes :

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

D’autres informations sont disponibles ici :

- [Blog de l’équipe WSL pour Interop](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [Documentation MSDN Interop](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>Fixe

- Ubuntu 16.04 (Xenial) est maintenant installé pour toutes les nouvelles instances WSL.  Les utilisateurs avec des instances 14.04 (Trusty) existantes ne sont pas automatiquement mis à niveau.
- Les paramètres régionaux définis lors de l’installation s’affichent désormais
- Améliorations apportées au terminal, notamment correction du bogue lié à la redirection d’un processus WSL vers un fichier
- La durée de vie de la console doit être liée à celle de bash.exe
- La taille de la fenêtre de console doit utiliser la taille visible, pas la taille du tampon
- Corrections de bogues et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 665 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Build 14946

Pour obtenir des informations Windows d’ordre général sur la build 14946, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fixe

- Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT contenant des espaces ou des guillemets. 
- Modification de VolFs et DrvFs pour retourner 0 pour le nombre de liens du répertoire dans stat
- Prise en charge de l’option de socket IPV6_MULTICAST_HOPS.
- Limitation à une seule boucle d’E/S de console par tty. Par exemple, la commande suivante est possible :
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- Remplacement des espaces par des tabulations dans /proc/cpuinfo (GH #1115)
- DrvFs apparaît maintenant dans mountinfo avec un nom qui correspond au volume Windows monté
- /home et /root apparaissent désormais dans mountinfo avec des noms corrects
- Corrections de bogues et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 665 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Build 14942

Pour obtenir des informations Windows d’ordre général sur la build 14942, visitez le [blog Windows](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fixe

- Traitement de plusieurs vérifications de bogues, notamment l’incident de la mise en réseau « ATTEMPTED EXECUTE OF NOEXECUTE MEMORY » qui bloque SSH
- Prise en charge d’inotifiy pour les notifications générées à partir d’applications Windows sur DrvFs
- Implémentation de TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod. (GH #695)
- Implémentation de l’appel système pivot_root
- Implémentation de l’option de socket pour SO_DONTROUTE
- Corrections de bogues et améliorations supplémentaires


### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 665 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 263 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Build 14936

Pour obtenir des informations Windows d’ordre général sur la build 14936, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Remarque : WSL va installer Ubuntu version 16.04 (Xenial) au lieu d’Ubuntu 14.04 (Trusty) dans une prochaine version.  Cette modification s’appliquera aux versions Insiders qui installent de nouvelles instances (lxrun.exe /install ou première exécution de bash.exe).  Les instances existantes avec Trusty ne sont pas mises à niveau automatiquement. Les utilisateurs peuvent mettre à niveau leur image Trusty vers Xenial à l’aide de la commande do-release-upgrade.

### <a name="known-issue"></a>Problème connu
WSL rencontre un problème avec certaines implémentations de sockets.  La vérification de bogue se manifeste comme un incident avec l’erreur « ATTEMPTED EXECUTE OF NOEXECUTE MEMORY ».  La manifestation la plus courante de ce problème est un incident lors de l’utilisation de ssh.  La cause racine est résolue sur les builds internes et envoyée (push) aux versions Insiders dès que possible.

### <a name="fixed"></a>Fixe

- Implémentation de l’appel système chroot
- Améliorations apportées à inotify, ~~notamment la prise en charge des notifications générées à partir d’applications Windows sur DrvFs~~
  - Correction : Prise en charge d’inotify pour les modifications provenant d’applications Windows non disponibles pour le moment.
- La liaison de socket à IPV6::<port n> prend désormais en charge IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)
- Implémentation du comportement WNOWAIT pour l’appel système waitid (GH #638)
- Prise en charge des options de socket IP IP_HDRINCL et IP_TTL
- Retour immédiat de read() de longueur nulle (GH #975)
- Gestion correcte des noms de fichiers et des préfixes de noms de fichiers qui n’incluent pas de marque de fin NULL dans un fichier .tar.
- Prise en charge d’epoll pour /dev/null
- Correction de la source de temps /dev/alarm
- Capacité de Bash -c à effectuer une redirection vers un fichier
- Corrections de bogues et améliorations supplémentaires

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 664 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 264 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Build 14931

Pour obtenir des informations Windows d’ordre général sur la build 14931, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fixe

 - En raison de circonstances hors de notre contrôle, il n’existe aucune mise à jour dans cette build pour le sous-système Windows pour Linux.  Les mises à jour planifiées régulièrement reprennent à la prochaine version.

<br/>

## <a name="build-14926"></a>Build 14926

Pour obtenir des informations Windows d’ordre général sur la build 14926, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fixe

- Ping fonctionne désormais dans les consoles qui ne disposent pas de privilèges administrateur
- Ping6 désormais pris en charge, également sans privilèges administrateur
- Prise en charge par inotify des fichiers modifiés par le biais de WSL. (GH #216)
  - Indicateurs pris en charge :
    - inotify_init1 : LX_O_CLOEXEC, LX_O_NONBLOCK
    - Événements inotify_add_watch : LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - Attributs inotify_add_watch : LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - Sortie de lecture : LX_IN_ISDIR, LX_IN_IGNORED
  - Problème connu : La modification de fichiers à partir d’applications Windows ne génère pas d’événements
- Le socket Unix prend désormais en charge SCM_CREDENTIALS

### <a name="ltp-results"></a>Résultats LTP :
Nombre de tests réussis : 651 </br>
Nombre de non-réussites (échec, ignoré, etc.) : 258 </br>
[Journaux de la série de tests LTP](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Build 14915

Pour obtenir des informations Windows d’ordre général sur la build 14915, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fixe
-  Paire de sockets pour les sockets de datagramme Unix (GH #262)
- Prise en charge des sockets Unix pour SO_REUSEADDR
- Prise en charge des sockets UNIX pour SO_BROADCAST (GH #568)
- Prise en charge des sockets Unix pour SOCK_SEQPACKET (GH #758, #546)
- Ajout de la prise en charge de l’envoi, de la réception et de l’arrêt des sockets de datagramme Unix
- Correction de la vérification de bogue due à une validation de paramètre mmap non valide pour les adresses non fixes. (GH #847)
- Prise en charge de l’interruption/la reprise des états des terminaux
- Prise en charge de l’IOCTL TIOCPKT pour débloquer l’utilitaire Screen (GH #774)
    - Problème connu : Clés de fonction non opérationnelles
- Correction d’une concurrence dans TimerFd qui peut provoquer l’accès à un membre libéré « ReaderReady » par LxpTimerFdWorkerRoutine (GH #814)
- Activation de la prise en charge des appels système redémarrables pour futex, poll et clock_nanosleep
- Ajout de la prise en charge du montage de liaison
- Prise en charge de l’annulation du partage des espaces de noms de montage
    - Problème connu : Quand vous créez un espace de noms de montage avec `unshare(CLONE_NEWNS)`, le répertoire de travail actuel continue de pointer vers l’ancien espace de noms
- Améliorations et correctifs de bogues supplémentaires

<br/>

## <a name="build-14905"></a>Build 14905

Pour obtenir des informations Windows d’ordre général sur la build 14905, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fixe
- Prise en charge des appels système redémarrables (GH #349, GH #520)
- Les liens symboliques vers des répertoires se terminant par / sont maintenant opérationnels (GH #650)
- Implémentation de la commande IOCTL RNDGETENTCNT pour /dev/random
- Implémentation des fichiers /proc/[pid]/mounts, /proc/[pid]/mountinfo et /proc/[pid]/mountstats
- Corrections de bogues et améliorations supplémentaires

</br>

## <a name="build-14901"></a>Build 14901
Première build Insider pour la version ultérieure à la mise à jour anniversaire Windows 10.

Pour obtenir des informations Windows d’ordre général sur la build 14901, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fixe
- Correction du problème lié à la barre oblique de fin
    - Les commandes comme `$ mv a/c/ a/b/` fonctionnent à présent
- L’installation demande à présent si les paramètres régionaux Ubuntu doivent être définis sur les paramètres régionaux Windows
- Prise en charge de procfs pour le dossier ns
- Ajout du montage et démontage pour les systèmes de fichiers tmpfs, procfs et sysfs
- Correction de la signature ABI 32 bits de mknod[at]
- Déplacement des sockets Unix vers le modèle de distribution
- La taille du tampon de réception des sockets INET définie à l’aide de setsockopt doit être respectée
- Implémentation de l’indicateur de message de réception de socket Unix MSG_CMSG_CLOEXEC
- Redirection des canaux stdin/stdout de processus Linux (GH #2)
    - Autorisation de la transmission de commandes bash -c dans CMD.  Exemple : >dir | bash -c "grep foo"
- Bash peut maintenant être installé sur des systèmes avec plusieurs fichiers d’échange (GH #538, #358)
- La taille du tampon des sockets INET par défaut doit correspondre à celle du programme d’installation Ubuntu par défaut
- Alignement des syscalls xattr sur listxattr
- Retour des interfaces avec une adresse IPv4 valide uniquement depuis SIOCGIFCONF
- Correction de l’action par défaut du signal quant elle est injectée par ptrace
- Implémentation de /proc/sys/vm/min_free_kbytes
- Utilisation des valeurs de Registre du contexte d’ordinateur lors de la restauration du contexte dans sigreturn
    - Le problème de blocage de java et javac est ainsi résolu pour certains utilisateurs
- Implémentation de /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Build 14388 vers Mise à jour anniversaire Windows 10
Pour obtenir des informations Windows d’ordre général sur la build 14388, visitez le [blog Windows](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fixe
- Correctifs pour préparer la mise à jour anniversaire Windows 10 du 2 août
  - Pour plus d’informations sur WSL dans la mise à jour anniversaire, consultez notre [blog](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>Build 14376
Pour obtenir des informations Windows d’ordre général sur la build 14376, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fixe
- Suppression de certaines instances où apt-get se bloque (GH #493)
- Résolution d’un problème lié à une gestion incorrecte des montages vides
- Correction d’un problème lié au montage incorrect des RAMDISK
- Modification de l’acceptation des sockets UNIX pour prendre en charge les indicateurs (GH #451 partiel)
- Correction de l’écran bleu lié au réseau commun
- Correction de l’écran bleu lors de l’accès à /proc/[pid]/task (GH #523)
- Correction de l’utilisation élevée du processeur pour certains scénarios pty (GH #488, #504)
- Corrections de bogues et améliorations supplémentaires

<br/>

## <a name="build-14371"></a>Build 14371
Pour obtenir des informations Windows d’ordre général sur la build 14371, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fixe
- Correction de la concurrence de timing avec SIGCHLD et wait() lors de l’utilisation de ptrace
- Correction de certains comportements quand les chemins se terminent par une barre oblique / (GH #432)
- Résolution du problème lié à l’échec du renommage/de l’annulation de lien en raison de handles ouverts vers des enfants
- Corrections de bogues et améliorations supplémentaires

<br/>

## <a name="build-14366"></a>Build 14366
Pour obtenir des informations Windows d’ordre général sur la build 14366, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fixe
- Correction de la création de fichiers par le biais de liens symboliques
-   Ajout de listxattr pour Python (GH 385)
-   Corrections de bogues et améliorations supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
-   Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Build 14361
Pour obtenir des informations Windows d’ordre général sur la build 14361, visitez le [blog Windows](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fixe
- DrvFs est maintenant sensible à la casse lors de l’exécution dans Bash sur Ubuntu sur Windows.
  - Les utilisateurs peuvent utiliser case.txt et CASE.TXT sur leurs lecteurs /mnt/c
  - Le respect de la casse est pris en charge uniquement dans bash sur Ubuntu sur Windows. En dehors de Bash, le système NTFS signale les fichiers correctement, mais un comportement inattendu peut se produire lors de l’interaction avec les fichiers à partir de Windows.
  - La racine de chaque volume (c.-à-d. /mnt/c) n’est pas sensible à la casse
  - Pour plus d’informations sur la gestion de ces fichiers dans Windows, consultez [cet article](https://support.microsoft.com/en-us/kb/100625).
- Prise en charge considérablement améliorée de pty/tty.  Prise en charge d’applications comme TMUX (GH #40)
- Résolution d’un problème d’installation où les comptes d’utilisateur ne sont pas toujours créés
- Optimisation de la structure d’arguments de la ligne de commande permettant une liste d’arguments extrêmement longue. (GH #153)
- Possibilité de supprimer et d’utiliser chmod sur des fichiers read_only de DrvFs
- Correction de certaines instances où le terminal se bloque lors de la déconnexion (GH #43)
- chmod et chown fonctionnent désormais sur les appareils tty
- Autorisation de la connexion à 0.0.0.0 et :: en tant que localhost (GH #388)
- Gestion d’une longueur de vecteur d’E/S >1 pour sendmsg/recvmsg (GH #376 partiel)
- Les utilisateurs peuvent désormais se désinscrire du fichier d’hôtes générés automatiquement (GH #398)
- Correspondance automatique des paramètres régionaux Linux avec les paramètres régionaux NT pendant l’installation (GH #11)
- Ajout du fichier /proc/sys/vm/swappiness (GH #306)
- Fermeture correcte de strace
- Autorisation de la rouverture des canaux par le biais de /proc/self/fd (GH #222)
- Masquage des répertoires sous %LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)
- Meilleure gestion de bash.exe ~.  Prise en charge des commandes comme « bash ~ -c ls » (GH #467)
- Les sockets notifient désormais la lecture epoll disponible pendant l’arrêt (GH #271)
- Meilleure suppresion des fichiers et dossiers par lxrun /uninstall
- Correction de ps -f (GH #246)
- Prise en charge améliorée des applications x11 comme xEmacs (GH #481)
- Mise à jour de la taille de la pile des threads initiale pour qu’elle corresponde au paramètre Ubuntu par défaut et signale la taille correctement au syscall get_rlimit (GH #172, #258)
- Amélioration du signalement des noms d’image de processus pico (par exemple, pour l’audit)
- Implémentation de /proc/mountinfo pour la commande df
- Correction du code d’erreur de lien symbolique pour le nom d’enfant . et .
- Améliorations et corrections de bogues supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Build 14352
Pour obtenir des informations Windows d’ordre général sur la build 14352, visitez le [blog Windows](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fixe
- Résolution d’un problème lié au téléchargement/à la création incorrects de fichiers volumineux.  npm et d’autres scénarios doivent s’en retrouver débloqués (GH #3, GH #313)
- Suppression de certaines instances où les sockets se bloquent
- Correction de certaines erreurs de ptrace
- Résolution d’un problème lié à WSL qui autorise des noms de fichiers contenant plus de 255 caractères
- Amélioration de la prise en charge des caractères non anglais
- Ajout et définition par défaut des données de fuseau horaire Windows actuelles
- ID d’appareil unique pour chaque point de montage (correctif jre – GH #49)
- Correction du problème liés aux chemins contenant « . » et « .. »
- Ajout de la prise en charge FIFO (GH #71)
- Mise à jour du format de resolv.conf pour correspondre au format Ubuntu natif
- Nettoyage de certains procfs
- Activation de ping pour les consoles administrateur (GH #18)

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Build 14342
Pour obtenir des informations Windows d’ordre général sur la build 14342, visitez le [blog Windows](https://aka.ms/wip14342). <br/>

Pour plus d’informations sur VolFs et DriveFs, consultez le [blog WSL](https://blogs.msdn.microsoft.com/wsl). <br/>

### <a name="fixed"></a>Fixe
- Résolution du problème d’installation quand le nom d’utilisateur Windows contient des caractères Unicode
- La solution de contournement apt-get update udev dans les questions fréquentes (FAQ) est désormais fournie par défaut lors de la première exécution
- Activation de liens symboliques dans les répertoires DriveFs (/mnt/<drive>)
- Fonctionnement des liens symboliques entre DriveFs et VolFs
- Traitement du problème d’analyse du chemin de niveau supérieur : fonctionnement comme prévu de ls .//
- Fonctionnement de l’installation de npm sur DriveFs et des options -g
- Résolution du problème empêchant le lancement du serveur PHP
- Mise à jour des valeurs d’environnement par défaut, comme $PATH pour correspondre davantage à Ubuntu natif
- Ajout d’une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache de package apt
- Résolution du problème lié à la validation de l’en-tête ELF, prise en charge par WSL de toutes les options Melkor
- Interpréteur de commandes Zsh fonctionnel
- Prise en charge des binaires Go précompilés
- Localisation correcte de l’invite lors de la première exécution de Bash.exe
- Retour d’informations correctes par /proc/meminfo
- Prise en charge des sockets dans VFS
- Montage de /dev en tant que tempfs
- Prise en charge de FIFO
- Présentation correcte des systèmes multicœurs dans /proc/cpuinfo
- Téléchargement d’améliorations et de messages d’erreur supplémentaires lors de la première exécution
- Améliorations et corrections de bogues syscall. Prise en charge de la liste syscall ci-dessous.
- Corrections de bogues et améliorations supplémentaires

### <a name="known-issues"></a>Problèmes connus
- Résolution incorrecte de « .. » sur DriveFs dans certains cas

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL. Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

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

## <a name="build-14332"></a>Build 14332

Pour obtenir des informations Windows d’ordre général sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fixe
- Meilleure génération de resolv.conf, y compris la hiérarchisation des entrées DNS
- Problème lié au déplacement de fichiers et de répertoires entre des lecteurs /mnt et non-/mnt
- Création désormais possible de fichiers tar avec des liens symboliques
- Ajout du répertoire /run/lock par défaut lors de la création de l’instance
- Mise à jour de /dev/null pour retourner des informations statistiques appropriées
- Erreurs supplémentaires lors du téléchargement pendant la première exécution
- Améliorations et corrections de bogues syscall. Prise en charge de la liste syscall ci-dessous.
- Améliorations et corrections de bogues supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
Voici le nouveau syscall qui a une certaine implémentation dans WSL. Le syscall figurant dans cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Build 14328

Pour obtenir des informations Windows d’ordre général sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Nouvelles fonctionnalités
* Prise en charge des utilisateurs Linux.  L’installation de Bash sur Ubuntu sur Windows vous invite à créer un utilisateur Linux.  Pour plus d’informations, visitez https://aka.ms/wslusers.
* Le nom d’hôte est maintenant défini sur le nom de l’ordinateur Windows, pas sur @localhost
* Pour plus d’informations sur la build 14328, visitez : https://aka.ms/wip14328

### <a name="fixed"></a>Fixe
* Améliorations des liens symboliques pour les fichiers non/mnt/<drive>
    * Fonctionnement de l’installation npm
    * Installation désormais possible de jdk/jre en suivant les instructions données [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).
    * Problème connu : les liens symboliques ne fonctionnent pas pour les montages Windows.  Cette fonctionnalité sera disponible dans une prochaine version
* Affichage de top et htop
* Messages d’erreur supplémentaires pour certains échecs d’installation
* Améliorations et corrections de bogues syscall.  Prise en charge de la liste syscall ci-dessous.
* Améliorations et corrections de bogues supplémentaires

### <a name="syscall-support"></a>Prise en charge de syscall
Voici la liste des syscalls qui ont une certaine implémentation dans WSL.  Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.

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
