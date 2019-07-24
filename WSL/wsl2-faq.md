---
title: Forum aux questions sur WSL 2
description: Forum aux questions sur le sous-système Windows pour Linux 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a74f5e3f5879d0af274d2e2b10aaf05e95a97a6f
ms.sourcegitcommit: e16097a3d863bbda8c4655054f154415cdd7f2f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/05/2019
ms.locfileid: "67587142"
---
# <a name="wsl-2-faq"></a>FAQ WSL 2

Vous trouverez ci-dessous une liste des questions fréquemment posées (FAQ) sur le sous-système Windows pour Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 utilise-t-il Hyper-V? Sera-t-il disponible sur Windows 10 famille?

WSL 2 sera disponible sur toutes les références SKU où WSL est actuellement disponible, y compris Windows 10 famille.

La dernière version de WSL utilise l’architecture Hyper-V pour activer sa virtualisation. Cette architecture sera disponible dans le composant facultatif «plateforme de machine virtuelle». Ce composant facultatif sera disponible sur toutes les références (SKU). Vous pouvez vous attendre à obtenir plus de détails sur cette expérience dès que nous approcherons de la version WSL 2.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>Qu’arrive-t-il à WSL 1? Va-t-il être abandonné?

Nous n’avons actuellement aucun projet de dépréciation de WSL 1. Vous pouvez exécuter WSL 1 et WSL 2 distributions côte à côte, et vous pouvez mettre à niveau et rétrograder n’importe quel distribution à tout moment. L’ajout de WSL 2 en tant que nouvelle architecture offre une meilleure plateforme permettant à l’équipe WSL de fournir des fonctionnalités qui font de WSL une façon incroyable d’exécuter un environnement Linux dans Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>Suis-je en mesure d’exécuter WSL 2 et d’autres outils de virtualisation tiers tels que VMware ou VirtualBox?

Certaines applications tierces ne fonctionnent pas quand Hyper-V est en cours d’utilisation, ce qui signifie qu’elles ne peuvent pas s’exécuter quand WSL 2 est activé. Malheureusement, cela inclut VMware, et les versions de VirtualBox antérieures à VirtualBox 6 (VirtualBox 6.0.0 publiée en décembre 2018 [prennent désormais en charge Hyper-V comme noyau d’exécution de secours sur un hôte Windows][1]!)

Nous étudions des moyens d’aider à résoudre ce problème. Par exemple, nous exposons un ensemble d’API appelé [plateforme][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s. This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3]hyperviseur, et VirtualBox 6 et versions ultérieures, qui sont désormais compatibles avec Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>Puis-je accéder au GPU dans WSL 2? Existe-t-il des plans pour augmenter la prise en charge du matériel?

Dans les versions initiales de WSL 2, la prise en charge de l’accès matériel sera limitée, par exemple: vous ne pourrez pas accéder au GPU, série ou USBs. Toutefois, l’ajout d’une meilleure prise en charge des appareils est élevé dans notre backlog, car cela ouvre beaucoup plus de cas d’utilisation pour les développeurs qui souhaitent interagir avec ces appareils. En attendant, vous pouvez toujours utiliser WSL 1, qui a un port série et un accès USB. Restez informé sur ce blog et les membres de l’équipe WSL sur Twitter pour rester informé sur les fonctionnalités les plus récentes des builds Insider et vous contacter pour nous faire part de vos commentaires sur les appareils avec lesquels vous aimeriez interagir.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 pourra-t-il utiliser des applications de mise en réseau?

Oui, dans la plupart des applications réseau sont plus rapides et plus performantes, car la compatibilité des appels système est complète. Toutefois, la nouvelle architecture utilise des composants de mise en réseau virtualisés. Cela signifie que dans les versions préliminaires initiales, WSL 2 se comportera de façon similaire à une machine virtuelle, par exemple: WSL 2 aura une adresse IP différente de celle de l’ordinateur hôte. Nous nous efforçons de faire de WSL 2 le même que WSL 1, et cela implique l’amélioration de notre histoire de mise en réseau. Nous prévoyons d’ajouter des améliorations aussi rapidement que possible, telles que l’accès à toutes les applications de mise en réseau à partir de Linux ou Windows à l’aide de localhost. Nous publierons plus de détails sur notre histoire réseau et les améliorations apportées à l’approche de la version de WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>Puis-je exécuter WSL 2 sur une machine virtuelle?

Oui. Vous devez vous assurer que la virtualisation imbriquée est activée sur l’ordinateur virtuel. Vous pouvez activer cette option dans Hyper-V en exécutant la commande suivante dans une fenêtre PowerShell avec des privilèges d’administrateur:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Veillez à remplacer «&lt;vmname&gt;» par le nom de votre machine virtuelle.

## <a name="can-i-use-wslconf-in-wsl-2"></a>Puis-je utiliser WSL. conf dans WSL 2?

WSL 2 prend en charge le même fichier WSL. conf que WSL 1 utilise. Cela signifie que toutes les options de configuration que vous aviez définies dans un distribution WSL 1, telles que le montage automatique de lecteurs Windows, l’activation ou la désactivation de l’interopérabilité, la modification du répertoire dans lequel les lecteurs Windows seront montés, etc. fonctionneront toutes dans WSL 2. Vous pouvez en savoir plus sur les options de configuration dans WSL dans la page de [gestion distribution](./wsl-config.md) . 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/