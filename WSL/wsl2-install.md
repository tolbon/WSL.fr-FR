---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c031b1348a77e1dac967fae5e4df772e10a9084
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256342"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="21b57-104">Instructions d’installation pour WSL 2</span><span class="sxs-lookup"><span data-stu-id="21b57-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="21b57-105">Vous pouvez regarder la vidéo ci-dessous ou lire cet article pour découvrir comment installer WSL2.</span><span class="sxs-lookup"><span data-stu-id="21b57-105">You can watch the video below, or read on in this article to learn how to install WSL2.</span></span> 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

<span data-ttu-id="21b57-106">Pour installer et commencer à utiliser WSL 2, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="21b57-106">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="21b57-107">WSL 2 est disponible uniquement dans les builds 18917 et ultérieures de Windows 10</span><span class="sxs-lookup"><span data-stu-id="21b57-107">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="21b57-108">Vérifiez que vous avez installé WSL (vous trouverez des instructions pour cela [ici](./install-win10.md)) et que vous exécutez la **build 18917** ou ultérieure de Windows 10</span><span class="sxs-lookup"><span data-stu-id="21b57-108">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="21b57-109">Pour veiller à utiliser la build 18917 ou ultérieure, rejoignez [le programme Windows Insider](https://insider.windows.com/en-us/) et sélectionnez l’anneau « Rapide » ou l’anneau « Lent ».</span><span class="sxs-lookup"><span data-stu-id="21b57-109">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="21b57-110">Vous pouvez vérifier votre version de Windows en ouvrant l’invite de commandes et en exécutant la commande `ver`.</span><span class="sxs-lookup"><span data-stu-id="21b57-110">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="21b57-111">Activer le composant facultatif « Plateforme de machine virtuelle »</span><span class="sxs-lookup"><span data-stu-id="21b57-111">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="21b57-112">Définir une distribution basée sur WSL 2 en utilisant la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="21b57-112">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="21b57-113">Vérifier les versions de WSL que vos distributions utilisent</span><span class="sxs-lookup"><span data-stu-id="21b57-113">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="21b57-114">Activer le composant facultatif « Plateforme de machine virtuelle » et s’assurer que WSL est activé</span><span class="sxs-lookup"><span data-stu-id="21b57-114">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="21b57-115">Vous devez vous assurer que le sous-système Windows pour Linux et les composants facultatifs de la plateforme de machine virtuelle sont installés.</span><span class="sxs-lookup"><span data-stu-id="21b57-115">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="21b57-116">Pour ce faire, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="21b57-116">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="21b57-117">Redémarrez votre machine pour terminer l’installation des deux composants.</span><span class="sxs-lookup"><span data-stu-id="21b57-117">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="21b57-118">Définir une distribution basée sur WSL 2 en utilisant la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="21b57-118">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="21b57-119">Si vous n’avez pas de distribution Linux installée, reportez-vous à la page [Installer sur Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) pour obtenir des instructions sur son installation.</span><span class="sxs-lookup"><span data-stu-id="21b57-119">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="21b57-120">Pour définir une distribution, exécutez :</span><span class="sxs-lookup"><span data-stu-id="21b57-120">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="21b57-121">et veillez à remplacer `<Distro>` par le vrai nom de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="21b57-121">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="21b57-122">(Vous pouvez le trouver avec la commande : `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="21b57-122">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="21b57-123">Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».</span><span class="sxs-lookup"><span data-stu-id="21b57-123">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="21b57-124">Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="21b57-124">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="21b57-125">Ainsi, toutes les nouvelles distributions que vous installerez seront initialisées en tant que distributions WSL 2.</span><span class="sxs-lookup"><span data-stu-id="21b57-125">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="21b57-126">Pour terminer, vérifiez quelles versions de WSL utilisent vos distributions.</span><span class="sxs-lookup"><span data-stu-id="21b57-126">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="21b57-127">Pour vérifier les versions de WSL qu’utilise chaque distribution, utilisez la commande suivante (disponible uniquement dans la build 18917 ou ultérieure de Windows) :</span><span class="sxs-lookup"><span data-stu-id="21b57-127">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="21b57-128">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="21b57-128">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="21b57-129">La distribution que vous avez choisie ci-dessus doit maintenant afficher un « 2 » dans la colonne « version ».</span><span class="sxs-lookup"><span data-stu-id="21b57-129">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="21b57-130">Maintenant que vous avez terminé, n’hésitez pas à commencer à utiliser votre distribution WSL 2 !</span><span class="sxs-lookup"><span data-stu-id="21b57-130">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="21b57-131">Dépannage :</span><span class="sxs-lookup"><span data-stu-id="21b57-131">Troubleshooting:</span></span> 

<span data-ttu-id="21b57-132">Vous trouverez ci-dessous des erreurs associées et des suggestions de correction lors de l’installation de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="21b57-132">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="21b57-133">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir d’autres erreurs WSL générales et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="21b57-133">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="21b57-134">**Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="21b57-134">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="21b57-135">Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="21b57-135">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="21b57-136">Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.</span><span class="sxs-lookup"><span data-stu-id="21b57-136">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="21b57-137">**Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="21b57-137">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="21b57-138">Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez Windows version de build 18917 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="21b57-138">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="21b57-139">Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="21b57-139">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="21b57-140">Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="21b57-140">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="21b57-141">**Impossible de terminer l’opération demandée du fait d’une limitation du système de disque virtuel. Les fichiers de disque dur virtuel doivent être décompressés et déchiffrés, mais ne doivent pas être partiellement alloués.**</span><span class="sxs-lookup"><span data-stu-id="21b57-141">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="21b57-142">Vérifiez le [thread GitHub WSL n° 4103](https://github.com/microsoft/WSL/issues/4103) où ce problème est suivi pour obtenir des informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="21b57-142">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="21b57-143">**Le terme « wsl » n’est pas reconnu comme nom d’applet de commande, fonction, fichier de script ou programme exécutable.**</span><span class="sxs-lookup"><span data-stu-id="21b57-143">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="21b57-144">Assurez-vous que le [composant facultatif Sous-système Windows pour Linux est installé](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="21b57-144">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="21b57-145">De plus, si vous utilisez un appareil Arm64 et exécutez cette commande à partir de PowerShell, vous recevrez cette erreur.</span><span class="sxs-lookup"><span data-stu-id="21b57-145">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="21b57-146">Au lieu de cela, exécutez `wsl.exe` à partir de [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="21b57-146">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
