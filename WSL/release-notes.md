---
title: Notes de version de sous-système Windows pour Linux
description: Notes de publication pour le sous-système Windows pour Linux.  Mise à jour chaque semaine.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 3eee7ff6d1f8302e98cde84fccabf5d9113c83f2
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063627"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="690d8-105">Notes de version de sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="690d8-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18342"></a><span data-ttu-id="690d8-106">Build 18342</span><span class="sxs-lookup"><span data-stu-id="690d8-106">Build 18342</span></span>
<span data-ttu-id="690d8-107">Pour Windows général plus d’informations sur la build 18342 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="690d8-107">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-108">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-108">WSL</span></span>
* <span data-ttu-id="690d8-109">Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans une distribution WSL à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-109">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="690d8-110">Ces fichiers sont accessibles via la ligne de commande et également des applications Windows, comme l’Explorateur de fichiers, VSCode, etc. peuvent interagir avec ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="690d8-110">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="690d8-111">Accéder à vos fichiers en accédant à \\ \\wsl$\\< distro_name >, ou afficher la liste des distributions en cours d’exécution en accédant à \\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="690d8-111">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="690d8-112">Ajouter des balises d’informations supplémentaires du processeur et de corriger les valeurs de Cpus_allowed [_liste] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="690d8-112">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="690d8-113">Prend en charge exec de thread non leader [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="690d8-113">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="690d8-114">Traiter les échecs de mise à jour de configuration comme non irrécupérable [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="690d8-114">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="690d8-115">Mettre à jour binfmt pour gérer correctement les décalages [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="690d8-115">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="690d8-116">Activer le mappage des lecteurs réseau pour planifier 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="690d8-116">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="690d8-117">Prise en charge Windows -> Linux et Linux -> traduction de chemin d’accès Windows pour les montages de liaisons</span><span class="sxs-lookup"><span data-stu-id="690d8-117">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="690d8-118">Créer des sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule</span><span class="sxs-lookup"><span data-stu-id="690d8-118">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="690d8-119">Build 18334</span><span class="sxs-lookup"><span data-stu-id="690d8-119">Build 18334</span></span>
<span data-ttu-id="690d8-120">Pour Windows général plus d’informations sur la build 18334 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="690d8-120">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-121">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-121">WSL</span></span>
* <span data-ttu-id="690d8-122">Redéfinir la façon que le fuseau horaire de Windows est mappé à un fuseau horaire de Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="690d8-122">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="690d8-123">Corriger les fuites de mémoire et ajouter de nouvelles fonctions de traduction de chaîne [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="690d8-123">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="690d8-124">SIGCONT sur un threadgroup avec aucun thread n’est une absence d’opération [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="690d8-124">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="690d8-125">Afficher correctement les descripteurs de fichier socket et epoll /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="690d8-125">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="690d8-126">Build 18305</span><span class="sxs-lookup"><span data-stu-id="690d8-126">Build 18305</span></span>
<span data-ttu-id="690d8-127">Pour Windows général plus d’informations sur la build 18305 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="690d8-127">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-128">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-128">WSL</span></span>
* <span data-ttu-id="690d8-129">pthreads perdre l’accès aux fichiers quand le thread principal s’arrête [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="690d8-129">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="690d8-130">TIOCSCTTY doit ignorer le paramètre « force », sauf si elle est nécessaire [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="690d8-130">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="690d8-131">améliorations de ligne de commande wsl.exe et ajout d’importation / exportation de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="690d8-131">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="690d8-132">Build 18277</span><span class="sxs-lookup"><span data-stu-id="690d8-132">Build 18277</span></span>
<span data-ttu-id="690d8-133">Pour Windows général plus d’informations sur la build 18277 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="690d8-133">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-134">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-134">WSL</span></span>
* <span data-ttu-id="690d8-135">Corriger l’erreur « interface non pris en charge » introduit dans la version 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="690d8-135">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="690d8-136">Ignorer l’indicateur MNT_FORCE pour syscall unmount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="690d8-136">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="690d8-137">Interopérabilité WSL de commutateur à utiliser l’API CreatePseudoConsole officiel</span><span class="sxs-lookup"><span data-stu-id="690d8-137">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="690d8-138">Mettre à jour aucune valeur de délai d’attente lorsque FUTEX_WAIT redémarre</span><span class="sxs-lookup"><span data-stu-id="690d8-138">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="690d8-139">Build 18272</span><span class="sxs-lookup"><span data-stu-id="690d8-139">Build 18272</span></span>
<span data-ttu-id="690d8-140">Pour Windows général plus d’informations sur la build 18272 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="690d8-140">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-141">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-141">WSL</span></span>
* <span data-ttu-id="690d8-142">**AVERTISSEMENT :** Il existe un problème dans la génération qui rend WSL inutilisable.</span><span class="sxs-lookup"><span data-stu-id="690d8-142">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="690d8-143">Lorsque vous tentez de lancer votre distribution, vous verrez une erreur « Interface non pris en charge ».</span><span class="sxs-lookup"><span data-stu-id="690d8-143">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="690d8-144">Le problème a été résolu et sera dans la build de la semaine prochaine Insider rapide.</span><span class="sxs-lookup"><span data-stu-id="690d8-144">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="690d8-145">Si vous avez installé cette build, vous pouvez revenir à la build précédente de Windows à l’aide de « Go revenir à la version précédente de Windows 10 » dans les paramètres -> mise à jour & sécurité -> Recovery.</span><span class="sxs-lookup"><span data-stu-id="690d8-145">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="690d8-146">Build 18267</span><span class="sxs-lookup"><span data-stu-id="690d8-146">Build 18267</span></span>
<span data-ttu-id="690d8-147">Pour Windows général plus d’informations sur la build 18267 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="690d8-147">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-148">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-148">WSL</span></span>
* <span data-ttu-id="690d8-149">Corrigez le problème dans lequel les processus inactifs ne peuvent pas différentes et rester indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="690d8-149">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="690d8-150">WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="690d8-150">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="690d8-151">Autoriser fsync échoué pour les fichiers en lecture seule sur DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="690d8-151">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="690d8-152">Vérifiez que les répertoires /bin et /sbin existent avant de créer des liens symboliques à l’intérieur de [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="690d8-152">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="690d8-153">Ajouter un mécanisme de délai d’attente d’arrêt instance pour les instances WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-153">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="690d8-154">Le délai d’attente est actuellement définie sur 15 secondes, ce qui signifie que l’instance s’arrête dès que le dernier processus WSL quitte les 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="690d8-154">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="690d8-155">Pour mettre fin immédiatement à une distribution, utilisez :</span><span class="sxs-lookup"><span data-stu-id="690d8-155">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="690d8-156">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="690d8-156">Build 17763 (1809)</span></span>
<span data-ttu-id="690d8-157">Pour Windows général plus d’informations sur la build 17763 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="690d8-157">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-158">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-158">WSL</span></span>
* <span data-ttu-id="690d8-159">Vérification des autorisations SetPriority syscall trop stricte pour modifier la priorité de thread même [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="690d8-159">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="690d8-160">Garantir que les temps d’interruption non biaisée est utilisé pour le démarrage pour éviter le renvoi des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="690d8-160">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="690d8-161">Gérer les liens symboliques dans l’interpréteur de binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="690d8-161">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="690d8-162">Meilleure gestion de nettoyage de descripteur de fichier de leader threadgroup.</span><span class="sxs-lookup"><span data-stu-id="690d8-162">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="690d8-163">Commutateur WSL à utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter du afin d’éviter le dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="690d8-163">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="690d8-164">Ptrace attacher mai provoquer la mauvaise valeur de retour à partir des appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="690d8-164">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="690d8-165">Correctif que relatif AF_UNIX plusieurs problèmes [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="690d8-165">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="690d8-166">Correction d’un problème qui provoquait interop WSL échoue si le répertoire de travail actuel est inférieur à 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="690d8-166">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="690d8-167">Éviter un délai deuxième échec des connexions de bouclage aux ports inexistant [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="690d8-167">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="690d8-168">Ajouter un fichier stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="690d8-168">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="690d8-169">Informations de portée IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="690d8-169">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="690d8-170">Prise en charge PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="690d8-170">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="690d8-171">Canal de système de fichiers par inadvertance effacement epoll déclenchée par edge événement [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="690d8-171">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="690d8-172">Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="690d8-172">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="690d8-173">Prise en charge de zombie [GH 1353] améliorée</span><span class="sxs-lookup"><span data-stu-id="690d8-173">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="690d8-174">Ajouter des entrées wsl.conf pour contrôler le comportement d’interopérabilité Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="690d8-174">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="690d8-175">Correctif pour getsockname pas toujours renvoyer le type de famille du socket UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="690d8-175">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="690d8-176">Ajouter la prise en charge pour TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="690d8-176">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="690d8-177">Non bloquant de sockets en cours de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="690d8-177">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="690d8-178">Prendre en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="690d8-178">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="690d8-179">Corriger le problème sur le dossier racine [GH 3304] de vérification d’autorisation</span><span class="sxs-lookup"><span data-stu-id="690d8-179">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="690d8-180">Prise en charge limitée TTY clavier ioctls KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="690d8-180">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="690d8-181">Applications d’interface utilisateur Windows doivent s’exécuter même lorsque lancé en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="690d8-181">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="690d8-182">Ajouter l’option -u ou--utilisateur wsl [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="690d8-182">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="690d8-183">Résoudre les problèmes de lancement WSL de démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="690d8-183">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="690d8-184">Sockets UNIX doivent conserver les informations d’identification homologue déconnectée [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="690d8-184">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="690d8-185">Sockets Unix de non bloquants indéfiniment échoué à cause d’EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="690d8-185">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="690d8-186">cas = off est de type [2937 GH 3212, 3328] de montage des nouvelle drvfs par défaut</span><span class="sxs-lookup"><span data-stu-id="690d8-186">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="690d8-187">Consultez [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="690d8-187">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="690d8-188">Ajouter wslconfig / arrêter pour arrêter l’exécution des distributions.</span><span class="sxs-lookup"><span data-stu-id="690d8-188">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="690d8-189">Résoudre les problème avec le contexte du shell WSL les entrées de menu qui ne gèrent pas correctement les chemins d’accès avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="690d8-189">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="690d8-190">Exposer par répertoire respecte la casse comme un attribut étendu</span><span class="sxs-lookup"><span data-stu-id="690d8-190">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="690d8-191">ARM64 : Émuler des opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="690d8-191">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="690d8-192">Résoudre [dotnet problème](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="690d8-192">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="690d8-193">DrvFs : unescape uniquement des caractères dans la plage privées qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="690d8-193">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="690d8-194">Corriger désactivé par une erreur de validation de la longueur interpréteur ELF analyseur [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="690d8-194">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="690d8-195">Minuteurs d’absolu WSL avec une heure dans le passé ne déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="690d8-195">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="690d8-196">Vérifiez qui vient d’être des points d’analyse créés sont répertoriés en tant que tel dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="690d8-196">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="690d8-197">Créer atomiquement répertoires respecte la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="690d8-197">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="690d8-198">Correction d’un problème supplémentaire où les opérations multithread peut retourner ENOENT, même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="690d8-198">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="690d8-199">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="690d8-199">[GH 2712]</span></span>
* <span data-ttu-id="690d8-200">Fixe WSL lancer échec lorsque UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="690d8-200">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="690d8-201">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="690d8-201">[GH 3020]</span></span>
* <span data-ttu-id="690d8-202">Ajouter un menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="690d8-202">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="690d8-203">Pour utiliser, maintenez la touche MAJ et avec le bouton droit dans une fenêtre d’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="690d8-203">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="690d8-204">Corriger le comportement Unix socket non bloquant [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="690d8-204">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="690d8-205">Correctif négatif de commande NETLINK comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="690d8-205">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="690d8-206">Ajouter la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="690d8-206">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="690d8-207">Résoudre le problème avec les événements inotify entraînant pas tronquer [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="690d8-207">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="690d8-208">Ajoutez--option exec pour wsl.exe appeler un fichier binaire unique sans un interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="690d8-208">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="690d8-209">Ajoutez--option de distribution pour wsl.exe sélectionner une distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="690d8-209">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="690d8-210">Prise en charge limitée dmesg.</span><span class="sxs-lookup"><span data-stu-id="690d8-210">Limited support for dmesg.</span></span> <span data-ttu-id="690d8-211">Les applications peuvent maintenant vous connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="690d8-211">Applications can now log to dmesg.</span></span> <span data-ttu-id="690d8-212">Pilote WSL consigne des informations limitées dans dmesg.</span><span class="sxs-lookup"><span data-stu-id="690d8-212">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="690d8-213">À l’avenir, cela peut être étendu pour effectuer d’autres informations/diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="690d8-213">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="690d8-214">Remarque : dmesg actuellement pris en charge par le biais du `/dev/kmsg` interface de périphérique.</span><span class="sxs-lookup"><span data-stu-id="690d8-214">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="690d8-215">syscall interface n’est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="690d8-215">syscall interface is not yet supported.</span></span> <span data-ttu-id="690d8-216">Et, par conséquent, certaines de la `dmesg` options de ligne de commande telles que `-S`, `-C` ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="690d8-216">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="690d8-217">Modifier les gid par défaut et périphériques série pour faire correspondre natif [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="690d8-217">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="690d8-218">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="690d8-218">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="690d8-219">Remarque: DrvFs présente certaines limitations sur le nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="690d8-219">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="690d8-220">Certains caractères (comme '/', ' :' et '\*') ne sont pas autorisées et étendu les noms d’attributs ne sont pas sensible à la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="690d8-220">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="690d8-221">Build 18252 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="690d8-221">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="690d8-222">Pour Windows général plus d’informations sur la build 18252 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="690d8-222">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-223">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-223">WSL</span></span>
* <span data-ttu-id="690d8-224">Déplacer des binaires init et bsdtar en dehors de la dll de lxssmanager et dans un dossier des outils distincts</span><span class="sxs-lookup"><span data-stu-id="690d8-224">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="690d8-225">Corriger la concurrence autour de fermer le descripteur de fichier lors de l’utilisation de CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="690d8-225">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="690d8-226">Gérer les champs facultatifs dans /proc/pid/mountinfo lors de la traduction des chemins d’accès DrvFs</span><span class="sxs-lookup"><span data-stu-id="690d8-226">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="690d8-227">Autoriser mknod DrvFs de réussir sans prise en charge des métadonnées pour S_IFREG</span><span class="sxs-lookup"><span data-stu-id="690d8-227">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="690d8-228">Fichiers en lecture seule créés sur DrvFs doivent avoir l’attribut en lecture seule définie [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="690d8-228">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="690d8-229">Ajouter d’assistance /sbin/mount.drvfs pour gérer le montage DrvFs</span><span class="sxs-lookup"><span data-stu-id="690d8-229">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="690d8-230">Utilisez le changement de nom POSIX dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="690d8-230">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="690d8-231">Permet la traduction de chemin d’accès sur les volumes sans GUID du volume.</span><span class="sxs-lookup"><span data-stu-id="690d8-231">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="690d8-232">Build 17738 (rapide)</span><span class="sxs-lookup"><span data-stu-id="690d8-232">Build 17738 (Fast)</span></span>
<span data-ttu-id="690d8-233">Pour Windows général plus d’informations sur la build 17738 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="690d8-233">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-234">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-234">WSL</span></span>
* <span data-ttu-id="690d8-235">Vérification des autorisations SetPriority syscall trop stricte pour modifier la priorité de thread même [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="690d8-235">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="690d8-236">Garantir que les temps d’interruption non biaisée est utilisé pour le démarrage pour éviter le renvoi des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="690d8-236">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="690d8-237">Gérer les liens symboliques dans l’interpréteur de binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="690d8-237">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="690d8-238">Meilleure gestion de nettoyage de descripteur de fichier de leader threadgroup.</span><span class="sxs-lookup"><span data-stu-id="690d8-238">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="690d8-239">Build 17728 (rapide)</span><span class="sxs-lookup"><span data-stu-id="690d8-239">Build 17728 (Fast)</span></span>
<span data-ttu-id="690d8-240">Pour Windows général plus d’informations sur la build 17728 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="690d8-240">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-241">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-241">WSL</span></span>
* <span data-ttu-id="690d8-242">Commutateur WSL à utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter du afin d’éviter le dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="690d8-242">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="690d8-243">Ptrace attacher mai provoquer la mauvaise valeur de retour à partir des appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="690d8-243">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="690d8-244">Correctif que relatif d’un nombre de AF_UNIX émet [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="690d8-244">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="690d8-245">Correction d’un problème qui provoquait interop WSL échoue si le répertoire de travail actuel est inférieur à 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="690d8-245">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="690d8-246">Build 18204 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="690d8-246">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="690d8-247">Pour Windows général plus d’informations sur la build 18204 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="690d8-247">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-248">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-248">WSL</span></span>
* <span data-ttu-id="690d8-249">Diriger inadvertenly filesystem effacer événement epoll déclenchée par edge [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="690d8-249">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="690d8-250">Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="690d8-250">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="690d8-251">Build 17723 (rapide)</span><span class="sxs-lookup"><span data-stu-id="690d8-251">Build 17723 (Fast)</span></span>
<span data-ttu-id="690d8-252">Pour Windows général plus d’informations sur la build 17723 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="690d8-252">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-253">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-253">WSL</span></span>
* <span data-ttu-id="690d8-254">Éviter un délai deuxième échec des connexions de bouclage aux ports inexistant [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="690d8-254">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="690d8-255">Ajouter un fichier stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="690d8-255">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="690d8-256">Informations de portée IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="690d8-256">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="690d8-257">Prise en charge PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="690d8-257">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="690d8-258">Diriger inadvertenly filesystem effacer événement epoll déclenchée par edge [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="690d8-258">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="690d8-259">Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="690d8-259">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="690d8-260">Build 17713</span><span class="sxs-lookup"><span data-stu-id="690d8-260">Build 17713</span></span>
<span data-ttu-id="690d8-261">Pour Windows général plus d’informations sur la build 17713 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="690d8-261">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-262">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-262">WSL</span></span>
* <span data-ttu-id="690d8-263">Prise en charge de zombie [GH 1353] améliorée</span><span class="sxs-lookup"><span data-stu-id="690d8-263">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="690d8-264">Ajouter des entrées wsl.conf pour contrôler le comportement d’interopérabilité Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="690d8-264">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="690d8-265">Correctif pour getsockname pas toujours renvoyer le type de famille du socket UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="690d8-265">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="690d8-266">Ajouter la prise en charge pour TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="690d8-266">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="690d8-267">Non bloquant de sockets en cours de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="690d8-267">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="690d8-268">Prendre en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="690d8-268">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="690d8-269">Corriger le problème sur le dossier racine [GH 3304] de vérification d’autorisation</span><span class="sxs-lookup"><span data-stu-id="690d8-269">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="690d8-270">Prise en charge limitée TTY clavier ioctls KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="690d8-270">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="690d8-271">Applications d’interface utilisateur Windows doivent s’exécuter même lorsque lancé en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="690d8-271">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="690d8-272">Build 17704</span><span class="sxs-lookup"><span data-stu-id="690d8-272">Build 17704</span></span>
<span data-ttu-id="690d8-273">Pour Windows général plus d’informations sur la build 17704 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="690d8-273">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-274">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-274">WSL</span></span>
* <span data-ttu-id="690d8-275">Ajouter l’option -u ou--utilisateur wsl [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="690d8-275">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="690d8-276">Résoudre les problèmes de lancement WSL de démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="690d8-276">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="690d8-277">Sockets UNIX doivent conserver les informations d’identification homologue déconnectée [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="690d8-277">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="690d8-278">Sockets Unix de non bloquants indéfiniment échoué à cause d’EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="690d8-278">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="690d8-279">cas = off est de type [2937 GH 3212, 3328] de montage des nouvelle drvfs par défaut</span><span class="sxs-lookup"><span data-stu-id="690d8-279">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="690d8-280">Consultez [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="690d8-280">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="690d8-281">Ajouter wslconfig / arrêter pour arrêter l’exécution des distributions.</span><span class="sxs-lookup"><span data-stu-id="690d8-281">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="690d8-282">Build 17692</span><span class="sxs-lookup"><span data-stu-id="690d8-282">Build 17692</span></span>
<span data-ttu-id="690d8-283">Pour Windows général plus d’informations sur la build 17692 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="690d8-283">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-284">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-284">WSL</span></span>
* <span data-ttu-id="690d8-285">Résoudre les problème avec le contexte du shell WSL les entrées de menu qui ne gèrent pas correctement les chemins d’accès avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="690d8-285">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="690d8-286">Exposer par répertoire respecte la casse comme un attribut étendu</span><span class="sxs-lookup"><span data-stu-id="690d8-286">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="690d8-287">ARM64 : Émuler des opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="690d8-287">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="690d8-288">Résoudre [dotnet problème](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="690d8-288">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="690d8-289">DrvFs : unescape uniquement des caractères dans la plage privées qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="690d8-289">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="690d8-290">Build 17686</span><span class="sxs-lookup"><span data-stu-id="690d8-290">Build 17686</span></span>
<span data-ttu-id="690d8-291">Pour Windows général plus d’informations sur la build 17686 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="690d8-291">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-292">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-292">WSL</span></span>
* <span data-ttu-id="690d8-293">Corriger désactivé par une erreur de validation de la longueur interpréteur ELF analyseur [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="690d8-293">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="690d8-294">Minuteurs d’absolu WSL avec une heure dans le passé ne déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="690d8-294">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="690d8-295">Vérifiez qui vient d’être des points d’analyse créés sont répertoriés en tant que tel dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="690d8-295">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="690d8-296">Créer atomiquement répertoires respecte la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="690d8-296">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="690d8-297">Build 17677</span><span class="sxs-lookup"><span data-stu-id="690d8-297">Build 17677</span></span>
<span data-ttu-id="690d8-298">Pour Windows général plus d’informations sur la build 17677 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="690d8-298">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-299">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-299">WSL</span></span>
* <span data-ttu-id="690d8-300">Correction d’un problème supplémentaire où les opérations multithread peut retourner ENOENT, même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="690d8-300">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="690d8-301">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="690d8-301">[GH 2712]</span></span>
* <span data-ttu-id="690d8-302">Fixe WSL lancer échec lorsque UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="690d8-302">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="690d8-303">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="690d8-303">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="690d8-304">Build 17666</span><span class="sxs-lookup"><span data-stu-id="690d8-304">Build 17666</span></span>
<span data-ttu-id="690d8-305">Pour Windows général plus d’informations sur la build 17666 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="690d8-305">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-306">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-306">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="690d8-307">AVERTISSEMENT : Il existe un problème WSL empêche de s’exécuter sur certains chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="690d8-307">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="690d8-308">Un correctif est prêt et qu’il apporte sa méthode pour la branche de Build Insider.</span><span class="sxs-lookup"><span data-stu-id="690d8-308">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="690d8-309">Ajouter un menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="690d8-309">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="690d8-310">Pour utiliser MAJ de blocage et avec le bouton droit dans une fenêtre d’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="690d8-310">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="690d8-311">Corriger le comportement unix socket non bloquant [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="690d8-311">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="690d8-312">Correctif négatif de commande NETLINK comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="690d8-312">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="690d8-313">Ajouter la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="690d8-313">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="690d8-314">Résoudre le problème avec les événements inotify entraînant pas tronquer [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="690d8-314">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="690d8-315">Ajoutez--option exec pour wsl.exe appeler un fichier binaire unique sans un interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="690d8-315">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="690d8-316">Ajoutez--option de distribution pour wsl.exe sélectionner une distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="690d8-316">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="690d8-317">Build 17655 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="690d8-317">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="690d8-318">Pour Windows général plus d’informations sur la build 17655 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="690d8-318">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-319">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-319">WSL</span></span>
* <span data-ttu-id="690d8-320">Prise en charge limitée dmesg.</span><span class="sxs-lookup"><span data-stu-id="690d8-320">Limited support for dmesg.</span></span> <span data-ttu-id="690d8-321">Les applications peuvent maintenant vous connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="690d8-321">Applications can now log to dmesg.</span></span> <span data-ttu-id="690d8-322">Pilote WSL consigne des informations limitées dans dmesg.</span><span class="sxs-lookup"><span data-stu-id="690d8-322">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="690d8-323">À l’avenir, cela peut être étendu pour effectuer d’autres informations/diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="690d8-323">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="690d8-324">Remarque : dmesg actuellement pris en charge par le biais du `/dev/kmsg` interface de périphérique.</span><span class="sxs-lookup"><span data-stu-id="690d8-324">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> `syslog` <span data-ttu-id="690d8-325">interface de sycall n’est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="690d8-325">sycall interface is not yet supported.</span></span> <span data-ttu-id="690d8-326">Et, par conséquent, certaines de la `dmesg` options de ligne de commande telles que `-S`, `-C` ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="690d8-326">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="690d8-327">Correction d’un problème où les opérations multithread peut retourner ENOENT, même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="690d8-327">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="690d8-328">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="690d8-328">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="690d8-329">Build 17639 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="690d8-329">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="690d8-330">Pour Windows général plus d’informations sur la build 17639 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="690d8-330">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-331">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-331">WSL</span></span>
* <span data-ttu-id="690d8-332">Modifier les gid par défaut et périphériques série pour faire correspondre natif [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="690d8-332">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="690d8-333">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="690d8-333">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="690d8-334">Remarque: DrvFs présente certaines limitations sur le nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="690d8-334">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="690d8-335">En particulier, certains caractères (comme '/', ' :' et '\*') ne sont pas autorisées et étendu les noms d’attributs ne sont pas sensible à la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="690d8-335">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="690d8-336">Build 17133 (rapide)</span><span class="sxs-lookup"><span data-stu-id="690d8-336">Build 17133 (Fast)</span></span>
<span data-ttu-id="690d8-337">Pour Windows général plus d’informations sur la build 17133 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="690d8-337">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-338">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-338">WSL</span></span>
* <span data-ttu-id="690d8-339">Correction d’un blocage dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-339">Fix for hang in WSL.</span></span> <span data-ttu-id="690d8-340">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="690d8-340">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="690d8-341">Build 17128 (rapide)</span><span class="sxs-lookup"><span data-stu-id="690d8-341">Build 17128 (Fast)</span></span>
<span data-ttu-id="690d8-342">Pour Windows général plus d’informations sur la build 17128 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="690d8-342">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-343">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-343">WSL</span></span>
* <span data-ttu-id="690d8-344">Aucune</span><span class="sxs-lookup"><span data-stu-id="690d8-344">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="690d8-345">Build 17627 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="690d8-345">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="690d8-346">Pour Windows général plus d’informations sur la build 17627 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="690d8-346">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-347">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-347">WSL</span></span>
* <span data-ttu-id="690d8-348">Ajouter la prise en charge pour les opérations prenant en charge les pi futex.</span><span class="sxs-lookup"><span data-stu-id="690d8-348">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="690d8-349">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="690d8-349">[GH 1006]</span></span>
    * <span data-ttu-id="690d8-350">Notez que les priorités ne sont pas actuellement une fonctionnalité WSL pris en charge par conséquent, il existe des limitations, mais l’utilisation standard doit être débloquée.</span><span class="sxs-lookup"><span data-stu-id="690d8-350">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="690d8-351">Prise en charge des pare-feu Windows pour les processus WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-351">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="690d8-352">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="690d8-352">[GH 1852]</span></span>
    * <span data-ttu-id="690d8-353">Par exemple, pour autoriser la WSL python traite pour écouter sur n’importe quel port, utilisez la commande Windows élevée :</span><span class="sxs-lookup"><span data-stu-id="690d8-353">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd:</span></span>
```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * <span data-ttu-id="690d8-354">Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="690d8-354">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="690d8-355">Respecter le shell par défaut de l’utilisateur lors de l’utilisation de wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="690d8-355">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="690d8-356">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="690d8-356">[GH 2372]</span></span>
* <span data-ttu-id="690d8-357">Déclarer toutes les interfaces réseau ethernet.</span><span class="sxs-lookup"><span data-stu-id="690d8-357">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="690d8-358">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="690d8-358">[GH 2996]</span></span>
* <span data-ttu-id="690d8-359">Meilleure gestion du fichier de passwd endommagé.</span><span class="sxs-lookup"><span data-stu-id="690d8-359">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="690d8-360">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="690d8-360">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="690d8-361">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-361">Console</span></span>
* <span data-ttu-id="690d8-362">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-362">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-363">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-363">LTP Results:</span></span>
<span data-ttu-id="690d8-364">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-364">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="690d8-365">Build 17618 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="690d8-365">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="690d8-366">Pour Windows général plus d’informations sur la build 17618 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="690d8-366">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-367">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-367">WSL</span></span>
* <span data-ttu-id="690d8-368">Introduire une fonctionnalité pseudoconsole pour l’interopérabilité de NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="690d8-368">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="690d8-369">Le mécanisme d’installation héritée (lxrun.exe) a été déconseillé.</span><span class="sxs-lookup"><span data-stu-id="690d8-369">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="690d8-370">Le mécanisme pris en charge pour l’installation de distributions est via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="690d8-370">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="690d8-371">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-371">Console</span></span>
* <span data-ttu-id="690d8-372">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-372">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-373">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-373">LTP Results:</span></span>
<span data-ttu-id="690d8-374">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-374">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="690d8-375">Build 17110</span><span class="sxs-lookup"><span data-stu-id="690d8-375">Build 17110</span></span>
<span data-ttu-id="690d8-376">Pour Windows général plus d’informations sur la build 17110 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="690d8-376">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-377">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-377">WSL</span></span>
* <span data-ttu-id="690d8-378">Autoriser /init à être arrêté à partir de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="690d8-378">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="690d8-379">DrvFs utilise désormais par répertoire respecte la casse par défaut (équivalent à la « cas = dir « option de montage).</span><span class="sxs-lookup"><span data-stu-id="690d8-379">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="690d8-380">À l’aide de « cas = force » (l’ancien comportement) requiert la définition d’une clé de Registre.</span><span class="sxs-lookup"><span data-stu-id="690d8-380">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="690d8-381">Exécutez la commande suivante pour activer « cas = force » si vous avez besoin pour l’utiliser : reg ajouter HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="690d8-381">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="690d8-382">Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui doivent respecter la casse, utiliser fsutil.exe pour les marquer comme respectant la casse : fsutil.exe fichier setcasesensitiveinfo <path> activer</span><span class="sxs-lookup"><span data-stu-id="690d8-382">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="690d8-383">Les chaînes retournées par la syscall uname finissant par NULL.</span><span class="sxs-lookup"><span data-stu-id="690d8-383">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="690d8-384">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-384">Console</span></span>
* <span data-ttu-id="690d8-385">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-385">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-386">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-386">LTP Results:</span></span>
<span data-ttu-id="690d8-387">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-387">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="690d8-388">Build 17107</span><span class="sxs-lookup"><span data-stu-id="690d8-388">Build 17107</span></span>
<span data-ttu-id="690d8-389">Pour Windows général plus d’informations sur la build 17107 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="690d8-389">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-390">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-390">WSL</span></span>
* <span data-ttu-id="690d8-391">Prend en charge TCSETSF et TCSETSW sur les points de terminaison maître pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="690d8-391">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="690d8-392">Démarrage des processus interop simultanées peut entraîner EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="690d8-392">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="690d8-393">Corriger PTRACE_ATTACH pour afficher l’état de suivi approprié dans /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="690d8-393">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="690d8-394">Concurrence de correctif où le processus de courte durée clonés avec indicateurs CLEARTID et de SETTID pu quitter sans effacer l’adresse TID.</span><span class="sxs-lookup"><span data-stu-id="690d8-394">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="690d8-395">Afficher un message lors de la mise à niveau les répertoires de système de fichiers Linux lors du déplacement d’une build de pre-17093.</span><span class="sxs-lookup"><span data-stu-id="690d8-395">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="690d8-396">Pour plus d’informations sur les modifications de système de 17093 fichiers, consultez les notes de publication pour [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="690d8-396">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="690d8-397">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-397">Console</span></span>
* <span data-ttu-id="690d8-398">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-398">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-399">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-399">LTP Results:</span></span>
<span data-ttu-id="690d8-400">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-400">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="690d8-401">Build 17101</span><span class="sxs-lookup"><span data-stu-id="690d8-401">Build 17101</span></span>
<span data-ttu-id="690d8-402">Pour Windows général plus d’informations sur la build 17101 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="690d8-402">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-403">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-403">WSL</span></span>
* <span data-ttu-id="690d8-404">Prise en charge signalfd.</span><span class="sxs-lookup"><span data-stu-id="690d8-404">Support for signalfd.</span></span> <span data-ttu-id="690d8-405">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="690d8-405">[GH 129]</span></span>
* <span data-ttu-id="690d8-406">Prend en charge les noms de fichier contenant des caractères NTFS non valides en les codant en tant que caractères Unicode privés.</span><span class="sxs-lookup"><span data-stu-id="690d8-406">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="690d8-407">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="690d8-407">[GH 1514]</span></span>
* <span data-ttu-id="690d8-408">Montage automatique utilisera en lecture seule lors de l’écriture n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="690d8-408">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="690d8-409">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="690d8-409">[GH 2603]</span></span>
* <span data-ttu-id="690d8-410">Autoriser le collage des paires de substitution Unicode (comme les caractères emoji).</span><span class="sxs-lookup"><span data-stu-id="690d8-410">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="690d8-411">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="690d8-411">[GH 2765]</span></span>
* <span data-ttu-id="690d8-412">Fichiers pseudo-élément dans /proc et /sys doivent retourner la lecture et écrire des prêts à partir de select, interrogation, epoll, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="690d8-412">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="690d8-413">Corrigez le problème qui pouvait entraîner service passe en boucle infinie lorsque le Registre a été falsifié ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="690d8-413">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="690d8-414">Résoudre les messages netlink pour travailler avec la nouvelle version (en amont 4.14) d’iproute2.</span><span class="sxs-lookup"><span data-stu-id="690d8-414">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="690d8-415">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-415">Console</span></span>
* <span data-ttu-id="690d8-416">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-416">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-417">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-417">LTP Results:</span></span>
<span data-ttu-id="690d8-418">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-418">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="690d8-419">Build 17093</span><span class="sxs-lookup"><span data-stu-id="690d8-419">Build 17093</span></span>
<span data-ttu-id="690d8-420">Pour Windows général plus d’informations sur la build 17093 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-420">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="690d8-421">Important :</span><span class="sxs-lookup"><span data-stu-id="690d8-421">Important:</span></span>
<span data-ttu-id="690d8-422">Lorsque vous démarrez WSL pour la première fois après la mise à niveau vers cette version, il doit effectuer un travail de la mise à niveau les répertoires de système de fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-422">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="690d8-423">Cela peut prendre jusqu'à plusieurs minutes, donc WSL peut sembler démarrer lentement.</span><span class="sxs-lookup"><span data-stu-id="690d8-423">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="690d8-424">Cela ne doit se produire une fois pour chaque distribution que vous avez installé à partir du magasin.</span><span class="sxs-lookup"><span data-stu-id="690d8-424">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="690d8-425">Meilleure prise en charge de la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="690d8-425">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="690d8-426">DrvFs prend désormais en charge par répertoire respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-426">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="690d8-427">Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme respectant la casse, ce qui permet de même des applications Windows ouvrir correctement les fichiers qui diffèrent uniquement par la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-427">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="690d8-428">DrvFs a de nouvelles options de montage contrôle respecte la casse sur une base par répertoire</span><span class="sxs-lookup"><span data-stu-id="690d8-428">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="690d8-429">cas = force : tous les répertoires sont traités comme respectant la casse (à l’exception de la racine du lecteur).</span><span class="sxs-lookup"><span data-stu-id="690d8-429">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="690d8-430">Nouveaux répertoires créés avec WSL sont marqués comme respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-430">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="690d8-431">Il s’agit de l’ancien comportement à l’exception de marquage de nouveaux répertoires respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-431">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="690d8-432">cas = dir : seuls les répertoires avec l’indicateur par répertoire respecte la casse sont traités comme respectant la casse ; autres répertoires respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-432">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="690d8-433">Nouveaux répertoires créés avec WSL sont marqués comme respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-433">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="690d8-434">cas = off : seuls les répertoires avec l’indicateur par répertoire respecte la casse sont traités comme respectant la casse ; autres répertoires respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-434">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="690d8-435">Nouveaux répertoires créés avec WSL portent la mention de la casse.</span><span class="sxs-lookup"><span data-stu-id="690d8-435">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="690d8-436">Remarque : répertoires créés par WSL dans les versions précédentes n’ont pas cet indicateur défini, afin de ne pas être traités comme respectant la casse si vous utilisez le « cas = dir « option.</span><span class="sxs-lookup"><span data-stu-id="690d8-436">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="690d8-437">Une façon de définir cet indicateur dans les répertoires existants sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="690d8-437">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="690d8-438">Exemple de montage avec ces options (pour les lecteurs existants, vous devez tout d’abord la démonter avant que vous pouvez monter avec des options différentes) : sudo mount -t drvfs C:/mnt/c -o cas = dir</span><span class="sxs-lookup"><span data-stu-id="690d8-438">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="690d8-439">Pour l’instant, cas = force est toujours l’option par défaut.</span><span class="sxs-lookup"><span data-stu-id="690d8-439">For now, case=force is still the default option.</span></span> <span data-ttu-id="690d8-440">Ce sera remplacé au cas = dir dans le futur.</span><span class="sxs-lookup"><span data-stu-id="690d8-440">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="690d8-441">Vous pouvez maintenant utiliser des barres obliques dans les chemins d’accès de Windows lors du montage DrvFs, par exemple : sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="690d8-441">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="690d8-442">WSL traite désormais le fichier/etc/fstab pendant le démarrage de l’instance [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="690d8-442">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="690d8-443">Cette opération est effectuée avant de monter automatiquement les lecteurs de DrvFs ; tous les lecteurs qui ont été déjà montés par fstab ne seront pas être remontées automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="690d8-443">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="690d8-444">Ce comportement peut être désactivé à l’aide de wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="690d8-444">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="690d8-445">Les fichiers de montage, mountinfo et mountstats dans /proc échappement correctement les caractères spéciaux tels que des barres obliques inverses et les espaces [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="690d8-445">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="690d8-446">Fichiers spéciaux créés avec DrvFs tels que des liens symboliques WSL, ou file d’attente FIFO et les sockets lorsque les métadonnées sont activées, peuvent désormais être copiés et déplacés à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-446">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="690d8-447">WSL est plus configurable avec wsl.conf</span><span class="sxs-lookup"><span data-stu-id="690d8-447">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="690d8-448">Nous avons ajouté une méthode vous permettant de configurer automatiquement certaines fonctionnalités dans WSL qui est appliqué chaque fois que vous lancez le sous-système.</span><span class="sxs-lookup"><span data-stu-id="690d8-448">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="690d8-449">Cela inclut les options de montage automatique et de configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="690d8-449">This includes automount options and network configuration.</span></span> <span data-ttu-id="690d8-450">Pour en savoir plus à ce sujet à notre billet de blog : https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="690d8-450">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="690d8-451">AF_UNIX autorise les connexions de socket entre les processus de Linux sur WSL et les processus natifs de Windows</span><span class="sxs-lookup"><span data-stu-id="690d8-451">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="690d8-452">Applications WSL et Windows peuvent désormais communiquer avec eux via des sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="690d8-452">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="690d8-453">Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible aux applications Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-453">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="690d8-454">Maintenant, c’est possible avec les sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="690d8-454">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="690d8-455">Lecture de plus, consultez notre blog publiez au https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="690d8-455">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-456">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-456">WSL</span></span>
* <span data-ttu-id="690d8-457">Mmap() prise en charge avec MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="690d8-457">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="690d8-458">Prendre en charge CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="690d8-458">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="690d8-459">Gérer le signal d’arrêt non SIGCHLD clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="690d8-459">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="690d8-460">Stub /proc/sys/fs/inotify/max_user_instances et /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="690d8-460">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="690d8-461">Erreur lors du chargement des fichiers binaires ELF qui contiennent des en-têtes de charge avec zéro décalages [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="690d8-461">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="690d8-462">Zéro octets de la page de fin lors du chargement d’images.</span><span class="sxs-lookup"><span data-stu-id="690d8-462">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="690d8-463">Réduire les cas où execve en mode silencieux pour achever</span><span class="sxs-lookup"><span data-stu-id="690d8-463">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="690d8-464">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-464">Console</span></span>
* <span data-ttu-id="690d8-465">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-465">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-466">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-466">LTP Results:</span></span>
<span data-ttu-id="690d8-467">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-467">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="690d8-468">Build 17083</span><span class="sxs-lookup"><span data-stu-id="690d8-468">Build 17083</span></span>
<span data-ttu-id="690d8-469">Pour Windows général plus d’informations sur la build 17083 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-469">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-470">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-470">WSL</span></span>
* <span data-ttu-id="690d8-471">Vérification d’erreur fixe liée à epoll [2798 GH 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="690d8-471">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="690d8-472">Fixe se bloque lors de la désactivation de l’ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="690d8-472">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="690d8-473">Vérifiez les opérations mmap apparaissent atomique [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="690d8-473">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="690d8-474">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-474">Console</span></span>
* <span data-ttu-id="690d8-475">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-475">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-476">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-476">LTP Results:</span></span>
<span data-ttu-id="690d8-477">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-477">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="690d8-478">Build 17074</span><span class="sxs-lookup"><span data-stu-id="690d8-478">Build 17074</span></span>
<span data-ttu-id="690d8-479">Pour Windows général plus d’informations sur la build 17074 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-479">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-480">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-480">WSL</span></span>
* <span data-ttu-id="690d8-481">Format de stockage fixe de métadonnées DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="690d8-481">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="690d8-482">**Important :** Métadonnées DrvFs créées avant cette build s’afficheront mal ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="690d8-482">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="690d8-483">Pour résoudre les fichiers affectés, utilisez chmod et chown à réappliquer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="690d8-483">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="690d8-484">Correction d’un problème avec plusieurs signaux et syscalls redémarrable.</span><span class="sxs-lookup"><span data-stu-id="690d8-484">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="690d8-485">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-485">Console</span></span>
* <span data-ttu-id="690d8-486">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-487">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-487">LTP Results:</span></span>
<span data-ttu-id="690d8-488">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-488">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="690d8-489">Build 17063</span><span class="sxs-lookup"><span data-stu-id="690d8-489">Build 17063</span></span>
<span data-ttu-id="690d8-490">Pour Windows général plus d’informations sur la build 17063 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-490">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="690d8-491">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-491">WSL</span></span>
* <span data-ttu-id="690d8-492">DrvFs prend en charge des métadonnées supplémentaires de Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-492">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="690d8-493">Cela permet de définir le propriétaire et le mode de fichiers à l’aide de chmod/chown, ainsi que la création de fichiers spéciaux tels que la file d’attente FIFO, les sockets unix et les fichiers de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="690d8-493">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="690d8-494">Cela est désactivée par défaut pour l’instant, car il est encore au stade expérimental.</span><span class="sxs-lookup"><span data-stu-id="690d8-494">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="690d8-495">**Remarque :**  Nous avons résolu un bogue dans le format de métadonnées utilisé par DrvFs.</span><span class="sxs-lookup"><span data-stu-id="690d8-495">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="690d8-496">Bien que métadonnées fonctionnement sur cette génération pour l’expérimentation, builds futures correctement ne lira pas les métadonnées créées par cette build.</span><span class="sxs-lookup"><span data-stu-id="690d8-496">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="690d8-497">Vous devrez peut-être mettre à jour manuellement le propriétaire pour les fichiers modifiés et appareils avec un ID d’appareil personnalisé devront être recréés.</span><span class="sxs-lookup"><span data-stu-id="690d8-497">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="690d8-498">Pour activer, DrvFs de montage avec l’option de métadonnées (pour l’activer sur un montage existant, vous devez tout d’abord la démonter) :</span><span class="sxs-lookup"><span data-stu-id="690d8-498">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="690d8-499">Autorisations de Linux sont ajoutées en tant que métadonnées supplémentaires au fichier ; elles n’affectent pas les autorisations de Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-499">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="690d8-500">N’oubliez pas de modification d’un fichier à l’aide d’un éditeur Windows peut supprimer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="690d8-500">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="690d8-501">Dans ce cas, le fichier reprendront ses autorisations par défaut.</span><span class="sxs-lookup"><span data-stu-id="690d8-501">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="690d8-502">Options de montage ajouté à DrvFs pour contrôler les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="690d8-502">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="690d8-503">UID : l’ID d’utilisateur utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="690d8-503">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="690d8-504">GID : l’ID de groupe utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="690d8-504">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="690d8-505">umask : un masque octal des autorisations à exclure pour tous les fichiers et répertoires.</span><span class="sxs-lookup"><span data-stu-id="690d8-505">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="690d8-506">cas : un masque octal des autorisations à exclure pour tous les fichiers régulières.</span><span class="sxs-lookup"><span data-stu-id="690d8-506">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="690d8-507">dmask : un masque octal des autorisations à exclure tous les répertoires.</span><span class="sxs-lookup"><span data-stu-id="690d8-507">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="690d8-508">Exemple :</span><span class="sxs-lookup"><span data-stu-id="690d8-508">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="690d8-509">Combiner avec l’option de métadonnées pour spécifier les autorisations par défaut pour les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="690d8-509">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="690d8-510">A introduit une nouvelle variable d’environnement, `WSLENV`, pour configurer le flux des variables d’environnement entre WSL et Win32.</span><span class="sxs-lookup"><span data-stu-id="690d8-510">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="690d8-511">Exemple :</span><span class="sxs-lookup"><span data-stu-id="690d8-511">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` <span data-ttu-id="690d8-512">est une liste délimitée par des deux-points de variables d’environnement qui peut être inclus lors du lancement du processus WSL à partir de Win32 ou Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-512">is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="690d8-513">Chaque variable peut être suivi du suffixe par une barre oblique suivie d’indicateurs pour spécifier la façon dont elle est convertie.</span><span class="sxs-lookup"><span data-stu-id="690d8-513">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="690d8-514">p : La valeur est un chemin d’accès qui doit être convertis entre les chemins de Win32 et WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-514">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="690d8-515">L : La valeur est une liste de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="690d8-515">l: The value is a list of paths.</span></span> <span data-ttu-id="690d8-516">Dans WSL, il est une liste délimitée par des deux-points.</span><span class="sxs-lookup"><span data-stu-id="690d8-516">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="690d8-517">Dans Win32, il est une liste délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="690d8-517">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="690d8-518">%U : La valeur doit être incluse uniquement lors de l’appel WSL à partir de Win32</span><span class="sxs-lookup"><span data-stu-id="690d8-518">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="690d8-519">w : La valeur doit être incluse uniquement lors de l’appel Win32 à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-519">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="690d8-520">Vous pouvez définir `WSLENV` dans .bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="690d8-520">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="690d8-521">drvfs montages conserve correctement les horodatages de tar, cp -p (1939 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-521">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="690d8-522">liens symboliques drvfs indiquent la taille correcte (2641 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-522">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="690d8-523">en lecture/écriture fonctionne pour les très grandes tailles d’e/s (2653 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-523">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="690d8-524">waitpid fonctionne avec le groupe de processus ID (2534 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-524">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="690d8-525">mmap amélioration significative des performances pour les régions de la réserve de grande taille ; améliore les performances de ghc (1671 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-525">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="690d8-526">prise en charge de la personnalité de READ_IMPLIES_EXEC ; résout les maxima et clisp (1185 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-526">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="690d8-527">mprotect prend en charge PROT_GROWSDOWN ; correctifs clisp (1128 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-527">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="690d8-528">page d’erreur correctifs dans sollicitation excessive du mode ; correctifs sbcl (1128 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-528">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="690d8-529">Clone prend en charge plusieurs combinaisons d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="690d8-529">clone supports more flags combinations</span></span>
* <span data-ttu-id="690d8-530">Prend en charge select/epoll des fichiers epoll (précédemment une absence d’opération).</span><span class="sxs-lookup"><span data-stu-id="690d8-530">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="690d8-531">Notifier ptrace de syscalls non implémentée.</span><span class="sxs-lookup"><span data-stu-id="690d8-531">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="690d8-532">Ignorer les interfaces qui ne sont pas des lors de la génération des serveurs de noms resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="690d8-532">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="690d8-533">Énumérer les interfaces réseau avec aucune adresse physique.</span><span class="sxs-lookup"><span data-stu-id="690d8-533">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="690d8-534">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="690d8-534">[GH 2685]</span></span>
* <span data-ttu-id="690d8-535">Améliorations et correctifs de bogues supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="690d8-535">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="690d8-536">Outils de Linux qui permettent aux développeurs sur Windows</span><span class="sxs-lookup"><span data-stu-id="690d8-536">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="690d8-537">Ligne de commande de Windows chaîne d’outils inclut bsdtar (tar) et curl.</span><span class="sxs-lookup"><span data-stu-id="690d8-537">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="690d8-538">Lecture [ce billet de blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et de voir comment ils vous mettre en forme l’expérience de développement sur Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-538">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   `AF_UNIX` <span data-ttu-id="690d8-539">est disponible dans le Kit de développement Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="690d8-539">is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="690d8-540">Lecture [ce billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus sur `AF_UNIX` et comment les développeurs sur Windows peuvent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="690d8-540">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="690d8-541">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-541">Console</span></span>
* <span data-ttu-id="690d8-542">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-542">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-543">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-543">LTP Results:</span></span>
<span data-ttu-id="690d8-544">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-544">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="690d8-545">Build 17046</span><span class="sxs-lookup"><span data-stu-id="690d8-545">Build 17046</span></span>

<span data-ttu-id="690d8-546">Pour Windows général plus d’informations sur la build 17046 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="690d8-546">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="690d8-547">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-547">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-548">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-548">WSL</span></span>
- <span data-ttu-id="690d8-549">Autoriser le processus à s’exécuter sans un Terminal Server actives.</span><span class="sxs-lookup"><span data-stu-id="690d8-549">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="690d8-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="690d8-550">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="690d8-551">Mieux prendre en charge de CLONE_VFORK et CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="690d8-551">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="690d8-552">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="690d8-552">[GH 1878, 2615]</span></span>
- <span data-ttu-id="690d8-553">Ignorer les pilotes de filtre TDI pour WSL opérations de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="690d8-553">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="690d8-554">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="690d8-554">[GH 1554]</span></span>
- <span data-ttu-id="690d8-555">DrvFs crée des liens symboliques NT lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="690d8-555">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="690d8-556">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="690d8-556">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="690d8-557">La cible du lien doit être relative, ne doit pas traverser les points de montage ou les liens symboliques et doit exister.</span><span class="sxs-lookup"><span data-stu-id="690d8-557">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="690d8-558">L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela requiert généralement que vous lancez wsl.exe avec élévation de privilèges), sauf si le Mode développeur est activé.</span><span class="sxs-lookup"><span data-stu-id="690d8-558">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="690d8-559">Dans toutes les autres situations, DrvFs crée toujours des liens symboliques WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-559">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="690d8-560">Autoriser en cours d’exécution avec élévation de privilèges et non élevés instances WSL simultanément.</span><span class="sxs-lookup"><span data-stu-id="690d8-560">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="690d8-561">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="690d8-561">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="690d8-562">Ajouter wslpath pour faire WSL <> – conversions de chemin d’accès de Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-562">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="690d8-563">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="690d8-563">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="690d8-564">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-564">Console</span></span>
- <span data-ttu-id="690d8-565">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="690d8-565">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-566">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-566">LTP Results:</span></span>
<span data-ttu-id="690d8-567">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-567">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="690d8-568">Build 17040</span><span class="sxs-lookup"><span data-stu-id="690d8-568">Build 17040</span></span>

<span data-ttu-id="690d8-569">Pour Windows général plus d’informations sur la build 17040 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="690d8-569">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-570">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-570">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-571">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-571">WSL</span></span>
- <span data-ttu-id="690d8-572">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="690d8-572">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-573">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-573">Console</span></span>
- <span data-ttu-id="690d8-574">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="690d8-574">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-575">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-575">LTP Results:</span></span>
<span data-ttu-id="690d8-576">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-576">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="690d8-577">Build 17035</span><span class="sxs-lookup"><span data-stu-id="690d8-577">Build 17035</span></span>

<span data-ttu-id="690d8-578">Pour Windows général plus d’informations sur la build 17035 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="690d8-578">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-579">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-579">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-580">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-580">WSL</span></span>
- <span data-ttu-id="690d8-581">Accéder aux fichiers sur DrvFs peut parfois échouer avec EINVAL.</span><span class="sxs-lookup"><span data-stu-id="690d8-581">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="690d8-582">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="690d8-582">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-583">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-583">Console</span></span>
- <span data-ttu-id="690d8-584">Une perte de couleur lors de l’insertion/suppression de lignes en mode de VT.</span><span class="sxs-lookup"><span data-stu-id="690d8-584">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-585">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-585">LTP Results:</span></span>
<span data-ttu-id="690d8-586">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-586">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="690d8-587">Version 17025</span><span class="sxs-lookup"><span data-stu-id="690d8-587">Build 17025</span></span>

<span data-ttu-id="690d8-588">Pour Windows général plus d’informations sur la build 17025 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="690d8-588">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-589">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-589">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-590">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-590">WSL</span></span>
- <span data-ttu-id="690d8-591">Démarrer le processus initiales dans un nouveau groupe de processus de premier plan [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="690d8-591">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="690d8-592">Remise SIGHUP résout [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="690d8-592">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="690d8-593">Générer un nom de pont virtuel par défaut si aucun ne fourni [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="690d8-593">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="690d8-594">Implémenter /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="690d8-594">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="690d8-595">Résout les plus interop canal stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="690d8-595">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="690d8-596">Appel de système de syncfs de stub.</span><span class="sxs-lookup"><span data-stu-id="690d8-596">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-597">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-597">Console</span></span>
- <span data-ttu-id="690d8-598">Corriger la traduction de VT d’entrée pour les consoles tiers [GH 111]</span><span class="sxs-lookup"><span data-stu-id="690d8-598">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-599">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-599">LTP Results:</span></span>
<span data-ttu-id="690d8-600">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-600">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="690d8-601">Build 17017</span><span class="sxs-lookup"><span data-stu-id="690d8-601">Build 17017</span></span>

<span data-ttu-id="690d8-602">Pour Windows général plus d’informations sur la build 17017 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="690d8-602">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-603">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-603">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-604">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-604">WSL</span></span>
- <span data-ttu-id="690d8-605">Ignorer les en-têtes de programme vides ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="690d8-605">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="690d8-606">Autoriser LxssManager créer des instances WSL pour les utilisateurs non interactifs (ssh et planifiée prise en charge de la tâche) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="690d8-606">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="690d8-607">Prise en charge WSL -> Win32 -> [GH 1228] les scénarios WSL (« début »).</span><span class="sxs-lookup"><span data-stu-id="690d8-607">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="690d8-608">Prise en charge limitée pour l’arrêt des applications de console appelé via interop [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="690d8-608">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="690d8-609">Prise en charge les options de montage pour devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="690d8-609">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="690d8-610">Ptrace blocage démarrage enfant [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="690d8-610">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="690d8-611">EPOLLET certains événements [GH 2462] manquants.</span><span class="sxs-lookup"><span data-stu-id="690d8-611">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="690d8-612">Retourner plus de données pour PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="690d8-612">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="690d8-613">Getdents avec lseek donne des résultats incorrects.</span><span class="sxs-lookup"><span data-stu-id="690d8-613">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="690d8-614">Corriger certains blocages d’application d’interopérabilité Win32, en attente d’entrée sur un canal qui n’a plus aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="690d8-614">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="690d8-615">O_ASYNC prend en charge pour les fichiers de tty/pty.</span><span class="sxs-lookup"><span data-stu-id="690d8-615">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="690d8-616">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-616">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-617">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-617">Console</span></span>
- <span data-ttu-id="690d8-618">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-618">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-619">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-619">LTP Results:</span></span>
<span data-ttu-id="690d8-620">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="690d8-620">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="690d8-621">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="690d8-621">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="690d8-622">Build 16288</span><span class="sxs-lookup"><span data-stu-id="690d8-622">Build 16288</span></span>

<span data-ttu-id="690d8-623">Pour Windows général plus d’informations sur la build 16288 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="690d8-623">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-624">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-624">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-625">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-625">WSL</span></span>
- <span data-ttu-id="690d8-626">Initialiser correctement et de signaler les uid et gid mode pour les descripteurs de fichier socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="690d8-626">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="690d8-627">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-628">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-628">Console</span></span>
- <span data-ttu-id="690d8-629">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-630">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-630">LTP Results:</span></span>
<span data-ttu-id="690d8-631">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="690d8-631">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="690d8-632">Build 16278</span><span class="sxs-lookup"><span data-stu-id="690d8-632">Build 16278</span></span>

<span data-ttu-id="690d8-633">Pour Windows général plus d’informations sur la build 162738 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="690d8-633">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-634">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-634">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-635">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-635">WSL</span></span>
- <span data-ttu-id="690d8-636">Explicitement annuler le mappage de vues mappées des sections de la sauvegarde de fichiers lors de la destruction de l’état LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="690d8-636">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="690d8-637">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-637">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-638">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-638">Console</span></span>
- <span data-ttu-id="690d8-639">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-639">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-640">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-640">LTP Results:</span></span>
<span data-ttu-id="690d8-641">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="690d8-641">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="690d8-642">Build 16275</span><span class="sxs-lookup"><span data-stu-id="690d8-642">Build 16275</span></span>

<span data-ttu-id="690d8-643">Pour Windows général plus d’informations sur la build 162735 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="690d8-643">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-644">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-645">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-645">WSL</span></span>
- <span data-ttu-id="690d8-646">Aucun WSL les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-646">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-647">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-647">Console</span></span>
- <span data-ttu-id="690d8-648">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-648">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-649">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-649">LTP Results:</span></span>
<span data-ttu-id="690d8-650">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="690d8-650">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="690d8-651">Build 16273</span><span class="sxs-lookup"><span data-stu-id="690d8-651">Build 16273</span></span>

<span data-ttu-id="690d8-652">Pour Windows général plus d’informations sur la build 16273 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-652">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-653">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-653">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-654">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-654">WSL</span></span>
- <span data-ttu-id="690d8-655">Correction d’un problème où DrvFs parfois signalé le type de fichier incorrect pour les répertoires [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="690d8-655">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="690d8-656">Autoriser la création de sockets NETLINK_KOBJECT_UEVENT débloquer des programmes qui uevent utilisation [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="690d8-656">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="690d8-657">Ajouter la prise en charge pour la connexion à non bloquant [GH 903, 1391, 1584 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="690d8-657">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="690d8-658">Implémentez CLONE_FS cloner l’indicateur d’appel système [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="690d8-658">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="690d8-659">Résoudre les problèmes liés à la gère ne pas de tabulations ou guillemets correctement dans l’interopérabilité de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="690d8-659">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="690d8-660">Résoudre l’erreur lorsque vous tentez de relancer WSL instances [GH 651, 2095] l’accès refusé</span><span class="sxs-lookup"><span data-stu-id="690d8-660">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="690d8-661">Implémenter des opérations FUTEX_REQUEUE et FUTEX_CMP_REQUEUE futex [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="690d8-661">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="690d8-662">Corriger les autorisations pour les divers fichiers SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="690d8-662">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="690d8-663">Corriger le blocage de pile de Haskell pendant l’installation [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="690d8-663">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="690d8-664">Implémenter binfmt_misc « C » ' o ' et les indicateurs « P » [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="690d8-664">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="690d8-665">Ajouter /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="690d8-665">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="690d8-666">Ajouter la prise en charge partielle de l’appel de système d’ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="690d8-666">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="690d8-667">Stub SO_REUSEPORT & Ajout de prise en charge pour SO_PASSCRED pour les sockets netlink [69 GH]</span><span class="sxs-lookup"><span data-stu-id="690d8-667">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="690d8-668">Retourner différents codes d’erreur à partir de RegisterDistribuiton si une distribution est actuellement installée ou désinstallée.</span><span class="sxs-lookup"><span data-stu-id="690d8-668">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="690d8-669">Autoriser la désinscription des distributions de WSL partiellement installées via wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="690d8-669">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="690d8-670">Corriger le blocage de test de socket python à partir de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="690d8-670">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="690d8-671">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-671">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-672">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-672">Console</span></span>
- <span data-ttu-id="690d8-673">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-673">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-674">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-674">LTP Results:</span></span>
<span data-ttu-id="690d8-675">Nombre total de Tests : 1904</span><span class="sxs-lookup"><span data-stu-id="690d8-675">Total Tests: 1904</span></span><br/>
<span data-ttu-id="690d8-676">Total ignoré des Tests : 209</span><span class="sxs-lookup"><span data-stu-id="690d8-676">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="690d8-677">Nombre total d’échecs : 229</span><span class="sxs-lookup"><span data-stu-id="690d8-677">Total Failures: 229</span></span><br/>
[<span data-ttu-id="690d8-678">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-678">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="690d8-679">Build 16257</span><span class="sxs-lookup"><span data-stu-id="690d8-679">Build 16257</span></span>

<span data-ttu-id="690d8-680">Pour Windows général plus d’informations sur la build 16257 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-680">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-681">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-681">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-682">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-682">WSL</span></span>
- <span data-ttu-id="690d8-683">Implémenter l’appel du système prlimit64</span><span class="sxs-lookup"><span data-stu-id="690d8-683">Implement prlimit64 system call</span></span>
- <span data-ttu-id="690d8-684">Ajouter la prise en charge pour ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="690d8-684">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="690d8-685">Stub MSG_MORE pour les sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="690d8-685">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="690d8-686">Corriger comportement de vecteur auxiliaires AT_EXECFN non valide [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="690d8-686">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="690d8-687">Corriger le comportement de copier/coller pour console/tty et ajouter de la mémoire tampon saturée une meilleure gestion des [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="690d8-687">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="690d8-688">Définissez AT_SECURE dans un vecteur auxiliaire pour les programmes de set-user-ID et set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="690d8-688">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="690d8-689">Point de terminaison maître pseudo-périphérique-Terminal Server ne gère ne pas TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="690d8-689">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="690d8-690">Correctif lseek effectue pour rembobiner des répertoires dans LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="690d8-690">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="690d8-691">/dev/ptmx se bloque après une utilisation élevée [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="690d8-691">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="690d8-692">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-692">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-693">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-693">Console</span></span>
- <span data-ttu-id="690d8-694">Correctif pour horizontal lignes/des traits de soulignement Everywhere [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="690d8-694">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="690d8-695">Correctif pour l’ordre de processus modifié NPM ce qui rend plus difficile à fermer [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="690d8-695">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="690d8-696">Ajouté à notre nouveau modèle de couleurs : https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="690d8-696">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-697">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-697">LTP Results:</span></span>
<span data-ttu-id="690d8-698">Aucune modification depuis 16251</span><span class="sxs-lookup"><span data-stu-id="690d8-698">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-699">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-699">Syscall Support</span></span>
<span data-ttu-id="690d8-700">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-700">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-701">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-701">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="690d8-702">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="690d8-702">Known Issues</span></span>
#### [<a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="690d8-703">Problème GitHub 2392 : Dossiers de Windows n’est ne pas reconnu par WSL...</span><span class="sxs-lookup"><span data-stu-id="690d8-703">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="690d8-704">Dans la build 16257, WSL présente des problèmes lors de l’énumération des fichiers/dossiers de Windows via `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="690d8-704">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="690d8-705">Ce problème a été résolu et doivent être libéré dans Insiders build pendant la semaine 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="690d8-705">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="690d8-706">Build 16251</span><span class="sxs-lookup"><span data-stu-id="690d8-706">Build 16251</span></span>

<span data-ttu-id="690d8-707">Pour Windows général plus d’informations sur la build 16251 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-707">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-708">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-709">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-709">WSL</span></span>
- <span data-ttu-id="690d8-710">Supprimer la balise de version bêta de composant facultatif WSL, consultez [billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="690d8-710">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="690d8-711">Initialiser correctement enregistré-set uid et gid pour les fichiers binaires de set-user-ID et set-group-ID sur exec [962 GH 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="690d8-711">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="690d8-712">Prise en charge ajoutée pour ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="690d8-712">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="690d8-713">Prise en charge pour ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="690d8-713">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="690d8-714">Fixe ptrace pour arrêter des signaux ignoré</span><span class="sxs-lookup"><span data-stu-id="690d8-714">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="690d8-715">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-715">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-716">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-716">Console</span></span>
- <span data-ttu-id="690d8-717">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-717">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-718">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-718">LTP Results:</span></span>
<span data-ttu-id="690d8-719">Nombre de Tests concluants : 768</span><span class="sxs-lookup"><span data-stu-id="690d8-719">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="690d8-720">Nombre de Tests ayant échoué : 244</span><span class="sxs-lookup"><span data-stu-id="690d8-720">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="690d8-721">Nombre de Tests ignorés : 96</span><span class="sxs-lookup"><span data-stu-id="690d8-721">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="690d8-722">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-722">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="690d8-723">Build 16241</span><span class="sxs-lookup"><span data-stu-id="690d8-723">Build 16241</span></span>

<span data-ttu-id="690d8-724">Pour Windows général plus d’informations sur la build 16241 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-724">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-725">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-725">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="690d8-726">WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-726">WSL</span></span>
- <span data-ttu-id="690d8-727">Aucun WSL les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-727">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="690d8-728">Console</span><span class="sxs-lookup"><span data-stu-id="690d8-728">Console</span></span>
- <span data-ttu-id="690d8-729">Correctif pour la sortie de caractères incorrect pour DEC lignes d’origine, signalé initialement [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="690d8-729">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="690d8-730">Correctif pour aucun texte de sortie qui est affiché dans la page de codes 65001 (UTF-8)</span><span class="sxs-lookup"><span data-stu-id="690d8-730">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="690d8-731">Ne transférez pas les modifications apportées à un seul valeurs RVB à d’autres parties de la palette de la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="690d8-731">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="690d8-732">Cela fera la feuille de propriétés de console beaucoup plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="690d8-732">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="690d8-733">CTRL + S ne semble pas fonctionner correctement</span><span class="sxs-lookup"><span data-stu-id="690d8-733">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="690d8-734">Non gras /-Dim complètement absent à partir des codes d’échappement ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="690d8-734">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="690d8-735">Console ne correctement prendre en charge des thèmes de couleurs Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="690d8-735">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="690d8-736">Impossible de coller des caractères particuliers [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="690d8-736">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="690d8-737">Redimensionnement de redistribution interagit étrangement avec redimensionnement d’une fenêtre d’interpréteur de commandes lorsque les éléments se trouvent sur la ligne de commande/modifier [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="690d8-737">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="690d8-738">CTRL-L quitte l’écran dirty [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="690d8-738">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="690d8-739">Bogue de rendu de console lors de l’affichage VT sur HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="690d8-739">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="690d8-740">Caractères de la version japonaise paraître étranges avec un caractère Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="690d8-740">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="690d8-741">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-741">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="690d8-742">Build 16237</span><span class="sxs-lookup"><span data-stu-id="690d8-742">Build 16237</span></span>

<span data-ttu-id="690d8-743">Pour Windows général plus d’informations sur la build 16237 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-743">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-744">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-744">Fixed</span></span>
- <span data-ttu-id="690d8-745">Utiliser des attributs par défaut pour les fichiers sans EAs dans lxfs (racine, racine, 0000)</span><span class="sxs-lookup"><span data-stu-id="690d8-745">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="690d8-746">Prise en charge pour les distributions qui utilisent des attributs étendus</span><span class="sxs-lookup"><span data-stu-id="690d8-746">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="690d8-747">Correctif de remplissage pour les entrées retournées par getdents et getdents64</span><span class="sxs-lookup"><span data-stu-id="690d8-747">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="690d8-748">Corriger la vérification des autorisations pour l’appel de système SHM_STAT shmctl [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="690d8-748">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="690d8-749">État fixe epoll initiale incorrect pour les TTY ne [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="690d8-749">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="690d8-750">Corriger readdir DrvFs ne pas renvoie toutes les entrées [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="690d8-750">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="690d8-751">Corriger LxFs readdir lorsque les fichiers sont dissocié [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="690d8-751">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="690d8-752">Autoriser les fichiers drvfs non liés à être rouverte via la commande procfs</span><span class="sxs-lookup"><span data-stu-id="690d8-752">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="690d8-753">Ajouté la substitution de clé de Registre global pour la désactivation des fonctionnalités WSL (interop / le montage du lecteur)</span><span class="sxs-lookup"><span data-stu-id="690d8-753">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="690d8-754">Résoudre le nombre de blocs incorrect dans « stat » pour DrvFs (et LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="690d8-754">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="690d8-755">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-755">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="690d8-756">Build 16232</span><span class="sxs-lookup"><span data-stu-id="690d8-756">Build 16232</span></span>

<span data-ttu-id="690d8-757">Pour Windows général plus d’informations sur la build 16232 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-757">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-758">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-758">Fixed</span></span>
- <span data-ttu-id="690d8-759">Aucun WSL les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="690d8-759">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="690d8-760">Build 16226</span><span class="sxs-lookup"><span data-stu-id="690d8-760">Build 16226</span></span>

<span data-ttu-id="690d8-761">Pour Windows général plus d’informations sur la build 16226 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-761">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-762">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-762">Fixed</span></span>
- <span data-ttu-id="690d8-763">xattr liés prise en charge syscalls (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="690d8-763">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="690d8-764">prise en charge de Security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="690d8-764">security.capablity xattr support.</span></span>
- <span data-ttu-id="690d8-765">Une meilleure compatibilité avec certains systèmes de fichiers et les filtres, y compris les serveurs SMB non - MS.</span><span class="sxs-lookup"><span data-stu-id="690d8-765">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="690d8-766">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="690d8-766">[GH #1952]</span></span>
- <span data-ttu-id="690d8-767">Prise en charge améliorée pour les espaces réservés de OneDrive, des espaces réservés GVFS et du système d’exploitation Compact des fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="690d8-767">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="690d8-768">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-768">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="690d8-769">Build 16215</span><span class="sxs-lookup"><span data-stu-id="690d8-769">Build 16215</span></span>

<span data-ttu-id="690d8-770">Pour Windows général plus d’informations sur la build 16215 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-770">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-771">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-771">Fixed</span></span>
- <span data-ttu-id="690d8-772">WSL ne requiert plus le mode développeur.</span><span class="sxs-lookup"><span data-stu-id="690d8-772">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="690d8-773">Prend en charge les jonctions de répertoires dans drvfs.</span><span class="sxs-lookup"><span data-stu-id="690d8-773">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="690d8-774">Gérer la désinstallation des packages appx de distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-774">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="690d8-775">Mise à jour de commande procfs pour afficher privés et partagés des mappages.</span><span class="sxs-lookup"><span data-stu-id="690d8-775">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="690d8-776">Ajoutez la possibilité pour wslconfig.exe nettoyer les distributions qui sont partiellement installées ou désinstallées.</span><span class="sxs-lookup"><span data-stu-id="690d8-776">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="690d8-777">Prise en charge ajoutée pour IP_MTU_DISCOVER pour les sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="690d8-777">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="690d8-778">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="690d8-778">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="690d8-779">Déduire la famille de protocoles pour les itinéraires à AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="690d8-779">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="690d8-780">Améliorations de l’appareil de série [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="690d8-780">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="690d8-781">Build 16199</span><span class="sxs-lookup"><span data-stu-id="690d8-781">Build 16199</span></span>

<span data-ttu-id="690d8-782">Pour Windows général plus d’informations sur la build 16199 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-782">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-783">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-783">Fixed</span></span>
- <span data-ttu-id="690d8-784">Aucun WSL les modifications n’associées dans ces versions.</span><span class="sxs-lookup"><span data-stu-id="690d8-784">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="690d8-785">Build 16193</span><span class="sxs-lookup"><span data-stu-id="690d8-785">Build 16193</span></span>

<span data-ttu-id="690d8-786">Pour Windows général plus d’informations sur la build 16193 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-786">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-787">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-787">Fixed</span></span>
- <span data-ttu-id="690d8-788">Condition de concurrence entre les envois de SIGCONT et un threadgroup fin d’exécution [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="690d8-788">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="690d8-789">modifier les appareils tty et pty au rapport FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="690d8-789">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="690d8-790">Correctif SSH pour IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="690d8-790">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="690d8-791">Déplacé le montage DrvFs init démon [1862 Hg, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="690d8-791">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="690d8-792">Prise en charge dans DrvFs pour les liens symboliques de NT.</span><span class="sxs-lookup"><span data-stu-id="690d8-792">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="690d8-793">Build 16184</span><span class="sxs-lookup"><span data-stu-id="690d8-793">Build 16184</span></span>

<span data-ttu-id="690d8-794">Pour Windows général plus d’informations sur la build 16184 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-794">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-795">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-795">Fixed</span></span>
- <span data-ttu-id="690d8-796">Supprimer la tâche de maintenance de package apt (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="690d8-796">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="690d8-797">Sortie fixe ne s’affichent ne pas dans des processus Windows dans node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="690d8-797">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="690d8-798">Assouplir les conditions d’alignement dans lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="690d8-798">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="690d8-799">Correction de la gestion de l’indicateur AT_EMPTY_PATH dans un nombre d’appels système.</span><span class="sxs-lookup"><span data-stu-id="690d8-799">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="690d8-800">Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts provoquera le fichier un comportement non défini [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="690d8-800">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="690d8-801">/ etc/hosts hérite désormais les entrées à partir du fichier d’hôtes Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="690d8-801">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="690d8-802">Build 16179</span><span class="sxs-lookup"><span data-stu-id="690d8-802">Build 16179</span></span>

<span data-ttu-id="690d8-803">Pour Windows général plus d’informations sur la build 16179 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-803">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-804">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-804">Fixed</span></span>
- <span data-ttu-id="690d8-805">Aucune modification WSL cette semaine.</span><span class="sxs-lookup"><span data-stu-id="690d8-805">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="690d8-806">Build 16176</span><span class="sxs-lookup"><span data-stu-id="690d8-806">Build 16176</span></span>

<span data-ttu-id="690d8-807">Pour Windows général plus d’informations sur la build 16176 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-807">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-808">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-808">Fixed</span></span>

- [<span data-ttu-id="690d8-809">Prise en charge de la série est activée</span><span class="sxs-lookup"><span data-stu-id="690d8-809">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="690d8-810">Option de socket ajoutée IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="690d8-810">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="690d8-811">Implémenté pwritev (fonction) (lors du téléchargement du fichier à nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="690d8-811">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="690d8-812">Ajouté des options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="690d8-812">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="690d8-813">Prise en charge pour l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="690d8-813">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="690d8-814">Option de socket IP (V6) _MTU ajoutée pour le nœud applications, détermination d’itinéraire, dig, nslookup, hôte</span><span class="sxs-lookup"><span data-stu-id="690d8-814">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="690d8-815">Option de socket ajoutée IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="690d8-815">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="690d8-816">Améliorations du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="690d8-816">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="690d8-817">Autoriser le montage des chemins d’accès UNC</span><span class="sxs-lookup"><span data-stu-id="690d8-817">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="690d8-818">Activer la prise en charge CDFS dans drvfs</span><span class="sxs-lookup"><span data-stu-id="690d8-818">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="690d8-819">Gérer correctement les autorisations pour les systèmes de fichiers réseau dans drvfs</span><span class="sxs-lookup"><span data-stu-id="690d8-819">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="690d8-820">Ajouter la prise en charge pour les lecteurs à distance à drvfs</span><span class="sxs-lookup"><span data-stu-id="690d8-820">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="690d8-821">Activer FAT prennent en charge dans drvfs</span><span class="sxs-lookup"><span data-stu-id="690d8-821">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="690d8-822">Autres correctifs et améliorations</span><span class="sxs-lookup"><span data-stu-id="690d8-822">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-823">Résultats LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-823">LTP Results</span></span>
<span data-ttu-id="690d8-824">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="690d8-824">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="690d8-825">Build 16170</span><span class="sxs-lookup"><span data-stu-id="690d8-825">Build 16170</span></span>

<span data-ttu-id="690d8-826">Pour Windows général plus d’informations sur la build 16170 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-826">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="690d8-827">Nous avons publié un nouveau [billet de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) traitant de nos efforts pour tester WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-827">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="690d8-828">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-828">Fixed</span></span>

- <span data-ttu-id="690d8-829">Socket de prise en charge option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="690d8-829">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="690d8-830">Ajouter la prise en charge pour PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="690d8-830">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="690d8-831">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="690d8-831">[GH 1692]</span></span>
- <span data-ttu-id="690d8-832">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-832">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-833">Résultats LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-833">LTP Results</span></span>
<span data-ttu-id="690d8-834">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="690d8-834">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="690d8-835">Build 15046 vers Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="690d8-835">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="690d8-836">Il existe plus aucune WSL correctifs ou les fonctionnalités prévues pour être inclus dans la mise à jour Windows 10 Creators.</span><span class="sxs-lookup"><span data-stu-id="690d8-836">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="690d8-837">Notes de publication pour WSL reprendra dans les semaines à venir pour les ajouts de ciblage de la prochaine mise à jour Windows majeures.</span><span class="sxs-lookup"><span data-stu-id="690d8-837">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="690d8-838">Pour Windows général plus d’informations sur la build 15046 et Insider futures versions visite le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-838">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="690d8-839">Build 15042</span><span class="sxs-lookup"><span data-stu-id="690d8-839">Build 15042</span></span>

<span data-ttu-id="690d8-840">Pour Windows général plus d’informations sur la build 15042 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-840">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-841">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-841">Fixed</span></span>

- <span data-ttu-id="690d8-842">Correction d’un blocage lors de la suppression d’un chemin d’accès se terminant par «... »</span><span class="sxs-lookup"><span data-stu-id="690d8-842">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="690d8-843">Correction d’un problème où FIONBIO ne pas retourner 0 en cas de réussite [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="690d8-843">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="690d8-844">Correction d’un problème avec des lectures de longueur nulle de sockets de datagramme inet</span><span class="sxs-lookup"><span data-stu-id="690d8-844">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="690d8-845">Résoudre un blocage possible en raison d’une condition de concurrence dans drvfs inode recherche [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="690d8-845">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="690d8-846">Prise en charge pour les données connexes de socket unix ; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="690d8-846">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="690d8-847">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-847">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-848">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-848">LTP Results:</span></span>
<span data-ttu-id="690d8-849">Nombre de Test réussi : 737</span><span class="sxs-lookup"><span data-stu-id="690d8-849">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="690d8-850">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="690d8-850">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="690d8-851">Build 15031</span><span class="sxs-lookup"><span data-stu-id="690d8-851">Build 15031</span></span>

<span data-ttu-id="690d8-852">Pour Windows général plus d’informations sur la build 15031 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-852">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-853">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-853">Fixed</span></span>

- <span data-ttu-id="690d8-854">Correction d’un bogue où time(2) est sporadique mener.</span><span class="sxs-lookup"><span data-stu-id="690d8-854">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="690d8-855">Fixe et émettre où \* SIGPROCMASK syscalls peut endommager le masque de signal.</span><span class="sxs-lookup"><span data-stu-id="690d8-855">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="690d8-856">Maintenant retourner la longueur de ligne de commande complète dans la notification de la création de processus WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-856">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="690d8-857">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="690d8-857">[GH 1632]</span></span>
- <span data-ttu-id="690d8-858">WSL signale désormais la sortie du thread via ptrace pour les blocages GDB.</span><span class="sxs-lookup"><span data-stu-id="690d8-858">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="690d8-859">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="690d8-859">[GH 1196]</span></span>
- <span data-ttu-id="690d8-860">Correction du bogue où se bloquait ptys après tmux importante d’e/s.</span><span class="sxs-lookup"><span data-stu-id="690d8-860">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="690d8-861">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="690d8-861">[GH 1358]</span></span>
- <span data-ttu-id="690d8-862">Validation du délai d’expiration fixe dans un grand nombre d’appels système (futex, semtimedop, ppoll, sigtimewait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="690d8-862">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="690d8-863">Prise en charge EFD_SEMAPHORE eventfd ajout [GH 452]</span><span class="sxs-lookup"><span data-stu-id="690d8-863">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="690d8-864">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-864">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-865">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-865">LTP Results:</span></span>
<span data-ttu-id="690d8-866">Nombre de Test réussi : 737</span><span class="sxs-lookup"><span data-stu-id="690d8-866">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="690d8-867">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="690d8-867">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="690d8-868">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-868">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="690d8-869">Build 15025</span><span class="sxs-lookup"><span data-stu-id="690d8-869">Build 15025</span></span>

<span data-ttu-id="690d8-870">Pour Windows général plus d’informations sur la build 15025 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-870">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-871">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-871">Fixed</span></span>

- <span data-ttu-id="690d8-872">Correctif pour bogue que grep ne 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="690d8-872">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="690d8-873">Indicateur EFD_SEMAPHORE implémentée pour syscall eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="690d8-873">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="690d8-874">Implémenté/proc / [pid] / net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="690d8-874">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="690d8-875">Signal contrôlée par la prise en charge d’e/s pour les sockets de flux unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="690d8-875">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="690d8-876">Prendre en charge F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="690d8-876">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="690d8-877">Implémenter recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="690d8-877">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="690d8-878">Correction du bogue où les epoll_wait() n’a pas été en attente [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="690d8-878">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="690d8-879">Implement /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="690d8-879">Implement /proc/version_signature</span></span>
- <span data-ttu-id="690d8-880">Tee syscall retourne maintenant échec si les deux descripteurs de fichier font référence au même canal</span><span class="sxs-lookup"><span data-stu-id="690d8-880">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="690d8-881">Comportement correct implémentée pour SO_PEERCRED pour les sockets Unix</span><span class="sxs-lookup"><span data-stu-id="690d8-881">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="690d8-882">Gestion des paramètres non valides de syscall tkill fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-882">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="690d8-883">Modifications pour augmenter la preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="690d8-883">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="690d8-884">Correctif mineur pour le blocage des e/s de Ruby</span><span class="sxs-lookup"><span data-stu-id="690d8-884">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="690d8-885">Fixe recvmsg() retour EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="690d8-885">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="690d8-886">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-886">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-887">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-887">LTP Results:</span></span>
<span data-ttu-id="690d8-888">Nombre de Test réussi : 732</span><span class="sxs-lookup"><span data-stu-id="690d8-888">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="690d8-889">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="690d8-889">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="690d8-890">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-890">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="690d8-891">Build 15019</span><span class="sxs-lookup"><span data-stu-id="690d8-891">Build 15019</span></span>

<span data-ttu-id="690d8-892">Pour Windows général plus d’informations sur la build 15019 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-892">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-893">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-893">Fixed</span></span>

- <span data-ttu-id="690d8-894">Correction du bogue qui est signalé à tort l’utilisation du processeur dans commande procfs pour des outils comme htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="690d8-894">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="690d8-895">Lors de l’appel open() avec O_TRUNC sur un fichier inotify génère désormais IN_MODIFY avant IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="690d8-895">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="690d8-896">Correctifs pour unix socket getsockopt SO_ERROR pour activer postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="690d8-896">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="690d8-897">Implémenter /proc/sys/net/core/somaxconn pour le langage GO</span><span class="sxs-lookup"><span data-stu-id="690d8-897">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="690d8-898">Tâche d’arrière-plan apt-get package mise à jour s’exécute désormais masqué à partir de la vue</span><span class="sxs-lookup"><span data-stu-id="690d8-898">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="690d8-899">Étendue clair pour ipv6 localhost (Spring-Framework(Java) échec).</span><span class="sxs-lookup"><span data-stu-id="690d8-899">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="690d8-900">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-900">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-901">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-901">LTP Results:</span></span>
<span data-ttu-id="690d8-902">Nombre de Test réussi : 714</span><span class="sxs-lookup"><span data-stu-id="690d8-902">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="690d8-903">Nombre de cas d’échec (échec, ignoré, etc....) : 249</span><span class="sxs-lookup"><span data-stu-id="690d8-903">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="690d8-904">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-904">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="690d8-905">Build 15014</span><span class="sxs-lookup"><span data-stu-id="690d8-905">Build 15014</span></span>

<span data-ttu-id="690d8-906">Pour Windows général plus d’informations sur la build 15014 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="690d8-906">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-907">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-907">Fixed</span></span>

- <span data-ttu-id="690d8-908">CTRL + C fonctionne désormais comme prévu</span><span class="sxs-lookup"><span data-stu-id="690d8-908">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="690d8-909">htop et ps auxw maintenant afficher correct l’utilisation des ressources (GH #516)</span><span class="sxs-lookup"><span data-stu-id="690d8-909">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="690d8-910">Traduction de base des exceptions de NT aux signaux.</span><span class="sxs-lookup"><span data-stu-id="690d8-910">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="690d8-911">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="690d8-911">(GH #513)</span></span>
- <span data-ttu-id="690d8-912">fallocate échoue avec ENOSPC alors EINVAL (GH #1571) au lieu de l’espace est insuffisant</span><span class="sxs-lookup"><span data-stu-id="690d8-912">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="690d8-913">/Proc/sys/kernel/sem ajouté.</span><span class="sxs-lookup"><span data-stu-id="690d8-913">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="690d8-914">Appels de système semop et semtimedop implémentées</span><span class="sxs-lookup"><span data-stu-id="690d8-914">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="690d8-915">Erreurs nslookup fixe avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (69 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-915">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="690d8-916">Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="690d8-916">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="690d8-917">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-917">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-918">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-918">LTP Results:</span></span>
<span data-ttu-id="690d8-919">Nombre de Test réussi : 709</span><span class="sxs-lookup"><span data-stu-id="690d8-919">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="690d8-920">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="690d8-920">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="690d8-921">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-921">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="690d8-922">Résumé de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-922">Syscall Summary</span></span>
<span data-ttu-id="690d8-923">Syscalls total : 384</span><span class="sxs-lookup"><span data-stu-id="690d8-923">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="690d8-924">Total implémenté : 235</span><span class="sxs-lookup"><span data-stu-id="690d8-924">Total Implemented: 235</span></span> </br>
<span data-ttu-id="690d8-925">Nombre total de l’objet d’un stub : 22</span><span class="sxs-lookup"><span data-stu-id="690d8-925">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="690d8-926">Total non implémenté : 127</span><span class="sxs-lookup"><span data-stu-id="690d8-926">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="690d8-927">Analyse détaillée</span><span class="sxs-lookup"><span data-stu-id="690d8-927">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="690d8-928">Build 15007</span><span class="sxs-lookup"><span data-stu-id="690d8-928">Build 15007</span></span>

<span data-ttu-id="690d8-929">Pour Windows général plus d’informations sur la build 15007 visitez le [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="690d8-929">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="690d8-930">Problème connu</span><span class="sxs-lookup"><span data-stu-id="690d8-930">Known Issue</span></span>

- <span data-ttu-id="690d8-931">Il existe un bogue connu dans lequel la console ne reconnaît pas certains Ctrl + <key> d’entrée.</span><span class="sxs-lookup"><span data-stu-id="690d8-931">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="690d8-932">Cela inclut la commande ctrl-c qui agira comme un keypress « c » normal.</span><span class="sxs-lookup"><span data-stu-id="690d8-932">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="690d8-933">Solution : Mapper une autre clé à Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="690d8-933">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="690d8-934">Par exemple, Ctrl + K, Ctrl + c faire pour mapper : `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="690d8-934">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="690d8-935">Ce mappage s’effectue par terminal et devra être fait *chaque* bash de temps est lancée.</span><span class="sxs-lookup"><span data-stu-id="690d8-935">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="690d8-936">Les utilisateurs peuvent Explorer la possibilité d’inclure cela dans leurs</span><span class="sxs-lookup"><span data-stu-id="690d8-936">Users can explore the option to include this in their</span></span> `.bashrc`

### <a name="fixed"></a><span data-ttu-id="690d8-937">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-937">Fixed</span></span>

- <span data-ttu-id="690d8-938">Correction du problème où en cours d’exécution WSL consomme 100 % d’un cœur de processeur</span><span class="sxs-lookup"><span data-stu-id="690d8-938">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="690d8-939">Option IP_PKTINFO, IPV6_RECVPKTINFO désormais pris en charge de socket.</span><span class="sxs-lookup"><span data-stu-id="690d8-939">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="690d8-940">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="690d8-940">(GH #851, 987)</span></span>
- <span data-ttu-id="690d8-941">Tronquer l’adresse d’interface réseau physique à 16 octets lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="690d8-941">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="690d8-942">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-942">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-943">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-943">LTP Results:</span></span>
<span data-ttu-id="690d8-944">Nombre de Test réussi : 709</span><span class="sxs-lookup"><span data-stu-id="690d8-944">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="690d8-945">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="690d8-945">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="690d8-946">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-946">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="690d8-947">Build 15002</span><span class="sxs-lookup"><span data-stu-id="690d8-947">Build 15002</span></span>

<span data-ttu-id="690d8-948">Pour Windows général plus d’informations sur la build 15002 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-948">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="690d8-949">Problème connu</span><span class="sxs-lookup"><span data-stu-id="690d8-949">Known Issue</span></span>

<span data-ttu-id="690d8-950">Deux problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="690d8-950">Two known issues:</span></span>
- <span data-ttu-id="690d8-951">Il existe un bogue connu dans lequel la console ne reconnaît pas certains Ctrl + <key> d’entrée.</span><span class="sxs-lookup"><span data-stu-id="690d8-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="690d8-952">Cela inclut la commande ctrl-c qui agira comme un keypress « c » normal.</span><span class="sxs-lookup"><span data-stu-id="690d8-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="690d8-953">Solution : Mapper une autre clé à Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="690d8-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="690d8-954">Par exemple, Ctrl + K, Ctrl + c faire pour mapper : `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="690d8-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="690d8-955">Ce mappage s’effectue par terminal et devra être fait *chaque* bash de temps est lancée.</span><span class="sxs-lookup"><span data-stu-id="690d8-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="690d8-956">Les utilisateurs peuvent Explorer la possibilité d’inclure cela dans leurs</span><span class="sxs-lookup"><span data-stu-id="690d8-956">Users can explore the option to include this in their</span></span> `.bashrc`

- <span data-ttu-id="690d8-957">Pendant l’exécution de WSL un thread système consomme 100 % d’un cœur de processeur.</span><span class="sxs-lookup"><span data-stu-id="690d8-957">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="690d8-958">La cause racine a été adressée et fixe en interne.</span><span class="sxs-lookup"><span data-stu-id="690d8-958">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="690d8-959">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-959">Fixed</span></span>

- <span data-ttu-id="690d8-960">Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="690d8-960">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="690d8-961">Vous essayez de démarrer une session à un autre niveau sera bloquée.</span><span class="sxs-lookup"><span data-stu-id="690d8-961">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="690d8-962">Cela signifie que les consoles administrateur et non-administrateur ne peut pas s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="690d8-962">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="690d8-963">(#626 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-963">(GH #626)</span></span>
<br/>
- <span data-ttu-id="690d8-964">Implémenté les messages NETLINK_ROUTE suivants (exige un administrateur de Windows)</span><span class="sxs-lookup"><span data-stu-id="690d8-964">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="690d8-965">RTM_NEWADDR (prend en charge `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="690d8-965">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="690d8-966">RTM_NEWROUTE (prend en charge `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="690d8-966">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="690d8-967">RTM_DELADDR (prend en charge `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="690d8-967">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="690d8-968">RTM_DELROUTE (prend en charge `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="690d8-968">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="690d8-969">Vérification des packages à mettre à jour de tâche planifiée ne s’est plus sur une connexion limitée (GH # 1 371)</span><span class="sxs-lookup"><span data-stu-id="690d8-969">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="690d8-970">Correction d’erreur dans lequel tuyauterie obtient bloquée par exemple, c - bash « ls - alR / » | Bash -c « cat » (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="690d8-970">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="690d8-971">Option de socket TCP_KEEPCNT implémentée (GH #843)</span><span class="sxs-lookup"><span data-stu-id="690d8-971">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="690d8-972">Option de socket IP_MTU_DISCOVER INET implémentée (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="690d8-972">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="690d8-973">Supprimé des fonctionnalités héritées pour exécuter des fichiers binaires de NT à partir d’init avec la recherche de chemin d’accès de NT.</span><span class="sxs-lookup"><span data-stu-id="690d8-973">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="690d8-974">(#1325 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-974">(GH #1325)</span></span>
- <span data-ttu-id="690d8-975">Corriger le mode de/dev/kmsg pour autoriser l’accès de lecture de groupe / autre (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="690d8-975">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="690d8-976">/Proc/sys/kernel/random/uuid implémentée (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="690d8-976">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="690d8-977">Correction d’erreur où l’heure de début de processus n’affiche qu’année 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="690d8-977">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="690d8-978">Variable d’environnement terme par défaut commuté xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="690d8-978">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="690d8-979">Modifié la façon dont les processus de validation est calculée pendant la duplication du processus.</span><span class="sxs-lookup"><span data-stu-id="690d8-979">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="690d8-980">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="690d8-980">(GH #1286)</span></span>
- <span data-ttu-id="690d8-981">/Proc/sys/vm/overcommit_memory implémentée.</span><span class="sxs-lookup"><span data-stu-id="690d8-981">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="690d8-982">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="690d8-982">(GH #1286)</span></span>
- <span data-ttu-id="690d8-983">Fichier /proc/net/route implémentée (GH #69)</span><span class="sxs-lookup"><span data-stu-id="690d8-983">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="690d8-984">Correction de l’erreur où nom raccourci a été correctement localisés (GH #696)</span><span class="sxs-lookup"><span data-stu-id="690d8-984">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="690d8-985">Elf fixe logique qui est incorrectement la validation des en-têtes de programme d’analyse doit être inférieur (ou égal à) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="690d8-985">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="690d8-986">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="690d8-986">(GH #1048)</span></span>
- <span data-ttu-id="690d8-987">Rappel statfs implémentée pour la commande procfs, sysfs cgroupfs et binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="690d8-987">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="690d8-988">Windows AptPackageIndexUpdate fixes qui ne se ferme pas (GH #1184, également abordées dans GH #1193)</span><span class="sxs-lookup"><span data-stu-id="690d8-988">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="690d8-989">Prise en charge ADDR_NO_RANDOMIZE du personnalité ASLR ajouté.</span><span class="sxs-lookup"><span data-stu-id="690d8-989">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="690d8-990">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="690d8-990">(GH #1148, 1128)</span></span>
- <span data-ttu-id="690d8-991">PTRACE_GETSIGINFO améliorée, SIGSEGV, pour les traces de pile gdb appropriée pendant AV (875 de # Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-991">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="690d8-992">ELF l’analyse n’est plus échoue pour les fichiers binaires patchelf.</span><span class="sxs-lookup"><span data-stu-id="690d8-992">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="690d8-993">(#471 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-993">(GH #471)</span></span>
- <span data-ttu-id="690d8-994">VPN DNS propagées à /etc/resolv.conf (GH #416 1350)</span><span class="sxs-lookup"><span data-stu-id="690d8-994">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="690d8-995">Améliorations apportées à TCP fermer pour le transfert de données plus fiable.</span><span class="sxs-lookup"><span data-stu-id="690d8-995">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="690d8-996">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="690d8-996">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="690d8-997">Code d’erreur correct retournent désormais lorsque trop de fichiers est ouverts (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="690d8-997">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="690d8-998">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="690d8-998">(GH #1126, 2090)</span></span>
- <span data-ttu-id="690d8-999">Rapports d’Audit de Windows journal maintenant nom de l’image dans le processus de création d’audit.</span><span class="sxs-lookup"><span data-stu-id="690d8-999">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="690d8-1000">Échouer normalement lors du lancement bash.exe à partir d’une fenêtre d’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="690d8-1000">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="690d8-1001">Message d’erreur ajoutés lorsque l’interopérabilité ne parvient pas à accéder à un répertoire de travail sous LxFs (par exemple, notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="690d8-1001">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="690d8-1002">Résolution du problème où le chemin d’accès Windows a été tronquée dans WSL</span><span class="sxs-lookup"><span data-stu-id="690d8-1002">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="690d8-1003">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1003">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1004">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1004">LTP Results:</span></span>
<span data-ttu-id="690d8-1005">Nombre de Test réussi : 690</span><span class="sxs-lookup"><span data-stu-id="690d8-1005">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="690d8-1006">Nombre de cas d’échec (échec, ignoré, etc....) : 274</span><span class="sxs-lookup"><span data-stu-id="690d8-1006">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="690d8-1007">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1007">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1008">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1008">Syscall Support</span></span>
<span data-ttu-id="690d8-1009">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1009">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1010">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1010">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="690d8-1011">Build 14986</span><span class="sxs-lookup"><span data-stu-id="690d8-1011">Build 14986</span></span>

<span data-ttu-id="690d8-1012">Pour Windows général plus d’informations sur la build 14986 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1012">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1013">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1013">Fixed</span></span>

- <span data-ttu-id="690d8-1014">Correction de bogues avec Netlink et Pty IOCTL</span><span class="sxs-lookup"><span data-stu-id="690d8-1014">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="690d8-1015">Version du noyau signale désormais 4.4.0-43 par souci de cohérence avec Xenial</span><span class="sxs-lookup"><span data-stu-id="690d8-1015">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="690d8-1016">Bash.exe lance maintenant lorsque l’entrée dirigée vers ' nul :' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="690d8-1016">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="690d8-1017">ID de thread signalés désormais correctement dans la commande procfs (#967 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-1017">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="690d8-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Indicateurs IN_ISDIR désormais pris en charge dans inotify_add_watch() (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="690d8-1018">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="690d8-1019">Implémentez timer_create et les appels système associées.</span><span class="sxs-lookup"><span data-stu-id="690d8-1019">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="690d8-1020">Cela permet la prise en charge GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="690d8-1020">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="690d8-1021">Résolution du problème où ping retourné un temps de 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="690d8-1021">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="690d8-1022">Retourne le code d’erreur approprié lorsque trop de fichiers est ouverts.</span><span class="sxs-lookup"><span data-stu-id="690d8-1022">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="690d8-1023">Résolution du problème dans WSL où demande Netlink pour les données de l’interface réseau échoue avec EINVAL si l’adresse matérielle de l’interface est de 32 octets (par exemple, l’interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="690d8-1023">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="690d8-1024">Notez que l’utilitaire de Linux « ip » contient un bogue dans lequel il se bloque si WSL signale une adresse matérielle de 32 octets.</span><span class="sxs-lookup"><span data-stu-id="690d8-1024">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="690d8-1025">Il s’agit d’un bogue dans « ip », pas WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1025">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="690d8-1026">Le « ip » utilitaire code en dur la longueur de la mémoire tampon de chaîne utilisée pour imprimer l’adresse de matériel, et cette mémoire tampon est trop petit pour imprimer une adresse matérielle de 32 octets.</span><span class="sxs-lookup"><span data-stu-id="690d8-1026">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="690d8-1027">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1027">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1028">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1028">LTP Results:</span></span>
<span data-ttu-id="690d8-1029">Nombre de Test réussi : 669</span><span class="sxs-lookup"><span data-stu-id="690d8-1029">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="690d8-1030">Nombre de cas d’échec (échec, ignoré, etc....) : 258</span><span class="sxs-lookup"><span data-stu-id="690d8-1030">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="690d8-1031">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1031">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1032">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1032">Syscall Support</span></span>
<span data-ttu-id="690d8-1033">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1033">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1034">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1034">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="690d8-1035">Build 14971</span><span class="sxs-lookup"><span data-stu-id="690d8-1035">Build 14971</span></span>

<span data-ttu-id="690d8-1036">Pour Windows général plus d’informations sur la build 14971 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1036">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1037">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1037">Fixed</span></span>

 - <span data-ttu-id="690d8-1038">En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-1038">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="690d8-1039">Mises à jour régulièrement planifiées reprendra à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="690d8-1039">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1040">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1040">LTP Results:</span></span>
<span data-ttu-id="690d8-1041">Inchangé depuis 14965</span><span class="sxs-lookup"><span data-stu-id="690d8-1041">Unchanged from 14965</span></span> </br>
<span data-ttu-id="690d8-1042">Nombre de Test réussi : 664</span><span class="sxs-lookup"><span data-stu-id="690d8-1042">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="690d8-1043">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1043">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1044">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="690d8-1045">Build 14965</span><span class="sxs-lookup"><span data-stu-id="690d8-1045">Build 14965</span></span>

<span data-ttu-id="690d8-1046">Pour Windows général plus d’informations sur la build 14965 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1046">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1047">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1047">Fixed</span></span>

- <span data-ttu-id="690d8-1048">Prise en charge de Netlink des sockets du protocole NETLINK_ROUTE RTM_GETLINK et RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="690d8-1048">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="690d8-1049">Permet aux commandes ifconfig et l’adresse ip pour l’énumération de réseau</span><span class="sxs-lookup"><span data-stu-id="690d8-1049">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="690d8-1050">Vous trouverez plus d’informations dans nos [WSL mise en réseau de billet de blog](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1050">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="690d8-1051">/sbin est désormais dans le chemin de l’utilisateur par défaut</span><span class="sxs-lookup"><span data-stu-id="690d8-1051">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="690d8-1052">Chemin d’accès de l’utilisateur NT maintenant ajouté pour le chemin d’accès WSL par défaut (par exemple, vous pouvez désormais taper notepad.exe sans ajouter System32 dans le chemin d’accès Linux)</span><span class="sxs-lookup"><span data-stu-id="690d8-1052">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="690d8-1053">Prise en charge ajoutée pour /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="690d8-1053">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="690d8-1054">Les fichiers binaires de NT peut maintenant être lancées depuis WSL lorsque le répertoire de travail actuel contient des caractères non-ansi (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="690d8-1054">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="690d8-1055">Autoriser l’arrêt sur un socket de flux de données déconnecté unix.</span><span class="sxs-lookup"><span data-stu-id="690d8-1055">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="690d8-1056">Prise en charge ajoutée pour PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="690d8-1056">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="690d8-1057">Prise en charge ajoutée pour CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="690d8-1057">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="690d8-1058">Correction d’erreur dans lequel tuyauterie obtient bloquée par exemple, c - bash « ls - alR / » | Bash -c « cat » (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="690d8-1058">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="690d8-1059">Demandes de handle de connexion vers le terminal actuel.</span><span class="sxs-lookup"><span data-stu-id="690d8-1059">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="690d8-1060">Marquer/proc /<pid>/oom_score_adj comme accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="690d8-1060">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="690d8-1061">Ajouter un dossier de /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="690d8-1061">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="690d8-1062">sched_setaffinity doit renvoyer le nombre de masque de bits d’affinité</span><span class="sxs-lookup"><span data-stu-id="690d8-1062">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="690d8-1063">Corriger la logique de validation ELF qui incorrectement suppose de chemins d’accès de l’interpréteur doivent comporter moins de 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="690d8-1063">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="690d8-1064">(#743 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-1064">(GH #743)</span></span>
- <span data-ttu-id="690d8-1065">Descripteurs de fichiers ouverts peuvent conserver la fenêtre de console ouverte (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="690d8-1065">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="690d8-1066">Erreur Fixeed où rename() a échoué avec barre oblique sur le nom de la cible (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="690d8-1066">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="690d8-1067">Implémenter /proc/net/dev fichier</span><span class="sxs-lookup"><span data-stu-id="690d8-1067">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="690d8-1068">0.000ms fixe effectue un test ping en raison de la résolution du chronomètre.</span><span class="sxs-lookup"><span data-stu-id="690d8-1068">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="690d8-1069">/Proc/self/environ implémentée (GH #730)</span><span class="sxs-lookup"><span data-stu-id="690d8-1069">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="690d8-1070">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1070">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1071">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1071">LTP Results:</span></span>
<span data-ttu-id="690d8-1072">Nombre de Test réussi : 664</span><span class="sxs-lookup"><span data-stu-id="690d8-1072">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="690d8-1073">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1073">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1074">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1074">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="690d8-1075">Build 14959</span><span class="sxs-lookup"><span data-stu-id="690d8-1075">Build 14959</span></span>

<span data-ttu-id="690d8-1076">Pour Windows général plus d’informations sur la build 14959 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="690d8-1076">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1077">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1077">Fixed</span></span>

- <span data-ttu-id="690d8-1078">Notification Pico processus amélioré pour Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-1078">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="690d8-1079">Des informations supplémentaires disponibles sur le [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1079">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="690d8-1080">Stabilité améliorée avec l’interopérabilité de Windows</span><span class="sxs-lookup"><span data-stu-id="690d8-1080">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="690d8-1081">Correction de l’erreur 0 x 80070057 lors du lancement bash.exe lorsque la Protection de données d’entreprise (EDP) est activée</span><span class="sxs-lookup"><span data-stu-id="690d8-1081">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="690d8-1082">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1082">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1083">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1083">LTP Results:</span></span>
<span data-ttu-id="690d8-1084">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="690d8-1084">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="690d8-1085">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1085">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1086">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1086">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="690d8-1087">Build 14955</span><span class="sxs-lookup"><span data-stu-id="690d8-1087">Build 14955</span></span>

<span data-ttu-id="690d8-1088">Pour Windows général plus d’informations sur la build 14955 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="690d8-1088">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1089">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1089">Fixed</span></span>

 - <span data-ttu-id="690d8-1090">En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-1090">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="690d8-1091">Mises à jour régulièrement planifiées reprendra à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="690d8-1091">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1092">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1092">LTP Results:</span></span>
<span data-ttu-id="690d8-1093">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="690d8-1093">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="690d8-1094">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1094">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1095">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1095">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="690d8-1096">Build 14951</span><span class="sxs-lookup"><span data-stu-id="690d8-1096">Build 14951</span></span>

<span data-ttu-id="690d8-1097">Pour Windows général plus d’informations sur la build 14951 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1097">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="690d8-1098">Nouvelle fonctionnalité : Windows / Ubuntu interopérabilité</span><span class="sxs-lookup"><span data-stu-id="690d8-1098">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="690d8-1099">Les fichiers binaires Windows peuvent maintenant être appelées directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1099">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="690d8-1100">Cela permet aux utilisateurs d’interagir avec leur environnement de Windows et le système d’une manière qui n’a pas été possible.</span><span class="sxs-lookup"><span data-stu-id="690d8-1100">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="690d8-1101">Exemple rapide, il est désormais possible pour les utilisateurs à exécuter les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="690d8-1101">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="690d8-1102">Vous trouverez plus d’informations sur :</span><span class="sxs-lookup"><span data-stu-id="690d8-1102">More information can be found at:</span></span>

- [<span data-ttu-id="690d8-1103">Blog de l’équipe WSL pour l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="690d8-1103">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="690d8-1104">Documentation Interop MSDN</span><span class="sxs-lookup"><span data-stu-id="690d8-1104">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1105">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1105">Fixed</span></span>

- <span data-ttu-id="690d8-1106">Ubuntu 16.04 (Xenial) est maintenant installé pour toutes les nouvelles instances WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1106">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="690d8-1107">Les utilisateurs avec des instances (fidèle) 14.04 existantes ne seront pas mis à niveau automatiquement.</span><span class="sxs-lookup"><span data-stu-id="690d8-1107">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="690d8-1108">Paramètres régionaux définis lors de l’installation sont maintenant affichée.</span><span class="sxs-lookup"><span data-stu-id="690d8-1108">Locale set during install is now displayed</span></span>
- <span data-ttu-id="690d8-1109">Améliorations de Terminal Server, y compris le bogue où rediriger un processus WSL vers un fichier ne pas toujours fonctionner</span><span class="sxs-lookup"><span data-stu-id="690d8-1109">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="690d8-1110">Durée de vie de console doit être liée à la durée de vie bash.exe</span><span class="sxs-lookup"><span data-stu-id="690d8-1110">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="690d8-1111">Taille de fenêtre de console doit utiliser la taille visible, taille de mémoire tampon pas</span><span class="sxs-lookup"><span data-stu-id="690d8-1111">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="690d8-1112">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1112">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1113">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1113">LTP Results:</span></span>
<span data-ttu-id="690d8-1114">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="690d8-1114">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="690d8-1115">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1115">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1116">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1116">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="690d8-1117">Build 14946</span><span class="sxs-lookup"><span data-stu-id="690d8-1117">Build 14946</span></span>

<span data-ttu-id="690d8-1118">Pour Windows général plus d’informations sur la build 14946 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="690d8-1118">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1119">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1119">Fixed</span></span>

- <span data-ttu-id="690d8-1120">Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT qui contiennent des espaces ou des guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="690d8-1120">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="690d8-1121">Modification VolFs et DrvFs pour retourner 0 pour le nombre de liens de l’annuaire dans stat</span><span class="sxs-lookup"><span data-stu-id="690d8-1121">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="690d8-1122">Prend en charge l’option de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="690d8-1122">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="690d8-1123">Limiter à une seule console boucle d’e/s par tty.</span><span class="sxs-lookup"><span data-stu-id="690d8-1123">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="690d8-1124">Exemple : la commande suivante est possible :</span><span class="sxs-lookup"><span data-stu-id="690d8-1124">Example: the following command is possible:</span></span>
  - <span data-ttu-id="690d8-1125">Bash -c « echo data » | Bash - c « ssh user@example.com ' cat > foo.txt » »</span><span class="sxs-lookup"><span data-stu-id="690d8-1125">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="690d8-1126">Remplacez les espaces par des tabulations dans /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="690d8-1126">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="690d8-1127">DrvFs apparaît désormais dans mountinfo avec un nom qui correspond au volume de Windows monté</span><span class="sxs-lookup"><span data-stu-id="690d8-1127">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="690d8-1128">/Home et/root apparaissent désormais dans mountinfo avec les noms corrects</span><span class="sxs-lookup"><span data-stu-id="690d8-1128">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="690d8-1129">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1129">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1130">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1130">LTP Results:</span></span>
<span data-ttu-id="690d8-1131">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="690d8-1131">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="690d8-1132">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1133">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="690d8-1134">Build 14942</span><span class="sxs-lookup"><span data-stu-id="690d8-1134">Build 14942</span></span>

<span data-ttu-id="690d8-1135">Pour Windows général plus d’informations sur la build 14942 visitez le [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="690d8-1135">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1136">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1136">Fixed</span></span>

- <span data-ttu-id="690d8-1137">Un nombre de bogues résolus, y compris la » a TENTÉ de s’exécuter de PasExécution ne peut être mémoire « incident qui a été blocage SSH de mise en réseau</span><span class="sxs-lookup"><span data-stu-id="690d8-1137">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="690d8-1138">inotifiy prise en charge pour les notifications générées à partir d’applications Windows sur DrvFs est présent dans</span><span class="sxs-lookup"><span data-stu-id="690d8-1138">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="690d8-1139">Implémenter TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod.</span><span class="sxs-lookup"><span data-stu-id="690d8-1139">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="690d8-1140">(#695 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-1140">(GH #695)</span></span>
- <span data-ttu-id="690d8-1141">Implémenter l’appel système pivot_root</span><span class="sxs-lookup"><span data-stu-id="690d8-1141">Implement the pivot_root system call</span></span>
- <span data-ttu-id="690d8-1142">Implémenter l’option de socket pour SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="690d8-1142">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="690d8-1143">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1143">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="690d8-1144">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1144">LTP Results:</span></span>
<span data-ttu-id="690d8-1145">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="690d8-1145">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="690d8-1146">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="690d8-1146">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="690d8-1147">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1147">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1148">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1148">Syscall Support</span></span>
<span data-ttu-id="690d8-1149">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1149">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1150">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1150">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="690d8-1151">Build 14936</span><span class="sxs-lookup"><span data-stu-id="690d8-1151">Build 14936</span></span>

<span data-ttu-id="690d8-1152">Pour Windows général plus d’informations sur la build 14936 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1152">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="690d8-1153">Remarque: WSL va installer Ubuntu version 16.04 (Xenial) au lieu d’Ubuntu 14.04 (fidèle) dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="690d8-1153">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="690d8-1154">Cette modification s’applique pour les Insiders installation de nouvelles instances (lxrun.exe /install ou première exécution de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="690d8-1154">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="690d8-1155">Les instances existantes avec fidèle ne seront pas mis à niveau automatiquement.</span><span class="sxs-lookup"><span data-stu-id="690d8-1155">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="690d8-1156">Les utilisateurs peuvent mettre à niveau leur image fidèle à Xenial à l’aide de la commande-version-mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="690d8-1156">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="690d8-1157">Problème connu</span><span class="sxs-lookup"><span data-stu-id="690d8-1157">Known Issue</span></span>
<span data-ttu-id="690d8-1158">WSL rencontre un problème avec certaines implémentations de socket.</span><span class="sxs-lookup"><span data-stu-id="690d8-1158">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="690d8-1159">La vérification d’erreur se manifeste comme un incident avec l’erreur « A TENTÉ de s’exécuter de PasExécution ne peut être mémoire ».</span><span class="sxs-lookup"><span data-stu-id="690d8-1159">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="690d8-1160">La manifestation la plus commune de ce problème est un incident lors de l’utilisation de ssh.</span><span class="sxs-lookup"><span data-stu-id="690d8-1160">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="690d8-1161">La cause racine est fixe sur des versions internes et n’est adressée aux initiés dès que possible.</span><span class="sxs-lookup"><span data-stu-id="690d8-1161">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="690d8-1162">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1162">Fixed</span></span>

- <span data-ttu-id="690d8-1163">Implémentation de l’appel système chroot</span><span class="sxs-lookup"><span data-stu-id="690d8-1163">Implemented the chroot system call</span></span>
- <span data-ttu-id="690d8-1164">Améliorations dans inotify ~~, y compris la prise en charge pour les notifications générées à partir d’applications Windows sur DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="690d8-1164">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="690d8-1165">Correction : Inotify prend en charge les modifications provenant d’applications Windows non disponibles pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1165">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="690d8-1166">Liaison à IPV6 de socket ::<port n> prend désormais en charge IPV6_V6ONLY (GH #68 #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="690d8-1166">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="690d8-1167">Comportement WNOWAIT pour waitid systemcall implémenté (GH #638)</span><span class="sxs-lookup"><span data-stu-id="690d8-1167">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="690d8-1168">Prise en charge des options de socket IP IP_HDRINCL et IP_TTL</span><span class="sxs-lookup"><span data-stu-id="690d8-1168">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="690d8-1169">Read() de longueur nulle doit retourner immédiatement (GH #975)</span><span class="sxs-lookup"><span data-stu-id="690d8-1169">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="690d8-1170">Gérer correctement les préfixes des noms de fichiers et le nom de fichier qui n’incluent pas une marque de fin NULL dans un fichier .tar.</span><span class="sxs-lookup"><span data-stu-id="690d8-1170">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="690d8-1171">prise en charge d’epoll de/dev/null</span><span class="sxs-lookup"><span data-stu-id="690d8-1171">epoll support for /dev/null</span></span>
- <span data-ttu-id="690d8-1172">Corriger la source de temps /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="690d8-1172">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="690d8-1173">Bash -c maintenant en mesure de rediriger vers un fichier</span><span class="sxs-lookup"><span data-stu-id="690d8-1173">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="690d8-1174">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1174">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1175">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1175">LTP Results:</span></span>
<span data-ttu-id="690d8-1176">Nombre de Test réussi : 664</span><span class="sxs-lookup"><span data-stu-id="690d8-1176">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="690d8-1177">Nombre de cas d’échec (échec, ignoré, etc....) : 264</span><span class="sxs-lookup"><span data-stu-id="690d8-1177">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="690d8-1178">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1178">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1179">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1179">Syscall Support</span></span>
<span data-ttu-id="690d8-1180">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1180">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1181">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1181">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="690d8-1182">Build 14931</span><span class="sxs-lookup"><span data-stu-id="690d8-1182">Build 14931</span></span>

<span data-ttu-id="690d8-1183">Pour Windows général plus d’informations sur la build 14931 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1183">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1184">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1184">Fixed</span></span>

 - <span data-ttu-id="690d8-1185">En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-1185">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="690d8-1186">Mises à jour régulièrement planifiées reprendra dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="690d8-1186">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="690d8-1187">Build 14926</span><span class="sxs-lookup"><span data-stu-id="690d8-1187">Build 14926</span></span>

<span data-ttu-id="690d8-1188">Pour Windows général plus d’informations sur la build 14926 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1188">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1189">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1189">Fixed</span></span>

- <span data-ttu-id="690d8-1190">Ping fonctionne désormais dans les consoles qui n’ont pas de privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="690d8-1190">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="690d8-1191">Ping6 maintenant également pris en charge, sans privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="690d8-1191">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="690d8-1192">Inotify prise en charge pour les fichiers modifiés via WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1192">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="690d8-1193">(#216 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-1193">(GH #216)</span></span>
  - <span data-ttu-id="690d8-1194">Indicateurs pris en charge :</span><span class="sxs-lookup"><span data-stu-id="690d8-1194">Flags supported:</span></span>
    - <span data-ttu-id="690d8-1195">inotify_init1 : LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="690d8-1195">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="690d8-1196">événements d’inotify_add_watch : LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="690d8-1196">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="690d8-1197">attributs d’inotify_add_watch : LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="690d8-1197">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="690d8-1198">lire la sortie : LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="690d8-1198">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="690d8-1199">Problème connu : Modification des fichiers à partir d’applications de Windows ne génère pas d’événements</span><span class="sxs-lookup"><span data-stu-id="690d8-1199">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="690d8-1200">Socket UNIX prend désormais en charge SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="690d8-1200">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="690d8-1201">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="690d8-1201">LTP Results:</span></span>
<span data-ttu-id="690d8-1202">Nombre de Test réussi : 651</span><span class="sxs-lookup"><span data-stu-id="690d8-1202">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="690d8-1203">Nombre de cas d’échec (échec, ignoré, etc....) : 258</span><span class="sxs-lookup"><span data-stu-id="690d8-1203">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="690d8-1204">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="690d8-1204">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="690d8-1205">Build 14915</span><span class="sxs-lookup"><span data-stu-id="690d8-1205">Build 14915</span></span>

<span data-ttu-id="690d8-1206">Pour Windows général plus d’informations sur la build 14915 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="690d8-1206">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1207">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1207">Fixed</span></span>
-  <span data-ttu-id="690d8-1208">Socketpair pour les sockets datagramme unix (GH #262)</span><span class="sxs-lookup"><span data-stu-id="690d8-1208">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="690d8-1209">Prise en charge de socket UNIX pour SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="690d8-1209">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="690d8-1210">Prise en charge de socket UNIX pour SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="690d8-1210">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="690d8-1211">Prise en charge de socket UNIX pour SOCK_SEQPACKET (758 GH #, #546)</span><span class="sxs-lookup"><span data-stu-id="690d8-1211">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="690d8-1212">Ajout de prise en charge pour l’envoi de socket datagramme unix, reçues et d’arrêt</span><span class="sxs-lookup"><span data-stu-id="690d8-1212">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="690d8-1213">Corriger la vérification d’erreur en raison de la validation de paramètre mmap non valide pour les adresses non fixe.</span><span class="sxs-lookup"><span data-stu-id="690d8-1213">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="690d8-1214">(#847 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-1214">(GH #847)</span></span>
- <span data-ttu-id="690d8-1215">Prise en charge pour interrompre / reprendre des États de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="690d8-1215">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="690d8-1216">Prise en charge d’ioctl TIOCPKT débloquer l’utilitaire d’écran (GH #774)</span><span class="sxs-lookup"><span data-stu-id="690d8-1216">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="690d8-1217">Problème connu : Touches de fonction non opérationnels</span><span class="sxs-lookup"><span data-stu-id="690d8-1217">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="690d8-1218">Correction d’une concurrence dans TimerFd qui peut entraîner un membre libéré 'ReaderReady' accessible par LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="690d8-1218">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="690d8-1219">Activer le support d’appel système pouvant être redémarrées pour futex, interrogation et clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="690d8-1219">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="690d8-1220">Prise en charge du montage de liaison ajouté</span><span class="sxs-lookup"><span data-stu-id="690d8-1220">Added bind mount support</span></span>
- <span data-ttu-id="690d8-1221">Annuler le partage pour la prise en charge de l’espace de noms de montage</span><span class="sxs-lookup"><span data-stu-id="690d8-1221">unshare for mount namespace support</span></span>
    - <span data-ttu-id="690d8-1222">Problème connu : Lorsque vous créez un nouvel espace de noms de montage avec `unshare(CLONE_NEWNS)` le répertoire de travail continue à pointer vers l’ancien espace de noms</span><span class="sxs-lookup"><span data-stu-id="690d8-1222">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="690d8-1223">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="690d8-1223">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="690d8-1224">Build 14905</span><span class="sxs-lookup"><span data-stu-id="690d8-1224">Build 14905</span></span>

<span data-ttu-id="690d8-1225">Pour Windows général plus d’informations sur la build 14905 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1225">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1226">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1226">Fixed</span></span>
- <span data-ttu-id="690d8-1227">Système redémarrable appels sont désormais pris en charge (GH #349 GH #520)</span><span class="sxs-lookup"><span data-stu-id="690d8-1227">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="690d8-1228">Liens symboliques vers des répertoires de fin dans / maintenant opérationnelle (GH #650)</span><span class="sxs-lookup"><span data-stu-id="690d8-1228">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="690d8-1229">Implémenté RNDGETENTCNT ioctl pour/dev/Random</span><span class="sxs-lookup"><span data-stu-id="690d8-1229">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="690d8-1230">Implémenté le/proc / [pid] / monte, / proc / [pid] / mountinfo et/proc / [pid] / mountstats fichiers</span><span class="sxs-lookup"><span data-stu-id="690d8-1230">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="690d8-1231">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1231">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="690d8-1232">Build 14901</span><span class="sxs-lookup"><span data-stu-id="690d8-1232">Build 14901</span></span>
<span data-ttu-id="690d8-1233">Première Insider générer pour la publication de mise à jour anniversaire de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="690d8-1233">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="690d8-1234">Pour Windows général plus d’informations sur la build 14901 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1234">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1235">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1235">Fixed</span></span>
- <span data-ttu-id="690d8-1236">Problème de barre oblique de fin fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1236">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="690d8-1237">Commandes telles que `$ mv a/c/ a/b/` fonctionne maintenant</span><span class="sxs-lookup"><span data-stu-id="690d8-1237">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="690d8-1238">Installation invite désormais l’utilisateur si les paramètres régionaux Ubuntu doivent être défini sur les paramètres régionaux Windows</span><span class="sxs-lookup"><span data-stu-id="690d8-1238">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="690d8-1239">Commande procfs prise en charge pour le dossier de ns</span><span class="sxs-lookup"><span data-stu-id="690d8-1239">Procfs support for ns folder</span></span>
- <span data-ttu-id="690d8-1240">Ajouté le montage et démontage pour tmpfs, commande procfs et systèmes de fichiers sysfs</span><span class="sxs-lookup"><span data-stu-id="690d8-1240">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="690d8-1241">Corriger mknod [at] signature ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="690d8-1241">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="690d8-1242">Sockets UNIX déplacés pour distribuer le modèle</span><span class="sxs-lookup"><span data-stu-id="690d8-1242">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="690d8-1243">Taille de mémoire tampon INET socket recv défini à l’aide de la setsockopt doit être respecté.</span><span class="sxs-lookup"><span data-stu-id="690d8-1243">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="690d8-1244">Indicateur de message de réception de socket MSG_CMSG_CLOEXEC unix implémenter</span><span class="sxs-lookup"><span data-stu-id="690d8-1244">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="690d8-1245">Redirection de canal de stdin/stdout de processus Linux (GH #2)</span><span class="sxs-lookup"><span data-stu-id="690d8-1245">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="690d8-1246">Permet de combinaison de l’interpréteur de commandes - c dans cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="690d8-1246">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="690d8-1247">Exemple : > dir | Bash -c « foo grep »</span><span class="sxs-lookup"><span data-stu-id="690d8-1247">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="690d8-1248">Bash peut désormais être installée sur les systèmes avec plusieurs fichiers d’échange (538 GH #, #358)</span><span class="sxs-lookup"><span data-stu-id="690d8-1248">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="690d8-1249">Taille de mémoire tampon par défaut INET Socket doit correspondre à celle de l’installation d’Ubuntu par défaut</span><span class="sxs-lookup"><span data-stu-id="690d8-1249">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="690d8-1250">Aligner syscalls xattr à listxattr</span><span class="sxs-lookup"><span data-stu-id="690d8-1250">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="690d8-1251">Retourner uniquement les interfaces avec une adresse IPv4 valide provenant de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="690d8-1251">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="690d8-1252">Corriger l’action par défaut de signal lorsque injecté par ptrace</span><span class="sxs-lookup"><span data-stu-id="690d8-1252">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="690d8-1253">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="690d8-1253">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="690d8-1254">Utilisez les valeurs de registres de contexte ordinateur lors de la restauration du contexte dans sigreturn</span><span class="sxs-lookup"><span data-stu-id="690d8-1254">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="690d8-1255">Cela résout le problème où java et javac ont été mise en suspens pour certains utilisateurs</span><span class="sxs-lookup"><span data-stu-id="690d8-1255">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="690d8-1256">Implémenter /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="690d8-1256">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1257">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1257">Syscall Support</span></span>
<span data-ttu-id="690d8-1258">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1258">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1259">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1259">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="690d8-1260">Build 14388 à la mise à jour anniversaire Windows 10</span><span class="sxs-lookup"><span data-stu-id="690d8-1260">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="690d8-1261">Pour Windows général plus d’informations sur la build 14388 visitez le [Windows Blog](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="690d8-1261">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1262">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1262">Fixed</span></span>
- <span data-ttu-id="690d8-1263">Correctifs pour vous préparer à la mise à jour anniversaire de Windows 10 sur 8/2</span><span class="sxs-lookup"><span data-stu-id="690d8-1263">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="690d8-1264">Vous trouverez plus d’informations sur WSL dans la mise à jour anniversaire sur notre [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="690d8-1264">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="690d8-1265">Build 14376</span><span class="sxs-lookup"><span data-stu-id="690d8-1265">Build 14376</span></span>
<span data-ttu-id="690d8-1266">Pour Windows général plus d’informations sur la build 14376 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1266">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1267">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1267">Fixed</span></span>
- <span data-ttu-id="690d8-1268">Supprimé certaines instances où apt-get bloque (GH #493)</span><span class="sxs-lookup"><span data-stu-id="690d8-1268">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="690d8-1269">Correction d’un problème où les montages vides n’étaient pas gérées correctement</span><span class="sxs-lookup"><span data-stu-id="690d8-1269">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="690d8-1270">Correction d’un problème où ramdisks n’étaient pas monté correctement</span><span class="sxs-lookup"><span data-stu-id="690d8-1270">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="690d8-1271">Acceptation du socket d’unix de modification pour prendre en charge les indicateurs (partielle GH #451)</span><span class="sxs-lookup"><span data-stu-id="690d8-1271">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="690d8-1272">Réseau commun fixe liés écran bleu</span><span class="sxs-lookup"><span data-stu-id="690d8-1272">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="690d8-1273">Correction d’écran bleu lorsque vous accédez à/proc / [pid] / tâches (GH #523)</span><span class="sxs-lookup"><span data-stu-id="690d8-1273">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="690d8-1274">Fixe utilisation élevée du processeur pour des scénarios de pty (488 GH #, #504)</span><span class="sxs-lookup"><span data-stu-id="690d8-1274">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="690d8-1275">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1275">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="690d8-1276">Build 14371</span><span class="sxs-lookup"><span data-stu-id="690d8-1276">Build 14371</span></span>
<span data-ttu-id="690d8-1277">Pour Windows général plus d’informations sur la build 14371 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1277">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1278">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1278">Fixed</span></span>
- <span data-ttu-id="690d8-1279">Corrigé concurrence de minutage avec SIGCHLD et wait() lors de l’utilisation de ptrace</span><span class="sxs-lookup"><span data-stu-id="690d8-1279">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="690d8-1280">Correction d’un comportement lorsque les chemins d’accès ont une fin / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="690d8-1280">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="690d8-1281">Résolution du problème de changement de nom/dissocier des échouent en raison de descripteurs ouverts pour enfants</span><span class="sxs-lookup"><span data-stu-id="690d8-1281">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="690d8-1282">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1282">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="690d8-1283">Build 14366</span><span class="sxs-lookup"><span data-stu-id="690d8-1283">Build 14366</span></span>
<span data-ttu-id="690d8-1284">Pour Windows général plus d’informations sur la build 14366 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="690d8-1284">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1285">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1285">Fixed</span></span>
- <span data-ttu-id="690d8-1286">Corriger dans la création de fichiers via les liens symboliques</span><span class="sxs-lookup"><span data-stu-id="690d8-1286">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="690d8-1287">Ajout de listxattr pour Python (385 Hg)</span><span class="sxs-lookup"><span data-stu-id="690d8-1287">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="690d8-1288">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1288">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1289">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1289">Syscall Support</span></span>
-   <span data-ttu-id="690d8-1290">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1290">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1291">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1291">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="690d8-1292">Build 14361</span><span class="sxs-lookup"><span data-stu-id="690d8-1292">Build 14361</span></span>
<span data-ttu-id="690d8-1293">Pour Windows général plus d’informations sur la build 14361 visitez le [Windows Blog](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="690d8-1293">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1294">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1294">Fixed</span></span>
- <span data-ttu-id="690d8-1295">DrvFs est désormais sensible à la casse lors de l’exécution dans Bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-1295">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="690d8-1296">Les utilisateurs mai case.txt et cas. TXT sur leur c/mnt/lecteurs</span><span class="sxs-lookup"><span data-stu-id="690d8-1296">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="690d8-1297">Respecte la casse est uniquement pris en charge dans Bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-1297">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="690d8-1298">Lorsque l’extérieur de NTFS Bash signale correctement les fichiers, mais un comportement inattendu peut se produire à interagir avec les fichiers à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="690d8-1298">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="690d8-1299">La racine de chaque volume (c'est-à-dire /mnt/c) n’est pas sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="690d8-1299">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="690d8-1300">Vous pouvez trouver plus d’informations sur la gestion des ces fichiers dans Windows [ici](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="690d8-1300">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="690d8-1301">Considérablement améliorée pty / tty prend en charge.</span><span class="sxs-lookup"><span data-stu-id="690d8-1301">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="690d8-1302">Les applications telles que TMUX désormais pris en charge que (# GH 40)</span><span class="sxs-lookup"><span data-stu-id="690d8-1302">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="690d8-1303">Problème d’installation fixe où les comptes d’utilisateurs créés pas toujours</span><span class="sxs-lookup"><span data-stu-id="690d8-1303">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="690d8-1304">Optimisé structure arg de ligne de commande permettant de liste d’arguments de très longs.</span><span class="sxs-lookup"><span data-stu-id="690d8-1304">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="690d8-1305">(#153 HG)</span><span class="sxs-lookup"><span data-stu-id="690d8-1305">(GH #153)</span></span>
- <span data-ttu-id="690d8-1306">Maintenant en mesure de supprimer et chmod read_only les fichiers à partir de DrvFs</span><span class="sxs-lookup"><span data-stu-id="690d8-1306">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="690d8-1307">Correction de certaines instances où les blocages de terminal sur Déconnecter (GH #43)</span><span class="sxs-lookup"><span data-stu-id="690d8-1307">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="690d8-1308">chmod et chown fonctionnent désormais sur les appareils tty</span><span class="sxs-lookup"><span data-stu-id="690d8-1308">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="690d8-1309">Autoriser la connexion à 0.0.0.0 et :: en tant que localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="690d8-1309">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="690d8-1310">Sendmsg/recvmsg gèrent maintenant une longueur de vecteur d’e/s de > 1 (partielle GH #376)</span><span class="sxs-lookup"><span data-stu-id="690d8-1310">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="690d8-1311">Les utilisateurs peuvent désormais annulations du fichier généré automatiquement les ordinateurs hôtes (GH #398)</span><span class="sxs-lookup"><span data-stu-id="690d8-1311">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="690d8-1312">Automatiquement en correspondance les paramètres régionaux de Linux pour les paramètres régionaux NT lors de l’installation (GH #11)</span><span class="sxs-lookup"><span data-stu-id="690d8-1312">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="690d8-1313">Ajouté le fichier /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="690d8-1313">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="690d8-1314">strace se ferme désormais correctement</span><span class="sxs-lookup"><span data-stu-id="690d8-1314">strace now exits correctly</span></span>
- <span data-ttu-id="690d8-1315">Autoriser les canaux être rouverte via /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="690d8-1315">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="690d8-1316">Masquer les répertoires sous %LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="690d8-1316">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="690d8-1317">Meilleure gestion des bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="690d8-1317">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="690d8-1318">Commandes telles que « bash ~ ls - c » désormais pris en charge (GH #467)</span><span class="sxs-lookup"><span data-stu-id="690d8-1318">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="690d8-1319">Sockets notifient maintenant epoll en lecture disponible lors de l’arrêt (GH #271)</span><span class="sxs-lookup"><span data-stu-id="690d8-1319">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="690d8-1320">lxrun / désinstallation est plus efficace de la suppression des fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="690d8-1320">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="690d8-1321">Corrigé ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="690d8-1321">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="690d8-1322">X11 prise en charge améliorée des applications telles que xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="690d8-1322">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="690d8-1323">Mise à jour de la taille de pile de thread initial au paramètre d’Ubuntu par défaut et de signalement de la taille correctement à la syscall get_rlimit (172 GH #, #258)</span><span class="sxs-lookup"><span data-stu-id="690d8-1323">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="690d8-1324">Amélioration des rapports pico image noms de processus (par exemple, pour l’audit)</span><span class="sxs-lookup"><span data-stu-id="690d8-1324">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="690d8-1325">/Proc/mountinfo implémentée pour la commande df</span><span class="sxs-lookup"><span data-stu-id="690d8-1325">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="690d8-1326">Code d’erreur de lien symbolique fixe pour le nom de l’enfant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1326">Fixed symlink error code for child name .</span></span> <span data-ttu-id="690d8-1327">et...</span><span class="sxs-lookup"><span data-stu-id="690d8-1327">and ..</span></span>
- <span data-ttu-id="690d8-1328">Améliorations et correctifs de bogues des améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1328">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1329">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1329">Syscall Support</span></span>
<span data-ttu-id="690d8-1330">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1330">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1331">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1331">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="690d8-1332">Build 14352</span><span class="sxs-lookup"><span data-stu-id="690d8-1332">Build 14352</span></span>
<span data-ttu-id="690d8-1333">Pour Windows général plus d’informations sur la build 14352 visitez le [Windows Blog](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="690d8-1333">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1334">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1334">Fixed</span></span>
- <span data-ttu-id="690d8-1335">Correction d’un problème où des fichiers volumineux ont été téléchargés non / créées correctement.</span><span class="sxs-lookup"><span data-stu-id="690d8-1335">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="690d8-1336">Cela doit débloquer npm et autres scénarios (GH n ° 3, Hg #313)</span><span class="sxs-lookup"><span data-stu-id="690d8-1336">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="690d8-1337">Supprimé certaines instances où sockets de blocage</span><span class="sxs-lookup"><span data-stu-id="690d8-1337">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="690d8-1338">Correction des erreurs ptrace</span><span class="sxs-lookup"><span data-stu-id="690d8-1338">Corrected some ptrace errors</span></span>
- <span data-ttu-id="690d8-1339">Correction d’un problème avec WSL autorisant les noms de fichiers plus de 255 caractères</span><span class="sxs-lookup"><span data-stu-id="690d8-1339">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="690d8-1340">Prise en charge améliorée pour les caractères non anglais</span><span class="sxs-lookup"><span data-stu-id="690d8-1340">Improved support for non-English characters</span></span>
- <span data-ttu-id="690d8-1341">Ajoutez des données de fuseau horaire Windows actuelles et définissez comme valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="690d8-1341">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="690d8-1342">D’id appareil unique pour chaque point de montage (correctif jre – GH #49)</span><span class="sxs-lookup"><span data-stu-id="690d8-1342">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="690d8-1343">Corriger le problème avec les chemins d’accès contenant «. »</span><span class="sxs-lookup"><span data-stu-id="690d8-1343">Correct issue with paths containing “.”</span></span> <span data-ttu-id="690d8-1344">et «... »</span><span class="sxs-lookup"><span data-stu-id="690d8-1344">and “..”</span></span>
- <span data-ttu-id="690d8-1345">Prise en charge Fifo (GH #71)</span><span class="sxs-lookup"><span data-stu-id="690d8-1345">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="690d8-1346">Format mis à jour de resolv.conf pour faire correspondre le format natif Ubuntu</span><span class="sxs-lookup"><span data-stu-id="690d8-1346">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="690d8-1347">Un nettoyage des commande procfs</span><span class="sxs-lookup"><span data-stu-id="690d8-1347">Some procfs cleanup</span></span>
- <span data-ttu-id="690d8-1348">Ping activé pour les consoles administrateur (GH #18)</span><span class="sxs-lookup"><span data-stu-id="690d8-1348">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1349">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1349">Syscall Support</span></span>
<span data-ttu-id="690d8-1350">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1351">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="690d8-1352">Build 14342</span><span class="sxs-lookup"><span data-stu-id="690d8-1352">Build 14342</span></span>
<span data-ttu-id="690d8-1353">Pour Windows général plus d’informations sur build 14342 le [Windows Blog](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="690d8-1353">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="690d8-1354">Vous trouverez plus d’informations sur VolFs et DriveFs sur le [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="690d8-1354">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="690d8-1355">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1355">Fixed</span></span>
- <span data-ttu-id="690d8-1356">Résolu le problème d’installation lorsque l’utilisateur Windows avait des caractères Unicode dans le nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="690d8-1356">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="690d8-1357">La solution de contournement udev apt-get update dans le Forum aux questions est désormais fournie par défaut sur la première exécution</span><span class="sxs-lookup"><span data-stu-id="690d8-1357">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="690d8-1358">Activé des liens symboliques dans DriveFs (/mnt/<drive>) répertoires</span><span class="sxs-lookup"><span data-stu-id="690d8-1358">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="690d8-1359">Fonctionnent désormais de liens symboliques entre DriveFs et VolFs</span><span class="sxs-lookup"><span data-stu-id="690d8-1359">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="690d8-1360">Adressée supérieur au niveau chemin d’accès de l’analyse du problème : %.\*ls. / / fonctionne désormais comme prévu</span><span class="sxs-lookup"><span data-stu-id="690d8-1360">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="690d8-1361">npm installez-y DriveFs et les options -g sont maintenant opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="690d8-1361">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="690d8-1362">Correction d’un problème empêchant le lancement de serveur PHP</span><span class="sxs-lookup"><span data-stu-id="690d8-1362">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="690d8-1363">Valeurs d’environnement par défaut de mise à jour, telles que $PATH pour rapprocher correspond à Ubuntu natif</span><span class="sxs-lookup"><span data-stu-id="690d8-1363">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="690d8-1364">Ajouter une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache du package apt</span><span class="sxs-lookup"><span data-stu-id="690d8-1364">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="690d8-1365">Correction du problème avec la validation de l’en-tête ELF, WSL prend désormais en charge toutes les options de Melkor</span><span class="sxs-lookup"><span data-stu-id="690d8-1365">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="690d8-1366">Interpréteur de commandes Zsh est fonctionnel</span><span class="sxs-lookup"><span data-stu-id="690d8-1366">Zsh shell is functional</span></span>
- <span data-ttu-id="690d8-1367">Les binaires précompilés Go sont donc compatibles</span><span class="sxs-lookup"><span data-stu-id="690d8-1367">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="690d8-1368">Inviter sur Bash.exe tout d’abord exécuter est maintenant correctement localisé</span><span class="sxs-lookup"><span data-stu-id="690d8-1368">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="690d8-1369">/proc/meminfo retourne désormais des informations correctes</span><span class="sxs-lookup"><span data-stu-id="690d8-1369">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="690d8-1370">Sockets désormais pris en charge dans le système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="690d8-1370">Sockets now supported in VFS</span></span>
- <span data-ttu-id="690d8-1371">/dev maintenant monté en tant que tempfs</span><span class="sxs-lookup"><span data-stu-id="690d8-1371">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="690d8-1372">FIFO désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="690d8-1372">Fifo now supported</span></span>
- <span data-ttu-id="690d8-1373">Des systèmes multicœurs montre maintenant correctement dans cpuinfo/proc /</span><span class="sxs-lookup"><span data-stu-id="690d8-1373">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="690d8-1374">Améliorations supplémentaires et des messages d’erreur téléchargé au cours de la première exécution</span><span class="sxs-lookup"><span data-stu-id="690d8-1374">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="690d8-1375">Syscall améliorations et correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="690d8-1375">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="690d8-1376">Syscall pris en charge de la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="690d8-1376">Supported syscall list below.</span></span>
- <span data-ttu-id="690d8-1377">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1377">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="690d8-1378">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="690d8-1378">Known Issues</span></span>
- <span data-ttu-id="690d8-1379">Ne pas de résolution '..'</span><span class="sxs-lookup"><span data-stu-id="690d8-1379">Not resolving ‘..’</span></span> <span data-ttu-id="690d8-1380">correctement sur DriveFs dans certains cas</span><span class="sxs-lookup"><span data-stu-id="690d8-1380">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1381">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1381">Syscall Support</span></span>
<span data-ttu-id="690d8-1382">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1382">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="690d8-1383">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1383">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="690d8-1384">Build 14332</span><span class="sxs-lookup"><span data-stu-id="690d8-1384">Build 14332</span></span>

<span data-ttu-id="690d8-1385">Pour Windows général plus d’informations sur la build 14332 visitez le [Windows Blog](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="690d8-1385">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="690d8-1386">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1386">Fixed</span></span>
- <span data-ttu-id="690d8-1387">Meilleure génération resolv.conf, y compris la hiérarchisation des entrées DNS</span><span class="sxs-lookup"><span data-stu-id="690d8-1387">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="690d8-1388">Problème avec le déplacement de fichiers et répertoires entre mnt et non- / mnt lecteurs</span><span class="sxs-lookup"><span data-stu-id="690d8-1388">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="690d8-1389">Fichiers .tar peuvent maintenant être créés avec des liens symboliques</span><span class="sxs-lookup"><span data-stu-id="690d8-1389">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="690d8-1390">Répertoire de /run/lock par défaut ajoutés lors de la création d’instance</span><span class="sxs-lookup"><span data-stu-id="690d8-1390">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="690d8-1391">Mise à jour/dev/null pour retourner des informations statistiques appropriées</span><span class="sxs-lookup"><span data-stu-id="690d8-1391">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="690d8-1392">Autres erreurs lors du téléchargement lors du premier démarrage</span><span class="sxs-lookup"><span data-stu-id="690d8-1392">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="690d8-1393">Syscall améliorations et correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="690d8-1393">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="690d8-1394">Syscall pris en charge de la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="690d8-1394">Supported syscall list below.</span></span>
- <span data-ttu-id="690d8-1395">Améliorations et correctifs de bogues des améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1395">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1396">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1396">Syscall Support</span></span>
<span data-ttu-id="690d8-1397">Voici la nouvelle syscall qui a déjà une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1397">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="690d8-1398">La syscall sur cette liste est pris en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1398">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="690d8-1399">Build 14328</span><span class="sxs-lookup"><span data-stu-id="690d8-1399">Build 14328</span></span>

<span data-ttu-id="690d8-1400">Pour Windows général plus d’informations sur la build 14332 visitez le [Windows Blog](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="690d8-1400">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="690d8-1401">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="690d8-1401">New Features</span></span>
* <span data-ttu-id="690d8-1402">Prennent désormais en charge les utilisateurs de Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-1402">Now support Linux users.</span></span>  <span data-ttu-id="690d8-1403">L’installation de Bash sur Ubuntu sur Windows vous demande de la création d’un utilisateur Linux.</span><span class="sxs-lookup"><span data-stu-id="690d8-1403">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="690d8-1404">Pour plus d’informations, visitez https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="690d8-1404">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="690d8-1405">Nom d’hôte est maintenant défini pour le nom d’ordinateur Windows, pas plus @localhost</span><span class="sxs-lookup"><span data-stu-id="690d8-1405">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="690d8-1406">Pour plus d’informations sur build 14328, visitez : https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="690d8-1406">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="690d8-1407">Fixe</span><span class="sxs-lookup"><span data-stu-id="690d8-1407">Fixed</span></span>
* <span data-ttu-id="690d8-1408">Améliorations de lien symbolique pour /mnt/ non<drive> fichiers</span><span class="sxs-lookup"><span data-stu-id="690d8-1408">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="690d8-1409">npm installation fonctionne désormais correctement</span><span class="sxs-lookup"><span data-stu-id="690d8-1409">npm install now works</span></span>
    * <span data-ttu-id="690d8-1410">JDK / jre installable maintenant à l’aide des instructions trouvées [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="690d8-1410">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="690d8-1411">problème connu : liens symboliques ne fonctionnent pas pour Windows monte.</span><span class="sxs-lookup"><span data-stu-id="690d8-1411">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="690d8-1412">Fonctionnalité sera disponible dans une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="690d8-1412">Functionality will be available in a later build</span></span>
* <span data-ttu-id="690d8-1413">haut et htop affichent désormais</span><span class="sxs-lookup"><span data-stu-id="690d8-1413">top and htop now display</span></span>
* <span data-ttu-id="690d8-1414">Messages d’erreur supplémentaires pour certains échecs de l’installation</span><span class="sxs-lookup"><span data-stu-id="690d8-1414">Additional error messages for some install failures</span></span>
* <span data-ttu-id="690d8-1415">Syscall améliorations et correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="690d8-1415">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="690d8-1416">Syscall pris en charge de la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="690d8-1416">Supported syscall list below.</span></span>
* <span data-ttu-id="690d8-1417">Améliorations et correctifs de bogues des améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="690d8-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="690d8-1418">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="690d8-1418">Syscall Support</span></span>
<span data-ttu-id="690d8-1419">Voici une liste d’appels qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="690d8-1419">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="690d8-1420">Syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="690d8-1420">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
