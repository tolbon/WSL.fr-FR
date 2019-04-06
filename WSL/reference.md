---
title: Sous-système Windows pour la référence de commande Linux
description: Liste des commandes qui gèrent le sous-système Windows pour Linux
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063577"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Référence des commandes pour le sous-système Windows pour Linux

> `lxrun.exe` est déconseillé à compter de Windows 10 1803 et versions ultérieures.

La commande `lxrun.exe` peut être utilisé pour interagir avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directement.  Ces commandes sont installées dans le `\Windows\System32` directory et peut être exécuté dans une invite de commandes Windows ou dans PowerShell.

* `lxrun.exe` est utilisé pour gérer les WSL.  Cette commande peut être utilisée pour installer ou désinstaller l’image Ubuntu.


| Command                     | Description                     |
|:----------------------------|:---------------------------|
| `bash`                      | Lance l’interpréteur de commandes Bash dans le répertoire actif.  Si l’interpréteur de commandes Bash n’est pas automatiquement installé s’exécute `lxrun /install` |
| `bash ~`                    | Lance l’interpréteur de commandes bash dans le répertoire de base de l’utilisateur Ubuntu.  Similaire à l’exécution des cd ~            |
| `bash -c "<command>"`       | Exécute la commande, imprime la sortie et se termine à l’invite de commandes Windows. <br/> <br/> Exemple : **bash -c « ls »** |

<p>

| Command                     | Description                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | La commande lxrun est utilisée pour gérer l’instance WSL. |
| `lxrun /install`            | Démarre le téléchargement et le processus d’installation. <br/> **/y** peuvent être ajoutés à ignorer toutes les invites.  L’invite de confirmation est accepté automatiquement et l’utilisateur par défaut est défini pour la racine.          |
| `lxrun /uninstall`          | Désinstalle et supprime l’image Ubuntu.  Par défaut, cela ne supprime pas le Ubuntu répertoire de base. <br/> **/y** peuvent être ajoutés à accepter automatiquement l’invite de confirmation <br/>**toutes les** désinstalle et supprime le répertoire de base de l’utilisateur Ubuntu         |
| `lxrun /setdefaultuser <userName>`     | Définit la valeur par défaut Bash sur Ubuntu utilisateur. Demande un mot de passe si l’utilisateur spécifié n’existe pas.  Pour plus d’informations, visitez : https://aka.ms/wslusers. <br/> **/y** promping de contournements pour le mot de passe.  L’utilisateur sera créé sans un mot de passe.|
| `lxrun /update`            | Met à jour les index de package du sous-système          |
