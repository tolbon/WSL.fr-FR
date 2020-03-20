---
title: Installer le sous-système Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation du sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200232"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="45bde-104">Guide d’installation du sous-système Windows pour Linux pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="45bde-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="45bde-105">Installer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="45bde-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="45bde-106">Avant d’installer des distributions Linux pour WSL, vous devez vous assurer que la fonctionnalité facultative « Sous-système Windows pour Linux » est activée :</span><span class="sxs-lookup"><span data-stu-id="45bde-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="45bde-107">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="45bde-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="45bde-108">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="45bde-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="45bde-109">Installer la distribution Linux de votre choix</span><span class="sxs-lookup"><span data-stu-id="45bde-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="45bde-110">Pour télécharger et installer vos distributions préférées, vous avez trois possibilités :</span><span class="sxs-lookup"><span data-stu-id="45bde-110">To download and install your preferred distro(s), you have three choices:</span></span>
* <span data-ttu-id="45bde-111">Télécharger et installer à partir du Microsoft Store (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="45bde-111">Download and install from the Microsoft Store (see below)</span></span>
* <span data-ttu-id="45bde-112">Télécharger et installer à partir de la ligne de commande/du script ([lisez les instructions d’installation manuelle](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="45bde-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
* <span data-ttu-id="45bde-113">Télécharger, décompresser manuellement et installer (pour Windows Server [instructions ici](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="45bde-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="45bde-114">Windows 10 Fall Creators Update et ultérieur : installer à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="45bde-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="45bde-115">Cette section concerne la build Windows 16215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="45bde-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="45bde-116">Procédez comme suit pour [vérifier votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="45bde-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="45bde-117">Ouvrez le Microsoft Store et choisissez votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="45bde-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    <span data-ttu-id="45bde-119">Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :</span><span class="sxs-lookup"><span data-stu-id="45bde-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="45bde-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="45bde-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="45bde-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="45bde-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="45bde-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="45bde-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="45bde-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="45bde-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="45bde-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="45bde-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="45bde-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="45bde-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="45bde-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="45bde-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="45bde-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="45bde-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="45bde-128">Fedora Remix pour WSL</span><span class="sxs-lookup"><span data-stu-id="45bde-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="45bde-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="45bde-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="45bde-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="45bde-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="45bde-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="45bde-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="45bde-132">Dans la page de la distribution, sélectionnez « Obtenir »</span><span class="sxs-lookup"><span data-stu-id="45bde-132">From the distro's page, select "Get"</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="45bde-134">Effectuer l’initialisation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="45bde-134">Complete initialization of your distro</span></span>
<span data-ttu-id="45bde-135">Maintenant que votre distribution Linux est installée, vous devez [initialiser la nouvelle instance de distribution](initialize-distro.md) une fois avant de pouvoir l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="45bde-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="45bde-136">Dépannage :</span><span class="sxs-lookup"><span data-stu-id="45bde-136">Troubleshooting:</span></span> 

<span data-ttu-id="45bde-137">Vous trouverez ci-dessous des erreurs associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="45bde-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="45bde-138">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="45bde-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="45bde-139">**Échec de l’installation avec l’erreur 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="45bde-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="45bde-140">Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`).</span><span class="sxs-lookup"><span data-stu-id="45bde-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="45bde-141">Vérifiez que les distributions sont stockées sur votre lecteur système :</span><span class="sxs-lookup"><span data-stu-id="45bde-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="45bde-142">Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Modifier l’emplacement d’enregistrement du nouveau contenu**
    ![Image des paramètres système pour installer les applications sur le lecteur C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="45bde-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="45bde-143">**Échec de WslRegisterDistribution avec l’erreur 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="45bde-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="45bde-144">Le composant facultatif Sous-système Windows pour Linux n’est pas activé :</span><span class="sxs-lookup"><span data-stu-id="45bde-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="45bde-145">Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="45bde-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
