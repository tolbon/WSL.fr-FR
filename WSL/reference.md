---
title: Informations de référence sur les commandes du sous-système Windows pour Linux
description: Liste des commandes qui gèrent le sous-système Windows pour Linux
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307653"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Informations de référence sur les commandes pour le sous-système Windows pour Linux

La meilleure façon d’interagir avec le sous-système Windows pour Linux consiste à utiliser `wsl.exe` la commande. 

## `wsl.exe` 

Voici une liste contenant toutes les options lors de `wsl.exe` l’utilisation de à partir de la version 1903 de Windows.

* Arguments pour l’exécution des fichiers binaires Linux:

    * Si aucune ligne de commande n’est fournie, WSL. exe lance l’interpréteur de commandes par défaut.

    * --Exec,-e<CommandLine>
        * Exécutez la commande spécifiée sans utiliser l’interpréteur de commandes Linux par défaut.

    * --
        * Transmettez la ligne de commande restante telle quelle.

* Options :
    * --distribution,-d<Distro>
        * Exécutez la distribution spécifiée.

    * --utilisateur,-u<UserName>
        * Exécuter en tant qu’utilisateur spécifié.

* Arguments pour la gestion du sous-système Windows pour Linux:

    * --exporter <Distro><FileName>
        * Exporte la distribution vers un fichier tar.
        Le nom de fichier peut être-pour la sortie standard.

    * --import <Distro> <InstallLocation>[options <FileName> ]
        * Importe le fichier tar spécifié en tant que nouvelle distribution.
        Le nom de fichier peut être-pour une entrée standard.

        * Options :
            * --version <Version> spécifie la version à utiliser pour la nouvelle distribution.

    * --List,-l [options]
        * Répertorie les distributions.

        * Options :
            * --tout
                * Répertorie toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.

            * --en cours d’exécution
                * Répertorier uniquement les distributions en cours d’exécution.

    * --Set-Default,-s<Distro>
        * Définit la distribution comme valeur par défaut.

    * --set-default-version<Version>
        * Modifie la version d’installation par défaut pour les nouvelles distributions.

    * --set-version <Distro><Version>
        * Modifie la version de la distribution spécifiée.

    * --Terminate,-t<Distro>
        * Met fin à la distribution spécifiée.

    * --annuler l’inscription<Distro>
        * Annule l’inscription de la distribution.

    * --help
        * Affichez les informations d’utilisation.

## <a name="additional-commands"></a>Commandes supplémentaires

Il existe également des commandes historiques pour interagir avec le sous-système Windows pour Linux. Leurs fonctionnalités sont comprises dans `wsl.exe`, mais elles peuvent toujours être utilisées. 

### `wslconfig.exe`

Cette commande vous permet de configurer votre distribution WSL. Vous trouverez ci-dessous une liste de ses options.

* /l,/list [option]
    * Répertorie les distributions inscrites.
        * /All: répertorie éventuellement toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.

        * /Running-répertorier uniquement les distributions en cours d’exécution.

* /s,/SetDefault<DistributionName>
    * Définit la distribution comme valeur par défaut.

* /t,/Terminate<DistributionName>
    * Met fin à la distribution.

* /u,/Unregister<DistributionName>
    * Annule l’inscription de la distribution.

### `bash.exe`

Cette commande permet de démarrer un interpréteur de commandes bash. Vous trouverez ci-dessous les options que vous pouvez utiliser avec cette commande.

* Aucune option donnée
    * Lance l’interpréteur de commandes bash dans le répertoire actif. Si l’interpréteur de commandes bash n’est pas installé automatiquement`lxrun /install`

* bash ~
    * Lance l’interpréteur de commandes bash dans le répertoire de départ de l’utilisateur.  Similaire à l' `cd ~`exécution de.

* bash-c "&lt;commande&gt;"
    * Exécute la commande, imprime la sortie et quitte l’invite de commandes Windows. <br/> <br/> Tels`bash -c "ls"`

## <a name="deprecated-commands"></a>Commandes déconseillées

`lxrun.exe` Était la première commande utilisée pour installer et gérer le sous-système Windows pour Linux. Elle est déconseillée à partir de Windows 10 1803 et versions ultérieures.

La commande `lxrun.exe` peut être utilisée pour interagir directement avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) .  Ces commandes sont installées dans `\Windows\System32` le répertoire et peuvent être exécutées dans une invite de commandes Windows ou dans PowerShell.

| Command                     | Description                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | La commande lxrun est utilisée pour gérer l’instance WSL. |
| `lxrun /install`            | Démarre le processus de téléchargement et d’installation. <br/> **/y** peut être ajouté pour ignorer toutes les invites.  L’invite de confirmation est automatiquement acceptée et l’utilisateur par défaut est défini sur root.          |
| `lxrun /uninstall`          | Désinstalle et supprime l’image Ubuntu.  Par défaut, cela ne supprime pas le répertoire d’hébergement Ubuntu de l’utilisateur. <br/> **/y** peut être ajouté pour accepter automatiquement l’invite de confirmation <br/>**/Full** désinstalle et supprime le répertoire de démarrage Ubuntu de l’utilisateur         |
| `lxrun /setdefaultuser <userName>`     | Définit le bash par défaut sur l’utilisateur Ubuntu. Demande un mot de passe si l’utilisateur spécifié n’existe pas.  Pour plus d’informations, https://aka.ms/wslusers visitez le site:. <br/> **/y** Ignore promping pour le mot de passe.  L’utilisateur sera créé sans mot de passe.|
| `lxrun /update`            | Met à jour l’index du package du sous-système          |
