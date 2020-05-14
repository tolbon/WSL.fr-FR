---
title: Interopérabilité Windows avec Linux
description: Décrit l’interopérabilité Windows avec les distributions Linux exécutées sur le sous-système Windows pour Linux.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: b1c7a64a86cf088159d1abee3b341328151428f6
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270843"
---
# <a name="windows-interoperability-with-linux"></a>Interopérabilité Windows avec Linux

Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.  Vous pouvez :

* Exécuter les outils Windows (p. ex. notepad.exe) à partir d’une ligne de commande Linux (p. ex. Ubuntu).
* Exécuter les outils Linux (p. ex. grep) à partir d’une ligne de commande Windows (p. ex. PowerShell).
* Partager des variables d’environnement entre Linux et Windows. (Build 17063+)

> [!NOTE]
> Si vous exécutez une version Creators Update (octobre 2017, build 16299) ou la mise à jour anniversaire (août 2016, build 14393), accédez aux [versions antérieures de Windows 10](#earlier-versions-of-windows-10).

## <a name="run-linux-tools-from-a-windows-command-line"></a>Exécuter les outils Linux à partir d’une ligne de commande Windows

Exécutez des fichiers binaires Linux à partir de l’invite de commandes Windows (CMD) ou de PowerShell en utilisant `wsl <command>` (ou `wsl.exe <command>`).

Par exemple :

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Les fichiers binaires appelés de cette façon :

* Utilisent le même répertoire de travail que l’invite CMD ou PowerShell en cours.
* Sont exécutés en tant qu’utilisateur par défaut WSL.
* Ont les mêmes droits d’administration Windows que le terminal et le processus appelant.

La commande Linux qui suit `wsl` (ou `wsl.exe`) est gérée comme n’importe quelle commande exécutée dans WSL.  Des actions comme l’exécution de sudo, la création de canaux et la redirection de fichiers fonctionnent.

Exemple utilisant sudo pour mettre à jour votre distribution Linux par défaut :

```powershell
C:\temp> wsl sudo apt-get update
```

Votre nom d’utilisateur de distribution Linux par défaut sera listé après l’exécution de cette commande et vous serez invité à entrer votre mot de passe. Une fois que vous avez entré correctement votre mot de passe, votre distribution télécharge les mises à jour.

## <a name="mixing-linux-and-windows-commands"></a>Combinaison de commandes Linux et Windows

Voici quelques exemples de combinaison de commandes Linux et Windows à l’aide de PowerShell.

Pour utiliser la commande Linux `ls -la` pour lister les fichiers et la commande PowerShell `findstr` pour filtrer les résultats avec des mots contenant « git », combinez les commandes suivantes :

```powershell
wsl ls -la | findstr "git"
```

Pour utiliser la commande PowerShell `dir` pour lister les fichiers et la commande Linux `grep` pour filtrer les résultats avec des mots contenant « git », combinez les commandes suivantes :

```powershell
C:\temp> dir | wsl grep git
```

Pour utiliser la commande Linux `ls -la` pour lister les fichiers et la commande PowerShell `> out.txt` pour imprimer cette liste dans un fichier texte nommé « out.txt », combinez les commandes suivantes :

```powershell
C:\temp> wsl ls -la > out.txt
```

Les commandes passées à `wsl.exe` sont transmises au processus WSL sans modification.  Les chemins de fichiers doivent être spécifiés au format WSL.

Pour utiliser la commande Linux `ls -la` pour lister les fichiers dans le chemin du système de fichiers Linux `/proc/cpuinfo`, à l’aide de PowerShell :

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

Pour utiliser la commande Linux `ls -la` pour lister les fichiers dans le chemin du système de fichiers Windows `C:\Program Files`, à l’aide de PowerShell :

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a>Exécuter des outils Windows à partir de Linux

WSL peut exécuter des outils Windows directement à partir de la ligne de commande WSL à l’aide de `[tool-name].exe`.  Par exemple, `notepad.exe`.

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

Les applications exécutées de cette manière ont les propriétés suivantes :

* Conservent le répertoire de travail en tant qu’invite de commandes WSL (en général, les exceptions sont décrites ci-dessous).
* Ont les mêmes autorisations que le processus WSL.
* Sont exécutées en tant qu’utilisateur Windows actif.
* Apparaissent dans le Gestionnaire des tâches de Windows comme si elles étaient directement exécutées à partir de l’invite CMD.

Les exécutables Windows exécutés dans WSL sont gérés de la même façon que les exécutables Linux natifs : la création de canaux, les redirections et même le travail en arrière-plan fonctionnent comme prévu.

Pour exécuter l’outil Windows `ipconfig.exe`, utiliser l’outil Linux `grep` afin de filtrer les résultats « IPv4 », et utiliser l’outil Linux `cut` afin de supprimer les champs de colonne, à partir d’une distribution Linux (par exemple, Ubuntu), entrez :

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Essayons un exemple combinant des commandes Windows et Linux. Ouvrez votre distribution Linux (p. ex. Ubuntu) et créez un fichier texte : `touch foo.txt`. À présent, utilisez la commande Linux `ls -la` pour lister les fichiers directs et les détails de leur création, ainsi que l’outil Windows PowerShell `findstr.exe` pour filtrer les résultats afin que seul votre fichier `foo.txt` s’affiche dans les résultats :

```bash
ls -la | findstr.exe foo.txt
```

Les outils Windows doivent inclure l’extension de fichier, correspondre à la casse de fichier et être exécutables.  Les fichiers non exécutables, dont les scripts de commandes et  les commandes natives CMD comme `dir`, peuvent être exécutés avec la commande `cmd.exe /C`.

Par exemple, listez le contenu du répertoire C:\ de votre système de fichiers Windows, en entrant :

```bash
cmd.exe /C dir
```

Ou utilisez la commande `ping` pour envoyer une demande d’écho au site web microsoft.com :

```bash
ping.exe www.microsoft.com
```

Les paramètres sont passés au fichier binaire Windows non modifié. Par exemple, la commande suivante ouvre `C:\temp\foo.txt` dans `notepad.exe` :

```bash
notepad.exe "C:\temp\foo.txt"
```

Cela fonctionne également :

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Partager des variables d’environnement entre Windows et WSL

WSL et Windows partagent une variable d’environnement spéciale, `WSLENV`, créée pour relier les distributions Windows et Linux s’exécutant sur WSL.

Propriétés de la variable `WSLENV` :

* Elle est partagée et existe dans les environnements Windows et WSL.
* Il s’agit d’une liste de variables d’environnement à partager entre Windows et WSL.
* Elle peut mettre en forme des variables d’environnement pour fonctionner correctement dans Windows et WSL.

> [!NOTE]
> Avant la build 17063, la seule variable d’environnement Windows à laquelle WSL pouvait accéder était `PATH` (par conséquent, vous pouviez lancer des exécutables Win32 sous WSL). Avec la build 17063, `WSLENV` commence à être pris en charge.

## <a name="wslenv-flags"></a>Indicateurs WSLENV

Quatre indicateurs sont disponibles dans `WSLENV` pour influencer la manière dont cette variable d’environnement est traduite.

Indicateurs `WSLENV` :

* `/p` : convertit le chemin entre les chemins de style WSL/Linux et les chemins Win32.
* `/l` : indique que la variable d’environnement est une liste de chemins.
* `/u` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de WSL à partir de Win32.
* `/w` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de Win32 à partir de WSL.

Les indicateurs peuvent être combinés en fonction des besoins.

## <a name="disable-interoperability"></a>Désactiver l’interopérabilité

Les utilisateurs peuvent désactiver la possibilité d’exécuter des outils Windows pour une session WSL individuelle en exécutant la commande suivante en tant que racine :

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Pour réactiver les fichiers binaires Windows, fermez toutes les sessions WSL et réexécutez bash.exe, ou exécutez la commande suivante en tant que racine :

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

La désactivation de l’interopérabilité n’est pas conservée entre les sessions WSL : l’interopérabilité sera réactivée lors du lancement d’une nouvelle session.

## <a name="earlier-versions-of-windows-10"></a>Versions antérieures de Windows 10

Il existe plusieurs différences pour les commandes d’interopérabilité sur les versions antérieures de Windows 10. Si vous exécutez une version Creators Update (octobre 2017, build 16299) ou la mise à jour anniversaire (août 2016, build 14393) de Windows 10, nous vous recommandons d’effectuer une [mise à jour vers la dernière version de Windows](ms-settings:windowsupdate). Toutefois, si cela n’est pas possible, nous décrivons certaines différences d’interopérabilité ci-dessous.

Résumé :

* `bash.exe` a été remplacé par `wsl.exe`.
* L’option `-c` permettant d’exécuter une seule commande n’est pas nécessaire avec `wsl.exe`.
* Le chemin Windows est inclus dans la variable WSL `$PATH`.
* Le processus de désactivation de l’interopérabilité est inchangé.

Les commandes Linux peuvent être exécutées à partir de l’invite de commandes Windows ou de PowerShell, mais pour les versions antérieures de Windows, vous pouvez être amené à utiliser la commande `bash`. Par exemple :

```powershell
C:\temp> bash -c "ls -la"
```

Des actions comme les entrées, la création de canaux et la redirection de fichiers fonctionnent comme prévu.

Les commandes WSL passées à `bash -c` sont transmises au processus WSL sans modification.  Les chemins de fichiers doivent être spécifiés au format WSL et des précautions doivent être prises pour placer les caractères appropriés dans une séquence d’échappement. Exemple :

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

Ou ...

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

Lorsque vous appelez un outil Windows à partir d’une distribution WSL dans une version antérieure de Windows 10, vous devez spécifier le chemin du répertoire. Par exemple, à partir de votre ligne de commande WSL, entrez :

```bash
/mnt/c/Windows/System32/notepad.exe
```

Dans WSL, ces exécutables sont gérés de la même façon que les exécutables Linux natifs.  Cela signifie que l’ajout de répertoires au chemin Linux et la création de canaux entre les commandes fonctionnent comme prévu.  Par exemple :

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
Ou

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Le fichier binaire Windows doit inclure l’extension de fichier, correspondre à la casse de fichier et être exécutable.  Les fichiers non exécutables, dont les scripts de commandes et une commande comme `dir`, peuvent être exécutés avec la commande `/mnt/c/Windows/System32/cmd.exe /C`. Par exemple :

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a>Ressources supplémentaires

* [Billet de blog WSL de 2016 sur l’interopérabilité](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
