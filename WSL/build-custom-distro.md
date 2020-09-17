---
title: Erstellen einer benutzerdefinierten Linux-Distribution für WSL
description: Erfahren Sie, wie Sie eine benutzerdefinierte Linux-Distribution für das Windows-Subsystem für Linux erstellen.
keywords: Bashonwindows, bash, WSL, Windows, Windows Subsystem, Distribution, Custom
ms.date: 09/15/2020
ms.topic: article
ms.openlocfilehash: 8b898cbee12aaff6e575afbeaa57d52c3a2c9e75
ms.sourcegitcommit: ba3399a5ffeffd23551315acd04ea6848d30693b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "90719149"
---
# <a name="creating-a-custom-linux-distribution-for-wsl"></a>Erstellen einer benutzerdefinierten Linux-Distribution für WSL

Verwenden Sie das Open Source-WSL-Beispiel, um WSL-Distributionen für das Microsoft Store zu erstellen und/oder um benutzerdefinierte Linux-Distribution-Pakete für das Sideloading zu erstellen. Das Repository für [Distribution](https://github.com/Microsoft/WSL-DistroLauncher) -Start Programm finden Sie auf GitHub.

Dieses Projekt aktiviert Folgendes:

- Linux-Verteilungs-Maintainer zum Verpacken und Übermitteln einer Linux-Distribution als AppX, die auf WSL ausgeführt wird
- Entwickler zum Erstellen von benutzerdefinierten Linux-Distributionen, die auf ihren Entwicklungs Computer quer geladen werden können

## <a name="background"></a>Hintergrund

Wir verteilen Linux-Distributionen für WSL als UWP-Anwendungen über die Microsoft Store. Sie können diese Anwendungen installieren, die dann auf WSL ausgeführt werden: das Subsystem, das sich im Windows-Kernel befindet. Dieser Übermittlungs Mechanismus hat viele Vorteile, wie in einem [früheren Blogbeitrag](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)erläutert.

## <a name="sideloading-a-custom-linux-distro-package"></a>Querladen eines benutzerdefinierten Linux-Distribution-Pakets

Sie können ein benutzerdefiniertes Linux-Distributionspaket als Anwendung zum querladen auf Ihren persönlichen Computer erstellen. Beachten Sie, dass das benutzerdefinierte Paket nicht über das Microsoft Store verteilt wird, es sei denn, Sie übermitteln als Verteilungs Maintainer.
Wenn Sie Ihren Computer zum querladen von apps einrichten möchten, müssen Sie diesen in den Systemeinstellungen unter "für Entwickler" aktivieren.  Stellen Sie sicher, dass Sie entweder den Entwicklermodus oder querladen von apps ausgewählt haben.

## <a name="for-linux-distro-maintainers"></a>Für Linux-Distribution-Betreuer

Um die Veröffentlichung an den Store zu übermitteln, müssen Sie mit uns zusammenarbeiten, um die Genehmigung der Veröffentlichung zu erhalten. Wenn Sie ein Linux-Verteilungs Besitzer sind, der ihre Verteilung zum Microsoft Store hinzufügen möchte, wenden Sie sich bitte an wslpartners@microsoft.com .

## <a name="getting-started"></a>Erste Schritte

Befolgen Sie die Anweisungen im [GitHub](https://github.com/Microsoft/WSL-DistroLauncher) -Repository "Distribution-Start Programm", um ein benutzerdefiniertes Linux-Distributionspaket zu erstellen.

## <a name="team-blogs"></a>Teamblogs

-  [Open Sourcing a WSL Sample for Linux Distribution Maintainer und Sideloading Custom Linux Distributionen](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
- [Befehlszeilenblog](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>Feedback geben

- [GitHub-Repository für Distribution-Start Programm](https://github.com/Microsoft/WSL-DistroLauncher)
- [GitHub Issue Tracker für WSL](https://github.com/Microsoft/BashOnWindows/issues)
- [UserVoice-Befehlszeilenportal](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
