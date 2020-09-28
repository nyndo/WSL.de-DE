---
title: GPU Accelerated Machine Learning Training im Windows-Subsystem für Linux
description: Erfahren Sie mehr über die Unterstützung von WSL 2 für NVIDIA CUDA, directml, tensorflow und pytorch.
keywords: WSL, Windows, Windows Subsystem, GPU COMPUTE, GPU Acceleration, NVIDIA, CUDA, directml, tensorflow, pytorch, NVIDIA CUDA Preview, GPU Driver, NVIDIA Container Toolkit, docker
ms.date: 06/17/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: bc20f2d3f1da646ba01dcdc00de8eca6c3825ec8
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413311"
---
# <a name="gpu-accelerated-machine-learning-training-in-the-windows-subsystem-for-linux"></a><span data-ttu-id="a066f-104">GPU-beschleunigtes Machine Learning-Training im Windows-Subsystem für Linux</span><span class="sxs-lookup"><span data-stu-id="a066f-104">GPU accelerated machine learning training in the Windows Subsystem for Linux</span></span>

<span data-ttu-id="a066f-105">Die Unterstützung für GPU-COMPUTE, das #1 die am meisten angeforderte WSL-Funktion, ist jetzt über das Windows Insider-Programm als Vorschau verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a066f-105">Support for GPU compute, the #1 most requested WSL feature, is now available for preview via the Windows Insider program.</span></span> <span data-ttu-id="a066f-106">[Blogbeitrag lesen](https://blogs.windows.com/windowsdeveloper/?p=55781).</span><span class="sxs-lookup"><span data-stu-id="a066f-106">[Read the blog post](https://blogs.windows.com/windowsdeveloper/?p=55781).</span></span>

## <a name="what-is-gpu-compute"></a><span data-ttu-id="a066f-107">Was ist GPU-Compute?</span><span class="sxs-lookup"><span data-stu-id="a066f-107">What is GPU compute?</span></span>

<span data-ttu-id="a066f-108">Die Nutzung der GPU-Beschleunigung für rechenintensive Aufgaben wird im Allgemeinen als "GPU-Compute" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a066f-108">Leveraging GPU acceleration for compute-intensive tasks is generally referred  to as "GPU compute".</span></span> <span data-ttu-id="a066f-109">GPU-Computing nutzt die GPU (Graphics Processing Unit) zum Beschleunigen von mathematischen, großen Arbeits Auslastungen und verwendet seine parallele Verarbeitung, um die erforderlichen Berechnungen schneller und in vielen Fällen als die Verwendung einer CPU auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a066f-109">GPU computing leverages the GPU (graphics processing unit) to accelerate math heavy workloads and uses its parallel processing to complete the required calculations faster, in many cases, than utilizing only a CPU.</span></span> <span data-ttu-id="a066f-110">Diese Parallelisierung ermöglicht deutliche Verbesserungen der Verarbeitungsgeschwindigkeit für diese mathematischen großen Arbeits Auslastungen, bei Ausführung auf einer CPU.</span><span class="sxs-lookup"><span data-stu-id="a066f-110">This parallelization enables significant processing speed improvements for these math heavy workloads then when running on a CPU.</span></span> <span data-ttu-id="a066f-111">Das Trainieren von Machine Learning-Modellen ist ein gutes Beispiel dafür, dass GPU-Compute die Zeit erheblich verkürzen kann, um diese rechenintensive Aufgabe abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="a066f-111">Training machine learning models is a great example in which GPU compute can significantly accelerate the time to complete this computationally expensive task.</span></span>

## <a name="install-and-set-up"></a><span data-ttu-id="a066f-112">Installieren und Einrichten</span><span class="sxs-lookup"><span data-stu-id="a066f-112">Install and set up</span></span>

<span data-ttu-id="a066f-113">Weitere Informationen zur Unterstützung von WSL 2 und zum Einstieg in das Training von Machine Learning-Modellen finden Sie im Leitfaden für die [GPU-Beschleunigung](/windows/win32/direct3d12/gpu-accelerated-training) in der directml-Dokumentation. In dieser Anleitung wird Folgendes behandelt:</span><span class="sxs-lookup"><span data-stu-id="a066f-113">Learn more about WSL 2 support and how to start training machine learning models in the [GPU Accelerated Training guide](/windows/win32/direct3d12/gpu-accelerated-training) inside the DirectML docs. This guide covers:</span></span>

* <span data-ttu-id="a066f-114">Leitfaden für Einsteiger oder Schüler/Studenten zum Einrichten von tensorflow mit directml</span><span class="sxs-lookup"><span data-stu-id="a066f-114">Guidance for beginners or students to set up TensorFlow with DirectML</span></span>
* <span data-ttu-id="a066f-115">Leitfaden für Fachleute, die mit der Ausführung Ihrer vorhandenen CUDA ml-Workflows beginnen</span><span class="sxs-lookup"><span data-stu-id="a066f-115">Guidance for professionals to start running their exisiting CUDA ML workflows</span></span>