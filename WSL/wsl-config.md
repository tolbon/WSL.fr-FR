---
title: Gérer les distributions Linux
description: Lister les références et configurer plusieurs distributions Linux exécutées sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 51099f21fe44fd8c7e8682332c939fbe6d5e5827
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269868"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Gérer et configurer le sous-système Windows pour Linux

> S’applique à Windows 10 Fall Creators Update et versions ultérieures.  Consultez notre [guide d’installation](./install_guide.md) mis à jour pour essayer les nouvelles fonctionnalités de gestion et commencer à exécuter plusieurs distributions Linux à partir du Microsoft Store.

## <a name="ways-to-run-wsl"></a>Méthodes d’exécution de WSL

Il existe de nombreuses façons d’exécuter Linux avec le sous-système Windows pour Linux.

1. `[distro]`, par exemple `ubuntu`
1. `wsl.exe` ou `bash.exe`
1. `wsl [command]` ou `bash -c [command]`

La méthode que vous devez utiliser dépend de ce que vous faites.

### <a name="launch-wsl-by-distribution"></a>Lancer WSL par distribution

L’exécution d’une distribution à l’aide de son application spécifique à la distribution lance cette distribution dans sa propre fenêtre de console.

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

Cela revient à cliquer sur « Lancer » dans le Microsoft Store.

![Lancer WSL à partir du Microsoft Store](media/store-launch.png)

Vous pouvez également exécuter la distribution à partir de la ligne de commande en exécutant `[distribution].exe`.

L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon est qu’elle définit automatiquement votre répertoire de travail sur le répertoire de base de la distribution.

**Exemple :**

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

### <a name="wsl-and-wsl-command"></a>wsl et wsl [commande]

La meilleure façon d’exécuter WSL à partir de la ligne de commande consiste à utiliser `wsl.exe`.

**Exemple :**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

Non seulement l’utilitaire `wsl` conserve le répertoire de travail actuel, mais il vous permet d’exécuter une seule commande à côté de commandes Windows.

**Exemple :**

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

**Exemple :**

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

### <a name="windows-10-version-1903-and-later"></a>Windows 10 version 1903 et ultérieures

Vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), notamment pour lister les distributions disponibles, définir une distribution par défaut et désinstaller des distributions.

Chaque distribution Linux gère indépendamment ses propres configurations. Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.  Par exemple, `ubuntu /?`.

#### <a name="list-distributions"></a>Lister les distributions

`wsl -l`, `wsl --list`  
Liste les distributions Linux disponibles pour WSL.  Si une distribution est listée, elle est installée et prête à l’emploi.

`wsl --list --all`   
Liste toutes les distributions, y compris celles qui ne sont pas utilisables.  Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.  

`wsl --list --running`   
Liste toutes les distributions en cours d’exécution.

#### <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution WSL par défaut est celle qui s’exécute quand vous exécutez `wsl` depuis une ligne de commande.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Définit la distribution par défaut sur `<DistributionName>`.

**Exemple :**  
`wsl -s Ubuntu` définit ma distribution par défaut sur Ubuntu.  À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.  Si j’exécute `wsl`, une session Ubuntu s’ouvre.

#### <a name="unregister-and-reinstall-a-distribution"></a>Désinscrire et réinstaller une distribution

Les distributions Linux peuvent être installées par l’intermédiaire du Microsoft Store, mais elles ne peuvent pas être désinstallées par ce biais.  WSL Config permet de désinscrire/désinstaller des distributions.

La désinscription permet également de réinstaller les distributions.

> **Attention :** Une fois qu’une distribution est désinscrite, toutes les données, paramètres et logiciels associés à celle-ci sont définitivement perdus.  La réinstallation à partir du Store installe une nouvelle copie de la distribution.

`wsl --unregister <DistributionName>`  
Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.

Par exemple : `wsl --unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.  Quand j’exécute `wsl --list`, celui-ci n’est pas listé.

Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».

#### <a name="run-as-a-specific-user"></a>Exécuter en tant qu’utilisateur spécifique

`wsl -u <Username>`, `wsl --user <Username>`

Exécutez WSL en tant qu’utilisateur spécifié. Notez que l’utilisateur doit exister dans la distribution WSL.

#### <a name="run-a-specific-distribution"></a>Exécuter une distribution spécifique

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

Exécutez une distribution spécifiée de WSL ; cette opération peut être utilisée pour envoyer des commandes à une distribution spécifique sans avoir à changer la distribution par défaut.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versions antérieures à la version 1903 de Windows 10

WSL Config (`wslconfig.exe`) est un outil en ligne de commande permettant de gérer les distributions Linux exécutées sur le sous-système Windows pour Linux (WSL).  Il vous permet de lister les distributions disponibles, de définir une distribution par défaut et de désinstaller des distributions.

Même si WSL Config est utile pour les paramètres qui englobent ou coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.  Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.  Par exemple, `ubuntu /?`.

Pour voir toutes les options disponibles pour wslconfig, exécutez : `wslconfig /?`

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

#### <a name="list-distributions"></a>Lister les distributions

`wslconfig /list`  
Liste les distributions Linux disponibles pour WSL.  Si une distribution est listée, elle est installée et prête à l’emploi.

`wslconfig /list /all`  
Liste toutes les distributions, y compris celles qui ne sont pas utilisables.  Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.  

#### <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution WSL par défaut est celle qui s’exécute quand vous exécutez `wsl` depuis une ligne de commande.

`wslconfig /setdefault <DistributionName>`

Définit la distribution par défaut sur `<DistributionName>`.

**Exemple :**  
`wslconfig /setdefault Ubuntu` définit ma distribution par défaut sur Ubuntu.  À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.  Si j’exécute `wsl`, une session Ubuntu s’ouvre.

#### <a name="unregister-and-reinstall-a-distribution"></a>Désinscrire et réinstaller une distribution

Les distributions Linux peuvent être installées par l’intermédiaire du Microsoft Store, mais elles ne peuvent pas être désinstallées par ce biais.  WSL Config permet de désinscrire/désinstaller des distributions.

La désinscription permet également de réinstaller les distributions.

> **Attention :** Une fois qu’une distribution est désinscrite, toutes les données, paramètres et logiciels associés à celle-ci sont définitivement perdus.  La réinstallation à partir du Store installe une nouvelle copie de la distribution.

`wslconfig /unregister <DistributionName>`  
Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.

Par exemple : `wslconfig /unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.  Quand j’exécute `wslconfig /list`, celui-ci n’est pas listé.

Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».

## <a name="set-wsl-launch-settings"></a>Définir les paramètres de lancement de WSL

> **Disponible dans Windows Insider build 17093 et ultérieures**

Configurez automatiquement certaines fonctionnalités dans WSL afin de les appliquer chaque fois que vous lancez le sous-système à l’aide de `wsl.conf`. 

Pour le moment, cela comprend les options de montage automatique et la configuration réseau.

`wsl.conf` se trouve dans chaque distribution Linux dans `/etc/wsl.conf`. Si le fichier n’y est pas, vous pouvez le créer vous-même. WSL détecte l’existence du fichier et lit son contenu. Si le fichier est manquant ou incorrect (mise en forme incorrecte du balisage), WSL continue à se lancer normalement.

Voici un exemple de fichier `wsl.conf` que vous pouvez ajouter à vos distributions :

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

Conformément aux conventions .ini, les clés sont déclarées sous une section. 

WSL prend en charge deux sections : `automount` et `network`.

#### <a name="automount"></a>automount

Section : `[automount]`


| key        | value                          | par défaut      | Remarques                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | booléen                        | true         | `true` : les lecteurs fixes (c.-à-d. `C:/` ou `D:/`) sont automatiquement montés avec DrvFs sous `/mnt`.  `false` : les disques ne sont pas montés automatiquement, mais vous pouvez les monter manuellement ou par le biais de `fstab`.                                                                                                             |
| mountFsTab | booléen                        | true         | `true` : `/etc/fstab` est traité au démarrage de WSL. /etc/fstab est un fichier dans lequel vous pouvez déclarer d’autres systèmes de fichiers, comme un partage SMB. Ainsi, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage.                                                                                                                |
| root       | Chaîne                         | `/mnt/`      | Définit le répertoire dans lequel les lecteurs fixes sont montés automatiquement. Par exemple, si vous avez un répertoire dans WSL à l’emplacement `/windir/` et que vous le spécifiez en tant que racine, vos lecteurs fixes sont censés être montés à l’emplacement `/windir/c`.                                                                                              |
| options    | Liste de valeurs séparées par des virgules | Chaîne vide | Cette valeur est ajoutée à la chaîne des options de montage DrvFs par défaut. **Seules les options propres à DrvFs peuvent être spécifiées.** Les options que le fichier binaire de montage analyse normalement dans un indicateur ne sont pas prises en charge. Si vous souhaitez spécifier explicitement ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans /etc/fstab. |

Par défaut, WSL définit les options uid et gid sur la valeur de l’utilisateur par défaut (dans une distribution Ubuntu, l’utilisateur par défaut est créé avec uid=1000,gid=1000). Si l’utilisateur spécifie une option gid ou uid explicitement par le biais de cette clé, la valeur associée est remplacée. Dans le cas contraire, la valeur par défaut est toujours ajoutée.

**Remarque :** Ces options sont appliquées en tant qu’options de montage pour tous les lecteurs montés automatiquement. Pour changer les options d’un lecteur spécifique uniquement, utilisez /etc/fstab à la place.

#### <a name="network"></a>réseau

Étiquette de section : `[network]`

| key | value | par défaut | Remarques|
|:----|:----|:----|:----|
| generateHosts | booléen | `true` | `true` : WSL génère `/etc/hosts`. Le fichier `hosts` contient une carte statique de noms d’hôtes correspondant à l’adresse IP. |
| generateResolvConf | booléen | `true` | `true` : WSL génère `/etc/resolv.conf`. `resolv.conf` contient une liste de noms DNS capables de résoudre un nom d’hôte donné en son adresse IP. | 

#### <a name="interop"></a>interop

Étiquette de section : `[interop]`

Ces options sont disponibles dans Insider build 17713 et ultérieures.

| key | value | par défaut | Remarques|
|:----|:----|:----|:----|
| enabled | booléen | `true` | La définition de cette clé permet de déterminer si WSL prend en charge le lancement des processus Windows. |
| appendWindowsPath | booléen | `true` | La définition de cette clé détermine si WSL ajoute des éléments de chemin Windows à la variable d’environnement $PATH. | 
