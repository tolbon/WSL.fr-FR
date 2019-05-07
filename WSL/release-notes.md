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
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="ad6f9-105">Notes de version de sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="ad6f9-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18890"></a><span data-ttu-id="ad6f9-106">Build 18890</span><span class="sxs-lookup"><span data-stu-id="ad6f9-106">Build 18890</span></span>
<span data-ttu-id="ad6f9-107">Pour Windows général plus d’informations sur la build 18890 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-107">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-108">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-108">WSL</span></span>
* <span data-ttu-id="ad6f9-109">Fuite de socket non bloquant [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-109">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="ad6f9-110">Entrée EOF à Terminal Server peut bloquer les lectures suivantes [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-110">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="ad6f9-111">Mettre à jour resolv.conf en-tête pour faire référence à wsl.conf [abordées dans GH 3928]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-111">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="ad6f9-112">Interblocage dans du code de suppression epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-112">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="ad6f9-113">Gérer les espaces dans les arguments à--importer et – exporter [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-113">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="ad6f9-114">Extension mmap des fichiers ne fonctionne pas correctement [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-114">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="ad6f9-115">Résoudre un problème avec ARM64 \\accès de $ wsl ne fonctionne ne pas correctement</span><span class="sxs-lookup"><span data-stu-id="ad6f9-115">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="ad6f9-116">Ajouter une meilleure icône par défaut pour wsl.exe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-116">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="ad6f9-117">Build 18342</span><span class="sxs-lookup"><span data-stu-id="ad6f9-117">Build 18342</span></span>
<span data-ttu-id="ad6f9-118">Pour Windows général plus d’informations sur la build 18342 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-118">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-119">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-119">WSL</span></span>
* <span data-ttu-id="ad6f9-120">Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans une distribution WSL à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-120">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="ad6f9-121">Ces fichiers sont accessibles via la ligne de commande et également des applications Windows, comme l’Explorateur de fichiers, VSCode, etc. peuvent interagir avec ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-121">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="ad6f9-122">Accéder à vos fichiers en accédant à \\ \\wsl$\\< distro_name >, ou afficher la liste des distributions en cours d’exécution en accédant à \\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="ad6f9-122">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="ad6f9-123">Ajouter des balises d’informations supplémentaires du processeur et de corriger les valeurs de Cpus_allowed [_liste] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-123">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="ad6f9-124">Prend en charge exec de thread non leader [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-124">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="ad6f9-125">Traiter les échecs de mise à jour de configuration comme non irrécupérable [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-125">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="ad6f9-126">Mettre à jour binfmt pour gérer correctement les décalages [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-126">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="ad6f9-127">Activer le mappage des lecteurs réseau pour planifier 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-127">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="ad6f9-128">Prise en charge Windows -> Linux et Linux -> traduction de chemin d’accès Windows pour les montages de liaisons</span><span class="sxs-lookup"><span data-stu-id="ad6f9-128">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="ad6f9-129">Créer des sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule</span><span class="sxs-lookup"><span data-stu-id="ad6f9-129">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="ad6f9-130">Build 18334</span><span class="sxs-lookup"><span data-stu-id="ad6f9-130">Build 18334</span></span>
<span data-ttu-id="ad6f9-131">Pour Windows général plus d’informations sur la build 18334 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-131">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-132">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-132">WSL</span></span>
* <span data-ttu-id="ad6f9-133">Redéfinir la façon que le fuseau horaire de Windows est mappé à un fuseau horaire de Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-133">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="ad6f9-134">Corriger les fuites de mémoire et ajouter de nouvelles fonctions de traduction de chaîne [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-134">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="ad6f9-135">SIGCONT sur un threadgroup avec aucun thread n’est une absence d’opération [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-135">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="ad6f9-136">Afficher correctement les descripteurs de fichier socket et epoll /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="ad6f9-136">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="ad6f9-137">Build 18305</span><span class="sxs-lookup"><span data-stu-id="ad6f9-137">Build 18305</span></span>
<span data-ttu-id="ad6f9-138">Pour Windows général plus d’informations sur la build 18305 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-138">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-139">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-139">WSL</span></span>
* <span data-ttu-id="ad6f9-140">pthreads perdre l’accès aux fichiers quand le thread principal s’arrête [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-140">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="ad6f9-141">TIOCSCTTY doit ignorer le paramètre « force », sauf si elle est nécessaire [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-141">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="ad6f9-142">améliorations de ligne de commande wsl.exe et ajout d’importation / exportation de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-142">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="ad6f9-143">Build 18277</span><span class="sxs-lookup"><span data-stu-id="ad6f9-143">Build 18277</span></span>
<span data-ttu-id="ad6f9-144">Pour Windows général plus d’informations sur la build 18277 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-144">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-145">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-145">WSL</span></span>
* <span data-ttu-id="ad6f9-146">Corriger l’erreur « interface non pris en charge » introduit dans la version 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-146">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="ad6f9-147">Ignorer l’indicateur MNT_FORCE pour syscall unmount [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-147">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="ad6f9-148">Interopérabilité WSL de commutateur à utiliser l’API CreatePseudoConsole officiel</span><span class="sxs-lookup"><span data-stu-id="ad6f9-148">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="ad6f9-149">Mettre à jour aucune valeur de délai d’attente lorsque FUTEX_WAIT redémarre</span><span class="sxs-lookup"><span data-stu-id="ad6f9-149">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="ad6f9-150">Build 18272</span><span class="sxs-lookup"><span data-stu-id="ad6f9-150">Build 18272</span></span>
<span data-ttu-id="ad6f9-151">Pour Windows général plus d’informations sur la build 18272 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-151">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-152">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-152">WSL</span></span>
* <span data-ttu-id="ad6f9-153">**AVERTISSEMENT :** Il existe un problème dans la génération qui rend WSL inutilisable.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-153">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="ad6f9-154">Lorsque vous tentez de lancer votre distribution, vous verrez une erreur « Interface non pris en charge ».</span><span class="sxs-lookup"><span data-stu-id="ad6f9-154">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="ad6f9-155">Le problème a été résolu et sera dans la build de la semaine prochaine Insider rapide.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-155">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="ad6f9-156">Si vous avez installé cette build, vous pouvez revenir à la build précédente de Windows à l’aide de « Go revenir à la version précédente de Windows 10 » dans les paramètres -> mise à jour & sécurité -> Recovery.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-156">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="ad6f9-157">Build 18267</span><span class="sxs-lookup"><span data-stu-id="ad6f9-157">Build 18267</span></span>
<span data-ttu-id="ad6f9-158">Pour Windows général plus d’informations sur la build 18267 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-158">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-159">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-159">WSL</span></span>
* <span data-ttu-id="ad6f9-160">Corrigez le problème dans lequel les processus inactifs ne peuvent pas différentes et rester indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-160">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="ad6f9-161">WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-161">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="ad6f9-162">Autoriser fsync échoué pour les fichiers en lecture seule sur DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-162">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="ad6f9-163">Vérifiez que les répertoires /bin et /sbin existent avant de créer des liens symboliques à l’intérieur de [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-163">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="ad6f9-164">Ajouter un mécanisme de délai d’attente d’arrêt instance pour les instances WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-164">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="ad6f9-165">Le délai d’attente est actuellement définie sur 15 secondes, ce qui signifie que l’instance s’arrête dès que le dernier processus WSL quitte les 15 secondes.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-165">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="ad6f9-166">Pour mettre fin immédiatement à une distribution, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-166">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="ad6f9-167">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-167">Build 17763 (1809)</span></span>
<span data-ttu-id="ad6f9-168">Pour Windows général plus d’informations sur la build 17763 visitez le [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-168">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-169">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-169">WSL</span></span>
* <span data-ttu-id="ad6f9-170">Vérification des autorisations SetPriority syscall trop stricte pour modifier la priorité de thread même [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-170">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="ad6f9-171">Garantir que les temps d’interruption non biaisée est utilisé pour le démarrage pour éviter le renvoi des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-171">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="ad6f9-172">Gérer les liens symboliques dans l’interpréteur de binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-172">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="ad6f9-173">Meilleure gestion de nettoyage de descripteur de fichier de leader threadgroup.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-173">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="ad6f9-174">Commutateur WSL à utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter du afin d’éviter le dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-174">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="ad6f9-175">Ptrace attacher mai provoquer la mauvaise valeur de retour à partir des appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-175">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="ad6f9-176">Correctif que relatif AF_UNIX plusieurs problèmes [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-176">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="ad6f9-177">Correction d’un problème qui provoquait interop WSL échoue si le répertoire de travail actuel est inférieur à 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-177">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="ad6f9-178">Éviter un délai deuxième échec des connexions de bouclage aux ports inexistant [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-178">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="ad6f9-179">Ajouter un fichier stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-179">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="ad6f9-180">Informations de portée IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-180">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="ad6f9-181">Prise en charge PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-181">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="ad6f9-182">Canal de système de fichiers par inadvertance effacement epoll déclenchée par edge événement [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-182">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="ad6f9-183">Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-183">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="ad6f9-184">Prise en charge de zombie [GH 1353] améliorée</span><span class="sxs-lookup"><span data-stu-id="ad6f9-184">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="ad6f9-185">Ajouter des entrées wsl.conf pour contrôler le comportement d’interopérabilité Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-185">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="ad6f9-186">Correctif pour getsockname pas toujours renvoyer le type de famille du socket UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-186">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="ad6f9-187">Ajouter la prise en charge pour TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-187">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="ad6f9-188">Non bloquant de sockets en cours de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-188">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="ad6f9-189">Prendre en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-189">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="ad6f9-190">Corriger le problème sur le dossier racine [GH 3304] de vérification d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ad6f9-190">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="ad6f9-191">Prise en charge limitée TTY clavier ioctls KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-191">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="ad6f9-192">Applications d’interface utilisateur Windows doivent s’exécuter même lorsque lancé en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-192">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="ad6f9-193">Ajouter l’option -u ou--utilisateur wsl [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-193">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="ad6f9-194">Résoudre les problèmes de lancement WSL de démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-194">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="ad6f9-195">Sockets UNIX doivent conserver les informations d’identification homologue déconnectée [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-195">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="ad6f9-196">Sockets Unix de non bloquants indéfiniment échoué à cause d’EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-196">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="ad6f9-197">cas = off est de type [2937 GH 3212, 3328] de montage des nouvelle drvfs par défaut</span><span class="sxs-lookup"><span data-stu-id="ad6f9-197">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="ad6f9-198">Consultez [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-198">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="ad6f9-199">Ajouter wslconfig / arrêter pour arrêter l’exécution des distributions.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-199">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="ad6f9-200">Résoudre les problème avec le contexte du shell WSL les entrées de menu qui ne gèrent pas correctement les chemins d’accès avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-200">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="ad6f9-201">Exposer par répertoire respecte la casse comme un attribut étendu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-201">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="ad6f9-202">ARM64 : Émuler des opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-202">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="ad6f9-203">Résoudre [dotnet problème](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-203">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="ad6f9-204">DrvFs : unescape uniquement des caractères dans la plage privées qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-204">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="ad6f9-205">Corriger désactivé par une erreur de validation de la longueur interpréteur ELF analyseur [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-205">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="ad6f9-206">Minuteurs d’absolu WSL avec une heure dans le passé ne déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-206">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="ad6f9-207">Vérifiez qui vient d’être des points d’analyse créés sont répertoriés en tant que tel dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-207">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="ad6f9-208">Créer atomiquement répertoires respecte la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-208">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="ad6f9-209">Correction d’un problème supplémentaire où les opérations multithread peut retourner ENOENT, même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-209">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="ad6f9-210">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-210">[GH 2712]</span></span>
* <span data-ttu-id="ad6f9-211">Fixe WSL lancer échec lorsque UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-211">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="ad6f9-212">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-212">[GH 3020]</span></span>
* <span data-ttu-id="ad6f9-213">Ajouter un menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-213">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="ad6f9-214">Pour utiliser, maintenez la touche MAJ et avec le bouton droit dans une fenêtre d’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-214">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="ad6f9-215">Corriger le comportement Unix socket non bloquant [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-215">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="ad6f9-216">Correctif négatif de commande NETLINK comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-216">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="ad6f9-217">Ajouter la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-217">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="ad6f9-218">Résoudre le problème avec les événements inotify entraînant pas tronquer [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-218">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="ad6f9-219">Ajoutez--option exec pour wsl.exe appeler un fichier binaire unique sans un interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-219">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="ad6f9-220">Ajoutez--option de distribution pour wsl.exe sélectionner une distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-220">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="ad6f9-221">Prise en charge limitée dmesg.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-221">Limited support for dmesg.</span></span> <span data-ttu-id="ad6f9-222">Les applications peuvent maintenant vous connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-222">Applications can now log to dmesg.</span></span> <span data-ttu-id="ad6f9-223">Pilote WSL consigne des informations limitées dans dmesg.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-223">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="ad6f9-224">À l’avenir, cela peut être étendu pour effectuer d’autres informations/diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-224">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="ad6f9-225">Remarque : dmesg actuellement pris en charge par le biais du `/dev/kmsg` interface de périphérique.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-225">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="ad6f9-226">`syslog` syscall interface n’est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-226">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="ad6f9-227">Et, par conséquent, certaines de la `dmesg` options de ligne de commande telles que `-S`, `-C` ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-227">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="ad6f9-228">Modifier les gid par défaut et périphériques série pour faire correspondre natif [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-228">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="ad6f9-229">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-229">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="ad6f9-230">Remarque: DrvFs présente certaines limitations sur le nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-230">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="ad6f9-231">Certains caractères (comme '/', ' :' et '\*') ne sont pas autorisées et étendu les noms d’attributs ne sont pas sensible à la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-231">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="ad6f9-232">Build 18252 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-232">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="ad6f9-233">Pour Windows général plus d’informations sur la build 18252 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-233">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-234">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-234">WSL</span></span>
* <span data-ttu-id="ad6f9-235">Déplacer des binaires init et bsdtar en dehors de la dll de lxssmanager et dans un dossier des outils distincts</span><span class="sxs-lookup"><span data-stu-id="ad6f9-235">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="ad6f9-236">Corriger la concurrence autour de fermer le descripteur de fichier lors de l’utilisation de CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="ad6f9-236">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="ad6f9-237">Gérer les champs facultatifs dans /proc/pid/mountinfo lors de la traduction des chemins d’accès DrvFs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-237">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="ad6f9-238">Autoriser mknod DrvFs de réussir sans prise en charge des métadonnées pour S_IFREG</span><span class="sxs-lookup"><span data-stu-id="ad6f9-238">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="ad6f9-239">Fichiers en lecture seule créés sur DrvFs doivent avoir l’attribut en lecture seule définie [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-239">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="ad6f9-240">Ajouter d’assistance /sbin/mount.drvfs pour gérer le montage DrvFs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-240">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="ad6f9-241">Utilisez le changement de nom POSIX dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-241">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="ad6f9-242">Permet la traduction de chemin d’accès sur les volumes sans GUID du volume.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-242">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="ad6f9-243">Build 17738 (rapide)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-243">Build 17738 (Fast)</span></span>
<span data-ttu-id="ad6f9-244">Pour Windows général plus d’informations sur la build 17738 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-244">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-245">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-245">WSL</span></span>
* <span data-ttu-id="ad6f9-246">Vérification des autorisations SetPriority syscall trop stricte pour modifier la priorité de thread même [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-246">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="ad6f9-247">Garantir que les temps d’interruption non biaisée est utilisé pour le démarrage pour éviter le renvoi des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-247">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="ad6f9-248">Gérer les liens symboliques dans l’interpréteur de binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-248">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="ad6f9-249">Meilleure gestion de nettoyage de descripteur de fichier de leader threadgroup.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-249">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="ad6f9-250">Build 17728 (rapide)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-250">Build 17728 (Fast)</span></span>
<span data-ttu-id="ad6f9-251">Pour Windows général plus d’informations sur la build 17728 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-251">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-252">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-252">WSL</span></span>
* <span data-ttu-id="ad6f9-253">Commutateur WSL à utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter du afin d’éviter le dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-253">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="ad6f9-254">Ptrace attacher mai provoquer la mauvaise valeur de retour à partir des appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-254">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="ad6f9-255">Correctif que relatif d’un nombre de AF_UNIX émet [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-255">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="ad6f9-256">Correction d’un problème qui provoquait interop WSL échoue si le répertoire de travail actuel est inférieur à 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-256">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="ad6f9-257">Build 18204 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-257">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="ad6f9-258">Pour Windows général plus d’informations sur la build 18204 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-258">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-259">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-259">WSL</span></span>
* <span data-ttu-id="ad6f9-260">Diriger inadvertenly filesystem effacer événement epoll déclenchée par edge [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-260">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="ad6f9-261">Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="ad6f9-262">Build 17723 (rapide)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-262">Build 17723 (Fast)</span></span>
<span data-ttu-id="ad6f9-263">Pour Windows général plus d’informations sur la build 17723 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-263">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-264">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-264">WSL</span></span>
* <span data-ttu-id="ad6f9-265">Éviter un délai deuxième échec des connexions de bouclage aux ports inexistant [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-265">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="ad6f9-266">Ajouter un fichier stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-266">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="ad6f9-267">Informations de portée IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-267">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="ad6f9-268">Prise en charge PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-268">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="ad6f9-269">Diriger inadvertenly filesystem effacer événement epoll déclenchée par edge [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="ad6f9-270">Exécutable Win32 lancée via le lien symbolique NTFS ne respecte pas le nom de lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="ad6f9-271">Build 17713</span><span class="sxs-lookup"><span data-stu-id="ad6f9-271">Build 17713</span></span>
<span data-ttu-id="ad6f9-272">Pour Windows général plus d’informations sur la build 17713 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-272">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-273">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-273">WSL</span></span>
* <span data-ttu-id="ad6f9-274">Prise en charge de zombie [GH 1353] améliorée</span><span class="sxs-lookup"><span data-stu-id="ad6f9-274">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="ad6f9-275">Ajouter des entrées wsl.conf pour contrôler le comportement d’interopérabilité Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-275">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="ad6f9-276">Correctif pour getsockname pas toujours renvoyer le type de famille du socket UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-276">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="ad6f9-277">Ajouter la prise en charge pour TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-277">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="ad6f9-278">Non bloquant de sockets en cours de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-278">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="ad6f9-279">Prendre en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-279">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="ad6f9-280">Corriger le problème sur le dossier racine [GH 3304] de vérification d’autorisation</span><span class="sxs-lookup"><span data-stu-id="ad6f9-280">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="ad6f9-281">Prise en charge limitée TTY clavier ioctls KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-281">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="ad6f9-282">Applications d’interface utilisateur Windows doivent s’exécuter même lorsque lancé en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-282">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="ad6f9-283">Build 17704</span><span class="sxs-lookup"><span data-stu-id="ad6f9-283">Build 17704</span></span>
<span data-ttu-id="ad6f9-284">Pour Windows général plus d’informations sur la build 17704 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-284">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-285">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-285">WSL</span></span>
* <span data-ttu-id="ad6f9-286">Ajouter l’option -u ou--utilisateur wsl [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-286">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="ad6f9-287">Résoudre les problèmes de lancement WSL de démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-287">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="ad6f9-288">Sockets UNIX doivent conserver les informations d’identification homologue déconnectée [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-288">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="ad6f9-289">Sockets Unix de non bloquants indéfiniment échoué à cause d’EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-289">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="ad6f9-290">cas = off est de type [2937 GH 3212, 3328] de montage des nouvelle drvfs par défaut</span><span class="sxs-lookup"><span data-stu-id="ad6f9-290">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="ad6f9-291">Consultez [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-291">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="ad6f9-292">Ajouter wslconfig / arrêter pour arrêter l’exécution des distributions.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-292">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="ad6f9-293">Build 17692</span><span class="sxs-lookup"><span data-stu-id="ad6f9-293">Build 17692</span></span>
<span data-ttu-id="ad6f9-294">Pour Windows général plus d’informations sur la build 17692 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-294">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-295">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-295">WSL</span></span>
* <span data-ttu-id="ad6f9-296">Résoudre les problème avec le contexte du shell WSL les entrées de menu qui ne gèrent pas correctement les chemins d’accès avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-296">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="ad6f9-297">Exposer par répertoire respecte la casse comme un attribut étendu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-297">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="ad6f9-298">ARM64 : Émuler des opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-298">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="ad6f9-299">Résoudre [dotnet problème](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-299">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="ad6f9-300">DrvFs : unescape uniquement des caractères dans la plage privées qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-300">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="ad6f9-301">Build 17686</span><span class="sxs-lookup"><span data-stu-id="ad6f9-301">Build 17686</span></span>
<span data-ttu-id="ad6f9-302">Pour Windows général plus d’informations sur la build 17686 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-302">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-303">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-303">WSL</span></span>
* <span data-ttu-id="ad6f9-304">Corriger désactivé par une erreur de validation de la longueur interpréteur ELF analyseur [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-304">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="ad6f9-305">Minuteurs d’absolu WSL avec une heure dans le passé ne déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-305">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="ad6f9-306">Vérifiez qui vient d’être des points d’analyse créés sont répertoriés en tant que tel dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-306">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="ad6f9-307">Créer atomiquement répertoires respecte la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-307">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="ad6f9-308">Build 17677</span><span class="sxs-lookup"><span data-stu-id="ad6f9-308">Build 17677</span></span>
<span data-ttu-id="ad6f9-309">Pour Windows général plus d’informations sur la build 17677 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-309">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-310">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-310">WSL</span></span>
* <span data-ttu-id="ad6f9-311">Correction d’un problème supplémentaire où les opérations multithread peut retourner ENOENT, même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-311">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="ad6f9-312">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-312">[GH 2712]</span></span>
* <span data-ttu-id="ad6f9-313">Fixe WSL lancer échec lorsque UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-313">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="ad6f9-314">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-314">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="ad6f9-315">Build 17666</span><span class="sxs-lookup"><span data-stu-id="ad6f9-315">Build 17666</span></span>
<span data-ttu-id="ad6f9-316">Pour Windows général plus d’informations sur la build 17666 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-316">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-317">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-317">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="ad6f9-318">AVERTISSEMENT : Il existe un problème WSL empêche de s’exécuter sur certains chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-318">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="ad6f9-319">Un correctif est prêt et qu’il apporte sa méthode pour la branche de Build Insider.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-319">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="ad6f9-320">Ajouter un menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-320">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="ad6f9-321">Pour utiliser MAJ de blocage et avec le bouton droit dans une fenêtre d’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-321">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="ad6f9-322">Corriger le comportement unix socket non bloquant [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-322">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="ad6f9-323">Correctif négatif de commande NETLINK comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-323">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="ad6f9-324">Ajouter la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-324">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="ad6f9-325">Résoudre le problème avec les événements inotify entraînant pas tronquer [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-325">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="ad6f9-326">Ajoutez--option exec pour wsl.exe appeler un fichier binaire unique sans un interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-326">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="ad6f9-327">Ajoutez--option de distribution pour wsl.exe sélectionner une distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-327">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="ad6f9-328">Build 17655 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-328">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="ad6f9-329">Pour Windows général plus d’informations sur la build 17655 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-329">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-330">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-330">WSL</span></span>
* <span data-ttu-id="ad6f9-331">Prise en charge limitée dmesg.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-331">Limited support for dmesg.</span></span> <span data-ttu-id="ad6f9-332">Les applications peuvent maintenant vous connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-332">Applications can now log to dmesg.</span></span> <span data-ttu-id="ad6f9-333">Pilote WSL consigne des informations limitées dans dmesg.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-333">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="ad6f9-334">À l’avenir, cela peut être étendu pour effectuer d’autres informations/diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-334">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="ad6f9-335">Remarque : dmesg actuellement pris en charge par le biais du `/dev/kmsg` interface de périphérique.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-335">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="ad6f9-336">`syslog` interface de sycall n’est pas encore pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-336">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="ad6f9-337">Et, par conséquent, certaines de la `dmesg` options de ligne de commande telles que `-S`, `-C` ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-337">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="ad6f9-338">Correction d’un problème où les opérations multithread peut retourner ENOENT, même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-338">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="ad6f9-339">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-339">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="ad6f9-340">Build 17639 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-340">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="ad6f9-341">Pour Windows général plus d’informations sur la build 17639 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-341">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-342">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-342">WSL</span></span>
* <span data-ttu-id="ad6f9-343">Modifier les gid par défaut et périphériques série pour faire correspondre natif [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-343">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="ad6f9-344">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-344">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="ad6f9-345">Remarque: DrvFs présente certaines limitations sur le nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-345">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="ad6f9-346">En particulier, certains caractères (comme '/', ' :' et '\*') ne sont pas autorisées et étendu les noms d’attributs ne sont pas sensible à la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-346">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="ad6f9-347">Build 17133 (rapide)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-347">Build 17133 (Fast)</span></span>
<span data-ttu-id="ad6f9-348">Pour Windows général plus d’informations sur la build 17133 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-348">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-349">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-349">WSL</span></span>
* <span data-ttu-id="ad6f9-350">Correction d’un blocage dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-350">Fix for hang in WSL.</span></span> <span data-ttu-id="ad6f9-351">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-351">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="ad6f9-352">Build 17128 (rapide)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-352">Build 17128 (Fast)</span></span>
<span data-ttu-id="ad6f9-353">Pour Windows général plus d’informations sur la build 17128 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-353">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-354">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-354">WSL</span></span>
* <span data-ttu-id="ad6f9-355">Aucune</span><span class="sxs-lookup"><span data-stu-id="ad6f9-355">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="ad6f9-356">Build 17627 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-356">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="ad6f9-357">Pour Windows général plus d’informations sur la build 17627 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-357">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-358">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-358">WSL</span></span>
* <span data-ttu-id="ad6f9-359">Ajouter la prise en charge pour les opérations prenant en charge les pi futex.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-359">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="ad6f9-360">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-360">[GH 1006]</span></span>
    * <span data-ttu-id="ad6f9-361">Notez que les priorités ne sont pas actuellement une fonctionnalité WSL pris en charge par conséquent, il existe des limitations, mais l’utilisation standard doit être débloquée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-361">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="ad6f9-362">Prise en charge des pare-feu Windows pour les processus WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-362">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="ad6f9-363">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-363">[GH 1852]</span></span>
    * <span data-ttu-id="ad6f9-364">Par exemple, pour autoriser la WSL python traite pour écouter sur n’importe quel port, utilisez la commande Windows élevée : ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="ad6f9-364">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="ad6f9-365">Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-365">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="ad6f9-366">Respecter le shell par défaut de l’utilisateur lors de l’utilisation de wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-366">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="ad6f9-367">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-367">[GH 2372]</span></span>
* <span data-ttu-id="ad6f9-368">Déclarer toutes les interfaces réseau ethernet.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-368">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="ad6f9-369">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-369">[GH 2996]</span></span>
* <span data-ttu-id="ad6f9-370">Meilleure gestion du fichier de passwd endommagé.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-370">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="ad6f9-371">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-371">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-372">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-372">Console</span></span>
* <span data-ttu-id="ad6f9-373">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-373">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-374">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-374">LTP Results:</span></span>
<span data-ttu-id="ad6f9-375">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-375">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="ad6f9-376">Build 17618 (passer à l’avance)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-376">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="ad6f9-377">Pour Windows général plus d’informations sur la build 17618 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-377">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-378">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-378">WSL</span></span>
* <span data-ttu-id="ad6f9-379">Introduire une fonctionnalité pseudoconsole pour l’interopérabilité de NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-379">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="ad6f9-380">Le mécanisme d’installation héritée (lxrun.exe) a été déconseillé.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-380">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="ad6f9-381">Le mécanisme pris en charge pour l’installation de distributions est via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-381">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-382">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-382">Console</span></span>
* <span data-ttu-id="ad6f9-383">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-383">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-384">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-384">LTP Results:</span></span>
<span data-ttu-id="ad6f9-385">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-385">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="ad6f9-386">Build 17110</span><span class="sxs-lookup"><span data-stu-id="ad6f9-386">Build 17110</span></span>
<span data-ttu-id="ad6f9-387">Pour Windows général plus d’informations sur la build 17110 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-387">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-388">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-388">WSL</span></span>
* <span data-ttu-id="ad6f9-389">Autoriser /init à être arrêté à partir de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-389">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="ad6f9-390">DrvFs utilise désormais par répertoire respecte la casse par défaut (équivalent à la « cas = dir « option de montage).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-390">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="ad6f9-391">À l’aide de « cas = force » (l’ancien comportement) requiert la définition d’une clé de Registre.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-391">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="ad6f9-392">Exécutez la commande suivante pour activer « cas = force » si vous avez besoin pour l’utiliser : reg ajouter HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="ad6f9-392">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="ad6f9-393">Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui doivent respecter la casse, utiliser fsutil.exe pour les marquer comme respectant la casse : fsutil.exe fichier setcasesensitiveinfo <path> activer</span><span class="sxs-lookup"><span data-stu-id="ad6f9-393">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="ad6f9-394">Les chaînes retournées par la syscall uname finissant par NULL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-394">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-395">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-395">Console</span></span>
* <span data-ttu-id="ad6f9-396">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-396">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-397">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-397">LTP Results:</span></span>
<span data-ttu-id="ad6f9-398">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-398">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="ad6f9-399">Build 17107</span><span class="sxs-lookup"><span data-stu-id="ad6f9-399">Build 17107</span></span>
<span data-ttu-id="ad6f9-400">Pour Windows général plus d’informations sur la build 17107 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-400">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-401">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-401">WSL</span></span>
* <span data-ttu-id="ad6f9-402">Prend en charge TCSETSF et TCSETSW sur les points de terminaison maître pty [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-402">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="ad6f9-403">Démarrage des processus interop simultanées peut entraîner EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-403">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="ad6f9-404">Corriger PTRACE_ATTACH pour afficher l’état de suivi approprié dans /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-404">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="ad6f9-405">Concurrence de correctif où le processus de courte durée clonés avec indicateurs CLEARTID et de SETTID pu quitter sans effacer l’adresse TID.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-405">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="ad6f9-406">Afficher un message lors de la mise à niveau les répertoires de système de fichiers Linux lors du déplacement d’une build de pre-17093.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-406">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="ad6f9-407">Pour plus d’informations sur les modifications de système de 17093 fichiers, consultez les notes de publication pour [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-407">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-408">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-408">Console</span></span>
* <span data-ttu-id="ad6f9-409">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-409">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-410">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-410">LTP Results:</span></span>
<span data-ttu-id="ad6f9-411">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-411">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="ad6f9-412">Build 17101</span><span class="sxs-lookup"><span data-stu-id="ad6f9-412">Build 17101</span></span>
<span data-ttu-id="ad6f9-413">Pour Windows général plus d’informations sur la build 17101 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-413">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-414">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-414">WSL</span></span>
* <span data-ttu-id="ad6f9-415">Prise en charge signalfd.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-415">Support for signalfd.</span></span> <span data-ttu-id="ad6f9-416">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-416">[GH 129]</span></span>
* <span data-ttu-id="ad6f9-417">Prend en charge les noms de fichier contenant des caractères NTFS non valides en les codant en tant que caractères Unicode privés.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-417">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="ad6f9-418">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-418">[GH 1514]</span></span>
* <span data-ttu-id="ad6f9-419">Montage automatique utilisera en lecture seule lors de l’écriture n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-419">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="ad6f9-420">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-420">[GH 2603]</span></span>
* <span data-ttu-id="ad6f9-421">Autoriser le collage des paires de substitution Unicode (comme les caractères emoji).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-421">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="ad6f9-422">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-422">[GH 2765]</span></span>
* <span data-ttu-id="ad6f9-423">Fichiers pseudo-élément dans /proc et /sys doivent retourner la lecture et écrire des prêts à partir de select, interrogation, epoll, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-423">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="ad6f9-424">Corrigez le problème qui pouvait entraîner service passe en boucle infinie lorsque le Registre a été falsifié ou est endommagé.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-424">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="ad6f9-425">Résoudre les messages netlink pour travailler avec la nouvelle version (en amont 4.14) d’iproute2.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-425">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-426">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-426">Console</span></span>
* <span data-ttu-id="ad6f9-427">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-427">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-428">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-428">LTP Results:</span></span>
<span data-ttu-id="ad6f9-429">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-429">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="ad6f9-430">Build 17093</span><span class="sxs-lookup"><span data-stu-id="ad6f9-430">Build 17093</span></span>
<span data-ttu-id="ad6f9-431">Pour Windows général plus d’informations sur la build 17093 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-431">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="ad6f9-432">Important :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-432">Important:</span></span>
<span data-ttu-id="ad6f9-433">Lorsque vous démarrez WSL pour la première fois après la mise à niveau vers cette version, il doit effectuer un travail de la mise à niveau les répertoires de système de fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-433">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="ad6f9-434">Cela peut prendre jusqu'à plusieurs minutes, donc WSL peut sembler démarrer lentement.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-434">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="ad6f9-435">Cela ne doit se produire une fois pour chaque distribution que vous avez installé à partir du magasin.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-435">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="ad6f9-436">Meilleure prise en charge de la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-436">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="ad6f9-437">DrvFs prend désormais en charge par répertoire respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-437">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="ad6f9-438">Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme respectant la casse, ce qui permet de même des applications Windows ouvrir correctement les fichiers qui diffèrent uniquement par la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-438">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="ad6f9-439">DrvFs a de nouvelles options de montage contrôle respecte la casse sur une base par répertoire</span><span class="sxs-lookup"><span data-stu-id="ad6f9-439">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="ad6f9-440">cas = force : tous les répertoires sont traités comme respectant la casse (à l’exception de la racine du lecteur).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-440">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="ad6f9-441">Nouveaux répertoires créés avec WSL sont marqués comme respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-441">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="ad6f9-442">Il s’agit de l’ancien comportement à l’exception de marquage de nouveaux répertoires respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-442">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="ad6f9-443">cas = dir : seuls les répertoires avec l’indicateur par répertoire respecte la casse sont traités comme respectant la casse ; autres répertoires respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-443">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="ad6f9-444">Nouveaux répertoires créés avec WSL sont marqués comme respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-444">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="ad6f9-445">cas = off : seuls les répertoires avec l’indicateur par répertoire respecte la casse sont traités comme respectant la casse ; autres répertoires respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-445">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="ad6f9-446">Nouveaux répertoires créés avec WSL portent la mention de la casse.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-446">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="ad6f9-447">Remarque : répertoires créés par WSL dans les versions précédentes n’ont pas cet indicateur défini, afin de ne pas être traités comme respectant la casse si vous utilisez le « cas = dir « option.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-447">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="ad6f9-448">Une façon de définir cet indicateur dans les répertoires existants sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-448">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="ad6f9-449">Exemple de montage avec ces options (pour les lecteurs existants, vous devez tout d’abord la démonter avant que vous pouvez monter avec des options différentes) : sudo mount -t drvfs C:/mnt/c -o cas = dir</span><span class="sxs-lookup"><span data-stu-id="ad6f9-449">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="ad6f9-450">Pour l’instant, cas = force est toujours l’option par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-450">For now, case=force is still the default option.</span></span> <span data-ttu-id="ad6f9-451">Ce sera remplacé au cas = dir dans le futur.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-451">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="ad6f9-452">Vous pouvez maintenant utiliser des barres obliques dans les chemins d’accès de Windows lors du montage DrvFs, par exemple : sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="ad6f9-452">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="ad6f9-453">WSL traite désormais le fichier/etc/fstab pendant le démarrage de l’instance [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-453">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="ad6f9-454">Cette opération est effectuée avant de monter automatiquement les lecteurs de DrvFs ; tous les lecteurs qui ont été déjà montés par fstab ne seront pas être remontées automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-454">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="ad6f9-455">Ce comportement peut être désactivé à l’aide de wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-455">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="ad6f9-456">Les fichiers de montage, mountinfo et mountstats dans /proc échappement correctement les caractères spéciaux tels que des barres obliques inverses et les espaces [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-456">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="ad6f9-457">Fichiers spéciaux créés avec DrvFs tels que des liens symboliques WSL, ou file d’attente FIFO et les sockets lorsque les métadonnées sont activées, peuvent désormais être copiés et déplacés à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-457">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="ad6f9-458">WSL est plus configurable avec wsl.conf</span><span class="sxs-lookup"><span data-stu-id="ad6f9-458">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="ad6f9-459">Nous avons ajouté une méthode vous permettant de configurer automatiquement certaines fonctionnalités dans WSL qui est appliqué chaque fois que vous lancez le sous-système.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-459">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="ad6f9-460">Cela inclut les options de montage automatique et de configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-460">This includes automount options and network configuration.</span></span> <span data-ttu-id="ad6f9-461">Pour en savoir plus à ce sujet à notre billet de blog : https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="ad6f9-461">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="ad6f9-462">AF_UNIX autorise les connexions de socket entre les processus de Linux sur WSL et les processus natifs de Windows</span><span class="sxs-lookup"><span data-stu-id="ad6f9-462">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="ad6f9-463">Applications WSL et Windows peuvent désormais communiquer avec eux via des sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-463">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="ad6f9-464">Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible aux applications Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-464">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="ad6f9-465">Maintenant, c’est possible avec les sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-465">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="ad6f9-466">Lecture de plus, consultez notre blog publiez au https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="ad6f9-466">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-467">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-467">WSL</span></span>
* <span data-ttu-id="ad6f9-468">Mmap() prise en charge avec MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="ad6f9-469">Prendre en charge CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-469">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="ad6f9-470">Gérer le signal d’arrêt non SIGCHLD clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-470">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="ad6f9-471">Stub /proc/sys/fs/inotify/max_user_instances et /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-471">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="ad6f9-472">Erreur lors du chargement des fichiers binaires ELF qui contiennent des en-têtes de charge avec zéro décalages [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-472">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="ad6f9-473">Zéro octets de la page de fin lors du chargement d’images.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-473">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="ad6f9-474">Réduire les cas où execve en mode silencieux pour achever</span><span class="sxs-lookup"><span data-stu-id="ad6f9-474">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-475">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-475">Console</span></span>
* <span data-ttu-id="ad6f9-476">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-476">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-477">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-477">LTP Results:</span></span>
<span data-ttu-id="ad6f9-478">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-478">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="ad6f9-479">Build 17083</span><span class="sxs-lookup"><span data-stu-id="ad6f9-479">Build 17083</span></span>
<span data-ttu-id="ad6f9-480">Pour Windows général plus d’informations sur la build 17083 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-480">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-481">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-481">WSL</span></span>
* <span data-ttu-id="ad6f9-482">Vérification d’erreur fixe liée à epoll [2798 GH 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-482">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="ad6f9-483">Fixe se bloque lors de la désactivation de l’ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-483">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="ad6f9-484">Vérifiez les opérations mmap apparaissent atomique [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-484">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-485">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-485">Console</span></span>
* <span data-ttu-id="ad6f9-486">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-487">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-487">LTP Results:</span></span>
<span data-ttu-id="ad6f9-488">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-488">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="ad6f9-489">Build 17074</span><span class="sxs-lookup"><span data-stu-id="ad6f9-489">Build 17074</span></span>
<span data-ttu-id="ad6f9-490">Pour Windows général plus d’informations sur la build 17074 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-490">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-491">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-491">WSL</span></span>
* <span data-ttu-id="ad6f9-492">Format de stockage fixe de métadonnées DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-492">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="ad6f9-493">**Important :** Métadonnées DrvFs créées avant cette build s’afficheront mal ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-493">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="ad6f9-494">Pour résoudre les fichiers affectés, utilisez chmod et chown à réappliquer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-494">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="ad6f9-495">Correction d’un problème avec plusieurs signaux et syscalls redémarrable.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-495">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-496">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-496">Console</span></span>
* <span data-ttu-id="ad6f9-497">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-498">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-498">LTP Results:</span></span>
<span data-ttu-id="ad6f9-499">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-499">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="ad6f9-500">Build 17063</span><span class="sxs-lookup"><span data-stu-id="ad6f9-500">Build 17063</span></span>
<span data-ttu-id="ad6f9-501">Pour Windows général plus d’informations sur la build 17063 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-501">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="ad6f9-502">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-502">WSL</span></span>
* <span data-ttu-id="ad6f9-503">DrvFs prend en charge des métadonnées supplémentaires de Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-503">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="ad6f9-504">Cela permet de définir le propriétaire et le mode de fichiers à l’aide de chmod/chown, ainsi que la création de fichiers spéciaux tels que la file d’attente FIFO, les sockets unix et les fichiers de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-504">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="ad6f9-505">Cela est désactivée par défaut pour l’instant, car il est encore au stade expérimental.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-505">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="ad6f9-506">**Remarque :**  Nous avons résolu un bogue dans le format de métadonnées utilisé par DrvFs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-506">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="ad6f9-507">Bien que métadonnées fonctionnement sur cette génération pour l’expérimentation, builds futures correctement ne lira pas les métadonnées créées par cette build.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-507">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="ad6f9-508">Vous devrez peut-être mettre à jour manuellement le propriétaire pour les fichiers modifiés et appareils avec un ID d’appareil personnalisé devront être recréés.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-508">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="ad6f9-509">Pour activer, DrvFs de montage avec l’option de métadonnées (pour l’activer sur un montage existant, vous devez tout d’abord la démonter) :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-509">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="ad6f9-510">Autorisations de Linux sont ajoutées en tant que métadonnées supplémentaires au fichier ; elles n’affectent pas les autorisations de Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-510">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="ad6f9-511">N’oubliez pas de modification d’un fichier à l’aide d’un éditeur Windows peut supprimer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-511">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="ad6f9-512">Dans ce cas, le fichier reprendront ses autorisations par défaut.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-512">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="ad6f9-513">Options de montage ajouté à DrvFs pour contrôler les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-513">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="ad6f9-514">UID : l’ID d’utilisateur utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-514">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="ad6f9-515">GID : l’ID de groupe utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-515">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="ad6f9-516">umask : un masque octal des autorisations à exclure pour tous les fichiers et répertoires.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-516">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="ad6f9-517">cas : un masque octal des autorisations à exclure pour tous les fichiers régulières.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-517">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="ad6f9-518">dmask : un masque octal des autorisations à exclure tous les répertoires.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-518">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="ad6f9-519">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-519">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="ad6f9-520">Combiner avec l’option de métadonnées pour spécifier les autorisations par défaut pour les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-520">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="ad6f9-521">A introduit une nouvelle variable d’environnement, `WSLENV`, pour configurer le flux des variables d’environnement entre WSL et Win32.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-521">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="ad6f9-522">Exemple :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-522">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="ad6f9-523">`WSLENV` est une liste délimitée par des deux-points de variables d’environnement qui peut être inclus lors du lancement du processus WSL à partir de Win32 ou Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-523">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="ad6f9-524">Chaque variable peut être suivi du suffixe par une barre oblique suivie d’indicateurs pour spécifier la façon dont elle est convertie.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-524">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="ad6f9-525">p : La valeur est un chemin d’accès qui doit être convertis entre les chemins de Win32 et WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-525">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="ad6f9-526">L : La valeur est une liste de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-526">l: The value is a list of paths.</span></span> <span data-ttu-id="ad6f9-527">Dans WSL, il est une liste délimitée par des deux-points.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-527">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="ad6f9-528">Dans Win32, il est une liste délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-528">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="ad6f9-529">%U : La valeur doit être incluse uniquement lors de l’appel WSL à partir de Win32</span><span class="sxs-lookup"><span data-stu-id="ad6f9-529">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="ad6f9-530">w : La valeur doit être incluse uniquement lors de l’appel Win32 à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-530">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="ad6f9-531">Vous pouvez définir `WSLENV` dans .bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-531">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="ad6f9-532">drvfs montages conserve correctement les horodatages de tar, cp -p (1939 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="ad6f9-533">liens symboliques drvfs indiquent la taille correcte (2641 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-533">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="ad6f9-534">en lecture/écriture fonctionne pour les très grandes tailles d’e/s (2653 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-534">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="ad6f9-535">waitpid fonctionne avec le groupe de processus ID (2534 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-535">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="ad6f9-536">mmap amélioration significative des performances pour les régions de la réserve de grande taille ; améliore les performances de ghc (1671 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-536">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="ad6f9-537">prise en charge de la personnalité de READ_IMPLIES_EXEC ; résout les maxima et clisp (1185 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-537">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="ad6f9-538">mprotect prend en charge PROT_GROWSDOWN ; correctifs clisp (1128 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="ad6f9-539">page d’erreur correctifs dans sollicitation excessive du mode ; correctifs sbcl (1128 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-539">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="ad6f9-540">Clone prend en charge plusieurs combinaisons d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-540">clone supports more flags combinations</span></span>
* <span data-ttu-id="ad6f9-541">Prend en charge select/epoll des fichiers epoll (précédemment une absence d’opération).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-541">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="ad6f9-542">Notifier ptrace de syscalls non implémentée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-542">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="ad6f9-543">Ignorer les interfaces qui ne sont pas des lors de la génération des serveurs de noms resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-543">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="ad6f9-544">Énumérer les interfaces réseau avec aucune adresse physique.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-544">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="ad6f9-545">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-545">[GH 2685]</span></span>
* <span data-ttu-id="ad6f9-546">Améliorations et correctifs de bogues supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-546">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="ad6f9-547">Outils de Linux qui permettent aux développeurs sur Windows</span><span class="sxs-lookup"><span data-stu-id="ad6f9-547">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="ad6f9-548">Ligne de commande de Windows chaîne d’outils inclut bsdtar (tar) et curl.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-548">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="ad6f9-549">Lecture [ce billet de blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et de voir comment ils vous mettre en forme l’expérience de développement sur Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-549">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="ad6f9-550">`AF_UNIX` est disponible dans le Kit de développement Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-550">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="ad6f9-551">Lecture [ce billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus sur `AF_UNIX` et comment les développeurs sur Windows peuvent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-551">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="ad6f9-552">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-552">Console</span></span>
* <span data-ttu-id="ad6f9-553">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-553">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-554">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-554">LTP Results:</span></span>
<span data-ttu-id="ad6f9-555">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-555">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="ad6f9-556">Build 17046</span><span class="sxs-lookup"><span data-stu-id="ad6f9-556">Build 17046</span></span>

<span data-ttu-id="ad6f9-557">Pour Windows général plus d’informations sur la build 17046 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-557">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="ad6f9-558">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-558">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-559">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-559">WSL</span></span>
- <span data-ttu-id="ad6f9-560">Autoriser le processus à s’exécuter sans un Terminal Server actives.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-560">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="ad6f9-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="ad6f9-562">Mieux prendre en charge de CLONE_VFORK et CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-562">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="ad6f9-563">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-563">[GH 1878, 2615]</span></span>
- <span data-ttu-id="ad6f9-564">Ignorer les pilotes de filtre TDI pour WSL opérations de mise en réseau.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-564">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="ad6f9-565">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-565">[GH 1554]</span></span>
- <span data-ttu-id="ad6f9-566">DrvFs crée des liens symboliques NT lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-566">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="ad6f9-567">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-567">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="ad6f9-568">La cible du lien doit être relative, ne doit pas traverser les points de montage ou les liens symboliques et doit exister.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-568">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="ad6f9-569">L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela requiert généralement que vous lancez wsl.exe avec élévation de privilèges), sauf si le Mode développeur est activé.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-569">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="ad6f9-570">Dans toutes les autres situations, DrvFs crée toujours des liens symboliques WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-570">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="ad6f9-571">Autoriser en cours d’exécution avec élévation de privilèges et non élevés instances WSL simultanément.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-571">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="ad6f9-572">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="ad6f9-572">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="ad6f9-573">Ajouter wslpath pour faire WSL <> – conversions de chemin d’accès de Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-573">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="ad6f9-574">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-574">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="ad6f9-575">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-575">Console</span></span>
- <span data-ttu-id="ad6f9-576">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-576">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-577">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-577">LTP Results:</span></span>
<span data-ttu-id="ad6f9-578">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-578">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="ad6f9-579">Build 17040</span><span class="sxs-lookup"><span data-stu-id="ad6f9-579">Build 17040</span></span>

<span data-ttu-id="ad6f9-580">Pour Windows général plus d’informations sur la build 17040 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-580">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-581">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-581">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-582">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-582">WSL</span></span>
- <span data-ttu-id="ad6f9-583">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-583">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-584">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-584">Console</span></span>
- <span data-ttu-id="ad6f9-585">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-585">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-586">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-586">LTP Results:</span></span>
<span data-ttu-id="ad6f9-587">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-587">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="ad6f9-588">Build 17035</span><span class="sxs-lookup"><span data-stu-id="ad6f9-588">Build 17035</span></span>

<span data-ttu-id="ad6f9-589">Pour Windows général plus d’informations sur la build 17035 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-589">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-590">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-591">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-591">WSL</span></span>
- <span data-ttu-id="ad6f9-592">Accéder aux fichiers sur DrvFs peut parfois échouer avec EINVAL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-592">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="ad6f9-593">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-593">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-594">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-594">Console</span></span>
- <span data-ttu-id="ad6f9-595">Une perte de couleur lors de l’insertion/suppression de lignes en mode de VT.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-595">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-596">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-596">LTP Results:</span></span>
<span data-ttu-id="ad6f9-597">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-597">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="ad6f9-598">Version 17025</span><span class="sxs-lookup"><span data-stu-id="ad6f9-598">Build 17025</span></span>

<span data-ttu-id="ad6f9-599">Pour Windows général plus d’informations sur la build 17025 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-599">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-600">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-600">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-601">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-601">WSL</span></span>
- <span data-ttu-id="ad6f9-602">Démarrer le processus initiales dans un nouveau groupe de processus de premier plan [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-602">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="ad6f9-603">Remise SIGHUP résout [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-603">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="ad6f9-604">Générer un nom de pont virtuel par défaut si aucun ne fourni [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-604">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="ad6f9-605">Implémenter /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="ad6f9-606">Résout les plus interop canal stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-606">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="ad6f9-607">Appel de système de syncfs de stub.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-607">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-608">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-608">Console</span></span>
- <span data-ttu-id="ad6f9-609">Corriger la traduction de VT d’entrée pour les consoles tiers [GH 111]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-609">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-610">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-610">LTP Results:</span></span>
<span data-ttu-id="ad6f9-611">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-611">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="ad6f9-612">Build 17017</span><span class="sxs-lookup"><span data-stu-id="ad6f9-612">Build 17017</span></span>

<span data-ttu-id="ad6f9-613">Pour Windows général plus d’informations sur la build 17017 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-613">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-614">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-614">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-615">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-615">WSL</span></span>
- <span data-ttu-id="ad6f9-616">Ignorer les en-têtes de programme vides ELF [GH 330].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-616">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="ad6f9-617">Autoriser LxssManager créer des instances WSL pour les utilisateurs non interactifs (ssh et planifiée prise en charge de la tâche) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-617">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="ad6f9-618">Prise en charge WSL -> Win32 -> [GH 1228] les scénarios WSL (« début »).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-618">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="ad6f9-619">Prise en charge limitée pour l’arrêt des applications de console appelé via interop [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-619">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="ad6f9-620">Prise en charge les options de montage pour devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-620">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="ad6f9-621">Ptrace blocage démarrage enfant [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-621">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="ad6f9-622">EPOLLET certains événements [GH 2462] manquants.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-622">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="ad6f9-623">Retourner plus de données pour PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-623">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="ad6f9-624">Getdents avec lseek donne des résultats incorrects.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-624">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="ad6f9-625">Corriger certains blocages d’application d’interopérabilité Win32, en attente d’entrée sur un canal qui n’a plus aucune donnée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-625">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="ad6f9-626">O_ASYNC prend en charge pour les fichiers de tty/pty.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-626">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="ad6f9-627">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-628">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-628">Console</span></span>
- <span data-ttu-id="ad6f9-629">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-630">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-630">LTP Results:</span></span>
<span data-ttu-id="ad6f9-631">Test en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-631">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="ad6f9-632">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="ad6f9-632">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="ad6f9-633">Build 16288</span><span class="sxs-lookup"><span data-stu-id="ad6f9-633">Build 16288</span></span>

<span data-ttu-id="ad6f9-634">Pour Windows général plus d’informations sur la build 16288 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-634">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-635">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-635">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-636">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-636">WSL</span></span>
- <span data-ttu-id="ad6f9-637">Initialiser correctement et de signaler les uid et gid mode pour les descripteurs de fichier socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-637">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="ad6f9-638">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-638">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-639">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-639">Console</span></span>
- <span data-ttu-id="ad6f9-640">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-640">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-641">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-641">LTP Results:</span></span>
<span data-ttu-id="ad6f9-642">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="ad6f9-642">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="ad6f9-643">Build 16278</span><span class="sxs-lookup"><span data-stu-id="ad6f9-643">Build 16278</span></span>

<span data-ttu-id="ad6f9-644">Pour Windows général plus d’informations sur la build 162738 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-644">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-645">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-645">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-646">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-646">WSL</span></span>
- <span data-ttu-id="ad6f9-647">Explicitement annuler le mappage de vues mappées des sections de la sauvegarde de fichiers lors de la destruction de l’état LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-647">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="ad6f9-648">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-648">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-649">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-649">Console</span></span>
- <span data-ttu-id="ad6f9-650">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-650">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-651">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-651">LTP Results:</span></span>
<span data-ttu-id="ad6f9-652">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="ad6f9-652">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="ad6f9-653">Build 16275</span><span class="sxs-lookup"><span data-stu-id="ad6f9-653">Build 16275</span></span>

<span data-ttu-id="ad6f9-654">Pour Windows général plus d’informations sur la build 162735 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-654">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-655">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-655">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-656">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-656">WSL</span></span>
- <span data-ttu-id="ad6f9-657">Aucun WSL les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-657">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-658">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-658">Console</span></span>
- <span data-ttu-id="ad6f9-659">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-660">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-660">LTP Results:</span></span>
<span data-ttu-id="ad6f9-661">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="ad6f9-661">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="ad6f9-662">Build 16273</span><span class="sxs-lookup"><span data-stu-id="ad6f9-662">Build 16273</span></span>

<span data-ttu-id="ad6f9-663">Pour Windows général plus d’informations sur la build 16273 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-663">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-664">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-665">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-665">WSL</span></span>
- <span data-ttu-id="ad6f9-666">Correction d’un problème où DrvFs parfois signalé le type de fichier incorrect pour les répertoires [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-666">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="ad6f9-667">Autoriser la création de sockets NETLINK_KOBJECT_UEVENT débloquer des programmes qui uevent utilisation [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-667">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="ad6f9-668">Ajouter la prise en charge pour la connexion à non bloquant [GH 903, 1391, 1584 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-668">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="ad6f9-669">Implémentez CLONE_FS cloner l’indicateur d’appel système [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-669">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="ad6f9-670">Résoudre les problèmes liés à la gère ne pas de tabulations ou guillemets correctement dans l’interopérabilité de NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-670">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="ad6f9-671">Résoudre l’erreur lorsque vous tentez de relancer WSL instances [GH 651, 2095] l’accès refusé</span><span class="sxs-lookup"><span data-stu-id="ad6f9-671">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="ad6f9-672">Implémenter des opérations FUTEX_REQUEUE et FUTEX_CMP_REQUEUE futex [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-672">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="ad6f9-673">Corriger les autorisations pour les divers fichiers SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-673">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="ad6f9-674">Corriger le blocage de pile de Haskell pendant l’installation [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-674">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="ad6f9-675">Implémenter binfmt_misc « C » ' o ' et les indicateurs « P » [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-675">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="ad6f9-676">Ajouter /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="ad6f9-677">Ajouter la prise en charge partielle de l’appel de système d’ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-677">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="ad6f9-678">Stub SO_REUSEPORT & Ajout de prise en charge pour SO_PASSCRED pour les sockets netlink [69 GH]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-678">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="ad6f9-679">Retourner différents codes d’erreur à partir de RegisterDistribuiton si une distribution est actuellement installée ou désinstallée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-679">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="ad6f9-680">Autoriser la désinscription des distributions de WSL partiellement installées via wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-680">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="ad6f9-681">Corriger le blocage de test de socket python à partir de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="ad6f9-681">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="ad6f9-682">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-682">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-683">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-683">Console</span></span>
- <span data-ttu-id="ad6f9-684">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-684">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-685">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-685">LTP Results:</span></span>
<span data-ttu-id="ad6f9-686">Nombre total de Tests : 1904</span><span class="sxs-lookup"><span data-stu-id="ad6f9-686">Total Tests: 1904</span></span><br/>
<span data-ttu-id="ad6f9-687">Total ignoré des Tests : 209</span><span class="sxs-lookup"><span data-stu-id="ad6f9-687">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="ad6f9-688">Nombre total d’échecs : 229</span><span class="sxs-lookup"><span data-stu-id="ad6f9-688">Total Failures: 229</span></span><br/>
[<span data-ttu-id="ad6f9-689">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-689">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="ad6f9-690">Build 16257</span><span class="sxs-lookup"><span data-stu-id="ad6f9-690">Build 16257</span></span>

<span data-ttu-id="ad6f9-691">Pour Windows général plus d’informations sur la build 16257 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-691">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-692">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-693">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-693">WSL</span></span>
- <span data-ttu-id="ad6f9-694">Implémenter l’appel du système prlimit64</span><span class="sxs-lookup"><span data-stu-id="ad6f9-694">Implement prlimit64 system call</span></span>
- <span data-ttu-id="ad6f9-695">Ajouter la prise en charge pour ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-695">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="ad6f9-696">Stub MSG_MORE pour les sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-696">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="ad6f9-697">Corriger comportement de vecteur auxiliaires AT_EXECFN non valide [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-697">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="ad6f9-698">Corriger le comportement de copier/coller pour console/tty et ajouter de la mémoire tampon saturée une meilleure gestion des [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-698">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="ad6f9-699">Définissez AT_SECURE dans un vecteur auxiliaire pour les programmes de set-user-ID et set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-699">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="ad6f9-700">Point de terminaison maître pseudo-périphérique-Terminal Server ne gère ne pas TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-700">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="ad6f9-701">Correctif lseek effectue pour rembobiner des répertoires dans LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-701">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="ad6f9-702">/dev/ptmx se bloque après une utilisation élevée [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-702">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="ad6f9-703">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-703">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-704">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-704">Console</span></span>
- <span data-ttu-id="ad6f9-705">Correctif pour horizontal lignes/des traits de soulignement Everywhere [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-705">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="ad6f9-706">Correctif pour l’ordre de processus modifié NPM ce qui rend plus difficile à fermer [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-706">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="ad6f9-707">Ajouté à notre nouveau modèle de couleurs : https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="ad6f9-707">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-708">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-708">LTP Results:</span></span>
<span data-ttu-id="ad6f9-709">Aucune modification depuis 16251</span><span class="sxs-lookup"><span data-stu-id="ad6f9-709">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-710">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-710">Syscall Support</span></span>
<span data-ttu-id="ad6f9-711">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-711">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-712">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-712">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="ad6f9-713">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad6f9-713">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="ad6f9-714">Problème GitHub 2392 : Dossiers de Windows n’est ne pas reconnu par WSL...</span><span class="sxs-lookup"><span data-stu-id="ad6f9-714">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="ad6f9-715">Dans la build 16257, WSL présente des problèmes lors de l’énumération des fichiers/dossiers de Windows via `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-715">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="ad6f9-716">Ce problème a été résolu et doivent être libéré dans Insiders build pendant la semaine 14/8/2017.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-716">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="ad6f9-717">Build 16251</span><span class="sxs-lookup"><span data-stu-id="ad6f9-717">Build 16251</span></span>

<span data-ttu-id="ad6f9-718">Pour Windows général plus d’informations sur la build 16251 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-718">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-719">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-719">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-720">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-720">WSL</span></span>
- <span data-ttu-id="ad6f9-721">Supprimer la balise de version bêta de composant facultatif WSL, consultez [billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-721">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="ad6f9-722">Initialiser correctement enregistré-set uid et gid pour les fichiers binaires de set-user-ID et set-group-ID sur exec [962 GH 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-722">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="ad6f9-723">Prise en charge ajoutée pour ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-723">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="ad6f9-724">Prise en charge pour ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-724">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="ad6f9-725">Fixe ptrace pour arrêter des signaux ignoré</span><span class="sxs-lookup"><span data-stu-id="ad6f9-725">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="ad6f9-726">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-727">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-727">Console</span></span>
- <span data-ttu-id="ad6f9-728">Aucune Console les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-729">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-729">LTP Results:</span></span>
<span data-ttu-id="ad6f9-730">Nombre de Tests concluants : 768</span><span class="sxs-lookup"><span data-stu-id="ad6f9-730">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="ad6f9-731">Nombre de Tests ayant échoué : 244</span><span class="sxs-lookup"><span data-stu-id="ad6f9-731">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="ad6f9-732">Nombre de Tests ignorés : 96</span><span class="sxs-lookup"><span data-stu-id="ad6f9-732">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="ad6f9-733">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-733">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="ad6f9-734">Build 16241</span><span class="sxs-lookup"><span data-stu-id="ad6f9-734">Build 16241</span></span>

<span data-ttu-id="ad6f9-735">Pour Windows général plus d’informations sur la build 16241 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-735">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-736">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="ad6f9-737">WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-737">WSL</span></span>
- <span data-ttu-id="ad6f9-738">Aucun WSL les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-738">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="ad6f9-739">Console</span><span class="sxs-lookup"><span data-stu-id="ad6f9-739">Console</span></span>
- <span data-ttu-id="ad6f9-740">Correctif pour la sortie de caractères incorrect pour DEC lignes d’origine, signalé initialement [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-740">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="ad6f9-741">Correctif pour aucun texte de sortie qui est affiché dans la page de codes 65001 (UTF-8)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-741">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="ad6f9-742">Ne transférez pas les modifications apportées à un seul valeurs RVB à d’autres parties de la palette de la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-742">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="ad6f9-743">Cela fera la feuille de propriétés de console beaucoup plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-743">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="ad6f9-744">CTRL + S ne semble pas fonctionner correctement</span><span class="sxs-lookup"><span data-stu-id="ad6f9-744">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="ad6f9-745">Non gras /-Dim complètement absent à partir des codes d’échappement ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-745">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="ad6f9-746">Console ne correctement prendre en charge des thèmes de couleurs Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-746">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="ad6f9-747">Impossible de coller des caractères particuliers [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-747">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="ad6f9-748">Redimensionnement de redistribution interagit étrangement avec redimensionnement d’une fenêtre d’interpréteur de commandes lorsque les éléments se trouvent sur la ligne de commande/modifier [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-748">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="ad6f9-749">CTRL-L quitte l’écran dirty [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-749">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="ad6f9-750">Bogue de rendu de console lors de l’affichage VT sur HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-750">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="ad6f9-751">Caractères de la version japonaise paraître étranges avec un caractère Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-751">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="ad6f9-752">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-752">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="ad6f9-753">Build 16237</span><span class="sxs-lookup"><span data-stu-id="ad6f9-753">Build 16237</span></span>

<span data-ttu-id="ad6f9-754">Pour Windows général plus d’informations sur la build 16237 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-754">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-755">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-755">Fixed</span></span>
- <span data-ttu-id="ad6f9-756">Utiliser des attributs par défaut pour les fichiers sans EAs dans lxfs (racine, racine, 0000)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-756">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="ad6f9-757">Prise en charge pour les distributions qui utilisent des attributs étendus</span><span class="sxs-lookup"><span data-stu-id="ad6f9-757">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="ad6f9-758">Correctif de remplissage pour les entrées retournées par getdents et getdents64</span><span class="sxs-lookup"><span data-stu-id="ad6f9-758">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="ad6f9-759">Corriger la vérification des autorisations pour l’appel de système SHM_STAT shmctl [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-759">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="ad6f9-760">État fixe epoll initiale incorrect pour les TTY ne [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-760">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="ad6f9-761">Corriger readdir DrvFs ne pas renvoie toutes les entrées [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-761">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="ad6f9-762">Corriger LxFs readdir lorsque les fichiers sont dissocié [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-762">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="ad6f9-763">Autoriser les fichiers drvfs non liés à être rouverte via la commande procfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-763">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="ad6f9-764">Ajouté la substitution de clé de Registre global pour la désactivation des fonctionnalités WSL (interop / le montage du lecteur)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-764">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="ad6f9-765">Résoudre le nombre de blocs incorrect dans « stat » pour DrvFs (et LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-765">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="ad6f9-766">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-766">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="ad6f9-767">Build 16232</span><span class="sxs-lookup"><span data-stu-id="ad6f9-767">Build 16232</span></span>

<span data-ttu-id="ad6f9-768">Pour Windows général plus d’informations sur la build 16232 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-768">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-769">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-769">Fixed</span></span>
- <span data-ttu-id="ad6f9-770">Aucun WSL les modifications n’associées dans cette version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-770">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="ad6f9-771">Build 16226</span><span class="sxs-lookup"><span data-stu-id="ad6f9-771">Build 16226</span></span>

<span data-ttu-id="ad6f9-772">Pour Windows général plus d’informations sur la build 16226 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-772">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-773">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-773">Fixed</span></span>
- <span data-ttu-id="ad6f9-774">xattr liés prise en charge syscalls (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-774">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="ad6f9-775">prise en charge de Security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-775">security.capablity xattr support.</span></span>
- <span data-ttu-id="ad6f9-776">Une meilleure compatibilité avec certains systèmes de fichiers et les filtres, y compris les serveurs SMB non - MS.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-776">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="ad6f9-777">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-777">[GH #1952]</span></span>
- <span data-ttu-id="ad6f9-778">Prise en charge améliorée pour les espaces réservés de OneDrive, des espaces réservés GVFS et du système d’exploitation Compact des fichiers compressés.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-778">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="ad6f9-779">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-779">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="ad6f9-780">Build 16215</span><span class="sxs-lookup"><span data-stu-id="ad6f9-780">Build 16215</span></span>

<span data-ttu-id="ad6f9-781">Pour Windows général plus d’informations sur la build 16215 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-781">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-782">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-782">Fixed</span></span>
- <span data-ttu-id="ad6f9-783">WSL ne requiert plus le mode développeur.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-783">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="ad6f9-784">Prend en charge les jonctions de répertoires dans drvfs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-784">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="ad6f9-785">Gérer la désinstallation des packages appx de distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-785">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="ad6f9-786">Mise à jour de commande procfs pour afficher privés et partagés des mappages.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-786">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="ad6f9-787">Ajoutez la possibilité pour wslconfig.exe nettoyer les distributions qui sont partiellement installées ou désinstallées.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-787">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="ad6f9-788">Prise en charge ajoutée pour IP_MTU_DISCOVER pour les sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-788">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="ad6f9-789">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-789">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="ad6f9-790">Déduire la famille de protocoles pour les itinéraires à AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-790">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="ad6f9-791">Améliorations de l’appareil de série [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="ad6f9-791">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="ad6f9-792">Build 16199</span><span class="sxs-lookup"><span data-stu-id="ad6f9-792">Build 16199</span></span>

<span data-ttu-id="ad6f9-793">Pour Windows général plus d’informations sur la build 16199 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-793">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-794">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-794">Fixed</span></span>
- <span data-ttu-id="ad6f9-795">Aucun WSL les modifications n’associées dans ces versions.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-795">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="ad6f9-796">Build 16193</span><span class="sxs-lookup"><span data-stu-id="ad6f9-796">Build 16193</span></span>

<span data-ttu-id="ad6f9-797">Pour Windows général plus d’informations sur la build 16193 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-797">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-798">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-798">Fixed</span></span>
- <span data-ttu-id="ad6f9-799">Condition de concurrence entre les envois de SIGCONT et un threadgroup fin d’exécution [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-799">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="ad6f9-800">modifier les appareils tty et pty au rapport FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-800">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="ad6f9-801">Correctif SSH pour IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="ad6f9-801">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="ad6f9-802">Déplacé le montage DrvFs init démon [1862 Hg, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-802">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="ad6f9-803">Prise en charge dans DrvFs pour les liens symboliques de NT.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-803">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="ad6f9-804">Build 16184</span><span class="sxs-lookup"><span data-stu-id="ad6f9-804">Build 16184</span></span>

<span data-ttu-id="ad6f9-805">Pour Windows général plus d’informations sur la build 16184 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-805">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-806">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-806">Fixed</span></span>
- <span data-ttu-id="ad6f9-807">Supprimer la tâche de maintenance de package apt (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-807">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="ad6f9-808">Sortie fixe ne s’affichent ne pas dans des processus Windows dans node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-808">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="ad6f9-809">Assouplir les conditions d’alignement dans lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-809">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="ad6f9-810">Correction de la gestion de l’indicateur AT_EMPTY_PATH dans un nombre d’appels système.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-810">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="ad6f9-811">Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts provoquera le fichier un comportement non défini [GH 544,966,1357,1535,1615]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-811">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="ad6f9-812">/ etc/hosts hérite désormais les entrées à partir du fichier d’hôtes Windows (% windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-812">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="ad6f9-813">Build 16179</span><span class="sxs-lookup"><span data-stu-id="ad6f9-813">Build 16179</span></span>

<span data-ttu-id="ad6f9-814">Pour Windows général plus d’informations sur la build 16179 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-814">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-815">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-815">Fixed</span></span>
- <span data-ttu-id="ad6f9-816">Aucune modification WSL cette semaine.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-816">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="ad6f9-817">Build 16176</span><span class="sxs-lookup"><span data-stu-id="ad6f9-817">Build 16176</span></span>

<span data-ttu-id="ad6f9-818">Pour Windows général plus d’informations sur la build 16176 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-818">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-819">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-819">Fixed</span></span>

- [<span data-ttu-id="ad6f9-820">Prise en charge de la série est activée</span><span class="sxs-lookup"><span data-stu-id="ad6f9-820">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="ad6f9-821">Option de socket ajoutée IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-821">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="ad6f9-822">Implémenté pwritev (fonction) (lors du téléchargement du fichier à nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-822">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="ad6f9-823">Ajouté des options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-823">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="ad6f9-824">Prise en charge pour l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-824">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="ad6f9-825">Option de socket IP (V6) _MTU ajoutée pour le nœud applications, détermination d’itinéraire, dig, nslookup, hôte</span><span class="sxs-lookup"><span data-stu-id="ad6f9-825">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="ad6f9-826">Option de socket ajoutée IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="ad6f9-826">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="ad6f9-827">Améliorations du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="ad6f9-827">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="ad6f9-828">Autoriser le montage des chemins d’accès UNC</span><span class="sxs-lookup"><span data-stu-id="ad6f9-828">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="ad6f9-829">Activer la prise en charge CDFS dans drvfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-829">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="ad6f9-830">Gérer correctement les autorisations pour les systèmes de fichiers réseau dans drvfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-830">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="ad6f9-831">Ajouter la prise en charge pour les lecteurs à distance à drvfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-831">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="ad6f9-832">Activer FAT prennent en charge dans drvfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-832">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="ad6f9-833">Autres correctifs et améliorations</span><span class="sxs-lookup"><span data-stu-id="ad6f9-833">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-834">Résultats LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-834">LTP Results</span></span>
<span data-ttu-id="ad6f9-835">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="ad6f9-835">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="ad6f9-836">Build 16170</span><span class="sxs-lookup"><span data-stu-id="ad6f9-836">Build 16170</span></span>

<span data-ttu-id="ad6f9-837">Pour Windows général plus d’informations sur la build 16170 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-837">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="ad6f9-838">Nous avons publié un nouveau [billet de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) traitant de nos efforts pour tester WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-838">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="ad6f9-839">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-839">Fixed</span></span>

- <span data-ttu-id="ad6f9-840">Socket de prise en charge option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-840">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="ad6f9-841">Ajouter la prise en charge pour PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-841">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="ad6f9-842">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-842">[GH 1692]</span></span>
- <span data-ttu-id="ad6f9-843">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-843">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-844">Résultats LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-844">LTP Results</span></span>
<span data-ttu-id="ad6f9-845">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="ad6f9-845">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="ad6f9-846">Build 15046 vers Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="ad6f9-846">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="ad6f9-847">Il existe plus aucune WSL correctifs ou les fonctionnalités prévues pour être inclus dans la mise à jour Windows 10 Creators.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-847">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="ad6f9-848">Notes de publication pour WSL reprendra dans les semaines à venir pour les ajouts de ciblage de la prochaine mise à jour Windows majeures.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-848">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="ad6f9-849">Pour Windows général plus d’informations sur la build 15046 et Insider futures versions visite le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-849">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="ad6f9-850">Build 15042</span><span class="sxs-lookup"><span data-stu-id="ad6f9-850">Build 15042</span></span>

<span data-ttu-id="ad6f9-851">Pour Windows général plus d’informations sur la build 15042 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-851">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-852">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-852">Fixed</span></span>

- <span data-ttu-id="ad6f9-853">Correction d’un blocage lors de la suppression d’un chemin d’accès se terminant par «... »</span><span class="sxs-lookup"><span data-stu-id="ad6f9-853">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="ad6f9-854">Correction d’un problème où FIONBIO ne pas retourner 0 en cas de réussite [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-854">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="ad6f9-855">Correction d’un problème avec des lectures de longueur nulle de sockets de datagramme inet</span><span class="sxs-lookup"><span data-stu-id="ad6f9-855">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="ad6f9-856">Résoudre un blocage possible en raison d’une condition de concurrence dans drvfs inode recherche [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-856">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="ad6f9-857">Prise en charge pour les données connexes de socket unix ; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-857">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="ad6f9-858">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-858">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-859">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-859">LTP Results:</span></span>
<span data-ttu-id="ad6f9-860">Nombre de Test réussi : 737</span><span class="sxs-lookup"><span data-stu-id="ad6f9-860">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="ad6f9-861">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="ad6f9-861">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="ad6f9-862">Build 15031</span><span class="sxs-lookup"><span data-stu-id="ad6f9-862">Build 15031</span></span>

<span data-ttu-id="ad6f9-863">Pour Windows général plus d’informations sur la build 15031 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-863">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-864">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-864">Fixed</span></span>

- <span data-ttu-id="ad6f9-865">Correction d’un bogue où time(2) est sporadique mener.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-865">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="ad6f9-866">Fixe et émettre où \* SIGPROCMASK syscalls peut endommager le masque de signal.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-866">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="ad6f9-867">Maintenant retourner la longueur de ligne de commande complète dans la notification de la création de processus WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-867">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="ad6f9-868">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-868">[GH 1632]</span></span>
- <span data-ttu-id="ad6f9-869">WSL signale désormais la sortie du thread via ptrace pour les blocages GDB.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-869">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="ad6f9-870">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-870">[GH 1196]</span></span>
- <span data-ttu-id="ad6f9-871">Correction du bogue où se bloquait ptys après tmux importante d’e/s.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-871">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="ad6f9-872">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-872">[GH 1358]</span></span>
- <span data-ttu-id="ad6f9-873">Validation du délai d’expiration fixe dans un grand nombre d’appels système (futex, semtimedop, ppoll, sigtimewait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-873">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="ad6f9-874">Prise en charge EFD_SEMAPHORE eventfd ajout [GH 452]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-874">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="ad6f9-875">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-875">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-876">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-876">LTP Results:</span></span>
<span data-ttu-id="ad6f9-877">Nombre de Test réussi : 737</span><span class="sxs-lookup"><span data-stu-id="ad6f9-877">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="ad6f9-878">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="ad6f9-878">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="ad6f9-879">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-879">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="ad6f9-880">Build 15025</span><span class="sxs-lookup"><span data-stu-id="ad6f9-880">Build 15025</span></span>

<span data-ttu-id="ad6f9-881">Pour Windows général plus d’informations sur la build 15025 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-881">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-882">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-882">Fixed</span></span>

- <span data-ttu-id="ad6f9-883">Correctif pour bogue que grep ne 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-883">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="ad6f9-884">Indicateur EFD_SEMAPHORE implémentée pour syscall eventfd2 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-884">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="ad6f9-885">Implémenté/proc / [pid] / net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="ad6f9-886">Signal contrôlée par la prise en charge d’e/s pour les sockets de flux unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-886">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="ad6f9-887">Prendre en charge F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-887">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="ad6f9-888">Implémenter recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-888">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="ad6f9-889">Correction du bogue où les epoll_wait() n’a pas été en attente [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-889">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="ad6f9-890">Implement /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="ad6f9-890">Implement /proc/version_signature</span></span>
- <span data-ttu-id="ad6f9-891">Tee syscall retourne maintenant échec si les deux descripteurs de fichier font référence au même canal</span><span class="sxs-lookup"><span data-stu-id="ad6f9-891">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="ad6f9-892">Comportement correct implémentée pour SO_PEERCRED pour les sockets Unix</span><span class="sxs-lookup"><span data-stu-id="ad6f9-892">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="ad6f9-893">Gestion des paramètres non valides de syscall tkill fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-893">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="ad6f9-894">Modifications pour augmenter la preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-894">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="ad6f9-895">Correctif mineur pour le blocage des e/s de Ruby</span><span class="sxs-lookup"><span data-stu-id="ad6f9-895">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="ad6f9-896">Fixe recvmsg() retour EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-896">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="ad6f9-897">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-897">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-898">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-898">LTP Results:</span></span>
<span data-ttu-id="ad6f9-899">Nombre de Test réussi : 732</span><span class="sxs-lookup"><span data-stu-id="ad6f9-899">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="ad6f9-900">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="ad6f9-900">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="ad6f9-901">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-901">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="ad6f9-902">Build 15019</span><span class="sxs-lookup"><span data-stu-id="ad6f9-902">Build 15019</span></span>

<span data-ttu-id="ad6f9-903">Pour Windows général plus d’informations sur la build 15019 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-903">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-904">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-904">Fixed</span></span>

- <span data-ttu-id="ad6f9-905">Correction du bogue qui est signalé à tort l’utilisation du processeur dans commande procfs pour des outils comme htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-905">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="ad6f9-906">Lors de l’appel open() avec O_TRUNC sur un fichier inotify génère désormais IN_MODIFY avant IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="ad6f9-906">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="ad6f9-907">Correctifs pour unix socket getsockopt SO_ERROR pour activer postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="ad6f9-907">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="ad6f9-908">Implémenter /proc/sys/net/core/somaxconn pour le langage GO</span><span class="sxs-lookup"><span data-stu-id="ad6f9-908">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="ad6f9-909">Tâche d’arrière-plan apt-get package mise à jour s’exécute désormais masqué à partir de la vue</span><span class="sxs-lookup"><span data-stu-id="ad6f9-909">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="ad6f9-910">Étendue clair pour ipv6 localhost (Spring-Framework(Java) échec).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-910">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="ad6f9-911">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-911">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-912">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-912">LTP Results:</span></span>
<span data-ttu-id="ad6f9-913">Nombre de Test réussi : 714</span><span class="sxs-lookup"><span data-stu-id="ad6f9-913">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="ad6f9-914">Nombre de cas d’échec (échec, ignoré, etc....) : 249</span><span class="sxs-lookup"><span data-stu-id="ad6f9-914">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="ad6f9-915">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-915">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="ad6f9-916">Build 15014</span><span class="sxs-lookup"><span data-stu-id="ad6f9-916">Build 15014</span></span>

<span data-ttu-id="ad6f9-917">Pour Windows général plus d’informations sur la build 15014 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-917">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-918">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-918">Fixed</span></span>

- <span data-ttu-id="ad6f9-919">CTRL + C fonctionne désormais comme prévu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-919">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="ad6f9-920">htop et ps auxw maintenant afficher correct l’utilisation des ressources (GH #516)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-920">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="ad6f9-921">Traduction de base des exceptions de NT aux signaux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-921">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="ad6f9-922">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-922">(GH #513)</span></span>
- <span data-ttu-id="ad6f9-923">fallocate échoue avec ENOSPC alors EINVAL (GH #1571) au lieu de l’espace est insuffisant</span><span class="sxs-lookup"><span data-stu-id="ad6f9-923">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="ad6f9-924">/Proc/sys/kernel/sem ajouté.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-924">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="ad6f9-925">Appels de système semop et semtimedop implémentées</span><span class="sxs-lookup"><span data-stu-id="ad6f9-925">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="ad6f9-926">Erreurs nslookup fixe avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (69 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-926">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="ad6f9-927">Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="ad6f9-927">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="ad6f9-928">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-928">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-929">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-929">LTP Results:</span></span>
<span data-ttu-id="ad6f9-930">Nombre de Test réussi : 709</span><span class="sxs-lookup"><span data-stu-id="ad6f9-930">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="ad6f9-931">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="ad6f9-931">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="ad6f9-932">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-932">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="ad6f9-933">Résumé de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-933">Syscall Summary</span></span>
<span data-ttu-id="ad6f9-934">Syscalls total : 384</span><span class="sxs-lookup"><span data-stu-id="ad6f9-934">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="ad6f9-935">Total implémenté : 235</span><span class="sxs-lookup"><span data-stu-id="ad6f9-935">Total Implemented: 235</span></span> </br>
<span data-ttu-id="ad6f9-936">Nombre total de l’objet d’un stub : 22</span><span class="sxs-lookup"><span data-stu-id="ad6f9-936">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="ad6f9-937">Total non implémenté : 127</span><span class="sxs-lookup"><span data-stu-id="ad6f9-937">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="ad6f9-938">Analyse détaillée</span><span class="sxs-lookup"><span data-stu-id="ad6f9-938">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="ad6f9-939">Build 15007</span><span class="sxs-lookup"><span data-stu-id="ad6f9-939">Build 15007</span></span>

<span data-ttu-id="ad6f9-940">Pour Windows général plus d’informations sur la build 15007 visitez le [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-940">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="ad6f9-941">Problème connu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-941">Known Issue</span></span>

- <span data-ttu-id="ad6f9-942">Il existe un bogue connu dans lequel la console ne reconnaît pas certains Ctrl + <key> d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-942">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="ad6f9-943">Cela inclut la commande ctrl-c qui agira comme un keypress « c » normal.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-943">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="ad6f9-944">Solution : Mapper une autre clé à Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-944">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="ad6f9-945">Par exemple, Ctrl + K, Ctrl + c faire pour mapper : `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-945">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="ad6f9-946">Ce mappage s’effectue par terminal et devra être fait *chaque* bash de temps est lancée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-946">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="ad6f9-947">Les utilisateurs peuvent Explorer la possibilité d’inclure cela dans leurs `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="ad6f9-947">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="ad6f9-948">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-948">Fixed</span></span>

- <span data-ttu-id="ad6f9-949">Correction du problème où en cours d’exécution WSL consomme 100 % d’un cœur de processeur</span><span class="sxs-lookup"><span data-stu-id="ad6f9-949">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="ad6f9-950">Option IP_PKTINFO, IPV6_RECVPKTINFO désormais pris en charge de socket.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-950">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="ad6f9-951">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-951">(GH #851, 987)</span></span>
- <span data-ttu-id="ad6f9-952">Tronquer l’adresse d’interface réseau physique à 16 octets lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-952">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="ad6f9-953">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-954">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-954">LTP Results:</span></span>
<span data-ttu-id="ad6f9-955">Nombre de Test réussi : 709</span><span class="sxs-lookup"><span data-stu-id="ad6f9-955">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="ad6f9-956">Nombre de cas d’échec (échec, ignoré, etc....) : 255</span><span class="sxs-lookup"><span data-stu-id="ad6f9-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="ad6f9-957">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="ad6f9-958">Build 15002</span><span class="sxs-lookup"><span data-stu-id="ad6f9-958">Build 15002</span></span>

<span data-ttu-id="ad6f9-959">Pour Windows général plus d’informations sur la build 15002 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-959">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="ad6f9-960">Problème connu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-960">Known Issue</span></span>

<span data-ttu-id="ad6f9-961">Deux problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-961">Two known issues:</span></span>
- <span data-ttu-id="ad6f9-962">Il existe un bogue connu dans lequel la console ne reconnaît pas certains Ctrl + <key> d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-962">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="ad6f9-963">Cela inclut la commande ctrl-c qui agira comme un keypress « c » normal.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-963">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="ad6f9-964">Solution : Mapper une autre clé à Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-964">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="ad6f9-965">Par exemple, Ctrl + K, Ctrl + c faire pour mapper : `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-965">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="ad6f9-966">Ce mappage s’effectue par terminal et devra être fait *chaque* bash de temps est lancée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-966">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="ad6f9-967">Les utilisateurs peuvent Explorer la possibilité d’inclure cela dans leurs `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="ad6f9-967">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="ad6f9-968">Pendant l’exécution de WSL un thread système consomme 100 % d’un cœur de processeur.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-968">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="ad6f9-969">La cause racine a été adressée et fixe en interne.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-969">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="ad6f9-970">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-970">Fixed</span></span>

- <span data-ttu-id="ad6f9-971">Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-971">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="ad6f9-972">Vous essayez de démarrer une session à un autre niveau sera bloquée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-972">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="ad6f9-973">Cela signifie que les consoles administrateur et non-administrateur ne peut pas s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-973">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="ad6f9-974">(#626 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-974">(GH #626)</span></span>
<br/>
- <span data-ttu-id="ad6f9-975">Implémenté les messages NETLINK_ROUTE suivants (exige un administrateur de Windows)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-975">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="ad6f9-976">RTM_NEWADDR (prend en charge `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-976">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="ad6f9-977">RTM_NEWROUTE (prend en charge `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-977">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="ad6f9-978">RTM_DELADDR (prend en charge `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-978">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="ad6f9-979">RTM_DELROUTE (prend en charge `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-979">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="ad6f9-980">Vérification des packages à mettre à jour de tâche planifiée ne s’est plus sur une connexion limitée (GH # 1 371)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-980">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="ad6f9-981">Correction d’erreur dans lequel tuyauterie obtient bloquée par exemple, c - bash « ls - alR / » | Bash -c « cat » (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-981">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="ad6f9-982">Option de socket TCP_KEEPCNT implémentée (GH #843)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-982">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="ad6f9-983">Option de socket IP_MTU_DISCOVER INET implémentée (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-983">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="ad6f9-984">Supprimé des fonctionnalités héritées pour exécuter des fichiers binaires de NT à partir d’init avec la recherche de chemin d’accès de NT.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-984">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="ad6f9-985">(#1325 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-985">(GH #1325)</span></span>
- <span data-ttu-id="ad6f9-986">Corriger le mode de/dev/kmsg pour autoriser l’accès de lecture de groupe / autre (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-986">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="ad6f9-987">/Proc/sys/kernel/random/uuid implémentée (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-987">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="ad6f9-988">Correction d’erreur où l’heure de début de processus n’affiche qu’année 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-988">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="ad6f9-989">Variable d’environnement terme par défaut commuté xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-989">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="ad6f9-990">Modifié la façon dont les processus de validation est calculée pendant la duplication du processus.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-990">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="ad6f9-991">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-991">(GH #1286)</span></span>
- <span data-ttu-id="ad6f9-992">/Proc/sys/vm/overcommit_memory implémentée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-992">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="ad6f9-993">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-993">(GH #1286)</span></span>
- <span data-ttu-id="ad6f9-994">Fichier /proc/net/route implémentée (GH #69)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-994">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="ad6f9-995">Correction de l’erreur où nom raccourci a été correctement localisés (GH #696)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-995">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="ad6f9-996">Elf fixe logique qui est incorrectement la validation des en-têtes de programme d’analyse doit être inférieur (ou égal à) PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-996">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="ad6f9-997">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-997">(GH #1048)</span></span>
- <span data-ttu-id="ad6f9-998">Rappel statfs implémentée pour la commande procfs, sysfs cgroupfs et binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-998">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="ad6f9-999">Windows AptPackageIndexUpdate fixes qui ne se ferme pas (GH #1184, également abordées dans GH #1193)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-999">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="ad6f9-1000">Prise en charge ADDR_NO_RANDOMIZE du personnalité ASLR ajouté.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1000">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="ad6f9-1001">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1001">(GH #1148, 1128)</span></span>
- <span data-ttu-id="ad6f9-1002">PTRACE_GETSIGINFO améliorée, SIGSEGV, pour les traces de pile gdb appropriée pendant AV (875 de # Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1002">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="ad6f9-1003">ELF l’analyse n’est plus échoue pour les fichiers binaires patchelf.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1003">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="ad6f9-1004">(#471 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1004">(GH #471)</span></span>
- <span data-ttu-id="ad6f9-1005">VPN DNS propagées à /etc/resolv.conf (GH #416 1350)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1005">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="ad6f9-1006">Améliorations apportées à TCP fermer pour le transfert de données plus fiable.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1006">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="ad6f9-1007">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1007">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="ad6f9-1008">Code d’erreur correct retournent désormais lorsque trop de fichiers est ouverts (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1008">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="ad6f9-1009">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1009">(GH #1126, 2090)</span></span>
- <span data-ttu-id="ad6f9-1010">Rapports d’Audit de Windows journal maintenant nom de l’image dans le processus de création d’audit.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1010">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="ad6f9-1011">Échouer normalement lors du lancement bash.exe à partir d’une fenêtre d’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1011">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="ad6f9-1012">Message d’erreur ajoutés lorsque l’interopérabilité ne parvient pas à accéder à un répertoire de travail sous LxFs (par exemple, notepad.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1012">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="ad6f9-1013">Résolution du problème où le chemin d’accès Windows a été tronquée dans WSL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1013">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="ad6f9-1014">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1015">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1015">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1016">Nombre de Test réussi : 690</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1016">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="ad6f9-1017">Nombre de cas d’échec (échec, ignoré, etc....) : 274</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1017">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="ad6f9-1018">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1019">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1019">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1020">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1020">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1021">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1021">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="ad6f9-1022">Build 14986</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1022">Build 14986</span></span>

<span data-ttu-id="ad6f9-1023">Pour Windows général plus d’informations sur la build 14986 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1023">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1024">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1024">Fixed</span></span>

- <span data-ttu-id="ad6f9-1025">Correction de bogues avec Netlink et Pty IOCTL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1025">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="ad6f9-1026">Version du noyau signale désormais 4.4.0-43 par souci de cohérence avec Xenial</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1026">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="ad6f9-1027">Bash.exe lance maintenant lorsque l’entrée dirigée vers ' nul :' (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1027">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="ad6f9-1028">ID de thread signalés désormais correctement dans la commande procfs (#967 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1028">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="ad6f9-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Indicateurs IN_ISDIR désormais pris en charge dans inotify_add_watch() (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="ad6f9-1030">Implémentez timer_create et les appels système associées.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1030">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="ad6f9-1031">Cela permet la prise en charge GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1031">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="ad6f9-1032">Résolution du problème où ping retourné un temps de 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1032">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="ad6f9-1033">Retourne le code d’erreur approprié lorsque trop de fichiers est ouverts.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1033">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="ad6f9-1034">Résolution du problème dans WSL où demande Netlink pour les données de l’interface réseau échoue avec EINVAL si l’adresse matérielle de l’interface est de 32 octets (par exemple, l’interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1034">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="ad6f9-1035">Notez que l’utilitaire de Linux « ip » contient un bogue dans lequel il se bloque si WSL signale une adresse matérielle de 32 octets.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1035">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="ad6f9-1036">Il s’agit d’un bogue dans « ip », pas WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1036">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="ad6f9-1037">Le « ip » utilitaire code en dur la longueur de la mémoire tampon de chaîne utilisée pour imprimer l’adresse de matériel, et cette mémoire tampon est trop petit pour imprimer une adresse matérielle de 32 octets.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1037">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="ad6f9-1038">Améliorations et correctifs supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1038">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1039">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1039">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1040">Nombre de Test réussi : 669</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1040">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="ad6f9-1041">Nombre de cas d’échec (échec, ignoré, etc....) : 258</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1041">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="ad6f9-1042">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1042">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1043">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1043">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1044">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1044">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1045">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1045">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="ad6f9-1046">Build 14971</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1046">Build 14971</span></span>

<span data-ttu-id="ad6f9-1047">Pour Windows général plus d’informations sur la build 14971 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1047">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1048">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1048">Fixed</span></span>

 - <span data-ttu-id="ad6f9-1049">En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1049">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="ad6f9-1050">Mises à jour régulièrement planifiées reprendra à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1050">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1051">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1051">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1052">Inchangé depuis 14965</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1052">Unchanged from 14965</span></span> </br>
<span data-ttu-id="ad6f9-1053">Nombre de Test réussi : 664</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1053">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="ad6f9-1054">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1054">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1055">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="ad6f9-1056">Build 14965</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1056">Build 14965</span></span>

<span data-ttu-id="ad6f9-1057">Pour Windows général plus d’informations sur la build 14965 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1057">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1058">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1058">Fixed</span></span>

- <span data-ttu-id="ad6f9-1059">Prise en charge de Netlink des sockets du protocole NETLINK_ROUTE RTM_GETLINK et RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1059">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="ad6f9-1060">Permet aux commandes ifconfig et l’adresse ip pour l’énumération de réseau</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1060">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="ad6f9-1061">Vous trouverez plus d’informations dans nos [WSL mise en réseau de billet de blog](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1061">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="ad6f9-1062">/sbin est désormais dans le chemin de l’utilisateur par défaut</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1062">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="ad6f9-1063">Chemin d’accès de l’utilisateur NT maintenant ajouté pour le chemin d’accès WSL par défaut (par exemple, vous pouvez désormais taper notepad.exe sans ajouter System32 dans le chemin d’accès Linux)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1063">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="ad6f9-1064">Prise en charge ajoutée pour /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1064">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="ad6f9-1065">Les fichiers binaires de NT peut maintenant être lancées depuis WSL lorsque le répertoire de travail actuel contient des caractères non-ansi (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1065">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="ad6f9-1066">Autoriser l’arrêt sur un socket de flux de données déconnecté unix.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1066">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="ad6f9-1067">Prise en charge ajoutée pour PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1067">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="ad6f9-1068">Prise en charge ajoutée pour CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1068">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="ad6f9-1069">Correction d’erreur dans lequel tuyauterie obtient bloquée par exemple, c - bash « ls - alR / » | Bash -c « cat » (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1069">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="ad6f9-1070">Demandes de handle de connexion vers le terminal actuel.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1070">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="ad6f9-1071">Marquer/proc /<pid>/oom_score_adj comme accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1071">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="ad6f9-1072">Ajouter un dossier de /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1072">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="ad6f9-1073">sched_setaffinity doit renvoyer le nombre de masque de bits d’affinité</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1073">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="ad6f9-1074">Corriger la logique de validation ELF qui incorrectement suppose de chemins d’accès de l’interpréteur doivent comporter moins de 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1074">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="ad6f9-1075">(#743 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1075">(GH #743)</span></span>
- <span data-ttu-id="ad6f9-1076">Descripteurs de fichiers ouverts peuvent conserver la fenêtre de console ouverte (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1076">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="ad6f9-1077">Erreur Fixeed où rename() a échoué avec barre oblique sur le nom de la cible (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1077">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="ad6f9-1078">Implémenter /proc/net/dev fichier</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1078">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="ad6f9-1079">0.000ms fixe effectue un test ping en raison de la résolution du chronomètre.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1079">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="ad6f9-1080">/Proc/self/environ implémentée (GH #730)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1080">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="ad6f9-1081">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1081">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1082">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1082">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1083">Nombre de Test réussi : 664</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1083">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="ad6f9-1084">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1084">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1085">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1085">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="ad6f9-1086">Build 14959</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1086">Build 14959</span></span>

<span data-ttu-id="ad6f9-1087">Pour Windows général plus d’informations sur la build 14959 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1087">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1088">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1088">Fixed</span></span>

- <span data-ttu-id="ad6f9-1089">Notification Pico processus amélioré pour Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1089">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="ad6f9-1090">Des informations supplémentaires disponibles sur le [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1090">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="ad6f9-1091">Stabilité améliorée avec l’interopérabilité de Windows</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1091">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="ad6f9-1092">Correction de l’erreur 0 x 80070057 lors du lancement bash.exe lorsque la Protection de données d’entreprise (EDP) est activée</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1092">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="ad6f9-1093">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1093">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1094">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1094">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1095">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1095">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="ad6f9-1096">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1096">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1097">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1097">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="ad6f9-1098">Build 14955</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1098">Build 14955</span></span>

<span data-ttu-id="ad6f9-1099">Pour Windows général plus d’informations sur la build 14955 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1099">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1100">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1100">Fixed</span></span>

 - <span data-ttu-id="ad6f9-1101">En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1101">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="ad6f9-1102">Mises à jour régulièrement planifiées reprendra à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1102">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1103">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1103">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1104">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="ad6f9-1105">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1106">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="ad6f9-1107">Build 14951</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1107">Build 14951</span></span>

<span data-ttu-id="ad6f9-1108">Pour Windows général plus d’informations sur la build 14951 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1108">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="ad6f9-1109">Nouvelle fonctionnalité : Windows / Ubuntu interopérabilité</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1109">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="ad6f9-1110">Les fichiers binaires Windows peuvent maintenant être appelées directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1110">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="ad6f9-1111">Cela permet aux utilisateurs d’interagir avec leur environnement de Windows et le système d’une manière qui n’a pas été possible.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1111">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="ad6f9-1112">Exemple rapide, il est désormais possible pour les utilisateurs à exécuter les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1112">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="ad6f9-1113">Vous trouverez plus d’informations sur :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1113">More information can be found at:</span></span>

- [<span data-ttu-id="ad6f9-1114">Blog de l’équipe WSL pour l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1114">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="ad6f9-1115">Documentation Interop MSDN</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1115">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1116">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1116">Fixed</span></span>

- <span data-ttu-id="ad6f9-1117">Ubuntu 16.04 (Xenial) est maintenant installé pour toutes les nouvelles instances WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1117">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="ad6f9-1118">Les utilisateurs avec des instances (fidèle) 14.04 existantes ne seront pas mis à niveau automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1118">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="ad6f9-1119">Paramètres régionaux définis lors de l’installation sont maintenant affichée.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1119">Locale set during install is now displayed</span></span>
- <span data-ttu-id="ad6f9-1120">Améliorations de Terminal Server, y compris le bogue où rediriger un processus WSL vers un fichier ne pas toujours fonctionner</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1120">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="ad6f9-1121">Durée de vie de console doit être liée à la durée de vie bash.exe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1121">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="ad6f9-1122">Taille de fenêtre de console doit utiliser la taille visible, taille de mémoire tampon pas</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1122">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="ad6f9-1123">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1123">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1124">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1124">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1125">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1125">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="ad6f9-1126">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1126">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1127">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1127">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="ad6f9-1128">Build 14946</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1128">Build 14946</span></span>

<span data-ttu-id="ad6f9-1129">Pour Windows général plus d’informations sur la build 14946 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1129">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1130">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1130">Fixed</span></span>

- <span data-ttu-id="ad6f9-1131">Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT qui contiennent des espaces ou des guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1131">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="ad6f9-1132">Modification VolFs et DrvFs pour retourner 0 pour le nombre de liens de l’annuaire dans stat</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1132">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="ad6f9-1133">Prend en charge l’option de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1133">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="ad6f9-1134">Limiter à une seule console boucle d’e/s par tty.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1134">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="ad6f9-1135">Exemple : la commande suivante est possible :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1135">Example: the following command is possible:</span></span>
  - <span data-ttu-id="ad6f9-1136">Bash -c « echo data » | Bash - c « ssh user@example.com ' cat > foo.txt » »</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="ad6f9-1137">Remplacez les espaces par des tabulations dans /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1137">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="ad6f9-1138">DrvFs apparaît désormais dans mountinfo avec un nom qui correspond au volume de Windows monté</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1138">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="ad6f9-1139">/Home et/root apparaissent désormais dans mountinfo avec les noms corrects</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1139">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="ad6f9-1140">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1140">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1141">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1141">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1142">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1142">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="ad6f9-1143">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1143">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1144">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1144">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="ad6f9-1145">Build 14942</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1145">Build 14942</span></span>

<span data-ttu-id="ad6f9-1146">Pour Windows général plus d’informations sur la build 14942 visitez le [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1146">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1147">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1147">Fixed</span></span>

- <span data-ttu-id="ad6f9-1148">Un nombre de bogues résolus, y compris la » a TENTÉ de s’exécuter de PasExécution ne peut être mémoire « incident qui a été blocage SSH de mise en réseau</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1148">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="ad6f9-1149">inotifiy prise en charge pour les notifications générées à partir d’applications Windows sur DrvFs est présent dans</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1149">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="ad6f9-1150">Implémenter TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1150">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="ad6f9-1151">(#695 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1151">(GH #695)</span></span>
- <span data-ttu-id="ad6f9-1152">Implémenter l’appel système pivot_root</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1152">Implement the pivot_root system call</span></span>
- <span data-ttu-id="ad6f9-1153">Implémenter l’option de socket pour SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1153">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="ad6f9-1154">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1154">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1155">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1155">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1156">Nombre de Test réussi : 665</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1156">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="ad6f9-1157">Nombre de cas d’échec (échec, ignoré, etc....) : 263</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="ad6f9-1158">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1159">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1159">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1160">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1160">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1161">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1161">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="ad6f9-1162">Build 14936</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1162">Build 14936</span></span>

<span data-ttu-id="ad6f9-1163">Pour Windows général plus d’informations sur la build 14936 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1163">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="ad6f9-1164">Remarque: WSL va installer Ubuntu version 16.04 (Xenial) au lieu d’Ubuntu 14.04 (fidèle) dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1164">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="ad6f9-1165">Cette modification s’applique pour les Insiders installation de nouvelles instances (lxrun.exe /install ou première exécution de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1165">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="ad6f9-1166">Les instances existantes avec fidèle ne seront pas mis à niveau automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1166">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="ad6f9-1167">Les utilisateurs peuvent mettre à niveau leur image fidèle à Xenial à l’aide de la commande-version-mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1167">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="ad6f9-1168">Problème connu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1168">Known Issue</span></span>
<span data-ttu-id="ad6f9-1169">WSL rencontre un problème avec certaines implémentations de socket.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1169">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="ad6f9-1170">La vérification d’erreur se manifeste comme un incident avec l’erreur « A TENTÉ de s’exécuter de PasExécution ne peut être mémoire ».</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1170">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="ad6f9-1171">La manifestation la plus commune de ce problème est un incident lors de l’utilisation de ssh.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1171">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="ad6f9-1172">La cause racine est fixe sur des versions internes et n’est adressée aux initiés dès que possible.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1172">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1173">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1173">Fixed</span></span>

- <span data-ttu-id="ad6f9-1174">Implémentation de l’appel système chroot</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1174">Implemented the chroot system call</span></span>
- <span data-ttu-id="ad6f9-1175">Améliorations dans inotify ~~, y compris la prise en charge pour les notifications générées à partir d’applications Windows sur DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1175">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="ad6f9-1176">Correction : Inotify prend en charge les modifications provenant d’applications Windows non disponibles pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1176">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="ad6f9-1177">Liaison à IPV6 de socket ::<port n> prend désormais en charge IPV6_V6ONLY (GH #68 #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1177">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="ad6f9-1178">Comportement WNOWAIT pour waitid systemcall implémenté (GH #638)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1178">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="ad6f9-1179">Prise en charge des options de socket IP IP_HDRINCL et IP_TTL</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1179">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="ad6f9-1180">Read() de longueur nulle doit retourner immédiatement (GH #975)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1180">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="ad6f9-1181">Gérer correctement les préfixes des noms de fichiers et le nom de fichier qui n’incluent pas une marque de fin NULL dans un fichier .tar.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1181">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="ad6f9-1182">prise en charge d’epoll de/dev/null</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1182">epoll support for /dev/null</span></span>
- <span data-ttu-id="ad6f9-1183">Corriger la source de temps /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1183">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="ad6f9-1184">Bash -c maintenant en mesure de rediriger vers un fichier</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1184">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="ad6f9-1185">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1185">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1186">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1186">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1187">Nombre de Test réussi : 664</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1187">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="ad6f9-1188">Nombre de cas d’échec (échec, ignoré, etc....) : 264</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1188">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="ad6f9-1189">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1189">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1190">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1190">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1191">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1191">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1192">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1192">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="ad6f9-1193">Build 14931</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1193">Build 14931</span></span>

<span data-ttu-id="ad6f9-1194">Pour Windows général plus d’informations sur la build 14931 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1194">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1195">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1195">Fixed</span></span>

 - <span data-ttu-id="ad6f9-1196">En raison de circonstances nous ne contrôlons ne contient aucune mise à jour cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1196">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="ad6f9-1197">Mises à jour régulièrement planifiées reprendra dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1197">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="ad6f9-1198">Build 14926</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1198">Build 14926</span></span>

<span data-ttu-id="ad6f9-1199">Pour Windows général plus d’informations sur la build 14926 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1199">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1200">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1200">Fixed</span></span>

- <span data-ttu-id="ad6f9-1201">Ping fonctionne désormais dans les consoles qui n’ont pas de privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1201">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="ad6f9-1202">Ping6 maintenant également pris en charge, sans privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1202">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="ad6f9-1203">Inotify prise en charge pour les fichiers modifiés via WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1203">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="ad6f9-1204">(#216 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1204">(GH #216)</span></span>
  - <span data-ttu-id="ad6f9-1205">Indicateurs pris en charge :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1205">Flags supported:</span></span>
    - <span data-ttu-id="ad6f9-1206">inotify_init1 : LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="ad6f9-1207">événements d’inotify_add_watch : LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1207">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="ad6f9-1208">attributs d’inotify_add_watch : LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1208">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="ad6f9-1209">lire la sortie : LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1209">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="ad6f9-1210">Problème connu : Modification des fichiers à partir d’applications de Windows ne génère pas d’événements</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1210">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="ad6f9-1211">Socket UNIX prend désormais en charge SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1211">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="ad6f9-1212">LTP résultats :</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1212">LTP Results:</span></span>
<span data-ttu-id="ad6f9-1213">Nombre de Test réussi : 651</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1213">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="ad6f9-1214">Nombre de cas d’échec (échec, ignoré, etc....) : 258</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1214">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="ad6f9-1215">Journaux de série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1215">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="ad6f9-1216">Build 14915</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1216">Build 14915</span></span>

<span data-ttu-id="ad6f9-1217">Pour Windows général plus d’informations sur la build 14915 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1217">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1218">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1218">Fixed</span></span>
-  <span data-ttu-id="ad6f9-1219">Socketpair pour les sockets datagramme unix (GH #262)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1219">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="ad6f9-1220">Prise en charge de socket UNIX pour SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1220">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="ad6f9-1221">Prise en charge de socket UNIX pour SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1221">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="ad6f9-1222">Prise en charge de socket UNIX pour SOCK_SEQPACKET (758 GH #, #546)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1222">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="ad6f9-1223">Ajout de prise en charge pour l’envoi de socket datagramme unix, reçues et d’arrêt</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1223">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="ad6f9-1224">Corriger la vérification d’erreur en raison de la validation de paramètre mmap non valide pour les adresses non fixe.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1224">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="ad6f9-1225">(#847 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1225">(GH #847)</span></span>
- <span data-ttu-id="ad6f9-1226">Prise en charge pour interrompre / reprendre des États de Terminal Server</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1226">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="ad6f9-1227">Prise en charge d’ioctl TIOCPKT débloquer l’utilitaire d’écran (GH #774)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1227">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="ad6f9-1228">Problème connu : Touches de fonction non opérationnels</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1228">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="ad6f9-1229">Correction d’une concurrence dans TimerFd qui peut entraîner un membre libéré 'ReaderReady' accessible par LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1229">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="ad6f9-1230">Activer le support d’appel système pouvant être redémarrées pour futex, interrogation et clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1230">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="ad6f9-1231">Prise en charge du montage de liaison ajouté</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1231">Added bind mount support</span></span>
- <span data-ttu-id="ad6f9-1232">Annuler le partage pour la prise en charge de l’espace de noms de montage</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1232">unshare for mount namespace support</span></span>
    - <span data-ttu-id="ad6f9-1233">Problème connu : Lorsque vous créez un nouvel espace de noms de montage avec `unshare(CLONE_NEWNS)` le répertoire de travail continue à pointer vers l’ancien espace de noms</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1233">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="ad6f9-1234">Autres améliorations et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1234">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="ad6f9-1235">Build 14905</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1235">Build 14905</span></span>

<span data-ttu-id="ad6f9-1236">Pour Windows général plus d’informations sur la build 14905 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1236">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1237">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1237">Fixed</span></span>
- <span data-ttu-id="ad6f9-1238">Système redémarrable appels sont désormais pris en charge (GH #349 GH #520)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1238">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="ad6f9-1239">Liens symboliques vers des répertoires de fin dans / maintenant opérationnelle (GH #650)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1239">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="ad6f9-1240">Implémenté RNDGETENTCNT ioctl pour/dev/Random</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1240">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="ad6f9-1241">Implémenté le/proc / [pid] / monte, / proc / [pid] / mountinfo et/proc / [pid] / mountstats fichiers</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1241">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="ad6f9-1242">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1242">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="ad6f9-1243">Build 14901</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1243">Build 14901</span></span>
<span data-ttu-id="ad6f9-1244">Première Insider générer pour la publication de mise à jour anniversaire de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1244">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="ad6f9-1245">Pour Windows général plus d’informations sur la build 14901 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1245">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1246">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1246">Fixed</span></span>
- <span data-ttu-id="ad6f9-1247">Problème de barre oblique de fin fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1247">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="ad6f9-1248">Commandes telles que `$ mv a/c/ a/b/` fonctionne maintenant</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1248">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="ad6f9-1249">Installation invite désormais l’utilisateur si les paramètres régionaux Ubuntu doivent être défini sur les paramètres régionaux Windows</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1249">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="ad6f9-1250">Commande procfs prise en charge pour le dossier de ns</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1250">Procfs support for ns folder</span></span>
- <span data-ttu-id="ad6f9-1251">Ajouté le montage et démontage pour tmpfs, commande procfs et systèmes de fichiers sysfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1251">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="ad6f9-1252">Corriger mknod [at] signature ABI de 32 bits</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1252">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="ad6f9-1253">Sockets UNIX déplacés pour distribuer le modèle</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1253">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="ad6f9-1254">Taille de mémoire tampon INET socket recv défini à l’aide de la setsockopt doit être respecté.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1254">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="ad6f9-1255">Indicateur de message de réception de socket MSG_CMSG_CLOEXEC unix implémenter</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1255">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="ad6f9-1256">Redirection de canal de stdin/stdout de processus Linux (GH #2)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1256">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="ad6f9-1257">Permet de combinaison de l’interpréteur de commandes - c dans cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1257">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="ad6f9-1258">Exemple : > dir | Bash -c « foo grep »</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1258">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="ad6f9-1259">Bash peut désormais être installée sur les systèmes avec plusieurs fichiers d’échange (538 GH #, #358)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1259">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="ad6f9-1260">Taille de mémoire tampon par défaut INET Socket doit correspondre à celle de l’installation d’Ubuntu par défaut</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1260">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="ad6f9-1261">Aligner syscalls xattr à listxattr</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1261">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="ad6f9-1262">Retourner uniquement les interfaces avec une adresse IPv4 valide provenant de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1262">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="ad6f9-1263">Corriger l’action par défaut de signal lorsque injecté par ptrace</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1263">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="ad6f9-1264">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1264">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="ad6f9-1265">Utilisez les valeurs de registres de contexte ordinateur lors de la restauration du contexte dans sigreturn</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1265">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="ad6f9-1266">Cela résout le problème où java et javac ont été mise en suspens pour certains utilisateurs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1266">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="ad6f9-1267">Implémenter /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1267">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1268">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1268">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1269">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1270">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="ad6f9-1271">Build 14388 à la mise à jour anniversaire Windows 10</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1271">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="ad6f9-1272">Pour Windows général plus d’informations sur la build 14388 visitez le [Windows Blog](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1272">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1273">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1273">Fixed</span></span>
- <span data-ttu-id="ad6f9-1274">Correctifs pour vous préparer à la mise à jour anniversaire de Windows 10 sur 8/2</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1274">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="ad6f9-1275">Vous trouverez plus d’informations sur WSL dans la mise à jour anniversaire sur notre [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1275">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="ad6f9-1276">Build 14376</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1276">Build 14376</span></span>
<span data-ttu-id="ad6f9-1277">Pour Windows général plus d’informations sur la build 14376 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1277">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1278">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1278">Fixed</span></span>
- <span data-ttu-id="ad6f9-1279">Supprimé certaines instances où apt-get bloque (GH #493)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1279">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="ad6f9-1280">Correction d’un problème où les montages vides n’étaient pas gérées correctement</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1280">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="ad6f9-1281">Correction d’un problème où ramdisks n’étaient pas monté correctement</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1281">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="ad6f9-1282">Acceptation du socket d’unix de modification pour prendre en charge les indicateurs (partielle GH #451)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1282">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="ad6f9-1283">Réseau commun fixe liés écran bleu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1283">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="ad6f9-1284">Correction d’écran bleu lorsque vous accédez à/proc / [pid] / tâches (GH #523)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1284">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="ad6f9-1285">Fixe utilisation élevée du processeur pour des scénarios de pty (488 GH #, #504)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1285">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="ad6f9-1286">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1286">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="ad6f9-1287">Build 14371</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1287">Build 14371</span></span>
<span data-ttu-id="ad6f9-1288">Pour Windows général plus d’informations sur la build 14371 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1288">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1289">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1289">Fixed</span></span>
- <span data-ttu-id="ad6f9-1290">Corrigé concurrence de minutage avec SIGCHLD et wait() lors de l’utilisation de ptrace</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1290">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="ad6f9-1291">Correction d’un comportement lorsque les chemins d’accès ont une fin / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1291">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="ad6f9-1292">Résolution du problème de changement de nom/dissocier des échouent en raison de descripteurs ouverts pour enfants</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1292">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="ad6f9-1293">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1293">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="ad6f9-1294">Build 14366</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1294">Build 14366</span></span>
<span data-ttu-id="ad6f9-1295">Pour Windows général plus d’informations sur la build 14366 visitez le [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1295">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1296">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1296">Fixed</span></span>
- <span data-ttu-id="ad6f9-1297">Corriger dans la création de fichiers via les liens symboliques</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1297">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="ad6f9-1298">Ajout de listxattr pour Python (385 Hg)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1298">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="ad6f9-1299">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1299">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1300">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1300">Syscall Support</span></span>
-   <span data-ttu-id="ad6f9-1301">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1301">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1302">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1302">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="ad6f9-1303">Build 14361</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1303">Build 14361</span></span>
<span data-ttu-id="ad6f9-1304">Pour Windows général plus d’informations sur la build 14361 visitez le [Windows Blog](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1304">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1305">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1305">Fixed</span></span>
- <span data-ttu-id="ad6f9-1306">DrvFs est désormais sensible à la casse lors de l’exécution dans Bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1306">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="ad6f9-1307">Les utilisateurs mai case.txt et cas. TXT sur leur c/mnt/lecteurs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1307">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="ad6f9-1308">Respecte la casse est uniquement pris en charge dans Bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1308">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="ad6f9-1309">Lorsque l’extérieur de NTFS Bash signale correctement les fichiers, mais un comportement inattendu peut se produire à interagir avec les fichiers à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1309">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="ad6f9-1310">La racine de chaque volume (c'est-à-dire /mnt/c) n’est pas sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1310">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="ad6f9-1311">Vous pouvez trouver plus d’informations sur la gestion des ces fichiers dans Windows [ici](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1311">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="ad6f9-1312">Considérablement améliorée pty / tty prend en charge.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1312">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="ad6f9-1313">Les applications telles que TMUX désormais pris en charge que (# GH 40)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1313">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="ad6f9-1314">Problème d’installation fixe où les comptes d’utilisateurs créés pas toujours</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1314">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="ad6f9-1315">Optimisé structure arg de ligne de commande permettant de liste d’arguments de très longs.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1315">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="ad6f9-1316">(#153 HG)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1316">(GH #153)</span></span>
- <span data-ttu-id="ad6f9-1317">Maintenant en mesure de supprimer et chmod read_only les fichiers à partir de DrvFs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1317">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="ad6f9-1318">Correction de certaines instances où les blocages de terminal sur Déconnecter (GH #43)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1318">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="ad6f9-1319">chmod et chown fonctionnent désormais sur les appareils tty</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1319">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="ad6f9-1320">Autoriser la connexion à 0.0.0.0 et :: en tant que localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1320">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="ad6f9-1321">Sendmsg/recvmsg gèrent maintenant une longueur de vecteur d’e/s de > 1 (partielle GH #376)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1321">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="ad6f9-1322">Les utilisateurs peuvent désormais annulations du fichier généré automatiquement les ordinateurs hôtes (GH #398)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1322">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="ad6f9-1323">Automatiquement en correspondance les paramètres régionaux de Linux pour les paramètres régionaux NT lors de l’installation (GH #11)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1323">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="ad6f9-1324">Ajouté le fichier /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1324">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="ad6f9-1325">strace se ferme désormais correctement</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1325">strace now exits correctly</span></span>
- <span data-ttu-id="ad6f9-1326">Autoriser les canaux être rouverte via /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1326">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="ad6f9-1327">Masquer les répertoires sous %LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1327">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="ad6f9-1328">Meilleure gestion des bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1328">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="ad6f9-1329">Commandes telles que « bash ~ ls - c » désormais pris en charge (GH #467)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1329">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="ad6f9-1330">Sockets notifient maintenant epoll en lecture disponible lors de l’arrêt (GH #271)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1330">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="ad6f9-1331">lxrun / désinstallation est plus efficace de la suppression des fichiers et dossiers</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1331">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="ad6f9-1332">Corrigé ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1332">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="ad6f9-1333">X11 prise en charge améliorée des applications telles que xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1333">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="ad6f9-1334">Mise à jour de la taille de pile de thread initial au paramètre d’Ubuntu par défaut et de signalement de la taille correctement à la syscall get_rlimit (172 GH #, #258)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1334">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="ad6f9-1335">Amélioration des rapports pico image noms de processus (par exemple, pour l’audit)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1335">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="ad6f9-1336">/Proc/mountinfo implémentée pour la commande df</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1336">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="ad6f9-1337">Code d’erreur de lien symbolique fixe pour le nom de l’enfant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1337">Fixed symlink error code for child name .</span></span> <span data-ttu-id="ad6f9-1338">et...</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1338">and ..</span></span>
- <span data-ttu-id="ad6f9-1339">Améliorations et correctifs de bogues des améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1339">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1340">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1340">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1341">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1341">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1342">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1342">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="ad6f9-1343">Build 14352</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1343">Build 14352</span></span>
<span data-ttu-id="ad6f9-1344">Pour Windows général plus d’informations sur la build 14352 visitez le [Windows Blog](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1344">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1345">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1345">Fixed</span></span>
- <span data-ttu-id="ad6f9-1346">Correction d’un problème où des fichiers volumineux ont été téléchargés non / créées correctement.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1346">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="ad6f9-1347">Cela doit débloquer npm et autres scénarios (GH n ° 3, Hg #313)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1347">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="ad6f9-1348">Supprimé certaines instances où sockets de blocage</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1348">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="ad6f9-1349">Correction des erreurs ptrace</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1349">Corrected some ptrace errors</span></span>
- <span data-ttu-id="ad6f9-1350">Correction d’un problème avec WSL autorisant les noms de fichiers plus de 255 caractères</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1350">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="ad6f9-1351">Prise en charge améliorée pour les caractères non anglais</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1351">Improved support for non-English characters</span></span>
- <span data-ttu-id="ad6f9-1352">Ajoutez des données de fuseau horaire Windows actuelles et définissez comme valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1352">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="ad6f9-1353">D’id appareil unique pour chaque point de montage (correctif jre – GH #49)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1353">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="ad6f9-1354">Corriger le problème avec les chemins d’accès contenant «. »</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1354">Correct issue with paths containing “.”</span></span> <span data-ttu-id="ad6f9-1355">et «... »</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1355">and “..”</span></span>
- <span data-ttu-id="ad6f9-1356">Prise en charge Fifo (GH #71)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1356">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="ad6f9-1357">Format mis à jour de resolv.conf pour faire correspondre le format natif Ubuntu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1357">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="ad6f9-1358">Un nettoyage des commande procfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1358">Some procfs cleanup</span></span>
- <span data-ttu-id="ad6f9-1359">Ping activé pour les consoles administrateur (GH #18)</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1359">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1360">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1360">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1361">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1361">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1362">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1362">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="ad6f9-1363">Build 14342</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1363">Build 14342</span></span>
<span data-ttu-id="ad6f9-1364">Pour Windows général plus d’informations sur build 14342 le [Windows Blog](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1364">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="ad6f9-1365">Vous trouverez plus d’informations sur VolFs et DriveFs sur le [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1365">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1366">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1366">Fixed</span></span>
- <span data-ttu-id="ad6f9-1367">Résolu le problème d’installation lorsque l’utilisateur Windows avait des caractères Unicode dans le nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1367">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="ad6f9-1368">La solution de contournement udev apt-get update dans le Forum aux questions est désormais fournie par défaut sur la première exécution</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1368">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="ad6f9-1369">Activé des liens symboliques dans DriveFs (/mnt/<drive>) répertoires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1369">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="ad6f9-1370">Fonctionnent désormais de liens symboliques entre DriveFs et VolFs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1370">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="ad6f9-1371">Adressée supérieur au niveau chemin d’accès de l’analyse du problème : %.ls. / / fonctionne désormais comme prévu</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1371">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="ad6f9-1372">npm installez-y DriveFs et les options -g sont maintenant opérationnelles.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1372">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="ad6f9-1373">Correction d’un problème empêchant le lancement de serveur PHP</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1373">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="ad6f9-1374">Valeurs d’environnement par défaut de mise à jour, telles que $PATH pour rapprocher correspond à Ubuntu natif</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1374">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="ad6f9-1375">Ajouter une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache du package apt</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1375">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="ad6f9-1376">Correction du problème avec la validation de l’en-tête ELF, WSL prend désormais en charge toutes les options de Melkor</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1376">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="ad6f9-1377">Interpréteur de commandes Zsh est fonctionnel</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1377">Zsh shell is functional</span></span>
- <span data-ttu-id="ad6f9-1378">Les binaires précompilés Go sont donc compatibles</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1378">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="ad6f9-1379">Inviter sur Bash.exe tout d’abord exécuter est maintenant correctement localisé</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1379">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="ad6f9-1380">/proc/meminfo retourne désormais des informations correctes</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1380">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="ad6f9-1381">Sockets désormais pris en charge dans le système de fichiers virtuel</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1381">Sockets now supported in VFS</span></span>
- <span data-ttu-id="ad6f9-1382">/dev maintenant monté en tant que tempfs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1382">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="ad6f9-1383">FIFO désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1383">Fifo now supported</span></span>
- <span data-ttu-id="ad6f9-1384">Des systèmes multicœurs montre maintenant correctement dans cpuinfo/proc /</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1384">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="ad6f9-1385">Améliorations supplémentaires et des messages d’erreur téléchargé au cours de la première exécution</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1385">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="ad6f9-1386">Syscall améliorations et correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1386">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="ad6f9-1387">Syscall pris en charge de la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1387">Supported syscall list below.</span></span>
- <span data-ttu-id="ad6f9-1388">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1388">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="ad6f9-1389">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1389">Known Issues</span></span>
- <span data-ttu-id="ad6f9-1390">Ne pas de résolution '..'</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1390">Not resolving ‘..’</span></span> <span data-ttu-id="ad6f9-1391">correctement sur DriveFs dans certains cas</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1391">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1392">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1392">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1393">Voici une liste des nouvelles ou améliorées syscalls qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1394">Les syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="ad6f9-1395">Build 14332</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1395">Build 14332</span></span>

<span data-ttu-id="ad6f9-1396">Pour Windows général plus d’informations sur la build 14332 visitez le [Windows Blog](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1396">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="ad6f9-1397">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1397">Fixed</span></span>
- <span data-ttu-id="ad6f9-1398">Meilleure génération resolv.conf, y compris la hiérarchisation des entrées DNS</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1398">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="ad6f9-1399">Problème avec le déplacement de fichiers et répertoires entre mnt et non- / mnt lecteurs</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1399">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="ad6f9-1400">Fichiers .tar peuvent maintenant être créés avec des liens symboliques</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1400">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="ad6f9-1401">Répertoire de /run/lock par défaut ajoutés lors de la création d’instance</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1401">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="ad6f9-1402">Mise à jour/dev/null pour retourner des informations statistiques appropriées</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1402">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="ad6f9-1403">Autres erreurs lors du téléchargement lors du premier démarrage</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1403">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="ad6f9-1404">Syscall améliorations et correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1404">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="ad6f9-1405">Syscall pris en charge de la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1405">Supported syscall list below.</span></span>
- <span data-ttu-id="ad6f9-1406">Améliorations et correctifs de bogues des améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1406">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1407">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1407">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1408">Voici la nouvelle syscall qui a déjà une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1408">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="ad6f9-1409">La syscall sur cette liste est pris en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1409">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="ad6f9-1410">Build 14328</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1410">Build 14328</span></span>

<span data-ttu-id="ad6f9-1411">Pour Windows général plus d’informations sur la build 14332 visitez le [Windows Blog](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1411">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="ad6f9-1412">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1412">New Features</span></span>
* <span data-ttu-id="ad6f9-1413">Prennent désormais en charge les utilisateurs de Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1413">Now support Linux users.</span></span>  <span data-ttu-id="ad6f9-1414">L’installation de Bash sur Ubuntu sur Windows vous demande de la création d’un utilisateur Linux.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1414">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="ad6f9-1415">Pour plus d’informations, visitez https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1415">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="ad6f9-1416">Nom d’hôte est maintenant défini pour le nom d’ordinateur Windows, pas plus @localhost</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1416">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="ad6f9-1417">Pour plus d’informations sur build 14328, visitez : https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1417">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="ad6f9-1418">Fixe</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1418">Fixed</span></span>
* <span data-ttu-id="ad6f9-1419">Améliorations de lien symbolique pour /mnt/ non<drive> fichiers</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1419">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="ad6f9-1420">npm installation fonctionne désormais correctement</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1420">npm install now works</span></span>
    * <span data-ttu-id="ad6f9-1421">JDK / jre installable maintenant à l’aide des instructions trouvées [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1421">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="ad6f9-1422">problème connu : liens symboliques ne fonctionnent pas pour Windows monte.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1422">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="ad6f9-1423">Fonctionnalité sera disponible dans une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1423">Functionality will be available in a later build</span></span>
* <span data-ttu-id="ad6f9-1424">haut et htop affichent désormais</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1424">top and htop now display</span></span>
* <span data-ttu-id="ad6f9-1425">Messages d’erreur supplémentaires pour certains échecs de l’installation</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1425">Additional error messages for some install failures</span></span>
* <span data-ttu-id="ad6f9-1426">Syscall améliorations et correctifs de bogues.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1426">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="ad6f9-1427">Syscall pris en charge de la liste ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1427">Supported syscall list below.</span></span>
* <span data-ttu-id="ad6f9-1428">Améliorations et correctifs de bogues des améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1428">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="ad6f9-1429">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1429">Syscall Support</span></span>
<span data-ttu-id="ad6f9-1430">Voici une liste d’appels qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1430">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="ad6f9-1431">Syscalls sur cette liste sont prises en charge au moins l’un des scénarios, mais ne peuvent pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="ad6f9-1431">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
