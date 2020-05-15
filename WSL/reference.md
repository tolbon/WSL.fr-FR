---
title: Informations de référence sur les commandes du sous-système Windows pour Linux
description: Liste des commandes de gestion du sous-système Windows pour Linux
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows pour Linux, sous-système Windows, Ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 72b78a73bf68b28dd14b4826943a0c81ea04bbad
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270873"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Informations de référence sur les commandes pour le sous-système Windows pour Linux

La commande `wsl.exe` offre le meilleur moyen d’interagir avec le sous-système Windows pour Linux.

## <a name="set-wsl-2-as-your-default-version"></a>Définir WSL 2 comme version par défaut

Exécutez la commande suivante dans PowerShell pour définir WSL 2 comme version par défaut lors de l’installation d’une nouvelle distribution Linux :

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Définir votre version de distribution sur WSL 1 ou WSL 2

Vous pouvez vérifier la version WSL affectée à chacune des distributions Linux que vous avez installées en ouvrant la ligne de commande PowerShell et en entrant la commande (disponible uniquement dans la [build Windows 19041 ou ultérieure](ms-settings:windowsupdate)) : `wsl -l -v`

```bash
wsl --list --verbose
```

Pour définir une distribution devant reposer sur l’une ou l’autre des versions WSL, exécutez :

```bash
wsl --set-version <distribution name> <versionNumber>
```

Veillez à remplacer `<distribution name>` par le vrai nom de votre distribution et `<versionNumber>` par le chiffre « 1 » ou « 2 ». Vous pouvez revenir à WSL 1 quand vous voulez en exécutant la même commande que ci-dessus, mais en remplaçant le « 2 » par un « 1 ».

Par ailleurs, si vous souhaitez faire de WSL 2 votre architecture par défaut, utilisez cette commande :

```bash
wsl --set-default-version 2
```

Cela permet de définir la version de toute nouvelle distribution installée sur WSL 2.

## `wsl.exe`

Voici une liste complète des options pouvant être utilisées avec la commande `wsl.exe` à partir de la version 1903 de Windows.

Utilisation : `wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-commands"></a>Arguments pour l’exécution de commandes Linux

* **Sans argument**

  Si aucune ligne de commande n’est fournie, wsl.exe lance le shell par défaut.

* **--exec, -e \<Ligne de commande>**
  
  Exécute la commande spécifiée sans utiliser le shell Linux par défaut.

* **--**
  
  Transmet le reste de la ligne de commande tel quel.

Les commandes ci-dessus acceptent également les options suivantes :

* **--distribution, -d \<Distribution>**

  Exécute la distribution spécifiée.

* **--user, -u \<Nom d’utilisateur>**

  Procède à l’exécution sous l’utilisateur spécifié.

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Arguments pour la gestion du sous-système Windows pour Linux

* **--export \<Distribution> \<Nom de fichier>**
  
  Exporte la distribution vers un fichier tar. Le nom de fichier peut être - pour une sortie standard.

* **--import \<Distribution> \<Emplacement d’installation> \<Nom de fichier>**
  
  Importe le fichier tar spécifié en tant que nouvelle distribution. Le nom de fichier peut être - pour une entrée standard.

* **--list, -l [Options]**
  
  Liste les distributions.

  Options :
  * **--all**

    Liste toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation.

  * **--running**

    Liste uniquement les distributions en cours d’exécution.

* **--set-default, -s \<Distribution>**
  
  Définit la distribution en tant que distribution par défaut.

* **--terminate, -t \<Distribution>**
  
  Met fin à la distribution spécifiée.

* **--unregister \<Distribution>**
  
  Annule l’inscription de la distribution.

* **--help** Affiche des informations sur l’utilisation.

## <a name="additional-commands"></a>Commandes supplémentaires

Certaines commandes historiques permettent également d’interagir avec le sous-système Windows pour Linux. `wsl.exe` englobe leurs fonctionnalités, mais elles restent toujours à disposition.

### `wslconfig.exe`

Cette commande vous permet de configurer votre distribution WSL. Voici une liste des options correspondantes.

Utilisation : `wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>Arguments

* **/l, /list [Options]**
  
  Liste les distributions inscrites.
  
Options :

* **/all** Liste toutes les distributions, y compris les distributions en cours d’installation ou de désinstallation (facultatif).

* **/running** Liste uniquement les distributions en cours d’exécution.

* **/s, /setdefault \<Distro>** Définit la distribution en tant que distribution par défaut.

* **/t, /terminate \<Distro>** Met fin à la distribution.

* **/u, /unregister \<Distro>** Annule l’inscription de la distribution.

* **/upgrade \<Distro>** Met à niveau la distribution vers le format du système de fichiers WslFs.

### `bash.exe`

Cette commande permet de démarrer un shell Bash. Vous trouverez ci-dessous les options que vous pouvez utiliser avec cette commande.

Utilisation : `bash [Options...]`

* **Aucune option indiquée**
  
  Lance le shell Bash dans le répertoire actif. Si le shell Bash n’est pas installé, cette commande lance automatiquement `lxrun /install`.

* **~**
  
  `bash ~` lance le shell Bash dans le répertoire de base de l’utilisateur.  Cette option est similaire à `cd ~`.

* **-c "\<commande>"**
  
  Exécute la commande, affiche la sortie et revient à l’invite de commandes Windows.

  Par exemple : `bash -c "ls"`.

## <a name="deprecated-commands"></a>Commandes dépréciées

`lxrun.exe` était la première commande utilisée pour installer et gérer le sous-système Windows pour Linux. Elle est dépréciée pour les versions 1803 et ultérieures de Windows 10.

La commande `lxrun.exe` peut être utilisée pour interagir directement avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-).  Ces commandes sont installées dans le répertoire `\Windows\System32` et peuvent être exécutées dans une invite de commandes Windows ou dans PowerShell.

| Commande                     | Description                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | La commande lxrun est utilisée pour gérer l’instance de WSL. |
| `lxrun /install`            | Démarre le processus de téléchargement et d’installation. <br/> **/y** peut être ajouté pour ignorer toutes les invites.  L’invite de confirmation est automatiquement acceptée et l’utilisateur par défaut est défini sur la racine.          |
| `lxrun /uninstall`          | Désinstalle et supprime l’image Ubuntu.  Par défaut, le répertoire de base Ubuntu de l’utilisateur n’est pas supprimé. <br/> **/y** peut être ajouté pour accepter automatiquement l’invite de confirmation. <br/>**/full** désinstalle et supprime le répertoire de base Ubuntu de l’utilisateur.         |
| `lxrun /setdefaultuser <userName>`     | Définit l’utilisateur Bash sur Ubuntu par défaut. Demande un mot de passe si l’utilisateur spécifié n’existe pas.  Pour plus d’informations, consultez : https://aka.ms/wslusers. <br/> **/y** ignore la demande de mot de passe.  L’utilisateur sera créé sans mot de passe.|
| `lxrun /update`            | Met à jour l’index du package du sous-système.          |
