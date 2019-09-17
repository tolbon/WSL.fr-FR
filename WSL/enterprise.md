---
title: Sous-système Windows pour Linux Enterprise
description: Ressources et instructions sur la façon d’utiliser au mieux le sous-système Windows pour Linux dans un environnement d’entreprise.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, Enterprise, déploiement, hors connexion, empaquetage, stockage, distribution, installation, installation
author: craigloewen-msft
ms.author: crloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: ea03f2c67d8389eb41d686a99140e11b3181401c
ms.sourcegitcommit: ed5cf72d5ceb92edd50cf9260ac31fd4d95a02c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "71020970"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Sous-système Windows pour Linux Enterprise

Le Microsoft Store pour les entreprises offre une variété de solutions aux entreprises qui souhaitent déployer des WSL dans leur entreprise. Les [documents en ligne](https://docs.microsoft.com/en-us/microsoft-store/) de l’Microsoft Store pour les entreprises sont une excellente ressource pour trouver des informations générales sur l’expérience du Store.

Si vous êtes une société à l’origine de la configuration pour commencer le déploiement de WSL, vous pouvez suivre ces étapes, qui sont expliquées dans les documents Microsoft Store :

* [Inscrivez-vous à l’Microsoft Store pour les entreprises et commencez](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Gérez vos produits et services (notamment qui peut accéder aux applications de votre magasin privé)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Ici, vous pouvez ajouter WSL distributions à votre boutique et contrôler qui peut les installer
* [Utilisez une méthode de distribution de votre choix pour déployer le logiciel dans votre entreprise](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Communiquez avec les utilisateurs qui ont accès à WSL distributions pour qu’ils puissent [utiliser ces étapes](https://docs.microsoft.com/en-us/windows/wsl/install-win10) pour installer le distribution ou le distributions de leur choix. 

## <a name="how-to-distribute-a-distro-offline"></a>Distribution d’un distribution hors connexion

Si les ordinateurs de votre entreprise n’ont pas accès au Microsoft Store ou à la Microsoft Store pour l’entreprise, vous pouvez télécharger le programme d’installation d’un distribution Linux disposant d’une licence hors connexion en procédant comme suit. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Configurer un compte d’Azure Active Directory (AD) 

Vous devez disposer d’un compte Azure AD et être l’administrateur général de votre organisation pour obtenir le programme d’installation des applications Microsoft Store. Si vous disposez déjà d’un compte, vous pouvez ignorer cette étape.

Vous trouverez les instructions d’inscription d’un compte ici : https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Connectez-vous au Store pour entreprises et accédez à la page d’accueil
Connectez-vous ici : www.microsoft.com/business-store

![Page d’espace MS Store pour entreprises](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Accédez à gérer-> paramètres et activez « afficher les applications hors connexion »

![Page des paramètres MS Store pour entreprises](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Revenez à la page principale en cliquant sur « acheter pour mon groupe »

![Page d’espace MS Store pour entreprises](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Recherchez le distribution souhaité et sélectionnez-le

![Page d’espace MS Store pour entreprises avec recherche active](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Sélectionnez une licence « hors connexion » dans le menu déroulant type de licence, puis cliquez sur « Télécharger l’application ».

![Page produit MS Store pour entreprises Ubuntu](media/offlineinstallscreens/4-screen.png)

Remarque : certains distributions peuvent choisir de ne pas disposer d’une licence en mode hors connexion

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Cliquez sur le bouton « gérer » pour accéder à la page du produit de l’application

![Page produit MS Store pour entreprises Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Sélectionnez votre architecture et téléchargez le package pour une utilisation hors connexion

![Page Détails du produit MS Store pour entreprises Ubuntu](media/offlineinstallscreens/6-screen.png)

Ce programme d’installation peut ensuite être distribué à n’importe quel ordinateur sur lequel vous souhaitez installer WSL.