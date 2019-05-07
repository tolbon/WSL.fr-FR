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
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063287"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="5ddad-104">Sous-système Windows pour le Guide d’Installation de Linux pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="5ddad-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="5ddad-105">Installer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="5ddad-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="5ddad-106">Avant d’installer toutes les distributions Linux pour WSL, vous devez vous assurer que les « Windows sous-système pour Linux » fonctionnalité facultative est activée :</span><span class="sxs-lookup"><span data-stu-id="5ddad-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="5ddad-107">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="5ddad-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="5ddad-108">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="5ddad-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="5ddad-109">Installer votre Distribution Linux de choix</span><span class="sxs-lookup"><span data-stu-id="5ddad-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="5ddad-110">Pour télécharger et installer votre distro(s) préférée, vous avez trois possibilités :</span><span class="sxs-lookup"><span data-stu-id="5ddad-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="5ddad-111">Téléchargez et installez depuis le Store de Windows (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="5ddad-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="5ddad-112">Télécharger et installer à partir de la commande-ligne ou des scripts ([Lisez les instructions d’installation manuelle](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="5ddad-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="5ddad-113">Télécharger et décompresser et installer manuellement (pour Windows Server - [instructions fournies ici](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="5ddad-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="5ddad-114">Windows 10 Fall Creators Update et versions ultérieures : Installer à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="5ddad-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="5ddad-115">Cette section concerne Windows build 16215 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="5ddad-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="5ddad-116">Suivez ces étapes pour [vérifier votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="5ddad-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="5ddad-117">Le Microsoft Store et votre distribution Linux favorite.</span><span class="sxs-lookup"><span data-stu-id="5ddad-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Affichage des distributions de Linux dans le magasin Windows](media/store.png)

    <span data-ttu-id="5ddad-119">Les liens suivants seront ouvre à la page magasin de Windows pour chaque distribution :</span><span class="sxs-lookup"><span data-stu-id="5ddad-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="5ddad-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="5ddad-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="5ddad-121">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="5ddad-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="5ddad-122">SLES</span><span class="sxs-lookup"><span data-stu-id="5ddad-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="5ddad-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="5ddad-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="5ddad-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="5ddad-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="5ddad-125">À partir de la page de la distribution, sélectionnez « Get »</span><span class="sxs-lookup"><span data-stu-id="5ddad-125">From the distro's page, select "Get"</span></span>

    ![Affichage des distributions de Linux dans le magasin Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="5ddad-127">Termine l’initialisation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="5ddad-127">Complete initialization of your distro</span></span>
<span data-ttu-id="5ddad-128">Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distributeur](initialize-distro.md) une fois, avant de pouvoir être utilisé.</span><span class="sxs-lookup"><span data-stu-id="5ddad-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="5ddad-129">Dépannage :</span><span class="sxs-lookup"><span data-stu-id="5ddad-129">Troubleshooting:</span></span> 

<span data-ttu-id="5ddad-130">Voici les erreurs associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="5ddad-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="5ddad-131">Reportez-vous à la [page Résolution des problèmes de WSL](troubleshooting.md) pour les autres erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="5ddad-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="5ddad-132">**Installation a échoué avec l’erreur 0 x 80070003**</span><span class="sxs-lookup"><span data-stu-id="5ddad-132">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="5ddad-133">Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (il s’agit généralement votre `C:` lecteur).</span><span class="sxs-lookup"><span data-stu-id="5ddad-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="5ddad-134">Assurez-vous que les distributions sont stockées sur votre lecteur système :</span><span class="sxs-lookup"><span data-stu-id="5ddad-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="5ddad-135">Ouvrez **paramètres** -> **stockage** -> **davantage de paramètres de stockage : Modification dans lequel le nouveau contenu est enregistré**
    ![image des paramètres système pour installer des applications sur le lecteur C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="5ddad-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
