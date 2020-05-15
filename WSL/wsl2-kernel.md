---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: wsl, windows, noyau linux, sous-système windows pour linux, noyau
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 89e5755699938b7797aa65a5f3131f93e3e31796
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343831"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="4f4ae-104">Mise à jour du noyau Linux WSL 2</span><span class="sxs-lookup"><span data-stu-id="4f4ae-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="4f4ae-105">Pour mettre à jour manuellement le noyau Linux dans WSL 2, suivez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="4f4ae-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="4f4ae-106">Si le programme d’installation ne trouve pas WSL 1, cliquez avec le bouton droit sur le programme d’installation de la mise à jour du noyau Linux, puis réexécutez-le.</span><span class="sxs-lookup"><span data-stu-id="4f4ae-106">If the installer cant find WSL 1 right click the Linux kernel update installer, then press uninstall then rerun the installer</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="4f4ae-107">Télécharger le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="4f4ae-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="4f4ae-108">[Téléchargez le dernier package de mise à jour du noyau Linux WSL2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour les machines x64.</span><span class="sxs-lookup"><span data-stu-id="4f4ae-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="4f4ae-109">Si vous utilisez une machine ARM64, téléchargez le [package ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) à la place.</span><span class="sxs-lookup"><span data-stu-id="4f4ae-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="4f4ae-110">Installer le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="4f4ae-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="4f4ae-111">Pour installer le package de mise à jour du noyau Linux :</span><span class="sxs-lookup"><span data-stu-id="4f4ae-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="4f4ae-112">Exécutez le package de mise à jour téléchargé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="4f4ae-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="4f4ae-113">Des autorisations élevées vous sont demandées, sélectionnez « Oui » pour approuver cette installation.</span><span class="sxs-lookup"><span data-stu-id="4f4ae-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="4f4ae-114">Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2 !</span><span class="sxs-lookup"><span data-stu-id="4f4ae-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="4f4ae-115">Plans à venir pour la mise à jour du noyau Linux WSL2</span><span class="sxs-lookup"><span data-stu-id="4f4ae-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="4f4ae-116">Pour plus d’informations, consultez l’article sur les [changements apportés à la mise à jour du noyau Linux WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible sur le [blog de la ligne de commande Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="4f4ae-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
