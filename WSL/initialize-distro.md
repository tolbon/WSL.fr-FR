---
title: Initialiser une nouvelle distribution Linux de WSL
description: Après avoir installé une distribution Linux pour WSL, terminer l’initialisation en suivant ces étapes simples
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902046"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="abdb6-104">L’initialisation d’une distribution nouvellement installée</span><span class="sxs-lookup"><span data-stu-id="abdb6-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="abdb6-105">Une fois que votre distribution a été téléchargée et installée, vous devez effectuer l’initialisation de la nouvelle distribution :</span><span class="sxs-lookup"><span data-stu-id="abdb6-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="abdb6-106">Lancer un distributeur</span><span class="sxs-lookup"><span data-stu-id="abdb6-106">Launch a distro</span></span>
<span data-ttu-id="abdb6-107">Pour terminer l’initialisation de votre distribution nouvellement installée, lancez une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="abdb6-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="abdb6-108">Vous pouvez le faire en cliquant sur le bouton « lancement » dans l’application du Windows Store, ou en lançant la distribution dans le menu Démarrer :</span><span class="sxs-lookup"><span data-stu-id="abdb6-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="abdb6-109">Astuce : Vous souhaiterez peut-être épingler vos distributions fréquemment utilisées dans votre menu Démarrer, et/ou à votre barre des tâches !</span><span class="sxs-lookup"><span data-stu-id="abdb6-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Lancer des distributions à partir du menu Démarrer](media/start-menu.png)

> <span data-ttu-id="abdb6-111">Sur Windows Server, vous pouvez lancer le Lanceur de votre distribution exécutable `<distro>.exe` à partir du dossier d’installation de distribution.</span><span class="sxs-lookup"><span data-stu-id="abdb6-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="abdb6-112">La première fois une distribution nouvellement installée s’exécute, une Console fenêtre s’ouvre, et vous devrez attendre une ou deux minutes pour terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="abdb6-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="abdb6-113">Au cours de cette étape finale de l’installation, les fichiers de la distribution sont retirer compressés et stockés sur votre PC, prêt à être utilisé.</span><span class="sxs-lookup"><span data-stu-id="abdb6-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="abdb6-114">Cette opération peut prendre autour d’une minute ou plus selon les performances des périphériques de stockage de votre PC.</span><span class="sxs-lookup"><span data-stu-id="abdb6-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="abdb6-115">Cette phase de l’installation initiale est uniquement requis lorsqu’un distributeur est correctement installé - tous les futurs lancements doivent prendre moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="abdb6-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="abdb6-116">Configuration d’un nouveau compte d’utilisateur Linux</span><span class="sxs-lookup"><span data-stu-id="abdb6-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="abdb6-117">Une fois l’installation terminée, vous devrez créer un nouveau compte d’utilisateur (et son mot de passe).</span><span class="sxs-lookup"><span data-stu-id="abdb6-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Ubuntu décompression dans la console Windows](media/UbuntuInstall.png)

<span data-ttu-id="abdb6-119">Ce compte d’utilisateur est pour l’utilisateur non-administrateur normal que vous serez connecté en tant que par défaut lors du lancement d’un distributeur.</span><span class="sxs-lookup"><span data-stu-id="abdb6-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="abdb6-120">Vous pouvez choisir n’importe quel nom d’utilisateur et le mot de passe : ils n’ont aucune incidence sur votre nom d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="abdb6-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="abdb6-121">Lorsque vous ouvrez une nouvelle instance de distributeur, vous ne sont pas être invité à entrer votre mot de passe, mais **si vous élevez un processus utilisant `sudo`, vous devez entrer votre mot de passe**, assurez-vous que vous choisissez un mot de passe que vous vous souviendrez facilement !</span><span class="sxs-lookup"><span data-stu-id="abdb6-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="abdb6-122">Consultez le [prise en charge de l’utilisateur](user-support.md) page pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="abdb6-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="abdb6-123">Mise à jour & Mettre à niveau les packages de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="abdb6-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="abdb6-124">La plupart des distributions sont livrés avec un catalogue de package vide/minimale.</span><span class="sxs-lookup"><span data-stu-id="abdb6-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="abdb6-125">Nous vous recommandons fortement régulièrement mise à jour de votre catalogue de package et la mise à niveau vos packages installés à l’aide du Gestionnaire de package préféré de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="abdb6-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="abdb6-126">Sur Debian/Ubuntu, vous utilisez apt :</span><span class="sxs-lookup"><span data-stu-id="abdb6-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="abdb6-127">Windows ne pas automatiquement mise à jour et mettre à niveau votre distro(s) Linux : Il s’agit d’une tâche que les utilisateurs Linux préfèrent contrôler eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="abdb6-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="abdb6-128">C’est terminé !</span><span class="sxs-lookup"><span data-stu-id="abdb6-128">You're done!</span></span> <span data-ttu-id="abdb6-129">Profitez de l’utilisation de votre distribution Linux de nouveau sur WSL !</span><span class="sxs-lookup"><span data-stu-id="abdb6-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="abdb6-130">Pour en savoir plus sur WSL, passez en revue l’autre [docs WSL](https://aka.ms/wsldocs), ou le [WSL page de ressources de formation](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="abdb6-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Vous profiterez Linux sur WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="abdb6-132">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="abdb6-132">Troubleshooting</span></span>

<span data-ttu-id="abdb6-133">Voici les erreurs associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="abdb6-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="abdb6-134">Reportez-vous à la [page Résolution des problèmes de WSL](troubleshooting.md) pour les autres erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="abdb6-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="abdb6-135">**Échec de l’installation avec l’erreur 0x8007007e** cette erreur se produit lorsque votre système ne prend pas en charge Linux à partir du magasin.</span><span class="sxs-lookup"><span data-stu-id="abdb6-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="abdb6-136">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="abdb6-136">Make sure that:</span></span>
> * <span data-ttu-id="abdb6-137">Vous exécutez Windows build 16215 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="abdb6-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="abdb6-138">[Vérifier votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="abdb6-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="abdb6-139">Le sous-système Windows pour le composant facultatif de Linux est activé et que l’ordinateur a redémarré.</span><span class="sxs-lookup"><span data-stu-id="abdb6-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="abdb6-140">[Assurez-vous que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="abdb6-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
