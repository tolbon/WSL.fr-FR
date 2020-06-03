---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: wsl, windows, noyau linux, sous-système windows pour linux, noyau
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153050"
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
