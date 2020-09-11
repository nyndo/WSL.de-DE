---
title: Installieren des Windows-Subsystems für Linux (WSL) unter Windows 10
description: Erfahren Sie, wie Sie das Windows-Subsystem für Linux unter Windows 10 installieren. Windows 10 muss auf Version 2004, Build 19041 oder höher aktualisiert werden.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Installieren, Aktivieren, WSL2, Version 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 50b434e288ba90173875cf5e7cd5fe9e6c3d8a16
ms.sourcegitcommit: 498592fa4b09015be3ee9a8913e5e3cf755de24b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559290"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Windows-Subsystem für Linux: Installationsleitfaden für Windows 10

## <a name="install-the-windows-subsystem-for-linux"></a>Installieren des Windows-Subsystems für Linux

Bevor Sie eine Linux-Verteilung unter Windows installieren können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ aktivieren.

Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

Um nur WSL 1 zu installieren, sollten Sie nun den Computer neu starten und mit dem [Installieren der Linux-Verteilung Ihrer Wahl](./install-win10.md#install-your-linux-distribution-of-choice) fortfahren. Andernfalls warten Sie auf den Neustart, und fahren Sie mit dem Update auf WSL 2 fort. Erfahren Sie mehr über den [Vergleich zwischen WSL 2 und WSL 1](./compare-versions.md).

## <a name="update-to-wsl-2"></a>Aktualisieren auf WSL 2

Um ein Update auf WSL 2 durchführen zu können, müssen die folgenden Kriterien erfüllt sein:

- Ausführen von Windows 10, [aktualisiert auf Version 1903 oder höher](ms-settings:windowsupdate), **Build 18362** oder höher, für x64-Systeme.
   - Wenn Sie Windows 10, Version 1903 oder 1909, verwenden, stellen Sie sicher, dass die Buildnummer Ihrer Nebenversion 1049 oder höher ist. Ausführliche Informationen zur Problembehandlung finden Sie [hier](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).
- Ausführen von Windows 10, aktualisiert auf Version 2004 oder höher, **Build 19041**, für ARM64-Systeme.
- Beachten Sie, dass Sie unter Windows 10, Version 1903 oder 1909, sicherstellen müssen, dass Sie über den richtigen Backport verfügen. Anweisungen finden Sie [hier](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it). 

- Überprüfen Sie Ihre Windows-Version, indem Sie die **Windows-Logo-Taste+R** auswählen, **winver** eingeben und **OK** auswählen. (Oder geben Sie den Befehl `ver` an der Windows-Eingabeaufforderung ein.) [Aktualisieren Sie auf die neueste Windows-Version](ms-settings:windowsupdate), wenn Ihr Build niedriger als 18361 ist. [Holen Sie sich den Windows Update-Assistenten](https://www.microsoft.com/software-download/windows10).

### <a name="enable-the-virtual-machine-platform-optional-component"></a>Aktivieren Sie die optionale Komponente „Virtual Machine Platform“.

Vor der Installation von WSL 2 müssen Sie das optionale Feature „Virtual Machine Platform“ aktivieren.

Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

**Starten Sie Ihrem Computer neu**, um die WSL-Installation und das Update auf WSL 2 abzuschließen.

### <a name="set-wsl-2-as-your-default-version"></a>Festlegen von WSL 2 als Standardversion

Öffnen Sie PowerShell als Administrator und führen Sie den folgenden Befehl aus, um WSL 2 als Standardversion bei der Installation einer neuen Linux-Verteilung festzulegen:

```powershell
wsl --set-default-version 2
```

Diese Meldung wird möglicherweise nach dem Ausführen des folgenden Befehls angezeigt: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`. Befolgen Sie den Link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)), und installieren Sie die MSI von dieser Seite in unserer Dokumentation, um einen Linux-Kernel auf Ihrem Computer zu installieren, der von WSL 2 verwendet werden kann. Sobald Sie den Kernel installiert haben, führen Sie den Befehl erneut aus. Er sollte nun erfolgreich abgeschlossen werden, ohne dass die Meldung angezeigt wird. 

> [!NOTE]
> Die Aktualisierung von WSL 1 auf WSL 2 kann je nach Umfang Ihrer Zielverteilung mehrere Minuten dauern. Wenn Sie eine ältere (Legacy) Installation der WSL 1 von Windows 10 Anniversary Update oder Creators Update aus ausführen, kann ein Updatefehler auftreten. Befolgen Sie diese Anweisungen, um [alle Legacyverteilungen zu deinstallieren und zu entfernen](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro). 
>
> Wenn `wsl --set-default-version` als ungültiger Befehl angezeigt wird, geben Sie `wsl --help` ein. Wenn die `--set-default-version` nicht aufgeführt ist, bedeutet dies, dass Ihr Betriebssystem sie nicht unterstützt und Sie auf Version 1903, Build 18362 oder höher, aktualisieren müssen.

## <a name="install-your-linux-distribution-of-choice"></a>Installieren der Linux-Verteilung Ihrer Wahl

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

## <a name="set-up-a-new-distribution"></a>Einrichten einer neuen Verteilung

Wenn Sie eine neu installierte Linux-Verteilung zum ersten Mal starten, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, ein oder zwei Minuten zu warten, bis die Dateien dekomprimiert und auf dem PC gespeichert wurden. Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.

Anschließend müssen Sie [ein Benutzerkonto und Kennwort für Ihre neue Linux-Verteilung erstellen](./user-support.md).

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

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
  - Öffnen Sie **Einstellungen** -> **Speicher** -> **Weitere Speichereinstellungen: Ändern Sie den Speicherort für neue Inhalte**
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
  - Vergewissern Sie sich, dass die [optionale Komponente Windows-Subsystem für Linux installiert ist](./install-win10.md#enable-the-virtual-machine-platform-optional-component). Außerdem wird dieser Fehler angezeigt, wenn Sie ein ARM64-Gerät verwenden und diesen Befehl aus PowerShell ausführen. Führen Sie stattdessen `wsl.exe` in [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) oder einer Eingabeaufforderung aus.
