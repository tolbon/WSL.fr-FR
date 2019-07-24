---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Windows Server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308791"
---
# <a name="windows-server-installation-guide"></a>Guide d’installation de Windows Server

> S’applique à Windows Server 2019 et versions ultérieures

Chez//Build2017, Microsoft a annoncé que le sous-système Windows pour Linux sera [disponible sur Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Ces instructions vous guident tout au long de l’exécution du sous-système Windows pour Linux sur Windows Server 1709 et versions ultérieures.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Activer le sous-système Windows pour Linux (WSL)

Avant de pouvoir exécuter Linux distributions sur Windows, vous devez activer la fonctionnalité facultative «sous-système Windows pour Linux» et redémarrer.

1. Ouvrez PowerShell en tant qu’administrateur et exécutez:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Redémarrez votre ordinateur lorsque vous y êtes invité. **Ce redémarrage est nécessaire** pour garantir que WSL peut lancer un environnement d’exécution approuvé.

## <a name="download-a-linux-distro"></a>Télécharger un distribution Linux

Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.

## <a name="extract-and-install-a-linux-distro"></a>Extraire et installer un distribution Linux
Maintenant que vous avez téléchargé un distribution, extrayez son contenu et installez manuellement le distribution:

1. Extrayez le `<distro>.appx` contenu du package, par exemple à l’aide de PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. Exécutez le lanceur distribution pour terminer l’installation, exécutez l’application distribution Launcher dans le dossier cible `<distro>.exe`, nommé. Par exemple: `ubuntu.exe`, etc.

    ![Ubuntu distribution développé sur Windows Server](media/server-appx-expand.png)

    > **Dépannage**
    > * **Échec de l’installation avec l’erreur 0x8007007e**: Cette erreur se produit lorsque votre système ne prend pas en charge WSL. Vérifiez que :
    >   * Vous exécutez Windows Build 16215 ou version ultérieure. [Vérifiez votre Build](troubleshooting.md#check-your-build-number).
    >   * Le composant facultatif sous-système Windows pour Linux est activé et l’ordinateur a redémarré.  Vérifiez [que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Ajoutez votre chemin distribution au chemin d’accès de l'`C:\Users\Administrator\Ubuntu` environnement Windows (dans cet exemple), par exemple, à l’aide de PowerShell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Vous pouvez maintenant lancer votre distribution à partir de n’importe `<distro>.exe`quel chemin d’accès en tapant. Par exemple : `ubuntu.exe`

Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distribution avant d'](initialize-distro.md) utiliser votre distribution.
