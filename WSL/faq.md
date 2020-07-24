---
title: Häufig gestellte Fragen
description: Häufig gestellte Fragen zum Windows-Subsystem für Linux.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, faq
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 8e3ebb44c139b5e7b8c25e8e813766b0107426dc
ms.sourcegitcommit: 97cc93f8e26391c09a31a4ab42c4b5e9d98d1c32
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/22/2020
ms.locfileid: "86948634"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>Häufig gestellte Fragen zum Windows-Subsystem für Linux

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>Was ist das Windows-Subsystem für Linux (WSL)?

Das Windows-Subsystem für Linux (WSL) ist ein neues Windows 10-Feature, das es ermöglicht, native Befehlszeilentools für Linux direkt unter Windows zusammen mit Ihren traditionellen Desktop- und modernen Store-Apps auszuführen.

Ausführlichere Informationen finden Sie auf der Seite [Informationen](./about.md).

## <a name="who-is-wsl-for"></a>Für wen ist WSL geeignet?

Dies ist in erster Linie ein Tool für Entwickler, insbesondere Webentwickler und Benutzer, die an oder mit Open-Source-Projekten arbeiten. Dies ermöglicht es Benutzern, die Bash, gängige Linux-Tools (`sed`, `awk` usw.) und viele Linux-First-Tools (Ruby, Python usw.) verwenden möchten/müssen, Ihre Toolkette unter Windows zu nutzen.

## <a name="what-can-i-do-with-wsl"></a>Welche Aufgaben kann ich mit WSL erledigen?

WSL bietet eine Anwendung namens „Bash. exe“, die eine Windows-Konsole mit der Bash-Shell öffnet, wenn sie gestartet wird. Mithilfe von Bash können Sie Linux-Befehlszeilentools und -Apps ausführen. Geben Sie z.B. `lsb_release -a` ein, und drücken Sie die EINGABETASTE. Es werden Details zu der derzeit ausgeführten Linux-Distribution angezeigt:

![Screenshot der Details der Distribution](media/distro.png)

Sie können über die Linux Bash-Shell auch auf das Dateisystem des lokalen Computers zugreifen. Ihre lokalen Laufwerke werden unter dem Ordner `/mnt` eingebunden. Das Laufwerk `C:` wird beispielsweise unter `/mnt/c` eingebunden:  

![Screenshot des eingebundenen Laufwerks „C:“](media/ls.png)

## <a name="could-you-describe-a-typical-development-workflow-that-incorporates-wsl"></a>Könnten Sie einen typischen Entwicklungsworkflow beschreiben, der WSL einbezieht?

Die WSL richtet sich an ein Entwicklerpublikum mit der Absicht, als Teil einer inneren Entwicklungsschleife verwendet zu werden. Nehmen wir an, Sam erstellt eine CI/CD-Pipeline (Continuous Integration & Continuous Delivery) und möchte diese zunächst auf einem lokalen Computer (Laptop) testen, bevor er sie in der Cloud bereitstellt. Sam kann WSL (& WSL 2 zur Verbesserung von Geschwindigkeit und Leistung) aktivieren und dann lokal (auf dem Laptop) eine Linux-Ubuntu-Originalinstanz mit den von jeweiligen bevorzugten Bash-Befehlen und Tools verwenden. Sobald die Entwicklungspipeline lokal überprüft wurde, kann Sam diese CI/CD-Pipeline in die Cloud pushen, indem er sie in einen Dockercontainer umwandelt, und den Container in eine Cloudinstanz pushen, wo er auf einer produktionsbereiten Ubuntu-VM ausgeführt wird.

## <a name="what-is-bash"></a>Was ist Bash?

[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) ist eine beliebte, textbasierte Shell und Befehlssprache. Dabei handelt es sich um die Standardshell, die in Ubuntu und anderen Linux-Distributionen sowie in macOS enthalten ist. Benutzer geben Befehle in eine Shell ein, um Skripts und/oder Befehle und Tools auszuführen, um zahlreiche Aufgaben zu erledigen.

## <a name="how-does-this-work"></a>Wie funktioniert das?

Sehen Sie sich unseren [Blog](https://blogs.msdn.microsoft.com/wsl/) an, in dem wir ausführlich über die zugrunde liegende Technologie informieren.

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>Warum sollte ich WSL anstelle von Linux auf einem virtuellen Computer verwenden?

WSL erfordert weniger Ressourcen (CPU, Arbeitsspeicher und Speicher) als ein vollständiger virtueller Computer. WSL ermöglicht es Ihnen auch, Linux-Befehlszeilentools und -Apps neben Ihren Windows Befehlszeilen-, Desktop- und Store-Apps auszuführen und von Linux aus auf Ihre Windows-Dateien zuzugreifen. Auf diese Weise können Sie Windows-Apps und Linux-Befehlszeilentools für denselben Satz von Dateien verwenden, wenn Sie möchten.

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>Warum sollte ich beispielsweise Ruby unter Linux anstatt unter Windows verwenden?

Einige plattformübergreifende Tools wurden unter der Annahme erstellt, dass sich die Umgebung, in der sie ausgeführt werden, wie Linux verhält. Einige Tools gehen beispielsweise davon aus, dass auf sehr lange Dateipfade zugegriffen werden kann oder dass bestimmte Dateien/Ordner vorhanden sind. Dies verursacht unter Windows häufig Probleme, da sich dieses Betriebssystem meistens anders als Linux verhält.

Viele Sprachen wie Ruby und node werden häufig in Windows portiert und lassen sich dort hervorragend ausführen. Allerdings portieren nicht alle Besitzer von Ruby Gem- oder node/NPM-Bibliotheken ihre Bibliotheken, um Windows zu unterstützen, und viele von ihnen verfügen über Linux-spezifische Abhängigkeiten. Dies kann häufig dazu führen, dass Systeme, die mit solchen Tools und Bibliotheken erstellt wurden, unter Windows unter Build- und manchmal unter Laufzeitfehlern leiden oder unerwünschtes Verhalten aufweisen.

Dies sind nur einige der Probleme, die viele Benutzer veranlasst haben, Microsoft zu bitten, die Befehlszeilentools von Windows zu verbessern. Dies hat uns auch dazu veranlasst, eine Partnerschaft mit Canonical einzugehen, damit native Bash- und Linux-Befehlszeilentools unter Windows ausgeführt werden können.

## <a name="what-does-this-mean-for-powershell"></a>Was bedeutet das für PowerShell?

Während der Arbeit mit OSS-Projekten gibt es zahlreiche Szenarien, in denen es äußerst nützlich ist, aus einer PowerShell-Eingabeaufforderung zu Bash zu wechseln. Die Bash-Unterstützung ist ergänzend und stärkt den Wert der Befehlszeile unter Windows, sodass PowerShell und die PowerShell-Community andere gängige Technologien nutzen können.

Weitere Informationen finden Sie im Blog des PowerShell-Teams: [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/).

## <a name="can-i-run-all-linux-apps-in-wsl"></a>Kann ich ALLE Linux-Apps in WSL ausführen?

Nein! WSL ist ein Tool, das es Benutzern, die diese Funktionalität benötigen, ermöglicht, Bash und wichtige Linux-Befehlszeilentools unter Windows auszuführen.

WSL zielt **nicht** darauf ab, GUI-Desktops oder -Anwendungen (z.B. Gnome, KDE usw.) zu unterstützen.  

Auch wenn Sie viele gängige Serveranwendungen (z.B. Redis) ausführen können, empfehlen wir WSL nicht für das Hosting von Produktionsdiensten. Microsoft bietet eine Vielzahl von Lösungen für die Ausführung von Linux-Produktionsworkloads in Azure, Hyper-V und Docker. 

## <a name="what-windows-skus-is-wsl-included-in"></a>In welchen Windows-SKUs ist WSL enthalten?

Das Windows-Subsystem für Linux ist in der Desktopversion von Windows für Windows 10 Anniversary und Creators Update oder höher verfügbar.

Beginnend mit dem Fall Creators Update ist WSL für die Desktop- und Server-SKUs von Windows verfügbar.

## <a name="what-processors-does-wsl-support"></a>Welche Prozessoren werden von WSL unterstützt?

WSL unterstützt x64- und ARM-CPUs.

## <a name="how-do-i-access-my-c-drive"></a>Wie greife ich auf mein Laufwerk „C:“ zu?

Einbindungspunkte für Festplatten auf dem lokalen Computer werden automatisch erstellt und ermöglichen einfachen Zugriff auf das Windows-Dateisystem.

**/mnt/\<drive letter>/**

Beispielsyntax für den Zugriff auf „C:\“: `cd /mnt/c`

## <a name="how-do-i-set-up-git-credential-manager-how-do-i-use-my-windows-git-permissions-in-wsl"></a>Wie richte ich die Git-Anmeldeinformationsverwaltung ein? (Wie verwende ich meine Windows Git-Berechtigungen in WSL?) 

Die Git-Anmeldeinformationsverwaltung ermöglicht Ihnen das Authentifizieren eines Git-Remoteservers, auch wenn Sie über ein komplexes Authentifizierungsmuster wie Azure Active Directory oder eine zweistufige Authentifizierung verfügen. Die Git-Anmeldeinformationsverwaltung kann in den Authentifizierungsablauf für Dienste wie GitHub integriert werden, und sobald Sie bei Ihrem Hostinganbieter authentifiziert sind, fordert sie ein neues Authentifizierungstoken an. Anschließend wird das Token sicher in der Windows-Anmeldeinformationsverwaltung gespeichert. Nach dem ersten Mal können Sie Git verwenden, um mit Ihrem Hostinganbieter zu kommunizieren, ohne sich erneut authentifizieren zu müssen. Er greift einfach auf das Token in Windows-Anmeldeinformationsverwaltung zu.

Zum Einrichten der Git-Anmeldeinformationsverwaltung für die Verwendung mit einer WSL-Distribution öffnen Sie die Distribution, und geben Sie den folgenden Befehl ein:

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

Nun wird für jeden Git-Vorgang, den Sie in der WSL-Distribution ausführen, die Anmeldeinformationsverwaltung verwendet. Wenn Sie bereits Anmeldeinformationen für einen Host zwischengespeichert haben, greifen Sie über die Anmeldeinformationsverwaltung auf diese zu. Andernfalls erhalten Sie eine Dialogfeldantwort, in der Ihre Anmeldeinformationen angefordert werden, auch wenn Sie sich in einer Linux-Konsole befinden.

Diese Unterstützung basiert auf der [Interoperabilität zwischen dem Windows-Subsystem für Linux und Windows selbst](https://docs.microsoft.com/windows/wsl/interop).

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>Wie verwende ich eine Windows-Datei mit einer Linux-App?

Einer der Vorteile von WSL besteht darin, dass Sie über Windows- und Linux-Apps oder -Tools auf Ihre Dateien zugreifen können. 

WSL bindet die Festplattenlaufwerke Ihres Computers unter dem Ordner `/mnt/<drive>` in Ihre Linux-Distributionen ein. Das Laufwerk `C:` wird beispielsweise unter `/mnt/c/` eingebunden.

Mit den eingebundenen Laufwerken können Sie beispielsweise Code in `C:\dev\myproj\` mit [Visual Studio](https://visualstudio.microsoft.com/vs/) oder [VS Code](https://code.visualstudio.com/) bearbeiten und diesen Code in Linux erstellen und testen, indem Sie über `/mnt/c/dev/myproj` auf die gleichen Dateien zugreifen.

> **WICHTIGER HINWEIS**: Eine der wichtigsten Einschränkungen bei der Verwendung von WSL besteht darin, dass der direkte Zugriff auf und die Änderung von Dateien im Dateisystem Ihrer Linux-Distribution mit Windows-Anwendungen oder -Tools nicht unterstützt wird. Weitere Informationen: [Ändern Sie Linux-Dateien nicht mithilfe von Windows-Apps und -Tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Unterscheiden sich die Dateien im Linux-Laufwerk vom eingebundenen Windows-Laufwerk?

1. Dateien unter dem Linuxstamm (d.h. `/`) werden von WSL gesteuert, indem Linux-spezifisches Verhalten imitiert wird, einschließlich, aber nicht beschränkt auf:
   * Dateien, die ungültige Zeichen für Windows-Dateinamen enthalten
   * Für Benutzer ohne Administratorrechte erstellte symbolische Verknüpfungen
   * Ändern von Dateiattributen über chmod und chown
   * Unterscheidung von Groß-/Kleinschreibung für Dateien/Ordner

2. Dateien in eingebundenen Laufwerken werden von Windows gesteuert und weisen das folgende Verhalten auf:
   * Unterstützung von Unterscheidung zwischen Groß-/Kleinschreibung
   * Alle Berechtigungen sind so festgelegt, dass Sie die Windows-Berechtigungen bestmöglich widerspiegeln

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>Warum treten so viele Fehler auf, wenn ich apt-get upgrade ausführe?

In einigen Paketen werden Features verwendet, die noch nicht implementiert wurden. `udev` wird z.B. noch nicht unterstützt und verursacht mehrere `apt-get upgrade`-Fehler.

Führen Sie die folgenden Schritte aus, um Probleme im Zusammenhang mit `udev` zu beheben:

1. Schreiben Sie Folgendes in `/usr/sbin/policy-rc.d`, und speichern Sie die Änderungen.

    ```bash
    #!/bin/sh
    exit 101
    ```

2. Fügen Sie `/usr/sbin/policy-rc.d` Ausführungsberechtigungen hinzu.

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
3. Führen Sie die folgenden Befehle aus.

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>Wie deinstalliere ich eine WSL-Distribution?

Öffnen Sie in Builds vor 1709 (16299) eine Eingabeaufforderung, und führen Sie Folgendes aus:

  ```batchfile
  lxrun /uninstall /full
  ```
  
WSL-Distributionen, die aus dem Store installiert werden, können wie jede andere Windows-App deinstalliert werden, indem Sie mit der rechten Maustaste auf die App-Kachel und dann auf „Deinstallieren“ klicken oder indem Sie PowerShell und das [`Remove-AppxPackage`-Cmdlet](https://technet.microsoft.com/library/hh856038.aspx) verwenden.

## <a name="why-does-ping-generate-permission-denied-errors"></a>Warum werden bei Ping Fehler des Typs „Berechtigung verweigert“ generiert?

In WSL-Builds vor 14926 erforderte Ping, dass WSL über eine Konsole mit erhöhten Rechten ausgeführt wird. Dieses Problem wurde in Build 14926 und höher behoben.

## <a name="how-do-i-run-an-openssh-server"></a>Wie führe ich einen OpenSSH-Server aus?

Zum Ausführen von OpenSSH in WSL sind Administratorberechtigungen in Windows erforderlich. Um einen OpenSSH-Server auszuführen, führen Sie Bash unter Ubuntu unter Windows als Administrator aus, oder starten Sie „bash.exe“ über eine CMD-/PowerShell-Eingabeaufforderung mit Administratorrechten.

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>Warum erhalte ich „Error: 0x80040306“ beim Installationsversuch?

WSL unterstützt die Ausführung in einer Legacykonsole nicht. So deaktivieren Sie die Legacykonsole:

1. Öffnen Sie WSL, PowerShell oder Cmd.
1. Klicken Sie mit der rechten Maustaste auf der Titelleiste auf „Eigenschaften“. Deaktivieren Sie die Option „Legacykonsole verwenden“.
1. Auf "OK" klicken

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>Warum erhalte ich „Error: 0x80040154“ beim Ausführen von „bash.exe“ nach dem Upgrade von Windows?

Das Feature „Windows-Subsystem für Linux“ ist möglicherweise während eines Windows-Updates deaktiviert. Wenn dies der Fall ist, muss das Windows-Feature erneut aktiviert werden. Anweisungen zum Aktivieren des Features „Windows-Subsystem für Linux“ finden Sie im [Installationshandbuch.](https://docs.microsoft.com/windows/wsl/install-win10#install-the-windows-subsystem-for-linux)

## <a name="how-do-i-change-the-display-language-of-wsl"></a>Wie ändere ich die Anzeigesprache von WSL?

Die WSL-Installation versucht, das Ubuntu-Gebietsschema automatisch so zu ändern, dass es dem Gebietsschema Ihrer Windows-Installation entspricht. Wenn Sie dieses Verhalten nicht wünschen, können Sie diesen Befehl ausführen, um das Ubuntu-Gebietsschema zu ändern, nachdem die Installation abgeschlossen wurde. Sie müssen „bash.exe“ neu starten, damit diese Änderung wirksam wird.

Im folgenden Beispiel wird das Gebietsschema in „en-US“ geändert:

```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>Warum habe ich aus WSL keinen Internetzugriff?

Einige Benutzer haben Probleme mit bestimmten Firewallanwendungen gemeldet, die den Internetzugriff in WSL blockieren. Die gemeldeten Firewalls sind:

1. Kaspersky
1. AVG
1. Avast

In einigen Fällen ermöglicht das Deaktivieren der Firewall den Zugriff. In einigen Fällen sieht es so aus, als ob bereits die Installation der Firewall den Zugriff blockiert.

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>Wie greife ich aus WSL unter Windows auf einen Port zu?
WSL nutzt die IP-Adresse von Windows, da es unter Windows ausgeführt wird. Daher können Sie auf alle Ports auf localhost zugreifen. Wenn Sie z.B. Webinhalte an Port 1234 verwenden, können Sie https://localhost:1234 in Ihren Windows-Browser eingeben.

## <a name="how-can-i-back-up-my-wsl-distros-or-move-them-from-one-drive-to-another"></a>Wie kann ich meine WSL-Verteilungen sichern oder von einem Laufwerk auf ein anderes verschieben?

Die beste Möglichkeit zum Sichern oder Verschieben Ihrer Verteilungen sind die in Windows Version 1809 und höher verfügbaren Export/Import-Befehle. Sie können die gesamte Distribution mithilfe des Befehls `wsl --export` in einen Tarball exportieren. Sie können diese Verteilung dann mit dem Befehl `wsl --import`, in dem ein neuer Speicherort für den Import angegeben werden kann, wieder in WSL importieren, wodurch Sie Zustände Ihrer WSL-Verteilungen sichern und speichern (oder verschieben) können. 

Beachten Sie, dass herkömmliche Sicherungsdienste, die Dateien in ihren Appdata-Ordnern sichern (z.B. die Windows-Sicherung), Ihre Linux-Dateien nicht beschädigen.

## <a name="where-can-i-provide-feedback"></a>Wo kann ich Feedback bereitstellen?

Sie können Ihr Feedback über mehrere Kanäle übermitteln und Fragen stellen.

Wenn Sie technische Probleme haben oder neue Features anfordern möchten, besuchen Sie unsere GitHub-Problemverfolgung:

* [GitHub-Problemverfolgung](https://github.com/Microsoft/BashOnWindows/issues)

Wenn Sie mit den neuesten WSL-News auf dem neuesten Stand bleiben möchten, nutzen Sie Folgendes:

* Unseren [Befehlszeilen-Teamblog](https://blogs.msdn.microsoft.com/commandline/)
* Twitter. Folgen Sie [@craigaloewen](https://twitter.com/craigaloewen) auf Twitter, um über Neuigkeiten, Updates usw. informiert zu werden.
