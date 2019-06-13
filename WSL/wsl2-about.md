---
title: À propos de WSL 2
description: À propos de 2 WSL la nouvelle architecture pour le sous-système Windows pour Linux
keywords: BashOnWindows, bash, wsl, wsl2, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, installer
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038129"
---
WSL 2 est une nouvelle version de l’architecture qui alimente le sous-système Windows pour Linux exécuter des fichiers binaires ELF64 Linux sur Windows. Ses principaux objectifs sont d’augmenter les performances du système de fichiers, ainsi que l’ajout de compatibilité d’appel complète du système. Cette nouvelle architecture modifie la façon dont ces fichiers binaires Linux interagissent avec Windows et le matériel de votre ordinateur, mais qui constitue la même expérience utilisateur, comme dans WSL 1 (la version largement disponible actuelle). Linux individuel distributions peuvent être exécutées comme un distributeur WSL 1, ou comme un distributeur WSL 2, peut être mis à niveau ou rétrogradée à tout moment, et vous pouvez exécuter des distributions WSL 1 et 2 de WSL côte à côte. WSL 2 utilise une architecture entièrement nouvelle qui utilise un noyau Linux réel.

## <a name="linux-kernel-in-wsl-2"></a>Noyau Linux dans WSL 2

Le noyau Linux WSL 2 est généré en interne à partir de la branche stable plus récente, basée sur la source disponible à l’adresse kernel.org. Ce noyau a été spécialement réglé pour WSL 2. Il a été optimisé pour la taille et de performances pour donner une expérience exceptionnelle de Linux sur Windows et puisse être traitée par le biais des mises à jour Windows, ce qui signifie que vous obtenez les derniers correctifs de sécurité et les améliorations du noyau sans avoir à gérer vous-même.

En outre, ce noyau seront open source. Vous trouverez le code source complet pour le noyau Linux [ici](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip). Si vous souhaitez en savoir plus sur ce noyau, vous pouvez consulter [ce billet de blog](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) rédigé par l’équipe qui a créé l’application.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Vue d’ensemble de l’architecture WSL 2

WSL 2 utilise les dernières nouveautés dans la technologie de virtualisation pour exécuter son noyau Linux à l’intérieur d’une machine virtuelle d’utilitaire léger (VM). Toutefois, WSL 2 ne sera pas une expérience de machine virtuelle classique. Une expérience de machine virtuelle classique peut être lente à démarrer est isolée, consomme beaucoup de ressources et nécessite votre temps pour le gérer. WSL 2 n’a pas de ces attributs. Il présente les avantages remarquables WSL 1 : Des niveaux élevés d’intégration entre Windows et Linux, temps de démarrage extrêmement rapides, faible encombrement de ressource et surtout ne nécessitera aucune configuration de machine virtuelle ou de gestion. Tandis que les 2 WSL utilise une machine virtuelle, il sera géré et exécuter en arrière-plan en vous laissant avec la même expérience utilisateur en tant que WSL 1.

## <a name="increased-file-io-performance"></a>Les performances d’e/s de fichier accrue

Opérations intensives du fichier comme git clone, installation npm, mise à jour apt, apt mise à niveau et bien plus encore seront tous sensiblement plus rapide. L’augmentation de la vitesse réelle varie sur quelle application que vous êtes en cours d’exécution et la façon dont il interagit avec le système de fichiers. Versions initiales des WSL 2 exécutent jusqu'à 20 fois plus rapide comparé à WSL 1 lors de la décompression d’une archive tar compressée, autour de 2 à 5 fois plus rapide lors de l’utilisation de clone git, installation npm et cmake sur divers projets.

## <a name="full-system-call-compatibility"></a>Compatibilité des appels complète du système

Les fichiers binaires Linux utilisent des appels système pour effectuer de nombreuses fonctions telles que l’accès aux fichiers, la demande de mémoire, la création de processus et bien plus encore. Tandis que WSL 1 utilisé dans une couche de traduction qui a été créée par l’équipe WSL, WSL 2 inclut son propre noyau Linux avec la compatibilité des appels complète du système. Cela introduit un nouvel ensemble d’applications que vous pouvez exécuter à l’intérieur de WSL, tels que Docker et bien plus encore. En outre, les mises à jour le noyau Linux peuvent être immédiatement prêts à être ajouté à votre ordinateur, au lieu d’attendre de l’équipe WSL implémenter les modifications, puis les ajouter.