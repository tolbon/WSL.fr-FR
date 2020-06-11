---
title: Prise en main de Git sur le sous-système Windows pour Linux
description: Découvrez comment configurer Git pour la gestion de version sur le sous-système Windows pour Linux.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, git, GitHub, contrôle de version
ms.date: 06/04/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 687a12186d11343a2d4131e0fdeeef3bcec902fb
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671009"
---
# <a name="get-started-using-git-on-windows-subsystem-for-linux"></a>Prise en main de Git sur le sous-système Windows pour Linux

Git est le système de contrôle de version le plus couramment utilisé. Avec git, vous pouvez suivre les modifications apportées aux fichiers, afin de disposer d’un enregistrement de ce qui a été effectué et de pouvoir revenir aux versions antérieures des fichiers si nécessaire. Git facilite également la collaboration, ce qui permet de fusionner les modifications de plusieurs personnes dans une seule source.

## <a name="git-can-be-installed-on-windows-and-on-wsl"></a>Git peut être installé sur Windows et sur WSL

Remarque importante : lorsque vous activez WSL et installez une distribution Linux, vous installez un nouveau système de fichiers, séparé de Windows NTFS C:\ sur votre ordinateur. Dans Linux, les lecteurs ne disposent pas de lettres. Ils reçoivent des points de montage. La racine de votre système de fichiers `/` est le point de montage de votre partition racine, ou dossier, dans le cas de WSL. Tout ce qui `/` se trouve sous est le même lecteur. Par exemple, sur mon ordinateur portable, j’ai installé deux versions d’Ubuntu (20,04 et 18,04), ainsi que Debian. Si j’ouvre ces distributions, sélectionnez le répertoire racine à l’aide de la commande `cd ~` , puis entrez la commande `explorer.exe .` , l’Explorateur de fichiers Windows s’ouvre et affiche le chemin d’accès au répertoire pour cette distribution.

| Distribution Linux | Chemin Windows pour accéder au dossier de destination |
| ----------- | ----------- |
| Ubuntu 20.04 | `\\wsl$\Ubuntu-20.04\home\username` |
| Ubuntu 18.04 | `\\wsl$\Ubuntu-18.04\home\username` |
| Debian | `\\wsl$\Debian\home\username` |
| Windows PowerShell | `C:\Users\username` |

> [!TIP]
> Si vous cherchez à accéder au répertoire de fichiers Windows à partir de votre ligne de commande de distribution WSL, au lieu de `C:\Users\username` , le répertoire est accessible à l’aide de `/mnt/c/Users/username` , car la distribution Linux affiche votre système de fichiers Windows en tant que lecteur monté.

Vous devez installer Git sur chaque système de fichiers avec lequel vous avez l’intention de l’utiliser.

![Présentation des versions de git par distribution](../media/git-versions.gif)

## <a name="installing-git"></a>Installation de Git

Git est déjà installé avec la plupart du sous-système Windows pour les distributions Linux. Toutefois, vous souhaiterez peut-être mettre à jour vers la version la plus récente et vous devrez configurer votre fichier de configuration git.

Pour installer Git, consultez le site [Télécharger git pour Linux](https://git-scm.com/download/linux) . Chaque distribution Linux possède son propre gestionnaire de package et sa propre commande d’installation. Par exemple, pour installer Git sur la distribution Alpine, utilisez : `apk add git` . Vous pouvez également [installer Git pour Windows](https://git-scm.com/download/win) si vous ne l’avez pas déjà fait.

## <a name="git-config-file-setup"></a>Configuration du fichier de configuration git

Pour configurer votre fichier de configuration git, ouvrez une ligne de commande pour la distribution dans laquelle vous travaillez, puis entrez : `git config --global user.name "Your Name"` , puis `git config --global user.email "youremail@domain.com"` . En remplaçant le contenu par des citations par le nom et l’adresse de messagerie que vous avez utilisés pour créer votre compte git.

> [!TIP]
> Si vous n’avez pas encore de compte Git, vous pouvez [vous inscrire pour en obtenir un sur GitHub](https://github.com/join). Si vous n’avez jamais travaillé avec Git, les [guides GitHub](https://guides.github.com/) peuvent vous aider à démarrer. Si vous avez besoin de modifier votre configuration git, vous pouvez le faire avec un éditeur de texte intégré tel que Nano : `nano ~/.gitconfig`.

Nous vous recommandons de [sécuriser votre compte avec l’authentification à deux facteurs (2FA)](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa).

## <a name="git-credential-manager-setup"></a>Installation du gestionnaire d’informations d’identification git

Git Credential Manager vous permet d’authentifier un serveur git distant, même si vous disposez d’un modèle d’authentification complexe comme l’authentification à deux facteurs, Azure Active Directory ou à l’aide d’URL distantes SSH qui requièrent un mot de passe de clé SSH pour chaque Push git. Git Credential Manager s’intègre au flux d’authentification des services tels que GitHub et, une fois que vous êtes authentifié auprès de votre fournisseur d’hébergement, demande un nouveau jeton d’authentification. Il stocke ensuite le jeton en toute sécurité dans le [Gestionnaire d’informations d’identification Windows](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager). Après la première fois, vous pouvez utiliser Git pour communiquer avec votre fournisseur d’hébergement sans avoir à vous réauthentifier. Il accède simplement au jeton dans le gestionnaire d’informations d’identification Windows.

Pour configurer Git Credential Manager en vue de l’utiliser avec une distribution WSL, ouvrez votre distribution et entrez cette commande :

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

À présent, toute opération git que vous effectuez dans votre distribution WSL utilise le gestionnaire d’informations d’identification. Si vous avez déjà mis en cache les informations d’identification d’un hôte, celui-ci y accède à partir du gestionnaire d’informations d’identification. Si ce n’est pas le cas, vous recevez une réponse de boîte de dialogue demandant vos informations d’identification, même si vous êtes dans une console Linux.

## <a name="adding-a-git-ignore-file"></a>Ajout d’un fichier git ignore

Nous vous recommandons d’ajouter un [fichier. gitignore](https://help.github.com/en/articles/ignoring-files) à vos projets. GitHub offre [une collection de modèles. gitignore utiles](https://github.com/github/gitignore) avec les configurations de fichiers. gitignore recommandés, organisées en fonction de votre cas d’utilisation.

Si vous choisissez de [créer un référentiel à l’aide du site Web GitHub](https://help.github.com/articles/create-a-repo), des cases à cocher sont disponibles pour initialiser votre référentiel avec un fichier Lisez-moi, un fichier. gitignore configuré pour votre type de projet spécifique, ainsi que des options pour ajouter une licence si vous en avez besoin.

## <a name="git-and-vs-code"></a>Git et VS Code

Visual Studio Code est fourni avec la prise en charge intégrée de git, y compris un onglet de contrôle de code source qui affiche vos modifications et gère diverses commandes git pour vous. En savoir plus sur [la prise en charge de git par vs code](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).

## <a name="git-line-endings"></a>Fins de ligne git

Si vous utilisez le même dossier de référentiel entre Windows, WSL ou un conteneur, veillez à définir des fins de ligne cohérentes.

Étant donné que Windows et Linux utilisent des fins de ligne par défaut différentes, git peut signaler un grand nombre de fichiers modifiés qui n’ont pas de différences par rapport à leurs fins de ligne. Pour éviter ce problème, vous pouvez désactiver la conversion de fin de ligne à l’aide d’un `.gitattributes` fichier ou globalement du côté Windows. Consultez cette [vs code document sur la résolution des problèmes de fin de ligne git](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files).

## <a name="additional-resources"></a>Ressources supplémentaires

* [WSL & VS Code](./wsl-vscode.md)
* [Laboratoire d’apprentissage GitHub : cours en ligne](https://lab.github.com/)
* [Outil de visualisation git](http://git-school.github.io/visualizing-git/)
* [Outils git-stockage des informations d’identification](https://git-scm.com/book/it/v2/Git-Tools-Credential-Storage)
