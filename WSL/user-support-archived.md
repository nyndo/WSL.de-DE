---
title: WSL-Benutzerkonto Updates in früheren Windows-Versionen
description: Referenz für frühere Windows-Versionen zum Aktualisieren von Linux-Benutzerkonten mit dem Windows-Subsystem für Linux.
ms.date: 01/20/2020
ms.topic: article
ROBOTS: NOINDEX
ms.openlocfilehash: 33a42c8f3bd518fa45df2874a6c59b76cd8ec80a
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413361"
---
# <a name="wsl-user-account-updates-on-previous-windows-versions"></a>WSL-Benutzerkonto Updates in früheren Windows-Versionen

Dieser Inhalt ist für Benutzer früherer Versionen des Windows-Betriebssystems archiviert, die das-Subsystem für Linux unterstützen und Unterstützung beim Aktualisieren von Linux-Benutzerkonten benötigen.

Die aktuelle Dokumentation finden Sie unter [Benutzerkonten für das Windows-Subsystem für Linux](./user-support.md).

### <a name="for-creators-update-version-of-windows-and-earlier"></a>Für Creators Update-Version von Windows und früher

Wenn Sie Windows 10 Creators Update oder eine frühere Version ausführen, können Sie den Bash-Standardbenutzer ändern, indem Sie die folgenden Befehle ausführen:

1. Ändern Sie den Standardbenutzer in `root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. Führen `bash.exe` Sie aus, um sich jetzt als `root` anzumelden:

    ```console
    C:\> bash.exe
    ```

1. Setzen Sie Ihr Kennwort mit dem Kennwortbefehl der Distribution zurück, und schließen Sie die Linux-Konsole:

    ```BASH
    $ passwd username
    $ exit
    ```

1. Setzen Sie Ihren Standardbenutzer über Windows-CMD zurück auf Ihr normales Linux-Benutzerkonto:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update und höhere Versionen

Um anzuzeigen, welche Befehle für eine bestimmte Distribution verfügbar sind, führen Sie `[distro.exe] /?` aus.
    
Beispielsweise bei einer Ubuntu-Installation:

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

Schrittweise Anleitungen für Ubuntu:

1. Öffnen Sie CMD.
1. Legen Sie den Linux -Standardbenutzer auf `root` fest:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. Starten Sie Ihre Linux-Distribution (`ubuntu`).  Sie werden automatisch als `root` angemeldet:

1. Setzen Sie Ihr Kennwort mit dem Befehl `passwd` zurück:

    ```BASH
    $ passwd username
    ```

1. Setzen Sie Ihren Standardbenutzer über Windows-CMD zurück auf Ihr normales Linux-Benutzerkonto.

    ```console
    C:\> ubuntu config --default-user username
    ```
