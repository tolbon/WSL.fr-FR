---
title: Installer ou supprimer sur la mise à jour anniversaire de Windows 10 ou Creators Update
description: Instructions d’installation et de désinstallation pour le hérité, la distribution bêta sur la mise à jour anniversaire de Windows 10 ou Creators Update
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, hérité, bêta, installer, supprimer, désinstaller, désinstaller, delete, déconseillée
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040839"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>Guide pour installer ou désinstaller le sous-système de Windows pour Linux sur la mise à jour anniversaire de Windows 10 et Creators Update 

Si vous utilisez Windows 10 Creators Update ou une version ultérieure, veuillez [suivez les instructions d’installation de Windows 10](install-win10.md).

<strong><em><span style="color: #f28014">Les instructions suivantes concernent les utilisateurs qui exécutent la mise à jour anniversaire de Windows 10 ou Windows 10 Creators Update</span></em></strong>

Avant Windows 10 Fall Creators Update (version 1709), WSL a été publié comme une fonctionnalité bêta et installé une seule instance Ubuntu lors de la première exécution du « Bash sur Ubuntu sur Windows » (ou Bash.exe).

> Vous pouvez utiliser WSL sur des versions antérieures de Windows 10, cette version bêta de « distributeur hérité » est désormais considéré comme obsolète. Nous vous encourageons vivement à exécuter la version la plus récente de Windows 10 disponibles. Chaque nouvelle version de Windows 10 inclut plusieurs centaines de correctifs et améliorations dans WSL uniquement, ce qui permet plus jamais outils Linux et les applications à s’exécuter correctement sur WSL.

Si vous ne peut pas mettre à niveau vers Fall Creators Update ou version ultérieure, suivez les étapes ci-dessous pour activer et utiliser WSL :

1. Activer développeur Mode pour exécuter WSL sur la mise à jour anniversaire de Windows 10 ou Creators Update, vous devez activer le Mode développeur :

    Ouvrez **paramètres** -> **mise à jour et sécurité** -> **pour les développeurs**

    Sélectionnez la case d’option Mode développeur  
    ![Activer le mode développeur](media/updateAndSecurity.png)

    > La nécessité d’activer le Mode développeur a été [supprimée dans Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. Ouvrez une invite de commandes.  Type `bash` puis appuyez sur entrée

    La première fois que vous exécutez Bash sur Ubuntu sur Windows, vous devrez faire pour accepter les licences de Canonical. Une fois accepté, WSL téléchargera et installera l’instance Ubuntu sur votre ordinateur, et un raccourci « Bash sur Ubuntu sur Windows » sera ajouté à votre menu Démarrer.

    ![Inviter à installer Ubuntu](media/bashShellInstall.png)

    La première fois que vous exécutez Bash sur Ubuntu sur Windows, vous devrez créer un nom d’utilisateur UNIX et le mot de passe. Suivez le [nouvelles instructions d’instance de distributeur](initialize-distro.md) pour terminer l’installation

1. Lancer un nouvel interpréteur Ubuntu à l’aide :
    * En cours d’exécution `bash` à partir d’une invite de commandes
    * En cliquant sur le raccourci « Bash sur Ubuntu sur Windows » du menu Démarrer

    
## <a name="uninstallingremoving-the-legacy-distro"></a>Désinstallation/la suppression de la distribution héritée
Si vous mettez à niveau depuis une version antérieure de Windows 10 sur lequel vous avez installé WSL pour Windows 10 Fall Creators Update, votre distribution existante demeureront intacte. Toutefois, nous fortement vous recommandons d’installer une nouvelle distribution assurée par le Store dès que possible et migrer les fichiers nécessaires, données etc. à partir de votre distribution héritée pour votre nouvelle distribution.

Pour supprimer la distribution héritée à partir de votre ordinateur, exécutez la commande suivante à partir d’une instance de la ligne de commande ou PowerShell :

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>Suppression manuelle de la distribution héritée
Si vous le souhaitez, vous pouvez supprimer manuellement l’ancienne instance. Cela peut être nécessaire si vous rencontrez des problèmes pour désinstaller le distributeur hérité à l’aide `lxrun.exe`, ou de la mise à jour Windows 10 printemps 2018 sont en cours d’exécution (ou version ultérieure) qui ne sont pas fournies avec `lxrun.exe`.

Pour forcer la suppression de votre distribution WSL héritée, supprimez le `%localappdata%\lxss\` dossier (et tous les il s’agit de contenu secondaire) à l’aide de l’Explorateur de fichiers des Windows ou la ligne de commande :

À l'aide de PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

En utilisant une commande :
```console
DEL /S %localappdata%\lxss\
```
