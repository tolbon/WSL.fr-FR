---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256392"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="a9ba7-104">Guide d’installation sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="a9ba7-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="a9ba7-105">S’applique à Windows Server 2019 et ultérieur</span><span class="sxs-lookup"><span data-stu-id="a9ba7-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="a9ba7-106">Avec la build 2017, Microsoft a annoncé que le sous-système Windows pour Linux sera [disponible sur Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span><span class="sxs-lookup"><span data-stu-id="a9ba7-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="a9ba7-107">Ces instructions vous guident tout au long de l’exécution du sous-système Windows pour Linux sur Windows Server 1709 et ultérieur.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="a9ba7-108">Activer le sous-système Windows pour Linux (WSL)</span><span class="sxs-lookup"><span data-stu-id="a9ba7-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="a9ba7-109">Avant de pouvoir exécuter les distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » et redémarrer.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="a9ba7-110">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="a9ba7-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="a9ba7-111">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-111">Restart your computer when prompted.</span></span> <span data-ttu-id="a9ba7-112">**Ce redémarrage est nécessaire** pour s’assurer que WSL peut lancer un environnement d’exécution approuvé.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="a9ba7-113">Télécharger une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="a9ba7-113">Download a Linux distro</span></span>

<span data-ttu-id="a9ba7-114">Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="a9ba7-115">Extraire et installer une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="a9ba7-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="a9ba7-116">Maintenant que vous avez téléchargé une distribution, extrayez son contenu et installez manuellement la distribution :</span><span class="sxs-lookup"><span data-stu-id="a9ba7-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="a9ba7-117">Extrayez le contenu du package `<distro>.appx`, par exemple à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="a9ba7-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="a9ba7-118">Exécutez le lanceur de distribution. Pour réaliser l’installation, exécutez l’application de lancement de distribution dans le dossier cible, nommé `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="a9ba7-119">Par exemple : `ubuntu.exe`, etc.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Distribution Ubuntu développée sur Windows Server](media/server-appx-expand.png)

    > <span data-ttu-id="a9ba7-121">**Résolution des problèmes**</span><span class="sxs-lookup"><span data-stu-id="a9ba7-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="a9ba7-122">**Échec de l’installation avec l’erreur 0x8007007e** : Cette erreur se produit lorsque votre système ne prend pas en charge WSL.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="a9ba7-123">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="a9ba7-123">Make sure that:</span></span>
    >   * <span data-ttu-id="a9ba7-124">Vous exécutez la build Windows 16215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="a9ba7-125">[Vérifiez votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="a9ba7-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="a9ba7-126">Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="a9ba7-127">[Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="a9ba7-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="a9ba7-128">Ajoutez votre chemin de distribution au chemin d’environnement Windows (`C:\Users\Administrator\Ubuntu` dans cet exemple), par exemple, à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="a9ba7-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="a9ba7-129">Vous pouvez maintenant lancer votre distribution à partir de n’importe quel chemin en tapant `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="a9ba7-130">Par exemple : `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="a9ba7-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="a9ba7-131">Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distribution](initialize-distro.md) avant d’utiliser votre distribution.</span><span class="sxs-lookup"><span data-stu-id="a9ba7-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
