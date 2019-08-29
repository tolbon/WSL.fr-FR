---
title: Résolution des problèmes liés au sous-système Windows pour Linux
description: Fournit des informations détaillées sur les erreurs courantes et les problèmes rencontrés lors de l’exécution de Linux sur le sous-système Windows pour Linux.
keywords: BashOnWindows, bash, WSL, Windows, windowssubsystem, Ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6a5fec8b8e054b4d3399ee9bcd903acebca7aace
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122692"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Résolution des problèmes du sous-système Windows pour Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash perd la connectivité réseau une fois connecté à un VPN

Si, après vous être connecté à un VPN sur Windows, bash perd la connectivité réseau, essayez cette solution de contournement dans bash. Cette solution de contournement vous permet de remplacer manuellement la résolution DNS par `/etc/resolv.conf`le biais de.

1. Prenez note du serveur DNS du VPN`ipconfig.exe /all`
2. Effectuer une copie du resolv. conf existant`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Dissocier le resolv. con actuel`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Ouvrez `/etc/resolv.conf` et <br/>
   a. Supprimez la première ligne du fichier, qui indique «\# ce fichier a été généré automatiquement par WSL. Pour arrêter la génération automatique de ce fichier, supprimez cette ligne.». <br/>
   b. Ajoutez l’entrée DNS de (1) au-dessus de la toute première entrée de la liste des serveurs DNS. <br/>
   c. Fermez le fichier. <br/>

Une fois que vous avez déconnecté le VPN, vous devez annuler les modifications apportées à `/etc/resolv.conf`. Pour ce faire, procédez comme suit:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Le démarrage de WSL ou l’installation d’une distribution retourne un code d’erreur

Suivez [ces instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) pour collecter des journaux détaillés et générer un problème sur notre github.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Mise à jour de bash sur Ubuntu sur Windows

Il existe deux composants de bash sur Ubuntu sur Windows qui peuvent nécessiter une mise à jour. 

1. Sous-système Windows pour Linux
  
   La mise à niveau de cette partie de bash sur Ubuntu sur Windows activera tous les nouveaux correctifs dans les [notes de publication](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Vérifiez que vous êtes abonné au programme Windows Insider et que votre Build est à jour. Pour un contrôle plus fin, notamment la réinitialisation de votre instance Ubuntu, consultez la [page de référence des commandes](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Fichiers binaires de l’utilisateur Ubuntu 

   La mise à niveau de cette partie de bash sur Ubuntu sur Windows installe toutes les mises à jour des fichiers binaires de l’utilisateur Ubuntu, y compris les applications que vous avez installées par le biais de apt-obtenir. Pour mettre à jour, exécutez les commandes suivantes dans bash:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt-recevoir des erreurs de mise à niveau
Certains packages utilisent des fonctionnalités que nous n’avons pas encore implémentées. `udev`, par exemple, n’est pas encore pris en `apt-get upgrade` charge et provoque plusieurs erreurs.

Pour résoudre les problèmes liés `udev`à, procédez comme suit:

1. Écrivez les éléments suivants `/usr/sbin/policy-rc.d` dans et enregistrez vos modifications.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Ajouter des autorisations d’exécution à`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Exécutez les commandes suivantes
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>Erreurs 0x80040306» lors de l’installation
Cela a pour effet de ne pas prendre en charge la console héritée.
Pour désactiver la console héritée:

1. Ouvrez cmd. exe
1. Cliquez avec le bouton droit sur la barre de titre-propriétés de >-> Décochez utiliser la console héritée
1. Cliquez sur OK

### <a name="error-0x80040154-after-windows-update"></a>Erreurs 0x80040154» après Windows Update
La fonctionnalité sous-système Windows pour Linux peut être désactivée au cours d’une mise à jour de Windows. Dans ce cas, la fonctionnalité Windows doit être réactivée. Pour plus d’informations sur l’activation du sous-système Windows pour Linux, consultez le [Guide d’installation](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Modification de la langue d’affichage
WSL install va tenter de modifier automatiquement les paramètres régionaux Ubuntu afin qu’ils correspondent aux paramètres régionaux de votre installation Windows.  Si vous ne souhaitez pas ce comportement, vous pouvez exécuter cette commande pour modifier les paramètres régionaux Ubuntu une fois l’installation terminée.  Vous devrez relancer bash. exe pour que cette modification prenne effet.

L’exemple ci-dessous passe de paramètres régionaux à en-US:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problèmes d’installation après la restauration du système Windows
1.  Supprimez `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` le dossier. <br/>
  **Remarque : N’effectuez pas cette opération si votre fonctionnalité facultative est entièrement installée et opérationnelle.**
2.  Activer la fonctionnalité facultative WSL (si ce n’est pas déjà fait)
3.  Redémarrer
4.  lxrun/Uninstall/Full
5.  Installer bash

### <a name="no-internet-access-in-wsl"></a>Aucun accès Internet dans WSL
Certains utilisateurs ont signalé des problèmes avec des applications de pare-feu spécifiques qui bloquent l’accès à Internet dans WSL.  Les pare-feu signalés sont:

1. Kaspersky
1. AVG
1. Avast

Dans certains cas, la désactivation du pare-feu autorise l’accès.  Dans certains cas, l’installation du pare-feu semble bloquer l’accès.

### <a name="permission-denied-error-when-using-ping"></a>Erreur de refus d’autorisation lors de l’utilisation de ping
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[Mise à jour anniversaire](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Les privilèges d’administrateur dans Windows sont requis pour exécuter la commande ping dans WSL.  Pour exécuter la commande ping, exécutez bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash. exe à partir d’une invite de commandes CMD/PowerShell avec des privilèges d’administrateur.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[Build 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Les privilèges d’administrateur ne sont plus nécessaires.

### <a name="bash-is-hung"></a>Bash est bloqué
Si, lors de l’utilisation de bash, vous constatez que bash est bloqué (ou bloqué) et ne répond pas aux entrées, aidez-nous à diagnostiquer le problème en collectant et en signalant une image mémoire. Notez que ces étapes bloquent votre système. N’effectuez pas cette opération si vous n’êtes pas familiarisé avec cette opération ou enregistrez votre travail avant de le faire.  <br/>
Pour collecter un vidage de la mémoire:
1. Changez le type de vidage de la mémoire en «terminer l’image mémoire». Tout en modifiant le type de vidage, prenez note de votre type actuel.
2. Utilisez les [étapes](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) pour configurer l’incident à l’aide du contrôle clavier.
3. Reproduire le blocage ou le blocage.
4. Bloquez le système à l’aide de la séquence de touches de (2).
5. Le système se bloque et collecte l’image mémoire.
6. Une fois le système redémarré, signalez le fichier Memory. secure@microsoft.comDMP à. L’emplacement par défaut du fichier dump est%SystemRoot%\memory.dmp ou C:\Windows\memory.dmp si C: est le lecteur système. Dans l’e-mail, Notez que le vidage est destiné à l’équipe WSL ou bash sur Windows.
7. Restaurez le type d’image mémoire sur le paramètre d’origine.

### <a name="check-your-build-number"></a>Vérifier votre numéro de build

Pour trouver l’architecture de votre PC et le numéro de version de Windows, ouvrez  
**Paramètres** > systèmeà > **propos de**

Recherchez les champs **version du système d’exploitation** et **type de système** .  
    ![Capture d’écran des champs de type de build et système](media/system.png) 


Pour rechercher votre numéro de build Windows Server, exécutez la commande suivante dans PowerShell:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirmer l’activation de WSL
Vous pouvez vérifier que le sous-système Windows pour Linux est activé en exécutant la commande suivante dans PowerShell:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH-problèmes de connexion au serveur
Échec de la tentative de connexion du serveur SSH avec l’erreur suivante: «La connexion a été fermée par le port 127.0.0.1 22».
1. Assurez-vous que votre serveur OpenSSH est en cours d’exécution:
   ``` BASH
   sudo service ssh status
   ```
   et que vous avez suivi ce didacticiel: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Arrêtez le service sshd et démarrez sshd en mode débogage:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Vérifiez les journaux de démarrage et assurez-vous que les HostKeys sont disponibles et que vous ne voyez pas les messages de journalisation tels que:
   ```
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

Si vous voyez des messages de ce type et que les clés `/etc/ssh/`sont manquantes sous, vous devrez régénérer les clés ou simplement purger & installer OpenSSH-Server:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

