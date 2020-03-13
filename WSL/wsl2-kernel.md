---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138188"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="35d75-104">Mise à jour du noyau Linux WSL 2</span><span class="sxs-lookup"><span data-stu-id="35d75-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="35d75-105">Pour mettre à jour manuellement le noyau Linux à l’intérieur de WSL 2, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="35d75-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="35d75-106">Télécharger le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="35d75-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="35d75-107">Cliquez sur [ce lien](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour télécharger le dernier package de mise à jour du noyau WSL2 Linux pour les machines amd64.</span><span class="sxs-lookup"><span data-stu-id="35d75-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] <span data-ttu-id="35d75-108">Si vous utilisez une machine ARM64, téléchargez [ce package à la](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) place.</span><span class="sxs-lookup"><span data-stu-id="35d75-108">if you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="35d75-109">Installer le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="35d75-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="35d75-110">Pour installer le package de mise à jour du noyau Linux :</span><span class="sxs-lookup"><span data-stu-id="35d75-110">To install the Linux kernel update package:</span></span>
    1. <span data-ttu-id="35d75-111">Exécutez le package de mise à jour téléchargé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="35d75-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="35d75-112">Vous serez invité à fournir des autorisations élevées, sélectionner « Oui » pour approuver cette installation.</span><span class="sxs-lookup"><span data-stu-id="35d75-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="35d75-113">Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2.</span><span class="sxs-lookup"><span data-stu-id="35d75-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="35d75-114">Plans futurs pour la mise à jour du noyau Linux WSL2</span><span class="sxs-lookup"><span data-stu-id="35d75-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="35d75-115">Pour plus d’informations sur ces modifications, consultez [ce](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) billet de blog sur le blog de la [ligne de commande Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="35d75-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>