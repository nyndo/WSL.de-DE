---
title: Informationen zum Windows-Subsystem für Linux
description: Informieren Sie sich über das Windows-Subsystem für Linux, die verschiedenen Versionen und die Art und Weise, wie Sie sie verwenden können.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 07/21/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.localizationpriority: high
ms.openlocfilehash: 512b5dc96892e2b66721e5e164301f2e9be6cd65
ms.sourcegitcommit: b494c8a76f867d69fa7fff4878c4e38140eaeb8a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2020
ms.locfileid: "87235454"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a>Was ist das Windows-Subsystem für Linux?

Mit dem Windows-Subsystem für Linux können Entwickler eine GNU-/Linux-Umgebung (einschließlich der meisten Befehlszeilentools, Hilfsprogramme und Anwendungen) direkt unter Windows unverändert ausführen, ohne den Mehraufwand eines traditionellen virtuellen Computers oder eines Dual-Boot-Setups betreiben zu müssen.

Sie haben folgende Möglichkeiten:

* Wählen Sie Ihre bevorzugten GNU-/Linux -Distributionen aus dem [Microsoft Store](https://aka.ms/wslstore) aus.
* Führen Sie gängige Befehlszeilentools wie `grep`, `sed`, `awk` oder andere ELF-64-Binärdateien aus.
* Führen Sie Skripts der Bash-Shell und GNU-/Linux-Befehlszeilenanwendungen aus, beispielsweise:  
    * Tools: vim, emacs, tmux
    * Sprachen: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go usw.
    * Dienste: SSHD, [MySQL](./tutorials/wsl-database.md), Apache, lighttpd, [MongoDB](./tutorials/wsl-database.md), [PostgreSQL](./tutorials/wsl-database.md).
* Installieren Sie zusätzliche Software mit einem eigenen Paket-Manager für die GNU-/Linux-Distribution.
* Rufen Sie Windows-Anwendungen mithilfe einer Unix-ähnlichen Befehlszeilenshell auf.
* Rufen Sie GNU-/Linux-Anwendungen unter Windows auf.

> [!div class="nextstepaction"]
> [Installieren von WSL](install-win10.md)

<br>

> [!VIDEO https://www.youtube.com/embed/48k317kOxqg]

## <a name="what-is-wsl-2"></a>Was ist WSL 2?

WSL 2 ist eine neue Version der Windows-Subsystem für Linux-Architektur, die es dem Windows-Subsystem für Linux ermöglicht, ELF64-Linux-Binärdateien unter Windows auszuführen. Die Hauptziele sind eine **gesteigerte Leistung des Dateisystems** sowie das Hinzufügen **vollständiger Kompatibilität von Systemaufrufen**.

Diese neue Architektur führt zu einer Änderung der Interaktion dieser Linux-Binärdateien mit Windows und der Hardware Ihres Computers, bietet aber die gleiche Benutzererfahrung wie WSL 1 (die aktuelle, allgemein verfügbar Version).

Einzelne Linux-Verteilungen können mit der WSL 1- oder der WSL 2-Architektur ausgeführt werden. Für jede Verteilung kann jederzeit ein Upgrade oder Downgrade ausgeführt werden, und Sie können WSL 1- und WSL 2-Verteilungen parallel verwenden. WSL 2 weist eine völlig neue Architektur auf, die von der Ausführung eines echten Linux-Kernels profitiert.

<br>

> [!VIDEO https://www.youtube.com/embed/MrZolfGm8Zk]

## <a name="next-steps"></a>Nächste Schritte

* [Installieren von WSL 1 und Aktualisieren auf WSL 2](./install-win10.md)

* [Vergleich zwischen WSL 2 und WSL 1](./compare-versions.md)

* [Erstellen eines Benutzerkontos und Kennworts für Ihre neue Linux-Verteilung](./user-support.md)

* [Häufig gestellte Fragen (FAQ)](./faq.md)

* [Häufig gestellte Fragen zu WSL 2](./wsl2-faq.md)

* [Problembehandlung](./troubleshooting.md)

* [Ausführen von Interoperabilitätsbefehlen zwischen Windows und Linux](./interop.md)

* [Ausführen von Startbefehlen und Konfigurationen](./wsl-config.md)

* [Einrichten von Dateiberechtigungen](./file-permissions.md)

* [Einrichten von WSL für Unternehmen](./enterprise.md)

* [Verweisen auf WSL-Befehle](./reference.md)

* [Erstellen von benutzerdefinierten Verteilungen](./build-custom-distro.md)

* [Lesen Sie die Anmerkungen zu dieser Version von WSL.](./release-notes.md)
