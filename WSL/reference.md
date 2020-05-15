---
title: Informations de référence sur les commandes du sous-système Windows pour Linux
description: Liste des commandes de gestion du sous-système Windows pour Linux
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows pour Linux, sous-système Windows, Ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 72b78a73bf68b28dd14b4826943a0c81ea04bbad
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270873"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="a9922-104">Informations de référence sur les commandes pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="a9922-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="a9922-105">La commande `wsl.exe` offre le meilleur moyen d’interagir avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="a9922-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span>

## <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="a9922-106">Définir WSL 2 comme version par défaut</span><span class="sxs-lookup"><span data-stu-id="a9922-106">Set WSL 2 as your default version</span></span>

<span data-ttu-id="a9922-107">Exécutez la commande suivante dans PowerShell pour définir WSL 2 comme version par défaut lors de l’installation d’une nouvelle distribution Linux :</span><span class="sxs-lookup"><span data-stu-id="a9922-107">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="a9922-108">Définir votre version de distribution sur WSL 1 ou WSL 2</span><span class="sxs-lookup"><span data-stu-id="a9922-108">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="a9922-109">Vous pouvez vérifier la version WSL affectée à chacune des distributions Linux que vous avez installées en ouvrant la ligne de commande PowerShell et en entrant la commande (disponible uniquement dans la [build Windows 19041 ou ultérieure](ms-settings:windowsupdate)) : `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="a9922-109">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```bash
wsl --list --verbose
```

<span data-ttu-id="a9922-110">Pour définir une distribution devant reposer sur l’une ou l’autre des versions WSL, exécutez :</span><span class="sxs-lookup"><span data-stu-id="a9922-110">To set a distribution to be backed by either version of WSL please run:</span></span>

```bash
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="a9922-111">Veillez à remplacer `<distribution name>` par le vrai nom de votre distribution et `<versionNumber>` par le chiffre « 1 » ou « 2 ».</span><span class="sxs-lookup"><span data-stu-id="a9922-111">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="a9922-112">Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».</span><span class="sxs-lookup"><span data-stu-id="a9922-112">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="a9922-113">Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="a9922-113">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```bash
wsl --set-default-version 2
```

<span data-ttu-id="a9922-114">Cela permet de définir la version de toute nouvelle distribution installée sur WSL 2.</span><span class="sxs-lookup"><span data-stu-id="a9922-114">This will set the version of any new distribution installed to WSL 2.</span></span>

## `wsl.exe`

<span data-ttu-id="a9922-115">Voici une liste complète des options pouvant être utilisées avec la commande `wsl.exe` à partir de la version 1903 de Windows.</span><span class="sxs-lookup"><span data-stu-id="a9922-115">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="a9922-116">Utilisation : `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="a9922-116">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-commands"></a><span data-ttu-id="a9922-117">Arguments pour l’exécution de commandes Linux</span><span class="sxs-lookup"><span data-stu-id="a9922-117">Arguments for running Linux commands</span></span>

* <span data-ttu-id="a9922-118">**Sans argument**</span><span class="sxs-lookup"><span data-stu-id="a9922-118">**Without arguments**</span></span>

  <span data-ttu-id="a9922-119">Si aucune ligne de commande n’est fournie, wsl.exe lance le shell par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9922-119">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="a9922-120">**--exec, -e \<Ligne de commande>**</span><span class="sxs-lookup"><span data-stu-id="a9922-120">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="a9922-121">Exécute la commande spécifiée sans utiliser le shell Linux par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9922-121">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="a9922-122">Transmet le reste de la ligne de commande tel quel.</span><span class="sxs-lookup"><span data-stu-id="a9922-122">Pass the remaining command line as is.</span></span>

<span data-ttu-id="a9922-123">Les commandes ci-dessus acceptent également les options suivantes :</span><span class="sxs-lookup"><span data-stu-id="a9922-123">The above commands also accept the following options:</span></span>

* <span data-ttu-id="a9922-124">**--distribution, -d \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="a9922-124">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="a9922-125">Exécute la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a9922-125">Run the specified distribution.</span></span>

* <span data-ttu-id="a9922-126">**--user, -u \<Nom d’utilisateur>**</span><span class="sxs-lookup"><span data-stu-id="a9922-126">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="a9922-127">Procède à l’exécution sous l’utilisateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="a9922-127">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="a9922-128">Arguments pour la gestion du sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="a9922-128">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="a9922-129">**--export \<Distribution> \<Nom de fichier>**</span><span class="sxs-lookup"><span data-stu-id="a9922-129">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="a9922-130">Exporte la distribution vers un fichier tar.</span><span class="sxs-lookup"><span data-stu-id="a9922-130">Exports the distribution to a tar file.</span></span> <span data-ttu-id="a9922-131">Le nom de fichier peut être - pour une sortie standard.</span><span class="sxs-lookup"><span data-stu-id="a9922-131">The filename can be - for standard output.</span></span>

* <span data-ttu-id="a9922-132">**--import \<Distribution> \<Emplacement d’installation> \<Nom de fichier>**</span><span class="sxs-lookup"><span data-stu-id="a9922-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="a9922-133">Importe le fichier tar spécifié en tant que nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="a9922-133">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="a9922-134">Le nom de fichier peut être - pour une entrée standard.</span><span class="sxs-lookup"><span data-stu-id="a9922-134">The filename can be - for standard input.</span></span>

* <span data-ttu-id="a9922-135">**--list, -l [Options]**</span><span class="sxs-lookup"><span data-stu-id="a9922-135">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="a9922-136">Liste les distributions.</span><span class="sxs-lookup"><span data-stu-id="a9922-136">Lists distributions.</span></span>

  <span data-ttu-id="a9922-137">Options :</span><span class="sxs-lookup"><span data-stu-id="a9922-137">Options:</span></span>
  * <span data-ttu-id="a9922-138">**--all**</span><span class="sxs-lookup"><span data-stu-id="a9922-138">**--all**</span></span>

    <span data-ttu-id="a9922-139">Liste toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="a9922-139">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="a9922-140">**--running**</span><span class="sxs-lookup"><span data-stu-id="a9922-140">**--running**</span></span>

    <span data-ttu-id="a9922-141">Liste uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a9922-141">List only distributions that are currently running.</span></span>

* <span data-ttu-id="a9922-142">**--set-default, -s \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="a9922-142">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="a9922-143">Définit la distribution en tant que distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9922-143">Sets the distribution as the default.</span></span>

* <span data-ttu-id="a9922-144">**--terminate, -t \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="a9922-144">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="a9922-145">Met fin à la distribution spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a9922-145">Terminates the specified distribution.</span></span>

* <span data-ttu-id="a9922-146">**--unregister \<Distribution>**</span><span class="sxs-lookup"><span data-stu-id="a9922-146">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="a9922-147">Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="a9922-147">Un-register the distribution.</span></span>

* <span data-ttu-id="a9922-148">**--help** Affiche des informations sur l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a9922-148">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="a9922-149">Commandes supplémentaires</span><span class="sxs-lookup"><span data-stu-id="a9922-149">Additional Commands</span></span>

<span data-ttu-id="a9922-150">Certaines commandes historiques permettent également d’interagir avec le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="a9922-150">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="a9922-151">`wsl.exe` englobe leurs fonctionnalités, mais elles restent toujours à disposition.</span><span class="sxs-lookup"><span data-stu-id="a9922-151">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span>

### `wslconfig.exe`

<span data-ttu-id="a9922-152">Cette commande vous permet de configurer votre distribution WSL.</span><span class="sxs-lookup"><span data-stu-id="a9922-152">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="a9922-153">Voici une liste des options correspondantes.</span><span class="sxs-lookup"><span data-stu-id="a9922-153">Below is a list of its options.</span></span>

<span data-ttu-id="a9922-154">Utilisation : `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="a9922-154">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="a9922-155">Arguments</span><span class="sxs-lookup"><span data-stu-id="a9922-155">Arguments</span></span>

* <span data-ttu-id="a9922-156">**/l, /list [Options]**</span><span class="sxs-lookup"><span data-stu-id="a9922-156">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="a9922-157">Liste les distributions inscrites.</span><span class="sxs-lookup"><span data-stu-id="a9922-157">Lists registered distributions.</span></span>
  
<span data-ttu-id="a9922-158">Options :</span><span class="sxs-lookup"><span data-stu-id="a9922-158">Options:</span></span>

* <span data-ttu-id="a9922-159">**/all** Liste toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation (facultatif).</span><span class="sxs-lookup"><span data-stu-id="a9922-159">**/all** Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

* <span data-ttu-id="a9922-160">**/running** Liste uniquement les distributions en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a9922-160">**/running** List only distributions that are currently running.</span></span>

* <span data-ttu-id="a9922-161">**/s, /setdefault \<Distro>** Définit la distribution en tant que distribution par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9922-161">**/s, /setdefault \<Distro>** Sets the distribution as the default.</span></span>

* <span data-ttu-id="a9922-162">**/t, /terminate \<Distro>** Met fin à la distribution.</span><span class="sxs-lookup"><span data-stu-id="a9922-162">**/t, /terminate \<Distro>** Terminates the distribution.</span></span>

* <span data-ttu-id="a9922-163">**/u, /unregister \<Distro>** Annule l’inscription de la distribution.</span><span class="sxs-lookup"><span data-stu-id="a9922-163">**/u, /unregister \<Distro>** Un-registers the distribution.</span></span>

* <span data-ttu-id="a9922-164">**/upgrade \<Distro>** Met à niveau la distribution vers le format du système de fichiers WslFs.</span><span class="sxs-lookup"><span data-stu-id="a9922-164">**/upgrade \<Distro>** Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="a9922-165">Cette commande permet de démarrer un shell Bash.</span><span class="sxs-lookup"><span data-stu-id="a9922-165">This command is used to start a bash shell.</span></span> <span data-ttu-id="a9922-166">Vous trouverez ci-dessous les options que vous pouvez utiliser avec cette commande.</span><span class="sxs-lookup"><span data-stu-id="a9922-166">Below are the options you can use with this command.</span></span>

<span data-ttu-id="a9922-167">Utilisation : `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="a9922-167">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="a9922-168">**Aucune option indiquée**</span><span class="sxs-lookup"><span data-stu-id="a9922-168">**No Option given**</span></span>
  
  <span data-ttu-id="a9922-169">Lance le shell Bash dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="a9922-169">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="a9922-170">Si le shell Bash n’est pas installé, cette commande lance automatiquement `lxrun /install`.</span><span class="sxs-lookup"><span data-stu-id="a9922-170">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="a9922-171">`bash ~` lance le shell Bash dans le répertoire de base de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a9922-171">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="a9922-172">Cette option est similaire à `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="a9922-172">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="a9922-173">**-c "\<commande>"**</span><span class="sxs-lookup"><span data-stu-id="a9922-173">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="a9922-174">Exécute la commande, affiche la sortie et revient à l’invite de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="a9922-174">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>

  <span data-ttu-id="a9922-175">Par exemple : `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="a9922-175">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="a9922-176">Commandes dépréciées</span><span class="sxs-lookup"><span data-stu-id="a9922-176">Deprecated Commands</span></span>

<span data-ttu-id="a9922-177">`lxrun.exe` était la première commande utilisée pour installer et gérer le sous-système Windows pour Linux.</span><span class="sxs-lookup"><span data-stu-id="a9922-177">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="a9922-178">Elle est dépréciée pour les versions 1803 et ultérieures de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="a9922-178">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="a9922-179">La commande `lxrun.exe` peut être utilisée pour interagir directement avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-).</span><span class="sxs-lookup"><span data-stu-id="a9922-179">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="a9922-180">Ces commandes sont installées dans le répertoire `\Windows\System32` et peuvent être exécutées dans une invite de commandes Windows ou dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a9922-180">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="a9922-181">Commande</span><span class="sxs-lookup"><span data-stu-id="a9922-181">Command</span></span>                     | <span data-ttu-id="a9922-182">Description</span><span class="sxs-lookup"><span data-stu-id="a9922-182">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="a9922-183">La commande lxrun est utilisée pour gérer l’instance de WSL.</span><span class="sxs-lookup"><span data-stu-id="a9922-183">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="a9922-184">Démarre le processus de téléchargement et d’installation.</span><span class="sxs-lookup"><span data-stu-id="a9922-184">Starts the download and install process.</span></span> <br/> <span data-ttu-id="a9922-185">**/y** peut être ajouté pour ignorer toutes les invites.</span><span class="sxs-lookup"><span data-stu-id="a9922-185">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="a9922-186">L’invite de confirmation est automatiquement acceptée et l’utilisateur par défaut est défini sur la racine.</span><span class="sxs-lookup"><span data-stu-id="a9922-186">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="a9922-187">Désinstalle et supprime l’image Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="a9922-187">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="a9922-188">Par défaut, le répertoire de base Ubuntu de l’utilisateur n’est pas supprimé.</span><span class="sxs-lookup"><span data-stu-id="a9922-188">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="a9922-189">**/y** peut être ajouté pour accepter automatiquement l’invite de confirmation.</span><span class="sxs-lookup"><span data-stu-id="a9922-189">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="a9922-190">**/full** désinstalle et supprime le répertoire de base Ubuntu de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a9922-190">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="a9922-191">Définit l’utilisateur Bash sur Ubuntu par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9922-191">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="a9922-192">Demande un mot de passe si l’utilisateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a9922-192">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="a9922-193">Pour plus d’informations, consultez : https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="a9922-193">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="a9922-194">**/y** ignore la demande de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a9922-194">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="a9922-195">L’utilisateur sera créé sans mot de passe.</span><span class="sxs-lookup"><span data-stu-id="a9922-195">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="a9922-196">Met à jour l’index du package du sous-système.</span><span class="sxs-lookup"><span data-stu-id="a9922-196">Updates the subsystem's package index</span></span>          |
