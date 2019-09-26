---
title: Créer un distribution Linux personnalisé pour WSL
description: Découvrez comment créer une distribution Linux personnalisée pour le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows, distribution, personnalisé
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 181badd4ee2f69e904099c12b54dfbdf3a37e294
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269704"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>Création d’un distribution Linux personnalisé pour WSL

Utilisez notre exemple Open source WSL pour créer des packages WSL distribution pour le Microsoft Store et/ou pour créer des packages distribution Linux personnalisés pour chargement. Vous pouvez trouver [distribution Launcher référentiel](https://github.com/Microsoft/WSL-DistroLauncher) sur GitHub.

Ce projet active les éléments suivants :
* Maintenance de la distribution Linux pour empaqueter et soumettre une distribution Linux sous la forme d’un fichier AppX qui s’exécute sur WSL
* Développeurs pour créer des distributions Linux personnalisées qui peuvent être faisant sur leur ordinateur de développement

## <a name="background"></a>Présentation
Nous distribuons Linux distributions pour WSL en tant qu’applications UWP par le biais du Microsoft Store. Vous pouvez installer ces applications qui s’exécuteront ensuite sur WSL-le sous-système qui se trouve dans le noyau Windows. Ce mécanisme de remise présente de nombreux avantages, comme indiqué dans un [billet de blog précédent](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).

## <a name="sideloading-a-custom-linux-distro-package"></a>Chargement un package distribution Linux personnalisé
Vous pouvez créer un package distribution Linux personnalisé en tant qu’application pour chargement sur votre ordinateur personnel. Notez que votre package personnalisé n’est pas distribué via le Microsoft Store, sauf si vous soumettez en tant que chargé de maintenance de la distribution.
Pour configurer votre ordinateur pour chargement des applications, vous devez l’activer dans les paramètres système sous « pour les développeurs ».  Assurez-vous que vous avez sélectionné le mode développeur ou les applications chargement

## <a name="for-linux-distro-maintainers"></a>Pour les Maintenateurs Linux distribution
Pour envoyer un message au magasin, vous devez nous contacter pour recevoir l’approbation de la publication. Si vous êtes un propriétaire de distribution Linux désireux d’ajouter votre distribution à la Microsoft Store, contactez wslpartners@microsoft.com.

## <a name="getting-started"></a>Prise en main
Suivez les instructions du [distribution Launcher GitHub référentiel](https://github.com/Microsoft/WSL-DistroLauncher) pour créer un package distribution Linux personnalisé.

 
## <a name="team-blogs"></a>Blogs de l’équipe
*  [Open source-exemple WSL pour les préserveurs de distribution Linux et les distributions Linux personnalisées chargement](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [Blog de ligne de commande](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Commentaires
* [Distribution Launcher GitHub référentiel](https://github.com/Microsoft/WSL-DistroLauncher)
* [GitHub Issue Tracker pour WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [Portail UserVoice de la ligne de commande](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
