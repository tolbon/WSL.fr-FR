---
title: Télécharger manuellement le sous-système Windows pour Linux (WSL) distributions
description: Instructions sur la façon de télécharger manuellement le sous-système Windows pour les distributions Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, WSL, sous-système Windows, distribution, Ubuntu, openSUSE, SLES, Debian, Kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 55cea2c4b7087f3dd8a29986aaddc8c313763448
ms.sourcegitcommit: b07769a3140db9ac63e42c7d7d1290c0bad8c40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67467552"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="7332f-104">Télécharger manuellement le sous-système Windows pour les packages distribution Linux</span><span class="sxs-lookup"><span data-stu-id="7332f-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="7332f-105">Il existe plusieurs scénarios dans lesquels il est possible que vous ne soyez pas en mesure d’installer WSL Linux distributions via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7332f-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="7332f-106">Plus précisément, vous utilisez peut-être une référence de système d’exploitation de bureau Windows Server ou long-term maintenance (LTSB/LTSC) qui ne prend pas en charge Microsoft Store, ou vos stratégies de réseau d’entreprise et/ou administrateurs ne peuvent pas autoriser l’utilisation d’Microsoft Store dans votre environnement.</span><span class="sxs-lookup"><span data-stu-id="7332f-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="7332f-107">Dans ce cas, bien que WSL soit disponible, comment télécharger et installer Linux distributions dans WSL si vous ne pouvez pas accéder au Store?</span><span class="sxs-lookup"><span data-stu-id="7332f-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="7332f-108">Remarque : **Les environnements d’interpréteur de ligne de commande, notamment cmd, PowerShell et Linux/WSL distributions, ne sont pas autorisés à s’exécuter sur le mode Windows 10 S**.</span><span class="sxs-lookup"><span data-stu-id="7332f-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="7332f-109">Cette restriction existe afin de garantir l’intégrité et les objectifs de sécurité fournis par le mode S: Pour plus d’informations, lisez [ce billet](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) .</span><span class="sxs-lookup"><span data-stu-id="7332f-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="7332f-110">Téléchargement de distributions</span><span class="sxs-lookup"><span data-stu-id="7332f-110">Downloading distros</span></span>

<span data-ttu-id="7332f-111">Si l’application Microsoft Store n’est pas disponible, vous pouvez télécharger et installer manuellement les distributions Linux en cliquant sur les liens suivants:</span><span class="sxs-lookup"><span data-stu-id="7332f-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="7332f-112">Ubuntu 18,04</span><span class="sxs-lookup"><span data-stu-id="7332f-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="7332f-113">Ubuntu 18,04 ARM</span><span class="sxs-lookup"><span data-stu-id="7332f-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="7332f-114">Ubuntu 16,04</span><span class="sxs-lookup"><span data-stu-id="7332f-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="7332f-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="7332f-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="7332f-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="7332f-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="7332f-117">OpenSUSE LEAP 42</span><span class="sxs-lookup"><span data-stu-id="7332f-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="7332f-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="7332f-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="7332f-119">Fedora Remix pour WSL</span><span class="sxs-lookup"><span data-stu-id="7332f-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="7332f-120">Cela entraîne le `<distro>.appx` téléchargement des packages dans un dossier de votre choix.</span><span class="sxs-lookup"><span data-stu-id="7332f-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="7332f-121">Suivez les [instructions d’installation](#Installing-your-distro) pour installer vos distribution téléchargés.</span><span class="sxs-lookup"><span data-stu-id="7332f-121">Follow the [installation instructions](#Installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="7332f-122">Téléchargement de distributions via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="7332f-122">Downloading distros via the command line</span></span>
<span data-ttu-id="7332f-123">Si vous préférez, vous pouvez également télécharger vos distribution préférés à l’aide de la ligne de commande:</span><span class="sxs-lookup"><span data-stu-id="7332f-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="7332f-124">Télécharger à l’aide de PowerShell</span><span class="sxs-lookup"><span data-stu-id="7332f-124">Download using PowerShell</span></span>
 <span data-ttu-id="7332f-125">Pour télécharger distributions à l’aide de PowerShell, utilisez l’applet [de commande Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) .</span><span class="sxs-lookup"><span data-stu-id="7332f-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="7332f-126">Voici un exemple d’instruction pour télécharger Ubuntu 16,04.</span><span class="sxs-lookup"><span data-stu-id="7332f-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="7332f-127">Si le téléchargement prend beaucoup de temps, désactivez la barre de progression en définissant`$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="7332f-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="7332f-128">Télécharger à l’aide de la boucle</span><span class="sxs-lookup"><span data-stu-id="7332f-128">Download using curl</span></span>
<span data-ttu-id="7332f-129">La mise à jour Spring 2018 de Windows 10 (ou version ultérieure) comprend l' [utilitaire de ligne de commande de boucles](https://curl.haxx.se/) populaires avec lequel vous pouvez appeler des requêtes Web (par exemple, des commandes HTTP, http, put, etc.) à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7332f-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="7332f-130">Vous pouvez utiliser `curl.exe` pour télécharger les distributions ci-dessus:</span><span class="sxs-lookup"><span data-stu-id="7332f-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="7332f-131">Dans l’exemple ci- `curl.exe` dessus, est exécuté ( `curl`pas seulement) pour garantir que, dans PowerShell, l’exécutable Real bouclé est appelé, et non l’alias PowerShell pour [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="7332f-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="7332f-132">Remarque : L' `curl` utilisation de peut être préférable si vous devez appeler/écrire des étapes de téléchargement à l’aide de `.bat` CMD Shell et/ou  /  `.cmd` de scripts.</span><span class="sxs-lookup"><span data-stu-id="7332f-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="7332f-133">Installation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="7332f-133">Installing your distro</span></span>
<span data-ttu-id="7332f-134">Si vous utilisez Windows 10, vous pouvez installer votre distribution avec PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7332f-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="7332f-135">Accédez simplement au dossier contenant le distribution téléchargé à partir de la version ci-dessus et, dans ce `app_name` répertoire, exécutez la commande suivante, où est le nom de votre fichier distribution. Appx.</span><span class="sxs-lookup"><span data-stu-id="7332f-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="7332f-136">Si vous utilisez Windows Server, vous trouverez les instructions d’installation sur la page de documentation de [Windows Server](install-on-server.md) .</span><span class="sxs-lookup"><span data-stu-id="7332f-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="7332f-137">Une fois votre distribution installé, reportez-vous à la page [étapes Intilization](initialize-distro.md) pour initialiser votre nouveau distribution.</span><span class="sxs-lookup"><span data-stu-id="7332f-137">Once your distro is installed please refer to the [Intilization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
