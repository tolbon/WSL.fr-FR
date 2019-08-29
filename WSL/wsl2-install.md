---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 6b7ed18480ea88200d00b67a3a6dc859947397db
ms.sourcegitcommit: 6f10b40f6199538c8eedf6301f02b7d70ead3fe7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70117835"
---
# <a name="installation-instructions-for-wsl-2"></a>Instructions d’installation pour WSL 2

Pour installer et commencer à utiliser WSL 2, effectuez les étapes suivantes :

- Vérifiez que vous avez installé WSL (vous trouverez des instructions pour le faire [ici](./install-win10.md)) et que vous exécutez Windows 10 Build 18917 ou une version ultérieure.
   - Pour vous assurer que vous utilisez la version 18917 ou une version ultérieure, rejoignez [le programme Windows](https://insider.windows.com/en-us/) Insider et sélectionnez l’anneau «Fast». 
   - Vous pouvez vérifier votre version de Windows en ouvrant l’invite de commandes `ver` et en exécutant la commande.
- Activer le composant facultatif « Plateforme de machine virtuelle »
- Définir une distribution basée sur WSL 2 en utilisant la ligne de commande
- Vérifier les versions de WSL que vos distributions utilisent

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Activer le composant facultatif « Plateforme de machine virtuelle »

Ouvrez PowerShell en tant qu’administrateur et exécutez :

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

Une fois que ces changements sont activés, vous devez redémarrer votre ordinateur.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Définir une distribution basée sur WSL 2 en utilisant la ligne de commande

Dans PowerShell, exécutez :

`wsl --set-version <Distro> 2`

et veillez à remplacer `<Distro>` par le vrai nom de votre distribution. (Vous pouvez le trouver avec la commande : `wsl -l`). Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».

Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :

`wsl --set-default-version 2`

Ainsi, toutes les nouvelles distributions que vous installerez seront initialisées en tant que distributions WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Pour terminer, vérifiez quelles versions de WSL utilisent vos distributions.

Pour vérifier quelles versions de WSL utilise chaque distribution, utilisez la commande suivante :

`wsl --list --verbose` ou `wsl -l -v`

La distribution que vous avez choisie ci-dessus doit maintenant afficher un « 2 » dans la colonne « version ». Maintenant que vous avez terminé, n’hésitez pas à commencer à utiliser votre distribution WSL 2 ! 

## <a name="troubleshooting"></a>Résolution des problèmes : 

Vous trouverez ci-dessous des erreurs associées et des suggestions de correction lors de l’installation de WSL 2. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir d’autres erreurs WSL générales et leurs solutions.

* **Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**
    * Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur. Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.
   
* **Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez Windows version de build 18917 ou ultérieure. Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).