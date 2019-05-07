---
title: Sous-système Windows pour la référence de commande Linux
description: Liste des commandes qui gèrent le sous-système Windows pour Linux
keywords: BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063577"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="141e6-104">Référence des commandes pour le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="141e6-104">Command Reference for Windows Subsystem for Linux</span></span>

> <span data-ttu-id="141e6-105">`lxrun.exe` est déconseillé à compter de Windows 10 1803 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="141e6-105">`lxrun.exe` is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="141e6-106">La commande `lxrun.exe` peut être utilisé pour interagir avec le [sous-système Windows pour Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directement.</span><span class="sxs-lookup"><span data-stu-id="141e6-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="141e6-107">Ces commandes sont installées dans le `\Windows\System32` directory et peut être exécuté dans une invite de commandes Windows ou dans PowerShell.</span><span class="sxs-lookup"><span data-stu-id="141e6-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* <span data-ttu-id="141e6-108">`lxrun.exe` est utilisé pour gérer les WSL.</span><span class="sxs-lookup"><span data-stu-id="141e6-108">`lxrun.exe` is used to manage WSL.</span></span>  <span data-ttu-id="141e6-109">Cette commande peut être utilisée pour installer ou désinstaller l’image Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="141e6-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="141e6-110">Command</span><span class="sxs-lookup"><span data-stu-id="141e6-110">Command</span></span>                     | <span data-ttu-id="141e6-111">Description</span><span class="sxs-lookup"><span data-stu-id="141e6-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="141e6-112">Lance l’interpréteur de commandes Bash dans le répertoire actif.</span><span class="sxs-lookup"><span data-stu-id="141e6-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="141e6-113">Si l’interpréteur de commandes Bash n’est pas automatiquement installé s’exécute `lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="141e6-113">If the Bash shell is not installed automatically runs `lxrun /install`</span></span> |
| `bash ~`                    | <span data-ttu-id="141e6-114">Lance l’interpréteur de commandes bash dans le répertoire de base de l’utilisateur Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="141e6-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="141e6-115">Similaire à l’exécution des cd ~</span><span class="sxs-lookup"><span data-stu-id="141e6-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="141e6-116">Exécute la commande, imprime la sortie et se termine à l’invite de commandes Windows.</span><span class="sxs-lookup"><span data-stu-id="141e6-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="141e6-117">Exemple : **bash -c « ls »**</span><span class="sxs-lookup"><span data-stu-id="141e6-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="141e6-118">Command</span><span class="sxs-lookup"><span data-stu-id="141e6-118">Command</span></span>                     | <span data-ttu-id="141e6-119">Description</span><span class="sxs-lookup"><span data-stu-id="141e6-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="141e6-120">La commande lxrun est utilisée pour gérer l’instance WSL.</span><span class="sxs-lookup"><span data-stu-id="141e6-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="141e6-121">Démarre le téléchargement et le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="141e6-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="141e6-122">**/y** peuvent être ajoutés à ignorer toutes les invites.</span><span class="sxs-lookup"><span data-stu-id="141e6-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="141e6-123">L’invite de confirmation est accepté automatiquement et l’utilisateur par défaut est défini pour la racine.</span><span class="sxs-lookup"><span data-stu-id="141e6-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="141e6-124">Désinstalle et supprime l’image Ubuntu.</span><span class="sxs-lookup"><span data-stu-id="141e6-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="141e6-125">Par défaut, cela ne supprime pas le Ubuntu répertoire de base.</span><span class="sxs-lookup"><span data-stu-id="141e6-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="141e6-126">**/y** peuvent être ajoutés à accepter automatiquement l’invite de confirmation</span><span class="sxs-lookup"><span data-stu-id="141e6-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="141e6-127">**toutes les** désinstalle et supprime le répertoire de base de l’utilisateur Ubuntu</span><span class="sxs-lookup"><span data-stu-id="141e6-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="141e6-128">Définit la valeur par défaut Bash sur Ubuntu utilisateur.</span><span class="sxs-lookup"><span data-stu-id="141e6-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="141e6-129">Demande un mot de passe si l’utilisateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="141e6-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="141e6-130">Pour plus d’informations, visitez : https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="141e6-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="141e6-131">**/y** promping de contournements pour le mot de passe.</span><span class="sxs-lookup"><span data-stu-id="141e6-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="141e6-132">L’utilisateur sera créé sans un mot de passe.</span><span class="sxs-lookup"><span data-stu-id="141e6-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="141e6-133">Met à jour les index de package du sous-système</span><span class="sxs-lookup"><span data-stu-id="141e6-133">Updates the subsystem's package index</span></span>          |
