---
title: Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux  Monatlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu, Kernel
ms.date: 06/09/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: eb93135355384013b93b4b5c4af03a582280febf
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719119"
---
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a><span data-ttu-id="af4f8-105">Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="af4f8-105">Release Notes for Windows Subsystem for Linux kernel</span></span>

<span data-ttu-id="af4f8-106">Wir haben Unterstützung für WSL 2-Verteilungen hinzugefügt, [, die einen vollständigen Linux-Kernel verwenden](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span><span class="sxs-lookup"><span data-stu-id="af4f8-106">We've added support for WSL 2 distributions, [which use a full Linux kernel](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/).</span></span> <span data-ttu-id="af4f8-107">Der Linux-Kernel ist Open Source, und der Quellcode ist im [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel)-Repository verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af4f8-107">This Linux kernel is open source, with its source code available at the [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel) repository.</span></span> <span data-ttu-id="af4f8-108">Dieser Linux-Kernel wird Ihrem Computer über Microsoft Update bereitgestellt und folgt einem separaten Veröffentlichungszeitplan für das Windows-Subsystem für Linux, das als Teil des Windows-Images bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="af4f8-108">This Linux kernel is delivered to your machine via Microsoft Update, and follows a separate release schedule to the Windows Subsystem for Linux which is delivered as part of the Windows image.</span></span>

## <a name="419128-microsoft-standard"></a><span data-ttu-id="af4f8-109">4.19.128-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="af4f8-109">4.19.128-microsoft-standard</span></span>
<span data-ttu-id="af4f8-110">*Veröffentlichungsdatum*: 15.09.2020</span><span class="sxs-lookup"><span data-stu-id="af4f8-110">*Release Date*: 09/15/2020</span></span>

<span data-ttu-id="af4f8-111">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="af4f8-111">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).</span></span>

* <span data-ttu-id="af4f8-112">Dies ist eine stabile Version von 4.19.128</span><span class="sxs-lookup"><span data-stu-id="af4f8-112">This is a stable release of 4.19.128</span></span>
* <span data-ttu-id="af4f8-113">Korrigieren der IOCTL-Speicherbeschädigung durch dxgkrnl-Treiber</span><span class="sxs-lookup"><span data-stu-id="af4f8-113">Fix dxgkrnl driver IOCTL memory corruption</span></span>

## <a name="419121-microsoft-standard"></a><span data-ttu-id="af4f8-114">4.19.121-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="af4f8-114">4.19.121-microsoft-standard</span></span>
<span data-ttu-id="af4f8-115">*Veröffentlichungsdatum*: Vorabversion</span><span class="sxs-lookup"><span data-stu-id="af4f8-115">*Release Date*: Prerelease</span></span>

<span data-ttu-id="af4f8-116">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="af4f8-116">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).</span></span>

* <span data-ttu-id="af4f8-117">Treiber: hv: vmbus: hook up dxgkrnl</span><span class="sxs-lookup"><span data-stu-id="af4f8-117">Drivers: hv: vmbus: hook up dxgkrnl</span></span>
* <span data-ttu-id="af4f8-118">Hinzugefügte Unterstützung für GPU Compute</span><span class="sxs-lookup"><span data-stu-id="af4f8-118">Added support for GPU Compute</span></span>

## <a name="419104-microsoft-standard"></a><span data-ttu-id="af4f8-119">4.19.104-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="af4f8-119">4.19.104-microsoft-standard</span></span>
<span data-ttu-id="af4f8-120">*Veröffentlichungsdatum*: 09.06.2020</span><span class="sxs-lookup"><span data-stu-id="af4f8-120">*Release Date*: 06/09/2020</span></span> 

<span data-ttu-id="af4f8-121">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="af4f8-121">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).</span></span>

* <span data-ttu-id="af4f8-122">Aktualisierte WSL-Konfiguration für 4.19.104</span><span class="sxs-lookup"><span data-stu-id="af4f8-122">Update WSL config for 4.19.104</span></span>

## <a name="41984-microsoft-standard"></a><span data-ttu-id="af4f8-123">4.19.84-microsoft-standard</span><span class="sxs-lookup"><span data-stu-id="af4f8-123">4.19.84-microsoft-standard</span></span>
<span data-ttu-id="af4f8-124">*Veröffentlichungsdatum*: 12.11.2019</span><span class="sxs-lookup"><span data-stu-id="af4f8-124">*Release Date*: 11/12/2019</span></span> 

<span data-ttu-id="af4f8-125">[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span><span class="sxs-lookup"><span data-stu-id="af4f8-125">[Official Github release link](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).</span></span>

* <span data-ttu-id="af4f8-126">Dies ist das 4.19.84-Stable Release</span><span class="sxs-lookup"><span data-stu-id="af4f8-126">This is the 4.19.84 stable release</span></span>

