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
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063247"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="3d8ff-103">Sous-système Windows pour l’interopérabilité Linux avec Windows</span><span class="sxs-lookup"><span data-stu-id="3d8ff-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="3d8ff-104">**Mise à jour pour Fall Creators Update.**</span><span class="sxs-lookup"><span data-stu-id="3d8ff-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="3d8ff-105">Si vous exécutez Creators Update ou mise à jour anniversaire, passez directement à la [section de mise à jour Creators/anniversaire](interop.md#creators-update-and-anniversary-update).</span><span class="sxs-lookup"><span data-stu-id="3d8ff-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="3d8ff-106">Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="3d8ff-107">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-107">You can:</span></span>

1. <span data-ttu-id="3d8ff-108">Appeler les fichiers binaires Windows à partir de la console Linux.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="3d8ff-109">Appeler les fichiers binaires de Linux à partir d’une console Windows.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="3d8ff-110">**Les Builds Windows Insiders 17063 +** partagent des variables d’environnement entre Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="3d8ff-111">Cela offre une expérience transparente entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="3d8ff-112">Détails techniques sont sur le [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span><span class="sxs-lookup"><span data-stu-id="3d8ff-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="3d8ff-113">Exécuter des outils Linux à partir d’une ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="3d8ff-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="3d8ff-114">Exécuter des fichiers binaires de Linux à partir de l’invite de commandes Windows (CMD ou PowerShell) à l’aide `wsl.exe <command>`.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="3d8ff-115">Fichiers binaires de l’appelé de cette façon :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="3d8ff-116">Utiliser le même répertoire de travail en tant que l’invite CMD ou PowerShell actuel.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="3d8ff-117">Exécuter en tant qu’utilisateur WSL par défaut.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="3d8ff-118">Avoir les mêmes droits d’administration de Windows en tant que le processus appelant et le terminal.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="3d8ff-119">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="3d8ff-120">La commande qui suit Linux `wsl.exe` est gérée comme n’importe quelle commande Exécuter dans WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="3d8ff-121">Les éléments tels que sudo, pipelines et la redirection de fichiers fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="3d8ff-122">Exemple à l’aide de sudo :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="3d8ff-123">Exemples de combinaison de commandes WSL et Windows :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="3d8ff-124">Les commandes passées dans `wsl.exe` sont transférés vers le processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="3d8ff-125">Chemins d’accès de fichier doivent être spécifiés dans le format WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="3d8ff-126">Exemple avec des chemins d’accès :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="3d8ff-127">Exécuter des outils de Windows à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="3d8ff-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="3d8ff-128">WSL peut appeler les fichiers binaires Windows directement à partir de la ligne de commande WSL à l’aide `[binary name].exe`.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="3d8ff-129">Par exemple, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="3d8ff-130">Pour faciliter les exécutables Windows exécuter, chemin d’accès Windows est inclus dans le Linux `$PATH` dans Fall Creators Update.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="3d8ff-131">Les applications exécutées de cette façon ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="3d8ff-132">Conserver le répertoire de travail en tant que l’invite de commandes WSL (la plupart du temps, les exceptions sont expliquées ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="3d8ff-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="3d8ff-133">Avoir les mêmes droits d’autorisation que le processus WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="3d8ff-134">Exécuter en tant que l’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="3d8ff-135">S’affichent dans le Gestionnaire des tâches Windows comme si exécuté directement à partir de l’invite de commande.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="3d8ff-136">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="3d8ff-137">Les exécutables Windows s’exécutent dans WSL sont gérées de la même façon à natif Linux exécutables--tuyauterie, effectue une redirection et même backgrounding travail comme prévu.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="3d8ff-138">Exemples d’utilisation de canaux :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="3d8ff-139">Exemple d’utilisation des commandes Windows et WSL mixtes :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="3d8ff-140">Les fichiers binaires Windows doivent inclure l’extension de fichier, correspond à la casse de fichier et être exécutable.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="3d8ff-141">Non-fichiers exécutables, y compris les scripts de commandes.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="3d8ff-142">Comme les commandes natives CMD `dir` peut être exécuté avec `cmd.exe /C` commande.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="3d8ff-143">Exemples :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="3d8ff-144">Paramètres sont passés à la Windows binaire tels quels.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="3d8ff-145">Par exemple, les commandes suivantes seront ouvre `C:\temp\foo.txt` dans `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="3d8ff-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="3d8ff-146">Modification des fichiers situés sur VolFs (ne fichiers pas sous `/mnt/<x>`) avec un Windows application dans WSL n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="3d8ff-147">Par défaut, WSL tente de conserver le répertoire de travail de la Windows binaire comme répertoire actuel WSL mais reviendra sur le répertoire de la création d’instance si le répertoire de travail se trouve sur VolFs.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="3d8ff-148">Par exemple ; `wsl.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est modifié à l’accueil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="3d8ff-149">Lorsque `notepad.exe` est appelée à partir du répertoire de base de l’utilisateur, WSL revient automatiquement à `C:\temp` comme répertoire de travail notepad.exe :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="3d8ff-150">Partager des variables d’environnement entre Windows et WSL</span><span class="sxs-lookup"><span data-stu-id="3d8ff-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="3d8ff-151">Disponible dans les builds Windows Insider 17063 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="3d8ff-152">Avant de 17063, était uniquement Windows variable d’environnement WSL pourrait accéder `PATH` (donc vous pouvez lancer des exécutables Win32 sous WSL).</span><span class="sxs-lookup"><span data-stu-id="3d8ff-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="3d8ff-153">À compter de 17063, WSL et Windows partagent `WSLENV`, une variable d’environnement spécial créée pour combler les distributions Windows et Linux en cours d’exécution sur WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="3d8ff-154">Propriétés de `WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="3d8ff-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="3d8ff-155">Elle est partagée ; Il existe dans les environnements Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="3d8ff-156">C’est une liste de variables d’environnement à partager entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="3d8ff-157">Il peut mettre en forme des variables d’environnement pour fonctionner correctement dans Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="3d8ff-158">Il existe quatre indicateurs disponibles dans `WSLENV` pour influencer la façon dont cette variable d’environnement est convertie.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="3d8ff-159">`WSLENV` indicateurs :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="3d8ff-160">`/p` -Convertit le chemin d’accès entre les chemins de Win32 et style WSL/Linux.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="3d8ff-161">`/l` -Indique la variable d’environnement est une liste de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="3d8ff-162">`/u` -Indique que cette variable d’environnement doit uniquement apparaître lors de l’exécution WSL à partir de Win32.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="3d8ff-163">`/w` -Indique que cette variable d’environnement doit uniquement apparaître lors de l’exécution de Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="3d8ff-164">Indicateurs peuvent être combinées en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="3d8ff-165">Désactiver l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="3d8ff-165">Disable Interop</span></span>

<span data-ttu-id="3d8ff-166">Les utilisateurs peuvent désactiver la capacité d’exécuter des fichiers binaires Windows pour une seule session WSL en exécutant la commande suivante en tant que racine :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="3d8ff-167">Pour réactiver Windows binaires quitter toutes les sessions WSL et réexécutez bash.exe ou exécutez la commande suivante en tant que racine :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="3d8ff-168">La désactivation d’interopérabilité n’est pas persistante entre les sessions WSL--interop est de nouveau activée lorsqu’une nouvelle session est lancée.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="3d8ff-169">Creators Update et mise à jour anniversaire</span><span class="sxs-lookup"><span data-stu-id="3d8ff-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="3d8ff-170">Alors que l’automne préliminaire expérience interop Creators Update est similaire aux expériences d’interopérabilité plus récentes, il existe un handfull des différences majeures.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handfull of major differences.</span></span>

<span data-ttu-id="3d8ff-171">Résumé :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-171">To summarize:</span></span>

* <span data-ttu-id="3d8ff-172">`bash.exe` a été déconseillée et remplacée par `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="3d8ff-173">`-c` option pour une seule commande en cours d’exécution n’est pas nécessaire avec `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="3d8ff-174">Chemin d’accès de Windows est inclus dans le WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="3d8ff-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="3d8ff-175">Le processus de désactivation d’interopérabilité est inchangé.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="3d8ff-176">Appel de WSL à partir de la ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="3d8ff-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="3d8ff-177">Les fichiers binaires de Linux peuvent être appelées à partir de l’invite de commandes Windows ou à partir de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="3d8ff-178">Les fichiers binaires appelés de cette façon ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="3d8ff-179">Utiliser le même répertoire de travail en tant que l’invite CMD ou PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="3d8ff-180">Exécuter en tant qu’utilisateur WSL par défaut.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="3d8ff-181">Avoir les mêmes droits d’administration de Windows en tant que le processus appelant et le terminal.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="3d8ff-182">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="3d8ff-183">Commandes Linux appelés de cette façon sont gérées comme toute autre application Windows.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="3d8ff-184">Éléments tels que la redirection de fichiers d’entrée et tuyauterie fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="3d8ff-185">Exemples :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-185">Examples:</span></span>

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

<span data-ttu-id="3d8ff-186">Les commandes WSL passé dans `bash -c` sont transférés vers le processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="3d8ff-187">Chemins d’accès de fichier doivent être spécifiés dans le format WSL et être vigilant pour échapper les caractères appropriés.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="3d8ff-188">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="3d8ff-189">Appel des fichiers binaires Windows à partir de WSL</span><span class="sxs-lookup"><span data-stu-id="3d8ff-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="3d8ff-190">Le sous-système Windows pour Linux peut appeler les fichiers binaires Windows directement à partir de la ligne de commande WSL.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="3d8ff-191">Les applications exécutées de cette façon ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="3d8ff-192">Conserver le répertoire de travail en tant que l’invite de commandes WSL, sauf dans le scénario expliqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="3d8ff-193">Ont les mêmes droits d’autorisation que le `bash.exe` processus.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="3d8ff-194">Exécuter en tant que l’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="3d8ff-195">S’affichent dans le Gestionnaire des tâches Windows comme si exécuté directement à partir de l’invite de commande.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="3d8ff-196">Exemple :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="3d8ff-197">Dans WSL, ces fichiers exécutables sont gérées similaire pour des exécutables natifs Linux.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="3d8ff-198">Cela signifie l’ajout de répertoires pour le chemin d’accès de Linux et tuyauterie entre le fonctionnement des commandes comme prévu.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="3d8ff-199">Exemples :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="3d8ff-200">Le fichier binaire Windows doit inclure l’extension de fichier, correspond à la casse de fichier et être exécutable.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="3d8ff-201">Non-fichiers exécutables, y compris par lot de scripts et de commande comme `dir` peut être exécuté avec `/mnt/c/Windows/System32/cmd.exe /C` commande.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="3d8ff-202">Exemples :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="3d8ff-203">Paramètres sont passés à la Windows binaire tels quels.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="3d8ff-204">Par exemple, les commandes suivantes seront ouvre `C:\temp\foo.txt` dans `notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="3d8ff-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="3d8ff-205">Modification des fichiers situés sur VolFs (ne fichiers pas sous `/mnt/<x>`) avec un Windows application n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="3d8ff-206">Par défaut, WSL tente de conserver le répertoire de travail de la Windows binaire comme répertoire actuel WSL mais reviendra sur le répertoire de la création d’instance si le répertoire de travail se trouve sur VolFs.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="3d8ff-207">Par exemple ; `bash.exe` est initialement lancé à partir de `C:\temp` et le répertoire WSL actif est modifié à l’accueil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d8ff-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="3d8ff-208">Lorsque `notepad.exe` est appelée à partir du répertoire de base de l’utilisateur, WSL revient automatiquement à `C:\temp` comme répertoire de travail notepad.exe :</span><span class="sxs-lookup"><span data-stu-id="3d8ff-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
