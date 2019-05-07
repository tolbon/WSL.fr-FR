---
title: Sous-système Windows pour Linux Enterprise
description: Ressources et obtenir des instructions sur comment mieux utilisent le sous-système Windows pour Linux dans un environnement d’entreprise.
keywords: Installer BashOnWindows, bash, wsl, windows, le sous-système windows pour linux, windowssubsystem, ubuntu, debian, suse, windows 10, entreprise, déploiement, hors connexion, de création de package, store, distribution, installation
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063277"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="8bf62-104">Sous-système Windows pour Linux Enterprise</span><span class="sxs-lookup"><span data-stu-id="8bf62-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="8bf62-105">Le Microsoft Store pour entreprises offre un large éventail de solutions pour les entreprises qui souhaitent déployer WSL à leur entreprise.</span><span class="sxs-lookup"><span data-stu-id="8bf62-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="8bf62-106">Le [documentation en ligne de](https://docs.microsoft.com/en-us/microsoft-store/) pour le Microsoft Store pour entreprises sont une ressource précieuse pour obtenir des informations générales sur l’expérience de Store.</span><span class="sxs-lookup"><span data-stu-id="8bf62-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="8bf62-107">Si vous êtes une entreprise qui vise uniquement pour la définition de configuration pour commencer le déploiement WSL vous pouvez suivre ces étapes, qui sont décrits à l’intérieur de la documentation de Microsoft Store :</span><span class="sxs-lookup"><span data-stu-id="8bf62-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="8bf62-108">Inscrivez-vous pour le Microsoft Store pour entreprises et de prise en main</span><span class="sxs-lookup"><span data-stu-id="8bf62-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="8bf62-109">[Gérer vos produits et services (y compris qui peut accéder à quelles applications dans votre magasin privé)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span><span class="sxs-lookup"><span data-stu-id="8bf62-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="8bf62-110">Ici, vous pouvez ajouter les distributions WSL et votre magasin de contrôler les utilisateurs qui peut les installer</span><span class="sxs-lookup"><span data-stu-id="8bf62-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="8bf62-111">Utiliser une méthode de distribution de votre choix pour déployer le logiciel sur votre entreprise</span><span class="sxs-lookup"><span data-stu-id="8bf62-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="8bf62-112">Communiquer aux utilisateurs qui ont accès à des distributions WSL qu’ils peuvent [Utilisez ces étapes](https://docs.microsoft.com/en-us/windows/wsl/install-win10) pour installer le distributeur ou les distributions de leur choix</span><span class="sxs-lookup"><span data-stu-id="8bf62-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="8bf62-113">Comment distribuer une distribution en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="8bf62-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="8bf62-114">Si les ordinateurs de votre société n’ont pas accès pour le Microsoft Store ou le Microsoft Store pour entreprises, vous pouvez télécharger le programme d’installation d’une distribution Linux qui dispose d’une licence hors connexion en suivant ces étapes.</span><span class="sxs-lookup"><span data-stu-id="8bf62-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="8bf62-115">Configurer un compte Azure Active Directory (AD)</span><span class="sxs-lookup"><span data-stu-id="8bf62-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="8bf62-116">Vous devez disposer d’un compte Azure AD et l’administrateur global pour votre organisation pour obtenir le programme d’installation d’applications du Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="8bf62-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="8bf62-117">Si vous avez déjà un compte, vous pouvez ignorer cette étape.</span><span class="sxs-lookup"><span data-stu-id="8bf62-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="8bf62-118">Vous trouverez ici les instructions pour inscrire un compte : https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="8bf62-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="8bf62-119">Connectez-vous le Store pour entreprises, puis accédez à la page d’accueil</span><span class="sxs-lookup"><span data-stu-id="8bf62-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="8bf62-120">Connectez-vous ici : www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="8bf62-120">Sign in here: www.microsoft.com/business-store</span></span>

![Store MS pour la page d’accueil professionnelle](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="8bf62-122">Accédez à gérer -> paramètres et activer afficher les applications hors connexion</span><span class="sxs-lookup"><span data-stu-id="8bf62-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![Store MS pour la page de paramètres d’entreprise](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="8bf62-124">Revenez à la page principale en cliquant sur « Acheter de mon groupe »</span><span class="sxs-lookup"><span data-stu-id="8bf62-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![Store MS pour la page d’accueil professionnelle](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="8bf62-126">Recherchez votre distribution souhaitée et sélectionnez-le</span><span class="sxs-lookup"><span data-stu-id="8bf62-126">Search for your desired distro and select it</span></span>

![Store MS pour la page d’accueil professionnelle avec recherche active](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="8bf62-128">Sélectionnez une licence « Hors connexion » dans le menu déroulant de type licence et cliquez sur « Obtenir l’application »</span><span class="sxs-lookup"><span data-stu-id="8bf62-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![Store MS pour la page de produit business Ubuntu](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="8bf62-130">Remarque : certaines distributions peuvent choisir de ne pas disposer d’une licence hors connexion</span><span class="sxs-lookup"><span data-stu-id="8bf62-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="8bf62-131">Cliquez sur le bouton 'Gérer' pour accéder à la page de produit de l’application</span><span class="sxs-lookup"><span data-stu-id="8bf62-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![Store MS pour la page de produit business Ubuntu](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="8bf62-133">Sélectionnez votre architecture et téléchargez le package pour une utilisation hors connexion</span><span class="sxs-lookup"><span data-stu-id="8bf62-133">Select your architecture and download the package for offline use</span></span>

![Store MS pour la page de détails du produit business Ubuntu](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="8bf62-135">Ce programme d’installation peut ensuite être distribué à n’importe quel ordinateur où vous souhaitez installer WSL.</span><span class="sxs-lookup"><span data-stu-id="8bf62-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>