---
title: Installer le sous-système de Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation pour le sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, installer
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035054"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="004b7-104">Sous-système Windows pour le Guide d’Installation de Linux pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="004b7-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="004b7-105">Installer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="004b7-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="004b7-106">Avant d’installer toutes les distributions Linux pour WSL, vous devez vous assurer que les « Windows sous-système pour Linux » fonctionnalité facultative est activée :</span><span class="sxs-lookup"><span data-stu-id="004b7-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="004b7-107">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="004b7-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="004b7-108">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="004b7-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="004b7-109">Installer votre Distribution Linux de choix</span><span class="sxs-lookup"><span data-stu-id="004b7-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="004b7-110">Pour télécharger et installer votre distro(s) préférée, vous avez trois possibilités :</span><span class="sxs-lookup"><span data-stu-id="004b7-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="004b7-111">Téléchargez et installez depuis le Store de Windows (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="004b7-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="004b7-112">Télécharger et installer à partir de la commande-ligne ou des scripts ([Lisez les instructions d’installation manuelle](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="004b7-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="004b7-113">Télécharger et décompresser et installer manuellement (pour Windows Server - [instructions fournies ici](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="004b7-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="004b7-114">Windows 10 Fall Creators Update et versions ultérieures : Installer à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="004b7-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="004b7-115">Cette section concerne Windows build 16215 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="004b7-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="004b7-116">Suivez ces étapes pour [vérifier votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="004b7-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="004b7-117">Le Microsoft Store et votre distribution Linux favorite.</span><span class="sxs-lookup"><span data-stu-id="004b7-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Affichage des distributions de Linux dans le magasin Windows](media/store.png)

    <span data-ttu-id="004b7-119">Les liens suivants seront ouvre à la page magasin de Windows pour chaque distribution :</span><span class="sxs-lookup"><span data-stu-id="004b7-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="004b7-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="004b7-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="004b7-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="004b7-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="004b7-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="004b7-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="004b7-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="004b7-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="004b7-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="004b7-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="004b7-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="004b7-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="004b7-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="004b7-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="004b7-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="004b7-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="004b7-128">Remix Fedora pour WSL</span><span class="sxs-lookup"><span data-stu-id="004b7-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="004b7-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="004b7-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="004b7-130">WLinux Enterprise</span><span class="sxs-lookup"><span data-stu-id="004b7-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="004b7-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="004b7-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="004b7-132">À partir de la page de la distribution, sélectionnez « Get »</span><span class="sxs-lookup"><span data-stu-id="004b7-132">From the distro's page, select "Get"</span></span>

    ![Affichage des distributions de Linux dans le magasin Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="004b7-134">Termine l’initialisation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="004b7-134">Complete initialization of your distro</span></span>
<span data-ttu-id="004b7-135">Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distributeur](initialize-distro.md) une fois, avant de pouvoir être utilisé.</span><span class="sxs-lookup"><span data-stu-id="004b7-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="004b7-136">Dépannage :</span><span class="sxs-lookup"><span data-stu-id="004b7-136">Troubleshooting:</span></span> 

<span data-ttu-id="004b7-137">Voici les erreurs associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="004b7-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="004b7-138">Reportez-vous à la [page Résolution des problèmes de WSL](troubleshooting.md) pour les autres erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="004b7-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="004b7-139">**Installation a échoué avec l’erreur 0 x 80070003**</span><span class="sxs-lookup"><span data-stu-id="004b7-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="004b7-140">Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (il s’agit généralement votre `C:` lecteur).</span><span class="sxs-lookup"><span data-stu-id="004b7-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="004b7-141">Assurez-vous que les distributions sont stockées sur votre lecteur système :</span><span class="sxs-lookup"><span data-stu-id="004b7-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="004b7-142">Ouvrez **paramètres** -> **stockage** -> **davantage de paramètres de stockage : Modification dans lequel le nouveau contenu est enregistré**
    ![image des paramètres système pour installer des applications sur le lecteur C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="004b7-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="004b7-143">**WslRegisterDistribution a échoué avec l’erreur 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="004b7-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="004b7-144">Le sous-système Windows pour Linux, composant facultatif n’est pas activé :</span><span class="sxs-lookup"><span data-stu-id="004b7-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="004b7-145">Ouvrez **le panneau de configuration** -> **programmes et fonctionnalités** -> \*\* activer ou désactiver la fonction Windows \*\* -> cochez **sous-système Windows pour Linux** ou à l’aide de la Applet de commande PowerShell mentionné au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="004b7-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
