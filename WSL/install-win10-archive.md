---
title: Installer le sous-système Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation du sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6ed12ba9d63d3f4038b67489035e13113a372928
ms.sourcegitcommit: 9f12e168b80775cd967f22f97376e51043c3667e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2020
ms.locfileid: "84301200"
---
# <a name="install-windows-subsystem-for-linux"></a><span data-ttu-id="8a58e-104">Installer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="8a58e-104">Install Windows Subsystem for Linux</span></span>

<span data-ttu-id="8a58e-105">Le guide suivant vous accompagne tout au long des étapes d’installation du sous-système Windows pour Linux (WSL) sur un ordinateur exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8a58e-105">The following guide will walk through the steps required to install the Windows Subsystem for Linux (WSL) on a computer running Windows 10.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a><span data-ttu-id="8a58e-106">Activer la fonctionnalité facultative Sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="8a58e-106">Enable the Windows Subsystem for Linux optional feature</span></span>

<span data-ttu-id="8a58e-107">Avant d’installer une distribution Linux, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » sur Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="8a58e-107">Before installing a Linux distribution, you must enable the "Windows Subsystem for Linux" optional feature on Windows 10:</span></span>

1. <span data-ttu-id="8a58e-108">Ouvrez PowerShell en tant qu’administrateur, puis entrez le script suivant :</span><span class="sxs-lookup"><span data-stu-id="8a58e-108">Open PowerShell as Administrator and enter this script:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. <span data-ttu-id="8a58e-109">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="8a58e-109">Restart your computer when prompted.</span></span>

## <a name="install-a-linux-distribution"></a><span data-ttu-id="8a58e-110">Installer une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="8a58e-110">Install a Linux distribution</span></span>

<span data-ttu-id="8a58e-111">Il existe trois façons de télécharger et d’installer vos distributions Linux préférées :</span><span class="sxs-lookup"><span data-stu-id="8a58e-111">There are three ways to download and install your preferred Linux distribution(s):</span></span>

- <span data-ttu-id="8a58e-112">Télécharger et installer à partir du Microsoft Store (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="8a58e-112">Download and install from the Microsoft Store (see below)</span></span>
- [<span data-ttu-id="8a58e-113">Télécharger et installer manuellement à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="8a58e-113">Download and manually install from command line</span></span>](install-manual.md)
- [<span data-ttu-id="8a58e-114">Installation sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="8a58e-114">Install on Windows Server</span></span>](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a><span data-ttu-id="8a58e-115">installer à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="8a58e-115">Install from the Microsoft Store</span></span>

<span data-ttu-id="8a58e-116">Les distributions Linux peuvent être installées à partir de Microsoft Store sur Windows 10 (build 16215+).</span><span class="sxs-lookup"><span data-stu-id="8a58e-116">Linux distributions can be installed from the Microsoft Store on Windows 10 (Build 16215+).</span></span>

> [!NOTE]
> <span data-ttu-id="8a58e-117">Effectuez ces étapes pour [vérifier votre numéro de build de Windows 10](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="8a58e-117">Follow these steps to [check your Windows 10 build number](troubleshooting.md#check-your-build-number).</span></span>

1. <span data-ttu-id="8a58e-118">Ouvrez le Microsoft Store et choisissez votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="8a58e-118">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    <span data-ttu-id="8a58e-120">Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :</span><span class="sxs-lookup"><span data-stu-id="8a58e-120">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="8a58e-121">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="8a58e-121">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="8a58e-122">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="8a58e-122">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="8a58e-123">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="8a58e-123">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [<span data-ttu-id="8a58e-124">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="8a58e-124">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [<span data-ttu-id="8a58e-125">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="8a58e-125">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [<span data-ttu-id="8a58e-126">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="8a58e-126">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [<span data-ttu-id="8a58e-127">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="8a58e-127">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="8a58e-128">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="8a58e-128">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="8a58e-129">Fedora Remix pour WSL</span><span class="sxs-lookup"><span data-stu-id="8a58e-129">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="8a58e-130">Pengwin</span><span class="sxs-lookup"><span data-stu-id="8a58e-130">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="8a58e-131">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="8a58e-131">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="8a58e-132">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="8a58e-132">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="8a58e-133">Sélectionnez « Obtenir », puis, une fois le téléchargement de la distribution terminé, sélectionnez « Lancer ».</span><span class="sxs-lookup"><span data-stu-id="8a58e-133">Select "Get" and once the distribution has finished downloading, select "Launch".</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="8a58e-135">Effectuer l’initialisation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="8a58e-135">Complete initialization of your distro</span></span>

<span data-ttu-id="8a58e-136">Après avoir lancé votre distribution Linux, suivez les instructions affichées à l’écran pour initialiser votre distribution.</span><span class="sxs-lookup"><span data-stu-id="8a58e-136">After launching your Linux distribution, follow the onscreen instructions to initialize your distro.</span></span>

> [!NOTE]
> <span data-ttu-id="8a58e-137">Pour Windows Server, lancez votre distribution à l’aide de l’exécutable, `<distro>.exe`, dans le dossier d’installation.</span><span class="sxs-lookup"><span data-stu-id="8a58e-137">For Windows Server, launch your distribution using the executable, `<distro>.exe`, in the installation folder.</span></span>

<span data-ttu-id="8a58e-138">Lors de la première exécution d’une distribution nouvellement installée, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux, le temps que l’installation se termine.</span><span class="sxs-lookup"><span data-stu-id="8a58e-138">The first time a newly installed distribution runs, a console window will open and you'll be asked to wait for a minute or two for the installation to complete.</span></span> <span data-ttu-id="8a58e-139">Au cours de cette dernière étape de l’installation, les fichiers de la distribution sont décompressés et stockés sur votre PC, prêts à être utilisés.</span><span class="sxs-lookup"><span data-stu-id="8a58e-139">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="8a58e-140">Cette opération peut prendre environ une minute ou plus en fonction des performances des dispositifs de stockage de votre PC.</span><span class="sxs-lookup"><span data-stu-id="8a58e-140">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="8a58e-141">Cette phase d’installation initiale est requise uniquement lors d’une nouvelle installation d’une distribution : tous les lancements ultérieurs doivent prendre moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="8a58e-141">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="set-up-a-new-linux-user-account"></a><span data-ttu-id="8a58e-142">Configurer un nouveau compte d’utilisateur Linux</span><span class="sxs-lookup"><span data-stu-id="8a58e-142">Set up a new Linux user account</span></span>

<span data-ttu-id="8a58e-143">Une fois l’installation terminée, vous êtes invité à créer un compte d’utilisateur (et son mot de passe).</span><span class="sxs-lookup"><span data-stu-id="8a58e-143">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

<span data-ttu-id="8a58e-145">Ce compte d’utilisateur est destiné à l’utilisateur non-administrateur normal sous lequel vous vous connectez par défaut lors du lancement d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="8a58e-145">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span> <span data-ttu-id="8a58e-146">Vous pouvez choisir le nom d’utilisateur et le mot de passe de votre choix : ils n’ont aucun impact sur votre nom d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="8a58e-146">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="8a58e-147">Quand vous ouvrez une nouvelle instance de la distribution, vous n’êtes pas invité à entrer votre mot de passe, mais **si vous élevez un processus à l’aide de `sudo`, vous devez l’entrer**. Veillez donc à choisir un mot de passe facile à mémoriser !</span><span class="sxs-lookup"><span data-stu-id="8a58e-147">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="8a58e-148">Pour plus d’informations, consultez la page du [support utilisateur](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="8a58e-148">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-packages"></a><span data-ttu-id="8a58e-149">Mettre à jour et mettre à niveau des packages</span><span class="sxs-lookup"><span data-stu-id="8a58e-149">Update & upgrade packages</span></span>

<span data-ttu-id="8a58e-150">La plupart des distributions sont livrées avec un catalogue de packages vide ou minimal.</span><span class="sxs-lookup"><span data-stu-id="8a58e-150">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="8a58e-151">Nous vous recommandons vivement de mettre à jour régulièrement votre catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="8a58e-151">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="8a58e-152">Pour Debian/Ubuntu, utilisez apt :</span><span class="sxs-lookup"><span data-stu-id="8a58e-152">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="8a58e-153">Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="8a58e-153">Windows does not automatically update or upgrade your Linux distro(s).</span></span> <span data-ttu-id="8a58e-154">Il s’agit d’une tâche que la plupart des utilisateurs Linux préfèrent contrôler eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="8a58e-154">This is a task that the most Linux users prefer to control themselves.</span></span>

<span data-ttu-id="8a58e-155">Profitez de votre nouvelle distribution Linux sur WSL !</span><span class="sxs-lookup"><span data-stu-id="8a58e-155">Enjoy using your new Linux distro on WSL!</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8a58e-156">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="8a58e-156">Troubleshooting</span></span>

<span data-ttu-id="8a58e-157">Vous trouverez ci-dessous des erreurs d’installation associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="8a58e-157">Below are related installation errors and suggested fixes.</span></span> <span data-ttu-id="8a58e-158">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="8a58e-158">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

### <a name="installation-failed-with-error-0x8007007e"></a><span data-ttu-id="8a58e-159">Échec de l’installation avec l’erreur 0x8007007e</span><span class="sxs-lookup"><span data-stu-id="8a58e-159">Installation failed with error 0x8007007e</span></span>

<span data-ttu-id="8a58e-160">Cette erreur se produit quand votre système ne prend pas en charge Linux à partir du Store.</span><span class="sxs-lookup"><span data-stu-id="8a58e-160">This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="8a58e-161">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="8a58e-161">Make sure that:</span></span>

- <span data-ttu-id="8a58e-162">Vous exécutez la build Windows 16215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8a58e-162">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="8a58e-163">[Vérifiez votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="8a58e-163">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
- <span data-ttu-id="8a58e-164">Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.</span><span class="sxs-lookup"><span data-stu-id="8a58e-164">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="8a58e-165">[Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="8a58e-165">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>

### <a name="installation-failed-with-error-0x80070003"></a><span data-ttu-id="8a58e-166">Échec de l’installation avec l’erreur 0x80070003</span><span class="sxs-lookup"><span data-stu-id="8a58e-166">Installation failed with error 0x80070003</span></span>

<span data-ttu-id="8a58e-167">Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`).</span><span class="sxs-lookup"><span data-stu-id="8a58e-167">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="8a58e-168">Vérifiez que les distributions sont stockées sur votre lecteur système :</span><span class="sxs-lookup"><span data-stu-id="8a58e-168">Make sure that distros are stored on your system drive:</span></span>

- <span data-ttu-id="8a58e-169">Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Changer l’emplacement d’enregistrement du nouveau contenu**</span><span class="sxs-lookup"><span data-stu-id="8a58e-169">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**</span></span>
  
    ![Image des paramètres système pour installer des applications sur le lecteur C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a><span data-ttu-id="8a58e-171">Échec de WslRegisterDistribution avec l’erreur 0x8007019e</span><span class="sxs-lookup"><span data-stu-id="8a58e-171">WslRegisterDistribution failed with error 0x8007019e</span></span>

<span data-ttu-id="8a58e-172">Le composant facultatif Sous-système Windows pour Linux n’est pas activé :</span><span class="sxs-lookup"><span data-stu-id="8a58e-172">The Windows Subsystem for Linux optional component is not enabled:</span></span>

- <span data-ttu-id="8a58e-173">Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="8a58e-173">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
