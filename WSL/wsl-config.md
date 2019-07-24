---
title: Gérer les distributions Linux
description: Liste de références et configuration de plusieurs distributions Linux exécutées sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, WSL. conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499279"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="34581-104">Gérer et configurer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="34581-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="34581-105">S’applique à Windows 10 automne Creators Update et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="34581-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="34581-106">Consultez notre [Guide d’installation](./install_guide.md) mis à jour pour essayer les nouvelles fonctionnalités de gestion et démarrer l’exécution de plusieurs distributions Linux à partir du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="34581-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="34581-107">Méthodes d’exécution de WSL</span><span class="sxs-lookup"><span data-stu-id="34581-107">Ways to run WSL</span></span>

<span data-ttu-id="34581-108">Il existe de nombreuses façons d’exécuter Linux avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="34581-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="34581-109">`[distro]`, par exemple`ubuntu`</span><span class="sxs-lookup"><span data-stu-id="34581-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="34581-110">`wsl.exe` ou `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="34581-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="34581-111">`wsl [command]` ou `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="34581-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="34581-112">La méthode que vous devez utiliser dépend de ce que vous faites.</span><span class="sxs-lookup"><span data-stu-id="34581-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="34581-113">Lancer WSL par distribution</span><span class="sxs-lookup"><span data-stu-id="34581-113">Launch WSL by distribution</span></span>

<span data-ttu-id="34581-114">L’exécution d’une distribution à l’aide de son application spécifique à distribution lance cette distribution dans sa propre fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="34581-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

<span data-ttu-id="34581-116">Cela revient à cliquer sur «lancer» dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="34581-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Lancer WSL à partir du Microsoft Store](media/store-launch.png)

<span data-ttu-id="34581-118">Vous pouvez également exécuter la distribution à partir de la ligne de `[distribution].exe`commande en exécutant.</span><span class="sxs-lookup"><span data-stu-id="34581-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="34581-119">L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon est qu’elle modifie automatiquement votre répertoire de travail du répertoire actif vers le répertoire de départ de la distribution.</span><span class="sxs-lookup"><span data-stu-id="34581-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="34581-120">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="34581-120">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="34581-121">WSL et WSL [commande]</span><span class="sxs-lookup"><span data-stu-id="34581-121">wsl and wsl [command]</span></span>

<span data-ttu-id="34581-122">La meilleure façon d’exécuter WSL à partir de la ligne de `wsl.exe`commande consiste à utiliser.</span><span class="sxs-lookup"><span data-stu-id="34581-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="34581-123">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="34581-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="34581-124">Non seulement `wsl` conserve le répertoire de travail actuel, mais il vous permet d’exécuter une seule commande sur les commandes Windows latérales.</span><span class="sxs-lookup"><span data-stu-id="34581-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="34581-125">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="34581-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="34581-126">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="34581-126">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="34581-127">Gestion de plusieurs distributions Linux</span><span class="sxs-lookup"><span data-stu-id="34581-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="34581-128">Windows 10 version 1903 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="34581-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="34581-129">Vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), notamment la liste des distributions disponibles, la définition d’une distribution par défaut et la désinstallation des distributions.</span><span class="sxs-lookup"><span data-stu-id="34581-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="34581-130">Chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="34581-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="34581-131">Pour afficher les commandes spécifiques à la distribution `[distro.exe] /?`, exécutez.</span><span class="sxs-lookup"><span data-stu-id="34581-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="34581-132">Par exemple : `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="34581-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="34581-133">Répertorier les distributions</span><span class="sxs-lookup"><span data-stu-id="34581-133">List distributions</span></span>

<span data-ttu-id="34581-134">`wsl -l`,`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="34581-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="34581-135">Répertorie les distributions Linux disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="34581-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="34581-136">Si une distribution est indiquée, elle est installée et prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="34581-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="34581-137">Répertorie toutes les distributions, y compris celles qui ne sont pas actuellement utilisables.</span><span class="sxs-lookup"><span data-stu-id="34581-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="34581-138">Ils peuvent être en cours d’installation, de désinstallation ou de rupture.</span><span class="sxs-lookup"><span data-stu-id="34581-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="34581-139">Répertorie toutes les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="34581-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="34581-140">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="34581-140">Set a default distribution</span></span>

<span data-ttu-id="34581-141">La distribution WSL par défaut est celle qui s’exécute lorsque vous `wsl` exécutez sur une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="34581-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="34581-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="34581-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="34581-143">Définit la distribution par défaut `<DistributionName>`sur.</span><span class="sxs-lookup"><span data-stu-id="34581-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="34581-144">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="34581-144">**Example:**</span></span>  
<span data-ttu-id="34581-145">`wsl -s Ubuntu`définit la distribution par défaut sur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="34581-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="34581-146">À présent, lorsque `wsl npm init` je l’exécute, il s’exécute sous Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="34581-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="34581-147">Si je l' `wsl` exécute, une session Ubuntu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="34581-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="34581-148">Désinscrire et réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="34581-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="34581-149">Alors que les distributions Linux peuvent être installées via le Microsoft Store, elles ne peuvent pas être désinstallées via le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="34581-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="34581-150">WSL config permet d’annuler l’inscription/la désinstallation des distributions.</span><span class="sxs-lookup"><span data-stu-id="34581-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="34581-151">L’annulation de l’inscription permet également de réinstaller les distributions.</span><span class="sxs-lookup"><span data-stu-id="34581-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="34581-152">**Attention :** Une fois l’inscription annulée, toutes les données, tous les paramètres et tous les logiciels associés à cette distribution seront définitivement perdus.</span><span class="sxs-lookup"><span data-stu-id="34581-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="34581-153">La réinstallation à partir du Store installe une copie propre de la distribution.</span><span class="sxs-lookup"><span data-stu-id="34581-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="34581-154">Annule l’enregistrement de la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="34581-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="34581-155">Par exemple: `wsl --unregister Ubuntu` supprimez Ubuntu des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="34581-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="34581-156">Lorsque je l' `wsl --list` exécute, il ne figure pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="34581-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="34581-157">Pour réinstaller, recherchez la distribution dans le Microsoft Store et sélectionnez «lancer».</span><span class="sxs-lookup"><span data-stu-id="34581-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="34581-158">Exécuter en tant qu’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="34581-158">Run as a specific user</span></span>

<span data-ttu-id="34581-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="34581-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="34581-160">Exécuter WSL en tant qu’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="34581-160">Run WSL as the specified user.</span></span> <span data-ttu-id="34581-161">Veuillez noter que l’utilisateur doit exister dans la distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="34581-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="34581-162">Exécuter une distribution spécifique</span><span class="sxs-lookup"><span data-stu-id="34581-162">Run a specific distribution</span></span>

<span data-ttu-id="34581-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="34581-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="34581-164">Exécuter une distribution spécifiée de WSL, peut être utilisé pour envoyer des commandes à une distribution spécifique sans avoir à modifier votre valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="34581-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="34581-165">Versions antérieures à la version 1903 de Windows 10</span><span class="sxs-lookup"><span data-stu-id="34581-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="34581-166">WSL config (`wslconfig.exe`) est un outil de ligne de commande permettant de gérer les distributions Linux exécutées sur le sous-système Windows pour Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="34581-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="34581-167">Elle vous permet de répertorier les distributions disponibles, de définir une distribution par défaut et de désinstaller les distributions.</span><span class="sxs-lookup"><span data-stu-id="34581-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="34581-168">Alors que la configuration de WSL est utile pour les paramètres qui s’étendent ou coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="34581-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="34581-169">Pour afficher les commandes spécifiques à la distribution `[distro.exe] /?`, exécutez.</span><span class="sxs-lookup"><span data-stu-id="34581-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="34581-170">Par exemple : `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="34581-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="34581-171">Pour afficher toutes les options disponibles pour wslconfig, exécutez:`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="34581-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="34581-172">Répertorier les distributions</span><span class="sxs-lookup"><span data-stu-id="34581-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="34581-173">Répertorie les distributions Linux disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="34581-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="34581-174">Si une distribution est indiquée, elle est installée et prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="34581-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="34581-175">Répertorie toutes les distributions, y compris celles qui ne sont pas actuellement utilisables.</span><span class="sxs-lookup"><span data-stu-id="34581-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="34581-176">Ils peuvent être en cours d’installation, de désinstallation ou de rupture.</span><span class="sxs-lookup"><span data-stu-id="34581-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="34581-177">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="34581-177">Set a default distribution</span></span>

<span data-ttu-id="34581-178">La distribution WSL par défaut est celle qui s’exécute lorsque vous `wsl` exécutez sur une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="34581-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="34581-179">Définit la distribution par défaut `<DistributionName>`sur.</span><span class="sxs-lookup"><span data-stu-id="34581-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="34581-180">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="34581-180">**Example:**</span></span>  
<span data-ttu-id="34581-181">`wslconfig /setdefault Ubuntu`définit la distribution par défaut sur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="34581-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="34581-182">À présent, lorsque `wsl npm init` je l’exécute, il s’exécute sous Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="34581-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="34581-183">Si je l' `wsl` exécute, une session Ubuntu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="34581-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="34581-184">Désinscrire et réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="34581-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="34581-185">Alors que les distributions Linux peuvent être installées via le Microsoft Store, elles ne peuvent pas être désinstallées via le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="34581-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="34581-186">WSL config permet d’annuler l’inscription/la désinstallation des distributions.</span><span class="sxs-lookup"><span data-stu-id="34581-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="34581-187">L’annulation de l’inscription permet également de réinstaller les distributions.</span><span class="sxs-lookup"><span data-stu-id="34581-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="34581-188">**Attention :** Une fois l’inscription annulée, toutes les données, tous les paramètres et tous les logiciels associés à cette distribution seront définitivement perdus.</span><span class="sxs-lookup"><span data-stu-id="34581-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="34581-189">La réinstallation à partir du Store installe une copie propre de la distribution.</span><span class="sxs-lookup"><span data-stu-id="34581-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="34581-190">Annule l’enregistrement de la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="34581-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="34581-191">Par exemple: `wslconfig /unregister Ubuntu` supprimez Ubuntu des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="34581-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="34581-192">Lorsque je l' `wslconfig /list` exécute, il ne figure pas dans la liste.</span><span class="sxs-lookup"><span data-stu-id="34581-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="34581-193">Pour réinstaller, recherchez la distribution dans le Microsoft Store et sélectionnez «lancer».</span><span class="sxs-lookup"><span data-stu-id="34581-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="34581-194">Définir les paramètres de lancement de WSL</span><span class="sxs-lookup"><span data-stu-id="34581-194">Set WSL launch settings</span></span>

> <span data-ttu-id="34581-195">**Disponible dans Windows Insider Build 17093 et versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="34581-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="34581-196">Configurez automatiquement certaines fonctionnalités dans WSL qui seront appliquées chaque fois que vous lancerez le `wsl.conf`sous-système à l’aide de.</span><span class="sxs-lookup"><span data-stu-id="34581-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="34581-197">Pour le moment, cela comprend les options de montage automatique et la configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="34581-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="34581-198">`wsl.conf`se trouve dans chaque distribution Linux dans `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="34581-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="34581-199">Si le fichier n’est pas là, vous pouvez le créer vous-même.</span><span class="sxs-lookup"><span data-stu-id="34581-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="34581-200">WSL détectera l’existence du fichier et lira son contenu.</span><span class="sxs-lookup"><span data-stu-id="34581-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="34581-201">Si le fichier est manquant ou incorrect (il s’agit d’une mise en forme de balisage incorrecte), WSL continuera à se lancer normalement.</span><span class="sxs-lookup"><span data-stu-id="34581-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="34581-202">Voici un exemple `wsl.conf` de fichier que vous pouvez ajouter à votre distributions:</span><span class="sxs-lookup"><span data-stu-id="34581-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="34581-203">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="34581-203">Configuration Options</span></span>

<span data-ttu-id="34581-204">Conformément aux conventions. ini, les clés sont déclarées sous une section.</span><span class="sxs-lookup"><span data-stu-id="34581-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="34581-205">WSL prend en charge deux `automount` sections `network`: et.</span><span class="sxs-lookup"><span data-stu-id="34581-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="34581-206">montage automatique</span><span class="sxs-lookup"><span data-stu-id="34581-206">automount</span></span>

<span data-ttu-id="34581-207">Section`[automount]`</span><span class="sxs-lookup"><span data-stu-id="34581-207">Section: `[automount]`</span></span>


| <span data-ttu-id="34581-208">Clé</span><span class="sxs-lookup"><span data-stu-id="34581-208">key</span></span>        | <span data-ttu-id="34581-209">valeur</span><span class="sxs-lookup"><span data-stu-id="34581-209">value</span></span>                          | <span data-ttu-id="34581-210">par défaut</span><span class="sxs-lookup"><span data-stu-id="34581-210">default</span></span>      | <span data-ttu-id="34581-211">Notes</span><span class="sxs-lookup"><span data-stu-id="34581-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34581-212">enabled</span><span class="sxs-lookup"><span data-stu-id="34581-212">enabled</span></span>    | <span data-ttu-id="34581-213">booléenne</span><span class="sxs-lookup"><span data-stu-id="34581-213">boolean</span></span>                        | <span data-ttu-id="34581-214">true</span><span class="sxs-lookup"><span data-stu-id="34581-214">true</span></span>         | <span data-ttu-id="34581-215">`true`provoque des lecteurs fixes (c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="34581-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="34581-216">`C:/`ou `D:/`) à monter automatiquement avec DrvFs sous `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="34581-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="34581-217">`false`signifie que les disques ne seront pas montés automatiquement, mais vous pouvez les monter `fstab`manuellement ou via.</span><span class="sxs-lookup"><span data-stu-id="34581-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="34581-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="34581-218">mountFsTab</span></span> | <span data-ttu-id="34581-219">booléenne</span><span class="sxs-lookup"><span data-stu-id="34581-219">boolean</span></span>                        | <span data-ttu-id="34581-220">true</span><span class="sxs-lookup"><span data-stu-id="34581-220">true</span></span>         | <span data-ttu-id="34581-221">`true`définit `/etc/fstab` à traiter au démarrage de WSL.</span><span class="sxs-lookup"><span data-stu-id="34581-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="34581-222">/etc/fstab est un fichier dans lequel vous pouvez déclarer d’autres systèmes de fichiers, comme un partage SMB.</span><span class="sxs-lookup"><span data-stu-id="34581-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="34581-223">Par conséquent, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage.</span><span class="sxs-lookup"><span data-stu-id="34581-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="34581-224">causes</span><span class="sxs-lookup"><span data-stu-id="34581-224">root</span></span>       | <span data-ttu-id="34581-225">String</span><span class="sxs-lookup"><span data-stu-id="34581-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="34581-226">Définit le répertoire dans lequel les lecteurs fixes seront montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="34581-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="34581-227">Par exemple, si vous avez un répertoire dans WSL à `/windir/` l’adresse et que vous le spécifiez en tant que racine, vous vous attendez à ce que vos lecteurs fixes soient montés sur`/windir/c`</span><span class="sxs-lookup"><span data-stu-id="34581-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="34581-228">options</span><span class="sxs-lookup"><span data-stu-id="34581-228">options</span></span>    | <span data-ttu-id="34581-229">liste de valeurs séparées par des virgules</span><span class="sxs-lookup"><span data-stu-id="34581-229">comma-separated list of values</span></span> | <span data-ttu-id="34581-230">chaîne vide</span><span class="sxs-lookup"><span data-stu-id="34581-230">empty string</span></span> | <span data-ttu-id="34581-231">Cette valeur est ajoutée à la chaîne des options de montage DrvFs par défaut.</span><span class="sxs-lookup"><span data-stu-id="34581-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="34581-232">**Seules les options spécifiques à DrvFs peuvent être spécifiées.**</span><span class="sxs-lookup"><span data-stu-id="34581-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="34581-233">Les options que le fichier binaire de montage analyse normalement dans un indicateur ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="34581-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="34581-234">Si vous souhaitez spécifier explicitement ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="34581-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="34581-235">Par défaut, WSL définit l’UID et le GID sur la valeur de l’utilisateur par défaut (dans Ubuntu distribution, l’utilisateur par défaut est créé avec UID = 1000, GID = 1000).</span><span class="sxs-lookup"><span data-stu-id="34581-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="34581-236">Si l’utilisateur spécifie une option GID ou uid explicitement via cette clé, la valeur associée est remplacée.</span><span class="sxs-lookup"><span data-stu-id="34581-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="34581-237">Dans le cas contraire, la valeur par défaut sera toujours ajoutée.</span><span class="sxs-lookup"><span data-stu-id="34581-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="34581-238">**Remarque :** Ces options sont appliquées en tant qu’options de montage pour tous les lecteurs montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="34581-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="34581-239">Pour modifier les options d’un lecteur spécifique uniquement, utilisez/etc/fstab à la place.</span><span class="sxs-lookup"><span data-stu-id="34581-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="34581-240">réseau</span><span class="sxs-lookup"><span data-stu-id="34581-240">network</span></span>

<span data-ttu-id="34581-241">Étiquette de section:`[network]`</span><span class="sxs-lookup"><span data-stu-id="34581-241">Section label: `[network]`</span></span>

| <span data-ttu-id="34581-242">Clé</span><span class="sxs-lookup"><span data-stu-id="34581-242">key</span></span> | <span data-ttu-id="34581-243">valeur</span><span class="sxs-lookup"><span data-stu-id="34581-243">value</span></span> | <span data-ttu-id="34581-244">par défaut</span><span class="sxs-lookup"><span data-stu-id="34581-244">default</span></span> | <span data-ttu-id="34581-245">Notes</span><span class="sxs-lookup"><span data-stu-id="34581-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="34581-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="34581-246">generateHosts</span></span> | <span data-ttu-id="34581-247">booléenne</span><span class="sxs-lookup"><span data-stu-id="34581-247">boolean</span></span> | `true` | <span data-ttu-id="34581-248">`true`définit WSL à générer `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="34581-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="34581-249">Le `hosts` fichier contient une carte statique de noms d’hôtes correspondant à l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="34581-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="34581-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="34581-250">generateResolvConf</span></span> | <span data-ttu-id="34581-251">booléenne</span><span class="sxs-lookup"><span data-stu-id="34581-251">boolean</span></span> | `true` | <span data-ttu-id="34581-252">`true`Définissez WSL sur Generate `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="34581-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="34581-253">Le `resolv.conf` contient une liste DNS capable de résoudre un nom d’hôte donné en son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="34581-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="34581-254">salon</span><span class="sxs-lookup"><span data-stu-id="34581-254">interop</span></span>

<span data-ttu-id="34581-255">Étiquette de section:`[interop]`</span><span class="sxs-lookup"><span data-stu-id="34581-255">Section label: `[interop]`</span></span>

<span data-ttu-id="34581-256">Ces options sont disponibles dans la build Insider 17713 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="34581-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="34581-257">Clé</span><span class="sxs-lookup"><span data-stu-id="34581-257">key</span></span> | <span data-ttu-id="34581-258">valeur</span><span class="sxs-lookup"><span data-stu-id="34581-258">value</span></span> | <span data-ttu-id="34581-259">par défaut</span><span class="sxs-lookup"><span data-stu-id="34581-259">default</span></span> | <span data-ttu-id="34581-260">Notes</span><span class="sxs-lookup"><span data-stu-id="34581-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="34581-261">enabled</span><span class="sxs-lookup"><span data-stu-id="34581-261">enabled</span></span> | <span data-ttu-id="34581-262">booléenne</span><span class="sxs-lookup"><span data-stu-id="34581-262">boolean</span></span> | `true` | <span data-ttu-id="34581-263">La définition de cette clé permet de déterminer si WSL prend en charge le lancement des processus Windows.</span><span class="sxs-lookup"><span data-stu-id="34581-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="34581-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="34581-264">appendWindowsPath</span></span> | <span data-ttu-id="34581-265">booléenne</span><span class="sxs-lookup"><span data-stu-id="34581-265">boolean</span></span> | `true` | <span data-ttu-id="34581-266">La définition de cette clé détermine si WSL ajoute des éléments de chemin d’accès Windows à la variable d’environnement $PATH.</span><span class="sxs-lookup"><span data-stu-id="34581-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
