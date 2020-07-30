---
title: Prise en main de l’utilisation de VS Code avec le sous-système Windows pour Linux
description: Découvrez comment configurer VS Code pour créer et déboguer du code à l’aide du sous-système Windows pour Linux.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, vs code, extension distante, Debug, path, Visual Studio
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: f5d7bd4f582f504ea3c4bd814454b1dc881ffed2
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948653"
---
# <a name="get-started-using-visual-studio-code-with-windows-subsystem-for-linux"></a>Prise en main de l’utilisation de Visual Studio Code avec le sous-système Windows pour Linux

Visual Studio Code, avec l’extension WSL distante, vous permet d’utiliser WSL en tant qu’environnement de développement à plein temps directement à partir de VS Code. Vous pouvez :

* développer dans un environnement Linux
* utiliser des chaînes et des utilitaires spécifiques à Linux
* Exécutez et déboguez vos applications Linux à partir du confort de Windows tout en conservant l’accès aux outils de productivité comme Outlook et Office
* utiliser le VS Code terminal intégré pour exécuter votre distribution Linux de votre choix
* Tirez parti des fonctionnalités de VS Code telles que la [saisie semi-automatique de code IntelliSense](https://code.visualstudio.com/docs/editor/intellisense) [, le](https://code.visualstudio.com/docs/python/linting)décodage, la [prise en charge du débogage](https://code.visualstudio.com/docs/nodejs/nodejs-debugging), les [extraits de code](https://code.visualstudio.com/docs/editor/userdefinedsnippets)et les [tests unitaires](https://code.visualstudio.com/docs/python/testing)
* Gérez facilement votre contrôle de version avec la [prise en charge](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support) intégrée de Git de vs code
* exécuter des commandes et des extensions de VS Code directement dans vos projets WSL
* Modifiez les fichiers de votre système de fichiers Linux ou Windows monté (par exemple/mnt/c) sans vous soucier des problèmes de chemin d’accès, de compatibilité binaire ou d’autres problèmes liés au système d’exploitation.

## <a name="install-vs-code-and-the-remote-wsl-extension"></a>Installer VS Code et l’extension WSL distante

* Accédez à la [page d’installation de vs code](https://code.visualstudio.com/download) et sélectionnez le programme d’installation 32 ou 64 bits. Installez Visual Studio Code sur Windows (et non dans votre système de fichiers WSL).

* Lorsque vous êtes invité à **Sélectionner des tâches supplémentaires** lors de l’installation, veillez à cocher l’option **Ajouter au chemin d’accès** afin de pouvoir ouvrir facilement un dossier dans WSL à l’aide de la commande code.

* Installez le [Pack d’extension de développement distant](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). Ce pack d’extension comprend l’extension WSL distante, en plus des extensions Remote-SSH et Remote-Containers, ce qui vous permet d’ouvrir n’importe quel dossier dans un conteneur, sur un ordinateur distant ou dans WSL.

> [!IMPORTANT]
> Pour installer l’extension WSL à distance, vous avez besoin de la version [1,35 de mai](https://code.visualstudio.com/updates/v1_35) ou d’une version ultérieure de vs code. Nous vous déconseillons d’utiliser WSL dans VS Code sans l’extension WSL distante, car vous perdrez la prise en charge de la saisie semi-automatique, du débogage, du découpage, etc. Fait amusant : cette extension WSL est installée dans $HOME/.vscode/extensions (entrez la commande `ls $HOME\.vscode\extensions\` dans PowerShell).

## <a name="update-your-linux-distribution"></a>Mettre à jour votre distribution Linux

Certaines distributions Linux WSL ne disposent pas de bibliothèques requises par le serveur VS Code pour démarrer. Vous pouvez ajouter des bibliothèques supplémentaires à votre distribution Linux à l’aide de son gestionnaire de package.

Par exemple, pour mettre à jour Debian ou Ubuntu, utilisez :

```bash
sudo apt-get update
```

Pour ajouter wget (pour récupérer du contenu à partir de serveurs Web) et des certificats d’autorité de certification (pour permettre aux applications SSL de vérifier l’authenticité des connexions SSL), entrez :

```bash
sudo apt-get install wget ca-certificates
```

## <a name="open-a-wsl-project-in-visual-studio-code"></a>Ouvrez un projet WSL dans Visual Studio Code

### <a name="from-the-command-line"></a>À partir de la ligne de commande

Pour ouvrir un projet à partir de votre distribution WSL, ouvrez la ligne de commande de la distribution, puis entrez :`code .`

![Ouvrir le projet WSL avec VS Code serveur distant](../media/wsl-open-vs-code.gif)

### <a name="from-vs-code"></a>À partir de VS Code

Vous pouvez également accéder à d’autres options de VS Code à distance à l’aide du raccourci : `CTRL+SHIFT+P` dans vs code pour afficher la palette de commandes. Si vous tapez `VSCODE-REMOTE` , vous verrez toutes les options de vs code à distance disponibles, ce qui vous permet de rouvrir le dossier dans une session à distance, de spécifier la distribution que vous souhaitez ouvrir dans, et bien plus encore.

![Palette de commandes de VS Code](../media/vscode-remote-command-palette.png)

## <a name="extensions-inside-of-vs-code-remote"></a>Extensions à l’intérieur de VS Code à distance

L’extension WSL distante fractionne les VS Code dans une architecture « client-serveur », avec le client (l’interface utilisateur) en cours d’exécution sur votre ordinateur Windows et le serveur (votre code, git, plug-ins, etc.) exécuté à distance.

Lors de l’exécution de VS Code à distance, la sélection de l’onglet « Extensions » affiche une liste d’extensions comprise entre votre ordinateur local et votre distribution WSL.

L’installation d’une extension locale, comme un [thème](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs), ne doit être installée qu’une seule fois.

Certaines extensions, telles que l' [extension Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) ou tout élément qui gère des éléments tels que le débogage ou le débogage, doivent être installées séparément sur chaque distribution WSL distante. VS Code affichera une icône d’avertissement ⚠ , ainsi qu’un bouton « installer en WSL » vert, si une extension installée localement n’est pas installée sur votre ordinateur distant WSL.

![VS Code avec les extensions WSL à distance et les extensions locales](../media/vscode-remote-wsl-extensions.png)

Pour plus d’informations, consultez les documents VS Code :

* Lorsque VS Code Remote est démarré dans WSL, aucun script de démarrage de l’interpréteur de commandes n’est exécuté. Pour plus d’informations sur l’exécution de commandes supplémentaires ou la modification de l’environnement, consultez [l’article script de configuration de l’environnement avancé](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script) .

* Vous rencontrez des problèmes lors du lancement de VS Code à partir de votre ligne de commande WSL ? Ce [Guide de dépannage](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working) contient des conseils sur la modification des variables de chemin d’accès, la résolution des erreurs d’extension sur les dépendances manquantes, la résolution des problèmes de fin de ligne git, l’installation d’un VSIX local sur un ordinateur distant, le lancement d’une fenêtre de navigateur, le port localhost du bloqueur, les sockets Web qui ne fonctionnent pas, les erreurs de stockage des

## <a name="install-git-optional"></a>Installer Git (facultatif)

Si vous envisagez de collaborer avec d’autres personnes ou d’héberger votre projet sur un site open source (comme GitHub), VS Code prend en charge le [contrôle de version avec Git](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support). L’onglet Contrôle de code source de VS Code assure le suivi de toutes vos modifications et contient des commandes Git courantes (ajouter, valider, pousser, extraire) intégrées directement dans l’interface utilisateur.

Pour installer Git, consultez [configurer Git pour fonctionner avec le sous-système Windows pour Linux](./wsl-git.md).

## <a name="install-windows-terminal-optional"></a>Installer le Terminal Windows (facultatif)

Le nouveau terminal Windows active plusieurs onglets (basculer rapidement entre l’invite de commandes, PowerShell ou plusieurs distributions Linux), les combinaisons de touches personnalisées (créez vos propres touches de raccourci pour ouvrir ou fermer les onglets, copier + coller, etc.), les Emoji ☺ et les thèmes personnalisés (modèles de couleurs, styles et tailles de police, image d’arrière-plan/flou En savoir plus dans les [documents Windows Terminal Server](https://docs.microsoft.com/windows/terminal).

1. Procurez-vous [le terminal Windows dans le Microsoft Store](https://www.microsoft.com/store/apps/9n0dx20hk701): en installant via le Store, les mises à jour sont gérées automatiquement.

2. Une fois l’installation terminée, ouvrez le Terminal Windows, puis sélectionnez **Paramètres** pour personnaliser votre terminal à l’aide du fichier `profile.json`.

## <a name="additional-resources"></a>Ressources supplémentaires

* [Développement à distance VS Code](https://code.visualstudio.com/docs/remote/remote-overview)
* [Conseils et astuces pour le développement à distance](https://code.visualstudio.com/docs/remote/troubleshooting)
* [Didacticiel sur le développement à distance avec WSL](https://code.visualstudio.com/remote-tutorials/wsl/getting-started)
* [Utilisation de Docker avec WSL 2 et VS Code](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
* [Utilisation de C++ et de WSL dans VS Code](https://code.visualstudio.com/docs/cpp/config-wsl)
* [Service R à distance pour Linux](https://docs.microsoft.com/visualstudio/rtvs/setting-up-remote-r-service-on-linux?view=vs-2017)

D’autres extensions sont disponibles :

* [Mappages de touches d'autres éditeurs](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) : ces extensions peuvent être utiles si vous utilisiez auparavant un autre éditeur de texte (comme Atom, Sublime, Vim, eMacs, Notepad++, etc.).
* [Synchronisation des paramètres](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) : vous permet de synchroniser vos paramètres VS Code entre différentes installations à l'aide de GitHub. Si vous travaillez sur plusieurs ordinateurs, cela permet de garantir la cohérence de votre environnement.
* [Débogueur pour Chrome](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): une fois que vous avez terminé le développement côté serveur avec Linux, vous devez développer et tester le côté client. Cette extension intègre votre éditeur VS Code au service de débogage de votre navigateur Chrome, pour plus d'efficacité.
