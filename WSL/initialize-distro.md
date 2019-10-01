---
title: Initialisation d’une nouvelle distribution Linux WSL
description: Après avoir installé une distribution Linux pour WSL, effectuez l’initialisation en suivant ces étapes simples.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c33d349a6d39c325b079ccbf7ed6350bed796e33
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269587"
---
# <a name="initializing-a-newly-installed-distro"></a>Initialisation d’une distribution nouvellement installée
Une fois votre distribution téléchargée et installée, vous devez effectuer l’initialisation de la nouvelle distribution :

## <a name="launch-a-distro"></a>Lancer une distribution
Pour effectuer l’initialisation de votre distribution nouvellement installée, lancez une nouvelle instance. Pour ce faire, vous pouvez cliquer sur le bouton « Lancer » dans l’application Microsoft Store ou lancer la distribution à partir du menu Démarrer :

> Astuce : Vous pouvez épingler vos distributions les plus fréquemment utilisées à votre menu Démarrer et/ou à votre barre des tâches.

![Lancer les distributions à partir du menu Démarrer](media/start-menu.png)

> Sur Windows Server, vous pouvez lancer l’exécutable du lanceur de votre distribution `<distro>.exe` à partir du dossier d’installation de la distribution.

La première fois qu’une distribution nouvellement installée s’exécute, une fenêtre de console s’ouvre et vous êtes invité à attendre une minute ou deux, le temps que l’installation se termine.

> Au cours de cette dernière étape de l’installation, les fichiers de la distribution sont décompressés et stockés sur votre PC, prêts à être utilisés. Cette opération peut prendre environ une minute ou plus en fonction des performances des dispositifs de stockage de votre PC. Cette phase d’installation initiale est requise uniquement lors d’une nouvelle installation d’une distribution : tous les lancements ultérieurs doivent prendre moins d’une seconde.

## <a name="setting-up-a-new-linux-user-account"></a>Configuration d’un nouveau compte d’utilisateur Linux

Une fois l’installation terminée, vous êtes invité à créer un compte d’utilisateur (et son mot de passe). 

![Décompression Ubuntu dans la console Windows](media/UbuntuInstall.png)

Ce compte d’utilisateur est destiné à l’utilisateur non-administrateur normal sous lequel vous vous connectez par défaut lors du lancement d’une distribution.

> Vous pouvez choisir le nom d’utilisateur et le mot de passe de votre choix : ils n’ont aucun impact sur votre nom d’utilisateur Windows. 

Quand vous ouvrez une nouvelle instance de la distribution, vous n’êtes pas invité à entrer votre mot de passe, mais **si vous élevez un processus à l’aide de `sudo`, vous devez l’entrer**. Veillez donc à choisir un mot de passe facile à mémoriser ! Pour plus d’informations, consultez la page du [support utilisateur](user-support.md).

## <a name="update--upgrade-your-distros-packages"></a>Mettre à jour et mettre à niveau les packages de votre distribution

La plupart des distributions sont livrées avec un catalogue de packages vides/minimaux. Nous vous recommandons vivement de mettre à jour régulièrement le catalogue de packages et de mettre à niveau vos packages installés à l’aide du gestionnaire de package par défaut de votre distribution. Sur Debian/Ubuntu, vous utilisez apt :

```bash
sudo apt update && sudo apt upgrade
```

> Windows ne met pas automatiquement à jour ou à niveau vos distributions Linux : Il s’agit d’une tâche que les utilisateurs de Linux préfèrent contrôler eux-mêmes.

C’est terminé ! Profitez de votre nouvelle distribution Linux sur WSL ! Pour en savoir plus sur WSL, consultez l’autre [documentation sur WSL](https://aka.ms/wsldocs) ou la page des [ressources de formation WSL](https://aka.ms/learnwsl).

![Profitez de l’utilisation de Linux sur WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Résolution des problèmes

Vous trouverez ci-dessous des erreurs associées et des suggestions de correction. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir des erreurs courantes et leurs solutions.

> **Échec de l’installation avec l’erreur 0x8007007e** Cette erreur se produit quand votre système ne prend pas en charge Linux à partir du Store.  Vérifiez que :
> * Vous exécutez la build Windows 16215 ou ultérieure. [Vérifiez votre build](troubleshooting.md#check-your-build-number).
> * Le composant facultatif WSL (Sous-système Windows pour Linux) est activé et l’ordinateur a redémarré.  [Vérifiez que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).
