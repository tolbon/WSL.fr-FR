---
title: Gérer les distributions Linux
description: Lister les références et configurer plusieurs distributions Linux exécutées sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: e97b1030d5891bf8aa1cb656646a4d9e1d480a3d
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336082"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="f279c-104">Commandes WSL et configurations de lancement</span><span class="sxs-lookup"><span data-stu-id="f279c-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="f279c-105">Méthodes d’exécution de WSL</span><span class="sxs-lookup"><span data-stu-id="f279c-105">Ways to run WSL</span></span>

<span data-ttu-id="f279c-106">Il existe plusieurs façons d’exécuter une distribution Linux avec WSL une fois qu’elle est [installée](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="f279c-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="f279c-107">Ouvrez votre distribution Linux en visitant le menu Démarrer de Windows et en tapant le nom de vos distributions installées.</span><span class="sxs-lookup"><span data-stu-id="f279c-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="f279c-108">Par exemple : « Ubuntu ».</span><span class="sxs-lookup"><span data-stu-id="f279c-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="f279c-109">À partir de l’invite de commandes Windows ou de PowerShell, entrez le nom de votre distribution installée.</span><span class="sxs-lookup"><span data-stu-id="f279c-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="f279c-110">Par exemple : `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="f279c-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="f279c-111">À partir de l’invite de commandes Windows ou de PowerShell, pour ouvrir votre distribution Linux par défaut à l’intérieur de la ligne de commande actuelle, entrez : `wsl.exe` .</span><span class="sxs-lookup"><span data-stu-id="f279c-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="f279c-112">À partir de l’invite de commandes Windows ou de PowerShell, pour ouvrir votre distribution Linux par défaut à l’intérieur de la ligne de commande actuelle, entrez : `wsl [command]` .</span><span class="sxs-lookup"><span data-stu-id="f279c-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="f279c-113">La méthode que vous devez utiliser dépend de ce que vous faites.</span><span class="sxs-lookup"><span data-stu-id="f279c-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="f279c-114">Si vous avez ouvert une ligne de commande WSL dans une fenêtre d’invite de commandes Windows ou PowerShell et que vous souhaitez quitter, entrez la commande suivante : `exit` .</span><span class="sxs-lookup"><span data-stu-id="f279c-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="f279c-115">Lancer WSL par distribution</span><span class="sxs-lookup"><span data-stu-id="f279c-115">Launch WSL by distribution</span></span>

<span data-ttu-id="f279c-116">L’exécution d’une distribution à l’aide de son application spécifique à la distribution lance cette distribution dans sa propre fenêtre de console.</span><span class="sxs-lookup"><span data-stu-id="f279c-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

<span data-ttu-id="f279c-118">Cela revient à cliquer sur « Lancer » dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f279c-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Lancer WSL à partir du Microsoft Store](media/store-launch.png)

<span data-ttu-id="f279c-120">Vous pouvez également exécuter la distribution à partir de la ligne de commande en exécutant `[distribution].exe`.</span><span class="sxs-lookup"><span data-stu-id="f279c-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="f279c-121">L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon est qu’elle définit automatiquement votre répertoire de travail sur le répertoire de base de la distribution.</span><span class="sxs-lookup"><span data-stu-id="f279c-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="f279c-122">**Exemple : (à l’aide de PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f279c-122">**Example: (using PowerShell)**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="f279c-123">wsl et wsl [commande]</span><span class="sxs-lookup"><span data-stu-id="f279c-123">wsl and wsl [command]</span></span>

<span data-ttu-id="f279c-124">La meilleure façon d’exécuter WSL à partir de la ligne de commande consiste à utiliser `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="f279c-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="f279c-125">**Exemple : (à l’aide de PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f279c-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="f279c-126">Non seulement l’utilitaire `wsl` conserve le répertoire de travail actuel, mais il vous permet d’exécuter une seule commande à côté de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="f279c-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="f279c-127">**Exemple : (à l’aide de PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f279c-127">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

<span data-ttu-id="f279c-128">**Exemple : (à l’aide de PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f279c-128">**Example: (using PowerShell)**</span></span>

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

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="f279c-129">Gestion de plusieurs distributions Linux</span><span class="sxs-lookup"><span data-stu-id="f279c-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="f279c-130">Dans Windows 10 version 1903 [et versions ultérieures](ms-settings:windowsupdate), vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), notamment pour répertorier les distributions disponibles, définir une distribution par défaut et désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="f279c-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="f279c-131">Chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="f279c-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="f279c-132">Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="f279c-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="f279c-133">Par exemple, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="f279c-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="f279c-134">Lister les distributions</span><span class="sxs-lookup"><span data-stu-id="f279c-134">List distributions</span></span>

<span data-ttu-id="f279c-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="f279c-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="f279c-136">Liste les distributions Linux disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="f279c-137">Si une distribution est listée, elle est installée et prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="f279c-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="f279c-138">`wsl --list --all`Répertorie toutes les distributions, y compris celles qui ne sont pas actuellement utilisables.</span><span class="sxs-lookup"><span data-stu-id="f279c-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="f279c-139">Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.</span><span class="sxs-lookup"><span data-stu-id="f279c-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="f279c-140">`wsl --list --running`Répertorie toutes les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f279c-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="f279c-141">Définir une distribution par défaut</span><span class="sxs-lookup"><span data-stu-id="f279c-141">Set a default distribution</span></span>

<span data-ttu-id="f279c-142">La distribution WSL par défaut est celle qui s’exécute quand vous exécutez `wsl` depuis une ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="f279c-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="f279c-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="f279c-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="f279c-144">Définit la distribution par défaut sur `<DistributionName>`.</span><span class="sxs-lookup"><span data-stu-id="f279c-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="f279c-145">**Exemple : (à l’aide de PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f279c-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="f279c-146">`wsl -s Ubuntu` définit ma distribution par défaut sur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f279c-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="f279c-147">À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f279c-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="f279c-148">Si j’exécute `wsl`, une session Ubuntu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f279c-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="f279c-149">Désinscrire et réinstaller une distribution</span><span class="sxs-lookup"><span data-stu-id="f279c-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="f279c-150">Les distributions Linux peuvent être installées par l’intermédiaire du Microsoft Store, mais elles ne peuvent pas être désinstallées par ce biais.</span><span class="sxs-lookup"><span data-stu-id="f279c-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="f279c-151">WSL Config permet de désinscrire/désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="f279c-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="f279c-152">La désinscription permet également de réinstaller les distributions.</span><span class="sxs-lookup"><span data-stu-id="f279c-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="f279c-153">**Attention :** Une fois l’inscription annulée, toutes les données, tous les paramètres et tous les logiciels associés à cette distribution seront définitivement perdus.</span><span class="sxs-lookup"><span data-stu-id="f279c-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="f279c-154">La réinstallation à partir du Store installe une nouvelle copie de la distribution.</span><span class="sxs-lookup"><span data-stu-id="f279c-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="f279c-155">Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="f279c-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="f279c-156">Par exemple : `wsl --unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="f279c-157">Quand j’exécute `wsl --list`, celui-ci n’est pas listé.</span><span class="sxs-lookup"><span data-stu-id="f279c-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="f279c-158">Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».</span><span class="sxs-lookup"><span data-stu-id="f279c-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="f279c-159">Exécuter en tant qu’utilisateur spécifique</span><span class="sxs-lookup"><span data-stu-id="f279c-159">Run as a specific user</span></span>

<span data-ttu-id="f279c-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="f279c-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="f279c-161">Exécutez WSL en tant qu’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f279c-161">Run WSL as the specified user.</span></span> <span data-ttu-id="f279c-162">Notez que l’utilisateur doit exister dans la distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="change-the-default-user-for-a-distribution"></a><span data-ttu-id="f279c-163">Modifier l’utilisateur par défaut pour une distribution</span><span class="sxs-lookup"><span data-stu-id="f279c-163">Change the default user for a distribution</span></span>

`<DistributionName> config --default-user <Username>`

<span data-ttu-id="f279c-164">Modifiez l’utilisateur par défaut de votre journal de distribution.</span><span class="sxs-lookup"><span data-stu-id="f279c-164">Change the default user that for your distribution log-in.</span></span> <span data-ttu-id="f279c-165">L’utilisateur doit déjà exister à l’intérieur de la distribution afin de devenir l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f279c-165">The user has to already exist inside the distribution in order to become the default user.</span></span> 

<span data-ttu-id="f279c-166">Par exemple : `ubuntu config --default-user johndoe` modifier l’utilisateur par défaut de la distribution Ubuntu pour l’utilisateur « JohnDoe ».</span><span class="sxs-lookup"><span data-stu-id="f279c-166">For example: `ubuntu config --default-user johndoe` would change the default user for the Ubuntu distribution to the "johndoe" user.</span></span>

> [!NOTE]
> <span data-ttu-id="f279c-167">Si vous avez des difficultés à déterminer le nom de votre distribution, consultez la section [répertorier les distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) de la commande pour répertorier le nom officiel des distributions installées.</span><span class="sxs-lookup"><span data-stu-id="f279c-167">If you are having trouble figuring out the name of your distribution, see [List distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) for the command to list the official name of the installed distributions.</span></span> 

## <a name="run-a-specific-distribution"></a><span data-ttu-id="f279c-168">Exécuter une distribution spécifique</span><span class="sxs-lookup"><span data-stu-id="f279c-168">Run a specific distribution</span></span>

<span data-ttu-id="f279c-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="f279c-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="f279c-170">Exécutez une distribution spécifiée de WSL ; cette opération peut être utilisée pour envoyer des commandes à une distribution spécifique sans avoir à changer la distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="f279c-170">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="f279c-171">Gestion de plusieurs distributions Linux dans des versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="f279c-171">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="f279c-172">Dans Windows 10 antérieures à la version 1903, l' `wslconfig.exe` outil en ligne de commande WSL config () doit être utilisé pour gérer les distributions Linux exécutées sur le sous-système Windows pour Linux (WSL).</span><span class="sxs-lookup"><span data-stu-id="f279c-172">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="f279c-173">Il vous permet de lister les distributions disponibles, de définir une distribution par défaut et de désinstaller des distributions.</span><span class="sxs-lookup"><span data-stu-id="f279c-173">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="f279c-174">Même si WSL Config est utile pour les paramètres qui englobent ou coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.</span><span class="sxs-lookup"><span data-stu-id="f279c-174">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="f279c-175">Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="f279c-175">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="f279c-176">Par exemple, `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="f279c-176">For example `ubuntu /?`.</span></span>

<span data-ttu-id="f279c-177">Pour voir toutes les options disponibles pour wslconfig, exécutez : `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="f279c-177">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

<span data-ttu-id="f279c-178">Pour répertorier les distributions, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f279c-178">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="f279c-179">Liste les distributions Linux disponibles pour WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-179">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="f279c-180">Si une distribution est listée, elle est installée et prête à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="f279c-180">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="f279c-181">Liste toutes les distributions, y compris celles qui ne sont pas utilisables.</span><span class="sxs-lookup"><span data-stu-id="f279c-181">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="f279c-182">Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.</span><span class="sxs-lookup"><span data-stu-id="f279c-182">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="f279c-183">Pour définir une distribution par défaut qui s’exécute lorsque vous exécutez `wsl` sur une ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="f279c-183">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="f279c-184">`wslconfig /setdefault <DistributionName>`Définit la distribution par défaut sur `<DistributionName>` .</span><span class="sxs-lookup"><span data-stu-id="f279c-184">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="f279c-185">**Exemple : (à l’aide de PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f279c-185">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="f279c-186">`wslconfig /setdefault Ubuntu` définit ma distribution par défaut sur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f279c-186">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="f279c-187">À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f279c-187">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="f279c-188">Si j’exécute `wsl`, une session Ubuntu s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="f279c-188">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="f279c-189">Pour annuler l’inscription et réinstaller une distribution :</span><span class="sxs-lookup"><span data-stu-id="f279c-189">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="f279c-190">Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.</span><span class="sxs-lookup"><span data-stu-id="f279c-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="f279c-191">Par exemple : `wslconfig /unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="f279c-192">Quand j’exécute `wslconfig /list`, celui-ci n’est pas listé.</span><span class="sxs-lookup"><span data-stu-id="f279c-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="f279c-193">Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».</span><span class="sxs-lookup"><span data-stu-id="f279c-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="f279c-194">Configurer les paramètres de lancement de distribution avec wslconf</span><span class="sxs-lookup"><span data-stu-id="f279c-194">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="f279c-195">**Disponible dans Windows Build 17093 et versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="f279c-195">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="f279c-196">Configurez automatiquement certaines fonctionnalités dans WSL afin de les appliquer chaque fois que vous lancez le sous-système à l’aide de `wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="f279c-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="f279c-197">Pour le moment, cela comprend les options de montage automatique et la configuration réseau.</span><span class="sxs-lookup"><span data-stu-id="f279c-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="f279c-198">`wsl.conf` se trouve dans chaque distribution Linux dans `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="f279c-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="f279c-199">Si le fichier n’y est pas, vous pouvez le créer vous-même.</span><span class="sxs-lookup"><span data-stu-id="f279c-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="f279c-200">WSL détecte l’existence du fichier et lit son contenu.</span><span class="sxs-lookup"><span data-stu-id="f279c-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="f279c-201">Si le fichier est manquant ou incorrect (mise en forme incorrecte du balisage), WSL continue à se lancer normalement.</span><span class="sxs-lookup"><span data-stu-id="f279c-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="f279c-202">Voici un exemple de `wsl.conf` fichier que vous pouvez ajouter à vos distributions :</span><span class="sxs-lookup"><span data-stu-id="f279c-202">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="f279c-203">Options de configuration</span><span class="sxs-lookup"><span data-stu-id="f279c-203">Configuration Options</span></span>

<span data-ttu-id="f279c-204">Conformément aux conventions .ini, les clés sont déclarées sous une section.</span><span class="sxs-lookup"><span data-stu-id="f279c-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="f279c-205">WSL prend en charge deux sections : `automount` et `network`.</span><span class="sxs-lookup"><span data-stu-id="f279c-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="f279c-206">automount</span><span class="sxs-lookup"><span data-stu-id="f279c-206">automount</span></span>

<span data-ttu-id="f279c-207">Section : `[automount]`</span><span class="sxs-lookup"><span data-stu-id="f279c-207">Section: `[automount]`</span></span>

| <span data-ttu-id="f279c-208">key</span><span class="sxs-lookup"><span data-stu-id="f279c-208">key</span></span>        | <span data-ttu-id="f279c-209">value</span><span class="sxs-lookup"><span data-stu-id="f279c-209">value</span></span>                          | <span data-ttu-id="f279c-210">default</span><span class="sxs-lookup"><span data-stu-id="f279c-210">default</span></span>      | <span data-ttu-id="f279c-211">Remarques</span><span class="sxs-lookup"><span data-stu-id="f279c-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f279c-212">enabled</span><span class="sxs-lookup"><span data-stu-id="f279c-212">enabled</span></span>    | <span data-ttu-id="f279c-213">booléen</span><span class="sxs-lookup"><span data-stu-id="f279c-213">boolean</span></span>                        | <span data-ttu-id="f279c-214">true</span><span class="sxs-lookup"><span data-stu-id="f279c-214">true</span></span>         | <span data-ttu-id="f279c-215">`true` : les lecteurs fixes (c.-à-d.</span><span class="sxs-lookup"><span data-stu-id="f279c-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="f279c-216">`C:/` ou `D:/`) sont automatiquement montés avec DrvFs sous `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="f279c-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="f279c-217">`false`signifie que les disques ne seront pas montés automatiquement, mais vous pouvez les monter manuellement ou via `fstab` .</span><span class="sxs-lookup"><span data-stu-id="f279c-217">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="f279c-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="f279c-218">mountFsTab</span></span> | <span data-ttu-id="f279c-219">booléen</span><span class="sxs-lookup"><span data-stu-id="f279c-219">boolean</span></span>                        | <span data-ttu-id="f279c-220">true</span><span class="sxs-lookup"><span data-stu-id="f279c-220">true</span></span>         | <span data-ttu-id="f279c-221">`true` : `/etc/fstab` est traité au démarrage de WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="f279c-222">/etc/fstab est un fichier dans lequel vous pouvez déclarer d’autres systèmes de fichiers, comme un partage SMB.</span><span class="sxs-lookup"><span data-stu-id="f279c-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="f279c-223">Ainsi, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage.</span><span class="sxs-lookup"><span data-stu-id="f279c-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="f279c-224">root</span><span class="sxs-lookup"><span data-stu-id="f279c-224">root</span></span>       | <span data-ttu-id="f279c-225">String</span><span class="sxs-lookup"><span data-stu-id="f279c-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="f279c-226">Définit le répertoire dans lequel les lecteurs fixes sont montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f279c-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="f279c-227">Par exemple, si vous avez un répertoire dans WSL à l’emplacement `/windir/` et que vous le spécifiez en tant que racine, vos lecteurs fixes sont censés être montés à l’emplacement `/windir/c`.</span><span class="sxs-lookup"><span data-stu-id="f279c-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="f279c-228">options</span><span class="sxs-lookup"><span data-stu-id="f279c-228">options</span></span>    | <span data-ttu-id="f279c-229">Liste de valeurs séparées par des virgules</span><span class="sxs-lookup"><span data-stu-id="f279c-229">comma-separated list of values</span></span> | <span data-ttu-id="f279c-230">Chaîne vide</span><span class="sxs-lookup"><span data-stu-id="f279c-230">empty string</span></span> | <span data-ttu-id="f279c-231">Cette valeur est ajoutée à la chaîne des options de montage DrvFs par défaut.</span><span class="sxs-lookup"><span data-stu-id="f279c-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="f279c-232">**Seules les options propres à DrvFs peuvent être spécifiées.**</span><span class="sxs-lookup"><span data-stu-id="f279c-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="f279c-233">Les options que le fichier binaire de montage analyse normalement dans un indicateur ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f279c-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="f279c-234">Si vous souhaitez spécifier explicitement ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans /etc/fstab.</span><span class="sxs-lookup"><span data-stu-id="f279c-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="f279c-235">Par défaut, WSL définit les options uid et gid sur la valeur de l’utilisateur par défaut (dans une distribution Ubuntu, l’utilisateur par défaut est créé avec uid=1000,gid=1000).</span><span class="sxs-lookup"><span data-stu-id="f279c-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="f279c-236">Si l’utilisateur spécifie une option gid ou uid explicitement par le biais de cette clé, la valeur associée est remplacée.</span><span class="sxs-lookup"><span data-stu-id="f279c-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="f279c-237">Dans le cas contraire, la valeur par défaut est toujours ajoutée.</span><span class="sxs-lookup"><span data-stu-id="f279c-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="f279c-238">**Remarque :** Ces options sont appliquées en tant qu’options de montage pour tous les lecteurs montés automatiquement.</span><span class="sxs-lookup"><span data-stu-id="f279c-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="f279c-239">Pour changer les options d’un lecteur spécifique uniquement, utilisez /etc/fstab à la place.</span><span class="sxs-lookup"><span data-stu-id="f279c-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="f279c-240">Options de montage</span><span class="sxs-lookup"><span data-stu-id="f279c-240">Mount options</span></span>

<span data-ttu-id="f279c-241">La définition des différentes options de montage pour les lecteurs Windows (DrvFs) peut contrôler la façon dont les autorisations de fichier sont calculées pour les fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="f279c-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="f279c-242">Les options suivantes sont disponibles :</span><span class="sxs-lookup"><span data-stu-id="f279c-242">The following options are available:</span></span>

| <span data-ttu-id="f279c-243">Clé</span><span class="sxs-lookup"><span data-stu-id="f279c-243">Key</span></span> | <span data-ttu-id="f279c-244">Description</span><span class="sxs-lookup"><span data-stu-id="f279c-244">Description</span></span> | <span data-ttu-id="f279c-245">Par défaut</span><span class="sxs-lookup"><span data-stu-id="f279c-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="f279c-246">uid</span><span class="sxs-lookup"><span data-stu-id="f279c-246">uid</span></span>| <span data-ttu-id="f279c-247">identifiant utilisateur utilisé pour le propriétaire de tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="f279c-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="f279c-248">identifiant utilisateur par défaut de votre distribution WSL (à la première installation, la valeur par défaut est 1000)</span><span class="sxs-lookup"><span data-stu-id="f279c-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="f279c-249">gid</span><span class="sxs-lookup"><span data-stu-id="f279c-249">gid</span></span>| <span data-ttu-id="f279c-250">identifiant de groupe utilisé pour le propriétaire de tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="f279c-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="f279c-251">identifiant de groupe par défaut de votre distribution WSL (à la première installation, la valeur par défaut est 1000)</span><span class="sxs-lookup"><span data-stu-id="f279c-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="f279c-252">umask</span><span class="sxs-lookup"><span data-stu-id="f279c-252">umask</span></span> | <span data-ttu-id="f279c-253">masque octal des autorisations à exclure pour tous les fichiers et répertoires</span><span class="sxs-lookup"><span data-stu-id="f279c-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="f279c-254">000</span><span class="sxs-lookup"><span data-stu-id="f279c-254">000</span></span>
|<span data-ttu-id="f279c-255">fmask</span><span class="sxs-lookup"><span data-stu-id="f279c-255">fmask</span></span> | <span data-ttu-id="f279c-256">masque octal des autorisations à exclure pour tous les fichiers</span><span class="sxs-lookup"><span data-stu-id="f279c-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="f279c-257">000</span><span class="sxs-lookup"><span data-stu-id="f279c-257">000</span></span>
|<span data-ttu-id="f279c-258">dmask</span><span class="sxs-lookup"><span data-stu-id="f279c-258">dmask</span></span> | <span data-ttu-id="f279c-259">masque octal des autorisations à exclure pour tous les répertoires</span><span class="sxs-lookup"><span data-stu-id="f279c-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="f279c-260">000</span><span class="sxs-lookup"><span data-stu-id="f279c-260">000</span></span>

<span data-ttu-id="f279c-261">**Remarque :** Les masques d’autorisation passent par une opération OR logique avant d’être appliqués aux fichiers et aux répertoires.</span><span class="sxs-lookup"><span data-stu-id="f279c-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="f279c-262">réseau</span><span class="sxs-lookup"><span data-stu-id="f279c-262">network</span></span>

<span data-ttu-id="f279c-263">Étiquette de section : `[network]`</span><span class="sxs-lookup"><span data-stu-id="f279c-263">Section label: `[network]`</span></span>

| <span data-ttu-id="f279c-264">key</span><span class="sxs-lookup"><span data-stu-id="f279c-264">key</span></span> | <span data-ttu-id="f279c-265">value</span><span class="sxs-lookup"><span data-stu-id="f279c-265">value</span></span> | <span data-ttu-id="f279c-266">default</span><span class="sxs-lookup"><span data-stu-id="f279c-266">default</span></span> | <span data-ttu-id="f279c-267">Remarques</span><span class="sxs-lookup"><span data-stu-id="f279c-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f279c-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="f279c-268">generateHosts</span></span> | <span data-ttu-id="f279c-269">booléen</span><span class="sxs-lookup"><span data-stu-id="f279c-269">boolean</span></span> | `true` | <span data-ttu-id="f279c-270">`true` : WSL génère `/etc/hosts`.</span><span class="sxs-lookup"><span data-stu-id="f279c-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="f279c-271">Le fichier `hosts` contient une carte statique de noms d’hôtes correspondant à l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="f279c-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="f279c-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="f279c-272">generateResolvConf</span></span> | <span data-ttu-id="f279c-273">booléen</span><span class="sxs-lookup"><span data-stu-id="f279c-273">boolean</span></span> | `true` | <span data-ttu-id="f279c-274">`true` : WSL génère `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="f279c-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="f279c-275">`resolv.conf` contient une liste de noms DNS capables de résoudre un nom d’hôte donné en son adresse IP.</span><span class="sxs-lookup"><span data-stu-id="f279c-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="f279c-276">interop</span><span class="sxs-lookup"><span data-stu-id="f279c-276">interop</span></span>

<span data-ttu-id="f279c-277">Étiquette de section : `[interop]`</span><span class="sxs-lookup"><span data-stu-id="f279c-277">Section label: `[interop]`</span></span>

<span data-ttu-id="f279c-278">Ces options sont disponibles dans Insider build 17713 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f279c-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="f279c-279">key</span><span class="sxs-lookup"><span data-stu-id="f279c-279">key</span></span> | <span data-ttu-id="f279c-280">value</span><span class="sxs-lookup"><span data-stu-id="f279c-280">value</span></span> | <span data-ttu-id="f279c-281">default</span><span class="sxs-lookup"><span data-stu-id="f279c-281">default</span></span> | <span data-ttu-id="f279c-282">Remarques</span><span class="sxs-lookup"><span data-stu-id="f279c-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f279c-283">enabled</span><span class="sxs-lookup"><span data-stu-id="f279c-283">enabled</span></span> | <span data-ttu-id="f279c-284">booléen</span><span class="sxs-lookup"><span data-stu-id="f279c-284">boolean</span></span> | `true` | <span data-ttu-id="f279c-285">La définition de cette clé permet de déterminer si WSL prend en charge le lancement des processus Windows.</span><span class="sxs-lookup"><span data-stu-id="f279c-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="f279c-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="f279c-286">appendWindowsPath</span></span> | <span data-ttu-id="f279c-287">booléen</span><span class="sxs-lookup"><span data-stu-id="f279c-287">boolean</span></span> | `true` | <span data-ttu-id="f279c-288">La définition de cette clé détermine si WSL ajoute des éléments de chemin Windows à la variable d’environnement $PATH.</span><span class="sxs-lookup"><span data-stu-id="f279c-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="f279c-289">utilisateur</span><span class="sxs-lookup"><span data-stu-id="f279c-289">user</span></span>

<span data-ttu-id="f279c-290">Étiquette de section : `[user]`</span><span class="sxs-lookup"><span data-stu-id="f279c-290">Section label: `[user]`</span></span>

<span data-ttu-id="f279c-291">Ces options sont disponibles dans Build 18980 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f279c-291">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="f279c-292">key</span><span class="sxs-lookup"><span data-stu-id="f279c-292">key</span></span> | <span data-ttu-id="f279c-293">value</span><span class="sxs-lookup"><span data-stu-id="f279c-293">value</span></span> | <span data-ttu-id="f279c-294">default</span><span class="sxs-lookup"><span data-stu-id="f279c-294">default</span></span> | <span data-ttu-id="f279c-295">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f279c-295">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f279c-296">default</span><span class="sxs-lookup"><span data-stu-id="f279c-296">default</span></span> | <span data-ttu-id="f279c-297">string</span><span class="sxs-lookup"><span data-stu-id="f279c-297">string</span></span> | <span data-ttu-id="f279c-298">Nom d’utilisateur initial créé lors de la première exécution</span><span class="sxs-lookup"><span data-stu-id="f279c-298">The initial username created on first run</span></span> | <span data-ttu-id="f279c-299">La définition de cette clé spécifie l’utilisateur à exécuter comme lors du premier démarrage d’une session WSL.</span><span class="sxs-lookup"><span data-stu-id="f279c-299">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="f279c-300">Configurer des options globales avec. wslconfig</span><span class="sxs-lookup"><span data-stu-id="f279c-300">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="f279c-301">**Disponible dans Windows Build 19041 et versions ultérieures**</span><span class="sxs-lookup"><span data-stu-id="f279c-301">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="f279c-302">Vous pouvez configurer des options globales de WSL en plaçant un `.wslconfig` fichier dans le répertoire racine de votre dossier utilisateurs : `C:\Users\<yourUserName>\.wslconfig` .</span><span class="sxs-lookup"><span data-stu-id="f279c-302">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="f279c-303">La plupart de ces fichiers sont liés à WSL 2. n’oubliez pas que vous devrez peut-être exécuter `wsl --shutdown` pour arrêter la machine virtuelle WSL 2, puis redémarrer votre instance WSL pour que ces modifications prennent effet.</span><span class="sxs-lookup"><span data-stu-id="f279c-303">Many of these files are related to WSL 2, please keep in mind you may need to run `wsl --shutdown` to shut down the WSL 2 VM and then restart your WSL instance for these changes to take affect.</span></span>

<span data-ttu-id="f279c-304">Voici un exemple de fichier. wslconfig :</span><span class="sxs-lookup"><span data-stu-id="f279c-304">Here is a sample .wslconfig file:</span></span>

```console
[wsl2]
kernel=C:\\temp\\myCustomKernel
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```

<span data-ttu-id="f279c-305">Ce fichier peut contenir les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="f279c-305">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="f279c-306">Paramètres WSL 2</span><span class="sxs-lookup"><span data-stu-id="f279c-306">WSL 2 Settings</span></span>

<span data-ttu-id="f279c-307">Étiquette de section : `[wsl2]`</span><span class="sxs-lookup"><span data-stu-id="f279c-307">Section label: `[wsl2]`</span></span>

<span data-ttu-id="f279c-308">Ces paramètres affectent la machine virtuelle qui alimente toute distribution WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f279c-308">These settings affect the VM that powers any WSL 2 distribution.</span></span>

| <span data-ttu-id="f279c-309">key</span><span class="sxs-lookup"><span data-stu-id="f279c-309">key</span></span> | <span data-ttu-id="f279c-310">value</span><span class="sxs-lookup"><span data-stu-id="f279c-310">value</span></span> | <span data-ttu-id="f279c-311">default</span><span class="sxs-lookup"><span data-stu-id="f279c-311">default</span></span> | <span data-ttu-id="f279c-312">HDInsight</span><span class="sxs-lookup"><span data-stu-id="f279c-312">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f279c-313">noyau</span><span class="sxs-lookup"><span data-stu-id="f279c-313">kernel</span></span> | <span data-ttu-id="f279c-314">string</span><span class="sxs-lookup"><span data-stu-id="f279c-314">string</span></span> | <span data-ttu-id="f279c-315">Boîte de réception fournie par le noyau Microsoft</span><span class="sxs-lookup"><span data-stu-id="f279c-315">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="f279c-316">Chemin Windows absolu vers un noyau Linux personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f279c-316">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="f279c-317">memory</span><span class="sxs-lookup"><span data-stu-id="f279c-317">memory</span></span> | <span data-ttu-id="f279c-318">taille</span><span class="sxs-lookup"><span data-stu-id="f279c-318">size</span></span> | <span data-ttu-id="f279c-319">80% de la mémoire totale sur Windows</span><span class="sxs-lookup"><span data-stu-id="f279c-319">80% of your total memory on Windows</span></span> | <span data-ttu-id="f279c-320">Quantité de mémoire à affecter à la machine virtuelle WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f279c-320">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="f279c-321">processeurs</span><span class="sxs-lookup"><span data-stu-id="f279c-321">processors</span></span> | <span data-ttu-id="f279c-322">nombre</span><span class="sxs-lookup"><span data-stu-id="f279c-322">number</span></span> | <span data-ttu-id="f279c-323">Le même nombre de processeurs sur Windows</span><span class="sxs-lookup"><span data-stu-id="f279c-323">The same number of processors on Windows</span></span> | <span data-ttu-id="f279c-324">Nombre de processeurs à affecter à la machine virtuelle WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f279c-324">How many processors to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="f279c-325">localhostForwarding</span><span class="sxs-lookup"><span data-stu-id="f279c-325">localhostForwarding</span></span> | <span data-ttu-id="f279c-326">boolean</span><span class="sxs-lookup"><span data-stu-id="f279c-326">boolean</span></span> | `true` | <span data-ttu-id="f279c-327">Valeur booléenne spécifiant si les ports liés à un caractère générique ou localhost dans la machine virtuelle WSL 2 doivent être connectés à partir de l’hôte via localhost : port.</span><span class="sxs-lookup"><span data-stu-id="f279c-327">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="f279c-328">kernelCommandLine</span><span class="sxs-lookup"><span data-stu-id="f279c-328">kernelCommandLine</span></span> | <span data-ttu-id="f279c-329">string</span><span class="sxs-lookup"><span data-stu-id="f279c-329">string</span></span> | <span data-ttu-id="f279c-330">Vide</span><span class="sxs-lookup"><span data-stu-id="f279c-330">Blank</span></span> | <span data-ttu-id="f279c-331">Arguments de ligne de commande du noyau supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f279c-331">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="f279c-332">swap</span><span class="sxs-lookup"><span data-stu-id="f279c-332">swap</span></span> | <span data-ttu-id="f279c-333">taille</span><span class="sxs-lookup"><span data-stu-id="f279c-333">size</span></span> | <span data-ttu-id="f279c-334">25% de la taille de la mémoire sur Windows arrondie aux Go les plus proches</span><span class="sxs-lookup"><span data-stu-id="f279c-334">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="f279c-335">Espace d’échange à ajouter à la machine virtuelle WSL 2, 0 pour aucun fichier d’échange.</span><span class="sxs-lookup"><span data-stu-id="f279c-335">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="f279c-336">Échange</span><span class="sxs-lookup"><span data-stu-id="f279c-336">swapFile</span></span> | <span data-ttu-id="f279c-337">string</span><span class="sxs-lookup"><span data-stu-id="f279c-337">string</span></span> | <span data-ttu-id="f279c-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span><span class="sxs-lookup"><span data-stu-id="f279c-338">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="f279c-339">Chemin d’accès Windows absolu au disque dur virtuel d’échange.</span><span class="sxs-lookup"><span data-stu-id="f279c-339">An absolute Windows path to the swap virtual hard disk.</span></span> |

<span data-ttu-id="f279c-340">Les entrées avec la `path` valeur doivent être des chemins d’accès Windows avec des barres obliques inverses par échappement, par exemple :`C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="f279c-340">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="f279c-341">Les entrées avec la `size` valeur doivent être une taille suivie d’une unité, par exemple `8GB` ou `512MB` .</span><span class="sxs-lookup"><span data-stu-id="f279c-341">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>
