---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91994f3a075436c022acb9dadeea072142687b72
ms.sourcegitcommit: cf6d8e277ed3102f8f879b9f39ba0966d4ea6135
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2019
ms.locfileid: "74164344"
---
# <a name="installation-instructions-for-wsl-2"></a>Instructions d’installation pour WSL 2

Pour installer et commencer à utiliser WSL 2, effectuez les étapes suivantes :

> WSL 2 est disponible uniquement dans Windows 10 versions 18917 ou ultérieures

- Vérifiez que vous avez installé WSL (vous trouverez des instructions pour le faire [ici](./install-win10.md)) et que vous exécutez Windows 10 **Build 18917** ou une version ultérieure.
   - Pour vous assurer que vous utilisez la version 18917 ou une version ultérieure, rejoignez [le programme Windows Insider](https://insider.windows.com/en-us/) et sélectionnez l’anneau « Fast ». 
   - Vous pouvez vérifier votre version de Windows en ouvrant l’invite de commandes et en exécutant la commande `ver`.
- Activer le composant facultatif « Plateforme de machine virtuelle »
- Définir une distribution basée sur WSL 2 en utilisant la ligne de commande
- Vérifier les versions de WSL que vos distributions utilisent

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Activez le composant facultatif « plateforme de machine virtuelle » et assurez-vous que WSL est activé

Pour activer le composant « plateforme d’ordinateur virtuel », ouvrez PowerShell en tant qu’administrateur et exécutez la commande ci-dessous. Si vous installez WSL pour la première fois, sélectionnez « non » quand vous êtes invité à redémarrer, car vous devrez redémarrer votre ordinateur quand même après avoir installé le composant facultatif « sous-système Windows pour Linux ».

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

Vous devez également vous assurer que le composant facultatif sous-système Windows pour Linux est activé. Pour ce faire, vous pouvez exécuter la commande suivante à partir d’une fenêtre PowerShell avec des privilèges d’administrateur : 

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Redémarrez votre ordinateur pour terminer l’installation des deux composants.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Définir une distribution basée sur WSL 2 en utilisant la ligne de commande

Si vous n’avez pas de distribution Linux installé, reportez-vous à la page relative à l' [installation sur Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs pour obtenir des instructions sur l’installation d’un. 

Dans PowerShell, exécutez :

`wsl --set-version <Distro> 2`

et veillez à remplacer `<Distro>` par le vrai nom de votre distribution. (Vous pouvez le trouver avec la commande : `wsl -l`). Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».

Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :

`wsl --set-default-version 2`

Ainsi, toutes les nouvelles distributions que vous installerez seront initialisées en tant que distributions WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Pour terminer, vérifiez quelles versions de WSL utilisent vos distributions.

Pour vérifier les versions de WSL que chaque distribution utilise, utilisez la commande suivante (disponible uniquement dans Windows Build 18917 ou version ultérieure) :

`wsl --list --verbose` ou `wsl -l -v`

La distribution que vous avez choisie ci-dessus doit maintenant afficher un « 2 » dans la colonne « version ». Maintenant que vous avez terminé, n’hésitez pas à commencer à utiliser votre distribution WSL 2 ! 

## <a name="troubleshooting"></a>Dépannage : 

Vous trouverez ci-dessous des erreurs associées et des suggestions de correction lors de l’installation de WSL 2. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir d’autres erreurs WSL générales et leurs solutions.

* **Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**
    * Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur. Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.
   
* **Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez Windows version de build 18917 ou ultérieure. Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).

* **L’opération demandée n’a pas pu être effectuée en raison d’une limitation du système de disque virtuel. Les fichiers de disque dur virtuel doivent être décompressés et déchiffrés et ne doivent pas être éparpillés.**
    * Vérifiez [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) où ce problème est suivi pour obtenir des informations mises à jour.