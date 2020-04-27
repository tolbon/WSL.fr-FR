---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: a1a2f23fb05c426f80878e12e82026a96c71354e
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "79447745"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="4e870-104">Mise à jour du noyau Linux WSL 2</span><span class="sxs-lookup"><span data-stu-id="4e870-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="4e870-105">Pour mettre à jour manuellement le noyau Linux dans WSL 2, suivez ces étapes.</span><span class="sxs-lookup"><span data-stu-id="4e870-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="4e870-106">Télécharger le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="4e870-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="4e870-107">Cliquez sur [ce lien](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour télécharger le dernier package de mise à jour du noyau Linux WSL2 pour les machines x64.</span><span class="sxs-lookup"><span data-stu-id="4e870-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for x64 machines.</span></span>

> [!NOTE] 
> <span data-ttu-id="4e870-108">Si vous utilisez un ordinateur ARM64, téléchargez [ce package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) à la place.</span><span class="sxs-lookup"><span data-stu-id="4e870-108">If you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="4e870-109">Installer le package de mise à jour du noyau Linux</span><span class="sxs-lookup"><span data-stu-id="4e870-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="4e870-110">Pour installer le package de mise à jour du noyau Linux :</span><span class="sxs-lookup"><span data-stu-id="4e870-110">To install the Linux kernel update package:</span></span>

    1. <span data-ttu-id="4e870-111">Exécutez le package de mise à jour téléchargé à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="4e870-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="4e870-112">Des autorisations élevées vous sont demandées, sélectionnez « Oui » pour approuver cette installation.</span><span class="sxs-lookup"><span data-stu-id="4e870-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="4e870-113">Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2 !</span><span class="sxs-lookup"><span data-stu-id="4e870-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="4e870-114">Plans à venir pour la mise à jour du noyau Linux WSL2</span><span class="sxs-lookup"><span data-stu-id="4e870-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="4e870-115">Pour plus d’informations sur ces changements, consultez [ce billet de blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) sur le [blog de la ligne de commande Windows](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="4e870-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
