---
title: Gérer les distributions Linux
description: Liste de références et configuration de plusieurs distributions Linux exécutées sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, WSL. conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: ca65cf6fde3e0ba4750ffc44f5aec542be6cfabf
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122707"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Gérer et configurer le sous-système Windows pour Linux

> S’applique à Windows 10 automne Creators Update et versions ultérieures.  Consultez notre [Guide d’installation](./install_guide.md) mis à jour pour essayer les nouvelles fonctionnalités de gestion et démarrer l’exécution de plusieurs distributions Linux à partir du Microsoft Store.

## <a name="ways-to-run-wsl"></a>Méthodes d’exécution de WSL

Il existe de nombreuses façons d’exécuter Linux avec le sous-système Windows pour Linux.

1. `[distro]`, par exemple`ubuntu`
1. `wsl.exe` ou `bash.exe`
1. `wsl [command]` ou `bash -c [command]`

La méthode que vous devez utiliser dépend de ce que vous faites.

### <a name="launch-wsl-by-distribution"></a>Lancer WSL par distribution

L’exécution d’une distribution à l’aide de son application spécifique à distribution lance cette distribution dans sa propre fenêtre de console.

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

Cela revient à cliquer sur «lancer» dans le Microsoft Store.

![Lancer WSL à partir du Microsoft Store](media/store-launch.png)

Vous pouvez également exécuter la distribution à partir de la ligne de `[distribution].exe`commande en exécutant.

L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon est qu’elle modifie automatiquement votre répertoire de travail du répertoire actif vers le répertoire de départ de la distribution.

**Exemple :**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>WSL et WSL [commande]

La meilleure façon d’exécuter WSL à partir de la ligne de `wsl.exe`commande consiste à utiliser.

**Exemple :**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

Non seulement `wsl` conserve le répertoire de travail actuel, mais il vous permet d’exécuter une seule commande sur les commandes Windows latérales.

**Exemple :**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**Exemple :**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>Gestion de plusieurs distributions Linux

### <a name="windows-10-version-1903-and-later"></a>Windows 10 version 1903 et versions ultérieures

Vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), notamment la liste des distributions disponibles, la définition d’une distribution par défaut et la désinstallation des distributions.

Chaque distribution Linux gère indépendamment ses propres configurations. Pour afficher les commandes spécifiques à la distribution `[distro.exe] /?`, exécutez.  Par exemple : `ubuntu /?`.

#### <a name="list-distributions"></a>Répertorier les distributions

`wsl -l`,`wsl --list`  
Répertorie les distributions Linux disponibles pour WSL.  Si une distribution est indiquée, elle est installée et prête à l’emploi.

`wsl --list --all`   
Répertorie toutes les distributions, y compris celles qui ne sont pas actuellement utilisables.  Ils peuvent être en cours d’installation, de désinstallation ou de rupture.  

`wsl --list --running`   
Répertorie toutes les distributions en cours d’exécution.

#### <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution WSL par défaut est celle qui s’exécute lorsque vous `wsl` exécutez sur une ligne de commande.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Définit la distribution par défaut `<DistributionName>`sur.

**Exemple :**  
`wsl -s Ubuntu`définit la distribution par défaut sur Ubuntu.  À présent, lorsque `wsl npm init` je l’exécute, il s’exécute sous Ubuntu.  Si je l' `wsl` exécute, une session Ubuntu s’ouvre.

#### <a name="unregister-and-reinstall-a-distribution"></a>Désinscrire et réinstaller une distribution

Alors que les distributions Linux peuvent être installées via le Microsoft Store, elles ne peuvent pas être désinstallées via le Windows Store.  WSL config permet d’annuler l’inscription/la désinstallation des distributions.

L’annulation de l’inscription permet également de réinstaller les distributions.

> **Attention :** Une fois l’inscription annulée, toutes les données, tous les paramètres et tous les logiciels associés à cette distribution seront définitivement perdus.  La réinstallation à partir du Store installe une copie propre de la distribution.

`wsl --unregister <DistributionName>`  
Annule l’enregistrement de la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.

Par exemple: `wsl --unregister Ubuntu` supprimez Ubuntu des distributions disponibles dans WSL.  Lorsque je l' `wsl --list` exécute, il ne figure pas dans la liste.

Pour réinstaller, recherchez la distribution dans le Microsoft Store et sélectionnez «lancer».

#### <a name="run-as-a-specific-user"></a>Exécuter en tant qu’utilisateur spécifique

`wsl -u <Username>`, `wsl --user <Username>`

Exécuter WSL en tant qu’utilisateur spécifié. Veuillez noter que l’utilisateur doit exister dans la distribution WSL.

#### <a name="run-a-specific-distribution"></a>Exécuter une distribution spécifique

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Exécuter une distribution spécifiée de WSL, peut être utilisé pour envoyer des commandes à une distribution spécifique sans avoir à modifier votre valeur par défaut.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versions antérieures à la version 1903 de Windows 10

WSL config (`wslconfig.exe`) est un outil de ligne de commande permettant de gérer les distributions Linux exécutées sur le sous-système Windows pour Linux (WSL).  Elle vous permet de répertorier les distributions disponibles, de définir une distribution par défaut et de désinstaller les distributions.

Alors que la configuration de WSL est utile pour les paramètres qui s’étendent ou coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.  Pour afficher les commandes spécifiques à la distribution `[distro.exe] /?`, exécutez.  Par exemple : `ubuntu /?`.

Pour afficher toutes les options disponibles pour wslconfig, exécutez:`wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>Répertorier les distributions

`wslconfig /list`  
Répertorie les distributions Linux disponibles pour WSL.  Si une distribution est indiquée, elle est installée et prête à l’emploi.

`wslconfig /list /all`  
Répertorie toutes les distributions, y compris celles qui ne sont pas actuellement utilisables.  Ils peuvent être en cours d’installation, de désinstallation ou de rupture.  

#### <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution WSL par défaut est celle qui s’exécute lorsque vous `wsl` exécutez sur une ligne de commande.

`wslconfig /setdefault <DistributionName>`

Définit la distribution par défaut `<DistributionName>`sur.

**Exemple :**  
`wslconfig /setdefault Ubuntu`définit la distribution par défaut sur Ubuntu.  À présent, lorsque `wsl npm init` je l’exécute, il s’exécute sous Ubuntu.  Si je l' `wsl` exécute, une session Ubuntu s’ouvre.

#### <a name="unregister-and-reinstall-a-distribution"></a>Désinscrire et réinstaller une distribution

Alors que les distributions Linux peuvent être installées via le Microsoft Store, elles ne peuvent pas être désinstallées via le Windows Store.  WSL config permet d’annuler l’inscription/la désinstallation des distributions.

L’annulation de l’inscription permet également de réinstaller les distributions.

> **Attention :** Une fois l’inscription annulée, toutes les données, tous les paramètres et tous les logiciels associés à cette distribution seront définitivement perdus.  La réinstallation à partir du Store installe une copie propre de la distribution.

`wslconfig /unregister <DistributionName>`  
Annule l’enregistrement de la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.

Par exemple: `wslconfig /unregister Ubuntu` supprimez Ubuntu des distributions disponibles dans WSL.  Lorsque je l' `wslconfig /list` exécute, il ne figure pas dans la liste.

Pour réinstaller, recherchez la distribution dans le Microsoft Store et sélectionnez «lancer».

## <a name="set-wsl-launch-settings"></a>Définir les paramètres de lancement de WSL

> **Disponible dans Windows Insider Build 17093 et versions ultérieures**

Configurez automatiquement certaines fonctionnalités dans WSL qui seront appliquées chaque fois que vous lancerez le `wsl.conf`sous-système à l’aide de. 

Pour le moment, cela comprend les options de montage automatique et la configuration réseau.

`wsl.conf`se trouve dans chaque distribution Linux dans `/etc/wsl.conf`. Si le fichier n’est pas là, vous pouvez le créer vous-même. WSL détectera l’existence du fichier et lira son contenu. Si le fichier est manquant ou incorrect (il s’agit d’une mise en forme de balisage incorrecte), WSL continuera à se lancer normalement.

Voici un exemple `wsl.conf` de fichier que vous pouvez ajouter à votre distributions:

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>Options de configuration

Conformément aux conventions. ini, les clés sont déclarées sous une section. 

WSL prend en charge deux `automount` sections `network`: et.

#### <a name="automount"></a>montage automatique

Section`[automount]`


| Clé        | valeur                          | par défaut      | Notes                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | booléenne                        | true         | `true`provoque des lecteurs fixes (c.-à-d. `C:/`ou `D:/`) à monter automatiquement avec DrvFs sous `/mnt`.  `false`signifie que les disques ne seront pas montés automatiquement, mais vous pouvez les monter `fstab`manuellement ou via.                                                                                                             |
| mountFsTab | booléenne                        | true         | `true`définit `/etc/fstab` à traiter au démarrage de WSL. /etc/fstab est un fichier dans lequel vous pouvez déclarer d’autres systèmes de fichiers, comme un partage SMB. Par conséquent, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage.                                                                                                                |
| causes       | String                         | `/mnt/`      | Définit le répertoire dans lequel les lecteurs fixes seront montés automatiquement. Par exemple, si vous avez un répertoire dans WSL à `/windir/` l’adresse et que vous le spécifiez en tant que racine, vous vous attendez à ce que vos lecteurs fixes soient montés sur`/windir/c`                                                                                              |
| options    | liste de valeurs séparées par des virgules | chaîne vide | Cette valeur est ajoutée à la chaîne des options de montage DrvFs par défaut. **Seules les options spécifiques à DrvFs peuvent être spécifiées.** Les options que le fichier binaire de montage analyse normalement dans un indicateur ne sont pas prises en charge. Si vous souhaitez spécifier explicitement ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans/etc/fstab. |

Par défaut, WSL définit l’UID et le GID sur la valeur de l’utilisateur par défaut (dans Ubuntu distribution, l’utilisateur par défaut est créé avec UID = 1000, GID = 1000). Si l’utilisateur spécifie une option GID ou uid explicitement via cette clé, la valeur associée est remplacée. Dans le cas contraire, la valeur par défaut sera toujours ajoutée.

**Remarque :** Ces options sont appliquées en tant qu’options de montage pour tous les lecteurs montés automatiquement. Pour modifier les options d’un lecteur spécifique uniquement, utilisez/etc/fstab à la place.

#### <a name="network"></a>réseau

Étiquette de section:`[network]`

| Clé | valeur | par défaut | Notes|
|:----|:----|:----|:----|
| generateHosts | booléenne | `true` | `true`définit WSL à générer `/etc/hosts`. Le `hosts` fichier contient une carte statique de noms d’hôtes correspondant à l’adresse IP. |
| generateResolvConf | booléenne | `true` | `true`Définissez WSL sur Generate `/etc/resolv.conf`. Le `resolv.conf` contient une liste DNS capable de résoudre un nom d’hôte donné en son adresse IP. | 

#### <a name="interop"></a>salon

Étiquette de section:`[interop]`

Ces options sont disponibles dans la build Insider 17713 et versions ultérieures.

| Clé | valeur | par défaut | Notes|
|:----|:----|:----|:----|
| enabled | booléenne | `true` | La définition de cette clé permet de déterminer si WSL prend en charge le lancement des processus Windows. |
| appendWindowsPath | booléenne | `true` | La définition de cette clé détermine si WSL ajoute des éléments de chemin d’accès Windows à la variable d’environnement $PATH. | 
