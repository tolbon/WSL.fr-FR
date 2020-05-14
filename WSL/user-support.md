---
title: Créer et mettre à jour des comptes d’utilisateur pour les distributions Linux
description: Informations de référence sur les comptes d’utilisateur et la gestion des autorisations avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, comptes d’utilisateur
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235908"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a><span data-ttu-id="3c2a2-104">Créer un compte d’utilisateur et un mot de passe pour votre nouvelle distribution Linux</span><span class="sxs-lookup"><span data-stu-id="3c2a2-104">Create a user account and password for your new Linux distribution</span></span>

<span data-ttu-id="3c2a2-105">Une fois que vous avez [activé WSL et installé une distribution Linux à partir du Microsoft Store](./install-win10.md), la première étape qu’il vous est demandé d’effectuer lors de l’ouverture de la distribution Linux nouvellement installée consiste à créer un compte avec un **nom d’utilisateur** et un **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-105">Once you have [enabled WSL and installed a Linux distribution from the Microsoft Store](./install-win10.md), the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="3c2a2-106">Ce **nom d’utilisateur** et ce **mot de passe** sont propres à votre distribution Linux et n’ont aucune incidence sur votre nom d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="3c2a2-107">Une fois que vous avez créé ce **nom d’utilisateur** et ce **mot de passe**, le compte devient votre utilisateur par défaut pour la distribution et se connecte automatiquement au démarrage.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="3c2a2-108">Ce compte est considéré comme l’administrateur Linux, avec la capacité d’exécuter des commandes d’administration `sudo` (Super User Do).</span><span class="sxs-lookup"><span data-stu-id="3c2a2-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="3c2a2-109">Chaque distribution Linux exécutée sur le sous-système Windows pour Linux a ses propres comptes d’utilisateur et mots de passe Linux.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="3c2a2-110">Vous devez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez, réinstallez ou réinitialisez une distribution.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a><span data-ttu-id="3c2a2-112">Mettre à jour et mettre à niveau des packages</span><span class="sxs-lookup"><span data-stu-id="3c2a2-112">Update and upgrade packages</span></span>

<span data-ttu-id="3c2a2-113">La plupart des distributions sont livrées avec un catalogue de packages vide ou minimal.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-113">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="3c2a2-114">Nous vous recommandons vivement de mettre à jour régulièrement votre catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-114">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="3c2a2-115">Pour Debian/Ubuntu, utilisez apt :</span><span class="sxs-lookup"><span data-stu-id="3c2a2-115">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="3c2a2-116">Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-116">Windows does not automatically update or upgrade your Linux distribution(s).</span></span> <span data-ttu-id="3c2a2-117">Il s’agit d’une tâche que la plupart des utilisateurs Linux préfèrent contrôler eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-117">This is a task that the most Linux users prefer to control themselves.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="3c2a2-118">Réinitialiser votre mot de passe Linux</span><span class="sxs-lookup"><span data-stu-id="3c2a2-118">Reset your Linux password</span></span>

<span data-ttu-id="3c2a2-119">Pour changer votre mot de passe, ouvrez votre distribution Linux (Ubuntu, par exemple) et entrez la commande : `passwd`</span><span class="sxs-lookup"><span data-stu-id="3c2a2-119">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="3c2a2-120">Vous êtes invité à entrer votre mot de passe actuel, à entrer votre nouveau mot de passe, puis à confirmer votre nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-120">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

## <a name="forgot-your-password"></a><span data-ttu-id="3c2a2-121">Vous avez oublié votre mot de passe</span><span class="sxs-lookup"><span data-stu-id="3c2a2-121">Forgot your password</span></span>

<span data-ttu-id="3c2a2-122">Si vous avez oublié le mot de passe de votre distribution Linux :</span><span class="sxs-lookup"><span data-stu-id="3c2a2-122">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="3c2a2-123">Ouvrez PowerShell et entrez la racine de votre distribution WSL par défaut en utilisant la commande : `wsl -u root`</span><span class="sxs-lookup"><span data-stu-id="3c2a2-123">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

    > <span data-ttu-id="3c2a2-124">Si vous devez mettre à jour le mot de passe oublié sur une distribution qui n’est pas celle par défaut, utilisez la commande : `wsl -d Debian -u root` en remplaçant `Debian` par le nom de votre distribution ciblée.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-124">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="3c2a2-125">Une fois votre distribution WSL ouverte au niveau de la racine dans PowerShell, vous pouvez utiliser cette commande pour mettre à jour votre mot de passe : `passwd`</span><span class="sxs-lookup"><span data-stu-id="3c2a2-125">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="3c2a2-126">Vous serez invité à entrer un nouveau mot de passe UNIX, puis à confirmer ce mot de passe.</span><span class="sxs-lookup"><span data-stu-id="3c2a2-126">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="3c2a2-127">Une fois que vous êtes informé que le mot de passe a été correctement mis à jour, fermez WSL dans PowerShell en utilisant la commande : `exit`</span><span class="sxs-lookup"><span data-stu-id="3c2a2-127">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="3c2a2-128">Si vous exécutez une version antérieure du système d’exploitation Windows, comme 1703 (Creators Update) ou 1709 (Fall Creators Update), consultez la [documentation de la version archivée de cette mise à jour de compte d’utilisateur](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="3c2a2-128">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
