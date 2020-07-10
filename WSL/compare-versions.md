---
title: Vue d’ensemble du sous-système Windows pour Linux
description: Découvrez le sous-système Windows pour Linux, les différentes versions et les différentes façons de les utiliser.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux, ubuntu, debian, suse, windows 10, changements de l’expérience utilisateur, WSL 2, noyau linux, applications réseau, localhost, IPv6, disque matériel virtuel, VHD, limitations VHD, erreur VHD
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 8354e9c35d1e97f38c4cf6aa53a861c2c5e290be
ms.sourcegitcommit: 386d47a1c53a85b91f5a2b0f1f99ce2c46b20a77
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "86093279"
---
# <a name="comparing-wsl-2-and-wsl-1"></a>Comparaison entre WSL 2 et WSL 1

Les principaux objectifs de la mise à jour du sous-système Windows pour Linux vers une nouvelle version sont d’**augmenter les performances du système de fichiers** et de prendre en charge la **compatibilité complète des appels système**. 

WSL 2 utilise la technologie de virtualisation la plus récente et efficace pour exécuter un noyau Linux au sein d’une machine virtuelle utilitaire légère. Toutefois, WSL 2 n’est pas une expérience de machine virtuelle standard. [En savoir plus sur l’architecture WSL 2](#wsl-2-architecture).

## <a name="comparing-features"></a>Comparaison des fonctionnalités

Fonctionnalité | WSL 1 | WSL 2
--- | --- | ---
 Intégration entre Windows et Linux| ✅|✅
 Temps de démarrage courts| ✅ | ✅
 Faible encombrement des ressources| ✅ |✅
 Exécutions avec les versions actuelles de VMWare et VirtualBox| ✅ | ✅
 Machine virtuelle managée| ❌ | ✅
 Noyau Linux complet| ❌ |✅
 Compatibilité complète des appels système| ❌ | ✅
 Performances dans les systèmes de fichiers du système d’exploitation| ✅ | ❌

Vous utilisez WSL 1 et souhaitez mettre à niveau vers WSL 2 ? Suivez les instructions de [mise à jour vers WSL 2](./install-win10.md#update-to-wsl-2).

WSL 2 est disponible uniquement dans Windows 10, version 2004, build 19041 ou ultérieure. Vérifiez votre version de Windows en sélectionnant la **touche Windows + R**, tapez **winver** et sélectionnez **OK**. (Ou entrez la commande `ver` dans l’invite de commandes Windows). Vous devrez peut-être effectuer une [mise à jour vers la dernière version de Windows](ms-settings:windowsupdate). Pour les builds inférieures à 19041, WSL n’est pas pris en charge du tout.

> [!NOTE]
> WSL 2 fonctionne avec [VMWare 15.5.5 +](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) et [VirtualBox 6 +](https://www.virtualbox.org/wiki/Changelog-6.0).

## <a name="use-the-linux-file-system-for-faster-performance"></a>Utiliser le système de fichiers Linux pour des performances plus rapides

Pour optimiser les performances, veillez à stocker vos fichiers de projet dans le système de fichiers Linux (et non dans le système de fichiers Windows).

Par exemple, lors du stockage de vos fichiers de projet WSL :

* Utilisez le répertoire racine du système de fichiers Linux : `\\wsl$\Ubuntu-18.04\home\<user name>\Project`
* Et non pas le répertoire racine du système de fichiers Windows : `C:\Users\<user name>\Project`

Les fichiers de projet avec lesquels vous travaillez à l’aide d’une distribution WSL (comme Ubuntu) doivent se trouver dans le système de fichiers racine Linux pour tirer parti de l’accès plus rapide au système de fichiers.

Vous pouvez accéder à votre système de fichiers racine Linux à l’aide d’outils et d’applications Windows, tels que l’Explorateur de fichiers. Essayez d’ouvrir une distribution Linux (comme Ubuntu), assurez-vous d’être dans le répertoire racine de Linux en entrant la commande suivante : `cd ~`. Ouvrez ensuite votre système de fichiers Linux dans l’Explorateur de fichiers en entrant *(n’oubliez pas le point final)*  : `explorer.exe .`

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a>Exceptions pour l’utilisation de WSL 1 à la place de WSL 2

Nous vous recommandons d’utiliser WSL 2 parce qu’il offre de meilleures performances et une compatibilité à 100 % des appels système. Toutefois, il existe quelques scénarios spécifiques où vous préférerez peut-être utiliser WSL 1. Envisagez d’utiliser WSL 1 dans les cas suivants :

* Vos fichiers de projet doivent être stockés dans le système de fichiers Windows.
  * Si vous souhaitez utiliser votre distribution WSL Linux pour accéder aux fichiers de projet dans le système de fichiers Windows et que ces fichiers ne peuvent pas être stockés dans le système de fichiers Linux, vous obtiendrez de meilleures performances dans les systèmes de fichiers du système d’exploitation en utilisant WSL 1.
* Un projet qui requiert une compilation croisée avec des outils Windows et Linux sur les mêmes fichiers.
  * Les performances des fichiers sur les systèmes d’exploitation Windows et Linux sont plus rapides dans WSL 1 que WSL 2. Par conséquent, si vous utilisez des applications Windows pour accéder à des fichiers Linux, vous obtiendrez actuellement de meilleures performances en termes de rapidité avec WSL 1.

> [!NOTE]
> Envisagez de tester l’[extension Remote WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) de VS Code pour pouvoir stocker vos fichiers de projet dans le système de fichiers Linux en utilisant les outils en ligne de commande Linux, mais également VS Code sur Windows pour créer, modifier, déboguer et exécuter votre projet dans un navigateur Internet sans les ralentissements de performances associés à l’utilisation des systèmes de fichiers Linux et Windows. [En savoir plus](https://code.visualstudio.com/docs/remote/wsl)

## <a name="wsl-2-architecture"></a>Architecture WSL 2

Une expérience de machine virtuelle traditionnelle peut être lente à démarrer, est isolée, consomme beaucoup de ressources et vous prend du temps pour la gérer. WSL 2 n’a pas ces attributs,

WSL 2 offre les avantages de WSL 1, y compris une intégration transparente entre Windows et Linux, des temps de démarrage courts et un faible encombrement des ressources. De plus, il ne nécessite aucune configuration ni gestion de machine virtuelle. WSL 2 utilise une machine virtuelle. Celle-ci est gérée et exécutée en arrière-plan, ce qui vous permet de jouir de la même expérience utilisateur qu’avec WSL 1.

### <a name="full-linux-kernel"></a>Noyau Linux complet

Le noyau Linux dans WSL 2 est élaboré par Microsoft à partir de la dernière branche stable, en fonction de la source disponible sur kernel.org. Ce noyau a été spécialement réglé pour WSL 2, afin d’optimiser la taille et les performances pour offrir une expérience Linux exceptionnelle sur Windows. Le noyau sera géré par le biais des mises à jour Windows, ce qui signifie que vous obtiendrez les derniers correctifs de sécurité et les dernières améliorations du noyau sans avoir à gérer cela vous-même.

Le [noyau Linux WSL 2 est disponible en open source](https://github.com/microsoft/WSL2-Linux-Kernel). Si vous souhaitez en savoir plus, consultez le billet de blog [Shipping a Linux Kernel with Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) rédigé par l’équipe qui l’a créé.

### <a name="increased-file-io-performance"></a>Amélioration des performances d’E/S de fichier

Les opérations gourmandes en fichiers, telles que git clone, npm install, apt update, apt upgrade, etc., sont toutes nettement plus rapides avec WSL 2.

L’augmentation de la vitesse réelle dépend de l’application que vous exécutez et de la manière dont elle interagit avec le système de fichiers. Les versions initiales de WSL 2 s’exécutent jusqu’à 20 fois plus vite que WSL 1 lors de la décompression d’un tarball compressé, et environ 2 à 5 fois plus vite lors de l’utilisation de git clone, npm install et cmake sur divers projets.

### <a name="full-system-call-compatibility"></a>Compatibilité complète des appels système

Les binaires Linux utilisent des appels système pour exécuter des fonctions, telles que l’accès aux fichiers, la demande de mémoire, la création de processus et bien plus encore. Alors que WSL 1 utilisait une couche de traduction créée par l’équipe WSL, WSL 2 inclut son propre noyau Linux avec compatibilité complète des appels système. Les avantages sont les suivants :

* Un tout nouvel ensemble d’applications que vous pouvez exécuter au sein de WSL, telles que **[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** et plus encore.

* Les mises à jour du noyau Linux sont toutes immédiatement prêtes à l’emploi. (Vous n’avez pas besoin d’attendre que l’équipe WSL implémente les mises à jour et ajoute les modifications).

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a>WSL 2 utilise une plus petite quantité de mémoire au démarrage.

WSL 2 utilise une machine virtuelle utilitaire légère sur un noyau Linux réel avec un faible encombrement mémoire. L’utilitaire alloue la mémoire stockée à l’adresse virtuelle au démarrage. Il est configuré pour démarrer avec une plus petite proportion de votre mémoire totale que celle requise pour WSL 1.

## <a name="accessing-network-applications"></a>Accès aux applications réseau

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a>Accès aux applications réseau Linux à partir de Windows (localhost)

Si vous créez une application réseau (par exemple, une application qui s’exécute sur un serveur SQL ou NodeJS) dans votre distribution Linux, vous pouvez y accéder à partir d’une application Windows (comme votre navigateur Internet Edge ou Chrome) à l’aide de `localhost` (comme vous le feriez normalement).

Toutefois, si vous exécutez une version antérieure de Windows (build 18945 ou inférieure), vous devez récupérer l’adresse IP de la machine virtuelle hôte Linux (ou effectuer une [mise à jour vers la dernière version de Windows](ms-settings:windowsupdate)).

Pour trouver l’adresse IP de la machine virtuelle qui alimente votre distribution Linux :

* À partir de votre distribution WSL (p. ex. Ubuntu), exécutez la commande : `ip addr`
* Recherchez et copiez l’adresse sous la valeur `inet` de l’interface `eth0`.
* Si vous avez installé l’outil grep, trouvez-la plus facilement en filtrant la sortie à l’aide de la commande : `ip addr | grep eth0`
* Connectez-vous à votre serveur Linux à l’aide de cette adresse IP.

L’image ci-dessous illustre un exemple de cela avec la connexion à un serveur Node.js à l’aide du navigateur Edge.

![Accès aux applications réseau Linux à partir de Windows](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a>Accès aux applications réseau Windows à partir de Linux (adresse IP de l’hôte)

Si vous souhaitez accéder à une application réseau qui s’exécute sur Windows (par exemple, une application s’exécutant sur un serveur SQL ou NodeJS) à partir de votre distribution Linux (p. ex. Ubuntu), vous devez utiliser l’adresse IP de votre ordinateur hôte. Il ne s’agit pas d’un scénario courant, mais vous pouvez suivre ces étapes pour le faire fonctionner.
    - Obtenez l’adresse IP de votre ordinateur hôte en exécutant cette commande à partir de votre distribution Linux : `cat /etc/resolv.conf`
    - Copiez l’adresse IP qui suit le terme : `nameserver`.
    - Connectez-vous à n’importe quel serveur Windows à l’aide de l’adresse IP copiée.

L’image ci-dessous présente un exemple de cela avec la connexion à un serveur Node.js en cours d’exécution dans Windows via curl.

![Accès aux applications réseau Linux à partir de Windows](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a>Autres considérations relatives aux réseaux

#### <a name="connecting-via-remote-ip-addresses"></a>Connexion via des adresses IP distantes

Lorsque vous utilisez des adresses IP distantes pour vous connecter à vos applications, celles-ci sont traitées comme des connexions à partir du réseau local (LAN). Cela signifie que vous devez vous assurer que votre application peut accepter les connexions LAN.

Par exemple, vous devrez peut-être lier votre application à `0.0.0.0` au lieu de `127.0.0.1`. Dans l’exemple d’une application Python utilisant Flask, vous pouvez procéder à l’aide de la commande : `app.run(host='0.0.0.0')`. Gardez à l’esprit la sécurité lorsque vous apportez ces changements, car cela permettra d’établir des connexions à partir de votre réseau local.

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a>Accès à une distribution WSL 2 à partir de votre réseau local (LAN)

Lorsque vous utilisez une distribution WSL 1, si votre ordinateur était configuré pour être accessible via votre réseau local, les applications qui s’exécutent dans WSL sont également accessibles sur votre réseau local.

Ce n’est pas le cas par défaut dans WSL 2. WSL 2 a une carte Ethernet virtualisée avec sa propre adresse IP unique. Actuellement, pour activer ce flux de travail, vous devez suivre les mêmes étapes que pour une machine virtuelle standard. (Nous recherchons des moyens d’améliorer cette expérience.)

#### <a name="ipv6-access"></a>Accès IPv6

Les distributions WSL 2 ne peuvent actuellement pas atteindre les adresses IPv6 uniquement. Nous travaillons à l’ajout de cette fonctionnalité.

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a>Augmentation de la taille de votre disque matériel virtuel WSL 2

WSL 2 utilise un disque dur virtuel (VHD) pour stocker vos fichiers Linux. Si vous atteignez sa taille maximale, vous devrez peut-être l’augmenter.

Le disque dur virtuel WSL 2 utilise le système de fichiers ext4. Ce disque dur virtuel est redimensionné automatiquement en fonction de vos besoins de stockage et a une taille maximale initiale de 256 Go. Si la taille de votre distribution vient à dépasser 256 Go, vous verrez des erreurs indiquant que l’espace disque est insuffisant. Vous pouvez corriger cette erreur en augmentant la taille du disque dur virtuel.

Pour augmenter la taille maximale du disque dur virtuel au-delà de 256 Go :

1. Arrêtez toutes les instances WSL à l’aide de la commande : `wsl --shutdown`

2. Recherchez le nom du package d’installation de votre distribution ('PackageFamilyName')
    * Dans PowerShell ('distro' étant le nom de votre distribution), entrez la commande :
    * `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. Localisez le paramètre `fullpath` du fichier sur le disque dur virtuel, utilisé par votre installation WSL 2. Il s’agit de votre `pathToVHD` :
     * `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. Redimensionnez votre disque dur virtuel WSL 2 en exécutant les commandes suivantes :
   * Ouvrez l’invite de commandes Windows avec des privilèges d’administrateur et entrez :
      * `diskpart`
      * `Select vdisk file="<pathToVHD>"`
      * `expand vdisk maximum="<sizeInMegaBytes>"`

5. Lancez votre distribution WSL (Ubuntu, par exemple).

6. Indiquez à WSL qu’il peut augmenter la taille de son système de fichiers en exécutant les commandes suivantes à partir de votre ligne de commande de distribution Linux :
    * `sudo mount -t devtmpfs none /dev`
    * `mount | grep ext4`
    * Copiez le nom de cette entrée, qui ressemble à ceci : `/dev/sdXX` (X représentant tout autre caractère)
    * `sudo resize2fs /dev/sdXX`
    * Utilisez la valeur que vous avez copiée précédemment. Vous devrez peut-être également installer resize2fs : `apt install resize2fs`

> [!NOTE]
> En général, vous ne devez pas modifier, déplacer ni accéder aux fichiers associés à WSL, situés dans votre dossier AppData, à l’aide d’outils ou d’éditeurs Windows. Cela pourrait entraîner la corruption de votre distribution Linux.
