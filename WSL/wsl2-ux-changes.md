---
title: Modifications de l’expérience utilisateur entre WSL 1 et WSL 2
description: L’expérience utilisateur passe de WSL 1 à WSL 2
keywords: BashOnWindows, bash, WSL, wsl2, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 635e4335bd3fe5dd1629faba0168ec4fa331e190
ms.sourcegitcommit: 6f6b7b67dd35b5fc7b582bb7ac27b9936dedb23d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/02/2019
ms.locfileid: "74681643"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>L’expérience utilisateur passe de WSL 1 à WSL 2

Cette page présente les différences d’expérience utilisateur entre WSL 1 et WSL 2 Preview. Les modifications clés à prendre en compte sont les suivantes :

- Placez les fichiers auxquels vos applications Linux accéderont dans votre système de fichiers racine Linux pour accélérer les performances des fichiers.
- Dans les versions initiales de la version préliminaire de WSL 2, vous devez accéder aux applications réseau à l’aide d’une adresse IP et non de localhost

Vous trouverez ci-dessous la liste complète des autres modifications que vous pouvez remarquer :

- WSL 2 utilise un [disque dur virtuel](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) pour stocker vos fichiers et, si vous atteignez sa taille maximale, vous devrez peut-être le développer
- Lors du démarrage de, WSL 2 utilise à présent une petite proportion de mémoire
- La vitesse d’accès aux fichiers entre systèmes d’exploitation sera plus lente dans les versions préliminaires initiales

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Placez vos fichiers Linux dans votre système de fichiers racine Linux
Veillez à placer les fichiers auxquels vous accédez fréquemment avec les applications Linux à l’intérieur de votre système de fichiers racine Linux pour bénéficier des avantages en matière de performances des fichiers. Ces fichiers doivent se trouver dans le système de fichiers racine Linux pour bénéficier d’un accès plus rapide au système de fichiers. Nous avons également rendu possible les applications Windows à accéder au système de fichiers racine Linux (comme l’Explorateur de fichiers ! Essayez d’exécuter : `explorer.exe .` dans le répertoire de démarrage de votre distribution Linux et voyez ce qui se passe), ce qui rend cette transition beaucoup plus facile. 

## <a name="accessing-network-applications"></a>Accès aux applications réseau
Dans les versions initiales de la version préliminaire de WSL 2, vous devrez accéder à n’importe quel serveur Windows à partir de Linux à l’aide de l’adresse IP de votre ordinateur hôte.

### <a name="accessing-windows-applications-from-linux"></a>Accès aux applications Windows à partir de Linux
Pour accéder à une application réseau Windows, vous devez utiliser l’adresse IP de votre ordinateur hôte. Pour ce faire, procédez comme suit :

- Obtenez l’adresse IP de votre ordinateur hôte en exécutant la commande `cat /etc/resolv.conf` et en copiant l’adresse IP à la suite du terme `nameserver`. 
- Connectez-vous à n’importe quel serveur Windows à l’aide de l’adresse IP copiée.

L’image ci-dessous en présente un exemple en se connectant à un serveur node. js s’exécutant sous Windows via la boucle. 

![Accès aux applications réseau Linux à partir de Windows](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows-only-in-builds-lower-than-18945"></a>Accès aux applications Linux à partir de Windows (uniquement dans les builds inférieures à 18945)
Si vous avez un serveur dans un distribution WSL, vous devez trouver l’adresse IP de la machine virtuelle qui alimente votre distribution et s’y connecter avec cette adresse IP. Pour ce faire, procédez comme suit :

- Obtenez l’adresse IP de votre distribution en exécutant la commande `ip addr` à l’intérieur de votre distribution WSL et en la recherchant sous la valeur `inet` de l’interface `eth0`.
   - Vous pouvez le trouver plus facilement en filtrant la sortie de la commande à l’aide de grep comme suit : `ip addr | grep eth0`.
- Connectez-vous à votre serveur Linux à l’aide de l’adresse IP que vous avez trouvée ci-dessus.

L’image ci-dessous en présente un exemple en vous connectant à un serveur node. js à l’aide du navigateur Edge.

![Accès aux applications réseau Linux à partir de Windows](media/wsl2-network-w2l.jpg)

Si votre Build est 18945 ou une version ultérieure, vous pouvez utiliser localhost comme normal. 

### <a name="other-networking-considerations"></a>Autres considérations relatives à la mise en réseau

#### <a name="connecting-via-remote-ip-addresses"></a>Connexion via des adresses IP distantes

Lorsque vous utilisez des adresses IP distantes pour vous connecter à vos applications, celles-ci sont traitées comme des connexions à partir du réseau local (LAN). Cela signifie que vous devrez vous assurer que votre application peut accepter des connexions LAN, par exemple, vous devrez peut-être lier votre application à `0.0.0.0` au lieu de `127.0.0.1`. Par exemple, dans Python à l’aide de la fiole, vous pouvez effectuer cette opération à l’aide de la commande : `app.run(host='0.0.0.0')`. Gardez à l’esprit la sécurité lorsque vous apportez ces modifications, car cela permettra d’établir des connexions à partir de votre réseau local. 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>Accès à un distribution WSL2 à partir de votre réseau local (LAN)

Lors de l’utilisation d’un distribution WSL1, si votre ordinateur est configuré pour être accessible par dans votre réseau local, les applications s’exécutant dans WSL sont également accessibles sur votre réseau local. Ce n’est pas le cas par défaut dans WSL2, car WSL2 a une carte Ethernet virtualisée avec sa propre adresse IP. Actuellement, pour activer ce flux de travail, vous devez suivre les mêmes étapes que pour une machine virtuelle standard. Nous recherchons des moyens d’améliorer cette expérience.

#### <a name="ipv6-access"></a>Accès IPv6

WSL2 distributions ne peut pas accéder actuellement aux adresses IPv6. Nous travaillons à l’ajout de cette fonctionnalité.

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>La compréhension de WSL 2 utilise un disque dur virtuel et explique ce qu’il faut faire si vous atteignez sa taille maximale
WSL 2 stocke tous vos fichiers Linux à l’intérieur d’un VHD qui utilise le système de fichiers ext4. Ce disque dur virtuel est redimensionné automatiquement en fonction de vos besoins de stockage. Ce disque dur virtuel a également une taille maximale initiale de 256 Go. Si la taille de votre distribution est supérieure à 256 Go, vous verrez des erreurs indiquant que l’espace disque est insuffisant. Vous pouvez résoudre ces problème en développant la taille du disque dur virtuel. Vous trouverez ci-dessous des instructions sur la procédure à suivre :

1. Arrêter toutes les instances WSL à l’aide de la commande `wsl --shutdown`
2. Recherchez le nom de votre package d’installation distribution « PackageFamilyName »
   - Dans une invite PowerShell (où « distribution » est le nom de votre distribution), tapez :
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. Localisez le fichier de disque dur virtuel (FullPath) utilisé par votre installation de WSL 2, il s’agit de votre « pathToVHD » :
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. Redimensionnez votre disque dur virtuel WSL 2 en exécutant les commandes suivantes
   - Ouvrez une fenêtre d’invite de commandes avec des privilèges d’administrateur et exécutez les commandes suivantes :
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. Lancez votre distribution WSL
6. Rendre WSL conscient qu’il peut étendre sa taille de système de fichiers
   - Exécutez ces commandes dans votre distribution WSL :
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copiez le nom de cette entrée, qui ressemble à ceci:/dev/sdXX (avec X représentant tout autre caractère)
      - `sudo resize2fs /dev/sdXX`
         - Veillez à utiliser la valeur que vous avez copiée précédemment et vous devrez peut-être utiliser : `apt install resize2fs`.

Remarque : en général, vous ne devez pas modifier, déplacer ou accéder aux fichiers associés à WSL situés à l’intérieur de votre dossier AppData à l’aide des outils ou des éditeurs Windows. Cela peut entraîner la corruption de vos distribution Linux.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 va utiliser de la mémoire au démarrage
WSL 2 utilise une machine virtuelle utilitaire légère sur un véritable noyau Linux pour offrir des performances optimales pour le système de fichiers et une compatibilité complète des appels système tout en étant aussi clair, rapide, intégré et réactif que WSL 1. Cette machine virtuelle de l’utilitaire présente un faible encombrement mémoire et alloue de la mémoire à l’adresse virtuelle au démarrage. Il est configuré pour démarrer avec une petite partie de la mémoire totale.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>La vitesse des fichiers de système d’exploitation est plus lente dans les versions préliminaires initiales
Vous remarquerez des vitesses de fichiers plus lentes par rapport à WSL 1 lorsque vous accédez à des fichiers Windows à partir d’une application Linux, ou lorsque vous accédez à des fichiers Linux à partir d’une application Windows. Il s’agit d’un résultat des modifications architecturales dans WSL 2. il s’agit d’une étude active de l’équipe WSL sur la façon dont nous pouvons améliorer cette expérience.
