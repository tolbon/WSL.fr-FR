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
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="e3e92-103">Interopérabilité du sous-système Windows pour Linux avec Windows</span><span class="sxs-lookup"><span data-stu-id="e3e92-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="e3e92-104">**Mise à jour pour Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="e3e92-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="e3e92-105">Si vous exécutez Mise à jour anniversaire ou Creators Update, passez à la [section Mise à jour anniversaire et Creators Update](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="e3e92-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="e3e92-106">Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="e3e92-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="e3e92-107">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="e3e92-107">You can:</span></span>

1. <span data-ttu-id="e3e92-108">Appeler des fichiers binaires Windows à partir de la console Linux.</span><span class="sxs-lookup"><span data-stu-id="e3e92-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="e3e92-109">Appeler des fichiers binaires Linux à partir d’une console Windows.</span><span class="sxs-lookup"><span data-stu-id="e3e92-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="e3e92-110">**Builds Windows Insiders 17063 et ultérieures** Partager des variables d’environnement entre Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="e3e92-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="e3e92-111">Vous obtenez ainsi une expérience fluide entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="e3e92-112">Vous trouverez les détails techniques sur le [blog WSL](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="e3e92-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="e3e92-113">Exécuter les outils Linux à partir d’une ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="e3e92-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="e3e92-114">Exécutez des fichiers binaires Linux à partir de l’invite de commandes Windows (CMD ou PowerShell) en utilisant `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="e3e92-115">Les fichiers binaires appelés de cette façon :</span><span class="sxs-lookup"><span data-stu-id="e3e92-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="e3e92-116">Utilisent le même répertoire de travail que l’invite CMD ou PowerShell en cours.</span><span class="sxs-lookup"><span data-stu-id="e3e92-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="e3e92-117">Sont exécutés en tant qu’utilisateur par défaut WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="e3e92-118">Ont les mêmes droits d’administration Windows que le terminal et le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="e3e92-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="e3e92-119">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e3e92-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="e3e92-120">La commande Linux qui suit `wsl.exe` est gérée comme n’importe quelle commande exécutée dans WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="e3e92-121">Des actions comme l’exécution de sudo, la création de canaux et la redirection de fichiers fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="e3e92-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="e3e92-122">Exemple d’utilisation de sudo :</span><span class="sxs-lookup"><span data-stu-id="e3e92-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="e3e92-123">Exemples de combinaison de commandes WSL et Windows :</span><span class="sxs-lookup"><span data-stu-id="e3e92-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="e3e92-124">Les commandes passées à `wsl.exe` sont transmises au processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="e3e92-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="e3e92-125">Les chemins de fichiers doivent être spécifiés au format WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="e3e92-126">Exemple avec chemins :</span><span class="sxs-lookup"><span data-stu-id="e3e92-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="e3e92-127">Exécuter des outils Windows à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="e3e92-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="e3e92-128">WSL peut appeler des fichiers binaires Windows directement à partir de la ligne de commande WSL à l’aide de `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="e3e92-129">Exemple : `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="e3e92-130">Pour faciliter l’exécution des exécutables Windows, le chemin Windows est inclus dans la variable Linux `$PATH` dans Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="e3e92-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="e3e92-131">Les applications exécutées de cette manière ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3e92-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="e3e92-132">Conservent le répertoire de travail en tant qu’invite de commandes WSL (en général, les exceptions sont décrites ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="e3e92-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="e3e92-133">Ont les mêmes autorisations que le processus WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="e3e92-134">Sont exécutées en tant qu’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="e3e92-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="e3e92-135">Apparaissent dans le Gestionnaire des tâches de Windows comme si elles étaient directement exécutées à partir de l’invite CMD.</span><span class="sxs-lookup"><span data-stu-id="e3e92-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="e3e92-136">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e3e92-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="e3e92-137">Les exécutables Windows exécutés dans WSL sont gérés de la même façon que les exécutables Linux natifs : la création de canaux, les redirections et même le travail en arrière-plan fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e3e92-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="e3e92-138">Exemples d’utilisation de canaux :</span><span class="sxs-lookup"><span data-stu-id="e3e92-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="e3e92-139">Exemple d’utilisation de commandes Windows et WSL mixtes :</span><span class="sxs-lookup"><span data-stu-id="e3e92-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="e3e92-140">Les fichiers binaires Windows doivent inclure l’extension de fichier, correspondre à la casse de fichier et être exécutables.</span><span class="sxs-lookup"><span data-stu-id="e3e92-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="e3e92-141">Les fichiers non exécutables, dont les scripts de commandes et</span><span class="sxs-lookup"><span data-stu-id="e3e92-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="e3e92-142">les commandes natives CMD comme `dir`, peuvent être exécutés avec la commande `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="e3e92-143">Exemples :</span><span class="sxs-lookup"><span data-stu-id="e3e92-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="e3e92-144">Les paramètres sont passés au fichier binaire Windows non modifié.</span><span class="sxs-lookup"><span data-stu-id="e3e92-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="e3e92-145">Par exemple, les commandes suivantes ouvrent `C:\temp\foo.txt` dans `notepad.exe` :</span><span class="sxs-lookup"><span data-stu-id="e3e92-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="e3e92-146">La modification de fichiers situés sur VolFs (fichiers qui ne se trouvent pas sous `/mnt/<x>`) avec une application Windows dans WSL n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e3e92-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="e3e92-147">Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actif, mais a recours au répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.</span><span class="sxs-lookup"><span data-stu-id="e3e92-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="e3e92-148">Par exemple, `wsl.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est remplacé par le répertoire racine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3e92-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="e3e92-149">Quand `notepad.exe` est appelé à partir du répertoire racine de l’utilisateur, WSL rétablit automatiquement `C:\temp` comme répertoire de travail de notepad.exe :</span><span class="sxs-lookup"><span data-stu-id="e3e92-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="e3e92-150">Partager des variables d’environnement entre Windows et WSL</span><span class="sxs-lookup"><span data-stu-id="e3e92-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="e3e92-151">Disponible dans les builds Windows Insiders 17063 et ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e3e92-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="e3e92-152">Avant la build 17063, la seule variable d’environnement Windows à laquelle WSL pouvait accéder était `PATH` (par conséquent, vous pouviez lancer des exécutables Win32 sous WSL).</span><span class="sxs-lookup"><span data-stu-id="e3e92-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="e3e92-153">À partir de la build 17063, WSL et Windows partagent `WSLENV`, une variable d’environnement spéciale créée pour relier les distributions Windows et Linux s’exécutant sur WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="e3e92-154">Propriétés de la variable `WSLENV` :</span><span class="sxs-lookup"><span data-stu-id="e3e92-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="e3e92-155">Elle est partagée et existe dans les environnements Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="e3e92-156">Il s’agit d’une liste de variables d’environnement à partager entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="e3e92-157">Elle peut mettre en forme des variables d’environnement pour fonctionner correctement dans Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="e3e92-158">Quatre indicateurs sont disponibles dans `WSLENV` pour influencer la manière dont cette variable d’environnement est traduite.</span><span class="sxs-lookup"><span data-stu-id="e3e92-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="e3e92-159">Indicateurs `WSLENV` :</span><span class="sxs-lookup"><span data-stu-id="e3e92-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="e3e92-160">`/p` : convertit le chemin entre les chemins de style WSL/Linux et les chemins Win32.</span><span class="sxs-lookup"><span data-stu-id="e3e92-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="e3e92-161">`/l` : indique que la variable d’environnement est une liste de chemins.</span><span class="sxs-lookup"><span data-stu-id="e3e92-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="e3e92-162">`/u` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de WSL à partir de Win32.</span><span class="sxs-lookup"><span data-stu-id="e3e92-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="e3e92-163">`/w` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="e3e92-164">Les indicateurs peuvent être combinés en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="e3e92-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="e3e92-165">Désactiver l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="e3e92-165">Disable Interop</span></span>

<span data-ttu-id="e3e92-166">Les utilisateurs peuvent désactiver la possibilité d’exécuter des fichiers binaires Windows pour une seule session WSL en exécutant la commande suivante en tant que racine :</span><span class="sxs-lookup"><span data-stu-id="e3e92-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="e3e92-167">Pour réactiver les fichiers binaires Windows, fermez toutes les sessions WSL et réexécutez bash.exe, ou exécutez la commande suivante en tant que racine :</span><span class="sxs-lookup"><span data-stu-id="e3e92-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="e3e92-168">La désactivation de l’interopérabilité n’est pas conservée entre les sessions WSL : l’interopérabilité sera réactivée lors du lancement d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="e3e92-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="e3e92-169">Mise à jour anniversaire et Creators Update</span><span class="sxs-lookup"><span data-stu-id="e3e92-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="e3e92-170">Alors que l’expérience d’interopérabilité avant Fall Creators Update est similaire à des expériences d’interopérabilité plus récentes, il existe quelques différences majeures.</span><span class="sxs-lookup"><span data-stu-id="e3e92-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="e3e92-171">Pour résumer :</span><span class="sxs-lookup"><span data-stu-id="e3e92-171">To summarize:</span></span>

* <span data-ttu-id="e3e92-172">`bash.exe` a été déprécié et remplacé par `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="e3e92-173">L’option `-c` permettant d’exécuter une seule commande n’est pas nécessaire avec `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="e3e92-174">Le chemin Windows est inclus dans la variable WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="e3e92-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="e3e92-175">Le processus de désactivation de l’interopérabilité est inchangé.</span><span class="sxs-lookup"><span data-stu-id="e3e92-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="e3e92-176">Appel de WSL à partir de la ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="e3e92-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="e3e92-177">Les fichiers binaires Linux peuvent être appelés à partir de l’invite de commandes Windows ou de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3e92-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="e3e92-178">Les fichiers binaires appelés de cette manière ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3e92-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="e3e92-179">Utilisent le même répertoire de travail que l’invite CMD ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e3e92-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="e3e92-180">Sont exécutés en tant qu’utilisateur par défaut WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="e3e92-181">Ont les mêmes droits d’administration Windows que le terminal et le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="e3e92-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="e3e92-182">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e3e92-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="e3e92-183">Les commandes Linux appelées de cette façon sont gérées comme n’importe quelle autre application Windows.</span><span class="sxs-lookup"><span data-stu-id="e3e92-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="e3e92-184">Des actions comme les entrées, la création de canaux et la redirection de fichiers fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e3e92-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="e3e92-185">Exemples :</span><span class="sxs-lookup"><span data-stu-id="e3e92-185">Examples:</span></span>

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

<span data-ttu-id="e3e92-186">Les commandes WSL passées à `bash -c` sont transmises au processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="e3e92-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="e3e92-187">Les chemins de fichiers doivent être spécifiés au format WSL et des précautions doivent être prises pour placer les caractères appropriés dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="e3e92-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="e3e92-188">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e3e92-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="e3e92-189">Appel des fichiers binaires Windows à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="e3e92-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="e3e92-190">Le sous-système Windows pour Linux peut appeler des fichiers binaires Windows directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="e3e92-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="e3e92-191">Les applications exécutées de cette manière ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="e3e92-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="e3e92-192">Conservent le répertoire de travail en tant qu’invite de commandes WSL, sauf dans le scénario décrit ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e3e92-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="e3e92-193">Ont les mêmes autorisations que le processus `bash.exe`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="e3e92-194">Sont exécutées en tant qu’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="e3e92-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="e3e92-195">Apparaissent dans le Gestionnaire des tâches de Windows comme si elles étaient directement exécutées à partir de l’invite CMD.</span><span class="sxs-lookup"><span data-stu-id="e3e92-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="e3e92-196">Exemple :</span><span class="sxs-lookup"><span data-stu-id="e3e92-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="e3e92-197">Dans WSL, ces exécutables sont gérés de la même façon que les exécutables Linux natifs.</span><span class="sxs-lookup"><span data-stu-id="e3e92-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="e3e92-198">Cela signifie que l’ajout de répertoires au chemin Linux et la création de canaux entre les commandes fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="e3e92-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="e3e92-199">Exemples :</span><span class="sxs-lookup"><span data-stu-id="e3e92-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="e3e92-200">Le fichier binaire Windows doit inclure l’extension de fichier, correspondre à la casse de fichier et être exécutable.</span><span class="sxs-lookup"><span data-stu-id="e3e92-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="e3e92-201">Les fichiers non exécutables, dont les scripts de commandes et une commande comme `dir`, peuvent être exécutés avec la commande `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="e3e92-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="e3e92-202">Exemples :</span><span class="sxs-lookup"><span data-stu-id="e3e92-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="e3e92-203">Les paramètres sont passés au fichier binaire Windows non modifié.</span><span class="sxs-lookup"><span data-stu-id="e3e92-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="e3e92-204">Par exemple, les commandes suivantes ouvrent `C:\temp\foo.txt` dans `notepad.exe` :</span><span class="sxs-lookup"><span data-stu-id="e3e92-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="e3e92-205">La modification de fichiers situés sur VolFs (fichiers qui ne se trouvent pas sous `/mnt/<x>`) avec une application Windows n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e3e92-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="e3e92-206">Par défaut, WSL tente de conserver le répertoire de travail du fichier binaire Windows en tant que répertoire WSL actif, mais a recours au répertoire de création de l’instance si le répertoire de travail se trouve sur VolFs.</span><span class="sxs-lookup"><span data-stu-id="e3e92-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="e3e92-207">Par exemple, `bash.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est remplacé par le répertoire racine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e3e92-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="e3e92-208">Quand `notepad.exe` est appelé à partir du répertoire racine de l’utilisateur, WSL rétablit automatiquement `C:\temp` comme répertoire de travail de notepad.exe :</span><span class="sxs-lookup"><span data-stu-id="e3e92-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
