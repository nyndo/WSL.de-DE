---
title: Einstieg in die Verwendung von Docker-Containern mit dem Windows-Subsystem für Linux
description: Erfahren Sie, wie Sie docker-Container im Windows-Subsystem für Linux einrichten.
keywords: WSL, Windows, windowssubsystem, Windows 10, Docker, Container
ms.date: 08/28/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: a972cd6f179059e0841e1aef4bc3929fa46fcc4d
ms.sourcegitcommit: 1c7f2e9928672ad3941a9327162595cb73ef5a3f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "89609670"
---
# <a name="get-started-with-docker-remote-containers-on-wsl-2"></a>Einstieg in docker-Remote Container auf WSL 2

Diese Schritt-für-Schritt-Anleitung hilft Ihnen beim Einstieg in die Entwicklung mit Remote Containern, indem Sie **docker Desktop für Windows mit WSL 2** (Windows-Subsystem für Linux, Version 2) einrichten.

Docker Desktop für Windows ist kostenlos verfügbar und bietet eine Entwicklungsumgebung für das entwickeln, versenden und Ausführen von apps in einer App. Durch Aktivieren des WSL 2-basierten Moduls können Sie Linux-und Windows-Container in docker Desktop auf demselben Computer ausführen.

## <a name="overview-of-docker-containers"></a>Übersicht über Docker-Container

Docker ist ein Tool zum Erstellen, Bereitstellen und Ausführen von Anwendungen mithilfe von Containern. Mithilfe von Containern können Entwickler eine App mit allen benötigten Komponenten (Bibliotheken, Frameworks, Abhängigkeiten usw.) packen und alles als ein Paket bereitstellen. Durch die Verwendung eines Containers wird sichergestellt, dass die App unabhängig von angepasstem Einstellungen oder zuvor installierten Bibliotheken auf dem Computer unverändert ausgeführt wird, auch wenn es sich um einen anderen Computer handelt als der zum Schreiben und Testen des App-Codes verwendete. Dadurch können sich Entwickler auf das Schreiben von Code konzentrieren, ohne sich Gedanken über das System machen zu müssen, auf dem der Code ausgeführt wird.

Docker-Container ähneln virtuellen Computern, erstellen aber kein vollständiges virtuelles Betriebssystem. Stattdessen ermöglicht Docker der App die Verwendung desselben Linux-Kernels wie das System, auf dem sie ausgeführt wird. Dadurch benötigt das App-Paket nur noch die nicht auf dem Hostcomputer verfügbaren Komponenten. Dies verringert die Paketgröße und verbessert die Leistung.

Kontinuierliche Verfügbarkeit durch die Verwendung von Docker-Containern mit Tools wie [Kubernetes](https://docs.microsoft.com/azure/aks/) ist ein weiterer Grund für die Beliebtheit von Containern. Dadurch können mehrere Versionen des App-Containers zu unterschiedlichen Zeitpunkten erstellt werden. Anstatt ein gesamtes System für Updates oder Wartungsmaßnahmen offline zu schalten, können alle Container (und die jeweiligen Microservices) ohne Unterbrechung ersetzt werden. Du kannst einen neuen Container mit all deinen Updates vorbereiten, den Container für die Produktion einrichten und erst dann auf den neuen Container verweisen, wenn er bereit ist. Du kannst auch verschiedene Versionen deiner App mithilfe von Containern archivieren und bei Bedarf als Sicherheitsfallback ausführen.

Weitere Informationen finden Sie in der [Einführung in docker-Container](https://docs.microsoft.com/learn/modules/intro-to-docker-containers/) auf Microsoft Learn.

## <a name="prerequisites"></a>Voraussetzungen

- Stellen Sie sicher, dass auf Ihrem Computer Windows 10 ausgeführt wird, [auf Version 2004](ms-settings:windowsupdate), **Build 18362** oder höher aktualisiert wurde.
- [Aktivieren Sie WSL, installieren Sie eine Linux-Distribution, und aktualisieren Sie auf WSL 2](https://docs.microsoft.com/windows/wsl/install-win10).
- [Laden Sie das Linux Kernel Update Package herunter, und installieren Sie](https://docs.microsoft.com/windows/wsl/wsl2-kernel)es.
- [Installieren Sie Visual Studio Code](https://code.visualstudio.com/download) *(optional)*. Dies bietet eine optimale Benutzerfreundlichkeit, einschließlich der Möglichkeit, in einem docker-Remote Container zu programmieren und zu Debuggen und mit Ihrer Linux-Distribution verbunden zu sein.
- [Installieren Sie das Windows-Terminal](https://docs.microsoft.com/windows/terminal/get-started) *(optional)*. Dies bietet die beste Oberfläche, einschließlich der Möglichkeit zum Anpassen und Öffnen mehrerer Terminals auf derselben Oberfläche (einschließlich Ubuntu, Debian, PowerShell, Azure CLI oder der gewünschten Verwendung).
- [Registrieren Sie sich für eine docker-ID bei docker Hub](https://hub.docker.com/signup) *(optional)*.

> [!NOTE]
> WSL kann Verteilungen sowohl im WSL-Version 1-als auch im WSL 2-Modus ausführen. Sie können dies überprüfen, indem Sie PowerShell öffnen und Folgendes eingeben: `wsl -l -v` . Stellen Sie sicher, dass die Verteilung der Verteilung auf WSL 2 festgelegt ist, indem Sie Folgendes eingeben: `wsl --set-version  <distro> 2` . Ersetzen Sie dies `<distro>` durch den Namen der Distribution (z. b. Ubuntu 18,04).
> 
> In WSL Version 1 konnte die Docker-Engine aufgrund grundlegender Unterschiede zwischen Windows und Linux nicht direkt in WSL ausgeführt werden, sodass das docker-Team eine alternative Lösung mithilfe von Hyper-V-VMS und linuxkit entwickelte. Da WSL 2 nun auf einem Linux-Kernel mit vollständiger System aufrufkapazität ausgeführt wird, kann docker vollständig in WSL 2 ausgeführt werden. Dies bedeutet, dass Linux-Container nativ ohne Emulation ausgeführt werden können. Dies führt zu einer besseren Leistung und Interoperabilität zwischen Ihren Windows-und Linux-Tools.

## <a name="install-docker-desktop"></a>Installieren von Docker Desktop

Mit dem WSL 2-Back-End, das in docker Desktop für Windows unterstützt wird, können Sie in einer Linux-basierten Entwicklungsumgebung arbeiten und Linux-basierte Container erstellen, während Sie Visual Studio Code für Code Bearbeitung und-Debuggen verwenden und den Container im Microsoft Edge-Browser unter Windows ausführen.

So installieren Sie docker (nachdem Sie [WSL 2 bereits installiert](https://docs.microsoft.com/windows/wsl/install-win10)haben):

1. Laden Sie [docker Desktop](https://docs.docker.com/docker-for-windows/wsl/#download) herunter, und befolgen Sie die Installationsanweisungen.

2. Starten Sie nach der Installation docker Desktop über das Windows-Startmenü, und wählen Sie dann das docker-Symbol aus dem Menü Ausgeblendete Symbole auf der Taskleiste aus. Klicken Sie mit der rechten Maustaste auf das Symbol, um das docker-Menübefehle anzuzeigen und "Einstellungen" auszuwählen.
    ![Docker Desktop-Dashboard (Symbol)](../media/docker-starting.png)

3. Stellen Sie sicher, dass die Option "WSL 2-basiertes Modul verwenden" in den **Einstellungen**  >  **Allgemein**aktiviert ist.
    ![Allgemeine Einstellungen für docker Desktop](../media/docker-running.png)

4. Wählen Sie eine der installierten WSL 2-Distributionen aus, für die Sie die Docker-Integration aktivieren möchten, indem Sie zu: **Einstellungen**  >  **Ressourcen**  >  **WSL-Integration**wechseln.
    ![Docker-Desktop Ressourcen Einstellungen](../media/docker-dashboard.png)

5. Um zu bestätigen, dass docker installiert wurde, öffnen Sie eine WSL-Distribution (z. b. Ubuntu), und zeigen Sie die Version und die Buildnummer an, indem Sie `docker --version`

6. Testen Sie, ob die Installation ordnungsgemäß funktioniert, indem Sie ein einfaches integriertes docker-Image mit folgenden Aktionen ausführen: `docker run hello-world`

> [!TIP]
> Im folgenden finden Sie einige hilfreiche docker-Befehle, die Sie kennen sollten:
>
> - Auflisten der in der Docker-Befehlszeilenschnittstelle verfügbaren Befehle: `docker`
> - Auflisten von Informationen zu einem bestimmten Befehl: `docker <COMMAND> --help`
> - Auflisten der Docker-Images auf deinem Computer (zu diesem Zeitpunkt nur das Hello-World-Image): `docker image ls --all`
> - Auflisten der Container auf dem Computer mit: `docker container ls --all` oder `docker ps -a` (ohne das Flag "-a Show all" werden nur ausgelaufende Container angezeigt)
> - Auflisten von systemweiten Informationen zur docker-Installation, einschließlich Statistiken und Ressourcen (CPU & Arbeitsspeicher), die Ihnen im WSL 2-Kontext zur Verfügung stehen: `docker info`

## <a name="develop-in-remote-containers-using-vs-code"></a>Entwickeln in Remote Containern mithilfe von vs Code

Zum Einstieg in die Entwicklung von apps mit docker und WSL 2 empfehlen wir die Verwendung von vs Code zusammen mit der Remote-WSL-Erweiterung und der Docker-Erweiterung.

- [Installieren Sie die vs Code Remote-WSL-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl). Diese Erweiterung ermöglicht es Ihnen, Ihr Linux-Projekt, das auf WSL ausgeführt wird, in vs Code zu öffnen (es muss sich nicht um Probleme mit der Problembehandlung, binäre Kompatibilität oder andere außer Betrieb greifende Herausforderungen kümmern).

- [Installieren Sie die vs Code-Remote Container Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers). Diese Erweiterung ermöglicht es Ihnen, Ihren Projektordner oder das Repository in einem Container zu öffnen, indem Sie die Vorteile der vollständigen Featuregruppe Visual Studio Code nutzen, um Ihre Entwicklung innerhalb des Containers zu erledigen.

- [Installieren Sie die vs Code docker-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker). Diese Erweiterung bietet die Funktionalität zum Erstellen, verwalten und Bereitstellen von Anwendungen in Containern aus vs Code. (Sie benötigen die Remote Container Erweiterung, um den Container tatsächlich als Entwicklungsumgebung zu verwenden.)

Verwenden Sie Docker, um einen Entwicklungs Container für ein vorhandenes App-Projekt zu erstellen.

1. In diesem Beispiel verwende ich den Quellcode aus meinem [Hallo Welt Tutorial für Django](https://docs.microsoft.com/windows/python/web-frameworks#hello-world-tutorial-for-django) in der python-Entwicklungsumgebung einrichten der Dokumentation. Sie können diesen Schritt überspringen, wenn Sie Ihren eigenen Projekt Quell Code verwenden möchten. Öffnen Sie zum Herunterladen meiner HelloWorld-Django-Web-App von GitHub ein WSL-Terminal (z. b. Ubuntu), und geben Sie Folgendes ein: `git clone https://github.com/mattwojo/helloworld-django.git`

    > [!NOTE]
    > Speichern Sie Ihren Code immer im gleichen Dateisystem, in dem Sie auch Tools verwenden. Dies führt zu einer schnelleren Datei Zugriffsleistung. In diesem Beispiel verwenden wir eine Linux-Distribution (Ubuntu) und möchten unsere Projektdateien im WSL-Dateisystem speichern `\\wsl\` . Das Speichern von Projektdateien im Windows-Dateisystem würde die Dinge erheblich verlangsamen, wenn Sie Linux-Tools in WSL verwenden, um auf diese Dateien zuzugreifen.

2. Wechseln Sie in Ihrem WSL-Terminal in den Quell Code Ordner für dieses Projekt:

    ```bash
    cd helloworld-django
    ```

3. Öffnen Sie das Projekt in vs Code, das auf dem lokalen WSL-Remote Erweiterungs Server ausgeführt wird, indem Sie Folgendes eingeben:

    ```bash
    code .
    ```

    Vergewissern Sie sich, dass Sie mit ihrer WSL-Linux-Distribution verbunden sind, indem Sie den grünen Remote Indikator in der unteren linken Ecke der vs Code Instanz überprüfen.

    ![WSL-Remote Indikator vs Code](../media/vscode-remote-indicator.png)

4. Geben Sie in der vs Code-befehlspaletten(STRG + UMSCHALT + P) Folgendes ein: **Remote-Container: Ordner öffnen in Container..** . Wenn dieser Befehl bei der Eingabe nicht angezeigt wird, stellen Sie sicher, dass Sie die oben verknüpfte Remote Container Erweiterung installiert haben.

    ![Befehl "Remote Container vs Code"](../media/docker-extension.png)

5. Wählen Sie den Projektordner aus, den Sie containerisieren möchten. In meinem Fall ist dies `\\wsl\Ubuntu-20.04\home\mattwojo\repos\helloworld-django\`

    ![Remote Container Ordner vs Code](../media/docker-extension2.png)

6. Eine Liste mit Container Definitionen wird angezeigt, da noch keine devcontainer-Konfiguration im Projektordner (Repository) vorhanden ist. Die Liste der angezeigten Container Konfigurations Definitionen wird basierend auf dem Projekttyp gefiltert. Für mein Django-Projekt wähle ich python 3 aus.

    ![Konfigurations Definitionen für Remote Container vs Code](../media/docker-extension3.png)

7. Eine neue Instanz von vs Code wird geöffnet, das neue Image wird erstellt, und sobald der Build abgeschlossen ist, wird der Container gestartet. Sie werden feststellen, dass ein neuer `.devcontainer` Ordner mit Container Konfigurationsinformationen in einer `Dockerfile` -und-Datei angezeigt wird `devcontainer.json` .  

    ![VS Code. devcontainer-Ordner](../media/docker-extension4.png)

8. Um zu bestätigen, dass das Projekt weiterhin mit WSL und innerhalb eines Containers verbunden ist, öffnen Sie das vs Code integrierte Terminal (STRG + UMSCHALT + ~). Überprüfen Sie das Betriebssystem, indem Sie Folgendes eingeben: `uname` und die Python-Version mit: `python3 --version` . Sie sehen, dass der uname als "Linux" zurückgekehrt ist, sodass Sie weiterhin mit dem WSL 2-Modul verbunden sind und die python-Versionsnummer auf der Container Konfiguration basiert, die sich möglicherweise von der auf der WSL-Distribution installierten Python-Version unterscheidet.

9. Zum Ausführen und Debuggen der APP innerhalb des Containers mithilfe Visual Studio Code öffnen Sie zunächst das Menü **Ausführen** (STRG + UMSCHALT + D, oder klicken Sie auf die Registerkarte in der linken Menüleiste). Wählen Sie dann **ausführen und Debuggen** aus, um eine Debugkonfiguration auszuwählen, und wählen Sie die Konfiguration aus, die Ihr Projekt am besten aufführt (in diesem Beispiel lautet dies "Django"). Dadurch wird eine `launch.json` Datei im Ordner Ihres `.vscode` Projekts mit Anweisungen zum Ausführen der App erstellt.

    ![VS Code ausführen der Debugkonfiguration](../media/vscode-run-config.png)

10. Wählen Sie in vs Code **Ausführen**  >  **Debuggen starten** aus (oder drücken Sie einfach die Taste **F5** ). Dadurch wird in vs Code ein Terminal geöffnet, und es sollte ein Ergebnis wie folgt angezeigt werden: "Starten des Entwicklungs Servers beim http://127.0.0.1:8000/ Beenden des Servers mit Control-C". Halten Sie die STRG-Taste gedrückt, und wählen Sie die angezeigte Adresse aus, um die app in Ihrem Standard Webbrowser zu öffnen, und sehen Sie, dass Ihr Projekt innerhalb des Containers ausgeführt wird.

    ![VS Code ausführen eines docker-Containers](../media/vscode-running-in-container.png)

Sie haben nun erfolgreich einen remoteentwicklungs-Container mithilfe von Docker Desktop konfiguriert, der vom WSL 2-Back-End betrieben wird, das Sie mit vs Code codieren, erstellen, ausführen, bereitstellen oder Debuggen können.

## <a name="troubleshooting"></a>Problembehandlung

### <a name="wsl-docker-context-deprecated"></a>WSL-docker-Kontext veraltet

Wenn Sie eine frühe technische Vorschau von Docker für WSL verwendet haben, verfügen Sie möglicherweise über einen docker-Kontext mit dem Namen "WSL", der nun veraltet ist und nicht mehr verwendet wird. Sie können mit dem folgenden Befehl überprüfen: `docker context ls` . Sie können diesen "WSL"-Kontext entfernen, um Fehler mit dem Befehl zu vermeiden: `docker context rm wsl` da Sie den Standardkontext sowohl für Windows als auch für WSL2 verwenden möchten.

Mögliche Fehler, die mit diesem veralteten WSL-Kontext auftreten können, sind: `docker wsl open //./pipe/docker_wsl: The system cannot find the file specified.` oder. `error during connect: Get http://%2F%2F.%2Fpipe%2Fdocker_wsl/v1.40/images/json?all=1: open //./pipe/docker_wsl: The system cannot find the file specified.`

Weitere Informationen zu diesem Problem finden [Sie unter Einrichten von Docker in Windows-System für Linux (WSL2) unter Windows 10](https://www.hanselman.com/blog/HowToSetUpDockerWithinWindowsSystemForLinuxWSL2OnWindows10.aspx).

### <a name="trouble-finding-docker-image-storage-folder"></a>Probleme beim Auffinden des docker-Image Speicher Ordners

Docker erstellt zwei Distribution-Ordner zum Speichern von Daten:
- \\WSL $ \docker-Desktop
- \\WSL $ \docker-Desktop-Data

Sie finden diese Ordner durch Öffnen der WSL-Linux-Distribution und eingeben von: `explorer.exe .` , um den Ordner im Windows-Datei-Explorer anzuzeigen. Geben Sie Folgendes ein: `\\wsl\<distro name>\mnt\wsl` Ersetzen Sie `<distro name>` durch den Namen Ihrer Distribution (d.h. Ubuntu-20,04), um diese Ordner anzuzeigen.

Weitere Informationen zum Suchen von Docker-Speicherorten in WSL finden Sie in diesem [Problem im WSL](https://github.com/microsoft/WSL/issues/4176) -Repository oder in diesem [stackoverlow-Beitrag](https://stackoverflow.com/questions/62380124/where-docker-image-is-stored-with-docker-desktop-for-windows).

Weitere Hilfe bei der allgemeinen Problembehandlung in WSL finden Sie im Dokument zur [Problem](../troubleshooting.md) Behandlung.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Docker-Dokumentation: bewährte Methoden für docker Desktop mit WSL 2](https://docs.docker.com/docker-for-windows/wsl/#best-practices)
- [Feedback zu docker Desktop für Windows: Problem melden](https://github.com/docker/for-win/issues)
- [VS Code Blog: Richtlinien für die Auswahl einer Entwicklungsumgebung](https://code.visualstudio.com/docs/containers/choosing-dev-environment#_guidelines-for-choosing-a-development-environment)
- [VS Code Blog: Verwenden von Docker in WSL 2](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)
- [VS Code Blog: Verwenden von Remote Containern in WSL 2](https://code.visualstudio.com/blogs/2020/07/01/containers-wsl)
- [Hanselminutes-Podcast: Erstellen von Docker für Entwickler mit Simon ferquel](https://hanselminutes.com/736/making-docker-lovely-for-developers-with-simon-ferquel)