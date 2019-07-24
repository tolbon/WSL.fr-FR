---
title: Informations de référence sur les commandes du sous-système Windows pour Linux
description: Liste des commandes qui gèrent le sous-système Windows pour Linux
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307653"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="08a89-104">Informations de référence sur les commandes pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="08a89-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="08a89-105">La meilleure façon d’interagir avec le sous-système Windows pour Linux consiste à utiliser `wsl.exe` la commande.</span><span class="sxs-lookup"><span data-stu-id="08a89-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="08a89-106">Voici une liste contenant toutes les options lors de `wsl.exe` l’utilisation de à partir de la version 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="08a89-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="08a89-107">Arguments pour l’exécution des fichiers binaires Linux:</span><span class="sxs-lookup"><span data-stu-id="08a89-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="08a89-108">Si aucune ligne de commande n’est fournie, WSL. exe lance l’interpréteur de commandes par défaut.</span><span class="sxs-lookup"><span data-stu-id="08a89-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="08a89-109">--Exec,-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="08a89-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="08a89-110">Exécutez la commande spécifiée sans utiliser l’interpréteur de commandes Linux par défaut.</span><span class="sxs-lookup"><span data-stu-id="08a89-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="08a89-111">Transmettez la ligne de commande restante telle quelle.</span><span class="sxs-lookup"><span data-stu-id="08a89-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="08a89-112">Options :</span><span class="sxs-lookup"><span data-stu-id="08a89-112">Options:</span></span>
    * <span data-ttu-id="08a89-113">--distribution,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="08a89-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="08a89-114">Exécutez la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="08a89-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="08a89-115">--utilisateur,-u<UserName></span><span class="sxs-lookup"><span data-stu-id="08a89-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="08a89-116">Exécuter en tant qu’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="08a89-116">Run as the specified user.</span></span>

* <span data-ttu-id="08a89-117">Arguments pour la gestion du sous-système Windows pour Linux:</span><span class="sxs-lookup"><span data-stu-id="08a89-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="08a89-118">--exporter <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="08a89-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="08a89-119">Exporte la distribution vers un fichier tar.</span><span class="sxs-lookup"><span data-stu-id="08a89-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="08a89-120">Le nom de fichier peut être-pour la sortie standard.</span><span class="sxs-lookup"><span data-stu-id="08a89-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="08a89-121">--import <Distro> <InstallLocation>[options <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="08a89-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="08a89-122">Importe le fichier tar spécifié en tant que nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="08a89-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="08a89-123">Le nom de fichier peut être-pour une entrée standard.</span><span class="sxs-lookup"><span data-stu-id="08a89-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="08a89-124">Options :</span><span class="sxs-lookup"><span data-stu-id="08a89-124">Options:</span></span>
            * <span data-ttu-id="08a89-125">--version <Version> spécifie la version à utiliser pour la nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="08a89-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="08a89-126">--List,-l [options]</span><span class="sxs-lookup"><span data-stu-id="08a89-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="08a89-127">Répertorie les distributions.</span><span class="sxs-lookup"><span data-stu-id="08a89-127">Lists distributions.</span></span>

        * <span data-ttu-id="08a89-128">Options :</span><span class="sxs-lookup"><span data-stu-id="08a89-128">Options:</span></span>
            * <span data-ttu-id="08a89-129">--tout</span><span class="sxs-lookup"><span data-stu-id="08a89-129">--all</span></span>
                * <span data-ttu-id="08a89-130">Répertorie toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="08a89-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="08a89-131">--en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="08a89-131">--running</span></span>
                * <span data-ttu-id="08a89-132">Répertorier uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="08a89-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="08a89-133">--Set-Default,-s<Distro></span><span class="sxs-lookup"><span data-stu-id="08a89-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="08a89-134">Définit la distribution comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="08a89-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="08a89-135">--set-default-version<Version></span><span class="sxs-lookup"><span data-stu-id="08a89-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="08a89-136">Modifie la version d’installation par défaut pour les nouvelles distributions.</span><span class="sxs-lookup"><span data-stu-id="08a89-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="08a89-137">--set-version <Distro><Version></span><span class="sxs-lookup"><span data-stu-id="08a89-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="08a89-138">Modifie la version de la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="08a89-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="08a89-139">--Terminate,-t<Distro></span><span class="sxs-lookup"><span data-stu-id="08a89-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="08a89-140">Met fin à la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="08a89-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="08a89-141">--annuler l’inscription<Distro></span><span class="sxs-lookup"><span data-stu-id="08a89-141">--unregister <Distro></span></span>
        * <span data-ttu-id="08a89-142">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="08a89-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="08a89-143">--help</span><span class="sxs-lookup"><span data-stu-id="08a89-143">--help</span></span>
        * <span data-ttu-id="08a89-144">Affichez les informations d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="08a89-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="08a89-145">Commandes supplémentaires</span><span class="sxs-lookup"><span data-stu-id="08a89-145">Additional Commands</span></span>

<span data-ttu-id="08a89-146">Il existe également des commandes historiques pour interagir avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="08a89-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="08a89-147">Leurs fonctionnalités sont comprises dans `wsl.exe`, mais elles peuvent toujours être utilisées.</span><span class="sxs-lookup"><span data-stu-id="08a89-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="08a89-148">Cette commande vous permet de configurer votre distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="08a89-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="08a89-149">Vous trouverez ci-dessous une liste de ses options.</span><span class="sxs-lookup"><span data-stu-id="08a89-149">Below is a list of its options.</span></span>

* <span data-ttu-id="08a89-150">/l,/list [option]</span><span class="sxs-lookup"><span data-stu-id="08a89-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="08a89-151">Répertorie les distributions inscrites.</span><span class="sxs-lookup"><span data-stu-id="08a89-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="08a89-152">/All: répertorie éventuellement toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="08a89-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="08a89-153">/Running-répertorier uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="08a89-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="08a89-154">/s,/SetDefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="08a89-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="08a89-155">Définit la distribution comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="08a89-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="08a89-156">/t,/Terminate<DistributionName></span><span class="sxs-lookup"><span data-stu-id="08a89-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="08a89-157">Met fin à la distribution.</span><span class="sxs-lookup"><span data-stu-id="08a89-157">Terminates the distribution.</span></span>

* <span data-ttu-id="08a89-158">/u,/Unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="08a89-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="08a89-159">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="08a89-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="08a89-160">Cette commande permet de démarrer un interpréteur de commandes bash.</span><span class="sxs-lookup"><span data-stu-id="08a89-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="08a89-161">Vous trouverez ci-dessous les options que vous pouvez utiliser avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="08a89-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="08a89-162">Aucune option donnée</span><span class="sxs-lookup"><span data-stu-id="08a89-162">No Option given</span></span>
    * <span data-ttu-id="08a89-163">Lance l’interpréteur de commandes bash dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="08a89-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="08a89-164">Si l’interpréteur de commandes bash n’est pas installé automatiquement`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="08a89-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="08a89-165">bash ~</span><span class="sxs-lookup"><span data-stu-id="08a89-165">bash ~</span></span>
    * <span data-ttu-id="08a89-166">Lance l’interpréteur de commandes bash dans le répertoire de départ de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08a89-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="08a89-167">Similaire à l' `cd ~`exécution de.</span><span class="sxs-lookup"><span data-stu-id="08a89-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="08a89-168">bash-c "&lt;commande&gt;"</span><span class="sxs-lookup"><span data-stu-id="08a89-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="08a89-169">Exécute la commande, imprime la sortie et quitte l’invite de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="08a89-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="08a89-170">Tels`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="08a89-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="08a89-171">Commandes déconseillées</span><span class="sxs-lookup"><span data-stu-id="08a89-171">Deprecated Commands</span></span>

<span data-ttu-id="08a89-172">`lxrun.exe` Était la première commande utilisée pour installer et gérer le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="08a89-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="08a89-173">Elle est déconseillée à partir de Windows 10 1803 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="08a89-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="08a89-174">La commande `lxrun.exe` peut être utilisée pour interagir directement avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .</span><span class="sxs-lookup"><span data-stu-id="08a89-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="08a89-175">Ces commandes sont installées dans `\Windows\System32` le répertoire et peuvent être exécutées dans une invite de commandes Windows ou dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="08a89-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="08a89-176">Command</span><span class="sxs-lookup"><span data-stu-id="08a89-176">Command</span></span>                     | <span data-ttu-id="08a89-177">Description</span><span class="sxs-lookup"><span data-stu-id="08a89-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="08a89-178">La commande lxrun est utilisée pour gérer l’instance WSL.</span><span class="sxs-lookup"><span data-stu-id="08a89-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="08a89-179">Démarre le processus de téléchargement et d’installation.</span><span class="sxs-lookup"><span data-stu-id="08a89-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="08a89-180">**/y** peut être ajouté pour ignorer toutes les invites.</span><span class="sxs-lookup"><span data-stu-id="08a89-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="08a89-181">L’invite de confirmation est automatiquement acceptée et l’utilisateur par défaut est défini sur root.</span><span class="sxs-lookup"><span data-stu-id="08a89-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="08a89-182">Désinstalle et supprime l’image Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08a89-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="08a89-183">Par défaut, cela ne supprime pas le répertoire d’hébergement Ubuntu de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="08a89-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="08a89-184">**/y** peut être ajouté pour accepter automatiquement l’invite de confirmation</span><span class="sxs-lookup"><span data-stu-id="08a89-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="08a89-185">**/Full** désinstalle et supprime le répertoire de démarrage Ubuntu de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="08a89-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="08a89-186">Définit le bash par défaut sur l’utilisateur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="08a89-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="08a89-187">Demande un mot de passe si l’utilisateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="08a89-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="08a89-188">Pour plus d’informations, https://aka.ms/wslusers visitez le site:.</span><span class="sxs-lookup"><span data-stu-id="08a89-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="08a89-189">**/y** Ignore promping pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="08a89-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="08a89-190">L’utilisateur sera créé sans mot de passe.</span><span class="sxs-lookup"><span data-stu-id="08a89-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="08a89-191">Met à jour l’index du package du sous-système</span><span class="sxs-lookup"><span data-stu-id="08a89-191">Updates the subsystem's package index</span></span>          |
