---
title: Sous-système Windows pour Linux pour l’entreprise
description: Ressources et obtenir des instructions sur comment mieux utilisent le sous-système Windows pour Linux dans un environnement d’entreprise.
keywords: Installer BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, entreprise, déploiement, hors connexion, de création de package, store, distribution, installation
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063277"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Sous-système Windows pour Linux pour l’entreprise

Le Microsoft Store pour entreprises offre un large éventail de solutions pour les entreprises qui souhaitent déployer WSL à leur entreprise. Le [documentation en ligne de](https://docs.microsoft.com/en-us/microsoft-store/) pour le Microsoft Store pour entreprises sont une ressource précieuse pour obtenir des informations générales sur l’expérience de Store.

Si vous êtes une entreprise qui vise uniquement pour la définition de configuration pour commencer le déploiement WSL vous pouvez suivre ces étapes, qui sont décrits à l’intérieur de la documentation de Microsoft Store :

* [Inscrivez-vous pour le Microsoft Store pour entreprises et de prise en main](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [Gérer vos produits et services (y compris qui peut accéder à quelles applications dans votre magasin privé)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview). Ici, vous pouvez ajouter les distributions WSL et votre magasin de contrôler les utilisateurs qui peut les installer
* [Utiliser une méthode de distribution de votre choix pour déployer le logiciel sur votre entreprise](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Communiquer aux utilisateurs qui ont accès à des distributions WSL qu’ils peuvent [Utilisez ces étapes](https://docs.microsoft.com/en-us/windows/wsl/install-win10) pour installer le distributeur ou les distributions de leur choix 

## <a name="how-to-distribute-a-distro-offline"></a>Comment distribuer une distribution en mode hors connexion

Si les ordinateurs de votre société n’ont pas accès pour le Microsoft Store ou le Microsoft Store pour entreprises, vous pouvez télécharger le programme d’installation d’une distribution Linux qui dispose d’une licence hors connexion en suivant ces étapes. 

### <a name="set-up-an-azure-active-directory-ad-account"></a>Configurer un compte Azure Active Directory (AD) 

Vous devez disposer d’un compte Azure AD et l’administrateur global pour votre organisation pour obtenir le programme d’installation d’applications du Microsoft Store. Si vous avez déjà un compte, vous pouvez ignorer cette étape.

Vous trouverez ici les instructions pour inscrire un compte : https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>Connectez-vous le Store pour entreprises, puis accédez à la page d’accueil
Connectez-vous ici : www.microsoft.com/business-store

![Store MS pour la page d’accueil professionnelle](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>Accédez à gérer -> paramètres et activer afficher les applications hors connexion

![Store MS pour la page de paramètres d’entreprise](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>Revenez à la page principale en cliquant sur « Acheter de mon groupe »

![Store MS pour la page d’accueil professionnelle](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>Recherchez votre distribution souhaitée et sélectionnez-le

![Store MS pour la page d’accueil professionnelle avec recherche active](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>Sélectionnez une licence « Hors connexion » dans le menu déroulant de type licence et cliquez sur « Obtenir l’application »

![Store MS pour la page de produit business Ubuntu](media/offlineinstallscreens/4-screen.png)

Remarque : certaines distributions peuvent choisir de ne pas disposer d’une licence hors connexion

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>Cliquez sur le bouton 'Gérer' pour accéder à la page de produit de l’application

![Store MS pour la page de produit business Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>Sélectionnez votre architecture et téléchargez le package pour une utilisation hors connexion

![Store MS pour la page de détails du produit business Ubuntu](media/offlineinstallscreens/6-screen.png)

Ce programme d’installation peut ensuite être distribué à n’importe quel ordinateur où vous souhaitez installer WSL.