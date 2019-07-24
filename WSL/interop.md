---
title: Interopérabilité Windows avec Linux
description: Décrit l’interopérabilité de Windows avec les distributions Linux exécutées sur le sous-système Windows pour Linux.
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040818"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Sous-système Windows pour l’interopérabilité Linux avec Windows

> **Mise à jour de la mise à jour des créateurs de automne.**  
Si vous exécutez Creators Update ou une mise à jour anniversaire, passez à la [section créateurs/mise à jour anniversaire](interop.md#creators-update-and-anniversary-update).

Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.  Vous pouvez :

1. Appeler des fichiers binaires Windows à partir de la console Linux.
1. Appeler des binaires Linux à partir d’une console Windows.
1. **Windows Insiders builds 17063 +** Partager des variables d’environnement entre Linux et Windows.

Cela offre une expérience transparente entre Windows et WSL.  Les détails techniques se trouvent sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Exécuter les outils Linux à partir d’une ligne de commande Windows

Exécutez des fichiers binaires Linux à partir de l’invite de commandes Windows ( `wsl.exe <command>`cmd ou PowerShell) à l’aide de.

Les binaires sont appelés de cette façon:

1. Utilisez le même répertoire de travail que l’invite CMD ou PowerShell en cours.
1. Exécutez en tant qu’utilisateur par défaut WSL.
1. Avoir les mêmes droits d’administration Windows que le processus et le terminal appelant.

Exemple :

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

La commande Linux suivante `wsl.exe` est gérée comme n’importe quelle commande exécutée dans WSL.  Les éléments tels que sudo, le canalisation et la redirection de fichiers fonctionnent.

Exemple utilisant sudo:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

Exemples de mélange des commandes WSL et Windows:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

Les commandes passées `wsl.exe` à sont transmises au processus WSL sans modification.  Les chemins d’accès de fichiers doivent être spécifiés au format WSL.

Exemple avec chemins d’accès:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>Exécuter des outils Windows à partir de WSL

WSL peut appeler des binaires Windows directement à partir de la ligne `[binary name].exe`de commande WSL à l’aide de.  Par exemple, `notepad.exe`.  Pour faciliter l’exécution des fichiers exécutables Windows, le chemin d’accès Windows `$PATH` est inclus dans la mise à jour des créateurs de fichiers Linux dans automne.

Les applications exécutées de cette manière ont les propriétés suivantes:

1. Conservez le répertoire de travail en tant qu’invite de commandes WSL (pour la plupart, les exceptions sont expliquées ci-dessous).
1. Avoir les mêmes droits d’autorisation que le processus WSL.
1. Exécuter en tant qu’utilisateur Windows actif.
1. Apparaissent dans le gestionnaire des tâches de Windows comme s’ils étaient directement exécutés à partir de l’invite CMD.

Exemple :

``` BASH
$ notepad.exe
```

Les exécutables Windows exécutés dans WSL sont gérés de la même façon que les exécutables Linux natifs: la tuyauterie, les redirections et même le travail en arrière-plan, comme prévu.

Exemples utilisant des canaux:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

Exemple utilisant des commandes mixtes Windows et WSL:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Les fichiers binaires Windows doivent inclure l’extension de fichier, correspondre au cas du fichier et être exécutables.  Fichiers non exécutables, y compris les scripts batch.  Les commandes natives `dir` cmd comme peuvent être `cmd.exe /C` exécutées avec la commande.

Exemples :

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

Les paramètres sont passés au fichier binaire Windows non modifié.

Par exemple, les commandes suivantes s’ouvrent `C:\temp\foo.txt` dans `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

La modification des fichiers situés sur VolFs (fichiers non `/mnt/<x>`sous) avec une application Windows dans WSL n’est pas prise en charge.

Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actuel, mais il revient au répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.

Par exemple: est initialement lancée `C:\temp` à partir de et le répertoire WSL actuel est remplacé par le répertoire d’origine de l’utilisateur. `wsl.exe`  Lorsque `notepad.exe` est appelé à partir du répertoire de départ de l’utilisateur, WSL revient automatiquement `C:\temp` au répertoire de travail Notepad. exe:

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

> Disponible dans les versions 17063 et ultérieures de Windows Insider.

Avant le 17063, seule la variable d’environnement Windows à laquelle WSL `PATH` pouvait accéder était (par conséquent, vous pouviez lancer des exécutables Win32 à partir de sous WSL).

À partir de 17063, WSL et Windows `WSLENV`Share, il s’agit d’une variable d’environnement spéciale créée pour établir un pont entre Windows et Linux distributions s’exécutant sur WSL.

Propriétés de `WSLENV`:

* Il est partagé; Il existe dans les environnements Windows et WSL.
* Il s’agit d’une liste de variables d’environnement à partager entre Windows et WSL.
* Il peut mettre en forme les variables d’environnement pour fonctionner correctement dans Windows et WSL.

Quatre indicateurs sont disponibles dans `WSLENV` pour influencer la manière dont la variable d’environnement est traduite.

`WSLENV`père

* `/p`-convertit le chemin d’accès entre les chemins de style WSL/Linux et les chemins d’accès Win32.
* `/l`-indique que la variable d’environnement est une liste de chemins d’accès.
* `/u`-indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de WSL à partir de Win32.
* `/w`-indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de Win32 à partir de WSL.

Les indicateurs peuvent être combinés en fonction des besoins.

## <a name="disable-interop"></a>Désactiver l’interopérabilité

Les utilisateurs peuvent désactiver la possibilité d’exécuter des binaires Windows pour une seule session WSL en exécutant la commande suivante en tant que racine:

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Pour réactiver les fichiers binaires Windows, fermez toutes les sessions WSL et réexécutez bash. exe, ou exécutez la commande suivante en tant que racine:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La désactivation de l’interopérabilité n’est pas conservée entre les sessions WSL--l’interopérabilité sera réactivée lors du lancement d’une nouvelle session.

## <a name="creators-update-and-anniversary-update"></a>Creators Update et mise à jour anniversaire

Alors que la mise à jour des créateurs d’expérience d’interopérabilité est similaire à celle des expériences d’interopérabilité les plus récentes, il existe quelques différences majeures.

Pour résumer:

* `bash.exe`a été déconseillé et remplacé par `wsl.exe`.
* `-c`l’option permettant d’exécuter une seule commande n' `wsl.exe`est pas nécessaire avec.
* Le chemin d’accès Windows est inclus dans le WSL`$PATH`

Le processus de désactivation de l’interopérabilité n’est pas modifié.

### <a name="invoking-wsl-from-the-windows-command-line"></a>Appel de WSL à partir de la ligne de commande Windows

Les binaires Linux peuvent être appelés à partir de l’invite de commandes Windows ou de PowerShell.  Les binaires appelés de cette manière ont les propriétés suivantes:

1. Utilisez le même répertoire de travail que l’invite CMD ou PowerShell.
1. Exécutez en tant qu’utilisateur par défaut WSL.
1. Avoir les mêmes droits d’administration Windows que le processus et le terminal appelant.

Exemple :

```console
C:\temp> bash -c "ls -la"
```

Les commandes Linux appelées de cette façon sont gérées comme n’importe quelle autre application Windows.  Les opérations telles que l’entrée, la canalisation et la redirection de fichiers fonctionnent comme prévu.

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

Les commandes WSL transmises `bash -c` à sont transmises au processus WSL sans modification.  Les chemins d’accès aux fichiers doivent être spécifiés au format WSL et doivent être pris pour échapper les caractères appropriés. Exemple :

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>Appel des binaires Windows à partir de WSL

Le sous-système Windows pour Linux peut appeler des fichiers binaires Windows directement à partir de la ligne de commande WSL.  Les applications exécutées de cette manière ont les propriétés suivantes:

1. Conservez le répertoire de travail comme invite de commandes WSL, sauf dans le scénario décrit ci-dessous.
1. Avoir les mêmes droits d’autorisation que `bash.exe` le processus. 
1. Exécuter en tant qu’utilisateur Windows actif.
1. Apparaissent dans le gestionnaire des tâches de Windows comme s’ils étaient directement exécutés à partir de l’invite CMD.

Exemple :

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

Dans WSL, ces exécutables sont gérés de la même façon que les exécutables Linux natifs.  Cela signifie que l’ajout de répertoires au chemin Linux et la canalisation entre les commandes fonctionnent comme prévu.  Exemples :

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Le fichier binaire Windows doit inclure l’extension de fichier, correspondre au cas du fichier et être exécutable.  Les fichiers non exécutables, y compris les `dir` scripts batch et les `/mnt/c/Windows/System32/cmd.exe /C` commandes comme, peuvent être exécutés avec la commande.

Exemples :

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

Les paramètres sont passés au fichier binaire Windows non modifié.  

Par exemple, les commandes suivantes s’ouvrent `C:\temp\foo.txt` dans `notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

La modification des fichiers situés sur VolFs (fichiers non `/mnt/<x>`sous) avec une application Windows n’est pas prise en charge.  Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actuel, mais il repasse sur le répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.

Par exemple: est initialement lancée `C:\temp` à partir de et le répertoire WSL actuel est remplacé par le répertoire d’origine de l’utilisateur. `bash.exe`  Lorsque `notepad.exe` est appelé à partir du répertoire de départ de l’utilisateur, WSL revient automatiquement `C:\temp` au répertoire de travail Notepad. exe:

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
