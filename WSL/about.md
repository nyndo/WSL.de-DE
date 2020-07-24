---
title: Informationen zum Windows-Subsystem für Linux
description: Informieren Sie sich über das Windows-Subsystem für Linux, die verschiedenen Versionen und die Art und Weise, wie Sie sie verwenden können.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
ms.date: 05/12/2020
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ROBOTS: NOINDEX
ms.openlocfilehash: ddc242360adf67e3c5b6cd14d35fb6c869b83b2d
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948624"
---
# <a name="what-is-the-windows-subsystem-for-linux"></a><span data-ttu-id="75d42-104">Was ist das Windows-Subsystem für Linux?</span><span class="sxs-lookup"><span data-stu-id="75d42-104">What is the Windows Subsystem for Linux?</span></span>

<span data-ttu-id="75d42-105">Mit dem Windows-Subsystem für Linux können Entwickler eine GNU-/Linux-Umgebung (einschließlich der meisten Befehlszeilentools, Hilfsprogramme und Anwendungen) direkt unter Windows unverändert ausführen, ohne den Mehraufwand eines traditionellen virtuellen Computers oder eines Dual-Boot-Setups betreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="75d42-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a traditional virtual machine or dualboot setup.</span></span>

<span data-ttu-id="75d42-106">Sie haben folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="75d42-106">You can:</span></span>

* <span data-ttu-id="75d42-107">Wählen Sie Ihre bevorzugten GNU-/Linux -Distributionen aus dem [Microsoft Store](https://aka.ms/wslstore) aus.</span><span class="sxs-lookup"><span data-stu-id="75d42-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
* <span data-ttu-id="75d42-108">Führen Sie gängige Befehlszeilentools wie `grep`, `sed`, `awk` oder andere ELF-64-Binärdateien aus.</span><span class="sxs-lookup"><span data-stu-id="75d42-108">Run common command-line tools such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span>
* <span data-ttu-id="75d42-109">Führen Sie Skripts der Bash-Shell und GNU-/Linux-Befehlszeilenanwendungen aus, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="75d42-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="75d42-110">Tools: vim, emacs, tmux</span><span class="sxs-lookup"><span data-stu-id="75d42-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="75d42-111">Sprachen: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go usw.</span><span class="sxs-lookup"><span data-stu-id="75d42-111">Languages: [NodeJS](https://docs.microsoft.com/windows/nodejs/setup-on-wsl2), Javascript, [Python](https://docs.microsoft.com/windows/python/web-frameworks), Ruby, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="75d42-112">Dienste: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span><span class="sxs-lookup"><span data-stu-id="75d42-112">Services: SSHD, MySQL, Apache, lighttpd, [MongoDB](https://docs.microsoft.com/windows/nodejs/databases), [PostgreSQL](https://docs.microsoft.com/windows/python/databases).</span></span>
* <span data-ttu-id="75d42-113">Installieren Sie zusätzliche Software mit einem eigenen Paket-Manager für die GNU-/Linux-Distribution.</span><span class="sxs-lookup"><span data-stu-id="75d42-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
* <span data-ttu-id="75d42-114">Rufen Sie Windows-Anwendungen mithilfe einer Unix-ähnlichen Befehlszeilenshell auf.</span><span class="sxs-lookup"><span data-stu-id="75d42-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
* <span data-ttu-id="75d42-115">Rufen Sie GNU-/Linux-Anwendungen unter Windows auf.</span><span class="sxs-lookup"><span data-stu-id="75d42-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="what-is-wsl-2"></a><span data-ttu-id="75d42-116">Was ist WSL 2?</span><span class="sxs-lookup"><span data-stu-id="75d42-116">What is WSL 2?</span></span>

<span data-ttu-id="75d42-117">WSL 2 ist eine neue Version der Windows-Subsystem für Linux-Architektur, die es dem Windows-Subsystem für Linux ermöglicht, ELF64-Linux-Binärdateien unter Windows auszuführen.</span><span class="sxs-lookup"><span data-stu-id="75d42-117">WSL 2 is a new version of the Windows Subsystem for Linux architecture that powers the Windows Subsystem for Linux to run ELF64 Linux binaries on Windows.</span></span> <span data-ttu-id="75d42-118">Die Hauptziele sind eine **gesteigerte Leistung des Dateisystems** sowie das Hinzufügen **vollständiger Kompatibilität von Systemaufrufen**.</span><span class="sxs-lookup"><span data-stu-id="75d42-118">Its primary goals are to **increase file system performance**, as well as adding **full system call compatibility**.</span></span>

<span data-ttu-id="75d42-119">Diese neue Architektur führt zu einer Änderung der Interaktion dieser Linux-Binärdateien mit Windows und der Hardware Ihres Computers, bietet aber die gleiche Benutzererfahrung wie WSL 1 (die aktuelle, allgemein verfügbar Version).</span><span class="sxs-lookup"><span data-stu-id="75d42-119">This new architecture changes how these Linux binaries interact with Windows and your computer's hardware, but still provides the same user experience as in WSL 1 (the current widely available version).</span></span>

<span data-ttu-id="75d42-120">Einzelne Linux-Verteilungen können mit der WSL 1- oder der WSL 2-Architektur ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="75d42-120">Individual Linux distributions can be run with either the WSL 1 or WSL 2 architecture.</span></span> <span data-ttu-id="75d42-121">Für jede Verteilung kann jederzeit ein Upgrade oder Downgrade ausgeführt werden, und Sie können WSL 1- und WSL 2-Verteilungen parallel verwenden.</span><span class="sxs-lookup"><span data-stu-id="75d42-121">Each distribution can be upgraded or downgraded at any time and you can run WSL 1 and WSL 2 distributions side by side.</span></span> <span data-ttu-id="75d42-122">WSL 2 weist eine völlig neue Architektur auf, die von der Ausführung eines echten Linux-Kernels profitiert.</span><span class="sxs-lookup"><span data-stu-id="75d42-122">WSL 2 uses an entirely new architecture that benefits from running a real Linux kernel.</span></span>

## <a name="next-steps"></a><span data-ttu-id="75d42-123">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="75d42-123">Next steps</span></span>

* [<span data-ttu-id="75d42-124">Installieren von WSL 1 und Aktualisieren auf WSL 2</span><span class="sxs-lookup"><span data-stu-id="75d42-124">Install WSL 1 and update to WSL 2</span></span>](./install-win10.md)

* [<span data-ttu-id="75d42-125">Vergleich zwischen WSL 2 und WSL 1</span><span class="sxs-lookup"><span data-stu-id="75d42-125">Compare WSL 2 and WSL 1</span></span>](./compare-versions.md)

* [<span data-ttu-id="75d42-126">Erstellen eines Benutzerkontos und Kennworts für Ihre neue Linux-Verteilung</span><span class="sxs-lookup"><span data-stu-id="75d42-126">Create a user account and password for your new Linux distribution</span></span>](./user-support.md)

* [<span data-ttu-id="75d42-127">Häufig gestellte Fragen (FAQ)</span><span class="sxs-lookup"><span data-stu-id="75d42-127">Read Frequently Asked Questions</span></span>](./faq.md)

* [<span data-ttu-id="75d42-128">Häufig gestellte Fragen zu WSL 2</span><span class="sxs-lookup"><span data-stu-id="75d42-128">Read Frequently Asked Questions about WSL 2</span></span>](./wsl2-faq.md)

* [<span data-ttu-id="75d42-129">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="75d42-129">Troubleshooting</span></span>](./troubleshooting.md)

* [<span data-ttu-id="75d42-130">Ausführen von Interoperabilitätsbefehlen zwischen Windows und Linux</span><span class="sxs-lookup"><span data-stu-id="75d42-130">Run interoperability commands between Windows and Linux</span></span>](./interop.md)

* [<span data-ttu-id="75d42-131">Ausführen von Startbefehlen und Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="75d42-131">Run launch commands and configurations</span></span>](./wsl-config.md)

* [<span data-ttu-id="75d42-132">Einrichten von Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="75d42-132">Set up file permissions</span></span>](./file-permissions.md)

* [<span data-ttu-id="75d42-133">Einrichten von WSL für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="75d42-133">Set up WSL for Enterprise</span></span>](./enterprise.md)

* [<span data-ttu-id="75d42-134">Verweisen auf WSL-Befehle</span><span class="sxs-lookup"><span data-stu-id="75d42-134">Reference WSL commands</span></span>](./reference.md)

* [<span data-ttu-id="75d42-135">Erstellen von benutzerdefinierten Verteilungen</span><span class="sxs-lookup"><span data-stu-id="75d42-135">Build a custom distributions</span></span>](./build-custom-distro.md)

* [<span data-ttu-id="75d42-136">Lesen Sie die Anmerkungen zu dieser Version von WSL.</span><span class="sxs-lookup"><span data-stu-id="75d42-136">Read the WSL Release Notes</span></span>](./release-notes.md)
