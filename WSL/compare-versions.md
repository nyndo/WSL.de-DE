---
title: Vergleich zwischen WSL 2 und WSL 1
description: Vergleichen Sie Version 1 und Version 2 des Windows-Subsystems für Linux. Erfahren Sie mehr über die Neuerungen in WSL 2 – tatsächlicher Linux-Kernel, höhere Geschwindigkeit, volle Kompatibilität mit Systemaufrufen. WSL 1 funktioniert besser, wenn Sie Dateien über verschiedene Betriebssystem-Dateisysteme hinweg speichern. Sie können die Größe Ihrer virtuellen WSL 2-Festplatte (VHD) erweitern.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem, GNU, Linux, Ubuntu, Debian, Suse, Windows 10, UX-Änderungen, WSL 2, Linux-Kernel, Netzwerkanwendungen, localhost, IPv6, Virtual Hardware Disk, VHD, VHD-Beschränkungen, VHD-Fehler
ms.date: 09/15/2020
ms.topic: conceptual
ms.localizationpriority: high
ms.custom: contperfq1
ms.openlocfilehash: 5aa37c632fe1e02680bdef307a5923d05dfb3f60
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413120"
---
# <a name="comparing-wsl-1-and-wsl-2"></a>Vergleich zwischen WSL 1 und WSL 2

Der Hauptunterschied und die Gründe für die Aktualisierung des Windows-Subsystems für Linux von WSL 1 auf WSL 2 sind:

- **Steigern der Leistung des Dateisystems**,
- **Unterstützen der vollständigen Kompatibilität von Systemaufrufen**.

WSL 2 verwendet das Neueste und Beste an Virtualisierungstechnologie, um einen Linux-Kernel innerhalb einer schlanken Hilfsprogramms-VM auszuführen. WSL 2 ist jedoch keine herkömmliche VM-Benutzererfahrung.

> [!div class="nextstepaction"]
> [Installieren von WSL 1 und Aktualisieren auf WSL 2](install-win10.md)

## <a name="comparing-features"></a>Vergleich der Features

Feature | WSL 1 | WSL 2
--- | --- | ---
 Integration zwischen Windows und Linux| ✅|✅
 Schnelle Startzeiten| ✅ | ✅
 Geringer Ressourcenbedarf| ✅ |✅
 Wird mit aktuellen Versionen von VMware und VirtualBox ausgeführt| ✅ | ✅
 Verwaltete VM| ❌ | ✅
 Vollständiger Linux-Kernel| ❌ |✅
 Vollständige Kompatibilität von Systemaufrufen| ❌ | ✅
 Leistung über Betriebssystem-Dateisysteme hinweg| ✅ | ❌

Wie Sie aus der Vergleichstabelle oben ersehen können, übertrifft die WSL 2-Architektur WSL 1 in mehrfacher Hinsicht, mit Ausnahme der Leistung über Betriebssystem-Dateisysteme hinweg.

## <a name="performance-across-os-file-systems"></a>Leistung über Betriebssystem-Dateisysteme hinweg

Es wird davon abgeraten, mit Ihren Dateien betriebssystemübergreifend zu arbeiten, es sei denn, es liegt ein besonderer Grund dafür vor. Für die schnellste Leistungsgeschwindigkeit speichern Sie Ihre Dateien im WSL-Dateisystem, wenn Sie mit einer Linux-Befehlszeile (Ubuntu, OpenSUSE usw.) arbeiten. Wenn Sie in einer Windows-Befehlszeile (PowerShell, Eingabeaufforderung) arbeiten, speichern Sie Ihre Dateien im Windows-Dateisystem.

Wenn Sie z. B. die WSL-Projektdateien speichern:

- Verwenden Sie das Stammverzeichnis des Linux-Dateisystems: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`
- Verwenden Sie nicht das Stammverzeichnis des Windows-Dateisystems: `C:\Users\<user name>\Project`

Sie können mit Windows-Apps und -Tools wie dem Datei-Explorer auf Ihr Linux-Stammdateisystem zugreifen. Öffnen Sie eine Linux-Verteilung (z. B. Ubuntu), und stellen Sie sicher, dass Sie sich im Basisverzeichnis von Linux befinden, indem Sie den Befehl `cd ~` eingeben. Öffnen Sie dann das Linux-Dateisystem im Datei-Explorer, indem Sie Folgendes eingeben *(den Punkt am Ende nicht vergessen)* : `explorer.exe .`

WSL 2 ist nur in Windows 10, Version 1903, Build 18362 oder höher verfügbar. Überprüfen Sie Ihre Windows-Version, indem Sie die **Windows-Logo-Taste+R** auswählen, **winver** eingeben und **OK** auswählen. (Oder geben Sie den Befehl `ver` an der Windows-Eingabeaufforderung ein.) Möglicherweise müssen Sie [auf die neueste Windows-Version aktualisieren](ms-settings:windowsupdate). Für Builds vor 18362 wird WSL überhaupt nicht unterstützt.

> [!NOTE]
> Die WSL 2 verwendet [VMware 15.5.5+](https://blogs.vmware.com/workstation/2020/05/vmware-workstation-now-supports-hyper-v-mode.html) und [VirtualBox 6+](https://www.virtualbox.org/wiki/Changelog-6.0). Weitere Informationen finden Sie in den [häufig gestellten Fragen zu WSL 2](./wsl2-faq.md#will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox).

## <a name="whats-new-in-wsl-2"></a>Neues in WSL 2

WSL 2 ist eine wichtige Überarbeitung der zugrunde liegenden Architektur und nutzt Virtualisierungstechnologie und einen Linux-Kernel, um neue Features zu ermöglichen. Die Hauptziele für diese Aktualisierung sind eine gesteigerte Leistung des Dateisystems und das Hinzufügen vollständiger Kompatibilität von Systemaufrufen.

- [Systemanforderungen für WSL 2](./install-win10.md#step-2---update-to-wsl-2)
- [Aktualisieren von WSL 1 auf WSL 2](./install-win10.md#step-2---update-to-wsl-2)
- [Häufig gestellte Fragen zu WSL 2](./wsl2-faq.md)

### <a name="wsl-2-architecture"></a>WSL 2-Architektur

Eine herkömmliche VM-Benutzerumgebung lässt sich unter Umständen nur langsam starten, verbraucht viele Ressourcen und nimmt für die Verwaltung Ihre Zeit in Anspruch. WSL 2 weist diese Merkmale nicht auf.

WSL 2 bietet die Vorteile von WSL 1, einschließlich der nahtlosen Integration zwischen Windows und Linux, schnellen Startzeiten, einem geringem Ressourcenbedarf und erfordert keine VM-Konfiguration oder -Verwaltung. Zwar verwendet WSL 2 eine VM, diese wird jedoch hinter den Kulissen verwaltet und ausgeführt, und Ihnen bleibt die Benutzererfahrung von WSL 1 erhalten.

### <a name="full-linux-kernel"></a>Vollständiger Linux-Kernel

Der Linux-Kernel in WSL 2 wird von Microsoft aus dem aktuellsten Stable-Branch auf der Grundlage der auf „kernel.org“ verfügbaren Quelle erstellt. Dieser Kernel wurde speziell für WSL 2 optimiert und zwar hinsichtlich Größe und Leistung, um unter Windows eine beeindruckende Linux-Erfahrung zu bieten. Der Kernel wird mit Windows-Updates gewartet, was bedeutet, dass Sie die neuesten Sicherheitskorrekturen und Kernelverbesserungen erhalten, ohne die Aktualisierungen selbst verwalten zu müssen.

Der [WSL 2 Linux-Kernel ist Open Source-](https://github.com/microsoft/WSL2-Linux-Kernel). Wenn Sie weitere Informationen benötigen, lesen Sie den Blogbeitrag [Shipping a Linux Kernel with Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) (Ausliefern eines Linux-Kernels mit Windows), der von dem Team geschrieben wurde, das ihn erstellt hat.

### <a name="increased-file-io-performance"></a>Verbesserte E/A-Leistung für Dateien

Dateiintensive Vorgänge wie Git-Klon, npm-Installation, apt-Update, apt-Upgrade und mehr sind mit WSL 2 deutlich schneller.

Die tatsächliche Geschwindigkeitssteigerung hängt davon ab, welche App Sie ausführen und wie sie mit dem Dateisystem interagiert. Anfängliche Versionen von WSL 2 werden im Vergleich mit WSL 1 bis zu 20mal schneller ausgeführt (Entpacken eines gezippten Tarballs) und 2–5mal schneller beim Verwenden von Git-Klon, npm-Installation und CMake in verschiedenen Projekten.

### <a name="full-system-call-compatibility"></a>Vollständige Kompatibilität von Systemaufrufen

Linux-Binärdateien verwenden Systemaufrufe für Funktionen, wie den Zugriff auf Dateien, das Anfordern von Arbeitsspeicher, das Erstellen von Prozessen und mehr. Während WSL 1 eine Übersetzungsschicht verwendete, die vom WSL-Team erstellt wurde, enthält WSL 2 seinen eigenen Linux-Kernel mit vollständiger Kompatibilität der Systemaufrufe. Vorteile umfassen:

- Ein ganz neuer Satz von Apps, die Sie in WSL ausführen können, wie etwa **[Docker](tutorials/wsl-containers.md)** und mehr.

- Alle Updates des Linux-Kernels sind sofort einsatzbereit. (Sie müssen nicht warten, bis das WSL-Team Updates implementiert und die Änderungen hinzufügt).

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a>WSL 2 benötigt beim Start weniger Arbeitsspeicher.

WSL 2 verwendet eine schlanke Hilfsprogramm-VM auf einem echten Linux-Kernel mit geringem Arbeitsspeicherbedarf. Das Hilfsprogramm weist beim Start den durch virtuelle Adressen gestützten Arbeitsspeicher zu. Es ist so konfiguriert, dass es mit einem kleinen Anteil des gesamten Arbeitsspeichers startet, der für WSL 1 benötigt wurde.

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a>Ausnahmen zur Verwendung von WSL 1 anstelle von WSL 2

Es wird empfohlen, WSL 2 zu verwenden, da es eine schnellere Leistung und 100%ige Kompatibilität von Systemaufrufen bietet. Es gibt jedoch einige spezielle Szenarien, in denen Sie möglicherweise WSL 1 verwenden möchten. Erwägen Sie in folgenden Fällen die Verwendung von WSL 1:

- Ihre Projektdateien müssen im Windows-Dateisystem gespeichert werden. WSL 1 bietet schnelleren Zugriff auf Dateien, die von Windows aus bereitgestellt werden.
  - Wenn Sie Ihre WSL Linux-Verteilung verwenden, um auf Projektdateien im Windows-Dateisystem zuzugreifen, und diese Dateien nicht im Linux-Dateisystem gespeichert werden können, erzielen Sie mithilfe von WSL 1 eine schnellere Leistung über die Betriebssystemdateien.
- Ein Projekt, das die Kreuzkompilierung mithilfe von Windows- und Linux-Tools für dieselben Dateien erfordert.
  - Die Dateileistung über Windows- und Linux-Betriebssysteme hinweg ist in WSL 1 schneller als in WSL 2. Wenn Sie also Windows-Anwendungen für den Zugriff auf Linux-Dateien verwenden, erzielen Sie derzeit eine schnellere Leistung mit WSL 1.

> [!NOTE]
> Probieren Sie den VS-Code [Remote WSL-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) aus, mit dem Sie Ihre Projektdateien im Linux-Dateisystem speichern können, indem Sie Linux-Befehlszeilentools verwenden, aber auch VS-Code unter Windows zum Verfassen, Bearbeiten, Debuggen oder Ausführen Ihres Projekts in einem Internetbrowser ohne die mit den Linux- und Windows-Dateisystemen verbundenen Leistungseinbußen. [Weitere Informationen](tutorials/wsl-vscode.md)

## <a name="accessing-network-applications"></a>Zugriff auf Netzwerkanwendungen

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a>Zugreifen auf Linux-Netzwerk-Apps aus Windows (localhost)

Wenn Sie in Ihrer Linux-Verteilung eine Netzwerk-App (z. B. eine App, die auf einer NodeJS- oder SQL Server-Instanz ausgeführt wird) entwickeln, können Sie auf diese über eine Windows-App (z. B. Ihren Microsoft Edge- oder Chrome-Internetbrowser) unter Verwendung von `localhost` zugreifen (genau wie Sie dies normalerweise tun würden).

Wenn Sie jedoch eine ältere Version von Windows ausführen (Build 18945 oder älter), müssen Sie die IP-Adresse der Linux-Host-VM abrufen (oder [auf die neueste Windows-Version aktualisieren](ms-settings:windowsupdate)).

So ermitteln Sie die IP-Adresse des virtuellen Computers, der Ihre Linux-Verteilung unterstützt:

- Führen Sie in ihrer WSL-Verteilung (z. B. Ubuntu) den folgenden Befehl aus: `ip addr`
- Suchen und kopieren Sie die Adresse unter dem `inet`-Wert der `eth0`-Schnittstelle.
- Wenn Sie das grep-Tool installiert haben, finden Sie es leichter, indem Sie die Ausgabe mit dem Befehl `ip addr | grep eth0` filtern.
- Stellen Sie mithilfe dieser IP-Adresse eine Verbindung mit Ihrem Linux-Server her.

Die Abbildung zeigt ein Beispiel dafür – hier wird mithilfe des Microsoft Edge-Browsers eine Verbindung mit einem Node.js-Server hergestellt.

![Herstellen einer Verbindung mit dem NodeJS-Server über Microsoft Edge](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a>Zugreifen auf Windows-Netzwerk-Apps aus Linux (Host-IP)

Wenn Sie von Ihrer Linux-Verteilung (d. h. Ubuntu) aus, auf eine Netzwerk-App zugreifen möchten, die unter Windows ausgeführt wird (z. B. eine App, die auf einer NodeJS- oder SQL Server-Instanz ausgeführt wird), müssen Sie die IP-Adresse des Hostcomputers verwenden. Obwohl dies kein gängiges Szenario ist, können Sie die folgenden Schritte ausführen, damit es funktioniert.
    - Rufen Sie die IP-Adresse Ihres Hostcomputers ab, indem Sie den folgenden Befehl aus Ihrer Linux-Verteilung heraus ausführen: `cat /etc/resolv.conf`
    - Kopieren Sie die IP-Adresse nach dem Begriff: `nameserver`.
    - Stellen Sie mithilfe der kopierten IP-Adresse eine Verbindung zu jedem beliebigen Windows-Server her.

Die Abbildung zeigt ein Beispiel dafür – hier wird über curl eine Verbindung mit einem Node.js-Server hergestellt, der unter Windows ausgeführt wird.

![Herstellen einer Verbindung mit dem NodeJS-Server in Windows über Curl](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a>Weitere Netzwerküberlegungen

#### <a name="connecting-via-remote-ip-addresses"></a>Verbinden über Remote-IP-Adressen

Wenn Sie Remote-IP-Adressen verwenden, um Verbindungen mit Ihren Anwendungen herzustellen, werden diese als Verbindungen aus dem LAN (Local Area Network) behandelt. Dies bedeutet, Sie müssen sicherstellen, dass Ihre Anwendung LAN-Verbindungen akzeptieren kann.

Sie müssen z. B. möglicherweise Ihre Anwendung an `0.0.0.0` statt an `127.0.0.1` binden. In dem Beispiel einer Python-App, die Flask verwendet, kann das mithilfe dieses Befehls erfolgen: `app.run(host='0.0.0.0')`. Beachten Sie bei diesen Änderungen die Sicherheit, da Verbindungen aus Ihrem LAN zugelassen werden.

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a>Zugreifen auf eine WSL 2-Verteilung aus Ihrem LAN (Local Area Network)

Wenn Sie eine WSL 1-Verteilung verwenden und Ihr Computer so eingerichtet wurde, dass auf ihn über Ihr LAN zugegriffen wird, kann auf Anwendungen, die in WSL ausgeführt werden, in Ihrem LAN ebenfalls zugegriffen werden.

Dies ist nicht der Standardfall in WSL 2. WSL 2 verfügt über einen virtualisierten Ethernet-Adapter mit einer eigenen eindeutigen IP-Adresse. Um diesen Workflow zu aktivieren, müssen Sie aktuell die gleichen Schritte wie bei einem gewöhnlichen virtuellen Computer durchlaufen. (Wir untersuchen Möglichkeiten, dieses Verhalten zu verbessern.)

Hier ist ein PowerShell-Beispielbefehl zum Hinzufügen eines Portproxys, der Port 4000 auf dem Host überwacht und ihn mit Port 4000 mit der IP-Adresse 192.168.101.100 zum WSL 2-Computer verbindet.

```powershell
netsh interface portproxy add v4tov4 listenport=4000 listenaddress=0.0.0.0 connectport=4000 connectaddress=192.168.101.100
```

#### <a name="ipv6-access"></a>IPv6-Zugriff

WSL 2-Verteilungen können aktuell keine reinen IPv6-Adressen erreichen. Wir arbeiten daran, diese Funktion hinzuzufügen.

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a>Erweitern der Größe Ihrer virtuellen WSL 2-Festplatte (VHD)

WSL 2 verwendet eine virtuelle Festplatte (VHD) zum Speichern Ihrer Linux-Dateien. Wenn die maximale Größe erreicht ist, müssen Sie sie möglicherweise erweitern.

Die WSL 2-VHD verwendet das Ext4-Dateisystem. Diese VHD wird automatisch an Ihre Speicheranforderungen angepasst, und verfügt über eine anfängliche maximale Größe von 256 GB. Wenn Ihre Verteilung über die Größe von 256 GB anwächst, werden Ihnen Fehler angezeigt, die besagen, dass kein Speicherplatz mehr zur Verfügung steht. Sie können diesen Fehler beheben, indem Sie die Größe der VHD heraufsetzen.

So erweitern Sie die maximale VHD-Größe auf über 256 GB:

1. Beenden Sie alle WSL-Instanzen mit dem Befehl `wsl --shutdown`.

2. Suchen Sie das Installationspaket Ihrer Verteilung mit dem Namen „PackageFamilyName“.
    - Geben Sie in PowerShell Folgendes ein (wobei „distro“ für den Namen Ihrer Verteilung steht):
    - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. Suchen Sie den `fullpath` der VHD-Datei, die von Ihrer WSL 2-Installation verwendet wird, dies ist Ihr `pathToVHD`:
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. Ändern Sie die Größe Ihrer WSL 2-VHD, indem Sie die folgenden Befehle ausführen:
   - Öffnen Sie die Windows-Eingabeaufforderung mit Administratorrechten, und geben Sie Folgendes ein:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`

5. Starten Sie Ihre WSL-Verteilung (z. B. Ubuntu).

6. Machen Sie WSL darauf aufmerksam, dass die Größe des Dateisystems durch Ausführen dieser Befehle über die Befehlszeile der Linux-Verteilung erweitert werden kann:
    - `sudo mount -t devtmpfs none /dev`
    - `mount | grep ext4`
    - Kopieren Sie den Namen dieses Eintrags, der diese Form hat: `/dev/sdXX` (wobei X für ein beliebiges anderes Zeichen steht).
    - `sudo resize2fs /dev/sdXX`
    - Verwenden Sie den Wert, den Sie zuvor kopiert haben. Möglicherweise müssen Sie auch „resize2fs“ installieren: `apt install resize2fs`

> [!NOTE]
> Im Allgemeinen sollten Sie die WSL-bezogenen Dateien, die sich in Ihrem AppData-Ordner befinden, nicht mithilfe von Windows-Tools oder-Editoren ändern, verschieben oder darauf zugreifen. Dies könnte zu einer Beschädigung Ihrer Linux-Verteilung führen.
