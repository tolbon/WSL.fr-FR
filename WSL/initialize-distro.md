---
title: Initialisation d’une nouvelle distribution Linux WSL
description: Après avoir installé une distribution Linux pour WSL, effectuez l’initialisation en suivant ces étapes simples.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c33d349a6d39c325b079ccbf7ed6350bed796e33
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269587"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="61c5f-104">Initialisation d’une distribution nouvellement installée</span><span class="sxs-lookup"><span data-stu-id="61c5f-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="61c5f-105">Une fois votre distribution téléchargée et installée, vous devez effectuer l’initialisation de la nouvelle distribution :</span><span class="sxs-lookup"><span data-stu-id="61c5f-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="61c5f-106">Lancer une distribution</span><span class="sxs-lookup"><span data-stu-id="61c5f-106">Launch a distro</span></span>
<span data-ttu-id="61c5f-107">Pour effectuer l’initialisation de votre distribution nouvellement installée, lancez une nouvelle instance.</span><span class="sxs-lookup"><span data-stu-id="61c5f-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="61c5f-108">Pour ce faire, vous pouvez cliquer sur le bouton « Lancer » dans l’application Microsoft Store ou lancer la distribution à partir du menu Démarrer :</span><span class="sxs-lookup"><span data-stu-id="61c5f-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="61c5f-109">Astuce : Vous pouvez épingler vos distributions les plus fréquemment utilisées à votre menu Démarrer et/ou à votre barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="61c5f-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![Lancer les distributions à partir du menu Démarrer](media/start-menu.png)

> <span data-ttu-id="61c5f-111">Sur Windows Server, vous pouvez lancer l’exécutable du lanceur de votre distribution `<distro>.exe` à partir du dossier d’installation de la distribution.</span><span class="sxs-lookup"><span data-stu-id="61c5f-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="61c5f-112">La première fois qu’une distribution nouvellement installée s’exécute, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux, le temps que l’installation se termine.</span><span class="sxs-lookup"><span data-stu-id="61c5f-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="61c5f-113">Au cours de cette dernière étape de l’installation, les fichiers de la distribution sont décompressés et stockés sur votre PC, prêts à être utilisés.</span><span class="sxs-lookup"><span data-stu-id="61c5f-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="61c5f-114">Cette opération peut prendre environ une minute ou plus en fonction des performances des dispositifs de stockage de votre PC.</span><span class="sxs-lookup"><span data-stu-id="61c5f-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="61c5f-115">Cette phase d’installation initiale est requise uniquement lors d’une nouvelle installation d’une distribution : tous les lancements ultérieurs doivent prendre moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="61c5f-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="61c5f-116">Configuration d’un nouveau compte d’utilisateur Linux</span><span class="sxs-lookup"><span data-stu-id="61c5f-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="61c5f-117">Une fois l’installation terminée, vous êtes invité à créer un compte d’utilisateur (et son mot de passe).</span><span class="sxs-lookup"><span data-stu-id="61c5f-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

<span data-ttu-id="61c5f-119">Ce compte d’utilisateur est destiné à l’utilisateur non-administrateur normal sous lequel vous vous connectez par défaut lors du lancement d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="61c5f-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="61c5f-120">Vous pouvez choisir le nom d’utilisateur et le mot de passe de votre choix : ils n’ont aucun impact sur votre nom d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="61c5f-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="61c5f-121">Quand vous ouvrez une nouvelle instance de la distribution, vous n’êtes pas invité à entrer votre mot de passe, mais **si vous élevez un processus à l’aide de `sudo`, vous devez l’entrer**. Veillez donc à choisir un mot de passe facile à mémoriser !</span><span class="sxs-lookup"><span data-stu-id="61c5f-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="61c5f-122">Pour plus d’informations, consultez la page du [support utilisateur](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="61c5f-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="61c5f-123">Mettre à jour et mettre à niveau les packages de votre distribution</span><span class="sxs-lookup"><span data-stu-id="61c5f-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="61c5f-124">La plupart des distributions sont livrées avec un catalogue de packages vides/minimaux.</span><span class="sxs-lookup"><span data-stu-id="61c5f-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="61c5f-125">Nous vous recommandons vivement de mettre à jour régulièrement le catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="61c5f-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="61c5f-126">Sur Debian/Ubuntu, vous utilisez apt :</span><span class="sxs-lookup"><span data-stu-id="61c5f-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="61c5f-127">Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux : Il s’agit d’une tâche que les utilisateurs de Linux préfèrent contrôler eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="61c5f-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="61c5f-128">C’est terminé !</span><span class="sxs-lookup"><span data-stu-id="61c5f-128">You're done!</span></span> <span data-ttu-id="61c5f-129">Profitez de votre nouvelle distribution Linux sur WSL !</span><span class="sxs-lookup"><span data-stu-id="61c5f-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="61c5f-130">Pour en savoir plus sur WSL, consultez l’autre [documentation sur WSL](https://aka.ms/wsldocs) ou la page des [ressources de formation WSL](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="61c5f-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Profitez de l’utilisation de Linux sur WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="61c5f-132">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="61c5f-132">Troubleshooting</span></span>

<span data-ttu-id="61c5f-133">Vous trouverez ci-dessous des erreurs associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="61c5f-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="61c5f-134">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="61c5f-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="61c5f-135">**Échec de l’installation avec l’erreur 0x8007007e** Cette erreur se produit quand votre système ne prend pas en charge Linux à partir du Store.</span><span class="sxs-lookup"><span data-stu-id="61c5f-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="61c5f-136">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="61c5f-136">Make sure that:</span></span>
> * <span data-ttu-id="61c5f-137">Vous exécutez la build Windows 16215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="61c5f-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="61c5f-138">[Vérifiez votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="61c5f-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="61c5f-139">Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.</span><span class="sxs-lookup"><span data-stu-id="61c5f-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="61c5f-140">[Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="61c5f-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
