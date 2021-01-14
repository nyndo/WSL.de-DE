---
title: Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux  Monatlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu, Kernel
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 07488d61ad1c01f85c1d78789274aa3afbc9e1d8
ms.sourcegitcommit: e2d586925b314ce4517773b9c78736450a9f75d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "97977105"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="22374-105">Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="22374-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="22374-106">Wir haben Unterstützung für WSL 2-Verteilungen hinzugefügt, [, die einen vollständigen Linux-Kernel verwenden](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="22374-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="22374-107">Der Linux-Kernel ist Open Source, und der Quellcode ist im [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel)-Repository verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22374-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="22374-108">Dieser Linux-Kernel wird Ihrem Computer über Microsoft Update bereitgestellt und folgt einem separaten Veröffentlichungszeitplan für das Windows-Subsystem für Linux, das als Teil des Windows-Images bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="22374-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="5472"></a><span data-ttu-id="22374-109">5.4.72</span><span class="sxs-lookup"><span data-stu-id="22374-109">5.4.72</span></span>
<span data-ttu-id="22374-110">*Veröffentlichungsdatum*: Vorabversion: 10.11.2020</span><span class="sxs-lookup"><span data-stu-id="22374-110">*Release Date*: Prerelease - 11/10/2020</span></span>

[<span data-ttu-id="22374-111">Offizieller Link zum GitHub-Release</span><span class="sxs-lookup"><span data-stu-id="22374-111">Official Github release link</span></span>](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.72)

* <span data-ttu-id="22374-112">Konfiguration für 5.4.72 wurde korrigiert.</span><span class="sxs-lookup"><span data-stu-id="22374-112">Fix config for 5.4.72</span></span>

## <a name="5451-microsoft-standard"></a><span data-ttu-id="22374-113">5.4.51-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="22374-113">5.4.51-microsoft-standard</span></span>
<span data-ttu-id="22374-114">*Veröffentlichungsdatum*: Vorabversion: 22.10.2020</span><span class="sxs-lookup"><span data-stu-id="22374-114">*Release Date*: Prerelease - 10/22/2020</span></span>

<span data-ttu-id="22374-115">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51).</span><span class="sxs-lookup"><span data-stu-id="22374-115">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51).</span></span>

* <span data-ttu-id="22374-116">Stabile Version von 5.4.51</span><span class="sxs-lookup"><span data-stu-id="22374-116">Stable release of 5.4.51</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="22374-117">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="22374-117">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="22374-118">*Veröffentlichungsdatum*: 15.09.2020</span><span class="sxs-lookup"><span data-stu-id="22374-118">*Release Date*: 09/15/2020</span></span>

<span data-ttu-id="22374-119">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="22374-119">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="22374-120">Dies ist eine stabile Version von 4.19.128</span><span class="sxs-lookup"><span data-stu-id="22374-120">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="22374-121">Korrigieren der IOCTL-Speicherbeschädigung durch dxgkrnl-Treiber</span><span class="sxs-lookup"><span data-stu-id="22374-121">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="22374-122">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="22374-122">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="22374-123">*Veröffentlichungsdatum*: Vorabversion</span><span class="sxs-lookup"><span data-stu-id="22374-123">*Release Date*: Prerelease</span></span>

<span data-ttu-id="22374-124">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="22374-124">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="22374-125">Treiber: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="22374-125">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="22374-126">Hinzugefügte Unterstützung für GPU Compute</span><span class="sxs-lookup"><span data-stu-id="22374-126">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="22374-127">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="22374-127">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="22374-128">*Veröffentlichungsdatum*: 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="22374-128">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="22374-129">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="22374-129">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="22374-130">Aktualisierte WSL-Konfiguration für 4.19.104</span><span class="sxs-lookup"><span data-stu-id="22374-130">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="22374-131">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="22374-131">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="22374-132">*Veröffentlichungsdatum*: 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="22374-132">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="22374-133">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="22374-133">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="22374-134">Dies ist das 4.19.84-Stable Release</span><span class="sxs-lookup"><span data-stu-id="22374-134">This is the 4.19.84 stable release</span></span>

