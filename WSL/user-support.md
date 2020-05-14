---
title: Créer et mettre à jour des comptes d’utilisateur pour les distributions Linux
description: Informations de référence sur les comptes d’utilisateur et la gestion des autorisations avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, comptes d’utilisateur
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235908"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>Créer un compte d’utilisateur et un mot de passe pour votre nouvelle distribution Linux

Une fois que vous avez [activé WSL et installé une distribution Linux à partir du Microsoft Store](./install-win10.md), la première étape qu’il vous est demandé d’effectuer lors de l’ouverture de la distribution Linux nouvellement installée consiste à créer un compte avec un **nom d’utilisateur** et un **mot de passe**.

- Ce **nom d’utilisateur** et ce **mot de passe** sont propres à votre distribution Linux et n’ont aucune incidence sur votre nom d’utilisateur Windows.

- Une fois que vous avez créé ce **nom d’utilisateur** et ce **mot de passe**, le compte devient votre utilisateur par défaut pour la distribution et se connecte automatiquement au démarrage.

- Ce compte est considéré comme l’administrateur Linux, avec la capacité d’exécuter des commandes d’administration `sudo` (Super User Do).

- Chaque distribution Linux exécutée sur le sous-système Windows pour Linux a ses propres comptes d’utilisateur et mots de passe Linux.  Vous devez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez, réinstallez ou réinitialisez une distribution.

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>Mettre à jour et mettre à niveau des packages

La plupart des distributions sont livrées avec un catalogue de packages vide ou minimal. Nous vous recommandons vivement de mettre à jour régulièrement votre catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution. Pour Debian/Ubuntu, utilisez apt :

```bash
sudo apt update && sudo apt upgrade
```

Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux. Il s’agit d’une tâche que la plupart des utilisateurs Linux préfèrent contrôler eux-mêmes.

## <a name="reset-your-linux-password"></a>Réinitialiser votre mot de passe Linux

Pour changer votre mot de passe, ouvrez votre distribution Linux (Ubuntu, par exemple) et entrez la commande : `passwd`

Vous êtes invité à entrer votre mot de passe actuel, à entrer votre nouveau mot de passe, puis à confirmer votre nouveau mot de passe.

## <a name="forgot-your-password"></a>Vous avez oublié votre mot de passe

Si vous avez oublié le mot de passe de votre distribution Linux :

1. Ouvrez PowerShell et entrez la racine de votre distribution WSL par défaut en utilisant la commande : `wsl -u root`

    > Si vous devez mettre à jour le mot de passe oublié sur une distribution qui n’est pas celle par défaut, utilisez la commande : `wsl -d Debian -u root` en remplaçant `Debian` par le nom de votre distribution ciblée.

2. Une fois votre distribution WSL ouverte au niveau de la racine dans PowerShell, vous pouvez utiliser cette commande pour mettre à jour votre mot de passe : `passwd`

3. Vous serez invité à entrer un nouveau mot de passe UNIX, puis à confirmer ce mot de passe. Une fois que vous êtes informé que le mot de passe a été correctement mis à jour, fermez WSL dans PowerShell en utilisant la commande : `exit`

> [!NOTE]
> Si vous exécutez une version antérieure du système d’exploitation Windows, comme 1703 (Creators Update) ou 1709 (Fall Creators Update), consultez la [documentation de la version archivée de cette mise à jour de compte d’utilisateur](./user-support-archived.md).
