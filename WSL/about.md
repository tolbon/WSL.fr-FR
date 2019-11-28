---
title: En savoir plus sur le sous-système Windows pour Linux
description: Apprenez-en plus sur le fonctionnement du sous-système Windows pour Linux.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, GNU, Linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: fbb1ce5cf5d5c83e25d0a6a0cece7b70537a44a1
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200192"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="c5732-104">Documentation sur le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="c5732-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="c5732-105">Le sous-système Windows pour Linux permet aux développeurs d’exécuter un environnement GNU/Linux (et notamment la plupart des utilitaires, applications et outils en ligne de commande) directement sur Windows, sans modification et tout en évitant la surcharge d’une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="c5732-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="c5732-106">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="c5732-106">You can:</span></span>

1. <span data-ttu-id="c5732-107">Choisir vos distributions GNU/Linux préférées à partir du [Microsoft Store](https://aka.ms/wslstore)</span><span class="sxs-lookup"><span data-stu-id="c5732-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="c5732-108">Exécuter des logiciels en ligne de commande courants gratuits tels que `grep`, `sed` et `awk` ou d’autres fichiers binaires ELF-64</span><span class="sxs-lookup"><span data-stu-id="c5732-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="c5732-109">Exécuter des scripts de shell Bash et des applications en ligne de commande GNU/Linux, notamment :</span><span class="sxs-lookup"><span data-stu-id="c5732-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="c5732-110">Outils : vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="c5732-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="c5732-111">Langages : Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span><span class="sxs-lookup"><span data-stu-id="c5732-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="c5732-112">Services : SSHD, MySQL, Apache, lighttpd</span><span class="sxs-lookup"><span data-stu-id="c5732-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="c5732-113">Installer des logiciels supplémentaires en utilisant votre propre gestionnaire de package de distribution GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="c5732-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="c5732-114">Appeler des applications Windows à l’aide d’un shell de ligne de commande de type UNIX</span><span class="sxs-lookup"><span data-stu-id="c5732-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="c5732-115">Appeler des applications GNU/Linux sur Windows</span><span class="sxs-lookup"><span data-stu-id="c5732-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="c5732-116">Prise en main</span><span class="sxs-lookup"><span data-stu-id="c5732-116">Getting Started</span></span>

* [<span data-ttu-id="c5732-117">Installer Linux sur Windows 10</span><span class="sxs-lookup"><span data-stu-id="c5732-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="c5732-118">Consulter les informations de référence sur les commandes</span><span class="sxs-lookup"><span data-stu-id="c5732-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="c5732-119">Consulter le forum aux questions</span><span class="sxs-lookup"><span data-stu-id="c5732-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="c5732-120">Blogs de l’équipe</span><span class="sxs-lookup"><span data-stu-id="c5732-120">Team Blogs</span></span>
*  [<span data-ttu-id="c5732-121">Billet de présentation offrant un ensemble de vidéos et de blogs</span><span class="sxs-lookup"><span data-stu-id="c5732-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="c5732-122">[Blog sur les lignes de commande](https://blogs.msdn.microsoft.com/commandline/) (actif)</span><span class="sxs-lookup"><span data-stu-id="c5732-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="c5732-123">[Blog sur le sous-système Windows pour Linux](https://blogs.msdn.microsoft.com/wsl/) (historique)</span><span class="sxs-lookup"><span data-stu-id="c5732-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="c5732-124">Billets et articles</span><span class="sxs-lookup"><span data-stu-id="c5732-124">Posts & Articles</span></span>
* [<span data-ttu-id="c5732-125">Run Bash on Ubuntu on Windows</span><span class="sxs-lookup"><span data-stu-id="c5732-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="c5732-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span><span class="sxs-lookup"><span data-stu-id="c5732-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="c5732-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span><span class="sxs-lookup"><span data-stu-id="c5732-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="c5732-128">Commentaires</span><span class="sxs-lookup"><span data-stu-id="c5732-128">Provide Feedback</span></span>
* [<span data-ttu-id="c5732-129">Outil de suivi des problèmes GitHub</span><span class="sxs-lookup"><span data-stu-id="c5732-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

