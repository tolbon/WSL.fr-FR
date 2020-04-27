---
title: Informations de référence sur les commandes du sous-système Windows pour Linux
description: Liste des commandes de gestion du sous-système Windows pour Linux
keywords: BashOnWindows, bash, wsl, Windows, sous-système Windows pour Linux, sous-système windows, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d74a6926fd797f2e1ede0fd5d8d080d0f1ce3f6b
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269841"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="79074-104">Informations de référence sur les commandes pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="79074-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="79074-105">La commande `wsl.exe` offre le meilleur moyen d’interagir avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="79074-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="79074-106">Voici une liste complète des options pouvant être utilisées avec la commande `wsl.exe` à partir de la version 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="79074-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="79074-107">Utilisation : `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="79074-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="79074-108">Arguments pour l’exécution de fichiers binaires Linux</span><span class="sxs-lookup"><span data-stu-id="79074-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="79074-109">**Sans argument**</span><span class="sxs-lookup"><span data-stu-id="79074-109">**Without arguments**</span></span>

  <span data-ttu-id="79074-110">Si aucune ligne de commande n’est fournie, wsl.exe lance le shell par défaut.</span><span class="sxs-lookup"><span data-stu-id="79074-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="79074-111">**--exec, -e \<Ligne de commande>**</span><span class="sxs-lookup"><span data-stu-id="79074-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="79074-112">Exécute la commande spécifiée sans utiliser le shell Linux par défaut.</span><span class="sxs-lookup"><span data-stu-id="79074-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="79074-113">Transmet le reste de la ligne de commande tel quel.</span><span class="sxs-lookup"><span data-stu-id="79074-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="79074-114">Les commandes ci-dessus acceptent également les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="79074-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="79074-115">**--distribution, -d \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="79074-116">Exécute la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="79074-116">Run the specified distribution.</span></span>

* <span data-ttu-id="79074-117">**--user, -u \<Nom d’utilisateur>**</span><span class="sxs-lookup"><span data-stu-id="79074-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="79074-118">Procède à l’exécution sous l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="79074-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="79074-119">Arguments pour la gestion du sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="79074-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="79074-120">**--export \<Distribution> \<Nom de fichier>**</span><span class="sxs-lookup"><span data-stu-id="79074-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="79074-121">Exporte la distribution vers un fichier tar.</span><span class="sxs-lookup"><span data-stu-id="79074-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="79074-122">Le nom de fichier peut être - pour une sortie standard.</span><span class="sxs-lookup"><span data-stu-id="79074-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="79074-123">**--import \<Distribution> \<Emplacement d’installation> \<Nom de fichier>**</span><span class="sxs-lookup"><span data-stu-id="79074-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="79074-124">Importe le fichier tar spécifié en tant que nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="79074-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="79074-125">Le nom de fichier peut être - pour une entrée standard.</span><span class="sxs-lookup"><span data-stu-id="79074-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="79074-126">**--list, -l [Options]**</span><span class="sxs-lookup"><span data-stu-id="79074-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="79074-127">Liste les distributions.</span><span class="sxs-lookup"><span data-stu-id="79074-127">Lists distributions.</span></span>

  <span data-ttu-id="79074-128">Options :</span><span class="sxs-lookup"><span data-stu-id="79074-128">Options:</span></span>
  * <span data-ttu-id="79074-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="79074-129">**--all**</span></span>
      
    <span data-ttu-id="79074-130">Liste toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="79074-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="79074-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="79074-131">**--running**</span></span>
      
    <span data-ttu-id="79074-132">Liste uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="79074-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="79074-133">**--set-default, -s \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="79074-134">Définit la distribution en tant que distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="79074-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="79074-135">**--terminate, -t \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="79074-136">Met fin à la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="79074-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="79074-137">**--unregister \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="79074-138">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="79074-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="79074-139">**--help** Affiche des informations sur l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="79074-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="79074-140">Commandes supplémentaires</span><span class="sxs-lookup"><span data-stu-id="79074-140">Additional Commands</span></span>

<span data-ttu-id="79074-141">Certaines commandes historiques permettent également d’interagir avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="79074-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="79074-142">`wsl.exe` englobe leurs fonctionnalités, mais elles restent toujours à disposition.</span><span class="sxs-lookup"><span data-stu-id="79074-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="79074-143">Cette commande vous permet de configurer votre distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="79074-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="79074-144">Voici une liste des options correspondantes.</span><span class="sxs-lookup"><span data-stu-id="79074-144">Below is a list of its options.</span></span>

<span data-ttu-id="79074-145">Utilisation : `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="79074-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="79074-146">Arguments</span><span class="sxs-lookup"><span data-stu-id="79074-146">Arguments</span></span>
* <span data-ttu-id="79074-147">**/l, /list [Options]**</span><span class="sxs-lookup"><span data-stu-id="79074-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="79074-148">Liste les distributions inscrites.</span><span class="sxs-lookup"><span data-stu-id="79074-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="79074-149">Options :</span><span class="sxs-lookup"><span data-stu-id="79074-149">Options:</span></span>
    * <span data-ttu-id="79074-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="79074-150">**/all**</span></span>
    
      <span data-ttu-id="79074-151">Liste toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation (facultatif).</span><span class="sxs-lookup"><span data-stu-id="79074-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="79074-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="79074-152">**/running**</span></span>
      
      <span data-ttu-id="79074-153">Liste uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="79074-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="79074-154">**/s, /setdefault \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="79074-155">Définit la distribution en tant que distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="79074-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="79074-156">**/t, /terminate \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="79074-157">Met fin à la distribution.</span><span class="sxs-lookup"><span data-stu-id="79074-157">Terminates the distribution.</span></span>

* <span data-ttu-id="79074-158">**/u, /unregister \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="79074-159">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="79074-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="79074-160">**/upgrade \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="79074-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="79074-161">Met à niveau la distribution vers le format du système de fichiers WslFs.</span><span class="sxs-lookup"><span data-stu-id="79074-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="79074-162">Cette commande permet de démarrer un shell Bash.</span><span class="sxs-lookup"><span data-stu-id="79074-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="79074-163">Vous trouverez ci-dessous les options que vous pouvez utiliser avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="79074-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="79074-164">Utilisation : `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="79074-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="79074-165">**Aucune option indiquée**</span><span class="sxs-lookup"><span data-stu-id="79074-165">**No Option given**</span></span>
  
  <span data-ttu-id="79074-166">Lance le shell Bash dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="79074-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="79074-167">Si le shell Bash n’est pas installé, cette commande lance automatiquement `lxrun /install`.</span><span class="sxs-lookup"><span data-stu-id="79074-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="79074-168">`bash ~` lance le shell Bash dans le répertoire de base de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79074-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="79074-169">Cette option est similaire à `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="79074-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="79074-170">**-c "\<commande>"**</span><span class="sxs-lookup"><span data-stu-id="79074-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="79074-171">Exécute la commande, affiche la sortie et revient à l’invite de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="79074-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="79074-172">Par exemple : `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="79074-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="79074-173">Commandes dépréciées</span><span class="sxs-lookup"><span data-stu-id="79074-173">Deprecated Commands</span></span>

<span data-ttu-id="79074-174">`lxrun.exe` était la première commande utilisée pour installer et gérer le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="79074-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="79074-175">Elle est dépréciée pour les versions 1803 et ultérieures de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="79074-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="79074-176">La commande `lxrun.exe` peut être utilisée pour interagir directement avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-).</span><span class="sxs-lookup"><span data-stu-id="79074-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="79074-177">Ces commandes sont installées dans le répertoire `\Windows\System32` et peuvent être exécutées dans une invite de commandes Windows ou dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79074-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="79074-178">Commande</span><span class="sxs-lookup"><span data-stu-id="79074-178">Command</span></span>                     | <span data-ttu-id="79074-179">Description</span><span class="sxs-lookup"><span data-stu-id="79074-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="79074-180">La commande lxrun est utilisée pour gérer l’instance de WSL.</span><span class="sxs-lookup"><span data-stu-id="79074-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="79074-181">Démarre le processus de téléchargement et d’installation.</span><span class="sxs-lookup"><span data-stu-id="79074-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="79074-182">**/y** peut être ajouté pour ignorer toutes les invites.</span><span class="sxs-lookup"><span data-stu-id="79074-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="79074-183">L’invite de confirmation est automatiquement acceptée et l’utilisateur par défaut est défini sur la racine.</span><span class="sxs-lookup"><span data-stu-id="79074-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="79074-184">Désinstalle et supprime l’image Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="79074-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="79074-185">Par défaut, le répertoire de base Ubuntu de l’utilisateur n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="79074-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="79074-186">**/y** peut être ajouté pour accepter automatiquement l’invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="79074-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="79074-187">**/full** désinstalle et supprime le répertoire de base Ubuntu de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="79074-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="79074-188">Définit l’utilisateur Bash sur Ubuntu par défaut.</span><span class="sxs-lookup"><span data-stu-id="79074-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="79074-189">Demande un mot de passe si l’utilisateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="79074-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="79074-190">Pour plus d’informations, consultez : https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="79074-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="79074-191">**/y** ignore la demande de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="79074-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="79074-192">L’utilisateur sera créé sans mot de passe.</span><span class="sxs-lookup"><span data-stu-id="79074-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="79074-193">Met à jour l’index du package du sous-système.</span><span class="sxs-lookup"><span data-stu-id="79074-193">Updates the subsystem's package index</span></span>          |
