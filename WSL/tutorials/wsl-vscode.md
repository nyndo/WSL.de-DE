---
title: Beginnen Sie mit der Verwendung von vs Code mit dem Windows-Subsystem für Linux
description: Erfahren Sie, wie Sie vs Code zum Erstellen und Debuggen von Code mithilfe des Windows-Subsystems für Linux einrichten.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, vs Code, Remote Extension, Debug, Path, Visual Studio
ms.date: 05/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: b39b34644040354df44bf62ec7b878e3f5d667e6
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413341"
---
# <a name="get-started-using-visual-studio-code-with-windows-subsystem-for-linux"></a>Beginnen Sie mit der Verwendung von Visual Studio Code mit dem Windows-Subsystem für Linux

Visual Studio Code können Sie zusammen mit der Remote-WSL-Erweiterung WSL als voll Zeit Entwicklungsumgebung direkt von vs Code verwenden. Ihre Möglichkeiten:

* entwickeln in einer Linux-basierten Umgebung
* Linux-spezifische Toolchain und Hilfsprogramme verwenden
* ausführen und Debuggen Ihrer Linux-basierten Anwendungen von der Komfort von Windows, während der Zugriff auf Produktivitäts Tools wie Outlook und Office gewährleisten wird
* Verwenden Sie das integrierte Terminal vs Code, um Ihre Linux-Distribution Ihrer Wahl auszuführen.
* profitieren Sie von vs Code Features wie [IntelliSense-Code Vervollständigung](https://code.visualstudio.com/docs/editor/intellisense), [linting](https://code.visualstudio.com/docs/python/linting), [Debug-Unterstützung](https://code.visualstudio.com/docs/nodejs/nodejs-debugging), [Code Ausschnitte](https://code.visualstudio.com/docs/editor/userdefinedsnippets)und Komponenten [Tests](https://code.visualstudio.com/docs/python/testing) .
* Verwalten Sie Ihre Versionskontrolle einfach mit der integrierten git- [Unterstützung](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support) von vs Code
* Ausführen von Befehlen und vs Code Erweiterungen direkt in ihren WSL-Projekten
* Bearbeiten Sie Dateien in Ihrem Linux-oder eingebundenen Windows-Dateisystem (z. b./mnt/c), ohne sich Gedanken über die Probleme mit der Bereitstellung, binäre Kompatibilität oder andere außer Betriebssysteme

## <a name="install-vs-code-and-the-remote-wsl-extension"></a>Installieren von vs Code und der WSL-Remote Erweiterung

* Besuchen Sie die [Seite vs Code Installation](https://code.visualstudio.com/download) , und wählen Sie den Installer 32 oder 64 Bit aus. Installieren Sie Visual Studio Code unter Windows (nicht in Ihrem WSL-Dateisystem).

* Wenn Sie aufgefordert werden, während der Installation **Weitere Aufgaben auszuwählen** , stellen Sie sicher, dass Sie die Option **zum Pfad hinzufügen** aktivieren, damit Sie mit dem Code Befehl problemlos einen Ordner in WSL öffnen können.

* Installieren Sie das [remoteentwicklungs-Erweiterungspaket](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack). Dieses Erweiterungspaket enthält zusätzlich zu den Remote-SSH-und Remote Container Erweiterungen die Remote-WSL-Erweiterung, mit der Sie einen beliebigen Ordner in einem Container, auf einem Remote Computer oder in WSL öffnen können.

> [!IMPORTANT]
> Um die Remote-WSL-Erweiterung zu installieren, benötigen Sie die Version [1,35](https://code.visualstudio.com/updates/v1_35) oder höher von vs Code. Es wird nicht empfohlen, WSL in vs Code ohne die Remote-WSL-Erweiterung zu verwenden, da Sie die Unterstützung für automatisches vervollständigen, Debuggen, linting usw. verlieren. Spaß Fakt: Diese WSL-Erweiterung wird in $Home/.vscode/Extensions installiert (geben Sie den Befehl `ls $HOME\.vscode\extensions\` in PowerShell ein).

## <a name="update-your-linux-distribution"></a>Aktualisieren Ihrer Linux-Distribution

In einigen WSL Linux-Distributionen fehlen Bibliotheken, die vom vs Code Server benötigt werden, um gestartet werden zu können. Mithilfe des Paket-Managers können Sie Ihrer Linux-Distribution weitere Bibliotheken hinzufügen.

Um z. b. Debian oder Ubuntu zu aktualisieren, verwenden Sie Folgendes:

```bash
sudo apt-get update
```

Geben Sie Folgendes ein, um wget (zum Abrufen von Inhalten von Webservern) und ZS-Zertifikaten (damit SSL-basierte Anwendungen die Authentizität von SSL-Verbindungen überprüfen können):

```bash
sudo apt-get install wget ca-certificates
```

## <a name="open-a-wsl-project-in-visual-studio-code"></a>Öffnen Sie ein WSL-Projekt in Visual Studio Code

### <a name="from-the-command-line"></a>Über die Befehlszeile

Öffnen Sie die Befehlszeile der Distribution, und geben Sie Folgendes ein, um ein Projekt aus der WSL-Distribution zu öffnen: `code .`

![WSL-Projekt mit vs Code Remote Server öffnen](../media/wsl-open-vs-code.gif)

### <a name="from-vs-code"></a>Von vs Code

Sie können auch auf weitere vs Code Remote Optionen zugreifen, indem Sie die Verknüpfung verwenden: `CTRL+SHIFT+P` in vs Code, um die Befehls Palette anzuzeigen. Wenn Sie dann eingeben, `VSCODE-REMOTE` werden alle verfügbaren vs Code Remote Optionen angezeigt. Dadurch können Sie den Ordner in einer Remote Sitzung erneut öffnen, angeben, welche Distribution Sie öffnen möchten, und vieles mehr.

![Befehls Palette vs Code](../media/vscode-remote-command-palette.png)

## <a name="extensions-inside-of-vs-code-remote"></a>Erweiterungen in vs Code Remote

Die Remote-WSL-Erweiterung teilt vs Code in eine Client-Server-Architektur auf, wobei der Client (die Benutzeroberfläche) auf Ihrem Windows-Computer und der Server (Code, git, Plug-ins usw.) Remote ausgeführt wird.

Wenn Sie vs Code Remote ausführen, wird durch Auswählen der Registerkarte "Extensions" eine Liste der Erweiterungen angezeigt, die zwischen dem lokalen Computer und der WSL-Distribution aufgeteilt sind.

Die Installation einer lokalen Erweiterung, wie z. b [. ein Design](https://marketplace.visualstudio.com/search?target=VSCode&category=Themes&sortBy=Installs), muss nur einmal installiert werden.

Einige Erweiterungen, wie z. b. die [python-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-python.python) oder Elemente, die Dinge wie das linting oder Debuggen verarbeiten, müssen separat auf jeder WSL-Remote Distribution installiert werden. In vs Code wird ein Warnsymbol ⚠ zusammen mit einer grünen Schaltfläche "in WSL installieren" angezeigt, wenn Sie lokal eine Erweiterung installiert haben, die nicht auf dem WSL-Remote Computer installiert ist.

![VS Code mit Remote-WSL-Erweiterungen im Vergleich zu lokalen Erweiterungen](../media/vscode-remote-wsl-extensions.png)

Weitere Informationen finden Sie in den vs Code-Dokumentation:

* Wenn vs Code Remote in WSL gestartet wird, werden keine shellstartskripts ausgeführt. Weitere Informationen zum Ausführen zusätzlicher Befehle oder zum Ändern der Umgebung finden Sie in diesem [Artikel zum Setup Skript für erweiterte Umgebungen](https://code.visualstudio.com/docs/remote/wsl#_advanced-environment-setup-script) .

* Haben Sie Probleme beim Starten von vs Code von der WSL-Befehlszeile? Dieses [Handbuch zur Problem](https://code.visualstudio.com/docs/remote/troubleshooting#_fixing-problems-with-the-code-command-not-working) Behandlung enthält Tipps zum Ändern von Pfad Variablen, zum Beheben von Erweiterungs Fehlern bei fehlenden Abhängigkeiten, zum Beheben von Problemen beim Beenden von git-Zeilen, zum Installieren einer lokalen VSIX auf einem Remote Computer, zum Starten eines Browserfensters, zum Blockieren des localhost-Diensts, zu nicht funktionierenden websockets, zum Speichern von Erweiterungs Daten

## <a name="install-git-optional"></a>Installieren von Git (optional)

Wenn du beabsichtigst, zusammen mit anderen zusammenzuarbeiten oder das Projekt an einem Open-Source-Standort (wie GitHub) zu hosten, unterstützt VS Code die [Versionskontrolle mit Git](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support). Auf der Registerkarte „Quellcodeverwaltung“ in VS Code werden alle Änderungen nachverfolgt und gängige Git-Befehle („Add“, „Commit“, „Push“, „Pull“) direkt in die Benutzeroberfläche integriert.

Informationen zur Installation von git finden Sie unter [Einrichten von git für die Arbeit mit dem Windows-Subsystem für Linux](./wsl-git.md).

## <a name="install-windows-terminal-optional"></a>Installieren von Windows-Terminal (optional)

Das neue Windows-Terminal ermöglicht mehrere Registerkarten (schnelles Umschalten zwischen Eingabeaufforderung, PowerShell oder mehreren Linux-Verteilungen), benutzerdefinierte Tastenbindungen (erstellen Sie eigene Tastenkombinationen zum Öffnen oder Schließen von Registerkarten, kopieren und Einfügen usw.), Emojis-☺ und benutzerdefinierte Designs (Farbschemas, Schriftarten und Größen, Hintergrundbild/weich/Transparenz). Weitere Informationen finden Sie in der [Windows-Terminal](/windows/terminal)Dokumentation.

1. Hole dir [Windows-Terminal im Microsoft Store](https://www.microsoft.com/store/apps/9n0dx20hk701): Durch die Installation über den Store werden Updates automatisch durchgeführt.

2. Öffne nach der Installation das Windows-Terminal, und wähle **Einstellungen** aus, um dein Terminal mithilfe der Datei `profile.json` anzupassen.

## <a name="additional-resources"></a>Weitere Ressourcen

* [VS Code Remote Entwicklung](https://code.visualstudio.com/docs/remote/remote-overview)
* [Tipps und Tricks zur Remote Entwicklung](https://code.visualstudio.com/docs/remote/troubleshooting)
* [Tutorial zur Remote Entwicklung mit WSL](https://code.visualstudio.com/remote-tutorials/wsl/getting-started)
* [Verwenden von Docker mit WSL 2 und vs Code](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
* [Verwenden von C++ und WSL in vs Code](https://code.visualstudio.com/docs/cpp/config-wsl)
* [Remote R Service für Linux](/visualstudio/rtvs/setting-up-remote-r-service-on-linux)

Folgende zusätzliche Erweiterungen solltest du ebenfalls in Erwägung ziehen:

* [Tastaturlayouts anderer Editoren:](https://marketplace.visualstudio.com/search?target=VSCode&category=Keymaps&sortBy=Downloads) Durch diese Erweiterungen wird die Arbeit in deiner Umgebung vereinfacht, wenn du von einem anderen Text-Editor umsteigst (z. B. Atom, Sublime, Vim, emacs, Notepad++ usw.).
* [Einstellungssynchronisierung:](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync) Damit kannst du die VS Code-Einstellungen in verschiedenen Installationen über GitHub synchronisieren. Wenn Sie auf verschiedenen Computern arbeiten, können Sie die Umgebung auf diese Weise konsistent halten.
* [Debugger für Chrome](https://code.visualstudio.com/blogs/2016/02/23/introducing-chrome-debugger-for-vs-code): Nachdem Sie die Entwicklung auf dem Server mit Linux abgeschlossen haben, müssen Sie die Clientseite entwickeln und testen. Diese Erweiterung integriert deinen VS Code-Editor mit dem Debugdienst deines Chrome-Browsers, sodass du effizienter arbeiten kannst.
