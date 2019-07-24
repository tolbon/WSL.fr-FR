---
title: Autorisations et compte d’utilisateur Linux
description: Référence pour les comptes d’utilisateur et la gestion des autorisations avec le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, comptes d’utilisateur
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040823"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>Comptes d’utilisateur et autorisations pour le sous-système Windows pour Linux

La création de votre utilisateur Linux constitue la première étape de la configuration d’une nouvelle distribution Linux sur WSL.  Le premier compte d’utilisateur que vous créez est automatiquement configuré avec quelques attributs spéciaux:

1. Il s’agit de votre utilisateur par défaut; il se connecte automatiquement au lancement.
1. Il s’agit de l’administrateur Linux (membre du groupe sudo) par défaut.

Chaque distribution Linux exécutée sur le sous-système Windows pour Linux possède ses propres comptes d’utilisateur et mots de passe Linux.  Vous devez configurer un compte d’utilisateur Linux chaque fois que vous ajoutez une distribution, réinstallez ou réinitialisez.  Les comptes d’utilisateur Linux ne sont pas uniquement indépendants par distribution. ils sont également indépendants de votre compte d’utilisateur Windows.

## <a name="resetting-your-linux-password"></a>Réinitialisation de votre mot de passe Linux

Si vous avez accès à votre compte d’utilisateur Linux et que vous connaissez votre mot de passe actuel, modifiez-le à l’aide des outils de `passwd`réinitialisation de mot de passe Linux de cette distribution, le plus probable.

Si ce n’est pas le cas, en fonction de la distribution, vous pourrez peut-être réinitialiser votre mot de passe en réinitialisant l’utilisateur par défaut.

WSL offre une balise utilisateur par défaut pour identifier le compte d’utilisateur qui se connecte automatiquement quand vous démarrez un WSL.  Étant donné que de nombreuses distributions incluent des commandes permettant de définir l’utilisateur par défaut à root et à un utilisateur racine sans mot de passe défini, la modification de l’utilisateur par défaut en root est un outil pratique pour effectuer des opérations telles que la réinitialisation de mot de passe.

### <a name="for-creators-update-and-earlier"></a>Pour Creators Update et versions antérieures
Si vous exécutez Windows 10 Creators Update ou une version antérieure, vous pouvez modifier l’utilisateur bash par défaut en exécutant les commandes suivantes:

1. Remplacez l’utilisateur `root`par défaut par:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Exécutez `bash.exe` pour vous connecter en `root`tant que:

    ```console
    C:\> bash.exe
    ```

1. Réinitialisez votre mot de passe à l’aide de la commande de mot de passe de la distribution, puis fermez la console Linux:

    ```BASH
    $ passwd username
    $ exit
    ```

1. À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Pour les créateurs de automne, mettez à jour et versions ultérieures
Pour connaître les commandes disponibles pour une distribution particulière, exécutez `[distro.exe] /?`.
    
Par exemple, avec Ubuntu installé:

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

Instructions pas à pas sur Ubuntu:

1. Ouvrir CMD
1. Définir l’utilisateur Linux par défaut `root`sur:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Lancez votre distribution Linux (`ubuntu`).  Vous vous connectez automatiquement en `root`tant que:

1. Réinitialisez votre mot `passwd` de passe à l’aide de la commande:

    ```BASH
    $ passwd username
    ```

1. À partir de Windows CMD, réinitialisez l’utilisateur par défaut sur votre compte d’utilisateur Linux normal.

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>Autorisations

Il existe deux concepts importants à garder à l’esprit lorsqu’il s’agit d’autorisations dans WSL:

1. Le modèle d’autorisation Windows régit les droits des processus sur les ressources Windows
2. Le modèle d’autorisation Linux contrôle un droit de processus aux ressources Linux

Lors de l’exécution de Linux sur WSL, Linux aura les mêmes autorisations Windows que le processus qui le lance. Linux peut être lancé dans l’un des deux niveaux d’autorisation suivants:

* Normal (non élevé): Linux s’exécute avec les autorisations de l’utilisateur connecté
* Élevé/administrateur: Linux s’exécute avec des autorisations Windows élevées/admin

> Étant donné que les processus élevés peuvent accéder/modifier (et par conséquent endommager) des paramètres à l’ensemble du système et des données système/protégées, **Évitez** de lancer des processus élevés, sauf si vous avez absolument besoin de savoir s’il s’agit d’applications/outils Windows ou Linux/ Coque!

Les autorisations Windows ci-dessus sont indépendantes des autorisations au sein d’une instance Linux: Les «privilèges racine» Linux affectent uniquement les droits de l’utilisateur au sein de l’environnement Linux & système de fichiers; ils n’ont aucun impact sur les privilèges Windows accordés. Ainsi, l’exécution d’un processus Linux en tant que racine `sudo`(par exemple, via) accorde uniquement ce processus à des droits d’administrateur au sein de l’environnement Linux.

**Exemple :**     
Une session bash avec des privilèges d’administrateur Windows `cd /mnt/c/Users/Administrator` peut accéder alors qu’une session bash sans privilèges d’administrateur voit une erreur «autorisation refusée».

Dans Linux, la `sudo cd /mnt/c/Users/Administrator` saisie n’accorde pas l’accès au répertoire de l’administrateur, car les autorisations dans Windows sont gérées par Windows.

Le modèle d’autorisation Linux est important dans l’environnement Linux où l’utilisateur dispose d’autorisations basées sur l’utilisateur Linux actuel.

**Exemple :**  
Un utilisateur du groupe sudo peut s’exécuter `sudo apt update`.
