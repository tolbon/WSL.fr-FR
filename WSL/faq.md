---
title: Forum Aux Questions (FAQ)
description: Forum aux questions sur le sous-système Windows pour Linux.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, FAQ
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 8e3ebb44c139b5e7b8c25e8e813766b0107426dc
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948633"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="1d7ea-104">Forum aux questions sur le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="1d7ea-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="1d7ea-105">Qu’est-ce que le sous-système Windows pour Linux (WSL) ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-105">What is Windows Subsystem for Linux (WSL)?</span></span>

<span data-ttu-id="1d7ea-106">Le sous-système Windows pour Linux (WSL) est une nouvelle fonctionnalité Windows 10 qui vous permet d’exécuter des outils en ligne de commande Linux natifs directement sur Windows, parallèlement à vos applications Windows de bureau classiques et du Store modernes.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="1d7ea-107">Pour plus d’informations, consultez la [page À propos de](./about.md).</span><span class="sxs-lookup"><span data-stu-id="1d7ea-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="1d7ea-108">À qui WSL s’adresse-t-il ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-108">Who is WSL for?</span></span>

<span data-ttu-id="1d7ea-109">Il s’agit principalement d’un outil destiné aux développeurs, en particulier les développeurs web et ceux qui travaillent sur des projets open source ou les utilisent.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="1d7ea-110">Il permet à ceux qui souhaitent/doivent utiliser Bash, les outils Linux courants (`sed`, `awk`, etc.) et de nombreux premiers outils Linux (Ruby, Python, etc.) d’utiliser leur chaîne d’outils sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="1d7ea-111">Qu’est-ce que WSL me permet de faire ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-111">What can I do with WSL?</span></span>

<span data-ttu-id="1d7ea-112">WSL fournit une application appelée Bash.exe qui, lorsqu’elle est démarrée, ouvre une console Windows exécutant l’interpréteur de commandes Bash.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="1d7ea-113">Bash vous permet d’exécuter des applications et des outils Linux en ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="1d7ea-114">Par exemple, tapez `lsb_release -a` et appuyez sur Entrée ; vous verrez les détails de la distribution Linux en cours d’exécution :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![Capture d’écran des détails de distribution](media/distro.png)

<span data-ttu-id="1d7ea-116">Vous pouvez également accéder au système de fichiers de votre ordinateur local à partir de l’interpréteur de commandes Bash Linux ; vous trouverez vos lecteurs locaux montés sous le dossier `/mnt`.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="1d7ea-117">Par exemple, votre lecteur `C:` est monté sous `/mnt/c` :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![Capture d’écran du lecteur C monté](media/ls.png)

## <a name="could-you-describe-a-typical-development-workflow-that-incorporates-wsl"></a><span data-ttu-id="1d7ea-119">Pouvez-vous décrire un workflow de développement typique qui incorpore WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-119">Could you describe a typical development workflow that incorporates WSL?</span></span>

<span data-ttu-id="1d7ea-120">WSL cible une audience de développeur avec l’intention d’être utilisé dans le cadre d’une boucle de développement interne.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-120">WSL targets a developer audience with the intent to be used as part of an inner development loop.</span></span> <span data-ttu-id="1d7ea-121">Supposons que Sam crée un pipeline CI/CD (intégration continue et livraison continue) et qu’il souhaite le tester d’abord sur un ordinateur local (portable) avant de le déployer dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-121">Let's say that Sam is creating a CI/CD pipeline (Continuous Integration & Continuous Delivery) and wants to test it first on a local machine (laptop) before deploying it to the cloud.</span></span> <span data-ttu-id="1d7ea-122">Sam peut activer WSL (et WSL 2 pour améliorer la vitesse et les performances), puis utiliser une vraie instance Linux Ubuntu en local (sur l’ordinateur portable) avec les commandes et les outils Bash qu’ils préfèrent.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-122">Sam can enable WSL (& WSL 2 to improve speed and performance), and then use a genuine Linux Ubuntu instance locally (on the laptop) with whatever Bash commands and tools they prefer.</span></span> <span data-ttu-id="1d7ea-123">Une fois le pipeline de développement vérifié localement, Sam peut alors envoyer (push) ce pipeline CI/CD vers le cloud (par ex. Azure) en le plaçant dans un conteneur Docker et en envoyant le conteneur à une instance cloud où il s’exécutera sur une machine virtuelle Ubuntu prête pour la production.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-123">Once the development pipeline is verified locally, Sam can then push that CI/CD pipeline up to the cloud (ie Azure) by making it into a Docker container and pushing the container to a cloud instance where it runs on a production-ready Ubuntu VM.</span></span>

## <a name="what-is-bash"></a><span data-ttu-id="1d7ea-124">Qu’est-ce que Bash ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-124">What is Bash?</span></span>

<span data-ttu-id="1d7ea-125">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) est un interpréteur de commandes texte et un langage de commandes connues.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-125">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="1d7ea-126">Il s’agit de l’interpréteur de commandes par défaut inclus dans Ubuntu et d’autres distributions Linux ainsi que dans macOS.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-126">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="1d7ea-127">Les utilisateurs tapent des commandes dans un interpréteur de commandes pour exécuter des scripts et/ou des commandes et des outils pour accomplir de nombreuses tâches.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-127">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="1d7ea-128">Comment cela fonctionne ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-128">How does this work?</span></span>

<span data-ttu-id="1d7ea-129">Consultez notre [blog](https://blogs.msdn.microsoft.com/wsl/) pour en savoir plus sur la technologie sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-129">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="1d7ea-130">Pourquoi utiliser WSL plutôt que Linux dans une machine virtuelle ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-130">Why would I use WSL rather than Linux in a VM?</span></span>

<span data-ttu-id="1d7ea-131">WSL demande moins de ressources (processeur, mémoire et stockage) qu’une machine virtuelle complète.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-131">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="1d7ea-132">WSL vous permet également d’exécuter des applications et des outils en ligne de commande Linux avec vos applications Windows en ligne de commande, de bureau et du Store, et d’accéder à vos fichiers Windows à partir de Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-132">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="1d7ea-133">Cela vous permet d’utiliser des applications Windows et des outils en ligne de commande Linux sur le même ensemble de fichiers si vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-133">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="1d7ea-134">Pourquoi utiliser, par exemple, Ruby sur Linux plutôt que sur Windows ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-134">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>

<span data-ttu-id="1d7ea-135">Certains outils multiplateformes ont été créés en supposant que l’environnement dans lequel ils s’exécutent se comporte comme Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-135">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="1d7ea-136">Par exemple, certains outils partent du principe qu’ils sont en mesure d’accéder à des chemins de fichiers très longs ou que des fichiers/dossiers spécifiques existent.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-136">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="1d7ea-137">Cela provoque parfois des problèmes sur Windows qui se comporte souvent différemment de Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-137">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="1d7ea-138">De nombreux langages comme Ruby et Node sont souvent portés sur Windows et s’y exécutent très bien.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-138">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="1d7ea-139">Toutefois, les propriétaires de bibliothèques Ruby Gem ou Node/NPM ne portent pas tous leurs bibliothèques pour la prise en charge de Windows, et beaucoup ont des dépendances spécifiques à Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-139">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="1d7ea-140">Cela peut souvent aboutir à des systèmes créés à l’aide de ces outils et bibliothèques qui font l’objet d’erreurs de build et parfois d’exécution ou de comportements indésirables sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-140">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="1d7ea-141">Il s’agit là de quelques-uns des problèmes qui ont conduit de nombreuses personnes à demander à Microsoft d’améliorer les outils en ligne de commande Windows et ce qui nous a amené à collaborer avec Canonical pour permettre aux outils en ligne de commande Linux et Bash natifs de s’exécuter sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-141">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="1d7ea-142">Qu’est-ce que cela signifie pour PowerShell ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-142">What does this mean for PowerShell?</span></span>

<span data-ttu-id="1d7ea-143">Lors de l’utilisation de projets OSS, il existe de nombreux scénarios dans lesquels il est très utile de passer à Bash à partir d’une invite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-143">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="1d7ea-144">La prise en charge de Bash est complémentaire et valorise davantage la ligne de commande sur Windows, ce qui permet à PowerShell et à la communauté PowerShell de tirer parti d’autres technologies répandues.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-144">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="1d7ea-145">Pour en savoir plus, accédez au blog de l’équipe PowerShell : [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-145">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="1d7ea-146">Puis-je exécuter TOUTES les applications Linux dans WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-146">Can I run ALL Linux apps in WSL?</span></span>

<span data-ttu-id="1d7ea-147">Non !</span><span class="sxs-lookup"><span data-stu-id="1d7ea-147">No!</span></span> <span data-ttu-id="1d7ea-148">WSL est un outil destiné à permettre aux utilisateurs qui en ont besoin d’exécuter les principaux outils en ligne de commande Linux et Bash sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-148">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span>

<span data-ttu-id="1d7ea-149">WSL n’a **pas** pour but de prendre en charge les applications ou les ordinateurs de bureau GUI (par exemple, GNOME, KDE, etc.)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-149">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="1d7ea-150">De plus, même si vous pouvez exécuter de nombreuses applications serveur connues (par exemple, Redis), nous vous déconseillons WSL pour l’hébergement des services de production. Microsoft propose diverses solutions pour l’exécution des charges de travail Linux de production dans Azure, Hyper-V et Docker.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-150">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="1d7ea-151">Dans quelles références SKU se trouve Windows WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-151">What Windows SKUs is WSL included in?</span></span>

<span data-ttu-id="1d7ea-152">Le sous-système Windows pour Linux est disponible sur la version bureau de Windows pour Mise à jour anniversaire Windows 10 et Windows 10 Creators Update ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-152">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="1d7ea-153">À partir de Fall Creators Update, WSL sera disponible à la fois sur les références SKU bureau et serveur de Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-153">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="1d7ea-154">Quels sont les processeurs pris en charge par WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-154">What processors does WSL support?</span></span>

<span data-ttu-id="1d7ea-155">WSL prend en charge les processeurs x64 et ARM.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-155">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="1d7ea-156">Comment accéder à mon lecteur C: ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-156">How do I access my C: drive?</span></span>

<span data-ttu-id="1d7ea-157">Des points de montage pour les disques durs sur l’ordinateur local sont créés automatiquement et offrent un accès facile au système de fichiers Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-157">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span>

<span data-ttu-id="1d7ea-158">**/mnt/\<drive letter>/**</span><span class="sxs-lookup"><span data-stu-id="1d7ea-158">**/mnt/\<drive letter>/**</span></span>

<span data-ttu-id="1d7ea-159">Un exemple d’utilisation serait `cd /mnt/c` pour accéder à c:</span><span class="sxs-lookup"><span data-stu-id="1d7ea-159">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-set-up-git-credential-manager-how-do-i-use-my-windows-git-permissions-in-wsl"></a><span data-ttu-id="1d7ea-160">Comment configurer Git Credential Manager ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-160">How do I set up Git Credential Manager?</span></span> <span data-ttu-id="1d7ea-161">(Comment utiliser mes autorisations Windows Git dans WSL ?)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-161">(How do I use my Windows Git permissions in WSL?)</span></span> 

<span data-ttu-id="1d7ea-162">Git Credential Manager vous permet d’authentifier un serveur Git distant, même si vous disposez d’un modèle d’authentification complexe comme Azure Active Directory ou une authentification à deux facteurs.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-162">Git Credential Manager enables you to authenticate a remote Git server, even if you have a complex authentication pattern like Azure Active Directory or two-factor authentication.</span></span> <span data-ttu-id="1d7ea-163">Git Credential Manager s’intègre au flux d’authentification des services tels que GitHub et, une fois que vous êtes authentifié auprès de votre fournisseur d’hébergement, demande un nouveau jeton d’authentification.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-163">Git Credential Manager integrates into the authentication flow for services like GitHub and, once you're authenticated to your hosting provider, requests a new authentication token.</span></span> <span data-ttu-id="1d7ea-164">Il stocke ensuite le jeton de façon sécurisée dans le gestionnaire d’informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-164">It then stores the token securely in the Windows Credential Manager.</span></span> <span data-ttu-id="1d7ea-165">Après la première fois, vous pouvez utiliser Git pour communiquer avec votre fournisseur d’hébergement sans avoir à vous réauthentifier.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-165">After the first time, you can use git to talk to your hosting provider without needing to re-authenticate.</span></span> <span data-ttu-id="1d7ea-166">Il accède simplement au jeton dans le gestionnaire d’informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-166">It will just access the token in the Windows Credential Manager.</span></span>

<span data-ttu-id="1d7ea-167">Pour configurer Git Credential Manager en vue de l’utiliser avec une distribution WSL, ouvrez votre distribution et entrez cette commande :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-167">To set up Git Credential Manager for use with a WSL distribution, open your distribution and enter this command:</span></span>

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

<span data-ttu-id="1d7ea-168">À présent, toute opération git que vous effectuez dans votre distribution WSL utilise le gestionnaire d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-168">Now any git operation you perform within your WSL distribution will use the credential manager.</span></span> <span data-ttu-id="1d7ea-169">Si vous avez déjà mis en cache les informations d’identification d’un hôte, celui-ci y accède à partir du gestionnaire d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-169">If you already have credentials cached for a host, it will access them from the credential manager.</span></span> <span data-ttu-id="1d7ea-170">Si ce n’est pas le cas, vous recevez une réponse de boîte de dialogue demandant vos informations d’identification, même si vous êtes dans une console Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-170">If not, you'll receive a dialog response requesting your credentials, even if you're in a Linux console.</span></span>

<span data-ttu-id="1d7ea-171">Cette prise en charge s’appuie sur l’[interopérabilité entre le sous-système Windows pour Linux et Windows lui-même](https://docs.microsoft.com/windows/wsl/interop).</span><span class="sxs-lookup"><span data-stu-id="1d7ea-171">This support relies on the [interoperability between Windows Subsystem for Linux and Windows itself](https://docs.microsoft.com/windows/wsl/interop).</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="1d7ea-172">Comment utiliser un fichier Windows avec une application Linux ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-172">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="1d7ea-173">L’un des avantages de WSL est la possibilité d’accéder à vos fichiers via des applications ou des outils Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-173">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="1d7ea-174">WSL monte les lecteurs fixes de votre ordinateur sous le dossier `/mnt/<drive>` de vos distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-174">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="1d7ea-175">Par exemple, votre lecteur `C:` est monté sous `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="1d7ea-175">For example, your `C:` drive is mounted under `/mnt/c/`</span></span>

<span data-ttu-id="1d7ea-176">À l’aide de vos lecteurs montés, vous pouvez modifier le code dans, par exemple, `C:\dev\myproj\` à l’aide de [Visual Studio](https://visualstudio.microsoft.com/vs/) /ou [VS Code](https://code.visualstudio.com/) et générer/tester ce code dans Linux en accédant aux mêmes fichiers via `/mnt/c/dev/myproj`.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-176">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="1d7ea-177">**REMARQUE IMPORTANTE** : L’une des principales limitations de l’utilisation de WSL est que l’accès direct aux fichiers ou leur modification dans le système de fichiers des distributions Linux à l’aide d’applications ou d’outils Windows n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-177">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="1d7ea-178">Voir : [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-178">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="1d7ea-179">Les fichiers du lecteur Linux sont-ils différents du lecteur Windows monté ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-179">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="1d7ea-180">Les fichiers sous la racine Linux (autrement dit, `/`) sont contrôlés par WSL, ce qui reproduit le comportement spécifique de Linux, notamment mais sans s’y limiter :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-180">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="1d7ea-181">Fichiers qui contiennent des caractères de nom de fichier Windows non valides</span><span class="sxs-lookup"><span data-stu-id="1d7ea-181">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="1d7ea-182">Liens symboliques créés pour les utilisateurs non-administrateurs</span><span class="sxs-lookup"><span data-stu-id="1d7ea-182">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="1d7ea-183">Changement des attributs de fichier via chmod et chown</span><span class="sxs-lookup"><span data-stu-id="1d7ea-183">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="1d7ea-184">Respect de la casse des fichiers/dossiers</span><span class="sxs-lookup"><span data-stu-id="1d7ea-184">File/folder case sensitivity</span></span>

2. <span data-ttu-id="1d7ea-185">Les fichiers des lecteurs montés sont contrôlés par Windows et présentent les comportements suivants :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-185">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="1d7ea-186">Prise en charge du respect de la casse</span><span class="sxs-lookup"><span data-stu-id="1d7ea-186">Support case sensitivity</span></span>
   * <span data-ttu-id="1d7ea-187">Toutes les autorisations sont définies pour mieux refléter les autorisations Windows</span><span class="sxs-lookup"><span data-stu-id="1d7ea-187">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="1d7ea-188">Pourquoi autant d’erreurs sont retournées quand j’exécute apt-get upgrade ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-188">Why are there so many errors when I run apt-get upgrade?</span></span>

<span data-ttu-id="1d7ea-189">Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-189">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="1d7ea-190">`udev`, par exemple, n’est pas encore pris en charge et provoque plusieurs erreurs avec `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-190">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="1d7ea-191">Pour résoudre les problèmes liés à `udev`, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-191">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="1d7ea-192">Écrivez le code suivant dans `/usr/sbin/policy-rc.d` et enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-192">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="1d7ea-193">Ajoutez des autorisations d’exécution à `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="1d7ea-193">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
3. <span data-ttu-id="1d7ea-194">Exécutez les commandes suivantes</span><span class="sxs-lookup"><span data-stu-id="1d7ea-194">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="1d7ea-195">Comment désinstaller une distribution WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-195">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="1d7ea-196">Sur les builds antérieures à 1709 (16299), ouvrez une invite de commandes et exécutez :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-196">On builds prior to 1709 (16299) open a command prompt and run:</span></span>

  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="1d7ea-197">Les distributions WSL installées à partir du Store peuvent être désinstallées comme n’importe quelle autre application Windows, en cliquant avec le bouton droit sur la vignette de l’application et en cliquant sur Désinstaller ou via PowerShell à l’aide de l’[`Remove-AppxPackage`applet de commande ](https://technet.microsoft.com/library/hh856038.aspx).</span><span class="sxs-lookup"><span data-stu-id="1d7ea-197">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="1d7ea-198">Pourquoi la commande ping génère des erreurs d’autorisation refusée ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-198">Why does ping generate permission denied errors?</span></span>

<span data-ttu-id="1d7ea-199">Dans les builds WSL antérieures à 14926, l’exécution de la commande ping via une console avec élévation de privilèges nécessitait WSL.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-199">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="1d7ea-200">Ce problème a été résolu dans la build 14926 et ultérieur.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-200">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="1d7ea-201">Comment exécuter un serveur OpenSSH ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-201">How do I run an OpenSSH server?</span></span>

<span data-ttu-id="1d7ea-202">L’exécution d’un serveur OpenSSH dans WSL nécessite des privilèges d’administrateur dans Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-202">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="1d7ea-203">Pour exécuter un serveur OpenSSH, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite de commandes CMD/PowerShell avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-203">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="1d7ea-204">Pourquoi est-ce que je reçois « Erreur : 0x80040306 » pendant l’installation ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-204">Why do I get "Error: 0x80040306" when I try to install?</span></span>

<span data-ttu-id="1d7ea-205">WSL ne prend pas en charge l’exécution dans une console héritée.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-205">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="1d7ea-206">Pour désactiver la console héritée :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-206">To turn off legacy console:</span></span>

1. <span data-ttu-id="1d7ea-207">Ouvrez WSL, PowerShell ou Cmd</span><span class="sxs-lookup"><span data-stu-id="1d7ea-207">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="1d7ea-208">Cliquez avec le bouton droit sur la barre de titre, sélectionnez Propriétés, puis décochez Utiliser la console héritée</span><span class="sxs-lookup"><span data-stu-id="1d7ea-208">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="1d7ea-209">Cliquez sur OK</span><span class="sxs-lookup"><span data-stu-id="1d7ea-209">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="1d7ea-210">Pourquoi est-ce que je reçois « Erreur : 0x80040154 » quand j’exécute bash.exe après la mise à niveau de Windows ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-210">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>

<span data-ttu-id="1d7ea-211">La fonctionnalité Sous-système Windows pour Linux peut être désactivée au cours d’une mise à jour de Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-211">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="1d7ea-212">Dans ce cas, la fonctionnalité Windows doit être réactivée.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-212">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="1d7ea-213">Pour obtenir des instructions sur l’activation de la fonctionnalité Sous-système Windows pour Linux, consultez le [guide d’installation](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span><span class="sxs-lookup"><span data-stu-id="1d7ea-213">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="1d7ea-214">Comment changer la langue d’affichage de WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-214">How do I change the display language of WSL?</span></span>

<span data-ttu-id="1d7ea-215">Le processus d’installation de WSL tente de changer automatiquement les paramètres régionaux d’Ubuntu de sorte qu’ils correspondent à ceux de votre installation Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-215">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="1d7ea-216">Si vous souhaitez éviter ce comportement, vous pouvez exécuter cette commande pour changer les paramètres régionaux d’Ubuntu une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-216">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="1d7ea-217">Vous devrez relancer bash.exe pour que ce changement prenne effet.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-217">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="1d7ea-218">L’exemple ci-dessous applique les paramètres régionaux en-US :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-218">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="1d7ea-219">Pourquoi est-ce que je n’ai pas d’accès Internet à partir de WSL ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-219">Why do I not have internet access from WSL?</span></span>

<span data-ttu-id="1d7ea-220">Des utilisateurs ont signalé des problèmes posés par certaines applications de pare-feu, qui bloquent l’accès Internet dans WSL.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-220">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="1d7ea-221">Les pare-feux signalés sont :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-221">The firewalls reported are:</span></span>

1. <span data-ttu-id="1d7ea-222">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="1d7ea-222">Kaspersky</span></span>
1. <span data-ttu-id="1d7ea-223">AVG</span><span class="sxs-lookup"><span data-stu-id="1d7ea-223">AVG</span></span>
1. <span data-ttu-id="1d7ea-224">Avast</span><span class="sxs-lookup"><span data-stu-id="1d7ea-224">Avast</span></span>

<span data-ttu-id="1d7ea-225">Dans certains cas, la désactivation du pare-feu permet d’obtenir l’accès.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-225">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="1d7ea-226">Parfois, il semble que la simple installation du pare-feu bloque l’accès.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-226">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="1d7ea-227">Comment accéder à un port à partir de WSL dans Windows ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-227">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="1d7ea-228">WSL partage l’adresse IP de Windows, car il s’exécute sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-228">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="1d7ea-229">Par conséquent, vous pouvez accéder à n’importe quel port sur localhost ; par exemple, si vous avez du contenu web sur le port 1234, vous pouvez utiliser https://localhost:1234 dans votre navigateur Windows.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-229">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros-or-move-them-from-one-drive-to-another"></a><span data-ttu-id="1d7ea-230">Comment sauvegarder mes distributions WSL ou les déplacer d’un lecteur à un autre ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-230">How can I back up my WSL distros, or move them from one drive to another?</span></span>

<span data-ttu-id="1d7ea-231">La meilleure façon de sauvegarder ou de déplacer vos distributions consiste à utiliser les commandes d’exportation/importation disponibles dans Windows version 1809 et ultérieure.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-231">The best way to backup or move your distros is via the export/import commands available in Windows Version 1809 and later.</span></span> <span data-ttu-id="1d7ea-232">Vous pouvez exporter l’intégralité de votre distribution vers un tarball à l’aide de la commande `wsl --export`.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-232">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="1d7ea-233">Vous pouvez ensuite réimporter cette distribution dans WSL à l’aide de la commande `wsl --import`, ce qui peut nommer un nouvel emplacement de lecteur pour l’importation. Vous pouvez ainsi sauvegarder et enregistrer les états de vos distributions WSL, ou déplacer ces dernières.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-233">You can then import this distro back into WSL using the `wsl --import` command, which can name a new drive location for the import, allowing you to backup and save states of (or move) your WSL distributions.</span></span> 

<span data-ttu-id="1d7ea-234">Notez que les services de sauvegarde classiques qui sauvegardent les fichiers dans vos dossiers Appdata (comme la sauvegarde Windows) n’endommageront pas vos fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-234">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="1d7ea-235">Où puis-je envoyer des commentaires ?</span><span class="sxs-lookup"><span data-stu-id="1d7ea-235">Where can I provide feedback?</span></span>

<span data-ttu-id="1d7ea-236">Vous pouvez partager vos commentaires et poser vos questions via plusieurs canaux.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-236">You can share feedback and ask questions through multiple channels.</span></span>

<span data-ttu-id="1d7ea-237">Si vous rencontrez des problèmes techniques ou si vous voulez demander de nouvelles fonctionnalités, accédez à notre suivi des problèmes Github :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-237">If you have technical issues, or want to request new features please go to our Github issue tracker:</span></span>

* [<span data-ttu-id="1d7ea-238">Outil de suivi des problèmes GitHub</span><span class="sxs-lookup"><span data-stu-id="1d7ea-238">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)

<span data-ttu-id="1d7ea-239">Si vous voulez rester informé des dernières informations sur WSL, vous pouvez le faire sur :</span><span class="sxs-lookup"><span data-stu-id="1d7ea-239">If you'd like to stay up to date with the latest WSL news you can do so with:</span></span>

* <span data-ttu-id="1d7ea-240">Notre [blog de l’équipe sur les lignes de commande](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="1d7ea-240">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="1d7ea-241">Twitter.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-241">Twitter.</span></span> <span data-ttu-id="1d7ea-242">Suivez [@craigaloewen](https://twitter.com/craigaloewen) sur Twitter pour être averti des nouveautés, mises à jour, etc.</span><span class="sxs-lookup"><span data-stu-id="1d7ea-242">Please follow [@craigaloewen](https://twitter.com/craigaloewen) on Twitter to learn of news, updates, etc.</span></span>
