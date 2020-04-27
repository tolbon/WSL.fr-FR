---
title: Créer et mettre à jour des comptes d’utilisateur pour les distributions WSL
description: Informations de référence sur les comptes d’utilisateur et la gestion des autorisations avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, comptes d’utilisateur
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "76973679"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="bad49-104">Créer et mettre à jour des comptes d’utilisateur pour les distributions WSL</span><span class="sxs-lookup"><span data-stu-id="bad49-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="bad49-105">Une fois que vous avez activé WSL et installé une distribution Linux à partir du Microsoft Store, la première étape qui vous est demandé d’effectuer lors de l’ouverture de la distribution Linux nouvellement installée consiste à créer un compte avec un **nom d’utilisateur** et un **mot de passe**.</span><span class="sxs-lookup"><span data-stu-id="bad49-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="bad49-106">Ce **nom d’utilisateur** et ce **mot de passe** sont propres à votre distribution Linux et n’ont aucune incidence sur votre nom d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="bad49-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="bad49-107">Une fois que vous avez créé ce **nom d’utilisateur** et ce **mot de passe**, le compte devient votre utilisateur par défaut pour la distribution et se connecte automatiquement au démarrage.</span><span class="sxs-lookup"><span data-stu-id="bad49-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="bad49-108">Ce compte est considéré comme l’administrateur Linux, avec la capacité d’exécuter des commandes d’administration `sudo` (Super User Do).</span><span class="sxs-lookup"><span data-stu-id="bad49-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="bad49-109">Chaque distribution Linux exécutée sur le sous-système Windows pour Linux a ses propres comptes d’utilisateur et mots de passe Linux.</span><span class="sxs-lookup"><span data-stu-id="bad49-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="bad49-110">Vous devez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez, réinstallez ou réinitialisez une distribution.</span><span class="sxs-lookup"><span data-stu-id="bad49-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="bad49-111">Réinitialiser votre mot de passe Linux</span><span class="sxs-lookup"><span data-stu-id="bad49-111">Reset your Linux password</span></span>

<span data-ttu-id="bad49-112">Pour changer votre mot de passe, ouvrez votre distribution Linux (Ubuntu, par exemple) et entrez la commande : `passwd`</span><span class="sxs-lookup"><span data-stu-id="bad49-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="bad49-113">Vous êtes invité à entrer votre mot de passe actuel, à entrer votre nouveau mot de passe, puis à confirmer votre nouveau mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bad49-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="bad49-114">Vous avez oublié votre mot de passe</span><span class="sxs-lookup"><span data-stu-id="bad49-114">Forgot your password</span></span>

<span data-ttu-id="bad49-115">Si vous avez oublié le mot de passe de votre distribution Linux :</span><span class="sxs-lookup"><span data-stu-id="bad49-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="bad49-116">Ouvrez PowerShell et entrez la racine de votre distribution WSL par défaut en utilisant la commande : `wsl -u root`</span><span class="sxs-lookup"><span data-stu-id="bad49-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

> <span data-ttu-id="bad49-117">Si vous devez mettre à jour le mot de passe oublié sur une distribution qui n’est pas celle par défaut, utilisez la commande : `wsl -d Debian -u root` en remplaçant `Debian` par le nom de votre distribution ciblée.</span><span class="sxs-lookup"><span data-stu-id="bad49-117">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="bad49-118">Une fois votre distribution WSL ouverte au niveau de la racine dans PowerShell, vous pouvez utiliser cette commande pour mettre à jour votre mot de passe : `passwd`</span><span class="sxs-lookup"><span data-stu-id="bad49-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="bad49-119">Vous serez invité à entrer un nouveau mot de passe UNIX, puis à confirmer ce mot de passe.</span><span class="sxs-lookup"><span data-stu-id="bad49-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="bad49-120">Une fois que vous êtes informé que le mot de passe a été correctement mis à jour, fermez WSL dans PowerShell en utilisant la commande : `exit`</span><span class="sxs-lookup"><span data-stu-id="bad49-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="bad49-121">Si vous exécutez une version antérieure du système d’exploitation Windows, comme 1703 (Creators Update) ou 1709 (Fall Creators Update), consultez la [documentation de la version archivée de cette mise à jour de compte d’utilisateur](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="bad49-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
