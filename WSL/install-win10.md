---
title: Installer le sous-système Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation du sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "74200232"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guide d’installation du sous-système Windows pour Linux pour Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Installer le sous-système Windows pour Linux

Avant d’installer des distributions Linux pour WSL, vous devez vous assurer que la fonctionnalité facultative « Sous-système Windows pour Linux » est activée :

1. Ouvrez PowerShell en tant qu’administrateur et exécutez :
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Redémarrez votre ordinateur lorsque vous y êtes invité.

## <a name="install-your-linux-distribution-of-choice"></a>Installer la distribution Linux de votre choix
Pour télécharger et installer vos distributions préférées, vous avez trois possibilités :
* Télécharger et installer à partir du Microsoft Store (voir ci-dessous)
* Télécharger et installer à partir de la ligne de commande/du script ([lisez les instructions d’installation manuelle](install-manual.md))
* Télécharger, décompresser manuellement et installer (pour Windows Server [instructions ici](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update et ultérieur : installer à partir du Microsoft Store

> Cette section concerne la build Windows 16215 ou ultérieure.  Procédez comme suit pour [vérifier votre build](troubleshooting.md#check-your-build-number). 

1. Ouvrez le Microsoft Store et choisissez votre distribution Linux préférée.

    ![Vue des distributions Linux dans le Microsoft Store](media/store.png)

    Les liens suivants ouvrent la page Microsoft Store pour chaque distribution :

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix pour WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Dans la page de la distribution, sélectionnez « Obtenir »

    ![Vue des distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Effectuer l’initialisation de votre distribution
Maintenant que votre distribution Linux est installée, vous devez [initialiser la nouvelle instance de distribution](initialize-distro.md) une fois avant de pouvoir l’utiliser.

## <a name="troubleshooting"></a>Dépannage : 

Vous trouverez ci-dessous des erreurs associées et des suggestions de correction. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.

* **Échec de l’installation avec l’erreur 0x80070003**
    * Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général, il s’agit de votre lecteur `C:`). Vérifiez que les distributions sont stockées sur votre lecteur système :  
    * Ouvrez **Paramètres** -> **Stockage** -> **Autres paramètres de stockage : Modifier l’emplacement d’enregistrement du nouveau contenu**
    ![Image des paramètres système pour installer les applications sur le lecteur C:](media/AppStorage.png)
    
    
 * **Échec de WslRegisterDistribution avec l’erreur 0x8007019e**   
  * Le composant facultatif Sous-système Windows pour Linux n’est pas activé : 
   * Ouvrez **Panneau de configuration** -> **Programmes et fonctionnalités** -> **Activer ou désactiver des fonctionnalités Windows** -> Cochez **Sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.
