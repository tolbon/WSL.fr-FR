---
title: Résolution des problèmes du sous-système Windows pour Linux
description: Cet article fournit des informations détaillées sur les erreurs et problèmes courants auxquels peuvent être confrontés les utilisateurs exécutant Linux sur le sous-système Windows pour Linux.
keywords: BashOnWindows, Bash, WSL, Windows, sous-système Windows, Ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: cc8f032a99fb087b7ef614dd3a3574cb8ee3f2da
ms.sourcegitcommit: ba52d673c123fe8ae61e872a33e218cfc30a1f82
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033058"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="1f58c-104">Résolution des problèmes liés au sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="1f58c-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="1f58c-105">Pour obtenir un support sur les problèmes liés à WSL, consultez notre dépôt GitHub :</span><span class="sxs-lookup"><span data-stu-id="1f58c-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="1f58c-106">Rechercher les problèmes existants en rapport avec votre problème</span><span class="sxs-lookup"><span data-stu-id="1f58c-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="1f58c-107">Pour les problèmes techniques, utilisez le dépôt du produit : https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="1f58c-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="1f58c-108">Pour les problèmes liés au contenu de cette documentation, utilisez le dépôt de la documentation : https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="1f58c-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="1f58c-109">Envoyer un rapport de bogues</span><span class="sxs-lookup"><span data-stu-id="1f58c-109">Submit a bug report</span></span>

<span data-ttu-id="1f58c-110">Pour les bogues liés aux fonctions ou fonctionnalités WSL, signalez un problème dans le dépôt du produit : https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="1f58c-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="1f58c-111">Envoyer une demande de fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="1f58c-111">Submit a feature request</span></span>

<span data-ttu-id="1f58c-112">Pour demander une nouvelle fonctionnalité liée au fonctionnement ou à la compatibilité de WSL, signalez un problème dans le dépôt du produit : https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="1f58c-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="1f58c-113">Contribution à la documentation</span><span class="sxs-lookup"><span data-stu-id="1f58c-113">Contribute to the docs</span></span>

<span data-ttu-id="1f58c-114">Pour contribuer à la documentation WSL, envoyez une demande de tirage (pull request) dans le dépôt de la documentation : https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="1f58c-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="1f58c-115">Terminal ou ligne de commande</span><span class="sxs-lookup"><span data-stu-id="1f58c-115">Terminal or Command Line</span></span>

<span data-ttu-id="1f58c-116">Enfin, si votre problème est lié au terminal Windows, à la console Windows ou à l’interface utilisateur de ligne de commande, utilisez le dépôt du terminal Windows : https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="1f58c-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="1f58c-117">Problèmes courants</span><span class="sxs-lookup"><span data-stu-id="1f58c-117">Common issues</span></span>

### <a name="cannot-access-wsl-files-from-windows"></a><span data-ttu-id="1f58c-118">Impossible d’accéder aux fichiers WSL à partir de Windows</span><span class="sxs-lookup"><span data-stu-id="1f58c-118">Cannot access WSL files from Windows</span></span>
<span data-ttu-id="1f58c-119">Un serveur de fichiers utilisant le protocole 9P fournit le service côté Linux pour permettre à Windows d’accéder au système de fichiers Linux.</span><span class="sxs-lookup"><span data-stu-id="1f58c-119">A 9p protocol file server provides the service on the Linux side to allow Windows to access the Linux file system.</span></span> <span data-ttu-id="1f58c-120">Si vous ne pouvez pas accéder à WSL en utilisant `\\wsl$` sur Windows, la raison peut en être que 9P n’a pas démarré correctement.</span><span class="sxs-lookup"><span data-stu-id="1f58c-120">If you cannot access WSL using `\\wsl$` on Windows, it could be because 9P did not start correctly.</span></span>

<span data-ttu-id="1f58c-121">Pour cela, vous pouvez vérifier les journaux de démarrage en utilisant `dmesg |grep 9p` : ceci vous montre les éventuelles erreurs.</span><span class="sxs-lookup"><span data-stu-id="1f58c-121">To check this, you can check the start up logs using: `dmesg |grep 9p`, and this will show you any errors.</span></span> <span data-ttu-id="1f58c-122">Une sortie indiquant la réussite se présente comme suit :</span><span class="sxs-lookup"><span data-stu-id="1f58c-122">A successfull output looks like the following:</span></span> 

```
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

<span data-ttu-id="1f58c-123">Pour plus d’informations sur ce problème, consultez [ce thread GitHub](https://github.com/microsoft/wsl/issues/5307).</span><span class="sxs-lookup"><span data-stu-id="1f58c-123">Please see [this Github thread](https://github.com/microsoft/wsl/issues/5307) for further discussion on this issue.</span></span>

### <a name="cant-start-wsl-2-distro-and-only-see-wsl-2-in-output"></a><span data-ttu-id="1f58c-124">Impossible de démarrer la distribution WSL 2 ; seul « WSL 2 » figure dans la sortie</span><span class="sxs-lookup"><span data-stu-id="1f58c-124">Can't start WSL 2 distro and only see 'WSL 2' in output</span></span>
<span data-ttu-id="1f58c-125">Si votre langue d’affichage n’est pas l’anglais, il est possible que seule une version tronquée d’un texte d’erreur soit affichée.</span><span class="sxs-lookup"><span data-stu-id="1f58c-125">If your display language is not English, then it is possible you are seeing a truncated version of an error text.</span></span>

```powershell
C:\Users\me>wsl
WSL 2
```

<span data-ttu-id="1f58c-126">Pour résoudre ce problème, consultez `https://aka.ms/wsl2kernel` et installez le noyau manuellement en suivant les instructions de cette page de la documentation.</span><span class="sxs-lookup"><span data-stu-id="1f58c-126">To resolve this issue, please visit `https://aka.ms/wsl2kernel` and install the kernel manually by following the directions on that doc page.</span></span> 

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a><span data-ttu-id="1f58c-127">Activez la fonctionnalité Windows Plateforme de machine virtuelle et vérifiez que la virtualisation est activée dans le BIOS.</span><span class="sxs-lookup"><span data-stu-id="1f58c-127">Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</span></span>

1. <span data-ttu-id="1f58c-128">Vérifiez la [configuration système pour Hyper-V](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span><span class="sxs-lookup"><span data-stu-id="1f58c-128">Check the [Hyper-V system requirements](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span></span>
2. <span data-ttu-id="1f58c-129">Si votre machine est une machine virtuelle, activez manuellement la [virtualisation imbriquée](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine).</span><span class="sxs-lookup"><span data-stu-id="1f58c-129">If your machine is a VM, please enable [nested virtualization](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manually.</span></span> <span data-ttu-id="1f58c-130">Lancez PowerShell avec un compte d’administrateur et exécutez :</span><span class="sxs-lookup"><span data-stu-id="1f58c-130">Launch powershell with admin, and run:</span></span> 

```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```

3. <span data-ttu-id="1f58c-131">Suivez les instructions du fabricant de votre PC pour savoir comment activer la virtualisation.</span><span class="sxs-lookup"><span data-stu-id="1f58c-131">Please follow guidelines from your PC's manufacturer on how to enable virtualization.</span></span> <span data-ttu-id="1f58c-132">En général, ceci peut impliquer l’utilisation du BIOS du système pour activer ces fonctionnalités sur votre processeur.</span><span class="sxs-lookup"><span data-stu-id="1f58c-132">In general, this can involve using the system BIOS to ensure that these features are enabled on your CPU.</span></span> 
4. <span data-ttu-id="1f58c-133">Redémarrez votre machine après avoir activé le composant facultatif `Virtual Machine Platform`.</span><span class="sxs-lookup"><span data-stu-id="1f58c-133">Restart your machine after enabling the `Virtual Machine Platform` optional component.</span></span> 

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="1f58c-134">Bash perd la connectivité réseau une fois connecté à un VPN</span><span class="sxs-lookup"><span data-stu-id="1f58c-134">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="1f58c-135">Si, après une connexion à un VPN sur Windows, Bash perd la connectivité réseau, essayez cette solution de contournement à partir de Bash.</span><span class="sxs-lookup"><span data-stu-id="1f58c-135">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="1f58c-136">Elle vous permet de remplacer la résolution DNS manuellement avec `/etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="1f58c-136">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="1f58c-137">Exécutez la commande `ipconfig.exe /all` et notez le serveur DNS du VPN.</span><span class="sxs-lookup"><span data-stu-id="1f58c-137">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="1f58c-138">Copiez le fichier resolv.conf existant avec `sudo cp /etc/resolv.conf /etc/resolv.conf.new`.</span><span class="sxs-lookup"><span data-stu-id="1f58c-138">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="1f58c-139">Dissociez le fichier resolv.conf actuel avec `sudo unlink /etc/resolv.conf`.</span><span class="sxs-lookup"><span data-stu-id="1f58c-139">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="1f58c-140">Ouvrez `/etc/resolv.conf` et</span><span class="sxs-lookup"><span data-stu-id="1f58c-140">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="1f58c-141">a.</span><span class="sxs-lookup"><span data-stu-id="1f58c-141">a.</span></span> <span data-ttu-id="1f58c-142">Supprimez la première ligne du fichier, comportant le message « \# This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="1f58c-142">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="1f58c-143">To stop automatic generation of this file, remove this line. » (Ce fichier a été généré automatiquement par WSL. Pour arrêter la génération automatique de ce fichier, supprimez cette ligne. »).</span><span class="sxs-lookup"><span data-stu-id="1f58c-143">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="1f58c-144">b.</span><span class="sxs-lookup"><span data-stu-id="1f58c-144">b.</span></span> <span data-ttu-id="1f58c-145">Ajoutez l’entrée DNS notée à l’étape 1 précédente comme première entrée de la liste des serveurs DNS.</span><span class="sxs-lookup"><span data-stu-id="1f58c-145">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="1f58c-146">c.</span><span class="sxs-lookup"><span data-stu-id="1f58c-146">c.</span></span> <span data-ttu-id="1f58c-147">Fermez le fichier.</span><span class="sxs-lookup"><span data-stu-id="1f58c-147">Close the file.</span></span> <br/>

<span data-ttu-id="1f58c-148">Une fois que vous avez déconnecté le VPN, vous devez revenir au fichier `/etc/resolv.conf` non modifié.</span><span class="sxs-lookup"><span data-stu-id="1f58c-148">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="1f58c-149">Pour ce faire, exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f58c-149">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="1f58c-150">Le démarrage de WSL ou l’installation d’une distribution retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="1f58c-150">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="1f58c-151">Suivez [ces instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) pour récupérer des journaux détaillés et signaler un problème sur notre plateforme GitHub.</span><span class="sxs-lookup"><span data-stu-id="1f58c-151">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="1f58c-152">Mise à jour de Bash sur Ubuntu sur Windows</span><span class="sxs-lookup"><span data-stu-id="1f58c-152">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="1f58c-153">Deux composants de Bash sur Ubuntu sur Windows peuvent nécessiter une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="1f58c-153">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="1f58c-154">Sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="1f58c-154">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="1f58c-155">La mise à niveau de cette partie de Bash sur Ubuntu sur Windows active tous les nouveaux correctifs mentionnés dans les [notes de publication](./release-notes.md).</span><span class="sxs-lookup"><span data-stu-id="1f58c-155">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="1f58c-156">Vérifiez que vous êtes abonné au programme Windows Insider et que votre build est à jour.</span><span class="sxs-lookup"><span data-stu-id="1f58c-156">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="1f58c-157">Pour un contrôle plus précis et, notamment, pour réinitialiser votre instance Ubuntu, consultez les [informations de référence sur les commandes](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="1f58c-157">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="1f58c-158">Fichiers binaires utilisateur Ubuntu</span><span class="sxs-lookup"><span data-stu-id="1f58c-158">The Ubuntu user binaries</span></span>

   <span data-ttu-id="1f58c-159">La mise à niveau de cette partie de Bash sur Ubuntu sur Windows installe toutes les mises à jour des fichiers binaires utilisateur Ubuntu, y compris les applications que vous avez installées avec apt-get.</span><span class="sxs-lookup"><span data-stu-id="1f58c-159">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="1f58c-160">Pour procéder à la mise à jour, exécutez les commandes suivantes dans Bash :</span><span class="sxs-lookup"><span data-stu-id="1f58c-160">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="1f58c-161">Erreurs avec apt-get upgrade</span><span class="sxs-lookup"><span data-stu-id="1f58c-161">Apt-get upgrade errors</span></span>

<span data-ttu-id="1f58c-162">Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées.</span><span class="sxs-lookup"><span data-stu-id="1f58c-162">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="1f58c-163">`udev`, par exemple, n’est pas encore pris en charge et provoque plusieurs erreurs avec `apt-get upgrade`.</span><span class="sxs-lookup"><span data-stu-id="1f58c-163">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="1f58c-164">Pour résoudre les problèmes liés à `udev`, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="1f58c-164">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="1f58c-165">Écrivez le code suivant dans `/usr/sbin/policy-rc.d` et enregistrez vos modifications.</span><span class="sxs-lookup"><span data-stu-id="1f58c-165">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="1f58c-166">Ajoutez des autorisations d’exécution à `/usr/sbin/policy-rc.d` :</span><span class="sxs-lookup"><span data-stu-id="1f58c-166">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="1f58c-167">Exécutez les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f58c-167">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="1f58c-168">« Error : 0x80040306 » lors de l’installation</span><span class="sxs-lookup"><span data-stu-id="1f58c-168">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="1f58c-169">Cette erreur est due au fait que nous ne prenons pas en charge la console héritée.</span><span class="sxs-lookup"><span data-stu-id="1f58c-169">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="1f58c-170">Pour désactiver la console héritée :</span><span class="sxs-lookup"><span data-stu-id="1f58c-170">To turn off legacy console:</span></span>

1. <span data-ttu-id="1f58c-171">Ouvrez cmd.exe.</span><span class="sxs-lookup"><span data-stu-id="1f58c-171">Open cmd.exe</span></span>
1. <span data-ttu-id="1f58c-172">Cliquez avec le bouton droit sur la barre de titre, sélectionnez Propriétés, puis désactivez la case Utiliser la console héritée.</span><span class="sxs-lookup"><span data-stu-id="1f58c-172">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="1f58c-173">Cliquez sur OK</span><span class="sxs-lookup"><span data-stu-id="1f58c-173">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="1f58c-174">« Error : 0x80040154 » après une mise à jour de Windows</span><span class="sxs-lookup"><span data-stu-id="1f58c-174">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="1f58c-175">La fonctionnalité de sous-système Windows pour Linux peut être désactivée au cours d’une mise à jour de Windows.</span><span class="sxs-lookup"><span data-stu-id="1f58c-175">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="1f58c-176">Dans ce cas, la fonctionnalité Windows doit être réactivée.</span><span class="sxs-lookup"><span data-stu-id="1f58c-176">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="1f58c-177">Pour obtenir des instructions sur l’activation du sous-système Windows pour Linux, consultez le [guide d’installation](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="1f58c-177">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="1f58c-178">Changement de la langue d’affichage</span><span class="sxs-lookup"><span data-stu-id="1f58c-178">Changing the display language</span></span>

<span data-ttu-id="1f58c-179">Le processus d’installation de WSL tente de changer automatiquement les paramètres régionaux d’Ubuntu de sorte qu’ils correspondent à ceux de votre installation Windows.</span><span class="sxs-lookup"><span data-stu-id="1f58c-179">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="1f58c-180">Si vous souhaitez éviter ce comportement, vous pouvez exécuter cette commande pour changer les paramètres régionaux d’Ubuntu une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="1f58c-180">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="1f58c-181">Vous devrez relancer bash.exe pour que ce changement prenne effet.</span><span class="sxs-lookup"><span data-stu-id="1f58c-181">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="1f58c-182">L’exemple ci-dessous applique les paramètres régionaux en-US :</span><span class="sxs-lookup"><span data-stu-id="1f58c-182">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="1f58c-183">Problèmes d’installation après une restauration du système Windows</span><span class="sxs-lookup"><span data-stu-id="1f58c-183">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="1f58c-184">Supprimez le dossier `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="1f58c-184">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="1f58c-185">**Remarque : N’effectuez pas cette opération si votre fonctionnalité facultative est entièrement installée et opérationnelle.**</span><span class="sxs-lookup"><span data-stu-id="1f58c-185">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="1f58c-186">Si ce n’est déjà fait, activez la fonctionnalité facultative WSL.</span><span class="sxs-lookup"><span data-stu-id="1f58c-186">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="1f58c-187">Redémarrer</span><span class="sxs-lookup"><span data-stu-id="1f58c-187">Reboot</span></span>
4. <span data-ttu-id="1f58c-188">lxrun /uninstall /full</span><span class="sxs-lookup"><span data-stu-id="1f58c-188">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="1f58c-189">Installez Bash.</span><span class="sxs-lookup"><span data-stu-id="1f58c-189">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="1f58c-190">Aucun accès Internet dans WSL</span><span class="sxs-lookup"><span data-stu-id="1f58c-190">No internet access in WSL</span></span>

<span data-ttu-id="1f58c-191">Certains utilisateurs ont signalé des problèmes posés par certaines applications de pare-feu, qui bloquent l’accès Internet dans WSL.</span><span class="sxs-lookup"><span data-stu-id="1f58c-191">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="1f58c-192">Les pare-feux signalés sont :</span><span class="sxs-lookup"><span data-stu-id="1f58c-192">The firewalls reported are:</span></span>

1. <span data-ttu-id="1f58c-193">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="1f58c-193">Kaspersky</span></span>
2. <span data-ttu-id="1f58c-194">AVG</span><span class="sxs-lookup"><span data-stu-id="1f58c-194">AVG</span></span>
3. <span data-ttu-id="1f58c-195">Avast</span><span class="sxs-lookup"><span data-stu-id="1f58c-195">Avast</span></span>

<span data-ttu-id="1f58c-196">Dans certains cas, la désactivation du pare-feu permet d’obtenir l’accès.</span><span class="sxs-lookup"><span data-stu-id="1f58c-196">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="1f58c-197">Parfois, il semble que la simple installation du pare-feu bloque l’accès.</span><span class="sxs-lookup"><span data-stu-id="1f58c-197">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="1f58c-198">Autorisation refusée lors de l’utilisation d’une commande ping</span><span class="sxs-lookup"><span data-stu-id="1f58c-198">Permission Denied error when using ping</span></span>

<span data-ttu-id="1f58c-199">Pour la [Mise à jour anniversaire Windows, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), les **privilèges administrateur** dans Windows doivent exécuter la commande ping dans WSL.</span><span class="sxs-lookup"><span data-stu-id="1f58c-199">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="1f58c-200">Pour exécuter une commande ping, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite de commandes/PowerShell avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="1f58c-200">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="1f58c-201">Pour les versions ultérieures de Windows, [Build 14926+](./release-notes.md#build-14926), les privilèges administrateur ne sont plus nécessaires.</span><span class="sxs-lookup"><span data-stu-id="1f58c-201">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="1f58c-202">Bash est bloqué.</span><span class="sxs-lookup"><span data-stu-id="1f58c-202">Bash is hung</span></span>

<span data-ttu-id="1f58c-203">Si, alors que vous utilisez Bash, celui-ci se bloque et ne répond pas aux entrées, aidez-nous à diagnostiquer le problème en collectant une image mémoire et en nous la communiquant.</span><span class="sxs-lookup"><span data-stu-id="1f58c-203">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="1f58c-204">Notez que la procédure ci-après entraînera le plantage de votre système.</span><span class="sxs-lookup"><span data-stu-id="1f58c-204">Note that these steps will crash your system.</span></span> <span data-ttu-id="1f58c-205">Suivez-la uniquement si vous êtes à l’aise avec ce type d’opération, ou enregistrez votre travail au préalable.</span><span class="sxs-lookup"><span data-stu-id="1f58c-205">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="1f58c-206">Pour collecter une image mémoire</span><span class="sxs-lookup"><span data-stu-id="1f58c-206">To collect a memory dump</span></span>

1. <span data-ttu-id="1f58c-207">Changez le type d’image mémoire en choisissant « Image mémoire complète ».</span><span class="sxs-lookup"><span data-stu-id="1f58c-207">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="1f58c-208">Lors de ce changement, prenez note du type d’image actuel.</span><span class="sxs-lookup"><span data-stu-id="1f58c-208">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="1f58c-209">Suivez [cette procédure](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) pour configurer une commande de clavier produisant un plantage.</span><span class="sxs-lookup"><span data-stu-id="1f58c-209">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="1f58c-210">Reproduisez le blocage.</span><span class="sxs-lookup"><span data-stu-id="1f58c-210">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="1f58c-211">Faites planter le système à l’aide de la séquence de touches définie à l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="1f58c-211">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="1f58c-212">Le système plante et collecte l’image mémoire.</span><span class="sxs-lookup"><span data-stu-id="1f58c-212">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="1f58c-213">Une fois le système redémarré, envoyez l’image memory.dmp sur secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="1f58c-213">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="1f58c-214">L’emplacement par défaut du fichier d’image mémoire est %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp si C: est le lecteur système.</span><span class="sxs-lookup"><span data-stu-id="1f58c-214">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="1f58c-215">Dans l’e-mail, indiquez que le fichier d’image mémoire est destiné à l’équipe WSL ou Bash sur Windows.</span><span class="sxs-lookup"><span data-stu-id="1f58c-215">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="1f58c-216">Rétablissez le type d’image mémoire d’origine.</span><span class="sxs-lookup"><span data-stu-id="1f58c-216">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="1f58c-217">Vérifier votre numéro de build</span><span class="sxs-lookup"><span data-stu-id="1f58c-217">Check your build number</span></span>

<span data-ttu-id="1f58c-218">Pour trouver le numéro de build de Windows et de l’architecture de votre PC, sélectionnez :</span><span class="sxs-lookup"><span data-stu-id="1f58c-218">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="1f58c-219">**Paramètres** > **Système** > **À propos**</span><span class="sxs-lookup"><span data-stu-id="1f58c-219">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="1f58c-220">Recherchez les champs **Build du système d’exploitation** et **Type de système**.</span><span class="sxs-lookup"><span data-stu-id="1f58c-220">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="1f58c-221">Capture d’écran montrant les champs ![Build du système d’exploitation](media/system.png) et Type de système</span><span class="sxs-lookup"><span data-stu-id="1f58c-221">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="1f58c-222">Pour trouver le numéro de build de Windows Server, exécutez la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1f58c-222">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="1f58c-223">Vérifier que WSL est activé</span><span class="sxs-lookup"><span data-stu-id="1f58c-223">Confirm WSL is enabled</span></span>

<span data-ttu-id="1f58c-224">Vous pouvez vérifier que le sous-système Windows pour Linux est activé en exécutant la commande suivante dans PowerShell :</span><span class="sxs-lookup"><span data-stu-id="1f58c-224">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="1f58c-225">Problèmes de connexion du serveur OpenSSH</span><span class="sxs-lookup"><span data-stu-id="1f58c-225">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="1f58c-226">L’erreur suivante se produit lors d’une tentative de connexion du serveur SSH : « Connection closed by 127.0.0.1 port 22 » (Connexion fermée par 127.0.0.1 port 22).</span><span class="sxs-lookup"><span data-stu-id="1f58c-226">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="1f58c-227">Vérifiez que votre serveur OpenSSH est en cours d’exécution :</span><span class="sxs-lookup"><span data-stu-id="1f58c-227">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="1f58c-228">et veillez à suivre ce tutoriel : https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span><span class="sxs-lookup"><span data-stu-id="1f58c-228">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="1f58c-229">Arrêtez le service SSHD et démarrez SSHD en mode débogage :</span><span class="sxs-lookup"><span data-stu-id="1f58c-229">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="1f58c-230">Consultez les journaux de démarrage et vérifiez que les clés d’hôte sont disponibles et que les journaux ne contiennent pas de message de ce type :</span><span class="sxs-lookup"><span data-stu-id="1f58c-230">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

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

<span data-ttu-id="1f58c-231">Si vous voyez des messages de ce type et que les clés ne sont pas disponibles sous `/etc/ssh/`, vous devrez régénérer les clés ou simplement purger et installer le serveur OpenSSH :</span><span class="sxs-lookup"><span data-stu-id="1f58c-231">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="1f58c-232">« L’assembly référencé est introuvable. »</span><span class="sxs-lookup"><span data-stu-id="1f58c-232">"The referenced assembly could not be found."</span></span> <span data-ttu-id="1f58c-233">lors de l’activation de la fonctionnalité facultative WSL</span><span class="sxs-lookup"><span data-stu-id="1f58c-233">when enabling the WSL optional feature</span></span>

<span data-ttu-id="1f58c-234">Cette erreur est liée à un mauvais état d’installation.</span><span class="sxs-lookup"><span data-stu-id="1f58c-234">This error is related to being in a bad install state.</span></span> <span data-ttu-id="1f58c-235">Effectuez les étapes suivantes pour essayer de résoudre ce problème :</span><span class="sxs-lookup"><span data-stu-id="1f58c-235">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="1f58c-236">Si vous exécutez la commande d’activation de la fonctionnalité WSL à partir de PowerShell, essayez d’utiliser l’interface GUI au lieu d’ouvrir le menu Démarrer, recherchez « Activer ou désactiver les fonctionnalités Windows », puis dans la liste, sélectionnez « Sous-système Windows pour Linux » qui installera le composant facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f58c-236">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="1f58c-237">Mettez à jour votre version de Windows en accédant à Paramètres, Mises à jour, puis en cliquant sur « Rechercher les mises à jour ».</span><span class="sxs-lookup"><span data-stu-id="1f58c-237">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="1f58c-238">Si les deux échouent et que vous devez accéder à WSL, procédez à une mise à niveau sur place en réinstallant Windows 10 avec un support d’installation et en sélectionnant « Tout conserver » pour vous assurer que vos applications et vos fichiers sont conservés.</span><span class="sxs-lookup"><span data-stu-id="1f58c-238">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="1f58c-239">Vous trouverez des instructions pour ce faire dans la [page Réinstaller Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="1f58c-239">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="1f58c-240">Erreurs d’autorisations correctes (liées à SSH)</span><span class="sxs-lookup"><span data-stu-id="1f58c-240">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="1f58c-241">Si vous voyez cette erreur :</span><span class="sxs-lookup"><span data-stu-id="1f58c-241">If you're seeing this error:</span></span>

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="1f58c-242">Pour la corriger, ajoutez ce qui suit au fichier ```/etc/wsl.conf``` :</span><span class="sxs-lookup"><span data-stu-id="1f58c-242">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="1f58c-243">Veuillez noter que l’ajout de cette commande inclura les métadonnées et modifiera les autorisations sur les fichiers Windows vus depuis WSL.</span><span class="sxs-lookup"><span data-stu-id="1f58c-243">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="1f58c-244">Pour plus d’informations, consultez [Autorisations de système de fichier](./file-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="1f58c-244">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>
