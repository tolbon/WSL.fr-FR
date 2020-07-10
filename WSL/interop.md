---
title: Interopérabilité Windows avec Linux
description: Décrit l’interopérabilité Windows avec les distributions Linux exécutées sur le sous-système Windows pour Linux.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: d78cc53aa40f896c20e40a5ef00570a97ccac258
ms.sourcegitcommit: 386d47a1c53a85b91f5a2b0f1f99ce2c46b20a77
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2020
ms.locfileid: "86093269"
---
# <a name="windows-interoperability-with-linux"></a><span data-ttu-id="95f84-103">Interopérabilité Windows avec Linux</span><span class="sxs-lookup"><span data-stu-id="95f84-103">Windows interoperability with Linux</span></span>

<span data-ttu-id="95f84-104">Le sous-système Windows pour Linux (WSL) améliore en permanence l’intégration entre Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="95f84-104">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="95f84-105">Vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="95f84-105">You can:</span></span>

* <span data-ttu-id="95f84-106">Exécuter les outils Windows (p. ex. notepad.exe) à partir d’une ligne de commande Linux (p. ex. Ubuntu).</span><span class="sxs-lookup"><span data-stu-id="95f84-106">Run Windows tools (ie. notepad.exe) from a Linux command line (ie. Ubuntu).</span></span>
* <span data-ttu-id="95f84-107">Exécuter les outils Linux (p. ex. grep) à partir d’une ligne de commande Windows (p. ex. PowerShell).</span><span class="sxs-lookup"><span data-stu-id="95f84-107">Run Linux tools (ie. grep) from a Windows command line (ie. PowerShell).</span></span>
* <span data-ttu-id="95f84-108">Partager des variables d’environnement entre Linux et Windows.</span><span class="sxs-lookup"><span data-stu-id="95f84-108">Share environment variables between Linux and Windows.</span></span> <span data-ttu-id="95f84-109">(Build 17063+)</span><span class="sxs-lookup"><span data-stu-id="95f84-109">(Build 17063+)</span></span>

> [!NOTE]
> <span data-ttu-id="95f84-110">Si vous exécutez une version Creators Update (octobre 2017, build 16299) ou la mise à jour anniversaire (août 2016, build 14393), accédez aux [versions antérieures de Windows 10](#earlier-versions-of-windows-10).</span><span class="sxs-lookup"><span data-stu-id="95f84-110">If you're running Creators Update (Oct 2017, Build 16299) or Anniversary Update (Aug 2016, Build 14393), jump to the [Earlier versions of Windows 10](#earlier-versions-of-windows-10).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="95f84-111">Exécuter les outils Linux à partir d’une ligne de commande Windows</span><span class="sxs-lookup"><span data-stu-id="95f84-111">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="95f84-112">Exécutez des fichiers binaires Linux à partir de l’invite de commandes Windows (CMD) ou de PowerShell en utilisant `wsl <command>` (ou `wsl.exe <command>`).</span><span class="sxs-lookup"><span data-stu-id="95f84-112">Run Linux binaries from the Windows Command Prompt (CMD) or PowerShell using `wsl <command>` (or `wsl.exe <command>`).</span></span>

<span data-ttu-id="95f84-113">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="95f84-113">For example:</span></span>

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="95f84-114">Les fichiers binaires appelés de cette façon :</span><span class="sxs-lookup"><span data-stu-id="95f84-114">Binaries invoked in this way:</span></span>

* <span data-ttu-id="95f84-115">Utilisent le même répertoire de travail que l’invite CMD ou PowerShell en cours.</span><span class="sxs-lookup"><span data-stu-id="95f84-115">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
* <span data-ttu-id="95f84-116">Sont exécutés en tant qu’utilisateur par défaut WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-116">Run as the WSL default user.</span></span>
* <span data-ttu-id="95f84-117">Ont les mêmes droits d’administration Windows que le terminal et le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="95f84-117">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="95f84-118">La commande Linux qui suit `wsl` (ou `wsl.exe`) est gérée comme n’importe quelle commande exécutée dans WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-118">The Linux command following `wsl` (or `wsl.exe`) is handled like any command run in WSL.</span></span>  <span data-ttu-id="95f84-119">Des actions comme l’exécution de sudo, la création de canaux et la redirection de fichiers fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="95f84-119">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="95f84-120">Exemple utilisant sudo pour mettre à jour votre distribution Linux par défaut :</span><span class="sxs-lookup"><span data-stu-id="95f84-120">Example using sudo to update your default Linux distribution:</span></span>

```powershell
C:\temp> wsl sudo apt-get update
```

<span data-ttu-id="95f84-121">Votre nom d’utilisateur de distribution Linux par défaut sera listé après l’exécution de cette commande et vous serez invité à entrer votre mot de passe.</span><span class="sxs-lookup"><span data-stu-id="95f84-121">Your default Linux distribution user name will be listed after running this command and you will be asked for your password.</span></span> <span data-ttu-id="95f84-122">Une fois que vous avez entré correctement votre mot de passe, votre distribution télécharge les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="95f84-122">After entering your password correctly, your distribution will download updates.</span></span>

## <a name="mixing-linux-and-windows-commands"></a><span data-ttu-id="95f84-123">Combinaison de commandes Linux et Windows</span><span class="sxs-lookup"><span data-stu-id="95f84-123">Mixing Linux and Windows commands</span></span>

<span data-ttu-id="95f84-124">Voici quelques exemples de combinaison de commandes Linux et Windows à l’aide de PowerShell.</span><span class="sxs-lookup"><span data-stu-id="95f84-124">Here are a few examples of mixing Linux and Windows commands using PowerShell.</span></span>

<span data-ttu-id="95f84-125">Pour utiliser la commande Linux `ls -la` pour lister les fichiers et la commande PowerShell `findstr` pour filtrer les résultats avec des mots contenant « git », combinez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="95f84-125">To use the Linux command `ls -la` to list files and the PowerShell command `findstr` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
wsl ls -la | findstr "git"
```

<span data-ttu-id="95f84-126">Pour utiliser la commande PowerShell `dir` pour lister les fichiers et la commande Linux `grep` pour filtrer les résultats avec des mots contenant « git », combinez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="95f84-126">To use the PowerShell command `dir` to list files and the Linux command `grep` to filter the results for words containing "git", combine the commands:</span></span>

```powershell
C:\temp> dir | wsl grep git
```

<span data-ttu-id="95f84-127">Pour utiliser la commande Linux `ls -la` pour lister les fichiers et la commande PowerShell `> out.txt` pour imprimer cette liste dans un fichier texte nommé « out.txt », combinez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="95f84-127">To use the Linux command `ls -la` to list files and the PowerShell command `> out.txt` to print that list to a text file named "out.txt", combine the commands:</span></span>

```powershell
C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="95f84-128">Les commandes passées à `wsl.exe` sont transmises au processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="95f84-128">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="95f84-129">Les chemins de fichiers doivent être spécifiés au format WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-129">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="95f84-130">Pour utiliser la commande Linux `ls -la` pour lister les fichiers dans le chemin du système de fichiers Linux `/proc/cpuinfo`, à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="95f84-130">To use the Linux command `ls -la` to list files in the `/proc/cpuinfo` Linux file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

<span data-ttu-id="95f84-131">Pour utiliser la commande Linux `ls -la` pour lister les fichiers dans le chemin du système de fichiers Windows `C:\Program Files`, à l’aide de PowerShell :</span><span class="sxs-lookup"><span data-stu-id="95f84-131">To use the Linux command `ls -la` to list files in the `C:\Program Files` Windows file system path, using PowerShell:</span></span>

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a><span data-ttu-id="95f84-132">Exécuter des outils Windows à partir de Linux</span><span class="sxs-lookup"><span data-stu-id="95f84-132">Run Windows tools from Linux</span></span>

<span data-ttu-id="95f84-133">WSL peut exécuter des outils Windows directement à partir de la ligne de commande WSL à l’aide de `[tool-name].exe`.</span><span class="sxs-lookup"><span data-stu-id="95f84-133">WSL can run Windows tools directly from the WSL command line using `[tool-name].exe`.</span></span>  <span data-ttu-id="95f84-134">Par exemple, `notepad.exe`.</span><span class="sxs-lookup"><span data-stu-id="95f84-134">For example, `notepad.exe`.</span></span>

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

<span data-ttu-id="95f84-135">Les applications exécutées de cette manière ont les propriétés suivantes :</span><span class="sxs-lookup"><span data-stu-id="95f84-135">Applications run this way have the following properties:</span></span>

* <span data-ttu-id="95f84-136">Conservent le répertoire de travail en tant qu’invite de commandes WSL (en général, les exceptions sont décrites ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="95f84-136">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
* <span data-ttu-id="95f84-137">Ont les mêmes autorisations que le processus WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-137">Have the same permission rights as the WSL process.</span></span>
* <span data-ttu-id="95f84-138">Sont exécutées en tant qu’utilisateur Windows actif.</span><span class="sxs-lookup"><span data-stu-id="95f84-138">Run as the active Windows user.</span></span>
* <span data-ttu-id="95f84-139">Apparaissent dans le Gestionnaire des tâches de Windows comme si elles étaient directement exécutées à partir de l’invite CMD.</span><span class="sxs-lookup"><span data-stu-id="95f84-139">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="95f84-140">Les exécutables Windows exécutés dans WSL sont gérés de la même façon que les exécutables Linux natifs : la création de canaux, les redirections et même le travail en arrière-plan fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="95f84-140">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="95f84-141">Pour exécuter l’outil Windows `ipconfig.exe`, utiliser l’outil Linux `grep` afin de filtrer les résultats « IPv4 », et utiliser l’outil Linux `cut` afin de supprimer les champs de colonne, à partir d’une distribution Linux (par exemple, Ubuntu), entrez :</span><span class="sxs-lookup"><span data-stu-id="95f84-141">To run the Windows tool `ipconfig.exe`, use the Linux tool `grep` to filter the "IPv4" results, and use the Linux tool `cut` to remove the column fields, from a Linux distribution (for example, Ubuntu) enter:</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="95f84-142">Essayons un exemple combinant des commandes Windows et Linux.</span><span class="sxs-lookup"><span data-stu-id="95f84-142">Let's try an example mixing Windows and Linux commands.</span></span> <span data-ttu-id="95f84-143">Ouvrez votre distribution Linux (p. ex. Ubuntu) et créez un fichier texte : `touch foo.txt`.</span><span class="sxs-lookup"><span data-stu-id="95f84-143">Open your Linux distribution (ie. Ubuntu) and create a text file: `touch foo.txt`.</span></span> <span data-ttu-id="95f84-144">À présent, utilisez la commande Linux `ls -la` pour lister les fichiers directs et les détails de leur création, ainsi que l’outil Windows PowerShell `findstr.exe` pour filtrer les résultats afin que seul votre fichier `foo.txt` s’affiche dans les résultats :</span><span class="sxs-lookup"><span data-stu-id="95f84-144">Now use the Linux command `ls -la` to list the direct files and their creation details, plus the Windows PowerShell tool `findstr.exe` to filter the results so only your `foo.txt` file shows in the results:</span></span>

```bash
ls -la | findstr.exe foo.txt
```

<span data-ttu-id="95f84-145">Les outils Windows doivent inclure l’extension de fichier, correspondre à la casse de fichier et être exécutables.</span><span class="sxs-lookup"><span data-stu-id="95f84-145">Windows tools must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="95f84-146">Les fichiers non exécutables, dont les scripts de commandes et</span><span class="sxs-lookup"><span data-stu-id="95f84-146">Non-executables including batch scripts.</span></span>  <span data-ttu-id="95f84-147">les commandes natives CMD comme `dir`, peuvent être exécutés avec la commande `cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="95f84-147">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="95f84-148">Par exemple, listez le contenu du répertoire C:\ de votre système de fichiers Windows, en entrant :</span><span class="sxs-lookup"><span data-stu-id="95f84-148">For example, list the contents of your Windows files system C:\ directory, by entering:</span></span>

```bash
cmd.exe /C dir
```

<span data-ttu-id="95f84-149">Ou utilisez la commande `ping` pour envoyer une demande d’écho au site web microsoft.com :</span><span class="sxs-lookup"><span data-stu-id="95f84-149">Or use the `ping` command to send an echo request to the microsoft.com website:</span></span>

```bash
ping.exe www.microsoft.com
```

<span data-ttu-id="95f84-150">Les paramètres sont passés au fichier binaire Windows non modifié.</span><span class="sxs-lookup"><span data-stu-id="95f84-150">Parameters are passed to the Windows binary unmodified.</span></span> <span data-ttu-id="95f84-151">Par exemple, la commande suivante ouvre `C:\temp\foo.txt` dans `notepad.exe` :</span><span class="sxs-lookup"><span data-stu-id="95f84-151">As an example, the following command will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

```bash
notepad.exe "C:\temp\foo.txt"
```

<span data-ttu-id="95f84-152">Cela fonctionne également :</span><span class="sxs-lookup"><span data-stu-id="95f84-152">This will also work:</span></span>

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="95f84-153">Partager des variables d’environnement entre Windows et WSL</span><span class="sxs-lookup"><span data-stu-id="95f84-153">Share environment variables between Windows and WSL</span></span>

<span data-ttu-id="95f84-154">WSL et Windows partagent une variable d’environnement spéciale, `WSLENV`, créée pour relier les distributions Windows et Linux s’exécutant sur WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-154">WSL and Windows share a special environment variable, `WSLENV`, created to bridge Windows and Linux distributions running on WSL.</span></span>

<span data-ttu-id="95f84-155">Propriétés de la variable `WSLENV` :</span><span class="sxs-lookup"><span data-stu-id="95f84-155">Properties of `WSLENV` variable:</span></span>

* <span data-ttu-id="95f84-156">Elle est partagée et existe dans les environnements Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-156">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="95f84-157">Il s’agit d’une liste de variables d’environnement à partager entre Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-157">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="95f84-158">Elle peut mettre en forme des variables d’environnement pour fonctionner correctement dans Windows et WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-158">It can format environment variables to work well in Windows and WSL.</span></span>
* <span data-ttu-id="95f84-159">Elle peut faciliter le flux entre WSL et Win32.</span><span class="sxs-lookup"><span data-stu-id="95f84-159">It can assist in the flow between WSL and Win32.</span></span>

> [!NOTE]
> <span data-ttu-id="95f84-160">Avant la build 17063, la seule variable d’environnement Windows à laquelle WSL pouvait accéder était `PATH` (par conséquent, vous pouviez lancer des exécutables Win32 sous WSL).</span><span class="sxs-lookup"><span data-stu-id="95f84-160">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span> <span data-ttu-id="95f84-161">Avec la build 17063, `WSLENV` commence à être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="95f84-161">Starting in 17063, `WSLENV` begins being supported.</span></span>
> <span data-ttu-id="95f84-162">WSLENV respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="95f84-162">WSLENV is case sensitive.</span></span>

## <a name="wslenv-flags"></a><span data-ttu-id="95f84-163">Indicateurs WSLENV</span><span class="sxs-lookup"><span data-stu-id="95f84-163">WSLENV flags</span></span>

<span data-ttu-id="95f84-164">Quatre indicateurs sont disponibles dans `WSLENV` pour influencer la manière dont cette variable d’environnement est traduite.</span><span class="sxs-lookup"><span data-stu-id="95f84-164">There are four flags available in `WSLENV` to influence how the environment variable is translated.</span></span>

<span data-ttu-id="95f84-165">Indicateurs `WSLENV` :</span><span class="sxs-lookup"><span data-stu-id="95f84-165">`WSLENV` flags:</span></span>

* <span data-ttu-id="95f84-166">`/p` : convertit le chemin entre les chemins de style WSL/Linux et les chemins Win32.</span><span class="sxs-lookup"><span data-stu-id="95f84-166">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="95f84-167">`/l` : indique que la variable d’environnement est une liste de chemins.</span><span class="sxs-lookup"><span data-stu-id="95f84-167">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="95f84-168">`/u` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de WSL à partir de Win32.</span><span class="sxs-lookup"><span data-stu-id="95f84-168">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="95f84-169">`/w` : indique que cette variable d’environnement doit être incluse uniquement lors de l’exécution de Win32 à partir de WSL.</span><span class="sxs-lookup"><span data-stu-id="95f84-169">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="95f84-170">Les indicateurs peuvent être combinés en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="95f84-170">Flags can be combined as needed.</span></span>

<span data-ttu-id="95f84-171">Pour en savoir plus sur WSLENV, [consultez ce blog](https://devblogs.microsoft.com/commandline/share-environment-vars-between-wsl-and-windows/). Vous y trouverez notamment des questions fréquentes et des exemples pour définir la valeur de WSLENV avec une concaténation de variables d’environnement prédéfinies, chaque variable ayant pour suffixe une barre oblique suivie d’indicateurs pour spécifier comment la valeur doit être traduite. Vous apprendrez également à passer des variables avec un script.</span><span class="sxs-lookup"><span data-stu-id="95f84-171">[Read more about WSLENV](https://devblogs.microsoft.com/commandline/share-environment-vars-between-wsl-and-windows/), including FAQs and examples of setting the value of WSLENV to a concatenation of other pre-defined environment vars, each suffixed with a slash followed by flags to specify how the value should be translated and passing variables with a script.</span></span> <span data-ttu-id="95f84-172">Cet article contient aussi un exemple montrant comment configurer un environnement de développement avec le [langage de programmation Go](https://golang.org/) pour partager un GOPATH entre WSL et Win32.</span><span class="sxs-lookup"><span data-stu-id="95f84-172">This article also includes an example for setting up a dev environment with the [Go programming language](https://golang.org/), configured to share a GOPATH between WSL and Win32.</span></span>

## <a name="disable-interoperability"></a><span data-ttu-id="95f84-173">Désactiver l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="95f84-173">Disable interoperability</span></span>

<span data-ttu-id="95f84-174">Les utilisateurs peuvent désactiver la possibilité d’exécuter des outils Windows pour une session WSL individuelle en exécutant la commande suivante en tant que racine :</span><span class="sxs-lookup"><span data-stu-id="95f84-174">Users may disable the ability to run Windows tools for a single WSL session by running the following command as root:</span></span>

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="95f84-175">Pour réactiver les fichiers binaires Windows, fermez toutes les sessions WSL et réexécutez bash.exe, ou exécutez la commande suivante en tant que racine :</span><span class="sxs-lookup"><span data-stu-id="95f84-175">To re-enable Windows binaries, exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="95f84-176">La désactivation de l’interopérabilité n’est pas conservée entre les sessions WSL : l’interopérabilité sera réactivée lors du lancement d’une nouvelle session.</span><span class="sxs-lookup"><span data-stu-id="95f84-176">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="earlier-versions-of-windows-10"></a><span data-ttu-id="95f84-177">Versions antérieures de Windows 10</span><span class="sxs-lookup"><span data-stu-id="95f84-177">Earlier versions of Windows 10</span></span>

<span data-ttu-id="95f84-178">Il existe plusieurs différences pour les commandes d’interopérabilité sur les versions antérieures de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="95f84-178">There are several differences for the interoperability commands on earlier Windows 10 versions.</span></span> <span data-ttu-id="95f84-179">Si vous exécutez une version Creators Update (octobre 2017, build 16299) ou la mise à jour anniversaire (août 2016, build 14393) de Windows 10, nous vous recommandons d’effectuer une [mise à jour vers la dernière version de Windows](ms-settings:windowsupdate). Toutefois, si cela n’est pas possible, nous décrivons certaines différences d’interopérabilité ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="95f84-179">If you're running a Creators Update (Oct 2017, Build 16299), or Anniversary Update (Aug 2016, Build 14393) version of Windows 10, we recommend you [update to the latest Windows version](ms-settings:windowsupdate), but if that's not possible, we have outlined some of the interop differences below.</span></span>

<span data-ttu-id="95f84-180">Résumé :</span><span class="sxs-lookup"><span data-stu-id="95f84-180">Summary:</span></span>

* <span data-ttu-id="95f84-181">`bash.exe` a été remplacé par `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="95f84-181">`bash.exe` has been replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="95f84-182">L’option `-c` permettant d’exécuter une seule commande n’est pas nécessaire avec `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="95f84-182">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="95f84-183">Le chemin Windows est inclus dans la variable WSL `$PATH`.</span><span class="sxs-lookup"><span data-stu-id="95f84-183">Windows path is included in the WSL `$PATH`.</span></span>
* <span data-ttu-id="95f84-184">Le processus de désactivation de l’interopérabilité est inchangé.</span><span class="sxs-lookup"><span data-stu-id="95f84-184">The process for disabling interop is unchanged.</span></span>

<span data-ttu-id="95f84-185">Les commandes Linux peuvent être exécutées à partir de l’invite de commandes Windows ou de PowerShell, mais pour les versions antérieures de Windows, vous pouvez être amené à utiliser la commande `bash`.</span><span class="sxs-lookup"><span data-stu-id="95f84-185">Linux commands can be run from the Windows Command Prompt or from PowerShell, but for early Windows versions, you man need to use the `bash` command.</span></span> <span data-ttu-id="95f84-186">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="95f84-186">For example:</span></span>

```powershell
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="95f84-187">Des actions comme les entrées, la création de canaux et la redirection de fichiers fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="95f84-187">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="95f84-188">Les commandes WSL passées à `bash -c` sont transmises au processus WSL sans modification.</span><span class="sxs-lookup"><span data-stu-id="95f84-188">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="95f84-189">Les chemins de fichiers doivent être spécifiés au format WSL et des précautions doivent être prises pour placer les caractères appropriés dans une séquence d’échappement.</span><span class="sxs-lookup"><span data-stu-id="95f84-189">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="95f84-190">Exemple :</span><span class="sxs-lookup"><span data-stu-id="95f84-190">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

<span data-ttu-id="95f84-191">Ou ...</span><span class="sxs-lookup"><span data-stu-id="95f84-191">Or...</span></span>

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

<span data-ttu-id="95f84-192">Lorsque vous appelez un outil Windows à partir d’une distribution WSL dans une version antérieure de Windows 10, vous devez spécifier le chemin du répertoire.</span><span class="sxs-lookup"><span data-stu-id="95f84-192">When calling a Windows tool from a WSL distribution in an earlier version of Windows 10, you will need to specify the directory path.</span></span> <span data-ttu-id="95f84-193">Par exemple, à partir de votre ligne de commande WSL, entrez :</span><span class="sxs-lookup"><span data-stu-id="95f84-193">For example, from your WSL command line, enter:</span></span>

```bash
/mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="95f84-194">Dans WSL, ces exécutables sont gérés de la même façon que les exécutables Linux natifs.</span><span class="sxs-lookup"><span data-stu-id="95f84-194">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="95f84-195">Cela signifie que l’ajout de répertoires au chemin Linux et la création de canaux entre les commandes fonctionnent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="95f84-195">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="95f84-196">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="95f84-196">For example:</span></span>

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
<span data-ttu-id="95f84-197">Ou</span><span class="sxs-lookup"><span data-stu-id="95f84-197">Or</span></span>

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

<span data-ttu-id="95f84-198">Le fichier binaire Windows doit inclure l’extension de fichier, correspondre à la casse de fichier et être exécutable.</span><span class="sxs-lookup"><span data-stu-id="95f84-198">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="95f84-199">Les fichiers non exécutables, dont les scripts de commandes et une commande comme `dir`, peuvent être exécutés avec la commande `/mnt/c/Windows/System32/cmd.exe /C`.</span><span class="sxs-lookup"><span data-stu-id="95f84-199">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span> <span data-ttu-id="95f84-200">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="95f84-200">For example:</span></span>

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a><span data-ttu-id="95f84-201">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="95f84-201">Additional resources</span></span>

* [<span data-ttu-id="95f84-202">Billet de blog WSL de 2016 sur l’interopérabilité</span><span class="sxs-lookup"><span data-stu-id="95f84-202">WSL blog post on interoperability from 2016</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
