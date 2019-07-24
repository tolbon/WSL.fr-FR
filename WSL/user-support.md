---
title: Autorisations et compte d’utilisateur Linux
description: Référence pour les comptes d’utilisateur et la gestion des autorisations avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, comptes d’utilisateur
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040823"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="18f13-104">Comptes d’utilisateur et autorisations pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="18f13-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="18f13-105">La création de votre utilisateur Linux constitue la première étape de la configuration d’une nouvelle distribution Linux sur WSL.</span><span class="sxs-lookup"><span data-stu-id="18f13-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="18f13-106">Le premier compte d’utilisateur que vous créez est automatiquement configuré avec quelques attributs spéciaux:</span><span class="sxs-lookup"><span data-stu-id="18f13-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="18f13-107">Il s’agit de votre utilisateur par défaut; il se connecte automatiquement au lancement.</span><span class="sxs-lookup"><span data-stu-id="18f13-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="18f13-108">Il s’agit de l’administrateur Linux (membre du groupe sudo) par défaut.</span><span class="sxs-lookup"><span data-stu-id="18f13-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="18f13-109">Chaque distribution Linux exécutée sur le sous-système Windows pour Linux possède ses propres comptes d’utilisateur et mots de passe Linux.</span><span class="sxs-lookup"><span data-stu-id="18f13-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="18f13-110">Vous devez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez une distribution, réinstallez ou réinitialisez.</span><span class="sxs-lookup"><span data-stu-id="18f13-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="18f13-111">Les comptes d’utilisateur Linux ne sont pas uniquement indépendants par distribution. ils sont également indépendants de votre compte d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="18f13-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="18f13-112">Réinitialisation de votre mot de passe Linux</span><span class="sxs-lookup"><span data-stu-id="18f13-112">Resetting your Linux password</span></span>

<span data-ttu-id="18f13-113">Si vous avez accès à votre compte d’utilisateur Linux et que vous connaissez votre mot de passe actuel, modifiez-le à l’aide des outils de `passwd`réinitialisation de mot de passe Linux de cette distribution, le plus probable.</span><span class="sxs-lookup"><span data-stu-id="18f13-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="18f13-114">Si ce n’est pas le cas, en fonction de la distribution, vous pourrez peut-être réinitialiser votre mot de passe en réinitialisant l’utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="18f13-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="18f13-115">WSL offre une balise utilisateur par défaut pour identifier le compte d’utilisateur qui se connecte automatiquement quand vous démarrez un WSL.</span><span class="sxs-lookup"><span data-stu-id="18f13-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="18f13-116">Étant donné que de nombreuses distributions incluent des commandes permettant de définir l’utilisateur par défaut à root et à un utilisateur racine sans mot de passe défini, la modification de l’utilisateur par défaut en root est un outil pratique pour effectuer des opérations telles que la réinitialisation de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="18f13-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="18f13-117">Pour Creators Update et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="18f13-117">For Creators Update and earlier</span></span>
<span data-ttu-id="18f13-118">Si vous exécutez Windows 10 Creators Update ou une version antérieure, vous pouvez modifier l’utilisateur bash par défaut en exécutant les commandes suivantes:</span><span class="sxs-lookup"><span data-stu-id="18f13-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="18f13-119">Remplacez l’utilisateur `root`par défaut par:</span><span class="sxs-lookup"><span data-stu-id="18f13-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="18f13-120">Exécutez `bash.exe` pour vous connecter en `root`tant que:</span><span class="sxs-lookup"><span data-stu-id="18f13-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="18f13-121">Réinitialisez votre mot de passe à l’aide de la commande de mot de passe de la distribution, puis fermez la console Linux:</span><span class="sxs-lookup"><span data-stu-id="18f13-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="18f13-122">À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal:</span><span class="sxs-lookup"><span data-stu-id="18f13-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="18f13-123">Pour les créateurs de automne, mettez à jour et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="18f13-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="18f13-124">Pour connaître les commandes disponibles pour une distribution particulière, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="18f13-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="18f13-125">Par exemple, avec Ubuntu installé:</span><span class="sxs-lookup"><span data-stu-id="18f13-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="18f13-126">Instructions pas à pas sur Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="18f13-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="18f13-127">Ouvrir CMD</span><span class="sxs-lookup"><span data-stu-id="18f13-127">Open CMD</span></span>
1. <span data-ttu-id="18f13-128">Définir l’utilisateur Linux par défaut `root`sur:</span><span class="sxs-lookup"><span data-stu-id="18f13-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="18f13-129">Lancez votre distribution Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="18f13-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="18f13-130">Vous vous connectez automatiquement en `root`tant que:</span><span class="sxs-lookup"><span data-stu-id="18f13-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="18f13-131">Réinitialisez votre mot `passwd` de passe à l’aide de la commande:</span><span class="sxs-lookup"><span data-stu-id="18f13-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="18f13-132">À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal.</span><span class="sxs-lookup"><span data-stu-id="18f13-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="18f13-133">Autorisations</span><span class="sxs-lookup"><span data-stu-id="18f13-133">Permissions</span></span>

<span data-ttu-id="18f13-134">Il existe deux concepts importants à garder à l’esprit lorsqu’il s’agit d’autorisations dans WSL:</span><span class="sxs-lookup"><span data-stu-id="18f13-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="18f13-135">Le modèle d’autorisation Windows régit les droits des processus sur les ressources Windows</span><span class="sxs-lookup"><span data-stu-id="18f13-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="18f13-136">Le modèle d’autorisation Linux contrôle un droit de processus aux ressources Linux</span><span class="sxs-lookup"><span data-stu-id="18f13-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="18f13-137">Lors de l’exécution de Linux sur WSL, Linux aura les mêmes autorisations Windows que le processus qui le lance.</span><span class="sxs-lookup"><span data-stu-id="18f13-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="18f13-138">Linux peut être lancé dans l’un des deux niveaux d’autorisation suivants:</span><span class="sxs-lookup"><span data-stu-id="18f13-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="18f13-139">Normal (non élevé): Linux s’exécute avec les autorisations de l’utilisateur connecté</span><span class="sxs-lookup"><span data-stu-id="18f13-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="18f13-140">Élevé/administrateur: Linux s’exécute avec des autorisations Windows élevées/admin</span><span class="sxs-lookup"><span data-stu-id="18f13-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="18f13-141">Étant donné que les processus élevés peuvent accéder/modifier (et par conséquent endommager) des paramètres à l’ensemble du système et des données système/protégées, **Évitez** de lancer des processus élevés, sauf si vous avez absolument besoin de savoir s’il s’agit d’applications/outils Windows ou Linux/ Coque!</span><span class="sxs-lookup"><span data-stu-id="18f13-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="18f13-142">Les autorisations Windows ci-dessus sont indépendantes des autorisations au sein d’une instance Linux: Les «privilèges racine» Linux affectent uniquement les droits de l’utilisateur au sein de l’environnement Linux & système de fichiers; ils n’ont aucun impact sur les privilèges Windows accordés.</span><span class="sxs-lookup"><span data-stu-id="18f13-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="18f13-143">Ainsi, l’exécution d’un processus Linux en tant que racine `sudo`(par exemple, via) accorde uniquement ce processus à des droits d’administrateur au sein de l’environnement Linux.</span><span class="sxs-lookup"><span data-stu-id="18f13-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="18f13-144">**Exemple :**   </span><span class="sxs-lookup"><span data-stu-id="18f13-144">**Example:**  </span></span>  
<span data-ttu-id="18f13-145">Une session bash avec des privilèges d’administrateur Windows `cd /mnt/c/Users/Administrator` peut accéder alors qu’une session bash sans privilèges d’administrateur voit une erreur «autorisation refusée».</span><span class="sxs-lookup"><span data-stu-id="18f13-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="18f13-146">Dans Linux, la `sudo cd /mnt/c/Users/Administrator` saisie n’accorde pas l’accès au répertoire de l’administrateur, car les autorisations dans Windows sont gérées par Windows.</span><span class="sxs-lookup"><span data-stu-id="18f13-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="18f13-147">Le modèle d’autorisation Linux est important dans l’environnement Linux où l’utilisateur dispose d’autorisations basées sur l’utilisateur Linux actuel.</span><span class="sxs-lookup"><span data-stu-id="18f13-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="18f13-148">**Exemple :**</span><span class="sxs-lookup"><span data-stu-id="18f13-148">**Example:**</span></span>  
<span data-ttu-id="18f13-149">Un utilisateur du groupe sudo peut s’exécuter `sudo apt update`.</span><span class="sxs-lookup"><span data-stu-id="18f13-149">A user in the sudo group may run `sudo apt update`.</span></span>
