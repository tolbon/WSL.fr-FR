---
title: À propos de WSL 2
description: À propos de WSL 2, la nouvelle architecture du sous-système Windows pour Linux
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7122fcbd73e064871eba2ac80c727178aaf3ca7b
ms.sourcegitcommit: 5c92b820f84de57a04ab11faf4dd0d24fff6b320
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2019
ms.locfileid: "74161479"
---
# <a name="about-wsl-2"></a>À propos de WSL 2

WSL 2 est une nouvelle version de l’architecture qui sous-tend le sous-système Windows pour Linux afin d’exécuter les binaires ELF64 Linux sur Windows. Ses principaux objectifs consistent à augmenter les performances du système de fichiers, ainsi qu’à ajouter la compatibilité complète des appels système. Cette nouvelle architecture change la façon dont ces fichiers binaires Linux interagissent avec Windows et votre matériel informatique, mais offre toujours la même expérience utilisateur que dans WSL 1 (la version actuellement largement disponible). Les distributions Linux individuelles peuvent être exécutées en tant que distributions WSL 1 ou distributions WSL 2, elles peuvent être mises à niveau ou rétrogradées à tout moment, et vous pouvez exécuter des distributions WSL 1 et WSL 2 côte à côte. WSL 2 exploite une architecture entièrement nouvelle qui utilise un véritable noyau Linux.

## <a name="linux-kernel-in-wsl-2"></a>Noyau Linux dans WSL 2

Le noyau Linux dans WSL 2 est élaboré en interne à partir de la dernière branche stable, en fonction de la source disponible sur kernel.org. Ce noyau a été spécialement réglé pour WSL 2. Sa taille et ses performances ont été optimisées afin d’offrir une expérience Linux exceptionnelle sur Windows et il sera géré par le biais des mises à jour Windows, ce qui signifie que vous obtiendrez les derniers correctifs de sécurité et les dernières améliorations du noyau sans avoir à gérer cela vous-même.

De plus, ce noyau sera open source. Vous trouverez le code source complet pour le noyau Linux [ici](https://github.com/microsoft/WSL2-Linux-Kernel). Si vous souhaitez en savoir plus sur ce noyau, vous pouvez consulter [cette publication](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) rédigée par l’équipe qui l’a créé.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Brève présentation de l’architecture WSL 2

WSL 2 utilise la technologie de virtualisation la plus récente et la plus efficace pour exécuter son noyau Linux au sein d’une machine virtuelle utilitaire légère. Toutefois, WSL 2 n’est PAS une expérience de machine virtuelle traditionnelle. Une expérience de machine virtuelle traditionnelle peut être lente à démarrer, est isolée, consomme beaucoup de ressources et vous prend du temps pour la gérer. WSL 2 n’a pas ces attributs, mais offre les avantages remarquables de WSL 1 : de hauts niveaux d’intégration entre Windows et Linux, des temps de démarrage extrêmement courts, un faible encombrement des ressources et, par-dessus tout, ne nécessite aucune configuration ni gestion de machine virtuelle. WSL 2 utilise une machine virtuelle, mais celle-ci est gérée et exécutée en arrière-plan, ce qui vous permet de jouir de la même expérience utilisateur qu’avec WSL 1.

## <a name="increased-file-io-performance"></a>Amélioration des performances d’E/S de fichier

Les opérations gourmandes en fichiers, telles que `git clone`, `npm install`, `apt update`, `apt upgrade`, entre autres, sont toutes nettement plus rapides. L’augmentation de la vitesse réelle dépend de l’application que vous exécutez et de la manière dont elle interagit avec le système de fichiers. Les versions initiales de WSL 2 s’exécutent jusqu’à 20 fois plus vite que WSL 1 lors de la décompression d’un tarball compressé, et environ 2 à 5 fois plus vite lors de l’utilisation de `git clone`, `npm install` et `cmake` sur divers projets.

## <a name="full-system-call-compatibility"></a>Compatibilité complète des appels système

Les binaires Linux utilisent des appels système pour effectuer de nombreuses fonctions, telles que l’accès aux fichiers, la demande de mémoire, la création de processus et bien plus encore. Alors que WSL 1 utilisait une couche de traduction créée par l’équipe WSL, WSL 2 inclut son propre noyau Linux avec compatibilité complète des appels système. Cela introduit un tout nouvel ensemble d’applications que vous pouvez exécuter au sein de WSL, telles que Docker et plus encore. En outre, toutes les mises à jour du noyau Linux pourront être prêtes à être ajoutées immédiatement à votre ordinateur et vous n’aurez plus besoin d’attendre que l’équipe WSL implémente les modifications pour les ajouter.