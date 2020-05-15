---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 86fd7de0ef45af760f46bb2a18932f513b813609
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270883"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="3bc5e-104">Guide d’installation sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="3bc5e-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="3bc5e-105">Le sous-système Windows pour Linux peut être installé sur Windows Server 2019 (version 1709) et ultérieur.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="3bc5e-106">Ce guide vous accompagne tout au long des étapes d’activation de WSL sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="3bc5e-107">Activer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="3bc5e-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="3bc5e-108">Avant de pouvoir exécuter les distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » et redémarrer.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="3bc5e-109">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="3bc5e-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

<span data-ttu-id="3bc5e-110">**Si vous recherchez une compatibilité à 100 % des appels système et des performances d’E/S plus rapides, lisez ce qui suit pour installer WSL 2.**</span><span class="sxs-lookup"><span data-stu-id="3bc5e-110">**If you're looking for 100% system call compatibility and faster IO performance, read below to install WSL 2!**</span></span>

<span data-ttu-id="3bc5e-111">WSL 2 est disponible uniquement dans Windows 10, version 2004, build 19041 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-111">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="3bc5e-112">Vous devez [mettre à jour votre version de Windows](ms-settings:windowsupdate) et [rejoindre le programme Windows Insider](https://insider.windows.com/insidersigninboth/) sur l’anneau « Release Preview » jusqu’à la publication de la version publique fin mai.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-112">You will need to [update your Windows version](ms-settings:windowsupdate) and [join the Windows Insider program](https://insider.windows.com/insidersigninboth/) on the "Release Preview" ring until the public release in late May.</span></span>

<span data-ttu-id="3bc5e-113">**Si vous continuez avec WSL 1, redémarrez votre ordinateur lorsque vous y êtes invité et poursuivez l’installation [ici](./install-on-server.md#download-a-linux-distribution)**</span><span class="sxs-lookup"><span data-stu-id="3bc5e-113">**If continuing with WSL 1, restart your machine when prompted and continue with installation [here](./install-on-server.md#download-a-linux-distribution)**</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="3bc5e-114">Activer le composant facultatif Plateforme de machine virtuelle</span><span class="sxs-lookup"><span data-stu-id="3bc5e-114">Enable the Virtual Machine Platform optional component</span></span>

<span data-ttu-id="3bc5e-115">Veillez à ce que le composant facultatif « Plateforme de machine virtuelle » soit installé.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-115">Ensure the 'Virtual Machine Platform' optional component is installed.</span></span> <span data-ttu-id="3bc5e-116">Pour ce faire, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3bc5e-116">You can do that by running the following command in PowerShell:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="3bc5e-117">Télécharger une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="3bc5e-117">Download a Linux distribution</span></span>

<span data-ttu-id="3bc5e-118">Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-118">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="3bc5e-119">Extraire et installer une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="3bc5e-119">Extract and install a Linux distribution</span></span>

<span data-ttu-id="3bc5e-120">Maintenant que vous avez téléchargé une distribution Linux, afin d’extraire son contenu et de l’installer manuellement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3bc5e-120">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="3bc5e-121">Extrayez le contenu du package `<distro>.appx` à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3bc5e-121">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="3bc5e-122">Exécutez l’application de lancement de distribution dans le dossier cible.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-122">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="3bc5e-123">Le lanceur est généralement nommé `<distro>.exe` (par exemple, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="3bc5e-123">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Distribution Ubuntu développée sur Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="3bc5e-125">**Échec de l’installation avec l’erreur 0x8007007e** : Si vous recevez cette erreur, votre système ne prend pas en charge WSL.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-125">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="3bc5e-126">Veillez à exécuter la build 16215 ou ultérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-126">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="3bc5e-127">[Vérifiez votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="3bc5e-127">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="3bc5e-128">[Vérifiez également que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled) et que votre ordinateur a été redémarré après l’activation de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-128">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="3bc5e-129">3. Ajoutez votre chemin de distribution à la variable PATH de chemin d’environnement Windows (`C:\Users\Administrator\Ubuntu` dans cet exemple), à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="3bc5e-129">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="3bc5e-130">Vous pouvez maintenant lancer votre distribution à partir de n’importe quel chemin en tapant `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-130">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="3bc5e-131">Par exemple : `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-131">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="3bc5e-132">Maintenant qu’elle est installée, vous devez [initialiser votre nouvelle instance de distribution](initialize-distro.md) avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="3bc5e-132">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
