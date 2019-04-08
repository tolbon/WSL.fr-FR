---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation pour le sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063617"
---
# <a name="windows-server-installation-guide"></a>Guide d’Installation de Windows Server

> S’applique à Windows Server 2019 et versions ultérieures

À / / Build2017, Microsoft a annoncé que le sous-système Windows pour Linux seront [disponible sur Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).  Ces instructions guident en cours d’exécution le sous-système Windows pour Linux sur Windows Server 1709 et versions ultérieures.

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>Activer le sous-système Windows pour Linux (WSL)

Avant de pouvoir exécuter des distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » et redémarrez.

1. Ouvrez PowerShell en tant qu’administrateur et exécutez :
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. Redémarrez votre ordinateur lorsque vous y êtes invité. **Ce redémarrage est nécessaire** afin de garantir que les WSL peut lancer un environnement d’exécution approuvé.

## <a name="download-a-linux-distro"></a>Télécharger une distribution Linux

Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux favorite.

## <a name="extract-and-install-a-linux-distro"></a>Extraire et d’installer une distribution Linux
Maintenant que vous avez téléchargé un distributeur, extrayez son contenu et installer manuellement la distribution :

1. Extraire le `<distro>.appx` contenu du package, par exemple, à l’aide de PowerShell :

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. Exécuter le Lanceur distributeur pour terminer l’installation, exécutez l’application de lancement de distribution dans le dossier cible, nommé `<distro>.exe`. Par exemple : `ubuntu.exe`, etc.

    ![Développé distribution Ubuntu sur Windows Server](media/server-appx-expand.png)

    > **Résolution des problèmes**
    > * **Échec de l’installation avec l’erreur 0x8007007e**: Cette erreur se produit lorsque votre système ne prend pas en charge WSL. Vérifiez que :
    >   * Vous exécutez Windows build 16215 ou version ultérieure. [Vérifier votre build](troubleshooting.md#check-your-build-number).
    >   * Le sous-système Windows pour le composant facultatif de Linux est activé et que l’ordinateur a redémarré.  [Assurez-vous que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).
    
3. Ajouter votre chemin d’accès de la distribution à l’environnement Windows PATH (`C:\Users\Administrator\Ubuntu` dans cet exemple), par exemple, à l’aide de Powershell :
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    Vous pouvez maintenant lancer votre distribution à partir de n’importe quel chemin d’accès en tapant `<distro>.exe`. Exemple : `ubuntu.exe`

Maintenant que votre distribution Linux est installée, vous devez [initialiser votre nouvelle instance de distributeur](initialize-distro.md) avant d’utiliser votre distribution.
