---
title: Übersicht über das Windows-Subsystem für Linux
description: Informieren Sie sich über das Windows-Subsystem für Linux, die verschiedenen Versionen und die Art und Weise, wie Sie sie verwenden können.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 75da6389beec4af7ac684ec7ee2ef31431e14071
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336063"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>Was ist das Windows-Subsystem für Linux?

Mit dem Windows-Subsystem für Linux können Entwickler eine GNU-/Linux-Umgebung (einschließlich der meisten Befehlszeilentools, Hilfsprogramme und Anwendungen) direkt unter Windows unverändert ausführen, ohne den Mehraufwand eines traditionellen virtuellen Computers oder eines Dual-Boot-Setups betreiben zu müssen.

Sie haben folgende Möglichkeiten:

* Wählen Sie Ihre bevorzugten GNU-/Linux -Distributionen aus dem [Microsoft Store](https://aka.ms/wslstore) aus.
* Führen Sie gängige Befehlszeilentools wie `grep`, `sed`, `awk` oder andere ELF-64-Binärdateien aus.
* Führen Sie Skripts der Bash-Shell und GNU-/Linux-Befehlszeilenanwendungen aus, beispielsweise:  
    * Tools: vim, emacs, tmux
    * Sprachen: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go usw.
    * Dienste: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).
* Installieren Sie zusätzliche Software mit einem eigenen Paket-Manager für die GNU-/Linux-Distribution.
* Rufen Sie Windows-Anwendungen mithilfe einer Unix-ähnlichen Befehlszeilenshell auf.
* Rufen Sie GNU-/Linux-Anwendungen unter Windows auf.

## <a name="what-is-wsl-2"></a>Was ist WSL 2?

WSL 2 ist eine neue Version der Windows-Subsystem für Linux-Architektur, die es dem Windows-Subsystem für Linux ermöglicht, ELF64-Linux-Binärdateien unter Windows auszuführen. Die Hauptziele sind eine **gesteigerte Leistung des Dateisystems** sowie das Hinzufügen **vollständiger Kompatibilität von Systemaufrufen**.

Diese neue Architektur führt zu einer Änderung der Interaktion dieser Linux-Binärdateien mit Windows und der Hardware Ihres Computers, bietet aber die gleiche Benutzererfahrung wie WSL 1 (die aktuelle, allgemein verfügbar Version).

Einzelne Linux-Distributionen können mit der WSL 1- oder der WSL 2-Architektur ausgeführt werden. Für jede Distribution kann jederzeit ein Upgrade oder Downgrade ausgeführt werden, und Sie können WSL 1- und WSL 2-Distributionen parallel verwenden. WSL 2 weist eine völlig neue Architektur auf, die von der Ausführung eines echten Linux-Kernels profitiert.

## <a name="next-steps"></a>Nächste Schritte

* [Installieren von WSL 1 und Aktualisieren auf WSL 2](./install-win10.md)

* [Vergleich zwischen WSL 2 und WSL 1](./compare-versions.md)

* [Erstellen eines Benutzerkontos und Kennworts für Ihre neue Linux-Distribution](./user-support.md)

* [Häufig gestellte Fragen (FAQ)](./faq.md)

* [Häufig gestellte Fragen zu WSL 2](./wsl2-faq.md)

* [Problembehandlung](./troubleshooting.md)

* [Ausführen von Interoperabilitätsbefehlen zwischen Windows und Linux](./interop.md)

* [Ausführen von Startbefehlen und Konfigurationen](./wsl-config.md)

* [Einrichten von Dateiberechtigungen](./file-permissions.md)

* [Einrichten von WSL für Unternehmen](./enterprise.md)

* [Verweisen auf WSL-Befehle](./reference.md)

* [Erstellen von benutzerdefinierten Distributionen](./build-custom-distro.md)

* [Lesen Sie die Anmerkungen zu dieser Version von WSL.](./release-notes.md)
