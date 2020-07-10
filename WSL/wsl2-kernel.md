---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: wsl, windows, noyau linux, sous-système windows pour linux, noyau
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: bef722f5653380d9f6d104f1a7c116a7599658c9
ms.sourcegitcommit: ba52d673c123fe8ae61e872a33e218cfc30a1f82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033044"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="b78d4-104">Mise à jour du noyau Linux WSL 2</span><span class="sxs-lookup"><span data-stu-id="b78d4-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="b78d4-105">Pour mettre à jour manuellement le noyau Linux dans WSL 2, suivez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="b78d4-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="b78d4-106">Si le programme d’installation ne trouve pas WSL 1, cliquez avec le bouton droit sur le programme d’installation de la mise à jour du noyau Linux et réexécutez-le.</span><span class="sxs-lookup"><span data-stu-id="b78d4-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="b78d4-107">Télécharger le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="b78d4-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="b78d4-108">[Téléchargez le dernier package de mise à jour du noyau Linux WSL2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour les machines x64.</span><span class="sxs-lookup"><span data-stu-id="b78d4-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="b78d4-109">Si vous utilisez une machine ARM64, téléchargez le [package ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) à la place.</span><span class="sxs-lookup"><span data-stu-id="b78d4-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="b78d4-110">Installer le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="b78d4-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="b78d4-111">Pour installer le package de mise à jour du noyau Linux :</span><span class="sxs-lookup"><span data-stu-id="b78d4-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="b78d4-112">Exécutez le package de mise à jour téléchargé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="b78d4-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="b78d4-113">Des autorisations élevées vous sont demandées, sélectionnez « Oui » pour approuver cette installation.</span><span class="sxs-lookup"><span data-stu-id="b78d4-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="b78d4-114">Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2 !</span><span class="sxs-lookup"><span data-stu-id="b78d4-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="b78d4-115">Plans à venir pour la mise à jour du noyau Linux WSL2</span><span class="sxs-lookup"><span data-stu-id="b78d4-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="b78d4-116">Pour plus d’informations, consultez l’article sur les [changements apportés à la mise à jour du noyau Linux WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible sur le [blog de la ligne de commande Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="b78d4-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="b78d4-117">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="b78d4-117">Troubleshooting</span></span>

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a><span data-ttu-id="b78d4-118">Cette mise à jour s’applique seulement aux machines avec le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="b78d4-118">This update only applies to machines with the Windows Subsystem for Linux</span></span>
<span data-ttu-id="b78d4-119">Pour installer le noyau MSI, WSL est nécessaire et doit être activé en premier.</span><span class="sxs-lookup"><span data-stu-id="b78d4-119">To install MSI kernel, WSL is required and should be enabled first.</span></span> <span data-ttu-id="b78d4-120">En cas d’échec, le message suivant s’affiche : `This update only applies to machines with the Windows Subsytem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="b78d4-120">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsytem for Linux`.</span></span> 

<span data-ttu-id="b78d4-121">Ce message apparaît pour trois raisons possibles :</span><span class="sxs-lookup"><span data-stu-id="b78d4-121">There are three possible reason you see this message:</span></span>

1. <span data-ttu-id="b78d4-122">Vous êtes toujours dans une ancienne version de Windows qui ne prend pas en charge WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b78d4-122">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="b78d4-123">Vérifiez les [exigences de WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) et effectuez une mise à niveau pour utiliser WSL 2.</span><span class="sxs-lookup"><span data-stu-id="b78d4-123">Please check the [WSL 2 requirements](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) and upgrade to use WSL 2.</span></span> 
2. <span data-ttu-id="b78d4-124">`Windows Subsystem for Linux` n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="b78d4-124">`Windows Subsystem for Linux` is not enabled.</span></span> <span data-ttu-id="b78d4-125">Suivez le [Guide d’installation du sous-système Windows pour Linux](https://docs.microsoft.com/windows/wsl/install-win10).</span><span class="sxs-lookup"><span data-stu-id="b78d4-125">Please follow the [Windows Subsystem for Linux Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
3. <span data-ttu-id="b78d4-126">Une fois que vous avez activé `Windows Subsystem for Linux`, un redémarrage est nécessaire pour sa prise en compte : redémarrez votre machine, puis réessayez.</span><span class="sxs-lookup"><span data-stu-id="b78d4-126">After you enabled `Windows Subsystem for Linux`, a reboot is required to take into effect, please reboot your machine and try again.</span></span>

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

<span data-ttu-id="b78d4-127">Chaque fois que le noyau est manquant dans %SystemRoot%\system32\lxss\tools\,, vous pouvez rencontrer l’erreur ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="b78d4-127">Each time kernel is missing in %SystemRoot%\system32\lxss\tools\, you may run into the above error.</span></span>

<span data-ttu-id="b78d4-128">Voici quelques moyens possibles de la résoudre :</span><span class="sxs-lookup"><span data-stu-id="b78d4-128">Here are some possible ways to resolve it:</span></span>

1. <span data-ttu-id="b78d4-129">Installez le noyau Linux manuellement en suivant les instructions fournies dans : https://aka.ms/wsl2kernel</span><span class="sxs-lookup"><span data-stu-id="b78d4-129">Please install the Linux kernel manually by following the instructions at: https://aka.ms/wsl2kernel</span></span>
2. <span data-ttu-id="b78d4-130">Désinstallez le MSI dans « Ajout/suppression de programmes », puis réinstallez-le.</span><span class="sxs-lookup"><span data-stu-id="b78d4-130">Uninstall the MSI from 'Add or Remove Programs', and install it again</span></span>
