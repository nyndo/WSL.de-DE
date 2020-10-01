---
title: Manuelles Herunterladen von WSL-Distributionen (Windows-Subsystem für Linux)
description: Anweisungen zum manuellen Herunterladen von Distributionen des Windows-Subsystems für Linux.
keywords: WSL, Windows-Subsystem für Linux, manuelle Installation, manuell installieren, Microsoft Store, Windows 10s, curl, Add-AppxPackage, Langzeitwartung, LTSC
ms.date: 09/15/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 1894f0bfcb9ede7b05870c99912f30f6d0b7286e
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413250"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>Manuelles Herunterladen von Distributionspaketen des Windows-Subsystems für Linux

Es gibt eine Reihe von Szenarien, in denen Sie möglicherweise nicht in der Lage sind, Distributionen von WSL Linux über den Microsoft Store zu installieren, oder dies nicht wünschen. Insbesondere kann dies eintreten, wenn Sie eine SKU von Windows Server oder eines LTSC-Desktopbetriebssystems (Long-Term Servicing) ausführen, die den Microsoft Store nicht unterstützt, oder die Netzwerkrichtlinien Ihres Unternehmens und/oder die Administratoren die Nutzung des Microsoft Stores in Ihrer Umgebung nicht erlauben.

Wie können Sie in diesen Fällen, wenn das eigentliche WSL verfügbar ist, Linux-Distributionen herunterladen und in WSL installieren, wenn Sie nicht auf den Store zugreifen können?

> Hinweis: **Befehlszeilenshellumgebungen, einschließlich Cmd, PowerShell und Linux/WSL-Distributionen, dürfen im Windows 10 S-Modus nicht ausgeführt werden**. Diese Einschränkung wurde implementiert, um die Integritäts- und Sicherheitsziele des S-Modus sicherzustellen: Weitere Informationen finden Sie in [diesem Beitrag](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/).

## <a name="downloading-distros"></a>Herunterladen von Distributionen

Wenn die Microsoft Store-App nicht verfügbar ist, können Sie Linux-Distributionen manuell herunterladen und installieren, indem Sie auf die folgenden Links klicken:
* [Ubuntu 20.04](https://aka.ms/wslubuntu2004)
* [Ubuntu 20.04 ARM](https://aka.ms/wslubuntu2004arm)
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [Fedora Remix for WSL](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

Dies bewirkt den Download der `<distro>.appx`-Pakete in einen Ordner Ihrer Wahl. Befolgen Sie die [Installationsanweisungen](#installing-your-distro), um die heruntergeladenen Distributionen zu installieren.

## <a name="downloading-distros-via-the-command-line"></a>Herunterladen von Distributionen über die Befehlszeile
Wenn Sie möchten, können Sie Ihre bevorzugten Distributionen auch über die Befehlszeile herunterladen:

 ### <a name="download-using-powershell"></a>Herunterladen mithilfe von PowerShell
 Zum Herunterladen von Distributionen mithilfe von PowerShell verwenden Sie das [Invoke-WebRequest](/powershell/module/microsoft.powershell.utility/invoke-webrequest)-Cmdlet. Hier sehen Sie eine Beispielanweisung zum Herunterladen von Ubuntu 16.04.

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> Wenn der Download sehr lange dauert, deaktivieren Sie die Statusanzeige, indem Sie `$ProgressPreference = 'SilentlyContinue'` festlegen.

### <a name="download-using-curl"></a>Herunterladen mit curl
Das Windows 10-Update aus Frühjahr 2018 (oder höher) umfasst das beliebte [curl-Befehlszeilenhilfsprogramm](https://curl.haxx.se/), mit dem Sie Webanforderungen (d. h. Befehle der Art HTTP GET, POST, PUT usw.) von der Befehlszeile aus aufrufen können. Mit `curl.exe` können Sie die oben genannten Distributionen herunterladen:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

Im Beispiel oben wird `curl.exe` ausgeführt (nicht einfach `curl`), um sicherzustellen, dass in PowerShell die echte curl-Programmdatei aufgerufen wird, nicht der curl-Alias von PowerShell für [Invoke-WebRequest](/powershell/module/microsoft.powershell.utility/invoke-webrequest)

> Hinweis: Die Verwendung von `curl` kann Vorteile bieten, wenn Sie mithilfe der Cmd-Shell und/oder `.bat` / `.cmd` Schritte zum Herunterladen aufrufen/skripten müssen.

## <a name="installing-your-distro"></a>Installieren der Distribution
Wenn Sie Windows 10 verwenden, können Sie Ihre Distribution mit PowerShell installieren. Navigieren Sie einfach zu dem Ordner, der die oben heruntergeladene Distribution enthält, und führen Sie in diesem Verzeichnis den folgenden Befehl aus, wobei `app_name` für den Namen der APPX-Datei Ihrer Distribution steht.  
```Powershell
Add-AppxPackage .\app_name.appx
```

Wenn Sie Windows Server verwenden, finden Sie die Installationsanweisungen auf der [Windows Server](install-on-server.md)-Dokumentationsseite.

Sobald Ihre Verteilung installiert wurde, folgen Sie den normalen Anweisungen, um [auf WSL 2 zu aktualisieren](./install-win10.md#step-2---update-to-wsl-2) oder [ein neues Benutzerkonto und Kennwort zu erstellen](./user-support.md).