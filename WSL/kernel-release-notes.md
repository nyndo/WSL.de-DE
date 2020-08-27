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
# <a name="release-notes-for-windows-subsystem-for-linux-kernel"></a>Anmerkungen zu dieser Version des Windows-Subsystems für den Linux-Kernel

Wir haben Unterstützung für WSL 2-Verteilungen hinzugefügt, [, die einen vollständigen Linux-Kernel verwenden](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/). Der Linux-Kernel ist Open Source, und der Quellcode ist im [WSL2-Linux-Kernel](https://github.com/microsoft/WSL2-Linux-Kernel)-Repository verfügbar. Dieser Linux-Kernel wird Ihrem Computer über Microsoft Update bereitgestellt und folgt einem separaten Veröffentlichungszeitplan für das Windows-Subsystem für Linux, das als Teil des Windows-Images bereitgestellt wird.

## <a name="419128-microsoft-standard"></a>4.19.128-microsoft-standard
*Veröffentlichungsdatum*: Vorabversion

[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.128-microsoft-standard).

* Dies ist eine stabile Version von 4.19.128
* Korrigieren der IOCTL-Speicherbeschädigung durch dxgkrnl-Treiber

## <a name="419121-microsoft-standard"></a>4.19.121-microsoft-standard
*Veröffentlichungsdatum*: Vorabversion

[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.121-microsoft-standard).

* Treiber: hv: vmbus: hook up dxgkrnl
* Hinzugefügte Unterstützung für GPU Compute

## <a name="419104-microsoft-standard"></a>4.19.104-microsoft-standard
*Veröffentlichungsdatum*: 09.06.2020 

[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.104-microsoft-standard).

* Aktualisierte WSL-Konfiguration für 4.19.104

## <a name="41984-microsoft-standard"></a>4.19.84-microsoft-standard
*Veröffentlichungsdatum*: 12.11.2019 

[Offizieller Link zum GitHub-Release](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/4.19.84-microsoft-standard).

* Dies ist das 4.19.84-Stable Release

