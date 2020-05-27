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
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guide d’installation du sous-système Windows pour Linux pour Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Installer le sous-système Windows pour Linux

Avant d’installer des distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux ».

Ouvrez PowerShell en tant qu’administrateur et exécutez :

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Pour installer WSL 1 uniquement, vous devez redémarrer votre ordinateur maintenant et ensuite passer à [Installer la distribution Linux de votre choix](./install-win10.md#install-your-linux-distribution-of-choice). Sinon, attendez pour redémarrer et passez à la mise à jour vers WSL 2. Apprenez-en davantage sur la [comparaison entre WSL 2 et WSL 1](./compare-versions.md).

## <a name="update-to-wsl-2"></a>Mettre à jour vers WSL 2

Pour effectuer une mise à jour vers WSL 2, vous devez respecter les critères suivants :

- Exécution de Windows 10, [mis à jour vers la version 2004](ms-settings:windowsupdate), **build 19041** ou ultérieure.

> [!IMPORTANT]
> Actuellement, pour effectuer une mise à jour vers Windows 10, version 2004 (build 19041), vous devez [rejoindre le programme Windows Insider](https://insider.windows.com/insidersigninboth/) et sélectionner l’anneau « Release Preview ». La version publique devrait arriver d’ici fin mai.

- Vérifiez votre version de Windows en sélectionnant la **touche Windows + R**, tapez **winver** et sélectionnez **OK**. (Ou entrez la commande `ver` dans l’invite de commandes Windows). Effectuez la [mise à jour vers la dernière version de Windows](ms-settings:windowsupdate) si votre build est antérieure à la build 19041. [Procurez-vous l’Assistant Windows Update](https://www.microsoft.com/software-download/windows10).

### <a name="enable-the-virtual-machine-platform-optional-component"></a>Activer le composant facultatif « Plateforme de machine virtuelle »

Avant d’installer WSL 2, vous devez activer la fonctionnalité facultative « Plateforme de machine virtuelle ».

Ouvrez PowerShell en tant qu’administrateur et exécutez :

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Redémarrez** votre ordinateur pour terminer l’installation de WSL et mettre à jour vers WSL 2.

### <a name="set-wsl-2-as-your-default-version"></a>Définir WSL 2 comme version par défaut

Exécutez la commande suivante dans PowerShell pour définir WSL 2 comme version par défaut lors de l’installation d’une nouvelle distribution Linux :

```powershell
wsl --set-default-version 2
```

## <a name="install-your-linux-distribution-of-choice"></a>Installer la distribution Linux de votre choix

1. Ouvrez le [Microsoft Store](https://aka.ms/wslstore) et sélectionnez votre distribution Linux préférée.

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [openSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix pour WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. Dans la page de la distribution, sélectionnez « Obtenir ».

    ![Distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a>Configurer une nouvelle distribution

La première fois que vous lancez une distribution Linux nouvellement installée, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux pour que les fichiers soient décompressés et stockés sur votre PC. Tous les lancements ultérieurs doivent prendre moins d’une seconde.

Vous devez ensuite [créer un compte d’utilisateur et un mot de passe pour votre nouvelle distribution Linux](./user-support.md).

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Définir votre version de distribution sur WSL 1 ou WSL 2

Vous pouvez vérifier la version WSL affectée à chacune des distributions Linux que vous avez installées en ouvrant la ligne de commande PowerShell et en entrant la commande (disponible uniquement dans la [build Windows 19041 ou ultérieure](ms-settings:windowsupdate)) : `wsl -l -v`

```bash
wsl --list --verbose
```

Pour définir une distribution devant reposer sur l’une ou l’autre des versions WSL, exécutez :

```bash
wsl --set-version <distribution name> <versionNumber>
```

Veillez à remplacer `<distribution name>` par le vrai nom de votre distribution et `<versionNumber>` par le chiffre « 1 » ou « 2 ». Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».

Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :

```bash
wsl --set-default-version 2
```

Cela permet de définir la version de toute nouvelle distribution installée sur WSL 2.

## <a name="troubleshooting-installation"></a>Résolution des problèmes liés à l’installation

Vous trouverez ci-dessous des erreurs associées et des suggestions de correction. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.

- **Échec de l’installation avec l’erreur 0x80070003**
  - Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`). Vérifiez que les distributions sont stockées sur votre lecteur système :  
  - Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Modifier l’emplacement d’enregistrement du nouveau contenu**
    ![Image des paramètres système pour installer les applications sur le lecteur C:](media/AppStorage.png)

- **Échec de WslRegisterDistribution avec l’erreur 0x8007019e**
  - Le composant facultatif Sous-système Windows pour Linux n’est pas activé :
  - Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.

- **Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**
  - Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur. Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.

- **Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**
  - Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez la version de build 19041 ou ultérieure de Windows. Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).

- **Impossible de terminer l’opération demandée du fait d’une limitation du système de disque virtuel. Les fichiers de disque dur virtuel doivent être décompressés et déchiffrés, mais ne doivent pas être partiellement alloués.**
  - Vérifiez le [thread GitHub WSL n° 4103](https://github.com/microsoft/WSL/issues/4103) où ce problème est suivi pour obtenir des informations mises à jour.

- **Le terme « wsl » n’est pas reconnu comme nom d’applet de commande, fonction, fichier de script ou programme exécutable.**
  - Assurez-vous que le [composant facultatif Sous-système Windows pour Linux est installé](./install-win10.md#enable-the-virtual-machine-platform-optional-component). De plus, si vous utilisez un appareil Arm64 et exécutez cette commande à partir de PowerShell, vous recevrez cette erreur. Au lieu de cela, exécutez `wsl.exe` à partir de [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou d’une invite de commandes.
