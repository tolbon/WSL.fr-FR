---
title: Gérer les distributions Linux
description: Lister les références et configurer plusieurs distributions Linux exécutées sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: e72822bdec0ef5788bd384a5795a91d746428800
ms.sourcegitcommit: e6e888f2b88a2d9c105cee46e5ab5b70aa43dd80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83343892"
---
# <a name="wsl-commands-and-launch-configurations"></a>Commandes WSL et configurations de lancement

## <a name="ways-to-run-wsl"></a>Méthodes d’exécution de WSL

Il existe plusieurs façons d’exécuter une distribution Linux avec WSL une fois qu’elle est [installée](install-win10.md).

1. Ouvrez votre distribution Linux en visitant le menu Démarrer de Windows et en tapant le nom de vos distributions installées. Par exemple : « Ubuntu ».
2. À partir de l’invite de commandes Windows ou de PowerShell, entrez le nom de votre distribution installée. Par exemple : `ubuntu`
3. À partir de l’invite de commandes Windows ou de PowerShell, pour ouvrir votre distribution Linux par défaut à l’intérieur de la ligne de commande actuelle, entrez : `wsl.exe` .
4. À partir de l’invite de commandes Windows ou de PowerShell, pour ouvrir votre distribution Linux par défaut à l’intérieur de la ligne de commande actuelle, entrez : `wsl [command]` .

La méthode que vous devez utiliser dépend de ce que vous faites. Si vous avez ouvert une ligne de commande WSL dans une fenêtre d’invite de commandes Windows ou PowerShell et que vous souhaitez quitter, entrez la commande suivante : `exit` .

## <a name="launch-wsl-by-distribution"></a>Lancer WSL par distribution

L’exécution d’une distribution à l’aide de son application spécifique à la distribution lance cette distribution dans sa propre fenêtre de console.

![Lancer WSL à partir du menu Démarrer](media/start-launch.png)

Cela revient à cliquer sur « Lancer » dans le Microsoft Store.

![Lancer WSL à partir du Microsoft Store](media/store-launch.png)

Vous pouvez également exécuter la distribution à partir de la ligne de commande en exécutant `[distribution].exe`.

L’inconvénient de l’exécution d’une distribution à partir de la ligne de commande de cette façon est qu’elle définit automatiquement votre répertoire de travail sur le répertoire de base de la distribution.

**Exemple : (à l’aide de PowerShell)**

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

**Exemple : (à l’aide de PowerShell)**

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

**Exemple : (à l’aide de PowerShell)**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

**Exemple : (à l’aide de PowerShell)**

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

Dans Windows 10 version 1903 [et versions ultérieures](ms-settings:windowsupdate), vous pouvez utiliser `wsl.exe` pour gérer vos distributions dans le sous-système Windows pour Linux (WSL), notamment pour répertorier les distributions disponibles, définir une distribution par défaut et désinstaller des distributions.

Chaque distribution Linux gère indépendamment ses propres configurations. Pour voir les commandes propres à une distribution, exécutez `[distro.exe] /?`.  Par exemple, `ubuntu /?`.

## <a name="list-distributions"></a>Lister les distributions

`wsl -l` , `wsl --list`  
Liste les distributions Linux disponibles pour WSL.  Si une distribution est listée, elle est installée et prête à l’emploi.

`wsl --list --all`Répertorie toutes les distributions, y compris celles qui ne sont pas actuellement utilisables.  Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.  

`wsl --list --running`Répertorie toutes les distributions en cours d’exécution.

## <a name="set-a-default-distribution"></a>Définir une distribution par défaut

La distribution WSL par défaut est celle qui s’exécute quand vous exécutez `wsl` depuis une ligne de commande.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Définit la distribution par défaut sur `<DistributionName>`.

**Exemple : (à l’aide de PowerShell)**  
`wsl -s Ubuntu` définit ma distribution par défaut sur Ubuntu.  À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.  Si j’exécute `wsl`, une session Ubuntu s’ouvre.

## <a name="unregister-and-reinstall-a-distribution"></a>Désinscrire et réinstaller une distribution

Les distributions Linux peuvent être installées par l’intermédiaire du Microsoft Store, mais elles ne peuvent pas être désinstallées par ce biais.  WSL Config permet de désinscrire/désinstaller des distributions.

La désinscription permet également de réinstaller les distributions.

> **Attention :** Une fois l’inscription annulée, toutes les données, tous les paramètres et tous les logiciels associés à cette distribution seront définitivement perdus.  La réinstallation à partir du Store installe une nouvelle copie de la distribution.

`wsl --unregister <DistributionName>`  
Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.

Par exemple : `wsl --unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.  Quand j’exécute `wsl --list`, celui-ci n’est pas listé.

Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».

## <a name="run-as-a-specific-user"></a>Exécuter en tant qu’utilisateur spécifique

`wsl -u <Username>`, `wsl --user <Username>`

Exécutez WSL en tant qu’utilisateur spécifié. Notez que l’utilisateur doit exister dans la distribution WSL.

## <a name="change-the-default-user-for-a-distribution"></a>Modifier l’utilisateur par défaut pour une distribution

`<DistributionName> config --default-user <Username>`

Modifiez l’utilisateur par défaut de votre journal de distribution. L’utilisateur doit déjà exister à l’intérieur de la distribution afin de devenir l’utilisateur par défaut. 

Par exemple : `ubuntu config --default-user johndoe` modifier l’utilisateur par défaut de la distribution Ubuntu pour l’utilisateur « JohnDoe ».

> [!NOTE]
> Si vous avez des difficultés à déterminer le nom de votre distribution, consultez la section [répertorier les distributions](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) de la commande pour répertorier le nom officiel des distributions installées. 

## <a name="run-a-specific-distribution"></a>Exécuter une distribution spécifique

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

Exécutez une distribution spécifiée de WSL ; cette opération peut être utilisée pour envoyer des commandes à une distribution spécifique sans avoir à changer la distribution par défaut.

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a>Gestion de plusieurs distributions Linux dans des versions antérieures de Windows

Dans Windows 10 antérieures à la version 1903, l' `wslconfig.exe` outil en ligne de commande WSL config () doit être utilisé pour gérer les distributions Linux exécutées sur le sous-système Windows pour Linux (WSL).  Il vous permet de lister les distributions disponibles, de définir une distribution par défaut et de désinstaller des distributions.

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

Pour répertorier les distributions, utilisez :

`wslconfig /list`  
Liste les distributions Linux disponibles pour WSL.  Si une distribution est listée, elle est installée et prête à l’emploi.

`wslconfig /list /all`  
Liste toutes les distributions, y compris celles qui ne sont pas utilisables.  Elles peuvent être en cours d’installation, de désinstallation ou dans un état défectueux.  

Pour définir une distribution par défaut qui s’exécute lorsque vous exécutez `wsl` sur une ligne de commande :

`wslconfig /setdefault <DistributionName>`Définit la distribution par défaut sur `<DistributionName>` .

**Exemple : (à l’aide de PowerShell)**  
`wslconfig /setdefault Ubuntu` définit ma distribution par défaut sur Ubuntu.  À présent, quand j’exécute `wsl npm init`, elle s’exécute dans Ubuntu.  Si j’exécute `wsl`, une session Ubuntu s’ouvre.

Pour annuler l’inscription et réinstaller une distribution :

`wslconfig /unregister <DistributionName>`  
Désinscrit la distribution de WSL pour qu’elle puisse être réinstallée ou nettoyée.

Par exemple : `wslconfig /unregister Ubuntu` supprime Ubuntu des distributions disponibles dans WSL.  Quand j’exécute `wslconfig /list`, celui-ci n’est pas listé.

Pour réinstaller la distribution, recherchez-la dans le Microsoft Store et sélectionnez « Lancer ».

## <a name="configure-per-distro-launch-settings-with-wslconf"></a>Configurer les paramètres de lancement de distribution avec wslconf

> **Disponible dans Windows Build 17093 et versions ultérieures**

Configurez automatiquement certaines fonctionnalités dans WSL afin de les appliquer chaque fois que vous lancez le sous-système à l’aide de `wsl.conf`.

Pour le moment, cela comprend les options de montage automatique et la configuration réseau.

`wsl.conf` se trouve dans chaque distribution Linux dans `/etc/wsl.conf`. Si le fichier n’y est pas, vous pouvez le créer vous-même. WSL détecte l’existence du fichier et lit son contenu. Si le fichier est manquant ou incorrect (mise en forme incorrecte du balisage), WSL continue à se lancer normalement.

Voici un exemple de `wsl.conf` fichier que vous pouvez ajouter à vos distributions :

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>Options de configuration

Conformément aux conventions .ini, les clés sont déclarées sous une section. 

WSL prend en charge deux sections : `automount` et `network`.

#### <a name="automount"></a>automount

Section : `[automount]`

| key        | value                          | default      | Remarques                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | booléen                        | true         | `true` : les lecteurs fixes (c.-à-d. `C:/` ou `D:/`) sont automatiquement montés avec DrvFs sous `/mnt`.  `false`signifie que les disques ne seront pas montés automatiquement, mais vous pouvez les monter manuellement ou via `fstab` .                                                                                                             |
| mountFsTab | booléen                        | true         | `true` : `/etc/fstab` est traité au démarrage de WSL. /etc/fstab est un fichier dans lequel vous pouvez déclarer d’autres systèmes de fichiers, comme un partage SMB. Ainsi, vous pouvez monter ces systèmes de fichiers automatiquement dans WSL au démarrage.                                                                                                                |
| root       | String                         | `/mnt/`      | Définit le répertoire dans lequel les lecteurs fixes sont montés automatiquement. Par exemple, si vous avez un répertoire dans WSL à l’emplacement `/windir/` et que vous le spécifiez en tant que racine, vos lecteurs fixes sont censés être montés à l’emplacement `/windir/c`.                                                                                              |
| options    | Liste de valeurs séparées par des virgules | Chaîne vide | Cette valeur est ajoutée à la chaîne des options de montage DrvFs par défaut. **Seules les options propres à DrvFs peuvent être spécifiées.** Les options que le fichier binaire de montage analyse normalement dans un indicateur ne sont pas prises en charge. Si vous souhaitez spécifier explicitement ces options, vous devez inclure chaque lecteur pour lequel vous souhaitez le faire dans /etc/fstab. |

Par défaut, WSL définit les options uid et gid sur la valeur de l’utilisateur par défaut (dans une distribution Ubuntu, l’utilisateur par défaut est créé avec uid=1000,gid=1000). Si l’utilisateur spécifie une option gid ou uid explicitement par le biais de cette clé, la valeur associée est remplacée. Dans le cas contraire, la valeur par défaut est toujours ajoutée.

**Remarque :** Ces options sont appliquées en tant qu’options de montage pour tous les lecteurs montés automatiquement. Pour changer les options d’un lecteur spécifique uniquement, utilisez /etc/fstab à la place.

#### <a name="mount-options"></a>Options de montage

La définition des différentes options de montage pour les lecteurs Windows (DrvFs) peut contrôler la façon dont les autorisations de fichier sont calculées pour les fichiers Windows. Les options suivantes sont disponibles :

| Clé | Description | Par défaut |
|:----|:----|:----|
|uid| identifiant utilisateur utilisé pour le propriétaire de tous les fichiers | identifiant utilisateur par défaut de votre distribution WSL (à la première installation, la valeur par défaut est 1000)
|gid| identifiant de groupe utilisé pour le propriétaire de tous les fichiers | identifiant de groupe par défaut de votre distribution WSL (à la première installation, la valeur par défaut est 1000)
|umask | masque octal des autorisations à exclure pour tous les fichiers et répertoires | 000
|fmask | masque octal des autorisations à exclure pour tous les fichiers | 000
|dmask | masque octal des autorisations à exclure pour tous les répertoires | 000

**Remarque :** Les masques d’autorisation passent par une opération OR logique avant d’être appliqués aux fichiers et aux répertoires. 

#### <a name="network"></a>réseau

Étiquette de section : `[network]`

| key | value | default | Remarques|
|:----|:----|:----|:----|
| generateHosts | booléen | `true` | `true` : WSL génère `/etc/hosts`. Le fichier `hosts` contient une carte statique de noms d’hôtes correspondant à l’adresse IP. |
| generateResolvConf | booléen | `true` | `true` : WSL génère `/etc/resolv.conf`. `resolv.conf` contient une liste de noms DNS capables de résoudre un nom d’hôte donné en son adresse IP. | 

#### <a name="interop"></a>interop

Étiquette de section : `[interop]`

Ces options sont disponibles dans Insider build 17713 et ultérieures.

| key | value | default | Remarques|
|:----|:----|:----|:----|
| enabled | booléen | `true` | La définition de cette clé permet de déterminer si WSL prend en charge le lancement des processus Windows. |
| appendWindowsPath | booléen | `true` | La définition de cette clé détermine si WSL ajoute des éléments de chemin Windows à la variable d’environnement $PATH. |

#### <a name="user"></a>utilisateur

Étiquette de section : `[user]`

Ces options sont disponibles dans Build 18980 et versions ultérieures.

| key | value | default | HDInsight|
|:----|:----|:----|:----|
| default | string | Nom d’utilisateur initial créé lors de la première exécution | La définition de cette clé spécifie l’utilisateur à exécuter comme lors du premier démarrage d’une session WSL. |

## <a name="configure-global-options-with-wslconfig"></a>Configurer des options globales avec. wslconfig

> **Disponible dans Windows Build 19041 et versions ultérieures**

Vous pouvez configurer des options globales de WSL en plaçant un `.wslconfig` fichier dans le répertoire racine de votre dossier utilisateurs : `C:\Users\<yourUserName>\.wslconfig` . Ce fichier peut contenir les options suivantes :

### <a name="wsl-2-settings"></a>Paramètres WSL 2

Ces paramètres affectent la machine virtuelle qui alimente toute distribution WSL 2. 

| key | value | default | HDInsight|
|:----|:----|:----|:----|
| noyau | string | Boîte de réception fournie par le noyau Microsoft | Chemin Windows absolu vers un noyau Linux personnalisé. |
| memory | taille | 80% de la mémoire totale sur Windows | Quantité de mémoire à affecter à la machine virtuelle WSL 2. |
| processeurs | nombre | Le même nombre de processeurs sur Windows | Nombre de processeurs à assigner à la machine virtuelle WSL 2. |
| localhostForwarding | boolean | `true` | Valeur booléenne spécifiant si les ports liés à un caractère générique ou localhost dans la machine virtuelle WSL 2 doivent être connectés à partir de l’hôte via localhost : port. |
| kernelCommandLine | string | Vide | Arguments de ligne de commande du noyau supplémentaires. |
| swap | taille | 25% de la taille de la mémoire sur Windows arrondie aux Go les plus proches | Espace d’échange à ajouter à la machine virtuelle WSL 2, 0 pour aucun fichier d’échange. |
| Échange | taille | %USERPROFILE%\AppData\Local\Temp\swap.vhdx | Chemin d’accès Windows absolu au disque dur virtuel d’échange. |

Les entrées avec la `path` valeur doivent être des chemins d’accès Windows avec des barres obliques inverses par échappement, par exemple :`C:\\Temp\\myCustomKernel`

Les entrées avec la `size` valeur doivent être une taille suivie d’une unité, par exemple `8GB` ou `512MB` .