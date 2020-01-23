---
title: Mises à jour de compte d’utilisateur WSL sur les versions précédentes de Windows
description: Informations de référence sur les versions précédentes de Windows pour mettre à jour les comptes d’utilisateur Linux avec le sous-système Windows pour Linux.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 406158d769c4b465b6168d7cca45b48ff1f201fe
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520838"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a>Mises à jour de compte d’utilisateur WSL sur les versions précédentes de Windows

Ce contenu est archivé pour les utilisateurs des versions antérieures du système d’exploitation Windows qui prennent en charge le sous-système pour Linux et ont besoin de la prise en charge de la mise à jour des comptes d’utilisateur Linux.

Pour obtenir la documentation actuelle, consultez [comptes d’utilisateur pour le sous-système Windows pour Linux](../user-support.md).

### <a name="for-creators-update-version-of-windows-and-earlier"></a>Pour Creators Update version de Windows et versions antérieures

Si vous exécutez Windows 10 Creators Update ou version antérieure, vous pouvez changer l’utilisateur Bash par défaut en exécutant les commandes suivantes :

1. Définissez l’utilisateur par défaut sur `root` :

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Exécutez `bash.exe` pour vous connecter maintenant en tant que `root` :

    ```console
    C:\> bash.exe
    ```

1. Réinitialisez votre mot de passe à l’aide de la commande de mot de passe de la distribution, puis fermez la console Linux :

    ```BASH
    $ passwd username
    $ exit
    ```

1. À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal :

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Pour Fall Creators Update et versions ultérieures

Pour connaître les commandes disponibles pour une distribution en particulier, exécutez `[distro.exe] /?`.
    
Par exemple, avec Ubuntu installé :

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

Instructions pas à pas sur Ubuntu :

1. Ouvrez CMD.
1. Définissez l’utilisateur Linux par défaut sur `root` :

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Lancez votre distribution Linux (`ubuntu`).  Vous vous connectez automatiquement en tant que `root` :

1. Réinitialisez votre mot de passe à l’aide de la commande `passwd` :

    ```BASH
    $ passwd username
    ```

1. À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```
