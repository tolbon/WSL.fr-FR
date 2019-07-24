---
title: À propos de WSL 2
description: À propos de WSL 2 la nouvelle architecture du sous-système Windows pour Linux
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: e9c1f043207193a5c00ecf6176f54f240aa48680
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499252"
---
# <a name="about-wsl-2"></a>À propos de WSL 2

WSL 2 est une nouvelle version de l’architecture qui alimente le sous-système Windows pour Linux afin d’exécuter des binaires ELF64 Linux sur Windows. Ses principaux objectifs consistent à augmenter les performances du système de fichiers, ainsi qu’à ajouter la compatibilité complète des appels système. Cette nouvelle architecture modifie la façon dont ces fichiers binaires Linux interagissent avec Windows et le matériel de votre ordinateur, mais offre toujours la même expérience utilisateur que dans WSL 1 (la version actuellement largement disponible). Les distributions Linux individuels peuvent être exécutés en tant que WSL 1 distribution, ou WSL 2 distribution, peuvent être mis à niveau ou rétrogradés à tout moment, et vous pouvez exécuter WSL 1 et WSL 2 distributions côte à côte. WSL 2 utilise une architecture entièrement nouvelle qui utilise un véritable noyau Linux.

## <a name="linux-kernel-in-wsl-2"></a>Noyau Linux dans WSL 2

Le noyau Linux dans WSL 2 est intégré à partir de la dernière branche stable, en fonction de la source disponible sur kernel.org. Ce noyau a été spécialement réglé pour WSL 2. Il a été optimisé pour la taille et les performances afin d’offrir une expérience Linux exceptionnelle sur Windows et sera géré par le biais des mises à jour Windows, ce qui signifie que vous obtiendrez les derniers correctifs de sécurité et les améliorations du noyau sans avoir à le gérer vous-même.

En outre, ce noyau sera Open source. Vous pouvez trouver le code source complet pour le noyau Linux [ici](https://github.com/microsoft/WSL2-Linux-Kernel). Si vous souhaitez en savoir plus sur ce noyau, vous pouvez consulter ce billet de [blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) écrit par l’équipe qui l’a créé.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Brève présentation de l’architecture WSL 2

WSL 2 utilise la technologie de virtualisation la plus récente et la plus grande pour exécuter son noyau Linux à l’intérieur d’une machine virtuelle utilitaire légère. Toutefois, WSL 2 n’est pas une expérience de machine virtuelle traditionnelle. Une expérience de machine virtuelle traditionnelle peut être lente à démarrer, est isolée, consomme beaucoup de ressources et nécessite votre temps pour la gérer. WSL 2 n’a pas ces attributs. Il offre toujours les avantages remarquables de WSL 1: Des niveaux élevés d’intégration entre Windows et Linux, des temps de démarrage extrêmement rapides, un faible encombrement des ressources et le meilleur de tous ne nécessitent aucune configuration ou gestion de machine virtuelle. Alors que WSL 2 utilise une machine virtuelle, elle est gérée et s’exécute en arrière-plan, ce qui vous laisse la même expérience utilisateur que WSL 1.

## <a name="increased-file-io-performance"></a>Amélioration des performances d’e/s de fichier

Les opérations gourmandes en fichiers telles que le clone git, l’installation NPM, la mise à jour apt, la mise à niveau de apt, etc., sont toutes beaucoup plus rapides. L’augmentation de la vitesse réelle dépend de l’application que vous exécutez et de la manière dont elle interagit avec le système de fichiers. Les versions initiales de WSL 2 s’exécutent jusqu’à 20 fois plus rapidement qu’avec WSL 1 lors de la décompression d’un tarball compressé, et environ 2 à 5 fois plus rapidement lors de l’utilisation du clone git, NPM install et cmake sur différents projets.

## <a name="full-system-call-compatibility"></a>Compatibilité complète des appels système

Les binaires Linux utilisent des appels système pour effectuer de nombreuses fonctions, telles que l’accès aux fichiers, la demande de mémoire, la création de processus et bien plus encore. Tandis que WSL 1 a utilisé une couche de traduction créée par l’équipe WSL, WSL 2 comprend son propre noyau Linux avec compatibilité complète des appels système. Cela introduit un tout nouvel ensemble d’applications que vous pouvez exécuter à l’intérieur de WSL, par exemple l’ancrage et bien plus encore. En outre, toutes les mises à jour du noyau Linux peuvent être immédiatement prêtes à être ajoutées à votre ordinateur, au lieu d’attendre que l’équipe WSL implémente les modifications, puis les ajoute.