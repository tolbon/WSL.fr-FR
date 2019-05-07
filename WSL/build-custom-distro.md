---
title: Créer une distribution Linux personnalisée pour WSL
description: Découvrez comment créer une distribution Linux personnalisée pour le sous-système de Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows, distributeur, personnalisé
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063257"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>Création d’une distribution Linux personnalisée pour WSL

Utilisez notre exemple WSL open source pour créer des packages de distribution WSL pour le Microsoft Store et/ou pour créer des packages de distribution Linux personnalisés pour le chargement indépendant. Vous pouvez trouver la [référentiel de lanceur distributeur](https://github.com/Microsoft/WSL-DistroLauncher) sur GitHub.

Ce projet permet de :
* Les chargés de maintenance de distribution Linux pour empaqueter et soumettre une distribution Linux comme un appx qui s’exécute sur WSL
* Aux développeurs de créer des distributions de Linux qui peuvent être chargées indépendamment sur son ordinateur de développement

## <a name="background"></a>Arrière-plan
Nous distribuons des distributions Linux pour WSL en tant qu’applications UWP via le Microsoft Store. Vous pouvez installer les applications qui pourra ensuite s’exécuter sur WSL - le sous-système qui se trouve dans le noyau Windows. Ce mécanisme de livraison présente de nombreux avantages comme indiqué dans un billet de blog antérieures.

## <a name="sideloading-a-custom-linux-distro-package"></a>Chargement de version test un Package de distribution Linux personnalisée
Vous pouvez créer un package de distribution Linux personnalisé en tant qu’application à charger une version test sur votre ordinateur personnel. Veuillez noter que votre package personnalisé ne serait pas distribué via le Microsoft Store, sauf si vous envoyez en tant que responsable de maintenance de la distribution.
Pour configurer votre ordinateur pour supprimer des applications, vous devez l’activer sur les paramètres du système sous « Pour les développeurs ».  Veillez à avoir mode développeur, ou supprimer des applications sélectionnées

## <a name="for-linux-distro-maintainers"></a>Pour une distribution Linux chargés de maintenance
Pour envoyer vers le Store, vous devrez collaborer avec nous pour recevoir l’approbation de publication. Si vous êtes propriétaire d’une distribution Linux intéressé par l’ajout de votre distribution pour le Microsoft Store, contactez wslpartners@microsoft.com.

## <a name="getting-started"></a>Prise en main
Suivez les instructions la [référentiel GitHub de lanceur distributeur](https://github.com/Microsoft/WSL-DistroLauncher) pour créer un package de distribution Linux personnalisé.

 
## <a name="team-blogs"></a>Blogs de l’équipe
*  [Ouvrez l’approvisionnement en un exemple WSL pour chargés de maintenance de Distribution Linux et les Distributions de Linux personnalisée de chargement de version test](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [Blog de ligne de commande](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Commentaires
* [Référentiel de distributeur Lanceur Github](https://github.com/Microsoft/WSL-DistroLauncher)
* [Suivi des problèmes GitHub pour WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [Portail de UserVoice de ligne de commande](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
