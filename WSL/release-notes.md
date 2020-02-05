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
ms.sourcegitcommit: 7069b8d452308c32cc7fa31d1158fcb130d42e06
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/01/2020
ms.locfileid: "76911703"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="e1549-105">Notes de publication pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="e1549-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19555"></a><span data-ttu-id="e1549-106">Build 19555</span><span class="sxs-lookup"><span data-stu-id="e1549-106">Build 19555</span></span>
<span data-ttu-id="e1549-107">Pour des informations Windows d’ordre général sur la build 19555, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span><span class="sxs-lookup"><span data-stu-id="e1549-107">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="e1549-108">[WSL2] Utilisation d’un cgroup de mémoire pour limiter la quantité de mémoire utilisée par les opérations d’installation et de conversion [GH 4669]</span><span class="sxs-lookup"><span data-stu-id="e1549-108">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="e1549-109">Ajout de la présence de wsl.exe quand le composant facultatif Sous-système Windows pour Linux n’est pas activé pour améliorer la découvertabilité des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e1549-109">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="e1549-110">Changement de wsl.exe pour afficher le texte d’aide si le composant facultatif WSL n’est pas installé</span><span class="sxs-lookup"><span data-stu-id="e1549-110">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="e1549-111">Correction de la condition de concurrence lors de la création d’instances</span><span class="sxs-lookup"><span data-stu-id="e1549-111">Fix race condition when creating instances</span></span>
* <span data-ttu-id="e1549-112">Création de wslclient.dll qui contient toutes les fonctionnalités de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="e1549-112">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="e1549-113">Plus de plantage pendant l’arrêt du service LxssManagerUser</span><span class="sxs-lookup"><span data-stu-id="e1549-113">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="e1549-114">Correction de l’échec rapide de wslapi.dll quand le paramètre distroName est NULL</span><span class="sxs-lookup"><span data-stu-id="e1549-114">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="e1549-115">Build 19041</span><span class="sxs-lookup"><span data-stu-id="e1549-115">Build 19041</span></span>
<span data-ttu-id="e1549-116">Pour des informations Windows d’ordre général sur la build 19041, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span><span class="sxs-lookup"><span data-stu-id="e1549-116">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="e1549-117">[WSL2] Effacement du masque de signal avant de lancer les processus</span><span class="sxs-lookup"><span data-stu-id="e1549-117">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="e1549-118">[WSL2] Mise à jour du noyau Linux vers 4.19.84</span><span class="sxs-lookup"><span data-stu-id="e1549-118">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="e1549-119">Gestion de la création d’un lien symbolique /etc/resolv.conf quand le lien symbolique n’est pas relatif</span><span class="sxs-lookup"><span data-stu-id="e1549-119">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="e1549-120">Build 19028</span><span class="sxs-lookup"><span data-stu-id="e1549-120">Build 19028</span></span>
<span data-ttu-id="e1549-121">Pour des informations Windows d’ordre général sur la build 19028, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="e1549-121">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="e1549-122">[WSL2] Mise à jour du noyau Linux vers 4.19.81</span><span class="sxs-lookup"><span data-stu-id="e1549-122">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="e1549-123">[WSL2] Remplacer l’autorisation par défaut de /dev/net/Tun par 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="e1549-123">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="e1549-124">[WSL2] Ajuster la quantité de mémoire par défaut affectée à la machine virtuelle Linux pour qu’elle soit à 80 % de mémoire hôte</span><span class="sxs-lookup"><span data-stu-id="e1549-124">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="e1549-125">[WSL2] Correction du serveur Interop pour gérer les demandes avec un délai d’attente de sorte à empêcher les appelants incorrects de bloquer le serveur</span><span class="sxs-lookup"><span data-stu-id="e1549-125">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="e1549-126">Build 19018</span><span class="sxs-lookup"><span data-stu-id="e1549-126">Build 19018</span></span>
<span data-ttu-id="e1549-127">Pour des informations Windows d’ordre général sur la build 19018, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="e1549-127">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="e1549-128">[WSL2] Utilisation de cache=mmap comme valeur par défaut pour les montages 9p afin de corriger les applications dotnet</span><span class="sxs-lookup"><span data-stu-id="e1549-128">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="e1549-129">[WSL2] Corrections pour le relais localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="e1549-129">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="e1549-130">[WSL2] Introduction d’un montage tmpfs partagé multidistribution pour le partage de l’état entre plusieurs distributions</span><span class="sxs-lookup"><span data-stu-id="e1549-130">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="e1549-131">Correction de la restauration d’un lecteur réseau persistant pour \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="e1549-131">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="e1549-132">Build 19013</span><span class="sxs-lookup"><span data-stu-id="e1549-132">Build 19013</span></span>
<span data-ttu-id="e1549-133">Pour des informations Windows d’ordre général sur la build 19013, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="e1549-133">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="e1549-134">[WSL2] Amélioration des performances de la mémoire de la machine virtuelle de l’utilitaire WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-134">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="e1549-135">La mémoire qui n’est plus utilisée sera libérée et retournée à l’hôte.</span><span class="sxs-lookup"><span data-stu-id="e1549-135">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="e1549-136">[WSL2] Mise à jour de la version du noyau vers 4.19.79.</span><span class="sxs-lookup"><span data-stu-id="e1549-136">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="e1549-137">(ajout de CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK et CONFIG_BRIDGE_VLAN_FILTERING).</span><span class="sxs-lookup"><span data-stu-id="e1549-137">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="e1549-138">[WSL2] Correction du relais d’entrée pour gérer les cas où stdin est un handle de canal qui n’est pas fermé [GH 4424]</span><span class="sxs-lookup"><span data-stu-id="e1549-138">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="e1549-139">Vérification que \\\\wsl$ n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-139">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="e1549-140">Build 19002</span><span class="sxs-lookup"><span data-stu-id="e1549-140">Build 19002</span></span>
<span data-ttu-id="e1549-141">Pour des informations Windows d’ordre général sur la build 19002, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="e1549-141">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="e1549-142">[WSL] Correction du problème de gestion de certains caractères Unicode : https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="e1549-142">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="e1549-143">[WSL] Correction de cas rares où des distributions pouvaient être désinscrites si elles étaient lancées immédiatement après une mise à niveau build-à-build.</span><span class="sxs-lookup"><span data-stu-id="e1549-143">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="e1549-144">[WSL] Correction d’un problème mineur avec wsl. exe --shutdown où les minuteurs inactifs d’instance n’étaient pas annulés.</span><span class="sxs-lookup"><span data-stu-id="e1549-144">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="e1549-145">Build 18995</span><span class="sxs-lookup"><span data-stu-id="e1549-145">Build 18995</span></span>
<span data-ttu-id="e1549-146">Pour des informations Windows d’ordre général sur la build 18995, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="e1549-146">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="e1549-147">[WSL2] Correction d’un problème où les montages DrvFs cessaient de fonctionner après l’interruption d’une opération (par ex. ctrl-c) [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="e1549-147">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="e1549-148">[WSL2] Correction de la gestion des très longs messages hvsocket [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="e1549-148">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="e1549-149">[WSL2] Correction du problème avec l’interopérabilité quand stdin est un fichier [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="e1549-149">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="e1549-150">[WSL2] Correction du plantage du service lors d’un état inattendu du réseau [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="e1549-150">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="e1549-151">[WSL2] Interrogation du nom de distribution du serveur d’interopérabilité si le processus actuel n’a pas la variable d’environnement</span><span class="sxs-lookup"><span data-stu-id="e1549-151">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="e1549-152">[WSL2] Correction du problème avec l’interopérabilité quand stdin est un fichier</span><span class="sxs-lookup"><span data-stu-id="e1549-152">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="e1549-153">[WSL2] Mise à jour de la version du noyau Linux vers 4.19.72</span><span class="sxs-lookup"><span data-stu-id="e1549-153">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="e1549-154">[WSL2] Ajout de la possibilité de spécifier des paramètres de ligne de commande du noyau supplémentaires via .wslconfig</span><span class="sxs-lookup"><span data-stu-id="e1549-154">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="e1549-155">Build 18990</span><span class="sxs-lookup"><span data-stu-id="e1549-155">Build 18990</span></span>
<span data-ttu-id="e1549-156">Pour des informations Windows d’ordre général sur la build 18990, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="e1549-156">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="e1549-157">Améliorer les performances des listes de répertoires dans \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="e1549-157">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="e1549-158">[WSL2] Injecter un entropie de démarrage supplémentaire [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="e1549-158">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="e1549-159">[WSL2] Correctif pour Windows Interop lors de l’utilisation de su / sudo [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="e1549-159">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="e1549-160">Build 18980</span><span class="sxs-lookup"><span data-stu-id="e1549-160">Build 18980</span></span>
<span data-ttu-id="e1549-161">Pour obtenir des informations Windows d’ordre général sur la build 18980, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="e1549-161">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="e1549-162">Correction de la lecture des liens symboliques qui refusent FILE_READ_DATA.</span><span class="sxs-lookup"><span data-stu-id="e1549-162">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="e1549-163">Sont inclus tous les liens symboliques créés par Windows à des fins de compatibilité descendante, comme « C:\Document et Settings » et un ensemble de liens symboliques dans le répertoire du profil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1549-163">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="e1549-164">État de système de fichiers inattendu rendu récupérable [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="e1549-164">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="e1549-165">[WSL2] Ajout de la prise en charge d’arm64 si votre processeur/microprogramme prend en charge la virtualisation</span><span class="sxs-lookup"><span data-stu-id="e1549-165">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="e1549-166">[WSL2] Autorisation des utilisateurs non privilégiés à afficher le journal du noyau</span><span class="sxs-lookup"><span data-stu-id="e1549-166">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="e1549-167">[WSL2] Correction du relais de sortie quand les sockets stdout/stderr ont été fermés [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="e1549-167">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="e1549-168">[WSL2] Prise en charge du transfert de batterie et d’adaptateur secteur</span><span class="sxs-lookup"><span data-stu-id="e1549-168">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="e1549-169">[WSL2] Mise à jour du noyau Linux vers 4.19.67</span><span class="sxs-lookup"><span data-stu-id="e1549-169">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="e1549-170">Ajout de la possibilité de définir un nom d’utilisateur par défaut dans /etc/wsl.conf :</span><span class="sxs-lookup"><span data-stu-id="e1549-170">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="e1549-171">Build 18975</span><span class="sxs-lookup"><span data-stu-id="e1549-171">Build 18975</span></span>
<span data-ttu-id="e1549-172">Pour obtenir des informations Windows d’ordre général sur la Build 18975, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="e1549-172">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="e1549-173">[WSL2] Correction de plusieurs problèmes de fiabilité de localhost [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="e1549-173">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="e1549-174">Build 18970</span><span class="sxs-lookup"><span data-stu-id="e1549-174">Build 18970</span></span>
<span data-ttu-id="e1549-175">Pour obtenir des informations Windows d’ordre général sur la Build 18970, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="e1549-175">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="e1549-176">[WSL2] Synchronisation de l’heure avec celle de l’hôte quand le système sort de l’état de veille [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="e1549-176">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="e1549-177">[WSL2] Création de liens symboliques NT sur les volumes Windows quand cela est possible.</span><span class="sxs-lookup"><span data-stu-id="e1549-177">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="e1549-178">[WSL2] Création de distributions dans les espaces de noms UTS, IPC, PID et Mount.</span><span class="sxs-lookup"><span data-stu-id="e1549-178">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="e1549-179">[WSL2] Correction du relais de port localhost quand le serveur est directement lié à localhost [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="e1549-179">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="e1549-180">[WSL2] Correction d’interop quand la sortie est redirigée [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="e1549-180">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="e1549-181">[WSL2] Prise en charge de la traduction des liens symboliques NT absolus.</span><span class="sxs-lookup"><span data-stu-id="e1549-181">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="e1549-182">[WSL2] Mise à jour du noyau vers la version 4.19.59</span><span class="sxs-lookup"><span data-stu-id="e1549-182">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="e1549-183">[WSL2] Définition correcte du masque de sous-réseau pour eth0.</span><span class="sxs-lookup"><span data-stu-id="e1549-183">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="e1549-184">[WSL2] Changement de logique pour quitter la boucle de travail de la console lorsque l’événement de sortie est signalé.</span><span class="sxs-lookup"><span data-stu-id="e1549-184">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="e1549-185">[WSL2] Éjection du disque dur virtuel de distribution lorsque la distribution n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e1549-185">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="e1549-186">[WSL2] Correction de la bibliothèque d’analyse de configuration pour gérer correctement les valeurs vides.</span><span class="sxs-lookup"><span data-stu-id="e1549-186">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="e1549-187">[WSL2] Prise en charge de Docker Desktop en créant des montages entre les distributions.</span><span class="sxs-lookup"><span data-stu-id="e1549-187">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="e1549-188">Une distribution peut adopter ce comportement en ajoutant la ligne suivante au fichier /etc/wsl.conf :</span><span class="sxs-lookup"><span data-stu-id="e1549-188">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="e1549-189">Build 18945</span><span class="sxs-lookup"><span data-stu-id="e1549-189">Build 18945</span></span>
<span data-ttu-id="e1549-190">Pour obtenir des informations Windows d’ordre général sur la build 18945, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="e1549-190">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-191">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-191">WSL</span></span>
* <span data-ttu-id="e1549-192">[WSL2] Autorisation des sockets tcp d’écoute dans WSL2 pour qu’ils soient accessibles à partir de l’hôte en utilisant localhost:port</span><span class="sxs-lookup"><span data-stu-id="e1549-192">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="e1549-193">[WSL2] Correctifs pour les échecs d’installation/conversion et les diagnostics supplémentaires pour suivre les problèmes futurs [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="e1549-193">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="e1549-194">[WSL2] Améliorations de la possibilité de diagnostiquer les problèmes de réseau WSL2</span><span class="sxs-lookup"><span data-stu-id="e1549-194">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="e1549-195">[WSL2] Mise à jour de la version du noyau vers 4.19.55</span><span class="sxs-lookup"><span data-stu-id="e1549-195">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="e1549-196">[WSL2] Mise à jour du noyau avec les options de configuration requises pour Docker [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="e1549-196">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="e1549-197">[WSL2] Augmentation du nombre de processeurs affecté à la machine virtuelle utilitaire légère pour qu’il soit identique à celui de l’hôte (précédemment plafonné à 8 par CONFIG_NR_CPUS dans la configuration du noyau) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="e1549-197">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="e1549-198">[WSL2] Création d’un fichier d’échange pour la machine virtuelle légère WSL2</span><span class="sxs-lookup"><span data-stu-id="e1549-198">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="e1549-199">[WSL2] Autorisation de la visibilité des montages utilisateur par le biais de \\\\wsl$\\distro (par exemple, sshfs) [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="e1549-199">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="e1549-200">[WSL2] Amélioration des performances du système de fichiers 9p</span><span class="sxs-lookup"><span data-stu-id="e1549-200">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="e1549-201">[WSL2] Vérification que la liste ACL du disque dur virtuel n’augmente pas sans aucune limite [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="e1549-201">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="e1549-202">[WSL2] Mise à jour de la configuration du noyau pour prendre en charge squashfs et xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="e1549-202">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="e1549-203">[WSL2] Correctif pour interop.enabled /etc/wsl.conf option [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="e1549-203">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="e1549-204">[WSL2] Renvoi de ENOTSUP si le système de fichiers ne prend pas en charge les EA</span><span class="sxs-lookup"><span data-stu-id="e1549-204">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="e1549-205">[WSL2] Correction du blocage CopyFile avec \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="e1549-205">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="e1549-206">Remplacement de l’umask par défaut par 0022 et ajout du paramètre filesystem.umask à /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="e1549-206">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="e1549-207">Correction de wslpath pour résoudre correctement les liens symboliques (retour en arrière dans 19h1) [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="e1549-207">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="e1549-208">Introduction du fichier %UserProfile%\\.wslconfig pour modifier légèrement les paramètres WSL2</span><span class="sxs-lookup"><span data-stu-id="e1549-208">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="e1549-209">Build 18917</span><span class="sxs-lookup"><span data-stu-id="e1549-209">Build 18917</span></span>
<span data-ttu-id="e1549-210">Pour obtenir des informations Windows d’ordre général sur la build 18917, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="e1549-210">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-211">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-211">WSL</span></span>
* <span data-ttu-id="e1549-212">WSL 2 est maintenant disponible !</span><span class="sxs-lookup"><span data-stu-id="e1549-212">WSL 2 is now available!</span></span> <span data-ttu-id="e1549-213">Pour plus d’informations, consultez le [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="e1549-213">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="e1549-214">Correction d’un retour en arrière où le lancement de processus Windows par le biais de liens symboliques ne fonctionnait pas correctement [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="e1549-214">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="e1549-215">Ajout des options wsl.exe --list --verbose, wsl.exe --list --quiet et wsl.exe --import --version à wsl.exe</span><span class="sxs-lookup"><span data-stu-id="e1549-215">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="e1549-216">Ajout de l’option wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="e1549-216">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="e1549-217">Plan 9 : Autorisation de l’ouverture d’un répertoire pour que l’écriture aboutisse</span><span class="sxs-lookup"><span data-stu-id="e1549-217">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="e1549-218">Build 18890</span><span class="sxs-lookup"><span data-stu-id="e1549-218">Build 18890</span></span>
<span data-ttu-id="e1549-219">Pour obtenir des informations Windows d’ordre général sur la build 18890, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="e1549-219">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-220">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-220">WSL</span></span>
* <span data-ttu-id="e1549-221">Fuite de socket non bloquante [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="e1549-221">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="e1549-222">L’entrée EOF du terminal peut bloquer les lectures consécutives [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="e1549-222">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="e1549-223">Mise à jour de l’en-tête resolv.conf pour faire référence à wsl.conf [description dans GH 3928]</span><span class="sxs-lookup"><span data-stu-id="e1549-223">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="e1549-224">Blocage dans le code de suppression epoll [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="e1549-224">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="e1549-225">Gestion des espaces dans les arguments --import et –export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="e1549-225">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="e1549-226">L’extension des fichiers mmap ne fonctionne pas correctement [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="e1549-226">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="e1549-227">Correction du problème où l’accès ARM64 \\\\wsl$ ne fonctionnait pas correctement</span><span class="sxs-lookup"><span data-stu-id="e1549-227">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="e1549-228">Ajout d’une meilleure icône par défaut pour wsl.exe</span><span class="sxs-lookup"><span data-stu-id="e1549-228">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="e1549-229">Build 18342</span><span class="sxs-lookup"><span data-stu-id="e1549-229">Build 18342</span></span>
<span data-ttu-id="e1549-230">Pour obtenir des informations Windows d’ordre général sur la build 18342, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="e1549-230">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-231">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-231">WSL</span></span>
* <span data-ttu-id="e1549-232">Nous avons ajouté la possibilité pour les utilisateurs d’accéder aux fichiers Linux dans une distribution WSL à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-232">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="e1549-233">Ces fichiers sont accessibles par le biais de la ligne de commande. Des applications Windows, comme l’Explorateur de fichiers, VSCode, etc. peuvent aussi interagir avec ces fichiers.</span><span class="sxs-lookup"><span data-stu-id="e1549-233">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="e1549-234">Accédez à vos fichiers en naviguant vers \\\\wsl$\\<nom_distribution> ou consultez la liste des distributions en cours d’exécution en naviguant vers \\\\wsl$.</span><span class="sxs-lookup"><span data-stu-id="e1549-234">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="e1549-235">Ajout de balises d’informations de processeur supplémentaires et correction des valeurs Cpus_allowed[_list] [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="e1549-235">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="e1549-236">Prise en charge de l’exécution à partir d’un thread non-leader [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="e1549-236">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="e1549-237">Considération des échecs de mise à jour de configuration comme récupérables [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="e1549-237">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="e1549-238">Mise à jour de binfmt pour gérer correctement les décalages [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="e1549-238">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="e1549-239">Activation du mappage des lecteurs réseau pour le plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="e1549-239">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="e1549-240">Prise en charge de la traduction de chemins Windows > Linux et Linux-> Windows pour les montages de liaison</span><span class="sxs-lookup"><span data-stu-id="e1549-240">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="e1549-241">Création de sections en lecture seule pour les mappages sur les fichiers ouverts en lecture seule</span><span class="sxs-lookup"><span data-stu-id="e1549-241">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="e1549-242">Build 18334</span><span class="sxs-lookup"><span data-stu-id="e1549-242">Build 18334</span></span>
<span data-ttu-id="e1549-243">Pour obtenir des informations Windows d’ordre général sur la build 18334, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="e1549-243">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-244">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-244">WSL</span></span>
* <span data-ttu-id="e1549-245">Nouvelle conception de la façon dont le fuseau horaire Windows est mappé à un fuseau horaire Linux [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="e1549-245">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="e1549-246">Correction des fuites de mémoire et ajout de nouvelles fonctions de traduction de chaînes [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="e1549-246">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="e1549-247">SIGCONT sur un groupe de threads sans aucun thread est un no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="e1549-247">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="e1549-248">Correction de l’affichage des descripteurs de fichiers socket et epoll dans /proc/self/fd</span><span class="sxs-lookup"><span data-stu-id="e1549-248">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="e1549-249">Build 18305</span><span class="sxs-lookup"><span data-stu-id="e1549-249">Build 18305</span></span>
<span data-ttu-id="e1549-250">Pour obtenir des informations Windows d’ordre général sur la build 18305, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="e1549-250">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-251">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-251">WSL</span></span>
* <span data-ttu-id="e1549-252">Perte d’accès des pthreads aux fichiers lors de la sortie du thread principal [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="e1549-252">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="e1549-253">TIOCSCTTY doit ignorer le paramètre « force » sauf s’il est obligatoire [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="e1549-253">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="e1549-254">Améliorations de la ligne de commande wsl.exe et ajout de fonctionnalités d’importation/exportation.</span><span class="sxs-lookup"><span data-stu-id="e1549-254">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="e1549-255">Build 18277</span><span class="sxs-lookup"><span data-stu-id="e1549-255">Build 18277</span></span>
<span data-ttu-id="e1549-256">Pour obtenir des informations Windows d’ordre général sur la build 18277, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="e1549-256">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-257">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-257">WSL</span></span>
* <span data-ttu-id="e1549-258">Correction de l’erreur « Interface non prise en charge » introduite dans la build 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="e1549-258">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="e1549-259">Ignorance de l’indicateur MNT_FORCE pour umount syscall [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="e1549-259">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="e1549-260">Basculement d’interop WSL pour utiliser l’API CreatePseudoConsole officielle</span><span class="sxs-lookup"><span data-stu-id="e1549-260">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="e1549-261">Non-conservation d’une valeur de délai d’expiration au redémarrage de FUTEX_WAIT</span><span class="sxs-lookup"><span data-stu-id="e1549-261">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="e1549-262">Build 18272</span><span class="sxs-lookup"><span data-stu-id="e1549-262">Build 18272</span></span>
<span data-ttu-id="e1549-263">Pour obtenir des informations Windows d’ordre général sur la build 18272, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="e1549-263">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-264">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-264">WSL</span></span>
* <span data-ttu-id="e1549-265">**AVERTISSEMENT :** Un problème existant dans cette build rend WSL inopérable.</span><span class="sxs-lookup"><span data-stu-id="e1549-265">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="e1549-266">Quand vous essayez de lancer votre distribution, une erreur « Interface non prise en charge » s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e1549-266">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="e1549-267">Le problème est résolu et sa résolution va être intégrée à la build Insider Fast de la semaine prochaine.</span><span class="sxs-lookup"><span data-stu-id="e1549-267">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="e1549-268">Si vous avez installé cette build, vous pouvez revenir à la build Windows précédente en utilisant « Rétrograder vers la version précédente de Windows 10 » dans Paramètres->Mise à jour et sécurité->Récupération.</span><span class="sxs-lookup"><span data-stu-id="e1549-268">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="e1549-269">Build 18267</span><span class="sxs-lookup"><span data-stu-id="e1549-269">Build 18267</span></span>
<span data-ttu-id="e1549-270">Pour obtenir des informations Windows d’ordre général sur la build 18267, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="e1549-270">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-271">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-271">WSL</span></span>
* <span data-ttu-id="e1549-272">Correction du problème où le processus zombie n’est pas recueilli et reste indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="e1549-272">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="e1549-273">WslRegisterDistribution se bloque si le message d’erreur dépasse la longueur maximale [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="e1549-273">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="e1549-274">Autorisation de fsync à fonctionner correctement pour les fichiers en lecture seule sur DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="e1549-274">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="e1549-275">Vérification que les répertoires /bin et /sbin existent avant de créer des liens symboliques dans [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="e1549-275">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="e1549-276">Ajout d’un mécanisme de délai d’expiration avant l’arrêt d’une instance pour les instances WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-276">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="e1549-277">Le délai d’expiration est actuellement défini à 15 secondes, ce qui signifie que l’instance se termine 15 secondes après la fin du dernier processus WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-277">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="e1549-278">Pour arrêter immédiatement une distribution, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e1549-278">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="e1549-279">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="e1549-279">Build 17763 (1809)</span></span>
<span data-ttu-id="e1549-280">Pour obtenir des informations Windows d’ordre général sur la build 17763, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="e1549-280">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-281">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-281">WSL</span></span>
* <span data-ttu-id="e1549-282">Vérification des autorisations de Setpriority syscall trop stricte pour modifier la priorité du même thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="e1549-282">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="e1549-283">Garantie que l’heure d’interruption non biaisée est utilisée pour l’heure de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="e1549-283">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="e1549-284">Gestion des liens symboliques dans l’interpréteur binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="e1549-284">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="e1549-285">Meilleure gestion du nettoyage du descripteur de fichier leader de groupe de threads.</span><span class="sxs-lookup"><span data-stu-id="e1549-285">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="e1549-286">Basculement de WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter tout dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="e1549-286">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="e1549-287">Attachement ptrace à l’origine d’une valeur de retour incorrecte de la part des appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="e1549-287">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="e1549-288">Correction de plusieurs problèmes liés à AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="e1549-288">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="e1549-289">Correction du problème pouvant provoquer l’échec d’interop WSL si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="e1549-289">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="e1549-290">Évitement des connexions de boucle d’échec d’un délai d’une seconde à des ports inexistants [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="e1549-290">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="e1549-291">Ajout du fichier stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="e1549-291">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="e1549-292">Informations d’étendue IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="e1549-292">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="e1549-293">Prise en charge de PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="e1549-293">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="e1549-294">Système de fichiers de canal effaçant par inadvertance l’événement epoll déclenché latéralement [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="e1549-294">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="e1549-295">L’exécutable Win32 lancé par le biais d’un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="e1549-295">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="e1549-296">Prise en charge améliorée de zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="e1549-296">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="e1549-297">Ajout d’entrées wsl.conf pour contrôler le comportement d’interop Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="e1549-297">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="e1549-298">Correctif pour getsockname qui ne retourne pas toujours le type de famille des sockets UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="e1549-298">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="e1549-299">Ajout de la prise en charge de TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="e1549-299">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="e1549-300">Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="e1549-300">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="e1549-301">Prise en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="e1549-301">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="e1549-302">Correction du problème de vérification des autorisations sur le dossier racine [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="e1549-302">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="e1549-303">Prise en charge limitée des commandes IOCTL de clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="e1549-303">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="e1549-304">Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e1549-304">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="e1549-305">Ajout de l’option wsl -u ou --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="e1549-305">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="e1549-306">Correction des problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="e1549-306">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="e1549-307">Les sockets Unix ont besoin de conserver les informations d’identification des homologues déconnectés [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="e1549-307">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="e1549-308">Échec perpétuel des sockets Unix non bloquants avec EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="e1549-308">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="e1549-309">case=off est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="e1549-309">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="e1549-310">Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="e1549-310">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="e1549-311">Ajout de wslconfig /terminate pour arrêter les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e1549-311">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="e1549-312">Correction du problème lié aux entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins comportant des espaces.</span><span class="sxs-lookup"><span data-stu-id="e1549-312">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="e1549-313">Exposition du respect de la casse par répertoire en tant qu’attribut étendu</span><span class="sxs-lookup"><span data-stu-id="e1549-313">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="e1549-314">ARM64 : Émulation des opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="e1549-314">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="e1549-315">Résolution du [problème dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="e1549-315">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="e1549-316">DrvFs : uniquement les caractères de non-échappement de la plage privée qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="e1549-316">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="e1549-317">Correction de l’erreur « off-by-one » dans la validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="e1549-317">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="e1549-318">Les minuteurs absolus WSL avec une heure passée ne se déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="e1549-318">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="e1549-319">Vérification que les points de nouvelle analyse récemment créés sont listés comme tels dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="e1549-319">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="e1549-320">Création atomique de répertoires sensibles à la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="e1549-320">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="e1549-321">Correction d’un problème supplémentaire où les opérations multithread peuvent retourner ENOENT même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="e1549-321">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="e1549-322">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="e1549-322">[GH 2712]</span></span>
* <span data-ttu-id="e1549-323">Correction de l’échec de lancement de WSL quand UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="e1549-323">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="e1549-324">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="e1549-324">[GH 3020]</span></span>
* <span data-ttu-id="e1549-325">Ajout du menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="e1549-325">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="e1549-326">Pour l’utiliser, maintenez la touche Maj enfoncée et cliquez avec le bouton droit dans une fenêtre de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="e1549-326">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="e1549-327">Correction du comportement non bloquant du socket Unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="e1549-327">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="e1549-328">Correction de la commande NetLink bloquée comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="e1549-328">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="e1549-329">Ajout de la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="e1549-329">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="e1549-330">Correction du problème lié à la troncation qui n’engendre pas d’événements inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="e1549-330">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="e1549-331">Ajout de l’option --exec pour wsl.exe afin d’appeler un seul binaire sans shell.</span><span class="sxs-lookup"><span data-stu-id="e1549-331">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="e1549-332">Ajout de l’option --distribution pour wsl.exe afin de sélectionner une distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="e1549-332">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="e1549-333">Prise en charge limitée de dmesg.</span><span class="sxs-lookup"><span data-stu-id="e1549-333">Limited support for dmesg.</span></span> <span data-ttu-id="e1549-334">Les applications peuvent désormais se connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="e1549-334">Applications can now log to dmesg.</span></span> <span data-ttu-id="e1549-335">Le pilote WSL journalise des informations limitées sur dmesg.</span><span class="sxs-lookup"><span data-stu-id="e1549-335">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="e1549-336">À l’avenir, il sera développé pour transporter d’autres informations/diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="e1549-336">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="e1549-337">Remarque : dmesg est actuellement pris en charge par le biais de l’interface d’appareil `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="e1549-337">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="e1549-338">L’interface syscall `syslog` n’est pas encore prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1549-338">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="e1549-339">Et donc, certaines des options de ligne de commande `dmesg` comme `-S`, `-C`, ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="e1549-339">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="e1549-340">Changement du gid et du mode par défaut des appareils en série pour qu’ils correspondent aux natifs [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="e1549-340">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="e1549-341">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="e1549-341">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="e1549-342">Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="e1549-342">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="e1549-343">Certains caractères (comme « / », « : » et « \* ») ne sont pas autorisés et les noms d’attributs étendus ne sont pas sensibles à la casse sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="e1549-343">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="e1549-344">Build 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="e1549-344">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="e1549-345">Pour obtenir des informations Windows d’ordre général sur la build 18252, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="e1549-345">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-346">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-346">WSL</span></span>
* <span data-ttu-id="e1549-347">Déplacement des binaires init et bsdtar en dehors de la dll lxssmanager et dans un dossier d’outils distinct</span><span class="sxs-lookup"><span data-stu-id="e1549-347">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="e1549-348">Correction de la concurrence autour du descripteur de fichier de fermeture lors de l’utilisation de CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="e1549-348">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="e1549-349">Gestion des champs facultatifs dans /proc/pid/mountinfo lors de la traduction de chemins DrvFs</span><span class="sxs-lookup"><span data-stu-id="e1549-349">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="e1549-350">Autorisation de la réussite de DrvFs mknod sans prise en charge des métadonnées de S_IFREG</span><span class="sxs-lookup"><span data-stu-id="e1549-350">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="e1549-351">Les fichiers en lecture seule créés sur DrvFs doivent avoir l’attribut readonly défini [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="e1549-351">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="e1549-352">Ajout de l’assistance /sbin/mount.drvfs pour gérer le montage DrvFs</span><span class="sxs-lookup"><span data-stu-id="e1549-352">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="e1549-353">Utilisation du renommage POSIX dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="e1549-353">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="e1549-354">Autorisation de la traduction de chemins sur les volumes sans GUID de volume.</span><span class="sxs-lookup"><span data-stu-id="e1549-354">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="e1549-355">Build 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="e1549-355">Build 17738 (Fast)</span></span>
<span data-ttu-id="e1549-356">Pour obtenir des informations Windows d’ordre général sur la build 17738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="e1549-356">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-357">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-357">WSL</span></span>
* <span data-ttu-id="e1549-358">Vérification des autorisations de Setpriority syscall trop stricte pour modifier la priorité du même thread [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="e1549-358">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="e1549-359">Garantie que l’heure d’interruption non biaisée est utilisée pour l’heure de démarrage afin d’éviter de retourner des valeurs négatives pour clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="e1549-359">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="e1549-360">Gestion des liens symboliques dans l’interpréteur binfmt WSL [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="e1549-360">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="e1549-361">Meilleure gestion du nettoyage du descripteur de fichier leader de groupe de threads.</span><span class="sxs-lookup"><span data-stu-id="e1549-361">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="e1549-362">Build 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="e1549-362">Build 17728 (Fast)</span></span>
<span data-ttu-id="e1549-363">Pour obtenir des informations Windows d’ordre général sur la build 17728, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="e1549-363">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-364">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-364">WSL</span></span>
* <span data-ttu-id="e1549-365">Basculement de WSL pour utiliser KeQueryInterruptTimePrecise au lieu de KeQueryPerformanceCounter pour éviter tout dépassement de capacité [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="e1549-365">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="e1549-366">Attachement ptrace à l’origine d’une valeur de retour incorrecte de la part des appels système [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="e1549-366">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="e1549-367">Correction de plusieurs problèmes liés à AF_UNIX [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="e1549-367">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="e1549-368">Correction du problème pouvant provoquer l’échec d’interop WSL si le répertoire de travail actuel comporte moins de 5 caractères [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="e1549-368">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="e1549-369">Build 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="e1549-369">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="e1549-370">Pour obtenir des informations Windows d’ordre général sur la build 18204, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="e1549-370">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-371">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-371">WSL</span></span>
* <span data-ttu-id="e1549-372">Système de fichiers de canal effaçant par inadvertance l’événement epoll déclenché latéralement [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="e1549-372">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="e1549-373">L’exécutable Win32 lancé par le biais d’un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="e1549-373">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="e1549-374">Build 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="e1549-374">Build 17723 (Fast)</span></span>
<span data-ttu-id="e1549-375">Pour obtenir des informations Windows d’ordre général sur la build 17723, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="e1549-375">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-376">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-376">WSL</span></span>
* <span data-ttu-id="e1549-377">Évitement des connexions de boucle d’échec d’un délai d’une seconde à des ports inexistants [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="e1549-377">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="e1549-378">Ajout du fichier stub /proc/sys/fs/file-max [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="e1549-378">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="e1549-379">Informations d’étendue IPV6 plus précises.</span><span class="sxs-lookup"><span data-stu-id="e1549-379">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="e1549-380">Prise en charge de PR_SET_PTRACER [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="e1549-380">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="e1549-381">Système de fichiers de canal effaçant par inadvertance l’événement epoll déclenché latéralement [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="e1549-381">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="e1549-382">L’exécutable Win32 lancé par le biais d’un lien symbolique NTFS ne respecte pas le nom du lien symbolique [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="e1549-382">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="e1549-383">Build 17713</span><span class="sxs-lookup"><span data-stu-id="e1549-383">Build 17713</span></span>
<span data-ttu-id="e1549-384">Pour obtenir des informations Windows d’ordre général sur la build 17713, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="e1549-384">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-385">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-385">WSL</span></span>
* <span data-ttu-id="e1549-386">Prise en charge améliorée de zombie [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="e1549-386">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="e1549-387">Ajout d’entrées wsl.conf pour contrôler le comportement d’interop Windows [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="e1549-387">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="e1549-388">Correctif pour getsockname qui ne retourne pas toujours le type de famille des sockets UNIX [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="e1549-388">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="e1549-389">Ajout de la prise en charge de TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="e1549-389">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="e1549-390">Les sockets non bloquants dans le processus de connexion doivent retourner EAGAIN pour les tentatives d’écriture [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="e1549-390">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="e1549-391">Prise en charge d’interop sur les disques durs virtuels montés [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="e1549-391">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="e1549-392">Correction du problème de vérification des autorisations sur le dossier racine [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="e1549-392">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="e1549-393">Prise en charge limitée des commandes IOCTL de clavier TTY KDGKBTYPE, KDGKBMODE et KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="e1549-393">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="e1549-394">Les applications d’interface utilisateur Windows doivent s’exécuter même quand elles sont lancées en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e1549-394">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="e1549-395">Build 17704</span><span class="sxs-lookup"><span data-stu-id="e1549-395">Build 17704</span></span>
<span data-ttu-id="e1549-396">Pour obtenir des informations Windows d’ordre général sur la build 17704, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="e1549-396">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-397">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-397">WSL</span></span>
* <span data-ttu-id="e1549-398">Ajout de l’option wsl -u ou --user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="e1549-398">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="e1549-399">Correction des problèmes de lancement de WSL quand le démarrage rapide est activé [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="e1549-399">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="e1549-400">Les sockets Unix ont besoin de conserver les informations d’identification des homologues déconnectés [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="e1549-400">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="e1549-401">Échec perpétuel des sockets Unix non bloquants avec EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="e1549-401">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="e1549-402">case=off est le nouveau type de montage drvfs par défaut [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="e1549-402">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="e1549-403">Pour plus d’informations, consultez le [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="e1549-403">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="e1549-404">Ajout de wslconfig /terminate pour arrêter les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e1549-404">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="e1549-405">Build 17692</span><span class="sxs-lookup"><span data-stu-id="e1549-405">Build 17692</span></span>
<span data-ttu-id="e1549-406">Pour obtenir des informations Windows d’ordre général sur la build 17692, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="e1549-406">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-407">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-407">WSL</span></span>
* <span data-ttu-id="e1549-408">Correction du problème lié aux entrées du menu contextuel de l’interpréteur de commandes WSL qui ne gèrent pas correctement les chemins comportant des espaces.</span><span class="sxs-lookup"><span data-stu-id="e1549-408">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="e1549-409">Exposition du respect de la casse par répertoire en tant qu’attribut étendu</span><span class="sxs-lookup"><span data-stu-id="e1549-409">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="e1549-410">ARM64 : Émulation des opérations de maintenance du cache.</span><span class="sxs-lookup"><span data-stu-id="e1549-410">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="e1549-411">Résolution du [problème dotnet](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="e1549-411">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="e1549-412">DrvFs : uniquement les caractères de non-échappement de la plage privée qui correspondent à un caractère d’échappement.</span><span class="sxs-lookup"><span data-stu-id="e1549-412">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="e1549-413">Build 17686</span><span class="sxs-lookup"><span data-stu-id="e1549-413">Build 17686</span></span>
<span data-ttu-id="e1549-414">Pour obtenir des informations Windows d’ordre général sur la build 17686, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="e1549-414">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-415">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-415">WSL</span></span>
* <span data-ttu-id="e1549-416">Correction de l’erreur « off-by-one » dans la validation de la longueur de l’interpréteur de l’analyseur ELF [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="e1549-416">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="e1549-417">Les minuteurs absolus WSL avec une heure passée ne se déclenchent pas [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="e1549-417">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="e1549-418">Vérification que les points de nouvelle analyse récemment créés sont listés comme tels dans le répertoire parent.</span><span class="sxs-lookup"><span data-stu-id="e1549-418">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="e1549-419">Création atomique de répertoires sensibles à la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="e1549-419">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="e1549-420">Build 17677</span><span class="sxs-lookup"><span data-stu-id="e1549-420">Build 17677</span></span>
<span data-ttu-id="e1549-421">Pour obtenir des informations Windows d’ordre général sur la build 17677, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="e1549-421">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-422">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-422">WSL</span></span>
* <span data-ttu-id="e1549-423">Correction d’un problème supplémentaire où les opérations multithread peuvent retourner ENOENT même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="e1549-423">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="e1549-424">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="e1549-424">[GH 2712]</span></span>
* <span data-ttu-id="e1549-425">Correction de l’échec de lancement de WSL quand UMCI est activé.</span><span class="sxs-lookup"><span data-stu-id="e1549-425">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="e1549-426">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="e1549-426">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="e1549-427">Build 17666</span><span class="sxs-lookup"><span data-stu-id="e1549-427">Build 17666</span></span>
<span data-ttu-id="e1549-428">Pour obtenir des informations Windows d’ordre général sur la build 17666, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="e1549-428">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-429">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-429">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="e1549-430">AVERTISSEMENT : Un problème empêche WSL de s’exécuter sur certains chipsets AMD [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="e1549-430">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="e1549-431">Un correctif est prêt et rejoint la branche de la build Insider.</span><span class="sxs-lookup"><span data-stu-id="e1549-431">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="e1549-432">Ajout du menu contextuel de l’Explorateur pour lancer WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="e1549-432">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="e1549-433">Pour l’utiliser, maintenez la touche Maj enfoncée et cliquez avec le bouton droit dans une fenêtre de l’Explorateur.</span><span class="sxs-lookup"><span data-stu-id="e1549-433">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="e1549-434">Correction du comportement non bloquant du socket unix [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="e1549-434">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="e1549-435">Correction de la commande NetLink bloquée comme indiqué dans GH 2026.</span><span class="sxs-lookup"><span data-stu-id="e1549-435">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="e1549-436">Ajout de la prise en charge des indicateurs de propagation de montage [GH 2911].</span><span class="sxs-lookup"><span data-stu-id="e1549-436">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="e1549-437">Correction du problème lié à la troncation qui n’engendre pas d’événements inotify [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="e1549-437">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="e1549-438">Ajout de l’option --exec pour wsl.exe afin d’appeler un seul binaire sans shell.</span><span class="sxs-lookup"><span data-stu-id="e1549-438">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="e1549-439">Ajout de l’option --distribution pour wsl.exe afin de sélectionner une distribution spécifique.</span><span class="sxs-lookup"><span data-stu-id="e1549-439">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="e1549-440">Build 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="e1549-440">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="e1549-441">Pour obtenir des informations Windows d’ordre général sur la build 17655, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="e1549-441">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-442">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-442">WSL</span></span>
* <span data-ttu-id="e1549-443">Prise en charge limitée de dmesg.</span><span class="sxs-lookup"><span data-stu-id="e1549-443">Limited support for dmesg.</span></span> <span data-ttu-id="e1549-444">Les applications peuvent désormais se connecter à dmesg.</span><span class="sxs-lookup"><span data-stu-id="e1549-444">Applications can now log to dmesg.</span></span> <span data-ttu-id="e1549-445">Le pilote WSL journalise des informations limitées sur dmesg.</span><span class="sxs-lookup"><span data-stu-id="e1549-445">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="e1549-446">À l’avenir, il sera développé pour transporter d’autres informations/diagnostics à partir du pilote.</span><span class="sxs-lookup"><span data-stu-id="e1549-446">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="e1549-447">Remarque : dmesg est actuellement pris en charge par le biais de l’interface d’appareil `/dev/kmsg`.</span><span class="sxs-lookup"><span data-stu-id="e1549-447">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="e1549-448">L’interface sycall `syslog` n’est pas encore prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1549-448">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="e1549-449">Et donc, certaines des options de ligne de commande `dmesg` comme `-S`, `-C`, ne fonctionnent pas.</span><span class="sxs-lookup"><span data-stu-id="e1549-449">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="e1549-450">Correction d’un problème où les opérations multithread peuvent retourner ENOENT même si le fichier existe.</span><span class="sxs-lookup"><span data-stu-id="e1549-450">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="e1549-451">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="e1549-451">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="e1549-452">Build 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="e1549-452">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="e1549-453">Pour obtenir des informations Windows d’ordre général sur la build 17639, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="e1549-453">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-454">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-454">WSL</span></span>
* <span data-ttu-id="e1549-455">Changement du gid et du mode par défaut des appareils en série pour qu’ils correspondent aux natifs [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="e1549-455">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="e1549-456">DrvFs prend désormais en charge les attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="e1549-456">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="e1549-457">Remarque : DrvFs présente certaines limitations quant au nom des attributs étendus.</span><span class="sxs-lookup"><span data-stu-id="e1549-457">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="e1549-458">En particulier, certains caractères (comme « / », « : » et « \* ») ne sont pas autorisés et les noms d’attributs étendus ne sont pas sensibles à la casse sur DrvFs.</span><span class="sxs-lookup"><span data-stu-id="e1549-458">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="e1549-459">Build 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="e1549-459">Build 17133 (Fast)</span></span>
<span data-ttu-id="e1549-460">Pour obtenir des informations Windows d’ordre général sur la build 17133, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="e1549-460">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-461">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-461">WSL</span></span>
* <span data-ttu-id="e1549-462">Correction du blocage dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-462">Fix for hang in WSL.</span></span> <span data-ttu-id="e1549-463">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="e1549-463">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="e1549-464">Build 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="e1549-464">Build 17128 (Fast)</span></span>
<span data-ttu-id="e1549-465">Pour obtenir des informations Windows d’ordre général sur la build 17128, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="e1549-465">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-466">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-466">WSL</span></span>
* <span data-ttu-id="e1549-467">Aucune</span><span class="sxs-lookup"><span data-stu-id="e1549-467">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="e1549-468">Build 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="e1549-468">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="e1549-469">Pour obtenir des informations Windows d’ordre général sur la build 17627, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="e1549-469">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-470">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-470">WSL</span></span>
* <span data-ttu-id="e1549-471">Ajout de la prise en charge des opérations futex pi-aware.</span><span class="sxs-lookup"><span data-stu-id="e1549-471">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="e1549-472">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="e1549-472">[GH 1006]</span></span>
    * <span data-ttu-id="e1549-473">Notez qu’actuellement, les priorités ne sont pas une fonctionnalité de WSL prise en charge. Il existe donc des limitations, mais l’utilisation standard doit être débloquée.</span><span class="sxs-lookup"><span data-stu-id="e1549-473">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="e1549-474">Prise en charge du pare-feu Windows pour les processus WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-474">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="e1549-475">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="e1549-475">[GH 1852]</span></span>
    * <span data-ttu-id="e1549-476">Par exemple, pour autoriser le processus python WSL à écouter sur n’importe quel port, utilisez la commande Windows avec élévation de privilèges : ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="e1549-476">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="e1549-477">Pour plus d’informations sur l’ajout de règles de pare-feu, consultez [lien](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="e1549-477">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="e1549-478">Respectez le shell par défaut de l’utilisateur lors de l’utilisation de wsl.exe.</span><span class="sxs-lookup"><span data-stu-id="e1549-478">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="e1549-479">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="e1549-479">[GH 2372]</span></span>
* <span data-ttu-id="e1549-480">Signalisation de toutes les interfaces réseau en tant qu’Ethernet.</span><span class="sxs-lookup"><span data-stu-id="e1549-480">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="e1549-481">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="e1549-481">[GH 2996]</span></span>
* <span data-ttu-id="e1549-482">Meilleure gestion du fichier /etc/passwd endommagé.</span><span class="sxs-lookup"><span data-stu-id="e1549-482">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="e1549-483">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="e1549-483">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="e1549-484">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-484">Console</span></span>
* <span data-ttu-id="e1549-485">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-486">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-486">LTP Results:</span></span>
<span data-ttu-id="e1549-487">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-487">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="e1549-488">Build 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="e1549-488">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="e1549-489">Pour obtenir des informations Windows d’ordre général sur la build 17618, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="e1549-489">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-490">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-490">WSL</span></span>
* <span data-ttu-id="e1549-491">Introduction de la fonctionnalité de pseudoconsole pour interop NT [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="e1549-491">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="e1549-492">Le mécanisme d’installation hérité (lxrun.exe) est déprécié.</span><span class="sxs-lookup"><span data-stu-id="e1549-492">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="e1549-493">Le mécanisme pris en charge pour l’installation des distributions passe par Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="e1549-493">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="e1549-494">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-494">Console</span></span>
* <span data-ttu-id="e1549-495">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-496">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-496">LTP Results:</span></span>
<span data-ttu-id="e1549-497">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-497">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="e1549-498">Build 17110</span><span class="sxs-lookup"><span data-stu-id="e1549-498">Build 17110</span></span>
<span data-ttu-id="e1549-499">Pour obtenir des informations Windows d’ordre général sur la build 17110, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="e1549-499">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-500">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-500">WSL</span></span>
* <span data-ttu-id="e1549-501">Autorisation de l’arrêt de /init à partir de Windows [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="e1549-501">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="e1549-502">DrvFs utilise désormais par défaut le respect de la casse par répertoire (ce qui équivaut à l’option de montage « case=dir »).</span><span class="sxs-lookup"><span data-stu-id="e1549-502">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="e1549-503">L’utilisation de « case=force » (ancien comportement) demande la définition d’une clé de Registre.</span><span class="sxs-lookup"><span data-stu-id="e1549-503">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="e1549-504">Exécutez la commande suivante pour activer « case=force » si vous avez besoin de l’utiliser : reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="e1549-504">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="e1549-505">Si vous avez des répertoires existants créés avec WSL dans une version antérieure de Windows qui ont besoin d’être sensibles à la casse, utilisez fsutil.exe pour les marquer comme sensibles à la casse : fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="e1549-505">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="e1549-506">Chaînes d’arrêt NULL retournées par uname syscall.</span><span class="sxs-lookup"><span data-stu-id="e1549-506">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="e1549-507">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-507">Console</span></span>
* <span data-ttu-id="e1549-508">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-508">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-509">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-509">LTP Results:</span></span>
<span data-ttu-id="e1549-510">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-510">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="e1549-511">Build 17107</span><span class="sxs-lookup"><span data-stu-id="e1549-511">Build 17107</span></span>
<span data-ttu-id="e1549-512">Pour obtenir des informations Windows d’ordre général sur la build 17107, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="e1549-512">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-513">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-513">WSL</span></span>
* <span data-ttu-id="e1549-514">Prise en charge de TCSETSF et TCSETSW sur les points de terminaison pty maîtres [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="e1549-514">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="e1549-515">Le démarrage de processus interop simultanés peut entraîner EINVAL [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="e1549-515">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="e1549-516">Correction de PTRACE_ATTACH pour présenter l’état de suivi approprié dans /proc/pid/status.</span><span class="sxs-lookup"><span data-stu-id="e1549-516">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="e1549-517">Correction de la concurrence où les processus de courte durée clonés avec des indicateurs CLEARTID et SETTID peuvent quitter sans effacer l’adresse TID.</span><span class="sxs-lookup"><span data-stu-id="e1549-517">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="e1549-518">Affiche un message lors de la mise à niveau des répertoires du système de fichiers Linux à partir d’une build antérieure à 17093.</span><span class="sxs-lookup"><span data-stu-id="e1549-518">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="e1549-519">Pour plus d’informations sur les changements du système de fichiers 17093, consultez les notes de publication de [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="e1549-519">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="e1549-520">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-520">Console</span></span>
* <span data-ttu-id="e1549-521">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-521">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-522">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-522">LTP Results:</span></span>
<span data-ttu-id="e1549-523">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-523">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="e1549-524">Build 17101</span><span class="sxs-lookup"><span data-stu-id="e1549-524">Build 17101</span></span>
<span data-ttu-id="e1549-525">Pour obtenir des informations Windows d’ordre général sur la build 17101, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="e1549-525">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-526">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-526">WSL</span></span>
* <span data-ttu-id="e1549-527">Prise en charge de signalfd.</span><span class="sxs-lookup"><span data-stu-id="e1549-527">Support for signalfd.</span></span> <span data-ttu-id="e1549-528">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="e1549-528">[GH 129]</span></span>
* <span data-ttu-id="e1549-529">Prise en charge des noms de fichiers contenant des caractères NTFS non conformes en les encodant en tant que caractères Unicode privés.</span><span class="sxs-lookup"><span data-stu-id="e1549-529">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="e1549-530">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="e1549-530">[GH 1514]</span></span>
* <span data-ttu-id="e1549-531">Le montage automatique repasse en lecture seule quand l’écriture n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1549-531">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="e1549-532">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="e1549-532">[GH 2603]</span></span>
* <span data-ttu-id="e1549-533">Autorisation du collage de paires de substitution Unicode (comme les caractères Emoji).</span><span class="sxs-lookup"><span data-stu-id="e1549-533">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="e1549-534">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="e1549-534">[GH 2765]</span></span>
* <span data-ttu-id="e1549-535">Les pseudofichiers contenus dans /proc et /sys doivent revenir prêts pour la lecture et l’écriture à l’issue de select, poll, epoll et autres [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="e1549-535">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="e1549-536">Correction du problème qui peut amener le service à tourner infiniment en boucle quand le registre a été falsifié ou qu’il est endommagé.</span><span class="sxs-lookup"><span data-stu-id="e1549-536">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="e1549-537">Correction des messages netlink pour qu’ils fonctionnent avec la version plus récente (4.14 en amont) de iproute2.</span><span class="sxs-lookup"><span data-stu-id="e1549-537">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="e1549-538">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-538">Console</span></span>
* <span data-ttu-id="e1549-539">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-539">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-540">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-540">LTP Results:</span></span>
<span data-ttu-id="e1549-541">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-541">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="e1549-542">Build 17093</span><span class="sxs-lookup"><span data-stu-id="e1549-542">Build 17093</span></span>
<span data-ttu-id="e1549-543">Pour obtenir des informations Windows d’ordre général sur la build 17093, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-543">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="e1549-544">Important :</span><span class="sxs-lookup"><span data-stu-id="e1549-544">Important:</span></span>
<span data-ttu-id="e1549-545">Quand vous démarrez WSL pour la première fois après la mise à niveau vers cette build, certaines tâches doivent être effectuées pour mettre à niveau les répertoires du système de fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="e1549-545">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="e1549-546">Ces tâches peuvent prendre plusieurs minutes, c’est pourquoi WSL peut sembler démarrer lentement.</span><span class="sxs-lookup"><span data-stu-id="e1549-546">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="e1549-547">Cette lenteur ne devrait se produire qu’une seule fois pour chaque distribution installée à partir du Store.</span><span class="sxs-lookup"><span data-stu-id="e1549-547">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="e1549-548">Prise en charge améliorée du respect de la casse dans DrvFs.</span><span class="sxs-lookup"><span data-stu-id="e1549-548">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="e1549-549">DrvFs prend désormais en charge le respect de la casse par répertoire.</span><span class="sxs-lookup"><span data-stu-id="e1549-549">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="e1549-550">Il s’agit d’un nouvel indicateur qui peut être défini sur les répertoires pour indiquer que toutes les opérations dans ces répertoires doivent être traitées comme sensibles à la casse, ce qui permet même aux applications Windows d’ouvrir correctement les fichiers qui diffèrent uniquement par la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-550">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="e1549-551">DrvFs dispose de nouvelles options de montage contrôlant le respect de la casse par répertoire</span><span class="sxs-lookup"><span data-stu-id="e1549-551">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="e1549-552">case=force : tous les répertoires sont traités comme sensibles à la casse (à l’exception de la racine du lecteur).</span><span class="sxs-lookup"><span data-stu-id="e1549-552">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="e1549-553">Les nouveaux répertoires créés avec WSL sont marqués comme sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-553">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="e1549-554">Il s’agit du comportement hérité, à l’exception du marquage de nouveaux répertoires sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-554">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="e1549-555">case=dir : seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme sensibles à la casse ; les autres répertoires ne sont pas sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-555">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="e1549-556">Les nouveaux répertoires créés avec WSL sont marqués comme sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-556">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="e1549-557">case=off : seuls les répertoires avec l’indicateur de respect de la casse par répertoire sont traités comme sensibles à la casse ; les autres répertoires ne sont pas sensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-557">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="e1549-558">Les nouveaux répertoires créés avec WSL sont marqués comme insensibles à la casse.</span><span class="sxs-lookup"><span data-stu-id="e1549-558">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="e1549-559">Remarque : cet indicateur n’est pas défini pour les répertoires créés par WSL dans les versions précédentes, donc ils ne sont pas traités comme sensibles à la casse si vous utilisez l’option « case=dir ».</span><span class="sxs-lookup"><span data-stu-id="e1549-559">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="e1549-560">Un moyen de définir cet indicateur sur des répertoires existants sera bientôt disponible.</span><span class="sxs-lookup"><span data-stu-id="e1549-560">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="e1549-561">Exemple de montage avec ces options (pour les lecteurs existants, vous devez d’abord démonter avant de pouvoir monter avec des options différentes) : sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="e1549-561">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="e1549-562">Pour le moment, case=force est toujours l’option par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1549-562">For now, case=force is still the default option.</span></span> <span data-ttu-id="e1549-563">Celle-ci sera remplacée par case=dir à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="e1549-563">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="e1549-564">Vous pouvez maintenant utiliser des barres obliques dans les chemins Windows lors du montage de DrvFs, par exemple : sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="e1549-564">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="e1549-565">WSL traite maintenant le fichier /etc/fstab au démarrage de l’instance [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="e1549-565">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="e1549-566">Cette opération est effectuée avant le montage automatique des lecteurs DrvFs. Tous les lecteurs déjà montés par fstab ne sont pas remontés automatiquement, ce qui vous permet de modifier le point de montage pour des lecteurs spécifiques.</span><span class="sxs-lookup"><span data-stu-id="e1549-566">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="e1549-567">Ce comportement peut être désactivé à l’aide de wsl.conf.</span><span class="sxs-lookup"><span data-stu-id="e1549-567">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="e1549-568">Les fichiers mount, mountinfo et mountstats dans /proc échappent correctement les caractères spéciaux comme les barres obliques inverses et les espaces [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="e1549-568">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="e1549-569">Les fichiers spéciaux créés avec DrvFs, comme les liens symboliques WSL, les fichiers FIFO et les sockets quand les métadonnées sont activées, peuvent maintenant être copiés et déplacés à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-569">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="e1549-570">WSL est plus configurable avec wsl.conf</span><span class="sxs-lookup"><span data-stu-id="e1549-570">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="e1549-571">Nous avons ajouté une méthode pour vous permettre de configurer automatiquement certaines fonctionnalités dans WSL afin qu’elles soient appliquées chaque fois que vous lancez le sous-système.</span><span class="sxs-lookup"><span data-stu-id="e1549-571">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="e1549-572">Cela comprend les options de montage automatique et la configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="e1549-572">This includes automount options and network configuration.</span></span> <span data-ttu-id="e1549-573">Découvrez-en davantage dans notre billet de blog sur : https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="e1549-573">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="e1549-574">AF_UNIX autorise les connexions de sockets entre les processus Linux sur WSL et les processus natifs Windows</span><span class="sxs-lookup"><span data-stu-id="e1549-574">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="e1549-575">Les applications WSL et Windows peuvent maintenant communiquer entre elles par le biais de sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="e1549-575">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="e1549-576">Imaginez que vous souhaitez exécuter un service dans Windows et le rendre disponible aux applications à la fois Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-576">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="e1549-577">Désormais, cela est possible avec des sockets Unix.</span><span class="sxs-lookup"><span data-stu-id="e1549-577">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="e1549-578">Pour en savoir plus, consultez notre billet de blog sur https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="e1549-578">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-579">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-579">WSL</span></span>
* <span data-ttu-id="e1549-580">Prise en charge de mmap() avec MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="e1549-580">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="e1549-581">Prise en charge de CLONE_PTRACE et CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="e1549-581">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="e1549-582">Gestion du signal de fin non-SIGCHLD dans le clone [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="e1549-582">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="e1549-583">Stub /proc/sys/fs/inotify/max_user_instances et /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="e1549-583">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="e1549-584">Erreur lors du chargement des binaires ELF qui contiennent des en-têtes de charge avec des décalages non nuls [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="e1549-584">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="e1549-585">Zéro pour les octets de page de fin lors du chargement des images.</span><span class="sxs-lookup"><span data-stu-id="e1549-585">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="e1549-586">Réduction des cas où execve arrête silencieusement le processus</span><span class="sxs-lookup"><span data-stu-id="e1549-586">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="e1549-587">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-587">Console</span></span>
* <span data-ttu-id="e1549-588">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-588">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-589">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-589">LTP Results:</span></span>
<span data-ttu-id="e1549-590">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-590">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="e1549-591">Build 17083</span><span class="sxs-lookup"><span data-stu-id="e1549-591">Build 17083</span></span>
<span data-ttu-id="e1549-592">Pour obtenir des informations Windows d’ordre général sur la build 17083, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-592">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-593">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-593">WSL</span></span>
* <span data-ttu-id="e1549-594">Correction de la vérification d’erreur liée à epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="e1549-594">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="e1549-595">Correction des blocages lors de la désactivation d’ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="e1549-595">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="e1549-596">Assurance que les opérations mmap apparaissent atomiques [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="e1549-596">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="e1549-597">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-597">Console</span></span>
* <span data-ttu-id="e1549-598">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-598">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-599">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-599">LTP Results:</span></span>
<span data-ttu-id="e1549-600">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-600">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="e1549-601">Build 17074</span><span class="sxs-lookup"><span data-stu-id="e1549-601">Build 17074</span></span>
<span data-ttu-id="e1549-602">Pour obtenir des informations Windows d’ordre général sur la build 17074, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-602">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-603">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-603">WSL</span></span>
* <span data-ttu-id="e1549-604">Correction du format de stockage des métadonnées DrvFs [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="e1549-604">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="e1549-605">**Important :** Les métadonnées DrvFs créées avant cette build s’affichent de manière incorrecte ou pas du tout.</span><span class="sxs-lookup"><span data-stu-id="e1549-605">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="e1549-606">Pour corriger les fichiers affectés, utilisez chmod et chown pour réappliquer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e1549-606">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="e1549-607">Correction du problème lié à de multiples signaux et syscalls redémarrables.</span><span class="sxs-lookup"><span data-stu-id="e1549-607">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="e1549-608">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-608">Console</span></span>
* <span data-ttu-id="e1549-609">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-609">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-610">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-610">LTP Results:</span></span>
<span data-ttu-id="e1549-611">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-611">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="e1549-612">Build 17063</span><span class="sxs-lookup"><span data-stu-id="e1549-612">Build 17063</span></span>
<span data-ttu-id="e1549-613">Pour obtenir des informations Windows d’ordre général sur la build 17063, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-613">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="e1549-614">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-614">WSL</span></span>
* <span data-ttu-id="e1549-615">DrvFs prend en charge des métadonnées Linux supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e1549-615">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="e1549-616">Cette prise en charge permet de définir le propriétaire et le mode des fichiers à l’aide de chmod/chown, ainsi que de créer des fichiers spéciaux, comme les FIFO, les sockets Unix et les fichiers d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e1549-616">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="e1549-617">Cette fonctionnalité est désactivée par défaut pour le moment, car elle est toujours expérimentale.</span><span class="sxs-lookup"><span data-stu-id="e1549-617">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="e1549-618">**Remarque :**  Nous avons corrigé un bogue dans le format des métadonnées utilisé par DrvFs.</span><span class="sxs-lookup"><span data-stu-id="e1549-618">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="e1549-619">Bien que les métadonnées fonctionnent sur cette build à des fins d’expérimentation, les futures builds ne liront pas correctement les métadonnées créées par cette Build.</span><span class="sxs-lookup"><span data-stu-id="e1549-619">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="e1549-620">Vous devrez peut-être mettre à jour manuellement le propriétaire des fichiers modifiés et vous devrez recréer les appareils dont l’ID est personnalisé.</span><span class="sxs-lookup"><span data-stu-id="e1549-620">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="e1549-621">Pour activer cette fonctionnalité, montez DrvFs avec l’option métadonnées (pour l’activer sur un montage existant, vous devez d’abord le démonter) :</span><span class="sxs-lookup"><span data-stu-id="e1549-621">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="e1549-622">Les autorisations Linux sont ajoutées en tant que métadonnées supplémentaires au fichier ; elles n’affectent pas les autorisations Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-622">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="e1549-623">N’oubliez pas que la modification d’un fichier à l’aide d’un éditeur Windows risque de supprimer les métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e1549-623">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="e1549-624">Dans ce cas, le fichier reprend ses autorisations par défaut.</span><span class="sxs-lookup"><span data-stu-id="e1549-624">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="e1549-625">Ajout d’options de montage à DrvFs pour contrôler les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e1549-625">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="e1549-626">uid : identifiant utilisateur utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="e1549-626">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="e1549-627">gid : ID de groupe utilisé pour le propriétaire de tous les fichiers.</span><span class="sxs-lookup"><span data-stu-id="e1549-627">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="e1549-628">umask : masque octal des autorisations à exclure pour tous les fichiers et répertoires.</span><span class="sxs-lookup"><span data-stu-id="e1549-628">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="e1549-629">fmask : masque octal des autorisations à exclure pour tous les fichiers standard.</span><span class="sxs-lookup"><span data-stu-id="e1549-629">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="e1549-630">dmask : masque octal des autorisations à exclure pour tous les répertoires.</span><span class="sxs-lookup"><span data-stu-id="e1549-630">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="e1549-631">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e1549-631">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="e1549-632">Combinaison avec l’option de métadonnées pour spécifier des autorisations par défaut pour les fichiers sans métadonnées.</span><span class="sxs-lookup"><span data-stu-id="e1549-632">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="e1549-633">Introduction d’une nouvelle variable d’environnement, `WSLENV`, pour configurer la façon dont les variables d’environnement circulent entre WSL et Win32.</span><span class="sxs-lookup"><span data-stu-id="e1549-633">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="e1549-634">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e1549-634">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="e1549-635">`WSLENV` est une liste de variables d’environnement séparées par des deux-points qui peuvent être incluses lors du lancement de processus WSL à partir de Win32 ou de processus Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-635">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="e1549-636">Chaque variable peut être suffixée à l’aide d’une barre oblique suivie d’indicateurs pour spécifier son mode de traduction.</span><span class="sxs-lookup"><span data-stu-id="e1549-636">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="e1549-637">p : La valeur est un chemin qui doit être traduit entre les chemins WSL et les chemins Win32.</span><span class="sxs-lookup"><span data-stu-id="e1549-637">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="e1549-638">l : La valeur est une liste de chemins.</span><span class="sxs-lookup"><span data-stu-id="e1549-638">l: The value is a list of paths.</span></span> <span data-ttu-id="e1549-639">Dans WSL, il s’agit d’une liste délimitée par des deux-points.</span><span class="sxs-lookup"><span data-stu-id="e1549-639">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="e1549-640">Dans Win32, il s’agit d’une liste délimitée par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="e1549-640">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="e1549-641">u : La valeur doit être incluse uniquement lors de l’appel de WSL à partir de Win32.</span><span class="sxs-lookup"><span data-stu-id="e1549-641">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="e1549-642">w : La valeur doit être incluse uniquement lors de l’appel de Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-642">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="e1549-643">Vous pouvez définir `WSLENV` dans .bashrc ou dans l’environnement Windows personnalisé pour votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e1549-643">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="e1549-644">Les montages drvfs préservent correctement les horodatages de tar, cp -p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="e1549-644">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="e1549-645">Les liens symboliques drvfs signale la taille correcte (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="e1549-645">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="e1549-646">La lecture/écriture fonctionne pour de très grandes tailles d’E/S (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="e1549-646">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="e1549-647">waitpid fonctionne avec des ID de groupe de processus (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="e1549-647">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="e1549-648">Amélioration significative des performances mmap pour les régions de réserve volumineuses ; amélioration des performances ghc (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="e1549-648">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="e1549-649">Prise en charge de la personnalité pour READ_IMPLIES_EXEC ; correction de maxima et clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="e1549-649">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="e1549-650">Prise en charge par mprotect de PROT_GROWSDOWN ; correction de clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="e1549-650">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="e1549-651">Correction des erreurs de page en mode de survalidation ; correction de sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="e1549-651">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="e1549-652">Prise en charge par le clone de davantage de combinaisons d’indicateurs</span><span class="sxs-lookup"><span data-stu-id="e1549-652">clone supports more flags combinations</span></span>
* <span data-ttu-id="e1549-653">Prise en charge select/epoll de fichiers epoll (auparavant un no-op).</span><span class="sxs-lookup"><span data-stu-id="e1549-653">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="e1549-654">Notification de ptrace des syscalls non implémentés.</span><span class="sxs-lookup"><span data-stu-id="e1549-654">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="e1549-655">Ignorance des interfaces absentes lors de la génération de serveurs de noms resolv.conf [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="e1549-655">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="e1549-656">Énumération des interfaces réseau sans adresse physique.</span><span class="sxs-lookup"><span data-stu-id="e1549-656">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="e1549-657">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="e1549-657">[GH 2685]</span></span>
* <span data-ttu-id="e1549-658">Correctifs de bogues et améliorations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="e1549-658">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="e1549-659">Outils Linux disponibles pour les développeurs sur Windows</span><span class="sxs-lookup"><span data-stu-id="e1549-659">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="e1549-660">Inclusion par la chaîne d’outils de ligne de commande Windows de bsdtar (tar) et de curl.</span><span class="sxs-lookup"><span data-stu-id="e1549-660">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="e1549-661">Lisez [ce blog](https://aka.ms/tarcurlwindows) pour en savoir plus sur l’ajout de ces deux nouveaux outils et découvrir leur effet sur l’expérience des développeurs sur Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-661">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="e1549-662">`AF_UNIX` est disponible dans le SDK Windows Insider (17061+).</span><span class="sxs-lookup"><span data-stu-id="e1549-662">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="e1549-663">Lisez [ce blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) pour en savoir plus sur `AF_UNIX` et sur la manière dont les développeurs sur Windows peuvent l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="e1549-663">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="e1549-664">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-664">Console</span></span>
* <span data-ttu-id="e1549-665">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-665">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-666">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-666">LTP Results:</span></span>
<span data-ttu-id="e1549-667">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-667">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="e1549-668">Build 17046</span><span class="sxs-lookup"><span data-stu-id="e1549-668">Build 17046</span></span>

<span data-ttu-id="e1549-669">Pour obtenir des informations Windows d’ordre général sur la build 17046, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="e1549-669">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="e1549-670">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-670">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-671">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-671">WSL</span></span>
- <span data-ttu-id="e1549-672">Autorisation des processus à s’exécuter sans terminal actif.</span><span class="sxs-lookup"><span data-stu-id="e1549-672">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="e1549-673">[GH 709, 1007, 1511, 2252, 2391 et autres]</span><span class="sxs-lookup"><span data-stu-id="e1549-673">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="e1549-674">Meilleure prise en charge de CLONE_VFORK et CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="e1549-674">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="e1549-675">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="e1549-675">[GH 1878, 2615]</span></span>
- <span data-ttu-id="e1549-676">Ignorance des pilotes de filtre TDI pour les opérations de mise en réseau WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-676">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="e1549-677">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="e1549-677">[GH 1554]</span></span>
- <span data-ttu-id="e1549-678">DrvFs crée des liens symboliques NT lorsque certaines conditions sont remplies.</span><span class="sxs-lookup"><span data-stu-id="e1549-678">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="e1549-679">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="e1549-679">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="e1549-680">La cible du lien doit être relative, ne doit pas traverser des points de montage ni des liens symboliques et doit exister.</span><span class="sxs-lookup"><span data-stu-id="e1549-680">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="e1549-681">L’utilisateur doit avoir SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (cela nécessite normalement que vous lançiez wsl.exe avec élévation de privilèges), à moins que le mode développeur ne soit activé.</span><span class="sxs-lookup"><span data-stu-id="e1549-681">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="e1549-682">Dans toutes les autres situations, DrvFs crée toujours des liens symboliques WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-682">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="e1549-683">Autorisation de l’exécution simultanée d’instances WSL avec et sans élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="e1549-683">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="e1549-684">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="e1549-684">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="e1549-685">Ajout de wslpath pour effectuer des conversions de chemins WSL<->Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-685">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="e1549-686">[GH 522, 1243, 1834, 2327 et autres]</span><span class="sxs-lookup"><span data-stu-id="e1549-686">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="e1549-687">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-687">Console</span></span>
- <span data-ttu-id="e1549-688">Aucun correctif.</span><span class="sxs-lookup"><span data-stu-id="e1549-688">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-689">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-689">LTP Results:</span></span>
<span data-ttu-id="e1549-690">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-690">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="e1549-691">Build 17040</span><span class="sxs-lookup"><span data-stu-id="e1549-691">Build 17040</span></span>

<span data-ttu-id="e1549-692">Pour obtenir des informations Windows d’ordre général sur la build 17040, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="e1549-692">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-693">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-693">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-694">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-694">WSL</span></span>
- <span data-ttu-id="e1549-695">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="e1549-695">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-696">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-696">Console</span></span>
- <span data-ttu-id="e1549-697">Aucun correctif depuis 17035.</span><span class="sxs-lookup"><span data-stu-id="e1549-697">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-698">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-698">LTP Results:</span></span>
<span data-ttu-id="e1549-699">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-699">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="e1549-700">Build 17035</span><span class="sxs-lookup"><span data-stu-id="e1549-700">Build 17035</span></span>

<span data-ttu-id="e1549-701">Pour obtenir des informations Windows d’ordre général sur la build 17035, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="e1549-701">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-702">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-702">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-703">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-703">WSL</span></span>
- <span data-ttu-id="e1549-704">L’accès aux fichiers sur DrvFs peut parfois échouer avec EINVAL.</span><span class="sxs-lookup"><span data-stu-id="e1549-704">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="e1549-705">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="e1549-705">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-706">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-706">Console</span></span>
- <span data-ttu-id="e1549-707">Perte de couleurs lors de l’insertion/la suppression de lignes en mode VT.</span><span class="sxs-lookup"><span data-stu-id="e1549-707">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-708">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-708">LTP Results:</span></span>
<span data-ttu-id="e1549-709">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-709">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="e1549-710">Build 17025</span><span class="sxs-lookup"><span data-stu-id="e1549-710">Build 17025</span></span>

<span data-ttu-id="e1549-711">Pour obtenir des informations Windows d’ordre général sur la build 17025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="e1549-711">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-712">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-712">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-713">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-713">WSL</span></span>
- <span data-ttu-id="e1549-714">Démarrage des processus initiaux dans un nouveau groupe de processus de premier plan [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="e1549-714">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="e1549-715">Correctifs de remise SIGHUP [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="e1549-715">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="e1549-716">Génération d’un nom de pont virtuel par défaut s’il n’est pas fourni [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="e1549-716">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="e1549-717">Implémentation de /proc/sys/kernel/random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="e1549-717">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="e1549-718">Autres correctifs de canal stdout/stderr Interop.</span><span class="sxs-lookup"><span data-stu-id="e1549-718">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="e1549-719">Appel système syncfs stub.</span><span class="sxs-lookup"><span data-stu-id="e1549-719">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-720">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-720">Console</span></span>
- <span data-ttu-id="e1549-721">Correction de la traduction VT d’entrée pour les consoles tierces [GH 111]</span><span class="sxs-lookup"><span data-stu-id="e1549-721">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-722">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-722">LTP Results:</span></span>
<span data-ttu-id="e1549-723">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-723">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="e1549-724">Build 17017</span><span class="sxs-lookup"><span data-stu-id="e1549-724">Build 17017</span></span>

<span data-ttu-id="e1549-725">Pour obtenir des informations Windows d’ordre général sur la build 17017, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="e1549-725">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-726">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-726">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-727">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-727">WSL</span></span>
- <span data-ttu-id="e1549-728">Ignorance des en-têtes de programme ELF vides [GH 330].</span><span class="sxs-lookup"><span data-stu-id="e1549-728">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="e1549-729">Autorisation de LxssManager à créer des instances WSL pour les utilisateurs non interactifs (prise en charge de ssh et des tâches planifiées) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="e1549-729">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="e1549-730">Prise en charge des scénarios WSL->Win32->WSL (« introduction ») [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="e1549-730">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="e1549-731">Prise en charge limitée de l’arrêt des applications console appelées par le biais d’Interop [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="e1549-731">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="e1549-732">Prise en charge d’options de montage pour devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="e1549-732">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="e1549-733">Blocage du démarrage enfant par Ptrace [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="e1549-733">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="e1549-734">Événements manquants dans EPOLLET [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="e1549-734">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="e1549-735">Retour de données supplémentaires pour PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="e1549-735">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="e1549-736">Getdents avec lseek donne des résultats incorrects.</span><span class="sxs-lookup"><span data-stu-id="e1549-736">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="e1549-737">Correction de certains blocages d’application interop Win32, en attente d’une entrée sur un canal qui n’a plus de données.</span><span class="sxs-lookup"><span data-stu-id="e1549-737">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="e1549-738">Prise en charge O_ASYNC pour les fichiers tty/pty.</span><span class="sxs-lookup"><span data-stu-id="e1549-738">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="e1549-739">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-739">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-740">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-740">Console</span></span>
- <span data-ttu-id="e1549-741">Aucune modification liée à la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-741">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-742">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-742">LTP Results:</span></span>
<span data-ttu-id="e1549-743">Test en cours.</span><span class="sxs-lookup"><span data-stu-id="e1549-743">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="e1549-744">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="e1549-744">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="e1549-745">Build 16288</span><span class="sxs-lookup"><span data-stu-id="e1549-745">Build 16288</span></span>

<span data-ttu-id="e1549-746">Pour obtenir des informations Windows d’ordre général sur la build 16288, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="e1549-746">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-747">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-747">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-748">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-748">WSL</span></span>
- <span data-ttu-id="e1549-749">Lancement et signalement corrects des uid, gid et du mode pour les descripteurs de fichiers socket [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="e1549-749">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="e1549-750">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-750">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-751">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-751">Console</span></span>
- <span data-ttu-id="e1549-752">Aucune modification liée à la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-752">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-753">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-753">LTP Results:</span></span>
<span data-ttu-id="e1549-754">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="e1549-754">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="e1549-755">Build 16278</span><span class="sxs-lookup"><span data-stu-id="e1549-755">Build 16278</span></span>

<span data-ttu-id="e1549-756">Pour obtenir des informations Windows d’ordre général sur la build 162738, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="e1549-756">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-757">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-757">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-758">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-758">WSL</span></span>
- <span data-ttu-id="e1549-759">Annulation explicite du mappage des vues mappées de sections sauvegardées dans un fichier lors du déchirement de l’état LX MM [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="e1549-759">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="e1549-760">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-760">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-761">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-761">Console</span></span>
- <span data-ttu-id="e1549-762">Aucune modification liée à la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-762">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-763">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-763">LTP Results:</span></span>
<span data-ttu-id="e1549-764">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="e1549-764">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="e1549-765">Build 16275</span><span class="sxs-lookup"><span data-stu-id="e1549-765">Build 16275</span></span>

<span data-ttu-id="e1549-766">Pour obtenir des informations Windows d’ordre général sur la build 162735, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="e1549-766">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-767">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-767">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-768">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-768">WSL</span></span>
- <span data-ttu-id="e1549-769">Aucune modification liée à WSL dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-769">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-770">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-770">Console</span></span>
- <span data-ttu-id="e1549-771">Aucune modification liée à la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-771">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-772">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-772">LTP Results:</span></span>
<span data-ttu-id="e1549-773">Aucune modification depuis 16273</span><span class="sxs-lookup"><span data-stu-id="e1549-773">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="e1549-774">Build 16273</span><span class="sxs-lookup"><span data-stu-id="e1549-774">Build 16273</span></span>

<span data-ttu-id="e1549-775">Pour obtenir des informations Windows d’ordre général sur la build 16273, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-775">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-776">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-776">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-777">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-777">WSL</span></span>
- <span data-ttu-id="e1549-778">Résolution d’un problème lié au signalement occasionnel par DrvFs d’un type de fichier incorrect pour les répertoires [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="e1549-778">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="e1549-779">Autorisation de la création de sockets NETLINK_KOBJECT_UEVENT pour débloquer des programmes qui utilisent uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="e1549-779">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="e1549-780">Ajout de la prise en charge de la connexion non bloquante [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="e1549-780">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="e1549-781">Implémentation de l’indicateur d’appel système de clone CLONE_FS [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="e1549-781">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="e1549-782">Résolution des problèmes liés à la gestion incorrecte des tabulations ou des guillemets dans NT Interop [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="e1549-782">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="e1549-783">Correction de l’erreur d’accès refusé lors de la tentative de redémarrage des instances WSL [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="e1549-783">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="e1549-784">Implémentation des opérations futex FUTEX_REQUEUE et FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="e1549-784">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="e1549-785">Correction des autorisations de divers fichiers SysFs [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="e1549-785">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="e1549-786">Correction du blocage de l’assemblage Haskell lors de l’installation [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="e1549-786">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="e1549-787">Implémentation des indicateurs binfmt_misc C, O et P [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="e1549-787">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="e1549-788">Ajout de /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="e1549-788">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="e1549-789">Ajout de la prise en charge partielle de l’appel système ioprio_set [GH 498]</span><span class="sxs-lookup"><span data-stu-id="e1549-789">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="e1549-790">Stub SO_REUSEPORT & ajout de la prise en charge de SO_PASSCRED pour les sockets netlink [GH 69]</span><span class="sxs-lookup"><span data-stu-id="e1549-790">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="e1549-791">Retour de différents codes d’erreur à partir de RegisterDistribuiton si une distribution est en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="e1549-791">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="e1549-792">Autorisation de la désinscription des distributions WSL partiellement installées par le biais de wslconfig.exe</span><span class="sxs-lookup"><span data-stu-id="e1549-792">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="e1549-793">Correction du blocage du test de socket Python à partir de udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="e1549-793">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="e1549-794">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-794">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-795">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-795">Console</span></span>
- <span data-ttu-id="e1549-796">Aucune modification liée à la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-796">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-797">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-797">LTP Results:</span></span>
<span data-ttu-id="e1549-798">Nombre total de tests : 1904</span><span class="sxs-lookup"><span data-stu-id="e1549-798">Total Tests: 1904</span></span><br/>
<span data-ttu-id="e1549-799">Nombre total de tests ignorés : 209</span><span class="sxs-lookup"><span data-stu-id="e1549-799">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="e1549-800">Nombre total d’échecs : 229</span><span class="sxs-lookup"><span data-stu-id="e1549-800">Total Failures: 229</span></span><br/>
[<span data-ttu-id="e1549-801">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-801">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="e1549-802">Build 16257</span><span class="sxs-lookup"><span data-stu-id="e1549-802">Build 16257</span></span>

<span data-ttu-id="e1549-803">Pour obtenir des informations Windows d’ordre général sur la build 16257, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-803">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-804">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-804">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-805">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-805">WSL</span></span>
- <span data-ttu-id="e1549-806">Implémentation d’un appel système prlimit64</span><span class="sxs-lookup"><span data-stu-id="e1549-806">Implement prlimit64 system call</span></span>
- <span data-ttu-id="e1549-807">Ajout de la prise en charge de ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="e1549-807">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="e1549-808">Stub MSG_MORE pour les sockets TCP [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="e1549-808">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="e1549-809">Correction du comportement de vecteur auxiliaire AT_EXECFN non valide [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="e1549-809">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="e1549-810">Correction du comportement de copie/collage pour la console/tty et ajout d’une meilleure gestion du tampon complet [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="e1549-810">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="e1549-811">Définition d’AT_SECURE dans le vecteur auxiliaire pour des programmes set-user-ID et set-group-ID [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="e1549-811">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="e1549-812">Non-gestion de TIOCPGRP par le point de terminaison maître du pseudo-terminal [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="e1549-812">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="e1549-813">Correction d’lseek pour le rewind des répertoires dans LxFs [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="e1549-813">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="e1549-814">Verrouillage de /dev/ptmx après une utilisation intensive [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="e1549-814">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="e1549-815">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-815">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-816">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-816">Console</span></span>
- <span data-ttu-id="e1549-817">Correction des lignes horizontales/traits de soulignement partout [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="e1549-817">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="e1549-818">Correction de l’ordre du processus modifié à l’origine d’une fermeture de NPM plus difficile [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="e1549-818">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="e1549-819">Ajout de notre nouveau jeu de couleurs : https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="e1549-819">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-820">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-820">LTP Results:</span></span>
<span data-ttu-id="e1549-821">Aucune modification depuis 16251</span><span class="sxs-lookup"><span data-stu-id="e1549-821">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-822">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-822">Syscall Support</span></span>
<span data-ttu-id="e1549-823">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-823">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-824">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-824">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="e1549-825">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="e1549-825">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="e1549-826">Problème GitHub 2392 : Dossiers Windows non reconnus par WSL...</span><span class="sxs-lookup"><span data-stu-id="e1549-826">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="e1549-827">Dans la build 16257, WSL rencontre des problèmes lors de l’énumération des fichiers/dossiers Windows par le biais de `/mnt/c/...`.</span><span class="sxs-lookup"><span data-stu-id="e1549-827">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="e1549-828">Ce problème a été résolu et publié dans la build Insiders la semaine démarrant le 14/08/2017.</span><span class="sxs-lookup"><span data-stu-id="e1549-828">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="e1549-829">Build 16251</span><span class="sxs-lookup"><span data-stu-id="e1549-829">Build 16251</span></span>

<span data-ttu-id="e1549-830">Pour obtenir des informations Windows d’ordre général sur la build 16251, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-830">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-831">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-831">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-832">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-832">WSL</span></span>
- <span data-ttu-id="e1549-833">Suppression de la balise bêta du composant facultatif WSL. Pour plus d’informations, consultez ce [billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="e1549-833">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="e1549-834">Lancement correct des uid et gid définis et enregistrés pour les binaires set-user-ID et set-group-ID sur exec [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="e1549-834">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="e1549-835">Ajout de la prise en charge de ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="e1549-835">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="e1549-836">Ajout de la prise en charge de ptrace PTRACE_GETFPREGS et PTRACE_GETREGSET avec NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="e1549-836">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="e1549-837">Correction de ptrace pour effectuer un arrêt sur les signaux ignorés</span><span class="sxs-lookup"><span data-stu-id="e1549-837">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="e1549-838">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-838">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-839">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-839">Console</span></span>
- <span data-ttu-id="e1549-840">Aucune modification liée à la console dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-840">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-841">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-841">LTP Results:</span></span>
<span data-ttu-id="e1549-842">Nombre de tests réussis : 768</span><span class="sxs-lookup"><span data-stu-id="e1549-842">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="e1549-843">Nombre de tests ayant échoué : 244</span><span class="sxs-lookup"><span data-stu-id="e1549-843">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="e1549-844">Nombre de tests ignorés : 96</span><span class="sxs-lookup"><span data-stu-id="e1549-844">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="e1549-845">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-845">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="e1549-846">Build 16241</span><span class="sxs-lookup"><span data-stu-id="e1549-846">Build 16241</span></span>

<span data-ttu-id="e1549-847">Pour obtenir des informations Windows d’ordre général sur la build 16241, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-847">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-848">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-848">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="e1549-849">WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-849">WSL</span></span>
- <span data-ttu-id="e1549-850">Aucune modification liée à WSL dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-850">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="e1549-851">Console</span><span class="sxs-lookup"><span data-stu-id="e1549-851">Console</span></span>
- <span data-ttu-id="e1549-852">Correction de la sortie d’un caractère incorrect pour la décimale des lignes croisées, signalée [ici](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) à l’origine</span><span class="sxs-lookup"><span data-stu-id="e1549-852">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="e1549-853">Correction de l’absence de texte de sortie affiché dans la page de codes 65001 (UTF8)</span><span class="sxs-lookup"><span data-stu-id="e1549-853">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="e1549-854">Ne transférez pas les modifications apportées aux valeurs RVB d’une couleur vers d’autres parties de la palette lors de la modification de la sélection.</span><span class="sxs-lookup"><span data-stu-id="e1549-854">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="e1549-855">La feuille de propriétés de la console sera ainsi beaucoup plus facile à utiliser.</span><span class="sxs-lookup"><span data-stu-id="e1549-855">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="e1549-856">Ctrl+S ne semble pas fonctionner correctement</span><span class="sxs-lookup"><span data-stu-id="e1549-856">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="e1549-857">Annuler la mise en gras/estomper totalement absent des codes d’échappement ANSI [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="e1549-857">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="e1549-858">La console ne prend pas en charge correctement les thèmes de couleur Vim [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="e1549-858">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="e1549-859">Impossible de coller des caractères particuliers [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="e1549-859">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="e1549-860">Le redimensionnement de l’ajustement dynamique interagit de façon étrange avec le redimensionnement d’une fenêtre bash quand des éléments se trouvent sur la ligne de commande/d’édition [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="e1549-860">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="e1549-861">Ctrl-L laisse l’écran sale [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="e1549-861">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="e1549-862">Bogue de rendu de la console lors de l’affichage de VT sur HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="e1549-862">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="e1549-863">Apparence étrange des caractères japonais avec le caractère Unicode U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="e1549-863">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="e1549-864">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-864">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="e1549-865">Build 16237</span><span class="sxs-lookup"><span data-stu-id="e1549-865">Build 16237</span></span>

<span data-ttu-id="e1549-866">Pour obtenir des informations Windows d’ordre général sur la build 16237, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-866">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-867">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-867">Fixed</span></span>
- <span data-ttu-id="e1549-868">Utilisation d’attributs par défaut pour les fichiers sans EA dans lxfs (racine, racine, 0000)</span><span class="sxs-lookup"><span data-stu-id="e1549-868">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="e1549-869">Ajout de la prise en charge des distributions qui utilisent des attributs étendus</span><span class="sxs-lookup"><span data-stu-id="e1549-869">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="e1549-870">Correction du remplissage pour les entrées retournées par getdents et getdents64</span><span class="sxs-lookup"><span data-stu-id="e1549-870">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="e1549-871">Correction des autorisations pour l’appel système shmctl SHM_STAT [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="e1549-871">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="e1549-872">Correction de l’état epoll initial incorrect pour tty [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="e1549-872">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="e1549-873">Correction de DrvFs readdir qui ne retourne pas toutes les entrées [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="e1549-873">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="e1549-874">Correction de LxFs readdir quand des fichiers ne sont pas liés [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="e1549-874">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="e1549-875">Autorisation de la rouverture des fichiers drvfs non liés par le biais de procfs</span><span class="sxs-lookup"><span data-stu-id="e1549-875">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="e1549-876">Ajout d’un remplacement de clé de Registre global pour la désactivation des fonctionnalités WSL (interop/montage de lecteur)</span><span class="sxs-lookup"><span data-stu-id="e1549-876">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="e1549-877">Correction du nombre de blocs incorrects dans « stat » pour DrvFs (et LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="e1549-877">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="e1549-878">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-878">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="e1549-879">Build 16232</span><span class="sxs-lookup"><span data-stu-id="e1549-879">Build 16232</span></span>

<span data-ttu-id="e1549-880">Pour obtenir des informations Windows d’ordre général sur la build 16232, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-880">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-881">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-881">Fixed</span></span>
- <span data-ttu-id="e1549-882">Aucune modification liée à WSL dans cette version.</span><span class="sxs-lookup"><span data-stu-id="e1549-882">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="e1549-883">Build 16226</span><span class="sxs-lookup"><span data-stu-id="e1549-883">Build 16226</span></span>

<span data-ttu-id="e1549-884">Pour obtenir des informations Windows d’ordre général sur la build 16226, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-884">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-885">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-885">Fixed</span></span>
- <span data-ttu-id="e1549-886">Prise en charge des syscalls liés à xattr (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="e1549-886">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="e1549-887">Prise en charge de security.capablity xattr.</span><span class="sxs-lookup"><span data-stu-id="e1549-887">security.capablity xattr support.</span></span>
- <span data-ttu-id="e1549-888">Amélioration de la compatibilité avec certains filtres et systèmes de fichiers, notamment les serveurs SMB non-MS.</span><span class="sxs-lookup"><span data-stu-id="e1549-888">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="e1549-889">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="e1549-889">[GH #1952]</span></span>
- <span data-ttu-id="e1549-890">Prise en charge améliorée des espaces réservés OneDrive, des espaces réservés GVFS et des fichiers compressés Compact OS.</span><span class="sxs-lookup"><span data-stu-id="e1549-890">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="e1549-891">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-891">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="e1549-892">Build 16215</span><span class="sxs-lookup"><span data-stu-id="e1549-892">Build 16215</span></span>

<span data-ttu-id="e1549-893">Pour obtenir des informations Windows d’ordre général sur la build 16215, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-893">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-894">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-894">Fixed</span></span>
- <span data-ttu-id="e1549-895">WSL n’exige plus le mode développeur.</span><span class="sxs-lookup"><span data-stu-id="e1549-895">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="e1549-896">Prise en charge des jonctions de répertoires dans drvfs.</span><span class="sxs-lookup"><span data-stu-id="e1549-896">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="e1549-897">Gestion de la désinstallation des packages appx de distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-897">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="e1549-898">Mise à jour de procfs pour afficher les mappages privés et partagés.</span><span class="sxs-lookup"><span data-stu-id="e1549-898">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="e1549-899">Ajout de la possibilité pour wslconfig.exe de nettoyer les distributions partiellement installées ou désinstallées.</span><span class="sxs-lookup"><span data-stu-id="e1549-899">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="e1549-900">Ajout de la prise en charge de IP_MTU_DISCOVER pour les sockets TCP.</span><span class="sxs-lookup"><span data-stu-id="e1549-900">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="e1549-901">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="e1549-901">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="e1549-902">Déduction de la famille de protocoles pour les routes vers AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="e1549-902">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="e1549-903">Améliorations des appareils série [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="e1549-903">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="e1549-904">Build 16199</span><span class="sxs-lookup"><span data-stu-id="e1549-904">Build 16199</span></span>

<span data-ttu-id="e1549-905">Pour obtenir des informations Windows d’ordre général sur la Build 16199, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-905">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-906">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-906">Fixed</span></span>
- <span data-ttu-id="e1549-907">Aucune modification liée à WSL dans ces versions.</span><span class="sxs-lookup"><span data-stu-id="e1549-907">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="e1549-908">Build 16193</span><span class="sxs-lookup"><span data-stu-id="e1549-908">Build 16193</span></span>

<span data-ttu-id="e1549-909">Pour obtenir des informations Windows d’ordre général sur la Build 16193, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-909">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-910">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-910">Fixed</span></span>
- <span data-ttu-id="e1549-911">Condition de concurrence entre l’envoi de SIGCONT et un arrêt de groupe de threads [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="e1549-911">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="e1549-912">Modification des appareils tty et pty pour signaler FILE_DEVICE_NAMED_PIPE au lieu de FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="e1549-912">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="e1549-913">Correctif SSH pour IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="e1549-913">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="e1549-914">Déplacement du montage DrvFs vers le démon init [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="e1549-914">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="e1549-915">Ajout de la prise en charge dans DrvFs des liens symboliques NT suivants.</span><span class="sxs-lookup"><span data-stu-id="e1549-915">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="e1549-916">Build 16184</span><span class="sxs-lookup"><span data-stu-id="e1549-916">Build 16184</span></span>

<span data-ttu-id="e1549-917">Pour obtenir des informations Windows d’ordre général sur la Build 16184, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-917">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-918">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-918">Fixed</span></span>
- <span data-ttu-id="e1549-919">Suppression de la tâche de maintenance de package apt (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="e1549-919">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="e1549-920">Correction de la sortie qui ne s’affiche pas à partir des processus Windows dans node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="e1549-920">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="e1549-921">Assouplissement des exigences d’alignement dans lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="e1549-921">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="e1549-922">Correction de la gestion de l’indicateur AT_EMPTY_PATH dans plusieurs appels système.</span><span class="sxs-lookup"><span data-stu-id="e1549-922">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="e1549-923">Résolution du problème où la suppression de fichiers DrvFs avec des handles ouverts entraîne un comportement non défini du fichier [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="e1549-923">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="e1549-924">/etc/hosts hérite désormais des entrées du fichier hosts Windows (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="e1549-924">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="e1549-925">Build 16179</span><span class="sxs-lookup"><span data-stu-id="e1549-925">Build 16179</span></span>

<span data-ttu-id="e1549-926">Pour obtenir des informations Windows d’ordre général sur la Build 16179, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-926">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-927">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-927">Fixed</span></span>
- <span data-ttu-id="e1549-928">Aucune modification de WSL cette semaine.</span><span class="sxs-lookup"><span data-stu-id="e1549-928">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="e1549-929">Build 16176</span><span class="sxs-lookup"><span data-stu-id="e1549-929">Build 16176</span></span>

<span data-ttu-id="e1549-930">Pour obtenir des informations Windows d’ordre général sur la Build 16176, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-930">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-931">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-931">Fixed</span></span>

- [<span data-ttu-id="e1549-932">Prise en charge série activée</span><span class="sxs-lookup"><span data-stu-id="e1549-932">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="e1549-933">Ajout de l’option de socket IP IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="e1549-933">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="e1549-934">Implémentation de la fonction pwritev (lors du chargement du fichier sur nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="e1549-934">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="e1549-935">Ajout des options de socket IP IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="e1549-935">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="e1549-936">Prise en charge de l’option de socket IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="e1549-936">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="e1549-937">Ajout de l’option de socket IP(V6)_MTU pour apps node, traceroute, dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="e1549-937">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="e1549-938">Ajout de l’option de socket IP IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="e1549-938">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="e1549-939">Améliorations du système de fichiers</span><span class="sxs-lookup"><span data-stu-id="e1549-939">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="e1549-940">Autorisation du montage de chemins UNC</span><span class="sxs-lookup"><span data-stu-id="e1549-940">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="e1549-941">Activation de la prise en charge de CDFS dans drvfs</span><span class="sxs-lookup"><span data-stu-id="e1549-941">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="e1549-942">Gestion correcte des autorisations des systèmes de fichiers réseau dans drvfs</span><span class="sxs-lookup"><span data-stu-id="e1549-942">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="e1549-943">Ajout de la prise en charge des lecteurs distants à drvfs</span><span class="sxs-lookup"><span data-stu-id="e1549-943">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="e1549-944">Activation de la prise en charge de FAT dans drvfs</span><span class="sxs-lookup"><span data-stu-id="e1549-944">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="e1549-945">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-945">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-946">Résultats LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-946">LTP Results</span></span>
<span data-ttu-id="e1549-947">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="e1549-947">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="e1549-948">Build 16170</span><span class="sxs-lookup"><span data-stu-id="e1549-948">Build 16170</span></span>

<span data-ttu-id="e1549-949">Pour obtenir des informations Windows d’ordre général sur la Build 16170, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-949">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="e1549-950">Nous avons publié un nouveau [billet de blog](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) sur nos efforts pour tester WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-950">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="e1549-951">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-951">Fixed</span></span>

- <span data-ttu-id="e1549-952">Prise en charge de l’option de socket IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="e1549-952">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="e1549-953">Ajout de la prise en charge de PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="e1549-953">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="e1549-954">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="e1549-954">[GH 1692]</span></span>
- <span data-ttu-id="e1549-955">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-955">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-956">Résultats LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-956">LTP Results</span></span>
<span data-ttu-id="e1549-957">Aucune modification depuis 15042</span><span class="sxs-lookup"><span data-stu-id="e1549-957">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="e1549-958">Build 15046 vers Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="e1549-958">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="e1549-959">Il n’y a plus de correctifs ou fonctionnalités WSL prévus pour être inclus dans Windows 10 Creators Update.</span><span class="sxs-lookup"><span data-stu-id="e1549-959">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="e1549-960">Les notes de publication pour WSL reprennent dans les semaines à venir pour les ajouts ciblant la prochaine mise à jour majeure de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-960">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="e1549-961">Pour obtenir des informations Windows d’ordre général sur la build 15046 et sur les futures versions Insider, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-961">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="e1549-962">Build 15042</span><span class="sxs-lookup"><span data-stu-id="e1549-962">Build 15042</span></span>

<span data-ttu-id="e1549-963">Pour obtenir des informations Windows d’ordre général sur la Build 15042, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-963">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-964">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-964">Fixed</span></span>

- <span data-ttu-id="e1549-965">Correction d’un blocage lors de la suppression d’un chemin se terminant par « .. »</span><span class="sxs-lookup"><span data-stu-id="e1549-965">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="e1549-966">Résolution d’un problème où FIONBIO ne retourne pas 0 en cas de réussite [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="e1549-966">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="e1549-967">Résolution du problème avec les lectures de longueur nulle des sockets de datagramme inet</span><span class="sxs-lookup"><span data-stu-id="e1549-967">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="e1549-968">Correction du blocage possible en raison d’une condition de concurrence dans une recherche drvfs inode [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="e1549-968">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="e1549-969">Prise en charge étendue des données auxiliaires de socket Unix ; SCM_CREDENTIALS et SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="e1549-969">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="e1549-970">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-970">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-971">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-971">LTP Results:</span></span>
<span data-ttu-id="e1549-972">Nombre de tests réussis : 737</span><span class="sxs-lookup"><span data-stu-id="e1549-972">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="e1549-973">Nombre de non-réussites (échec, ignoré, etc.) : 255</span><span class="sxs-lookup"><span data-stu-id="e1549-973">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="e1549-974">Build 15031</span><span class="sxs-lookup"><span data-stu-id="e1549-974">Build 15031</span></span>

<span data-ttu-id="e1549-975">Pour obtenir des informations Windows d’ordre général sur la Build 15031, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-975">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-976">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-976">Fixed</span></span>

- <span data-ttu-id="e1549-977">Correction d’un bogue où time(2) se comporte de façon sporadique.</span><span class="sxs-lookup"><span data-stu-id="e1549-977">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="e1549-978">Correction d’un problème où des syscalls \*SIGPROCMASK peuvent corrompre un masque de signal.</span><span class="sxs-lookup"><span data-stu-id="e1549-978">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="e1549-979">Retour à présent de la longueur de la ligne de commande complète dans la notification de création de processus WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-979">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="e1549-980">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="e1549-980">[GH 1632]</span></span>
- <span data-ttu-id="e1549-981">WSL signale désormais la sortie du thread par le biais de ptrace pour les blocages de GDB.</span><span class="sxs-lookup"><span data-stu-id="e1549-981">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="e1549-982">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="e1549-982">[GH 1196]</span></span>
- <span data-ttu-id="e1549-983">Correction du bogue où ptys se bloque suite à des E/S tmux lourdes.</span><span class="sxs-lookup"><span data-stu-id="e1549-983">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="e1549-984">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="e1549-984">[GH 1358]</span></span>
- <span data-ttu-id="e1549-985">Correction de la validation du délai d’expiration dans de nombreux appels système (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="e1549-985">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="e1549-986">Ajout de la prise en charge d’eventfd EFD_SEMAPHORE [GH 452]</span><span class="sxs-lookup"><span data-stu-id="e1549-986">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="e1549-987">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-987">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-988">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-988">LTP Results:</span></span>
<span data-ttu-id="e1549-989">Nombre de tests réussis : 737</span><span class="sxs-lookup"><span data-stu-id="e1549-989">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="e1549-990">Nombre de non-réussites (échec, ignoré, etc.) : 255</span><span class="sxs-lookup"><span data-stu-id="e1549-990">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="e1549-991">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-991">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="e1549-992">Build 15025</span><span class="sxs-lookup"><span data-stu-id="e1549-992">Build 15025</span></span>

<span data-ttu-id="e1549-993">Pour obtenir des informations Windows d’ordre général sur la Build 15025, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-993">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-994">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-994">Fixed</span></span>

- <span data-ttu-id="e1549-995">Correction du bogue à l’origine de la rupture de grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="e1549-995">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="e1549-996">Implémentation de l’indicateur EFD_SEMAPHORE pour eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="e1549-996">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="e1549-997">Implémentation de /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="e1549-997">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="e1549-998">Prise en charge des E/S pilotées par signal pour les sockets de flux Unix [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="e1549-998">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="e1549-999">Prise en charge de F_GETPIPE_SZ et F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="e1549-999">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="e1549-1000">Implémentation de recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="e1549-1000">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="e1549-1001">Correction du bogue où epoll_wait() n’attendait pas [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="e1549-1001">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="e1549-1002">Implémentation de /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="e1549-1002">Implement /proc/version_signature</span></span>
- <span data-ttu-id="e1549-1003">Tee syscall retourne désormais une erreur si les deux descripteurs de fichier font référence au même canal</span><span class="sxs-lookup"><span data-stu-id="e1549-1003">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="e1549-1004">Implémentation du comportement correct pour SO_PEERCRED pour les sockets Unix</span><span class="sxs-lookup"><span data-stu-id="e1549-1004">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="e1549-1005">Correction de la gestion du paramètre non valide tkill syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1005">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="e1549-1006">Modifications pour augmenter les performances de drvfs</span><span class="sxs-lookup"><span data-stu-id="e1549-1006">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="e1549-1007">Correctif mineur pour le blocage des E/S Ruby</span><span class="sxs-lookup"><span data-stu-id="e1549-1007">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="e1549-1008">Correction de recvmsg() qui retourne EINVAL pour l’indicateur MSG_DONTWAIT pour les sockets inet [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="e1549-1008">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="e1549-1009">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1009">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1010">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1010">LTP Results:</span></span>
<span data-ttu-id="e1549-1011">Nombre de tests réussis : 732</span><span class="sxs-lookup"><span data-stu-id="e1549-1011">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="e1549-1012">Nombre de non-réussites (échec, ignoré, etc.) : 255</span><span class="sxs-lookup"><span data-stu-id="e1549-1012">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="e1549-1013">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1013">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="e1549-1014">Build 15019</span><span class="sxs-lookup"><span data-stu-id="e1549-1014">Build 15019</span></span>

<span data-ttu-id="e1549-1015">Pour obtenir des informations Windows d’ordre général sur la Build 15019, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1015">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1016">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1016">Fixed</span></span>

- <span data-ttu-id="e1549-1017">Correction du bogue qui signalait incorrectement l’utilisation du procfs dans procfs pour des outils comme htop (GH 823, 945, 971)</span><span class="sxs-lookup"><span data-stu-id="e1549-1017">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="e1549-1018">Lors de l’appel de open() avec O_TRUNC sur un fichier existant, inotify génère désormais IN_MODIFY avant IN_OPEN</span><span class="sxs-lookup"><span data-stu-id="e1549-1018">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="e1549-1019">Correctifs du socket Unix getsockopt SO_ERROR pour activer postgres [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="e1549-1019">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="e1549-1020">Implémentation de /proc/sys/net/core/somaxconn pour le langage GO</span><span class="sxs-lookup"><span data-stu-id="e1549-1020">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="e1549-1021">La tâche en arrière-plan de mise à jour du package apt-get s’exécute désormais de façon masquée</span><span class="sxs-lookup"><span data-stu-id="e1549-1021">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="e1549-1022">Retrait de l’étendue pour IPv6 localhost (défaillance de Spring-Framework(Java)).</span><span class="sxs-lookup"><span data-stu-id="e1549-1022">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="e1549-1023">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1024">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1024">LTP Results:</span></span>
<span data-ttu-id="e1549-1025">Nombre de tests réussis : 714</span><span class="sxs-lookup"><span data-stu-id="e1549-1025">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="e1549-1026">Nombre de non-réussites (échec, ignoré, etc.) : 249</span><span class="sxs-lookup"><span data-stu-id="e1549-1026">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="e1549-1027">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="e1549-1028">Build 15014</span><span class="sxs-lookup"><span data-stu-id="e1549-1028">Build 15014</span></span>

<span data-ttu-id="e1549-1029">Pour obtenir des informations Windows d’ordre général sur la Build 15014, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="e1549-1029">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1030">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1030">Fixed</span></span>

- <span data-ttu-id="e1549-1031">Ctrl+C fonctionne à présent comme prévu</span><span class="sxs-lookup"><span data-stu-id="e1549-1031">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="e1549-1032">htop et ps auxw affichent désormais une utilisation correcte des ressources (GH #516)</span><span class="sxs-lookup"><span data-stu-id="e1549-1032">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="e1549-1033">Traduction de base des exceptions NT en signaux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1033">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="e1549-1034">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="e1549-1034">(GH #513)</span></span>
- <span data-ttu-id="e1549-1035">Échec de fallocate avec ENOSPC en cas d’espace insuffisant au lieu d’EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="e1549-1035">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="e1549-1036">Ajout de /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="e1549-1036">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="e1549-1037">Implémentation des appels système semop et semtimedop</span><span class="sxs-lookup"><span data-stu-id="e1549-1037">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="e1549-1038">Correction des erreurs nslookup avec l’option de socket IP_RECVTOS & IPV6_RECVTCLASS (GH 69)</span><span class="sxs-lookup"><span data-stu-id="e1549-1038">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="e1549-1039">Prise en charge des options de socket IP_RECVTTL et IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="e1549-1039">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="e1549-1040">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1040">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1041">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1041">LTP Results:</span></span>
<span data-ttu-id="e1549-1042">Nombre de tests réussis : 709</span><span class="sxs-lookup"><span data-stu-id="e1549-1042">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="e1549-1043">Nombre de non-réussites (échec, ignoré, etc.) : 255</span><span class="sxs-lookup"><span data-stu-id="e1549-1043">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="e1549-1044">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1044">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="e1549-1045">Résumé de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1045">Syscall Summary</span></span>
<span data-ttu-id="e1549-1046">Nombre total de syscalls : 384</span><span class="sxs-lookup"><span data-stu-id="e1549-1046">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="e1549-1047">Nombre total implémenté : 235</span><span class="sxs-lookup"><span data-stu-id="e1549-1047">Total Implemented: 235</span></span> </br>
<span data-ttu-id="e1549-1048">Nombre total de stubs : 22</span><span class="sxs-lookup"><span data-stu-id="e1549-1048">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="e1549-1049">Nombre total non implémenté : 127</span><span class="sxs-lookup"><span data-stu-id="e1549-1049">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="e1549-1050">Répartition détaillée</span><span class="sxs-lookup"><span data-stu-id="e1549-1050">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="e1549-1051">Build 15007</span><span class="sxs-lookup"><span data-stu-id="e1549-1051">Build 15007</span></span>

<span data-ttu-id="e1549-1052">Pour obtenir des informations Windows d’ordre général sur la Build 15007, visitez le [blog Windows]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="e1549-1052">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="e1549-1053">Problème connu</span><span class="sxs-lookup"><span data-stu-id="e1549-1053">Known Issue</span></span>

- <span data-ttu-id="e1549-1054">Il existe un bogue connu dans lequel la console ne reconnaît pas une entrée Ctrl+<key>.</span><span class="sxs-lookup"><span data-stu-id="e1549-1054">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="e1549-1055">Est concernée la commande Ctrl+C qui agit comme une touche « C » normale.</span><span class="sxs-lookup"><span data-stu-id="e1549-1055">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="e1549-1056">Solution : Mappez une autre touche à Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="e1549-1056">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="e1549-1057">Par exemple, pour mapper Ctrl+K à Ctrl+C, procédez comme suit : `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="e1549-1057">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="e1549-1058">Ce mappage s’effectue par terminal et doit être effectué à *chaque* lancement de bash.</span><span class="sxs-lookup"><span data-stu-id="e1549-1058">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="e1549-1059">Les utilisateurs peuvent explorer l’option permettant de l’inclure dans leur `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="e1549-1059">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="e1549-1060">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1060">Fixed</span></span>

- <span data-ttu-id="e1549-1061">Correction du problème où l’exécution de WSL consomme 100 % d’un cœur de processeur</span><span class="sxs-lookup"><span data-stu-id="e1549-1061">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="e1549-1062">Option de socket IP_PKTINFO, IPV6_RECVPKTINFO désormais prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1549-1062">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="e1549-1063">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="e1549-1063">(GH #851, 987)</span></span>
- <span data-ttu-id="e1549-1064">Adresse physique de l’interface réseau tronquée à 16 octets dans lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="e1549-1064">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="e1549-1065">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1065">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1066">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1066">LTP Results:</span></span>
<span data-ttu-id="e1549-1067">Nombre de tests réussis : 709</span><span class="sxs-lookup"><span data-stu-id="e1549-1067">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="e1549-1068">Nombre de non-réussites (échec, ignoré, etc.) : 255</span><span class="sxs-lookup"><span data-stu-id="e1549-1068">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="e1549-1069">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1069">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="e1549-1070">Build 15002</span><span class="sxs-lookup"><span data-stu-id="e1549-1070">Build 15002</span></span>

<span data-ttu-id="e1549-1071">Pour obtenir des informations Windows d’ordre général sur la Build 15002, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1071">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="e1549-1072">Problème connu</span><span class="sxs-lookup"><span data-stu-id="e1549-1072">Known Issue</span></span>

<span data-ttu-id="e1549-1073">Deux problèmes connus :</span><span class="sxs-lookup"><span data-stu-id="e1549-1073">Two known issues:</span></span>
- <span data-ttu-id="e1549-1074">Il existe un bogue connu dans lequel la console ne reconnaît pas une entrée Ctrl+<key>.</span><span class="sxs-lookup"><span data-stu-id="e1549-1074">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="e1549-1075">Est concernée la commande Ctrl+C qui agit comme une touche « C » normale.</span><span class="sxs-lookup"><span data-stu-id="e1549-1075">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="e1549-1076">Solution : Mappez une autre touche à Ctrl+C.</span><span class="sxs-lookup"><span data-stu-id="e1549-1076">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="e1549-1077">Par exemple, pour mapper Ctrl+K à Ctrl+C, procédez comme suit : `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="e1549-1077">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="e1549-1078">Ce mappage s’effectue par terminal et doit être effectué à *chaque* lancement de bash.</span><span class="sxs-lookup"><span data-stu-id="e1549-1078">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="e1549-1079">Les utilisateurs peuvent explorer l’option permettant de l’inclure dans leur `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="e1549-1079">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="e1549-1080">Pendant l’exécution de WSL, un thread système consomme 100 % d’un cœur de processeur.</span><span class="sxs-lookup"><span data-stu-id="e1549-1080">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="e1549-1081">La cause racine a été traitée et corrigée en interne.</span><span class="sxs-lookup"><span data-stu-id="e1549-1081">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="e1549-1082">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1082">Fixed</span></span>

- <span data-ttu-id="e1549-1083">Toutes les sessions bash doivent maintenant être créées au même niveau d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="e1549-1083">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="e1549-1084">Toute tentative de démarrage d’une session à un niveau différent est bloquée.</span><span class="sxs-lookup"><span data-stu-id="e1549-1084">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="e1549-1085">Cela signifie que les consoles administrateur et non-administrateur ne peuvent pas s’exécuter en même temps.</span><span class="sxs-lookup"><span data-stu-id="e1549-1085">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="e1549-1086">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="e1549-1086">(GH #626)</span></span>
<br/>
- <span data-ttu-id="e1549-1087">Implémentation des messages NETLINK_ROUTE suivants (nécessite l’administrateur Windows)</span><span class="sxs-lookup"><span data-stu-id="e1549-1087">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="e1549-1088">RTM_NEWADDR (prend en charge `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="e1549-1088">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="e1549-1089">RTM_NEWROUTE (prend en charge `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="e1549-1089">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="e1549-1090">RTM_DELADDR (prend en charge `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="e1549-1090">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="e1549-1091">RTM_DELROUTE (prend en charge `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="e1549-1091">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="e1549-1092">La vérification des tâches planifiées pour les packages à mettre à jour ne s’exécute plus sur une connexion limitée (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="e1549-1092">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="e1549-1093">Correction de l’erreur où la transmission est bloquée, c.-à-d. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="e1549-1093">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="e1549-1094">Implémentation de l’option de socket TCP_KEEPCNT (GH #843)</span><span class="sxs-lookup"><span data-stu-id="e1549-1094">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="e1549-1095">Implémentation de l’option de socket IP_MTU_DISCOVER INET (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="e1549-1095">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="e1549-1096">Suppression des fonctionnalités héritées pour exécuter des binaires NT à partir du lancement avec recherche de chemin NT.</span><span class="sxs-lookup"><span data-stu-id="e1549-1096">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="e1549-1097">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="e1549-1097">(GH #1325)</span></span>
- <span data-ttu-id="e1549-1098">Correction du mode de /dev/kmsg pour autoriser l’accès en lecture au groupe ou autre (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="e1549-1098">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="e1549-1099">Implémentation de /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="e1549-1099">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="e1549-1100">Correction de l’erreur dans laquelle l’heure de début du processus affichée était l’année 2432 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="e1549-1100">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="e1549-1101">Basculement de la variable d’environnement TERM par défaut vers xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="e1549-1101">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="e1549-1102">Modification de la façon dont la validation de processus est calculée pendant la duplication de processus.</span><span class="sxs-lookup"><span data-stu-id="e1549-1102">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="e1549-1103">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="e1549-1103">(GH #1286)</span></span>
- <span data-ttu-id="e1549-1104">Implémentation de /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="e1549-1104">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="e1549-1105">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="e1549-1105">(GH #1286)</span></span>
- <span data-ttu-id="e1549-1106">Implémentation du fichier /proc/net/route (GH #69)</span><span class="sxs-lookup"><span data-stu-id="e1549-1106">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="e1549-1107">Correction de l’erreur où le nom du raccourci n’est pas localisé correctement (GH #696)</span><span class="sxs-lookup"><span data-stu-id="e1549-1107">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="e1549-1108">Correction de la logique d’analyse elf qui valide incorrectement les en-têtes de programme devant être inférieurs (ou égaux) à PATH_MAX.</span><span class="sxs-lookup"><span data-stu-id="e1549-1108">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="e1549-1109">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="e1549-1109">(GH #1048)</span></span>
- <span data-ttu-id="e1549-1110">Implémentation du rappel statfs pour procfs, sysfs, cgroupfs et binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="e1549-1110">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="e1549-1111">Correction des fenêtres AptPackageIndexUpdate qui ne se ferment pas (GH #1184, également décrit dans GH #1193)</span><span class="sxs-lookup"><span data-stu-id="e1549-1111">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="e1549-1112">Ajout de la prise en charge de la personnalité ASLR ADDR_NO_RANDOMIZE.</span><span class="sxs-lookup"><span data-stu-id="e1549-1112">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="e1549-1113">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="e1549-1113">(GH #1148, 1128)</span></span>
- <span data-ttu-id="e1549-1114">Amélioration de PTRACE_GETSIGINFO, SIGSEGV, pour les arborescences des appels de procédure gdb appropriées pendant AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="e1549-1114">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="e1549-1115">L’analyse elf n’échoue plus pour les binaires patchelf.</span><span class="sxs-lookup"><span data-stu-id="e1549-1115">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="e1549-1116">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="e1549-1116">(GH #471)</span></span>
- <span data-ttu-id="e1549-1117">DNS VPN propagé à /etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="e1549-1117">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="e1549-1118">Améliorations apportées à la fermeture de TCP pour un transfert de données plus fiable.</span><span class="sxs-lookup"><span data-stu-id="e1549-1118">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="e1549-1119">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="e1549-1119">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="e1549-1120">Retour d’un code d’erreur correct quand un nombre de fichiers trop élevé sont ouverts (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="e1549-1120">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="e1549-1121">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="e1549-1121">(GH #1126, 2090)</span></span>
- <span data-ttu-id="e1549-1122">Le journal d’audit Windows signale désormais le nom de l’image dans le processus de création d’audit.</span><span class="sxs-lookup"><span data-stu-id="e1549-1122">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="e1549-1123">Échec de bonne grâce lors du lancement de bash.exe à partir d’une fenêtre bash</span><span class="sxs-lookup"><span data-stu-id="e1549-1123">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="e1549-1124">Ajout d’un message d’erreur quand interop n’est pas en mesure d’accéder à un répertoire de travail sous LxFs (c.-à-d. Bloc-notes.exe .bashrc)</span><span class="sxs-lookup"><span data-stu-id="e1549-1124">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="e1549-1125">Correction du problème de troncation du chemin Windows dans WSL</span><span class="sxs-lookup"><span data-stu-id="e1549-1125">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="e1549-1126">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1126">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1127">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1127">LTP Results:</span></span>
<span data-ttu-id="e1549-1128">Nombre de tests réussis : 690</span><span class="sxs-lookup"><span data-stu-id="e1549-1128">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="e1549-1129">Nombre de non-réussites (échec, ignoré, etc.) : 274</span><span class="sxs-lookup"><span data-stu-id="e1549-1129">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="e1549-1130">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1130">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1131">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1131">Syscall Support</span></span>
<span data-ttu-id="e1549-1132">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1132">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1133">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1133">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="e1549-1134">Build 14986</span><span class="sxs-lookup"><span data-stu-id="e1549-1134">Build 14986</span></span>

<span data-ttu-id="e1549-1135">Pour obtenir des informations Windows d’ordre général sur la build 14986, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1135">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1136">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1136">Fixed</span></span>

- <span data-ttu-id="e1549-1137">Correction des vérifications d’erreurs avec des IOCTL Netlink et Pty</span><span class="sxs-lookup"><span data-stu-id="e1549-1137">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="e1549-1138">La version du noyau signale maintenant 4.4.0-43 à des fins de cohérence avec Xenial</span><span class="sxs-lookup"><span data-stu-id="e1549-1138">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="e1549-1139">Bash.exe se lance maintenant quand l’entrée est dirigée vers « nul: » (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="e1549-1139">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="e1549-1140">Les ID de thread sont désormais signalés correctement dans procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="e1549-1140">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="e1549-1141">Les indicateurs IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR sont désormais pris en charge dans inotify_add_watch() (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="e1549-1141">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="e1549-1142">Implémentation de timer_create et des appels système associés.</span><span class="sxs-lookup"><span data-stu-id="e1549-1142">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="e1549-1143">Cela permet la prise en charge de GHC (GH #307)</span><span class="sxs-lookup"><span data-stu-id="e1549-1143">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="e1549-1144">Correction du problème où ping retourne une heure de 0.000ms (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="e1549-1144">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="e1549-1145">Retour d’un code d’erreur correct quand un nombre de fichiers trop élevé sont ouverts.</span><span class="sxs-lookup"><span data-stu-id="e1549-1145">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="e1549-1146">Résolution d’un problème dans WSL où la demande Netlink de données d’interface réseau échoue avec EINVAL si l’adresse matérielle de l’interface correspond à 32 octets (comme l’interface Teredo)</span><span class="sxs-lookup"><span data-stu-id="e1549-1146">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="e1549-1147">Notez que l’utilitaire « ip » Linux contient un bogue qui entraîne un incident si WSL signale une adresse matérielle à 32 octets.</span><span class="sxs-lookup"><span data-stu-id="e1549-1147">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="e1549-1148">Il s’agit d’un bogue dans « ip », et non WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1148">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="e1549-1149">L’utilitaire « ip » code en dur la longueur du tampon de chaîne utilisé pour imprimer l’adresse matérielle et ce tampon est trop petit pour imprimer une adresse matérielle à 32 octets.</span><span class="sxs-lookup"><span data-stu-id="e1549-1149">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="e1549-1150">Correctifs et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1150">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1151">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1151">LTP Results:</span></span>
<span data-ttu-id="e1549-1152">Nombre de tests réussis : 669</span><span class="sxs-lookup"><span data-stu-id="e1549-1152">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="e1549-1153">Nombre de non-réussites (échec, ignoré, etc.) : 258</span><span class="sxs-lookup"><span data-stu-id="e1549-1153">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="e1549-1154">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1154">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1155">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1155">Syscall Support</span></span>
<span data-ttu-id="e1549-1156">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1156">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1157">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1157">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="e1549-1158">Build 14971</span><span class="sxs-lookup"><span data-stu-id="e1549-1158">Build 14971</span></span>

<span data-ttu-id="e1549-1159">Pour obtenir des informations Windows d’ordre général sur la build 14971, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1159">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1160">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1160">Fixed</span></span>

 - <span data-ttu-id="e1549-1161">En raison de circonstances hors de notre contrôle, il n’existe aucune mise à jour dans cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1161">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="e1549-1162">Les mises à jour planifiées régulièrement reprennent à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="e1549-1162">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1163">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1163">LTP Results:</span></span>
<span data-ttu-id="e1549-1164">Inchangés par rapport à 14965</span><span class="sxs-lookup"><span data-stu-id="e1549-1164">Unchanged from 14965</span></span> </br>
<span data-ttu-id="e1549-1165">Nombre de tests réussis : 664</span><span class="sxs-lookup"><span data-stu-id="e1549-1165">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="e1549-1166">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1167">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="e1549-1168">Build 14965</span><span class="sxs-lookup"><span data-stu-id="e1549-1168">Build 14965</span></span>

<span data-ttu-id="e1549-1169">Pour obtenir des informations Windows d’ordre général sur la build 14965, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1169">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1170">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1170">Fixed</span></span>

- <span data-ttu-id="e1549-1171">Prise en charge des sockets Netlink RTM_GETLINK et RTM_GETADDR du protocole NETLINK_ROUTE (GH #468)</span><span class="sxs-lookup"><span data-stu-id="e1549-1171">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="e1549-1172">Activation des commandes ifconfig et ip pour l’énumération réseau</span><span class="sxs-lookup"><span data-stu-id="e1549-1172">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="e1549-1173">Pour plus d’informations, consultez notre [billet de blog sur la mise en réseau WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1173">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="e1549-1174">/sbin est désormais dans le chemin de l’utilisateur par défaut</span><span class="sxs-lookup"><span data-stu-id="e1549-1174">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="e1549-1175">Le chemin de l’utilisateur NT est maintenant ajouté au chemin WSL par défaut (par exemple, vous pouvez maintenant taper Bloc-notes.exe sans ajouter System32 au chemin Linux)</span><span class="sxs-lookup"><span data-stu-id="e1549-1175">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="e1549-1176">Ajout de la prise en charge de /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="e1549-1176">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="e1549-1177">Les binaires NT peuvent maintenant être lancés à partir de WSL quand le répertoire de travail actuel contient des caractères non-ANSI (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="e1549-1177">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="e1549-1178">Autorisation de l’arrêt sur le socket de flux Unix déconnecté.</span><span class="sxs-lookup"><span data-stu-id="e1549-1178">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="e1549-1179">Ajout de la prise en charge de PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="e1549-1179">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="e1549-1180">Ajout de la prise en charge de CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="e1549-1180">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="e1549-1181">Correction de l’erreur où la transmission est bloquée, c.-à-d. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="e1549-1181">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="e1549-1182">Gestion des requêtes de connexion au terminal actuel.</span><span class="sxs-lookup"><span data-stu-id="e1549-1182">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="e1549-1183">Marquage de /proc/<pid>/oom_score_adj as writable.</span><span class="sxs-lookup"><span data-stu-id="e1549-1183">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="e1549-1184">Ajout du dossier /sys/fs/cgroup.</span><span class="sxs-lookup"><span data-stu-id="e1549-1184">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="e1549-1185">sched_setaffinity doit retourner le maque du nombre de bits d’affinité</span><span class="sxs-lookup"><span data-stu-id="e1549-1185">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="e1549-1186">Correction de la logique de validation ELF qui suppose à tors que les chemins de l’interpréteur ne doivent pas comprendre plus de 64 caractères.</span><span class="sxs-lookup"><span data-stu-id="e1549-1186">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="e1549-1187">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="e1549-1187">(GH #743)</span></span>
- <span data-ttu-id="e1549-1188">Les descripteurs de fichiers ouverts peuvent maintenir la fenêtre de console ouverte (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="e1549-1188">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="e1549-1189">Correction d’une erreur liée à l’échec de rename() avec une barre oblique de fin sur le nom cible (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="e1549-1189">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="e1549-1190">Implémentation du fichier /proc/net/dev</span><span class="sxs-lookup"><span data-stu-id="e1549-1190">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="e1549-1191">Correction de commandes ping 0.000ms dues à la résolution du minuteur.</span><span class="sxs-lookup"><span data-stu-id="e1549-1191">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="e1549-1192">Implémentation de /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="e1549-1192">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="e1549-1193">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1193">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1194">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1194">LTP Results:</span></span>
<span data-ttu-id="e1549-1195">Nombre de tests réussis : 664</span><span class="sxs-lookup"><span data-stu-id="e1549-1195">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="e1549-1196">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1196">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1197">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1197">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="e1549-1198">Build 14959</span><span class="sxs-lookup"><span data-stu-id="e1549-1198">Build 14959</span></span>

<span data-ttu-id="e1549-1199">Pour obtenir des informations Windows d’ordre général sur la build 14959, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="e1549-1199">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1200">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1200">Fixed</span></span>

- <span data-ttu-id="e1549-1201">Notification de processus Pico améliorée pour Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-1201">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="e1549-1202">Informations supplémentaires disponibles sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1202">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="e1549-1203">Amélioration de la stabilité avec l’interopérabilité Windows</span><span class="sxs-lookup"><span data-stu-id="e1549-1203">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="e1549-1204">Correction de l’erreur 0x80070057 lors du lancement de bash.exe quand la protection des données d’entreprise (PDE) est activée</span><span class="sxs-lookup"><span data-stu-id="e1549-1204">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="e1549-1205">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1205">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1206">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1206">LTP Results:</span></span>
<span data-ttu-id="e1549-1207">Nombre de tests réussis : 665</span><span class="sxs-lookup"><span data-stu-id="e1549-1207">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="e1549-1208">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1208">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1209">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1209">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="e1549-1210">Build 14955</span><span class="sxs-lookup"><span data-stu-id="e1549-1210">Build 14955</span></span>

<span data-ttu-id="e1549-1211">Pour obtenir des informations Windows d’ordre général sur la build 14955, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="e1549-1211">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1212">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1212">Fixed</span></span>

 - <span data-ttu-id="e1549-1213">En raison de circonstances hors de notre contrôle, il n’existe aucune mise à jour dans cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1213">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="e1549-1214">Les mises à jour planifiées régulièrement reprennent à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="e1549-1214">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1215">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1215">LTP Results:</span></span>
<span data-ttu-id="e1549-1216">Nombre de tests réussis : 665</span><span class="sxs-lookup"><span data-stu-id="e1549-1216">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="e1549-1217">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1217">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1218">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1218">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="e1549-1219">Build 14951</span><span class="sxs-lookup"><span data-stu-id="e1549-1219">Build 14951</span></span>

<span data-ttu-id="e1549-1220">Pour obtenir des informations Windows d’ordre général sur la build 14951, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1220">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="e1549-1221">Nouvelle fonctionnalité : Interopérabilité Windows/Ubuntu</span><span class="sxs-lookup"><span data-stu-id="e1549-1221">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="e1549-1222">Les binaires Windows peuvent désormais être appelés directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1222">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="e1549-1223">Cela permet aux utilisateurs d’interagir avec leurs environnement et système Windows d’une manière qui n’était auparavant pas possible.</span><span class="sxs-lookup"><span data-stu-id="e1549-1223">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="e1549-1224">En guise d’exemple rapide, il est maintenant possible pour les utilisateurs d’exécuter les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="e1549-1224">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="e1549-1225">D’autres informations sont disponibles ici :</span><span class="sxs-lookup"><span data-stu-id="e1549-1225">More information can be found at:</span></span>

- [<span data-ttu-id="e1549-1226">Blog de l’équipe WSL pour Interop</span><span class="sxs-lookup"><span data-stu-id="e1549-1226">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="e1549-1227">Documentation MSDN Interop</span><span class="sxs-lookup"><span data-stu-id="e1549-1227">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1228">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1228">Fixed</span></span>

- <span data-ttu-id="e1549-1229">Ubuntu 16.04 (Xenial) est maintenant installé pour toutes les nouvelles instances WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1229">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="e1549-1230">Les utilisateurs avec des instances 14.04 (Trusty) existantes ne sont pas automatiquement mis à niveau.</span><span class="sxs-lookup"><span data-stu-id="e1549-1230">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="e1549-1231">Les paramètres régionaux définis lors de l’installation s’affichent désormais</span><span class="sxs-lookup"><span data-stu-id="e1549-1231">Locale set during install is now displayed</span></span>
- <span data-ttu-id="e1549-1232">Améliorations apportées au terminal, notamment correction du bogue lié à la redirection d’un processus WSL vers un fichier</span><span class="sxs-lookup"><span data-stu-id="e1549-1232">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="e1549-1233">La durée de vie de la console doit être liée à celle de bash.exe</span><span class="sxs-lookup"><span data-stu-id="e1549-1233">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="e1549-1234">La taille de la fenêtre de console doit utiliser la taille visible, pas la taille du tampon</span><span class="sxs-lookup"><span data-stu-id="e1549-1234">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="e1549-1235">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1235">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1236">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1236">LTP Results:</span></span>
<span data-ttu-id="e1549-1237">Nombre de tests réussis : 665</span><span class="sxs-lookup"><span data-stu-id="e1549-1237">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="e1549-1238">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1238">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1239">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1239">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="e1549-1240">Build 14946</span><span class="sxs-lookup"><span data-stu-id="e1549-1240">Build 14946</span></span>

<span data-ttu-id="e1549-1241">Pour obtenir des informations Windows d’ordre général sur la build 14946, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="e1549-1241">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1242">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1242">Fixed</span></span>

- <span data-ttu-id="e1549-1243">Correction d’un problème qui empêchait la création de comptes d’utilisateur WSL pour les utilisateurs avec des noms d’utilisateur NT contenant des espaces ou des guillemets.</span><span class="sxs-lookup"><span data-stu-id="e1549-1243">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="e1549-1244">Modification de VolFs et DrvFs pour retourner 0 pour le nombre de liens du répertoire dans stat</span><span class="sxs-lookup"><span data-stu-id="e1549-1244">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="e1549-1245">Prise en charge de l’option de socket IPV6_MULTICAST_HOPS.</span><span class="sxs-lookup"><span data-stu-id="e1549-1245">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="e1549-1246">Limitation à une seule boucle d’E/S de console par tty.</span><span class="sxs-lookup"><span data-stu-id="e1549-1246">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="e1549-1247">Par exemple, la commande suivante est possible :</span><span class="sxs-lookup"><span data-stu-id="e1549-1247">Example: the following command is possible:</span></span>
  - <span data-ttu-id="e1549-1248">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="e1549-1248">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="e1549-1249">Remplacement des espaces par des tabulations dans /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="e1549-1249">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="e1549-1250">DrvFs apparaît maintenant dans mountinfo avec un nom qui correspond au volume Windows monté</span><span class="sxs-lookup"><span data-stu-id="e1549-1250">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="e1549-1251">/home et /root apparaissent désormais dans mountinfo avec des noms corrects</span><span class="sxs-lookup"><span data-stu-id="e1549-1251">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="e1549-1252">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1252">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1253">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1253">LTP Results:</span></span>
<span data-ttu-id="e1549-1254">Nombre de tests réussis : 665</span><span class="sxs-lookup"><span data-stu-id="e1549-1254">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="e1549-1255">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1255">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1256">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1256">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="e1549-1257">Build 14942</span><span class="sxs-lookup"><span data-stu-id="e1549-1257">Build 14942</span></span>

<span data-ttu-id="e1549-1258">Pour obtenir des informations Windows d’ordre général sur la build 14942, visitez le [blog Windows](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="e1549-1258">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1259">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1259">Fixed</span></span>

- <span data-ttu-id="e1549-1260">Traitement de plusieurs vérifications de bogues, notamment l’incident de la mise en réseau « ATTEMPTED EXECUTE OF NOEXECUTE MEMORY » qui bloque SSH</span><span class="sxs-lookup"><span data-stu-id="e1549-1260">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="e1549-1261">Prise en charge d’inotifiy pour les notifications générées à partir d’applications Windows sur DrvFs</span><span class="sxs-lookup"><span data-stu-id="e1549-1261">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="e1549-1262">Implémentation de TCP_KEEPIDLE et TCP_KEEPINTVL pour mongod.</span><span class="sxs-lookup"><span data-stu-id="e1549-1262">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="e1549-1263">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="e1549-1263">(GH #695)</span></span>
- <span data-ttu-id="e1549-1264">Implémentation de l’appel système pivot_root</span><span class="sxs-lookup"><span data-stu-id="e1549-1264">Implement the pivot_root system call</span></span>
- <span data-ttu-id="e1549-1265">Implémentation de l’option de socket pour SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="e1549-1265">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="e1549-1266">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1266">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="e1549-1267">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1267">LTP Results:</span></span>
<span data-ttu-id="e1549-1268">Nombre de tests réussis : 665</span><span class="sxs-lookup"><span data-stu-id="e1549-1268">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="e1549-1269">Nombre de non-réussites (échec, ignoré, etc.) : 263</span><span class="sxs-lookup"><span data-stu-id="e1549-1269">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="e1549-1270">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1270">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1271">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1271">Syscall Support</span></span>
<span data-ttu-id="e1549-1272">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1272">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1273">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1273">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="e1549-1274">Build 14936</span><span class="sxs-lookup"><span data-stu-id="e1549-1274">Build 14936</span></span>

<span data-ttu-id="e1549-1275">Pour obtenir des informations Windows d’ordre général sur la build 14936, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1275">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="e1549-1276">Remarque : WSL va installer Ubuntu version 16.04 (Xenial) au lieu d’Ubuntu 14.04 (Trusty) dans une prochaine version.</span><span class="sxs-lookup"><span data-stu-id="e1549-1276">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="e1549-1277">Cette modification s’appliquera aux versions Insiders qui installent de nouvelles instances (lxrun.exe /install ou première exécution de bash.exe).</span><span class="sxs-lookup"><span data-stu-id="e1549-1277">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="e1549-1278">Les instances existantes avec Trusty ne sont pas mises à niveau automatiquement.</span><span class="sxs-lookup"><span data-stu-id="e1549-1278">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="e1549-1279">Les utilisateurs peuvent mettre à niveau leur image Trusty vers Xenial à l’aide de la commande do-release-upgrade.</span><span class="sxs-lookup"><span data-stu-id="e1549-1279">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="e1549-1280">Problème connu</span><span class="sxs-lookup"><span data-stu-id="e1549-1280">Known Issue</span></span>
<span data-ttu-id="e1549-1281">WSL rencontre un problème avec certaines implémentations de sockets.</span><span class="sxs-lookup"><span data-stu-id="e1549-1281">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="e1549-1282">La vérification de bogue se manifeste comme un incident avec l’erreur « ATTEMPTED EXECUTE OF NOEXECUTE MEMORY ».</span><span class="sxs-lookup"><span data-stu-id="e1549-1282">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="e1549-1283">La manifestation la plus courante de ce problème est un incident lors de l’utilisation de ssh.</span><span class="sxs-lookup"><span data-stu-id="e1549-1283">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="e1549-1284">La cause racine est résolue sur les builds internes et envoyée (push) aux versions Insiders dès que possible.</span><span class="sxs-lookup"><span data-stu-id="e1549-1284">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="e1549-1285">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1285">Fixed</span></span>

- <span data-ttu-id="e1549-1286">Implémentation de l’appel système chroot</span><span class="sxs-lookup"><span data-stu-id="e1549-1286">Implemented the chroot system call</span></span>
- <span data-ttu-id="e1549-1287">Améliorations apportées à inotify, ~~notamment la prise en charge des notifications générées à partir d’applications Windows sur DrvFs~~</span><span class="sxs-lookup"><span data-stu-id="e1549-1287">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="e1549-1288">Correction : Prise en charge d’inotify pour les modifications provenant d’applications Windows non disponibles pour le moment.</span><span class="sxs-lookup"><span data-stu-id="e1549-1288">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="e1549-1289">La liaison de socket à IPV6::<port n> prend désormais en charge IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="e1549-1289">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="e1549-1290">Implémentation du comportement WNOWAIT pour l’appel système waitid (GH #638)</span><span class="sxs-lookup"><span data-stu-id="e1549-1290">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="e1549-1291">Prise en charge des options de socket IP IP_HDRINCL et IP_TTL</span><span class="sxs-lookup"><span data-stu-id="e1549-1291">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="e1549-1292">Retour immédiat de read() de longueur nulle (GH #975)</span><span class="sxs-lookup"><span data-stu-id="e1549-1292">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="e1549-1293">Gestion correcte des noms de fichiers et des préfixes de noms de fichiers qui n’incluent pas de marque de fin NULL dans un fichier .tar.</span><span class="sxs-lookup"><span data-stu-id="e1549-1293">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="e1549-1294">Prise en charge d’epoll pour /dev/null</span><span class="sxs-lookup"><span data-stu-id="e1549-1294">epoll support for /dev/null</span></span>
- <span data-ttu-id="e1549-1295">Correction de la source de temps /dev/alarm</span><span class="sxs-lookup"><span data-stu-id="e1549-1295">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="e1549-1296">Capacité de Bash -c à effectuer une redirection vers un fichier</span><span class="sxs-lookup"><span data-stu-id="e1549-1296">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="e1549-1297">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1297">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1298">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1298">LTP Results:</span></span>
<span data-ttu-id="e1549-1299">Nombre de tests réussis : 664</span><span class="sxs-lookup"><span data-stu-id="e1549-1299">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="e1549-1300">Nombre de non-réussites (échec, ignoré, etc.) : 264</span><span class="sxs-lookup"><span data-stu-id="e1549-1300">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="e1549-1301">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1301">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1302">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1302">Syscall Support</span></span>
<span data-ttu-id="e1549-1303">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1303">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1304">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1304">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="e1549-1305">Build 14931</span><span class="sxs-lookup"><span data-stu-id="e1549-1305">Build 14931</span></span>

<span data-ttu-id="e1549-1306">Pour obtenir des informations Windows d’ordre général sur la build 14931, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1306">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1307">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1307">Fixed</span></span>

 - <span data-ttu-id="e1549-1308">En raison de circonstances hors de notre contrôle, il n’existe aucune mise à jour dans cette build pour le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1308">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="e1549-1309">Les mises à jour planifiées régulièrement reprennent à la prochaine version.</span><span class="sxs-lookup"><span data-stu-id="e1549-1309">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="e1549-1310">Build 14926</span><span class="sxs-lookup"><span data-stu-id="e1549-1310">Build 14926</span></span>

<span data-ttu-id="e1549-1311">Pour obtenir des informations Windows d’ordre général sur la build 14926, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1311">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1312">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1312">Fixed</span></span>

- <span data-ttu-id="e1549-1313">Ping fonctionne désormais dans les consoles qui ne disposent pas de privilèges administrateur</span><span class="sxs-lookup"><span data-stu-id="e1549-1313">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="e1549-1314">Ping6 désormais pris en charge, également sans privilèges administrateur</span><span class="sxs-lookup"><span data-stu-id="e1549-1314">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="e1549-1315">Prise en charge par inotify des fichiers modifiés par le biais de WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1315">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="e1549-1316">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="e1549-1316">(GH #216)</span></span>
  - <span data-ttu-id="e1549-1317">Indicateurs pris en charge :</span><span class="sxs-lookup"><span data-stu-id="e1549-1317">Flags supported:</span></span>
    - <span data-ttu-id="e1549-1318">inotify_init1 : LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="e1549-1318">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="e1549-1319">Événements inotify_add_watch : LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="e1549-1319">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="e1549-1320">Attributs inotify_add_watch : LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="e1549-1320">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="e1549-1321">Sortie de lecture : LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="e1549-1321">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="e1549-1322">Problème connu : La modification de fichiers à partir d’applications Windows ne génère pas d’événements</span><span class="sxs-lookup"><span data-stu-id="e1549-1322">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="e1549-1323">Le socket Unix prend désormais en charge SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="e1549-1323">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="e1549-1324">Résultats LTP :</span><span class="sxs-lookup"><span data-stu-id="e1549-1324">LTP Results:</span></span>
<span data-ttu-id="e1549-1325">Nombre de tests réussis : 651</span><span class="sxs-lookup"><span data-stu-id="e1549-1325">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="e1549-1326">Nombre de non-réussites (échec, ignoré, etc.) : 258</span><span class="sxs-lookup"><span data-stu-id="e1549-1326">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="e1549-1327">Journaux de la série de tests LTP</span><span class="sxs-lookup"><span data-stu-id="e1549-1327">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="e1549-1328">Build 14915</span><span class="sxs-lookup"><span data-stu-id="e1549-1328">Build 14915</span></span>

<span data-ttu-id="e1549-1329">Pour obtenir des informations Windows d’ordre général sur la build 14915, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="e1549-1329">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1330">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1330">Fixed</span></span>
-  <span data-ttu-id="e1549-1331">Paire de sockets pour les sockets de datagramme Unix (GH #262)</span><span class="sxs-lookup"><span data-stu-id="e1549-1331">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="e1549-1332">Prise en charge des sockets Unix pour SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="e1549-1332">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="e1549-1333">Prise en charge des sockets UNIX pour SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="e1549-1333">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="e1549-1334">Prise en charge des sockets Unix pour SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="e1549-1334">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="e1549-1335">Ajout de la prise en charge de l’envoi, de la réception et de l’arrêt des sockets de datagramme Unix</span><span class="sxs-lookup"><span data-stu-id="e1549-1335">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="e1549-1336">Correction de la vérification de bogue due à une validation de paramètre mmap non valide pour les adresses non fixes.</span><span class="sxs-lookup"><span data-stu-id="e1549-1336">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="e1549-1337">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="e1549-1337">(GH #847)</span></span>
- <span data-ttu-id="e1549-1338">Prise en charge de l’interruption/la reprise des états des terminaux</span><span class="sxs-lookup"><span data-stu-id="e1549-1338">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="e1549-1339">Prise en charge de l’IOCTL TIOCPKT pour débloquer l’utilitaire Screen (GH #774)</span><span class="sxs-lookup"><span data-stu-id="e1549-1339">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="e1549-1340">Problème connu : Clés de fonction non opérationnelles</span><span class="sxs-lookup"><span data-stu-id="e1549-1340">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="e1549-1341">Correction d’une concurrence dans TimerFd qui peut provoquer l’accès à un membre libéré « ReaderReady » par LxpTimerFdWorkerRoutine (GH #814)</span><span class="sxs-lookup"><span data-stu-id="e1549-1341">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="e1549-1342">Activation de la prise en charge des appels système redémarrables pour futex, poll et clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="e1549-1342">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="e1549-1343">Ajout de la prise en charge du montage de liaison</span><span class="sxs-lookup"><span data-stu-id="e1549-1343">Added bind mount support</span></span>
- <span data-ttu-id="e1549-1344">Prise en charge de l’annulation du partage des espaces de noms de montage</span><span class="sxs-lookup"><span data-stu-id="e1549-1344">unshare for mount namespace support</span></span>
    - <span data-ttu-id="e1549-1345">Problème connu : Quand vous créez un espace de noms de montage avec `unshare(CLONE_NEWNS)`, le répertoire de travail actuel continue de pointer vers l’ancien espace de noms</span><span class="sxs-lookup"><span data-stu-id="e1549-1345">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="e1549-1346">Améliorations et correctifs de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1346">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="e1549-1347">Build 14905</span><span class="sxs-lookup"><span data-stu-id="e1549-1347">Build 14905</span></span>

<span data-ttu-id="e1549-1348">Pour obtenir des informations Windows d’ordre général sur la build 14905, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1348">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1349">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1349">Fixed</span></span>
- <span data-ttu-id="e1549-1350">Prise en charge des appels système redémarrables (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="e1549-1350">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="e1549-1351">Les liens symboliques vers des répertoires se terminant par / sont maintenant opérationnels (GH #650)</span><span class="sxs-lookup"><span data-stu-id="e1549-1351">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="e1549-1352">Implémentation de la commande IOCTL RNDGETENTCNT pour /dev/random</span><span class="sxs-lookup"><span data-stu-id="e1549-1352">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="e1549-1353">Implémentation des fichiers /proc/[pid]/mounts, /proc/[pid]/mountinfo et /proc/[pid]/mountstats</span><span class="sxs-lookup"><span data-stu-id="e1549-1353">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="e1549-1354">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1354">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="e1549-1355">Build 14901</span><span class="sxs-lookup"><span data-stu-id="e1549-1355">Build 14901</span></span>
<span data-ttu-id="e1549-1356">Première build Insider pour la version ultérieure à la mise à jour anniversaire Windows 10.</span><span class="sxs-lookup"><span data-stu-id="e1549-1356">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="e1549-1357">Pour obtenir des informations Windows d’ordre général sur la build 14901, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1357">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1358">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1358">Fixed</span></span>
- <span data-ttu-id="e1549-1359">Correction du problème lié à la barre oblique de fin</span><span class="sxs-lookup"><span data-stu-id="e1549-1359">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="e1549-1360">Les commandes comme `$ mv a/c/ a/b/` fonctionnent à présent</span><span class="sxs-lookup"><span data-stu-id="e1549-1360">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="e1549-1361">L’installation demande à présent si les paramètres régionaux Ubuntu doivent être définis sur les paramètres régionaux Windows</span><span class="sxs-lookup"><span data-stu-id="e1549-1361">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="e1549-1362">Prise en charge de procfs pour le dossier ns</span><span class="sxs-lookup"><span data-stu-id="e1549-1362">Procfs support for ns folder</span></span>
- <span data-ttu-id="e1549-1363">Ajout du montage et démontage pour les systèmes de fichiers tmpfs, procfs et sysfs</span><span class="sxs-lookup"><span data-stu-id="e1549-1363">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="e1549-1364">Correction de la signature ABI 32 bits de mknod[at]</span><span class="sxs-lookup"><span data-stu-id="e1549-1364">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="e1549-1365">Déplacement des sockets Unix vers le modèle de distribution</span><span class="sxs-lookup"><span data-stu-id="e1549-1365">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="e1549-1366">La taille du tampon de réception des sockets INET définie à l’aide de setsockopt doit être respectée</span><span class="sxs-lookup"><span data-stu-id="e1549-1366">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="e1549-1367">Implémentation de l’indicateur de message de réception de socket Unix MSG_CMSG_CLOEXEC</span><span class="sxs-lookup"><span data-stu-id="e1549-1367">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="e1549-1368">Redirection des canaux stdin/stdout de processus Linux (GH #2)</span><span class="sxs-lookup"><span data-stu-id="e1549-1368">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="e1549-1369">Autorisation de la transmission de commandes bash -c dans CMD.</span><span class="sxs-lookup"><span data-stu-id="e1549-1369">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="e1549-1370">Exemple : >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="e1549-1370">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="e1549-1371">Bash peut maintenant être installé sur des systèmes avec plusieurs fichiers d’échange (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="e1549-1371">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="e1549-1372">La taille du tampon des sockets INET par défaut doit correspondre à celle du programme d’installation Ubuntu par défaut</span><span class="sxs-lookup"><span data-stu-id="e1549-1372">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="e1549-1373">Alignement des syscalls xattr sur listxattr</span><span class="sxs-lookup"><span data-stu-id="e1549-1373">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="e1549-1374">Retour des interfaces avec une adresse IPv4 valide uniquement depuis SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="e1549-1374">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="e1549-1375">Correction de l’action par défaut du signal quant elle est injectée par ptrace</span><span class="sxs-lookup"><span data-stu-id="e1549-1375">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="e1549-1376">Implémentation de /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="e1549-1376">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="e1549-1377">Utilisation des valeurs de Registre du contexte d’ordinateur lors de la restauration du contexte dans sigreturn</span><span class="sxs-lookup"><span data-stu-id="e1549-1377">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="e1549-1378">Le problème de blocage de java et javac est ainsi résolu pour certains utilisateurs</span><span class="sxs-lookup"><span data-stu-id="e1549-1378">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="e1549-1379">Implémentation de /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="e1549-1379">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1380">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1380">Syscall Support</span></span>
<span data-ttu-id="e1549-1381">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1381">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1382">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1382">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="e1549-1383">Build 14388 vers Mise à jour anniversaire Windows 10</span><span class="sxs-lookup"><span data-stu-id="e1549-1383">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="e1549-1384">Pour obtenir des informations Windows d’ordre général sur la build 14388, visitez le [blog Windows](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="e1549-1384">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1385">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1385">Fixed</span></span>
- <span data-ttu-id="e1549-1386">Correctifs pour préparer la mise à jour anniversaire Windows 10 du 2 août</span><span class="sxs-lookup"><span data-stu-id="e1549-1386">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="e1549-1387">Pour plus d’informations sur WSL dans la mise à jour anniversaire, consultez notre [blog](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="e1549-1387">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="e1549-1388">Build 14376</span><span class="sxs-lookup"><span data-stu-id="e1549-1388">Build 14376</span></span>
<span data-ttu-id="e1549-1389">Pour obtenir des informations Windows d’ordre général sur la build 14376, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1389">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1390">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1390">Fixed</span></span>
- <span data-ttu-id="e1549-1391">Suppression de certaines instances où apt-get se bloque (GH #493)</span><span class="sxs-lookup"><span data-stu-id="e1549-1391">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="e1549-1392">Résolution d’un problème lié à une gestion incorrecte des montages vides</span><span class="sxs-lookup"><span data-stu-id="e1549-1392">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="e1549-1393">Correction d’un problème lié au montage incorrect des RAMDISK</span><span class="sxs-lookup"><span data-stu-id="e1549-1393">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="e1549-1394">Modification de l’acceptation des sockets UNIX pour prendre en charge les indicateurs (GH #451 partiel)</span><span class="sxs-lookup"><span data-stu-id="e1549-1394">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="e1549-1395">Correction de l’écran bleu lié au réseau commun</span><span class="sxs-lookup"><span data-stu-id="e1549-1395">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="e1549-1396">Correction de l’écran bleu lors de l’accès à /proc/[pid]/task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="e1549-1396">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="e1549-1397">Correction de l’utilisation élevée du processeur pour certains scénarios pty (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="e1549-1397">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="e1549-1398">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1398">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="e1549-1399">Build 14371</span><span class="sxs-lookup"><span data-stu-id="e1549-1399">Build 14371</span></span>
<span data-ttu-id="e1549-1400">Pour obtenir des informations Windows d’ordre général sur la build 14371, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1400">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1401">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1401">Fixed</span></span>
- <span data-ttu-id="e1549-1402">Correction de la concurrence de timing avec SIGCHLD et wait() lors de l’utilisation de ptrace</span><span class="sxs-lookup"><span data-stu-id="e1549-1402">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="e1549-1403">Correction de certains comportements quand les chemins se terminent par une barre oblique / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="e1549-1403">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="e1549-1404">Résolution du problème lié à l’échec du renommage/de l’annulation de lien en raison de handles ouverts vers des enfants</span><span class="sxs-lookup"><span data-stu-id="e1549-1404">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="e1549-1405">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1405">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="e1549-1406">Build 14366</span><span class="sxs-lookup"><span data-stu-id="e1549-1406">Build 14366</span></span>
<span data-ttu-id="e1549-1407">Pour obtenir des informations Windows d’ordre général sur la build 14366, visitez le [blog Windows](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="e1549-1407">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1408">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1408">Fixed</span></span>
- <span data-ttu-id="e1549-1409">Correction de la création de fichiers par le biais de liens symboliques</span><span class="sxs-lookup"><span data-stu-id="e1549-1409">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="e1549-1410">Ajout de listxattr pour Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="e1549-1410">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="e1549-1411">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1411">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1412">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1412">Syscall Support</span></span>
-   <span data-ttu-id="e1549-1413">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1413">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1414">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1414">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="e1549-1415">Build 14361</span><span class="sxs-lookup"><span data-stu-id="e1549-1415">Build 14361</span></span>
<span data-ttu-id="e1549-1416">Pour obtenir des informations Windows d’ordre général sur la build 14361, visitez le [blog Windows](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="e1549-1416">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1417">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1417">Fixed</span></span>
- <span data-ttu-id="e1549-1418">DrvFs est maintenant sensible à la casse lors de l’exécution dans Bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-1418">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="e1549-1419">Les utilisateurs peuvent utiliser case.txt et CASE.TXT sur leurs lecteurs /mnt/c</span><span class="sxs-lookup"><span data-stu-id="e1549-1419">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="e1549-1420">Le respect de la casse est pris en charge uniquement dans bash sur Ubuntu sur Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-1420">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="e1549-1421">En dehors de Bash, le système NTFS signale les fichiers correctement, mais un comportement inattendu peut se produire lors de l’interaction avec les fichiers à partir de Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-1421">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="e1549-1422">La racine de chaque volume (c.-à-d. /mnt/c) n’est pas sensible à la casse</span><span class="sxs-lookup"><span data-stu-id="e1549-1422">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="e1549-1423">Pour plus d’informations sur la gestion de ces fichiers dans Windows, consultez [cet article](https://support.microsoft.com/en-us/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="e1549-1423">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="e1549-1424">Prise en charge considérablement améliorée de pty/tty.</span><span class="sxs-lookup"><span data-stu-id="e1549-1424">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="e1549-1425">Prise en charge d’applications comme TMUX (GH #40)</span><span class="sxs-lookup"><span data-stu-id="e1549-1425">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="e1549-1426">Résolution d’un problème d’installation où les comptes d’utilisateur ne sont pas toujours créés</span><span class="sxs-lookup"><span data-stu-id="e1549-1426">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="e1549-1427">Optimisation de la structure d’arguments de la ligne de commande permettant une liste d’arguments extrêmement longue.</span><span class="sxs-lookup"><span data-stu-id="e1549-1427">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="e1549-1428">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="e1549-1428">(GH #153)</span></span>
- <span data-ttu-id="e1549-1429">Possibilité de supprimer et d’utiliser chmod sur des fichiers read_only de DrvFs</span><span class="sxs-lookup"><span data-stu-id="e1549-1429">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="e1549-1430">Correction de certaines instances où le terminal se bloque lors de la déconnexion (GH #43)</span><span class="sxs-lookup"><span data-stu-id="e1549-1430">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="e1549-1431">chmod et chown fonctionnent désormais sur les appareils tty</span><span class="sxs-lookup"><span data-stu-id="e1549-1431">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="e1549-1432">Autorisation de la connexion à 0.0.0.0 et :: en tant que localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="e1549-1432">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="e1549-1433">Gestion d’une longueur de vecteur d’E/S >1 pour sendmsg/recvmsg (GH #376 partiel)</span><span class="sxs-lookup"><span data-stu-id="e1549-1433">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="e1549-1434">Les utilisateurs peuvent désormais se désinscrire du fichier d’hôtes générés automatiquement (GH #398)</span><span class="sxs-lookup"><span data-stu-id="e1549-1434">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="e1549-1435">Correspondance automatique des paramètres régionaux Linux avec les paramètres régionaux NT pendant l’installation (GH #11)</span><span class="sxs-lookup"><span data-stu-id="e1549-1435">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="e1549-1436">Ajout du fichier /proc/sys/vm/swappiness (GH #306)</span><span class="sxs-lookup"><span data-stu-id="e1549-1436">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="e1549-1437">Fermeture correcte de strace</span><span class="sxs-lookup"><span data-stu-id="e1549-1437">strace now exits correctly</span></span>
- <span data-ttu-id="e1549-1438">Autorisation de la rouverture des canaux par le biais de /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="e1549-1438">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="e1549-1439">Masquage des répertoires sous %LOCALAPPDATA%\lxss à partir de DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="e1549-1439">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="e1549-1440">Meilleure gestion de bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="e1549-1440">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="e1549-1441">Prise en charge des commandes comme « bash ~ -c ls » (GH #467)</span><span class="sxs-lookup"><span data-stu-id="e1549-1441">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="e1549-1442">Les sockets notifient désormais la lecture epoll disponible pendant l’arrêt (GH #271)</span><span class="sxs-lookup"><span data-stu-id="e1549-1442">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="e1549-1443">Meilleure suppresion des fichiers et dossiers par lxrun /uninstall</span><span class="sxs-lookup"><span data-stu-id="e1549-1443">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="e1549-1444">Correction de ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="e1549-1444">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="e1549-1445">Prise en charge améliorée des applications x11 comme xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="e1549-1445">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="e1549-1446">Mise à jour de la taille de la pile des threads initiale pour qu’elle corresponde au paramètre Ubuntu par défaut et signale la taille correctement au syscall get_rlimit (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="e1549-1446">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="e1549-1447">Amélioration du signalement des noms d’image de processus pico (par exemple, pour l’audit)</span><span class="sxs-lookup"><span data-stu-id="e1549-1447">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="e1549-1448">Implémentation de /proc/mountinfo pour la commande df</span><span class="sxs-lookup"><span data-stu-id="e1549-1448">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="e1549-1449">Correction du code d’erreur de lien symbolique pour le nom d’enfant .</span><span class="sxs-lookup"><span data-stu-id="e1549-1449">Fixed symlink error code for child name .</span></span> <span data-ttu-id="e1549-1450">et .</span><span class="sxs-lookup"><span data-stu-id="e1549-1450">and ..</span></span>
- <span data-ttu-id="e1549-1451">Améliorations et corrections de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1451">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1452">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1452">Syscall Support</span></span>
<span data-ttu-id="e1549-1453">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1453">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1454">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1454">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="e1549-1455">Build 14352</span><span class="sxs-lookup"><span data-stu-id="e1549-1455">Build 14352</span></span>
<span data-ttu-id="e1549-1456">Pour obtenir des informations Windows d’ordre général sur la build 14352, visitez le [blog Windows](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="e1549-1456">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1457">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1457">Fixed</span></span>
- <span data-ttu-id="e1549-1458">Résolution d’un problème lié au téléchargement/à la création incorrects de fichiers volumineux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1458">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="e1549-1459">npm et d’autres scénarios doivent s’en retrouver débloqués (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="e1549-1459">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="e1549-1460">Suppression de certaines instances où les sockets se bloquent</span><span class="sxs-lookup"><span data-stu-id="e1549-1460">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="e1549-1461">Correction de certaines erreurs de ptrace</span><span class="sxs-lookup"><span data-stu-id="e1549-1461">Corrected some ptrace errors</span></span>
- <span data-ttu-id="e1549-1462">Résolution d’un problème lié à WSL qui autorise des noms de fichiers contenant plus de 255 caractères</span><span class="sxs-lookup"><span data-stu-id="e1549-1462">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="e1549-1463">Amélioration de la prise en charge des caractères non anglais</span><span class="sxs-lookup"><span data-stu-id="e1549-1463">Improved support for non-English characters</span></span>
- <span data-ttu-id="e1549-1464">Ajout et définition par défaut des données de fuseau horaire Windows actuelles</span><span class="sxs-lookup"><span data-stu-id="e1549-1464">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="e1549-1465">ID d’appareil unique pour chaque point de montage (correctif jre – GH #49)</span><span class="sxs-lookup"><span data-stu-id="e1549-1465">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="e1549-1466">Correction du problème liés aux chemins contenant « . »</span><span class="sxs-lookup"><span data-stu-id="e1549-1466">Correct issue with paths containing “.”</span></span> <span data-ttu-id="e1549-1467">et « .. »</span><span class="sxs-lookup"><span data-stu-id="e1549-1467">and “..”</span></span>
- <span data-ttu-id="e1549-1468">Ajout de la prise en charge FIFO (GH #71)</span><span class="sxs-lookup"><span data-stu-id="e1549-1468">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="e1549-1469">Mise à jour du format de resolv.conf pour correspondre au format Ubuntu natif</span><span class="sxs-lookup"><span data-stu-id="e1549-1469">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="e1549-1470">Nettoyage de certains procfs</span><span class="sxs-lookup"><span data-stu-id="e1549-1470">Some procfs cleanup</span></span>
- <span data-ttu-id="e1549-1471">Activation de ping pour les consoles administrateur (GH #18)</span><span class="sxs-lookup"><span data-stu-id="e1549-1471">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1472">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1472">Syscall Support</span></span>
<span data-ttu-id="e1549-1473">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1473">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1474">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1474">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="e1549-1475">Build 14342</span><span class="sxs-lookup"><span data-stu-id="e1549-1475">Build 14342</span></span>
<span data-ttu-id="e1549-1476">Pour obtenir des informations Windows d’ordre général sur la build 14342, visitez le [blog Windows](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="e1549-1476">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="e1549-1477">Pour plus d’informations sur VolFs et DriveFs, consultez le [blog WSL](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="e1549-1477">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="e1549-1478">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1478">Fixed</span></span>
- <span data-ttu-id="e1549-1479">Résolution du problème d’installation quand le nom d’utilisateur Windows contient des caractères Unicode</span><span class="sxs-lookup"><span data-stu-id="e1549-1479">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="e1549-1480">La solution de contournement apt-get update udev dans les questions fréquentes (FAQ) est désormais fournie par défaut lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="e1549-1480">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="e1549-1481">Activation de liens symboliques dans les répertoires DriveFs (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="e1549-1481">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="e1549-1482">Fonctionnement des liens symboliques entre DriveFs et VolFs</span><span class="sxs-lookup"><span data-stu-id="e1549-1482">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="e1549-1483">Traitement du problème d’analyse du chemin de niveau supérieur : fonctionnement comme prévu de ls .//</span><span class="sxs-lookup"><span data-stu-id="e1549-1483">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="e1549-1484">Fonctionnement de l’installation de npm sur DriveFs et des options -g</span><span class="sxs-lookup"><span data-stu-id="e1549-1484">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="e1549-1485">Résolution du problème empêchant le lancement du serveur PHP</span><span class="sxs-lookup"><span data-stu-id="e1549-1485">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="e1549-1486">Mise à jour des valeurs d’environnement par défaut, comme $PATH pour correspondre davantage à Ubuntu natif</span><span class="sxs-lookup"><span data-stu-id="e1549-1486">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="e1549-1487">Ajout d’une tâche de maintenance hebdomadaire dans Windows pour mettre à jour le cache de package apt</span><span class="sxs-lookup"><span data-stu-id="e1549-1487">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="e1549-1488">Résolution du problème lié à la validation de l’en-tête ELF, prise en charge par WSL de toutes les options Melkor</span><span class="sxs-lookup"><span data-stu-id="e1549-1488">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="e1549-1489">Interpréteur de commandes Zsh fonctionnel</span><span class="sxs-lookup"><span data-stu-id="e1549-1489">Zsh shell is functional</span></span>
- <span data-ttu-id="e1549-1490">Prise en charge des binaires Go précompilés</span><span class="sxs-lookup"><span data-stu-id="e1549-1490">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="e1549-1491">Localisation correcte de l’invite lors de la première exécution de Bash.exe</span><span class="sxs-lookup"><span data-stu-id="e1549-1491">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="e1549-1492">Retour d’informations correctes par /proc/meminfo</span><span class="sxs-lookup"><span data-stu-id="e1549-1492">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="e1549-1493">Prise en charge des sockets dans VFS</span><span class="sxs-lookup"><span data-stu-id="e1549-1493">Sockets now supported in VFS</span></span>
- <span data-ttu-id="e1549-1494">Montage de /dev en tant que tempfs</span><span class="sxs-lookup"><span data-stu-id="e1549-1494">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="e1549-1495">Prise en charge de FIFO</span><span class="sxs-lookup"><span data-stu-id="e1549-1495">Fifo now supported</span></span>
- <span data-ttu-id="e1549-1496">Présentation correcte des systèmes multicœurs dans /proc/cpuinfo</span><span class="sxs-lookup"><span data-stu-id="e1549-1496">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="e1549-1497">Téléchargement d’améliorations et de messages d’erreur supplémentaires lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="e1549-1497">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="e1549-1498">Améliorations et corrections de bogues syscall.</span><span class="sxs-lookup"><span data-stu-id="e1549-1498">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="e1549-1499">Prise en charge de la liste syscall ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e1549-1499">Supported syscall list below.</span></span>
- <span data-ttu-id="e1549-1500">Corrections de bogues et améliorations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1500">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="e1549-1501">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="e1549-1501">Known Issues</span></span>
- <span data-ttu-id="e1549-1502">Résolution incorrecte de « .. »</span><span class="sxs-lookup"><span data-stu-id="e1549-1502">Not resolving ‘..’</span></span> <span data-ttu-id="e1549-1503">sur DriveFs dans certains cas</span><span class="sxs-lookup"><span data-stu-id="e1549-1503">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1504">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1504">Syscall Support</span></span>
<span data-ttu-id="e1549-1505">Voici la liste des syscalls nouveaux ou améliorés qui ont une implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1505">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="e1549-1506">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1506">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="e1549-1507">Build 14332</span><span class="sxs-lookup"><span data-stu-id="e1549-1507">Build 14332</span></span>

<span data-ttu-id="e1549-1508">Pour obtenir des informations Windows d’ordre général sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="e1549-1508">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="e1549-1509">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1509">Fixed</span></span>
- <span data-ttu-id="e1549-1510">Meilleure génération de resolv.conf, y compris la hiérarchisation des entrées DNS</span><span class="sxs-lookup"><span data-stu-id="e1549-1510">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="e1549-1511">Problème lié au déplacement de fichiers et de répertoires entre des lecteurs /mnt et non-/mnt</span><span class="sxs-lookup"><span data-stu-id="e1549-1511">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="e1549-1512">Création désormais possible de fichiers tar avec des liens symboliques</span><span class="sxs-lookup"><span data-stu-id="e1549-1512">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="e1549-1513">Ajout du répertoire /run/lock par défaut lors de la création de l’instance</span><span class="sxs-lookup"><span data-stu-id="e1549-1513">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="e1549-1514">Mise à jour de /dev/null pour retourner des informations statistiques appropriées</span><span class="sxs-lookup"><span data-stu-id="e1549-1514">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="e1549-1515">Erreurs supplémentaires lors du téléchargement pendant la première exécution</span><span class="sxs-lookup"><span data-stu-id="e1549-1515">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="e1549-1516">Améliorations et corrections de bogues syscall.</span><span class="sxs-lookup"><span data-stu-id="e1549-1516">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="e1549-1517">Prise en charge de la liste syscall ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e1549-1517">Supported syscall list below.</span></span>
- <span data-ttu-id="e1549-1518">Améliorations et corrections de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1518">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1519">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1519">Syscall Support</span></span>
<span data-ttu-id="e1549-1520">Voici le nouveau syscall qui a une certaine implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1520">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="e1549-1521">Le syscall figurant dans cette liste est pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1521">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="e1549-1522">Build 14328</span><span class="sxs-lookup"><span data-stu-id="e1549-1522">Build 14328</span></span>

<span data-ttu-id="e1549-1523">Pour obtenir des informations Windows d’ordre général sur la build 14332, visitez le [blog Windows](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="e1549-1523">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="e1549-1524">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="e1549-1524">New Features</span></span>
* <span data-ttu-id="e1549-1525">Prise en charge des utilisateurs Linux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1525">Now support Linux users.</span></span>  <span data-ttu-id="e1549-1526">L’installation de Bash sur Ubuntu sur Windows vous invite à créer un utilisateur Linux.</span><span class="sxs-lookup"><span data-stu-id="e1549-1526">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="e1549-1527">Pour plus d’informations, visitez https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="e1549-1527">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="e1549-1528">Le nom d’hôte est maintenant défini sur le nom de l’ordinateur Windows, pas sur @localhost</span><span class="sxs-lookup"><span data-stu-id="e1549-1528">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="e1549-1529">Pour plus d’informations sur la build 14328, visitez : https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="e1549-1529">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="e1549-1530">Fixe</span><span class="sxs-lookup"><span data-stu-id="e1549-1530">Fixed</span></span>
* <span data-ttu-id="e1549-1531">Améliorations des liens symboliques pour les fichiers non/mnt/<drive></span><span class="sxs-lookup"><span data-stu-id="e1549-1531">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="e1549-1532">Fonctionnement de l’installation npm</span><span class="sxs-lookup"><span data-stu-id="e1549-1532">npm install now works</span></span>
    * <span data-ttu-id="e1549-1533">Installation désormais possible de jdk/jre en suivant les instructions données [ici](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span><span class="sxs-lookup"><span data-stu-id="e1549-1533">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="e1549-1534">Problème connu : les liens symboliques ne fonctionnent pas pour les montages Windows.</span><span class="sxs-lookup"><span data-stu-id="e1549-1534">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="e1549-1535">Cette fonctionnalité sera disponible dans une prochaine version</span><span class="sxs-lookup"><span data-stu-id="e1549-1535">Functionality will be available in a later build</span></span>
* <span data-ttu-id="e1549-1536">Affichage de top et htop</span><span class="sxs-lookup"><span data-stu-id="e1549-1536">top and htop now display</span></span>
* <span data-ttu-id="e1549-1537">Messages d’erreur supplémentaires pour certains échecs d’installation</span><span class="sxs-lookup"><span data-stu-id="e1549-1537">Additional error messages for some install failures</span></span>
* <span data-ttu-id="e1549-1538">Améliorations et corrections de bogues syscall.</span><span class="sxs-lookup"><span data-stu-id="e1549-1538">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="e1549-1539">Prise en charge de la liste syscall ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e1549-1539">Supported syscall list below.</span></span>
* <span data-ttu-id="e1549-1540">Améliorations et corrections de bogues supplémentaires</span><span class="sxs-lookup"><span data-stu-id="e1549-1540">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="e1549-1541">Prise en charge de syscall</span><span class="sxs-lookup"><span data-stu-id="e1549-1541">Syscall Support</span></span>
<span data-ttu-id="e1549-1542">Voici la liste des syscalls qui ont une certaine implémentation dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e1549-1542">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="e1549-1543">Les syscalls figurant dans cette liste sont pris en charge dans au moins un scénario, mais il est possible que tous les paramètres ne soient pas pris en charge pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="e1549-1543">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
