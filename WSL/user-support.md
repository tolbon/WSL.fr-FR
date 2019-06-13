---
title: Autorisations et le compte d’utilisateur Linux
description: Référence pour la gestion des autorisations et comptes d’utilisateur avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, comptes d’utilisateur
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040823"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Comptes d’utilisateur et les autorisations pour le sous-système de Windows pour Linux

Création de votre utilisateur Linux est la première étape dans la configuration d’une nouvelle distribution de Linux sur WSL.  Le premier compte d’utilisateur que vous créez est automatiquement configuré avec quelques attributs spécifiques :

1. C’est votre utilisateur par défaut, il se connecte en automatiquement lors du lancement.
1. Il est administrateur de Linux (il s’agit d’un membre du groupe sudo) par défaut.

Chaque distribution Linux en cours d’exécution sur le sous-système Windows pour Linux a ses propres comptes d’utilisateur Linux et les mots de passe.  Vous devrez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez une distribution, réinstallez ou réinitialisez.  Comptes d’utilisateur Linux ne sont pas uniquement indépendantes par distribution, elles sont également indépendantes à partir de votre compte d’utilisateur Windows.

## <a name="resetting-your-linux-password"></a>Réinitialiser votre mot de passe Linux

Si vous avez accès à votre compte d’utilisateur Linux et que vous connaissez votre mot de passe actuel, modifiez-le à l’aide de Linux mot de passe réinitialisé les outils de cette distribution--probablement `passwd`.

Si ce n’est pas une option, en fonction de la distribution, vous serez peut-être en mesure de réinitialiser votre mot de passe en réinitialisant l’utilisateur par défaut.

WSL offre une balise d’utilisateur par défaut pour identifier le compte d’utilisateur automatiquement se connecte lorsque vous démarrez un WSL.  Dans la mesure où les nombreuses distributions comprennent les commandes permettant de définir l’utilisateur par défaut à la racine et également un utilisateur racine avec aucun mot de passe défini, la modification de l’utilisateur par défaut à la racine est un outil pratique pour des opérations comme la réinitialisation de mot de passe.

### <a name="for-creators-update-and-earlier"></a>Pour Creators Update et versions antérieures
Si vous exécutez Windows 10 Creators update ou version antérieure, vous pouvez modifier l’utilisateur de Bash par défaut en exécutant les commandes suivantes :

1. Modifier l’utilisateur par défaut à `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Exécutez `bash.exe` à présent se connecter en tant que `root`:

    ```console
    C:\> bash.exe
    ```

1. Réinitialiser votre mot de passe à l’aide de la commande de mot de passe de la distribution, puis fermez la Console de Linux :

    ```BASH
    $ passwd username
    $ exit
    ```

1. À partir de Windows CMD, réinitialiser votre utilisateur par défaut à votre compte d’utilisateur Linux normal :

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Pour Fall Creators Update et versions ultérieures
Pour voir quelles sont les commandes sont disponibles pour une distribution particulière, exécutez `[distro.exe] /?`.
    
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

Procédure pas à obtenir des instructions détaillées à l’aide d’Ubuntu :

1. Ouvrez CMD
1. L’utilisateur de Linux par défaut la valeur `root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Lancez votre distribution Linux (`ubuntu`).  Vous rétablit automatiquement la connexion en tant que `root`:

1. Réinitialiser votre mot de passe à l’aide de la `passwd` commande :

    ```BASH
    $ passwd username
    ```

1. À partir de Windows CMD, réinitialiser votre utilisateur par défaut à votre compte d’utilisateur Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Autorisations

Il existe deux concepts importants à prendre en compte lorsqu’il s’agit des autorisations dans WSL :

1. Le modèle d’autorisation Windows régit les droits d’un processus aux ressources de Windows
2. Le modèle d’autorisation Linux contrôle les droits d’un processus aux ressources de Linux

Lors de l’exécution de Linux sur WSL, Linux aura les mêmes autorisations Windows en tant que le processus qui le lance. Linux peut être lancé dans un des deux niveaux d’autorisation :

* Normal (non élevés) : Linux s’exécute avec les autorisations de l’utilisateur connecté
* Avec élévation de privilèges/admin : Linux s’exécute avec des autorisations Windows avec élévation de privilèges/admin

> Étant donné que le processus avec élévation de privilèges peuvent modifier/accès (et par conséquent endommager) les paramètres de l’échelle du système et le système à l’échelle du/des données protégées **Évitez** lançant des processus avec élévation de privilèges, sauf si vous avez absolument - pour qu’ils soient Windows ou Linux outils/applications/shells !

Les autorisations Windows ci-dessus sont indépendantes des autorisations au sein d’une instance de Linux : Linux « privilèges racine » uniquement avoir un impact sur les droits d’utilisateur dans l’environnement Linux & système de fichiers ; ils n’ont aucun impact sur les privilèges Windows octroyés. Par conséquent, en exécutant un processus Linux en tant que racine (par exemple, via `sudo`) accorde uniquement qui traitent les droits d’administrateur dans l’environnement Linux.

**Exemple :**     
Une session d’interpréteur de commandes avec des privilèges d’administrateur Windows peut-être accéder à `cd /mnt/c/Users/Administrator` lors d’une session Bash sans privilèges d’administrateur pouvez voir une erreur « Autorisation refusée ».

Sous Linux, en tapant `sudo cd /mnt/c/Users/Administrator` pas accorde l’accès au répertoire de l’administrateur dans la mesure où les autorisations dans Windows sont gérées par Windows.

Le modèle d’autorisation Linux est important quand à l’intérieur de l’environnement Linux où l’utilisateur dispose des autorisations en fonction de l’utilisateur Linux actuel.

**Exemple :**  
Un utilisateur dans le groupe sudo peut-être s’exécuter `sudo apt update`.
