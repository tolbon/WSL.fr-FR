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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="33220-103">Sous-système Windows pour l’interopérabilité Linux avec Windows</span><span class="sxs-lookup"><span data-stu-id="33220-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="33220-104">**Mise à jour de la mise à jour des créateurs de automne.**</span><span class="sxs-lookup"><span data-stu-id="33220-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="33220-105">Si vous exécutez Creators Update ou une mise à jour anniversaire, passez à la [section créateurs/mise à jour anniversaire](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="33220-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="33220-106">Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="33220-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="33220-107">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="33220-107">You can:</span></span>

1. <span data-ttu-id="33220-108">Appeler des fichiers binaires Windows à partir de la console Linux.</span><span class="sxs-lookup"><span data-stu-id="33220-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="33220-109">Appeler des binaires Linux à partir d’une console Windows.</span><span class="sxs-lookup"><span data-stu-id="33220-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="33220-110">**Windows Insiders builds 17063 +** Partager des variables d’environnement entre Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="33220-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="33220-111">Cela offre une expérience transparente entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="33220-112">Les détails techniques se trouvent sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="33220-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="33220-113">Exécuter les outils Linux à partir d’une ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="33220-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="33220-114">Exécutez des fichiers binaires Linux à partir de l’invite de commandes Windows ( `wsl.exe <command>`cmd ou PowerShell) à l’aide de.</span><span class="sxs-lookup"><span data-stu-id="33220-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="33220-115">Les binaires sont appelés de cette façon:</span><span class="sxs-lookup"><span data-stu-id="33220-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="33220-116">Utilisez le même répertoire de travail que l’invite CMD ou PowerShell en cours.</span><span class="sxs-lookup"><span data-stu-id="33220-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="33220-117">Exécutez en tant qu’utilisateur par défaut WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="33220-118">Avoir les mêmes droits d’administration Windows que le processus et le terminal appelant.</span><span class="sxs-lookup"><span data-stu-id="33220-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="33220-119">Exemple :</span><span class="sxs-lookup"><span data-stu-id="33220-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="33220-120">La commande Linux suivante `wsl.exe` est gérée comme n’importe quelle commande exécutée dans WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="33220-121">Les éléments tels que sudo, le canalisation et la redirection de fichiers fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="33220-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="33220-122">Exemple utilisant sudo:</span><span class="sxs-lookup"><span data-stu-id="33220-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="33220-123">Exemples de mélange des commandes WSL et Windows:</span><span class="sxs-lookup"><span data-stu-id="33220-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="33220-124">Les commandes passées `wsl.exe` à sont transmises au processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="33220-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="33220-125">Les chemins d’accès de fichiers doivent être spécifiés au format WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="33220-126">Exemple avec chemins d’accès:</span><span class="sxs-lookup"><span data-stu-id="33220-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="33220-127">Exécuter des outils Windows à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="33220-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="33220-128">WSL peut appeler des binaires Windows directement à partir de la ligne `[binary name].exe`de commande WSL à l’aide de.</span><span class="sxs-lookup"><span data-stu-id="33220-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="33220-129">Par exemple, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="33220-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="33220-130">Pour faciliter l’exécution des fichiers exécutables Windows, le chemin d’accès Windows `$PATH` est inclus dans la mise à jour des créateurs de fichiers Linux dans automne.</span><span class="sxs-lookup"><span data-stu-id="33220-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="33220-131">Les applications exécutées de cette manière ont les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="33220-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="33220-132">Conservez le répertoire de travail en tant qu’invite de commandes WSL (pour la plupart, les exceptions sont expliquées ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="33220-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="33220-133">Avoir les mêmes droits d’autorisation que le processus WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="33220-134">Exécuter en tant qu’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="33220-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="33220-135">Apparaissent dans le gestionnaire des tâches de Windows comme s’ils étaient directement exécutés à partir de l’invite CMD.</span><span class="sxs-lookup"><span data-stu-id="33220-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="33220-136">Exemple :</span><span class="sxs-lookup"><span data-stu-id="33220-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="33220-137">Les exécutables Windows exécutés dans WSL sont gérés de la même façon que les exécutables Linux natifs: la tuyauterie, les redirections et même le travail en arrière-plan, comme prévu.</span><span class="sxs-lookup"><span data-stu-id="33220-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="33220-138">Exemples utilisant des canaux:</span><span class="sxs-lookup"><span data-stu-id="33220-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="33220-139">Exemple utilisant des commandes mixtes Windows et WSL:</span><span class="sxs-lookup"><span data-stu-id="33220-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="33220-140">Les fichiers binaires Windows doivent inclure l’extension de fichier, correspondre au cas du fichier et être exécutables.</span><span class="sxs-lookup"><span data-stu-id="33220-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="33220-141">Fichiers non exécutables, y compris les scripts batch.</span><span class="sxs-lookup"><span data-stu-id="33220-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="33220-142">Les commandes natives `dir` cmd comme peuvent être `cmd.exe /C` exécutées avec la commande.</span><span class="sxs-lookup"><span data-stu-id="33220-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="33220-143">Exemples :</span><span class="sxs-lookup"><span data-stu-id="33220-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="33220-144">Les paramètres sont passés au fichier binaire Windows non modifié.</span><span class="sxs-lookup"><span data-stu-id="33220-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="33220-145">Par exemple, les commandes suivantes s’ouvrent `C:\temp\foo.txt` dans `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="33220-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="33220-146">La modification des fichiers situés sur VolFs (fichiers non `/mnt/<x>`sous) avec une application Windows dans WSL n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="33220-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="33220-147">Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actuel, mais il revient au répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.</span><span class="sxs-lookup"><span data-stu-id="33220-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="33220-148">Par exemple: est initialement lancée `C:\temp` à partir de et le répertoire WSL actuel est remplacé par le répertoire d’origine de l’utilisateur. `wsl.exe`</span><span class="sxs-lookup"><span data-stu-id="33220-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="33220-149">Lorsque `notepad.exe` est appelé à partir du répertoire de départ de l’utilisateur, WSL revient automatiquement `C:\temp` au répertoire de travail Notepad. exe:</span><span class="sxs-lookup"><span data-stu-id="33220-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="33220-150">Partager des variables d’environnement entre Windows et WSL</span><span class="sxs-lookup"><span data-stu-id="33220-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="33220-151">Disponible dans les versions 17063 et ultérieures de Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="33220-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="33220-152">Avant le 17063, seule la variable d’environnement Windows à laquelle WSL `PATH` pouvait accéder était (par conséquent, vous pouviez lancer des exécutables Win32 à partir de sous WSL).</span><span class="sxs-lookup"><span data-stu-id="33220-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="33220-153">À partir de 17063, WSL et Windows `WSLENV`Share, il s’agit d’une variable d’environnement spéciale créée pour établir un pont entre Windows et Linux distributions s’exécutant sur WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="33220-154">Propriétés de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="33220-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="33220-155">Il est partagé; Il existe dans les environnements Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="33220-156">Il s’agit d’une liste de variables d’environnement à partager entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="33220-157">Il peut mettre en forme les variables d’environnement pour fonctionner correctement dans Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="33220-158">Quatre indicateurs sont disponibles dans `WSLENV` pour influencer la manière dont la variable d’environnement est traduite.</span><span class="sxs-lookup"><span data-stu-id="33220-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="33220-159">`WSLENV`père</span><span class="sxs-lookup"><span data-stu-id="33220-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="33220-160">`/p`-convertit le chemin d’accès entre les chemins de style WSL/Linux et les chemins d’accès Win32.</span><span class="sxs-lookup"><span data-stu-id="33220-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="33220-161">`/l`-indique que la variable d’environnement est une liste de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="33220-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="33220-162">`/u`-indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de WSL à partir de Win32.</span><span class="sxs-lookup"><span data-stu-id="33220-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="33220-163">`/w`-indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="33220-164">Les indicateurs peuvent être combinés en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="33220-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="33220-165">Désactiver l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="33220-165">Disable Interop</span></span>

<span data-ttu-id="33220-166">Les utilisateurs peuvent désactiver la possibilité d’exécuter des binaires Windows pour une seule session WSL en exécutant la commande suivante en tant que racine:</span><span class="sxs-lookup"><span data-stu-id="33220-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="33220-167">Pour réactiver les fichiers binaires Windows, fermez toutes les sessions WSL et réexécutez bash. exe, ou exécutez la commande suivante en tant que racine:</span><span class="sxs-lookup"><span data-stu-id="33220-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="33220-168">La désactivation de l’interopérabilité n’est pas conservée entre les sessions WSL--l’interopérabilité sera réactivée lors du lancement d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="33220-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="33220-169">Creators Update et mise à jour anniversaire</span><span class="sxs-lookup"><span data-stu-id="33220-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="33220-170">Alors que la mise à jour des créateurs d’expérience d’interopérabilité est similaire à celle des expériences d’interopérabilité les plus récentes, il existe quelques différences majeures.</span><span class="sxs-lookup"><span data-stu-id="33220-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="33220-171">Pour résumer:</span><span class="sxs-lookup"><span data-stu-id="33220-171">To summarize:</span></span>

* <span data-ttu-id="33220-172">`bash.exe`a été déconseillé et remplacé par `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="33220-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="33220-173">`-c`l’option permettant d’exécuter une seule commande n' `wsl.exe`est pas nécessaire avec.</span><span class="sxs-lookup"><span data-stu-id="33220-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="33220-174">Le chemin d’accès Windows est inclus dans le WSL`$PATH`</span><span class="sxs-lookup"><span data-stu-id="33220-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="33220-175">Le processus de désactivation de l’interopérabilité n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="33220-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="33220-176">Appel de WSL à partir de la ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="33220-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="33220-177">Les binaires Linux peuvent être appelés à partir de l’invite de commandes Windows ou de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33220-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="33220-178">Les binaires appelés de cette manière ont les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="33220-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="33220-179">Utilisez le même répertoire de travail que l’invite CMD ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="33220-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="33220-180">Exécutez en tant qu’utilisateur par défaut WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="33220-181">Avoir les mêmes droits d’administration Windows que le processus et le terminal appelant.</span><span class="sxs-lookup"><span data-stu-id="33220-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="33220-182">Exemple :</span><span class="sxs-lookup"><span data-stu-id="33220-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="33220-183">Les commandes Linux appelées de cette façon sont gérées comme n’importe quelle autre application Windows.</span><span class="sxs-lookup"><span data-stu-id="33220-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="33220-184">Les opérations telles que l’entrée, la canalisation et la redirection de fichiers fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="33220-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="33220-185">Exemples :</span><span class="sxs-lookup"><span data-stu-id="33220-185">Examples:</span></span>

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

<span data-ttu-id="33220-186">Les commandes WSL transmises `bash -c` à sont transmises au processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="33220-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="33220-187">Les chemins d’accès aux fichiers doivent être spécifiés au format WSL et doivent être pris pour échapper les caractères appropriés.</span><span class="sxs-lookup"><span data-stu-id="33220-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="33220-188">Exemple :</span><span class="sxs-lookup"><span data-stu-id="33220-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="33220-189">Appel des binaires Windows à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="33220-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="33220-190">Le sous-système Windows pour Linux peut appeler des fichiers binaires Windows directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="33220-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="33220-191">Les applications exécutées de cette manière ont les propriétés suivantes:</span><span class="sxs-lookup"><span data-stu-id="33220-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="33220-192">Conservez le répertoire de travail comme invite de commandes WSL, sauf dans le scénario décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="33220-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="33220-193">Avoir les mêmes droits d’autorisation que `bash.exe` le processus.</span><span class="sxs-lookup"><span data-stu-id="33220-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="33220-194">Exécuter en tant qu’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="33220-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="33220-195">Apparaissent dans le gestionnaire des tâches de Windows comme s’ils étaient directement exécutés à partir de l’invite CMD.</span><span class="sxs-lookup"><span data-stu-id="33220-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="33220-196">Exemple :</span><span class="sxs-lookup"><span data-stu-id="33220-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="33220-197">Dans WSL, ces exécutables sont gérés de la même façon que les exécutables Linux natifs.</span><span class="sxs-lookup"><span data-stu-id="33220-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="33220-198">Cela signifie que l’ajout de répertoires au chemin Linux et la canalisation entre les commandes fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="33220-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="33220-199">Exemples :</span><span class="sxs-lookup"><span data-stu-id="33220-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="33220-200">Le fichier binaire Windows doit inclure l’extension de fichier, correspondre au cas du fichier et être exécutable.</span><span class="sxs-lookup"><span data-stu-id="33220-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="33220-201">Les fichiers non exécutables, y compris les `dir` scripts batch et les `/mnt/c/Windows/System32/cmd.exe /C` commandes comme, peuvent être exécutés avec la commande.</span><span class="sxs-lookup"><span data-stu-id="33220-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="33220-202">Exemples :</span><span class="sxs-lookup"><span data-stu-id="33220-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="33220-203">Les paramètres sont passés au fichier binaire Windows non modifié.</span><span class="sxs-lookup"><span data-stu-id="33220-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="33220-204">Par exemple, les commandes suivantes s’ouvrent `C:\temp\foo.txt` dans `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="33220-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="33220-205">La modification des fichiers situés sur VolFs (fichiers non `/mnt/<x>`sous) avec une application Windows n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="33220-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="33220-206">Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actuel, mais il repasse sur le répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.</span><span class="sxs-lookup"><span data-stu-id="33220-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="33220-207">Par exemple: est initialement lancée `C:\temp` à partir de et le répertoire WSL actuel est remplacé par le répertoire d’origine de l’utilisateur. `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="33220-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="33220-208">Lorsque `notepad.exe` est appelé à partir du répertoire de départ de l’utilisateur, WSL revient automatiquement `C:\temp` au répertoire de travail Notepad. exe:</span><span class="sxs-lookup"><span data-stu-id="33220-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
