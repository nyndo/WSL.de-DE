---
title: Anmerkungen zu dieser Version des Windows-Subsystems für Linux
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux. Diese Versionsanmerkungen enthalten behobene Probleme und werden wöchentlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: c158cffde1c6f680f833b9f7e84f2d494ba64b78
ms.sourcegitcommit: e2d586925b314ce4517773b9c78736450a9f75d9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "97977125"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>Anmerkungen zu dieser Version des Windows-Subsystems für Linux

## <a name="build-21286"></a>Build 21286
Allgemeine Windows-Informationen zu Build 21286 finden Sie im [Windows-Blog](https://blogs.windows.com/windows-insider/2021/01/06/announcing-windows-10-insider-preview-build-21286/).

* Eine Option „boot.command“ wurde in „/etc/wsl.conf“ hinzugefügt, um Startbefehle zu aktivieren.
* Der Befehl „wsl.exe --cd“ wurde eingeführt, um das aktuelle Arbeitsverzeichnis eines Befehls festzulegen.
* Die Zuordnung von NTSTATUS zu Linux-Fehlercodes wurde verbessert. [GH 6063]
* Die „wsl.exe --mount“-Fehlerberichterstattung wurde verbessert.

## <a name="build-20226"></a>Build 20226
Allgemeine Windows-Informationen zu Build 20226 finden Sie im [Windows-Blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20226/).

* Beheben der Ursache für einen Absturz im LxssManager-Dienst. [GH 5902]

## <a name="build-20211"></a>Build 20211
Allgemeine Windows-Informationen zu Build 20211 finden Sie im [Windows-Blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).

* Stellen Sie `wsl.exe --mount` bereit, um physische oder virtuelle Datenträger bereitzustellen. Weitere Informationen finden Sie unter [Zugreifen auf Linux-Dateisysteme in Windows und WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).
* Fix für den Absturz des LxssManager-Diensts beim Überprüfen, ob die VM im Leerlauf ist. [GH 5768]
* Unterstützung für komprimierte VHD-Dateien. [GH 4103]
* Stellen Sie sicher, dass die unter „C:\windows\system32\lxss\lib“ installierte Linux-Benutzermodusbibliotheken bei Betriebssystemupgrades erhalten bleiben. [GH 5848]
* Die Möglichkeit zum Auflisten verfügbarer Verteilungen, die mit `wsl --install --list-distributions` installiert werden können, wurde hinzugefügt.
* WSL-Instanzen werden nun beendet, wenn sich der Benutzer abmeldet.

## <a name="build-20190"></a>Build 20190
Allgemeine Windows-Informationen zu Build 20190 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).

* Fehler behoben, der den Start von WSL1-Instanzen verhinderte. [GH 5633]
* Hängenbleiben beim Umleiten der Windows-Prozessausgabe behoben. [GH 5648]
* Option „%userprofile%\\.wslconfig“ zur Steuerung des VM-Leerlauftimeouts (wsl2.vmIdleTimeout=<Zeit_in_ms>) hinzugefügt.
* Unterstützung für das Starten von App-Ausführungsaliasen von WSL.
* Unterstützung für die Installation des WSL2-Kernels und der Verteilungen zu „wsl.exe --install“ hinzugefügt.

## <a name="build-20175"></a>Build 20175
Allgemeine Windows-Informationen zu Build 20175 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).

* Passen Sie die Standardspeicherzuweisung der WSL2-VM so an, dass sie 50 % des Hostspeichers oder 8 GB beträgt, je nachdem, welcher Wert kleiner ist [GH 4166].
* Ändern Sie das \\\\wsl$-Präfix in \\\\wsl, um die URI-Analyse zu unterstützen. Der alte \\\\wsl$-Pfad wird weiterhin unterstützt.
* Aktivieren Sie die geschachtelte Virtualisierung für WSL2 standardmäßig auf amd64. Sie können dies über „%userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false)“ deaktivieren.
* Lassen Sie die wsl.exe --update-Anforderung Microsoft Update starten.
* Unterstützen Sie die Umbenennung über eine schreibgeschützte Datei in DrvFs.
* Stellen Sie sicher, dass Fehlermeldungen immer in der richtigen Codepage ausgegeben werden.

## <a name="build-20150"></a>Build 20150
Allgemeine Windows-Informationen zu Build 20150 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).

* Informationen zu WSL2 GPU Compute finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).
* Führen Sie die Befehlszeilenoption „wsl.exe --install“ zum einfachen Einrichten von WSL ein.
* Führen Sie die Befehlszeilenoption „wsl.exe --update“ zum Verwalten von Updates für den WSL2-Kernel ein. 
* Legen Sie WSL2 als Standard fest.
* Erhöhen Sie das Timeout für das kontrollierte Beenden der WSL2-VM.
* Korrigieren Sie die virtio-9p-Racebedingung beim Zuordnen des Gerätespeichers.
* Führen Sie keinen 9p-Server mit erhöhten Rechten aus, wenn UAC deaktiviert ist.

## <a name="build-19640"></a>Build 19640
Allgemeine Windows-Informationen zu Build 19640 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).

* [WSL2] Stabilitätsverbesserungen für virtio-9p (drvfs).

## <a name="build-19555"></a>Build 19555
Allgemeine Windows-Informationen zu Build 19555 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).

* [WSL2] Verwenden einer Arbeitsspeicher-cgroup, um den von Installations- und Konvertierungsvorgängen verwendeten Speicherplatz zu begrenzen [GH 4669]
* Verfügbarmachen von „wsl.exe“, wenn die optionale Komponente „Windows-Subsystem für Linux“ (WSL) nicht aktiviert ist, um die Auffindbarkeit von Features zu verbessern.
* Ändern von „wsl.exe“, um Hilfetext auszugeben, wenn die optionale Komponente WSL nicht installiert ist
* Fehlerbehebung für die Racebedingung beim Erstellen von Instanzen
* Erstellen von „wslclient.dll“ mit allen Befehlszeilenfunktionen
* Verhindern eines Absturzes bei angehaltenem LxssManagerUser-Dienst
* Fehlerbehebung für ein wslapi.dll-Fast-Fail, wenn der distroName-Parameter NULL ist

## <a name="build-19041"></a>Build 19041
Allgemeine Windows-Informationen zu Build 19041 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).

* [WSL2] Löschen der Signalmaske vor dem Starten der Prozesse
* [WSL2] Aktualisieren des Linux-Kernels auf 4.19.84
* Verarbeiten der Erstellung der symbolischen Verknüpfung „/etc/resolv.conf“, wenn die symbolische Verknüpfung nicht relativ ist

## <a name="build-19028"></a>Build 19028
Allgemeine Windows-Informationen zu Build 19028 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).

* [WSL2] Aktualisieren des Linux-Kernels auf 4.19.81
* [WSL2] Ändern der Standardberechtigung von /dev/net/tun in 0666 [GH 4629]
* [WSL2] Optimieren der Standard-Arbeitsspeichergröße, die dem virtuellen Linux-Computer zugewiesen ist, auf 80% des Hostarbeitsspeichers
* [WSL2] Fehlerbehebung für den Interop-Server, um Anforderungen mit einem Timeout zu verarbeiten, damit sich der Server bei ungültigen Aufrufern nicht aufhängt

## <a name="build-19018"></a>Build 19018
Allgemeine Windows-Informationen zu Build 19018 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).

* [WSL2] Verwenden Sie cache=mmap als Standardeinstellung für 9p-Einbindungen, um Probleme mit Dotnet-Apps zu beheben
* [WSL2] Korrekturen für localhost-Relay [GH 4340]
* [WSL2] Einführen einer distributionsübergreifenden, gemeinsam genutzten tmpfs-Einbindung für den Freigabezustand zwischen Distributionen
* Korrektur der Wiederherstellung des permanenten Netzwerklaufwerks für \\\\wsl$

## <a name="build-19013"></a>Build 19013
Allgemeine Windows-Informationen zu Build 19013 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).

* [WSL2] Verbesserte Arbeitsspeicherleistung der VM des WSL-Hilfsprogramms Arbeitsspeicher, der nicht mehr verwendet wird, wird an den Host zurückgegeben.
* [WSL2] Aktualisieren der Kernelversion auf 4.19.79 (CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK und CONFIG_BRIDGE_VLAN_FILTERING hinzugefügt).
* [WSL2] Korrigiertes Eingaberelay zur Behandlung von Fällen, in denen stdin ein nicht geschlossenes Pipehandle ist [GH 4424]
* Die Überprüfung auf \\\\wsl$ unterscheidet nicht mehr zwischen Groß- und Kleinschreibung.
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a>Build 19002
Allgemeine Windows-Informationen zu Build 19002 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).

* [WSL] Beheben von Problemen bei der Behandlung einiger Unicode-Zeichen: https://github.com/microsoft/terminal/issues/2770
* [WSL] Korrektur seltener Fälle, in denen die Registrierung von Distributionen aufgehoben werden kann, wenn sie unmittelbar nach einem Build-zu-Build-Upgrade gestartet werden.
* [WSL] Korrektur eines kleinen Problems beim Herunterfahren mit „wsl.exe“, bei dem Leerlaufzeitgeber von Instanzen nicht abgebrochen wurden.

## <a name="build-18995"></a>Build 18995
Allgemeine Windows-Informationen zu Build 18995 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).

* [WSL2] Korrektur eines Problems, bei dem DrvFs-Einbindungen nach dem Abbruch eines Vorgangs (z.B. STRG-C) zu funktionieren aufhörten [GH 4377]
* [WSL2] Korrektur der Verarbeitung sehr großer hvsocket-Nachrichten [GH 4105]
* [WSL2] Korrektur eines Interop-Problems, wenn stdin eine Datei ist [GH 4475]
* [WSL2] Korrektur eines Absturzes, wenn ein unerwarteter Netzwerkstatus festgestellt wird [GH 4474]
* [WSL2] Abfragen des Namens der Distribution beim Interopserver, wenn der aktuelle Prozess nicht über die Umgebungsvariable verfügt
* [WSL2] Korrektur eines Interop-Problems, wenn stdin eine Datei ist
* [WSL2] Aktualisieren der Linux-Kernelversion auf 4.19.72
* [WSL2] Neu hinzugefügte Möglichkeit zum Angeben weiterer Kernelbefehle in der Befehlszeile mithilfe von WSLCONFIG
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a>Build 18990
Allgemeine Windows-Informationen zu Build 18990 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).

* Verbesserte Leistung für Verzeichnisauflistungen in \\\\wsl$
* [WSL2] Einführen zusätzlicher Entropie beim Systemstart [GH 4416]
* [WSL2] Problembehebung für Windows-Interop bei der Verwendung von „su“ / „sudo“ [GH 4465]

## <a name="build-18980"></a>Build 18980
Allgemeine Windows-Informationen zu Build 18980 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).

* Korrektur des Lesen von symbolischen Verknüpfungen, die FILE_READ_DATA verweigern. Dies umfasst alle symbolischen Verknüpfungen, die von Windows aus Gründen der Abwärtskompatibilität erstellt werden, z.B. „C:\Dokumente und Einstellungen“ und eine Reihe von symbolischen Verknüpfungen im Benutzerprofilverzeichnis.
* Festlegen eines unerwarteten Dateisystemzustands als nicht schwerwiegend [GH 4334, 4305]
* [WSL2] Hinzufügen von Unterstützung für arm64, wenn Ihre CPU/Firmware Virtualisierung unterstützt
* [WSL2] Zulassen der Anzeige von Kernelprotokollen durch nicht berechtigte Benutzer
* [WSL2] Korrigieren des Ausgaberelays, wenn stdout/stderr-Sockets geschlossen wurden [GH 4375]
* [WSL2] Unterstützung von Akku- und AC-Adapter-Passthrough
* [WSL2] Aktualisieren des Linux-Kernels auf 4.19.67
* Hinzufügen der Möglichkeit, den Standardbenutzernamen in „/etc/wsl.conf“ festzulegen:
```
[user]
default=<string>
```

## <a name="build-18975"></a>Build 18975
Allgemeine Windows-Informationen zu Build 18975 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).

* [WSL2] Korrektur einer Reihe von Problemen mit der localhost-Zuverlässigkeit [GH 4340]

## <a name="build-18970"></a>Build 18970
Allgemeine Windows-Informationen zu Build 18970 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).

* [WSL2] Synchronisierung der Uhrzeit mit der Hostzeit, wenn das System nach dem Ruhezustand fortgesetzt wird [GH 4245]
* [WSL2] Nach Möglichkeit Erstellen symbolischer NT-Verknüpfungen auf den Windows-Volumes
* [WSL2] Erstellen von Distributionen in den UTS-, IPC-, PID- und Mount-Namespaces.
* [WSL2] Korrigieren des localhost-Portrelays, wenn der Server direkt an localhost gebunden wird [GH 4353]
* [WSL2] Korrigieren von Interop, wenn die Ausgabe umgeleitet wird [GH 4337]
* [WSL2] Unterstützung der Übersetzung absoluter symbolischer NT-Verknüpfungen.
* [WSL2] Aktualisieren des Kernels auf 4.19.59
* [WSL2] Ordnungsgemäße Festlegung der Subnetzmaske für eth0.
* [WSL2] Ändern der Logik, um die Konsolenworkerschleife zu verlassen, wenn das Beendigungsereignis signalisiert wird.
* [WSL2] Auswerfen der Distributions-VHD, wenn die Distribution nicht ausgeführt wird.
* [WSL2] Korrigieren der Analysebibliothek, um leere Werte ordnungsgemäß zu verarbeiten.
* [WSL2] Unterstützung von Docker Desktop durch Erstellen von distributionsübergreifenden Einbindungen. Dieses Verhalten kann durch eine Distribution übernommen werden, indem die folgende Zeile der Datei „/etc/wsl.conf“ hinzugefügt wird:
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a>Build 18945
Allgemeine Windows-Informationen zu Build 18945 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).

### <a name="wsl"></a>WSL
* [WSL2] Zulassen, dass der Zugriff auf lauschende TCP-Sockets in WSL2 über „localhost:port“ vom Host erfolgen kann.
* [WSL2] Korrekturen für Installations- und Konvertierungsfehler und zusätzliche Diagnose zur Nachverfolgung zukünftiger Probleme [GH 4105] 
* [WSL2] Verbessern der Diagnose von WSL2-Netzwerkproblemen
* [WSL2] Aktualisieren der Kernelversion auf 4.19.55
* [WSL2] Aktualisieren des Kernels mit Konfigurationsoptionen, die für Docker erforderlich sind [GH 4165]
* [WSL2] Erhöhen der Anzahl der CPUs, die der Lightweight Utility-VM zugeordnet sind, um eine mit dem Host identische Anzahl zu erreichen (wurde zuvor durch CONFIG_NR_CPUS in der Kernelkonfiguration auf 8 begrenzt) [GH 4137]
* [WSL2] Erstellen einer Auslagerungsdatei für die WSL2-Lightweight-VM
* [WSL2] Zulassen, dass Benutzereinbindungen über die \\\\wsl$\\-Distribution (z.B. sshfs) sichtbar sind [GH 4172]
* [WSL2] Verbessern der Leistung des 9P-Dateisystems
* [WSL2] Sicherstellen, dass die VHD-ACL nicht unbegrenzt anwächst [GH 4126]
* [WSL2] Aktualisieren der Kernelkonfiguration für die Unterstützung von squashfs und xt_conntrack [GH 4107, 4123]
* [WSL2] Korrektur für interopaktivierte „/etc/wsl.conf“-Option [GH 4140]
* [WSL2] Rückgabe von ENOTSUP, wenn das Dateisystem EAS nicht unterstützt
* [WSL2] Korrigieren von CopyFile-Hänger mit \\\\wsl$
* Umschalten von Standard-umask in 0022 und Hinzufügen der filesystem.umask-Einstellung zu „/etc/wsl.conf“
* Korrigieren von wslpath, um symbolische Verknüpfungen ordnungsgemäß aufzulösen, dies wurde in 19h1 zurückgesetzt [GH 4078]
* Einführung der Datei „%UserProfile%\\.wslconfig“ für die Optimierung der WSL2-Einstellungen
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a>Build 18917
Allgemeine Windows-Informationen zu Build 18917 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).

### <a name="wsl"></a>WSL
* WSL 2 ist Jetzt verfügbar! Weitere Informationen finden Sie im [Blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).
* Korrektur einer Regression, bei der das Starten von Windows-Prozessen über symbolische Verknüpfungen nicht ordnungsgemäß funktioniert hat [GH 3999]
* Hinzufügen der Optionen wsl.exe --list --verbose, wsl.exe --list --quiet und wsl.exe --import --version zu „wsl.exe“
* Hinzufügen der Option wsl.exe --shutdown
* Plan 9: Zulassen des Öffnend eines Verzeichnisses für einen erfolgreichen Schreibvorgang

## <a name="build-18890"></a>Build 18890
Allgemeine Windows-Informationen zu Build 18890 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).

### <a name="wsl"></a>WSL
* Nicht blockierender Socketverlust [GH 2913]
* EOF-Eingabe für Terminal kann nachfolgende Lesevorgänge blockieren [GH 3421]
* Aktualisieren des resolv.conf-Headers, damit er auf „wsl.conf“ verweist [in GH 3928 beschrieben].
* Deadlock im epoll-Löschcode [GH 3922]
* Verarbeiten von Leerzeichen in Argumenten für --import und --export [GH 3932]
* Erweitern von mit mmap behandelten Dateien funktioniert nicht ordnungsgemäß [GH 3939]
* Korrektur eines Problems mit ARM64 \\\\wsl$-Zugriff funktioniert nicht ordnungsgemäß
* Hinzufügen eines besseren Standardsymbols für „wsl.exe“

## <a name="build-18342"></a>Build 18342
Allgemeine Windows-Informationen zu Build 18342 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).

### <a name="wsl"></a>WSL
* Wir haben für Benutzer die Möglichkeit hinzugefügt, auf Linux-Dateien in einer WSL-Distribution aus Windows zuzugreifen. Auf diese Dateien kann über die Befehlszeile zugegriffen werden. Außerdem können Windows-Apps wie der Datei-Explorer, VSCode usw. mit diesen Dateien interagieren. Greifen Sie auf Ihre Dateien zu, indem Sie zu \\\\wsl$\\<distributions_name> navigieren, oder zeigen Sie eine Liste der ausgeführten Distributionen an, indem Sie zu \\\\wsl$ navigieren.
* Hinzufügen zusätzlicher CPU-Infotags und Korrigieren der Cpus_allowed[_list]-Werte [GH 2234]
* Unterstützung der Ausführung aus Nicht-Leaderthread [GH 3800]
* Behandeln von Konfigurationsupdatefehlern als nicht schwerwiegend [GH 3785]
* Aktualisieren von binfmt für die ordnungsgemäße Verarbeitung von Offsets [GH 3768]
* Aktivieren der Zuordnung von Netzlaufwerken für Plan 9 [GH 3854]
* Unterstützung von Windows -> Linux und Linux -> Windows-Pfadübersetzung für Bindungseinbindungen
* Erstellen schreibgeschützter Abschnitte für Zuordnungen für Dateien, die schreibgeschützt geöffnet sind

## <a name="build-18334"></a>Build 18334
Allgemeine Windows-Informationen zu Build 18334 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).

### <a name="wsl"></a>WSL
* Umgestalten der Art und Weise, in der die Windows-Zeitzone einer Linux-Zeitzone zugeordnet wird [GH 3747]
* Beheben von Speicherverlusten und Hinzufügen neuer Zeichenfolgenübersetzungsfunktionen [GH 3746]
* SIGCONT für eine Threadgruppe ohne Threads ist eine Nulloperation [GH 3741] 
* Richtige Anzeige von Socket- und Epoll-Dateideskriptoren in „/proc/self/fd“

## <a name="build-18305"></a>Build 18305
Allgemeine Windows-Informationen zu Build 18305 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).

### <a name="wsl"></a>WSL
* pthreads verlieren den Zugriff auf Dateien, wenn der primäre Thread beendet wird [GH 3589]
* TIOCSCTTY sollte den Parameter „force“ ignorieren, wenn er nicht erforderlich ist [GH 3652]
* Verbesserungen an der Befehlszeile von „wsl.exe“ und Hinzufügung von Import-/Exportfunktionen.
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a>Build 18277
Allgemeine Windows-Informationen zu Build 18277 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).

### <a name="wsl"></a>WSL
* Korrektur des Fehlers „no such interface supported“ in Build 18272 [GH 3645]
* Ignorieren des MNT_FORCE-Flags für Systemaufruf zum Aufheben der Einbindung [GH 3605]
* Umschalten von WSL-Interop für die Verwendung der offiziellen CreatePseudoConsole-API
* Keinen Timeoutwert beibehalten, wenn FUTEX_WAIT neu gestartet wird

## <a name="build-18272"></a>Build 18272
Allgemeine Windows-Informationen zu Build 18272 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).

### <a name="wsl"></a>WSL
* **WARNUNG:** In diesem Build liegt ein Problem vor, durch das WSL nicht funktionsfähig wird. Wenn Sie versuchen, die Verteilung zu starten, wird der Fehler „Schnittstelle nicht unterstützt“ angezeigt. Das Problem wurde behoben und ist im Insider Fast-Build der nächsten Woche nicht mehr enthalten. Wenn Sie diesen Build installiert haben, können Sie ein Rollback auf den vorherigen Windows-Build durchführen, indem Sie unter „Einstellungen > Update und Sicherheit > Wiederherstellung“ die Option „Zur vorherigen Version von Windows 10 zurückkehren“ auswählen.

## <a name="build-18267"></a>Build 18267
Allgemeine Windows-Informationen zu Build 18267 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).

### <a name="wsl"></a>WSL
* Korrektur eines Problems, bei dem der Zombieprozess möglicherweise nicht beendet und unbegrenzt ausgeführt wird.
* WslRegisterDistribution hängt, wenn die Fehlermeldung die maximale Länge überschreitet [GH 3592]
* Zulassen der erfolgreichen Ausführung von fsync für schreibgeschützte Dateien auf DrvFs [GH 3556]
* Sicherstellen, dass die Verzeichnisse „/bin“ und „/sbin“ vorhanden sind, bevor symbolische Verknüpfungen darin erstellt werden [GH 3584]
* Hinzufügen eines Instanztimeoutmechanismus für WSL-Instanzen. Der Timeoutwert ist derzeit auf 15 Sekunden festgelegt. Das bedeutet, dass die Instanz 15 Sekunden nach Beendigung des letzten WSL-Prozesses beendet wird. Um eine Distribution sofort zu beenden, verwenden Sie Folgendes:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>Build 17763 (1809)
Allgemeine Windows-Informationen zu Build 17763 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).

### <a name="wsl"></a>WSL
* Berechtigungsüberprüfung für Setpriority-Systemaufruf ist zu streng, um die gleiche Threadpriorität zu ändern[GH 1838].
* Stellen Sie sicher, dass die unbeeinflusste Interruptzeit für die Startzeit verwendet wird, um zu vermeiden, dass negative Werte für clock_gettime (CLOCK_BOOTTIME) zurückgegeben werden [GH 3434]
* Verarbeiten von symbolischen Verknüpfungen im WSL-binfmt-Interpreter [GH 3424]
* Bessere Verarbeitung der Bereinigung des Threadgruppen-Leaderdateideskriptors.
* Umschalten von WSL für die Verwendung von KeQueryInterruptTimePrecise anstelle von KeQueryPerformanceCounter zur Vermeidung eines Überlaufs [GH 3252].
* Ptrace-Anfügevorgang kann zu einem ungültigen Rückgabewert von Systemaufrufen führen [GH 1731]
* Korrektur mehrerer Probleme, die sich auf AF_UNIX beziehen [GH 3371]
* Korrektur eines Problems, das dazu führen kann, dass WSL-Interop fehlschlägt, wenn das aktuelle Arbeitsverzeichnis weniger als 5 Zeichen lang ist [GH 3379]
* Vermeiden von einer Sekunde Verzögerung bei Ausfall von Loopbackverbindungen mit nicht vorhandenen Ports [GH 3286]
* Hinzufügen der Stubdatei „/proc/sys/fs/file-max“ [GH 2893]
* Genauere IPv6-Bereichsinformationen.
* PR_SET_PTRACER-Unterstützung [GH 3053]
* Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]
* Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]
* Verbesserte Zombieunterstützung [GH 1353]
* Hinzufügen von wsl.conf-Einträgen zum Steuern des Windows-Interop-Verhaltens [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Korrektur des Verhaltens, dass getsockname nicht immer den Porduktfamilientyp des UNIX-Sockets zurückgibt [GH 1774]
* Hinzufügen von Unterstützung für TIOCSTI [GH 1863]
* Nicht blockierende Sockets beim Verbindungsaufbau sollten für Schreibversuche EAGAIN zurückgeben [GH 2846]
* Unterstützung von Interop auf eingebundenen VHDs [GH 3246, 3291]
* Korrektur von Problem mit der Berechtigungsüberprüfung im Stammordner [GH 3304]
* Eingeschränkte Unterstützung für die TTY-Tastatur-ioctls KDGKBTYPE, KDGKBMODE und KDSKBMODE.
* Windows-UI-Apps sollten ausgeführt selbst dann werden, wenn Sie im Hintergrund gestartet werden.
* Hinzufügen der Option wsl -u oder--user [GH 1203]
* Korrektur von WSL-Startproblemen, wenn der Schnellstart aktiviert ist [GH 2576]
* Unix-Sockets müssen getrennte Peeranmelde Informationen beibehalten [GH 3183]
* Nicht blockierende Unix-Sockets, die unbegrenzt EAGAIN-Fehler ausgeben [GH 3191]
* case=off ist der neue standardmäßige drvfs-Einbindungstyp [GH 2937, 3212, 3328]
    * Weitere Informationen finden Sie im [Blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).
* Hinzufügen von wslconfig/terminate zum Beenden ausgeführter Distributionen
* Korrektur des Problems mit den Kontextmenüeinträgen der WSL-Shell, die Pfade mit Leerzeichen nicht ordnungsgemäß behandeln.
* Bereitstellen von Unterscheidung von Groß-/Kleinschreibung pro Verzeichnis als erweitertes Attribut
* ARM64: Emulieren von Cacheverwaltungsvorgängen. Beheben von [dotnet-Problem](https://github.com/dotnet/core/issues/1561).
* DrvFs: Nur Escapezeichen im privaten Bereich, die einem mit Escapezeichen versehenen Zeichen entsprechen.
* Korrektur eines Off-by-one-Fehlers in der Längenüberprüfung des ELF Parserinterpreters [GH 3154].
* Absolute WSL-Timer mit einer Zeitangabe in der Vergangenheit werden nicht ausgelöst [GH 3091]
* Sicherstellen, dass neu erstellte Analysepunkte als solche im übergeordneten Verzeichnis aufgelistet werden.
* Atomarisches Erstellen von Verzeichnissen mit Berücksichtigung von Groß- und Kleinschreibung in DrvFs.
* Korrektur eines zusätzlichen Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist. [GH 2712]
* Korrektur eines WSL-Startfehlers, wenn UMCI aktiviert ist.- [GH 3020]
* Hinzufügen des Explorer-Kontextmenüs zum Starten von WSL [GH 437, 603, 1836]. Halten Sie in einem Explorer-Fenster die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste, um diese Option zu verwenden.
* Korrektur des nicht blockierenden UNIX-Socketverhaltens [GH 2822, 3100]
* Korrigieren des hängenden NETLINK-Befehls, wie in GH 2026 gemeldet.
* Hinzufügen von Unterstützung für Einbindungsweitergabeflags [GH 2911]
* Korrektur von Problem mit truncate, das keine inotify-Ereignisse verursacht [GH 2978].
* Hinzufügen der Option --exec für „wsl.exe“ zum Aufrufen eine einzelne Binärdatei ohne Shell.
* Hinzufügen der Option --distribution für „wsl.exe“, um eine bestimmte Distribution auszuwählen.
* Eingeschränkte Unterstützung für dmesg. Anwendungen können sich jetzt in dmesg protokollieren. Der WSL-Treiber protokolliert eingeschränkte Informationen in dmesg. In Zukunft kann dies so erweitert werden, dass andere Informationen/Diagnoseinhalte vom Treiber erfasst werden.
    * Hinweis: dmesg wird derzeit über die `/dev/kmsg`-Geräteschnittstelle unterstützt. `syslog`-Systemaufrufschnittstelle wird noch nicht unterstützt. Daher funktionieren einige der `dmesg`-Befehlszeilenoptionen (z.B. `-S`, `-C`) nicht.
* Änderung der Standard-GID und des Modus von seriellen Geräten entsprechend den nativen Einstellungen [GH 3042]
* DrvFs unterstützt jetzt erweiterte Attribute.
    * Hinweis: Für DrvFs gelten einige Einschränkungen für den Namen erweiterter Attribute. Einige Zeichen (etwa „/“, „:“ und „\*“) sind unzulässig, und für Namen erweiterter Attribute wird in DrvFs keine Groß- und Kleinschreibung beachtet.

## <a name="build-18252-skip-ahead"></a>Build 18252 (Skip Ahead)
Allgemeine Windows-Informationen zu Build 18252 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).

### <a name="wsl"></a>WSL
* Verschieben von init- und bsdtar-Binärdateien aus der lxssmanager-DLL in einen separaten Toolsordner
* Korrektur von Racebedingung um schließenden Dateideskriptor bei Verwendung von CLONE_FILES
* Verarbeiten optionaler Felder in „/proc/pid/mountinfo“ bei der Übersetzung von DrvFs-Pfaden
* Zulassen, dass DrvFs mklod ohne Metadatenunterstützung für S_IFREG erfolgreich ist
* Für schreibgeschützte Dateien, die auf DrvFs erstellt wurden, muss das schreibgeschützte Attribut festgelegt werden [GH 3411]
* Hinzufügen von /sbin/mount.drvfs-Hilfsprogramm zur Verarbeitung der DrvFs-Einbindung
* Verwenden der POSIX-Umbenennung in DrvFs.
* Ermöglichen der Pfadübersetzung für Volumes ohne Volume-GUID.

## <a name="build-17738-fast"></a>Build 17738 (Fast)
Allgemeine Windows-Informationen zu Build 17738 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).

### <a name="wsl"></a>WSL
* Berechtigungsüberprüfung für Setpriority-Systemaufruf ist zu streng, um die gleiche Threadpriorität zu ändern[GH 1838].
* Stellen Sie sicher, dass die unbeeinflusste Interruptzeit für die Startzeit verwendet wird, um zu vermeiden, dass negative Werte für clock_gettime (CLOCK_BOOTTIME) zurückgegeben werden [GH 3434]
* Verarbeiten von symbolischen Verknüpfungen im WSL-binfmt-Interpreter [GH 3424]
* Bessere Verarbeitung der Bereinigung des Threadgruppen-Leaderdateideskriptors.

## <a name="build-17728-fast"></a>Build 17728 (Fast)
Allgemeine Windows-Informationen zu Build 17728 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).

### <a name="wsl"></a>WSL
* Umschalten von WSL für die Verwendung von KeQueryInterruptTimePrecise anstelle von KeQueryPerformanceCounter zur Vermeidung eines Überlaufs [GH 3252].
* Ptrace-Anfügevorgang kann zu einem ungültigen Rückgabewert von Systemaufrufen führen [GH 1731]
* Korrektur mehrerer Probleme, die sich auf AF_UNIX beziehen [GH 3371]
* Korrektur eines Problems, das dazu führen kann, dass WSL-Interop fehlschlägt, wenn das aktuelle Arbeitsverzeichnis weniger als 5 Zeichen lang ist [GH 3379]

## <a name="build-18204-skip-ahead"></a>Build 18204 (Skip Ahead)
Allgemeine Windows-Informationen zu Build 18204 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]
* Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]

## <a name="build-17723-fast"></a>Build 17723 (Fast)
Allgemeine Windows-Informationen zu Build 17723 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).

### <a name="wsl"></a>WSL
* Vermeiden von einer Sekunde Verzögerung bei Ausfall von Loopbackverbindungen mit nicht vorhandenen Ports [GH 3286]
* Hinzufügen der Stubdatei „/proc/sys/fs/file-max“ [GH 2893]
* Genauere IPv6-Bereichsinformationen.
* PR_SET_PTRACER-Unterstützung [GH 3053]
* Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]
* Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]

## <a name="build-17713"></a>Build 17713
Allgemeine Windows-Informationen zu Build 17713 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).

### <a name="wsl"></a>WSL
* Verbesserte Zombieunterstützung [GH 1353]
* Hinzufügen von wsl.conf-Einträgen zum Steuern des Windows-Interop-Verhaltens [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* Korrektur des Verhaltens, dass getsockname nicht immer den Porduktfamilientyp des UNIX-Sockets zurückgibt [GH 1774]
* Hinzufügen von Unterstützung für TIOCSTI [GH 1863]
* Nicht blockierende Sockets beim Verbindungsaufbau sollten für Schreibversuche EAGAIN zurückgeben [GH 2846]
* Unterstützung von Interop auf eingebundenen VHDs [GH 3246, 3291]
* Korrektur von Problem mit der Berechtigungsüberprüfung im Stammordner [GH 3304]
* Eingeschränkte Unterstützung für die TTY-Tastatur-ioctls KDGKBTYPE, KDGKBMODE und KDSKBMODE.
* Windows-UI-Apps sollten ausgeführt selbst dann werden, wenn Sie im Hintergrund gestartet werden.

## <a name="build-17704"></a>Build 17704
Allgemeine Windows-Informationen zu Build 17704 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).

### <a name="wsl"></a>WSL
* Hinzufügen der Option wsl -u oder--user [GH 1203]
* Korrektur von WSL-Startproblemen, wenn der Schnellstart aktiviert ist [GH 2576]
* Unix-Sockets müssen getrennte Peeranmelde Informationen beibehalten [GH 3183]
* Nicht blockierende Unix-Sockets, die unbegrenzt EAGAIN-Fehler ausgeben [GH 3191]
* case=off ist der neue standardmäßige drvfs-Einbindungstyp [GH 2937, 3212, 3328]
    * Weitere Informationen finden Sie im [Blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).
* Hinzufügen von wslconfig/terminate zum Beenden ausgeführter Distributionen

## <a name="build-17692"></a>Build 17692
Allgemeine Windows-Informationen zu Build 17692 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).

### <a name="wsl"></a>WSL
* Korrektur des Problems mit den Kontextmenüeinträgen der WSL-Shell, die Pfade mit Leerzeichen nicht ordnungsgemäß behandeln.
* Bereitstellen von Unterscheidung von Groß-/Kleinschreibung pro Verzeichnis als erweitertes Attribut
* ARM64: Emulieren von Cacheverwaltungsvorgängen. Beheben von [dotnet-Problem](https://github.com/dotnet/core/issues/1561).
* DrvFs: Nur Escapezeichen im privaten Bereich, die einem mit Escapezeichen versehenen Zeichen entsprechen.

## <a name="build-17686"></a>Build 17686
Allgemeine Windows-Informationen zu Build 17686 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).

### <a name="wsl"></a>WSL
* Korrektur eines Off-by-one-Fehlers in der Längenüberprüfung des ELF Parserinterpreters [GH 3154].
* Absolute WSL-Timer mit einer Zeitangabe in der Vergangenheit werden nicht ausgelöst [GH 3091]
* Sicherstellen, dass neu erstellte Analysepunkte als solche im übergeordneten Verzeichnis aufgelistet werden.
* Atomarisches Erstellen von Verzeichnissen mit Berücksichtigung von Groß- und Kleinschreibung in DrvFs.

## <a name="build-17677"></a>Build 17677
Allgemeine Windows-Informationen zu Build 17677 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).

### <a name="wsl"></a>WSL
* Korrektur eines zusätzlichen Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist. [GH 2712]
* Korrektur eines WSL-Startfehlers, wenn UMCI aktiviert ist.- [GH 3020]

## <a name="build-17666"></a>Build 17666
Allgemeine Windows-Informationen zu Build 17666 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>WARNUNG: Es gibt ein Problem, das das Ausführen von WSL in einigen AMD-Chipsätzen verhindert [GH 3134]. Eine Korrektur ist verfügbar und wird in den Insider Build-Branch integriert.
* Hinzufügen des Explorer-Kontextmenüs zum Starten von WSL [GH 437, 603, 1836]. Halten Sie in einem Explorer-Fenster die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste, um diese Option zu verwenden.
* Korrektur des nicht blockierenden UNIX-Socketverhaltens [GH 2822, 3100]
* Korrigieren des hängenden NETLINK-Befehls, wie in GH 2026 gemeldet.
* Hinzufügen von Unterstützung für Einbindungsweitergabeflags [GH 2911]
* Korrektur von Problem mit truncate, das keine inotify-Ereignisse verursacht [GH 2978].
* Hinzufügen der Option --exec für „wsl.exe“ zum Aufrufen eine einzelne Binärdatei ohne Shell.
* Hinzufügen der Option --distribution für „wsl.exe“, um eine bestimmte Distribution auszuwählen.

## <a name="build-17655-skip-ahead"></a>Build 17655 (Skip Ahead)
Allgemeine Windows-Informationen zu Build 17655 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Eingeschränkte Unterstützung für dmesg. Anwendungen können sich jetzt in dmesg protokollieren. Der WSL-Treiber protokolliert eingeschränkte Informationen in dmesg. In Zukunft kann dies so erweitert werden, dass andere Informationen/Diagnoseinhalte vom Treiber erfasst werden.
    * Hinweis: dmesg wird derzeit über die `/dev/kmsg`-Geräteschnittstelle unterstützt. `syslog`-Systemaufrufschnittstelle wird noch nicht unterstützt. Daher funktionieren einige der `dmesg`-Befehlszeilenoptionen (z.B. `-S`, `-C`) nicht.
* Korrektur eines Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist. [GH 2712]

## <a name="build-17639-skip-ahead"></a>Build 17639 (Skip Ahead)
Allgemeine Windows-Informationen zu Build 17639 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Änderung der Standard-GID und des Modus von seriellen Geräten entsprechend den nativen Einstellungen [GH 3042]
* DrvFs unterstützt jetzt erweiterte Attribute.
    * Hinweis: Für DrvFs gelten einige Einschränkungen für den Namen erweiterter Attribute. Insbesondere sind einige Zeichen (etwa „/“, „:“ und „\*“) unzulässig, und für Namen erweiterter Attribute wird in DrvFs keine Groß- und Kleinschreibung beachtet.

## <a name="build-17133-fast"></a>Build 17133 (Fast)
Allgemeine Windows-Informationen zu Build 17133 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).

### <a name="wsl"></a>WSL
* Fehlerbehebung für Hängen in WSL. [GH 3039, 3034]

## <a name="build-17128-fast"></a>Build 17128 (Fast)
Allgemeine Windows-Informationen zu Build 17128 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).

### <a name="wsl"></a>WSL
* Keine

## <a name="build-17627-skip-ahead"></a>Build 17627 (Skip Ahead)
Allgemeine Windows-Informationen zu Build 17627 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).

### <a name="wsl"></a>WSL
* Hinzufügen von Unterstützung für futex-pi-fähige Vorgänge. [GH 1006]
    * Beachten Sie, dass Prioritäten derzeit keine unterstützte WSL-Funktion sind, sodass Einschränkungen bestehen. Die Standardverwenund sollte jedoch aktiviert werden.
* Windows-Firewallunterstützung für WSL-Prozesse. [GH 1852]
    * Um beispielsweise zuzulassen, dass der WSL python-Prozess an einem beliebigen Port lauschen kann, verwenden Sie Windows-CMD mit erhöhten Rechten: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * Weitere Informationen zum Hinzufügen von Firewallregeln finden Sie unter [Link.](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* Beachten der Standardshell des Benutzers bei der Verwendung von „wsl.exe“. [GH 2372]
* Melden aller Netzwerkschnittstellen als Ethernet. [GH 2996]
* Bessere Verarbeitung von beschädigten /etc/passwd-Dateien. [GH 3001]

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17618-skip-ahead"></a>Build 17618 (Skip Ahead)
Allgemeine Windows-Informationen zu Build 17618 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).

### <a name="wsl"></a>WSL
* Einführung in Pseudoconsolenfunktionalität für NT-Interop [GH 988, 1366, 1433, 1542, 2370, 2406].
* Der Legacyinstallationsmechanismus („lxrun.exe“) ist veraltet. Der unterstützte Mechanismus zum Installieren von Distributionen ist der Microsoft Store.

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17110"></a>Build 17110
Allgemeine Windows-Informationen zu Build 17110 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).

### <a name="wsl"></a>WSL
* Zulassen, dass /init aus Windows beendet wird [GH 2928].
* DrvFs verwendet nun standardmäßig Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis (entspricht der Einbindungsoption „case=dir“).
    * Wenn Sie „case=force“ verwenden (das alte Verhalten), muss ein Registrierungsschlüssel festgelegt werden. Führen Sie den folgenden Befehl aus, um „case=force“ zu aktivieren, wenn Sie diese Option verwenden müssen: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * Wenn Sie über vorhandene Verzeichnisse verfügen, die mit WSL in einer älteren Version von Windows erstellt wurden, bei denen die Groß-/Kleinschreibung beachtet werden muss, verwenden Sie „fsutil.exe“, um sie für Unterscheidung von Groß-/Kleinschreibung zu markieren: fsutil.exe file setcasesensitiveinfo <path> enable
* NULL-Beendigungszeichenfolgen werden vom uname-Systemaufruf zurückgegeben.

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17107"></a>Build 17107
Allgemeine Windows-Informationen zu Build 17107 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).

### <a name="wsl"></a>WSL
* Unterstützung von TCSETSF und TCSETSW für pty-Masterendpunkte [GH 2552].
* Starten von gleichzeitigen Interop-Prozessen kann zu EINVAL führen [GH 2813].
* Korrektur von PTRACE_ATTACH, um den richtigen Ablaufverfolgungsstatus in „/proc/pid/status“ anzuzeigen.
* Korrektur der Racebedingung, bei der kurzlebige Prozesse, die mit den CLEARTID- und SETTID-Flags geklont wurden, ohne Löschen der TID-Adresse beendet werden konnten.
* Anzeigen einer Meldung beim Aktualisieren der Linux-Dateisystemverzeichnisse beim Umstieg von einem Build vor 17093. Weitere Informationen zu den Änderungen für das 17093-Dateisystem finden Sie in den Anmerkungen zur Version für [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17101"></a>Build 17101
Allgemeine Windows-Informationen zu Build 17101 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).

### <a name="wsl"></a>WSL
* Unterstützung für signalfd. [GH 129]
* Unterstützung von Dateinamen, die ungültige NTFS-Zeichen enthalten, durch Codieren als private Unicode-Zeichen. [GH 1514]
* Automatisches Einbinden greift auf den schreibgeschützten Modus zurück, wenn Schreibvorgänge nicht unterstützt werden. [GH 2603]
* Ermöglichen des Einfügens von Unicode-Ersatzzeichenpaaren (z.B. Emojis). [GH 2765]
* Pseudodateien in „/proc“ und „/sys“ sollten „read“ und „write ready“ aus select, poll, epoll, usw. zurückgeben [GH 2838].
* Korrektur eines Problems, das dazu führen kann, dass der Dienst in eine Endlosschleife übergeht, wenn die Registrierung manipuliert wurde oder beschädigt ist.
* Korrektur von Netlink-Nachrichten, sodass sie mit neueren Versionen von iproute2 (upstream 4.14) funktionieren.

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17093"></a>Build 17093
Allgemeine Windows-Informationen zu Build 17093 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).

#### <a name="important"></a>Wichtig:
Wenn Sie WSL zum ersten Mal nach dem Upgrade auf diesen Build starten, müssen Sie einige Aufgaben durchführen, um die Linux-Dateisystemverzeichnisse zu aktualisieren. Dieser Vorgang kann einige Minuten in Anspruch nehmen, sodass WSL möglicherweise langsam zu starten scheint. Dies sollte nur ein Mal für jede Distribution erfolgen, die Sie aus dem Store installiert haben.
* Verbesserte Unterscheidung von Groß-/Kleinschreibung in DrvFs.
    * DrvFs unterstützt jetzt Berücksichtigung von Groß-/Kleinschreibung pro Verzeichnis. Dies ist ein neues Flag, das für Verzeichnisse festgelegt werden kann, um anzugeben, dass alle Vorgänge in diesen Verzeichnissen mit Unterscheidung zwischen Groß-/Kleinschreibung behandelt werden sollen, sodass sogar Windows-Anwendungen Dateien ordnungsgemäß öffnen können, bei denen sich nur die Groß-/Kleinschreibung unterscheidet.
    * DrvFs verfügt über neue Einbindungsoptionen, die die Berücksichtigung von Groß-/Kleinschreibung pro Verzeichnis steuern.
        * case=force: Für alle Verzeichnisse wird zwischen Groß-/Kleinschreibung unterschieden (mit Ausnahme des Laufwerkstamms). Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung beachtet. Dies ist das Legacyverhalten (ausgenommen, wenn neue Verzeichnisse für Unterscheidung zwischen Groß-/Kleinschreibung markiert werden).
        * case=dir: Nur für Verzeichnisse mit dem Flag für Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis wird Groß-/Kleinschreibung beachtet, für alle anderen Verzeichnisse nicht. Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung beachtet.
        * case=dir: Nur für Verzeichnisse mit dem Flag für Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis wird Groß-/Kleinschreibung beachtet, für alle anderen Verzeichnisse nicht. Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung nicht beachtet.
    * Hinweis: Für Verzeichnisse, die in früheren Versionen von WSL erstellt wurden, ist dieses Flag nicht festgelegt, sodass bei Verwendung der Option „case=dir“ keine Groß-/Kleinschreibung beachtet wird. Eine Möglichkeit, dieses Flag für vorhandene Verzeichnisse festzulegen, ist in Kürze verfügbar.
    * Beispiel für die Einbindung mit diesen Optionen (für vorhandene Laufwerke müssen Sie zuerst die Einbindung aufheben, bevor Sie die Einbindung mit anderen Optionen ausführen können): sudo mount -t drvfs C: /mnt/c -o case=dir
    * Momentan ist case=force immer noch die Standardoption. Dies wird in Zukunft in case=dir geändert.
* Sie können jetzt Schrägstriche in Windows-Pfaden verwenden, wenn Sie DrvFs einbinden, z.B. sudo mount -t drvfs //server/share /mnt/share
* WSL verarbeitet nun die /etc/fstab-Datei während des Instanzstarts [GH 2636].
    * Dies erfolgt vor der automatischen Einbindung von DrvFs-Laufwerken. Alle Laufwerke, die bereits von fstab eingebunden wurden, werden nicht automatisch erneut eingebunden, sodass Sie den Einbindungspunkt für bestimmte Laufwerke ändern können.
    * Dieses Verhalten kann mithilfe von „wsl.conf“ deaktiviert werden.
* Die mount, mountinfo- und mountstats-Dateien in „/proc“ versehen Sonderzeichen wie umgekehrte Schrägstriche und Leerzeichen ordnungsgemäß mit Escapezeichen [GH 2799]
* Spezielle Dateien, die mit DrvFs erstellt werden (z.B. symbolische WSL-Verknüpfungen oder Fifos und Sockets, wenn Metadaten aktiviert sind), können nun aus Windows kopiert und verschoben werden.

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL ist mit „wsl.conf“ besser konfigurierbar.
Es wurde eine Methode zum automatischen Konfigurieren bestimmter Funktionen in WSL hinzugefügt, die jedes Mal angewendet wird, wenn Sie das Subsystem starten. Dies umfasst Optionen für die automatische Einbindung und Netzwerkkonfiguration. Weitere Informationen hierzu finden Sie in unserem Blogbeitrag unter: https://aka.ms/wslconf

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX ermöglicht Socketverbindungen zwischen Linux-Prozessen für WSL- und native Windows-Prozesse.
WSL- und Windows-Anwendungen können nun über Unix-Sockets miteinander kommunizieren. Stellen Sie sich vor, Sie möchten einen Dienst in Windows ausführen und sowohl für Windows- als auch für WSL-Apps verfügbar machen. Das ist nun mit UNIX-Sockets möglich. Weitere Informationen finden Sie in unserem Blogbeitrag unter https://aka.ms/afunixinterop.

### <a name="wsl"></a>WSL
* Unterstützung von mmap() mit MAP_NORESERVE [GH 121, 2784]
* Unterstützung von CLONE_PTRACE und CLONE_UNTRACED [GH 121, 2781]
* Verarbeiten eines Nicht-SIGCHLD-Beendigungssignals im Klon [GH 121, 2781]
* Stub für /proc/sys/fs/inotify/max_user_instances und /proc/sys/fs/inotify/max_user_watches [GH 1705]
* Fehler beim Laden von ELF-Binärdateien, die Ladeheader mit Offsets ungleich NULL enthalten [GH 1884]
* Eliminieren von nachfolgenden Seitenbytes beim Laden von Images.
* Verringern der Fälle, in denen execve den Prozess automatisch beendet

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17083"></a>Build 17083
Allgemeine Windows-Informationen zu Build 17083 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).

### <a name="wsl"></a>WSL
* Korrektur der Fehlerüberprüfung für epoll [GH 2798, 2801, 2857]
* Korrektur von Hängern beim Deaktivieren von ASLR [GH 1185, 2870]
* Sicherstellen, dass mmap-Vorgänge atomarisch erscheinen [GH 2732]

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17074"></a>Build 17074
Allgemeine Windows-Informationen zu Build 17074 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).

### <a name="wsl"></a>WSL
* Festes Speicherformat von DrvFs-Metadaten [GH 2777] </br>
**Wichtig:** Die vor diesem Build erstellten DrvFs-Metadaten werden falsch oder überhaupt nicht angezeigt. Um betroffene Dateien zu korrigieren, verwenden Sie chmod und chown zum erneuten Anwenden der Metadaten.
* Korrektur eines Problems mit mehreren Signalen und neu startbaren Systemaufrufen.

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17063"></a>Build 17063
Allgemeine Windows-Informationen zu Build 17063 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).

### <a name="wsl"></a>WSL
* DrvFs unterstützt zusätzliche Linux-Metadaten. Dies ermöglicht das Festlegen des Besitzers und des Dateimodus mit chmod/chown sowie das Erstellen spezieller Dateien, etwa Fifos, Unix-Sockets und Gerätedateien. Diese Option ist zurzeit standardmäßig deaktiviert, da Sie noch experimentell ist.
**Hinweis:**  Wir haben einen Fehler im Metadatenformat behoben, das von DrvFs verwendet wird. Obwohl Metadaten in diesem Build für Experimente funktionieren, lesen zukünftige Builds die von diesem Build erstellten Metadaten nicht ordnungsgemäß.  Möglicherweise müssen Sie den Besitzer für geänderte Dateien manuell aktualisieren, und Geräte mit einer benutzerdefinierten Geräte-ID müssen neu erstellt werden.

  Um diese Funktion zu aktivieren, binden Sie DrvFs mit der Metadatenoption ein (um sie für eine vorhandene Einbindung zu aktivieren, müssen Sie die Einbindung zunächst aufheben):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux-Berechtigungen werden der Datei als zusätzliche Metadaten hinzugefügt. Sie wirken sich nicht auf die Windows-Berechtigungen aus.  Beachten Sie, dass beim Bearbeiten einer Datei mithilfe eines Windows-Editors die Metadaten möglicherweise entfernt werden. In diesem Fall wird die Datei auf die Standardberechtigungen zurückgesetzt.

* Hinzufügen von Einbindungsoptionen zu DrvFs, um Dateien ohne Metadaten zu steuern.
  * uid: die Benutzer-ID, die für den Besitzer aller Dateien verwendet wird.
  * gid: die Gruppen-ID, die für den Besitzer aller Dateien verwendet wird.
  * umask: Eine oktale Maske mit Berechtigungen, die für alle Dateien und Verzeichnisse ausgeschlossen werden sollen.
  * fmask: Eine oktale Maske mit Berechtigungen, die für alle regulären Dateien ausgeschlossen werden sollen.
  * dmask: Eine oktale Maske mit Berechtigungen, die für alle Verzeichnisse ausgeschlossen werden sollen.

  Beispiel:
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  Kombinieren Sie dies mit der Metadatenoption, um Standardberechtigungen für Dateien ohne Metadaten anzugeben.

* Wird in einer neuen Umgebungsvariablen (`WSLENV`) eingeführt, um zu konfigurieren, wie Umgebungsvariablen zwischen WSL und Win32 ausgetauscht werden.

  Beispiel:

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` eine durch Doppelpunkte getrennte Liste von Umgebungsvariablen, die beim Starten von WSL-Prozessen aus Win32 oder Win32-Prozessen aus WSL eingeschlossen werden können.  Jeder Variablen kann ein Schrägstrich als Suffix vorangestellt werden, gefolgt von Flags, um anzugeben, wie sie übersetzt werden soll.
  * p: Der Wert ist ein Pfad, der zwischen WSL-Pfaden und Win32-Pfaden übersetzt werden soll.
  * l: Der Wert ist eine Liste von Pfaden. In WSL ist es eine durch Doppelpunkte getrennte Liste. In Win32 ist es eine durch Semikolons getrennte Liste.
  * u: Der Wert sollte nur beim Aufrufen von WSL aus Win32 eingeschlossen werden.
  * w: Der Wert sollte nur beim Aufrufen von Win32 aus WSL eingeschlossen werden.

  Sie können `WSLENV` in der BASHRC-Datei oder in der benutzerdefinierten Windows-Umgebung für Ihren Benutzer festlegen.

* drvfs wird ordnungsgemäß eingebunden und behält Zeitstempel aus from tar, cp -p bei (GH 1939)
* Symbolische drvfs-Verknüpfungen geben die richtige Größe an (GH 2641)
* Lese-/Schreibvorgänge funktionieren für sehr große E/A-Größen (GH 2653)
* waitpid funktioniert mit Prozessgruppen-IDs (GH 2534)
* Erheblich verbesserte mmap-Leistung für große reserve-Regionen, Verbesserung der ghc-Leistung (GH 1671)
* personality unterstützt READ_IMPLIES_EXEC, Korrekturen maxima und clisp (GH 1185)
* mprotect unterstützt PROT_GROWSDOWN,;Korrekturen clisp (GH 1128)
* Seitenfehlerkorrekturen im Overcommitmodus, Korrekturen sbcl (GH 1128)
* clone unterstützt weitere Flagkombinationen
* Unterstützung von select/epoll von epoll-Dateien (zuvor eine Nulloperation).
* Benachrichtigen von ptrace über nicht implementierte Systemaufrufe.
* Ignorieren von Schnittstellen, die nicht aktiv sind, beim Generieren von resolv.conf-Namenservern [GH 2694]
* Aufzählen von Netzwerkschnittstellen ohne physische Adresse. [GH 2685]
* Zusätzliche Fehlerbehebungen und Verbesserungen

### <a name="linux-tools-available-to-developers-on-windows"></a>Linux-Tools für Entwickler unter Windows verfügbar

* Windows-Befehlszeilen-Toolkette enthält bsdtar (tar) und curl.
  Lesen Sie [diesen Blog](https://aka.ms/tarcurlwindows), um mehr über das Hinzufügen dieser beiden neuen Tools zu erfahren, und sehen Sie, wie Sie das Entwicklererlebnis unter Windows formen.

*   `AF_UNIX` ist im Windows Insider SDK (17061 und höher) verfügbar.
  Lesen Sie [diesen Blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), um weitere Informationen zu `AF_UNIX` zu erhalten und mehr über die Verwendung in Windows durch Entwickler zu erfahren.

### <a name="console"></a>Konsole
* Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.


## <a name="build-17046"></a>Build 17046

Allgemeine Windows-Informationen zu Build 17046 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).

### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Ermöglicht das Ausführen von Prozessen ohne ein aktives Terminal. [GH 709, 1007, 1511, 2252, 2391 usw.]
- Bessere Unterstützung von CLONE_VFORK und CLONE_VM. [GH 1878, 2615]
- Überspringen der TDI-Filtertreiber für WSL-Netzwerkvorgänge. [GH 1554]
- DrvFs erstellt symbolische NT-Verknüpfungen, wenn bestimmte Bedingungen erfüllt sind. [GH 353, 1475, 2602]
    - Das Verknüpfungsziel muss relativ sein, darf keine Einbindungspunkte oder symbolische Verknüpfungen kreuzen und muss vorhanden sein.
    - Der Benutzer muss über SE_CREATE_SYMBOLIC_LINK_PRIVILEGE verfügen (dies erfordert normalerweise, dass Sie „wsl.exe“ mit erhöhten Rechten starten), sofern der Entwicklermodus nicht aktiviert ist.
    - Unter allen anderen Umständen erstellt DrvFs weiterhin symbolische WSL-Verknüpfungen.
- Ermöglichen der gleichzeitigen Ausführung von WSL-Instanzen mit und ohne erhöhten Rechten.
- Unterstützung von /proc/sys/kernel/Yama/ptrace_scope
- Hinzufügen von wslpath zum Durchführen von Konvertierungen von WSL-<- >Windows-Pfaden. [GH 522, 1243, 1834, 2327 usw.]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a>Konsole
- Keine Korrekturen.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.


## <a name="build-17040"></a>Build 17040

Allgemeine Windows-Informationen zu Build 17040 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Keine Korrekturen seit 17035.

#### <a name="console"></a>Konsole
- Keine Korrekturen seit 17035.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17035"></a>Build 17035

Allgemeine Windows-Informationen zu Build 17035 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Der Zugriff auf Dateien auf DrvFs kann gelegentlich mit EINVAL fehlschlagen. [GH 2448]

#### <a name="console"></a>Konsole
- Farbverlust beim Einfügen/Löschen von Zeilen im VT-Modus.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17025"></a>Build 17025

Allgemeine Windows-Informationen zu Build 17025 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Starten anfänglicher Prozesse in einer neuen Vordergrundprozessgruppe [GH 1653, 2510].
- Korrekturen der SIGHUP-Übermittlung [GH 2496].
- Generieren eines Standardnamens für virtuelle Bridge generieren, wenn keine Angabe erfolgt [GH 2497].
- Implementieren von /proc/sys/kernel/Random/boot_id [GH 2518].
- Weitere Interop-Pipekorrekturen für stdout/stderr.
- Stub für syncfs-Systemaufruf.

#### <a name="console"></a>Konsole
- Korrektur der VT-Eingabeübersetzung für Drittanbieterkonsolen [GH 111]

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="build-17017"></a>Build 17017

Allgemeine Windows-Informationen zu Build 17017 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Ignorieren leerer ELF-Programmheader [GH 330].
- Ermöglichen, dass LxssManager WSL-Instanzen für nicht interaktive Benutzer erstellt (Unterstützung für SSH und geplante Aufgaben) [GH 777, 1602].
- Unterstützung von WSL->Win32->WSL-Szenarien („Inception“) [GH 1228].
- Eingeschränkte Unterstützung für das Beenden von Konsolen-Apps, die über Interop aufgerufen wurden [GH 1614].
- Unterstützung von Einbindungsoptionen für devpts [GH 1948].
- Ptrace blockiert den Start untergeordneter Prozesse [GH 2333].
- EPOLLET fehlen einige Ereignisse [GH 2462].
- Rückgabe einer größeren Anzahl von Daten für PTRACE_GETSIGINFO.
- Getdents mit lseek liefert falsche Ergebnisse.
- Korrektur einiger Hänger von Win32-Interop-Apps, die auf Eingaben in einer Pipe warten, die keine weiteren Daten enthält.
- O_ASYNC-Unterstützung für tty/pty-Dateien.
- Weitere Verbesserungen und Fehlerbehebungen

#### <a name="console"></a>Konsole
- Keine konsolenbezogenen Änderungen in diesem Release.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests werden zurzeit ausgeführt.

## <a name="fall-creators-update"></a>Fall Creators Update

## <a name="build-16288"></a>Build 16288

Allgemeine Windows-Informationen zu Build 16288 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Ordnungsgemäße Initialisierung und Meldung von uid, gid und Modus für Socketdateideskriptoren [GH 2490]
- Weitere Verbesserungen und Fehlerbehebungen

#### <a name="console"></a>Konsole
- Keine konsolenbezogenen Änderungen in diesem Release.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Keine Änderung seit 16273

## <a name="build-16278"></a>Build 16278

Allgemeine Windows-Informationen zu Build 162738 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Explizite Aufhebung der Zuordnung zugeordneter Ansichten von dateigestützten Abschnitten beim Beenden des LX MM-Status [GH 2415]
- Weitere Verbesserungen und Fehlerbehebungen

#### <a name="console"></a>Konsole
- Keine konsolenbezogenen Änderungen in diesem Release.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Keine Änderung seit 16273

## <a name="build-16275"></a>Build 16275

Allgemeine Windows-Informationen zu Build 162735 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- In diesem Release gibt es keine WSL-bezogenen Änderungen.

#### <a name="console"></a>Konsole
- Keine konsolenbezogenen Änderungen in diesem Release.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Keine Änderung seit 16273

## <a name="build-16273"></a>Build 16273

Allgemeine Windows-Informationen zu Build 16273 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Korrektur eines Problems, bei dem DrvFs manchmal den falschen Dateityp für Verzeichnisse gemeldet hat [GH 2392]
- Ermöglichen der Erstellung von NETLINK_KOBJECT_UEVENT-Sockets zum Entsperren von Programmen, die uevent verwenden [GH 1121, 2293, 2242, 2295, 2235, 648, 637]
- Hinzufügen von Unterstützung für nicht blockierende Verbindungen [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]
- Implementieren des CLONE_FS-Klonsystem-Aufrufflags [GH 2242]
- Korrektur von Problemen im Zusammenhang mit der nicht ordnungsgemäßen Behandlung von Registerkarten oder Anführungszeichen in NT-Interop [GH 1625, 2164]
- Beheben des Fehlers „Zugriff verweigert“ beim Versuch, WSL-Instanzen erneut zu starten [GH 651, 2095]
- Implementieren von Futex-Vorgängen FUTEX_REQUEUE und FUTEX_CMP_REQUEUE [GH 2242]
- Korrigieren von Berechtigungen für verschiedene SysFs-Dateien [GH 2214]
- Korrigieren des Hängens des Haskell-Stapels während des Setups [GH 2290]
- Implementieren der Flags „C“, „O“ und „P“ von binfmt_misc [GH 2103]
- Hinzufügen von /proc/sys/kernel/shmmax/shmmni und /threads-max [GH 1753]
- Hinzufügen partieller Unterstützung für den ioprio_set-Systemaufruf [GH 498]
- Stub für SO_REUSEPORT und Hinzufügen von Unterstützung für SO_PASSCRED für netlink-Sockets [GH 69]
- Rückgabe anderer Fehlercodes aus RegisterDistribuiton, wenn zurzeit eine Distribution installiert oder deinstalliert wird.
- Ermöglichen des Aufhebens der Registrierung von teilweise installierten WSL-Distributionen über „wslconfig.exe“
- Korrektur des Hängens des Python-Sockettests von udp::msg_peek
- Weitere Verbesserungen und Fehlerbehebungen

#### <a name="console"></a>Konsole
- Keine konsolenbezogenen Änderungen in diesem Release.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Tests gesamt: 1904<br/>
Übersprungene Tests gesamt: 209<br/>
Fehler gesamt: 229<br/>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>Build 16257

Allgemeine Windows-Informationen zu Build 16257 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Implementieren des prlimit64-Systemaufrufs
- Hinzufügen von Unterstützung für ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]
- Stub für MSG_MORE für TCP-Sockets [GH 2351]
- Korrektur des ungültigen Verhaltens des AT_EXECFN-Hilfsvektors [GH 2133]
- Korrektur des Kopier-/Einfügeverhalten für Konsole/TTY und Hinzufügen einer besseren Verarbeitung voller Puffer [GH 2204, 2131]
- Festlegen von T_SECURE im Hilfsvektor für set-user-ID- und set-group-ID-Programme [GH 2031]
- Psuedoterminal-Masterendpunkt verarbeitet TIOCPGRP nicht [GH 1063]
- Korrektur des Nichtzurückspulens von Verzeichnissen in LxFs durch lseek [GH 2310]
- /dev/ptmx wird nach hoher Auslastung gesperrt [GH 1882]
- Weitere Verbesserungen und Fehlerbehebungen

#### <a name="console"></a>Konsole
- Korrektur für horizontale Linien/Unterstriche überall [GH 2168]
- Korrektur der Änderung der Prozessreihenfolge, wodurch das Schließen von NPM erschwert wird [GH 2170]
- Hinzufügen des neuen Farbschemas: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP-Ergebnisse:
Keine Änderung seit 16251

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`prlimit64`<br/>

### <a name="known-issues"></a>Bekannte Probleme
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a>[GitHub-Issue 2392: Windows-Ordner werden von WSL nicht erkannt (](https://github.com/Microsoft/BashOnWindows/issues/2392))
In Build 16257 hat WSL beim Aufzählen von Windows-Dateien/-Ordnern über `/mnt/c/...` Probleme.
Dieses Problem wurde behoben und sollte im Insider-Builds in der Woche ab dem 14.08.2017 veröffentlicht werden.

<br/>

## <a name="build-16251"></a>Build 16251

Allgemeine Windows-Informationen zu Build 16251 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- Entfernen des Beta-Tags aus der optionalen WSL-Komponente. Weitere Informationen finden Sie im [Blogbeitrag](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).
- Ordnungsgemäße Initialisierung der saved-set uid und gid für set-user-ID- and set-group-ID-Binärdateien bei der Ausführung [GH 962, 1415, 2072]
- Hinzufügen von Unterstützung für PTRACE_O_TRACEEXIT [GH 555]
- Hinzufügen von Unterstützung für PTRACE_GETFPREGS und PTRACE_GETREGSET mit NT_FPREGSET [GH 555]
- Korrektur von ptrace, um bei ignorierten Signalen anzuhalten
- Weitere Verbesserungen und Fehlerbehebungen

#### <a name="console"></a>Konsole
- Keine konsolenbezogenen Änderungen in diesem Release.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 768</br>
Anzahl fehlgeschlagener Tests: 244</br>
Anzahl übersprungener Tests: 96</br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>Build 16241

Allgemeine Windows-Informationen zu Build 16241 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).<br/>


### <a name="fixed"></a>Fest
#### <a name="wsl"></a>WSL
- In diesem Release gibt es keine WSL-bezogenen Änderungen.

#### <a name="console"></a>Konsole
- Korrektur für die Ausgabe des falschen Zeichens für Schnittlinien-DEC, ursprünglich [hier](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) gemeldet
- Korrektur, dass kein Ausgabetext in Codepage 65001 (UTF8) angezeigt wird
- Übertragen Sie an den RGB-Werten einer Farbe vorgenommene Änderungen nicht an andere Teile der Palette bei Änderungen der Auswahl. Dadurch wird die Verwendung des Konsoleneigenschaftenblatts erheblich vereinfacht.
- STRG+S funktioniert anscheinend nicht ordnungsgemäß
- Un-Bold/-Dim fehlt in ANSI-Escapecodes vollständig [GH 2174]
- Die Konsole unterstützt VIM-Farbdesigns nicht ordnungsgemäß [GH 1706]
- Bestimmte Zeichen können nicht eingefügt werden [GH 2149]
- Die Größenänderung von dynamischem Umbruch interagiert seltsam mit der Größenänderung eines Bash-Fensters, wenn sich die Inhalte in der Bearbeitungs-/Befehlszeile befinden [GH-Verbindung 1123]
- STRG+L hinterlässt Fragmente auf dem Bildschirm [GH 1978]
- Konsolenrenderingfehler bei der Anzeige von VT für HDPI [GH 1907]
- Japanische Zeichen sehen mit dem Unicode-Zeichen U+30FB seltsam aus [GH 2146]
- Weitere Verbesserungen und Fehlerbehebungen

</br>

## <a name="build-16237"></a>Build 16237

Allgemeine Windows-Informationen zu Build 16237 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).<br/>


### <a name="fixed"></a>Fest
- Verwenden von Standardattributen für Dateien ohne E/As in lxfs (root, root, 0000)
- Hinzufügen von Unterstützung für Distributionen, die erweiterte Attribute verwenden
- Korrektur des Auffüllens für von getdents und getdents64 zurückgegebene Einträge
- Korrektur der Berechtigungsüberprüfung für den SHM_STAT-Systemaufruf [GH 2068]
- Korrektur des falschen anfänglichen epoll-Zustands für ttys [GH 2231]
- Korrektur, dass DrvFs readdir nicht alle Einträge zurückgibt [GH 2077]
- Korrektur von LxFs readdir, wenn Dateien nicht verknüpft sind [GH 2077]
- Ermöglichen des erneuten Öffnens von nicht verknüpfter drvfs-Dateien über procfs
- Hinzufügen einer Außerkraftsetzung des globalen Registrierungsschlüssels zum Deaktivieren von WSL-Features (Interop/Laufwerkeinbindung)
- Korrektur falscher Blockanzahl in „stat“ für DrvFs (und LxFs) [GH 1894]
- Weitere Verbesserungen und Fehlerbehebungen

</br>

## <a name="build-16232"></a>Build 16232

Allgemeine Windows-Informationen zu Build 16232 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).<br/>


### <a name="fixed"></a>Fest
- In diesem Release gibt es keine WSL-bezogenen Änderungen.

</br>

## <a name="build-16226"></a>Build 16226

Allgemeine Windows-Informationen zu Build 16226 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).<br/>


### <a name="fixed"></a>Fest
- Unterstützung von auf xattr bezogenen Systemaufrufen (getxattr, setxattr, listxattr, removexattr).
- xattr-Unterstützung für security.capablity.
- Verbesserte Kompatibilität mit bestimmten Dateisystemen und Filtern, einschließlich Nicht-MS-SMB-Servern. [GH #1952]
- Verbesserte Unterstützung für OneDrive-Platzhalter, GVFS-Platzhalter und komprimierte Compact OS-Dateien.
- Weitere Verbesserungen und Fehlerbehebungen

</br>

## <a name="build-16215"></a>Build 16215

Allgemeine Windows-Informationen zu Build 16215 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).<br/>


### <a name="fixed"></a>Fest
- Für WSL ist der Entwicklermodus nicht mehr erforderlich.
- Unterstützung von Verzeichnisverbindungen in drvfs.
- Verarbeiten der Deinstallation von appx-Paketen der WSL-Distribution.
- Aktualisieren von procfs, um private und freigegebene Zuordnungen anzuzeigen.
- Hinzufügen einer Möglichkeit für „wslconfig.exe“ zum Bereinigen von Distributionen, die teilweise installiert oder deinstalliert wurden.
- Hinzufügen von Unterstützung für IP_MTU_DISCOVER für TCP-Sockets. [GH 1639, 2115, 2205]
- Ableiten der Protokollfamilie für Routen zu AF_INADDR.
- Verbesserungen an seriellen Geräten [GH 1929].

</br>

## <a name="build-16199"></a>Build 16199

Allgemeine Windows-Informationen zu Build 16199 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).<br/>


### <a name="fixed"></a>Fest
- In diesen Releases gibt es keine WSL-bezogenen Änderungen.

</br>

## <a name="build-16193"></a>Build 16193

Allgemeine Windows-Informationen zu Build 16193 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).<br/>


### <a name="fixed"></a>Fest
- Racebedingung zwischen dem Senden von SIGCONT und einer Threadgruppe, die beendet wird [GH 1973]
- Ändern von TTY-und PTY-Geräten zum Melden von FILE_DEVICE_NAMED_PIPE anstelle von FILE_DEVICE_CONSOLE [GH 1840]
- SSH-Korrektur für IP_OPTIONS
- Verschieben der DrvFs-Einbindung in den init-Daemon [GH 1862, 1968, 1767, 1933]
- Hinzufügen von Unterstützung in DrvFs für die folgenden symbolischen NT-Verknüpfungen.

</br>

## <a name="build-16184"></a>Build 16184

Allgemeine Windows-Informationen zu Build 16184 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).<br/>


### <a name="fixed"></a>Fest
- Entfernen des apt-Paketverwaltungstasks (lxrun.exe /update) wurde entfernt.
- Korrektur der Nichtanzeige der Ausgabe aus Windows-Prozessen in node.js [GH 1840]
- Lockern der Ausrichtungsanforderungen in lxcore [GH 1794]
- Korrektur der Verarbeitung des AT_EMPTY_PATH-Flags in mehreren Systemaufrufen.
- Korrektur eines Problems, bei dem das Löschen von DrvFs-Dateien mit geöffneten Handles bewirkt, dass die Datei nicht definiertes Verhalten aufweist [GH 544, 966, 1357, 1535, 1615]
- „/etc/hosts“ erbt nun Einträge von der Windows-Hostdatei (%windir%\system32\drivers\etc\hosts) [GH 1495]

</br>

## <a name="build-16179"></a>Build 16179

Allgemeine Windows-Informationen zu Build 16179 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).<br/>


### <a name="fixed"></a>Fest
- Keine WSL-Änderungen in dieser Woche.

</br>

## <a name="build-16176"></a>Build 16176

Allgemeine Windows-Informationen zu Build 16176 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).<br/>


### <a name="fixed"></a>Fest

- [Aktivierte serielle Unterstützung](/archive/blogs/wsl/serial-support-on-the-windows-subsystem-for-linux)
- Hinzufügen der IP-Socketoption IP_OPTIONS [GH 1116]
- Implementierung der pwritev-Funktion (beim Hochladen der Datei nach nginx/PHP-FPM) [GH 1506]
- Hinzufügen der IP-Socket-Optionen IP_MULTICAST_IF und IPV6_MULTICAST_IF [GH 990]
- Unterstützung für Socketoption IP_MULTICAST_LOOP und IPV6_MULTICAST_LOOP [GH 1678]
- Hinzufügen von IP(V6)_MTU-Socketoption für den Knoten apps, traceroute, dig, nslookup, host
- Hinzufügen der IP-Socketoption IPV6_UNICAST_HOPS
- [Verbesserungen des Dateisystems](/archive/blogs/wsl/file-system-improvements-to-the-windows-subsystem-for-linux)
    * Ermöglichen der Einbindung von UNC-Pfaden
    * Ermöglichen von CDFS-Unterstützung in drvfs
    * Ordnungsgemäße Verarbeitung von Berechtigungen für Netzwerkdateisysteme in drvfs
    * Hinzufügen von Unterstützung für Remotelaufwerke zu drvfs
    * Ermöglichen von FAT-Unterstützung in drvfs
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse
Keine Änderungen seit 15042

</br>

## <a name="build-16170"></a>Build 16170

Allgemeine Windows-Informationen zu Build 16170 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).<br/>

Wir haben einen neuen [Blogbeitrag](/archive/blogs/wsl/testing-the-windows-subsystem-for-linux) veröffentlicht, in dem unsere Anstrengungen beim Testen von WSL erläutert werden.

### <a name="fixed"></a>Fest

- Unterstützung für Socketoption IP_ADD_MEMBERSHIP und IPV6_ADD_MEMBERSHIP [GH 1678]
- Hinzufügen von Unterstützung für PTRACE_OLDSETOPTIONS. [GH 1692]
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse
Keine Änderungen seit 15042

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>Build 15046 für Windows 10 Creators Update
Es gibt keine weiteren WSL-Korrekturen oder-Funktionen, die für die Einbindung in das Creators Update in Windows 10 geplant sind. Die Anmerkungen zu dieser Version von WSL werden in den kommenden Wochen fortgesetzt, um Ergänzungen für das nächste Hauptupdate von Windows aufzuführen. Allgemeine Windows-Informationen zu Build 15046 und zukünftigen Insider Releases finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/). <br/><br/>
 <br/>

## <a name="build-15042"></a>Build 15042

Allgemeine Windows-Informationen zu Build 15042 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).<br/>


### <a name="fixed"></a>Fest

- Korrektur eines Deadlocks beim Entfernen eines Pfades, der auf „..“ endet
- Korrektur eines Problems, bei dem FIONBIO bei Erfolg 0 zurückgibt [GH 1683]
- Korrektur eines Problems bei Lesevorgängen mit einer Länge von Null von Internetdatagrammsockets
- Korrektur eines möglichen Deadlocks aufgrund einer Racebedingung bei der drvfs inode-Suche [GH 1675]
- Erweiterte Unterstützung für Hilfsdaten von Unix-Sockets, SCM_CREDENTIALS und SCM_RIGHTS [GH 514, 613, 1326]
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 737</br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255

</br>

## <a name="build-15031"></a>Build 15031

Allgemeine Windows-Informationen zu Build 15031 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).<br/>


### <a name="fixed"></a>Fest

- Korrektur eines Fehlers, bei dem sich time(2) sporadisch falsch verhielt.
- Korrektur eines Problems, bei dem *SIGPROCMASK-Systemaufrufe die Signalmaske beschädigen konnten.
- Jetzt Rückgabe der vollständigen Länge der Befehlszeile in WSL-Benachrichtigung zur Prozesserstellung. [GH 1632]
- WSL meldet jetzt die Threadbeendigung über ptrace für GDB-Hänger. [GH 1196]
- Korrektur eines Fehlers, bei dem ptys nach hoher tmux-E/A nicht mehr reagiert [GH 1358]
- Korrektur der Timeoutüberprüfung in zahlreichen Systemaufrufen (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)
- Hinzufügen von eventfd EFD_SEMAPHORE-Unterstützung [GH 452]
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 737</br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>Build 15025

Allgemeine Windows-Informationen zu Build 15025 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).<br/>


### <a name="fixed"></a>Fest

- Korrektur eines Fehlers, bei dem grep 2.27 nicht mehr funktioniert [GH 1578]
- Implementierung des EFD_SEMAPHORE-Flags für den eventfd2-Systemaufruf [GH 452]
- Implementierung von /proc/[pid]/net/ipv6_route [GH 1608]
- Signalgestützte E/A-Unterstützung für Unix-Streamsockets [GH 393, 68]
- Unterstützung für F_GETPIPE_SZ und F_SETPIPE_SZ [GH 1012]
- Implementierung des recvmmsg()-Systemaufrufs [GH 1531]
- Korrektur eines Fehlers, bei dem epoll_wait() nicht gewartet hat [GH 1609]
- Implementierung von /proc/version_signature
- Tee-Systemaufruf gibt jetzt einen Fehler zurück, wenn beide Dateideskriptoren auf dieselbe Pipe verweisen
- Implementierung des richtigen Verhaltens für SO_PEERCRED für Unix-Sockets
- Korrektur der Verarbeitung ungültiger Parameter des tkill-Systemaufrufs
- Änderungen zum Verbessern der Leistung von drvfs
- Kleinere Korrektur für Ruby-E/A-Blockierung
- Korrektur von recvmsg() beim Zurückgeben von EINVAL für das MSG_DONTWAIT-Flag für Inet-Sockets [GH 1296]
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 732</br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>Build 15019

Allgemeine Windows-Informationen zu Build 15019 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).<br/>


### <a name="fixed"></a>Fest

- Korrektur eines Fehlers, der fälschlicherweise die CPU-Auslastung in procfs für Tools wie htop gemeldet hat [GH 823, 945, 971]
- Beim Aufrufen von open() mit O_TRUNC für eine vorhandene Datei „inotify“ wird nun IN_MODIFY vor IN_OPEN generiert
- Korrekturen für den Unix-Socket getsockopt SO_ERROR zum Aktivieren von Postgress [GH 61, 1354]
- Implementierung von /proc/sys/net/core/somaxconn für die Sprache GO
- Der Apt-get-Packageupdate-Hintergrundtask wird jetzt aus der Ansicht ausgeblendet
- Löschen des Bereichs für ipv6 localhost (Fehler Spring-Framework (Java)).
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 714 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 249 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>Build 15014

Allgemeine Windows-Informationen zu Build 15014 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fest

- STRG+C funktioniert nun wie beabsichtigt
- htop und ps auxw zeigen jetzt die richtige Ressourcenverwendung an (GH #516)
- Grundlegende Übersetzung von NT-Ausnahmen in Signale. (GH #513)
- fallocate schlägt nun mit ENOSPC anstatt mit EINVAL fehl, wenn nicht genügend Speicherplatz verfügbar ist (GH #1571)
- Hinzufügen von /proc/sys/kernel/sem.
- Implementierung der semop- und semtimedop-Systemaufrufe
- Korrektur von nslookup-Fehlern mit der IP_RECVTOS- und IPV6_RECVTCLASS-Socketoption (GH 69)
- Unterstützung für Socketoptionen IP_RECVTTL und IPV6_RECVHOPLIMIT
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 709 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Zusammenfassung der Systemaufrufe
Systemaufrufe gesamt: 384 </br>
Implementiert gesamt: 235 </br>
Mit Stub versehen gesamt: 22 </br>
Nicht implementiert gesamt: 127 </br>
[Ausführliche Aufschlüsselung](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>Build 15007

Allgemeine Windows-Informationen zu Build 15007 finden Sie im [Windows-Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).<br/>


### <a name="known-issue"></a>Bekanntes Problem

- Es gibt einen bekannten Fehler, bei dem die Konsole einige Eingaben über STRG+<key> nicht erkennt.  Dies schließt den Befehl STRG+C ein, der als normaler C-Tastendruck fungiert.

  - Problemumgehung: Ordnen Sie STRG+C eine alternative Taste zu. Gehen Sie beispielsweise folgendermaßen vor, um STRG+K der Tastenkombination STRG+C zuzuordnen: `stty intr \^k`.  Diese Zuordnung erfolgt pro Terminal und muss *jedes* Mal ausgeführt werden, wenn Bash gestartet wird. Benutzer können die Option zum Einbeziehen in ihre `.bashrc`-Datei untersuchen

### <a name="fixed"></a>Fest

- Korrektur eines Problems, bei dem die Ausführung von WSL 100 % eines CPU-Kerns verbraucht
- Socketoption IP_PKTINFO, IPV6_RECVPKTINFO wird jetzt unterstützt. (GH #851, 987)
- Abschneiden der physischen Adresse der Netzwerkschnittstelle auf 16 Bytes in lxcore (GH #1452, 1414, 1343, 468, 308)
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 709 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>Build 15002

Allgemeine Windows-Informationen zu Build 15002 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).<br/>


### <a name="known-issue"></a>Bekanntes Problem

Zwei bekannte Probleme:
- Es gibt einen bekannten Fehler, bei dem die Konsole einige Eingaben über STRG+<key> nicht erkennt.  Dies schließt den Befehl STRG+C ein, der als normaler C-Tastendruck fungiert.

  - Problemumgehung: Ordnen Sie STRG+C eine alternative Taste zu. Gehen Sie beispielsweise folgendermaßen vor, um STRG+K der Tastenkombination STRG+C zuzuordnen: `stty intr \^k`.  Diese Zuordnung erfolgt pro Terminal und muss *jedes* Mal ausgeführt werden, wenn Bash gestartet wird. Benutzer können die Option zum Einbeziehen in ihre `.bashrc`-Datei untersuchen

- Während der Ausführung von WSL werden von einem Systemthread 100 % eines CPU-Kerns beansprucht.  Die Ursache wurde untersucht und intern behoben.

### <a name="fixed"></a>Fest

- Alle Bash-Sitzungen müssen jetzt auf derselben Berechtigungsebene erstellt werden.  Der Versuch, eine Sitzung auf einer anderen Ebene zu starten, wird blockiert.  Dies bedeutet, dass Administrator-und Nicht-Administratorkonsolen nicht gleichzeitig ausgeführt werden können. (GH #626)
<br/>
- Implementierung der folgenden NETLINK_ROUTE-Meldungen (erfordert Windows-Administrator)
     - RTM_NEWADDR (unterstützt `ip addr add`)
     - RTM_NEWROUTE (unterstützt `ip route add`)
     - RTM_DELADDR (unterstützt `ip addr del`)
     - RTM_DELROUTE (unterstützt `ip route del`)
- Die geplante Tasküberprüfung für zu aktualisierende Pakete wird nicht mehr über eine getaktete Verbindung ausgeführt (GH #1371)
- Korrektur eines Fehlers, bei dem die Weiterleitung unterbrochen wird. Beispiel: bash -c "ls -alR /" | bash -c "cat" (GH #1214)
- Implementierung der TCP_KEEPCNT-Socketoption (GH #843)
- Implementierung der IP_MTU_DISCOVER INET-Socketoption (GH #720, 717, 170, 69)
- Entfernen der Legacyfnktionalität zum Ausführen von NT-Binärdateien aus init mit NT-Pfadsuche. (GH #1325)
- Korrektur des Modus von /dev/kmsg zum Zulassen von Gruppen-/sonstigem Lesezugriff (0644) (GH #1321)
- Implementierung von /proc/sys/kernel/random/uuid (GH #1092)
- Korrektur eines Fehlers, bei dem die Startzeit des Prozesses als Jahr 2432 angezeigt wurde (GH #974)
- Wechseln der TERM-Standardumgebungsvariablen in xterm-256color (GH #1446)
- Änderung der Art und Weise, in der der Prozesscommit während des Prozessforks berechnet wird. (GH #1286)
- Implementierung von /proc/sys/vm/overcommit_memory. (GH #1286)
- Implementierung der /proc/net/route-Datei (GH #69)
- Korrektur eines Fehlers, bei dem der Verknüpfungsname falsch lokalisiert wurde (GH #696)
- Korrektur der fehlerhaften ELF-Verarbeitungslogik, die die Programmheader nicht ordnungsgemäß so überprüft, dass sie kleiner als (oder gleich) PATH_MAX sein müssen. (GH #1048)
- Implementierung des statfs-Rückrufs für procfs, sysfs, cgroupfs und binfmts (GH #1378)
- Korrektur der AptPackageIndexUpdate-Fenster, die nicht geschlossen werden (GH #1184, auch in GH #1193 beschrieben)
- Hinzufügen von ASLR-Personality, ADDR_NO_RANDOMIZE-Unterstützung. [GH #1148, 1128]
- Verbesserung von PTRACE_GETSIGINFO, SIGSEGV für ordnungsgemäße gdb-Stapelüberwachungen während AV (GH #875)
- Elf-Verarbeitung schlägt für patchelf-Binärdateien nicht mehr fehl. [GH #471]
- VPN DNS-Weitergabe an /etc/resolv.conf (GH #416, 1350)
- Verbesserungen an TCP Close für eine zuverlässigere Datenübertragung. (GH #610, 616, 1025, 1335)
- Jetzt Rückgabe des richtigen Fehlercodes, wenn zu viele Dateien geöffnet werden (EMFILE). (GH #1126, 2090)
- Windows-Überwachungsprotokoll erfasst jetzt den Imagenamen in Process Create Audit.
- Jetzt normaler Fehler beim Starten von „bash.exe“ in einem Bash-Fenster.
- Hinzufügen einer Fehlermeldung, wenn Interop nicht auf ein Arbeitsverzeichnis unter LxFs zugreifen kann (z.B. BASHRC-Datei von „notepad.exe“).
- Korrektur eines Problems, bei dem der Windows-Pfad in WSL abgeschnitten wurde
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 690 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 274 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>Build 14986

Allgemeine Windows-Informationen zu Build 14986 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).<br/>


### <a name="fixed"></a>Fest

- Korrektur von Fehlerüberprüfungen mit Netlink und Pty IOCTLs
- Kernel Version meldet nun 4.4.0-43 aus Gründen der Konsistenz mit Xenial
- „Bash.exe“ wird jetzt gestartet, wenn die Eingabe an „nul:“ gerichtet ist (GH #1259)
- Thread-IDs werden nun ordnungsgemäß in procfs erfasst (GH #967)
- Flags IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR werden jetzt in inotify_add_watch() unterstützt (GH #1280)
- Implementierung von timer_create und verwandten Systemaufrufen.  Dies ermöglicht die GHC-Unterstützung (GH #307).
- Korrektur eines Problems, bei dem Ping eine Zeitangabe von 0,000 ms zurückgab (GH #1296)
- Rückgabe des richtigen Fehlercodes, wenn zu viele Dateien geöffnet werden.
- Korrektur eines Problems in WSL, bei dem die Netlink-Anforderung für Netzwerkschnittstellendaten mit EINVAL fehlschlägt, wenn die Hardwareadresse der Schnittstelle 32 Bytes groß ist (z.B. die Teredo-Schnittstelle)
   - Beachten Sie, dass das Linux-Hilfsprogramm „ip“ einen Fehler enthält, bei dem ein Absturz erfolgt, wenn WSL eine 32-Byte-Hardwareadresse meldet. Dies ist ein Fehler in „ip“, nicht in WSL. Mit dem Hilfsprogramm „ip“ wird die Länge des Zeichenfolgenpuffers fest codiert, der zum Ausgeben der Hardwareadresse verwendet wird, und dieser Puffer ist zu klein, um eine 32-Byte-Hardwareadresse auszugeben.
- Zusätzliche Korrekturen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 669 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 258 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>Build 14971

Allgemeine Windows-Informationen zu Build 14971 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).<br/>


### <a name="fixed"></a>Fest

 - Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.  Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Keine Änderungen seit 14965 </br>
Anzahl bestandener Tests: 664 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>Build 14965

Allgemeine Windows-Informationen zu Build 14965 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).<br/>


### <a name="fixed"></a>Fest

- Unterstützung für Netlink-Sockets RTM_GETLINK und RTM_GETADDR des NETLINK_ROUTE-Protokolls (GH #468)
  - Aktiviert ifconfig- und ip-Befehle für die Netzwerkenumeration.
  - Weitere Informationen finden Sie in unserem [Blogbeitrag zu WSL-Netzwerken](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).

- „/sbin“ befindet sich jetzt standardmäßig im Pfad des Benutzers.
- Der NT-Benutzerpfad wird jetzt standardmäßig an den WSL-Pfad angefügt (Sie können nun also „notepad.exe“ eingeben, ohne dem Linux-Pfad System32 hinzuzufügen).
- Hinzufügen von Unterstützung für /proc/sys/kernel/cap_last_cap
- NT-Binärdateien können nun aus WSL gestartet werden, wenn das aktuelle Arbeitsverzeichnis Nicht-ANSI-Zeichen enthält (GH #1254)
- Ermöglichen des Herunterfahrens für getrennten UNIX-Streamsocket
- Hinzufügen von Unterstützung für PR_GET_PDEATHSIG.
- Hinzufügen von Unterstützung für CLONE_PARENT
- Korrektur eines Fehlers, bei dem die Weiterleitung unterbrochen wird. Beispiel: bash -c "ls -alR /" | bash -c "cat" (GH #1214)
- Verarbeiten von Anforderungen zum Herstellen einer Verbindung mit dem aktuellen Terminal.
- Markieren von /proc/<pid>/oom_score_adj als beschreibbar.
- Hinzufügen des Ordners „/sys/fs/cgroup“.
- sched_setaffinity sollte den Wert der Affinitätsbitsmaske zurückgeben.
- Korrektur der ELF-Validierungslogik, die fälschlicherweise annimmt, dass Interpreterpfade weniger als 64 Zeichen lang sein müssen. (GH #743)
- Geöffnete Dateideskriptoren können das Konsolenfenster geöffnet lassen (GH #1187)
- Korrektur eines Fehlers, bei dem rename() mit einem nachgestellten Schrägstrich für den Zielnamen fehlschlägt (GH #1008)
- Implementierung der/proc/net/dev-Datei
- Korrektur von Pings mit 0,000 ms aufgrund der Timerauflösung.
- Implementierung von /proc/self/environ (GH #730)
- Weitere Fehlerbehebungen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 664 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>Build 14959

Allgemeine Windows-Informationen zu Build 14959 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).<br/>


### <a name="fixed"></a>Fest

- Verbesserte Pico-Prozessbenachrichtigung für Windows.  Weitere Informationen finden Sie im [WSL-Blog](/archive/blogs/wsl/wsl-antivirus-and-firewall-compatibility).
- Verbesserte Stabilität mit Windows-Interoperabilität
- Korrektur von Fehler 0x80070057 beim Starten von „bash.exe“, wenn der Enterprise Data Protection (EDP) aktiviert ist
- Weitere Fehlerbehebungen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 665 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>Build 14955

Allgemeine Windows-Informationen zu Build 14955 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).<br/>


### <a name="fixed"></a>Fest

 - Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.  Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 665 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>Build 14951

Allgemeine Windows-Informationen zu Build 14951 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>Neues Feature: Windows-/Ubuntu-Interoperabilität
Windows-Binärdateien können jetzt direkt über die WSL-Befehlszeile aufgerufen werden.  Dadurch haben Benutzer die Möglichkeit, mit Ihrer Windows-Umgebung und dem -System auf eine Weise zu interagieren, die bisher nicht möglich war.  Als kurzes Beispiel können Benutzer nun die folgenden Befehle ausführen:

```bash
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Weitere Informationen finden Sie hier:

- [WSL-Teamblog für Interop](/archive/blogs/wsl/windows-and-ubuntu-interoperability)<br/>
- [MSDN-Interop-Dokumentation](./interop.md)<br/>

### <a name="fixed"></a>Fest

- Ubuntu 16.04 (Xenial) wird jetzt für alle neuen WSL-Instanzen installiert.  Benutzer mit vorhandenen 14.04-Instanzen (Trusty) erhalten kein automatisches Upgrade.
- Das während der Installation festgelegte Gebietsschema wird jetzt angezeigt
- Terminalverbesserungen, einschließlich des Fehlers bei der Umleitung eines WSL-Prozesses an eine Datei, funktionieren nicht immer
- Die Konsolenlebensdauer muss an die Lebensdauer von „bash.exe“ gebunden sein
- Die Größe des Konsolenfensters sollte die sichtbare Größe und nicht die Puffergröße verwenden
- Weitere Fehlerbehebungen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 665 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>Build 14946

Allgemeine Windows-Informationen zu Build 14946 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).<br/>


### <a name="fixed"></a>Fest

- Korrektur eines Problems, das das Erstellen von WSL-Benutzerkonten für Benutzer mit NT-Benutzernamen verhindert hat, die Leerzeichen oder Anführungszeichen enthalten. 
- Änderung von VolFs und DrvFs, damit 0 für die Verknüpfungsanzahl des Verzeichnisses im Status zurückgegeben wird
- Unterstützung der IPV6_MULTICAST_HOPS-Socketoption.
- Einschränkung auf eine einzige Konsolen-E/A-Schleife pro TTY. Der folgende Befehl ist beispielsweise möglich:
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- Ersetzen von Leerzeichen durch Tabstoppzeichen in /proc/cpuinfo (GH #1115)
- DrvFs wird jetzt in den Einbindungsinformationen mit einem Namen angezeigt, der dem eingebundenen Windows-Volume entspricht
- /home und/root werden nun in den Einbindungsinformationen mit den richtigen Namen angezeigt
- Weitere Fehlerbehebungen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 665 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>Build 14942

Allgemeine Windows-Informationen zu Build 14942 finden Sie im [Windows-Blog](https://aka.ms/onefourninefourtwoooooo).<br/>


### <a name="fixed"></a>Fest

- Eine Reihe von Fehlerüberprüfungen, einschließlich des Netzwerkabsturzes durch „ATTEMPTED EXECUTE OF NOEXECUTE MEMORY“, der SSH blockiert hat
- inotify-Unterstützung für Benachrichtigungen, die von Windows-Anwendungen auf DrvFs generiert werden
- Implementierung von TCP_KEEPIDLE und TCP_KEEPINTVL für mongod. (GH #695)
- Implementierung des pivot_root-Systemaufrufs
- Implementierung der Socketoption für SO_DONTROUTE
- Weitere Fehlerbehebungen und Verbesserungen


### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 665 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>Build 14936

Allgemeine Windows-Informationen zu Build 14936 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).<br/>


Hinweis: WSL wird in einem zukünftigen Release Ubuntu Version 16.04 (Xenial) anstelle von Ubuntu 14.04 (Trusty) installieren.  Diese Änderung gilt für Insider, die neue Instanzen installieren (lxrun.exe /install oder erste Ausführung von „bash.exe“).  Vorhandene Instanzen mit Trusty werden nicht automatisch aktualisiert. Benutzer können mit dem Befehl „do-release-upgrade“ Ihr Trusty-Image auf Xenial aktualisieren.

### <a name="known-issue"></a>Bekanntes Problem
Bei WSL treten Probleme mit einigen Socketimplementierungen auf.  Die Fehlerüberprüfung manifestiert sich als Absturz mit dem Fehler „ATTEMPTED EXECUTE OF NOEXECUTE MEMORY“.  Die häufigste Variante dieses Problems ist ein Absturz bei der Verwendung von SSH.  Die Ursache ist bei internen Builds korrigiert und wird so bald wie möglich in Insider gepusht.

### <a name="fixed"></a>Fest

- Der chroot-Systemaufruf wurde implementiert.
- Verbesserungen in inotify ~~einschließlich Unterstützung für Benachrichtigungen, die von Windows-Anwendungen auf DrvFs generiert werden~~
  - Korrektur: Inotify-Unterstützung von Änderungen, die von Windows-Anwendungen stammen, ist zurzeit nicht verfügbar.
- Die Socketbindung an IPv6::<port n> unterstützt jetzt IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)
- Implementierung des WNOWAIT-Verhaltens für den waitid-Systemaufruf (GH #638)
- Unterstützung für IP-Socketoptionen IP_HDRINCL und IP_TTL
- read() der Länge Null sollte sofort zurückgegeben werden (GH #975)
- Ordnungsgemäße Verarbeitung von Dateinamen und Dateinamenpräfixen, die keinen NULL-Terminator in einer TAR-Datei enthalten.
- epoll-Unterstützung für/dev/null
- Korrektur der /dev/alarm-Zeitquelle
- Bash -c kann nun in eine Datei umgeleitet werden
- Weitere Fehlerbehebungen und Verbesserungen

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 664 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 264 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`chroot`<br/>
<br/>

## <a name="build-14931"></a>Build 14931

Allgemeine Windows-Informationen zu Build 14931 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).<br/>


### <a name="fixed"></a>Fest

 - Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.  Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.

<br/>

## <a name="build-14926"></a>Build 14926

Allgemeine Windows-Informationen zu Build 14926 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).<br/>


### <a name="fixed"></a>Fest

- Ping funktioniert nun in Konsolen, die nicht über Administratorberechtigungen verfügen.
- Ping6 wird jetzt auch ohne Administratorberechtigungen unterstützt.
- Inotify-Unterstützung für Dateien, die über WSL geändert wurden. (GH #216)
  - Unterstützte Flags:
    - inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watchEreignisse: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch-Attribute: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - Lesen der Ausgabe: LX_IN_ISDIR, LX_IN_IGNORED
  - Bekanntes Problem: Durch das Ändern von Dateien aus Windows-Anwendungen werden keine Ereignisse generiert
- Unix-Socket unterstützt jetzt SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP-Ergebnisse:
Anzahl bestandener Tests: 651 </br>
Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 258 </br>
[LTP-Testlaufprotokolle](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>Build 14915

Allgemeine Windows-Informationen zu Build 14915 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).<br/>


### <a name="fixed"></a>Fest
-  Socketpair für Unix-Datagrammsockets (GH #262)
- Unix-Socketunterstützung für SO_REUSEADDR
- Unix-Socketunterstützung für SO_BROADCAST (GH #568)
- Unix-Socketunterstützung für SOCK_SEQPACKET (GH #758, #546)
- Hinzufügen von Unterstützung für unix datagram socket send, recv und shutdown
- Korrektur einer Fehlerüberprüfung aufgrund einer ungültigen Überprüfung des mmap-Parameters für nicht feste Adressen. (GH #847)
- Unterstützung für das Anhalten/Fortsetzen von Terminalzuständen
- Unterstützung für TIOCPKT ioctl zum Entsperren des Bildschirmhilfsprogramms (GH #774)
    - Bekanntes Problem: Funktionstasten sind nicht funktionsfähig
- Korrektur einer Racebedingung in TimerFd, die dazu führen konnte, dass auf einen freigegebenen Member „ReaderReady“ durch LxpTimerFdWorkerRoutine zugegriffen wurde (GH #814)
- Aktivieren der Unterstützung für erneut startbaren Systemaufruf für futex, poll und clock_nanosleep
- Hinzufügen von Unterstützung für Bindungseinbindung
- Unterstützung für Aufheben der Freigabe für Einbindungsnamespace
    - Bekanntes Problem: Beim Erstellen eines neuen Einbindngsnamespace mit `unshare(CLONE_NEWNS)` zeigt das aktuelle Arbeitsverzeichnis weiterhin auf den alten Namespace
- Weitere Verbesserungen und Fehlerbehebungen

<br/>

## <a name="build-14905"></a>Build 14905

Allgemeine Windows-Informationen zu Build 14905 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).<br/>


### <a name="fixed"></a>Fest
- Erneut startbare Systemaufrufe werden jetzt unterstützt (GH #349, GH #520)
- Symbolische Verknüpfungen mit Verzeichnissen, die auf / wenden, sind jetzt funktionstüchtig (GH #650)
- Implementierung von RNDGETENTCNT ioctl für „/dev/random“
- Implementierung der /proc/[pid]/mounts, /proc/[pid]/mountinfo- und /proc/[pid]/mountstats-Dateien
- Weitere Fehlerbehebungen und Verbesserungen

</br>

## <a name="build-14901"></a>Build 14901
Der erste Insider-Build für das Windows 10 Anniversary Update-Release.

Allgemeine Windows-Informationen zu Build 14901 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).<br/>


### <a name="fixed"></a>Fest
- Korrektur eines Problems mit nachfolgenden Schrägstrichen
    - Befehle wie `$ mv a/c/ a/b/` funktionieren jetzt
- Installation von Eingabeaufforderungen, wenn das Ubuntu-Gebietsschema auf das Windows-Gebietsschema festgelegt werden soll
- Procfs-Unterstützung für den Ordner „ns“
- Hinzufügen von „mount“ und „unmount“ für tmpfs-, procfs-und sysfs-Dateisysteme
- Korrektur der 32-Bit-ABI-Signatur von mklod [at]
- Verschieben von Unix-Sockets in Dispatchmodell
- Mit setsockopt festgelegte recv-Puffergröße von INET-Socket muss berücksichtigt werden
- Implementierung des MSG_CMSG_CLOEXEC-Unis-Socket-Empfangsnachrichtenflags
- stdin/stdout-Pipeumleitung des Linux-Prozesses (GH #2)
    - Ermöglicht das Weiterleiten von bash -c-Befehlen in CMD.  Beispiel: >dir | bash -c "grep foo"
- Bash kann nun auf Systemen mit mehreren Auslagerungsdateien installiert werden (GH #538, #358)
- Standardpuffergröße des INET-Sockets sollte mit der Größe des Ubuntu- Standardsetups übereinstimmen
- Ausrichten von xattr-Systemaufrufen an listxattr
- Nur Rückgabe von Schnittstellen mit einer gültigen IPv4-Adresse von SIOCGIFCONF
- Korrektur der Signalatandardaktion, wenn von ptrace eingefügt
- Implementierung von /proc/sys/vm/min_free_kbytes
- Verwenden der Computerkontext-Registerwerte beim Wiederherstellen von Kontext in sigreturn
    - Dadurch wird das Problem behoben, dass Java und javac bei einigen Benutzern nicht mehr reagiert haben
- Implementierung von /proc/sys/kernel/hostname

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>Update von Build 14388 auf Windows 10 Anniversary Update
Allgemeine Windows-Informationen zu Build 14388 finden Sie im [Windows-Blog](https://aka.ms/14388wip). <br/>

### <a name="fixed"></a>Fest
- Korrekturen als Vorbereitung auf das Windows 10 Anniversary Update am 02.08.
  - Weitere Informationen zu WSL im Anniversary Update finden Sie in unserem [Blog](/archive/blogs/wsl/).

<br/>

## <a name="build-14376"></a>Build 14376
Allgemeine Windows-Informationen zu Build 14376 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/). <br/>

### <a name="fixed"></a>Fest
- Entfernen einiger Instanzen, in denen apt-get nicht mehr reagiert (GH #493)
- Korrektur eines Problems, bei dem leere Einbindungen nicht ordnungsgemäß verarbeitet wurden
- Korrektur eines Problems, bei dem Ramdisks nicht ordnungsgemäß eingebunden wurden
- Änderung von „unix socket accept“ für die Unterstützung von Flags (Teil von GH #451)
- Korrektur eines allgemeinen netzwerkbezogenen Bluescreens
- Korrektur des Bluescreens beim Zugriff auf /proc/[pid]/task (GH #523)
- Korrektur hoher CPU-Auslastung für einige Pty-Szenarien (GH #488, #504)
- Weitere Fehlerbehebungen und Verbesserungen

<br/>

## <a name="build-14371"></a>Build 14371
Allgemeine Windows-Informationen zu Build 14371 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/). <br/>

### <a name="fixed"></a>Fest
- Korrektur der Timingracebedingung mit SIGCHLD und wait() bei Verwendung von ptrace
- Korrektur von Verhalten, wenn Pfade ein nachfolgendes Zeichen / aufweisen (GH #432)
- Korrektur eines Problems, bei dem Umbenennen/Aufheben der Verknüpfung aufgrund von geöffneten Handles für untergeordnete Elemente fehlschlägt
- Weitere Fehlerbehebungen und Verbesserungen

<br/>

## <a name="build-14366"></a>Build 14366
Allgemeine Windows-Informationen zu Build 14366 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/). <br/>

### <a name="fixed"></a>Fest
- Korrektur der Dateierstellung durch symbolische Verknüpfungen
-   Hinzugefügter von listxattr für Python (GH 385)
-   Weitere Fehlerbehebungen und Verbesserungen

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
-   Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>Build 14361
Allgemeine Windows-Informationen zu Build 14361 finden Sie im [Windows-Blog](https://aka.ms/wip14361). <br/>

### <a name="fixed"></a>Fest
- Für DrvFs wird nun bei der Ausführung in Bash unter Ubuntu unter Windows die Groß-/Kleinschreibung beachtet.
  - Benutzer können case.txt und CASE.TXT auf Ihren /mnt/c-Laufwerken verwenden
  - Die Beachtung von Groß-/Kleinschreibung wird nur in Bash unter Ubuntu unter Windows unterstützt. Außerhalb von Bash zeigt NTFS die Dateien richtig an, aber es kann zu unerwartetem Verhalten bei der Interaktion mit den Dateien von Windows kommen.
  - Für den Stamm der einzelnen Volumes (d.h. /mnt/c) wird die Groß-/Kleinschreibung nicht beachtet.
  - Weitere Informationen zum Verarbeiten dieser Dateien in Windows finden Sie [hier](https://support.microsoft.com/kb/100625).
- Stark verbesserte PTY-/TTY-Unterstützung.  Anwendungen wie TMUX werden jetzt unterstützt (GH #40)
- Korrektur eines Installationsproblems, bei dem Benutzerkonten nicht immer erstellt wurden
- Optimierte Befehlszeilen-Argumentstruktur, die eine extrem lange Argumentliste zulässt. (GH #153)
- Jetzt können chmod read_only-Dateien aus DrvFs gelöscht werden.
- Korrektur einiger Instanzen, bei denen das Terminal beim Trennen nicht mehr reagiert (GH #43)
- chmod und chown funktionieren jetzt auf TTY-Geräten
- Verbindung mit 0.0.0.0 und :: as localhost zulassen (GH #388)
- Sendmsg/recvmsg verarbeitet nun eine E/A-Vektorlänge > 1 (Teil von GH #376)
- Benutzer können jetzt die automatisch generierte Hostdatei ablehnen (GH #398)
- Automatisches Zuordnen des Linux-Gebietsschemas zum NT-Gebietsschema während der Installation (GH #11)
- Hinzufügen der /proc/sys/vm/swappiness-Datei (GH #306)
- strace wird jetzt ordnungsgemäß beendet
- Ermöglichen des erneuten Öffnens von Pipes über /proc/self/fd (GH #222)
- Ausblenden von Verzeichnissen unter „%LOCALAPPDATA%\lxss“ aus DrvFs (GH #270)
- Bessere Verarbeitung von bash.exe ~.  Befehle wie „bash ~ -c ls“ werden jetzt unterstützt (GH #467)
- Sockets benachrichtigen nun darüber, dass epoll read beim Herunterfahren verfügbar ist (GH #271)
- lxrun/uninstall arbeitet besser beim Löschen der Dateien und Ordner.
- Korrektur für ps-f (GH #246)
- Verbesserte Unterstützung für X11-Apps, z.B. xEmacs (GH #481)
- Aktualisierte anfängliche Threadstapelgröße, um der standardmäßigen Ubuntu-Einstellung zu entsprechen und die Größe ordnungsgemäß an den get_rlimit-Systemaufruf zu melden (GH #172, #258)
- Verbesserte Berichterstellung von Pico-Prozessimagenamen (z.B. für die Überwachung)
- Implementierung von /proc/mountinfo für df-Befehl
- Korrektur des Fehlercodes der symbolischen Verknüpfung für den untergeordneten Namen . und .
- Weitere optimierende Fehlerbehebungen und Verbesserungen

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>Build 14352
Allgemeine Windows-Informationen zu Build 14352 finden Sie im [Windows-Blog](https://aka.ms/wip14352).<br/>


### <a name="fixed"></a>Fest
- Korrektur eines Problems, bei dem große Dateien nicht ordnungsgemäß heruntergeladen bzw. ordnungsgemäß erstellt wurden.  Dadurch sollte die Blockierung von npm und anderen Szenarien aufgehoben werden (GH #3, GH #313)
- Entfernen einiger Instanzen, in denen Sockets nicht mehr reagieren
- Korrektur einiger ptrace-Fehler
- Korrektur eines Problems, bei dem WSL Dateinamen mit mehr als 255 Zeichen zuließ
- Verbesserte Unterstützung nicht-englischer Zeichen
- Hinzufügen aktueller Windows-Zeitzonendaten und Festlegen als Standard
- Eindeutige Geräte-IDs für jeden Einbindungspunkt (jre-Korrektur – GH #49)
- Korrektur eines Problems mit Pfaden, die „.“ und „..“ enthalten
- Hinzufügen von FIFO-Unterstützung (GH #71)
- Aktualisiertes Format von „resolv.conf“ entsprechend dem nativen Ubuntu-Format
- procfs-Bereinigung
- Aktivierten von Ping für Administratorkonsolen (GH #18)

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>Build 14342
Allgemeine Windows-Informationen zu Build 14342 finden Sie im [Windows-Blog](https://aka.ms/wip14342). <br/>

Informationen zu VolFs und DriveFs finden Sie im [WSL-Blog](/archive/blogs/wsl/). <br/>

### <a name="fixed"></a>Fest
- Korrektur eines Installationsproblems, wenn der Windows-Benutzer Unicode-Zeichen im Benutzernamen enthielt
- Die Problemumgehung „apt-get update udev“ in den FAQ wird jetzt standardmäßig bei der ersten Ausführung bereitgestellt
- Aktivierte symbolische Verknüpfungen in DriveFs-Verzeichnissen (/mnt/<drive>)
- Symbolische Verknüpfungen funktionieren nun zwischen DriveFs und VolFs
- Korrektur des Pfadanalyseproblems auf oberster Ebene: ls .// funktioniert jetzt wie erwartet
- npm install auf DriveFs und die -g-Optionen funktionieren jetzt
- Korrektur eines Problems, das den Start des PHP-Servers verhinderte
- Aktualisierte Standardumgebungswerte, z.B. $PATH, um nativem Ubuntu besser zu entsprechen
- Hinzufügen eines wöchentlichen Wartungstasks in Windows zum Aktualisieren des apt-Paketcaches
- Korrektur eines Problems bei der Überprüfung von ELF-Headern, WSL unterstützt jetzt alle Melkor-Optionen
- Zsh-Shell ist funktionsfähig
- Vorkompilierte Go-Binärdateien werden jetzt unterstützt
- Eingabeaufforderung bei der ersten Ausführung von „bash.exe“ ist nun richtig lokalisiert
- /proc/meminfo gibt jetzt richtige Informationen zurück
- Sockets werden jetzt in VFS unterstützt
- /dev jetzt als tempfs eingebunden
- Fifo wird jetzt unterstützt
- Mehrkernsysteme werden nun ordnungsgemäß in /proc/cpuinfo angezeigt
- Weitere Verbesserungen und Fehlermeldungen, die während der ersten Ausführung heruntergeladen werden
- Systemaufrufverbesserungen und -fehlerbehebungen. Unterstützte Systemaufrufliste unten.
- Weitere Fehlerbehebungen und Verbesserungen

### <a name="known-issues"></a>Bekannte Probleme
- „.“ wird in einigen Fällen nicht ordnungsgemäß auf DriveFs aufgelöst

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen. Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a>Build 14332

Allgemeine Windows-Informationen zu Build 14332 finden Sie im [Windows-Blog](https://aka.ms/wip14332). <br/>


### <a name="fixed"></a>Fest
- Bessere resolv.conf-Generierung einschließlich Priorisieren von DNS-Einträgen
- Problem beim Verschieben von Dateien und Verzeichnissen zwischen/mnt- und Nicht-/mnt-Laufwerken
- TAR-Dateien können jetzt mit symbolischen Verknüpfungen erstellt werden.
- Hinzufügen des /run/lock-Standardverzeichnisses bei der Instanzerstellung
- Aktualisieren von /dev/null, um die richtigen Statusinformationen zurückzugeben
- Weitere Fehler beim Herunterladen während der ersten Ausführung
- Systemaufrufverbesserungen und -fehlerbehebungen. Unterstützte Systemaufrufliste unten.
- Weitere optimierende Fehlerbehebungen und Verbesserungen

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie den neuen Systemaufruf, der in WSL implementiert ist. Der Systemaufruf in dieser Liste wird in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>Build 14328

Allgemeine Windows-Informationen zu Build 14332 finden Sie im [Windows-Blog](https://aka.ms/wip14328). <br/>


### <a name="new-features"></a>Neue Funktionen
* Jetzt werden Linux-Benutzer unterstützt.  Bei der Installation von Bash unter Ubuntu unter Windows werden Sie aufgefordert, einen Linux-Benutzer zu erstellen.  Weitere Informationen finden Sie unter https://aka.ms/wslusers.
* Der Hostname ist jetzt auf den Windows-Computernamen festgelegt, nicht mehr auf @localhost
* Weitere Informationen zu Build 14328 finden Sie unter: https://aka.ms/wip14328

### <a name="fixed"></a>Fest
* Verbesserungen von symbolischen Verknüpfungen für Nicht-/mnt/<drive>-Dateien
    * Die npm-Installation funktioniert jetzt
    * jdk/jre kann nun mithilfe der Anweisungen installiert werden, die Sie [hier](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html) finden.
    * Bekanntes Problem: Symbolische Verknüpfungen funktionieren für Windows-Einbindungen nicht.  Diese Funktionen werden in einem späteren Build verfügbar sein.
* top und htop werden jetzt angezeigt
* Zusätzliche Fehlermeldungen bei einigen Installationsfehlern
* Systemaufrufverbesserungen und -fehlerbehebungen.  Unterstützte Systemaufrufliste unten.
* Weitere optimierende Fehlerbehebungen und Verbesserungen

### <a name="syscall-support"></a>Unterstützung von Systemaufrufen
Im folgenden finden Sie eine Liste der Systemaufrufe, die einige Implementierungen in WSL aufweisen.  Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>