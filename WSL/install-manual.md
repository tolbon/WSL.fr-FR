---
title: Télécharger manuellement des distributions du sous-système Windows pour Linux (WSL)
description: Instructions sur la façon de télécharger manuellement des distributions du sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, WSL, sous-système windows, distribution, ubuntu, openSUSE, SLES, debian, kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 37d8ad589d0108534c27137614a005c0c0ac55bc
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256372"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="9309b-104">Télécharger manuellement des packages de distribution du sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="9309b-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="9309b-105">Il existe plusieurs scénarios où vous pouvez ne pas être en mesure d’installer (ou ne pas vouloir installer) des distributions WSL Linux via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9309b-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="9309b-106">Plus précisément, vous utilisez peut-être une référence SKU de système d’exploitation de bureau Windows Server ou de maintenance à long terme (LTSC) qui ne prend pas en charge le Microsoft Store, ou vos stratégies et/ou administrateurs de réseau d’entreprise ne permettent pas l’utilisation du Microsoft Store dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="9309b-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="9309b-107">Dans ces cas, alors que WSL est lui-même disponible, comment télécharger et installer des distributions Linux dans WSL si vous ne pouvez pas accéder au Store ?</span><span class="sxs-lookup"><span data-stu-id="9309b-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="9309b-108">Remarque : **Les environnements d’interpréteur de ligne de commande, notamment cmd, PowerShell et les distributions Linux/WSL, ne sont pas autorisés à s’exécuter sur Windows 10 en mode S**.</span><span class="sxs-lookup"><span data-stu-id="9309b-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="9309b-109">Cette restriction a pour but de garantir les objectifs d’intégrité et de sécurité fournis par le mode S : Lisez [cette publication](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="9309b-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="9309b-110">Téléchargement de distributions</span><span class="sxs-lookup"><span data-stu-id="9309b-110">Downloading distros</span></span>

<span data-ttu-id="9309b-111">Si l’application Microsoft Store n’est pas disponible, vous pouvez télécharger et installer manuellement les distributions Linux en cliquant sur les liens suivants :</span><span class="sxs-lookup"><span data-stu-id="9309b-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="9309b-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="9309b-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="9309b-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="9309b-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="9309b-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="9309b-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="9309b-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="9309b-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="9309b-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="9309b-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="9309b-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="9309b-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="9309b-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="9309b-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="9309b-119">Fedora Remix pour WSL</span><span class="sxs-lookup"><span data-stu-id="9309b-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="9309b-120">Cela entraîne le téléchargement des packages `<distro>.appx` dans un dossier de votre choix.</span><span class="sxs-lookup"><span data-stu-id="9309b-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="9309b-121">Suivez les [instructions d’installation](#installing-your-distro) pour installer la ou les distributions téléchargées.</span><span class="sxs-lookup"><span data-stu-id="9309b-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="9309b-122">Téléchargement de distributions via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="9309b-122">Downloading distros via the command line</span></span>
<span data-ttu-id="9309b-123">Si vous préférez, vous pouvez également télécharger vos distributions préférées via la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="9309b-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="9309b-124">Télécharger à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="9309b-124">Download using PowerShell</span></span>
 <span data-ttu-id="9309b-125">Pour télécharger des distributions à l’aide de PowerShell, utilisez l’applet de commande [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest).</span><span class="sxs-lookup"><span data-stu-id="9309b-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="9309b-126">Voici un exemple d’instruction permettant de télécharger Ubuntu 16.04.</span><span class="sxs-lookup"><span data-stu-id="9309b-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="9309b-127">Si le téléchargement prend beaucoup de temps, désactivez la barre de progression en définissant `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="9309b-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="9309b-128">Télécharger à l’aide de curl</span><span class="sxs-lookup"><span data-stu-id="9309b-128">Download using curl</span></span>
<span data-ttu-id="9309b-129">La mise à jour de Windows 10 Printemps 2018 (ou ultérieure) inclut l’[utilitaire de ligne de commande curl](https://curl.haxx.se/) populaire avec lequel vous pouvez appeler des requêtes web (par exemple, des commandes HTTP GET, POST, PUT, etc.) à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="9309b-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="9309b-130">Vous pouvez utiliser `curl.exe` pour télécharger les distributions ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="9309b-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="9309b-131">Dans l’exemple ci-dessus, `curl.exe` est exécuté (pas seulement `curl`) pour s’assurer que, dans PowerShell, l’exécutable curl réel est appelé, et non pas l’alias curl PowerShell pour [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="9309b-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="9309b-132">Remarque : L’utilisation de `curl` peut être préférable si vous devez écrire des scripts/appeler des étapes de téléchargement à l’aide de l’interpréteur cmd et/ou des scripts `.bat` / `.cmd`.</span><span class="sxs-lookup"><span data-stu-id="9309b-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="9309b-133">Installation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="9309b-133">Installing your distro</span></span>
<span data-ttu-id="9309b-134">Si vous utilisez Windows 10, vous pouvez installer votre distribution avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9309b-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="9309b-135">Accédez simplement au dossier contenant la distribution téléchargée ci-dessus et, dans ce répertoire, exécutez la commande suivante avec `app_name` comme nom de votre fichier .appx de distribution.</span><span class="sxs-lookup"><span data-stu-id="9309b-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="9309b-136">Si vous utilisez Windows Server, vous trouverez les instructions d’installation dans la page de documentation de [Windows Server](install-on-server.md).</span><span class="sxs-lookup"><span data-stu-id="9309b-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="9309b-137">Une fois votre distribution installée, reportez-vous à la page [Étapes d’initialisation](initialize-distro.md) pour initialiser votre nouvelle distribution.</span><span class="sxs-lookup"><span data-stu-id="9309b-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
