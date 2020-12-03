---
title: Problembehandlung des Windows-Subsystems für Linux
description: Bietet ausführliche Informationen zu häufigen Fehlern und Problemen, die bei der Ausführung von Linux im Windows-Subsystem für Linux auftreten.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 09/28/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f4040cbe9faf5d55324b56974dd5677052224dd1
ms.sourcegitcommit: d5d3dd8b91e93d46653f9512bceafd8b5340255f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96443745"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Problembehandlung des Windows-Subsystems für Linux

Unterstützung bei Fragen im Zusammenhang mit WSL finden Sie in unserem [WSL-Produkt-Repository in GitHub](https://github.com/Microsoft/wsl/issues).

## <a name="search-for-any-existing-issues-related-to-your-problem"></a>Suchen nach vorhandenen Themen zu Ihrem Problem

Verwenden Sie für technische Probleme das [Produktrepository](https://github.com/Microsoft/wsl/issues).

Verwenden Sie für Probleme im Zusammenhang mit dem Inhalt dieser Dokumentation das [Dokumentrepository](https://github.com/MicrosoftDocs/wsl/issues).

## <a name="submit-a-bug-report"></a>Senden eines Fehlerberichts

Bei Fehlern im Zusammenhang mit WSL-Funktionen oder -Features melden Sie ein Problem im Produktrepository: https://github.com/Microsoft/wsl/issues

## <a name="submit-a-feature-request"></a>Übermitteln einer Featureanforderung

Um ein neues Feature im Zusammenhang mit der WSL-Funktionalität oder -Kompatibilität anzufordern, [melden Sie ein Problem im Produktrepository](https://github.com/Microsoft/wsl/issues).

## <a name="contribute-to-the-docs"></a>Beiträge zu den Dokumenten leisten

Um einen Beitrag zur WSL-Dokumentation zu leisten, senden Sie ein Pull Request im Dokumentrepository: https://github.com/MicrosoftDocs/wsl/issues

## <a name="terminal-or-command-line"></a>Terminal oder Befehlszeile

Wenn sich Ihr Problem auf den Windows-Terminal, die Windows-Konsole oder die Befehlszeilenschnittstelle bezieht, verwenden Sie schließlich das Windows-Terminal-Repository: https://github.com/microsoft/terminal

## <a name="common-issues"></a>Allgemeine Probleme

### <a name="im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2"></a>Ich verwende Windows 10, Version 1903, und es werden trotzdem keine Optionen für WSL 2 angezeigt

Dies liegt wahrscheinlich daran, dass auf Ihrem Computer der Backport für WSL 2 noch nicht eingerichtet ist. Die einfachste Möglichkeit zur Lösung des Problems besteht darin, zu den Windows-Einstellungen zu wechseln und auf „Nach Updates suchen“ zu klicken, um die neuesten Updates auf Ihrem System zu installieren. Schauen Sie sich [die vollständigen Anweisungen zur Einrichtung des Backports finden](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it) an.

Wenn Sie auf „Nach Updates suchen“ klicken und das Update immer noch nicht erhalten, können Sie [KB4566116 manuell installieren](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).  

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a>„Fehler: 0x1bc wenn `wsl --set-default-version 2`

Dies kann vorkommen, wenn die Einstellung „Anzeigesprache“ oder „Systemgebietsschema“ nicht auf Englisch festgelegt ist.

```powershell
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

Der tatsächliche Fehler für `0x1bc` lautet:

```powershell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

Weitere Informationen finden Sie im Problem [5749](https://github.com/microsoft/WSL/issues/5749).

### <a name="cannot-access-wsl-files-from-windows"></a>Kein Zugriff auf WSL-Dateien von Windows aus möglich

Ein 9p-Protokolldateiserver stellt den Dienst auf der Linux-Seite bereit, um Windows den Zugriff auf das Linux-Dateisystem zu ermöglichen. Wenn Sie nicht über `\\wsl$` unter Windows auf WSL zugreifen können, kann dies daran liegen, dass 9P nicht ordnungsgemäß gestartet wurde.

Um dies zu überprüfen, können Sie die Startprotokolle mit `dmesg |grep 9p` überprüfen. Dadurch werden Fehler angezeigt. Eine erfolgreiche Ausgabe sieht wie folgt aus:

```bash
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

Weitere Informationen zu diesem Problem finden Sie in [diesem GitHub-Thread](https://github.com/microsoft/wsl/issues/5307).

### <a name="cant-start-wsl-2-distribution-and-only-see-wsl-2-in-output"></a>WSL 2-Verteilung kann nicht gestartet werden, und in der Ausgabe wird nur "WSL 2" angezeigt

Wenn Ihre Anzeigesprache nicht Englisch ist, sehen Sie möglicherweise eine abgeschnittene Version eines Fehlertexts.

```powershell
C:\Users\me>wsl
WSL 2
```

Um dieses Problem zu beheben, navigieren Sie zu `https://aka.ms/wsl2kernel`, und installieren Sie den Kernel manuell, indem Sie die Anweisungen auf der doc-Seite befolgen. 

### <a name="command-not-found-when-executing-windows-exe-in-linux"></a>`command not found` beim Ausführen von „windows.exe“ unter Linux

Benutzer können ausführbare Windows-Programmdateien wie „notepad.exe“ direkt aus Linux ausführen. Manchmal kann es vorkommen, dass "Befehl nicht gefunden" angezeigt wird, wie unten dargestellt: 

```Bash
$ notepad.exe
-bash: notepad.exe: command not found
```

Wenn es keine win32-Pfade in Ihrem $PATH gibt, findet interop die EXE-Datei nicht.
Sie können dies überprüfen, indem Sie `echo $PATH` in Linux ausführen. In der Ausgabe sollte ein win32-Pfad (z. B. „/mnt/c/Windows“) angezeigt werden.
Werden keine Windows-Pfade angezeigt, wird Ihr PATH höchstwahrscheinlich von Ihrer Linux-Shell außer Kraft gesetzt. 

Im folgenden Beispiel hat „/etc/profile“ auf Debian zu diesem Problem beigetragen:

```Bash
if [ "`id -u`" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

Die richtige Vorgehensweise unter Debian besteht darin, die obigen Zeilen zu entfernen.
Sie können auch $PATH während der Zuweisung anhängen, wie unten beschrieben, aber das führt zu einigen [anderen Problemen](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) mit WSL und VSCode.

Weitere Informationen finden Sie unter den Problemen [5296](https://github.com/microsoft/WSL/issues/5296) und [5779](https://github.com/microsoft/WSL/issues/5779).

### <a name="error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed"></a>„Error: 0x80370102 Der virtuelle Computer konnte nicht gestartet werden, weil ein erforderliches Feature nicht installiert ist.“

Aktivieren Sie das Windows-Feature "Virtual Machine Platform", und stellen Sie sicher, dass Virtualisierung im BIOS aktiviert ist.

1. Klicken Sie auf [Systemanforderungen von Hyper-V](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.).

2. Wenn es sich bei dem Computer um einen virtuellen Computer handelt, aktivieren Sie die [geschachtelte Virtualisierung](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) manuell. Starten Sie PowerShell als Administrator, und führen Sie folgende Schritte aus:

    ```powershell
    Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
    ```

3. Befolgen Sie die Richtlinien des Herstellers Ihres PCs, um zu erfahren, wie Sie die Virtualisierung aktivieren. Dadurch müssen Sie möglicherweise den System-BIOS verwenden, um sicherzustellen, dass diese Features auf Ihrer CPU aktiviert sind. Die Anweisungen für diesen Prozess können von Computer zu Computer variieren. In [diesem Artikel](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) von Bleeping Computer finden Sie ein Beispiel.

4. Starten Sie den Computer neu, nachdem Sie die optionale `Virtual Machine Platform`-Komponente aktiviert haben.

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash verliert nach dem Herstellen einer Verbindung mit einem VPN die Netzwerkkonnektivität

Wenn Bash nach dem Herstellen einer Verbindung mit einem VPN unter Windows die Netzwerkkonnektivität verliert, können Sie diese Problemumgehung innerhalb von Bash versuchen. Mit dieser Problemumgehung können Sie die DNS-Auflösung manuell durch `/etc/resolv.conf` außer Kraft setzen.

1. Notieren Sie sich den DNS-Server des VPN (`ipconfig.exe /all`).
2. Erstellen Sie eine Kopie der vorhandenen Datei „resolv.conf“ (`sudo cp /etc/resolv.conf /etc/resolv.conf.new`).
3. Heben Sie die Verknüpfung der aktuellen Datei „resolv.conf“ auf (`sudo unlink /etc/resolv.conf`).
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. Öffnen Sie `/etc/resolv.conf` und <br/>
   ein. Löschen Sie die erste Zeile aus der Datei, die Folgendes besagt: „\#This file was automatically generated by WSL. To stop automatic generation of this file, remove this line.“ (Diese Datei wurde automatisch von WSL generiert. Um die automatische Generierung dieser Datei zu beenden, entfernen Sie diese Zeile.) <br/>
   b. Fügen Sie den DNS-Eintrag aus (1) oben als ersten Eintrag in der Liste der DNS-Server hinzu. <br/>
   c. Schließen Sie die Datei. <br/>

Nachdem Sie die Verbindung mit dem VPN getrennt haben, müssen Sie die Änderungen auf `/etc/resolv.conf` zurücksetzen. Gehen Sie dazu folgendermaßen vor:

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>Beim Starten von WSL oder beim Installieren einer Distribution wird ein Fehlercode zurückgegeben

Befolgen Sie [diese Anweisungen](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs), um detaillierte Protokolle zu erfassen und ein Issue auf GitHub zu melden.

### <a name="updating-bash-on-ubuntu-on-windows"></a>Aktualisieren von Bash unter Ubuntu unter Windows

Es gibt zwei Komponenten von Bash unter Ubuntu unter Windows, die eine Aktualisierung erfordern.

1. Das Windows-Subsystem für Linux
  
   Durch das Upgrade dieses Teils von Bash unter Ubuntu unter Windows werden alle neuen Problembehandlungen aktiviert, die in den [Anmerkungen zu dieser Version](./release-notes.md) beschrieben werden. Stellen Sie sicher, dass Sie das Windows-Insider-Programm abonniert haben und dass Ihr Build auf dem neuesten Stand ist. Informationen zu einer genaueren Steuerung (einschließlich des Zurücksetzens der Ubuntu-Instanz) finden Sie auf der [Befehlsreferenzseite](./reference.md).

2. Die Ubuntu-Benutzerbinärdateien

   Durch das Upgrade dieses Teils von Bash unter Ubuntu unter Windows werden alle Updates der Ubuntu-Benutzerbinärdateien einschließlich der Anwendungen installiert, die Sie über apt-get installiert haben. Führen Sie die folgenden Befehle in Bash aus, um das Update auszuführen:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt-get-Upgradefehler

In einigen Paketen werden Features verwendet, die noch nicht implementiert wurden. `udev` wird z.B. noch nicht unterstützt und verursacht mehrere `apt-get upgrade`-Fehler.

Führen Sie die folgenden Schritte aus, um Probleme im Zusammenhang mit `udev` zu beheben:

1. Schreiben Sie Folgendes in `/usr/sbin/policy-rc.d`, und speichern Sie die Änderungen.
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. Fügen Sie `/usr/sbin/policy-rc.d` Ausführungsberechtigungen hinzu:

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. Führen Sie die folgenden Befehle aus:

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>„Error: 0x80040306“ bei der Installation

Dies hat mit der Tatsache zu tun, dass die Legacykonsole nicht unterstützt wird.
So deaktivieren Sie die Legacykonsole:

1. Öffnen Sie „cmd. exe“.
1. Klicken Sie mit der rechten Maustaste auf der Titelleiste auf „Eigenschaften“. Deaktivieren Sie die Option „Legacykonsole verwenden“.
1. Auf "OK" klicken

### <a name="error-0x80040154-after-windows-update"></a>„Error: 0x80040154“ nach Windows-Update

Das Feature „Windows-Subsystem für Linux“ ist möglicherweise während eines Windows-Updates deaktiviert. Wenn dies der Fall ist, muss das Windows-Feature erneut aktiviert werden. Anweisungen zum Aktivieren des Windows-Subsystems für Linux finden Sie im [Installationsleitfaden](./install-win10.md).

### <a name="changing-the-display-language"></a>Ändern der Anzeigesprache

Die WSL-Installation versucht, das Ubuntu-Gebietsschema automatisch so zu ändern, dass es dem Gebietsschema Ihrer Windows-Installation entspricht.  Wenn Sie dieses Verhalten nicht wünschen, können Sie diesen Befehl ausführen, um das Ubuntu-Gebietsschema zu ändern, nachdem die Installation abgeschlossen wurde.  Sie müssen „bash.exe“ neu starten, damit diese Änderung wirksam wird.

Im folgenden Beispiel wird das Gebietsschema in „en-US“ geändert:

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Installationsprobleme nach der Windows-Systemwiederherstellung

1. Löschen Sie den Ordner `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`. <br/>
  **Hinweis: Unterlassen Sie dies, wenn Ihre optionale Funktion vollständig installiert und funktionsfähig ist.**
2. Aktivieren Sie das optionale WSL-Feature (falls noch nicht geschehen).
3. Neustart
4. lxrun/uninstall/full
5. Installieren von Bash

### <a name="no-internet-access-in-wsl"></a>Kein Internetzugriff in WSL

Einige Benutzer haben Probleme mit bestimmten Firewallanwendungen gemeldet, die den Internetzugriff in WSL blockieren.  Die gemeldeten Firewalls sind:

1. Kaspersky
2. AVG
3. Avast

In einigen Fällen ermöglicht das Deaktivieren der Firewall den Zugriff.  In einigen Fällen sieht es so aus, als ob bereits die Installation der Firewall den Zugriff blockiert.

### <a name="permission-denied-error-when-using-ping"></a>Fehler des Typs „Berechtigung verweigert“ bei Verwendung von Ping

Für [Windows Anniversary Update, Version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), sind **Administratorberechtigungen** in Windows erforderlich, um Ping in WSL auszuführen.  Um Ping auszuführen, führen Sie Bash unter Ubuntu unter Windows als Administrator aus, oder starten Sie „bash.exe“ über eine CMD-/PowerShell-Eingabeaufforderung mit Administratorrechten.

Für spätere Versionen von Windows, [ab Build 14926](./release-notes.md#build-14926), sind Administratorberechtigungen nicht mehr erforderlich.

### <a name="bash-is-hung"></a>Bash reagiert nicht

Wenn Sie beim Arbeiten mit Bash feststellen, dass Bash hängt (oder blockiert ist) und nicht mehr auf Eingaben reagiert, helfen Sie uns, das Problem zu diagnostizieren, indem Sie ein Speicherabbild erfassen und melden. Beachten Sie, dass diese Schritte zu einem Absturz Ihres Systems führen. Unterlassen Sie dies, wenn Sie damit nicht einverstanden sind, oder speichern Sie Ihre Arbeit zuvor.

So erfassen Sie ein Speicherabbild

1. Ändern Sie den Typ des Speicherabbilds in „Vollständiges Speicherabbild“. Notieren Sie sich den aktuellen Typ, bevor Sie den Speicherabbildtyp ändern.

2. Verwenden Sie diese [Schritte](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) zum Konfigurieren von Abstürzen mithilfe der Tastatursteuerung.

3. Reproduzieren Sie das Hängen oder die Blockade.

4. Lassen Sie das System mithilfe der Tastensequenz aus (2) abstürzen.

5. Das System stürzt ab und erfasst das Speicherabbild.

6. Nachdem das System neu gestartet wurde, übermitteln Sie die Datei „memory.dmp“ an secure@microsoft.com. Der Standardspeicherort der Speicherabbilddatei ist „%SystemRoot%\memory.dmp“ oder „C:\Windows\memory.dmp“, wenn „C:“ das Systemlaufwerk ist. Geben Sie in der E-Mail an, dass das Speicherabbild für das WSL- oder Bash unter Windows-Team vorgesehen ist.

7. Stellen Sie die ursprünglichen Einstellung für den Speicherabbildtyp wieder her.

### <a name="check-your-build-number"></a>Überprüfen der Buildnummer

Um die Architektur des PCs und die Windows-Buildnummer zu ermitteln, öffnen Sie  
**Einstellungen** > **System** > **Info**

Suchen Sie nach den Feldern **Betriebssystembuild** und **Systemtyp**.  
    ![Screenshot der Felder „Betriebssystembuild“ und „Systemtyp“](media/system.png)

Führen Sie Folgendes in PowerShell aus, um die Windows Server-Buildnummer zu ermitteln:  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>Bestätigen, dass WSL aktiviert ist

Sie können bestätigen, dass das Windows-Subsystem für Linux aktiviert ist, indem Sie Folgendes in PowerShell ausführen:  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>Verbindungsprobleme des OpenSSH-Servers

Beim Versuch, den SSH-Server zu verbinden, tritt ein Fehler auf: „Connection closed by 127.0.0.1 port 22“ (Verbindung wurde durch 127.0.0.1 Port 22 geschlossen).

1. Stellen Sie sicher, dass der OpenSSH-Server ausgeführt wird:

   ```bash
   sudo service ssh status
   ```

   und Sie dieses Tutorial befolgt haben: https://ubuntu.com/server/docs/service-openssh

2. Beenden Sie den sshd-Dienst, und starten Sie sshd im Debugmodus:

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. Überprüfen Sie die Startprotokolle, und stellen Sie sicher, dass HostKeys verfügbar sind und keine Protokollmeldungen wie die folgenden angezeigt werden:

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

Wenn solche Meldungen angezeigt werden und die Schlüssel unter `/etc/ssh/` fehlen, müssen Sie die Schlüssel neu generieren oder openssh-server einfach bereinigen und installieren:

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a>"Die referenzierte Assembly konnte nicht gefunden werden." beim Aktivieren des optionalen WSL-Features

Dieser Fehler bezieht sich auf einen fehlerhaften Installationsstatus. Führen Sie die folgenden Schritte aus, um eine Behebung dieses Problems zu versuchen:

- Wenn Sie den Befehl zum Aktivieren des WSL-Features aus PowerShell ausführen, versuchen Sie stattdessen, die grafische Benutzeroberfläche zu verwenden, indem Sie das Startmenü öffnen, nach „Windows-Features aktivieren oder deaktivieren“ suchen und dann in der Liste „Windows Subsystem für Linux“ auswählen, wodurch die optionale Komponente installiert wird.

- Aktualisieren Sie Ihre Windows-Version, indem Sie zu „Einstellungen“, „Updates“ wechseln und dann auf „Nach Updates suchen“ klicken

- Wenn beide Versuche erfolglos bleiben und Sie auf WSL zugreifen müssen, erwägen Sie, ein lokales Upgrade auszuführen, indem Sie Windows 10 mithilfe der Installationsmedien erneut installieren und „Alles beibehalten“ auswählen, um sicherzustellen, dass Ihre Apps und Dateien erhalten bleiben. Anweisungen dazu finden Sie auf der Seite [Erneutes Installieren von Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).

### <a name="correct-ssh-related-permission-errors"></a>Beheben von (SSH-bezogenen) Berechtigungsfehlern

Wenn dieser Fehler angezeigt wird:

```bash
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

Um dieses Problem zu beheben, fügen Sie Folgendes an die ```/etc/wsl.conf```-Datei an:

```bash
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

Beachten Sie, dass durch Hinzufügen dieses Befehls Metadaten hinzugefügt und die in WSL angezeigten Dateiberechtigungen für die Windows-Dateien geändert werden. Weitere Informationen finden Sie in den [Dateisystemberechtigungen](./file-permissions.md).

### <a name="running-windows-commands-fails-inside-a-distribution"></a>Fehler beim Ausführen von Windows-Befehlen innerhalb einer Verteilung

Einige [im Microsoft Store verfügbare](install-win10.md#step-6---install-your-linux-distribution-of-choice) Verteilungen sind noch nicht vollständig kompatibel, um Windows-Befehle sofort in [Terminal](https://en.wikipedia.org/wiki/Linux_console) auszuführen. Wenn Sie beim Ausführen von `powershell.exe /c start .` oder eines anderen Windows-Befehls der Fehler `-bash: powershell.exe: command not found` angezeigt wird, können Sie ihn mit den folgenden Schritten beheben:

1. Führen Sie `echo $PATH` in Ihrer WSL-Verteilung aus.  
   Wenn `/mnt/c/Windows/system32` nicht enthalten ist, wird die PATH-Standardvariable von irgendeiner Komponente neu definiert.
2. Prüfen Sie die Profileinstellungen mit `cat /etc/profile`.  
   Ist die Zuweisung der PATH-Variablen enthalten, bearbeiten Sie die Datei, um den PATH-Zuweisungsblock mit einem **#** -Zeichen auszukommentieren.
3. Prüfen Sie, ob „wsl.conf“ vorhanden ist (`cat /etc/wsl.conf`), und stellen Sie sicher, dass `appendWindowsPath=false` nicht enthalten ist. Andernfalls kommentieren Sie es aus.
4. Starten Sie die Verteilung neu, indem Sie `wsl -t ` eingeben, gefolgt vom Namen der Verteilung, oder indem Sie `wsl --shutdown` entweder in cmd oder PowerShell ausführen.

### <a name="unable-to-boot-after-installing-wsl-2"></a>Starten nach der Installation von WSL 2 nicht möglich

Es ist ein Problem bekannt, das Benutzer betrifft, wenn Sie nach der Installation von WSL 2 nicht starten können. Während unserer umfassenden Diagnose dieser Probleme haben Benutzer berichtet, dass [das Ändern der Puffergröße](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363) oder [das Installieren der richtigen Treiber](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244) helfen kann, dieses Problem zu beheben. Im folgenden [GitHub-Artikel](https://github.com/microsoft/WSL/issues/4784) finden Sie die neuesten Updates zu diesem Problem. 
