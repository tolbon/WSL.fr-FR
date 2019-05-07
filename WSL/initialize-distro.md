---
title: Initialiser une nouvelle distribution Linux de WSL
description: Après avoir installé une distribution Linux pour WSL, terminer l’initialisation en suivant ces étapes simples
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902046"
---
# <a name="initializing-a-newly-installed-distro"></a>L’initialisation d’une distribution nouvellement installée
Une fois que votre distribution a été téléchargée et installée, vous devez effectuer l’initialisation de la nouvelle distribution :

## <a name="launch-a-distro"></a>Lancer un distributeur
Pour terminer l’initialisation de votre distribution nouvellement installée, lancez une nouvelle instance. Vous pouvez le faire en cliquant sur le bouton « lancement » dans l’application du Windows Store, ou en lançant la distribution dans le menu Démarrer :

> Astuce : Vous souhaiterez peut-être épingler vos distributions fréquemment utilisées dans votre menu Démarrer, et/ou à votre barre des tâches !

![Lancer des distributions à partir du menu Démarrer](media/start-menu.png)

> Sur Windows Server, vous pouvez lancer le Lanceur de votre distribution exécutable `<distro>.exe` à partir du dossier d’installation de distribution.

La première fois une distribution nouvellement installée s’exécute, une Console fenêtre s’ouvre, et vous devrez attendre une ou deux minutes pour terminer l’installation.

> Au cours de cette étape finale de l’installation, les fichiers de la distribution sont retirer compressés et stockés sur votre PC, prêt à être utilisé. Cette opération peut prendre autour d’une minute ou plus selon les performances des périphériques de stockage de votre PC. Cette phase de l’installation initiale est uniquement requis lorsqu’un distributeur est correctement installé - tous les futurs lancements doivent prendre moins d’une seconde.

## <a name="setting-up-a-new-linux-user-account"></a>Configuration d’un nouveau compte d’utilisateur Linux

Une fois l’installation terminée, vous devrez créer un nouveau compte d’utilisateur (et son mot de passe). 

![Ubuntu décompression dans la console Windows](media/UbuntuInstall.png)

Ce compte d’utilisateur est pour l’utilisateur non-administrateur normal que vous serez connecté en tant que par défaut lors du lancement d’un distributeur.

> Vous pouvez choisir n’importe quel nom d’utilisateur et le mot de passe : ils n’ont aucune incidence sur votre nom d’utilisateur Windows. 

Lorsque vous ouvrez une nouvelle instance de distributeur, vous ne sont pas être invité à entrer votre mot de passe, mais **si vous élevez un processus utilisant `sudo`, vous devez entrer votre mot de passe**, assurez-vous que vous choisissez un mot de passe que vous vous souviendrez facilement ! Consultez le [prise en charge de l’utilisateur](user-support.md) page pour plus d’informations.

## <a name="update--upgrade-your-distros-packages"></a>Mise à jour & Mettre à niveau les packages de votre distribution.

La plupart des distributions sont livrés avec un catalogue de package vide/minimale. Nous vous recommandons fortement régulièrement mise à jour de votre catalogue de package et la mise à niveau vos packages installés à l’aide du Gestionnaire de package préféré de votre distribution. Sur Debian/Ubuntu, vous utilisez apt :

```bash
sudo apt update && sudo apt upgrade
```

> Windows ne pas automatiquement mise à jour et mettre à niveau votre distro(s) Linux : Il s’agit d’une tâche que les utilisateurs Linux préfèrent contrôler eux-mêmes.

C’est terminé ! Profitez de l’utilisation de votre distribution Linux de nouveau sur WSL ! Pour en savoir plus sur WSL, passez en revue l’autre [docs WSL](https://aka.ms/wsldocs), ou le [WSL page de ressources de formation](https://aka.ms/learnwsl).

![Vous profiterez Linux sur WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Résolution des problèmes

Voici les erreurs associées et des suggestions de correction. Reportez-vous à la [page Résolution des problèmes de WSL](troubleshooting.md) pour les autres erreurs courantes et leurs solutions.

> **Échec de l’installation avec l’erreur 0x8007007e** cette erreur se produit lorsque votre système ne prend pas en charge Linux à partir du magasin.  Vérifiez que :
> * Vous exécutez Windows build 16215 ou version ultérieure. [Vérifier votre build](troubleshooting.md#check-your-build-number).
> * Le sous-système Windows pour le composant facultatif de Linux est activé et que l’ordinateur a redémarré.  [Assurez-vous que WSL est activé](troubleshooting.md#confirm-wsl-is-enabled).
