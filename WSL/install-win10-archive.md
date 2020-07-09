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
# <a name="archived-instructions"></a>Instructions archivées

Le guide suivant vous accompagne tout au long des étapes d’installation du sous-système Windows pour Linux (WSL) sur un ordinateur exécutant Windows 10.

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Activer la fonctionnalité facultative Sous-système Windows pour Linux

Avant d’installer une distribution Linux, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » sur Windows 10 :

1. Ouvrez PowerShell en tant qu’administrateur, puis entrez le script suivant :

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. Redémarrez votre ordinateur lorsque vous y êtes invité.

## <a name="install-a-linux-distribution"></a>Installer une distribution Linux

Il existe trois façons de télécharger et d’installer vos distributions Linux préférées :

- Télécharger et installer à partir du Microsoft Store (voir ci-dessous)
- [Télécharger et installer manuellement à partir de la ligne de commande](install-manual.md)
- [Installation sur Windows Server](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a>installer à partir du Microsoft Store

Les distributions Linux peuvent être installées à partir de Microsoft Store sur Windows 10 (build 16215+).

> [!NOTE]
> Effectuez ces étapes pour [vérifier votre numéro de build de Windows 10](troubleshooting.md#check-your-build-number).

1. Ouvrez le Microsoft Store et choisissez votre distribution Linux préférée.

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix pour WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Sélectionnez « Obtenir », puis, une fois le téléchargement de la distribution terminé, sélectionnez « Lancer ».

    ![Vue des distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Effectuer l’initialisation de votre distribution

Après avoir lancé votre distribution Linux, suivez les instructions affichées à l’écran pour initialiser votre distribution.

> [!NOTE]
> Pour Windows Server, lancez votre distribution à l’aide de l’exécutable, `<distro>.exe`, dans le dossier d’installation.

Lors de la première exécution d’une distribution nouvellement installée, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux, le temps que l’installation se termine. Au cours de cette dernière étape de l’installation, les fichiers de la distribution sont décompressés et stockés sur votre PC, prêts à être utilisés. Cette opération peut prendre environ une minute ou plus en fonction des performances des dispositifs de stockage de votre PC. Cette phase d’installation initiale est requise uniquement lors d’une nouvelle installation d’une distribution : tous les lancements ultérieurs doivent prendre moins d’une seconde.

## <a name="set-up-a-new-linux-user-account"></a>Configurer un nouveau compte d’utilisateur Linux

Une fois l’installation terminée, vous êtes invité à créer un compte d’utilisateur (et son mot de passe).

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

Ce compte d’utilisateur est destiné à l’utilisateur non-administrateur normal sous lequel vous vous connectez par défaut lors du lancement d’une distribution. Vous pouvez choisir le nom d’utilisateur et le mot de passe de votre choix : ils n’ont aucun impact sur votre nom d’utilisateur Windows.

Quand vous ouvrez une nouvelle instance de la distribution, vous n’êtes pas invité à entrer votre mot de passe, mais **si vous élevez un processus à l’aide de `sudo`, vous devez l’entrer**. Veillez donc à choisir un mot de passe facile à mémoriser ! Pour plus d’informations, consultez la page du [support utilisateur](user-support.md).

## <a name="update--upgrade-packages"></a>Mettre à jour et mettre à niveau des packages

La plupart des distributions sont livrées avec un catalogue de packages vide ou minimal. Nous vous recommandons vivement de mettre à jour régulièrement votre catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution. Pour Debian/Ubuntu, utilisez apt :

```bash
sudo apt update && sudo apt upgrade
```

Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux. Il s’agit d’une tâche que la plupart des utilisateurs Linux préfèrent contrôler eux-mêmes.

Profitez de votre nouvelle distribution Linux sur WSL !

## <a name="troubleshooting"></a>Résolution des problèmes

Vous trouverez ci-dessous des erreurs d’installation associées et des suggestions de correction. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.

### <a name="installation-failed-with-error-0x8007007e"></a>Échec de l’installation avec l’erreur 0x8007007e

Cette erreur se produit quand votre système ne prend pas en charge Linux à partir du Store.  Vérifiez que :

- Vous exécutez la build Windows 16215 ou ultérieure. [Vérifiez votre build](troubleshooting.md#check-your-build-number).
- Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.  [Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).

### <a name="installation-failed-with-error-0x80070003"></a>Échec de l’installation avec l’erreur 0x80070003

Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`). Vérifiez que les distributions sont stockées sur votre lecteur système :

- Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Changer l’emplacement d’enregistrement du nouveau contenu**
  
    ![Image des paramètres système pour installer des applications sur le lecteur C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>Échec de WslRegisterDistribution avec l’erreur 0x8007019e

Le composant facultatif Sous-système Windows pour Linux n’est pas activé :

- Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.
