---
title: Résolution des problèmes de la Susbystem Windows pour Linux
description: Fournit des informations détaillées sur les erreurs courantes et émet des personnes de rencontrer lors de l’exécution de Linux sur le Susbystem Windows pour Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 055bdc02dcf8f078caa014abd6dd755a47c99cfe
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063297"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Résolution des problèmes sous-système Windows pour Linux

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash perd la connectivité de réseau une fois connectée à un réseau privé virtuel

Si après la connexion à un réseau privé virtuel sur Windows, bash perd la connectivité réseau, essayez cette solution de contournement à partir de bash. Cette solution de contournement vous permettra de remplacer manuellement la résolution DNS via `/etc/resolv.conf`.

1. Prenez note du serveur DNS de la connexion VPN à partir de cette opération `ipconfig.exe /all`
2. Faites une copie de resolv.conf existant `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. Dissocier le resolv.con actuel `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Ouvrez `/etc/resolv.conf` et <br/>
   a. Supprimez la première ligne du fichier, qui porte la mention «\# ce fichier a été automatiquement généré par WSL. Pour arrêter la génération automatique de ce fichier, supprimez cette ligne. ». <br/>
   b. Ajoutez l’entrée DNS à partir de (1) ci-dessus en tant que la toute première entrée dans la liste des serveurs DNS. <br/>
   c. Fermez le fichier. <br/>

Une fois que vous avez déconnecté du VPN, vous devrez rétablir les modifications apportées à `/etc/resolv.conf`. Pour ce faire, effectuez :
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Démarrage WSL ou de l’installation d’une distribution retourne un code d’erreur

Suivez [ces instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) pour collecter des journaux détaillés et de signaler un problème sur notre GitHub.

### <a name="updating-bash-on-ubuntu-on-windows"></a>La mise à jour de Bash sur Ubuntu sur Windows

Il existe deux composants de Bash sur Ubuntu sur Windows qui peuvent nécessiter la mise à jour. 

1. Le sous-système Windows pour Linux
  
   La mise à niveau de cette partie de Bash sur Ubuntu sur Windows activera la toute nouvelle contours de correctifs dans le [notes de version](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes). Assurez-vous que vous êtes inscrit au programme Windows Insider et que votre build est à jour. Pour un contrôle plus précis, y compris la réinitialisation de votre Ubuntu grain de l’instance, consultez la [page de référence de commande](https://msdn.microsoft.com/en-us/commandline/wsl/reference).

2. Les binaires d’utilisateur Ubuntu 

   La mise à niveau de cette partie de Bash sur Ubuntu sur Windows installe les mises à jour pour les binaires d’utilisateur Ubuntu, y compris les applications que vous avez installés via apt-get. Pour mettre à jour d’exécuter les commandes suivantes dans l’interpréteur de commandes :
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Erreurs de mise à niveau d’apt-get
Certains packages utilisent les fonctionnalités que nous n’avons pas encore implémentée. `udev`, par exemple, n’est pas encore pris en charge et empêche plusieurs `apt-get upgrade` erreurs.

Pour résoudre les problèmes liés à `udev`, suivez les étapes suivantes :

1. Écrivez le code suivant à `/usr/sbin/policy-rc.d` et enregistrez vos modifications.
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. Ajouter des autorisations d’exécution `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Exécutez les commandes suivantes
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>« Erreur : 0x80040306 » sur l’installation
Cela a à voir avec le fait que nous ne prennent pas en charge l’ancienne console.
Pour désactiver l’ancienne console :

1. Ouvrez cmd.exe
1. Cliquez avec le bouton droit sur titre de la barre -> Propriétés -> utiliser décochez l’ancienne console
1. Cliquez sur OK

### <a name="error-0x80040154-after-windows-update"></a>« Erreur : 0 x 80040154 » après la mise à jour de Windows
Le sous-système Windows pour Linux fonctionnalité peut être désactivé pendant une mise à jour de Windows. Dans ce cas, la fonctionnalité de Windows doit être réactivée. Des instructions pour activer le sous-système Windows pour Linux sont disponibles dans le [Guide d’Installation](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).

### <a name="changing-the-display-language"></a>Modification de la langue d’affichage
Installation WSL tente de modifier automatiquement les paramètres régionaux Ubuntu pour faire correspondre les paramètres régionaux de votre installation de Windows.  Si vous ne souhaitez pas ce comportement, vous pouvez exécuter cette commande pour modifier les paramètres régionaux Ubuntu, une fois l’installation terminée.  Vous devez relancer bash.exe pour que cette modification prenne effet.

Le ci-dessous exemple modifie les paramètres régionaux en-US :
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Problèmes d’installation après la restauration du système Windows
1.  Supprimer le `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` dossier. <br/>
  **Remarque : Ne le faites pas cela si votre fonctionnalité facultative est entièrement installée et fonctionne.**
2.  Activer la fonctionnalité facultative WSL (si pas déjà)
3.  Redémarrer
4.  lxrun / désinstaller/total
5.  Installer l’interpréteur de commandes

### <a name="no-internet-access-in-wsl"></a>Aucun accès internet dans WSL
Certains utilisateurs ont signalé des problèmes avec les applications de pare-feu spécifiques bloque l’accès internet dans WSL.  Les pare-feux signalés sont :

1. Kaspersky
1. AVG
1. Avast

Dans certains cas désactiver le pare-feu autorise l’accès.  Dans certains cas le simple fait d’avoir le pare-feu installé recherche pour bloquer l’accès.

### <a name="permission-denied-error-when-using-ping"></a>Erreur autorisation refusée lors de l’utilisation de ping
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[Mise à jour anniversaire](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Privilèges d’administrateur dans Windows sont requis pour exécuter un test ping dans WSL.  Pour exécuter la commande ping, exécutez Bash sur Ubuntu sur Windows en tant qu’administrateur, ou exécutez bash.exe à partir d’une invite CMD/PowerShell avec des privilèges d’administrateur.

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[Build 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  Privilèges d’administrateur n’est plus nécessaires.

### <a name="bash-is-hung"></a>Bash est bloqué
Si tout en travaillant avec bash, vous trouvez que bash est bloqué (ou bloquée) et ne répond ne pas aux entrées, nous aider à diagnostiquer le problème en collectant et envoyant un vidage de mémoire. Notez que ces étapes seront bloque votre système. Ne le faites pas cela si vous n’êtes pas familiarisé avec qui ou que vous enregistrez votre travail avant de faire cela.  <br/>
Pour collecter un vidage de mémoire :
1. Modifier le type de vidage de mémoire pour « image mémoire complète ». Lors de la modification du type de vidage, prenez note de votre type actuel.
2. Utilisez le [étapes](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/) pour configurer l’incident à l’aide du contrôle de clavier.
3. Reproduction le blocage ou le blocage.
4. Arrêter le système à l’aide de la séquence de touches à partir de (2).
5. Le système de se bloquer et collecter l’image mémoire.
6. Une fois que le système redémarre, signaler memory.dmp à secure@microsoft.com. L’emplacement par défaut du fichier de vidage est %SystemRoot%\memory.dmp ou C:\Windows\memory.dmp si C: est le lecteur système. Dans l’e-mail, notez que le vidage concerne le WSL ou Bash sur l’équipe de Windows.
7. Restaurer le type de vidage de mémoire pour le paramètre d’origine.

### <a name="check-your-build-number"></a>Vérifier votre numéro de build

Pour rechercher le que numéro de build de Windows et architecture de votre ordinateur, ouvrez  
**Paramètres** > **système** > **sur**

Recherchez le **Build du système d’exploitation** et **système Type** champs.  
    ![Capture d’écran de Build et le Type de système de champs](media/system.png) 


Pour rechercher votre numéro de build de Windows Server, exécutez la commande suivante dans PowerShell :  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Confirmer que WSL est activée
Vous pouvez vérifier que le sous-système Windows pour Linux est activé en exécutant la commande suivante dans PowerShell :  
``` PowerShell
PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Problèmes de connexion OpenSSH-Server
Essayez de vous connecter à votre serveur SSH est a échoué avec l’erreur suivante : « Connexion fermée par 127.0.0.1 port 22 ».
1. Assurez-vous que votre serveur OpenSSH est en cours d’exécution :
   ``` BASH
   sudo service ssh status
   ```
   et que vous avez suivi ce didacticiel : https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. Arrêter le service sshd et démarrez sshd en mode débogage :
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. Vérifiez les journaux de démarrage et assurez-vous que les clés d’hôte sont disponibles et vous ne voyez pas les messages de journal comme : debug1 : version sshd OpenSSH_7.2, OpenSSL 1.0.2g 1er mars 2016 debug1 : key_load_private : mot de passe incorrect fourni pour déchiffrer debug1 de clé privée : key_load_public : Ce fichier ou répertoire n’a pas pu charger clé d’hôte : /etc/ssh/ssh_host_rsa_key debug1 : key_load_private : Ce type debug1 aucun fichier ou répertoire : key_load_public : Ce fichier ou répertoire n’a pas pu charger clé d’hôte : /etc/ssh/ssh_host_dsa_key debug1 : key_load_private : Ce type debug1 aucun fichier ou répertoire : key_load_public : Ce fichier ou répertoire n’a pas pu charger clé d’hôte : /etc/ssh/ssh_host_ecdsa_key debug1 : key_load_private : Ce type debug1 aucun fichier ou répertoire : key_load_public : Ce fichier ou répertoire n’a pas pu charger clé d’hôte : /etc/ssh/ssh_host_ed25519_key

Si vous ne voyez pas ces messages et des clés sont manquantes sous `/etc/ssh/`, vous devrez régénérer les clés ou juste purger & Installer openssh-server :
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

