---
title: En savoir plus sur le sous-système Windows pour Linux
description: En savoir plus sur le fonctionnement du sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, GNU, Linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: edff78b1447aa382253417d27df52fe497c58b08
ms.sourcegitcommit: e17038c166b69f73e593ae3ac351c9d66e2ba64b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2019
ms.locfileid: "67694627"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="b6357-104">Documentation sur le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="b6357-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="b6357-105">Le sous-système Windows pour Linux permet aux développeurs d’exécuter un environnement GNU/Linux, y compris la plupart des outils en ligne de commande, des utilitaires et des applications, directement sur Windows, non modifiés, sans la surcharge d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="b6357-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="b6357-106">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="b6357-106">You can:</span></span>

1. <span data-ttu-id="b6357-107">Choisissez vos distributions GNU/Linux favorites [à partir de la Microsoft Store](https://aka.ms/wslstore).</span><span class="sxs-lookup"><span data-stu-id="b6357-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="b6357-108">Exécutez des logiciels gratuits de ligne de commande courants `grep`tels `sed`que `awk`,, ou d’autres fichiers binaires ELF-64.</span><span class="sxs-lookup"><span data-stu-id="b6357-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="b6357-109">Exécutez des scripts d’interpréteur de commandes bash et des applications en ligne de commande GNU/Linux, notamment:</span><span class="sxs-lookup"><span data-stu-id="b6357-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="b6357-110">Outils: vim, Emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="b6357-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="b6357-111">Traduction: JavaScript/node. js, Ruby, Python, C/C++, C# & F#, rouille, Go, etc.</span><span class="sxs-lookup"><span data-stu-id="b6357-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="b6357-112">Services: sshd, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="b6357-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="b6357-113">Installer des logiciels supplémentaires en utilisant le gestionnaire de package de distribution GNU/Linux.</span><span class="sxs-lookup"><span data-stu-id="b6357-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="b6357-114">Appeler des applications Windows à l’aide d’un interpréteur de ligne de commande de type UNIX.</span><span class="sxs-lookup"><span data-stu-id="b6357-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="b6357-115">Appelez des applications GNU/Linux sur Windows.</span><span class="sxs-lookup"><span data-stu-id="b6357-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="b6357-116">Prise en main</span><span class="sxs-lookup"><span data-stu-id="b6357-116">Getting Started</span></span>

* [<span data-ttu-id="b6357-117">Installer Linux sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6357-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="b6357-118">Consulter la référence de la commande</span><span class="sxs-lookup"><span data-stu-id="b6357-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="b6357-119">Lire les questions fréquentes</span><span class="sxs-lookup"><span data-stu-id="b6357-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="b6357-120">Blogs de l’équipe</span><span class="sxs-lookup"><span data-stu-id="b6357-120">Team Blogs</span></span>
*  [<span data-ttu-id="b6357-121">Présentation de la publication avec une collection de vidéos et de blogs</span><span class="sxs-lookup"><span data-stu-id="b6357-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="b6357-122">[Blog de ligne de commande](https://blogs.msdn.microsoft.com/commandline/) Proactive</span><span class="sxs-lookup"><span data-stu-id="b6357-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="b6357-123">[Blog du sous-système Windows pour Linux](https://blogs.msdn.microsoft.com/wsl/) Correspondante</span><span class="sxs-lookup"><span data-stu-id="b6357-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="b6357-124">Publie des articles &</span><span class="sxs-lookup"><span data-stu-id="b6357-124">Posts & Articles</span></span>
* [<span data-ttu-id="b6357-125">Exécutez bash sur Ubuntu sur Windows</span><span class="sxs-lookup"><span data-stu-id="b6357-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="b6357-126">Les développeurs peuvent exécuter des fichiers binaires bash et de la fonction de démarrage en Ubuntu Linux sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="b6357-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="b6357-127">Ubuntu sur Windows: Ubuntu Userspace pour les développeurs Windows</span><span class="sxs-lookup"><span data-stu-id="b6357-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="b6357-128">Commentaires</span><span class="sxs-lookup"><span data-stu-id="b6357-128">Provide Feedback</span></span>
* [<span data-ttu-id="b6357-129">Suivi des problèmes GitHub</span><span class="sxs-lookup"><span data-stu-id="b6357-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="b6357-130">Portail UserVoice de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="b6357-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
