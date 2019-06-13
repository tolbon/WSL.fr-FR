---
title: Télécharger manuellement le sous-système de Windows pour les distributions de Linux (WSL)
description: Instructions pour savoir comment télécharger manuellement le sous-système de Windows pour les distributions Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, WSL, sous-système windows, distributeur, ubuntu, openSUSE, kali debian, SLES,
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 669c017c97aba70c107484b32acd99296265d84a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035037"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="a8ef1-104">Télécharger manuellement le sous-système de Windows pour les packages de distribution de Linux</span><span class="sxs-lookup"><span data-stu-id="a8ef1-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="a8ef1-105">Il existe plusieurs scénarios dans lequel peut ne pas pouvoir (ou souhaitez) pour installer des distributions de Linux de WSL via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="a8ef1-106">Plus précisément, vous exécutez peut-être un serveur Windows ou le bureau de Long-Term Servicing (LTSB/LTSC) référence (SKU) du système d’exploitation qui ne prennent en charge Microsoft Store, ou vos stratégies de réseau d’entreprise et/ou Administrateurs pour autoriser l’utilisation de Microsoft Store ne pas dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="a8ef1-107">Dans ces cas, tandis que WSL lui-même est disponible, comment télécharger et installer des distributions de Linux dans WSL si vous ne pouvez pas accéder au magasin ?</span><span class="sxs-lookup"><span data-stu-id="a8ef1-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="a8ef1-108">Remarque: **Environnements de shell de ligne de commande, y compris les distributions Linux/WSL Cmd et PowerShell ne sont pas autorisées à s’exécuter sur Windows 10 S Mode**.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="a8ef1-109">Cette restriction existe afin de garantir les objectifs de l’intégrité et la sécurité en Mode S offre : Lecture [ce billet](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="a8ef1-110">Téléchargement de distributions</span><span class="sxs-lookup"><span data-stu-id="a8ef1-110">Downloading distros</span></span>

<span data-ttu-id="a8ef1-111">Si l’application Microsoft Store n’est pas disponible, vous pouvez télécharger et installer manuellement les distributions de Linux en cliquant sur ces liens :</span><span class="sxs-lookup"><span data-stu-id="a8ef1-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="a8ef1-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="a8ef1-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="a8ef1-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="a8ef1-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="a8ef1-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="a8ef1-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="a8ef1-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="a8ef1-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="a8ef1-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="a8ef1-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="a8ef1-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="a8ef1-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="a8ef1-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="a8ef1-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="a8ef1-119">Remix Fedora pour WSL</span><span class="sxs-lookup"><span data-stu-id="a8ef1-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="a8ef1-120">Cela entraîne le `<distro>.appx` packages à télécharger vers un dossier de votre choix.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="a8ef1-121">Suivez le [instructions d’installation](#installing-your-distro) pour installer votre distro(s) téléchargé.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="a8ef1-122">Téléchargement des distributions via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="a8ef1-122">Downloading distros via the command line</span></span>
<span data-ttu-id="a8ef1-123">Si vous préférez, vous pouvez également télécharger votre distro(s) préféré par le biais de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="a8ef1-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="a8ef1-124">Télécharger à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="a8ef1-124">Download using PowerShell</span></span>
 <span data-ttu-id="a8ef1-125">Pour télécharger les distributions à l’aide de PowerShell, utilisez le [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) applet de commande.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="a8ef1-126">Voici un exemple d’instruction pour télécharger Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="a8ef1-127">Si le téléchargement prend beaucoup de temps, désactiver la barre de progression en définissant `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="a8ef1-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="a8ef1-128">Télécharger à l’aide de curl</span><span class="sxs-lookup"><span data-stu-id="a8ef1-128">Download using curl</span></span>
<span data-ttu-id="a8ef1-129">Mise à jour Windows 10 printemps 2018 (ou version ultérieure) inclut le fameux [curl utilitaire de ligne de commande](https://curl.haxx.se/) avec laquelle vous pouvez appeler les requêtes web (par exemple, HTTP GET, POST, méthode PUT, les commandes etc.) à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="a8ef1-130">Vous pouvez utiliser `curl.exe` pour télécharger les distributions ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="a8ef1-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="a8ef1-131">Dans l’exemple ci-dessus, `curl.exe` est exécutée (pas seulement `curl`) pour vous assurer que, dans PowerShell, le fichier exécutable réel curl est appelé, pas PowerShell curl alias [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="a8ef1-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="a8ef1-132">Remarque: À l’aide de `curl` peut être préférable si vous devez appeler/script des étapes de téléchargement à l’aide de Cmd shell et/ou `.bat`  /  `.cmd` scripts.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="a8ef1-133">L’installation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="a8ef1-133">Installing your distro</span></span>
<span data-ttu-id="a8ef1-134">Pour obtenir des instructions sur la façon d’installer votre distro(s) téléchargé, reportez-vous à la [Windows Desktop](install-win10.md) ou [Windows Server](install-on-server.md) instructions d’installation.</span><span class="sxs-lookup"><span data-stu-id="a8ef1-134">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
