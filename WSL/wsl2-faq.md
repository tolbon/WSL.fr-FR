---
title: Questions fréquentes (FAQ) sur WSL 2
description: Questions fréquentes relatives au sous-système Windows pour Linux 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 35edad06775e75eef6d81d018355d8f28d772deb
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235892"
---
# <a name="wsl-2-faqs"></a>FAQ WSL 2

Vous trouverez ci-dessous une liste de questions fréquemment posées (FAQ) sur le sous-système Windows pour Linux 2.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 utilise-t-il Hyper-V ? Sera-t-il disponible sur Windows 10 Famille ?

WSL 2 sera disponible sur toutes les références SKU où WSL est actuellement disponible, y compris Windows 10 Famille.

La dernière version de WSL utilise l’architecture Hyper-V pour activer sa virtualisation. Cette architecture sera disponible dans le composant facultatif « Plateforme de machine virtuelle ». Ce composant facultatif sera disponible sur toutes les références SKU. Vous pouvez vous attendre à obtenir plus de détails sur cette expérience quand nous approcherons de la version WSL 2.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>Qu’arrivera-t-il à WSL 1 ? Sera-t-il abandonné ?

Nous n’avons actuellement aucun projet de dépréciation de WSL 1. Vous pouvez exécuter les distributions WSL 1 et WSL 2 côte à côte, et vous pouvez mettre à niveau et rétrograder n’importe quelle distribution à tout moment. L’ajout de WSL 2 comme nouvelle architecture offre une meilleure plateforme permettant à l’équipe WSL de fournir des fonctionnalités qui font de WSL un outil optimal pour exécuter un environnement Linux dans Windows.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>Est-il possible d’exécuter WSL 2 et d’autres outils de virtualisation tiers tels que VMware ou VirtualBox ?

Certaines applications tierces ne fonctionnent pas quand Hyper-V est en cours d’utilisation, ce qui signifie qu’elles ne pourront pas s’exécuter quand WSL 2 est activé, comme VMware et VirtualBox. Toutefois, récemment, VirtualBox et VMware ont tous deux publié des versions qui prennent en charge Hyper-V et WSL2 ! Vous pouvez en savoir plus sur les [changements de VirtualBox ici][1] et sur les [changements de VMware ici][4].

Nous étudions des moyens qui contribueront à résoudre ce problème. Par exemple, nous exposons un ensemble d’API appelé [Plateforme hyperviseur][2] que les fournisseurs de virtualisation tiers pourront utiliser pour rendre leurs logiciels compatibles avec ceux d’Hyper-V. Cela permet aux applications d’utiliser l’architecture Hyper-V pour leur émulation, comme [l’émulateur Google Android][3] et VirtualBox 6 et ultérieur, qui sont désormais compatibles avec Hyper-V.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>Puis-je accéder au GPU dans WSL 2 ? Existe-t-il des plans pour améliorer la prise en charge du matériel ?

Dans les versions initiales de WSL 2, la prise en charge de l’accès matériel sera limitée, par exemple : vous ne pourrez pas accéder aux périphériques USB, série ni GPU. Toutefois, l’ajout d’une meilleure prise en charge des appareils est haut placé dans notre backlog, car cela ouvre beaucoup plus de cas d’utilisation pour les développeurs qui souhaitent interagir avec ces appareils. En attendant, vous pouvez toujours utiliser WSL 1 qui a accès au port série. Suivez sur ce blog et les membres de l’équipe WSL sur Twitter pour rester informé des dernières fonctionnalités introduites sur les builds Insider et faites-nous part de vos commentaires sur les appareils avec lesquels vous aimeriez interagir.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 pourra-t-il utiliser des applications réseau ?

Oui, en général, les applications réseau sont plus rapides et plus performantes, car la compatibilité des appels système est complète. Toutefois, la nouvelle architecture utilise des composants de réseau virtualisés. Cela signifie que dans les versions d’évaluation initiales, WSL 2 se comportera d’une façon plus similaire à une machine virtuelle, par exemple : WSL 2 aura une adresse IP différente de celle de l’ordinateur hôte. Nous nous efforçons de vous fournir avec WSL 2 une expérience similaire à celle que vous aviez avec WSL 1, et cela implique l’amélioration de notre histoire de réseau. Nous prévoyons d’ajouter des améliorations dès que possible, telles que l’accès à toutes les applications réseau à partir de Linux ou de Windows à l’aide de localhost. Nous publierons plus de détails sur notre histoire de réseau et les améliorations apportées au fur et à mesure que nous approcherons de la publication de WSL 2.

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>Puis-je exécuter WSL 2 sur une machine virtuelle ?

Oui. Vous devez vous assurer que la virtualisation imbriquée est activée sur la machine virtuelle. Vous pouvez l’activer dans votre hôte Hyper-V parent en exécutant la commande suivante dans une fenêtre PowerShell avec des privilèges d’administrateur :

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Veillez à remplacer « &lt;VMName&gt; » par le nom de votre machine virtuelle.

## <a name="can-i-use-wslconf-in-wsl-2"></a>Puis-je utiliser wsl.conf dans WSL 2 ?

WSL 2 prend en charge le même fichier wsl.conf que WSL 1 utilise. Cela signifie que toutes les options de configuration que vous aviez définies dans une distribution WSL 1, telles que le montage automatique de lecteurs Windows, l’activation ou la désactivation de l’interopérabilité, le changement du répertoire où les lecteurs Windows sont montés, etc., fonctionneront aussi dans WSL 2. Vous pouvez en apprendre davantage sur les options de configuration dans WSL dans la page [Gestion des distributions](./wsl-config.md).

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
 [4]: https://blogs.vmware.com/workstation/2020/01/vmware-workstation-tech-preview-20h1.html