---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d4ce22fda7baea77c0a8d3d7101d0ab09b78e8f8
ms.sourcegitcommit: d110e2bbcd92438781453137ba0ab747cddb28e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2019
ms.locfileid: "72998252"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="549e8-104">Instructions d’installation pour WSL 2</span><span class="sxs-lookup"><span data-stu-id="549e8-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="549e8-105">Pour installer et commencer à utiliser WSL 2, effectuez les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="549e8-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="549e8-106">WSL 2 est disponible uniquement dans Windows 10 versions 18917 ou ultérieures</span><span class="sxs-lookup"><span data-stu-id="549e8-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="549e8-107">Vérifiez que vous avez installé WSL (vous trouverez des instructions pour le faire [ici](./install-win10.md)) et que vous exécutez Windows 10 **Build 18917** ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="549e8-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="549e8-108">Pour vous assurer que vous utilisez la version 18917 ou une version ultérieure, rejoignez [le programme Windows Insider](https://insider.windows.com/en-us/) et sélectionnez l’anneau « Fast ».</span><span class="sxs-lookup"><span data-stu-id="549e8-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="549e8-109">Vous pouvez vérifier votre version de Windows en ouvrant l’invite de commandes et en exécutant la commande `ver`.</span><span class="sxs-lookup"><span data-stu-id="549e8-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="549e8-110">Activer le composant facultatif « Plateforme de machine virtuelle »</span><span class="sxs-lookup"><span data-stu-id="549e8-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="549e8-111">Définir une distribution basée sur WSL 2 en utilisant la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="549e8-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="549e8-112">Vérifier les versions de WSL que vos distributions utilisent</span><span class="sxs-lookup"><span data-stu-id="549e8-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="549e8-113">Activez le composant facultatif « plateforme de machine virtuelle » et assurez-vous que WSL est activé</span><span class="sxs-lookup"><span data-stu-id="549e8-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="549e8-114">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="549e8-114">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="549e8-115">Cela permet de s’assurer que les composants facultatifs plateforme de machine virtuelle et sous-système Windows pour Linux sont installés.</span><span class="sxs-lookup"><span data-stu-id="549e8-115">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="549e8-116">Une fois que vous avez exécuté ces commandes, vous devez redémarrer votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="549e8-116">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="549e8-117">Définir une distribution basée sur WSL 2 en utilisant la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="549e8-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="549e8-118">Dans PowerShell, exécutez :</span><span class="sxs-lookup"><span data-stu-id="549e8-118">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="549e8-119">et veillez à remplacer `<Distro>` par le vrai nom de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="549e8-119">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="549e8-120">(Vous pouvez le trouver avec la commande : `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="549e8-120">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="549e8-121">Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».</span><span class="sxs-lookup"><span data-stu-id="549e8-121">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="549e8-122">Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="549e8-122">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="549e8-123">Ainsi, toutes les nouvelles distributions que vous installerez seront initialisées en tant que distributions WSL 2.</span><span class="sxs-lookup"><span data-stu-id="549e8-123">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="549e8-124">Pour terminer, vérifiez quelles versions de WSL utilisent vos distributions.</span><span class="sxs-lookup"><span data-stu-id="549e8-124">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="549e8-125">Pour vérifier les versions de WSL que chaque distribution utilise, utilisez la commande suivante (disponible uniquement dans Windows Build 18917 ou version ultérieure) :</span><span class="sxs-lookup"><span data-stu-id="549e8-125">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="549e8-126">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="549e8-126">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="549e8-127">La distribution que vous avez choisie ci-dessus doit maintenant afficher un « 2 » dans la colonne « version ».</span><span class="sxs-lookup"><span data-stu-id="549e8-127">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="549e8-128">Maintenant que vous avez terminé, n’hésitez pas à commencer à utiliser votre distribution WSL 2 !</span><span class="sxs-lookup"><span data-stu-id="549e8-128">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="549e8-129">Dépannage :</span><span class="sxs-lookup"><span data-stu-id="549e8-129">Troubleshooting:</span></span> 

<span data-ttu-id="549e8-130">Vous trouverez ci-dessous des erreurs associées et des suggestions de correction lors de l’installation de WSL 2.</span><span class="sxs-lookup"><span data-stu-id="549e8-130">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="549e8-131">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir d’autres erreurs WSL générales et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="549e8-131">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="549e8-132">**Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="549e8-132">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="549e8-133">Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="549e8-133">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="549e8-134">Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.</span><span class="sxs-lookup"><span data-stu-id="549e8-134">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="549e8-135">**Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="549e8-135">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="549e8-136">Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez Windows version de build 18917 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="549e8-136">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="549e8-137">Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="549e8-137">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="549e8-138">Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="549e8-138">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="549e8-139">**L’opération demandée n’a pas pu être effectuée en raison d’une limitation du système de disque virtuel. Les fichiers de disque dur virtuel doivent être décompressés et déchiffrés et ne doivent pas être éparpillés.**</span><span class="sxs-lookup"><span data-stu-id="549e8-139">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="549e8-140">Vérifiez [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) où ce problème est suivi pour obtenir des informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="549e8-140">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>