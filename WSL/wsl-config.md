---
title: Verwalten von Linux-Distributionen
description: Referenzliste und Konfigurieren mehrerer Linux-Distributionen, die unter dem Windows-Subsystem für Linux ausgeführt werden.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: b8aa740233f3ac9517744212eb7b362a18378822
ms.sourcegitcommit: 90577817a9321949da2a3971b4c78bb00f6d977f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/10/2020
ms.locfileid: "88039413"
---
# <a name="wsl-commands-and-launch-configurations"></a>WSL-Befehle und Start Konfigurationen

## <a name="ways-to-run-wsl"></a>Möglichkeiten zum Ausführen von WSL

Es gibt mehrere Möglichkeiten, eine Linux-Distribution mit WSL auszuführen, nachdem Sie [installiert](install-win10.md)wurde.

1. Öffnen Sie die Linux-Distribution, indem Sie im Windows-Startmenü den Namen der installierten Verteilungen eingeben. Beispiel: "Ubuntu".
2. Geben Sie an der Windows-Eingabeaufforderung oder in PowerShell den Namen der installierten Distribution ein. Beispiel: `ubuntu`
3. Geben Sie an der Windows-Eingabeaufforderung oder PowerShell Folgendes ein, um die Standard-Linux-Distribution in der aktuellen Befehlszeile zu öffnen: `wsl.exe` .
4. Geben Sie an der Windows-Eingabeaufforderung oder PowerShell Folgendes ein, um die Standard-Linux-Distribution in der aktuellen Befehlszeile zu öffnen: `wsl [command]` .

Welche Methode Sie verwenden sollten, hängt vom Anwendungsfall ab. Wenn Sie in einer Windows-Eingabeaufforderung oder einem PowerShell-Fenster eine WSL-Befehlszeile geöffnet haben und den Vorgang beenden möchten, geben Sie den folgenden Befehl ein: `exit` .

## <a name="launch-wsl-by-distribution"></a>Starten von WSL nach Distribution

Durch das Ausführen einer Distribution mit ihrer distributionsspezifischen Anwendung wird diese Distribution in einem eigenen Konsolenfenster gestartet.

![Starten von WSL aus dem Startmenü](media/start-launch.png)

Dies entspricht dem Klicken auf „Starten“ im Microsoft Store.

![Starten von WSL aus dem Microsoft Store](media/store-launch.png)

Sie können die Distribution auch über die Befehlszeile ausführen, indem Sie `[distribution].exe` ausführen.

Der Nachteil, eine Distribution auf diese Weise über die Befehlszeile auszuführen, besteht darin, dass sich Ihr Arbeitsverzeichnis automatisch aus dem aktuellen Verzeichnis in das Startverzeichnis der Distribution ändert.

**Beispiel: (mithilfe von PowerShell)**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>wsl und wsl [Befehl]

Die beste Methode zum Ausführen von WSL über die Befehlszeile ist die Verwendung von `wsl.exe`.

**Beispiel: (mithilfe von PowerShell)**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

`wsl` behält nicht nur das aktuelle Arbeitsverzeichnis bei, sondern ermöglicht es auch, einen einzelnen Befehl neben Windows-Befehlen auszuführen.

**Beispiel: (mithilfe von PowerShell)**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

**Beispiel: (mithilfe von PowerShell)**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```

## <a name="managing-multiple-linux-distributions"></a>Verwalten mehrerer Linux-Distributionen

In Windows 10, Version 1903 [und](ms-settings:windowsupdate)höher, können Sie verwenden, `wsl.exe` um die Verteilungen im Windows-Subsystem für Linux (WSL) zu verwalten, einschließlich der Auflistung verfügbarer Verteilungen, der Festlegung einer Standardverteilung und der Deinstallieren von Verteilungen.

Jede Linux-Distribution verwaltet unabhängig ihre eigenen Konfigurationen. Führen Sie `[distro.exe] /?` aus, um distributionsspezifische Befehle anzuzeigen.  Beispiel: `ubuntu /?`.

## <a name="list-distributions"></a>Auflisten von Distributionen

`wsl -l` , `wsl --list`  
Listet verfügbare Linux-Distributionen für WSL auf.  Wenn eine Distribution aufgeführt wird, ist sie installiert und einsatzbereit.

`wsl --list --all`Listet alle Verteilungen auf, einschließlich derjenigen, die derzeit nicht verwendbar sind.  Sie werden möglicherweise gerade installiert, deinstalliert oder sind beschädigt.  

`wsl --list --running`Listet alle Verteilungen auf, die zurzeit ausgeführt werden.

## <a name="set-a-default-distribution"></a>Festlegen einer Standarddistribution

Die WSL-Standarddistribution ist die Distribution, die ausgeführt wird, wenn Sie `wsl` in einer Befehlszeile ausführen.

`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`

Legt die Standarddistribution auf `<DistributionName>` fest.

**Beispiel: (mithilfe von PowerShell)**  
`wsl -s Ubuntu` würde die Standarddistribution auf Ubuntu festlegen.  Wenn jetzt `wsl npm init` ausgeführt wird, wird Ubuntu ausgeführt.  Wenn `wsl` ausgeführt wird, wird eine Ubuntu-Sitzung geöffnet.

## <a name="unregister-and-reinstall-a-distribution"></a>Aufheben der Registrierung und Neuinstallation einer Distribution

Obwohl Linux-Distributionen über den Microsoft Store installiert werden können, können Sie nicht über den Store deinstalliert werden.  WSL Config ermöglicht die Aufhebung der Registrierung/Deinstallation von Distributionen.

Durch das Aufheben der Registrierung können Distributionen auch erneut installiert werden.

> **Vorsicht:** Nachdem die Registrierung aufgehoben wurde, gehen alle Daten, Einstellungen und Software, die dieser Verteilung zugeordnet sind, dauerhaft verloren.  Bei der erneuten Installation aus dem Store wird eine saubere Kopie der Distribution installiert.

`wsl --unregister <DistributionName>`  
Hebt die Registrierung der Distribution bei WSL auf, damit Sie erneut installiert oder bereinigt werden kann.

Beispiel: `wsl --unregister Ubuntu` würde Ubuntu aus den in WSL verfügbaren Distributionen entfernen.  Beim Ausführen von `wsl --list` würde diese Distribution nicht aufgelistet.

Zum erneuten Installieren suchen Sie die Distribution im Microsoft Store, und wählen Sie dann „Starten“ aus.

## <a name="run-as-a-specific-user"></a>Ausführen als ein bestimmter Benutzer

`wsl -u <Username>`, `wsl --user <Username>`

Führen Sie WSL als der angegebene Benutzer aus. Beachten Sie, dass der Benutzer in der WSL-Distribution vorhanden sein muss.

## <a name="change-the-default-user-for-a-distribution"></a>Ändern des Standard Benutzers für eine Distribution

`<DistributionName> config --default-user <Username>`

Ändern Sie den Standardbenutzer für Ihre Verteilungs Anmeldung. Der Benutzer muss bereits innerhalb der Verteilung vorhanden sein, damit er der Standardbenutzer wird. 

Beispiel: `ubuntu config --default-user johndoe` würde den Standardbenutzer für die Ubuntu-Distribution in den Benutzer "JohnDoe" ändern.

> [!NOTE]
> Wenn Sie Probleme haben, den Namen der Verteilung herauszufinden, finden Sie weitere Informationen unter [Auflisten von Verteilungen](https://docs.microsoft.com/windows/wsl/wsl-config#list-distributions) für den Befehl zum Auflisten des offiziellen Namens der installierten Verteilungen. 

## <a name="run-a-specific-distribution"></a>Ausführen als eine bestimmte Distribution

`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`

Führen Sie eine angegebene Distribution von WSL aus. Kann zum Senden von Befehlen an eine bestimmte Distribution verwendet werden, ohne die Standardeinstellung ändern zu müssen.

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a>Verwalten von mehreren Linux-Distributionen in früheren Windows-Versionen

In Windows 10 vor Version 1903 sollte das Befehlszeilen Tool WSL config ( `wslconfig.exe` ) zum Verwalten von Linux-Distributionen verwendet werden, die unter dem Windows-Subsystem für Linux (WSL) ausgeführt werden.  Damit können Sie verfügbare Distributionen auflisten, eine Standarddistribution festlegen und Distributionen deinstallieren.

Während WSL Config für Einstellungen nützlich ist, die Distributionen umspannen oder koordinieren, verwaltet jede Linux-Distribution unabhängig ihre eigenen Konfigurationen.  Führen Sie `[distro.exe] /?` aus, um distributionsspezifische Befehle anzuzeigen.  Beispiel: `ubuntu /?`.

Um alle verfügbaren Optionen für wslconfig anzuzeigen, führen Sie Folgendes aus: `wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

Zum Auflisten von Verteilungen verwenden Sie Folgendes:

`wslconfig /list`  
Listet verfügbare Linux-Distributionen für WSL auf.  Wenn eine Distribution aufgeführt wird, ist sie installiert und einsatzbereit.

`wslconfig /list /all`  
Listet alle Distributionen auf, einschließlich derjenigen, die zurzeit nicht verwendbar sind.  Sie werden möglicherweise gerade installiert, deinstalliert oder sind beschädigt.  

So legen Sie eine Standardverteilung fest, die ausgeführt wird, wenn Sie `wsl` in einer Befehlszeile ausführen:

`wslconfig /setdefault <DistributionName>`Legt die Standardverteilung auf fest `<DistributionName>` .

**Beispiel: (mithilfe von PowerShell)**  
`wslconfig /setdefault Ubuntu` würde die Standarddistribution auf Ubuntu festlegen.  Wenn jetzt `wsl npm init` ausgeführt wird, wird Ubuntu ausgeführt.  Wenn `wsl` ausgeführt wird, wird eine Ubuntu-Sitzung geöffnet.

So heben Sie die Registrierung und die erneute Installation einer Verteilung auf:

`wslconfig /unregister <DistributionName>`  
Hebt die Registrierung der Distribution bei WSL auf, damit Sie erneut installiert oder bereinigt werden kann.

Beispiel: `wslconfig /unregister Ubuntu` würde Ubuntu aus den in WSL verfügbaren Distributionen entfernen.  Beim Ausführen von `wslconfig /list` würde diese Distribution nicht aufgelistet.

Zum erneuten Installieren suchen Sie die Distribution im Microsoft Store, und wählen Sie dann „Starten“ aus.

## <a name="configure-per-distro-launch-settings-with-wslconf"></a>Konfigurieren von pro-Distribution-Start Einstellungen mit wslconf

> **Verfügbar in Windows Build 17093 und höher**

Konfigurieren Sie automatisch bestimmte Funktionen in WSL, die jedes Mal angewendet werden, wenn Sie das Subsystem mithilfe von `wsl.conf` starten.

Zurzeit umfasst dies Optionen für die automatische Einbindung und Netzwerkkonfiguration.

`wsl.conf` befindet sich in jeder Linux-Distribution in `/etc/wsl.conf`. Wenn die Datei nicht vorhanden ist, können Sie sie selbst erstellen. WSL erkennt das Vorhandensein der Datei und liest ihren Inhalt. Wenn die Datei fehlt oder falsch formatiert ist (d.h. falsche Markupformatierung), wird WSL weiterhin normal gestartet.

Im folgenden finden Sie eine Beispiel `wsl.conf` Datei, die Sie Ihren Verteilungen hinzufügen können:

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>Konfigurationsoptionen

In Übereinstimmung mit INI-Konventionen werden Schlüssel in einem Abschnitt deklariert. 

WSL unterstützt zwei Abschnitte: `automount` und `network`.

#### <a name="automount"></a>automount

Abschnitt: `[automount]`

| key        | value                          | Standard      | notes                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | wahr         | `true` bewirkt, dass lokale Festplattenlaufwerke (d.h. `C:/` oder `D:/`) mit DrvFs automatisch unter `/mnt` eingebunden werden.  `false`bedeutet, dass Laufwerke nicht automatisch bereitgestellt werden, aber Sie können Sie trotzdem manuell oder über bereitstellen `fstab` .                                                                                                             |
| mountFsTab | boolean                        | wahr         | `true` legt fest, dass `/etc/fstab` beim WSL-Start verarbeitet wird. Bei „/etc/fstab“ handelt es sich um eine Datei, in der Sie andere Dateisysteme wie eine SMB-Freigabe deklarieren können. Daher können Sie diese Dateisysteme beim Start automatisch in WSL einbinden.                                                                                                                |
| root       | Zeichenfolge                         | `/mnt/`      | Legt das Verzeichnis fest, in dem lokale Festplattenlaufwerke automatisch eingebunden werden. Wenn Sie z.B. ein Verzeichnis unter `/windir/` in WSL verwenden und Sie dieses als Stammverzeichnis angeben, erwarten Sie, dass die lokalen Festplattenlaufwerke unter `/windir/c` eingebunden werden.                                                                                              |
| Optionen    | Durch Kommas getrennte Liste mit Werten | Leere Zeichenfolge | Dieser Wert wird an die Standardzeichenfolge der DrvFs-Einbindungsoptionen angefügt. **Es können nur DrvFs-spezifische Optionen angegeben werden.** Optionen, die die Einbindungsbinärdatei normalerweise in ein Flag analysieren würde, werden nicht unterstützt. Wenn Sie diese Optionen explizit angeben möchten, müssen Sie jedes Laufwerk, für das dies gelten soll, in „/etc/fstab“ einschließen. |

Standardmäßig legt WSL die UID und die GID auf den Wert des Standardbenutzers fest (in der Ubuntu-Distribution wird der Standardbenutzer mit „uid=1000,gid=1000“ erstellt). Wenn der Benutzer eine GID-oder UID-Option explizit über diesen Schlüssel angibt, wird der zugehörige Wert überschrieben. Andernfalls wird der Standardwert immer angefügt.

**Hinweis:** Diese Optionen werden als Einbindungsoptionen für alle automatisch eingebundenen Laufwerke angewendet. Verwenden Sie stattdessen „/etc/fstab“, um die Optionen nur für ein bestimmtes Laufwerk zu ändern.

#### <a name="mount-options"></a>Einbindungsoptionen

Durch Festlegen verschiedener Einbindungsoptionen für Windows-Laufwerke (DrvFs) kann gesteuert werden, wie Dateiberechtigungen für Windows-Dateien berechnet werden. Die folgenden Optionen sind verfügbar:

| Schlüssel | Beschreibung | Standardwert |
|:----|:----|:----|
|uid| Die Benutzer-ID, die für den Besitzer aller Dateien verwendet wird | Die Standard-Benutzer-ID Ihrer WSL-Distribution (bei der erstmaligen Installation ist der Standardwert 1000)
|gid| Die Gruppen-ID, die für den Besitzer aller Dateien verwendet wird | Die Standard-Gruppen-ID Ihrer WSL-Distribution (bei der erstmaligen Installation ist der Standardwert 1000)
|umask | Eine oktale Maske mit Berechtigungen, die für alle Dateien und Verzeichnisse ausgeschlossen werden sollen | 000
|fmask | Eine oktale Maske mit Berechtigungen, die für alle Dateien ausgeschlossen werden sollen | 000
|dmask | Eine oktale Maske mit Berechtigungen, die für alle Verzeichnisse ausgeschlossen werden sollen | 000

**Hinweis:** Die Berechtigungsmasken werden durch eine logische ODER-Operation festgelegt, bevor sie auf Dateien oder Verzeichnisse angewendet werden. 

#### <a name="network"></a>Netzwerk

Abschnittsbezeichnung: `[network]`

| key | value | Standard | notes|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` legt fest, dass WSL `/etc/hosts` generiert. Die Datei `hosts` enthält eine statische Zuordnung der entsprechenden IP-Adresse von Hostnamen. |
| generateResolvConf | boolean | `true` | `true` legt fest, dass WSL `/etc/resolv.conf` generiert. `resolv.conf` enthält eine DNS-Liste, mit der ein angegebener Hostnamen in seine IP-Adresse aufgelöst werden kann. | 

#### <a name="interop"></a>interop

Abschnittsbezeichnung: `[interop]`

Diese Optionen sind in Insider Build 17713 und höher verfügbar.

| key | value | Standard | notes|
|:----|:----|:----|:----|
| enabled | boolean | `true` | Durch Festlegen dieses Schlüssels wird festgelegt, ob WSL das Starten von Windows-Prozessen unterstützt. |
| appendWindowsPath | boolean | `true` | Durch Festlegen dieses Schlüssels wird festgelegt, ob WSL der $PATH-Umgebungsvariablen Windows-Pfadelemente hinzufügt. |

#### <a name="user"></a>user

Abschnittsbezeichnung: `[user]`

Diese Optionen sind in Build 18980 und höher verfügbar.

| Schlüssel | value | default | notes|
|:----|:----|:----|:----|
| default | Zeichenfolge | Der anfängliche Benutzername, der bei der ersten Ausführen erstellt wurde | Durch Festlegen dieses Schlüssels wird angegeben, welcher Benutzer beim ersten Starten einer WSL-Sitzung ausgeführt werden soll. |

## <a name="configure-global-options-with-wslconfig"></a>Konfigurieren globaler Optionen mit wslconfig

> **Verfügbar in Windows Build 19041 und höher**

Sie können globale WSL-Optionen konfigurieren, indem Sie eine `.wslconfig` Datei in das Stammverzeichnis Ihres Benutzer Ordners einfügen: `C:\Users\<yourUserName>\.wslconfig` . Viele dieser Dateien beziehen sich auf WSL 2. Beachten Sie, dass Sie möglicherweise ausführen müssen `wsl --shutdown` , um die WSL 2-VM herunterzufahren, und dann die WSL-Instanz neu starten, damit diese Änderungen wirksam werden.

Im folgenden finden Sie eine wslconfig-Beispieldatei:

```console
[wsl2]
kernel=C:\\temp\\myCustomKernel
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```

Diese Datei kann die folgenden Optionen enthalten:

### <a name="wsl-2-settings"></a>WSL 2-Einstellungen

Abschnittsbezeichnung: `[wsl2]`

Diese Einstellungen wirken sich auf die VM aus, die jede WSL 2-Distribution unterstützt.

| Schlüssel | value | default | notes|
|:----|:----|:----|:----|
| kernel | Zeichenfolge | Der von Microsoft bereitgestellte Posteingang | Ein absoluter Windows-Pfad zu einem benutzerdefinierten Linux-Kernel. |
| Arbeitsspeicher | size | 80% ihres gesamten Arbeitsspeichers unter Windows * | Wie viel Arbeitsspeicher für die WSL 2-VM zugewiesen werden soll. |
| Prozessoren | number | Die gleiche Anzahl von Prozessoren unter Windows | Gibt an, wie viele Prozessoren der WSL 2-VM zugewiesen werden sollen. |
| localhostforwarding | boolean | `true` | Boolescher Wert, der angibt, ob an den Platzhalter oder localhost in der WSL 2-VM gebundene Ports über localhost: Port vom Host aus verbunden werden sollen. |
| kernelcommandline | Zeichenfolge | Leer | Zusätzliche Kernel-Befehlszeilenargumente. |
| swap | size | 25% der Arbeitsspeicher Größe unter Windows auf das nächste GB aufgerundet | Wie viel Auslagerungs Bereich zum virtuellen WSL 2-Computer hinzugefügt werden soll, 0 für keine Auslagerungs Datei. |
| Auslagerungs Datei | Zeichenfolge | %UserProfile%\appdata\local\temp\tauap.vhdx | Ein absoluter Windows-Pfad zu der virtuellen Auslagerungs-Festplatte. |

* Hinweis: dieser Wert gilt für Windows Build 19041 und unterscheidet sich möglicherweise in Windows-Builds im Insider-Programm.

Einträge mit dem `path` Wert müssen Windows-Pfade mit Escapezeichen mit Escapezeichen sein, z. b.:`C:\\Temp\\myCustomKernel`

Einträge mit dem `size` Wert müssen eine Größe gefolgt von einer Einheit sein, z `8GB` . b `512MB` . oder.
