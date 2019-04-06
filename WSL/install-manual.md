---
title: Télécharger manuellement le sous-système de Windows pour les distributions de Linux (WSL)
description: Instructions pour savoir comment télécharger manuellement le sous-système de Windows pour les distributions Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, WSL, sous-système windows, distributeur, ubuntu, openSUSE, kali debian, SLES,
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: be1c1331183317d4f970696464110b9968208d21
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063567"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Télécharger manuellement le sous-système de Windows pour les packages de distribution de Linux

Il existe plusieurs scénarios dans lequel peut ne pas pouvoir (ou souhaitez) pour installer des distributions de Linux de WSL via le Microsoft Store. Plus précisément, vous exécutez peut-être un serveur Windows ou le bureau de Long-Term Servicing (LTSB/LTSC) référence (SKU) du système d’exploitation qui ne prennent en charge Microsoft Store, ou vos stratégies de réseau d’entreprise et/ou Administrateurs pour autoriser l’utilisation de Microsoft Store ne pas dans votre environnement.

Dans ces cas, tandis que WSL lui-même est disponible, comment télécharger et installer des distributions de Linux dans WSL si vous ne pouvez pas accéder au magasin ?

> Remarque: **Environnements de shell de ligne de commande, y compris les distributions Linux/WSL Cmd et PowerShell ne sont pas autorisées à s’exécuter sur Windows 10 S Mode**. Cette restriction existe afin de garantir les objectifs de l’intégrité et la sécurité en Mode S offre : Lecture [ce billet](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) pour plus d’informations.

## <a name="downloading-distros"></a>Téléchargement de distributions

Si l’application Microsoft Store n’est pas disponible, vous pouvez télécharger et installer manuellement les distributions de Linux en cliquant sur ces liens :
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [openSUSE](https://aka.ms/wsl-opensuse-42)
* [SLES](https://aka.ms/wsl-sles-12)

Cela entraîne le `<distro>.appx` packages à télécharger vers un dossier de votre choix. Suivez le [instructions d’installation](#installing-your-distro) pour installer votre distro(s) téléchargé.

## <a name="downloading-distros-via-the-command-line"></a>Téléchargement des distributions via la ligne de commande
Si vous préférez, vous pouvez également télécharger votre distro(s) préféré par le biais de la ligne de commande :

 ### <a name="download-using-powershell"></a>Télécharger à l’aide de PowerShell
 Pour télécharger les distributions à l’aide de PowerShell, utilisez le [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) applet de commande. Voici un exemple d’instruction pour télécharger Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Si le téléchargement prend beaucoup de temps, désactiver la barre de progression en définissant `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Télécharger à l’aide de curl
Mise à jour Windows 10 printemps 2018 (ou version ultérieure) inclut le fameux [curl utilitaire de ligne de commande](https://curl.haxx.se/) avec laquelle vous pouvez appeler les requêtes web (par exemple, HTTP GET, POST, méthode PUT, les commandes etc.) à partir de la ligne de commande. Vous pouvez utiliser `curl.exe` pour télécharger les distributions ci-dessus :

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

Dans l’exemple ci-dessus, `curl.exe` est exécutée (pas seulement `curl`) pour vous assurer que, dans PowerShell, le fichier exécutable réel curl est appelé, pas PowerShell curl alias [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Remarque: À l’aide de `curl` peut être préférable si vous devez appeler/script des étapes de téléchargement à l’aide de Cmd shell et/ou `.bat`  /  `.cmd` scripts.

## <a name="installing-your-distro"></a>L’installation de votre distribution
Pour obtenir des instructions sur la façon d’installer votre distro(s) téléchargé, reportez-vous à la [Windows Desktop](install-win10.md) ou [Windows Server](install-on-server.md) instructions d’installation.
