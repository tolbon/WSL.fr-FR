---
title: Formation Machine Learning accélérée du GPU dans le sous-système Windows pour Linux
description: En savoir plus sur la prise en charge de WSL 2 pour NVIDIA CUDA, DirectML, Tensorflow et PyTorch.
keywords: WSL, Windows, Windows, sous-système, calcul GPU, accélération GPU, NVIDIA, CUDA, DirectML, Tensorflow, PyTorch, NVIDIA CUDA Preview, pilote GPU, NVIDIA Container Toolkit, amarrage
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: f101022dec534055905b25619a6c4fcee36f3f7d
ms.sourcegitcommit: 031a74801e03a90aed4b34c4fd5bfe964fc30994
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2020
ms.locfileid: "84947409"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a><span data-ttu-id="a4ea1-104">Formation Machine Learning accélérée du GPU dans le sous-système Windows pour Linux</span><span class="sxs-lookup"><span data-stu-id="a4ea1-104">GPU accelerated machine learning training in the Windows Subsystem for Linux</span></span>

<span data-ttu-id="a4ea1-105">La prise en charge du calcul GPU, la #1 fonctionnalité WSL la plus demandée, est désormais disponible en version préliminaire via le programme Windows Insider.</span><span class="sxs-lookup"><span data-stu-id="a4ea1-105">Support for GPU compute, the #1 most requested WSL feature, is now available for preview via the Windows Insider program.</span></span> <span data-ttu-id="a4ea1-106">[Lire le billet de blog](https://blogs.windows.com/windowsdeveloper/?p=55781).</span><span class="sxs-lookup"><span data-stu-id="a4ea1-106">[Read the blog post](https://blogs.windows.com/windowsdeveloper/?p=55781).</span></span>

## <a name="what-is-gpu-compute"></a><span data-ttu-id="a4ea1-107">Qu’est-ce que le calcul GPU ?</span><span class="sxs-lookup"><span data-stu-id="a4ea1-107">What is GPU compute?</span></span>

<span data-ttu-id="a4ea1-108">Tirer parti de l’accélération GPU pour les tâches nécessitant beaucoup de ressources est généralement appelé « calcul GPU ».</span><span class="sxs-lookup"><span data-stu-id="a4ea1-108">Leveraging GPU acceleration for compute-intensive tasks is generally referred  to as "GPU compute".</span></span> <span data-ttu-id="a4ea1-109">L’informatique GPU s’appuie sur le GPU (unité de traitement graphique) pour accélérer les charges de travail lourdes mathématiques et utilise son traitement parallèle pour effectuer les calculs requis plus rapidement, dans de nombreux cas, que l’utilisation d’un processeur uniquement.</span><span class="sxs-lookup"><span data-stu-id="a4ea1-109">GPU computing leverages the GPU (graphics processing unit) to accelerate math heavy workloads and uses its parallel processing to complete the required calculations faster, in many cases, than utilizing only a CPU.</span></span> <span data-ttu-id="a4ea1-110">Cette parallélisation permet des améliorations significatives de la vitesse de traitement pour ces charges de travail lourdes mathématiques, puis lors de l’exécution sur un processeur.</span><span class="sxs-lookup"><span data-stu-id="a4ea1-110">This parallelization enables significant processing speed improvements for these math heavy workloads then when running on a CPU.</span></span> <span data-ttu-id="a4ea1-111">L’apprentissage des modèles de Machine Learning est un excellent exemple dans lequel le calcul GPU peut accélérer considérablement le temps nécessaire à la réalisation de cette tâche coûteuse en ressources informatiques.</span><span class="sxs-lookup"><span data-stu-id="a4ea1-111">Training machine learning models is a great example in which GPU compute can significantly accelerate the time to complete this computationally expensive task.</span></span>

## <a name="install-and-set-up"></a><span data-ttu-id="a4ea1-112">Installer et configurer</span><span class="sxs-lookup"><span data-stu-id="a4ea1-112">Install and set up</span></span>

<span data-ttu-id="a4ea1-113">En savoir plus sur la prise en charge de WSL 2 et sur la façon de démarrer l’apprentissage Machine Learning des modèles dans le [Guide de formation accélérée GPU](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) à l’intérieur des documents DirectML. Ce guide couvre les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="a4ea1-113">Learn more about WSL 2 support and how to start training machine learning models in the [GPU Accelerated Training guide](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) inside the DirectML docs. This guide covers:</span></span>

* <span data-ttu-id="a4ea1-114">Aide pour les débutants ou les élèves pour configurer TensorFlow avec DirectML</span><span class="sxs-lookup"><span data-stu-id="a4ea1-114">Guidance for beginners or students to set up TensorFlow with DirectML</span></span>
* <span data-ttu-id="a4ea1-115">Aide pour les professionnels qui commencent à exécuter leurs flux de travail CUDA ML existants</span><span class="sxs-lookup"><span data-stu-id="a4ea1-115">Guidance for professionals to start running their exisiting CUDA ML workflows</span></span>
