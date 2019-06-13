---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, installer
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038079"
---
# <a name="installation-instructions-for-wsl-2"></a>Instructions d’installation pour WSL 2

Pour installer et commencer à utiliser WSL 2 procédez comme suit :

- Activer le composant facultatif « Plateforme de Machine virtuelle »
- Définir un distributeur pour être sauvegardé par 2 WSL à l’aide de la ligne de commande
- Vérifiez que les versions de WSL vos distributions sont à l’aide de

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Activer le composant facultatif « Plateforme de Machine virtuelle »

Ouvrez PowerShell en tant qu’administrateur et exécutez :

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

Une fois ces modifications sont activées, vous devrez redémarrer votre ordinateur.

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Définir un distributeur pour être sauvegardé par 2 WSL à l’aide de la ligne de commande

Dans l’exécution de PowerShell :

`wsl --set-version <Distro> 2`

et veillez à remplacer `<Distro>` par le nom réel de votre distribution. (Vous pouvez trouver ces éléments avec la commande : `wsl -l`). Vous pouvez modifier à tout moment à 1 WSL à en exécutant la même commande que ci-dessus, mais en remplaçant ' 2' avec un ' 1'.

En outre, si vous souhaitez rendre WSL 2 votre architecture par défaut vous pouvez le faire avec cette commande :

`wsl --set-default-version 2`

Vous serez ainsi une nouvelle distribution que vous installez initialisé dans une distribution WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Terminer avec la vérification de ce que les versions de WSL votre distributeur sont à l’aide de

Pour vérifier quelles versions de chaque distributeur est à l’aide de WSL utilisent la commande suivante :

`wsl --list --verbose` ou `wsl -l -v`

La distribution que vous avez choisi ci-dessus doit maintenant s’afficher un « 2 » dans la colonne « version ». Maintenant que vous avez terminé n’hésitez pas à démarrer à l’aide de votre distribution WSL 2 ! 