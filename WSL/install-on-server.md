---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256392"
---
# <a name="windows-server-installation-guide"></a>Guide d’installation sur Windows Server

> S’applique à Windows Server 2019 et ultérieur

Avec la build 2017, Microsoft a annoncé que le sous-système Windows pour Linux sera [disponible sur Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Ces instructions vous guident tout au long de l’exécution du sous-système Windows pour Linux sur Windows Server 1709 et ultérieur.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Activer le sous-système Windows pour Linux (WSL)

Avant de pouvoir exécuter les distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » et redémarrer.

1. Ouvrez PowerShell en tant qu’administrateur et exécutez :
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Redémarrez votre ordinateur lorsque vous y êtes invité. **Ce redémarrage est nécessaire** pour s’assurer que WSL peut lancer un environnement d’exécution approuvé.

## <a name="download-a-linux-distro"></a>Télécharger une distribution Linux

Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.

## <a name="extract-and-install-a-linux-distro"></a>Extraire et installer une distribution Linux
Maintenant que vous avez téléchargé une distribution, extrayez son contenu et installez manuellement la distribution :

1. Extrayez le contenu du package `<distro>.appx`, par exemple à l’aide de PowerShell :

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Exécutez le lanceur de distribution. Pour réaliser l’installation, exécutez l’application de lancement de distribution dans le dossier cible, nommé `<distro>.exe`. Par exemple : `ubuntu.exe`, etc.

    ![Distribution Ubuntu développée sur Windows Server](media/server-appx-expand.png)

    > **Résolution des problèmes**
    > * **Échec de l’installation avec l’erreur 0x8007007e** : Cette erreur se produit lorsque votre système ne prend pas en charge WSL. Vérifiez que :
    >   * Vous exécutez la build Windows 16215 ou ultérieure. [Vérifiez votre build](troubleshooting.md#check-your-build-number).
    >   * Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.  [Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Ajoutez votre chemin de distribution au chemin d’environnement Windows (`C:\Users\Administrator\Ubuntu` dans cet exemple), par exemple, à l’aide de PowerShell :
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    Vous pouvez maintenant lancer votre distribution à partir de n’importe quel chemin en tapant `<distro>.exe`. Par exemple : `ubuntu.exe`

Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distribution](initialize-distro.md) avant d’utiliser votre distribution.
