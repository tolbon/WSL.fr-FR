---
title: Installer le sous-système Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation du sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installer, activer, WSL2, version 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: acb83234a90dc5e65c98518b869f29c4ecf973d8
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343911"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="749d7-104">Guide d’installation du sous-système Windows pour Linux pour Windows 10</span><span class="sxs-lookup"><span data-stu-id="749d7-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="749d7-105">Installer le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="749d7-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="749d7-106">Avant d’installer des distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux ».</span><span class="sxs-lookup"><span data-stu-id="749d7-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="749d7-107">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="749d7-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="749d7-108">Pour installer uniquement WSL 1, vous devez maintenant redémarrer votre ordinateur et passer à [Installer la distribution Linux de votre choix](./install-win10.md#install-your-linux-distribution-of-choice). Sinon, attendez de redémarrer et passez à la mise à jour vers WSL 2.</span><span class="sxs-lookup"><span data-stu-id="749d7-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="749d7-109">Découvrez plus en détail la [comparaison entre WSL 2 et WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="749d7-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="749d7-110">Mettre à jour vers WSL 2</span><span class="sxs-lookup"><span data-stu-id="749d7-110">Update to WSL 2</span></span>

<span data-ttu-id="749d7-111">Pour effectuer une mise à jour vers WSL 2, vous devez respecter les critères suivants :</span><span class="sxs-lookup"><span data-stu-id="749d7-111">To update to WSL 2, you must meet the follow criteria:</span></span>

- <span data-ttu-id="749d7-112">Exécution de Windows 10, [mis à jour vers la version 2004](ms-settings:windowsupdate), **build 19041** ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="749d7-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="749d7-113">Actuellement, pour effectuer une mise à jour vers Windows 10, version 2004 (build 19041), vous devez [rejoindre le programme Windows Insider](https://insider.windows.com/insidersigninboth/) et sélectionner l’anneau « Release Preview ».</span><span class="sxs-lookup"><span data-stu-id="749d7-113">Currently to update to Windows 10, version 2004 (Build 19041), you will need to [join the Windows Insider program](https://insider.windows.com/insidersigninboth/) and select the "Release Preview" ring.</span></span> <span data-ttu-id="749d7-114">La version publique devrait arriver d’ici fin mai.</span><span class="sxs-lookup"><span data-stu-id="749d7-114">The public release should arrive by late May.</span></span>

- <span data-ttu-id="749d7-115">Vérifiez votre version de Windows en sélectionnant la **touche Windows + R**, tapez **winver** et sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="749d7-115">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="749d7-116">(Ou entrez la commande `ver` dans l’invite de commandes Windows).</span><span class="sxs-lookup"><span data-stu-id="749d7-116">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="749d7-117">Effectuez la [mise à jour vers la dernière version de Windows](ms-settings:windowsupdate) si votre build est antérieure à la build 19041.</span><span class="sxs-lookup"><span data-stu-id="749d7-117">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="749d7-118">[Procurez-vous l’Assistant Windows Update](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="749d7-118">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="749d7-119">Activer le composant facultatif « Plateforme de machine virtuelle »</span><span class="sxs-lookup"><span data-stu-id="749d7-119">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="749d7-120">Avant d’installer WSL 2, vous devez activer la fonctionnalité facultative « Plateforme de machine virtuelle ».</span><span class="sxs-lookup"><span data-stu-id="749d7-120">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="749d7-121">Ouvrez PowerShell en tant qu’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="749d7-121">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="749d7-122">**Redémarrez** votre ordinateur pour terminer l’installation de WSL et mettre à jour vers WSL 2.</span><span class="sxs-lookup"><span data-stu-id="749d7-122">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="749d7-123">Définir WSL 2 comme version par défaut</span><span class="sxs-lookup"><span data-stu-id="749d7-123">Set WSL 2 as your default version</span></span>

<span data-ttu-id="749d7-124">Exécutez la commande suivante dans PowerShell pour définir WSL 2 comme version par défaut lors de l’installation d’une nouvelle distribution Linux :</span><span class="sxs-lookup"><span data-stu-id="749d7-124">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="749d7-125">Installer la distribution Linux de votre choix</span><span class="sxs-lookup"><span data-stu-id="749d7-125">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="749d7-126">Ouvrez le [Microsoft Store](https://aka.ms/wslstore) et sélectionnez votre distribution Linux préférée.</span><span class="sxs-lookup"><span data-stu-id="749d7-126">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    <span data-ttu-id="749d7-128">Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :</span><span class="sxs-lookup"><span data-stu-id="749d7-128">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="749d7-129">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="749d7-129">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="749d7-130">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="749d7-130">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="749d7-131">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="749d7-131">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="749d7-132">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="749d7-132">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="749d7-133">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="749d7-133">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="749d7-134">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="749d7-134">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="749d7-135">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="749d7-135">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="749d7-136">Fedora Remix pour WSL</span><span class="sxs-lookup"><span data-stu-id="749d7-136">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="749d7-137">Pengwin</span><span class="sxs-lookup"><span data-stu-id="749d7-137">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="749d7-138">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="749d7-138">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="749d7-139">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="749d7-139">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="749d7-140">Dans la page de la distribution, sélectionnez « Obtenir ».</span><span class="sxs-lookup"><span data-stu-id="749d7-140">From the distribution's page, select "Get".</span></span>

    ![Distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="749d7-142">Configurer une nouvelle distribution</span><span class="sxs-lookup"><span data-stu-id="749d7-142">Set up a new distribution</span></span>

<span data-ttu-id="749d7-143">La première fois que vous lancez une distribution Linux nouvellement installée, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux pour que les fichiers soient décompressés et stockés sur votre PC.</span><span class="sxs-lookup"><span data-stu-id="749d7-143">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="749d7-144">Tous les lancements ultérieurs doivent prendre moins d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="749d7-144">All future launches should take less than a second.</span></span>

<span data-ttu-id="749d7-145">Vous devez ensuite [créer un compte d’utilisateur et un mot de passe pour votre nouvelle distribution Linux](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="749d7-145">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="749d7-147">Définir votre version de distribution sur WSL 1 ou WSL 2</span><span class="sxs-lookup"><span data-stu-id="749d7-147">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="749d7-148">Vous pouvez vérifier la version WSL affectée à chacune des distributions Linux que vous avez installées en ouvrant la ligne de commande PowerShell et en entrant la commande (disponible uniquement dans la [build Windows 19041 ou ultérieure](ms-settings:windowsupdate)) : `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="749d7-148">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```bash
wsl --list --verbose
```

<span data-ttu-id="749d7-149">Pour définir une distribution devant reposer sur l’une ou l’autre des versions WSL, exécutez :</span><span class="sxs-lookup"><span data-stu-id="749d7-149">To set a distribution to be backed by either version of WSL please run:</span></span>

```bash
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="749d7-150">Veillez à remplacer `<distribution name>` par le vrai nom de votre distribution et `<versionNumber>` par le chiffre « 1 » ou « 2 ».</span><span class="sxs-lookup"><span data-stu-id="749d7-150">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="749d7-151">Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».</span><span class="sxs-lookup"><span data-stu-id="749d7-151">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="749d7-152">Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :</span><span class="sxs-lookup"><span data-stu-id="749d7-152">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```bash
wsl --set-default-version 2
```

<span data-ttu-id="749d7-153">Cela permet de définir la version de toute nouvelle distribution installée sur WSL 2.</span><span class="sxs-lookup"><span data-stu-id="749d7-153">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="749d7-154">Résolution des problèmes liés à l’installation</span><span class="sxs-lookup"><span data-stu-id="749d7-154">Troubleshooting installation</span></span>

<span data-ttu-id="749d7-155">Vous trouverez ci-dessous des erreurs associées et des suggestions de correction.</span><span class="sxs-lookup"><span data-stu-id="749d7-155">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="749d7-156">Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.</span><span class="sxs-lookup"><span data-stu-id="749d7-156">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="749d7-157">**Échec de l’installation avec l’erreur 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="749d7-157">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="749d7-158">Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`).</span><span class="sxs-lookup"><span data-stu-id="749d7-158">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="749d7-159">Vérifiez que les distributions sont stockées sur votre lecteur système :</span><span class="sxs-lookup"><span data-stu-id="749d7-159">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="749d7-160">Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Modifier l’emplacement d’enregistrement du nouveau contenu**
    ![Image des paramètres système pour installer les applications sur le lecteur C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="749d7-160">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="749d7-161">**Échec de WslRegisterDistribution avec l’erreur 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="749d7-161">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="749d7-162">Le composant facultatif Sous-système Windows pour Linux n’est pas activé :</span><span class="sxs-lookup"><span data-stu-id="749d7-162">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="749d7-163">Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.</span><span class="sxs-lookup"><span data-stu-id="749d7-163">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>

- <span data-ttu-id="749d7-164">**Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="749d7-164">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="749d7-165">Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="749d7-165">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="749d7-166">Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.</span><span class="sxs-lookup"><span data-stu-id="749d7-166">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="749d7-167">**Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="749d7-167">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="749d7-168">Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez la version de build 19041 ou ultérieure de Windows.</span><span class="sxs-lookup"><span data-stu-id="749d7-168">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="749d7-169">Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="749d7-169">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="749d7-170">Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="749d7-170">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="749d7-171">**Impossible de terminer l’opération demandée du fait d’une limitation du système de disque virtuel. Les fichiers de disque dur virtuel doivent être décompressés et déchiffrés, mais ne doivent pas être partiellement alloués.**</span><span class="sxs-lookup"><span data-stu-id="749d7-171">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="749d7-172">Vérifiez le [thread GitHub WSL n° 4103](https://github.com/microsoft/WSL/issues/4103) où ce problème est suivi pour obtenir des informations mises à jour.</span><span class="sxs-lookup"><span data-stu-id="749d7-172">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="749d7-173">**Le terme « wsl » n’est pas reconnu comme nom d’applet de commande, fonction, fichier de script ou programme exécutable.**</span><span class="sxs-lookup"><span data-stu-id="749d7-173">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="749d7-174">Assurez-vous que le [composant facultatif Sous-système Windows pour Linux est installé](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="749d7-174">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="749d7-175">De plus, si vous utilisez un appareil Arm64 et exécutez cette commande à partir de PowerShell, vous recevrez cette erreur.</span><span class="sxs-lookup"><span data-stu-id="749d7-175">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="749d7-176">Au lieu de cela, exécutez `wsl.exe` à partir de [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou d’une invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="749d7-176">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
