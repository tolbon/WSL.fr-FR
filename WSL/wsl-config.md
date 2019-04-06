---
title: Gérer les Distributions de Linux
description: Référencer le listing et la configuration de plusieurs distributions de Linux en cours d’exécution sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063497"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>Gérer et configurer le sous-système de Windows pour Linux

> S’applique à Windows 10 Fall Creators Update et versions ultérieures.  Consultez notre mise à jour [guide d’installation](./install_guide.md) pour essayer les nouvelles fonctionnalités de gestion et de démarrer plusieurs distributions de Linux en cours d’exécution à partir du Windows Store.

## <a name="ways-to-run-wsl"></a>Façons d’exécuter WSL

Il existe de nombreuses façons d’exécuter Linux avec le sous-système Windows pour Linux.

1. `[distro]` ie `ubuntu`
1. `wsl.exe` ou Gestionnaire de configuration `bash.exe`
1. `wsl [command]` ou Gestionnaire de configuration `bash -c [command]`

Quelle méthode vous devez utiliser dépend de ce que vous faites.

### <a name="launch-wsl-by-distribution"></a>Lancez WSL par distribution

Une distribution à l’aide de son application de distribution spécifique en cours d’exécution lance cette distribution dans sa propre fenêtre de console.

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

Il est le même qu’un clic sur « Lancement » dans le Windows Store.

![Lancer WSL à partir du Windows Store](media/store-launch.png)

Vous pouvez également exécuter la distribution à partir de la ligne de commande en exécutant `[distribution].exe`.

L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon, qu’il remplace automatiquement votre répertoire de travail à partir du répertoire actuel au répertoire de base de la distribution.

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

À l’aide de la meilleure façon d’exécuter WSL à partir de la ligne de commande `wsl.exe`.

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

Non seulement `wsl` conserver le répertoire de travail en place, il vous permet d’exécuter une seule commande le long de commandes Windows de côté.

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


## <a name="managing-multiple-linux-distributions"></a>La gestion de plusieurs Distributions Linux

### <a name="windows-10-version-1903-and-later"></a>Windows 10 Version 1903 et versions ultérieure

Vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), y compris la liste des distributions disponibles, la définition d’une distribution par défaut et la désinstallation de distributions.

Chaque distribution Linux gère indépendamment de sa propre configuration. Pour afficher des commandes spécifiques à la distribution, exécutez `[distro.exe] /?`.  Par exemple : `ubuntu /?`.

#### <a name="list-distributions"></a>Distributions de liste

`wsl -l` , `wsl --list`  
Listes disponibles distributions de Linux sont disponibles pour WSL.  Si une distribution est répertoriée, il est installé et prêt à utiliser.

`wsl --list --all`   
Répertorie toutes les distributions, y compris ceux qui ne sont pas actuellement utilisable.  Ils peuvent être en train d’installer, désinstaller, ou sont dans un état interrompu.  

`wsl --list --running`   
Répertorie toutes les distributions qui sont en cours d’exécution.

#### <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution de WSL par défaut est celui qui s’exécute lorsque vous exécutez `wsl` sur une ligne de commande.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Définit la distribution par défaut `<DistributionName>`.

**Exemple :**  
`wsl -s Ubuntu` Définissez mon distribution par défaut d’Ubuntu.  Maintenant lors de l’exécution `wsl npm init` il s’exécutera sous Ubuntu.  Si j’exécute `wsl` il ouvrira une session d’Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Annuler l’inscription et de réinstaller une distribution

Linux distributions peuvent être installées via le Windows lors de la banque, ils ne peut pas être désinstallés via le Windows store.  WSL Config permet des distributions soit désinscrit ou désinstallé.

Annuler l’inscription permet également de distributions être réinstallé.

> **Attention :** Une fois la désinscription, toutes les données, les paramètres et les logiciels associés à cette distribution seront définitivement perdues.  La réinstallation à partir du magasin installera une nouvelle copie de la distribution.

`wsl --unregister <DistributionName>`  
Annule l’inscription de la distribution à partir de WSL afin de pouvoir être réinstallé ou nettoyée.

Par exemple : `wsl -unregister Ubuntu` supprimerait Ubuntu à partir des distributions disponibles dans WSL.  Lors de l’exécution `wsl --list` il ne sera pas répertorié.

Pour réinstaller, recherchez la répartition dans le Windows Store et sélectionnez « Lancement ».

#### <a name="run-as-a-specific-user"></a>Exécuter en tant qu’un utilisateur spécifique

`wsl -u <Username>`, `wsl --user <Username>`

Exécutez WSL en tant que l’utilisateur spécifié. Veuillez noter que l’utilisateur doit exister à l’intérieur de la distribution WSL.

#### <a name="run-a-specific-distribution"></a>Exécutez une distribution spécifique

`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`

Exécutez une distribution spécifiée de WSL, peut être utilisé pour envoyer des commandes à une distribution spécifique sans avoir à modifier votre valeur par défaut.

### <a name="versions-earlier-than-windows-10-version-1903"></a>Versions antérieures à Windows 10 Version 1903

Configuration de WSL (`wslconfig.exe`) est un outil de ligne de commande pour la gestion des distributions de Linux en cours d’exécution sur le sous-système Windows pour Linux (WSL).  Il vous permet de répertorier des distributions disponibles, définir une distribution par défaut et désinstaller des distributions.

Tandis que la configuration de WSL est utile pour les paramètres qui s’étendent sur ou de coordonnent les distributions, chaque distribution Linux gère indépendamment ses propres configurations.  Pour afficher des commandes spécifiques à la distribution, exécutez `[distro.exe] /?`.  Par exemple : `ubuntu /?`.

Pour afficher toutes les options disponibles pour wslconfig, exécutez :  `wslconfig /?`

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

#### <a name="list-distributions"></a>Distributions de liste

`wslconfig /list`  
Listes disponibles distributions de Linux sont disponibles pour WSL.  Si une distribution est répertoriée, il est installé et prêt à utiliser.

`wslconfig /list /all`  
Répertorie toutes les distributions, y compris ceux qui ne sont pas actuellement utilisable.  Ils peuvent être en train d’installer, désinstaller, ou sont dans un état interrompu.  

#### <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution de WSL par défaut est celui qui s’exécute lorsque vous exécutez `wsl` sur une ligne de commande.

`wslconfig /setdefault <DistributionName>`

Définit la distribution par défaut `<DistributionName>`.

**Exemple :**  
`wslconfig /setdefault Ubuntu` Définissez mon distribution par défaut d’Ubuntu.  Maintenant lors de l’exécution `wsl npm init` il s’exécutera sous Ubuntu.  Si j’exécute `wsl` il ouvrira une session d’Ubuntu.

#### <a name="unregister-and-reinstall-a-distribution"></a>Annuler l’inscription et de réinstaller une distribution

Linux distributions peuvent être installées via le Windows lors de la banque, ils ne peut pas être désinstallés via le Windows store.  WSL Config permet des distributions soit désinscrit ou désinstallé.

Annuler l’inscription permet également de distributions être réinstallé.

> **Attention :** Une fois la désinscription, toutes les données, les paramètres et les logiciels associés à cette distribution seront définitivement perdues.  La réinstallation à partir du magasin installera une nouvelle copie de la distribution.

`wslconfig /unregister <DistributionName>`  
Annule l’inscription de la distribution à partir de WSL afin de pouvoir être réinstallé ou nettoyée.

Par exemple : `wslconfig /unregister Ubuntu` supprimerait Ubuntu à partir des distributions disponibles dans WSL.  Lors de l’exécution `wslconfig /list` il ne sera pas répertorié.

Pour réinstaller, recherchez la répartition dans le Windows Store et sélectionnez « Lancement ».

## <a name="set-wsl-launch-settings"></a>Définir les paramètres de lancement WSL

> **Disponible dans Windows Insider Build 17093 et versions ultérieures**

Configurer automatiquement certaines fonctionnalités dans WSL qui est appliqué chaque fois que vous lancez le sous-système à l’aide `wsl.conf`. 

Droite, cela inclut désormais des options de montage automatique et la configuration du réseau.

`wsl.conf` se trouve dans chaque distribution Linux dans `/etc/wsl.conf`. Si le fichier n’y ne figure pas, vous pouvez le créer vous-même. WSL détecte l’existence du fichier et lit son contenu. Si le fichier est manquante ou incorrecte (autrement dit, incorrecte balisage mise en forme), WSL continuera à lancer comme d’habitude.

Voici un exemple `wsl.conf` fichier que vous pouvez ajouter dans vos distributions :

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

Conformément aux conventions .ini, les clés sont déclarés dans une section. 

WSL prend en charge les deux sections : `automount` et `network`.

#### <a name="automount"></a>Montage automatique

Section : `[automount]`


| Clé        | valeur                          | par défaut      | notes                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | booléen                        | true         | `true` causes fixé de lecteurs (ex.) `C:/` ou `D:/`) soit monté automatiquement avec DrvFs sous `/mnt`.  `false` signifie que les lecteurs ne sont pas automatiquement montés, mais vous pouvez toujours Montez-les manuellement ou via `fstab`.                                                                                                             |
| mountFsTab | booléen                        | true         | `true` définit `/etc/fstab` à traiter au démarrage WSL. / etc/fstab est un fichier dans lequel vous pouvez déclarer des autres systèmes de fichiers, comme un partage SMB. Par conséquent, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage de.                                                                                                                |
| Racine       | Chaîne                         | `/mnt/`      | Définit le répertoire dans lequel les lecteurs fixes seront automatiquement montés. Par exemple, si vous avez un répertoire dans WSL à `/windir/` et que vous spécifiez comme racine, vous pourriez l’exiger voir votre montés sur les lecteurs fixes `/windir/c`                                                                                              |
| options    | virgule comme séparateur de liste de valeurs | Chaîne vide | Cette valeur est ajoutée à la chaîne par défaut des options de montage de DrvFs. **Uniquement les options DrvFs spécifiques peuvent être spécifiées.** Options qui le montage binaire est alors normalement analysée en un indicateur ne sont pas prises en charge. Si vous souhaitez explicitement spécifier ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans/etc/fstab. |

Par défaut, WSL définit l’uid et gid à la valeur de l’utilisateur par défaut (dans la distribution Ubuntu, l’utilisateur par défaut est créé avec un ID utilisateur = 1000, gid = 1000). Si l’utilisateur spécifie une option gid ou uid explicitement par le biais de cette clé, la valeur associée est remplacée. Sinon, la valeur par défaut est toujours ajoutée.

**Remarque :** Ces options sont appliquées en tant que les options de montage pour tous les lecteurs montés automatiquement. Pour modifier les options pour un lecteur spécifique uniquement, utilisez plutôt/etc/fstab.

#### <a name="network"></a>réseau

Étiquette de la section : `[network]`

| Clé | valeur | par défaut | notes|
|:----|:----|:----|:----|
| generateHosts | booléen | `true` | `true` définit WSL pour générer `/etc/hosts`. Le `hosts` fichier contient un mappage statique de l’adresse IP correspondante de noms d’hôte. |
| generateResolvConf | booléen | `true` | `true` Définissez WSL pour générer `/etc/resolv.conf`. Le `resolv.conf` contient une liste DNS qui sont capables de résoudre un nom d’hôte donné à son adresse IP. | 

#### <a name="interop"></a>Interop

Étiquette de la section : `[interop]`

Ces options sont disponibles dans les initiés Build 17713 et versions ultérieures.

| Clé | valeur | par défaut | notes|
|:----|:----|:----|:----|
| enabled | booléen | `true` | Paramètre de cette clé déterminent si WSL prendra en charge les processus de lancement Windows. |
| appendWindowsPath | booléen | `true` | Paramètre de cette clé déterminent si WSL ajoute des éléments de chemin d’accès de Windows à la variable d’environnement $PATH. | 
