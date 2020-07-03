---
title: Vue d’ensemble du sous-système Windows pour Linux
description: Découvrez le sous-système Windows pour Linux, les différentes versions et les différentes façons de les utiliser.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, GNU, Linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 75da6389beec4af7ac684ec7ee2ef31431e14071
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336062"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>Qu’est-ce que le sous-système Windows pour Linux ?

Le Sous-système Windows pour Linux permet aux développeurs d’exécuter un environnement GNU/Linux (et notamment la plupart des utilitaires, applications et outils en ligne de commande) directement sur Windows, sans modification et tout en évitant la surcharge d’une machine virtuelle traditionnelle ou d’une configuration à double démarrage.

Vous pouvez :

* Choisir vos distributions GNU/Linux préférées à partir du [Microsoft Store](https://aka.ms/wslstore)
* Exécuter des outils en ligne de commande courants tels que `grep`, `sed` et `awk`, ou d’autres fichiers binaires ELF-64.
* Exécuter des scripts de shell Bash et des applications en ligne de commande GNU/Linux, notamment :  
    * Outils : vim, emacs, tmux
    * Langages : [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc.
    * Services : SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).
* Installer des logiciels supplémentaires en utilisant votre propre gestionnaire de package de distribution GNU/Linux
* Appeler des applications Windows à l’aide d’un shell de ligne de commande de type UNIX
* Appeler des applications GNU/Linux sur Windows

## <a name="what-is-wsl-2"></a>Qu’est-ce que WSL 2 ?

WSL 2 est une nouvelle version de l’architecture du sous-système Windows pour Linux qui sous-tend le sous-système Windows pour Linux afin d’exécuter les binaires ELF64 Linux sur Windows. Ses principaux objectifs consistent à **augmenter les performances du système de fichiers**, ainsi qu’à ajouter la **compatibilité complète des appels système**.

Cette nouvelle architecture change la façon dont ces fichiers binaires Linux interagissent avec Windows et votre matériel informatique, mais offre toujours la même expérience utilisateur que dans WSL 1 (la version actuellement largement disponible).

Les distributions Linux individuelles peuvent être exécutées avec l’architecture WSL 1 ou WSL 2. Chaque distribution peut être mise à niveau ou rétrogradée à tout moment et vous pouvez exécuter des distributions WSL 1 et WSL 2 côte à côte. WSL 2 exploite une architecture entièrement nouvelle qui tire profit de l’exécution d’un véritable noyau Linux.

## <a name="next-steps"></a>Étapes suivantes

* [Installer WSL 1 et le mettre à jour vers WSL 2](./install-win10.md)

* [Comparer WSL 2 et WSL 1](./compare-versions.md)

* [Créer un compte d’utilisateur et un mot de passe pour votre nouvelle distribution Linux](./user-support.md)

* [Consulter les questions fréquentes](./faq.md)

* [Consulter les questions fréquentes sur WSL 2](./wsl2-faq.md)

* [Résolution des problèmes](./troubleshooting.md)

* [Exécuter des commandes d’interopérabilité entre Windows et Linux](./interop.md)

* [Exécuter des commandes et des configurations de lancement](./wsl-config.md)

* [Configurer les autorisations de fichier](./file-permissions.md)

* [Configurer WSL pour les entreprises](./enterprise.md)

* [Référencer les commandes WSL](./reference.md)

* [Créer une distribution personnalisée](./build-custom-distro.md)

* [Consulter les notes de publication de WSL](./release-notes.md)
