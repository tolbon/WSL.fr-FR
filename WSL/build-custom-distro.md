---
title: Créer une distribution Linux personnalisée pour WSL
description: Découvrez comment créer une distribution Linux personnalisée pour le sous-système de Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows, distributeur, personnalisé
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 4072df5fa81f65fd9a3ff875ab887c03b234bce1
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040777"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="abb56-104">Création d’une distribution Linux personnalisée pour WSL</span><span class="sxs-lookup"><span data-stu-id="abb56-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="abb56-105">Utilisez notre exemple WSL open source pour créer des packages de distribution WSL pour le Microsoft Store et/ou pour créer des packages de distribution Linux personnalisés pour le chargement indépendant.</span><span class="sxs-lookup"><span data-stu-id="abb56-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="abb56-106">Vous pouvez trouver la [référentiel de lanceur distributeur](https://github.com/Microsoft/WSL-DistroLauncher) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="abb56-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="abb56-107">Ce projet permet de :</span><span class="sxs-lookup"><span data-stu-id="abb56-107">This project enables:</span></span>
* <span data-ttu-id="abb56-108">Les chargés de maintenance de distribution Linux pour empaqueter et soumettre une distribution Linux comme un appx qui s’exécute sur WSL</span><span class="sxs-lookup"><span data-stu-id="abb56-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="abb56-109">Aux développeurs de créer des distributions de Linux qui peuvent être chargées indépendamment sur son ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="abb56-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="abb56-110">Arrière-plan</span><span class="sxs-lookup"><span data-stu-id="abb56-110">Background</span></span>
<span data-ttu-id="abb56-111">Nous distribuons des distributions Linux pour WSL en tant qu’applications UWP via le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="abb56-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="abb56-112">Vous pouvez installer les applications qui pourra ensuite s’exécuter sur WSL - le sous-système qui se trouve dans le noyau Windows.</span><span class="sxs-lookup"><span data-stu-id="abb56-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="abb56-113">Ce mécanisme de livraison présente de nombreux avantages comme indiqué dans un [antérieures billet de blog](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span><span class="sxs-lookup"><span data-stu-id="abb56-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="abb56-114">Chargement de version test un Package de distribution Linux personnalisée</span><span class="sxs-lookup"><span data-stu-id="abb56-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="abb56-115">Vous pouvez créer un package de distribution Linux personnalisé en tant qu’application à charger une version test sur votre ordinateur personnel.</span><span class="sxs-lookup"><span data-stu-id="abb56-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="abb56-116">Veuillez noter que votre package personnalisé ne serait pas distribué via le Microsoft Store, sauf si vous envoyez en tant que responsable de maintenance de la distribution.</span><span class="sxs-lookup"><span data-stu-id="abb56-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="abb56-117">Pour configurer votre ordinateur pour supprimer des applications, vous devez l’activer sur les paramètres du système sous « Pour les développeurs ».</span><span class="sxs-lookup"><span data-stu-id="abb56-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="abb56-118">Veillez à avoir mode développeur, ou supprimer des applications sélectionnées</span><span class="sxs-lookup"><span data-stu-id="abb56-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="abb56-119">Pour une distribution Linux chargés de maintenance</span><span class="sxs-lookup"><span data-stu-id="abb56-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="abb56-120">Pour envoyer vers le Store, vous devrez collaborer avec nous pour recevoir l’approbation de publication.</span><span class="sxs-lookup"><span data-stu-id="abb56-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="abb56-121">Si vous êtes propriétaire d’une distribution Linux intéressé par l’ajout de votre distribution pour le Microsoft Store, contactez wslpartners@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="abb56-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="abb56-122">Prise en main</span><span class="sxs-lookup"><span data-stu-id="abb56-122">Getting Started</span></span>
<span data-ttu-id="abb56-123">Suivez les instructions la [référentiel GitHub de lanceur distributeur](https://github.com/Microsoft/WSL-DistroLauncher) pour créer un package de distribution Linux personnalisé.</span><span class="sxs-lookup"><span data-stu-id="abb56-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="abb56-124">Blogs de l’équipe</span><span class="sxs-lookup"><span data-stu-id="abb56-124">Team Blogs</span></span>
*  [<span data-ttu-id="abb56-125">Ouvrez l’approvisionnement en un exemple WSL pour chargés de maintenance de Distribution Linux et les Distributions de Linux personnalisée de chargement de version test</span><span class="sxs-lookup"><span data-stu-id="abb56-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="abb56-126">Blog de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="abb56-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="abb56-127">Commentaires</span><span class="sxs-lookup"><span data-stu-id="abb56-127">Provide Feedback</span></span>
* [<span data-ttu-id="abb56-128">Référentiel GitHub de Lanceur de distribution</span><span class="sxs-lookup"><span data-stu-id="abb56-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="abb56-129">Suivi des problèmes GitHub pour WSL</span><span class="sxs-lookup"><span data-stu-id="abb56-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="abb56-130">Portail de UserVoice de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="abb56-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
