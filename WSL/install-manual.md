---
title: Télécharger manuellement le sous-système Windows pour Linux (WSL) distributions
description: Instructions sur la façon de télécharger manuellement le sous-système Windows pour les distributions Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, WSL, sous-système Windows, distribution, Ubuntu, openSUSE, SLES, Debian, Kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 55cea2c4b7087f3dd8a29986aaddc8c313763448
ms.sourcegitcommit: b07769a3140db9ac63e42c7d7d1290c0bad8c40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/28/2019
ms.locfileid: "67467552"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Télécharger manuellement le sous-système Windows pour les packages distribution Linux

Il existe plusieurs scénarios dans lesquels il est possible que vous ne soyez pas en mesure d’installer WSL Linux distributions via le Microsoft Store. Plus précisément, vous utilisez peut-être une référence de système d’exploitation de bureau Windows Server ou long-term maintenance (LTSB/LTSC) qui ne prend pas en charge Microsoft Store, ou vos stratégies de réseau d’entreprise et/ou administrateurs ne peuvent pas autoriser l’utilisation d’Microsoft Store dans votre environnement.

Dans ce cas, bien que WSL soit disponible, comment télécharger et installer Linux distributions dans WSL si vous ne pouvez pas accéder au Store?

> Remarque : **Les environnements d’interpréteur de ligne de commande, notamment cmd, PowerShell et Linux/WSL distributions, ne sont pas autorisés à s’exécuter sur le mode Windows 10 S**. Cette restriction existe afin de garantir l’intégrité et les objectifs de sécurité fournis par le mode S: Pour plus d’informations, lisez [ce billet](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) .

## <a name="downloading-distros"></a>Téléchargement de distributions

Si l’application Microsoft Store n’est pas disponible, vous pouvez télécharger et installer manuellement les distributions Linux en cliquant sur les liens suivants:
* [Ubuntu 18,04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18,04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16,04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE LEAP 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix pour WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Cela entraîne le `<distro>.appx` téléchargement des packages dans un dossier de votre choix. Suivez les [instructions d’installation](#Installing-your-distro) pour installer vos distribution téléchargés.

## <a name="downloading-distros-via-the-command-line"></a>Téléchargement de distributions via la ligne de commande
Si vous préférez, vous pouvez également télécharger vos distribution préférés à l’aide de la ligne de commande:

 ### <a name="download-using-powershell"></a>Télécharger à l’aide de PowerShell
 Pour télécharger distributions à l’aide de PowerShell, utilisez l’applet [de commande Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) . Voici un exemple d’instruction pour télécharger Ubuntu 16,04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Si le téléchargement prend beaucoup de temps, désactivez la barre de progression en définissant`$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>Télécharger à l’aide de la boucle
La mise à jour Spring 2018 de Windows 10 (ou version ultérieure) comprend l' [utilitaire de ligne de commande de boucles](https://curl.haxx.se/) populaires avec lequel vous pouvez appeler des requêtes Web (par exemple, des commandes HTTP, http, put, etc.) à partir de la ligne de commande. Vous pouvez utiliser `curl.exe` pour télécharger les distributions ci-dessus:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

Dans l’exemple ci- `curl.exe` dessus, est exécuté ( `curl`pas seulement) pour garantir que, dans PowerShell, l’exécutable Real bouclé est appelé, et non l’alias PowerShell pour [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> Remarque : L' `curl` utilisation de peut être préférable si vous devez appeler/écrire des étapes de téléchargement à l’aide de `.bat` CMD Shell et/ou  /  `.cmd` de scripts.

## <a name="installing-your-distro"></a>Installation de votre distribution
Si vous utilisez Windows 10, vous pouvez installer votre distribution avec PowerShell. Accédez simplement au dossier contenant le distribution téléchargé à partir de la version ci-dessus et, dans ce `app_name` répertoire, exécutez la commande suivante, où est le nom de votre fichier distribution. Appx.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Si vous utilisez Windows Server, vous trouverez les instructions d’installation sur la page de documentation de [Windows Server](install-on-server.md) .

Une fois votre distribution installé, reportez-vous à la page [étapes Intilization](initialize-distro.md) pour initialiser votre nouveau distribution.
