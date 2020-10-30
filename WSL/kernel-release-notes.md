---
title: Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux  Monatlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu, Kernel
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 0ab1e7e85ce9d601bd8eb602d98e3487e8202e03
ms.sourcegitcommit: 609850fadd20687636b8486264e87af47c538111
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "92444818"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="77a01-105">Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="77a01-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="77a01-106">Wir haben Unterstützung für WSL 2-Verteilungen hinzugefügt, [, die einen vollständigen Linux-Kernel verwenden](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="77a01-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="77a01-107">Der Linux-Kernel ist Open Source, und der Quellcode ist im [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel)-Repository verfügbar.</span><span class="sxs-lookup"><span data-stu-id="77a01-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="77a01-108">Dieser Linux-Kernel wird Ihrem Computer über Microsoft Update bereitgestellt und folgt einem separaten Veröffentlichungszeitplan für das Windows-Subsystem für Linux, das als Teil des Windows-Images bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="77a01-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="5451-microsoft-standard"></a><span data-ttu-id="77a01-109">5.4.51-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="77a01-109">5.4.51-microsoft-standard</span></span>
<span data-ttu-id="77a01-110">*Veröffentlichungsdatum* : Vorabversion: 22.10.2020</span><span class="sxs-lookup"><span data-stu-id="77a01-110">*Release Date* : Prerelease - 10/22/2020</span></span>

<span data-ttu-id="77a01-111">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51).</span><span class="sxs-lookup"><span data-stu-id="77a01-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-5.4.51).</span></span>

* <span data-ttu-id="77a01-112">Stabile Version von 5.4.51</span><span class="sxs-lookup"><span data-stu-id="77a01-112">Stable release of 5.4.51</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="77a01-113">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="77a01-113">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="77a01-114">*Veröffentlichungsdatum* : 15.09.2020</span><span class="sxs-lookup"><span data-stu-id="77a01-114">*Release Date* : 09/15/2020</span></span>

<span data-ttu-id="77a01-115">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="77a01-115">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="77a01-116">Dies ist eine stabile Version von 4.19.128</span><span class="sxs-lookup"><span data-stu-id="77a01-116">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="77a01-117">Korrigieren der IOCTL-Speicherbeschädigung durch dxgkrnl-Treiber</span><span class="sxs-lookup"><span data-stu-id="77a01-117">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="77a01-118">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="77a01-118">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="77a01-119">*Veröffentlichungsdatum* : Vorabversion</span><span class="sxs-lookup"><span data-stu-id="77a01-119">*Release Date* : Prerelease</span></span>

<span data-ttu-id="77a01-120">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="77a01-120">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="77a01-121">Treiber: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="77a01-121">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="77a01-122">Hinzugefügte Unterstützung für GPU Compute</span><span class="sxs-lookup"><span data-stu-id="77a01-122">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="77a01-123">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="77a01-123">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="77a01-124">*Veröffentlichungsdatum* : 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="77a01-124">*Release Date* : 06/09/2020</span></span> 

<span data-ttu-id="77a01-125">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="77a01-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="77a01-126">Aktualisierte WSL-Konfiguration für 4.19.104</span><span class="sxs-lookup"><span data-stu-id="77a01-126">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="77a01-127">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="77a01-127">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="77a01-128">*Veröffentlichungsdatum* : 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="77a01-128">*Release Date* : 11/12/2019</span></span> 

<span data-ttu-id="77a01-129">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="77a01-129">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="77a01-130">Dies ist das 4.19.84-Stable Release</span><span class="sxs-lookup"><span data-stu-id="77a01-130">This is the 4.19.84 stable release</span></span>

