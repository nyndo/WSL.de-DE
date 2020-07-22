---
title: Archivierte WSL-Anweisungen
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ROBOTS: NOINDEX
ms.openlocfilehash: 1de614dccbbb8d0ef1b9ac070f6ec90281339858
ms.sourcegitcommit: 16ffb1a096a4a7fbb77c58f92258051930cc82da
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2020
ms.locfileid: "86157956"
---
# <a name="archived-instructions"></a>Archivierte Anweisungen

Im folgenden Leitfaden werden die Schritte beschrieben, die ausgeführt werden müssen, um das Windows-Subsystem für Linux (WSL) auf einem Computer mit Windows 10 zu installieren.

## <a name="enable-the-windows-subsystem-for-linux-optional-feature"></a>Aktivieren des optionalen Features „Windows-Subsystem für Linux“

Bevor Sie eine Linux-Distribution installieren können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ unter Windows 10 aktivieren:

1. Öffnen Sie PowerShell als Administrator, und geben Sie dieses Skript ein:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

1. Starten Sie den Computer neu, wenn Sie dazu aufgefordert werden.

## <a name="install-a-linux-distribution"></a>Installieren einer Linux-Distribution

Es gibt drei Möglichkeiten, Ihre bevorzugte(n) Linux-Distribution(en) herunterzuladen und zu installieren:

- Herunterladen und Installieren aus dem Microsoft Store (siehe unten)
- [Herunterladen und manuelles Installieren über die Befehlszeile](install-manual.md)
- [Installieren unter Windows Server](install-on-server.md)

### <a name="install-from-the-microsoft-store"></a>Herunterladen aus dem Microsoft Store

Linux-Distributionen können über den Microsoft Store auf Windows 10 (Build 16215+) installiert werden.

> [!NOTE]
> Führen Sie diese Schritte aus, um [die Nummer Ihres Windows 10-Builds zu überprüfen](troubleshooting.md#check-your-build-number).

1. Öffnen Sie den Microsoft Store, und wählen Sie Ihre bevorzugte Linux-Distribution aus.

    ![Ansicht der Linux-Distributionen im Microsoft Store](media/store.png)

    Über die folgenden Links wird die Seite des Microsoft Store für jede Distribution geöffnet:

    - [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    - [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    - [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    - [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    - [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. Wählen Sie „Get“ aus, und klicken Sie nach dem Herunterladen der Distribution auf „Starten“.

    ![Ansicht der Linux-Distributionen im Microsoft Store](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>Vervollständigen der Initialisierung Ihrer Distribution

Nachdem Sie Ihre Linux-Distribution gestartet haben, befolgen Sie die Anweisungen auf dem Bildschirm, um Ihre Distribution zu initialisieren.

> [!NOTE]
> Starten Sie die Distribution für Windows Server mithilfe der ausführbaren Datei `<distro>.exe` im Installationsordner.

Wenn eine neu installierte Distribution zum ersten Mal ausgeführt wird, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, bis zum Abschluss der Installation wenige Minuten zu warten. In dieser letzten Phase der Installation werden die Dateien der Distribution dekomprimiert und auf Ihrem PC gespeichert. Sie sind dann einsatzbereit. Dies kann je nach Leistung der Speichergeräte Ihres PCs etwa eine Minute oder ggf. auch länger dauern. Diese erste Installationsphase ist nur erforderlich, wenn eine „saubere“ Distribution installiert wird. Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.

## <a name="set-up-a-new-linux-user-account"></a>Einrichten eines neuen Linux-Benutzerkontos

Nach Abschluss der Installation werden Sie aufgefordert, ein neues Benutzerkonto (und das zugehörige Kennwort) zu erstellen.

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

Dieses Benutzerkonto gilt für den normalen Benutzer ohne Administratorrechte, als der Sie beim Starten einer Distribution standardmäßig angemeldet werden. Sie können einen beliebigen Benutzernamen und ein gewünschtes Kennwort auswählen. Beides hat keinen Einfluss auf Ihren Windows-Benutzernamen.

Wenn Sie eine neue Distributionsinstanz öffnen, werden Sie nicht zur Eingabe Ihres Kennworts aufgefordert. Wenn Sie jedoch **einen Prozess mit `sudo` heraufstufen, müssen Sie Ihr Kennwort eingeben**. Stellen Sie also sicher, dass Sie ein Kennwort auswählen, das Sie sich leicht merken können. Weitere Informationen finden Sie auf der Seite [Benutzersupport](user-support.md).

## <a name="update--upgrade-packages"></a>Update- und Upgradepakete

Die meisten Distributionen werden mit einem leeren oder minimalen Paketkatalog ausgeliefert. Es wird dringend empfohlen, den Paketkatalog regelmäßig zu aktualisieren und ein Upgrade der installierten Pakete mit dem bevorzugten Paket-Manager Ihrer Distribution auszuführen. Für Debian/Ubuntu verwenden Sie apt:

```bash
sudo apt update && sudo apt upgrade
```

Windows führt für Ihre Linux-Distribution(en) nicht automatisch eine Aktualisierung oder ein Upgrade aus. Dies ist eine Aufgabe, die die meisten Linux-Benutzer lieber selbst in die Hand nehmen.

Viel Spaß bei der Verwendung Ihrer neuen Linux-Distribution unter WSL!

## <a name="troubleshooting"></a>Problembehandlung

Nachfolgend werden einige Installationsfehler und vorgeschlagene Korrekturen beschrieben. Weitere allgemeine Fehler und zugehörige Lösungen finden Sie auf der [Seite für die WSL-Problembehandlung](troubleshooting.md).

### <a name="installation-failed-with-error-0x8007007e"></a>Installationsfehler mit Fehlercode 0x8007007e

Dieser Fehler tritt auf, wenn das System Linux aus dem Store nicht unterstützt.  Stellen Sie Folgendes sicher:

- Sie führen Windows-Build 16215 oder höher aus. [Überprüfen Sie Ihren Build](troubleshooting.md#check-your-build-number).
- Die optionale Komponente des Windows-Subsystems für Linux ist aktiviert, und der Computer wurde neu gestartet.  [Stellen Sie sicher, dass WSL aktiviert ist](troubleshooting.md#confirm-wsl-is-enabled).

### <a name="installation-failed-with-error-0x80070003"></a>Installationsfehler mit Fehlercode 0x80070003

Das Windows-Subsystem für Linux wird nur auf dem Systemlaufwerk ausgeführt (in der Regel ist dies Ihr Laufwerk `C:`). Stellen Sie sicher, dass die Distributionen auf dem Systemlaufwerk gespeichert sind:

- Öffnen Sie **Einstellungen** -> **Speicher** -> **Weitere Speichereinstellungen: Ändern Sie den Speicherort für neue Inhalte**
  
    ![Abbildung der Systemeinstellungen für die Installation von Apps auf dem Laufwerk C:](media/AppStorage.png)

### <a name="wslregisterdistribution-failed-with-error-0x8007019e"></a>WslRegisterDistribution-Fehler mit Fehlercode 0x8007019e

Die optionale Komponente des Windows-Subsystems für Linux ist nicht aktiviert:

- Öffnen Sie **Systemsteuerung** -> **Programme und Funktionen** -> **Windows-Funktion aktivieren oder deaktivieren**. Aktivieren Sie die Option **Windows-Subsystem für Linux**, oder verwenden Sie das PowerShell-Cmdlet, das am Anfang dieses Artikels erwähnt wurde.
