---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: bced0fd0bf948842b8c465f645aa5c368c2f4335
ms.sourcegitcommit: ebc6ae7e7546a6d33644e68788fa0215028859b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2019
ms.locfileid: "71070307"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="4bacf-104">Instructions d’installation pour WSL 2</span><span class="sxs-lookup"><span data-stu-id="4bacf-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="4bacf-105">Pour installer et commencer à utiliser WSL 2, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4bacf-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="4bacf-106">Vérifiez que vous avez installé WSL (vous trouverez des instructions pour le faire [ici](./install-win10.md)) et que vous exécutez Windows 10 Build 18917 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4bacf-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
   - <span data-ttu-id="4bacf-107">Pour vous assurer que vous utilisez la version 18917 ou une version ultérieure, rejoignez [le programme Windows Insider](https://insider.windows.com/en-us/) et sélectionnez l’anneau « Fast ».</span><span class="sxs-lookup"><span data-stu-id="4bacf-107">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="4bacf-108">Vous pouvez vérifier votre version de Windows en ouvrant l’invite de commandes `ver` et en exécutant la commande.</span><span class="sxs-lookup"><span data-stu-id="4bacf-108">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="4bacf-109">Activer le composant facultatif « Plateforme de machine virtuelle »</span><span class="sxs-lookup"><span data-stu-id="4bacf-109">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="4bacf-110">Définir une distribution basée sur WSL 2 en utilisant la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="4bacf-110">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="4bacf-111">Vérifier les versions de WSL que vos distributions utilisent</span><span class="sxs-lookup"><span data-stu-id="4bacf-111">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="4bacf-112">Activez le composant facultatif « plateforme de machine virtuelle » et assurez-vous que WSL est activé</span><span class="sxs-lookup"><span data-stu-id="4bacf-112">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="4bacf-113">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="4bacf-113">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="4bacf-114">Cela permet de s’assurer que les composants facultatifs plateforme de machine virtuelle et sous-système Windows pour Linux sont installés.</span><span class="sxs-lookup"><span data-stu-id="4bacf-114">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="4bacf-115">Une fois que vous avez exécuté ces commandes, vous devez redémarrer votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4bacf-115">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="4bacf-116">Définir une distribution basée sur WSL 2 en utilisant la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="4bacf-116">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="4bacf-117">Dans PowerShell, exécutez :</span><span class="sxs-lookup"><span data-stu-id="4bacf-117">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="4bacf-118">et veillez à remplacer `<Distro>` par le vrai nom de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="4bacf-118">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="4bacf-119">(Vous pouvez le trouver avec la commande : `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="4bacf-119">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="4bacf-120">Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».</span><span class="sxs-lookup"><span data-stu-id="4bacf-120">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="4bacf-121">Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="4bacf-121">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="4bacf-122">Ainsi, toutes les nouvelles distributions que vous installerez seront initialisées en tant que distributions WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4bacf-122">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="4bacf-123">Pour terminer, vérifiez quelles versions de WSL utilisent vos distributions.</span><span class="sxs-lookup"><span data-stu-id="4bacf-123">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="4bacf-124">Pour vérifier quelles versions de WSL utilise chaque distribution, utilisez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="4bacf-124">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="4bacf-125">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="4bacf-125">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="4bacf-126">La distribution que vous avez choisie ci-dessus doit maintenant afficher un « 2 » dans la colonne « version ».</span><span class="sxs-lookup"><span data-stu-id="4bacf-126">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="4bacf-127">Maintenant que vous avez terminé, n’hésitez pas à commencer à utiliser votre distribution WSL 2 !</span><span class="sxs-lookup"><span data-stu-id="4bacf-127">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="4bacf-128">Résolution des problèmes :</span><span class="sxs-lookup"><span data-stu-id="4bacf-128">Troubleshooting:</span></span> 

<span data-ttu-id="4bacf-129">Vous trouverez ci-dessous des erreurs associées et des suggestions de correction lors de l’installation de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="4bacf-129">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="4bacf-130">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir d’autres erreurs WSL générales et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="4bacf-130">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="4bacf-131">**Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="4bacf-131">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="4bacf-132">Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4bacf-132">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="4bacf-133">Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.</span><span class="sxs-lookup"><span data-stu-id="4bacf-133">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="4bacf-134">**Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="4bacf-134">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="4bacf-135">Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez Windows version de build 18917 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4bacf-135">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="4bacf-136">Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="4bacf-136">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="4bacf-137">Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="4bacf-137">You can find the full WSL install instructions [here](./install-win10.md).</span></span>