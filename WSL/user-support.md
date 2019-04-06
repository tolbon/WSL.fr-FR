---
title: Autorisations et le compte d’utilisateur Linux
description: Référence pour la gestion des autorisations et comptes d’utilisateur avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, comptes d’utilisateur
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063597"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="9d8c2-104">Comptes d’utilisateur et les autorisations pour le sous-système de Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="9d8c2-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="9d8c2-105">Création de votre utilisateur Linux est la première étape dans la configuration d’une nouvelle distribution de Linux sur WSL.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="9d8c2-106">Le premier compte d’utilisateur que vous créez est automatiquement configuré avec quelques attributs spécifiques :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="9d8c2-107">C’est votre utilisateur par défaut, il se connecte en automatiquement lors du lancement.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="9d8c2-108">Il est administrateur de Linux (il s’agit d’un membre du groupe sudo) par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="9d8c2-109">Chaque distribution Linux en cours d’exécution sur le sous-système Windows pour Linux a ses propres comptes d’utilisateur Linux et les mots de passe.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="9d8c2-110">Vous devrez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez une distribution, réinstallez ou réinitialisez.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="9d8c2-111">Comptes d’utilisateur Linux ne sont pas uniquement indépendantes par distribution, elles sont également indépendantes à partir de votre compte d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="9d8c2-112">Réinitialiser votre mot de passe Linux</span><span class="sxs-lookup"><span data-stu-id="9d8c2-112">Resetting your Linux password</span></span>

<span data-ttu-id="9d8c2-113">Si vous avez accès à votre compte d’utilisateur Linux et que vous connaissez votre mot de passe actuel, modifiez-le à l’aide de Linux mot de passe réinitialisé les outils de cette distribution--probablement `passwd`.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="9d8c2-114">Si ce n’est pas une option, en fonction de la distribution, vous serez peut-être en mesure de réinitialiser votre mot de passe en réinitialisant l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="9d8c2-115">WSL offre une balise d’utilisateur par défaut pour identifier le compte d’utilisateur automatiquement se connecte lorsque vous démarrez un WSL.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="9d8c2-116">Dans la mesure où les nombreuses distributions comprennent les commandes permettant de définir l’utilisateur par défaut à la racine et également un utilisateur racine avec aucun mot de passe défini, la modification de l’utilisateur par défaut à la racine est un outil pratique pour des opérations comme la réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="9d8c2-117">Pour Creators Update et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="9d8c2-117">For Creators Update and earlier</span></span>
<span data-ttu-id="9d8c2-118">Si vous exécutez Windows 10 Creators update ou version antérieure, vous pouvez modifier l’utilisateur de Bash par défaut en exécutant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="9d8c2-119">Modifier l’utilisateur par défaut à `root`:</span><span class="sxs-lookup"><span data-stu-id="9d8c2-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="9d8c2-120">Exécutez `bash.exe` à présent se connecter en tant que `root`:</span><span class="sxs-lookup"><span data-stu-id="9d8c2-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="9d8c2-121">Réinitialiser votre mot de passe à l’aide de la commande de mot de passe de la distribution, puis fermez la Console de Linux :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="9d8c2-122">À partir de Windows CMD, réinitialiser votre utilisateur par défaut à votre compte d’utilisateur Linux normal :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="9d8c2-123">Pour Fall Creators Update et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="9d8c2-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="9d8c2-124">Pour voir quelles sont les commandes sont disponibles pour une distribution particulière, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="9d8c2-125">Par exemple, avec Ubuntu installé :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="9d8c2-126">Procédure pas à obtenir des instructions détaillées à l’aide d’Ubuntu :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="9d8c2-127">Ouvrez CMD</span><span class="sxs-lookup"><span data-stu-id="9d8c2-127">Open CMD</span></span>
1. <span data-ttu-id="9d8c2-128">L’utilisateur de Linux par défaut la valeur `root`:</span><span class="sxs-lookup"><span data-stu-id="9d8c2-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="9d8c2-129">Lancez votre distribution Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="9d8c2-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="9d8c2-130">Vous rétablit automatiquement la connexion en tant que `root`:</span><span class="sxs-lookup"><span data-stu-id="9d8c2-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="9d8c2-131">Réinitialiser votre mot de passe à l’aide de la `passwd` commande :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="9d8c2-132">À partir de Windows CMD, réinitialiser votre utilisateur par défaut à votre compte d’utilisateur Linux normal.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="9d8c2-133">Autorisations</span><span class="sxs-lookup"><span data-stu-id="9d8c2-133">Permissions</span></span>

<span data-ttu-id="9d8c2-134">Il existe deux concepts importants à prendre en compte lorsqu’il s’agit des autorisations dans WSL :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="9d8c2-135">Le modèle d’autorisation Windows régit les droits d’un processus aux ressources de Windows</span><span class="sxs-lookup"><span data-stu-id="9d8c2-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="9d8c2-136">Le modèle d’autorisation Linux contrôle les droits d’un processus aux ressources de Linux</span><span class="sxs-lookup"><span data-stu-id="9d8c2-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="9d8c2-137">Lors de l’exécution de Linux sur WSL, Linux aura les mêmes autorisations Windows en tant que le processus qui le lance.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="9d8c2-138">Linux peut être lancé dans un des deux niveaux d’autorisation :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="9d8c2-139">Normal (non élevés) : Linux s’exécute avec les autorisations de l’utilisateur connecté</span><span class="sxs-lookup"><span data-stu-id="9d8c2-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="9d8c2-140">Avec élévation de privilèges/admin : Linux s’exécute avec des autorisations Windows avec élévation de privilèges/admin</span><span class="sxs-lookup"><span data-stu-id="9d8c2-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="9d8c2-141">Étant donné que qui élevés processus peuvent modifier/dommages des paramètres système et des données, et peut modifier/accès protégé de fichiers et dossiers, **Évitez** lançant des processus élevés, sauf si vous avez absolument - pour qu’ils soient Windows ou Applications/tools/shells Linux !</span><span class="sxs-lookup"><span data-stu-id="9d8c2-141">Because that elevated processes can change/damage system-wide settings and data, and can access/modify protected files and folders, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="9d8c2-142">Les autorisations Windows ci-dessus sont indépendantes des autorisations au sein d’une instance de Linux : Linux « privilèges racine » uniquement avoir un impact sur les droits d’utilisateur dans l’environnement Linux & système de fichiers ; ils n’ont aucun impact sur les privilèges Windows octroyés.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="9d8c2-143">Par conséquent, en exécutant un processus Linux en tant que racine (par exemple, via `sudo`) accorde uniquement qui traitent les droits d’administrateur dans l’environnement Linux.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

**<span data-ttu-id="9d8c2-144">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-144">Example:</span></span>**    
<span data-ttu-id="9d8c2-145">Une session d’interpréteur de commandes avec des privilèges d’administrateur Windows peut-être accéder à `cd /mnt/c/Users/Administrator` lors d’une session Bash sans privilèges d’administrateur pouvez voir une erreur « Autorisation refusée ».</span><span class="sxs-lookup"><span data-stu-id="9d8c2-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="9d8c2-146">Sous Linux, en tapant `sudo cd /mnt/c/Users/Administrator` pas accorde l’accès au répertoire de l’administrateur dans la mesure où les autorisations dans Windows sont gérées par Windows.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="9d8c2-147">Le modèle d’autorisation Linux est important quand à l’intérieur de l’environnement Linux où l’utilisateur dispose des autorisations en fonction de l’utilisateur Linux actuel.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

**<span data-ttu-id="9d8c2-148">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9d8c2-148">Example:</span></span>**  
<span data-ttu-id="9d8c2-149">Un utilisateur dans le groupe sudo peut-être s’exécuter `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="9d8c2-149">A user in the sudo group may run `sudo apt update`.</span></span>
