---
title: Installer ou supprimer la mise à jour anniversaire de Windows 10 ou les créateurs de la mise à jour
description: Instructions d’installation et de désinstallation pour la mise à jour anniversaire héritée, bêta distribution sur Windows 10 ou Creators Update
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, hérité, bêta, installation, suppression, désinstallation, désinstallation, suppression, déconseillé
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499263"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="8b1b7-104">Guide pour installer ou désinstaller le sous-système Windows pour Linux sur la mise à jour anniversaire Windows 10 et les créateurs de la mise à jour</span><span class="sxs-lookup"><span data-stu-id="8b1b7-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="8b1b7-105">Si vous exécutez Windows 10 Creators Update ou une version ultérieure, veuillez [suivre les instructions d’installation de Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="8b1b7-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="8b1b7-106"><strong><em><span style="color: #f28014">Les instructions suivantes concernent les utilisateurs qui exécutent la mise à jour anniversaire Windows 10 ou Windows 10 Creators Update</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="8b1b7-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="8b1b7-107">Avant la mise à jour de Windows 10 automne Creators (version 1709), WSL a été publié en tant que fonctionnalité bêta et installait une seule instance Ubuntu lors de la première exécution de «bash sur Ubuntu sur Windows» (ou bash. exe).</span><span class="sxs-lookup"><span data-stu-id="8b1b7-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="8b1b7-108">Bien que vous puissiez utiliser WSL sur des versions antérieures de Windows 10, cette version bêta «Legacy distribution» est désormais considérée comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="8b1b7-109">Nous vous encourageons vivement à exécuter la version la plus récente de Windows 10 disponible.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="8b1b7-110">Chaque nouvelle version de Windows 10 inclut un grand nombre de centaines de correctifs et d’améliorations dans WSL seul, ce qui permet à d’autres outils et applications Linux de s’exécuter correctement sur WSL.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="8b1b7-111">Si vous ne pouvez pas effectuer une mise à niveau vers automne Creators Update ou une version ultérieure, suivez les étapes ci-dessous pour activer et utiliser WSL:</span><span class="sxs-lookup"><span data-stu-id="8b1b7-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="8b1b7-112">Activer le mode développeur pour exécuter WSL sur la mise à jour anniversaire de Windows 10 ou sur Creators Update, vous devez activer le mode développeur:</span><span class="sxs-lookup"><span data-stu-id="8b1b7-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="8b1b7-113">Ouvrir la**mise à jour et la sécurité** -> des **paramètres** -> **pour les développeurs**</span><span class="sxs-lookup"><span data-stu-id="8b1b7-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="8b1b7-114">Sélectionnez la case d’option mode développeur</span><span class="sxs-lookup"><span data-stu-id="8b1b7-114">Select the Developer Mode radio button</span></span>  
    ![Activer le mode développeur](media/updateAndSecurity.png)

    > <span data-ttu-id="8b1b7-116">La nécessité d’activer le mode développeur a été [supprimée dans Windows 10 automne Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="8b1b7-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="8b1b7-117">Ouvrez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-117">Open a command prompt.</span></span>  <span data-ttu-id="8b1b7-118">Tapez `bash` et appuyez sur entrée</span><span class="sxs-lookup"><span data-stu-id="8b1b7-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="8b1b7-119">La première fois que vous exécutez bash sur Ubuntu sur Windows, vous êtes invité à accepter la licence de Canonical.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="8b1b7-120">Une fois accepté, WSL télécharge et installe l’instance Ubuntu sur votre ordinateur, et un raccourci «Bash sur Ubuntu sur Windows» est ajouté à votre menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Demander l’installation d’Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="8b1b7-122">La première fois que vous exécutez bash sur Ubuntu sur Windows, vous êtes invité à créer un nom d’utilisateur et un mot de passe UNIX.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="8b1b7-123">Suivez les [nouvelles instructions de l’instance distribution](initialize-distro.md) pour terminer l’installation</span><span class="sxs-lookup"><span data-stu-id="8b1b7-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="8b1b7-124">Lancez un nouveau shell Ubuntu en procédant de l’une des deux:</span><span class="sxs-lookup"><span data-stu-id="8b1b7-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="8b1b7-125">Exécution `bash` à partir d’une invite de commandes</span><span class="sxs-lookup"><span data-stu-id="8b1b7-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="8b1b7-126">Cliquer sur le menu Démarrer «bash sur Ubuntu sur Windows»</span><span class="sxs-lookup"><span data-stu-id="8b1b7-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="8b1b7-127">Désinstallation/suppression de la distribution héritée</span><span class="sxs-lookup"><span data-stu-id="8b1b7-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="8b1b7-128">Si vous effectuez une mise à niveau vers Windows 10 automne Creators Update à partir d’une version antérieure de Windows 10 sur laquelle vous avez installé WSL, votre distribution existante reste intacte.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="8b1b7-129">Toutefois, nous vous encourageons VIVEment à installer un nouveau distribution ASAP remis en magasin et à migrer les fichiers, les données, etc. nécessaires de votre distribution hérité vers votre nouveau distribution.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="8b1b7-130">Pour supprimer les distribution hérités de votre ordinateur, exécutez la commande suivante à partir d’une ligne de commande ou d’une instance de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8b1b7-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="8b1b7-131">Si vous n’utilisez pas Windows version 1903 ou ultérieure, vous devrez peut-être `wslconfig /u Legacy` exécuter `lxrun /uninstall /full` ou à la place.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="8b1b7-132">Suppression manuelle de la distribution héritée</span><span class="sxs-lookup"><span data-stu-id="8b1b7-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="8b1b7-133">Si vous le souhaitez, vous pouvez supprimer manuellement votre instance héritée.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="8b1b7-134">Cela peut être nécessaire si vous rencontrez des problèmes lors de la désinstallation de `lxrun.exe`la distribution héritée à l’aide de, ou si vous exécutez Windows 10 Spring 2018 Update `lxrun.exe`(ou version ultérieure) qui n’est pas livré avec.</span><span class="sxs-lookup"><span data-stu-id="8b1b7-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="8b1b7-135">Pour forcer la suppression de votre distribution WSL héritée, `%localappdata%\lxss\` supprimez le dossier (et tous ses sous-contenus) à l’aide de l’Explorateur de fichiers Windows, ou de la ligne de commande:</span><span class="sxs-lookup"><span data-stu-id="8b1b7-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="8b1b7-136">À l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="8b1b7-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="8b1b7-137">Utilisation de cmd:</span><span class="sxs-lookup"><span data-stu-id="8b1b7-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
