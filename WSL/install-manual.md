---
title: Télécharger manuellement des distributions du sous-système Windows pour Linux (WSL)
description: Instructions sur la façon de télécharger manuellement des distributions du sous-système Windows pour Linux.
keywords: wsl, sous-système Windows pour Linux, installation manuelle, installer manuellement, microsoft store, Windows 10, curl, Add-AppxPackage, maintenance à long terme, LTSC
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: d948ce9d304314bdd15b98136b8a99ca35723139
ms.sourcegitcommit: e67eb4aedff57a304188ca3360aba25605f8bdb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2020
ms.locfileid: "84746275"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Télécharger manuellement des packages de distribution du sous-système Windows pour Linux

Il existe plusieurs scénarios où vous pouvez ne pas être en mesure d’installer (ou ne pas vouloir installer) des distributions WSL Linux via le Microsoft Store. Plus précisément, vous utilisez peut-être une référence SKU de système d’exploitation de bureau Windows Server ou de maintenance à long terme (LTSC) qui ne prend pas en charge le Microsoft Store, ou vos stratégies et/ou administrateurs de réseau d’entreprise ne permettent pas l’utilisation du Microsoft Store dans votre environnement.

Dans ces cas, alors que WSL est lui-même disponible, comment télécharger et installer des distributions Linux dans WSL si vous ne pouvez pas accéder au Store ?

> Remarque : **Les environnements d’interpréteur de ligne de commande, notamment cmd, PowerShell et les distributions Linux/WSL, ne sont pas autorisés à s’exécuter sur Windows 10 en mode S**. Cette restriction a pour but de garantir les objectifs d’intégrité et de sécurité fournis par le mode S : Lisez [cette publication](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) pour plus d’informations.

## <a name="downloading-distros"></a>Téléchargement de distributions

Si l’application Microsoft Store n’est pas disponible, vous pouvez télécharger et installer manuellement les distributions Linux en cliquant sur les liens suivants :
* [Ubuntu 20.04](https://aka.ms/wslubuntu2004)
* [Ubuntu 20.04 ARM](https://aka.ms/wslubuntu2004arm)
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix pour WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Cela entraîne le téléchargement des packages `<distro>.appx` dans un dossier de votre choix. Suivez les [instructions d’installation](#installing-your-distro) pour installer la ou les distributions téléchargées.

## <a name="downloading-distros-via-the-command-line"></a>Téléchargement de distributions via la ligne de commande
Si vous préférez, vous pouvez également télécharger vos distributions préférées via la ligne de commande :

 ### <a name="download-using-powershell"></a>Télécharger à l’aide de PowerShell
 Pour télécharger des distributions à l’aide de PowerShell, utilisez l’applet de commande [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-5.1). Voici un exemple d’instruction permettant de télécharger Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Si le téléchargement prend beaucoup de temps, désactivez la barre de progression en définissant `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Télécharger à l’aide de curl
La mise à jour de Windows 10 Printemps 2018 (ou ultérieure) inclut l’[utilitaire de ligne de commande curl](https://curl.haxx.se/) populaire avec lequel vous pouvez appeler des requêtes web (par exemple, des commandes HTTP GET, POST, PUT, etc.) à partir de la ligne de commande. Vous pouvez utiliser `curl.exe` pour télécharger les distributions ci-dessus :

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

Dans l’exemple ci-dessus, `curl.exe` est exécuté (pas seulement `curl`) pour s’assurer que, dans PowerShell, l’exécutable curl réel est appelé, et non pas l’alias curl PowerShell pour [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Remarque : L’utilisation de `curl` peut être préférable si vous devez écrire des scripts/appeler des étapes de téléchargement à l’aide de l’interpréteur cmd et/ou des scripts `.bat` / `.cmd`.

## <a name="installing-your-distro"></a>Installation de votre distribution
Si vous utilisez Windows 10, vous pouvez installer votre distribution avec PowerShell. Accédez simplement au dossier contenant la distribution téléchargée ci-dessus et, dans ce répertoire, exécutez la commande suivante avec `app_name` comme nom de votre fichier .appx de distribution.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Si vous utilisez Windows Server, vous trouverez les instructions d’installation dans la page de documentation de [Windows Server](install-on-server.md).

Une fois votre distribution installée, suivez les instructions normales pour [mettre à jour WSL 2](./install-win10.md#update-to-wsl-2) ou [créer un compte d’utilisateur et un mot de passe](./user-support.md).
