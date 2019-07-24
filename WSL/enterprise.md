---
title: Sous-système Windows pour Linux Enterprise
description: Ressources et instructions sur la façon d’utiliser au mieux le sous-système Windows pour Linux dans un environnement d’entreprise.
keywords: BashOnWindows, bash, WSL, Windows, sous-système Windows pour Linux, windowssubsystem, Ubuntu, Debian, SUSE, Windows 10, Enterprise, déploiement, hors connexion, empaquetage, stockage, distribution, installation, installation
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063277"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="891cc-104">Sous-système Windows pour Linux Enterprise</span><span class="sxs-lookup"><span data-stu-id="891cc-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="891cc-105">Le Microsoft Store pour les entreprises offre une variété de solutions aux entreprises qui souhaitent déployer des WSL dans leur entreprise.</span><span class="sxs-lookup"><span data-stu-id="891cc-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="891cc-106">Les [documents en ligne](https://docs.microsoft.com/en-us/microsoft-store/) de l’Microsoft Store pour les entreprises sont une excellente ressource pour trouver des informations générales sur l’expérience du Store.</span><span class="sxs-lookup"><span data-stu-id="891cc-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="891cc-107">Si vous êtes une société à l’origine de la configuration pour commencer le déploiement de WSL, vous pouvez suivre ces étapes, qui sont expliquées dans les documents Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="891cc-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="891cc-108">Inscrivez-vous à l’Microsoft Store pour les entreprises et commencez</span><span class="sxs-lookup"><span data-stu-id="891cc-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="891cc-109">[Gérez vos produits et services (notamment qui peut accéder aux applications de votre magasin privé)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="891cc-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="891cc-110">Ici, vous pouvez ajouter WSL distributions à votre boutique et contrôler qui peut les installer</span><span class="sxs-lookup"><span data-stu-id="891cc-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="891cc-111">Utilisez une méthode de distribution de votre choix pour déployer le logiciel dans votre entreprise</span><span class="sxs-lookup"><span data-stu-id="891cc-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="891cc-112">Communiquez avec les utilisateurs qui ont accès à WSL distributions pour qu’ils puissent [utiliser ces étapes](https://docs.microsoft.com/en-us/windows/wsl/install-win10) pour installer le distribution ou le distributions de leur choix.</span><span class="sxs-lookup"><span data-stu-id="891cc-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="891cc-113">Distribution d’un distribution hors connexion</span><span class="sxs-lookup"><span data-stu-id="891cc-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="891cc-114">Si les ordinateurs de votre entreprise n’ont pas accès au Microsoft Store ou à la Microsoft Store pour l’entreprise, vous pouvez télécharger le programme d’installation d’un distribution Linux disposant d’une licence hors connexion en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="891cc-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="891cc-115">Configurer un compte d’Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="891cc-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="891cc-116">Vous devez disposer d’un compte Azure AD et être l’administrateur général de votre organisation pour obtenir le programme d’installation des applications Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="891cc-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="891cc-117">Si vous disposez déjà d’un compte, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="891cc-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="891cc-118">Vous trouverez les instructions d’inscription d’un compte ici: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="891cc-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="891cc-119">Connectez-vous au Store pour entreprises et accédez à la page d’accueil</span><span class="sxs-lookup"><span data-stu-id="891cc-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="891cc-120">Connectez-vous ici: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="891cc-120">Sign in here: www.microsoft.com/business-store</span></span>

![Page d’espace MS Store pour entreprises](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="891cc-122">Accédez à gérer-> paramètres et activez «afficher les applications hors connexion»</span><span class="sxs-lookup"><span data-stu-id="891cc-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![Page des paramètres MS Store pour entreprises](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="891cc-124">Revenez à la page principale en cliquant sur «acheter pour mon groupe»</span><span class="sxs-lookup"><span data-stu-id="891cc-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![Page d’espace MS Store pour entreprises](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="891cc-126">Recherchez le distribution souhaité et sélectionnez-le</span><span class="sxs-lookup"><span data-stu-id="891cc-126">Search for your desired distro and select it</span></span>

![Page d’espace MS Store pour entreprises avec recherche active](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="891cc-128">Sélectionnez une licence «hors connexion» dans le menu déroulant type de licence, puis cliquez sur «Télécharger l’application».</span><span class="sxs-lookup"><span data-stu-id="891cc-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![Page produit MS Store pour entreprises Ubuntu](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="891cc-130">Remarque: certains distributions peuvent choisir de ne pas disposer d’une licence en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="891cc-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="891cc-131">Cliquez sur le bouton «gérer» pour accéder à la page du produit de l’application</span><span class="sxs-lookup"><span data-stu-id="891cc-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![Page produit MS Store pour entreprises Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="891cc-133">Sélectionnez votre architecture et téléchargez le package pour une utilisation hors connexion</span><span class="sxs-lookup"><span data-stu-id="891cc-133">Select your architecture and download the package for offline use</span></span>

![Page Détails du produit MS Store pour entreprises Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="891cc-135">Ce programme d’installation peut ensuite être distribué à n’importe quel ordinateur sur lequel vous souhaitez installer WSL.</span><span class="sxs-lookup"><span data-stu-id="891cc-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>