---
title: Sous-système Windows pour Linux Enterprise
description: Ressources et instructions sur la façon d’utiliser au mieux le sous-système Windows pour Linux dans un environnement d’entreprise.
keywords: BashOnWindows, bash, wsl, windows, sous-système windows pour linux, sous-système windows, ubuntu, debian, suse, windows 10, entreprise, déploiement, hors connexion, empaquetage, stockage, distribution, installation, installer
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 02f4ff41614f78c0e588f329c777a87f8b416233
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235830"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>Installer le sous-système Windows pour Linux pour votre entreprise

Microsoft Store pour Entreprises offre des solutions variées aux entreprises qui souhaitent déployer WSL. La [documentation Microsoft Store pour Entreprises et Éducation](https://docs.microsoft.com/microsoft-store/) constitue une ressource de premier plan qui propose des informations générales sur l’expérience du Store.

Si vous êtes une entreprise qui cherche simplement à commencer à déployer WSL, suivez ces étapes :

* [Inscrivez-vous au Microsoft Store pour Entreprises pour commencer](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview).
* [Gérez vos produits et services (notamment qui peut accéder aux applications dans votre magasin privé)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview). Ici, vous pouvez ajouter des distributions WSL à votre magasin et contrôler qui peut les installer.
* [Utilisez une méthode de distribution de votre choix pour déployer le logiciel dans votre entreprise](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business).
* Expliquez aux employés de votre entreprise qu’ils peuvent utiliser le lien de documentation suivant pour installer WSL : [Installer le sous-système Windows pour Linux](./install-win10.md).

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Comment distribuer une distribution Linux sur Windows en mode hors connexion

Si les ordinateurs de votre entreprise n’ont pas accès au Microsoft Store ou au Microsoft Store pour Entreprises, vous pouvez télécharger le programme d’installation d’une distribution Linux disposant d’une licence hors connexion en suivant ces étapes.

### <a name="set-up-an-azure-active-directory-account"></a>Configurer un compte Azure Active Directory

Vous devez [vous inscrire pour obtenir un compte Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) et être l’administrateur général de votre organisation pour obtenir le programme d’installation des applications du Microsoft Store. Si vous avez déjà un compte, vous pouvez ignorer cette étape.

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>Configurer WSL en utilisant votre compte Microsoft Store pour Entreprises

Les instructions permettant d’inscrire un compte sont disponibles ici : https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business

1. Connectez-vous à Microsoft Store pour Entreprises et accédez à la page d’accueil : https://www.microsoft.com/business-store

    ![Page d’accueil de Microsoft Store pour Entreprises](media/offlineinstallscreens/1-screen.png)

2. Accédez à Gérer > Paramètres et activez « Afficher les applications hors connexion ».

    ![Page Paramètres du Microsoft Store pour Entreprises](media/offlineinstallscreens/2-screen.png)

3. Revenez à la page principale en sélectionnant « Acheter pour mon groupe ».

    ![Page d’accueil de Microsoft Store pour Entreprises](media/offlineinstallscreens/1-screen.png)

4. Recherchez la distribution souhaitée et sélectionnez-la.

    ![Page d’accueil de Microsoft Store pour Entreprises avec recherche active](media/offlineinstallscreens/3-screen.png)

5. Sélectionnez une licence « Hors connexion » dans le menu déroulant de type de licence et sélectionnez « Obtenir l’application ». (Certaines distributions Linux peuvent choisir de ne pas fournir de licence hors connexion).

    ![Page de produit Ubuntu dans Microsoft Store pour Entreprises](media/offlineinstallscreens/4-screen.png)

6. Sélectionnez le bouton « Gérer » pour accéder à la page de produit de l’application.

    ![Page de produit Ubuntu dans Microsoft Store pour Entreprises](media/offlineinstallscreens/5-screen.png)

7. Sélectionnez votre architecture et téléchargez le package pour une utilisation hors connexion.

    ![Page de détails du produit Ubuntu dans Microsoft Store pour Entreprises](media/offlineinstallscreens/6-screen.png)

Ce programme d’installation peut ensuite être distribué sur tout ordinateur sur lequel vous souhaitez installer WSL.
