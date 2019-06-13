---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, installer
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038079"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="f5511-104">Instructions d’installation pour WSL 2</span><span class="sxs-lookup"><span data-stu-id="f5511-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="f5511-105">Pour installer et commencer à utiliser WSL 2 procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f5511-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="f5511-106">Activer le composant facultatif « Plateforme de Machine virtuelle »</span><span class="sxs-lookup"><span data-stu-id="f5511-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="f5511-107">Définir un distributeur pour être sauvegardé par 2 WSL à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="f5511-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="f5511-108">Vérifiez que les versions de WSL vos distributions sont à l’aide de</span><span class="sxs-lookup"><span data-stu-id="f5511-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="f5511-109">Activer le composant facultatif « Plateforme de Machine virtuelle »</span><span class="sxs-lookup"><span data-stu-id="f5511-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="f5511-110">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="f5511-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="f5511-111">Une fois ces modifications sont activées, vous devrez redémarrer votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f5511-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="f5511-112">Définir un distributeur pour être sauvegardé par 2 WSL à l’aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="f5511-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="f5511-113">Dans l’exécution de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="f5511-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="f5511-114">et veillez à remplacer `<Distro>` par le nom réel de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="f5511-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="f5511-115">(Vous pouvez trouver ces éléments avec la commande : `wsl -l`).</span><span class="sxs-lookup"><span data-stu-id="f5511-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="f5511-116">Vous pouvez modifier à tout moment à 1 WSL à en exécutant la même commande que ci-dessus, mais en remplaçant ' 2' avec un ' 1'.</span><span class="sxs-lookup"><span data-stu-id="f5511-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="f5511-117">En outre, si vous souhaitez rendre WSL 2 votre architecture par défaut vous pouvez le faire avec cette commande :</span><span class="sxs-lookup"><span data-stu-id="f5511-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="f5511-118">Vous serez ainsi une nouvelle distribution que vous installez initialisé dans une distribution WSL 2.</span><span class="sxs-lookup"><span data-stu-id="f5511-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="f5511-119">Terminer avec la vérification de ce que les versions de WSL votre distributeur sont à l’aide de</span><span class="sxs-lookup"><span data-stu-id="f5511-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="f5511-120">Pour vérifier quelles versions de chaque distributeur est à l’aide de WSL utilisent la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="f5511-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="f5511-121">`wsl --list --verbose` ou `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="f5511-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="f5511-122">La distribution que vous avez choisi ci-dessus doit maintenant s’afficher un « 2 » dans la colonne « version ».</span><span class="sxs-lookup"><span data-stu-id="f5511-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="f5511-123">Maintenant que vous avez terminé n’hésitez pas à démarrer à l’aide de votre distribution WSL 2 !</span><span class="sxs-lookup"><span data-stu-id="f5511-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 