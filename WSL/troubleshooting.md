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
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Résolution des problèmes liés au sous-système Windows pour Linux

Pour obtenir un support sur les problèmes liés à WSL, consultez notre dépôt GitHub :

## <a name="search-for-any-existing-issues-related-to-your-problem"></a>Rechercher les problèmes existants en rapport avec votre problème

Pour les problèmes techniques, utilisez le dépôt du produit : https://github.com/Microsoft/wsl/issues

Pour les problèmes liés au contenu de cette documentation, utilisez le dépôt de la documentation : https://github.com/MicrosoftDocs/wsl/issues

## <a name="submit-a-bug-report"></a>Envoyer un rapport de bogues

Pour les bogues liés aux fonctions ou fonctionnalités WSL, signalez un problème dans le dépôt du produit : https://github.com/Microsoft/wsl/issues

## <a name="submit-a-feature-request"></a>Envoyer une demande de fonctionnalité

Pour demander une nouvelle fonctionnalité liée au fonctionnement ou à la compatibilité de WSL, signalez un problème dans le dépôt du produit : https://github.com/Microsoft/wsl/issues

## <a name="contribute-to-the-docs"></a>Contribution à la documentation

Pour contribuer à la documentation WSL, envoyez une demande de tirage (pull request) dans le dépôt de la documentation : https://github.com/MicrosoftDocs/wsl/issues

## <a name="terminal-or-command-line"></a>Terminal ou ligne de commande

Enfin, si votre problème est lié au terminal Windows, à la console Windows ou à l’interface utilisateur de ligne de commande, utilisez le dépôt du terminal Windows : https://github.com/microsoft/terminal

## <a name="common-issues"></a>Problèmes courants

### <a name="cannot-access-wsl-files-from-windows"></a>Impossible d’accéder aux fichiers WSL à partir de Windows
Un serveur de fichiers utilisant le protocole 9P fournit le service côté Linux pour permettre à Windows d’accéder au système de fichiers Linux. Si vous ne pouvez pas accéder à WSL en utilisant `\\wsl$` sur Windows, la raison peut en être que 9P n’a pas démarré correctement.

Pour cela, vous pouvez vérifier les journaux de démarrage en utilisant `dmesg |grep 9p` : ceci vous montre les éventuelles erreurs. Une sortie indiquant la réussite se présente comme suit : 

```
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

Pour plus d’informations sur ce problème, consultez [ce thread GitHub](https://github.com/microsoft/wsl/issues/5307).

### <a name="cant-start-wsl-2-distro-and-only-see-wsl-2-in-output"></a>Impossible de démarrer la distribution WSL 2 ; seul « WSL 2 » figure dans la sortie
Si votre langue d’affichage n’est pas l’anglais, il est possible que seule une version tronquée d’un texte d’erreur soit affichée.

```powershell
C:\Users\me>wsl
WSL 2
```

Pour résoudre ce problème, consultez `https://aka.ms/wsl2kernel` et installez le noyau manuellement en suivant les instructions de cette page de la documentation. 

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a>Activez la fonctionnalité Windows Plateforme de machine virtuelle et vérifiez que la virtualisation est activée dans le BIOS.

1. Vérifiez la [configuration système pour Hyper-V](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)
2. Si votre machine est une machine virtuelle, activez manuellement la [virtualisation imbriquée](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine). Lancez PowerShell avec un compte d’administrateur et exécutez : 

```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```

3. Suivez les instructions du fabricant de votre PC pour savoir comment activer la virtualisation. En général, ceci peut impliquer l’utilisation du BIOS du système pour activer ces fonctionnalités sur votre processeur. 
4. Redémarrez votre machine après avoir activé le composant facultatif `Virtual Machine Platform`. 

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash perd la connectivité réseau une fois connecté à un VPN

Si, après une connexion à un VPN sur Windows, Bash perd la connectivité réseau, essayez cette solution de contournement à partir de Bash. Elle vous permet de remplacer la résolution DNS manuellement avec `/etc/resolv.conf`.

1. Exécutez la commande `ipconfig.exe /all` et notez le serveur DNS du VPN.
2. Copiez le fichier resolv.conf existant avec `sudo cp /etc/resolv.conf /etc/resolv.conf.new`.
3. Dissociez le fichier resolv.conf actuel avec `sudo unlink /etc/resolv.conf`.
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Ouvrez `/etc/resolv.conf` et <br/>
   a. Supprimez la première ligne du fichier, comportant le message « \# This file was automatically generated by WSL. To stop automatic generation of this file, remove this line. » (Ce fichier a été généré automatiquement par WSL. Pour arrêter la génération automatique de ce fichier, supprimez cette ligne. »). <br/>
   b. Ajoutez l’entrée DNS notée à l’étape 1 précédente comme première entrée de la liste des serveurs DNS. <br/>
   c. Fermez le fichier. <br/>

Une fois que vous avez déconnecté le VPN, vous devez revenir au fichier `/etc/resolv.conf` non modifié. Pour ce faire, exécutez les commandes suivantes :

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Le démarrage de WSL ou l’installation d’une distribution retourne un code d’erreur.

Suivez [ces instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) pour récupérer des journaux détaillés et signaler un problème sur notre plateforme GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Mise à jour de Bash sur Ubuntu sur Windows

Deux composants de Bash sur Ubuntu sur Windows peuvent nécessiter une mise à jour.

1. Sous-système Windows pour Linux
  
   La mise à niveau de cette partie de Bash sur Ubuntu sur Windows active tous les nouveaux correctifs mentionnés dans les [notes de publication](./release-notes.md). Vérifiez que vous êtes abonné au programme Windows Insider et que votre build est à jour. Pour un contrôle plus précis et, notamment, pour réinitialiser votre instance Ubuntu, consultez les [informations de référence sur les commandes](./reference.md).

2. Fichiers binaires utilisateur Ubuntu

   La mise à niveau de cette partie de Bash sur Ubuntu sur Windows installe toutes les mises à jour des fichiers binaires utilisateur Ubuntu, y compris les applications que vous avez installées avec apt-get. Pour procéder à la mise à jour, exécutez les commandes suivantes dans Bash :
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Erreurs avec apt-get upgrade

Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées. `udev`, par exemple, n’est pas encore pris en charge et provoque plusieurs erreurs avec `apt-get upgrade`.

Pour résoudre les problèmes liés à `udev`, procédez comme suit :

1. Écrivez le code suivant dans `/usr/sbin/policy-rc.d` et enregistrez vos modifications.
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. Ajoutez des autorisations d’exécution à `/usr/sbin/policy-rc.d` :

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Exécutez les commandes suivantes :

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>« Error : 0x80040306 » lors de l’installation

Cette erreur est due au fait que nous ne prenons pas en charge la console héritée.
Pour désactiver la console héritée :

1. Ouvrez cmd.exe.
1. Cliquez avec le bouton droit sur la barre de titre, sélectionnez Propriétés, puis désactivez la case Utiliser la console héritée.
1. Cliquez sur OK

### <a name="error-0x80040154-after-windows-update"></a>« Error : 0x80040154 » après une mise à jour de Windows

La fonctionnalité de sous-système Windows pour Linux peut être désactivée au cours d’une mise à jour de Windows. Dans ce cas, la fonctionnalité Windows doit être réactivée. Pour obtenir des instructions sur l’activation du sous-système Windows pour Linux, consultez le [guide d’installation](./install-win10.md).

### <a name="changing-the-display-language"></a>Changement de la langue d’affichage

Le processus d’installation de WSL tente de changer automatiquement les paramètres régionaux d’Ubuntu de sorte qu’ils correspondent à ceux de votre installation Windows.  Si vous souhaitez éviter ce comportement, vous pouvez exécuter cette commande pour changer les paramètres régionaux d’Ubuntu une fois l’installation terminée.  Vous devrez relancer bash.exe pour que ce changement prenne effet.

L’exemple ci-dessous applique les paramètres régionaux en-US :

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problèmes d’installation après une restauration du système Windows

1. Supprimez le dossier `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`. <br/>
  **Remarque : N’effectuez pas cette opération si votre fonctionnalité facultative est entièrement installée et opérationnelle.**
2. Si ce n’est déjà fait, activez la fonctionnalité facultative WSL.
3. Redémarrer
4. lxrun /uninstall /full
5. Installez Bash.

### <a name="no-internet-access-in-wsl"></a>Aucun accès Internet dans WSL

Certains utilisateurs ont signalé des problèmes posés par certaines applications de pare-feu, qui bloquent l’accès Internet dans WSL.  Les pare-feux signalés sont :

1. Kaspersky
2. AVG
3. Avast

Dans certains cas, la désactivation du pare-feu permet d’obtenir l’accès.  Parfois, il semble que la simple installation du pare-feu bloque l’accès.

### <a name="permission-denied-error-when-using-ping"></a>Autorisation refusée lors de l’utilisation d’une commande ping

Pour la [Mise à jour anniversaire Windows, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), les **privilèges administrateur** dans Windows doivent exécuter la commande ping dans WSL.  Pour exécuter une commande ping, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite de commandes/PowerShell avec des privilèges d’administrateur.

Pour les versions ultérieures de Windows, [Build 14926+](./release-notes.md#build-14926), les privilèges administrateur ne sont plus nécessaires.

### <a name="bash-is-hung"></a>Bash est bloqué.

Si, alors que vous utilisez Bash, celui-ci se bloque et ne répond pas aux entrées, aidez-nous à diagnostiquer le problème en collectant une image mémoire et en nous la communiquant. Notez que la procédure ci-après entraînera le plantage de votre système. Suivez-la uniquement si vous êtes à l’aise avec ce type d’opération, ou enregistrez votre travail au préalable.

Pour collecter une image mémoire

1. Changez le type d’image mémoire en choisissant « Image mémoire complète ». Lors de ce changement, prenez note du type d’image actuel.

2. Suivez [cette procédure](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) pour configurer une commande de clavier produisant un plantage.

3. Reproduisez le blocage.

4. Faites planter le système à l’aide de la séquence de touches définie à l’étape 2.

5. Le système plante et collecte l’image mémoire.

6. Une fois le système redémarré, envoyez l’image memory.dmp sur secure@microsoft.com. L’emplacement par défaut du fichier d’image mémoire est %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp si C: est le lecteur système. Dans l’e-mail, indiquez que le fichier d’image mémoire est destiné à l’équipe WSL ou Bash sur Windows.

7. Rétablissez le type d’image mémoire d’origine.

### <a name="check-your-build-number"></a>Vérifier votre numéro de build

Pour trouver le numéro de build de Windows et de l’architecture de votre PC, sélectionnez :  
**Paramètres** > **Système** > **À propos**

Recherchez les champs **Build du système d’exploitation** et **Type de système**.  
    Capture d’écran montrant les champs ![Build du système d’exploitation](media/system.png) et Type de système

Pour trouver le numéro de build de Windows Server, exécutez la commande suivante dans PowerShell :  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Vérifier que WSL est activé

Vous pouvez vérifier que le sous-système Windows pour Linux est activé en exécutant la commande suivante dans PowerShell :  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Problèmes de connexion du serveur OpenSSH

L’erreur suivante se produit lors d’une tentative de connexion du serveur SSH : « Connection closed by 127.0.0.1 port 22 » (Connexion fermée par 127.0.0.1 port 22).

1. Vérifiez que votre serveur OpenSSH est en cours d’exécution :

   ```bash
   sudo service ssh status
   ```

   et veillez à suivre ce tutoriel : https://help.ubuntu.com/lts/serverguide/openssh-server.html.en

2. Arrêtez le service SSHD et démarrez SSHD en mode débogage :

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. Consultez les journaux de démarrage et vérifiez que les clés d’hôte sont disponibles et que les journaux ne contiennent pas de message de ce type :

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

Si vous voyez des messages de ce type et que les clés ne sont pas disponibles sous `/etc/ssh/`, vous devrez régénérer les clés ou simplement purger et installer le serveur OpenSSH :

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a>« L’assembly référencé est introuvable. » lors de l’activation de la fonctionnalité facultative WSL

Cette erreur est liée à un mauvais état d’installation. Effectuez les étapes suivantes pour essayer de résoudre ce problème :

- Si vous exécutez la commande d’activation de la fonctionnalité WSL à partir de PowerShell, essayez d’utiliser l’interface GUI au lieu d’ouvrir le menu Démarrer, recherchez « Activer ou désactiver les fonctionnalités Windows », puis dans la liste, sélectionnez « Sous-système Windows pour Linux » qui installera le composant facultatif.

- Mettez à jour votre version de Windows en accédant à Paramètres, Mises à jour, puis en cliquant sur « Rechercher les mises à jour ».

- Si les deux échouent et que vous devez accéder à WSL, procédez à une mise à niveau sur place en réinstallant Windows 10 avec un support d’installation et en sélectionnant « Tout conserver » pour vous assurer que vos applications et vos fichiers sont conservés. Vous trouverez des instructions pour ce faire dans la [page Réinstaller Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).

### <a name="correct-ssh-related-permission-errors"></a>Erreurs d’autorisations correctes (liées à SSH)

Si vous voyez cette erreur :

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

Pour la corriger, ajoutez ce qui suit au fichier ```/etc/wsl.conf``` :

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

Veuillez noter que l’ajout de cette commande inclura les métadonnées et modifiera les autorisations sur les fichiers Windows vus depuis WSL. Pour plus d’informations, consultez [Autorisations de système de fichier](./file-permissions.md).
