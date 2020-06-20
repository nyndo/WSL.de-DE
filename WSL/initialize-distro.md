---
title: Initialisieren einer neuen WSL Linux-Distribution
description: Nach dem Installieren einer Linux-Distribution für WSL führen Sie die folgenden einfachen Schritte aus, um die Initialisierung abzuschließen.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7ce4455dd4ab5e75d69ba841d7dfb7963af9c891
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235793"
---
# <a name="initializing-a-newly-installed-distribution"></a>Initialisieren einer neu installierten Distribution

Nachdem Sie Ihre Distribution heruntergeladen und installiert haben, müssen Sie die Initialisierung der neuen Distribution abschließen:

## <a name="launch-a-distribution"></a>Starten einer Distribution

Um die Initialisierung der neu installierten Distribution abzuschließen, starten Sie eine neue Instanz. Klicken Sie hierzu in der Microsoft Store-App auf die Schaltfläche „Starten“, oder starten Sie die Distribution über das Startmenü:

> Tipp: Möglicherweise möchten Sie Ihre am häufigsten verwendeten Distributionen an das Startmenü und/oder an die Taskleiste anheften.

![Starten von Distributionen über das Startmenü](media/start-menu.png)

> Unter Windows Server können Sie die ausführbare Startprogrammdatei `<distribution>.exe` Ihrer Distribution über dem Distributionsinstallationsordner starten.

Wenn eine neu installierte Distribution zum ersten Mal ausgeführt wird, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, bis zum Abschluss der Installation wenige Minuten zu warten.

> In dieser letzten Phase der Installation werden die Dateien der Distribution dekomprimiert und auf Ihrem PC gespeichert. Sie sind dann einsatzbereit. Dies kann je nach Leistung der Speichergeräte Ihres PCs etwa eine Minute oder ggf. auch länger dauern. Diese erste Installationsphase ist nur erforderlich, wenn eine „saubere“ Distribution installiert wird. Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.

## <a name="setting-up-a-new-linux-user-account"></a>Einrichten eines neuen Linux-Benutzerkontos

Nach Abschluss der Installation werden Sie aufgefordert, ein neues Benutzerkonto (und das zugehörige Kennwort) zu erstellen.

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

Dieses Benutzerkonto gilt für den normalen Benutzer ohne Administratorrechte, als der Sie beim Starten einer Distribution standardmäßig angemeldet werden.

> Sie können einen beliebigen Benutzernamen und ein gewünschtes Kennwort auswählen. Beides hat keinen Einfluss auf Ihren Windows-Benutzernamen.

Wenn Sie eine neue Distributionsinstanz öffnen, werden Sie nicht zur Eingabe Ihres Kennworts aufgefordert. Wenn Sie jedoch **einen Prozess mit `sudo` heraufstufen, müssen Sie Ihr Kennwort eingeben**. Stellen Sie also sicher, dass Sie ein Kennwort auswählen, das Sie sich leicht merken können. Weitere Informationen finden Sie auf der Seite [Benutzersupport](user-support.md).

## <a name="update--upgrade-your-distributions-packages"></a>Aktualisieren und Upgraden der Pakete Ihrer Distribution

Die meisten Distributionen werden mit einem leeren/minimalen Paketkatalog ausgeliefert. Es wird dringend empfohlen, den Paketkatalog regelmäßig zu aktualisieren und ein Upgrade der installierten Pakete mit dem bevorzugten Paket-Manager Ihrer Distribution auszuführen. Unter Debian/Ubuntu verwenden Sie apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows führt für Ihre Linux-Distribution(en) nicht automatisch eine Aktualisierung oder ein Upgrade aus: Linux-Benutzer ziehen es vor, diese Aufgabe selbst zu steuern.

Fertig! Viel Spaß bei der Verwendung Ihrer neuen Linux-Distribution unter WSL! Weitere Informationen zu WSL finden Sie in der weiteren [WSL-Dokumentation](https://aka.ms/wsldocs) oder auf der [Seite mit den WSL-Lernressourcen](https://aka.ms/learnwsl).

![Viel Spaß bei der Verwendung von Linux unter WSL!](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>Problembehandlung

Nachfolgend werden einige Fehler und vorgeschlagene Korrekturen beschrieben. Weitere allgemeine Fehler und zugehörige Lösungen finden Sie auf der [Seite für die WSL-Problembehandlung](troubleshooting.md).

> **Fehler bei der Installation: 0x8007007e**: Dieser Fehler tritt auf, wenn das System Linux aus dem Store nicht unterstützt.  Stellen Sie Folgendes sicher:
> * Sie führen Windows-Build 16215 oder höher aus. [Überprüfen Sie Ihren Build](troubleshooting.md#check-your-build-number).
> * Die optionale Komponente des Windows-Subsystems für Linux ist aktiviert, und der Computer wurde neu gestartet.  [Stellen Sie sicher, dass WSL aktiviert ist](troubleshooting.md#confirm-wsl-is-enabled).
