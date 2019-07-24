---
title: Initialisation d’un nouveau WSL Linux distribution
description: Après l’installation d’un distribution Linux pour WSL, terminez l’initialisation en suivant ces étapes simples.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499300"
---
# <a name="initializing-a-newly-installed-distro"></a>Initialisation d’un distribution récemment installé
Une fois que votre distribution a été téléchargé et installé, vous devez effectuer l’initialisation du nouveau distribution:

## <a name="launch-a-distro"></a>Lancer un distribution
Pour terminer l’initialisation de votre distribution nouvellement installée, lancez une nouvelle instance. Pour ce faire, vous pouvez cliquer sur le bouton «lancer» dans l’application Microsoft Store ou lancer le distribution à partir du menu Démarrer:

> Conseil : Vous pouvez épingler vos distributions les plus fréquemment utilisés à votre menu Démarrer, et/ou à votre barre des tâches.

![Lancer distributions à partir du menu Démarrer](media/start-menu.png)

> Sur Windows Server, vous pouvez lancer l’exécutable `<distro>.exe` du lanceur de distribution à partir du dossier d’installation de distribution.

La première fois qu’un distribution récemment installé s’exécute, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux pour que l’installation se termine.

> Au cours de cette dernière étape de l’installation, les fichiers de distribution sont décompressés et stockés sur votre PC, prêts à être utilisés. Cela peut prendre environ une minute ou plus en fonction des performances des périphériques de stockage de votre PC. Cette phase d’installation initiale est requise uniquement quand un distribution est installé de façon propre. tous les lancements ultérieurs doivent prendre moins d’une seconde.

## <a name="setting-up-a-new-linux-user-account"></a>Configuration d’un nouveau compte d’utilisateur Linux

Une fois l’installation terminée, vous êtes invité à créer un nouveau compte d’utilisateur (et son mot de passe). 

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

Ce compte d’utilisateur est destiné à l’utilisateur non administrateur normal auquel vous êtes connecté par défaut lors du lancement d’un distribution.

> Vous pouvez choisir le nom d’utilisateur et le mot de passe de votre choix. ils n’ont aucun impact sur votre nom d’utilisateur Windows. 

Lorsque vous ouvrez une nouvelle instance distribution, vous n’êtes pas invité à entrer votre mot de passe, mais **si vous élevez `sudo`un processus à l’aide de, vous devez entrer votre mot de passe**. Veillez donc à choisir un mot de passe facile à mémoriser! Pour plus d’informations, consultez la page de [support utilisateur](user-support.md) .

## <a name="update--upgrade-your-distros-packages"></a>Mettre à jour & mettre à niveau les packages de votre distribution

La plupart des distributions sont livrés avec un catalogue de packages vide/minimal. Nous vous recommandons vivement de mettre à jour régulièrement le catalogue de votre package et de mettre à niveau vos packages installés à l’aide du gestionnaire de package préféré de votre distribution. Sur Debian/Ubuntu, vous utilisez apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux: Il s’agit d’une tâche que les utilisateurs de Linux préfèrent contrôler eux-mêmes.

C’est terminé ! Profitez de votre nouvelle distribution Linux sur WSL! Pour en savoir plus sur WSL, consultez les autres [documents WSL](https://aka.ms/wsldocs)ou la [page des ressources de formation WSL](https://aka.ms/learnwsl).

![Profitez de l’utilisation de Linux sur WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Résolution des problèmes

Vous trouverez ci-dessous des erreurs connexes et des corrections suggérées. Reportez-vous à la [page de dépannage WSL](troubleshooting.md) pour d’autres erreurs courantes et leurs solutions.

> **Échec de l’installation avec l’erreur 0x8007007e** Cette erreur se produit lorsque votre système ne prend pas en charge Linux à partir du Windows Store.  Vérifiez que :
> * Vous exécutez Windows Build 16215 ou version ultérieure. [Vérifiez votre Build](troubleshooting.md#check-your-build-number).
> * Le composant facultatif sous-système Windows pour Linux est activé et l’ordinateur a redémarré.  Vérifiez [que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).
