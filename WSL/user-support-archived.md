---
title: Mises à jour de compte d’utilisateur WSL sur les versions précédentes de Windows
description: Informations de référence sur les versions précédentes de Windows pour mettre à jour les comptes d’utilisateur Linux avec le sous-système Windows pour Linux.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 406158d769c4b465b6168d7cca45b48ff1f201fe
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520838"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a><span data-ttu-id="7f0e0-103">Mises à jour de compte d’utilisateur WSL sur les versions précédentes de Windows</span><span class="sxs-lookup"><span data-stu-id="7f0e0-103">WSL User Account updates on Previous Windows Versions</span></span>

<span data-ttu-id="7f0e0-104">Ce contenu est archivé pour les utilisateurs des versions antérieures du système d’exploitation Windows qui prennent en charge le sous-système pour Linux et ont besoin de la prise en charge de la mise à jour des comptes d’utilisateur Linux.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-104">This content is archived for users of earlier versions of Windows operating system that support the subsystem for Linux and need support with updating Linux user accounts.</span></span>

<span data-ttu-id="7f0e0-105">Pour obtenir la documentation actuelle, consultez [comptes d’utilisateur pour le sous-système Windows pour Linux](../user-support.md).</span><span class="sxs-lookup"><span data-stu-id="7f0e0-105">For current documentation, see [User Accounts for Windows Subsystem for Linux](../user-support.md).</span></span>

### <a name="for-creators-update-version-of-windows-and-earlier"></a><span data-ttu-id="7f0e0-106">Pour Creators Update version de Windows et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="7f0e0-106">For Creators Update version of Windows and earlier</span></span>

<span data-ttu-id="7f0e0-107">Si vous exécutez Windows 10 Creators Update ou version antérieure, vous pouvez changer l’utilisateur Bash par défaut en exécutant les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-107">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="7f0e0-108">Définissez l’utilisateur par défaut sur `root` :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-108">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="7f0e0-109">Exécutez `bash.exe` pour vous connecter maintenant en tant que `root` :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-109">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="7f0e0-110">Réinitialisez votre mot de passe à l’aide de la commande de mot de passe de la distribution, puis fermez la console Linux :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-110">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="7f0e0-111">À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-111">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="7f0e0-112">Pour Fall Creators Update et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="7f0e0-112">For Fall Creators Update and later</span></span>

<span data-ttu-id="7f0e0-113">Pour connaître les commandes disponibles pour une distribution en particulier, exécutez `[distro.exe] /?`.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-113">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="7f0e0-114">Par exemple, avec Ubuntu installé :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-114">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="7f0e0-115">Instructions pas à pas sur Ubuntu :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-115">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="7f0e0-116">Ouvrez CMD.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-116">Open CMD</span></span>
1. <span data-ttu-id="7f0e0-117">Définissez l’utilisateur Linux par défaut sur `root` :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-117">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="7f0e0-118">Lancez votre distribution Linux (`ubuntu`).</span><span class="sxs-lookup"><span data-stu-id="7f0e0-118">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="7f0e0-119">Vous vous connectez automatiquement en tant que `root` :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-119">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="7f0e0-120">Réinitialisez votre mot de passe à l’aide de la commande `passwd` :</span><span class="sxs-lookup"><span data-stu-id="7f0e0-120">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="7f0e0-121">À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal.</span><span class="sxs-lookup"><span data-stu-id="7f0e0-121">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```
