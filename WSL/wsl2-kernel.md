---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: wsl, windows, noyau linux, sous-système windows pour linux, noyau
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: bef722f5653380d9f6d104f1a7c116a7599658c9
ms.sourcegitcommit: ba52d673c123fe8ae61e872a33e218cfc30a1f82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033044"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Mise à jour du noyau Linux WSL 2

Pour mettre à jour manuellement le noyau Linux dans WSL 2, suivez ces étapes.

> [!NOTE] 
> Si le programme d’installation ne trouve pas WSL 1, cliquez avec le bouton droit sur le programme d’installation de la mise à jour du noyau Linux et réexécutez-le.

## <a name="download-the-linux-kernel-update-package"></a>Télécharger le package de mise à jour du noyau Linux

[Téléchargez le dernier package de mise à jour du noyau Linux WSL2](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour les machines x64.

> [!NOTE]
> Si vous utilisez une machine ARM64, téléchargez le [package ARM64](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) à la place.

## <a name="install-the-linux-kernel-update-package"></a>Installer le package de mise à jour du noyau Linux

Pour installer le package de mise à jour du noyau Linux :

  1. Exécutez le package de mise à jour téléchargé à l’étape précédente.

  2. Des autorisations élevées vous sont demandées, sélectionnez « Oui » pour approuver cette installation.

  3. Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2 !

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Plans à venir pour la mise à jour du noyau Linux WSL2

Pour plus d’informations, consultez l’article sur les [changements apportés à la mise à jour du noyau Linux WSL2](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), disponible sur le [blog de la ligne de commande Windows](https://aka.ms/cliblog).

## <a name="troubleshooting"></a>Résolution des problèmes

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a>Cette mise à jour s’applique seulement aux machines avec le sous-système Windows pour Linux
Pour installer le noyau MSI, WSL est nécessaire et doit être activé en premier. En cas d’échec, le message suivant s’affiche : `This update only applies to machines with the Windows Subsytem for Linux`. 

Ce message apparaît pour trois raisons possibles :

1. Vous êtes toujours dans une ancienne version de Windows qui ne prend pas en charge WSL 2. Vérifiez les [exigences de WSL 2](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) et effectuez une mise à niveau pour utiliser WSL 2. 
2. `Windows Subsystem for Linux` n’est pas activé. Suivez le [Guide d’installation du sous-système Windows pour Linux](https://docs.microsoft.com/windows/wsl/install-win10).
3. Une fois que vous avez activé `Windows Subsystem for Linux`, un redémarrage est nécessaire pour sa prise en compte : redémarrez votre machine, puis réessayez.

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

Chaque fois que le noyau est manquant dans %SystemRoot%\system32\lxss\tools\,, vous pouvez rencontrer l’erreur ci-dessus.

Voici quelques moyens possibles de la résoudre :

1. Installez le noyau Linux manuellement en suivant les instructions fournies dans : https://aka.ms/wsl2kernel
2. Désinstallez le MSI dans « Ajout/suppression de programmes », puis réinstallez-le.
