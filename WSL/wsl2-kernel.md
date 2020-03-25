---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: a1a2f23fb05c426f80878e12e82026a96c71354e
ms.sourcegitcommit: 4b7b8bb0ac20c2336fcdbf44e6b3b2ed336bf4d6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2020
ms.locfileid: "79447745"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Mise à jour du noyau Linux WSL 2

Pour mettre à jour manuellement le noyau Linux dans WSL 2, suivez ces étapes. 

## <a name="download-the-linux-kernel-update-package"></a>Télécharger le package de mise à jour du noyau Linux

Cliquez sur [ce lien](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour télécharger le dernier package de mise à jour du noyau Linux WSL2 pour les machines x64.

> [!NOTE] 
> Si vous utilisez un ordinateur ARM64, téléchargez [ce package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) à la place.

## <a name="install-the-linux-kernel-update-package"></a>Installer le package de mise à jour du noyau Linux

Pour installer le package de mise à jour du noyau Linux :

    1. Exécutez le package de mise à jour téléchargé à l’étape précédente.
    2. Des autorisations élevées vous sont demandées, sélectionnez « Oui » pour approuver cette installation.
    3. Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2 !

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Plans à venir pour la mise à jour du noyau Linux WSL2

Pour plus d’informations sur ces changements, consultez [ce billet de blog](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) sur le [blog de la ligne de commande Windows](https://aka.ms/cliblog).
