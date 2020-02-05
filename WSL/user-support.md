---
title: Créer et mettre à jour des comptes d’utilisateur pour les distributions WSL
description: Informations de référence sur les comptes d’utilisateur et la gestion des autorisations avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, comptes d’utilisateur
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: e5fb773dd44abab7bcf289340da00f59528b88f7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/03/2020
ms.locfileid: "76973679"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a>Créer et mettre à jour des comptes d’utilisateur pour les distributions WSL

Une fois que vous avez activé WSL et installé une distribution Linux à partir du Microsoft Store, la première étape qui vous est demandé d’effectuer lors de l’ouverture de la distribution Linux nouvellement installée consiste à créer un compte avec un **nom d’utilisateur** et un **mot de passe**.

- Ce **nom d’utilisateur** et ce **mot de passe** sont propres à votre distribution Linux et n’ont aucune incidence sur votre nom d’utilisateur Windows.

- Une fois que vous avez créé ce **nom d’utilisateur** et ce **mot de passe**, le compte devient votre utilisateur par défaut pour la distribution et se connecte automatiquement au démarrage.

- Ce compte est considéré comme l’administrateur Linux, avec la capacité d’exécuter des commandes d’administration `sudo` (Super User Do).

- Chaque distribution Linux exécutée sur le sous-système Windows pour Linux a ses propres comptes d’utilisateur et mots de passe Linux.  Vous devez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez, réinstallez ou réinitialisez une distribution.

## <a name="reset-your-linux-password"></a>Réinitialiser votre mot de passe Linux

Pour changer votre mot de passe, ouvrez votre distribution Linux (Ubuntu, par exemple) et entrez la commande : `passwd`

Vous êtes invité à entrer votre mot de passe actuel, à entrer votre nouveau mot de passe, puis à confirmer votre nouveau mot de passe.

### <a name="forgot-your-password"></a>Vous avez oublié votre mot de passe

Si vous avez oublié le mot de passe de votre distribution Linux :

1. Ouvrez PowerShell et entrez la racine de votre distribution WSL par défaut en utilisant la commande : `wsl -u root`

> Si vous devez mettre à jour le mot de passe oublié sur une distribution qui n’est pas celle par défaut, utilisez la commande : `wsl -d Debian -u root` en remplaçant `Debian` par le nom de votre distribution ciblée.

2. Une fois votre distribution WSL ouverte au niveau de la racine dans PowerShell, vous pouvez utiliser cette commande pour mettre à jour votre mot de passe : `passwd`

3. Vous serez invité à entrer un nouveau mot de passe UNIX, puis à confirmer ce mot de passe. Une fois que vous êtes informé que le mot de passe a été correctement mis à jour, fermez WSL dans PowerShell en utilisant la commande : `exit`

> [!NOTE]
> Si vous exécutez une version antérieure du système d’exploitation Windows, comme 1703 (Creators Update) ou 1709 (Fall Creators Update), consultez la [documentation de la version archivée de cette mise à jour de compte d’utilisateur](./user-support-archived.md).
