---
title: Installieren des Linux-Subsystems unter Windows Server
description: Installationsanweisungen für das Linux-Subsystem unter Windows Server.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 805b7d266020c62e0c6f58889541517d44db3726
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153081"
---
# <a name="windows-server-installation-guide"></a>Windows Server-Installationsleitfaden

Das Windows-Subsystem für Linux ist für die Installation unter Windows Server 2019 (Version 1709) und höher verfügbar. Diese Anleitung führt Sie durch die Schritte zum Aktivieren von WSL auf Ihrem Computer.

## <a name="enable-the-windows-subsystem-for-linux"></a>Aktivieren des Windows-Subsystems für Linux

Damit Sie Linux-Distributionen unter Windows ausführen können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ aktivieren und das System neu starten.

Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

**Wenn Sie 100%ige Systemaufruf-Kompatibilität und schnellere E/A-Leistung suchen, lesen Sie die unten stehenden Informationen zur Installation von WSL 2.**

WSL 2 ist nur in Windows 10, Version 2004, Build 19041 oder höher verfügbar. Möglicherweise müssen Sie [Ihre Windows-Version aktualisieren](ms-settings:windowsupdate).

**Falls Sie mit WSL 1 fortfahren, starten Sie Ihren Rechner neu, wenn Sie dazu aufgefordert werden, und setzen Sie die Installation [hier](./install-on-server.md#download-a-linux-distribution) fort.**

## <a name="enable-the-virtual-machine-platform-optional-component"></a>Aktivieren Sie die optionale Komponente „Virtual Machine Platform“.

Stellen Sie sicher, dass die optionale Komponente „Virtual Machine Platform“ installiert ist. Zu diesem Zweck können Sie den folgenden Befehl in PowerShell ausführen:

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

## <a name="download-a-linux-distribution"></a>Herunterladen einer Linux-Distribution

Befolgen Sie [diese Anweisungen](install-manual.md), um Ihre bevorzugte Linux-Distribution herunterzuladen.

## <a name="extract-and-install-a-linux-distribution"></a>Extrahieren und Installieren einer Linux-Distribution

Nachdem Sie nun eine Linux-Distribution heruntergeladen haben, um ihren Inhalt zu extrahieren und manuell zu installieren, führen Sie die folgenden Schritte aus:

1. Extrahieren Sie den Inhalt des `<distro>.appx`-Pakets mithilfe von PowerShell:

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. Führen Sie die Startanwendung der Distribution im Zielordner aus. Die Startanwendung heißt normalerweise `<distro>.exe` (z. B. `ubuntu.exe`).

    ![Aufgeklappte Ubuntu-Distribution unter Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> **Installation failed with error 0x8007007e** (Installationsfehler mit Fehlercode 0x8007007e): Sie erhalten diesen Fehler, wenn das System WSL nicht unterstützt. Stellen Sie sicher, dass Sie Windows-Build 16215 oder höher aus führen. [Überprüfen Sie Ihren Build](troubleshooting.md#check-your-build-number). [Vergewissern Sie sich auch, dass die WSL aktiviert ist](troubleshooting.md#confirm-wsl-is-enabled) und Ihr Computer neu gestartet wurde, nachdem das Feature aktiviert wurde.  

3. Fügen Sie der Windows-Umgebungsvariablen PATH den Pfad der Distribution hinzu (in diesem Beispiel `C:\Users\Administrator\Ubuntu`), mithilfe von PowerShell:

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

Sie können Ihre Distribution nun über einen beliebigen Pfad starten, indem Sie `<distro>.exe`eingeben. Beispiel: `ubuntu.exe`.

Nachdem der Installation müssen Sie [Ihre neue Distributionsinstanz initialisieren](initialize-distro.md), bevor Sie sie verwenden.
