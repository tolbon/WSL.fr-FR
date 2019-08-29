---
title: Installer le sous-système Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation du sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, installation
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122776"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Guide d’installation du sous-système Windows pour Linux pour Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Installer le sous-système Windows pour Linux

Avant d’installer un distributions Linux pour WSL, vous devez vous assurer que la fonctionnalité facultative «sous-système Windows pour Linux» est activée:

1. Ouvrez PowerShell en tant qu’administrateur et exécutez:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Redémarrez votre ordinateur lorsque vous y êtes invité.

## <a name="install-your-linux-distribution-of-choice"></a>Installer votre distribution Linux de votre choix
Pour télécharger et installer vos distribution préférés, vous avez trois possibilités:
1. Téléchargez et installez à partir de la Microsoft Store (voir ci-dessous)
1. Téléchargez et installez à partir de la ligne de commande/du script ([Lisez les instructions d’installation manuelle](install-manual.md))
1. Télécharger et décompresser et installer manuellement (pour Windows Server- [instructions ici](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 automne Creators Update et versions ultérieures: Installer à partir du Microsoft Store

> Cette section est destinée à Windows Build 16215 ou version ultérieure.  Procédez comme suit pour [vérifier votre Build](troubleshooting.md#check-your-build-number). 

1. Ouvrez la Microsoft Store et choisissez votre distribution Linux préférée.

    ![Affichage des distributions Linux dans le Microsoft Store](media/store.png)

    Les liens suivants ouvrent la page Microsoft Store pour chaque distribution:

    * [Ubuntu 16,04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18,04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE LEAP 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE LEAP 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix pour WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [WSL Alpine](https://www.microsoft.com/store/apps/9p804crf0395)

1. À partir de la page de distribution, sélectionnez «récupérer».

    ![Affichage des distributions Linux dans le Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Initialisation complète de votre distribution
Maintenant que votre distribution Linux est installée, vous devez [initialiser la nouvelle instance de distribution](initialize-distro.md) avant de pouvoir l’utiliser.

## <a name="troubleshooting"></a>Résolution des problèmes : 

Vous trouverez ci-dessous des erreurs connexes et des corrections suggérées. Reportez-vous à la [page de dépannage WSL](troubleshooting.md) pour d’autres erreurs courantes et leurs solutions.

* **Échec de l’installation avec l’erreur 0x80070003**
    * Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (en général `C:` , il s’agit de votre lecteur). Assurez-vous que les distributions sont stockés sur votre lecteur système:  
    * Ouvrir les **paramètres** -> **stockage** -> plusde**paramètres de stockage: Modifier l’emplacement où le nouveau**contenu est enregistré
    ![image des paramètres système pour installer les applications sur le lecteur C:](media/AppStorage.png)
    
    
 * **Échec de WslRegisterDistribution avec l’erreur 0x8007019e**   
  * Le composant facultatif sous-système Windows pour Linux n’est pas activé: 
   * Ouvrez **le panneau de configuration** -> **programmes et fonctionnalités** -> **activer ou désactiver** les fonctionnalités Windows > Vérifiez le **sous-système Windows pour Linux** ou utilisez l’applet de commande PowerShell mentionnée au début de cet article.
