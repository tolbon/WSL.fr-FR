---
title: Vue d’ensemble du sous-système Windows pour Linux
description: Découvrez le sous-système Windows pour Linux, les différentes versions et les différentes façons de les utiliser.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, GNU, Linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 90a661c408cacbef95a869ac896a40381120d52e
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270793"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a><span data-ttu-id="70380-104">Qu’est-ce que le sous-système Windows pour Linux ?</span><span class="sxs-lookup"><span data-stu-id="70380-104">What is the Windows Subsystem for Linux?</span></span>

<span data-ttu-id="70380-105">Le sous-système Windows pour Linux permet aux développeurs d’exécuter un environnement GNU/Linux (et notamment la plupart des utilitaires, applications et outils en ligne de commande) directement sur Windows, sans modification et tout en évitant la surcharge d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="70380-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>

<span data-ttu-id="70380-106">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="70380-106">You can:</span></span>

* <span data-ttu-id="70380-107">Choisir vos distributions GNU/Linux préférées à partir du [Microsoft Store](https://aka.ms/wslstore)</span><span class="sxs-lookup"><span data-stu-id="70380-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
* <span data-ttu-id="70380-108">Exécuter des outils en ligne de commande courants tels que `grep`, `sed` et `awk`, ou d’autres fichiers binaires ELF-64.</span><span class="sxs-lookup"><span data-stu-id="70380-108">Run common command-line tools such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span>
* <span data-ttu-id="70380-109">Exécuter des scripts de shell Bash et des applications en ligne de commande GNU/Linux, notamment :</span><span class="sxs-lookup"><span data-stu-id="70380-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="70380-110">Outils : vim, emacs, tmux \*Langages : [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc. \*Services : SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span><span class="sxs-lookup"><span data-stu-id="70380-110">Tools: vim, emacs, tmux \*Languages: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc. \*Services: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span></span>
* <span data-ttu-id="70380-111">Installer des logiciels supplémentaires en utilisant votre propre gestionnaire de package de distribution GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="70380-111">Install additional software using own GNU/Linux distribution package manager.</span></span>
* <span data-ttu-id="70380-112">Appeler des applications Windows à l’aide d’un shell de ligne de commande de type UNIX</span><span class="sxs-lookup"><span data-stu-id="70380-112">Invoke Windows applications using a Unix-like command-line shell.</span></span>
* <span data-ttu-id="70380-113">Appeler des applications GNU/Linux sur Windows</span><span class="sxs-lookup"><span data-stu-id="70380-113">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="what-is-wsl-2"></a><span data-ttu-id="70380-114">Qu’est-ce que WSL 2 ?</span><span class="sxs-lookup"><span data-stu-id="70380-114">What is WSL 2?</span></span>

<span data-ttu-id="70380-115">WSL 2 est une nouvelle version de l’architecture du sous-système Windows pour Linux qui sous-tend le sous-système Windows pour Linux afin d’exécuter les binaires ELF64 Linux sur Windows.</span><span class="sxs-lookup"><span data-stu-id="70380-115">WSL 2 is a new version of the Windows Subsystem for Linux architecture that powers the Windows Subsystem for Linux to run ELF64 Linux binaries on Windows.</span></span> <span data-ttu-id="70380-116">Ses principaux objectifs consistent à **augmenter les performances du système de fichiers**, ainsi qu’à ajouter la **compatibilité complète des appels système**.</span><span class="sxs-lookup"><span data-stu-id="70380-116">Its primary goals are to **increase file system performance**, as well as adding **full system call compatibility**.</span></span>

<span data-ttu-id="70380-117">Cette nouvelle architecture change la façon dont ces fichiers binaires Linux interagissent avec Windows et votre matériel informatique, mais offre toujours la même expérience utilisateur que dans WSL 1 (la version actuellement largement disponible).</span><span class="sxs-lookup"><span data-stu-id="70380-117">This new architecture changes how these Linux binaries interact with Windows and your computer's hardware, but still provides the same user experience as in WSL 1 (the current widely available version).</span></span>

<span data-ttu-id="70380-118">Les distributions Linux individuelles peuvent être exécutées avec l’architecture WSL 1 ou WSL 2.</span><span class="sxs-lookup"><span data-stu-id="70380-118">Individual Linux distributions can be run with either the WSL 1 or WSL 2 architecture.</span></span> <span data-ttu-id="70380-119">Chaque distribution peut être mise à niveau ou rétrogradée à tout moment et vous pouvez exécuter des distributions WSL 1 et WSL 2 côte à côte.</span><span class="sxs-lookup"><span data-stu-id="70380-119">Each distribution can be upgraded or downgraded at any time and you can run WSL 1 and WSL 2 distributions side by side.</span></span> <span data-ttu-id="70380-120">WSL 2 exploite une architecture entièrement nouvelle qui tire profit de l’exécution d’un véritable noyau Linux.</span><span class="sxs-lookup"><span data-stu-id="70380-120">WSL 2 uses an entirely new architecture that benefits from running a real Linux kernel.</span></span>

## <a name="next-steps"></a><span data-ttu-id="70380-121">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="70380-121">Next steps</span></span>

* [<span data-ttu-id="70380-122">Installer WSL 1 et le mettre à jour vers WSL 2</span><span class="sxs-lookup"><span data-stu-id="70380-122">Install WSL 1 and update to WSL 2</span></span>](./install-win10.md)

* [<span data-ttu-id="70380-123">Comparer WSL 2 et WSL 1</span><span class="sxs-lookup"><span data-stu-id="70380-123">Compare WSL 2 and WSL 1</span></span>](./compare-versions.md)

* [<span data-ttu-id="70380-124">Créer un compte d’utilisateur et un mot de passe pour votre nouvelle distribution Linux</span><span class="sxs-lookup"><span data-stu-id="70380-124">Create a user account and password for your new Linux distribution</span></span>](./user-support.md)

* [<span data-ttu-id="70380-125">Consulter les questions fréquentes</span><span class="sxs-lookup"><span data-stu-id="70380-125">Read Frequently Asked Questions</span></span>](./faq.md)

* [<span data-ttu-id="70380-126">Consulter les questions fréquentes sur WSL 2</span><span class="sxs-lookup"><span data-stu-id="70380-126">Read Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

* [<span data-ttu-id="70380-127">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="70380-127">Troubleshooting</span></span>](./troubleshooting.md)

* [<span data-ttu-id="70380-128">Exécuter des commandes d’interopérabilité entre Windows et Linux</span><span class="sxs-lookup"><span data-stu-id="70380-128">Run interoperability commands between Windows and Linux</span></span>](./interop.md)

* [<span data-ttu-id="70380-129">Exécuter des commandes et des configurations de lancement</span><span class="sxs-lookup"><span data-stu-id="70380-129">Run launch commands and configurations</span></span>](./wsl-config.md)

* [<span data-ttu-id="70380-130">Configurer les autorisations de fichier</span><span class="sxs-lookup"><span data-stu-id="70380-130">Set up file permissions</span></span>](./file-permissions.md)

* [<span data-ttu-id="70380-131">Configurer WSL pour les entreprises</span><span class="sxs-lookup"><span data-stu-id="70380-131">Set up WSL for Enterprise</span></span>](./enterprise.md)

* [<span data-ttu-id="70380-132">Référencer les commandes WSL</span><span class="sxs-lookup"><span data-stu-id="70380-132">Reference WSL commands</span></span>](./reference.md)

* [<span data-ttu-id="70380-133">Créer une distribution personnalisée</span><span class="sxs-lookup"><span data-stu-id="70380-133">Build a custom distributions</span></span>](./build-custom-distro.md)

* [<span data-ttu-id="70380-134">Consulter les notes de publication de WSL</span><span class="sxs-lookup"><span data-stu-id="70380-134">Read the WSL Release Notes</span></span>](./release-notes.md)
