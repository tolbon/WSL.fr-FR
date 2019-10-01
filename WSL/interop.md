---
title: Interopérabilité Windows avec Linux
description: Décrit l’interopérabilité Windows avec les distributions Linux exécutées sur le sous-système Windows pour Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122734"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Interopérabilité du sous-système Windows pour Linux avec Windows

> **Mise à jour pour Fall Creators Update.**  
Si vous exécutez Mise à jour anniversaire ou Creators Update, passez à la [section Mise à jour anniversaire et Creators Update](interop.md#creators-update-and-anniversary-update).

Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.  Vous pouvez :

1. Appeler des fichiers binaires Windows à partir de la console Linux.
1. Appeler des fichiers binaires Linux à partir d’une console Windows.
1. **Builds Windows Insiders 17063 et ultérieures** Partager des variables d’environnement entre Linux et Windows.

Vous obtenez ainsi une expérience fluide entre Windows et WSL.  Vous trouverez les détails techniques sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Exécuter les outils Linux à partir d’une ligne de commande Windows

Exécutez des fichiers binaires Linux à partir de l’invite de commandes Windows (CMD ou PowerShell) en utilisant `wsl.exe <command>`.

Les fichiers binaires appelés de cette façon :

1. Utilisent le même répertoire de travail que l’invite CMD ou PowerShell en cours.
1. Sont exécutés en tant qu’utilisateur par défaut WSL.
1. Ont les mêmes droits d’administration Windows que le terminal et le processus appelant.

Par exemple :

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

La commande Linux qui suit `wsl.exe` est gérée comme n’importe quelle commande exécutée dans WSL.  Des actions comme l’exécution de sudo, la création de canaux et la redirection de fichiers fonctionnent.

Exemple d’utilisation de sudo :

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

Les commandes passées à `wsl.exe` sont transmises au processus WSL sans modification.  Les chemins de fichiers doivent être spécifiés au format WSL.

Exemple avec chemins :

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Exécuter des outils Windows à partir de WSL

WSL peut appeler des fichiers binaires Windows directement à partir de la ligne de commande WSL à l’aide de `[binary name].exe`.  Exemple : `notepad.exe`.  Pour faciliter l’exécution des exécutables Windows, le chemin Windows est inclus dans la variable Linux `$PATH` dans Fall Creators Update.

Les applications exécutées de cette manière ont les propriétés suivantes :

1. Conservent le répertoire de travail en tant qu’invite de commandes WSL (en général, les exceptions sont décrites ci-dessous).
1. Ont les mêmes autorisations que le processus WSL.
1. Sont exécutées en tant qu’utilisateur Windows actif.
1. Apparaissent dans le Gestionnaire des tâches de Windows comme si elles étaient directement exécutées à partir de l’invite CMD.

Exemple :

``` BASH
$ notepad.exe
```

Les exécutables Windows exécutés dans WSL sont gérés de la même façon que les exécutables Linux natifs : la création de canaux, les redirections et même le travail en arrière-plan fonctionnent comme prévu.

Exemples d’utilisation de canaux :

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Exemple d’utilisation de commandes Windows et WSL mixtes :

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Les fichiers binaires Windows doivent inclure l’extension de fichier, correspondre à la casse de fichier et être exécutables.  Les fichiers non exécutables, dont les scripts de commandes et  les commandes natives CMD comme `dir`, peuvent être exécutés avec la commande `cmd.exe /C`.

Exemples :

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Les paramètres sont passés au fichier binaire Windows non modifié.

Par exemple, les commandes suivantes ouvrent `C:\temp\foo.txt` dans `notepad.exe` :

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

La modification de fichiers situés sur VolFs (fichiers qui ne se trouvent pas sous `/mnt/<x>`) avec une application Windows dans WSL n’est pas prise en charge.

Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actif, mais a recours au répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.

Par exemple, `wsl.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est remplacé par le répertoire racine de l’utilisateur.  Quand `notepad.exe` est appelé à partir du répertoire racine de l’utilisateur, WSL rétablit automatiquement `C:\temp` comme répertoire de travail de notepad.exe :

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

> Disponible dans les builds Windows Insiders 17063 et ultérieures.

Avant la build 17063, la seule variable d’environnement Windows à laquelle WSL pouvait accéder était `PATH` (par conséquent, vous pouviez lancer des exécutables Win32 sous WSL).

À partir de la build 17063, WSL et Windows partagent `WSLENV`, une variable d’environnement spéciale créée pour relier les distributions Windows et Linux s’exécutant sur WSL.

Propriétés de la variable `WSLENV` :

* Elle est partagée et existe dans les environnements Windows et WSL.
* Il s’agit d’une liste de variables d’environnement à partager entre Windows et WSL.
* Elle peut mettre en forme des variables d’environnement pour fonctionner correctement dans Windows et WSL.

Quatre indicateurs sont disponibles dans `WSLENV` pour influencer la manière dont cette variable d’environnement est traduite.

Indicateurs `WSLENV` :

* `/p` : convertit le chemin entre les chemins de style WSL/Linux et les chemins Win32.
* `/l` : indique que la variable d’environnement est une liste de chemins.
* `/u` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de WSL à partir de Win32.
* `/w` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de Win32 à partir de WSL.

Les indicateurs peuvent être combinés en fonction des besoins.

## <a name="disable-interop"></a>Désactiver l’interopérabilité

Les utilisateurs peuvent désactiver la possibilité d’exécuter des fichiers binaires Windows pour une seule session WSL en exécutant la commande suivante en tant que racine :

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Pour réactiver les fichiers binaires Windows, fermez toutes les sessions WSL et réexécutez bash.exe, ou exécutez la commande suivante en tant que racine :

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La désactivation de l’interopérabilité n’est pas conservée entre les sessions WSL : l’interopérabilité sera réactivée lors du lancement d’une nouvelle session.

## <a name="creators-update-and-anniversary-update"></a>Mise à jour anniversaire et Creators Update

Alors que l’expérience d’interopérabilité avant Fall Creators Update est similaire à des expériences d’interopérabilité plus récentes, il existe quelques différences majeures.

Pour résumer :

* `bash.exe` a été déprécié et remplacé par `wsl.exe`.
* L’option `-c` permettant d’exécuter une seule commande n’est pas nécessaire avec `wsl.exe`.
* Le chemin Windows est inclus dans la variable WSL `$PATH`

Le processus de désactivation de l’interopérabilité est inchangé.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Appel de WSL à partir de la ligne de commande Windows

Les fichiers binaires Linux peuvent être appelés à partir de l’invite de commandes Windows ou de PowerShell.  Les fichiers binaires appelés de cette manière ont les propriétés suivantes :

1. Utilisent le même répertoire de travail que l’invite CMD ou PowerShell.
1. Sont exécutés en tant qu’utilisateur par défaut WSL.
1. Ont les mêmes droits d’administration Windows que le terminal et le processus appelant.

Exemple :

```console
C:\temp> bash -c "ls -la"
```

Les commandes Linux appelées de cette façon sont gérées comme n’importe quelle autre application Windows.  Des actions comme les entrées, la création de canaux et la redirection de fichiers fonctionnent comme prévu.

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

Les commandes WSL passées à `bash -c` sont transmises au processus WSL sans modification.  Les chemins de fichiers doivent être spécifiés au format WSL et des précautions doivent être prises pour placer les caractères appropriés dans une séquence d’échappement. Exemple :

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Appel des fichiers binaires Windows à partir de WSL

Le sous-système Windows pour Linux peut appeler des fichiers binaires Windows directement à partir de la ligne de commande WSL.  Les applications exécutées de cette manière ont les propriétés suivantes :

1. Conservent le répertoire de travail en tant qu’invite de commandes WSL, sauf dans le scénario décrit ci-dessous.
1. Ont les mêmes autorisations que le processus `bash.exe`. 
1. Sont exécutées en tant qu’utilisateur Windows actif.
1. Apparaissent dans le Gestionnaire des tâches de Windows comme si elles étaient directement exécutées à partir de l’invite CMD.

Exemple :

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

Dans WSL, ces exécutables sont gérés de la même façon que les exécutables Linux natifs.  Cela signifie que l’ajout de répertoires au chemin Linux et la création de canaux entre les commandes fonctionnent comme prévu.  Exemples :

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Le fichier binaire Windows doit inclure l’extension de fichier, correspondre à la casse de fichier et être exécutable.  Les fichiers non exécutables, dont les scripts de commandes et une commande comme `dir`, peuvent être exécutés avec la commande `/mnt/c/Windows/System32/cmd.exe /C`.

Exemples :

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Les paramètres sont passés au fichier binaire Windows non modifié.  

Par exemple, les commandes suivantes ouvrent `C:\temp\foo.txt` dans `notepad.exe` :

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

La modification de fichiers situés sur VolFs (fichiers qui ne se trouvent pas sous `/mnt/<x>`) avec une application Windows n’est pas prise en charge.  Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actif, mais a recours au répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.

Par exemple, `bash.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est remplacé par le répertoire racine de l’utilisateur.  Quand `notepad.exe` est appelé à partir du répertoire racine de l’utilisateur, WSL rétablit automatiquement `C:\temp` comme répertoire de travail de notepad.exe :

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
