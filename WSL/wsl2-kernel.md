---
title: Mise à jour du noyau Linux WSL 2
description: Instructions sur la mise à jour manuelle de votre noyau Linux WSL 2
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138188"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Mise à jour du noyau Linux WSL 2

Pour mettre à jour manuellement le noyau Linux à l’intérieur de WSL 2, procédez comme suit. 

## <a name="download-the-linux-kernel-update-package"></a>Télécharger le package de mise à jour du noyau Linux

Cliquez sur [ce lien](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) pour télécharger le dernier package de mise à jour du noyau WSL2 Linux pour les machines amd64.

> [!NOTE] Si vous utilisez une machine ARM64, téléchargez [ce package à la](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) place.

## <a name="install-the-linux-kernel-update-package"></a>Installer le package de mise à jour du noyau Linux

Pour installer le package de mise à jour du noyau Linux :
    1. Exécutez le package de mise à jour téléchargé à l’étape précédente.
    2. Vous serez invité à fournir des autorisations élevées, sélectionner « Oui » pour approuver cette installation.
    3. Une fois l’installation terminée, vous pouvez commencer à utiliser WSL2.

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Plans futurs pour la mise à jour du noyau Linux WSL2

Pour plus d’informations sur ces modifications, consultez [ce](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) billet de blog sur le blog de la [ligne de commande Windows](https://aka.ms/cliblog).