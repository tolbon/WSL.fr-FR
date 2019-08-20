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
ms.openlocfilehash: 018b02b43e859476f7ee38f54df8efa0ca0e652b
ms.sourcegitcommit: 62c49d435a91f2e390c3c495f3e09e62b5ada13c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2019
ms.locfileid: "69578841"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="f775b-104">Informations de référence sur les commandes pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="f775b-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="f775b-105">La meilleure façon d’interagir avec le sous-système Windows pour Linux consiste à utiliser `wsl.exe` la commande.</span><span class="sxs-lookup"><span data-stu-id="f775b-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="f775b-106">Voici une liste contenant toutes les options lors de `wsl.exe` l’utilisation de à partir de la version 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="f775b-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="f775b-107">À`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="f775b-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="f775b-108">Arguments pour l’exécution des fichiers binaires Linux</span><span class="sxs-lookup"><span data-stu-id="f775b-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="f775b-109">**Sans arguments**</span><span class="sxs-lookup"><span data-stu-id="f775b-109">**Without arguments**</span></span>

  <span data-ttu-id="f775b-110">Si aucune ligne de commande n’est fournie, WSL. exe lance l’interpréteur de commandes par défaut.</span><span class="sxs-lookup"><span data-stu-id="f775b-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="f775b-111">**--Exec,-e \<CommandLine >**</span><span class="sxs-lookup"><span data-stu-id="f775b-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="f775b-112">Exécutez la commande spécifiée sans utiliser l’interpréteur de commandes Linux par défaut.</span><span class="sxs-lookup"><span data-stu-id="f775b-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="f775b-113">Transmettez la ligne de commande restante telle quelle.</span><span class="sxs-lookup"><span data-stu-id="f775b-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="f775b-114">Les commandes ci-dessus acceptent également les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="f775b-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="f775b-115">**--distribution,-d \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="f775b-116">Exécutez la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f775b-116">Run the specified distribution.</span></span>

* <span data-ttu-id="f775b-117">**--User,-u \<nom_utilisateur >**</span><span class="sxs-lookup"><span data-stu-id="f775b-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="f775b-118">Exécuter en tant qu’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="f775b-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="f775b-119">Arguments pour la gestion du sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="f775b-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="f775b-120">**--Export \<distribution > \<filename >**</span><span class="sxs-lookup"><span data-stu-id="f775b-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="f775b-121">Exporte la distribution vers un fichier tar.</span><span class="sxs-lookup"><span data-stu-id="f775b-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="f775b-122">Le nom de fichier peut être-pour la sortie standard.</span><span class="sxs-lookup"><span data-stu-id="f775b-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="f775b-123">**--import \<distribution > \<INSTALLLOCATION > \<nom de fichier >**</span><span class="sxs-lookup"><span data-stu-id="f775b-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="f775b-124">Importe le fichier tar spécifié en tant que nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="f775b-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="f775b-125">Le nom de fichier peut être-pour une entrée standard.</span><span class="sxs-lookup"><span data-stu-id="f775b-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="f775b-126">**--List,-l [options]**</span><span class="sxs-lookup"><span data-stu-id="f775b-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="f775b-127">Répertorie les distributions.</span><span class="sxs-lookup"><span data-stu-id="f775b-127">Lists distributions.</span></span>

  <span data-ttu-id="f775b-128">Options :</span><span class="sxs-lookup"><span data-stu-id="f775b-128">Options:</span></span>
  * <span data-ttu-id="f775b-129">**--tout**</span><span class="sxs-lookup"><span data-stu-id="f775b-129">**--all**</span></span>
      
    <span data-ttu-id="f775b-130">Répertorie toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f775b-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="f775b-131">**--en cours d’exécution**</span><span class="sxs-lookup"><span data-stu-id="f775b-131">**--running**</span></span>
      
    <span data-ttu-id="f775b-132">Répertorier uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f775b-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="f775b-133">**--Set-Default,-s \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-134">Définit la distribution comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f775b-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="f775b-135">**--Terminate,-t \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-136">Met fin à la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f775b-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="f775b-137">**--annuler l' \<inscription de la > distribution**</span><span class="sxs-lookup"><span data-stu-id="f775b-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-138">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="f775b-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="f775b-139">**--aide** Affichez les informations d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="f775b-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="f775b-140">Commandes supplémentaires</span><span class="sxs-lookup"><span data-stu-id="f775b-140">Additional Commands</span></span>

<span data-ttu-id="f775b-141">Il existe également des commandes historiques pour interagir avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="f775b-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="f775b-142">Leurs fonctionnalités sont comprises dans `wsl.exe`, mais elles peuvent toujours être utilisées.</span><span class="sxs-lookup"><span data-stu-id="f775b-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="f775b-143">Cette commande vous permet de configurer votre distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="f775b-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="f775b-144">Vous trouverez ci-dessous une liste de ses options.</span><span class="sxs-lookup"><span data-stu-id="f775b-144">Below is a list of its options.</span></span>

<span data-ttu-id="f775b-145">À`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="f775b-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="f775b-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="f775b-146">Arguments</span></span>
* <span data-ttu-id="f775b-147">**/l,/list [options]**</span><span class="sxs-lookup"><span data-stu-id="f775b-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="f775b-148">Répertorie les distributions inscrites.</span><span class="sxs-lookup"><span data-stu-id="f775b-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="f775b-149">Options :</span><span class="sxs-lookup"><span data-stu-id="f775b-149">Options:</span></span>
    * <span data-ttu-id="f775b-150">**All**</span><span class="sxs-lookup"><span data-stu-id="f775b-150">**/all**</span></span>
    
      <span data-ttu-id="f775b-151">Répertoriez éventuellement toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="f775b-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="f775b-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="f775b-152">**/running**</span></span>
      
      <span data-ttu-id="f775b-153">Répertorier uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f775b-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="f775b-154">**/s,/SetDefault \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-155">Définit la distribution comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="f775b-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="f775b-156">**/t,/Terminate \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-157">Met fin à la distribution.</span><span class="sxs-lookup"><span data-stu-id="f775b-157">Terminates the distribution.</span></span>

* <span data-ttu-id="f775b-158">**/u,/Unregister \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-159">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="f775b-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="f775b-160">**/Upgrade \<distribution >**</span><span class="sxs-lookup"><span data-stu-id="f775b-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="f775b-161">Met à niveau la distribution vers le format du système de fichiers WslFs.</span><span class="sxs-lookup"><span data-stu-id="f775b-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="f775b-162">Cette commande permet de démarrer un interpréteur de commandes bash.</span><span class="sxs-lookup"><span data-stu-id="f775b-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="f775b-163">Vous trouverez ci-dessous les options que vous pouvez utiliser avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="f775b-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="f775b-164">À`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="f775b-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="f775b-165">**Aucune option donnée**</span><span class="sxs-lookup"><span data-stu-id="f775b-165">**No Option given**</span></span>
  
  <span data-ttu-id="f775b-166">Lance l’interpréteur de commandes bash dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="f775b-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="f775b-167">Si l’interpréteur de commandes bash n’est pas installé automatiquement`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="f775b-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="f775b-168">`bash ~`lance l’interpréteur de commandes bash dans le répertoire de départ de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f775b-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="f775b-169">Similaire à l' `cd ~`exécution de.</span><span class="sxs-lookup"><span data-stu-id="f775b-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="f775b-170">**-c "\<> de commande"**</span><span class="sxs-lookup"><span data-stu-id="f775b-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="f775b-171">Exécute la commande, imprime la sortie et quitte l’invite de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="f775b-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="f775b-172">Exemple: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="f775b-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="f775b-173">Commandes déconseillées</span><span class="sxs-lookup"><span data-stu-id="f775b-173">Deprecated Commands</span></span>

<span data-ttu-id="f775b-174">`lxrun.exe` Était la première commande utilisée pour installer et gérer le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="f775b-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="f775b-175">Elle est déconseillée à partir de Windows 10 1803 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="f775b-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="f775b-176">La commande `lxrun.exe` peut être utilisée pour interagir directement avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .</span><span class="sxs-lookup"><span data-stu-id="f775b-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="f775b-177">Ces commandes sont installées dans `\Windows\System32` le répertoire et peuvent être exécutées dans une invite de commandes Windows ou dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f775b-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="f775b-178">Command</span><span class="sxs-lookup"><span data-stu-id="f775b-178">Command</span></span>                     | <span data-ttu-id="f775b-179">Description</span><span class="sxs-lookup"><span data-stu-id="f775b-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="f775b-180">La commande lxrun est utilisée pour gérer l’instance WSL.</span><span class="sxs-lookup"><span data-stu-id="f775b-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="f775b-181">Démarre le processus de téléchargement et d’installation.</span><span class="sxs-lookup"><span data-stu-id="f775b-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="f775b-182">**/y** peut être ajouté pour ignorer toutes les invites.</span><span class="sxs-lookup"><span data-stu-id="f775b-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="f775b-183">L’invite de confirmation est automatiquement acceptée et l’utilisateur par défaut est défini sur root.</span><span class="sxs-lookup"><span data-stu-id="f775b-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="f775b-184">Désinstalle et supprime l’image Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f775b-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="f775b-185">Par défaut, cela ne supprime pas le répertoire d’hébergement Ubuntu de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f775b-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="f775b-186">**/y** peut être ajouté pour accepter automatiquement l’invite de confirmation</span><span class="sxs-lookup"><span data-stu-id="f775b-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="f775b-187">**/Full** désinstalle et supprime le répertoire de démarrage Ubuntu de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f775b-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="f775b-188">Définit le bash par défaut sur l’utilisateur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="f775b-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="f775b-189">Demande un mot de passe si l’utilisateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="f775b-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="f775b-190">Pour plus d’informations, https://aka.ms/wslusers visitez le site:.</span><span class="sxs-lookup"><span data-stu-id="f775b-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="f775b-191">**/y** Ignore promping pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f775b-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="f775b-192">L’utilisateur sera créé sans mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f775b-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="f775b-193">Met à jour l’index du package du sous-système</span><span class="sxs-lookup"><span data-stu-id="f775b-193">Updates the subsystem's package index</span></span>          |
