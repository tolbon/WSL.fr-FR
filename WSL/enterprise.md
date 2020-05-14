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
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a><span data-ttu-id="28578-104">Installer le sous-système Windows pour Linux pour votre entreprise</span><span class="sxs-lookup"><span data-stu-id="28578-104">Set up Windows Subsystem for Linux for your enterprise company</span></span>

<span data-ttu-id="28578-105">Microsoft Store pour Entreprises offre des solutions variées aux entreprises qui souhaitent déployer WSL.</span><span class="sxs-lookup"><span data-stu-id="28578-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="28578-106">La [documentation Microsoft Store pour Entreprises et Éducation](https://docs.microsoft.com/microsoft-store/) constitue une ressource de premier plan qui propose des informations générales sur l’expérience du Store.</span><span class="sxs-lookup"><span data-stu-id="28578-106">The [Microsoft Store for Business and Education docs](https://docs.microsoft.com/microsoft-store/) are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="28578-107">Si vous êtes une entreprise qui cherche simplement à commencer à déployer WSL, suivez ces étapes :</span><span class="sxs-lookup"><span data-stu-id="28578-107">If you're a company that's just looking to get set up to start deploying WSL, follow these steps:</span></span>

* <span data-ttu-id="28578-108">[Inscrivez-vous au Microsoft Store pour Entreprises pour commencer](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="28578-108">[Sign up for the Microsoft Store for Business and get started](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview)</span></span>
* <span data-ttu-id="28578-109">[Gérez vos produits et services (notamment qui peut accéder aux applications dans votre magasin privé)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="28578-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="28578-110">Ici, vous pouvez ajouter des distributions WSL à votre magasin et contrôler qui peut les installer.</span><span class="sxs-lookup"><span data-stu-id="28578-110">Here you can add WSL distros to your store and control who can install them</span></span>
* <span data-ttu-id="28578-111">[Utilisez une méthode de distribution de votre choix pour déployer le logiciel dans votre entreprise](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business).</span><span class="sxs-lookup"><span data-stu-id="28578-111">[Use a distribution method of your choice to deploy the software to your company](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)</span></span>
* <span data-ttu-id="28578-112">Expliquez aux employés de votre entreprise qu’ils peuvent utiliser le lien de documentation suivant pour installer WSL : [Installer le sous-système Windows pour Linux](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="28578-112">Communicate to the employees of your company that they can use this documentation link to install WSL: [Install the Windows Subsystem for Linux](./install-win10.md)</span></span>

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a><span data-ttu-id="28578-113">Comment distribuer une distribution Linux sur Windows en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="28578-113">How to distribute a Linux distribution on Windows offline</span></span>

<span data-ttu-id="28578-114">Si les ordinateurs de votre entreprise n’ont pas accès au Microsoft Store ou au Microsoft Store pour Entreprises, vous pouvez télécharger le programme d’installation d’une distribution Linux disposant d’une licence hors connexion en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="28578-114">If the computers in your company don't have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distribution that has an offline license by following these steps.</span></span>

### <a name="set-up-an-azure-active-directory-account"></a><span data-ttu-id="28578-115">Configurer un compte Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="28578-115">Set up an Azure Active Directory account</span></span>

<span data-ttu-id="28578-116">Vous devez [vous inscrire pour obtenir un compte Azure AD](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) et être l’administrateur général de votre organisation pour obtenir le programme d’installation des applications du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="28578-116">You need to [sign up for an Azure AD account](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="28578-117">Si vous avez déjà un compte, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="28578-117">If you already have an account, you can skip this step.</span></span>

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a><span data-ttu-id="28578-118">Configurer WSL en utilisant votre compte Microsoft Store pour Entreprises</span><span class="sxs-lookup"><span data-stu-id="28578-118">Set up WSL using your Microsoft Store for Business account</span></span>

<span data-ttu-id="28578-119">Les instructions permettant d’inscrire un compte sont disponibles ici : https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="28578-119">The instructions to register an account are found here: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business</span></span>

1. <span data-ttu-id="28578-120">Connectez-vous à Microsoft Store pour Entreprises et accédez à la page d’accueil : https://www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="28578-120">Sign into the Store for Business and go to the homepage: https://www.microsoft.com/business-store</span></span>

    ![Page d’accueil de Microsoft Store pour Entreprises](media/offlineinstallscreens/1-screen.png)

2. <span data-ttu-id="28578-122">Accédez à Gérer > Paramètres et activez « Afficher les applications hors connexion ».</span><span class="sxs-lookup"><span data-stu-id="28578-122">Go to Manage > Settings and enable 'Show offline apps'.</span></span>

    ![Page Paramètres du Microsoft Store pour Entreprises](media/offlineinstallscreens/2-screen.png)

3. <span data-ttu-id="28578-124">Revenez à la page principale en sélectionnant « Acheter pour mon groupe ».</span><span class="sxs-lookup"><span data-stu-id="28578-124">Go back to the main page by selecting 'Shop for my group'.</span></span>

    ![Page d’accueil de Microsoft Store pour Entreprises](media/offlineinstallscreens/1-screen.png)

4. <span data-ttu-id="28578-126">Recherchez la distribution souhaitée et sélectionnez-la.</span><span class="sxs-lookup"><span data-stu-id="28578-126">Search for your desired distribution and select it.</span></span>

    ![Page d’accueil de Microsoft Store pour Entreprises avec recherche active](media/offlineinstallscreens/3-screen.png)

5. <span data-ttu-id="28578-128">Sélectionnez une licence « Hors connexion » dans le menu déroulant de type de licence et sélectionnez « Obtenir l’application ».</span><span class="sxs-lookup"><span data-stu-id="28578-128">Select an 'Offline' license in the License type dropdown menu and select 'Get the app'.</span></span> <span data-ttu-id="28578-129">(Certaines distributions Linux peuvent choisir de ne pas fournir de licence hors connexion).</span><span class="sxs-lookup"><span data-stu-id="28578-129">(Some Linux distributions may elect not to provide an offline license).</span></span>

    ![Page de produit Ubuntu dans Microsoft Store pour Entreprises](media/offlineinstallscreens/4-screen.png)

6. <span data-ttu-id="28578-131">Sélectionnez le bouton « Gérer » pour accéder à la page de produit de l’application.</span><span class="sxs-lookup"><span data-stu-id="28578-131">Select the 'Manage' button to get to the app's product page.</span></span>

    ![Page de produit Ubuntu dans Microsoft Store pour Entreprises](media/offlineinstallscreens/5-screen.png)

7. <span data-ttu-id="28578-133">Sélectionnez votre architecture et téléchargez le package pour une utilisation hors connexion.</span><span class="sxs-lookup"><span data-stu-id="28578-133">Select your architecture and download the package for offline use.</span></span>

    ![Page de détails du produit Ubuntu dans Microsoft Store pour Entreprises](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="28578-135">Ce programme d’installation peut ensuite être distribué sur tout ordinateur sur lequel vous souhaitez installer WSL.</span><span class="sxs-lookup"><span data-stu-id="28578-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>
