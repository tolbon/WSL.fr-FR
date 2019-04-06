---
title: Interopérabilité Windows avec Linux
description: Décrit l’interopérabilité de Windows avec des distributions de Linux en cours d’exécution sur le sous-système Windows pour Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063247"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Sous-système Windows pour l’interopérabilité Linux avec Windows

> **Mise à jour pour Fall Creators Update.**  
Si vous exécutez Creators Update ou mise à jour anniversaire, passez directement à la [section de mise à jour Creators/anniversaire](interop.md#creators-update-and-anniversary-update).

Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.  Vous pouvez :

1. Appeler les fichiers binaires Windows à partir de la console Linux.
1. Appeler les fichiers binaires de Linux à partir d’une console Windows.
1. **Les Builds Windows Insiders 17063 +** partagent des variables d’environnement entre Linux et Windows.

Cela offre une expérience transparente entre Windows et WSL.  Détails techniques sont sur le [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Exécuter des outils Linux à partir d’une ligne de commande Windows

Exécuter des fichiers binaires de Linux à partir de l’invite de commandes Windows (CMD ou PowerShell) à l’aide `wsl.exe <command>`.

Fichiers binaires de l’appelé de cette façon :

1. Utiliser le même répertoire de travail en tant que l’invite CMD ou PowerShell actuel.
1. Exécuter en tant qu’utilisateur WSL par défaut.
1. Avoir les mêmes droits d’administration de Windows en tant que le processus appelant et le terminal.

Exemple :

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

La commande qui suit Linux `wsl.exe` est gérée comme n’importe quelle commande Exécuter dans WSL.  Les éléments tels que sudo, pipelines et la redirection de fichiers fonctionnent.

Exemple à l’aide de sudo :

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Exemples de combinaison de commandes WSL et Windows :

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Les commandes passées dans `wsl.exe` sont transférés vers le processus WSL sans modification.  Chemins d’accès de fichier doivent être spécifiés dans le format WSL.

Exemple avec des chemins d’accès :

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Exécuter des outils de Windows à partir de WSL

WSL peut appeler les fichiers binaires Windows directement à partir de la ligne de commande WSL à l’aide `[binary name].exe`.  Par exemple, `notepad.exe`.  Pour faciliter les exécutables Windows exécuter, chemin d’accès Windows est inclus dans le Linux `$PATH` dans Fall Creators Update.

Les applications exécutées de cette façon ont les propriétés suivantes :

1. Conserver le répertoire de travail en tant que l’invite de commandes WSL (la plupart du temps, les exceptions sont expliquées ci-dessous).
1. Avoir les mêmes droits d’autorisation que le processus WSL.
1. Exécuter en tant que l’utilisateur Windows actif.
1. S’affichent dans le Gestionnaire des tâches Windows comme si exécuté directement à partir de l’invite de commande.

Exemple :

``` BASH
$ notepad.exe
```

Les exécutables Windows s’exécutent dans WSL sont gérées de la même façon à natif Linux exécutables--tuyauterie, effectue une redirection et même backgrounding travail comme prévu.

Exemples d’utilisation de canaux :

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Exemple d’utilisation des commandes Windows et WSL mixtes :

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Les fichiers binaires Windows doivent inclure l’extension de fichier, correspond à la casse de fichier et être exécutable.  Non-fichiers exécutables, y compris les scripts de commandes.  Comme les commandes natives CMD `dir` peut être exécuté avec `cmd.exe /C` commande.

Exemples :

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Paramètres sont passés à la Windows binaire tels quels.

Par exemple, les commandes suivantes seront ouvre `C:\temp\foo.txt` dans `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Modification des fichiers situés sur VolFs (ne fichiers pas sous `/mnt/<x>`) avec un Windows application dans WSL n’est pas pris en charge.

Par défaut, WSL tente de conserver le répertoire de travail de la Windows binaire comme répertoire actuel WSL mais reviendra sur le répertoire de la création d’instance si le répertoire de travail se trouve sur VolFs.

Par exemple ; `wsl.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est modifié à l’accueil de l’utilisateur.  Lorsque `notepad.exe` est appelée à partir du répertoire de base de l’utilisateur, WSL revient automatiquement à `C:\temp` comme répertoire de travail notepad.exe :

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Partager des variables d’environnement entre Windows et WSL

> Disponible dans les builds Windows Insider 17063 et versions ultérieures.

Avant de 17063, était uniquement Windows variable d’environnement WSL pourrait accéder `PATH` (donc vous pouvez lancer des exécutables Win32 sous WSL).

À compter de 17063, WSL et Windows partagent `WSLENV`, une variable d’environnement spécial créée pour combler les distributions Windows et Linux en cours d’exécution sur WSL.

Propriétés de `WSLENV`:

* Elle est partagée ; Il existe dans les environnements Windows et WSL.
* C’est une liste de variables d’environnement à partager entre Windows et WSL.
* Il peut mettre en forme des variables d’environnement pour fonctionner correctement dans Windows et WSL.

Il existe quatre indicateurs disponibles dans `WSLENV` pour influencer la façon dont cette variable d’environnement est convertie.

`WSLENV` indicateurs :

* `/p` -Convertit le chemin d’accès entre les chemins de Win32 et style WSL/Linux.
* `/l` -Indique la variable d’environnement est une liste de chemins d’accès.
* `/u` -Indique que cette variable d’environnement doit uniquement apparaître lors de l’exécution WSL à partir de Win32.
* `/w` -Indique que cette variable d’environnement doit uniquement apparaître lors de l’exécution de Win32 à partir de WSL.

Indicateurs peuvent être combinées en fonction des besoins.

## <a name="disable-interop"></a>Désactiver l’interopérabilité

Les utilisateurs peuvent désactiver la capacité d’exécuter des fichiers binaires Windows pour une seule session WSL en exécutant la commande suivante en tant que racine :

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Pour réactiver Windows binaires quitter toutes les sessions WSL et réexécutez bash.exe ou exécutez la commande suivante en tant que racine :

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La désactivation d’interopérabilité n’est pas persistante entre les sessions WSL--interop est de nouveau activée lorsqu’une nouvelle session est lancée.

## <a name="creators-update-and-anniversary-update"></a>Creators Update et mise à jour anniversaire

Alors que l’automne préliminaire expérience interop Creators Update est similaire aux expériences d’interopérabilité plus récentes, il existe un handfull des différences majeures.

Résumé :

* `bash.exe` a été déconseillée et remplacée par `wsl.exe`.
* `-c` option pour une seule commande en cours d’exécution n’est pas nécessaire avec `wsl.exe`.
* Chemin d’accès de Windows est inclus dans le WSL `$PATH`

Le processus de désactivation d’interopérabilité est inchangé.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Appel de WSL à partir de la ligne de commande Windows

Les fichiers binaires de Linux peuvent être appelées à partir de l’invite de commandes Windows ou à partir de PowerShell.  Les fichiers binaires appelés de cette façon ont les propriétés suivantes :

1. Utiliser le même répertoire de travail en tant que l’invite CMD ou PowerShell.
1. Exécuter en tant qu’utilisateur WSL par défaut.
1. Avoir les mêmes droits d’administration de Windows en tant que le processus appelant et le terminal.

Exemple :

```console
C:\temp> bash -c "ls -la"
```

Commandes Linux appelés de cette façon sont gérées comme toute autre application Windows.  Éléments tels que la redirection de fichiers d’entrée et tuyauterie fonctionnent comme prévu.

Exemples :

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

Les commandes WSL passé dans `bash -c` sont transférés vers le processus WSL sans modification.  Chemins d’accès de fichier doivent être spécifiés dans le format WSL et être vigilant pour échapper les caractères appropriés. Exemple :

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Appel des fichiers binaires Windows à partir de WSL

Le sous-système Windows pour Linux peut appeler les fichiers binaires Windows directement à partir de la ligne de commande WSL.  Les applications exécutées de cette façon ont les propriétés suivantes :

1. Conserver le répertoire de travail en tant que l’invite de commandes WSL, sauf dans le scénario expliqué ci-dessous.
1. Ont les mêmes droits d’autorisation que le `bash.exe` processus. 
1. Exécuter en tant que l’utilisateur Windows actif.
1. S’affichent dans le Gestionnaire des tâches Windows comme si exécuté directement à partir de l’invite de commande.

Exemple :

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

Dans WSL, ces fichiers exécutables sont gérées similaire pour des exécutables natifs Linux.  Cela signifie l’ajout de répertoires pour le chemin d’accès de Linux et tuyauterie entre le fonctionnement des commandes comme prévu.  Exemples :

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Le fichier binaire Windows doit inclure l’extension de fichier, correspond à la casse de fichier et être exécutable.  Non-fichiers exécutables, y compris par lot de scripts et de commande comme `dir` peut être exécuté avec `/mnt/c/Windows/System32/cmd.exe /C` commande.

Exemples :

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Paramètres sont passés à la Windows binaire tels quels.  

Par exemple, les commandes suivantes seront ouvre `C:\temp\foo.txt` dans `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

Modification des fichiers situés sur VolFs (ne fichiers pas sous `/mnt/<x>`) avec un Windows application n’est pas pris en charge.  Par défaut, WSL tente de conserver le répertoire de travail de la Windows binaire comme répertoire actuel WSL mais reviendra sur le répertoire de la création d’instance si le répertoire de travail se trouve sur VolFs.

Par exemple ; `bash.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est modifié à l’accueil de l’utilisateur.  Lorsque `notepad.exe` est appelée à partir du répertoire de base de l’utilisateur, WSL revient automatiquement à `C:\temp` comme répertoire de travail notepad.exe :

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
