---
title: Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux  Monatlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu, Kernel
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ffec37d179005eb7015a8f9af8de0ac185710bec
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866119"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="874a6-105">Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="874a6-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="874a6-106">Wir haben Unterstützung für WSL 2-Verteilungen hinzugefügt, [, die einen vollständigen Linux-Kernel verwenden](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="874a6-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="874a6-107">Der Linux-Kernel ist Open Source, und der Quellcode ist im [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel)-Repository verfügbar.</span><span class="sxs-lookup"><span data-stu-id="874a6-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="874a6-108">Dieser Linux-Kernel wird Ihrem Computer über Microsoft Update bereitgestellt und folgt einem separaten Veröffentlichungszeitplan für das Windows-Subsystem für Linux, das als Teil des Windows-Images bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="874a6-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="874a6-109">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="874a6-109">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="874a6-110">*Veröffentlichungsdatum*: Vorabversion</span><span class="sxs-lookup"><span data-stu-id="874a6-110">*Release Date*: Prerelease</span></span>

<span data-ttu-id="874a6-111">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="874a6-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="874a6-112">Dies ist eine stabile Version von 4.19.128</span><span class="sxs-lookup"><span data-stu-id="874a6-112">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="874a6-113">Korrigieren der IOCTL-Speicherbeschädigung durch dxgkrnl-Treiber</span><span class="sxs-lookup"><span data-stu-id="874a6-113">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="874a6-114">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="874a6-114">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="874a6-115">*Veröffentlichungsdatum*: Vorabversion</span><span class="sxs-lookup"><span data-stu-id="874a6-115">*Release Date*: Prerelease</span></span>

<span data-ttu-id="874a6-116">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="874a6-116">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="874a6-117">Treiber: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="874a6-117">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="874a6-118">Hinzugefügte Unterstützung für GPU Compute</span><span class="sxs-lookup"><span data-stu-id="874a6-118">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="874a6-119">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="874a6-119">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="874a6-120">*Veröffentlichungsdatum*: 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="874a6-120">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="874a6-121">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="874a6-121">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="874a6-122">Aktualisierte WSL-Konfiguration für 4.19.104</span><span class="sxs-lookup"><span data-stu-id="874a6-122">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="874a6-123">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="874a6-123">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="874a6-124">*Veröffentlichungsdatum*: 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="874a6-124">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="874a6-125">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="874a6-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="874a6-126">Dies ist das 4.19.84-Stable Release</span><span class="sxs-lookup"><span data-stu-id="874a6-126">This is the 4.19.84 stable release</span></span>

