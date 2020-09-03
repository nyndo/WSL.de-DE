---
title: WSL 2 – Häufig gestellte Fragen
description: Finden Sie Antworten auf häufig gestellte Fragen (FAQs) zum Windows-Subsystem für Linux 2, etwa auf die Frage „Kann ich WSL 2 auf einem virtuellen Computer ausführen?“
keywords: BashOnWindows, Bash, WSL, WSL2, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Installation, installieren
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: a021dc3c6c3c2a14fea631f2733d2b846c6fe3ad
ms.sourcegitcommit: 910845e9b3f980b2c5b9b4968331a706720603c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2020
ms.locfileid: "89058485"
---
# <a name="wsl-2-faqs"></a>Häufig gestellte Fragen (FAQs) zu WSL 2

Unten finden Sie eine Liste mit häufig gestellten Fragen zum Windows-Subsystem 2 für Linux.

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>Verwendet WSL 2 Hyper-V? Soll es unter Windows 10 Home verfügbar sein?

WSL 2 ist für alle SKUs erhältlich, für die WSL aktuell verfügbar ist, einschließlich Windows 10 Home.

In der neuesten Version von WSL wurde Virtualisierung auf der Grundlage der Hyper-V-Architektur ermöglicht. Diese Architektur steht in Form der optionalen Komponente ‚Virtual Machine Platform‘ zur Verfügung. Diese optionale Komponente soll für alle SKUs verfügbar sein. Weitere Details dazu stehen Ihnen in Kürze zur Verfügung, wenn wir uns der Veröffentlichung von WSL 2 nähern.

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>Was geschieht mit WSL 1? Wird es aufgegeben?

Es ist zurzeit nicht geplant, WSL 1 als veraltet zu kennzeichnen. Sie können WSL 1 und WSL 2-Distributionen nebeneinander ausführen und jederzeit ein Upgrade und Downgrade für jede Distribution durchführen. Das Hinzufügen von WSL 2 als neue Architektur bietet dem WSL-Team eine bessere Plattform zum Bereitstellen von Features, die aus WSL eine beeindruckende Möglichkeit zum Ausführen einer Linux-Umgebung unter Windows machen.

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>Kann ich WSL 2 und andere Virtualisierungstools von Drittanbietern wie VMware oder VirtualBox ausführen?

Einige Anwendungen von Drittanbietern funktionieren nicht, wenn Hyper-V verwendet wird, was bedeutet, dass sie nicht ausgeführt werden können, wenn WSL 2 aktiviert ist (z. B. VMware und VirtualBox). Vor kurzem wurden jedoch von VirtualBox und VMware Versionen veröffentlicht, die Hyper-V und WSL2 unterstützen. Hier finden Sie weitere Informationen zu [VirtualBox-Änderungen][1] und [VMware-Änderungen][4].

Wir arbeiten kontinuierlich an Lösungen zur Unterstützung der Integration von Hyper-V in Drittanbieterlösungen. Beispielsweise machen wir eine Reihe von APIs mit der Bezeichnung [Hypervisor-Plattform][2] verfügbar, die von Drittanbietern von Virtualisierungslösungen verwendet werden können, um ihre Software mit Hyper-V kompatibel zu machen. Dadurch können Anwendungen die Hyper-V-Architektur für ihre Emulation verwenden, wie etwa [den Google Android Emulator][3] und VirtualBox 6 und höher, die jetzt beide mit Hyper-V kompatibel sind.

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>Kann ich in WSL 2 auf die GPU zugreifen? Gibt es Pläne, die Hardwareunterstützung auszuweiten?

Wir haben Unterstützung für den Zugriff auf die GPU innerhalb der WSL 2-Verteilungen veröffentlicht. Das bedeutet, dass Sie WSL jetzt leichter für Machine Learning-, KI- und Data Science-Szenarien mit großen Datasets verwenden können. Ein Tutorial für [die ersten Schritte mit GPU-Unterstützung finden Sie hier](./tutorials/gpu-compute). Ab sofort umfasst WSL 2 keine serielle Unterstützung oder Unterstützung für USB-Geräte. Wir untersuchen derzeit, wie sich diese Features am besten hinzufügen lassen.

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>Kann WSL 2 Netzwerkanwendungen verwenden?

Ja, in der Regel funktionieren Netzwerkanwendungen schneller und besser, da wir vollständige Kompatibilität der Systemaufrufe realisiert haben. Die neue Architektur verwendet jedoch virtualisierte Netzwerkkomponenten. Dies bedeutet, dass sich die anfänglichen Vorschaubuilds von WSL 2 eher ähnlich wie ein virtueller Computer verhalten, beispielsweise: WSL 2 weist eine andere IP-Adresse als der Hostcomputer auf. Wir arbeiten engagiert daran, dass sich WSL 2 genauso anfühlt wie WSL 1, und dazu gehören auch Verbesserungen unseres Netzwerkkonzepts. 

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>Kann ich WSL 2 auf einem virtuellen Computer ausführen?

Ja! Sie müssen sich vergewissern, dass für den virtuellen Computer verschachtelte Virtualisierung aktiviert ist. Dies kann auf Ihrem übergeordneten Hyper-V-Host aktiviert werden, indem Sie in einem PowerShell-Fenster mit Administratorberechtigungen den folgenden Befehl ausführen:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

Ersetzen Sie ‚&lt;VMName&gt;‘ durch den Namen des virtuellen Computers.

## <a name="can-i-use-wslconf-in-wsl-2"></a>Kann ich wsl.conf in WSL 2 verwenden?

WSL 2 unterstützt dieselbe wsl.conf-Datei, die von WSL 1 verwendet wird. Dies bedeutet, dass alle Konfigurationsoptionen, die Sie in einer WSL 1-Distribution festgelegt haben, z. B. das automatische Einbinden von Windows-Laufwerken, das Aktivieren oder Deaktivieren von Interop, das Ändern des Verzeichnisses, in dem Windows-Laufwerke bereitgestellt werden, auch in WSL 2 funktionieren. Weitere Informationen über die Konfigurationsoptionen in WSL finden Sie auf der Seite [Distributions-Management](./wsl-config.md).

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/
 [4]: https://blogs.vmware.com/workstation/2020/01/vmware-workstation-tech-preview-20h1.html
