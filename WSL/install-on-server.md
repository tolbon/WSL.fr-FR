---
title: Installer le sous-système Linux sur Windows Server
description: Instructions d’installation du sous-système Linux sur Windows Server.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671019"
---
# <a name="windows-server-installation-guide"></a>Guide d’installation sur Windows Server

Le sous-système Windows pour Linux peut être installé sur Windows Server 2019 (version 1709) et ultérieur. Ce guide vous accompagne tout au long des étapes d’activation de WSL sur votre ordinateur.

## <a name="enable-the-windows-subsystem-for-linux"></a>Activer le sous-système Windows pour Linux

Avant de pouvoir exécuter les distributions Linux sur Windows, vous devez activer la fonctionnalité facultative « Sous-système Windows pour Linux » et redémarrer.

Ouvrez PowerShell en tant qu’administrateur et exécutez :

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a>Télécharger une distribution Linux

Suivez [ces instructions](install-manual.md) pour télécharger votre distribution Linux préférée.

## <a name="extract-and-install-a-linux-distribution"></a>Extraire et installer une distribution Linux

Maintenant que vous avez téléchargé une distribution Linux, afin d’extraire son contenu et de l’installer manuellement, procédez comme suit :

1. Extrayez le contenu du package `<distro>.appx` à l’aide de PowerShell :

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Exécutez l’application de lancement de distribution dans le dossier cible. Le lanceur est généralement nommé `<distro>.exe` (par exemple, `ubuntu.exe`).

    ![Distribution Ubuntu développée sur Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> **Échec de l’installation avec l’erreur 0x8007007e** : Si vous recevez cette erreur, votre système ne prend pas en charge WSL. Veillez à exécuter la build 16215 ou ultérieure de Windows. [Vérifiez votre build](troubleshooting.md#check-your-build-number). [Vérifiez également que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled) et que votre ordinateur a été redémarré après l’activation de la fonctionnalité.  

3. Ajoutez votre chemin de distribution à la variable PATH de chemin d’environnement Windows (`C:\Users\Administrator\Ubuntu` dans cet exemple), à l’aide de PowerShell :

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

Vous pouvez maintenant lancer votre distribution à partir de n’importe quel chemin en tapant `<distro>.exe`. Par exemple : `ubuntu.exe`.

Maintenant qu’elle est installée, vous devez [initialiser votre nouvelle instance de distribution](initialize-distro.md) avant de l’utiliser.
