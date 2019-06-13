---
title: Modifications de l’expérience utilisateur entre WSL 1 et 2 de WSL
description: Modifications de l’expérience utilisateur entre WSL 1 et 2 de WSL
keywords: BashOnWindows, bash, wsl, wsl2, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038099"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>Modifications de l’expérience utilisateur entre WSL 1 et 2 de WSL

Cette page dépasse les différences d’expérience utilisateur entre WSL 1 et la version préliminaire WSL 2. Les principales modifications apportées à connaître sont :

- Placez les fichiers qui accèderont à vos applications Linux dans votre système de fichiers racine Linux pour la vitesse de performances plus rapide des fichiers
- Dans les versions initiales de la version préliminaire WSL 2, vous devez accéder aux applications de réseau à l’aide d’une adresse IP et n’utilisez ne pas localhost

Et Voici la liste complète des autres modifications que vous pouvez remarquer :

- WSL 2 utilise un disque dur virtuel pour stocker vos fichiers et si vous atteignez sa taille maximale, vous devrez développer
- Lors du démarrage, WSL 2 utilise désormais une petite proportion de mémoire
- Entre le système d’exploitation vitesse d’accès de fichier sera plus lente dans les versions d’évaluation initiale

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>Placez vos fichiers de Linux sur votre système de fichiers racine Linux
Veillez à placer les fichiers que vous accédez fréquemment avec Linux applications à l’intérieur de votre Linux de fichiers racine de profiter des avantages de performances de fichier. Ces fichiers doivent se trouver au sein du système de fichiers racine Linux pour avoir un accès de système de fichiers plus rapide. Nous avons également rendu possible pour les applications Windows accéder au système de fichiers Linux racine (par exemple, l’Explorateur de fichiers ! Essayez d’exécuter : `explorer.exe /` dans votre interpréteur de commandes bash et que se passe-t-il) qui rend cette transition considérablement plus facile. 

## <a name="accessing-network-applications"></a>L’accès aux applications de réseau
Dans les builds initiales de la version préliminaire WSL 2, vous devrez accéder à n’importe quel serveur Linux à partir de Windows à l’aide de l’adresse IP de votre distribution Linux et n’importe quel serveur Windows à partir de Linux à l’aide de l’adresse IP de votre ordinateur hôte. Il s’agit d’un élément qui est temporaire et très élevé de notre liste de priorité pour résoudre.

### <a name="accessing-linux-applications-from-windows"></a>L’accès aux applications Linux à partir de Windows
Si vous avez un serveur dans une distribution WSL, vous devrez trouver l’adresse IP de la machine virtuelle mise sous tension de votre distribution et vous y connecter avec cette adresse IP. Pour cela, procédez comme suit :

- Obtenir l’adresse IP de votre distribution en exécutant la commande `ip addr` à l’intérieur de votre distribution WSL et sa recherche sous la `inet` valeur de la `eth0` interface.
   - Vous pouvez le trouver plus facilement en filtrant la sortie de la commande à l’aide de grep comme suit : `ip addr | grep eth0`.
- Se connecter à votre serveur Linux à l’aide de l’adresse IP que vous avez trouvé précédemment.

L’illustration ci-dessous montre un exemple de cela en vous connectant à un serveur de nodeJS à l’aide du navigateur Microsoft Edge.

![L’accès aux applications de réseau de Linux à partir de Windows](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>L’accès aux applications Windows à partir de Linux
Pour accéder à une application de réseau Windows, vous devez utiliser l’adresse IP de votre ordinateur hôte. Vous pouvez le faire avec ces étapes :

- Obtenir l’adresse IP de votre ordinateur hôte en exécutant la commande `cat /etc/resolv.conf` et la copie de l’adresse IP après le terme `nameserver`. 
- Se connecter à n’importe quel serveur Windows à l’aide de l’adresse IP copié.

L’illustration ci-dessous montre un exemple de cela en vous connectant à un serveur de python en cours d’exécution dans Windows via curl. 

![L’accès aux applications de réseau de Linux à partir de Windows](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>Présentation de WSL 2 utilise un disque dur virtuel et que faire si vous atteignez sa taille maximale
WSL 2 stocke tous vos fichiers Linux à l’intérieur d’un disque dur virtuel qui utilise le système de fichiers ext4. Ce disque dur virtuel est redimensionné automatiquement pour répondre à vos besoins de stockage. Ce disque dur virtuel a également une taille initiale maximale de 256 Go. Si votre distribution augmente en taille est supérieure à 256 Go, vous verrez des erreurs que vous avez plus d’espace disque. Vous pouvez corriger ces en augmentant la taille de disque dur virtuel. Obtenir des instructions sur la marche à suivre sont les suivants :

1. Mettre fin à toutes les instances WSL à l’aide de la `wsl --shutdown` commande
2. Redimensionner votre disque dur virtuel de 2 WSL en effectuant les commandes suivantes
   - Ouvrez une fenêtre d’invite de commandes avec des privilèges d’administrateur et exécutez les commandes suivantes :
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. Lancez votre distribution WSL
4. Rendre WSL conscient que cela peut améliorer la taille de son système de fichiers
   - Exécutez les commandes suivantes dans votre distribution WSL :
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - Copiez le nom de cette entrée, qui doit ressembler à : / dev/sdXX (avec un X représentant un caractère quelconque)
      - `sudo resize2fs /dev/sdXX`
         - Assurez-vous d’utiliser la valeur que vous avez copiée précédemment, et vous devrez peut-être utiliser : `apt install resize2fs`.

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 utilisera la mémoire au démarrage
WSL 2 utilise un utilitaire léger de machine virtuelle sur un noyau Linux réel pour fournir des performances du système de fichiers excellent et complète du système d’appel compatibilité tout en étant toujours comme light, rapide et intégrée et réactives que WSL 1. Cet utilitaire machine virtuelle a un faible encombrement mémoire et alloue une adresse virtuelle soutenu de mémoire au démarrage. Il est configuré pour démarrer avec une faible proportion de votre mémoire totale.

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>Entre le système d’exploitation, vitesse du fichier sera plus lente dans les versions d’évaluation initiale
Vous remarquerez que les vitesses de fichier plus lentes par rapport à WSL 1 lors de l’accès des fichiers de Windows à partir d’une application de Linux, ou l’accès aux fichiers Linux à partir d’une application Windows. Ceci est le résultat des modifications architecturales dans WSL 2 et est quelque chose de l’équipe WSL activement examen sur la façon dont nous pouvons améliorer cette expérience.