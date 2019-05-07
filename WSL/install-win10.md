---
title: Installer le sous-système de Windows pour Linux (WSL) sur Windows 10
description: Instructions d’installation pour le sous-système Windows pour Linux sur Windows 10.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, installer
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063287"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Sous-système Windows pour le Guide d’Installation de Linux pour Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Installer le sous-système Windows pour Linux

Avant d’installer toutes les distributions Linux pour WSL, vous devez vous assurer que les « Windows sous-système pour Linux » fonctionnalité facultative est activée :

1. Ouvrez PowerShell en tant qu’administrateur et exécutez :
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Redémarrez votre ordinateur lorsque vous y êtes invité.

## <a name="install-your-linux-distribution-of-choice"></a>Installer votre Distribution Linux de choix
Pour télécharger et installer votre distro(s) préférée, vous avez trois possibilités :
1. Téléchargez et installez depuis le Store de Windows (voir ci-dessous)
1. Télécharger et installer à partir de la commande-ligne ou des scripts ([Lisez les instructions d’installation manuelle](install-manual.md))
1. Télécharger et décompresser et installer manuellement (pour Windows Server - [instructions fournies ici](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update et versions ultérieures : Installer à partir du Microsoft Store

> Cette section concerne Windows build 16215 ou version ultérieure.  Suivez ces étapes pour [vérifier votre build](troubleshooting.md#check-your-build-number). 

1. Le Microsoft Store et votre distribution Linux favorite.

    ![Affichage des distributions de Linux dans le magasin Windows](media/store.png)

    Les liens suivants seront ouvre à la page magasin de Windows pour chaque distribution :

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. À partir de la page de la distribution, sélectionnez « Get »

    ![Affichage des distributions de Linux dans le magasin Windows](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Termine l’initialisation de votre distribution
Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distributeur](initialize-distro.md) une fois, avant de pouvoir être utilisé.

## <a name="troubleshooting"></a>Dépannage : 

Voici les erreurs associées et des suggestions de correction. Reportez-vous à la [page Résolution des problèmes de WSL](troubleshooting.md) pour les autres erreurs courantes et leurs solutions.

* **Installation a échoué avec l’erreur 0 x 80070003**
    * Le sous-système Windows pour Linux s’exécute uniquement sur votre lecteur système (il s’agit généralement votre `C:` lecteur). Assurez-vous que les distributions sont stockées sur votre lecteur système :  
    * Ouvrez **paramètres** -> **stockage** -> **davantage de paramètres de stockage : Modification dans lequel le nouveau contenu est enregistré**
    ![image des paramètres système pour installer des applications sur le lecteur C:](media/AppStorage.png)
