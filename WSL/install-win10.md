---
title: Installieren des Windows-Subsystems für Linux (WSL) unter Windows 10
description: Erfahren Sie, wie Sie Linux-Verteilungen auf Ihrem Windows 10-Computer mit einem Bash-Terminal installieren, einschließlich Ubuntu, Debian, SUSE, Kali, Fedora, Pengwin und Alpine.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Installieren, Aktivieren, WSL2, Version 2
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 248afa4695cdfdf34dd44dd0692d2cba42c32a0b
ms.sourcegitcommit: 291c6767954e3d5034ea0099e5c1e1f1ea5b577d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96470492"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows-Subsystem für Linux: Installationsleitfaden für Windows 10

## <a name="install-windows-subsystem-for-linux"></a>Installieren des Windows-Subsystems für Linux

Das Windows-Subsystem für Linux verfügt über zwei verschiedene Versionen, zwischen denen Sie während des Installationsprozesses auswählen können. WSL 2 bietet eine bessere Gesamtleistung, und wir empfehlen seine Verwendung. Wenn Ihr System WSL 2 nicht unterstützt, oder wenn in einer bestimmten Situation die systemübergreifende Dateispeicherung erforderlich ist, sollten Sie bei WSL 1 bleiben. Erfahren Sie mehr über den [Vergleich zwischen WSL 2 und WSL 1](./compare-versions.md).

> [!NOTE]
> Um den neuen Befehl `wsl --install` zu verwenden und die Schritte 1-–6 unten zu überspringen, müssen Sie dem [Windows Insiders-Programm](https://insider.windows.com/getting-started) beitreten und einen Vorschaubuild von Windows 10 (Betriebssystembuild 20262 oder höher) installieren. 
>
> Sobald der Vorschaubuild installiert ist, können Sie ein Eingabeaufforderungsfenster mit Administratorrechten öffnen und `wsl --install` ausführen. Dadurch werden automatisch die optionalen WSL- und Virtual Machine Platform-Komponenten aktiviert, der neueste Linux-Kernel wird heruntergeladen und installiert, WSL 2 wird als Standard festgelegt und Ubuntu wird heruntergeladen (dies kann am Beispiel von `wsl --install -d Debian` geändert werden; um eine Liste der verfügbaren Linux-Verteilungen anzuzeigen, geben Sie `wsl --list --online` ein). Sobald der Befehl abgeschlossen ist, werden Sie zum Neustarten aufgefordert. Nach dem Neustart schließt die Linux-Verteilung (standardmäßig Ubuntu) die Installation ab und öffnet eine Linux-Befehlszeile, die Sie nun verwenden können. Sie könnten dann mit [Schritt 7: Einrichten einer neuen Verteilung](./install-win10.md#step-7---set-up-a-new-distribution) fortfahren.

### <a name="install-steps"></a>Installationsschritte

- Öffnen Sie ein Befehlsfenster mit Administratorrechten.
- Ausführen von `wsl.exe --install`
- Starten Sie Ihren Computer bei Bedarf neu, und folgen Sie der Befehlsausführung.
- Nach dem Neustart wird die Installation abgeschlossen, und Sie können mit der Verwendung von WSL beginnen.

Dadurch wird die Ubuntu-Verteilung installiert. Sie können auch andere Verteilungen installieren, indem Sie Argumente, mit `wsl --install -d Debian` wird beispielsweise Debian installiert. Wenn Sie `wsl --list --online` ausführen, wird eine Liste der verfügbaren Verteilungen angezeigt. 

## <a name="step-1---enable-the-windows-subsystem-for-linux"></a>Schritt 1: Aktivieren des Windows-Subsystems für Linux

Bevor Sie eine Linux-Verteilung unter Windows installieren, müssen Sie zunächst das optionale Feature „Windows-Subsystem für Linux“ aktivieren.

Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Es wird empfohlen, nun mit Schritt 2 fortzufahren und auf WSL 2 zu aktualisieren, aber wenn Sie nur WSL 1 installieren möchten, können Sie Ihren Computer jetzt **neu starten** und mit [Schritt 6: Installieren der Linux-Verteilung Ihrer Wahl](./install-win10.md#step-6---install-your-linux-distribution-of-choice) fortfahren. Um auf WSL 2 zu aktualisieren, **warten Sie mit dem Neustart** Ihres Computers, und fahren Sie mit dem nächsten Schritt fort.

## <a name="step-2---update-to-wsl-2"></a>Schritt 2: Aktualisieren auf WSL 2

Zum Aktualisieren auf WSL 2 müssen Sie Windows 10 ausführen.

### <a name="requirements"></a>Anforderungen

- Für x64-Systeme: **Version 1903** oder höher mit **Build 18362** oder höher.
- Für ARM64-Systeme: **Version 2004** oder höher mit **Build 19041** oder höher.
- Builds vor 18362 unterstützen WSL 2 nicht. Verwenden Sie den [Windows Update-Assistenten](https://www.microsoft.com/software-download/windows10), um Ihre Windows-Version zu aktualisieren.

Zum Überprüfen von Version und Build drücken Sie **Windows-Logo-Taste+R**, geben Sie **winver** ein, und wählen Sie dann **OK** aus. (Oder geben Sie den Befehl `ver` an der Windows-Eingabeaufforderung ein.) Im Menü „Einstellungen“ [aktualisieren Sie auf die neueste Windows-Version](ms-settings:windowsupdate).

> [!NOTE]
> Wenn Sie Windows 10, Version 1903 oder 1909, verwenden, öffnen Sie „Einstellungen" im Windows-Menü, navigieren Sie zu „Update und Sicherheit“, und wählen Sie „Nach Updates suchen“ aus. Die Buildnummer muss über 18362.1049 oder 18363.1049 sein, wobei die Buildnummer der Nebenversion über .1049 liegen muss. Weitere Informationen: [WSL 2-bald für die Windows 10-Versionen 1903 und 1909 verfügbar](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/). Hier finden Sie [Informationen zur Problembehandlung](./troubleshooting.md#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).

## <a name="step-3---enable-virtual-machine-feature"></a>Schritt 3: Aktivieren der Funktion des virtuellen Computers

Vor der Installation von WSL 2 müssen Sie das optionale Feature **Plattform des virtuellen Computers** aktivieren.

Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Starten Sie Ihrem Computer neu**, um die WSL-Installation und das Update auf WSL 2 abzuschließen.

## <a name="step-4---download-the-linux-kernel-update-package"></a>Schritt 4: Herunterladen des Updatepakets für den Linux-Kernel

1. Laden Sie das aktuelle Paket herunter:
    - [Updatepaket für den WSL2-Linux-Kernel für x64-Computer](http://aka.ms/wsl2kernelmsix64)

    > [!NOTE]
    > Wenn Sie einen ARM64-Computer verwenden, laden Sie stattdessen [das ARM64-Paket](http://aka.ms/wsl2kernelmsiarm64) herunter. Wenn Sie sich nicht sicher sind, welchen Computertyp Sie verwenden, öffnen Sie die Eingabeaufforderung oder PowerShell, und geben Sie Folgendes ein: `systeminfo | find "System Type"`.

2. Führen Sie das im vorherigen Schritt heruntergeladene Updatepaket aus. (Doppelklicken Sie zum Ausführen – Sie werden zur Eingabe erhöhter Berechtigungen aufgefordert. Wählen Sie „Ja“, um diese Installation zu genehmigen.)

Sobald die Installation abgeschlossen ist, wechseln Sie zum nächsten Schritt –Festlegen von WSL 2 als Standardversion für die Installation neuer Linux-Verteilungen. (Überspringen Sie diesen Schritt, wenn Sie möchten, dass Ihre neuen Linux-Installationen WSL 1 verwenden.)

> [!NOTE]
> Weitere Informationen finden Sie im Artikel über die [Änderungen an der Aktualisierung des WSL2 Linux-Kernels](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) im [Blog zur Windows-Befehlszeile](https://aka.ms/cliblog).

## <a name="step-5---set-wsl-2-as-your-default-version"></a>Schritt 5: Festlegen von WSL 2 als Standardversion

Öffnen Sie PowerShell, und führen Sie den folgenden Befehl aus, um WSL 2 als Standardversion bei der Installation einer neuen Linux-Verteilung festzulegen:

```powershell
wsl --set-default-version 2
```

> [!NOTE]
> Die Aktualisierung von WSL 1 auf WSL 2 kann je nach Umfang Ihrer Zielverteilung mehrere Minuten dauern. Wenn Sie eine ältere (Legacy) Installation der WSL 1 von Windows 10 Anniversary Update oder Creators Update aus ausführen, kann ein Updatefehler auftreten. Befolgen Sie diese Anweisungen, um [alle Legacyverteilungen zu deinstallieren und zu entfernen](./install-legacy.md#uninstallingremoving-the-legacy-distro).
>
> Wenn `wsl --set-default-version` als ungültiger Befehl angezeigt wird, geben Sie `wsl --help` ein. Wenn die `--set-default-version` nicht aufgeführt ist, bedeutet dies, dass Ihr Betriebssystem sie nicht unterstützt und Sie auf Version 1903, Build 18362 oder höher, aktualisieren müssen.
>
> Wenn diese Meldung nach dem Ausführen des Befehls angezeigt wird: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`. So müssen das MSI-Updatepaket für den Linux-Kernel trotzdem installieren.

## <a name="step-6---install-your-linux-distribution-of-choice"></a>Schritt 6: Installieren der Linux-Verteilung Ihrer Wahl

1. Öffnen Sie den [Microsoft Store](https://aka.ms/wslstore), und wählen Sie Ihre bevorzugte Linux-Verteilung aus.

    ![Ansicht der Linux-Verteilungen im Microsoft Store](media/store.png)

    Über die folgenden Links wird die Seite des Microsoft Store für jede Distribution geöffnet:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [Ubuntu 20.04 LTS](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [openSUSE Leap 15.1](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [SUSE Linux Enterprise Server 12 SP5](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [SUSE Linux Enterprise Server 15 SP1](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

2. Wählen Sie auf der Seite der Verteilung die Option „Get“ (Abrufen) aus.

    ![Linux-Verteilungen im Microsoft Store](media/UbuntuStore.png)

## <a name="step-7---set-up-a-new-distribution"></a>Schritt 7: Einrichten einer neuen Verteilung

Wenn Sie eine neu installierte Linux-Verteilung zum ersten Mal starten, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, ein oder zwei Minuten zu warten, bis die Dateien dekomprimiert und auf dem PC gespeichert wurden. Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.

Anschließend müssen Sie [ein Benutzerkonto und Kennwort für Ihre neue Linux-Verteilung erstellen](./user-support.md).

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

**Herzlichen Glückwunsch! Sie haben erfolgreich eine Linux-Verteilung installiert und eingerichtet, die vollständig in Ihr Windows-Betriebssystem integriert ist.**

## <a name="install-windows-terminal-optional"></a>Installieren von Windows-Terminal (optional)

Windows Terminal aktiviert mehrere Registerkarten (schnelles Umschalten zwischen mehreren Linux-Befehlszeilen, Windows-Eingabeaufforderung, PowerShell, Azure CLI usw.) und ermöglicht, benutzerdefinierte Tastenkombinationen zu erstellen (Tastenkombinationen zum Öffnen oder Schließen von Registerkarten, zum Kopieren und Einfügen usw.) sowie die Suchfunktion und benutzerdefinierte Designs zu verwenden (Farbschemata, Schriftschnitte und Schriftgrade, Hintergrundbild/Weichzeichnen/Transparenz). [Weitere Informationen.](/windows/terminal)

[Installieren von Windows-Terminal](/windows/terminal/get-started).

  ![Windows-Terminal](media/terminal.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Festlegen der Verteilungsversion auf WSL 1 oder WSL 2

Sie können die den einzelnen installierten Linux-Distributionen zugewiesenen WSL-Version überprüfen, indem Sie die PowerShell-Befehlszeile öffnen und den folgenden Befehl (nur verfügbar in [Windows Build 18362 oder höher](ms-settings:windowsupdate)) eingeben: `wsl -l -v`

```powershell
wsl --list --verbose
```

Um eine Verteilung so einzurichten, dass sie von einer der beiden WSL-Versionen unterstützt wird, führen Sie Folgendes aus:

```powershell
wsl --set-version <distribution name> <versionNumber>
```

Ersetzen Sie hierbei `<distribution name>` durch den tatsächlichen Namen Ihrer Verteilung und `<versionNumber>` durch die Ziffer „1“ oder „2“. Sie können jederzeit zu WSL 1 zurückwechseln, indem sie denselben Befehl wie oben ausführen, aber die 2 durch eine 1 ersetzen.

Wenn Sie WSL 2 als Ihre Standardarchitektur festlegen möchten, ist dies über diesen Befehl möglich:

```powershell
wsl --set-default-version 2
```

Dadurch wird die Version jeder neu installierten Verteilung auf WSL 2 festgelegt.

## <a name="troubleshooting-installation"></a>Problembehandlung bei der Installation

Nachfolgend werden einige Fehler und vorgeschlagene Korrekturen beschrieben. Weitere allgemeine Fehler und zugehörige Lösungen finden Sie auf der [Seite für die WSL-Problembehandlung](troubleshooting.md).

- **Installation failed with error 0x80070003 (Installationsfehler mit Fehlercode 0x80070003)**
  - Das Windows-Subsystem für Linux wird nur auf dem Systemlaufwerk ausgeführt (in der Regel ist dies Ihr Laufwerk `C:`). Stellen Sie sicher, dass die Verteilungen auf dem Systemlaufwerk gespeichert sind:  
  - Öffnen Sie **Einstellungen** -> **System --> **Speicher** -> **Weitere Speichereinstellungen: Ändern Sie den Speicherort für neue Inhalte**
    ![Abbildung der Systemeinstellungen für die Installation von Apps auf dem Laufwerk C:](media/AppStorage.png)

- **WslRegisterDistribution failed with error 0x8007019e (WslRegisterDistribution-Fehler mit Fehlercode 0x8007019e)**
  - Die optionale Komponente des Windows-Subsystems für Linux ist nicht aktiviert:
  - Öffnen Sie **Systemsteuerung** -> **Programme und Funktionen** -> **Windows-Funktion aktivieren oder deaktivieren**. Aktivieren Sie die Option **Windows-Subsystem für Linux**, oder verwenden Sie das PowerShell-Cmdlet, das am Anfang dieses Artikels erwähnt wurde.

- **Fehler 0x80070003 oder Fehler 0x80370102 während der Installation**
  - Stellen Sie sicher, dass im BIOS Ihres Computers die Virtualisierung aktiviert ist. Die Anweisungen zur Aktivierung variieren je nach Computer. Die entsprechenden Optionen befinden sich wahrscheinlich in den CPU-bezogenen Einstellungen.

- **Fehler beim Upgradeversuch: `Invalid command line option: wsl --set-version Ubuntu 2`**
  - Stellen Sie sicher, dass das Windows-Subsystem für Linux aktiviert wurde und Sie die Windows-Buildversion 18362 oder höher verwenden. Führen Sie zum Aktivieren von WSL in einer PowerShell-Eingabeaufforderung mit Administratorberechtigungen diesen Befehl aus: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.

- **Der angeforderte Vorgang konnte aufgrund einer Einschränkung des virtuellen Dateisystems nicht abgeschlossen werden. Dateien für virtuelle Festplatten müssen unkomprimiert und unverschlüsselt sein und dürfen keine geringe Dichte aufweisen.**
  - Zum Deaktivieren von „Inhalte komprimieren“ (sowie „Inhalte verschlüsseln“, falls aktiviert), öffnen Sie den Profilordner Ihrer Linux-Verteilung. Er sollte sich in einem Ordner auf Ihrem Windows-Dateisystem befinden, der etwa folgendermaßen heißt: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.
  - In diesem Linux-Verteilungsprofil sollte ein Ordner "LocalState" vorhanden sein. Klicken Sie mit der rechten Maustaste auf diesen Ordner, um ein Menü mit Optionen anzuzeigen. Wählen Sie „Eigenschaften“ > „Erweitert“ aus, und stellen Sie dann sicher, dass die Kontrollkästchen „Inhalt komprimieren, um Speicherplatz zu sparen“ und „Inhalt verschlüsseln, um Daten zu schützen“ nicht aktiviert (nicht ausgewählt) sind. Wenn Sie gefragt werden, ob Sie diese Einstellung nur auf den aktuellen Ordner oder auf alle Unterordner und Dateien anwenden möchten, wählen Sie „Nur dieser Ordner“ aus, da Sie nur das Komprimierungsflag löschen. Danach sollte der Befehl `wsl --set-version` funktionieren.

![Screenshot der Eigenschafteneinstellungen der WSL-Verteilung](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> In meinem Fall befand sich der Ordner „LocalState“ für meine Ubuntu 18.04-Verteilung unter „C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc“.
>
> Prüfen Sie den [GitHub-Thread #4103 in der WSL-Dokumentation](https://github.com/microsoft/WSL/issues/4103), der diesem Thema gewidmet ist, auf aktualisierte Informationen.

- **Der Ausdruck 'wsl' wurde nicht als Name eines Cmdlets, einer Funktion, einer Skriptdatei oder eines ausführbaren Programms erkannt.**
  - Vergewissern Sie sich, dass die [optionale Komponente Windows-Subsystem für Linux installiert ist](./install-win10.md#step-3---enable-virtual-machine-feature). Außerdem wird dieser Fehler angezeigt, wenn Sie ein ARM64-Gerät verwenden und diesen Befehl aus PowerShell ausführen. Führen Sie stattdessen `wsl.exe` in [PowerShell Core](/powershell/scripting/install/installing-powershell-core-on-windows) oder einer Eingabeaufforderung aus.

- **Error: Dieses Update gilt nur für Computer mit dem Windows-Subsystem für Linux.**
  - Zum Installieren des MSI-Updatepakets für den Linux-Kernel ist WSL erforderlich und sollte zuerst aktiviert werden. Wenn ein Fehler auftritt, wird die folgende Meldung angezeigt: `This update only applies to machines with the Windows Subsystem for Linux`.
  - Es gibt drei mögliche Gründe, warum diese Meldung angezeigt wird:

  1. Sie befinden sich immer noch in der alten Version von Windows, die WSL 2 nicht unterstützt. In Schritt 2 finden Sie Versionsanforderungen und Links zum Update.

  2. WSL ist nicht aktiviert. Sie müssen zu Schritt 1 zurückkehren und sicherstellen, dass das optionale WSL-Feature auf Ihrem Computer aktiviert ist.

  3. Nachdem Sie WSL aktiviert haben, muss ein Neustart durchgeführt werden, damit es wirksam wird. Starten Sie den Computer neu, und wiederholen Sie den Vorgang.

- **Error: WSL 2 erfordert ein Update der zugehörigen Kernel-Komponente. Weitere Informationen finden Sie unter https://aka.ms/wsl2kernel.**
  - Wenn das Linux-Kernelpaket im Ordner „%SystemRoot%\system32\lxss\tools“ fehlt, wird tritt dieser Fehler auf. Lösen Sie dieses Problem, indem Sie das MSI-Updatepaket für den Linux-Kernel (siehe Schritt 4 dieser Installationsanleitung) installieren. Sie müssen den MSI möglicherweise über [Software](ms-settings:appsfeatures-app) deinstallieren und dann erneut installieren.
