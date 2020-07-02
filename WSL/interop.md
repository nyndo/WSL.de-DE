---
title: Windows-Interoperabilität mit Linux
description: Beschreibt die Windows-Interoperabilität mit Linux-Distributionen, die im Windows-Subsystem für Linux ausgeführt werden.
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 2a9b6c8ac65fe28e029ada7f86475c44220a93fe
ms.sourcegitcommit: cb8a61e7de08b1c18622fc78bc5dfa38786e921a
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2020
ms.locfileid: "84663133"
---
# <a name="windows-interoperability-with-linux"></a>Windows-Interoperabilität mit Linux

Das Windows-Subsystem für Linux (WSL) verbessert die Integration zwischen Windows und Linux kontinuierlich.  Sie haben folgende Möglichkeiten:

* Ausführen von Windows-Tools (z. B. „notepad.exe“) über eine Linux-Befehlszeile aus (d. h. Ubuntu).
* Ausführen von Linux-Tools (z. B. „grep“) über eine Windows-Befehlszeile (d. h. PowerShell).
* Freigeben von Umgebungsvariablen zwischen Linux und Windows. (Build 17063+)

> [!NOTE]
> Wenn Sie das Creators Update (Okt. 2017, Build 16299) oder das Anniversary Update (Aug. 2016, Build 14393) ausführen, fahren Sie mit [Frühere Versionen von Windows 10](#earlier-versions-of-windows-10) fort.

## <a name="run-linux-tools-from-a-windows-command-line"></a>Ausführen von Linux-Tools über eine Windows-Befehlszeile

Führen Sie Linux-Binärdateien über die Windows-Eingabeaufforderung (CMD oder PowerShell) mithilfe von `wsl <command>` (oder `wsl.exe <command>`) aus.

Beispiel:

```powershell
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

Auf diese Weise aufgerufene Binärdateien:

* Verwenden das gleiche Arbeitsverzeichnis wie die aktuelle CMD- oder PowerShell-Eingabeaufforderung.
* Werden als WSL-Standardbenutzer aus geführt.
* Sie verfügen über dieselben Windows-Administratorrechte wie der aufrufende Prozess und das Terminal.

Der auf `wsl` (oder `wsl.exe`) folgende Linux-Befehl wird wie ein beliebiger Befehl verarbeitet, der in WSL ausgeführt wird.  Dinge wie sudo, Piping und Dateiumleitung funktionieren.

Beispiel für die Verwendung von sudo zum Aktualisieren Ihrer Linux-Standardverteilung:

```powershell
C:\temp> wsl sudo apt-get update
```

Nachdem Sie diesen Befehl ausgeführt haben, wird der Benutzername Ihrer Linux-Standardverteilung angezeigt, und Sie werden zur Eingabe Ihres Kennworts aufgefordert. Nachdem Sie Ihr Kennwort ordnungsgemäß eingegeben haben, werden von Ihrer Verteilung die Updates heruntergeladen.

## <a name="mixing-linux-and-windows-commands"></a>Kombinieren von Linux- und Windows-Befehlen

Hier finden Sie einige Beispiele für das Kombinieren von Linux- und Windows-Befehlen unter Verwendung von PowerShell.

Um den Linux-Befehl `ls -la` zum Auflisten von Dateien und den PowerShell-Befehl `findstr` zum Filtern der Ergebnisse nach Wörtern zu verwenden, die die Zeichenfolge „git“ enthalten, kombinieren Sie die Befehle:

```powershell
wsl ls -la | findstr "git"
```

Um den PowerShell-Befehl `dir` zum Auflisten von Dateien und den Linux-Befehl `grep` zum Filtern der Ergebnisse nach Wörtern zu verwenden, die die Zeichenfolge „git“ enthalten, kombinieren Sie die Befehle:

```powershell
C:\temp> dir | wsl grep git
```

Um den Linux-Befehl `ls -la` zum Auflisten von Dateien und den PowerShell-Befehl `> out.txt` zum Drucken dieser Liste in eine Textdatei mit dem Namen „out.txt“ zu verwenden, kombinieren Sie die Befehle:

```powershell
C:\temp> wsl ls -la > out.txt
```

Die an `wsl.exe` übergebenen Befehle werden ohne Änderung an den WSL-Prozess weitergeleitet.  Dateipfade müssen im WSL-Format angegeben werden.

So verwenden Sie den Linux-Befehl `ls -la` zum Auflisten von Dateien im `/proc/cpuinfo`-Linux-Dateisystempfad mithilfe von PowerShell:

```powershell
C:\temp> wsl ls -la /proc/cpuinfo
```

So verwenden Sie den Linux-Befehl `ls -la` zum Auflisten von Dateien im `C:\Program Files`-Windows-Dateisystempfad mithilfe von PowerShell:

```powershell
C:\temp> wsl ls -la "/mnt/c/Program Files"
```

## <a name="run-windows-tools-from-linux"></a>Ausführen von Windows-Tools aus Linux

WSL kann Windows-Tools direkt über die WSL-Befehlszeile mithilfe von `[tool-name].exe` ausführen.  Beispiel: `notepad.exe`.

<!-- Craig - could you help add a section with an example here to explain this scenario: "To access your Linux files using a Windows tool, use `\\wsl$\<distroName>\'` as the file path." Currently it I can just enter `notepad.exe foo.txt` and it seems to work fine, so explaining a situation where the file path is needed would be helpful. -->

Anwendungen, die auf diese Weise ausgeführt werden, besitzen die folgenden Eigenschaften:

* Sie behalten das Arbeitsverzeichnis als das Verzeichnis der WSL-Eingabeaufforderung bei (in den meisten Fällen, Ausnahmen werden unten erläutert).
* Sie verfügen über die gleichen Berechtigungen wie der WSL-Prozess.
* Sie werden als aktiver Windows-Benutzer ausgeführt.
* Sie werden im Task-Manager von Windows so angezeigt, als würden die direkt über die CMD-Eingabeaufforderung ausgeführt.

Ausführbare Windows-Dateien, die in WSL ausgeführt werden, werden ähnlich wie native ausführbare Linux-Dateien verarbeitet. Piping, Umleitungen und sogar Hintergrundverarbeitung funktionieren wie erwartet.

Um das Windows-Tool `ipconfig.exe` auszuführen, das Linux-Tool `grep` zum Filtern der „IPv4“-Ergebnisse und das Linux-Tool `cut` zum Entfernen der Spaltenfelder zu verwenden,geben Sie aus einer Linux-Verteilung (z. B. Ubuntu) Folgendes ein:

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Sehen wir uns ein Beispiel für das Kombinieren von Windows- und Linux-Befehlen an. Öffnen Sie Ihre Linux-Verteilung (d. h. Ubuntu) und erstellen Sie eine Textdatei: `touch foo.txt`. Verwenden Sie nun den Linux-Befehl `ls -la`, um die direkten Dateien und deren Erstellungsdetails aufzulisten, sowie das Windows PowerShell-Tool `findstr.exe`, um die Ergebnisse zu filtern, sodass nur Ihre `foo.txt`-Datei in den Ergebnissen angezeigt wird:

```bash
ls -la | findstr.exe foo.txt
```

Windows-Tools müssen die Dateierweiterung enthalten, der Groß-/Kleinschreibung der Datei Rechnung tragen und ausführbare Dateien sein.  Nicht ausführbare Dateien, einschließlich Batchskripts.  Native CMD-Befehle wie `dir` können mit einem Befehl `cmd.exe /C` ausgeführt werden.

Listen Sie z. B. den Inhalt Ihres Windows-Dateisystemverzeichnisses „C:\“ auf, indem Sie Folgendes eingeben:

```bash
cmd.exe /C dir
```

Oder verwenden Sie den Befehl `ping`, um eine Echoanforderung an die Website „microsoft.com“ zu senden:

```bash
ping.exe www.microsoft.com
```

Parameter werden unverändert an die Windows-Binärdatei übergeben. Beispielsweise öffnet der folgende Befehl `C:\temp\foo.txt` in `notepad.exe`:

```bash
notepad.exe "C:\temp\foo.txt"
```

Dies funktioniert auch:

```bash
notepad.exe C:\\temp\\foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Freigeben von Umgebungsvariablen zwischen Windows und WSL

WSL und Windows verwenden `WSLENV`, eine spezielle Umgebungsvariable, die entwickelt wurde, um Windows- und Linux-Verteilungen, die unter WSL ausgeführt werden, zu verbinden.

Eigenschaften einer `WSLENV`-Variablen:

* Die Variable ist freigegeben, und sie ist sowohl in Windows- als auch in WSL-Umgebungen vorhanden.
* Es handelt sich um eine Liste von Umgebungsvariablen, die von Windows und WSL gemeinsam genutzt werden können.
* Sie kann Umgebungsvariablen so formatieren, dass sie in Windows und WSL gut funktionieren.
* Sie kann den Flow zwischen WSL und Win32 unterstützen.

> [!NOTE]
> Vor 17063 war `PATH` die einzige Windows-Umgebungsvariable, auf die WSL zugreifen konnte (sodass Sie ausführbare Win32-Dateien unter WSL starten konnten). Ab 17063 wird `WSLENV` unterstützt.

## <a name="wslenv-flags"></a>WSLENV-Flags

In `WSLENV` sind vier Flags verfügbar, die beeinflussen, wie die Umgebungsvariable übersetzt wird.

`WSLENV`-Flags:

* `/p`: Übersetzt den Pfad zwischen Pfaden im WSL-/Linux-Stil und Win32-Pfaden.
* `/l`: Gibt an, dass die Umgebungsvariable eine Liste von Pfaden ist.
* `/u`: Gibt an, dass diese Umgebungsvariable nur beim Ausführen von WSL aus Win32 einbezogen werden soll.
* `/w`: Gibt an, dass diese Umgebungsvariable nur beim Ausführen von Win32 aus WSL einbezogen werden soll.

Diese Flags können nach Bedarf kombiniert werden.

[Hier finden Sie weitere Informationen über WSLENV](https://devblogs.microsoft.com/commandline/share-environment-vars-between-wsl-and-windows/), einschließlich FAQs und Beispiele für das Festlegen des Werts von WSLENV auf eine Verkettung anderer vordefinierter Umgebungsvariablen, jeweils mit einem Schrägstrich als Suffix, gefolgt von Flags, um Spezifizieren, wie der Wert übersetzt werden soll, und für die Übergabe von Variablen mit einem Skript. Dieser Artikel enthält auch ein Beispiel für das Einrichten einer Entwicklungsumgebung mit der [Programmiersprache „Go“](https://golang.org/), die für die gemeinsame Nutzung eines GOPATH zwischen WSL und Win32 konfiguriert ist.

## <a name="disable-interoperability"></a>Deaktivieren der Interoperabilität

Benutzer können die Möglichkeit zum Ausführen von Windows-Tools für eine einzelne WSL-Sitzung deaktivieren, indem Sie den folgenden Befehl als root ausführen:

```bash
echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Zum erneuten Aktivieren von Windows-Binärdateien beenden Sie alle WSL-Sitzungen und führen „bash.exe“ erneut aus, oder führen Sie den folgenden Befehl als root aus:

```bash
echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

Die Deaktivierung von Interop wird nicht zwischen WSL-Sitzungen beibehalten. Interop wird erneut aktiviert, wenn eine neue Sitzung gestartet wird.

## <a name="earlier-versions-of-windows-10"></a>Frühere Windows 10-Versionen

Für die Interoperabilitätsbefehle in früheren Windows 10-Versionen bestehen mehrere Unterschiede. Wenn Sie ein Creators Update (Okt. 2017, Build 16299) oder ein Anniversary Update (Aug. 2016, Build 14393) von Windows 10 ausführen, empfehlen wir, dass Sie [auf die neueste Windows-Version aktualisieren](ms-settings:windowsupdate). Wenn dies jedoch nicht möglich ist, werden nachfolgend einige der Unterschiede in der Interoperabilität erläutert.

Zusammenfassung:

* `bash.exe` wurde durch `wsl.exe` ersetzt.
* Die `-c`-Option zum Ausführen eines einzelnen Befehls ist mit `wsl.exe` nicht erforderlich.
* Der Windows-Pfad ist in `$PATH` von WSL enthalten.
* Der Prozess zum Deaktivieren von Interop ist unverändert.

Linux-Befehle können an der Windows-Eingabeaufforderung oder in PowerShell ausgeführt werden. Für frühe Windows-Versionen müssen Sie jedoch möglicherweise den Befehl `bash` verwenden. Beispiel:

```powershell
C:\temp> bash -c "ls -la"
```

Dinge wie Eingabe, Piping und Dateiumleitung funktionieren erwartungsgemäß.

Die an `bash -c` übergebenen WSL-Befehle werden ohne Änderung an den WSL-Prozess weitergeleitet.  Dateipfade müssen im WSL-Format angegeben werden, und es muss darauf geachtet werden, dass relevante Zeichen mit Escapezeichen versehen werden. Beispiel:

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
```

Oder:

```powershell
C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
```

Wenn Sie ein Windows-Tool aus einer WSL-Verteilung in einer früheren Version von Windows 10 aufrufen, müssen Sie den Verzeichnispfad angeben. Geben Sie z. B. in der WSL-Befehlszeile Folgendes ein:

```bash
/mnt/c/Windows/System32/notepad.exe
```

In WSL werden diese ausführbaren Dateien ähnlich wie native ausführbare Linux-Dateien behandelt.  Dies bedeutet, dass das Hinzufügen von Verzeichnissen zum Linux-Pfad und das Piping zwischen Befehlen erwartungsgemäß funktioniert.  Beispiel:

```bash
export PATH=$PATH:/mnt/c/Windows/System32
```
Oder

```bash
ipconfig.exe | grep IPv4 | cut -d: -f2
```

Die Windows-Binärdatei muss die Dateierweiterung enthalten, der Groß-/Kleinschreibung der Datei Rechnung tragen und eine ausführbare Dateien sein.  Nicht ausführbare Dateien einschließlich Batchskripts und Befehle wie `dir` können mit dem Befehl `/mnt/c/Windows/System32/cmd.exe /C` ausgeführt werden. Beispiel:

```bash
/mnt/c/Windows/System32/cmd.exe /C dir
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

* [WSL-Blogbeitrag zur Interoperabilität von 2016](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)
