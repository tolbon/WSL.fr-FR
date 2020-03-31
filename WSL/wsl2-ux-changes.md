---
title: Changements de l’expérience utilisateur entre WSL 1 et WSL 2
description: Changements de l’expérience utilisateur entre WSL 1 et WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1965a22a2e290777b207d9ded099ce4a79e1ed38
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256332"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Changements de l’expérience utilisateur entre WSL 1 et WSL 2

Cette page présente les différences d’expérience utilisateur entre WSL 1 et la préversion de WSL 2. Les changements clés à prendre en compte sont les suivants :

- Placez les fichiers auxquels vos applications Linux accéderont dans votre système de fichiers racine Linux pour accélérer l’accès et améliorer les performances de fichier
- Dans les versions initiales de la préversion de WSL 2, vous devez accéder aux applications réseau à l’aide d’une adresse IP et sans utiliser localhost

Vous trouverez ci-dessous la liste complète des autres changements que vous remarquerez peut-être :

- WSL 2 utilise un [disque dur virtuel](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) pour stocker vos fichiers et, si vous atteignez sa taille maximale, vous devrez peut-être le développer
- Au démarrage, WSL 2 utilise à présent une petite proportion de mémoire
- La vitesse d’accès aux fichiers du système d’exploitation est plus lente dans les versions d’évaluation initiales

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Placer les fichiers Linux dans votre système de fichiers racine Linux
Veillez à placer les fichiers auxquels vous accéderez fréquemment avec les applications Linux au sein de votre système de fichiers racine Linux pour bénéficier des avantages en matière de performances de fichier. Ces fichiers doivent se trouver dans le système de fichiers racine Linux pour bénéficier d’un accès plus rapide au système de fichiers. Nous avons également permis aux applications Windows d’accéder au système de fichiers racine Linux (comme l’Explorateur de fichiers ; essayez d’exécuter : `explorer.exe .` dans le répertoire de démarrage de votre distribution Linux et observez ce qui se passe), ce qui facilite grandement cette transition. 

## <a name="accessing-network-applications"></a>Accès aux applications réseau
Dans les versions initiales de la préversion de WSL 2, vous devrez accéder à n’importe quel serveur Windows à partir de Linux à l’aide de l’adresse IP de votre ordinateur hôte.

### <a name="accessing-windows-applications-from-linux"></a>Accès aux applications Windows à partir de Linux
Pour accéder à une application réseau Windows, vous devez utiliser l’adresse IP de votre ordinateur hôte. Pour ce faire, procédez comme suit :

- Obtenez l’adresse IP de votre ordinateur hôte en exécutant la commande `cat /etc/resolv.conf` et en copiant l’adresse IP suivant le terme `nameserver`. 
- Connectez-vous à n’importe quel serveur Windows à l’aide de l’adresse IP copiée.

L’image ci-dessous présente un exemple de cela avec la connexion à un serveur Node.js en cours d’exécution dans Windows via curl. 

![Accès aux applications réseau Linux à partir de Windows](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>Accès aux applications Linux à partir de Windows

Selon la version de Windows que vous utilisez, vous devrez peut-être récupérer l’adresse IP de la machine virtuelle. Si vous disposez de la build 18945 ou ultérieure, vous pouvez utiliser `localhost` de façon normale. 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a>Accès à Linux sur des builds antérieures à la build [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)

Si vous avez un serveur dans une distribution WSL, vous devez trouver l’adresse IP de la machine virtuelle qui alimente votre distribution et vous y connecter avec cette adresse IP. Pour ce faire, procédez comme suit :

- Obtenez l’adresse IP de votre distribution en exécutant la commande `ip addr` à l’intérieur de votre distribution WSL et en la recherchant sous la valeur `inet` de l’interface `eth0`.
   - Vous pouvez la trouver plus facilement en filtrant la sortie de la commande à l’aide de grep comme suit : `ip addr | grep eth0`.
- Connectez-vous à votre serveur Linux à l’aide de l’adresse IP que vous avez trouvée ci-dessus.

L’image ci-dessous illustre un exemple de cela avec la connexion à un serveur Node.js à l’aide du navigateur Edge.

![Accès aux applications réseau Linux à partir de Windows](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>Autres considérations relatives aux réseaux

#### <a name="connecting-via-remote-ip-addresses"></a>Connexion via des adresses IP distantes

Lorsque vous utilisez des adresses IP distantes pour vous connecter à vos applications, celles-ci sont traitées comme des connexions à partir du réseau local (LAN). Cela signifie que vous devez vous assurer que votre application peut accepter des connexions LAN, par exemple : Vous devrez peut-être lier votre application à `0.0.0.0` au lieu de `127.0.0.1`. Par exemple, dans Python avec Flask, vous pouvez effectuer cette opération à l’aide de la commande : `app.run(host='0.0.0.0')`. Gardez à l’esprit la sécurité lorsque vous apportez ces changements, car cela permettra d’établir des connexions à partir de votre réseau local. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>Accès à une distribution WSL2 à partir de votre réseau local (LAN)

Lorsque vous utilisez une distribution WSL1, si votre ordinateur a été configuré pour être accessible dans votre réseau local, les applications qui s’exécutent dans WSL sont également accessibles sur votre réseau local. Ce n’est pas le cas par défaut dans WSL2, car WSL2 a une carte Ethernet virtualisée avec sa propre adresse IP. Actuellement, pour activer ce flux de travail, vous devez suivre les mêmes étapes que pour une machine virtuelle standard. Nous recherchons des moyens d’améliorer cette expérience.

#### <a name="ipv6-access"></a>Accès IPv6

Les distributions WSL2 ne peuvent pas accéder actuellement aux adresses IPv6 uniquement. Nous travaillons à l’ajout de cette fonctionnalité.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Comprendre que WSL 2 utilise un disque dur virtuel et ce qu’il faut faire si vous atteignez sa taille maximale
WSL 2 stocke tous vos fichiers Linux sur un disque dur virtuel qui utilise le système de fichiers ext4. Ce disque dur virtuel est redimensionné automatiquement pour satisfaire vos besoins de stockage. Ce disque dur virtuel a également une taille maximale initiale de 256 Go. Si la taille de votre distribution vient à dépasser 256 Go, vous verrez des erreurs indiquant que l’espace disque est insuffisant. Vous pouvez résoudre ce problème en développant la taille du disque dur virtuel. Des instructions sur la façon de procéder sont fournies ci-dessous :

1. Arrêtez toutes les instances WSL à l’aide de la commande `wsl --shutdown`.
2. Recherchez le nom du package d’installation de votre distribution, « PackageFamilyName ».
   - Dans une invite PowerShell (où « distro » est le nom de votre distribution), tapez :
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. Localisez le chemin complet du fichier sur le disque dur virtuel, utilisé par votre installation WSL 2. Il s’agit de votre « pathToVHD » :
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. Redimensionnez votre disque dur virtuel WSL 2 en exécutant les commandes ci-dessous.
   - Ouvrez une fenêtre d’invite de commandes avec les privilèges d’administrateur et exécutez les commandes suivantes :
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. Lancez votre distribution WSL.
6. Rendez WSL conscient qu’il peut étendre la taille de son système de fichiers.
   - Exécutez ces commandes dans votre distribution WSL :
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copiez le nom de cette entrée, qui ressemble à ceci : /dev/sdXX (X représentant tout autre caractère).
      - `sudo resize2fs /dev/sdXX`
         - Veillez à utiliser la valeur que vous avez copiée précédemment et vous devrez peut-être utiliser : `apt install resize2fs`.

Remarque : En général, vous ne devez pas modifier, déplacer ni accéder aux fichiers associés à WSL, situés dans votre dossier AppData, à l’aide d’outils ou d’éditeurs Windows. Cela pourrait entraîner la corruption de votre distribution Linux.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 utilisera de la mémoire au démarrage
WSL 2 utilise une machine virtuelle utilitaire légère sur un véritable noyau Linux pour offrir de bonnes performances de système de fichiers et une compatibilité complète des appels système tout en restant aussi clair, rapide, intégré et réactif que WSL 1. Cette machine virtuelle utilitaire présente un faible encombrement mémoire et alloue de la mémoire stockée à l’adresse virtuelle au démarrage. Elle est configurée pour démarrer avec une petite proportion de votre mémoire totale.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>La vitesse des fichiers du système d’exploitation est plus lente dans les versions d’évaluation initiales
Vous remarquez des vitesses de fichiers inférieures par rapport à WSL 1 lorsque vous accédez à des fichiers Windows à partir d’une application Linux, ou lorsque vous accédez à des fichiers Linux à partir d’une application Windows. Cela résulte des changements architecturaux dans WSL 2 et fait l’objet d’une étude active de l’équipe WSL sur la façon d’améliorer cette expérience.
