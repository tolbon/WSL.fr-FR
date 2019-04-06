---
title: Gérer les Distributions de Linux
description: Référencer le listing et la configuration de plusieurs distributions de Linux en cours d’exécution sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063497"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="d2070-104">Gérer et configurer le sous-système de Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="d2070-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="d2070-105">S’applique à Windows 10 Fall Creators Update et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d2070-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="d2070-106">Consultez notre mise à jour [guide d’installation](./install_guide.md) pour essayer les nouvelles fonctionnalités de gestion et de démarrer plusieurs distributions de Linux en cours d’exécution à partir du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d2070-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="d2070-107">Façons d’exécuter WSL</span><span class="sxs-lookup"><span data-stu-id="d2070-107">Ways to run WSL</span></span>

<span data-ttu-id="d2070-108">Il existe de nombreuses façons d’exécuter Linux avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="d2070-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. `[distro]` <span data-ttu-id="d2070-109">ie</span><span class="sxs-lookup"><span data-stu-id="d2070-109">ie</span></span> `ubuntu`
1. `wsl.exe` <span data-ttu-id="d2070-110">ou Gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="d2070-110">or</span></span> `bash.exe`
1. `wsl [command]` <span data-ttu-id="d2070-111">ou Gestionnaire de configuration</span><span class="sxs-lookup"><span data-stu-id="d2070-111">or</span></span> `bash -c [command]`

<span data-ttu-id="d2070-112">Quelle méthode vous devez utiliser dépend de ce que vous faites.</span><span class="sxs-lookup"><span data-stu-id="d2070-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="d2070-113">Lancez WSL par distribution</span><span class="sxs-lookup"><span data-stu-id="d2070-113">Launch WSL by distribution</span></span>

<span data-ttu-id="d2070-114">Une distribution à l’aide de son application de distribution spécifique en cours d’exécution lance cette distribution dans sa propre fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="d2070-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

<span data-ttu-id="d2070-116">Il est le même qu’un clic sur « Lancement » dans le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d2070-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![Lancer WSL à partir du Windows Store](media/store-launch.png)

<span data-ttu-id="d2070-118">Vous pouvez également exécuter la distribution à partir de la ligne de commande en exécutant `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="d2070-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="d2070-119">L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon, qu’il remplace automatiquement votre répertoire de travail à partir du répertoire actuel au répertoire de base de la distribution.</span><span class="sxs-lookup"><span data-stu-id="d2070-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

**<span data-ttu-id="d2070-120">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d2070-120">Example:</span></span>**

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="d2070-121">wsl et wsl [commande]</span><span class="sxs-lookup"><span data-stu-id="d2070-121">wsl and wsl [command]</span></span>

<span data-ttu-id="d2070-122">À l’aide de la meilleure façon d’exécuter WSL à partir de la ligne de commande `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="d2070-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

**<span data-ttu-id="d2070-123">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d2070-123">Example:</span></span>**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="d2070-124">Non seulement `wsl` conserver le répertoire de travail en place, il vous permet d’exécuter une seule commande le long de commandes Windows de côté.</span><span class="sxs-lookup"><span data-stu-id="d2070-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

**<span data-ttu-id="d2070-125">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d2070-125">Example:</span></span>**

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

**<span data-ttu-id="d2070-126">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d2070-126">Example:</span></span>**

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="d2070-127">La gestion de plusieurs Distributions Linux</span><span class="sxs-lookup"><span data-stu-id="d2070-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="d2070-128">Windows 10 Version 1903 et versions ultérieure</span><span class="sxs-lookup"><span data-stu-id="d2070-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="d2070-129">Vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), y compris la liste des distributions disponibles, la définition d’une distribution par défaut et la désinstallation de distributions.</span><span class="sxs-lookup"><span data-stu-id="d2070-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="d2070-130">Chaque distribution Linux gère indépendamment de sa propre configuration.</span><span class="sxs-lookup"><span data-stu-id="d2070-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="d2070-131">Pour afficher des commandes spécifiques à la distribution, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="d2070-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="d2070-132">Par exemple : `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="d2070-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="d2070-133">Distributions de liste</span><span class="sxs-lookup"><span data-stu-id="d2070-133">List distributions</span></span>

`wsl -l` <span data-ttu-id="d2070-134">,</span><span class="sxs-lookup"><span data-stu-id="d2070-134">,</span></span> `wsl --list`  
<span data-ttu-id="d2070-135">Listes disponibles distributions de Linux sont disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="d2070-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="d2070-136">Si une distribution est répertoriée, il est installé et prêt à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d2070-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="d2070-137">Répertorie toutes les distributions, y compris ceux qui ne sont pas actuellement utilisable.</span><span class="sxs-lookup"><span data-stu-id="d2070-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="d2070-138">Ils peuvent être en train d’installer, désinstaller, ou sont dans un état interrompu.</span><span class="sxs-lookup"><span data-stu-id="d2070-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="d2070-139">Répertorie toutes les distributions qui sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="d2070-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="d2070-140">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="d2070-140">Set a default distribution</span></span>

<span data-ttu-id="d2070-141">La distribution de WSL par défaut est celui qui s’exécute lorsque vous exécutez `wsl` sur une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d2070-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wsl -s <DistributionName>`<span data-ttu-id="d2070-142">,</span><span class="sxs-lookup"><span data-stu-id="d2070-142">,</span></span> `wsl --setdefault <DistributionName>`

<span data-ttu-id="d2070-143">Définit la distribution par défaut `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="d2070-143">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="d2070-144">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d2070-144">Example:</span></span>**  
`wsl -s Ubuntu` <span data-ttu-id="d2070-145">Définissez mon distribution par défaut d’Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2070-145">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="d2070-146">Maintenant lors de l’exécution `wsl npm init` il s’exécutera sous Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2070-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="d2070-147">Si j’exécute `wsl` il ouvrira une session d’Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2070-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="d2070-148">Annuler l’inscription et de réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="d2070-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="d2070-149">Linux distributions peuvent être installées via le Windows lors de la banque, ils ne peut pas être désinstallés via le Windows store.</span><span class="sxs-lookup"><span data-stu-id="d2070-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="d2070-150">WSL Config permet des distributions soit désinscrit ou désinstallé.</span><span class="sxs-lookup"><span data-stu-id="d2070-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="d2070-151">Annuler l’inscription permet également de distributions être réinstallé.</span><span class="sxs-lookup"><span data-stu-id="d2070-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="d2070-152">**Attention :** Une fois la désinscription, toutes les données, les paramètres et les logiciels associés à cette distribution seront définitivement perdues.</span><span class="sxs-lookup"><span data-stu-id="d2070-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="d2070-153">La réinstallation à partir du magasin installera une nouvelle copie de la distribution.</span><span class="sxs-lookup"><span data-stu-id="d2070-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="d2070-154">Annule l’inscription de la distribution à partir de WSL afin de pouvoir être réinstallé ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="d2070-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="d2070-155">Par exemple : `wsl -unregister Ubuntu` supprimerait Ubuntu à partir des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="d2070-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="d2070-156">Lors de l’exécution `wsl --list` il ne sera pas répertorié.</span><span class="sxs-lookup"><span data-stu-id="d2070-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="d2070-157">Pour réinstaller, recherchez la répartition dans le Windows Store et sélectionnez « Lancement ».</span><span class="sxs-lookup"><span data-stu-id="d2070-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="d2070-158">Exécuter en tant qu’un utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="d2070-158">Run as a specific user</span></span>

`wsl -u <Username>`<span data-ttu-id="d2070-159">,</span><span class="sxs-lookup"><span data-stu-id="d2070-159">,</span></span> `wsl --user <Username>`

<span data-ttu-id="d2070-160">Exécutez WSL en tant que l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="d2070-160">Run WSL as the specified user.</span></span> <span data-ttu-id="d2070-161">Veuillez noter que l’utilisateur doit exister à l’intérieur de la distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="d2070-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="d2070-162">Exécutez une distribution spécifique</span><span class="sxs-lookup"><span data-stu-id="d2070-162">Run a specific distribution</span></span>

`wsl --d <DistributionName>`<span data-ttu-id="d2070-163">,</span><span class="sxs-lookup"><span data-stu-id="d2070-163">,</span></span> `wsl --distribution <DistributionName>`

<span data-ttu-id="d2070-164">Exécutez une distribution spécifiée de WSL, peut être utilisé pour envoyer des commandes à une distribution spécifique sans avoir à modifier votre valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d2070-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="d2070-165">Versions antérieures à Windows 10 Version 1903</span><span class="sxs-lookup"><span data-stu-id="d2070-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="d2070-166">Configuration de WSL (`wslconfig.exe`) est un outil de ligne de commande pour la gestion des distributions de Linux en cours d’exécution sur le sous-système Windows pour Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="d2070-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="d2070-167">Il vous permet de répertorier des distributions disponibles, définir une distribution par défaut et désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="d2070-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="d2070-168">Tandis que la configuration de WSL est utile pour les paramètres qui s’étendent sur ou de coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="d2070-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="d2070-169">Pour afficher des commandes spécifiques à la distribution, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="d2070-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="d2070-170">Par exemple : `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="d2070-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="d2070-171">Pour afficher toutes les options disponibles pour wslconfig, exécutez :</span><span class="sxs-lookup"><span data-stu-id="d2070-171">To see all available options for wslconfig, run:</span></span>  `wslconfig /?`

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

#### <a name="list-distributions"></a><span data-ttu-id="d2070-172">Distributions de liste</span><span class="sxs-lookup"><span data-stu-id="d2070-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="d2070-173">Listes disponibles distributions de Linux sont disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="d2070-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="d2070-174">Si une distribution est répertoriée, il est installé et prêt à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d2070-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="d2070-175">Répertorie toutes les distributions, y compris ceux qui ne sont pas actuellement utilisable.</span><span class="sxs-lookup"><span data-stu-id="d2070-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="d2070-176">Ils peuvent être en train d’installer, désinstaller, ou sont dans un état interrompu.</span><span class="sxs-lookup"><span data-stu-id="d2070-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="d2070-177">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="d2070-177">Set a default distribution</span></span>

<span data-ttu-id="d2070-178">La distribution de WSL par défaut est celui qui s’exécute lorsque vous exécutez `wsl` sur une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d2070-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="d2070-179">Définit la distribution par défaut `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="d2070-179">Sets the default distribution to `<DistributionName>`.</span></span>

**<span data-ttu-id="d2070-180">Exemple :</span><span class="sxs-lookup"><span data-stu-id="d2070-180">Example:</span></span>**  
`wslconfig /setdefault Ubuntu` <span data-ttu-id="d2070-181">Définissez mon distribution par défaut d’Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2070-181">would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="d2070-182">Maintenant lors de l’exécution `wsl npm init` il s’exécutera sous Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2070-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="d2070-183">Si j’exécute `wsl` il ouvrira une session d’Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="d2070-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="d2070-184">Annuler l’inscription et de réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="d2070-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="d2070-185">Linux distributions peuvent être installées via le Windows lors de la banque, ils ne peut pas être désinstallés via le Windows store.</span><span class="sxs-lookup"><span data-stu-id="d2070-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="d2070-186">WSL Config permet des distributions soit désinscrit ou désinstallé.</span><span class="sxs-lookup"><span data-stu-id="d2070-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="d2070-187">Annuler l’inscription permet également de distributions être réinstallé.</span><span class="sxs-lookup"><span data-stu-id="d2070-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="d2070-188">**Attention :** Une fois la désinscription, toutes les données, les paramètres et les logiciels associés à cette distribution seront définitivement perdues.</span><span class="sxs-lookup"><span data-stu-id="d2070-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="d2070-189">La réinstallation à partir du magasin installera une nouvelle copie de la distribution.</span><span class="sxs-lookup"><span data-stu-id="d2070-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="d2070-190">Annule l’inscription de la distribution à partir de WSL afin de pouvoir être réinstallé ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="d2070-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="d2070-191">Par exemple : `wslconfig /unregister Ubuntu` supprimerait Ubuntu à partir des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="d2070-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="d2070-192">Lors de l’exécution `wslconfig /list` il ne sera pas répertorié.</span><span class="sxs-lookup"><span data-stu-id="d2070-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="d2070-193">Pour réinstaller, recherchez la répartition dans le Windows Store et sélectionnez « Lancement ».</span><span class="sxs-lookup"><span data-stu-id="d2070-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="d2070-194">Définir les paramètres de lancement WSL</span><span class="sxs-lookup"><span data-stu-id="d2070-194">Set WSL launch settings</span></span>

> **<span data-ttu-id="d2070-195">Disponible dans Windows Insider Build 17093 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="d2070-195">Available in Windows Insider Build 17093 and later</span></span>**

<span data-ttu-id="d2070-196">Configurer automatiquement certaines fonctionnalités dans WSL qui est appliqué chaque fois que vous lancez le sous-système à l’aide `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="d2070-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="d2070-197">Droite, cela inclut désormais des options de montage automatique et la configuration du réseau.</span><span class="sxs-lookup"><span data-stu-id="d2070-197">Right now, this includes automount options and network configuration.</span></span>

`wsl.conf` <span data-ttu-id="d2070-198">se trouve dans chaque distribution Linux dans `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="d2070-198">is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="d2070-199">Si le fichier n’y ne figure pas, vous pouvez le créer vous-même.</span><span class="sxs-lookup"><span data-stu-id="d2070-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="d2070-200">WSL détecte l’existence du fichier et lit son contenu.</span><span class="sxs-lookup"><span data-stu-id="d2070-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="d2070-201">Si le fichier est manquante ou incorrecte (autrement dit, incorrecte balisage mise en forme), WSL continuera à lancer comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="d2070-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="d2070-202">Voici un exemple `wsl.conf` fichier que vous pouvez ajouter dans vos distributions :</span><span class="sxs-lookup"><span data-stu-id="d2070-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="d2070-203">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="d2070-203">Configuration Options</span></span>

<span data-ttu-id="d2070-204">Conformément aux conventions .ini, les clés sont déclarés dans une section.</span><span class="sxs-lookup"><span data-stu-id="d2070-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="d2070-205">WSL prend en charge les deux sections : `automount` et `network`.</span><span class="sxs-lookup"><span data-stu-id="d2070-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="d2070-206">Montage automatique</span><span class="sxs-lookup"><span data-stu-id="d2070-206">automount</span></span>

<span data-ttu-id="d2070-207">Section :</span><span class="sxs-lookup"><span data-stu-id="d2070-207">Section:</span></span> `[automount]`


| <span data-ttu-id="d2070-208">Clé</span><span class="sxs-lookup"><span data-stu-id="d2070-208">key</span></span>        | <span data-ttu-id="d2070-209">valeur</span><span class="sxs-lookup"><span data-stu-id="d2070-209">value</span></span>                          | <span data-ttu-id="d2070-210">par défaut</span><span class="sxs-lookup"><span data-stu-id="d2070-210">default</span></span>      | <span data-ttu-id="d2070-211">notes</span><span class="sxs-lookup"><span data-stu-id="d2070-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2070-212">enabled</span><span class="sxs-lookup"><span data-stu-id="d2070-212">enabled</span></span>    | <span data-ttu-id="d2070-213">booléen</span><span class="sxs-lookup"><span data-stu-id="d2070-213">boolean</span></span>                        | <span data-ttu-id="d2070-214">true</span><span class="sxs-lookup"><span data-stu-id="d2070-214">true</span></span>         | `true` <span data-ttu-id="d2070-215">causes fixé de lecteurs (ex.)</span><span class="sxs-lookup"><span data-stu-id="d2070-215">causes fixed drives (i.e</span></span> `C:/` <span data-ttu-id="d2070-216">ou `D:/`) soit monté automatiquement avec DrvFs sous `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="d2070-216">or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  `false` <span data-ttu-id="d2070-217">signifie que les lecteurs ne sont pas automatiquement montés, mais vous pouvez toujours Montez-les manuellement ou via `fstab`.</span><span class="sxs-lookup"><span data-stu-id="d2070-217">means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="d2070-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="d2070-218">mountFsTab</span></span> | <span data-ttu-id="d2070-219">booléen</span><span class="sxs-lookup"><span data-stu-id="d2070-219">boolean</span></span>                        | <span data-ttu-id="d2070-220">true</span><span class="sxs-lookup"><span data-stu-id="d2070-220">true</span></span>         | `true` <span data-ttu-id="d2070-221">définit `/etc/fstab` à traiter au démarrage WSL.</span><span class="sxs-lookup"><span data-stu-id="d2070-221">sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="d2070-222">/ etc/fstab est un fichier dans lequel vous pouvez déclarer des autres systèmes de fichiers, comme un partage SMB.</span><span class="sxs-lookup"><span data-stu-id="d2070-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="d2070-223">Par conséquent, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage de.</span><span class="sxs-lookup"><span data-stu-id="d2070-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="d2070-224">Racine</span><span class="sxs-lookup"><span data-stu-id="d2070-224">root</span></span>       | <span data-ttu-id="d2070-225">Chaîne</span><span class="sxs-lookup"><span data-stu-id="d2070-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="d2070-226">Définit le répertoire dans lequel les lecteurs fixes seront automatiquement montés.</span><span class="sxs-lookup"><span data-stu-id="d2070-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="d2070-227">Par exemple, si vous avez un répertoire dans WSL à `/windir/` et que vous spécifiez comme racine, vous pourriez l’exiger voir votre montés sur les lecteurs fixes</span><span class="sxs-lookup"><span data-stu-id="d2070-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at</span></span> `/windir/c`                                                                                              |
| <span data-ttu-id="d2070-228">options</span><span class="sxs-lookup"><span data-stu-id="d2070-228">options</span></span>    | <span data-ttu-id="d2070-229">virgule comme séparateur de liste de valeurs</span><span class="sxs-lookup"><span data-stu-id="d2070-229">comma-separated list of values</span></span> | <span data-ttu-id="d2070-230">Chaîne vide</span><span class="sxs-lookup"><span data-stu-id="d2070-230">empty string</span></span> | <span data-ttu-id="d2070-231">Cette valeur est ajoutée à la chaîne par défaut des options de montage de DrvFs.</span><span class="sxs-lookup"><span data-stu-id="d2070-231">This value is appended to the default DrvFs mount options string.</span></span> **<span data-ttu-id="d2070-232">Uniquement les options DrvFs spécifiques peuvent être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="d2070-232">Only DrvFs-specific options can be specified.</span></span>** <span data-ttu-id="d2070-233">Options qui le montage binaire est alors normalement analysée en un indicateur ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d2070-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="d2070-234">Si vous souhaitez explicitement spécifier ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="d2070-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="d2070-235">Par défaut, WSL définit l’uid et gid à la valeur de l’utilisateur par défaut (dans la distribution Ubuntu, l’utilisateur par défaut est créé avec un ID utilisateur = 1000, gid = 1000).</span><span class="sxs-lookup"><span data-stu-id="d2070-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="d2070-236">Si l’utilisateur spécifie une option gid ou uid explicitement par le biais de cette clé, la valeur associée est remplacée.</span><span class="sxs-lookup"><span data-stu-id="d2070-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="d2070-237">Sinon, la valeur par défaut est toujours ajoutée.</span><span class="sxs-lookup"><span data-stu-id="d2070-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="d2070-238">**Remarque :** Ces options sont appliquées en tant que les options de montage pour tous les lecteurs montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="d2070-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="d2070-239">Pour modifier les options pour un lecteur spécifique uniquement, utilisez plutôt/etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="d2070-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="d2070-240">réseau</span><span class="sxs-lookup"><span data-stu-id="d2070-240">network</span></span>

<span data-ttu-id="d2070-241">Étiquette de la section :</span><span class="sxs-lookup"><span data-stu-id="d2070-241">Section label:</span></span> `[network]`

| <span data-ttu-id="d2070-242">Clé</span><span class="sxs-lookup"><span data-stu-id="d2070-242">key</span></span> | <span data-ttu-id="d2070-243">valeur</span><span class="sxs-lookup"><span data-stu-id="d2070-243">value</span></span> | <span data-ttu-id="d2070-244">par défaut</span><span class="sxs-lookup"><span data-stu-id="d2070-244">default</span></span> | <span data-ttu-id="d2070-245">notes</span><span class="sxs-lookup"><span data-stu-id="d2070-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d2070-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="d2070-246">generateHosts</span></span> | <span data-ttu-id="d2070-247">booléen</span><span class="sxs-lookup"><span data-stu-id="d2070-247">boolean</span></span> | `true` | `true` <span data-ttu-id="d2070-248">définit WSL pour générer `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="d2070-248">sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="d2070-249">Le `hosts` fichier contient un mappage statique de l’adresse IP correspondante de noms d’hôte.</span><span class="sxs-lookup"><span data-stu-id="d2070-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="d2070-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="d2070-250">generateResolvConf</span></span> | <span data-ttu-id="d2070-251">booléen</span><span class="sxs-lookup"><span data-stu-id="d2070-251">boolean</span></span> | `true` | `true` <span data-ttu-id="d2070-252">Définissez WSL pour générer `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="d2070-252">set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="d2070-253">Le `resolv.conf` contient une liste DNS qui sont capables de résoudre un nom d’hôte donné à son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="d2070-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="d2070-254">Interop</span><span class="sxs-lookup"><span data-stu-id="d2070-254">interop</span></span>

<span data-ttu-id="d2070-255">Étiquette de la section :</span><span class="sxs-lookup"><span data-stu-id="d2070-255">Section label:</span></span> `[interop]`

<span data-ttu-id="d2070-256">Ces options sont disponibles dans les initiés Build 17713 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d2070-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="d2070-257">Clé</span><span class="sxs-lookup"><span data-stu-id="d2070-257">key</span></span> | <span data-ttu-id="d2070-258">valeur</span><span class="sxs-lookup"><span data-stu-id="d2070-258">value</span></span> | <span data-ttu-id="d2070-259">par défaut</span><span class="sxs-lookup"><span data-stu-id="d2070-259">default</span></span> | <span data-ttu-id="d2070-260">notes</span><span class="sxs-lookup"><span data-stu-id="d2070-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="d2070-261">enabled</span><span class="sxs-lookup"><span data-stu-id="d2070-261">enabled</span></span> | <span data-ttu-id="d2070-262">booléen</span><span class="sxs-lookup"><span data-stu-id="d2070-262">boolean</span></span> | `true` | <span data-ttu-id="d2070-263">Paramètre de cette clé déterminent si WSL prendra en charge les processus de lancement Windows.</span><span class="sxs-lookup"><span data-stu-id="d2070-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="d2070-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="d2070-264">appendWindowsPath</span></span> | <span data-ttu-id="d2070-265">booléen</span><span class="sxs-lookup"><span data-stu-id="d2070-265">boolean</span></span> | `true` | <span data-ttu-id="d2070-266">Paramètre de cette clé déterminent si WSL ajoute des éléments de chemin d’accès de Windows à la variable d’environnement $PATH.</span><span class="sxs-lookup"><span data-stu-id="d2070-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
