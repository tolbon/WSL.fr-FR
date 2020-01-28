---
title: Résolution des problèmes du sous-système Windows pour Linux
description: Cet article fournit des informations détaillées sur les erreurs et problèmes courants auxquels peuvent être confrontés les utilisateurs exécutant Linux sur le sous-système Windows pour Linux.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, Ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ec456c314ac4a1588ccb5c1aa35e22a2d33a39b0
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520528"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="40af0-104">Résolution des problèmes liés au sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="40af0-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="40af0-105">Pour obtenir un support sur les problèmes liés à WSL, consultez notre dépôt GitHub :</span><span class="sxs-lookup"><span data-stu-id="40af0-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="40af0-106">Rechercher les problèmes existants en rapport avec votre problème</span><span class="sxs-lookup"><span data-stu-id="40af0-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="40af0-107">Pour les problèmes techniques, utilisez le dépôt du produit : https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="40af0-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="40af0-108">Pour les problèmes liés au contenu de cette documentation, utilisez le dépôt de la documentation : https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="40af0-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="40af0-109">Envoyer un rapport de bogues</span><span class="sxs-lookup"><span data-stu-id="40af0-109">Submit a bug report</span></span>

<span data-ttu-id="40af0-110">Pour les bogues liés aux fonctions ou fonctionnalités WSL, signalez un problème dans le dépôt du produit : https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="40af0-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="40af0-111">Envoyer une demande de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="40af0-111">Submit a feature request</span></span>

<span data-ttu-id="40af0-112">Pour demander une nouvelle fonctionnalité liée au fonctionnement ou à la compatibilité de WSL, signalez un problème dans le dépôt du produit : https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="40af0-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="40af0-113">Contribution à la documentation</span><span class="sxs-lookup"><span data-stu-id="40af0-113">Contribute to the docs</span></span>

<span data-ttu-id="40af0-114">Pour contribuer à la documentation WSL, envoyez une demande de tirage (pull request) dans le dépôt de la documentation : https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="40af0-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="40af0-115">Terminal ou ligne de commande</span><span class="sxs-lookup"><span data-stu-id="40af0-115">Terminal or Command Line</span></span>

<span data-ttu-id="40af0-116">Enfin, si votre problème est lié au terminal Windows, à la console Windows ou à l’interface utilisateur de ligne de commande, utilisez le dépôt du terminal Windows : https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="40af0-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="40af0-117">Problèmes courants</span><span class="sxs-lookup"><span data-stu-id="40af0-117">Common issues</span></span>

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="40af0-118">Bash perd la connectivité réseau une fois connecté à un VPN</span><span class="sxs-lookup"><span data-stu-id="40af0-118">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="40af0-119">Si, après une connexion à un VPN sur Windows, Bash perd la connectivité réseau, essayez cette solution de contournement à partir de Bash.</span><span class="sxs-lookup"><span data-stu-id="40af0-119">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="40af0-120">Elle vous permet de remplacer la résolution DNS manuellement avec `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="40af0-120">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="40af0-121">Exécutez la commande `ipconfig.exe /all` et notez le serveur DNS du VPN.</span><span class="sxs-lookup"><span data-stu-id="40af0-121">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="40af0-122">Copiez le fichier resolv.conf existant avec `sudo cp /etc/resolv.conf /etc/resolv.conf.new`.</span><span class="sxs-lookup"><span data-stu-id="40af0-122">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="40af0-123">Dissociez le fichier resolv.conf actuel avec `sudo unlink /etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="40af0-123">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="40af0-124">Ouvrez `/etc/resolv.conf` et</span><span class="sxs-lookup"><span data-stu-id="40af0-124">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="40af0-125">a.</span><span class="sxs-lookup"><span data-stu-id="40af0-125">a.</span></span> <span data-ttu-id="40af0-126">Supprimez la première ligne du fichier, comportant le message « \# This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="40af0-126">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="40af0-127">To stop automatic generation of this file, remove this line. » (Ce fichier a été généré automatiquement par WSL. Pour arrêter la génération automatique de ce fichier, supprimez cette ligne. »).</span><span class="sxs-lookup"><span data-stu-id="40af0-127">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="40af0-128">b.</span><span class="sxs-lookup"><span data-stu-id="40af0-128">b.</span></span> <span data-ttu-id="40af0-129">Ajoutez l’entrée DNS notée à l’étape 1 précédente comme première entrée de la liste des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="40af0-129">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="40af0-130">c.</span><span class="sxs-lookup"><span data-stu-id="40af0-130">c.</span></span> <span data-ttu-id="40af0-131">Fermez le fichier.</span><span class="sxs-lookup"><span data-stu-id="40af0-131">Close the file.</span></span> <br/>

<span data-ttu-id="40af0-132">Une fois que vous avez déconnecté le VPN, vous devez revenir au fichier `/etc/resolv.conf` non modifié.</span><span class="sxs-lookup"><span data-stu-id="40af0-132">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="40af0-133">Pour ce faire, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="40af0-133">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="40af0-134">Le démarrage de WSL ou l’installation d’une distribution retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="40af0-134">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="40af0-135">Suivez [ces instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) pour récupérer des journaux détaillés et signaler un problème sur notre plateforme GitHub.</span><span class="sxs-lookup"><span data-stu-id="40af0-135">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="40af0-136">Mise à jour de Bash sur Ubuntu sur Windows</span><span class="sxs-lookup"><span data-stu-id="40af0-136">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="40af0-137">Deux composants de Bash sur Ubuntu sur Windows peuvent nécessiter une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="40af0-137">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="40af0-138">Sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="40af0-138">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="40af0-139">La mise à niveau de cette partie de Bash sur Ubuntu sur Windows active tous les nouveaux correctifs mentionnés dans les [notes de publication](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="40af0-139">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="40af0-140">Vérifiez que vous êtes abonné au programme Windows Insider et que votre build est à jour.</span><span class="sxs-lookup"><span data-stu-id="40af0-140">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="40af0-141">Pour un contrôle plus précis et, notamment, pour réinitialiser votre instance Ubuntu, consultez les [informations de référence sur les commandes](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="40af0-141">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="40af0-142">Fichiers binaires utilisateur Ubuntu</span><span class="sxs-lookup"><span data-stu-id="40af0-142">The Ubuntu user binaries</span></span>

   <span data-ttu-id="40af0-143">La mise à niveau de cette partie de Bash sur Ubuntu sur Windows installe toutes les mises à jour des fichiers binaires utilisateur Ubuntu, y compris les applications que vous avez installées avec apt-get.</span><span class="sxs-lookup"><span data-stu-id="40af0-143">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="40af0-144">Pour procéder à la mise à jour, exécutez les commandes suivantes dans Bash :</span><span class="sxs-lookup"><span data-stu-id="40af0-144">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="40af0-145">Erreurs avec apt-get upgrade</span><span class="sxs-lookup"><span data-stu-id="40af0-145">Apt-get upgrade errors</span></span>

<span data-ttu-id="40af0-146">Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées.</span><span class="sxs-lookup"><span data-stu-id="40af0-146">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="40af0-147">`udev`, par exemple, n’est pas encore pris en charge et provoque plusieurs erreurs avec `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="40af0-147">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="40af0-148">Pour résoudre les problèmes liés à `udev`, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="40af0-148">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="40af0-149">Écrivez le code suivant dans `/usr/sbin/policy-rc.d` et enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="40af0-149">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="40af0-150">Ajoutez des autorisations d’exécution à `/usr/sbin/policy-rc.d` :</span><span class="sxs-lookup"><span data-stu-id="40af0-150">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="40af0-151">Exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="40af0-151">Run the following commands:</span></span>

   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="40af0-152">« Error : 0x80040306 » lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="40af0-152">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="40af0-153">Cette erreur est due au fait que nous ne prenons pas en charge la console héritée.</span><span class="sxs-lookup"><span data-stu-id="40af0-153">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="40af0-154">Pour désactiver la console héritée :</span><span class="sxs-lookup"><span data-stu-id="40af0-154">To turn off legacy console:</span></span>

1. <span data-ttu-id="40af0-155">Ouvrez cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="40af0-155">Open cmd.exe</span></span>
1. <span data-ttu-id="40af0-156">Cliquez avec le bouton droit sur la barre de titre, sélectionnez Propriétés, puis désactivez la case Utiliser la console héritée.</span><span class="sxs-lookup"><span data-stu-id="40af0-156">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="40af0-157">Cliquez sur OK</span><span class="sxs-lookup"><span data-stu-id="40af0-157">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="40af0-158">« Error : 0x80040154 » après une mise à jour de Windows</span><span class="sxs-lookup"><span data-stu-id="40af0-158">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="40af0-159">La fonctionnalité de sous-système Windows pour Linux peut être désactivée au cours d’une mise à jour de Windows.</span><span class="sxs-lookup"><span data-stu-id="40af0-159">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="40af0-160">Dans ce cas, la fonctionnalité Windows doit être réactivée.</span><span class="sxs-lookup"><span data-stu-id="40af0-160">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="40af0-161">Pour obtenir des instructions sur l’activation du sous-système Windows pour Linux, consultez le [guide d’installation](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="40af0-161">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="40af0-162">Changement de la langue d’affichage</span><span class="sxs-lookup"><span data-stu-id="40af0-162">Changing the display language</span></span>

<span data-ttu-id="40af0-163">Le processus d’installation de WSL tente de changer automatiquement les paramètres régionaux d’Ubuntu de sorte qu’ils correspondent à ceux de votre installation Windows.</span><span class="sxs-lookup"><span data-stu-id="40af0-163">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="40af0-164">Si vous souhaitez éviter ce comportement, vous pouvez exécuter cette commande pour changer les paramètres régionaux d’Ubuntu une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="40af0-164">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="40af0-165">Vous devrez relancer bash.exe pour que ce changement prenne effet.</span><span class="sxs-lookup"><span data-stu-id="40af0-165">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="40af0-166">L’exemple ci-dessous applique les paramètres régionaux en-US :</span><span class="sxs-lookup"><span data-stu-id="40af0-166">The below example changes to locale to en-US:</span></span>

``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="40af0-167">Problèmes d’installation après une restauration du système Windows</span><span class="sxs-lookup"><span data-stu-id="40af0-167">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="40af0-168">Supprimez le dossier `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="40af0-168">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="40af0-169">**Remarque : N’effectuez pas cette opération si votre fonctionnalité facultative est entièrement installée et opérationnelle.**</span><span class="sxs-lookup"><span data-stu-id="40af0-169">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="40af0-170">Si ce n’est déjà fait, activez la fonctionnalité facultative WSL.</span><span class="sxs-lookup"><span data-stu-id="40af0-170">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="40af0-171">Redémarrer</span><span class="sxs-lookup"><span data-stu-id="40af0-171">Reboot</span></span>
4. <span data-ttu-id="40af0-172">lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="40af0-172">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="40af0-173">Installez Bash.</span><span class="sxs-lookup"><span data-stu-id="40af0-173">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="40af0-174">Aucun accès Internet dans WSL</span><span class="sxs-lookup"><span data-stu-id="40af0-174">No internet access in WSL</span></span>

<span data-ttu-id="40af0-175">Certains utilisateurs ont signalé des problèmes posés par certaines applications de pare-feu, qui bloquent l’accès Internet dans WSL.</span><span class="sxs-lookup"><span data-stu-id="40af0-175">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="40af0-176">Les pare-feux signalés sont :</span><span class="sxs-lookup"><span data-stu-id="40af0-176">The firewalls reported are:</span></span>

1. <span data-ttu-id="40af0-177">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="40af0-177">Kaspersky</span></span>
2. <span data-ttu-id="40af0-178">AVG</span><span class="sxs-lookup"><span data-stu-id="40af0-178">AVG</span></span>
3. <span data-ttu-id="40af0-179">Avast</span><span class="sxs-lookup"><span data-stu-id="40af0-179">Avast</span></span>

<span data-ttu-id="40af0-180">Dans certains cas, la désactivation du pare-feu permet d’obtenir l’accès.</span><span class="sxs-lookup"><span data-stu-id="40af0-180">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="40af0-181">Parfois, il semble que la simple installation du pare-feu bloque l’accès.</span><span class="sxs-lookup"><span data-stu-id="40af0-181">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="40af0-182">Autorisation refusée lors de l’utilisation d’une commande ping</span><span class="sxs-lookup"><span data-stu-id="40af0-182">Permission Denied error when using ping</span></span>

<span data-ttu-id="40af0-183">Pour la [Mise à jour anniversaire Windows, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), les **privilèges administrateur** dans Windows doivent exécuter la commande ping dans WSL.</span><span class="sxs-lookup"><span data-stu-id="40af0-183">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="40af0-184">Pour exécuter une commande ping, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite de commandes/PowerShell avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="40af0-184">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="40af0-185">Pour les versions ultérieures de Windows, [Build 14926+](./release-notes.md#build-14926), les privilèges administrateur ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="40af0-185">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="40af0-186">Bash est bloqué.</span><span class="sxs-lookup"><span data-stu-id="40af0-186">Bash is hung</span></span>

<span data-ttu-id="40af0-187">Si, alors que vous utilisez Bash, celui-ci se bloque et ne répond pas aux entrées, aidez-nous à diagnostiquer le problème en collectant une image mémoire et en nous la communiquant.</span><span class="sxs-lookup"><span data-stu-id="40af0-187">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="40af0-188">Notez que la procédure ci-après entraînera le plantage de votre système.</span><span class="sxs-lookup"><span data-stu-id="40af0-188">Note that these steps will crash your system.</span></span> <span data-ttu-id="40af0-189">Suivez-la uniquement si vous êtes à l’aise avec ce type d’opération, ou enregistrez votre travail au préalable.</span><span class="sxs-lookup"><span data-stu-id="40af0-189">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="40af0-190">Pour collecter une image mémoire</span><span class="sxs-lookup"><span data-stu-id="40af0-190">To collect a memory dump</span></span>

1. <span data-ttu-id="40af0-191">Changez le type d’image mémoire en choisissant « Image mémoire complète ».</span><span class="sxs-lookup"><span data-stu-id="40af0-191">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="40af0-192">Lors de ce changement, prenez note du type d’image actuel.</span><span class="sxs-lookup"><span data-stu-id="40af0-192">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="40af0-193">Suivez [cette procédure](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) pour configurer une commande de clavier produisant un plantage.</span><span class="sxs-lookup"><span data-stu-id="40af0-193">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="40af0-194">Reproduisez le blocage.</span><span class="sxs-lookup"><span data-stu-id="40af0-194">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="40af0-195">Faites planter le système à l’aide de la séquence de touches définie à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="40af0-195">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="40af0-196">Le système plante et collecte l’image mémoire.</span><span class="sxs-lookup"><span data-stu-id="40af0-196">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="40af0-197">Une fois le système redémarré, envoyez l’image memory.dmp sur secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="40af0-197">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="40af0-198">L’emplacement par défaut du fichier d’image mémoire est %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp si C: est le lecteur système.</span><span class="sxs-lookup"><span data-stu-id="40af0-198">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="40af0-199">Dans l’e-mail, indiquez que le fichier d’image mémoire est destiné à l’équipe WSL ou Bash sur Windows.</span><span class="sxs-lookup"><span data-stu-id="40af0-199">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="40af0-200">Rétablissez le type d’image mémoire d’origine.</span><span class="sxs-lookup"><span data-stu-id="40af0-200">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="40af0-201">Vérifier votre numéro de build</span><span class="sxs-lookup"><span data-stu-id="40af0-201">Check your build number</span></span>

<span data-ttu-id="40af0-202">Pour trouver le numéro de build de Windows et de l’architecture de votre PC, sélectionnez :</span><span class="sxs-lookup"><span data-stu-id="40af0-202">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="40af0-203">**Paramètres** > **Système** > **À propos**</span><span class="sxs-lookup"><span data-stu-id="40af0-203">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="40af0-204">Recherchez les champs **Build du système d’exploitation** et **Type de système**.</span><span class="sxs-lookup"><span data-stu-id="40af0-204">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="40af0-205">Capture d’écran montrant les champs ![Build du système d’exploitation](media/system.png) et Type de système</span><span class="sxs-lookup"><span data-stu-id="40af0-205">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="40af0-206">Pour trouver le numéro de build de Windows Server, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="40af0-206">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="40af0-207">Vérifier que WSL est activé</span><span class="sxs-lookup"><span data-stu-id="40af0-207">Confirm WSL is enabled</span></span>

<span data-ttu-id="40af0-208">Vous pouvez vérifier que le sous-système Windows pour Linux est activé en exécutant la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="40af0-208">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="40af0-209">Problèmes de connexion du serveur OpenSSH</span><span class="sxs-lookup"><span data-stu-id="40af0-209">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="40af0-210">L’erreur suivante se produit lors d’une tentative de connexion du serveur SSH : « Connection closed by 127.0.0.1 port 22 » (Connexion fermée par 127.0.0.1 port 22).</span><span class="sxs-lookup"><span data-stu-id="40af0-210">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="40af0-211">Vérifiez que votre serveur OpenSSH est en cours d’exécution :</span><span class="sxs-lookup"><span data-stu-id="40af0-211">Make sure your OpenSSH Server is running:</span></span>

   ``` BASH
   sudo service ssh status
   ```

   <span data-ttu-id="40af0-212">et veillez à suivre ce tutoriel : https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span><span class="sxs-lookup"><span data-stu-id="40af0-212">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="40af0-213">Arrêtez le service SSHD et démarrez SSHD en mode débogage :</span><span class="sxs-lookup"><span data-stu-id="40af0-213">Stop the sshd service and start sshd in debug mode:</span></span>

   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="40af0-214">Consultez les journaux de démarrage et vérifiez que les clés d’hôte sont disponibles et que les journaux ne contiennent pas de message de ce type :</span><span class="sxs-lookup"><span data-stu-id="40af0-214">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

<span data-ttu-id="40af0-215">Si vous voyez des messages de ce type et que les clés ne sont pas disponibles sous `/etc/ssh/`, vous devrez régénérer les clés ou simplement purger et installer le serveur OpenSSH :</span><span class="sxs-lookup"><span data-stu-id="40af0-215">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="40af0-216">« L’assembly référencé est introuvable. »</span><span class="sxs-lookup"><span data-stu-id="40af0-216">"The referenced assembly could not be found."</span></span> <span data-ttu-id="40af0-217">lors de l’activation de la fonctionnalité facultative WSL</span><span class="sxs-lookup"><span data-stu-id="40af0-217">when enabling the WSL optional feature</span></span>

<span data-ttu-id="40af0-218">Cette erreur est liée à un mauvais état d’installation.</span><span class="sxs-lookup"><span data-stu-id="40af0-218">This error is related to being in a bad install state.</span></span> <span data-ttu-id="40af0-219">Effectuez les étapes suivantes pour essayer de résoudre ce problème :</span><span class="sxs-lookup"><span data-stu-id="40af0-219">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="40af0-220">Si vous exécutez la commande d’activation de la fonctionnalité WSL à partir de PowerShell, essayez d’utiliser l’interface GUI au lieu d’ouvrir le menu Démarrer, recherchez « Activer ou désactiver les fonctionnalités Windows », puis dans la liste, sélectionnez « Sous-système Windows pour Linux » qui installera le composant facultatif.</span><span class="sxs-lookup"><span data-stu-id="40af0-220">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="40af0-221">Mettez à jour votre version de Windows en accédant à Paramètres, Mises à jour, puis en cliquant sur « Rechercher les mises à jour ».</span><span class="sxs-lookup"><span data-stu-id="40af0-221">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="40af0-222">Si les deux échouent et que vous devez accéder à WSL, procédez à une mise à niveau sur place en réinstallant Windows 10 avec un support d’installation et en sélectionnant « Tout conserver » pour vous assurer que vos applications et vos fichiers sont conservés.</span><span class="sxs-lookup"><span data-stu-id="40af0-222">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="40af0-223">Vous trouverez des instructions pour ce faire dans la [page Réinstaller Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="40af0-223">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>
