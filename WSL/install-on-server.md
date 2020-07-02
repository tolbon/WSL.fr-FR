---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671019"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="d37e2-104">Guide d’installation sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="d37e2-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="d37e2-105">Le sous-système Windows pour Linux peut être installé sur Windows Server 2019 (version 1709) et ultérieur.</span><span class="sxs-lookup"><span data-stu-id="d37e2-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="d37e2-106">Ce guide vous accompagne tout au long des étapes d’activation de WSL sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d37e2-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="d37e2-107">Activer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="d37e2-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="d37e2-108">Avant de pouvoir exécuter les distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » et redémarrer.</span><span class="sxs-lookup"><span data-stu-id="d37e2-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="d37e2-109">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="d37e2-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="d37e2-110">Télécharger une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="d37e2-110">Download a Linux distribution</span></span>

<span data-ttu-id="d37e2-111">Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="d37e2-111">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="d37e2-112">Extraire et installer une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="d37e2-112">Extract and install a Linux distribution</span></span>

<span data-ttu-id="d37e2-113">Maintenant que vous avez téléchargé une distribution Linux, afin d’extraire son contenu et de l’installer manuellement, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="d37e2-113">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="d37e2-114">Extrayez le contenu du package `<distro>.appx` à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="d37e2-114">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="d37e2-115">Exécutez l’application de lancement de distribution dans le dossier cible.</span><span class="sxs-lookup"><span data-stu-id="d37e2-115">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="d37e2-116">Le lanceur est généralement nommé `<distro>.exe` (par exemple, `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="d37e2-116">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Distribution Ubuntu développée sur Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="d37e2-118">**Échec de l’installation avec l’erreur 0x8007007e** : Si vous recevez cette erreur, votre système ne prend pas en charge WSL.</span><span class="sxs-lookup"><span data-stu-id="d37e2-118">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="d37e2-119">Veillez à exécuter la build 16215 ou ultérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="d37e2-119">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="d37e2-120">[Vérifiez votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="d37e2-120">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="d37e2-121">[Vérifiez également que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled) et que votre ordinateur a été redémarré après l’activation de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="d37e2-121">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="d37e2-122">3. Ajoutez votre chemin de distribution à la variable PATH de chemin d’environnement Windows (`C:\Users\Administrator\Ubuntu` dans cet exemple), à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="d37e2-122">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="d37e2-123">Vous pouvez maintenant lancer votre distribution à partir de n’importe quel chemin en tapant `<distro>.exe`.</span><span class="sxs-lookup"><span data-stu-id="d37e2-123">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="d37e2-124">Par exemple : `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="d37e2-124">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="d37e2-125">Maintenant qu’elle est installée, vous devez [initialiser votre nouvelle instance de distribution](initialize-distro.md) avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="d37e2-125">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
