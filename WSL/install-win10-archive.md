---
title: Instructions WSL archivées
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ROBOTS: NOINDEX
ms.openlocfilehash: 1de614dccbbb8d0ef1b9ac070f6ec90281339858
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/09/2020
ms.locfileid: "86157955"
---
# <a name="archived-instructions"></a><span data-ttu-id="44d9a-102">Instructions archivées</span><span class="sxs-lookup"><span data-stu-id="44d9a-102">Archived instructions</span></span>

<span data-ttu-id="44d9a-103">Le guide suivant vous accompagne tout au long des étapes d’installation du sous-système Windows pour Linux (WSL) sur un ordinateur exécutant Windows 10.</span><span class="sxs-lookup"><span data-stu-id="44d9a-103">The following guide will walk through the steps required to install the Windows Subsystem for Linux (WSL) on a computer running Windows 10.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a><span data-ttu-id="44d9a-104">Activer la fonctionnalité facultative Sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="44d9a-104">Enable the Windows Subsystem for Linux optional feature</span></span>

<span data-ttu-id="44d9a-105">Avant d’installer une distribution Linux, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » sur Windows 10 :</span><span class="sxs-lookup"><span data-stu-id="44d9a-105">Before installing a Linux distribution, you must enable the "Windows Subsystem for Linux" optional feature on Windows 10:</span></span>

1. <span data-ttu-id="44d9a-106">Ouvrez PowerShell en tant qu’administrateur, puis entrez le script suivant :</span><span class="sxs-lookup"><span data-stu-id="44d9a-106">Open PowerShell as Administrator and enter this script:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. <span data-ttu-id="44d9a-107">Redémarrez votre ordinateur lorsque vous y êtes invité.</span><span class="sxs-lookup"><span data-stu-id="44d9a-107">Restart your computer when prompted.</span></span>

## <a name="install-a-linux-distribution"></a><span data-ttu-id="44d9a-108">Installer une distribution Linux</span><span class="sxs-lookup"><span data-stu-id="44d9a-108">Install a Linux distribution</span></span>

<span data-ttu-id="44d9a-109">Il existe trois façons de télécharger et d’installer vos distributions Linux préférées :</span><span class="sxs-lookup"><span data-stu-id="44d9a-109">There are three ways to download and install your preferred Linux distribution(s):</span></span>

- <span data-ttu-id="44d9a-110">Télécharger et installer à partir du Microsoft Store (voir ci-dessous)</span><span class="sxs-lookup"><span data-stu-id="44d9a-110">Download and install from the Microsoft Store (see below)</span></span>
- [<span data-ttu-id="44d9a-111">Télécharger et installer manuellement à partir de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="44d9a-111">Download and manually install from command line</span></span>](install-manual.md)
- [<span data-ttu-id="44d9a-112">Installation sur Windows Server</span><span class="sxs-lookup"><span data-stu-id="44d9a-112">Install on Windows Server</span></span>](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a><span data-ttu-id="44d9a-113">installer à partir du Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="44d9a-113">Install from the Microsoft Store</span></span>

<span data-ttu-id="44d9a-114">Les distributions Linux peuvent être installées à partir de Microsoft Store sur Windows 10 (build 16215+).</span><span class="sxs-lookup"><span data-stu-id="44d9a-114">Linux distributions can be installed from the Microsoft Store on Windows 10 (Build 16215+).</span></span>

> [!NOTE]
> <span data-ttu-id="44d9a-115">Effectuez ces étapes pour [vérifier votre numéro de build de Windows 10](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="44d9a-115">Follow these steps to [check your Windows 10 build number](troubleshooting.md#check-your-build-number).</span></span>

1. <span data-ttu-id="44d9a-116">Ouvrez le Microsoft Store et choisissez votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="44d9a-116">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    <span data-ttu-id="44d9a-118">Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :</span><span class="sxs-lookup"><span data-stu-id="44d9a-118">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="44d9a-119">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="44d9a-119">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="44d9a-120">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="44d9a-120">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="44d9a-121">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="44d9a-121">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [<span data-ttu-id="44d9a-122">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="44d9a-122">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [<span data-ttu-id="44d9a-123">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="44d9a-123">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [<span data-ttu-id="44d9a-124">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="44d9a-124">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [<span data-ttu-id="44d9a-125">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="44d9a-125">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="44d9a-126">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="44d9a-126">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="44d9a-127">Fedora Remix pour WSL</span><span class="sxs-lookup"><span data-stu-id="44d9a-127">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="44d9a-128">Pengwin</span><span class="sxs-lookup"><span data-stu-id="44d9a-128">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="44d9a-129">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="44d9a-129">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="44d9a-130">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="44d9a-130">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="44d9a-131">Sélectionnez « Obtenir », puis, une fois le téléchargement de la distribution terminé, sélectionnez « Lancer ».</span><span class="sxs-lookup"><span data-stu-id="44d9a-131">Select "Get" and once the distribution has finished downloading, select "Launch".</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="44d9a-133">Effectuer l’initialisation de votre distribution</span><span class="sxs-lookup"><span data-stu-id="44d9a-133">Complete initialization of your distro</span></span>

<span data-ttu-id="44d9a-134">Après avoir lancé votre distribution Linux, suivez les instructions affichées à l’écran pour initialiser votre distribution.</span><span class="sxs-lookup"><span data-stu-id="44d9a-134">After launching your Linux distribution, follow the onscreen instructions to initialize your distro.</span></span>

> [!NOTE]
> <span data-ttu-id="44d9a-135">Pour Windows Server, lancez votre distribution à l’aide de l’exécutable, `<distro>.exe`, dans le dossier d’installation.</span><span class="sxs-lookup"><span data-stu-id="44d9a-135">For Windows Server, launch your distribution using the executable, `<distro>.exe`, in the installation folder.</span></span>

<span data-ttu-id="44d9a-136">Lors de la première exécution d’une distribution nouvellement installée, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux, le temps que l’installation se termine.</span><span class="sxs-lookup"><span data-stu-id="44d9a-136">The first time a newly installed distribution runs, a console window will open and you'll be asked to wait for a minute or two for the installation to complete.</span></span> <span data-ttu-id="44d9a-137">Au cours de cette dernière étape de l’installation, les fichiers de la distribution sont décompressés et stockés sur votre PC, prêts à être utilisés.</span><span class="sxs-lookup"><span data-stu-id="44d9a-137">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="44d9a-138">Cette opération peut prendre environ une minute ou plus en fonction des performances des dispositifs de stockage de votre PC.</span><span class="sxs-lookup"><span data-stu-id="44d9a-138">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="44d9a-139">Cette phase d’installation initiale est requise uniquement lors d’une nouvelle installation d’une distribution : tous les lancements ultérieurs doivent prendre moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="44d9a-139">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="set-up-a-new-linux-user-account"></a><span data-ttu-id="44d9a-140">Configurer un nouveau compte d’utilisateur Linux</span><span class="sxs-lookup"><span data-stu-id="44d9a-140">Set up a new Linux user account</span></span>

<span data-ttu-id="44d9a-141">Une fois l’installation terminée, vous êtes invité à créer un compte d’utilisateur (et son mot de passe).</span><span class="sxs-lookup"><span data-stu-id="44d9a-141">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

<span data-ttu-id="44d9a-143">Ce compte d’utilisateur est destiné à l’utilisateur non-administrateur normal sous lequel vous vous connectez par défaut lors du lancement d’une distribution.</span><span class="sxs-lookup"><span data-stu-id="44d9a-143">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span> <span data-ttu-id="44d9a-144">Vous pouvez choisir le nom d’utilisateur et le mot de passe de votre choix : ils n’ont aucun impact sur votre nom d’utilisateur Windows.</span><span class="sxs-lookup"><span data-stu-id="44d9a-144">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="44d9a-145">Quand vous ouvrez une nouvelle instance de la distribution, vous n’êtes pas invité à entrer votre mot de passe, mais **si vous élevez un processus à l’aide de `sudo`, vous devez l’entrer**. Veillez donc à choisir un mot de passe facile à mémoriser !</span><span class="sxs-lookup"><span data-stu-id="44d9a-145">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="44d9a-146">Pour plus d’informations, consultez la page du [support utilisateur](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="44d9a-146">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-packages"></a><span data-ttu-id="44d9a-147">Mettre à jour et mettre à niveau des packages</span><span class="sxs-lookup"><span data-stu-id="44d9a-147">Update & upgrade packages</span></span>

<span data-ttu-id="44d9a-148">La plupart des distributions sont livrées avec un catalogue de packages vide ou minimal.</span><span class="sxs-lookup"><span data-stu-id="44d9a-148">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="44d9a-149">Nous vous recommandons vivement de mettre à jour régulièrement votre catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution.</span><span class="sxs-lookup"><span data-stu-id="44d9a-149">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="44d9a-150">Pour Debian/Ubuntu, utilisez apt :</span><span class="sxs-lookup"><span data-stu-id="44d9a-150">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="44d9a-151">Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux.</span><span class="sxs-lookup"><span data-stu-id="44d9a-151">Windows does not automatically update or upgrade your Linux distro(s).</span></span> <span data-ttu-id="44d9a-152">Il s’agit d’une tâche que la plupart des utilisateurs Linux préfèrent contrôler eux-mêmes.</span><span class="sxs-lookup"><span data-stu-id="44d9a-152">This is a task that the most Linux users prefer to control themselves.</span></span>

<span data-ttu-id="44d9a-153">Profitez de votre nouvelle distribution Linux sur WSL !</span><span class="sxs-lookup"><span data-stu-id="44d9a-153">Enjoy using your new Linux distro on WSL!</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="44d9a-154">Résolution des problèmes</span><span class="sxs-lookup"><span data-stu-id="44d9a-154">Troubleshooting</span></span>

<span data-ttu-id="44d9a-155">Vous trouverez ci-dessous des erreurs d’installation associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="44d9a-155">Below are related installation errors and suggested fixes.</span></span> <span data-ttu-id="44d9a-156">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="44d9a-156">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

### <a name="installation-failed-with-error-0x8007007e"></a><span data-ttu-id="44d9a-157">Échec de l’installation avec l’erreur 0x8007007e</span><span class="sxs-lookup"><span data-stu-id="44d9a-157">Installation failed with error 0x8007007e</span></span>

<span data-ttu-id="44d9a-158">Cette erreur se produit quand votre système ne prend pas en charge Linux à partir du Store.</span><span class="sxs-lookup"><span data-stu-id="44d9a-158">This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="44d9a-159">Vérifiez que :</span><span class="sxs-lookup"><span data-stu-id="44d9a-159">Make sure that:</span></span>

- <span data-ttu-id="44d9a-160">Vous exécutez la build Windows 16215 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="44d9a-160">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="44d9a-161">[Vérifiez votre build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="44d9a-161">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
- <span data-ttu-id="44d9a-162">Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.</span><span class="sxs-lookup"><span data-stu-id="44d9a-162">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="44d9a-163">[Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="44d9a-163">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>

### <a name="installation-failed-with-error-0x80070003"></a><span data-ttu-id="44d9a-164">Échec de l’installation avec l’erreur 0x80070003</span><span class="sxs-lookup"><span data-stu-id="44d9a-164">Installation failed with error 0x80070003</span></span>

<span data-ttu-id="44d9a-165">Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`).</span><span class="sxs-lookup"><span data-stu-id="44d9a-165">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="44d9a-166">Vérifiez que les distributions sont stockées sur votre lecteur système :</span><span class="sxs-lookup"><span data-stu-id="44d9a-166">Make sure that distros are stored on your system drive:</span></span>

- <span data-ttu-id="44d9a-167">Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Changer l’emplacement d’enregistrement du nouveau contenu**</span><span class="sxs-lookup"><span data-stu-id="44d9a-167">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**</span></span>
  
    ![Image des paramètres système pour installer des applications sur le lecteur C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a><span data-ttu-id="44d9a-169">Échec de WslRegisterDistribution avec l’erreur 0x8007019e</span><span class="sxs-lookup"><span data-stu-id="44d9a-169">WslRegisterDistribution failed with error 0x8007019e</span></span>

<span data-ttu-id="44d9a-170">Le composant facultatif Sous-système Windows pour Linux n’est pas activé :</span><span class="sxs-lookup"><span data-stu-id="44d9a-170">The Windows Subsystem for Linux optional component is not enabled:</span></span>

- <span data-ttu-id="44d9a-171">Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="44d9a-171">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
