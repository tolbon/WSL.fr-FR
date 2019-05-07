---
title: Installer ou supprimer sur la mise à jour anniversaire de Windows 10 ou Creators Update
description: Instructions d’installation et de désinstallation pour le hérité, la distribution bêta sur la mise à jour anniversaire de Windows 10 ou Creators Update
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, hérité, bêta, installer, supprimer, désinstaller, désinstaller, delete, déconseillée
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063587"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="fa92c-104">Guide pour installer ou désinstaller le sous-système de Windows pour Linux sur la mise à jour anniversaire de Windows 10 et Creators Update</span><span class="sxs-lookup"><span data-stu-id="fa92c-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="fa92c-105">Si vous utilisez Windows 10 Creators Update ou une version ultérieure, veuillez [suivez les instructions d’installation de Windows 10](install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="fa92c-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="fa92c-106"><strong><em><span style="color: #f28014">Les instructions suivantes concernent les utilisateurs qui exécutent la mise à jour anniversaire de Windows 10 ou Windows 10 Creators Update</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="fa92c-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="fa92c-107">Avant Windows 10 Fall Creators Update (version 1709), WSL a été publié comme une fonctionnalité bêta et installé une seule instance Ubuntu lors de la première exécution du « Bash sur Ubuntu sur Windows » (ou Bash.exe).</span><span class="sxs-lookup"><span data-stu-id="fa92c-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="fa92c-108">Vous pouvez utiliser WSL sur des versions antérieures de Windows 10, cette version bêta de « distributeur hérité » est désormais considéré comme obsolète.</span><span class="sxs-lookup"><span data-stu-id="fa92c-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="fa92c-109">Nous vous encourageons vivement à exécuter la version la plus récente de Windows 10 disponibles.</span><span class="sxs-lookup"><span data-stu-id="fa92c-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="fa92c-110">Chaque nouvelle version de Windows 10 inclut plusieurs centaines de correctifs et améliorations dans WSL uniquement, ce qui permet plus jamais outils Linux et les applications à s’exécuter correctement sur WSL.</span><span class="sxs-lookup"><span data-stu-id="fa92c-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="fa92c-111">Si vous ne peut pas mettre à niveau vers Fall Creators Update ou version ultérieure, suivez les étapes ci-dessous pour activer et utiliser WSL :</span><span class="sxs-lookup"><span data-stu-id="fa92c-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="fa92c-112">Activer développeur Mode pour exécuter WSL sur la mise à jour anniversaire de Windows 10 ou Creators Update, vous devez activer le Mode développeur :</span><span class="sxs-lookup"><span data-stu-id="fa92c-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="fa92c-113">Ouvrez **paramètres** -> **mise à jour et sécurité** -> **pour les développeurs**</span><span class="sxs-lookup"><span data-stu-id="fa92c-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="fa92c-114">Sélectionnez la case d’option Mode développeur</span><span class="sxs-lookup"><span data-stu-id="fa92c-114">Select the Developer Mode radio button</span></span>  
    ![Activer le mode développeur](media/updateAndSecurity.png)

    > <span data-ttu-id="fa92c-116">La nécessité d’activer le Mode développeur a été [supprimée dans Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="fa92c-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="fa92c-117">Ouvrez une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="fa92c-117">Open a command prompt.</span></span>  <span data-ttu-id="fa92c-118">Type `bash` puis appuyez sur entrée</span><span class="sxs-lookup"><span data-stu-id="fa92c-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="fa92c-119">La première fois que vous exécutez Bash sur Ubuntu sur Windows, vous devrez faire pour accepter les licences de Canonical.</span><span class="sxs-lookup"><span data-stu-id="fa92c-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="fa92c-120">Une fois accpted, WSL téléchargera et installera l’instance Ubuntu sur votre ordinateur, et un raccourci « Bash sur Ubuntu sur Windows » sera ajouté à votre menu Démarrer.</span><span class="sxs-lookup"><span data-stu-id="fa92c-120">Once accpted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![Inviter à installer Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="fa92c-122">La première fois que vous exécutez Bash sur Ubuntu sur Windows, vous devrez créer un nom d’utilisateur UNIX et le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="fa92c-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="fa92c-123">Suivez le [nouvelles instructions d’instance de distributeur](initialize-distro.md) pour terminer l’installation</span><span class="sxs-lookup"><span data-stu-id="fa92c-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="fa92c-124">Lancer un nouvel interpréteur Ubuntu à l’aide :</span><span class="sxs-lookup"><span data-stu-id="fa92c-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="fa92c-125">En cours d’exécution `bash` à partir d’une invite de commandes</span><span class="sxs-lookup"><span data-stu-id="fa92c-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="fa92c-126">En cliquant sur le raccourci « Bash sur Ubuntu sur Windows » du menu Démarrer</span><span class="sxs-lookup"><span data-stu-id="fa92c-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="fa92c-127">Désinstallation/la suppression de la distribution héritée</span><span class="sxs-lookup"><span data-stu-id="fa92c-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="fa92c-128">Si vous mettez à niveau depuis une version antérieure de Windows 10 sur lequel vous avez installé WSL pour Windows 10 Fall Creators Update, votre distribution existante demeureront intacte.</span><span class="sxs-lookup"><span data-stu-id="fa92c-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="fa92c-129">Toutefois, nous fortement vous recommandons d’installer une nouvelle distribution assurée par le Store dès que possible et migrer les fichiers nécessaires, données etc. à partir de votre distribution héritée pour votre nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="fa92c-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="fa92c-130">Pour supprimer la distribution héritée à partir de votre ordinateur, exécutez la commande suivante à partir d’une instance de la ligne de commande ou PowerShell :</span><span class="sxs-lookup"><span data-stu-id="fa92c-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="fa92c-131">Suppression manuelle de la distribution héritée</span><span class="sxs-lookup"><span data-stu-id="fa92c-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="fa92c-132">Si vous le souhaitez, vous pouvez supprimer manuellement l’ancienne instance.</span><span class="sxs-lookup"><span data-stu-id="fa92c-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="fa92c-133">Cela peut être nécessaire si vous rencontrez des problèmes pour désinstaller le distributeur hérité à l’aide `lxrun.exe`, ou de la mise à jour Windows 10 printemps 2018 sont en cours d’exécution (ou version ultérieure) qui ne sont pas fournies avec `lxrun.exe`.</span><span class="sxs-lookup"><span data-stu-id="fa92c-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="fa92c-134">Pour forcer la suppression de votre distribution WSL héritée, supprimez le `%localappdata%\lxss\` dossier (et tous les il s’agit de contenu secondaire) à l’aide de l’Explorateur de fichiers des Windows ou la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="fa92c-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="fa92c-135">À l'aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa92c-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="fa92c-136">En utilisant une commande :</span><span class="sxs-lookup"><span data-stu-id="fa92c-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
