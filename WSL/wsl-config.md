---
title: Gérer les distributions Linux
description: Lister les références et configurer plusieurs distributions Linux exécutées sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999395"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="7d06a-104">Gérer et configurer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="7d06a-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="7d06a-105">S’applique à Windows 10 Fall Creators Update et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7d06a-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="7d06a-106">Consultez notre [guide d’installation](./install_guide.md) mis à jour pour essayer les nouvelles fonctionnalités de gestion et commencer à exécuter plusieurs distributions Linux à partir du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7d06a-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="7d06a-107">Méthodes d’exécution de WSL</span><span class="sxs-lookup"><span data-stu-id="7d06a-107">Ways to run WSL</span></span>

<span data-ttu-id="7d06a-108">Il existe de nombreuses façons d’exécuter Linux avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="7d06a-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="7d06a-109">`[distro]`, par exemple `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="7d06a-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="7d06a-110">`wsl.exe` ou `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="7d06a-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="7d06a-111">`wsl [command]` ou `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="7d06a-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="7d06a-112">La méthode que vous devez utiliser dépend de ce que vous faites.</span><span class="sxs-lookup"><span data-stu-id="7d06a-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="7d06a-113">Lancer WSL par distribution</span><span class="sxs-lookup"><span data-stu-id="7d06a-113">Launch WSL by distribution</span></span>

<span data-ttu-id="7d06a-114">L’exécution d’une distribution à l’aide de son application spécifique à la distribution lance cette distribution dans sa propre fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="7d06a-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

<span data-ttu-id="7d06a-116">Cela revient à cliquer sur « Lancer » dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7d06a-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Lancer WSL à partir du Microsoft Store](media/store-launch.png)

<span data-ttu-id="7d06a-118">Vous pouvez également exécuter la distribution à partir de la ligne de commande en exécutant `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="7d06a-119">L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon est qu’elle définit automatiquement votre répertoire de travail sur le répertoire de base de la distribution.</span><span class="sxs-lookup"><span data-stu-id="7d06a-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="7d06a-120">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="7d06a-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="7d06a-121">wsl et wsl [commande]</span><span class="sxs-lookup"><span data-stu-id="7d06a-121">wsl and wsl [command]</span></span>

<span data-ttu-id="7d06a-122">La meilleure façon d’exécuter WSL à partir de la ligne de commande consiste à utiliser `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="7d06a-123">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="7d06a-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="7d06a-124">Non seulement l’utilitaire `wsl` conserve le répertoire de travail actuel, mais il vous permet d’exécuter une seule commande à côté de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="7d06a-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="7d06a-125">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="7d06a-125">**Example:**</span></span>

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

<span data-ttu-id="7d06a-126">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="7d06a-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="7d06a-127">Gestion de plusieurs distributions Linux</span><span class="sxs-lookup"><span data-stu-id="7d06a-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="7d06a-128">Windows 10 version 1903 et ultérieures</span><span class="sxs-lookup"><span data-stu-id="7d06a-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="7d06a-129">Vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), notamment pour lister les distributions disponibles, définir une distribution par défaut et désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="7d06a-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="7d06a-130">Chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="7d06a-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="7d06a-131">Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="7d06a-132">Par exemple, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="7d06a-133">Lister les distributions</span><span class="sxs-lookup"><span data-stu-id="7d06a-133">List distributions</span></span>

<span data-ttu-id="7d06a-134">`wsl -l`, `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="7d06a-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="7d06a-135">Liste les distributions Linux disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="7d06a-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="7d06a-136">Si une distribution est listée, elle est installée et prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="7d06a-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="7d06a-137">Liste toutes les distributions, y compris celles qui ne sont pas utilisables.</span><span class="sxs-lookup"><span data-stu-id="7d06a-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="7d06a-138">Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.</span><span class="sxs-lookup"><span data-stu-id="7d06a-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="7d06a-139">Liste toutes les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="7d06a-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="7d06a-140">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="7d06a-140">Set a default distribution</span></span>

<span data-ttu-id="7d06a-141">La distribution WSL par défaut est celle qui s’exécute quand vous exécutez `wsl` depuis une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7d06a-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="7d06a-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="7d06a-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="7d06a-143">Définit la distribution par défaut sur `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="7d06a-144">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="7d06a-144">**Example:**</span></span>  
<span data-ttu-id="7d06a-145">`wsl -s Ubuntu` définit ma distribution par défaut sur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="7d06a-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="7d06a-146">À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="7d06a-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="7d06a-147">Si j’exécute `wsl`, une session Ubuntu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7d06a-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="7d06a-148">Désinscrire et réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="7d06a-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="7d06a-149">Les distributions Linux peuvent être installées par l’intermédiaire du Microsoft Store, mais elles ne peuvent pas être désinstallées par ce biais.</span><span class="sxs-lookup"><span data-stu-id="7d06a-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="7d06a-150">WSL Config permet de désinscrire/désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="7d06a-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="7d06a-151">La désinscription permet également de réinstaller les distributions.</span><span class="sxs-lookup"><span data-stu-id="7d06a-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="7d06a-152">**Attention :** Une fois qu’une distribution est désinscrite, toutes les données, paramètres et logiciels associés à celle-ci sont définitivement perdus.</span><span class="sxs-lookup"><span data-stu-id="7d06a-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="7d06a-153">La réinstallation à partir du Store installe une nouvelle copie de la distribution.</span><span class="sxs-lookup"><span data-stu-id="7d06a-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="7d06a-154">Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="7d06a-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="7d06a-155">Par exemple : `wsl --unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="7d06a-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="7d06a-156">Quand j’exécute `wsl --list`, celui-ci n’est pas listé.</span><span class="sxs-lookup"><span data-stu-id="7d06a-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="7d06a-157">Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».</span><span class="sxs-lookup"><span data-stu-id="7d06a-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="7d06a-158">Exécuter en tant qu’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="7d06a-158">Run as a specific user</span></span>

<span data-ttu-id="7d06a-159">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="7d06a-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="7d06a-160">Exécutez WSL en tant qu’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="7d06a-160">Run WSL as the specified user.</span></span> <span data-ttu-id="7d06a-161">Notez que l’utilisateur doit exister dans la distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="7d06a-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="7d06a-162">Exécuter une distribution spécifique</span><span class="sxs-lookup"><span data-stu-id="7d06a-162">Run a specific distribution</span></span>

<span data-ttu-id="7d06a-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="7d06a-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="7d06a-164">Exécutez une distribution spécifiée de WSL ; cette opération peut être utilisée pour envoyer des commandes à une distribution spécifique sans avoir à changer la distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="7d06a-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="7d06a-165">Versions antérieures à la version 1903 de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7d06a-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="7d06a-166">WSL Config (`wslconfig.exe`) est un outil en ligne de commande permettant de gérer les distributions Linux exécutées sur le sous-système Windows pour Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="7d06a-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="7d06a-167">Il vous permet de lister les distributions disponibles, de définir une distribution par défaut et de désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="7d06a-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="7d06a-168">Même si WSL Config est utile pour les paramètres qui englobent ou coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="7d06a-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="7d06a-169">Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="7d06a-170">Par exemple, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="7d06a-171">Pour voir toutes les options disponibles pour wslconfig, exécutez : `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="7d06a-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="7d06a-172">Lister les distributions</span><span class="sxs-lookup"><span data-stu-id="7d06a-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="7d06a-173">Liste les distributions Linux disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="7d06a-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="7d06a-174">Si une distribution est listée, elle est installée et prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="7d06a-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="7d06a-175">Liste toutes les distributions, y compris celles qui ne sont pas utilisables.</span><span class="sxs-lookup"><span data-stu-id="7d06a-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="7d06a-176">Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.</span><span class="sxs-lookup"><span data-stu-id="7d06a-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="7d06a-177">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="7d06a-177">Set a default distribution</span></span>

<span data-ttu-id="7d06a-178">La distribution WSL par défaut est celle qui s’exécute quand vous exécutez `wsl` depuis une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7d06a-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="7d06a-179">Définit la distribution par défaut sur `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="7d06a-180">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="7d06a-180">**Example:**</span></span>  
<span data-ttu-id="7d06a-181">`wslconfig /setdefault Ubuntu` définit ma distribution par défaut sur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="7d06a-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="7d06a-182">À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="7d06a-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="7d06a-183">Si j’exécute `wsl`, une session Ubuntu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="7d06a-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="7d06a-184">Désinscrire et réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="7d06a-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="7d06a-185">Les distributions Linux peuvent être installées par l’intermédiaire du Microsoft Store, mais elles ne peuvent pas être désinstallées par ce biais.</span><span class="sxs-lookup"><span data-stu-id="7d06a-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="7d06a-186">WSL Config permet de désinscrire/désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="7d06a-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="7d06a-187">La désinscription permet également de réinstaller les distributions.</span><span class="sxs-lookup"><span data-stu-id="7d06a-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="7d06a-188">**Attention :** Une fois qu’une distribution est désinscrite, toutes les données, paramètres et logiciels associés à celle-ci sont définitivement perdus.</span><span class="sxs-lookup"><span data-stu-id="7d06a-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="7d06a-189">La réinstallation à partir du Store installe une nouvelle copie de la distribution.</span><span class="sxs-lookup"><span data-stu-id="7d06a-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="7d06a-190">Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="7d06a-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="7d06a-191">Par exemple : `wslconfig /unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="7d06a-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="7d06a-192">Quand j’exécute `wslconfig /list`, celui-ci n’est pas listé.</span><span class="sxs-lookup"><span data-stu-id="7d06a-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="7d06a-193">Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».</span><span class="sxs-lookup"><span data-stu-id="7d06a-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="7d06a-194">Définir les paramètres de lancement de WSL</span><span class="sxs-lookup"><span data-stu-id="7d06a-194">Set WSL launch settings</span></span>

> <span data-ttu-id="7d06a-195">**Disponible dans Windows Insider build 17093 et ultérieures**</span><span class="sxs-lookup"><span data-stu-id="7d06a-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="7d06a-196">Configurez automatiquement certaines fonctionnalités dans WSL afin de les appliquer chaque fois que vous lancez le sous-système à l’aide de `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="7d06a-197">Pour le moment, cela comprend les options de montage automatique et la configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="7d06a-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="7d06a-198">`wsl.conf` se trouve dans chaque distribution Linux dans `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="7d06a-199">Si le fichier n’y est pas, vous pouvez le créer vous-même.</span><span class="sxs-lookup"><span data-stu-id="7d06a-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="7d06a-200">WSL détecte l’existence du fichier et lit son contenu.</span><span class="sxs-lookup"><span data-stu-id="7d06a-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="7d06a-201">Si le fichier est manquant ou incorrect (mise en forme incorrecte du balisage), WSL continue à se lancer normalement.</span><span class="sxs-lookup"><span data-stu-id="7d06a-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="7d06a-202">Voici un exemple de fichier `wsl.conf` que vous pouvez ajouter à vos distributions :</span><span class="sxs-lookup"><span data-stu-id="7d06a-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="7d06a-203">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="7d06a-203">Configuration Options</span></span>

<span data-ttu-id="7d06a-204">Conformément aux conventions .ini, les clés sont déclarées sous une section.</span><span class="sxs-lookup"><span data-stu-id="7d06a-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="7d06a-205">WSL prend en charge deux sections : `automount` et `network`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="7d06a-206">automount</span><span class="sxs-lookup"><span data-stu-id="7d06a-206">automount</span></span>

<span data-ttu-id="7d06a-207">Section : `[automount]`</span><span class="sxs-lookup"><span data-stu-id="7d06a-207">Section: `[automount]`</span></span>


| <span data-ttu-id="7d06a-208">key</span><span class="sxs-lookup"><span data-stu-id="7d06a-208">key</span></span>        | <span data-ttu-id="7d06a-209">value</span><span class="sxs-lookup"><span data-stu-id="7d06a-209">value</span></span>                          | <span data-ttu-id="7d06a-210">par défaut</span><span class="sxs-lookup"><span data-stu-id="7d06a-210">default</span></span>      | <span data-ttu-id="7d06a-211">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d06a-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d06a-212">enabled</span><span class="sxs-lookup"><span data-stu-id="7d06a-212">enabled</span></span>    | <span data-ttu-id="7d06a-213">booléen</span><span class="sxs-lookup"><span data-stu-id="7d06a-213">boolean</span></span>                        | <span data-ttu-id="7d06a-214">true</span><span class="sxs-lookup"><span data-stu-id="7d06a-214">true</span></span>         | <span data-ttu-id="7d06a-215">`true` : les lecteurs fixes (c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="7d06a-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="7d06a-216">`C:/` ou `D:/`) sont automatiquement montés avec DrvFs sous `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="7d06a-217">`false` : les disques ne sont pas montés automatiquement, mais vous pouvez les monter manuellement ou par le biais de `fstab`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="7d06a-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="7d06a-218">mountFsTab</span></span> | <span data-ttu-id="7d06a-219">booléen</span><span class="sxs-lookup"><span data-stu-id="7d06a-219">boolean</span></span>                        | <span data-ttu-id="7d06a-220">true</span><span class="sxs-lookup"><span data-stu-id="7d06a-220">true</span></span>         | <span data-ttu-id="7d06a-221">`true` : `/etc/fstab` est traité au démarrage de WSL.</span><span class="sxs-lookup"><span data-stu-id="7d06a-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="7d06a-222">/etc/fstab est un fichier dans lequel vous pouvez déclarer d’autres systèmes de fichiers, comme un partage SMB.</span><span class="sxs-lookup"><span data-stu-id="7d06a-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="7d06a-223">Ainsi, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage.</span><span class="sxs-lookup"><span data-stu-id="7d06a-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="7d06a-224">root</span><span class="sxs-lookup"><span data-stu-id="7d06a-224">root</span></span>       | <span data-ttu-id="7d06a-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="7d06a-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="7d06a-226">Définit le répertoire dans lequel les lecteurs fixes sont montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7d06a-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="7d06a-227">Par exemple, si vous avez un répertoire dans WSL à l’emplacement `/windir/` et que vous le spécifiez en tant que racine, vos lecteurs fixes sont censés être montés à l’emplacement `/windir/c`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="7d06a-228">options</span><span class="sxs-lookup"><span data-stu-id="7d06a-228">options</span></span>    | <span data-ttu-id="7d06a-229">Liste de valeurs séparées par des virgules</span><span class="sxs-lookup"><span data-stu-id="7d06a-229">comma-separated list of values</span></span> | <span data-ttu-id="7d06a-230">Chaîne vide</span><span class="sxs-lookup"><span data-stu-id="7d06a-230">empty string</span></span> | <span data-ttu-id="7d06a-231">Cette valeur est ajoutée à la chaîne des options de montage DrvFs par défaut.</span><span class="sxs-lookup"><span data-stu-id="7d06a-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="7d06a-232">**Seules les options propres à DrvFs peuvent être spécifiées.**</span><span class="sxs-lookup"><span data-stu-id="7d06a-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="7d06a-233">Les options que le fichier binaire de montage analyse normalement dans un indicateur ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7d06a-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="7d06a-234">Si vous souhaitez spécifier explicitement ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="7d06a-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="7d06a-235">Par défaut, WSL définit les options uid et gid sur la valeur de l’utilisateur par défaut (dans une distribution Ubuntu, l’utilisateur par défaut est créé avec uid=1000,gid=1000).</span><span class="sxs-lookup"><span data-stu-id="7d06a-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="7d06a-236">Si l’utilisateur spécifie une option gid ou uid explicitement par le biais de cette clé, la valeur associée est remplacée.</span><span class="sxs-lookup"><span data-stu-id="7d06a-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="7d06a-237">Dans le cas contraire, la valeur par défaut est toujours ajoutée.</span><span class="sxs-lookup"><span data-stu-id="7d06a-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="7d06a-238">**Remarque :** Ces options sont appliquées en tant qu’options de montage pour tous les lecteurs montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="7d06a-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="7d06a-239">Pour changer les options d’un lecteur spécifique uniquement, utilisez /etc/fstab à la place.</span><span class="sxs-lookup"><span data-stu-id="7d06a-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

##### <a name="mount-options"></a><span data-ttu-id="7d06a-240">Options de montage</span><span class="sxs-lookup"><span data-stu-id="7d06a-240">Mount options</span></span>

<span data-ttu-id="7d06a-241">La définition des différentes options de montage pour les lecteurs Windows (DrvFs) peut contrôler la façon dont les autorisations de fichier sont calculées pour les fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="7d06a-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="7d06a-242">Les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="7d06a-242">The following options are available:</span></span>

| <span data-ttu-id="7d06a-243">Clé</span><span class="sxs-lookup"><span data-stu-id="7d06a-243">Key</span></span> | <span data-ttu-id="7d06a-244">Description</span><span class="sxs-lookup"><span data-stu-id="7d06a-244">Description</span></span> | <span data-ttu-id="7d06a-245">Default</span><span class="sxs-lookup"><span data-stu-id="7d06a-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="7d06a-246">uid</span><span class="sxs-lookup"><span data-stu-id="7d06a-246">uid</span></span>| <span data-ttu-id="7d06a-247">identifiant utilisateur utilisé pour le propriétaire de tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="7d06a-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="7d06a-248">identifiant utilisateur par défaut de votre distribution WSL (à la première installation, la valeur par défaut est 1000)</span><span class="sxs-lookup"><span data-stu-id="7d06a-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="7d06a-249">gid</span><span class="sxs-lookup"><span data-stu-id="7d06a-249">gid</span></span>| <span data-ttu-id="7d06a-250">identifiant de groupe utilisé pour le propriétaire de tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="7d06a-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="7d06a-251">identifiant de groupe par défaut de votre distribution WSL (à la première installation, la valeur par défaut est 1000)</span><span class="sxs-lookup"><span data-stu-id="7d06a-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="7d06a-252">umask</span><span class="sxs-lookup"><span data-stu-id="7d06a-252">umask</span></span> | <span data-ttu-id="7d06a-253">masque octal des autorisations à exclure pour tous les fichiers et répertoires</span><span class="sxs-lookup"><span data-stu-id="7d06a-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="7d06a-254">000</span><span class="sxs-lookup"><span data-stu-id="7d06a-254">000</span></span>
|<span data-ttu-id="7d06a-255">fmask</span><span class="sxs-lookup"><span data-stu-id="7d06a-255">fmask</span></span> | <span data-ttu-id="7d06a-256">masque octal des autorisations à exclure pour tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="7d06a-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="7d06a-257">000</span><span class="sxs-lookup"><span data-stu-id="7d06a-257">000</span></span>
|<span data-ttu-id="7d06a-258">dmask</span><span class="sxs-lookup"><span data-stu-id="7d06a-258">dmask</span></span> | <span data-ttu-id="7d06a-259">masque octal des autorisations à exclure pour tous les répertoires</span><span class="sxs-lookup"><span data-stu-id="7d06a-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="7d06a-260">000</span><span class="sxs-lookup"><span data-stu-id="7d06a-260">000</span></span>

<span data-ttu-id="7d06a-261">**Remarque :** Les masques d’autorisation passent par une opération OR logique avant d’être appliqués aux fichiers et aux répertoires.</span><span class="sxs-lookup"><span data-stu-id="7d06a-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="7d06a-262">réseau</span><span class="sxs-lookup"><span data-stu-id="7d06a-262">network</span></span>

<span data-ttu-id="7d06a-263">Étiquette de section : `[network]`</span><span class="sxs-lookup"><span data-stu-id="7d06a-263">Section label: `[network]`</span></span>

| <span data-ttu-id="7d06a-264">key</span><span class="sxs-lookup"><span data-stu-id="7d06a-264">key</span></span> | <span data-ttu-id="7d06a-265">value</span><span class="sxs-lookup"><span data-stu-id="7d06a-265">value</span></span> | <span data-ttu-id="7d06a-266">par défaut</span><span class="sxs-lookup"><span data-stu-id="7d06a-266">default</span></span> | <span data-ttu-id="7d06a-267">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d06a-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="7d06a-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="7d06a-268">generateHosts</span></span> | <span data-ttu-id="7d06a-269">booléen</span><span class="sxs-lookup"><span data-stu-id="7d06a-269">boolean</span></span> | `true` | <span data-ttu-id="7d06a-270">`true` : WSL génère `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="7d06a-271">Le fichier `hosts` contient une carte statique de noms d’hôtes correspondant à l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="7d06a-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="7d06a-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="7d06a-272">generateResolvConf</span></span> | <span data-ttu-id="7d06a-273">booléen</span><span class="sxs-lookup"><span data-stu-id="7d06a-273">boolean</span></span> | `true` | <span data-ttu-id="7d06a-274">`true` : WSL génère `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="7d06a-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="7d06a-275">`resolv.conf` contient une liste de noms DNS capables de résoudre un nom d’hôte donné en son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="7d06a-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="7d06a-276">interop</span><span class="sxs-lookup"><span data-stu-id="7d06a-276">interop</span></span>

<span data-ttu-id="7d06a-277">Étiquette de section : `[interop]`</span><span class="sxs-lookup"><span data-stu-id="7d06a-277">Section label: `[interop]`</span></span>

<span data-ttu-id="7d06a-278">Ces options sont disponibles dans Insider build 17713 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7d06a-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="7d06a-279">key</span><span class="sxs-lookup"><span data-stu-id="7d06a-279">key</span></span> | <span data-ttu-id="7d06a-280">value</span><span class="sxs-lookup"><span data-stu-id="7d06a-280">value</span></span> | <span data-ttu-id="7d06a-281">par défaut</span><span class="sxs-lookup"><span data-stu-id="7d06a-281">default</span></span> | <span data-ttu-id="7d06a-282">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d06a-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="7d06a-283">enabled</span><span class="sxs-lookup"><span data-stu-id="7d06a-283">enabled</span></span> | <span data-ttu-id="7d06a-284">booléen</span><span class="sxs-lookup"><span data-stu-id="7d06a-284">boolean</span></span> | `true` | <span data-ttu-id="7d06a-285">La définition de cette clé permet de déterminer si WSL prend en charge le lancement des processus Windows.</span><span class="sxs-lookup"><span data-stu-id="7d06a-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="7d06a-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="7d06a-286">appendWindowsPath</span></span> | <span data-ttu-id="7d06a-287">booléen</span><span class="sxs-lookup"><span data-stu-id="7d06a-287">boolean</span></span> | `true` | <span data-ttu-id="7d06a-288">La définition de cette clé détermine si WSL ajoute des éléments de chemin Windows à la variable d’environnement $PATH.</span><span class="sxs-lookup"><span data-stu-id="7d06a-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
