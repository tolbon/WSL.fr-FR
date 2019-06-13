---
title: Questions fréquentes sur WSL 2
description: Forum aux Questions sur le sous-système Windows pour Linux 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, installer
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038089"
---
# <a name="wsl-2-faq"></a>FORUM AUX QUESTIONS WSL 2

Voici une liste de questions fréquemment posées (FAQ) sur le sous-système Windows pour Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 utilise-t-elle Hyper-V ? Il sera disponible sur Windows 10 famille ?

WSL 2 seront disponibles sur toutes les références où WSL est actuellement disponible, y compris Windows 10 Édition familiale.

La dernière version de WSL utilise l’architecture Hyper-V pour permettre sa virtualisation. Cette architecture seront disponible dans un composant facultatif qui est un sous-ensemble de la fonctionnalité Hyper-V. Ce composant sera disponible sur toutes les références. Vous pouvez vous attendre afficher plus de détails sur cette expérience dès que nous approcherons de la version 2 de WSL.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>Que se passera-t-il pour WSL 1 ? Sera être abandonné ?

Nous ne disposons actuellement aucuns prévu de déprécier WSL 1. Vous pouvez exécuter WSL 1 et 2 de WSL distributions côte à côte et peut mettre à niveau et rétrograder n’importe quelle distribution à tout moment. Ajout de WSL 2 en tant qu’une nouvelle architecture présente une meilleure plateforme pour l’équipe WSL fournir des fonctionnalités qui rendent WSL un moyen de fantastique d’exécuter un environnement Linux dans Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>J’ai sera en mesure d’exécuter WSL 2 et autres outils de virtualisation tiers 3e telles que VMware ou VirtualBox ?

Certaines applications tiers 3e ne fonctionnent pas lorsque Hyper-V est en cours d’utilisation, ce qui signifie qu’ils ne seront pas en mesure d’exécuter lorsque WSL 2 est activé. Malheureusement, cela inclut VMware et les versions de VirtualBox avant VirtualBox 6 (VirtualBox 6.0.0 publiée en décembre 2018 [prend désormais en charge Hyper-V comme un cœur de l’exécution de secours sur un ordinateur hôte Windows] [ 1]!)

Nous étudions des moyens pour aider à résoudre ce problème. Par exemple, nous exposer un ensemble d’API appelées [plate-forme hyperviseur] [ 2] que les fournisseurs de virtualisation de fournisseurs tiers peuvent utiliser pour rendre leurs logiciels compatibles avec Hyper-V Cela permet aux applications d’utiliser l’architecture de Hyper-V pour leur émulation comme [l’émulateur Google Android][3], VirtualBox 6 et au-dessus de laquelle sont désormais compatibles avec Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>Puis-je accéder à la GPU dans WSL 2 ? Existe-t-il des plans pour augmenter la prise en charge matérielle ?

Dans les versions initiales de l’accès au matériel de WSL 2 prise en charge sera limitée, par exemple : vous ne pourrez pas accès GPU, série ou USB. Toutefois, ajouter une meilleure prise en charge de périphériques est élevée sur notre backlog, comme s’ouvre plus de nombreux cas d’utilisation pour les développeurs désireux d’interagir avec ces périphériques. En attendant, vous pouvez toujours utiliser 1 WSL qui possède un accès USB et port série. Veuillez Restez informé sur ce blog et les membres de l’équipe WSL sur Twitter pour rester informé sur les dernières fonctionnalités à venir pour insider génère et contacter envoyez-nous vos commentaires sur les appareils que vous souhaitez interagir avec !

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 sera en mesure d’utiliser des applications de gestion réseau ?

Oui, mise en réseau en général des applications sera plus rapide et mieux travailler, puisque nous avons complète du système pour appeler la compatibilité. Toutefois, la nouvelle architecture utilise des composants de réseau virtualisés. Cela signifie qu’en version préliminaire initiale génère WSL 2 se comporte plus de la même façon à une machine virtuelle, par exemple : WSL 2 aura une adresse IP différente de l’ordinateur hôte. Nous nous engageons à rendre WSL 2 semble identique à WSL 1, et qui inclut l’amélioration de notre histoire de mise en réseau. Nous prévoyons d’ajouter des améliorations aussi rapidement que nous ne pouvons, telles que l’accès à toutes les applications de mise en réseau à partir de Linux ou Windows à l’aide de localhost. Publierons plus d’informations sur notre histoire et améliorations de mise en réseau l’approche de la version de WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>Puis-je exécuter WSL 2 sur une machine virtuelle ?

Oui ! Vous devez vous assurer que la machine virtuelle a imbriqués activés pour la virtualisation. Cette option peut être activée dans Hyper-V en exécutant la commande suivante dans une fenêtre PowerShell avec des privilèges d’administrateur :

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Veillez à remplacer «&lt;VMName&gt;» avec le nom de votre machine virtuelle.

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/