---
title: Notes de publication pour le sous-système Windows pour Linux
description: Notes de publication pour le sous-système Windows pour Linux.  Mise à jour hebdomadaire.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042425"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="cbc9f-105">Notes de publication pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="cbc9f-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18917"></a><span data-ttu-id="cbc9f-106">Build 18917</span><span class="sxs-lookup"><span data-stu-id="cbc9f-106">Build 18917</span></span>
<span data-ttu-id="cbc9f-107">Pour obtenir des informations générales sur Windows sur la build 18917, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-107">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-108">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-108">WSL</span></span>
* <span data-ttu-id="cbc9f-109">WSL 2 est maintenant disponible!</span><span class="sxs-lookup"><span data-stu-id="cbc9f-109">WSL 2 is now available!</span></span> <span data-ttu-id="cbc9f-110">Pour plus d’informations, consultez le [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) .</span><span class="sxs-lookup"><span data-stu-id="cbc9f-110">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="cbc9f-111">Corriger une régression où le lancement de processus Windows via liens symboliques ne fonctionnait pas correctement [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-111">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="cbc9f-112">Ajouter WSL. exe--List--verbose, WSL. exe--List--Quiet et WSL. exe--Import--options de version dans WSL. exe</span><span class="sxs-lookup"><span data-stu-id="cbc9f-112">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="cbc9f-113">Ajouter WSL. exe--option d’arrêt</span><span class="sxs-lookup"><span data-stu-id="cbc9f-113">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="cbc9f-114">Plan 9: Autoriser l’ouverture d’un répertoire pour que l’écriture aboutisse</span><span class="sxs-lookup"><span data-stu-id="cbc9f-114">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="cbc9f-115">Build 18890</span><span class="sxs-lookup"><span data-stu-id="cbc9f-115">Build 18890</span></span>
<span data-ttu-id="cbc9f-116">Pour obtenir des informations générales sur Windows sur la build 18890, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-116">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-117">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-117">WSL</span></span>
* <span data-ttu-id="cbc9f-118">Fuite de socket non bloquant [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-118">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="cbc9f-119">L’entrée EOF du terminal peut bloquer les lectures suivantes [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-119">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="cbc9f-120">Mettez à jour l’en-tête resolv. conf pour faire référence à WSL. conf [abordé dans GH 3928]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-120">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="cbc9f-121">Blocage dans epoll supprimer le code [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-121">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="cbc9f-122">Gérer les espaces dans les arguments pour--import et – Export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-122">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="cbc9f-123">L’extension des fichiers mmap ne fonctionne pas correctement [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-123">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="cbc9f-124">Résoudre le problème avec \\ARM64 WSL $ Access ne fonctionne pas correctement</span><span class="sxs-lookup"><span data-stu-id="cbc9f-124">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="cbc9f-125">Ajouter une meilleure icône par défaut pour WSL. exe</span><span class="sxs-lookup"><span data-stu-id="cbc9f-125">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="cbc9f-126">Build 18342</span><span class="sxs-lookup"><span data-stu-id="cbc9f-126">Build 18342</span></span>
<span data-ttu-id="cbc9f-127">Pour obtenir des informations générales sur Windows sur la build 18342, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-127">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-128">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-128">WSL</span></span>
* <span data-ttu-id="cbc9f-129">Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans un WSL distribution à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-129">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="cbc9f-130">Ces fichiers sont accessibles par le biais de la ligne de commande, et les applications Windows, telles que l’Explorateur de fichiers, VSCode, etc., peuvent interagir avec ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-130">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="cbc9f-131">Accédez à vos fichiers en accédant \\à \\WSL\\$ < distro_name > ou consultez la liste des distributions en cours d’exécution en \\accédant à \\WSL $</span><span class="sxs-lookup"><span data-stu-id="cbc9f-131">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="cbc9f-132">Ajouter des balises d’informations d’UC supplémentaires et corriger les valeurs Cpus_allowed [_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-132">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="cbc9f-133">Prendre en charge exec à partir d’un thread non leader [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-133">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="cbc9f-134">Considérer les échecs de mise à jour de configuration comme non récupérables [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-134">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="cbc9f-135">Mettre à jour binfmt pour gérer correctement les décalages [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-135">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="cbc9f-136">Activer le mappage de lecteurs réseau pour le plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-136">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="cbc9f-137">Prise en charge de Windows > Linux et Linux-> de la traduction de chemins d’accès Windows pour les montages de liaison</span><span class="sxs-lookup"><span data-stu-id="cbc9f-137">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="cbc9f-138">Créer des sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule</span><span class="sxs-lookup"><span data-stu-id="cbc9f-138">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="cbc9f-139">Build 18334</span><span class="sxs-lookup"><span data-stu-id="cbc9f-139">Build 18334</span></span>
<span data-ttu-id="cbc9f-140">Pour obtenir des informations générales sur Windows sur la build 18334, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-140">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-141">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-141">WSL</span></span>
* <span data-ttu-id="cbc9f-142">Remaniement de la façon dont le fuseau horaire Windows est mappé à un fuseau horaire Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-142">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="cbc9f-143">Corriger les fuites de mémoire et ajouter de nouvelles fonctions de traduction de chaînes [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-143">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="cbc9f-144">SIGCONT sur un ThreadGroup sans threads est une absence d’opération [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-144">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="cbc9f-145">Afficher correctement les descripteurs de fichiers socket et EPoll dans/proc/Self/FD</span><span class="sxs-lookup"><span data-stu-id="cbc9f-145">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="cbc9f-146">Build 18305</span><span class="sxs-lookup"><span data-stu-id="cbc9f-146">Build 18305</span></span>
<span data-ttu-id="cbc9f-147">Pour obtenir des informations générales sur Windows sur la build 18305, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-147">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-148">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-148">WSL</span></span>
* <span data-ttu-id="cbc9f-149">pthreads perdez l’accès aux fichiers lorsque le thread principal quitte [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-149">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="cbc9f-150">TIOCSCTTY doit ignorer le paramètre «force» à moins qu’il ne soit requis [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-150">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="cbc9f-151">améliorations de la ligne de commande WSL. exe et ajout de fonctionnalités d’importation/exportation.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-151">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="cbc9f-152">Build 18277</span><span class="sxs-lookup"><span data-stu-id="cbc9f-152">Build 18277</span></span>
<span data-ttu-id="cbc9f-153">Pour obtenir des informations générales sur Windows sur la build 18277, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-153">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-154">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-154">WSL</span></span>
* <span data-ttu-id="cbc9f-155">Correction de l’erreur «aucune interface non prise en charge» introduite dans la build 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-155">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="cbc9f-156">Ignorer l’indicateur MNT_FORCE pour umount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-156">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="cbc9f-157">Basculer l’interopérabilité WSL pour utiliser l’API CreatePseudoConsole officielle</span><span class="sxs-lookup"><span data-stu-id="cbc9f-157">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="cbc9f-158">Ne conserver aucune valeur de délai d’attente lors du redémarrage de FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="cbc9f-158">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="cbc9f-159">Build 18272</span><span class="sxs-lookup"><span data-stu-id="cbc9f-159">Build 18272</span></span>
<span data-ttu-id="cbc9f-160">Pour obtenir des informations générales sur Windows sur la build 18272, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-160">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-161">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-161">WSL</span></span>
* <span data-ttu-id="cbc9f-162">**TRES** Il y a un problème dans cette Build qui rend WSL inopérant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-162">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="cbc9f-163">Lors de la tentative de lancement de votre distribution, une erreur «aucune interface n’est prise en charge» s’affiche.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-163">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="cbc9f-164">Le problème a été résolu et sera intégré à la version d’Insider Fast de la semaine prochaine.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-164">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="cbc9f-165">Si vous avez installé cette Build, vous pouvez restaurer la version précédente de Windows à l’aide de «revenir à la version précédente de Windows 10» dans Paramètres-> Update & la récupération de la > de sécurité.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-165">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="cbc9f-166">Build 18267</span><span class="sxs-lookup"><span data-stu-id="cbc9f-166">Build 18267</span></span>
<span data-ttu-id="cbc9f-167">Pour obtenir des informations générales sur Windows sur la build 18267, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-167">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-168">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-168">WSL</span></span>
* <span data-ttu-id="cbc9f-169">Corrigez le problème où le processus zombie ne peut pas être récolté et rester indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-169">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="cbc9f-170">WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-170">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="cbc9f-171">Autoriser fsync à fonctionner correctement pour les fichiers en lecture seule sur DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-171">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="cbc9f-172">Vérifiez que les répertoires/bin et/sbin existent avant de créer des liens symboliques dans [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-172">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="cbc9f-173">Ajout d’un mécanisme de délai d’attente d’arrêt d’instance pour les instances WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-173">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="cbc9f-174">Le délai d’expiration est actuellement défini à 15 secondes, ce qui signifie que l’instance se termine 15 secondes après la fin du dernier processus WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-174">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="cbc9f-175">Pour arrêter immédiatement une distribution, utilisez:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-175">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="cbc9f-176">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-176">Build 17763 (1809)</span></span>
<span data-ttu-id="cbc9f-177">Pour obtenir des informations générales sur Windows sur la build 17763, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-177">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-178">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-178">WSL</span></span>
* <span data-ttu-id="cbc9f-179">La vérification des autorisations de SetPriority syscall est trop stricte pour modifier la même priorité de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-179">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="cbc9f-180">S’assurer que le temps d’interruption non biaisé est utilisé pour le temps de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-180">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="cbc9f-181">Handle liens symboliques dans l’interpréteur binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-181">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="cbc9f-182">Meilleure gestion du nettoyage du descripteur de fichier ThreadGroup leader.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-182">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="cbc9f-183">Basculer WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter le dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-183">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="cbc9f-184">L’attachement ptrace peut provoquer une valeur de retour incorrecte dans les appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-184">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="cbc9f-185">Correction de plusieurs problèmes liés à AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-185">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="cbc9f-186">Résoudre le problème qui peut provoquer l’échec de WSL Interop si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-186">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="cbc9f-187">Éviter une seconde tentative de connexion de bouclage à des ports inexistants [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-187">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="cbc9f-188">Ajouter un fichier stub/proc/sys/FS/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-188">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="cbc9f-189">Informations d’étendue IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-189">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="cbc9f-190">Prise en charge de PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-190">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="cbc9f-191">Système de fichiers du canal effaçant par inadvertance l’événement epoll déclenché par le bord [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-191">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="cbc9f-192">L’exécutable Win32 lancé via un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-192">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="cbc9f-193">Prise en charge améliorée de Zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-193">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="cbc9f-194">Ajouter des entrées WSL. conf pour contrôler le comportement de l’interopérabilité Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-194">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="cbc9f-195">Correctif pour GetSockName ne retournant pas toujours le type de famille de sockets UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-195">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="cbc9f-196">Ajout de la prise en charge de TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-196">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="cbc9f-197">Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-197">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="cbc9f-198">Prise en charge de l’interopérabilité sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-198">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="cbc9f-199">Résoudre le problème de vérification des autorisations sur le dossier racine [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-199">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="cbc9f-200">Prise en charge limitée des IOCTL du clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-200">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="cbc9f-201">Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-201">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="cbc9f-202">Ajouter WSL-u ou--User (option) [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-202">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="cbc9f-203">Résoudre les problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-203">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="cbc9f-204">Les sockets Unix doivent conserver les informations d’identification homologues déconnectées [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-204">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="cbc9f-205">Échec indéfiniment des sockets Unix non bloquants avec EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-205">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="cbc9f-206">case = OFF est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-206">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="cbc9f-207">Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) .</span><span class="sxs-lookup"><span data-stu-id="cbc9f-207">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="cbc9f-208">Ajoutez wslconfig/Terminate pour arrêter les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-208">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="cbc9f-209">Corrigez le problème avec les entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins d’accès avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-209">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="cbc9f-210">Exposer le respect de la casse par répertoire en tant qu’attribut étendu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-210">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="cbc9f-211">ARM64 Émule les opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-211">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="cbc9f-212">Résolvez le [problème dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-212">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="cbc9f-213">DrvFs: seuls les caractères d’échappement de la plage privée qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-213">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="cbc9f-214">Correction de l’erreur de validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-214">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="cbc9f-215">Les minuteurs absolus WSL avec une heure dans le passé ne se déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-215">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="cbc9f-216">Vérifiez que les points d’analyse nouvellement créés sont répertoriés comme tels dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-216">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="cbc9f-217">Créez de manière atomique des répertoires sensibles à la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-217">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="cbc9f-218">Correction d’un problème supplémentaire où les opérations multithread pouvaient retourner ENOENT même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-218">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="cbc9f-219">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-219">[GH 2712]</span></span>
* <span data-ttu-id="cbc9f-220">Correction de l’échec du lancement de WSL lorsque UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-220">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="cbc9f-221">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-221">[GH 3020]</span></span>
* <span data-ttu-id="cbc9f-222">Ajouter le menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-222">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="cbc9f-223">Pour utiliser, maintenez la touche Maj enfoncée et cliquez avec le bouton droit dans une fenêtre de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-223">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="cbc9f-224">Corriger le comportement non bloquant du socket Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-224">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="cbc9f-225">Correction de la commande NetLink en suspens comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-225">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="cbc9f-226">Ajoutez la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-226">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="cbc9f-227">Résoudre le problème avec TRUNCATE not provoquant des événements inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-227">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="cbc9f-228">Add--exec (option) pour WSL. exe afin d’appeler un seul binaire sans Shell.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-228">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="cbc9f-229">L’option Add--distribution de WSL. exe permet de sélectionner un distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-229">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="cbc9f-230">Prise en charge limitée de dmesg.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-230">Limited support for dmesg.</span></span> <span data-ttu-id="cbc9f-231">Les applications peuvent désormais se connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-231">Applications can now log to dmesg.</span></span> <span data-ttu-id="cbc9f-232">Le pilote WSL journalise des informations limitées sur dmesg.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-232">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="cbc9f-233">À l’avenir, il peut être étendu pour transporter d’autres informations/Diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-233">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="cbc9f-234">Remarque: dmesg est actuellement pris en charge `/dev/kmsg` par le biais de l’interface de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-234">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="cbc9f-235">`syslog`l’interface syscall n’est pas encore prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-235">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="cbc9f-236">Et, par conséquent, certaines des `dmesg` options de ligne de commande `-S`, `-C` telles que, ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-236">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="cbc9f-237">Modifier le GID et le mode par défaut des appareils série pour qu’ils correspondent au mode natif [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-237">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="cbc9f-238">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-238">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="cbc9f-239">Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-239">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="cbc9f-240">Certains caractères (tels que'/', ': 'et\*' ') ne sont pas autorisés, et les noms d’attributs étendus ne respectent pas la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-240">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="cbc9f-241">Build 18252 (avance)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-241">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="cbc9f-242">Pour obtenir des informations générales sur Windows sur la build 18252, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-242">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-243">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-243">WSL</span></span>
* <span data-ttu-id="cbc9f-244">Déplacer les fichiers binaires init et bsdtar hors de la dll lxssmanager et dans un dossier d’outils distinct</span><span class="sxs-lookup"><span data-stu-id="cbc9f-244">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="cbc9f-245">Corriger la course à la fermeture du descripteur de fichier lors de l’utilisation de CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="cbc9f-245">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="cbc9f-246">Gérer les champs facultatifs dans/proc/PID/mountinfo lors de la traduction de chemins d’accès DrvFs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-246">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="cbc9f-247">Autoriser DrvFs mknod à fonctionner sans la prise en charge des métadonnées pour S_IFREG</span><span class="sxs-lookup"><span data-stu-id="cbc9f-247">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="cbc9f-248">Les fichiers ReadOnly créés sur DrvFs doivent avoir l’attribut ReadOnly défini [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-248">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="cbc9f-249">Ajouter/sbin/Mount.drvfs Helper pour gérer le montage DrvFs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-249">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="cbc9f-250">Utilisez POSIX Rename dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-250">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="cbc9f-251">Autorisez la traduction de chemin sur les volumes sans GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-251">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="cbc9f-252">Build 17738 (rapide)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-252">Build 17738 (Fast)</span></span>
<span data-ttu-id="cbc9f-253">Pour obtenir des informations générales sur Windows sur la build 17738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-253">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-254">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-254">WSL</span></span>
* <span data-ttu-id="cbc9f-255">La vérification des autorisations de SetPriority syscall est trop stricte pour modifier la même priorité de thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-255">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="cbc9f-256">S’assurer que le temps d’interruption non biaisé est utilisé pour le temps de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime (CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-256">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="cbc9f-257">Handle liens symboliques dans l’interpréteur binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-257">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="cbc9f-258">Meilleure gestion du nettoyage du descripteur de fichier ThreadGroup leader.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-258">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="cbc9f-259">Build 17728 (rapide)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-259">Build 17728 (Fast)</span></span>
<span data-ttu-id="cbc9f-260">Pour obtenir des informations générales sur Windows sur la build 17728, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-260">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-261">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-261">WSL</span></span>
* <span data-ttu-id="cbc9f-262">Basculer WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter le dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-262">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="cbc9f-263">L’attachement ptrace peut provoquer une valeur de retour incorrecte dans les appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-263">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="cbc9f-264">Résoudre un certain nombre de problèmes liés à AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-264">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="cbc9f-265">Résoudre le problème qui peut provoquer l’échec de WSL Interop si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-265">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="cbc9f-266">Build 18204 (avance)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-266">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="cbc9f-267">Pour obtenir des informations générales sur Windows sur la build 18204, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-267">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-268">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-268">WSL</span></span>
* <span data-ttu-id="cbc9f-269">Inadvertenly du système de fichiers du canal effacement du bord de l’événement epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="cbc9f-270">L’exécutable Win32 lancé via un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="cbc9f-271">Build 17723 (rapide)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-271">Build 17723 (Fast)</span></span>
<span data-ttu-id="cbc9f-272">Pour obtenir des informations générales sur Windows sur la build 17723, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-272">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-273">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-273">WSL</span></span>
* <span data-ttu-id="cbc9f-274">Éviter une seconde tentative de connexion de bouclage à des ports inexistants [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-274">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="cbc9f-275">Ajouter un fichier stub/proc/sys/FS/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-275">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="cbc9f-276">Informations d’étendue IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-276">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="cbc9f-277">Prise en charge de PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-277">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="cbc9f-278">Inadvertenly du système de fichiers du canal effacement du bord de l’événement epoll [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-278">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="cbc9f-279">L’exécutable Win32 lancé via un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-279">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="cbc9f-280">Build 17713</span><span class="sxs-lookup"><span data-stu-id="cbc9f-280">Build 17713</span></span>
<span data-ttu-id="cbc9f-281">Pour obtenir des informations générales sur Windows sur la build 17713, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-281">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-282">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-282">WSL</span></span>
* <span data-ttu-id="cbc9f-283">Prise en charge améliorée de Zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-283">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="cbc9f-284">Ajouter des entrées WSL. conf pour contrôler le comportement de l’interopérabilité Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-284">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="cbc9f-285">Correctif pour GetSockName ne retournant pas toujours le type de famille de sockets UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-285">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="cbc9f-286">Ajout de la prise en charge de TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-286">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="cbc9f-287">Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-287">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="cbc9f-288">Prise en charge de l’interopérabilité sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-288">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="cbc9f-289">Résoudre le problème de vérification des autorisations sur le dossier racine [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-289">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="cbc9f-290">Prise en charge limitée des IOCTL du clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-290">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="cbc9f-291">Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-291">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="cbc9f-292">Build 17704</span><span class="sxs-lookup"><span data-stu-id="cbc9f-292">Build 17704</span></span>
<span data-ttu-id="cbc9f-293">Pour obtenir des informations générales sur Windows sur la build 17704, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-293">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-294">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-294">WSL</span></span>
* <span data-ttu-id="cbc9f-295">Ajouter WSL-u ou--User (option) [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-295">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="cbc9f-296">Résoudre les problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-296">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="cbc9f-297">Les sockets Unix doivent conserver les informations d’identification homologues déconnectées [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-297">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="cbc9f-298">Échec indéfiniment des sockets Unix non bloquants avec EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-298">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="cbc9f-299">case = OFF est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-299">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="cbc9f-300">Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) .</span><span class="sxs-lookup"><span data-stu-id="cbc9f-300">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="cbc9f-301">Ajoutez wslconfig/Terminate pour arrêter les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-301">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="cbc9f-302">Build 17692</span><span class="sxs-lookup"><span data-stu-id="cbc9f-302">Build 17692</span></span>
<span data-ttu-id="cbc9f-303">Pour obtenir des informations générales sur Windows sur la build 17692, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-303">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-304">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-304">WSL</span></span>
* <span data-ttu-id="cbc9f-305">Corrigez le problème avec les entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins d’accès avec des espaces.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-305">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="cbc9f-306">Exposer le respect de la casse par répertoire en tant qu’attribut étendu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-306">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="cbc9f-307">ARM64 Émule les opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-307">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="cbc9f-308">Résolvez le [problème dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-308">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="cbc9f-309">DrvFs: seuls les caractères d’échappement de la plage privée qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-309">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="cbc9f-310">Build 17686</span><span class="sxs-lookup"><span data-stu-id="cbc9f-310">Build 17686</span></span>
<span data-ttu-id="cbc9f-311">Pour obtenir des informations générales sur Windows sur la build 17686, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-311">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-312">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-312">WSL</span></span>
* <span data-ttu-id="cbc9f-313">Correction de l’erreur de validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-313">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="cbc9f-314">Les minuteurs absolus WSL avec une heure dans le passé ne se déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-314">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="cbc9f-315">Vérifiez que les points d’analyse nouvellement créés sont répertoriés comme tels dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-315">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="cbc9f-316">Créez de manière atomique des répertoires sensibles à la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-316">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="cbc9f-317">Build 17677</span><span class="sxs-lookup"><span data-stu-id="cbc9f-317">Build 17677</span></span>
<span data-ttu-id="cbc9f-318">Pour obtenir des informations générales sur Windows sur la build 17677, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-318">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-319">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-319">WSL</span></span>
* <span data-ttu-id="cbc9f-320">Correction d’un problème supplémentaire où les opérations multithread pouvaient retourner ENOENT même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-320">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="cbc9f-321">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-321">[GH 2712]</span></span>
* <span data-ttu-id="cbc9f-322">Correction de l’échec du lancement de WSL lorsque UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-322">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="cbc9f-323">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-323">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="cbc9f-324">Build 17666</span><span class="sxs-lookup"><span data-stu-id="cbc9f-324">Build 17666</span></span>
<span data-ttu-id="cbc9f-325">Pour obtenir des informations générales sur Windows sur la build 17666, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-325">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-326">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-326">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="cbc9f-327">AVERTISSEMENT : Un problème empêche WSL de s’exécuter sur certains chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-327">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="cbc9f-328">Un correctif est prêt et fait de même pour la branche de génération Insider.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-328">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="cbc9f-329">Ajouter le menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-329">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="cbc9f-330">Pour utiliser maintenir la touche Maj et cliquer avec le bouton droit dans une fenêtre de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-330">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="cbc9f-331">Corriger le comportement non bloquant du socket Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-331">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="cbc9f-332">Correction de la commande NetLink en suspens comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-332">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="cbc9f-333">Ajoutez la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-333">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="cbc9f-334">Résoudre le problème avec TRUNCATE not provoquant des événements inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-334">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="cbc9f-335">Add--exec (option) pour WSL. exe afin d’appeler un seul binaire sans Shell.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-335">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="cbc9f-336">L’option Add--distribution de WSL. exe permet de sélectionner un distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-336">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="cbc9f-337">Build 17655 (avance)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-337">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="cbc9f-338">Pour obtenir des informations générales sur Windows sur la build 17655, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-338">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-339">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-339">WSL</span></span>
* <span data-ttu-id="cbc9f-340">Prise en charge limitée de dmesg.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-340">Limited support for dmesg.</span></span> <span data-ttu-id="cbc9f-341">Les applications peuvent désormais se connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-341">Applications can now log to dmesg.</span></span> <span data-ttu-id="cbc9f-342">Le pilote WSL journalise des informations limitées sur dmesg.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-342">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="cbc9f-343">À l’avenir, il peut être étendu pour transporter d’autres informations/Diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-343">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="cbc9f-344">Remarque: dmesg est actuellement pris en charge `/dev/kmsg` par le biais de l’interface de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-344">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="cbc9f-345">`syslog`l’interface sycall n’est pas encore prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-345">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="cbc9f-346">Et, par conséquent, certaines des `dmesg` options de ligne de commande `-S`, `-C` telles que, ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-346">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="cbc9f-347">Correction d’un problème où les opérations multithread pouvaient retourner ENOENT même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-347">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="cbc9f-348">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-348">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="cbc9f-349">Build 17639 (avance)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-349">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="cbc9f-350">Pour obtenir des informations générales sur Windows sur la build 17639, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-350">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-351">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-351">WSL</span></span>
* <span data-ttu-id="cbc9f-352">Modifier le GID et le mode par défaut des appareils série pour qu’ils correspondent au mode natif [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="cbc9f-353">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="cbc9f-354">Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="cbc9f-355">En particulier, certains caractères (tels que'/', ': 'et\*' ') ne sont pas autorisés, et les noms d’attributs étendus ne respectent pas la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-355">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="cbc9f-356">Build 17133 (rapide)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-356">Build 17133 (Fast)</span></span>
<span data-ttu-id="cbc9f-357">Pour obtenir des informations générales sur Windows sur la build 17133, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-357">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-358">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-358">WSL</span></span>
* <span data-ttu-id="cbc9f-359">Correction du blocage dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-359">Fix for hang in WSL.</span></span> <span data-ttu-id="cbc9f-360">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-360">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="cbc9f-361">Build 17128 (rapide)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-361">Build 17128 (Fast)</span></span>
<span data-ttu-id="cbc9f-362">Pour obtenir des informations générales sur Windows sur la build 17128, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-362">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-363">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-363">WSL</span></span>
* <span data-ttu-id="cbc9f-364">Aucun</span><span class="sxs-lookup"><span data-stu-id="cbc9f-364">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="cbc9f-365">Build 17627 (avance)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-365">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="cbc9f-366">Pour obtenir des informations générales sur Windows sur la build 17627, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-366">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-367">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-367">WSL</span></span>
* <span data-ttu-id="cbc9f-368">Ajoutez la prise en charge des opérations compatibles Futex pi.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-368">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="cbc9f-369">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-369">[GH 1006]</span></span>
    * <span data-ttu-id="cbc9f-370">Notez que les priorités ne sont actuellement pas une fonctionnalité de WSL prise en charge. il existe donc des limitations, mais l’utilisation standard doit être débloquée.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-370">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="cbc9f-371">Prise en charge du pare-feu Windows pour les processus WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-371">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="cbc9f-372">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-372">[GH 1852]</span></span>
    * <span data-ttu-id="cbc9f-373">Par exemple, pour autoriser le processus python WSL à écouter sur n’importe quel port, utilisez la commande Windows avec élévation de privilèges:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="cbc9f-373">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="cbc9f-374">Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-374">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="cbc9f-375">Respectez le shell par défaut de l’utilisateur lors de l’utilisation de WSL. exe.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-375">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="cbc9f-376">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-376">[GH 2372]</span></span>
* <span data-ttu-id="cbc9f-377">Signale toutes les interfaces réseau comme Ethernet.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-377">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="cbc9f-378">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-378">[GH 2996]</span></span>
* <span data-ttu-id="cbc9f-379">Meilleure gestion des fichiers/etc/passwd endommagés.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-379">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="cbc9f-380">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-380">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-381">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-381">Console</span></span>
* <span data-ttu-id="cbc9f-382">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-382">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-383">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-383">LTP Results:</span></span>
<span data-ttu-id="cbc9f-384">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-384">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="cbc9f-385">Build 17618 (avance)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-385">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="cbc9f-386">Pour obtenir des informations générales sur Windows sur la build 17618, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-386">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-387">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-387">WSL</span></span>
* <span data-ttu-id="cbc9f-388">Introduisez la fonctionnalité pseudoconsole pour l’interopérabilité NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-388">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="cbc9f-389">Le mécanisme d’installation hérité (lxrun. exe) est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-389">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="cbc9f-390">Le mécanisme pris en charge pour l’installation des distributions s’effectue via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-390">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-391">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-391">Console</span></span>
* <span data-ttu-id="cbc9f-392">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-392">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-393">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-393">LTP Results:</span></span>
<span data-ttu-id="cbc9f-394">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-394">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="cbc9f-395">Build 17110</span><span class="sxs-lookup"><span data-stu-id="cbc9f-395">Build 17110</span></span>
<span data-ttu-id="cbc9f-396">Pour obtenir des informations générales sur Windows sur la build 17110, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-396">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-397">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-397">WSL</span></span>
* <span data-ttu-id="cbc9f-398">Autorisez l’arrêt de/init à partir de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-398">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="cbc9f-399">DrvFs utilise désormais le respect de la casse par répertoire par défaut (équivaut à l’option de montage «case = dir»).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-399">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="cbc9f-400">L’utilisation de «case = force» (l’ancien comportement) requiert la définition d’une clé de registre.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-400">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="cbc9f-401">Exécutez la commande suivante pour activer «case = force» si vous devez l’utiliser: reg Add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="cbc9f-401">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="cbc9f-402">Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui doivent respecter la casse, utilisez fsutil. exe pour les marquer comme respectant la casse: fsutil <path> . exe file setcasesensitiveinfo Enable</span><span class="sxs-lookup"><span data-stu-id="cbc9f-402">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="cbc9f-403">Chaînes de fin NULL retournées par le commande uname syscall.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-403">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-404">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-404">Console</span></span>
* <span data-ttu-id="cbc9f-405">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-405">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-406">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-406">LTP Results:</span></span>
<span data-ttu-id="cbc9f-407">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-407">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="cbc9f-408">Build 17107</span><span class="sxs-lookup"><span data-stu-id="cbc9f-408">Build 17107</span></span>
<span data-ttu-id="cbc9f-409">Pour obtenir des informations générales sur Windows sur la build 17107, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-409">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-410">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-410">WSL</span></span>
* <span data-ttu-id="cbc9f-411">Prise en charge de TCSETSF et TCSETSW sur les points de terminaison du PTY maître [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-411">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="cbc9f-412">Le démarrage de processus d’interopérabilité simultanés peut entraîner la EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-412">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="cbc9f-413">Corriger PTRACE_ATTACH pour afficher l’état de suivi approprié dans/proc/PID/Status.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-413">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="cbc9f-414">Corriger la concurrence où les processus de courte durée clonés avec les indicateurs CLEARTID et SETTID peuvent quitter sans effacer l’adresse TID.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-414">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="cbc9f-415">Affiche un message lors de la mise à niveau des répertoires du système de fichiers Linux lors du déplacement à partir d’une build antérieure à 17093.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-415">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="cbc9f-416">Pour plus d’informations sur les modifications du système de fichiers 17093, consultez les notes de publication de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-416">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-417">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-417">Console</span></span>
* <span data-ttu-id="cbc9f-418">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-418">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-419">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-419">LTP Results:</span></span>
<span data-ttu-id="cbc9f-420">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-420">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="cbc9f-421">Build 17101</span><span class="sxs-lookup"><span data-stu-id="cbc9f-421">Build 17101</span></span>
<span data-ttu-id="cbc9f-422">Pour obtenir des informations générales sur Windows sur la build 17101, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-422">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-423">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-423">WSL</span></span>
* <span data-ttu-id="cbc9f-424">Prise en charge de signalfd.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-424">Support for signalfd.</span></span> <span data-ttu-id="cbc9f-425">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-425">[GH 129]</span></span>
* <span data-ttu-id="cbc9f-426">Prennent en charge les noms de fichier contenant des caractères NTFS non conformes en les codant comme des caractères Unicode privés.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-426">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="cbc9f-427">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-427">[GH 1514]</span></span>
* <span data-ttu-id="cbc9f-428">Le montage automatique est en lecture seule lorsque l’écriture n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-428">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="cbc9f-429">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-429">[GH 2603]</span></span>
* <span data-ttu-id="cbc9f-430">Autoriser le collage de paires de substitution Unicode (comme les caractères Emoji).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-430">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="cbc9f-431">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-431">[GH 2765]</span></span>
* <span data-ttu-id="cbc9f-432">Les Pseudo-fichiers dans/proc et/sys doivent retourner lecture et écriture prêts à partir de Select, Poll, epoll, et al. [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-432">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="cbc9f-433">Corrigez le problème qui peut amener le service à passer en boucle infinie lorsque le registre a été falsifié ou qu’il est endommagé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-433">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="cbc9f-434">Corrigez les messages NetLink pour qu’ils fonctionnent avec la version plus récente (en amont 4,14) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-434">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-435">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-435">Console</span></span>
* <span data-ttu-id="cbc9f-436">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-436">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-437">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-437">LTP Results:</span></span>
<span data-ttu-id="cbc9f-438">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-438">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="cbc9f-439">Build 17093</span><span class="sxs-lookup"><span data-stu-id="cbc9f-439">Build 17093</span></span>
<span data-ttu-id="cbc9f-440">Pour obtenir des informations générales sur Windows sur la build 17093, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-440">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="cbc9f-441">Important :</span><span class="sxs-lookup"><span data-stu-id="cbc9f-441">Important:</span></span>
<span data-ttu-id="cbc9f-442">Quand vous démarrez WSL pour la première fois après la mise à niveau vers cette Build, vous devez effectuer une mise à niveau des répertoires du système de fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-442">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="cbc9f-443">Cela peut prendre plusieurs minutes. par conséquent, WSL peut sembler démarrer lentement.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-443">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="cbc9f-444">Cela ne doit se produire qu’une seule fois pour chaque distribution que vous avez installée à partir du magasin.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-444">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="cbc9f-445">Prise en charge améliorée du respect de la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-445">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="cbc9f-446">DrvFs prend désormais en charge le respect de la casse par répertoire.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-446">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="cbc9f-447">Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme respectant la casse, ce qui permet même aux applications Windows d’ouvrir correctement les fichiers qui diffèrent uniquement par la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-447">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="cbc9f-448">DrvFs dispose de nouvelles options de montage contrôlant le respect de la casse par répertoire</span><span class="sxs-lookup"><span data-stu-id="cbc9f-448">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="cbc9f-449">case = force: tous les répertoires sont traités comme respectant la casse (à l’exception de la racine du lecteur).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-449">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="cbc9f-450">Les nouveaux répertoires créés avec WSL sont marqués en respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-450">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="cbc9f-451">Il s’agit du comportement hérité, à l’exception du marquage de nouveaux répertoires sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-451">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="cbc9f-452">case = dir: seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme respectant la casse; les autres répertoires ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-452">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="cbc9f-453">Les nouveaux répertoires créés avec WSL sont marqués en respectant la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-453">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="cbc9f-454">case = OFF: seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme respectant la casse; les autres répertoires ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-454">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="cbc9f-455">Les nouveaux répertoires créés avec WSL sont marqués comme non sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-455">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="cbc9f-456">Remarque: cet indicateur n’est pas défini pour les répertoires créés par WSL dans les versions précédentes, donc ils ne seront pas traités comme respectant la casse si vous utilisez l’option «case = dir».</span><span class="sxs-lookup"><span data-stu-id="cbc9f-456">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="cbc9f-457">Un moyen de définir cet indicateur sur des répertoires existants sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-457">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="cbc9f-458">Exemple de montage avec ces options (pour les lecteurs existants, vous devez d’abord démonter avant de pouvoir monter avec des options différentes): sudo mount-t drvfs C:/mnt/c-o case = dir</span><span class="sxs-lookup"><span data-stu-id="cbc9f-458">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="cbc9f-459">Pour le moment, case = force est toujours l’option par défaut.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-459">For now, case=force is still the default option.</span></span> <span data-ttu-id="cbc9f-460">Celui-ci sera remplacé par case = dir dans le futur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-460">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="cbc9f-461">Vous pouvez maintenant utiliser des barres obliques dans les chemins d’accès Windows lors du montage de DrvFs, par exemple: sudo mount-t DrvFs//Server/Share/mnt/share</span><span class="sxs-lookup"><span data-stu-id="cbc9f-461">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="cbc9f-462">WSL traite maintenant le fichier/etc/fstab au démarrage de l’instance [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-462">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="cbc9f-463">Cette opération est effectuée avant le montage automatique des lecteurs DrvFs. les lecteurs déjà montés par fstab ne sont pas remontés automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-463">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="cbc9f-464">Ce comportement peut être désactivé à l’aide de WSL. conf.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-464">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="cbc9f-465">Les fichiers Mount, mountinfo et mountstats dans/proc échappent correctement aux caractères spéciaux tels que les barres obliques inverses et les espaces [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-465">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="cbc9f-466">Les fichiers spéciaux créés avec DrvFs tels que les liens symboliques WSL, ou FIFO et sockets lorsque les métadonnées sont activées, peuvent maintenant être copiés et déplacés de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-466">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="cbc9f-467">WSL est plus configurable avec WSL. conf</span><span class="sxs-lookup"><span data-stu-id="cbc9f-467">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="cbc9f-468">Nous avons ajouté une méthode vous permettant de configurer automatiquement certaines fonctionnalités dans WSL qui seront appliquées chaque fois que vous lancerez le sous-système.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-468">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="cbc9f-469">Cela comprend les options de montage automatique et la configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-469">This includes automount options and network configuration.</span></span> <span data-ttu-id="cbc9f-470">Pour en savoir plus, consultez notre billet de blog à l’adresse suivante: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="cbc9f-470">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="cbc9f-471">AF_UNIX autorise les connexions de socket entre les processus Linux sur WSL et les processus natifs Windows</span><span class="sxs-lookup"><span data-stu-id="cbc9f-471">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="cbc9f-472">Les applications WSL et Windows peuvent désormais communiquer entre elles via des sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-472">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="cbc9f-473">Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible pour les applications Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-473">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="cbc9f-474">Désormais, il est possible d’utiliser des sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-474">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="cbc9f-475">Pour en savoir plus, consultez notre billet de blog à l’adresse https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="cbc9f-475">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-476">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-476">WSL</span></span>
* <span data-ttu-id="cbc9f-477">Prise en charge de mmap () avec MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-477">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="cbc9f-478">Prise en charge de CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-478">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="cbc9f-479">Gérer le signal de fin non SIGCHLD dans le clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-479">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="cbc9f-480">Stub/proc/sys/FS/inotify/max_user_instances et/proc/sys/FS/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-480">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="cbc9f-481">Erreur lors du chargement des binaires ELF qui contiennent des en-têtes de charge avec des décalages non nuls [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-481">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="cbc9f-482">Zéro pour les octets de page de fin lors du chargement des images.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-482">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="cbc9f-483">Réduire les cas où execve arrête silencieusement le processus</span><span class="sxs-lookup"><span data-stu-id="cbc9f-483">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-484">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-484">Console</span></span>
* <span data-ttu-id="cbc9f-485">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-486">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-486">LTP Results:</span></span>
<span data-ttu-id="cbc9f-487">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-487">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="cbc9f-488">Build 17083</span><span class="sxs-lookup"><span data-stu-id="cbc9f-488">Build 17083</span></span>
<span data-ttu-id="cbc9f-489">Pour obtenir des informations générales sur Windows sur la build 17083, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-489">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-490">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-490">WSL</span></span>
* <span data-ttu-id="cbc9f-491">Correction de la vérification de bogue liée à epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-491">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="cbc9f-492">Correction des blocages lors de la désactivation de ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-492">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="cbc9f-493">S’assurer que les opérations mmap apparaissent atomiques [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-493">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-494">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-494">Console</span></span>
* <span data-ttu-id="cbc9f-495">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-496">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-496">LTP Results:</span></span>
<span data-ttu-id="cbc9f-497">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-497">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="cbc9f-498">Build 17074</span><span class="sxs-lookup"><span data-stu-id="cbc9f-498">Build 17074</span></span>
<span data-ttu-id="cbc9f-499">Pour obtenir des informations générales sur Windows sur la build 17074, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-499">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-500">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-500">WSL</span></span>
* <span data-ttu-id="cbc9f-501">Format de stockage fixe des métadonnées DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-501">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="cbc9f-502">**Important :** Les métadonnées DrvFs créées avant cette génération s’affichent de manière incorrecte ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-502">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="cbc9f-503">Pour corriger les fichiers affectés, utilisez chmod et chown pour réappliquer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-503">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="cbc9f-504">Correction du problème avec plusieurs signaux et syscalls redémarrable.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-504">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-505">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-505">Console</span></span>
* <span data-ttu-id="cbc9f-506">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-506">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-507">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-507">LTP Results:</span></span>
<span data-ttu-id="cbc9f-508">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-508">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="cbc9f-509">Build 17063</span><span class="sxs-lookup"><span data-stu-id="cbc9f-509">Build 17063</span></span>
<span data-ttu-id="cbc9f-510">Pour obtenir des informations générales sur Windows sur la build 17063, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-510">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cbc9f-511">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-511">WSL</span></span>
* <span data-ttu-id="cbc9f-512">DrvFs prend en charge des métadonnées Linux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-512">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="cbc9f-513">Cela permet de définir le propriétaire et le mode des fichiers à l’aide de chmod/chown, ainsi que la création de fichiers spéciaux, tels que les FIFO, les sockets Unix et les fichiers d’appareil.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-513">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="cbc9f-514">Cela est désactivé par défaut pour le moment, car il est toujours expérimental.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-514">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="cbc9f-515">**Remarque :**  Nous avons résolu un bogue dans le format de métadonnées utilisé par DrvFs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-515">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="cbc9f-516">Bien que les métadonnées fonctionnent sur cette build pour l’expérimentation, les builds ultérieures ne lisent pas correctement les métadonnées créées par cette Build.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-516">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="cbc9f-517">Vous devrez peut-être mettre à jour manuellement le propriétaire des fichiers et des appareils modifiés avec un ID d’appareil personnalisé doit être recréé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-517">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="cbc9f-518">Pour activer, montez DrvFs avec l’option Metadata (pour l’activer sur un montage existant, vous devez d’abord le démonter):</span><span class="sxs-lookup"><span data-stu-id="cbc9f-518">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="cbc9f-519">Les autorisations Linux sont ajoutées en tant que métadonnées supplémentaires au fichier; ils n’affectent pas les autorisations Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-519">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="cbc9f-520">N’oubliez pas que la modification d’un fichier à l’aide d’un éditeur Windows peut supprimer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-520">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="cbc9f-521">Dans ce cas, le fichier reprend ses autorisations par défaut.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-521">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="cbc9f-522">Ajout d’options de montage à DrvFs pour contrôler les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-522">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="cbc9f-523">UID: ID utilisateur utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-523">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="cbc9f-524">GID: ID de groupe utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-524">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="cbc9f-525">umask: masque octal d’autorisations à exclure pour tous les fichiers et répertoires.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-525">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="cbc9f-526">fmask: masque octal d’autorisations à exclure pour tous les fichiers normaux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-526">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="cbc9f-527">dmask: masque octal d’autorisations à exclure pour tous les répertoires.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-527">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="cbc9f-528">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cbc9f-528">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="cbc9f-529">Combinez avec l’option de métadonnées pour spécifier des autorisations par défaut pour les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-529">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="cbc9f-530">A introduit une nouvelle variable d' `WSLENV`environnement,, pour configurer le mode de passage des variables d’environnement entre WSL et Win32.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-530">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="cbc9f-531">Exemple :</span><span class="sxs-lookup"><span data-stu-id="cbc9f-531">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="cbc9f-532">`WSLENV`liste de variables d’environnement séparées par des virgules qui peuvent être incluses lors du lancement de processus WSL à partir de processus Win32 ou Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-532">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="cbc9f-533">Chaque variable peut être suivie d’un suffixe à l’aide d’une barre oblique suivie de balises pour spécifier la façon dont elle est traduite.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-533">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="cbc9f-534">p La valeur est un chemin d’accès qui doit être traduit entre les chemins d’accès WSL et les chemins d’accès Win32.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-534">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="cbc9f-535">budget La valeur est une liste de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-535">l: The value is a list of paths.</span></span> <span data-ttu-id="cbc9f-536">Dans WSL, il s’agit d’une liste délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-536">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="cbc9f-537">Dans Win32, il s’agit d’une liste délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-537">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="cbc9f-538">GOUDJARATI La valeur doit être incluse uniquement lors de l’appel de WSL à partir de Win32</span><span class="sxs-lookup"><span data-stu-id="cbc9f-538">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="cbc9f-539">s La valeur doit être incluse uniquement lors de l’appel de Win32 à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-539">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="cbc9f-540">Vous pouvez définir `WSLENV` in. bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-540">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="cbc9f-541">les montages drvfs préservent correctement les horodateurs de tar, CP-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-541">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="cbc9f-542">drvfs liens symboliques signale la taille correcte (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-542">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="cbc9f-543">la lecture/écriture fonctionne pour les très grandes tailles d’e/s (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-543">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="cbc9f-544">waitpid fonctionne avec des ID de groupe de processus (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-544">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="cbc9f-545">amélioration significative des performances de mmap pour les régions de réserve volumineuses; améliore les performances de GHC (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-545">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="cbc9f-546">la personnalité prend en charge READ_IMPLIES_EXEC; corrige les maxima et les clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-546">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="cbc9f-547">mprotect prend en charge PROT_GROWSDOWN; résout clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-547">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="cbc9f-548">correction des erreurs de page en mode de survalidation; résout sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-548">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="cbc9f-549">le clone prend en charge davantage de combinaisons d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-549">clone supports more flags combinations</span></span>
* <span data-ttu-id="cbc9f-550">Prend en charge Select/epoll de fichiers epoll (auparavant un non-op).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-550">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="cbc9f-551">Notifier ptrace des syscalls non implémentés.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-551">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="cbc9f-552">Ignorer les interfaces qui ne sont pas installées lors de la génération de noms de resolv. conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-552">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="cbc9f-553">Énumérer les interfaces réseau sans adresse physique.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-553">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="cbc9f-554">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-554">[GH 2685]</span></span>
* <span data-ttu-id="cbc9f-555">Améliorations et correctifs de bogues supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-555">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="cbc9f-556">Outils Linux disponibles pour les développeurs sur Windows</span><span class="sxs-lookup"><span data-stu-id="cbc9f-556">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="cbc9f-557">La ligne de commande Windows chaîne d’outils comprend bsdtar (tar) et une boucle.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-557">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="cbc9f-558">Lisez [ce blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et découvrir comment ils conforment l’expérience des développeurs sur Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-558">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="cbc9f-559">`AF_UNIX`est disponible dans le kit de développement logiciel (SDK) Windows Insider (17061 +).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-559">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="cbc9f-560">Lisez [ce blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus `AF_UNIX` sur et sur la manière dont les développeurs sur Windows peuvent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-560">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="cbc9f-561">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-561">Console</span></span>
* <span data-ttu-id="cbc9f-562">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-563">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-563">LTP Results:</span></span>
<span data-ttu-id="cbc9f-564">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-564">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="cbc9f-565">Build 17046</span><span class="sxs-lookup"><span data-stu-id="cbc9f-565">Build 17046</span></span>

<span data-ttu-id="cbc9f-566">Pour obtenir des informations générales sur Windows sur la build 17046, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-566">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="cbc9f-567">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-567">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-568">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-568">WSL</span></span>
- <span data-ttu-id="cbc9f-569">Autoriser les processus à s’exécuter sans terminal actif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-569">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="cbc9f-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="cbc9f-571">Meilleure prise en charge de CLONE_VFORK et CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-571">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="cbc9f-572">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-572">[GH 1878, 2615]</span></span>
- <span data-ttu-id="cbc9f-573">Ignorez les pilotes de filtre TDI pour les opérations de mise en réseau WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-573">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="cbc9f-574">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-574">[GH 1554]</span></span>
- <span data-ttu-id="cbc9f-575">DrvFs crée une liens symboliques NT lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-575">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="cbc9f-576">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-576">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="cbc9f-577">La cible du lien doit être relative, ne doit pas traverser les points de montage ou les liens symboliques et doit exister.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-577">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="cbc9f-578">L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela nécessite normalement que vous lançiez WSL. exe avec élévation de privilèges), à moins que le mode développeur soit activé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-578">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="cbc9f-579">Dans toutes les autres situations, DrvFs crée toujours WSL liens symboliques.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-579">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="cbc9f-580">Autorisez l’exécution simultanée d’instances WSL avec élévation de privilèges et non élevées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-580">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="cbc9f-581">Prise en charge/proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="cbc9f-581">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="cbc9f-582">Ajoutez wslpath pour effectuer des conversions de chemins d’accès Windows > <.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-582">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="cbc9f-583">[GH 522, 1243, 1834, 2327, et al.]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-583">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="cbc9f-584">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-584">Console</span></span>
- <span data-ttu-id="cbc9f-585">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-585">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-586">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-586">LTP Results:</span></span>
<span data-ttu-id="cbc9f-587">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-587">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="cbc9f-588">Build 17040</span><span class="sxs-lookup"><span data-stu-id="cbc9f-588">Build 17040</span></span>

<span data-ttu-id="cbc9f-589">Pour obtenir des informations générales sur Windows sur la build 17040, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-589">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-590">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-591">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-591">WSL</span></span>
- <span data-ttu-id="cbc9f-592">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-592">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-593">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-593">Console</span></span>
- <span data-ttu-id="cbc9f-594">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-594">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-595">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-595">LTP Results:</span></span>
<span data-ttu-id="cbc9f-596">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-596">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="cbc9f-597">Build 17035</span><span class="sxs-lookup"><span data-stu-id="cbc9f-597">Build 17035</span></span>

<span data-ttu-id="cbc9f-598">Pour obtenir des informations générales sur Windows sur la build 17035, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-598">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-599">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-599">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-600">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-600">WSL</span></span>
- <span data-ttu-id="cbc9f-601">L’accès aux fichiers sur DrvFs peut parfois échouer avec EINVAL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-601">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="cbc9f-602">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-602">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-603">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-603">Console</span></span>
- <span data-ttu-id="cbc9f-604">Perte de couleur lors de l’insertion/suppression de lignes en mode VT.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-604">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-605">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-605">LTP Results:</span></span>
<span data-ttu-id="cbc9f-606">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-606">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="cbc9f-607">Build 17025</span><span class="sxs-lookup"><span data-stu-id="cbc9f-607">Build 17025</span></span>

<span data-ttu-id="cbc9f-608">Pour obtenir des informations générales sur Windows sur la build 17025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-608">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-609">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-609">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-610">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-610">WSL</span></span>
- <span data-ttu-id="cbc9f-611">Démarrer les processus initiaux dans un nouveau groupe de processus de premier plan [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-611">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="cbc9f-612">Correctifs de remise SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-612">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="cbc9f-613">Générez un nom de pont virtuel par défaut s’il n’est pas fourni [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-613">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="cbc9f-614">Implémentez/proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-614">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="cbc9f-615">Autres correctifs de canal stdout/stderr Interop.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-615">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="cbc9f-616">Appel système syncfs stub.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-616">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-617">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-617">Console</span></span>
- <span data-ttu-id="cbc9f-618">Correction de la traduction VT d’entrée pour les consoles tierces [GH 111]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-618">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-619">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-619">LTP Results:</span></span>
<span data-ttu-id="cbc9f-620">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-620">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="cbc9f-621">Build 17017</span><span class="sxs-lookup"><span data-stu-id="cbc9f-621">Build 17017</span></span>

<span data-ttu-id="cbc9f-622">Pour obtenir des informations générales sur Windows sur la build 17017, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-622">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-623">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-623">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-624">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-624">WSL</span></span>
- <span data-ttu-id="cbc9f-625">Ignorer les en-têtes de programme ELF vides [GH 330].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-625">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="cbc9f-626">Autoriser LxssManager à créer des instances WSL pour les utilisateurs non interactifs (SSH et prise en charge des tâches planifiées) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-626">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="cbc9f-627">Prise en charge des scénarios WSL-> Win32-> WSL («création») [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-627">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="cbc9f-628">Prise en charge limitée de l’arrêt des applications console appelées par le biais de l’interopérabilité [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-628">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="cbc9f-629">Options de montage de prise en charge pour devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-629">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="cbc9f-630">Ptrace bloquant le démarrage enfant [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-630">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="cbc9f-631">EPOLLET manquant certains événements [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-631">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="cbc9f-632">Retourne plus de données pour PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-632">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="cbc9f-633">Getdents avec lseek donne des résultats incorrects.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-633">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="cbc9f-634">Corriger certaines interruptions de l’application d’interopérabilité Win32, en attente d’une entrée sur un canal qui n’a plus de données.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-634">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="cbc9f-635">Prise en charge O_ASYNC pour les fichiers TTY/Pty.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-635">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="cbc9f-636">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-636">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-637">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-637">Console</span></span>
- <span data-ttu-id="cbc9f-638">Aucune modification de la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-638">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-639">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-639">LTP Results:</span></span>
<span data-ttu-id="cbc9f-640">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-640">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="cbc9f-641">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="cbc9f-641">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="cbc9f-642">Build 16288</span><span class="sxs-lookup"><span data-stu-id="cbc9f-642">Build 16288</span></span>

<span data-ttu-id="cbc9f-643">Pour obtenir des informations générales sur Windows sur la build 16288, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-643">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-644">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-645">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-645">WSL</span></span>
- <span data-ttu-id="cbc9f-646">Initialisez et signalez correctement uid, GID et mode pour les descripteurs de fichiers socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-646">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="cbc9f-647">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-647">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-648">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-648">Console</span></span>
- <span data-ttu-id="cbc9f-649">Aucune modification de la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-649">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-650">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-650">LTP Results:</span></span>
<span data-ttu-id="cbc9f-651">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="cbc9f-651">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="cbc9f-652">Build 16278</span><span class="sxs-lookup"><span data-stu-id="cbc9f-652">Build 16278</span></span>

<span data-ttu-id="cbc9f-653">Pour obtenir des informations générales sur Windows sur la build 162738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-653">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-654">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-655">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-655">WSL</span></span>
- <span data-ttu-id="cbc9f-656">Annuler le mappage explicite des vues mappées des sections sauvegardées dans un fichier lors du déchirement de l’État LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-656">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="cbc9f-657">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-657">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-658">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-658">Console</span></span>
- <span data-ttu-id="cbc9f-659">Aucune modification de la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-660">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-660">LTP Results:</span></span>
<span data-ttu-id="cbc9f-661">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="cbc9f-661">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="cbc9f-662">Build 16275</span><span class="sxs-lookup"><span data-stu-id="cbc9f-662">Build 16275</span></span>

<span data-ttu-id="cbc9f-663">Pour obtenir des informations générales sur Windows sur la build 162735, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-663">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-664">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-665">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-665">WSL</span></span>
- <span data-ttu-id="cbc9f-666">Aucune modification liée à WSL dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-666">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-667">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-667">Console</span></span>
- <span data-ttu-id="cbc9f-668">Aucune modification de la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-668">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-669">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-669">LTP Results:</span></span>
<span data-ttu-id="cbc9f-670">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="cbc9f-670">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="cbc9f-671">Build 16273</span><span class="sxs-lookup"><span data-stu-id="cbc9f-671">Build 16273</span></span>

<span data-ttu-id="cbc9f-672">Pour obtenir des informations générales sur Windows sur la build 16273, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-672">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-673">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-674">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-674">WSL</span></span>
- <span data-ttu-id="cbc9f-675">Résolution d’un problème où DrvFs a parfois signalé un type de fichier incorrect pour les répertoires [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-675">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="cbc9f-676">Autoriser la création de sockets NETLINK_KOBJECT_UEVENT pour débloquer des programmes qui utilisent UEVENT [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-676">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="cbc9f-677">Ajout de la prise en charge de la connexion non bloquante [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-677">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="cbc9f-678">Implémenter l’indicateur d’appel système CLONE_FS Clone [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-678">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="cbc9f-679">Résoudre les problèmes liés à la non-gestion des tabulations ou des guillemets correctement dans l’interopérabilité NT [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-679">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="cbc9f-680">Erreur de résolution de l’accès refusé lors de la tentative de redémarrage des instances WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-680">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="cbc9f-681">Implémenter des opérations Futex FUTEX_REQUEUE et FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-681">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="cbc9f-682">Corriger les autorisations pour différents fichiers SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-682">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="cbc9f-683">Corriger le blocage de la pile Haskell lors de l’installation [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-683">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="cbc9f-684">Implémenter les indicateurs binfmt_misc’C' 'O’et’P' [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-684">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="cbc9f-685">Add/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-685">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="cbc9f-686">Ajout de la prise en charge partielle de l’appel système ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-686">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="cbc9f-687">Stub SO_REUSEPORT & ajout de la prise en charge de SO_PASSCRED pour les sockets NetLink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-687">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="cbc9f-688">Retourner des codes d’erreur différents à partir de RegisterDistribuiton si une distribution est en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-688">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="cbc9f-689">Autoriser la désinscription des distributions WSL partiellement installées via wslconfig. exe</span><span class="sxs-lookup"><span data-stu-id="cbc9f-689">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="cbc9f-690">Corriger le blocage du test de socket Python à partir de UDP:: MSG_PEEK</span><span class="sxs-lookup"><span data-stu-id="cbc9f-690">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="cbc9f-691">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-691">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-692">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-692">Console</span></span>
- <span data-ttu-id="cbc9f-693">Aucune modification de la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-693">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-694">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-694">LTP Results:</span></span>
<span data-ttu-id="cbc9f-695">Nombre total de tests: 1904</span><span class="sxs-lookup"><span data-stu-id="cbc9f-695">Total Tests: 1904</span></span><br/>
<span data-ttu-id="cbc9f-696">Nombre total de tests ignorés: 209</span><span class="sxs-lookup"><span data-stu-id="cbc9f-696">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="cbc9f-697">Nombre total d’échecs: 229</span><span class="sxs-lookup"><span data-stu-id="cbc9f-697">Total Failures: 229</span></span><br/>
[<span data-ttu-id="cbc9f-698">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-698">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="cbc9f-699">Build 16257</span><span class="sxs-lookup"><span data-stu-id="cbc9f-699">Build 16257</span></span>

<span data-ttu-id="cbc9f-700">Pour obtenir des informations générales sur Windows sur la build 16257, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-700">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-701">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-701">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-702">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-702">WSL</span></span>
- <span data-ttu-id="cbc9f-703">Implémenter un appel système prlimit64</span><span class="sxs-lookup"><span data-stu-id="cbc9f-703">Implement prlimit64 system call</span></span>
- <span data-ttu-id="cbc9f-704">Ajout de la prise en charge de commande ulimit-n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-704">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="cbc9f-705">Stub MSG_MORE pour les sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-705">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="cbc9f-706">Corriger le comportement de vecteur auxiliaire AT_EXECFN non valide [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-706">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="cbc9f-707">Corriger le comportement de copier/coller pour console/TTY et ajouter une meilleure gestion de mémoire tampon complète [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-707">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="cbc9f-708">Définir AT_SECURE dans le vecteur auxiliaire pour les programmes Set-User-ID et Set-Group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-708">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="cbc9f-709">Psuedo-point de terminaison du contrôleur de terminal non géré TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-709">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="cbc9f-710">Fix lseek effectue le rembobinage des répertoires dans LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-710">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="cbc9f-711">/dev/ptmx se bloque après une utilisation intensive [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-711">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="cbc9f-712">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-712">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-713">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-713">Console</span></span>
- <span data-ttu-id="cbc9f-714">Correction pour les lignes/traits de soulignement horizontaux partout [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-714">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="cbc9f-715">Correction de l’ordre du processus modification rendant la NPM plus difficile à fermer [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-715">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="cbc9f-716">Ajout de notre nouveau jeu de couleurs: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="cbc9f-716">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-717">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-717">LTP Results:</span></span>
<span data-ttu-id="cbc9f-718">Aucune modification depuis 16251</span><span class="sxs-lookup"><span data-stu-id="cbc9f-718">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-719">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-719">Syscall Support</span></span>
<span data-ttu-id="cbc9f-720">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-720">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-721">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-721">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="cbc9f-722">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="cbc9f-722">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="cbc9f-723">GitHub problème 2392: Dossiers Windows non reconnus par WSL...</span><span class="sxs-lookup"><span data-stu-id="cbc9f-723">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="cbc9f-724">Dans la build 16257, WSL rencontre des problèmes lors de l’énumération des `/mnt/c/...`fichiers/dossiers Windows via.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-724">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="cbc9f-725">Ce problème a été résolu et doit être publié dans le cadre de la génération de la version de la semaine à partir de 8/14/2017.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-725">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="cbc9f-726">Build 16251</span><span class="sxs-lookup"><span data-stu-id="cbc9f-726">Build 16251</span></span>

<span data-ttu-id="cbc9f-727">Pour obtenir des informations générales sur Windows sur la build 16251, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-727">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-728">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-729">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-729">WSL</span></span>
- <span data-ttu-id="cbc9f-730">Supprimez la balise bêta du composant facultatif WSL. pour plus d’informations, consultez le billet de [blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) .</span><span class="sxs-lookup"><span data-stu-id="cbc9f-730">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="cbc9f-731">Initialisez correctement l’UID et le GID enregistrés pour les fichiers binaires Set-User-ID et Set-Group-ID sur exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-731">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="cbc9f-732">Ajout de la prise en charge de ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-732">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="cbc9f-733">Ajout de la prise en charge de ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-733">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="cbc9f-734">Correction des ptrace à arrêter sur les signaux ignorés</span><span class="sxs-lookup"><span data-stu-id="cbc9f-734">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="cbc9f-735">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-735">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-736">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-736">Console</span></span>
- <span data-ttu-id="cbc9f-737">Aucune modification de la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-738">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-738">LTP Results:</span></span>
<span data-ttu-id="cbc9f-739">Nombre de tests réussis: 768</span><span class="sxs-lookup"><span data-stu-id="cbc9f-739">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="cbc9f-740">Nombre de tests ayant échoué: 244</span><span class="sxs-lookup"><span data-stu-id="cbc9f-740">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="cbc9f-741">Nombre de tests ignorés: 96</span><span class="sxs-lookup"><span data-stu-id="cbc9f-741">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="cbc9f-742">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-742">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="cbc9f-743">Build 16241</span><span class="sxs-lookup"><span data-stu-id="cbc9f-743">Build 16241</span></span>

<span data-ttu-id="cbc9f-744">Pour obtenir des informations générales sur Windows sur la build 16241, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-744">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-745">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cbc9f-746">WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-746">WSL</span></span>
- <span data-ttu-id="cbc9f-747">Aucune modification liée à WSL dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-747">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="cbc9f-748">Console</span><span class="sxs-lookup"><span data-stu-id="cbc9f-748">Console</span></span>
- <span data-ttu-id="cbc9f-749">Correction pour la génération d’un mauvais caractère pour le franchissement des lignes DEC, initialement signalé [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-749">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="cbc9f-750">Correctif pour aucun texte de sortie affiché dans la page de codes 65001 (UTF8)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-750">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="cbc9f-751">Ne transférez pas les modifications apportées aux valeurs RVB d’une couleur vers d’autres parties de la palette lors de la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-751">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="cbc9f-752">Cela rendra la feuille de propriétés de la console beaucoup plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-752">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="cbc9f-753">CTRL + S ne semble pas fonctionner correctement</span><span class="sxs-lookup"><span data-stu-id="cbc9f-753">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="cbc9f-754">Non gras/-Dim totalement absent des codes d’échappement ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-754">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="cbc9f-755">La console ne prend pas en charge correctement les thèmes de couleur vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-755">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="cbc9f-756">Impossible de coller des caractères particuliers [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-756">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="cbc9f-757">Le redimensionnement du redimensionnement interagit de façon étrange avec le redimensionnement d’une fenêtre bash quand des éléments se trouvent sur la ligne de commande Edit/Command [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-757">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="cbc9f-758">Ctrl-L laisse l’écran sale [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-758">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="cbc9f-759">Bogue de rendu de la console lors de l’affichage de VT sur HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-759">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="cbc9f-760">Les caractères Japansese semblent étranges avec le caractère Unicode U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-760">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="cbc9f-761">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-761">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="cbc9f-762">Build 16237</span><span class="sxs-lookup"><span data-stu-id="cbc9f-762">Build 16237</span></span>

<span data-ttu-id="cbc9f-763">Pour obtenir des informations générales sur Windows sur la build 16237, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-763">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-764">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-764">Fixed</span></span>
- <span data-ttu-id="cbc9f-765">Utiliser des attributs par défaut pour les fichiers sans EAs dans lxfs (racine, racine, 0000)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-765">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="cbc9f-766">Ajout de la prise en charge des distributions qui utilisent des attributs étendus</span><span class="sxs-lookup"><span data-stu-id="cbc9f-766">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="cbc9f-767">Correction du remplissage pour les entrées retournées par getdents et getdents64</span><span class="sxs-lookup"><span data-stu-id="cbc9f-767">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="cbc9f-768">Correction des autorisations pour l’appel système shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-768">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="cbc9f-769">Correction de l’État epoll initial incorrect pour les TTY ne [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-769">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="cbc9f-770">Fix DrvFs readdir ne retournant pas toutes les entrées [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-770">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="cbc9f-771">Corriger LxFs readdir lorsque des fichiers sont dissociés [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-771">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="cbc9f-772">Autoriser la réouverture des fichiers drvfs non liés via procfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-772">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="cbc9f-773">Ajout d’un remplacement de clé de registre global pour la désactivation des fonctionnalités WSL (montage d’interopérabilité/lecteur)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-773">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="cbc9f-774">Correction du nombre de blocs incorrects dans «STAT» pour DrvFs (et LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-774">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="cbc9f-775">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-775">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="cbc9f-776">Build 16232</span><span class="sxs-lookup"><span data-stu-id="cbc9f-776">Build 16232</span></span>

<span data-ttu-id="cbc9f-777">Pour obtenir des informations générales sur Windows sur la build 16232, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-777">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-778">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-778">Fixed</span></span>
- <span data-ttu-id="cbc9f-779">Aucune modification liée à WSL dans cette version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-779">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="cbc9f-780">Build 16226</span><span class="sxs-lookup"><span data-stu-id="cbc9f-780">Build 16226</span></span>

<span data-ttu-id="cbc9f-781">Pour obtenir des informations générales sur Windows sur la build 16226, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-781">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-782">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-782">Fixed</span></span>
- <span data-ttu-id="cbc9f-783">prise en charge d’syscalls xattr associée (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-783">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="cbc9f-784">la prise en charge de Security. capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-784">security.capablity xattr support.</span></span>
- <span data-ttu-id="cbc9f-785">Compatibilité améliorée avec certains filtres et systèmes de fichiers, y compris les serveurs SMB non-MS.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-785">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="cbc9f-786">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-786">[GH #1952]</span></span>
- <span data-ttu-id="cbc9f-787">Prise en charge améliorée des espaces réservés OneDrive, des espaces réservés GVFS et des fichiers compressés compact OS.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-787">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="cbc9f-788">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-788">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="cbc9f-789">Build 16215</span><span class="sxs-lookup"><span data-stu-id="cbc9f-789">Build 16215</span></span>

<span data-ttu-id="cbc9f-790">Pour obtenir des informations générales sur Windows sur la build 16215, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-790">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-791">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-791">Fixed</span></span>
- <span data-ttu-id="cbc9f-792">WSL ne requiert plus le mode développeur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-792">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="cbc9f-793">Prendre en charge les jonctions de répertoires dans drvfs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-793">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="cbc9f-794">Gérez la désinstallation des packages AppX de distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-794">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="cbc9f-795">Mettez à jour procfs pour afficher les mappages privés et partagés.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-795">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="cbc9f-796">Ajoutez la possibilité pour wslconfig. exe de nettoyer les distributions partiellement installées ou désinstallées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-796">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="cbc9f-797">Ajout de la prise en charge de IP_MTU_DISCOVER pour les sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-797">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="cbc9f-798">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-798">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="cbc9f-799">Déduire la famille de protocoles pour les itinéraires vers AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-799">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="cbc9f-800">Améliorations des appareils série [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="cbc9f-800">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="cbc9f-801">Build 16199</span><span class="sxs-lookup"><span data-stu-id="cbc9f-801">Build 16199</span></span>

<span data-ttu-id="cbc9f-802">Pour obtenir des informations générales sur Windows sur la build 16199, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-802">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-803">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-803">Fixed</span></span>
- <span data-ttu-id="cbc9f-804">Aucune modification liée à WSL dans ces versions.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-804">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="cbc9f-805">Build 16193</span><span class="sxs-lookup"><span data-stu-id="cbc9f-805">Build 16193</span></span>

<span data-ttu-id="cbc9f-806">Pour obtenir des informations générales sur Windows sur la build 16193, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-806">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-807">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-807">Fixed</span></span>
- <span data-ttu-id="cbc9f-808">Condition de concurrence entre l’envoi de SIGCONT et l’arrêt d’un ThreadGroup [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-808">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="cbc9f-809">modifier les appareils TTY et Pty pour signaler FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-809">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="cbc9f-810">Correctif SSH pour IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="cbc9f-810">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="cbc9f-811">Montage DrvFs déplacé vers le démon init [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-811">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="cbc9f-812">Ajout de la prise en charge dans DrvFs pour NT liens symboliques suivant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-812">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="cbc9f-813">Build 16184</span><span class="sxs-lookup"><span data-stu-id="cbc9f-813">Build 16184</span></span>

<span data-ttu-id="cbc9f-814">Pour obtenir des informations générales sur Windows sur la build 16184, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-814">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-815">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-815">Fixed</span></span>
- <span data-ttu-id="cbc9f-816">Suppression de la tâche de maintenance de package APT (lxrun. exe/Update)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-816">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="cbc9f-817">Correction de la sortie non affichée dans à partir des processus Windows dans node. js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-817">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="cbc9f-818">Assouplir les exigences d’alignement dans lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-818">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="cbc9f-819">Correction de la gestion de l’indicateur AT_EMPTY_PATH dans un nombre d’appels système.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-819">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="cbc9f-820">Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts entraînera un comportement non défini du fichier [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-820">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="cbc9f-821">/etc/hosts hérite désormais des entrées du fichier hosts Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-821">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="cbc9f-822">Build 16179</span><span class="sxs-lookup"><span data-stu-id="cbc9f-822">Build 16179</span></span>

<span data-ttu-id="cbc9f-823">Pour obtenir des informations générales sur Windows sur la build 16179, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-823">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-824">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-824">Fixed</span></span>
- <span data-ttu-id="cbc9f-825">Aucune modification de WSL cette semaine.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-825">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="cbc9f-826">Build 16176</span><span class="sxs-lookup"><span data-stu-id="cbc9f-826">Build 16176</span></span>

<span data-ttu-id="cbc9f-827">Pour obtenir des informations générales sur Windows sur la build 16176, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-827">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-828">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-828">Fixed</span></span>

- [<span data-ttu-id="cbc9f-829">Prise en charge série activée</span><span class="sxs-lookup"><span data-stu-id="cbc9f-829">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="cbc9f-830">Ajout de l’option de socket IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-830">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="cbc9f-831">Mise en œuvre de la fonction pwritev (lors du chargement du fichier dans Nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-831">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="cbc9f-832">Ajout d’options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-832">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="cbc9f-833">Prise en charge de l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-833">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="cbc9f-834">Ajout de l’option de socket IP (V6) _MTU pour les applications nœud, traceroute, creuser, nslookup, hôte</span><span class="sxs-lookup"><span data-stu-id="cbc9f-834">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="cbc9f-835">Ajout de l’option de socket IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="cbc9f-835">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="cbc9f-836">Améliorations du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="cbc9f-836">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="cbc9f-837">Autoriser le montage de chemins d’accès UNC</span><span class="sxs-lookup"><span data-stu-id="cbc9f-837">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="cbc9f-838">Activer la prise en charge de CDFS dans drvfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-838">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="cbc9f-839">Gérer correctement les autorisations pour les systèmes de fichiers réseau dans drvfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-839">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="cbc9f-840">Ajouter la prise en charge des lecteurs distants à drvfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-840">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="cbc9f-841">Activer la prise en charge de FAT dans drvfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-841">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="cbc9f-842">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-842">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-843">Résultats de LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-843">LTP Results</span></span>
<span data-ttu-id="cbc9f-844">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="cbc9f-844">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="cbc9f-845">Build 16170</span><span class="sxs-lookup"><span data-stu-id="cbc9f-845">Build 16170</span></span>

<span data-ttu-id="cbc9f-846">Pour obtenir des informations générales sur Windows sur la build 16170, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-846">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="cbc9f-847">Nous avons publié un nouveau billet de [blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) traitant de nos efforts pour tester WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-847">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="cbc9f-848">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-848">Fixed</span></span>

- <span data-ttu-id="cbc9f-849">Option de socket de support IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-849">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="cbc9f-850">Ajoutez la prise en charge de PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-850">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="cbc9f-851">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-851">[GH 1692]</span></span>
- <span data-ttu-id="cbc9f-852">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-852">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-853">Résultats de LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-853">LTP Results</span></span>
<span data-ttu-id="cbc9f-854">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="cbc9f-854">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="cbc9f-855">Build 15046 pour Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="cbc9f-855">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="cbc9f-856">Il n’y a plus de correctifs ou de fonctionnalités WSL prévus pour être inclus dans les créateurs de mise à jour de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-856">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="cbc9f-857">Les notes de publication pour WSL reprennent dans les semaines à venir pour les ajouts ciblant les Windows Update majeures suivantes.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-857">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="cbc9f-858">Pour obtenir des informations générales sur Windows sur la build 15046 et les versions ultérieures de l’Insider, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-858">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="cbc9f-859">Build 15042</span><span class="sxs-lookup"><span data-stu-id="cbc9f-859">Build 15042</span></span>

<span data-ttu-id="cbc9f-860">Pour obtenir des informations générales sur Windows sur la build 15042, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-860">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-861">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-861">Fixed</span></span>

- <span data-ttu-id="cbc9f-862">Correction d’un blocage lors de la suppression d’un chemin d’accès se terminant par «..»</span><span class="sxs-lookup"><span data-stu-id="cbc9f-862">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="cbc9f-863">Correction d’un problème où FIONBIO ne retourne pas 0 en cas de réussite [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-863">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="cbc9f-864">Résolution du problème avec les lectures de longueur nulle des sockets de datagramme inet</span><span class="sxs-lookup"><span data-stu-id="cbc9f-864">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="cbc9f-865">Résoudre le blocage possible en raison d’une condition de concurrence dans drvfs inode Lookup [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-865">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="cbc9f-866">Prise en charge étendue des données auxiliaires de socket Unix; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-866">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="cbc9f-867">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-867">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-868">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-868">LTP Results:</span></span>
<span data-ttu-id="cbc9f-869">Nombre de tests réussis: 737</span><span class="sxs-lookup"><span data-stu-id="cbc9f-869">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="cbc9f-870">Nombre de non-passage (échec, ignoré, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="cbc9f-870">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="cbc9f-871">Build 15031</span><span class="sxs-lookup"><span data-stu-id="cbc9f-871">Build 15031</span></span>

<span data-ttu-id="cbc9f-872">Pour obtenir des informations générales sur Windows sur la build 15031, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-872">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-873">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-873">Fixed</span></span>

- <span data-ttu-id="cbc9f-874">Correction d’un bogue où le point (2) se comporterait de façon sporadique.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-874">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="cbc9f-875">Correction et problème où \* SIGPROCMASK syscalls peut corrompre un masque de signal.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-875">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="cbc9f-876">Retournez à présent la longueur de la ligne de commande dans la notification de création de processus WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-876">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="cbc9f-877">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-877">[GH 1632]</span></span>
- <span data-ttu-id="cbc9f-878">WSL signale désormais la sortie du thread via ptrace pour les blocages de GDB.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-878">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="cbc9f-879">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-879">[GH 1196]</span></span>
- <span data-ttu-id="cbc9f-880">Correction du bogue où PTYs se bloque après des e/s tmux élevées.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-880">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="cbc9f-881">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-881">[GH 1358]</span></span>
- <span data-ttu-id="cbc9f-882">Validation du délai d’attente fixe dans de nombreux appels système (Futex, SEMTIMEDOP, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-882">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="cbc9f-883">Ajout de la prise en charge de EFD_SEMAPHORE eventfd [GH 452]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-883">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="cbc9f-884">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-884">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-885">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-885">LTP Results:</span></span>
<span data-ttu-id="cbc9f-886">Nombre de tests réussis: 737</span><span class="sxs-lookup"><span data-stu-id="cbc9f-886">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="cbc9f-887">Nombre de non-passage (échec, ignoré, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="cbc9f-887">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cbc9f-888">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="cbc9f-889">Build 15025</span><span class="sxs-lookup"><span data-stu-id="cbc9f-889">Build 15025</span></span>

<span data-ttu-id="cbc9f-890">Pour obtenir des informations générales sur Windows sur la build 15025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-890">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-891">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-891">Fixed</span></span>

- <span data-ttu-id="cbc9f-892">Correction du bogue qui a enfreint grep 2,27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-892">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="cbc9f-893">Implémentation de l’indicateur EFD_SEMAPHORE pour eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-893">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="cbc9f-894">Implemented/proc/[PID]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-894">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="cbc9f-895">Prise en charge des e/s par signal pour les sockets de flux UNIX [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-895">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="cbc9f-896">Prise en charge de F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-896">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="cbc9f-897">Implémenter recvmmsg () syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-897">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="cbc9f-898">Correction du bogue où epoll_wait () n’attendait pas [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-898">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="cbc9f-899">Implémenter/proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="cbc9f-899">Implement /proc/version_signature</span></span>
- <span data-ttu-id="cbc9f-900">Tee syscall retourne désormais une erreur si les deux descripteurs de fichiers font référence au même canal</span><span class="sxs-lookup"><span data-stu-id="cbc9f-900">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="cbc9f-901">Implémentation du comportement correct pour SO_PEERCRED pour les sockets Unix</span><span class="sxs-lookup"><span data-stu-id="cbc9f-901">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="cbc9f-902">Correction de la gestion des paramètres non valides tkill syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-902">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="cbc9f-903">Modifications pour augmenter la preformace de drvfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-903">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="cbc9f-904">Correctif mineur pour le blocage des e/s Ruby</span><span class="sxs-lookup"><span data-stu-id="cbc9f-904">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="cbc9f-905">Fixed recvmsg () retournant EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-905">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="cbc9f-906">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-906">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-907">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-907">LTP Results:</span></span>
<span data-ttu-id="cbc9f-908">Nombre de tests réussis: 732</span><span class="sxs-lookup"><span data-stu-id="cbc9f-908">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="cbc9f-909">Nombre de non-passage (échec, ignoré, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="cbc9f-909">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cbc9f-910">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-910">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="cbc9f-911">Build 15019</span><span class="sxs-lookup"><span data-stu-id="cbc9f-911">Build 15019</span></span>

<span data-ttu-id="cbc9f-912">Pour obtenir des informations générales sur Windows sur la build 15019, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-912">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-913">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-913">Fixed</span></span>

- <span data-ttu-id="cbc9f-914">Correction du bogue qui signalait incorrectement l’utilisation de l’UC dans procfs pour les outils tels que htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-914">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="cbc9f-915">Lors de l’appel de Open () avec O_TRUNC sur un fichier existant, inotify génère désormais IN_MODIFY avant IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="cbc9f-915">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="cbc9f-916">Correctifs du socket Unix getsockopt SO_ERROR pour activer les postgres [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-916">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="cbc9f-917">Implémenter/proc/sys/net/Core/SOMAXCONN pour le langage GO</span><span class="sxs-lookup"><span data-stu-id="cbc9f-917">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="cbc9f-918">La tâche en arrière-plan apt-obtenir le package s’exécute désormais à partir de l’affichage</span><span class="sxs-lookup"><span data-stu-id="cbc9f-918">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="cbc9f-919">Effacez l’étendue de l’hôte IPv6 localhost (défaillance de l’infrastructure à ressort (Java)).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-919">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="cbc9f-920">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-920">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-921">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-921">LTP Results:</span></span>
<span data-ttu-id="cbc9f-922">Nombre de tests réussis: 714</span><span class="sxs-lookup"><span data-stu-id="cbc9f-922">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="cbc9f-923">Nombre de non-passage (échec, ignoré, etc.): 249</span><span class="sxs-lookup"><span data-stu-id="cbc9f-923">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="cbc9f-924">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-924">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="cbc9f-925">Build 15014</span><span class="sxs-lookup"><span data-stu-id="cbc9f-925">Build 15014</span></span>

<span data-ttu-id="cbc9f-926">Pour obtenir des informations générales sur Windows sur la build 15014, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-926">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-927">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-927">Fixed</span></span>

- <span data-ttu-id="cbc9f-928">Ctrl + C fonctionne à présent comme prévu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-928">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="cbc9f-929">htop et PS auxw affichent désormais une utilisation correcte des ressources (GH #516)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-929">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="cbc9f-930">Traduction de base des exceptions NT en signaux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-930">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="cbc9f-931">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-931">(GH #513)</span></span>
- <span data-ttu-id="cbc9f-932">fallocate échoue maintenant avec ENOSPC lorsque l’espace est insuffisant au lieu de EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-932">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="cbc9f-933">Ajout de/proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-933">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="cbc9f-934">Implémentation des appels système semop et SEMTIMEDOP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-934">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="cbc9f-935">Correction des erreurs nslookup avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-935">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="cbc9f-936">Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="cbc9f-936">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="cbc9f-937">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-937">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-938">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-938">LTP Results:</span></span>
<span data-ttu-id="cbc9f-939">Nombre de tests réussis: 709</span><span class="sxs-lookup"><span data-stu-id="cbc9f-939">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="cbc9f-940">Nombre de non-passage (échec, ignoré, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="cbc9f-940">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cbc9f-941">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-941">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="cbc9f-942">Résumé de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-942">Syscall Summary</span></span>
<span data-ttu-id="cbc9f-943">Nombre total de syscalls: 384</span><span class="sxs-lookup"><span data-stu-id="cbc9f-943">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="cbc9f-944">Total implémenté: 235</span><span class="sxs-lookup"><span data-stu-id="cbc9f-944">Total Implemented: 235</span></span> </br>
<span data-ttu-id="cbc9f-945">Nombre total de stubs: 22</span><span class="sxs-lookup"><span data-stu-id="cbc9f-945">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="cbc9f-946">Total non implémenté: 127</span><span class="sxs-lookup"><span data-stu-id="cbc9f-946">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="cbc9f-947">Répartition détaillée</span><span class="sxs-lookup"><span data-stu-id="cbc9f-947">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="cbc9f-948">Build 15007</span><span class="sxs-lookup"><span data-stu-id="cbc9f-948">Build 15007</span></span>

<span data-ttu-id="cbc9f-949">Pour obtenir des informations générales sur Windows sur la build 15007, visitez le [blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-949">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="cbc9f-950">Problème connu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-950">Known Issue</span></span>

- <span data-ttu-id="cbc9f-951">Il existe un bogue connu dans lequel la console ne reconnaît pas une <key> entrée Ctrl +.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="cbc9f-952">Cela comprend la commande Ctrl-c qui agit comme une touche «c» normale.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="cbc9f-953">Solution de contournement : Mappez une autre clé à Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="cbc9f-954">Par exemple, pour mapper Ctrl + K à Ctrl + C, procédez comme suit: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="cbc9f-955">Ce mappage est par terminal et doit être effectué à *chaque* fois que bash est lancé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="cbc9f-956">Les utilisateurs peuvent explorer l’option permettant de les inclure dans leur`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="cbc9f-956">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="cbc9f-957">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-957">Fixed</span></span>

- <span data-ttu-id="cbc9f-958">Correction du problème où l’exécution de WSL consomme 100% d’un cœur de processeur</span><span class="sxs-lookup"><span data-stu-id="cbc9f-958">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="cbc9f-959">Option de socket IP_PKTINFO, IPV6_RECVPKTINFO désormais prise en charge.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-959">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="cbc9f-960">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-960">(GH #851, 987)</span></span>
- <span data-ttu-id="cbc9f-961">Tronquer l’adresse physique de l’interface réseau à 16 octets dans lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-961">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="cbc9f-962">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-962">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-963">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-963">LTP Results:</span></span>
<span data-ttu-id="cbc9f-964">Nombre de tests réussis: 709</span><span class="sxs-lookup"><span data-stu-id="cbc9f-964">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="cbc9f-965">Nombre de non-passage (échec, ignoré, etc.): 255</span><span class="sxs-lookup"><span data-stu-id="cbc9f-965">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cbc9f-966">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-966">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="cbc9f-967">Build 15002</span><span class="sxs-lookup"><span data-stu-id="cbc9f-967">Build 15002</span></span>

<span data-ttu-id="cbc9f-968">Pour obtenir des informations générales sur Windows sur la build 15002, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-968">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="cbc9f-969">Problème connu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-969">Known Issue</span></span>

<span data-ttu-id="cbc9f-970">Deux problèmes connus:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-970">Two known issues:</span></span>
- <span data-ttu-id="cbc9f-971">Il existe un bogue connu dans lequel la console ne reconnaît pas une <key> entrée Ctrl +.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="cbc9f-972">Cela comprend la commande Ctrl-c qui agit comme une touche «c» normale.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="cbc9f-973">Solution de contournement : Mappez une autre clé à Ctrl + C.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="cbc9f-974">Par exemple, pour mapper Ctrl + K à Ctrl + C, procédez comme suit: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="cbc9f-975">Ce mappage est par terminal et doit être effectué à *chaque* fois que bash est lancé.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="cbc9f-976">Les utilisateurs peuvent explorer l’option permettant de les inclure dans leur`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="cbc9f-976">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="cbc9f-977">Pendant l’exécution de WSL, un thread système consomme 100% d’un cœur de processeur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-977">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="cbc9f-978">La cause initiale a été résolue et corrigée en interne.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-978">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="cbc9f-979">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-979">Fixed</span></span>

- <span data-ttu-id="cbc9f-980">Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-980">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="cbc9f-981">Toute tentative de démarrage d’une session à un niveau différent est bloquée.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-981">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="cbc9f-982">Cela signifie que les consoles Administrateur et non-administrateur ne peuvent pas s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-982">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="cbc9f-983">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-983">(GH #626)</span></span>
<br/>
- <span data-ttu-id="cbc9f-984">Mise en œuvre des messages NETLINK_ROUTE suivants (nécessite l’administrateur Windows)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-984">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="cbc9f-985">RTM_NEWADDR (prend `ip addr add`en charge)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-985">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="cbc9f-986">RTM_NEWROUTE (prend `ip route add`en charge)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-986">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="cbc9f-987">RTM_DELADDR (prend `ip addr del`en charge)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-987">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="cbc9f-988">RTM_DELROUTE (prend `ip route del`en charge)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-988">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="cbc9f-989">La vérification des tâches planifiées pour les packages à mettre à jour ne s’exécutera plus sur une connexion limitée (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-989">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="cbc9f-990">Correction de l’erreur où le canaling est coincé, c.-à-d. bash-r «LS-alR/» | bash-c «Cat» (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-990">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="cbc9f-991">Implémentation de l’option de socket TCP_KEEPCNT (GH #843)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-991">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="cbc9f-992">Implémentation de l’option de socket IP_MTU_DISCOVER INET (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-992">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="cbc9f-993">Suppression des fonctionnalités héritées pour exécuter des binaires NT à partir de la recherche de chemin d’accès NT.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-993">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="cbc9f-994">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-994">(GH #1325)</span></span>
- <span data-ttu-id="cbc9f-995">Mode de correction de/dev/kmsg pour autoriser l’accès de groupe/autre accès en lecture (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-995">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="cbc9f-996">Implemented/proc/sys/kernel/Random/UUID (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-996">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="cbc9f-997">Erreur corrigée où l’heure de début du processus s’est affichée sous la forme année 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-997">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="cbc9f-998">Variable d’environnement de terme par défaut basculée vers xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-998">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="cbc9f-999">Modification de la façon dont la validation de processus est calculée pendant la duplication de processus.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-999">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="cbc9f-1000">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1000">(GH #1286)</span></span>
- <span data-ttu-id="cbc9f-1001">/Proc/sys/VM/overcommit_memory. implémentée</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1001">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="cbc9f-1002">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1002">(GH #1286)</span></span>
- <span data-ttu-id="cbc9f-1003">Fichier/proc/net/route implémenté (GH #69)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1003">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="cbc9f-1004">Correction de l’erreur où le nom du raccourci n’a pas été localisé correctement (GH #696)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1004">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="cbc9f-1005">Correction de la logique d’analyse de Elf qui valide incorrectement les en-têtes de programme doit être inférieure ou égale à PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1005">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="cbc9f-1006">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1006">(GH #1048)</span></span>
- <span data-ttu-id="cbc9f-1007">Implémentation du rappel statfs pour procfs, sysfs, cgroupfs et binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1007">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="cbc9f-1008">Correction des fenêtres AptPackageIndexUpdate qui ne sont pas fermées (GH #1184, également abordées dans GH #1193)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1008">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="cbc9f-1009">Ajout de la prise en charge de la personnalité ASLR ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1009">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="cbc9f-1010">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1010">(GH #1148, 1128)</span></span>
- <span data-ttu-id="cbc9f-1011">PTRACE_GETSIGINFO amélioré, SIGSEGV, pour les traces de pile gdb appropriées pendant l’AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1011">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="cbc9f-1012">L’analyse ELF n’échoue plus pour les fichiers binaires patchelf.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1012">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="cbc9f-1013">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1013">(GH #471)</span></span>
- <span data-ttu-id="cbc9f-1014">DNS VPN propagé à/etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1014">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="cbc9f-1015">Améliorations apportées à TCP Close pour un transfert de données plus fiable.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1015">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="cbc9f-1016">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1016">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="cbc9f-1017">Retourne à présent un code d’erreur correct lorsque trop de fichiers sont ouverts (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1017">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="cbc9f-1018">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1018">(GH #1126, 2090)</span></span>
- <span data-ttu-id="cbc9f-1019">Le journal d’audit Windows signale désormais le nom de l’image dans traiter créer un audit.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1019">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="cbc9f-1020">Échouent à présent correctement lors du lancement de bash. exe à partir d’une fenêtre bash</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1020">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="cbc9f-1021">Ajout d’un message d’erreur lorsque l’interopérabilité n’est pas en mesure d’accéder à un répertoire de travail sous LxFs (c.-à-d. Notepad. exe. bashrc)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1021">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="cbc9f-1022">Correction du problème où le chemin d’accès Windows était tronqué dans WSL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1022">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="cbc9f-1023">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1024">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1024">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1025">Nombre de tests réussis: 690</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1025">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="cbc9f-1026">Nombre de non-passage (échec, ignoré, etc.): 274</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1026">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="cbc9f-1027">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1028">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1028">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1029">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1029">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1030">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1030">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="cbc9f-1031">Build 14986</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1031">Build 14986</span></span>

<span data-ttu-id="cbc9f-1032">Pour obtenir des informations générales sur Windows sur la build 14986, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1032">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1033">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1033">Fixed</span></span>

- <span data-ttu-id="cbc9f-1034">Correction de bugchecks avec des IOCTL NetLink et Pty</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1034">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="cbc9f-1035">La version du noyau signale 4.4.0-43 pour assurer la cohérence avec Xenial</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1035">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="cbc9f-1036">Bash. exe se lance maintenant quand l’entrée est dirigée vers «nul:» (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1036">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="cbc9f-1037">Les ID de thread sont désormais signalés correctement dans procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1037">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="cbc9f-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | Indicateurs IN_ISDIR désormais pris en charge dans inotify_add_watch () (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="cbc9f-1039">Implémentez timer_create et les appels système associés.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1039">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="cbc9f-1040">Cela permet la prise en charge de GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1040">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="cbc9f-1041">Correction du problème où ping a retourné une heure de 0.000 MS (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1041">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="cbc9f-1042">Retourne un code d’erreur correct lorsque trop de fichiers sont ouverts.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1042">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="cbc9f-1043">Résolution d’un problème dans WSL où les données de l’interface réseau de l’interface réseau échouent avec EINVAL si l’adresse matérielle de l’interface est de 32 octets (par exemple, l’interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1043">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="cbc9f-1044">Notez que l’utilitaire «IP» Linux contient un bogue qui se bloque si WSL signale une adresse matérielle de 32 octets.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1044">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="cbc9f-1045">Il s’agit d’un bogue dans «IP», et non WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1045">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="cbc9f-1046">L’utilitaire «IP» code en dur la longueur de la mémoire tampon de chaîne utilisée pour imprimer l’adresse matérielle, et cette mémoire tampon est trop petite pour imprimer une adresse matérielle de 32 octets.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1046">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="cbc9f-1047">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1047">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1048">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1048">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1049">Nombre de tests réussis: 669</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1049">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="cbc9f-1050">Nombre de non-passage (échec, ignoré, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1050">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="cbc9f-1051">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1051">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1052">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1052">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1053">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1053">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1054">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1054">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="cbc9f-1055">Build 14971</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1055">Build 14971</span></span>

<span data-ttu-id="cbc9f-1056">Pour obtenir des informations générales sur Windows sur la build 14971, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1056">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1057">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1057">Fixed</span></span>

 - <span data-ttu-id="cbc9f-1058">En dehors de notre contrôle, aucune mise à jour n’est apportée à cette version pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1058">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="cbc9f-1059">Les mises à jour planifiées périodiquement reprendront à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1059">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1060">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1060">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1061">Non modifié à partir de 14965</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1061">Unchanged from 14965</span></span> </br>
<span data-ttu-id="cbc9f-1062">Nombre de tests réussis: 664</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1062">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="cbc9f-1063">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1063">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1064">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1064">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="cbc9f-1065">Build 14965</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1065">Build 14965</span></span>

<span data-ttu-id="cbc9f-1066">Pour obtenir des informations générales sur Windows sur la build 14965, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1066">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1067">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1067">Fixed</span></span>

- <span data-ttu-id="cbc9f-1068">Prise en charge des RTM_GETLINK et RTM_GETADDR du protocole NETLINK_ROUTE (GH #468)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1068">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="cbc9f-1069">Active les commandes ifconfig et IP pour l’énumération de réseau</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1069">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="cbc9f-1070">Pour plus d’informations, consultez notre billet de blog sur la [mise en réseau WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1070">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="cbc9f-1071">/sbin est désormais dans le chemin d’accès de l’utilisateur par défaut</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1071">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="cbc9f-1072">Le chemin d’accès de l’utilisateur NT est maintenant ajouté au chemin d’accès WSL par défaut (par exemple, vous pouvez maintenant taper Notepad. exe sans ajouter system32 au chemin Linux)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1072">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="cbc9f-1073">Ajout de la prise en charge de/proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1073">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="cbc9f-1074">Les fichiers binaires NT peuvent maintenant être lancés à partir de WSL lorsque le répertoire de travail actuel contient des caractères non ANSI (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1074">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="cbc9f-1075">Autoriser l’arrêt sur le socket de flux UNIX déconnecté.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1075">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="cbc9f-1076">Ajout de la prise en charge de PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1076">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="cbc9f-1077">Ajout de la prise en charge de CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1077">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="cbc9f-1078">Correction de l’erreur où le canaling est coincé, c.-à-d. bash-r «LS-alR/» | bash-c «Cat» (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1078">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="cbc9f-1079">Gérer les demandes de connexion au terminal actuel.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1079">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="cbc9f-1080">Marquez<pid>/proc//oom_score_adj comme accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1080">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="cbc9f-1081">Ajoutez le dossier/sys/FS/cgroup.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1081">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="cbc9f-1082">sched_setaffinity doit retourner le nombre de bits d’affinité Mask</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1082">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="cbc9f-1083">Corrigez la logique de validation ELF qui suppose que les chemins de l’interpréteur ne doivent pas dépasser 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1083">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="cbc9f-1084">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1084">(GH #743)</span></span>
- <span data-ttu-id="cbc9f-1085">Les descripteurs de fichiers ouverts peuvent maintenir la fenêtre de console ouverte (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1085">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="cbc9f-1086">Erreur fixe où Rename () a échoué avec la barre oblique de fin sur le nom de la cible (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1086">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="cbc9f-1087">Implémenter le fichier/proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1087">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="cbc9f-1088">Correction des 0.000 ms pings en raison de la résolution du minuteur.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1088">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="cbc9f-1089">Implemented/proc/Self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1089">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="cbc9f-1090">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1090">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1091">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1091">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1092">Nombre de tests réussis: 664</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1092">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="cbc9f-1093">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1093">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1094">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1094">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="cbc9f-1095">Build 14959</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1095">Build 14959</span></span>

<span data-ttu-id="cbc9f-1096">Pour obtenir des informations générales sur Windows sur la build 14959, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1096">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1097">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1097">Fixed</span></span>

- <span data-ttu-id="cbc9f-1098">Notification de processus de Pico améliorée pour Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1098">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="cbc9f-1099">Informations supplémentaires disponibles sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1099">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="cbc9f-1100">Stabilité améliorée avec l’interopérabilité Windows</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1100">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="cbc9f-1101">Correction de l’erreur 0x80070057 lors du lancement de bash. exe lorsque la protection des données d’entreprise (EDP) est activée</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1101">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="cbc9f-1102">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1102">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1103">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1103">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1104">Nombre de tests réussis: 665</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cbc9f-1105">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1106">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="cbc9f-1107">Build 14955</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1107">Build 14955</span></span>

<span data-ttu-id="cbc9f-1108">Pour obtenir des informations générales sur Windows sur la build 14955, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1108">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1109">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1109">Fixed</span></span>

 - <span data-ttu-id="cbc9f-1110">En dehors de notre contrôle, aucune mise à jour n’est apportée à cette version pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1110">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="cbc9f-1111">Les mises à jour planifiées périodiquement reprendront à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1111">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1112">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1112">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1113">Nombre de tests réussis: 665</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1113">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cbc9f-1114">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1114">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1115">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="cbc9f-1116">Build 14951</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1116">Build 14951</span></span>

<span data-ttu-id="cbc9f-1117">Pour obtenir des informations générales sur Windows sur la build 14951, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1117">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="cbc9f-1118">Nouvelle fonctionnalité: Interopérabilité Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1118">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="cbc9f-1119">Les binaires Windows peuvent désormais être appelés directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1119">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="cbc9f-1120">Cela permet aux utilisateurs d’interagir avec leurs environnements et systèmes Windows d’une manière qui n’a pas été possible.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1120">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="cbc9f-1121">En guise d’exemple rapide, les utilisateurs peuvent désormais exécuter les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1121">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="cbc9f-1122">Pour plus d’informations, consultez:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1122">More information can be found at:</span></span>

- [<span data-ttu-id="cbc9f-1123">Blog de l’équipe WSL pour l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1123">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="cbc9f-1124">Documentation MSDN Interop</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1124">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1125">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1125">Fixed</span></span>

- <span data-ttu-id="cbc9f-1126">Ubuntu 16,04 (Xenial) est maintenant installé pour toutes les nouvelles instances de WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1126">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="cbc9f-1127">Les utilisateurs avec des instances 14,04 (Trusty) existantes ne seront pas automatiquement mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1127">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="cbc9f-1128">Les paramètres régionaux définis lors de l’installation s’affichent maintenant</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1128">Locale set during install is now displayed</span></span>
- <span data-ttu-id="cbc9f-1129">Les améliorations des terminaux, y compris les bogues qui redirigent un processus WSL vers un fichier, ne fonctionnent pas toujours</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1129">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="cbc9f-1130">La durée de vie de la console doit être liée à bash. exe durée de vie</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1130">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="cbc9f-1131">La taille de la fenêtre de console doit utiliser la taille visible, pas la taille de la mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1131">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="cbc9f-1132">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1132">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1133">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1133">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1134">Nombre de tests réussis: 665</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1134">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cbc9f-1135">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1135">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1136">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1136">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="cbc9f-1137">Build 14946</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1137">Build 14946</span></span>

<span data-ttu-id="cbc9f-1138">Pour obtenir des informations générales sur Windows sur la build 14946, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1138">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1139">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1139">Fixed</span></span>

- <span data-ttu-id="cbc9f-1140">Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT qui contiennent des espaces ou des guillemets.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1140">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="cbc9f-1141">Modifiez VolFs et DrvFs pour retourner 0 pour le nombre de liens du répertoire dans stat</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1141">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="cbc9f-1142">Prise en charge de l’option de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1142">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="cbc9f-1143">Limiter à une seule boucle d’e/s de console par TTY.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1143">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="cbc9f-1144">Exemple: la commande suivante est possible:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1144">Example: the following command is possible:</span></span>
  - <span data-ttu-id="cbc9f-1145">bash-c "echo Data" | Chat-c «SSH user@example.com » > foo. txt»</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1145">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="cbc9f-1146">remplacer les espaces par des tabulations dans/proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1146">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="cbc9f-1147">DrvFs apparaît maintenant dans mountinfo avec un nom qui correspond au volume Windows monté</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1147">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="cbc9f-1148">/Home et/root s’affichent désormais dans mountinfo avec des noms corrects</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1148">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="cbc9f-1149">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1149">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1150">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1150">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1151">Nombre de tests réussis: 665</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1151">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cbc9f-1152">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1152">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1153">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1153">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="cbc9f-1154">Build 14942</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1154">Build 14942</span></span>

<span data-ttu-id="cbc9f-1155">Pour obtenir des informations générales sur Windows sur la build 14942, visitez le [blog Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1155">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1156">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1156">Fixed</span></span>

- <span data-ttu-id="cbc9f-1157">Un certain nombre de bugchecks adressés, y compris le blocage du réseau «tentative d’exécution de la mémoire noexecute», qui bloque SSH</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1157">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="cbc9f-1158">la prise en charge de inotifiy pour les notifications générées à partir d’applications Windows sur DrvFs est désormais</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1158">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="cbc9f-1159">Implémentez TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1159">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="cbc9f-1160">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1160">(GH #695)</span></span>
- <span data-ttu-id="cbc9f-1161">Implémenter l’appel système pivot_root</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1161">Implement the pivot_root system call</span></span>
- <span data-ttu-id="cbc9f-1162">Implémenter l’option de socket pour SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1162">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="cbc9f-1163">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1163">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1164">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1164">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1165">Nombre de tests réussis: 665</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1165">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cbc9f-1166">Nombre de non-passage (échec, ignoré, etc.): 263</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cbc9f-1167">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1168">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1168">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1169">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1169">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1170">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1170">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="cbc9f-1171">Build 14936</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1171">Build 14936</span></span>

<span data-ttu-id="cbc9f-1172">Pour obtenir des informations générales sur Windows sur la build 14936, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1172">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="cbc9f-1173">Remarque : WSL installe Ubuntu version 16,04 (Xenial) au lieu d’Ubuntu 14,04 (Trusty) dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1173">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="cbc9f-1174">Cette modification s’appliquera aux Insiders qui installent de nouvelles instances (lxrun. exe/install ou First Run. exe).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1174">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="cbc9f-1175">Les instances existantes avec l’approbation ne sont pas mises à niveau automatiquement.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1175">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="cbc9f-1176">Les utilisateurs peuvent mettre à niveau leur image de confiance vers Xenial à l’aide de la commande do-Release-Upgrade.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1176">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="cbc9f-1177">Problème connu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1177">Known Issue</span></span>
<span data-ttu-id="cbc9f-1178">WSL rencontre un problème avec certaines implémentations de Socket.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1178">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="cbc9f-1179">La vérification de bogue se manifeste comme un blocage avec l’erreur «tentative d’exécution de la mémoire noexecute».</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1179">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="cbc9f-1180">La manifestation la plus courante de ce problème est un blocage lors de l’utilisation de SSH.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1180">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="cbc9f-1181">L’origine du problème est résolue sur les builds internes et sera envoyée aux Insiders au plus tôt.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1181">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1182">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1182">Fixed</span></span>

- <span data-ttu-id="cbc9f-1183">Implémentation de l’appel système mécanisme chroot</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1183">Implemented the chroot system call</span></span>
- <span data-ttu-id="cbc9f-1184">Améliorations apportées à inotify ~~, notamment la prise en charge des notifications générées à partir d’applications Windows sur DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1184">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="cbc9f-1185">Correction La prise en charge de inotify pour les modifications provenant d’applications Windows non disponibles pour le moment.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1185">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="cbc9f-1186">Liaison de socket à IPv6:<port n> : prend désormais en charge IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1186">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="cbc9f-1187">Comportement WNOWAIT pour waitid systemcall implémenté (GH #638)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1187">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="cbc9f-1188">Prise en charge des options de socket IP IP_HDRINCL et IP_TTL</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1188">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="cbc9f-1189">La lecture de longueur nulle () doit être renvoyée immédiatement (GH #975)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1189">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="cbc9f-1190">Gérez correctement les noms de fichiers et les préfixes de noms de fichiers qui n’incluent pas de marque de fin NULL dans un fichier. tar.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1190">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="cbc9f-1191">prise en charge de epoll pour/dev/null</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1191">epoll support for /dev/null</span></span>
- <span data-ttu-id="cbc9f-1192">Corriger la source de temps/dev/Alarm</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1192">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="cbc9f-1193">Bash-c maintenant capable de rediriger vers un fichier</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1193">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="cbc9f-1194">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1194">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1195">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1195">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1196">Nombre de tests réussis: 664</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1196">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="cbc9f-1197">Nombre de non-passage (échec, ignoré, etc.): 264</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1197">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="cbc9f-1198">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1198">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1199">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1199">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1200">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1200">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1201">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1201">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="cbc9f-1202">Build 14931</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1202">Build 14931</span></span>

<span data-ttu-id="cbc9f-1203">Pour obtenir des informations générales sur Windows sur la build 14931, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1203">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1204">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1204">Fixed</span></span>

 - <span data-ttu-id="cbc9f-1205">En dehors de notre contrôle, aucune mise à jour n’est apportée à cette version pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1205">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="cbc9f-1206">Les mises à jour planifiées périodiquement reprendront dans la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1206">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="cbc9f-1207">Build 14926</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1207">Build 14926</span></span>

<span data-ttu-id="cbc9f-1208">Pour obtenir des informations générales sur Windows sur la build 14926, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1208">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1209">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1209">Fixed</span></span>

- <span data-ttu-id="cbc9f-1210">Ping fonctionne désormais dans les consoles qui ne disposent pas de privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1210">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="cbc9f-1211">Ping6 désormais pris en charge, sans privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1211">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="cbc9f-1212">Inotify la prise en charge des fichiers modifiés via WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1212">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="cbc9f-1213">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1213">(GH #216)</span></span>
  - <span data-ttu-id="cbc9f-1214">Indicateurs pris en charge:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1214">Flags supported:</span></span>
    - <span data-ttu-id="cbc9f-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="cbc9f-1216">événements inotify_add_watch: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1216">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="cbc9f-1217">attributs inotify_add_watch: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1217">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="cbc9f-1218">lire la sortie: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1218">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="cbc9f-1219">Problème connu: La modification de fichiers à partir d’applications Windows ne génère pas d’événements</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1219">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="cbc9f-1220">Le socket Unix prend désormais en charge SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1220">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cbc9f-1221">Résultats de LTP:</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1221">LTP Results:</span></span>
<span data-ttu-id="cbc9f-1222">Nombre de tests réussis: 651</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1222">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="cbc9f-1223">Nombre de non-passage (échec, ignoré, etc.): 258</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1223">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="cbc9f-1224">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1224">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="cbc9f-1225">Build 14915</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1225">Build 14915</span></span>

<span data-ttu-id="cbc9f-1226">Pour obtenir des informations générales sur Windows sur la build 14915, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1226">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1227">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1227">Fixed</span></span>
-  <span data-ttu-id="cbc9f-1228">Sockets de datagramme socketpair pour UNIX (GH #262)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1228">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="cbc9f-1229">Prise en charge des sockets Unix pour SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1229">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="cbc9f-1230">Prise en charge des sockets UNIX pour SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1230">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="cbc9f-1231">Prise en charge des sockets Unix pour SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1231">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="cbc9f-1232">Ajout de la prise en charge de l’envoi, du recv et de l’arrêt du socket de datagramme UNIX</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1232">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="cbc9f-1233">Corrigez les Bugcheck en raison d’une validation de paramètre mmap non valide pour les adresses non fixes.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1233">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="cbc9f-1234">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1234">(GH #847)</span></span>
- <span data-ttu-id="cbc9f-1235">Prise en charge de l’interruption/reprise des États des terminaux</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1235">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="cbc9f-1236">Prise en charge de TIOCPKT ioctl pour débloquer l’utilitaire Screen (GH #774)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1236">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="cbc9f-1237">Problème connu: Clés de fonction non opérationnelles</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1237">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="cbc9f-1238">Correction d’une course dans TimerFd qui pourrait provoquer l’accès d’un membre libéré’ReaderReady’par LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1238">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="cbc9f-1239">Activer la prise en charge des appels système pouvant être redémarrés pour Futex, Poll et clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1239">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="cbc9f-1240">Ajout de la prise en charge du montage bind</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1240">Added bind mount support</span></span>
- <span data-ttu-id="cbc9f-1241">annuler le partage pour la prise en charge des espaces de noms de montage</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1241">unshare for mount namespace support</span></span>
    - <span data-ttu-id="cbc9f-1242">Problème connu: Lorsque vous créez un espace de noms `unshare(CLONE_NEWNS)` de montage avec le répertoire de travail actuel, vous pointez sur l’ancien espace de noms</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1242">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="cbc9f-1243">Améliorations supplémentaires et correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1243">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="cbc9f-1244">Build 14905</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1244">Build 14905</span></span>

<span data-ttu-id="cbc9f-1245">Pour obtenir des informations générales sur Windows sur la build 14905, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1245">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1246">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1246">Fixed</span></span>
- <span data-ttu-id="cbc9f-1247">Les appels système redémarrables sont désormais pris en charge (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1247">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="cbc9f-1248">Liens symboliques vers les répertoires se terminant par/maintenant opérationnel (GH #650)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1248">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="cbc9f-1249">RNDGETENTCNT IOCTL implémenté pour/dev/random</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1249">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="cbc9f-1250">Mise en œuvre des fichiers/proc/[PID]/Mounts,/proc/[PID]/mountinfo et/proc/[PID]/mountstats</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1250">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="cbc9f-1251">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1251">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="cbc9f-1252">Build 14901</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1252">Build 14901</span></span>
<span data-ttu-id="cbc9f-1253">Première version d’Insider pour la publication de la mise à jour anniversaire Windows 10.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1253">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="cbc9f-1254">Pour obtenir des informations générales sur Windows sur la build 14901, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1254">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1255">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1255">Fixed</span></span>
- <span data-ttu-id="cbc9f-1256">Correction de la barre oblique de fin</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1256">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="cbc9f-1257">Les commandes telles `$ mv a/c/ a/b/` que fonctionnent maintenant</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1257">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="cbc9f-1258">Installation des invites maintenant si les paramètres régionaux Ubuntu doivent être définis sur les paramètres régionaux Windows</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1258">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="cbc9f-1259">Prise en charge procfs pour le dossier NS</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1259">Procfs support for ns folder</span></span>
- <span data-ttu-id="cbc9f-1260">Ajout de montage et démontage pour les systèmes de fichiers tmpfs, procfs et sysfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1260">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="cbc9f-1261">Correction de la signature ABI 32 bits de la solution mknod [at]</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1261">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="cbc9f-1262">Sockets Unix déplacés vers le modèle de distribution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1262">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="cbc9f-1263">La taille de la mémoire tampon de réception du socket INET à l’aide de setsockopt doit être respectée</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1263">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="cbc9f-1264">Implémenter l’indicateur de message de réception du socket Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1264">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="cbc9f-1265">Redirection de canaux Linux process stdin/stdout (GH #2)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1265">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="cbc9f-1266">Permet le canalisation des commandes bash-c dans CMD.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1266">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="cbc9f-1267">Exemple: > dir | bash-c «grep foo»</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1267">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="cbc9f-1268">Bash peut désormais être installé sur des systèmes avec plusieurs infromages (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1268">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="cbc9f-1269">La taille de la mémoire tampon du socket INET par défaut doit correspondre à celle du programme d’installation Ubuntu par défaut</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1269">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="cbc9f-1270">Aligner xattr syscalls sur listxattr</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1270">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="cbc9f-1271">Retourne uniquement les interfaces avec une adresse IPv4 valide à partir de SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1271">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="cbc9f-1272">Corriger l’action par défaut de signal quand elle est injectée par ptrace</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1272">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="cbc9f-1273">implémenter/proc/sys/VM/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1273">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="cbc9f-1274">Utiliser des valeurs de registre de contexte d’ordinateur lors de la restauration du contexte dans sigreturn</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1274">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="cbc9f-1275">Cela résout le problème où Java et javac étaient bloqués pour certains utilisateurs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1275">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="cbc9f-1276">Implémenter/proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1276">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1277">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1277">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1278">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1278">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1279">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1279">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="cbc9f-1280">Version 14388 de la mise à jour anniversaire de Windows 10</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1280">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="cbc9f-1281">Pour obtenir des informations générales sur Windows sur la build 14388, visitez le [blog Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1281">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1282">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1282">Fixed</span></span>
- <span data-ttu-id="cbc9f-1283">Correctifs pour préparer la mise à jour anniversaire Windows 10 sur 8/2</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1283">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="cbc9f-1284">Vous trouverez plus d’informations sur WSL dans la mise à jour anniversaire sur notre [blog](https://blogs.msdn.microsoft.com/wsl/) .</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1284">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="cbc9f-1285">Build 14376</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1285">Build 14376</span></span>
<span data-ttu-id="cbc9f-1286">Pour obtenir des informations générales sur Windows sur la build 14376, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1286">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1287">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1287">Fixed</span></span>
- <span data-ttu-id="cbc9f-1288">Suppression de certaines instances où apt-obtien se bloque (GH #493)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1288">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="cbc9f-1289">Résolution d’un problème où les montages vides n’étaient pas gérés correctement</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1289">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="cbc9f-1290">Correction d’un problème où les ramdisks n’étaient pas correctement montés</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1290">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="cbc9f-1291">Remplacer l’acceptation du socket UNIX par les indicateurs de prise en charge (GH #451 partiel)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1291">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="cbc9f-1292">Résolution de l’écran bleu commun lié au réseau</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1292">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="cbc9f-1293">Correction de l’écran bleu lors de l’accès à/proc/[PID]/Task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1293">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="cbc9f-1294">Correction de l’utilisation élevée du processeur pour certains cas de PTY (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1294">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="cbc9f-1295">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1295">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="cbc9f-1296">Build 14371</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1296">Build 14371</span></span>
<span data-ttu-id="cbc9f-1297">Pour obtenir des informations générales sur Windows sur la build 14371, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1297">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1298">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1298">Fixed</span></span>
- <span data-ttu-id="cbc9f-1299">Correction de la course temporelle avec SIGCHLD et attente () lors de l’utilisation de ptrace</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1299">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="cbc9f-1300">Correction de certains comportements lorsque les chemins d’accès ont une fin/(GH #432)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1300">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="cbc9f-1301">Résolution du problème lié à l’échec de renommage/dissociation en raison de handles ouverts vers des enfants</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1301">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="cbc9f-1302">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1302">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="cbc9f-1303">Build 14366</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1303">Build 14366</span></span>
<span data-ttu-id="cbc9f-1304">Pour obtenir des informations générales sur Windows sur la build 14366, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1304">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1305">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1305">Fixed</span></span>
- <span data-ttu-id="cbc9f-1306">Correction de la création de fichiers via liens symboliques</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1306">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="cbc9f-1307">Ajout de listxattr pour Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1307">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="cbc9f-1308">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1308">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1309">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1309">Syscall Support</span></span>
-   <span data-ttu-id="cbc9f-1310">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1310">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1311">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1311">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="cbc9f-1312">Build 14361</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1312">Build 14361</span></span>
<span data-ttu-id="cbc9f-1313">Pour obtenir des informations générales sur Windows sur la build 14361, visitez le [blog Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1313">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1314">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1314">Fixed</span></span>
- <span data-ttu-id="cbc9f-1315">DrvFs respecte désormais la casse lors de l’exécution dans bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1315">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="cbc9f-1316">Les utilisateurs peuvent les cas. txt et CASE. TXT sur leurs lecteurs/mnt/c</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1316">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="cbc9f-1317">Le respect de la casse est pris en charge uniquement dans bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1317">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="cbc9f-1318">En dehors du système NTFS bash signale les fichiers correctement, mais un comportement inattendu peut se produire lors de l’interaction avec les fichiers de Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1318">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="cbc9f-1319">La racine de chaque volume (c.-à-d./mnt/c) n’est pas sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1319">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="cbc9f-1320">Vous trouverez plus d’informations sur la gestion de ces fichiers dans Windows [ici](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1320">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="cbc9f-1321">Prise en charge de PTY/TTY beaucoup améliorée.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1321">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="cbc9f-1322">Applications telles que TMUX désormais prises en charge (GH #40)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1322">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="cbc9f-1323">Résolution d’un problème d’installation où les comptes d’utilisateurs n’ont pas toujours été créés</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1323">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="cbc9f-1324">Structure d’arguments de ligne de commande optimisée autorisant une liste d’arguments extrêmement longue.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1324">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="cbc9f-1325">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1325">(GH #153)</span></span>
- <span data-ttu-id="cbc9f-1326">Possibilité de supprimer et chmod des fichiers READ_ONLY de DrvFs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1326">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="cbc9f-1327">Correction de certaines instances où le terminal se bloque lors de la déconnexion (GH #43)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1327">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="cbc9f-1328">chmod et chown fonctionnent désormais sur les appareils TTY</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1328">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="cbc9f-1329">Autoriser la connexion à 0.0.0.0 et:: en tant que localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1329">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="cbc9f-1330">Sendmsg/recvmsg gère désormais une longueur de vecteur d’e/s de > 1 (à GH partiel #376)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1330">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="cbc9f-1331">Les utilisateurs peuvent désormais désactiver le fichier des hôtes générés automatiquement (GH #398)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1331">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="cbc9f-1332">Faire correspondre automatiquement les paramètres régionaux Linux aux paramètres régionaux NT lors de l’installation (GH #11)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1332">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="cbc9f-1333">Ajout du fichier/proc/sys/VM/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1333">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="cbc9f-1334">strace se ferme maintenant correctement</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1334">strace now exits correctly</span></span>
- <span data-ttu-id="cbc9f-1335">Autoriser la réouverture des canaux via/proc/Self/FD (GH #222)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1335">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="cbc9f-1336">Masquer les répertoires sous%LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1336">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="cbc9f-1337">Meilleure gestion de bash. exe ~.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1337">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="cbc9f-1338">Les commandes telles que «bash ~-c ls» sont maintenant prises en charge (GH #467)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1338">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="cbc9f-1339">Les sockets notifient désormais la lecture des epoll disponibles pendant l’arrêt (GH #271)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1339">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="cbc9f-1340">lxrun/Uninstall est un meilleur travail de suppression des fichiers et des dossiers</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1340">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="cbc9f-1341">Correction de PS-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1341">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="cbc9f-1342">Prise en charge améliorée des applications X11 comme xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1342">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="cbc9f-1343">Mise à jour de la taille de la pile des threads initiale pour qu’elle corresponde au paramètre Ubuntu par défaut et signale la taille correctement au get_rlimit syscall (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1343">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="cbc9f-1344">Amélioration de la création de rapports sur les noms d’image de processus de Pico (par exemple, pour l’audit)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1344">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="cbc9f-1345">Implémentation de/proc/mountinfo pour DF, commande</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1345">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="cbc9f-1346">Correction du code d’erreur symlink pour le nom de l’enfant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1346">Fixed symlink error code for child name .</span></span> <span data-ttu-id="cbc9f-1347">et.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1347">and ..</span></span>
- <span data-ttu-id="cbc9f-1348">Améliorations supplémentaires correctifs et améliorations</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1348">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1349">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1349">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1350">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1351">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="cbc9f-1352">Build 14352</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1352">Build 14352</span></span>
<span data-ttu-id="cbc9f-1353">Pour obtenir des informations générales sur Windows sur la build 14352, visitez le [blog Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1353">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1354">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1354">Fixed</span></span>
- <span data-ttu-id="cbc9f-1355">Résolution d’un problème où des fichiers volumineux n’ont pas été téléchargés/créés correctement.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1355">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="cbc9f-1356">Cela doit débloquer NPM et d’autres scénarios (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1356">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="cbc9f-1357">Suppression de certaines instances où les sockets se bloquent</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1357">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="cbc9f-1358">Correction de certaines erreurs de ptrace</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1358">Corrected some ptrace errors</span></span>
- <span data-ttu-id="cbc9f-1359">Résolution d’un problème avec WSL autorisant les noms de fichiers de plus de 255 caractères</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1359">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="cbc9f-1360">Amélioration de la prise en charge des caractères non anglais</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1360">Improved support for non-English characters</span></span>
- <span data-ttu-id="cbc9f-1361">Ajouter les données de fuseau horaire Windows actuelles et les définir par défaut</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1361">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="cbc9f-1362">ID d’appareil unique pour chaque point de montage (correctif JRE – GH #49)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1362">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="cbc9f-1363">Corriger le problème avec les chemins d’accès contenant «.»</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1363">Correct issue with paths containing “.”</span></span> <span data-ttu-id="cbc9f-1364">et ".."</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1364">and “..”</span></span>
- <span data-ttu-id="cbc9f-1365">Ajout de la prise en charge FIFO (GH #71)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1365">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="cbc9f-1366">Format de resolv. conf mis à jour pour correspondre au format Ubuntu natif</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1366">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="cbc9f-1367">Certains nettoyages de procfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1367">Some procfs cleanup</span></span>
- <span data-ttu-id="cbc9f-1368">Activation du test ping pour les consoles Administrateur (GH #18)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1368">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1369">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1369">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1370">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1371">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="cbc9f-1372">Build 14342</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1372">Build 14342</span></span>
<span data-ttu-id="cbc9f-1373">Pour obtenir des informations générales sur Windows sur la build 14342, le [blog Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1373">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="cbc9f-1374">Vous trouverez des informations sur VolFs et DriveFs sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1374">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1375">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1375">Fixed</span></span>
- <span data-ttu-id="cbc9f-1376">Résolution du problème d’installation lorsque l’utilisateur Windows contenait des caractères Unicode dans le nom d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1376">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="cbc9f-1377">La solution de contournement udev de mise à jour «apt-obtien» dans le Forum aux questions est désormais fournie par défaut lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1377">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="cbc9f-1378">Activation de liens symboliques dans les répertoires DriveFs (/MNT/<drive>)</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1378">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="cbc9f-1379">Liens symboliques fonctionne désormais entre DriveFs et VolFs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1379">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="cbc9f-1380">Adressée supérieur au niveau chemin d’accès de l’analyse du problème : %.ls. / / fonctionne désormais comme prévu</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1380">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="cbc9f-1381">NPM install sur DriveFs et les options-g fonctionnent désormais</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1381">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="cbc9f-1382">Résolution du problème empêchant le lancement du serveur PHP</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1382">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="cbc9f-1383">Mise à jour des valeurs d’environnement par défaut, par exemple $PATH pour une correspondance plus proche d’Ubuntu natif</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1383">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="cbc9f-1384">Ajout d’une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache de packages APT</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1384">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="cbc9f-1385">Résolution du problème avec la validation d’en-tête ELF, WSL prend désormais en charge toutes les options Melkor</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1385">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="cbc9f-1386">L’interpréteur de commandes zsh est fonctionnel</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1386">Zsh shell is functional</span></span>
- <span data-ttu-id="cbc9f-1387">Les fichiers binaires Go précompilés sont désormais pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1387">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="cbc9f-1388">L’invite de la première exécution de bash. exe est désormais localisée correctement</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1388">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="cbc9f-1389">/proc/meminfo retourne désormais des informations correctes</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1389">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="cbc9f-1390">Sockets pris en charge dans VFS</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1390">Sockets now supported in VFS</span></span>
- <span data-ttu-id="cbc9f-1391">/dev maintenant monté en tant que tempfs</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1391">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="cbc9f-1392">FIFO actuellement pris en charge</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1392">Fifo now supported</span></span>
- <span data-ttu-id="cbc9f-1393">Les systèmes multicœurs s’affichaient désormais correctement dans/proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1393">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="cbc9f-1394">Améliorations supplémentaires et messages d’erreur téléchargés lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1394">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="cbc9f-1395">Améliorations de syscall et correctifs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1395">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="cbc9f-1396">Liste syscall prise en charge ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1396">Supported syscall list below.</span></span>
- <span data-ttu-id="cbc9f-1397">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1397">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="cbc9f-1398">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1398">Known Issues</span></span>
- <span data-ttu-id="cbc9f-1399">Impossible de résoudre'.. '</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1399">Not resolving ‘..’</span></span> <span data-ttu-id="cbc9f-1400">correctement sur DriveFs dans certains cas</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1400">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1401">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1401">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1402">Vous trouverez ci-dessous une liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1402">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1403">Le syscalls de cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1403">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="cbc9f-1404">Build 14332</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1404">Build 14332</span></span>

<span data-ttu-id="cbc9f-1405">Pour obtenir des informations générales sur Windows sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1405">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="cbc9f-1406">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1406">Fixed</span></span>
- <span data-ttu-id="cbc9f-1407">Meilleure génération de resolv. conf, y compris la hiérarchisation des entrées DNS</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1407">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="cbc9f-1408">Problème lié au déplacement de fichiers et de répertoires entre les lecteurs/mnt et non-/MNT</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1408">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="cbc9f-1409">Les fichiers tar peuvent maintenant être créés avec liens symboliques</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1409">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="cbc9f-1410">Ajout du répertoire/Run/Lock par défaut lors de la création de l’instance</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1410">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="cbc9f-1411">Mettre à jour/dev/null pour retourner les informations statistiques appropriées</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1411">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="cbc9f-1412">Erreurs supplémentaires lors du téléchargement lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1412">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="cbc9f-1413">Améliorations de syscall et correctifs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1413">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="cbc9f-1414">Liste syscall prise en charge ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1414">Supported syscall list below.</span></span>
- <span data-ttu-id="cbc9f-1415">Améliorations supplémentaires correctifs et améliorations</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1415">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1416">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1416">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1417">Voici le nouveau syscall qui a une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1417">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="cbc9f-1418">Le syscall sur cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1418">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="cbc9f-1419">Build 14328</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1419">Build 14328</span></span>

<span data-ttu-id="cbc9f-1420">Pour obtenir des informations générales sur Windows sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1420">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="cbc9f-1421">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1421">New Features</span></span>
* <span data-ttu-id="cbc9f-1422">Prend désormais en charge les utilisateurs Linux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1422">Now support Linux users.</span></span>  <span data-ttu-id="cbc9f-1423">L’installation de bash sur Ubuntu sur Windows vous invite à créer un utilisateur Linux.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1423">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="cbc9f-1424">Pour plus d’informations, visitez le site https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1424">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="cbc9f-1425">Hostname est maintenant défini sur le nom de l’ordinateur Windows, pas plus@localhost</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1425">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="cbc9f-1426">Pour plus d’informations sur la build 14328, visitez le site: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1426">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="cbc9f-1427">Résolution</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1427">Fixed</span></span>
* <span data-ttu-id="cbc9f-1428">Améliorations des liens symboliques<drive> pour les fichiers non/MNT/</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1428">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="cbc9f-1429">l’installation de NPM fonctionne maintenant</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1429">npm install now works</span></span>
    * <span data-ttu-id="cbc9f-1430">JDK/JRE s’installe maintenant à l’aide des instructions fournies [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1430">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="cbc9f-1431">problème connu: liens symboliques ne fonctionne pas pour les montages Windows.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1431">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="cbc9f-1432">Les fonctionnalités seront disponibles dans une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1432">Functionality will be available in a later build</span></span>
* <span data-ttu-id="cbc9f-1433">affichages haut et htop maintenant</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1433">top and htop now display</span></span>
* <span data-ttu-id="cbc9f-1434">Messages d’erreur supplémentaires pour certains échecs d’installation</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1434">Additional error messages for some install failures</span></span>
* <span data-ttu-id="cbc9f-1435">Améliorations de syscall et correctifs.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1435">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="cbc9f-1436">Liste syscall prise en charge ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1436">Supported syscall list below.</span></span>
* <span data-ttu-id="cbc9f-1437">Améliorations supplémentaires correctifs et améliorations</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1437">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cbc9f-1438">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1438">Syscall Support</span></span>
<span data-ttu-id="cbc9f-1439">Vous trouverez ci-dessous une liste des syscalls qui ont été implémentées dans WSL.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1439">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="cbc9f-1440">Les syscalls dans cette liste sont pris en charge dans au moins un scénario, mais ils peuvent ne pas avoir tous les paramètres pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="cbc9f-1440">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
