---
title: Installer ou supprimer la mise à jour anniversaire de Windows 10 ou les créateurs de la mise à jour
description: Instructions d’installation et de désinstallation pour la mise à jour anniversaire héritée, bêta distribution sur Windows 10 ou Creators Update
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, hérité, bêta, installation, suppression, désinstallation, désinstallation, suppression, déconseillé
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 416bed3ed3a0470da2eb5e6beb75e73eb6836200
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269769"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Guide pour installer ou désinstaller le sous-système Windows pour Linux sur la mise à jour anniversaire Windows 10 et les créateurs de la mise à jour 

Si vous exécutez Windows 10 Creators Update ou une version ultérieure, veuillez [suivre les instructions d’installation de Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">Les instructions suivantes concernent les utilisateurs qui exécutent la mise à jour anniversaire Windows 10 ou Windows 10 Creators Update</span></em></strong>

Avant la mise à jour de Windows 10 automne Creators (version 1709), WSL a été publié en tant que fonctionnalité bêta et installait une seule instance Ubuntu lors de la première exécution de « bash sur Ubuntu sur Windows » (ou bash. exe).

> Bien que vous puissiez utiliser WSL sur des versions antérieures de Windows 10, cette version bêta « Legacy distribution » est désormais considérée comme obsolète. Nous vous encourageons vivement à exécuter la version la plus récente de Windows 10 disponible. Chaque nouvelle version de Windows 10 inclut un grand nombre de centaines de correctifs et d’améliorations dans WSL seul, ce qui permet à d’autres outils et applications Linux de s’exécuter correctement sur WSL.

Si vous ne pouvez pas effectuer une mise à niveau vers automne Creators Update ou une version ultérieure, suivez les étapes ci-dessous pour activer et utiliser WSL :

1. Activer le mode développeur pour exécuter WSL sur la mise à jour anniversaire de Windows 10 ou sur Creators Update, vous devez activer le mode développeur :

    Ouvrir des **paramètres** -> des -> de **sécurité et de mise à jour** **pour les développeurs**

    Sélectionnez la case d’option mode développeur  
    ![Activer le mode développeur](media/updateAndSecurity.png)

    > La nécessité d’activer le mode développeur a été [supprimée dans Windows 10 automne Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Ouvrez une invite de commandes.  Tapez `bash` et appuyez sur entrée.

    La première fois que vous exécutez bash sur Ubuntu sur Windows, vous êtes invité à accepter la licence de Canonical. Une fois accepté, WSL télécharge et installe l’instance Ubuntu sur votre ordinateur, et un raccourci « Bash sur Ubuntu sur Windows » est ajouté à votre menu Démarrer.

    ![Demander l’installation d’Ubuntu](media/bashShellInstall.png)

    La première fois que vous exécutez bash sur Ubuntu sur Windows, vous êtes invité à créer un nom d’utilisateur et un mot de passe UNIX. Suivez les [nouvelles instructions de l’instance distribution](initialize-distro.md) pour terminer l’installation

1. Lancez un nouveau shell Ubuntu en procédant de l’une des deux :
    * Exécution de `bash` à partir d’une invite de commandes
    * Cliquer sur le menu Démarrer « bash sur Ubuntu sur Windows »

    
## <a name="uninstallingremoving-the-legacy-distro"></a>Désinstallation/suppression de la distribution héritée
Si vous effectuez une mise à niveau vers Windows 10 automne Creators Update à partir d’une version antérieure de Windows 10 sur laquelle vous avez installé WSL, votre distribution existante reste intacte. Toutefois, nous vous encourageons VIVEment à installer un nouveau distribution ASAP remis en magasin et à migrer les fichiers, les données, etc. nécessaires de votre distribution hérité vers votre nouveau distribution.

Pour supprimer les distribution hérités de votre ordinateur, exécutez la commande suivante à partir d’une ligne de commande ou d’une instance de PowerShell :

```console
wsl --unregister Legacy
```

Si vous n’utilisez pas la version 1903 ou une version ultérieure de Windows, vous devrez peut-être exécuter `wslconfig /u Legacy` ou `lxrun /uninstall /full` à la place. 

### <a name="manually-deleting-the-legacy-distro"></a>Suppression manuelle de la distribution héritée
Si vous le souhaitez, vous pouvez supprimer manuellement votre instance héritée. Cela peut être nécessaire si vous rencontrez des problèmes lors de la désinstallation de la distribution héritée à l’aide de `lxrun.exe`ou si vous exécutez Windows 10 Spring 2018 Update (ou version ultérieure) qui n’est pas livré avec `lxrun.exe`.

Pour forcer la suppression de votre distribution WSL héritée, supprimez le dossier `%localappdata%\lxss\` (et tous ses sous-contenus) à l’aide de l’Explorateur de fichiers Windows, ou de la ligne de commande :

À l’aide de PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

Utilisation de cmd :
```console
DEL /S %localappdata%\lxss\
```
