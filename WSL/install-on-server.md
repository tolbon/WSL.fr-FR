---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Windows Server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308791"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="004b3-104">Guide d’installation de Windows Server</span><span class="sxs-lookup"><span data-stu-id="004b3-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="004b3-105">S’applique à Windows Server 2019 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="004b3-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="004b3-106">Chez//Build2017, Microsoft a annoncé que le sous-système Windows pour Linux sera [disponible sur Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="004b3-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="004b3-107">Ces instructions vous guident tout au long de l’exécution du sous-système Windows pour Linux sur Windows Server 1709 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="004b3-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="004b3-108">Activer le sous-système Windows pour Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="004b3-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="004b3-109">Avant de pouvoir exécuter Linux distributions sur Windows, vous devez activer la fonctionnalité facultative «sous-système Windows pour Linux» et redémarrer.</span><span class="sxs-lookup"><span data-stu-id="004b3-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="004b3-110">Ouvrez PowerShell en tant qu’administrateur et exécutez:</span><span class="sxs-lookup"><span data-stu-id="004b3-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="004b3-111">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="004b3-111">Restart your computer when prompted.</span></span> <span data-ttu-id="004b3-112">**Ce redémarrage est nécessaire** pour garantir que WSL peut lancer un environnement d’exécution approuvé.</span><span class="sxs-lookup"><span data-stu-id="004b3-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="004b3-113">Télécharger un distribution Linux</span><span class="sxs-lookup"><span data-stu-id="004b3-113">Download a Linux distro</span></span>

<span data-ttu-id="004b3-114">Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="004b3-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="004b3-115">Extraire et installer un distribution Linux</span><span class="sxs-lookup"><span data-stu-id="004b3-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="004b3-116">Maintenant que vous avez téléchargé un distribution, extrayez son contenu et installez manuellement le distribution:</span><span class="sxs-lookup"><span data-stu-id="004b3-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="004b3-117">Extrayez le `<distro>.appx` contenu du package, par exemple à l’aide de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="004b3-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="004b3-118">Exécutez le lanceur distribution pour terminer l’installation, exécutez l’application distribution Launcher dans le dossier cible `<distro>.exe`, nommé.</span><span class="sxs-lookup"><span data-stu-id="004b3-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="004b3-119">Par exemple: `ubuntu.exe`, etc.</span><span class="sxs-lookup"><span data-stu-id="004b3-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Ubuntu distribution développé sur Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="004b3-121">**Dépannage**</span><span class="sxs-lookup"><span data-stu-id="004b3-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="004b3-122">**Échec de l’installation avec l’erreur 0x8007007e**: Cette erreur se produit lorsque votre système ne prend pas en charge WSL.</span><span class="sxs-lookup"><span data-stu-id="004b3-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="004b3-123">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="004b3-123">Make sure that:</span></span>
    >   * <span data-ttu-id="004b3-124">Vous exécutez Windows Build 16215 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="004b3-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="004b3-125">[Vérifiez votre Build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="004b3-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="004b3-126">Le composant facultatif sous-système Windows pour Linux est activé et l’ordinateur a redémarré.</span><span class="sxs-lookup"><span data-stu-id="004b3-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="004b3-127">Vérifiez [que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="004b3-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="004b3-128">Ajoutez votre chemin distribution au chemin d’accès de l'`C:\Users\Administrator\Ubuntu` environnement Windows (dans cet exemple), par exemple, à l’aide de PowerShell:</span><span class="sxs-lookup"><span data-stu-id="004b3-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="004b3-129">Vous pouvez maintenant lancer votre distribution à partir de n’importe `<distro>.exe`quel chemin d’accès en tapant.</span><span class="sxs-lookup"><span data-stu-id="004b3-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="004b3-130">Par exemple : `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="004b3-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="004b3-131">Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distribution avant d'](initialize-distro.md) utiliser votre distribution.</span><span class="sxs-lookup"><span data-stu-id="004b3-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
