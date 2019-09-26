---
title: Créer un distribution Linux personnalisé pour WSL
description: Découvrez comment créer une distribution Linux personnalisée pour le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows, distribution, personnalisé
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 181badd4ee2f69e904099c12b54dfbdf3a37e294
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269704"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="8a5f6-104">Création d’un distribution Linux personnalisé pour WSL</span><span class="sxs-lookup"><span data-stu-id="8a5f6-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="8a5f6-105">Utilisez notre exemple Open source WSL pour créer des packages WSL distribution pour le Microsoft Store et/ou pour créer des packages distribution Linux personnalisés pour chargement.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="8a5f6-106">Vous pouvez trouver [distribution Launcher référentiel](https://github.com/Microsoft/WSL-DistroLauncher) sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="8a5f6-107">Ce projet active les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8a5f6-107">This project enables:</span></span>
* <span data-ttu-id="8a5f6-108">Maintenance de la distribution Linux pour empaqueter et soumettre une distribution Linux sous la forme d’un fichier AppX qui s’exécute sur WSL</span><span class="sxs-lookup"><span data-stu-id="8a5f6-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="8a5f6-109">Développeurs pour créer des distributions Linux personnalisées qui peuvent être faisant sur leur ordinateur de développement</span><span class="sxs-lookup"><span data-stu-id="8a5f6-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="8a5f6-110">Présentation</span><span class="sxs-lookup"><span data-stu-id="8a5f6-110">Background</span></span>
<span data-ttu-id="8a5f6-111">Nous distribuons Linux distributions pour WSL en tant qu’applications UWP par le biais du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="8a5f6-112">Vous pouvez installer ces applications qui s’exécuteront ensuite sur WSL-le sous-système qui se trouve dans le noyau Windows.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="8a5f6-113">Ce mécanisme de remise présente de nombreux avantages, comme indiqué dans un [billet de blog précédent](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span><span class="sxs-lookup"><span data-stu-id="8a5f6-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="8a5f6-114">Chargement un package distribution Linux personnalisé</span><span class="sxs-lookup"><span data-stu-id="8a5f6-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="8a5f6-115">Vous pouvez créer un package distribution Linux personnalisé en tant qu’application pour chargement sur votre ordinateur personnel.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="8a5f6-116">Notez que votre package personnalisé n’est pas distribué via le Microsoft Store, sauf si vous soumettez en tant que chargé de maintenance de la distribution.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="8a5f6-117">Pour configurer votre ordinateur pour chargement des applications, vous devez l’activer dans les paramètres système sous « pour les développeurs ».</span><span class="sxs-lookup"><span data-stu-id="8a5f6-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="8a5f6-118">Assurez-vous que vous avez sélectionné le mode développeur ou les applications chargement</span><span class="sxs-lookup"><span data-stu-id="8a5f6-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="8a5f6-119">Pour les Maintenateurs Linux distribution</span><span class="sxs-lookup"><span data-stu-id="8a5f6-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="8a5f6-120">Pour envoyer un message au magasin, vous devez nous contacter pour recevoir l’approbation de la publication.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="8a5f6-121">Si vous êtes un propriétaire de distribution Linux désireux d’ajouter votre distribution à la Microsoft Store, contactez wslpartners@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="8a5f6-122">Prise en main</span><span class="sxs-lookup"><span data-stu-id="8a5f6-122">Getting Started</span></span>
<span data-ttu-id="8a5f6-123">Suivez les instructions du [distribution Launcher GitHub référentiel](https://github.com/Microsoft/WSL-DistroLauncher) pour créer un package distribution Linux personnalisé.</span><span class="sxs-lookup"><span data-stu-id="8a5f6-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="8a5f6-124">Blogs de l’équipe</span><span class="sxs-lookup"><span data-stu-id="8a5f6-124">Team Blogs</span></span>
*  [<span data-ttu-id="8a5f6-125">Open source-exemple WSL pour les préserveurs de distribution Linux et les distributions Linux personnalisées chargement</span><span class="sxs-lookup"><span data-stu-id="8a5f6-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="8a5f6-126">Blog de ligne de commande</span><span class="sxs-lookup"><span data-stu-id="8a5f6-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="8a5f6-127">Commentaires</span><span class="sxs-lookup"><span data-stu-id="8a5f6-127">Provide Feedback</span></span>
* [<span data-ttu-id="8a5f6-128">Distribution Launcher GitHub référentiel</span><span class="sxs-lookup"><span data-stu-id="8a5f6-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="8a5f6-129">GitHub Issue Tracker pour WSL</span><span class="sxs-lookup"><span data-stu-id="8a5f6-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="8a5f6-130">Portail UserVoice de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="8a5f6-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
