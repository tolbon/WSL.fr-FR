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
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a>Formation Machine Learning accélérée du GPU dans le sous-système Windows pour Linux

La prise en charge du calcul GPU, la #1 fonctionnalité WSL la plus demandée, est désormais disponible en version préliminaire via le programme Windows Insider. [Lire le billet de blog](https://blogs.windows.com/windowsdeveloper/?p=55781).

## <a name="what-is-gpu-compute"></a>Qu’est-ce que le calcul GPU ?

Tirer parti de l’accélération GPU pour les tâches nécessitant beaucoup de ressources est généralement appelé « calcul GPU ». L’informatique GPU s’appuie sur le GPU (unité de traitement graphique) pour accélérer les charges de travail lourdes mathématiques et utilise son traitement parallèle pour effectuer les calculs requis plus rapidement, dans de nombreux cas, que l’utilisation d’un processeur uniquement. Cette parallélisation permet des améliorations significatives de la vitesse de traitement pour ces charges de travail lourdes mathématiques, puis lors de l’exécution sur un processeur. L’apprentissage des modèles de Machine Learning est un excellent exemple dans lequel le calcul GPU peut accélérer considérablement le temps nécessaire à la réalisation de cette tâche coûteuse en ressources informatiques.

## <a name="install-and-set-up"></a>Installer et configurer

En savoir plus sur la prise en charge de WSL 2 et sur la façon de démarrer l’apprentissage Machine Learning des modèles dans le [Guide de formation accélérée GPU](https://docs.microsoft.com/windows/win32/direct3d12/gpu-accelerated-training) à l’intérieur des documents DirectML. Ce guide couvre les sujets suivants :

* Aide pour les débutants ou les élèves pour configurer TensorFlow avec DirectML
* Aide pour les professionnels qui commencent à exécuter leurs flux de travail CUDA ML existants
