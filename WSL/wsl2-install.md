---
title: Installer WSL 2
description: Instructions d’installation pour WSL 2
keywords: BashOnWindows, bash, wsl, wsl2, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, installation
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520548"
---
# <a name="installation-instructions-for-wsl-2"></a>Instructions d’installation pour WSL 2

Vous pouvez regarder la vidéo ci-dessous ou lire cet article pour découvrir comment installer WSL2. 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

Pour installer et commencer à utiliser WSL 2, effectuez les étapes suivantes :

> WSL 2 est disponible uniquement dans les builds 18917 et ultérieures de Windows 10

- Vérifiez que vous avez installé WSL (vous trouverez des instructions pour cela [ici](./install-win10.md)) et que vous exécutez la **build 18917** ou ultérieure de Windows 10
   - Pour veiller à utiliser la build 18917 ou ultérieure, rejoignez [le programme Windows Insider](https://insider.windows.com/en-us/) et sélectionnez l’anneau « Rapide » ou l’anneau « Lent ». 
   - Vous pouvez vérifier votre version de Windows en ouvrant l’invite de commandes et en exécutant la commande `ver`.
- Activer le composant facultatif « Plateforme de machine virtuelle »
- Définir une distribution basée sur WSL 2 en utilisant la ligne de commande
- Vérifier les versions de WSL que vos distributions utilisent

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>Activer le composant facultatif « Plateforme de machine virtuelle » et s’assurer que WSL est activé

Vous devez vous assurer que le sous-système Windows pour Linux et les composants facultatifs de la plateforme de machine virtuelle sont installés. Pour ce faire, exécutez la commande suivante dans PowerShell : 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Redémarrez votre machine pour terminer l’installation des deux composants.


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>Définir une distribution basée sur WSL 2 en utilisant la ligne de commande

Si vous n’avez pas de distribution Linux installée, reportez-vous à la page [Installer sur Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) pour obtenir des instructions sur son installation. 

Pour définir une distribution, exécutez : 

```
wsl --set-version <Distro> 2
```

et veillez à remplacer `<Distro>` par le vrai nom de votre distribution. (Vous pouvez le trouver avec la commande : `wsl -l`). Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».

Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :

```
wsl --set-default-version 2
```

Ainsi, toutes les nouvelles distributions que vous installerez seront initialisées en tant que distributions WSL 2.

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>Pour terminer, vérifiez quelles versions de WSL utilisent vos distributions.

Pour vérifier les versions de WSL qu’utilise chaque distribution, utilisez la commande suivante (disponible uniquement dans la build 18917 ou ultérieure de Windows) :

`wsl --list --verbose` ou `wsl -l -v`

La distribution que vous avez choisie ci-dessus doit maintenant afficher un « 2 » dans la colonne « version ». Maintenant que vous avez terminé, n’hésitez pas à commencer à utiliser votre distribution WSL 2 ! 

## <a name="troubleshooting"></a>Dépannage : 

Vous trouverez ci-dessous des erreurs associées et des suggestions de correction lors de l’installation de WSL 2. Reportez-vous à la [page de résolution des problèmes WSL](troubleshooting.md) pour voir d’autres erreurs WSL générales et leurs solutions.

* **Échec de l’installation avec l’erreur 0x80070003 ou l’erreur 0x80370102**
    * Assurez-vous que la virtualisation est activée dans le BIOS de votre ordinateur. Les instructions sur la façon de procéder varient d’un ordinateur à l’autre et se trouvent très probablement sous les options liées au processeur.
   
* **Erreur lors d’une tentative de mise à niveau : `Invalid command line option: wsl --set-version Ubuntu 2`**
    * Vérifiez que le sous-système Windows pour Linux est activé et que vous utilisez Windows version de build 18917 ou ultérieure. Pour activer WSL, exécutez cette commande dans une invite PowerShell avec des privilèges d’administrateur : `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`. Vous trouverez les instructions complètes de l’installation de WSL [ici](./install-win10.md).

* **Impossible de terminer l’opération demandée du fait d’une limitation du système de disque virtuel. Les fichiers de disque dur virtuel doivent être décompressés et déchiffrés, mais ne doivent pas être partiellement alloués.**
    * Vérifiez le [thread GitHub WSL n° 4103](https://github.com/microsoft/WSL/issues/4103) où ce problème est suivi pour obtenir des informations mises à jour.

* **Le terme « wsl » n’est pas reconnu comme nom d’applet de commande, fonction, fichier de script ou programme exécutable.** 
    * Assurez-vous que le [composant facultatif Sous-système Windows pour Linux est installé](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).<br> De plus, si vous utilisez un appareil Arm64 et exécutez cette commande à partir de PowerShell, vous recevrez cette erreur. Au lieu de cela, exécutez `wsl.exe` à partir de [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) ou d’une invite de commandes. 
