---
title: Problembehandlung des Windows-Subsystems für Linux
description: Bietet ausführliche Informationen zu häufigen Fehlern und Problemen, die bei der Ausführung von Linux im Windows-Subsystem für Linux auftreten.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: cc8f032a99fb087b7ef614dd3a3574cb8ee3f2da
ms.sourcegitcommit: ba52d673c123fe8ae61e872a33e218cfc30a1f82
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/07/2020
ms.locfileid: "86033066"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>Problembehandlung des Windows-Subsystems für Linux

Unterstützung bei Fragen im Zusammenhang mit WSL finden Sie in unserem GitHub-Repository:

## <a name="search-for-any-existing-issues-related-to-your-problem"></a>Suchen nach vorhandenen Themen zu Ihrem Problem

Verwenden Sie für technische Probleme das Produktrepository: https://github.com/Microsoft/wsl/issues

Verwenden Sie für Probleme im Zusammenhang mit dem Inhalt dieser Dokumentation das Dokumentrepository: https://github.com/MicrosoftDocs/wsl/issues

## <a name="submit-a-bug-report"></a>Senden eines Fehlerberichts

Bei Fehlern im Zusammenhang mit WSL-Funktionen oder -Features melden Sie ein Problem im Produktrepository: https://github.com/Microsoft/wsl/issues

## <a name="submit-a-feature-request"></a>Übermitteln einer Featureanforderung

Um ein neues Feature im Zusammenhang mit der WSL-Funktionalität oder -Kompatibilität anzufordern, melden Sie ein Problem im Produktrepository: https://github.com/Microsoft/wsl/issues

## <a name="contribute-to-the-docs"></a>Beiträge zu den Dokumenten leisten

Um einen Beitrag zur WSL-Dokumentation zu leisten, senden Sie ein Pull Request im Dokumentrepository: https://github.com/MicrosoftDocs/wsl/issues

## <a name="terminal-or-command-line"></a>Terminal oder Befehlszeile

Wenn sich Ihr Problem auf den Windows-Terminal, die Windows-Konsole oder die Befehlszeilenschnittstelle bezieht, verwenden Sie schließlich das Windows-Terminal-Repository: https://github.com/microsoft/terminal

## <a name="common-issues"></a>Allgemeine Probleme

### <a name="cannot-access-wsl-files-from-windows"></a>Kein Zugriff auf WSL-Dateien von Windows aus möglich
Ein 9p-Protokolldateiserver stellt den Dienst auf der Linux-Seite bereit, um Windows den Zugriff auf das Linux-Dateisystem zu ermöglichen. Wenn Sie nicht über `\\wsl$` unter Windows auf WSL zugreifen können, kann dies daran liegen, dass 9P nicht ordnungsgemäß gestartet wurde.

Um dies zu überprüfen, können Sie die Startprotokolle mit `dmesg |grep 9p` überprüfen. Dadurch werden Fehler angezeigt. Eine erfolgreiche Ausgabe sieht wie folgt aus: 

```
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

Weitere Informationen zu diesem Problem finden Sie in [diesem GitHub-Thread](https://github.com/microsoft/wsl/issues/5307).

### <a name="cant-start-wsl-2-distro-and-only-see-wsl-2-in-output"></a>WSL 2-Verteilung kann nicht gestartet werden, und in der Ausgabe wird nur "WSL 2" angezeigt.
Wenn Ihre Anzeigesprache nicht Englisch ist, sehen Sie möglicherweise eine abgeschnittene Version eines Fehlertexts.

```powershell
C:\Users\me>wsl
WSL 2
```

Um dieses Problem zu beheben, navigieren Sie zu `https://aka.ms/wsl2kernel`, und installieren Sie den Kernel manuell, indem Sie die Anweisungen auf der doc-Seite befolgen. 

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a>Aktivieren Sie das Windows-Feature "Virtual Machine Platform", und stellen Sie sicher, dass Virtualisierung im BIOS aktiviert ist.

1. Klicken Sie auf [Systemanforderungen von Hyper-V](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.).
2. Wenn es sich bei dem Computer um einen virtuellen Computer handelt, aktivieren Sie die [geschachtelte Virtualisierung](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manuell. Starten Sie PowerShell als Administrator, und führen Sie folgende Schritte aus: 

```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```

3. Befolgen Sie die Richtlinien des Herstellers Ihres PCs, um zu erfahren, wie Sie die Virtualisierung aktivieren. Dadurch müssen Sie möglicherweise den System-BIOS verwenden, um sicherzustellen, dass diese Features auf Ihrer CPU aktiviert sind. 
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

   und Sie dieses Tutorial befolgt haben: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en

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

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

Um dieses Problem zu beheben, fügen Sie Folgendes an die ```/etc/wsl.conf```-Datei an:

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

Beachten Sie, dass durch Hinzufügen dieses Befehls Metadaten hinzugefügt und die in WSL angezeigten Dateiberechtigungen für die Windows-Dateien geändert werden. Weitere Informationen finden Sie in den [Dateisystemberechtigungen](./file-permissions.md).
