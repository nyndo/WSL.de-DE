---
title: 'Windows-Subsystem für Linux: Befehlsreferenz'
description: Zeigen Sie eine Liste von Befehlen an, die das Windows-Subsystem für Linux verwalten, z. B. Argumente für die Ausführung von Linux-Befehlen.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: fc5c9e06c597092a3790ba7f9eb06054a33450c1
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866130"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>Befehlsreferenz für das Windows-Subsystem für Linux

Die beste Möglichkeit, mit dem Windows-Subsystem für Linux zu interagieren, ist die Verwendung des Befehls `wsl.exe`.

## <a name="set-wsl-2-as-your-default-version"></a>Festlegen von WSL 2 als Standardversion

Führen Sie bei der Installation einer neuen Linux-Verteilung den folgenden Befehl in PowerShell aus, um WSL 2 als Standardversion festzulegen:

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a>Festlegen der Verteilungsversion auf WSL 1 oder WSL 2

Sie können die den einzelnen installierten Linux-Verteilungen zugewiesenen WSL-Version überprüfen, indem Sie die PowerShell-Befehlszeile öffnen und den folgenden Befehl (nur verfügbar in [Windows Build 19041 oder höher](ms-settings:windowsupdate)) eingeben: `wsl -l -v`

```bash
wsl --list --verbose
```

Um eine Verteilung so einzurichten, dass sie von einer der beiden WSL-Versionen unterstützt wird, führen Sie Folgendes aus:

```bash
wsl --set-version <distribution name> <versionNumber>
```

Ersetzen Sie hierbei `<distribution name>` durch den tatsächlichen Namen Ihrer Verteilung und `<versionNumber>` durch die Ziffer „1“ oder „2“. Sie können jederzeit zu WSL 1 zurückwechseln, indem sie denselben Befehl wie oben ausführen, aber die 2 durch eine 1 ersetzen.

Wenn Sie WSL 2 als Ihre Standardarchitektur festlegen möchten, ist dies über diesen Befehl möglich:

```bash
wsl --set-default-version 2
```

Dadurch wird die Version jeder neu installierten Verteilung auf WSL 2 festgelegt.

## `wsl.exe`

Unten finden Sie eine Liste mit allen Optionen, wenn Sie `wsl.exe` ab Windows Version 1903 verwenden.

Syntax: `wsl [Argument] [Options...] [CommandLine]`

### <a name="arguments-for-running-linux-commands"></a>Argumente für das Ausführen von Linux-Befehlen

* **Ohne Argumente**

  Wenn keine Befehlszeile angegeben wird, startet „wsl.exe“ die Standardshell.

* **--exec, -e \<CommandLine>**
  
  Führt den angegebenen Befehl ohne Verwendung der Linux-Standardshell aus.

* **--**
  
  Übergibt die verbleibende Befehlszeile unverändert.

Die oben genannten Befehle akzeptieren außerdem die folgenden Optionen:

* **--distribution, -d \<Distro>**

  Führt die angegebene Distribution aus.

* **--user, -u \<UserName>**

  Ausführung als der angegebene Benutzer.

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a>Argumente für die Verwaltung des Windows-Subsystems für Linux

* **--export \<Distro> \<FileName>**
  
  Exportiert die Distribution in eine TAR-Datei. Der Dateiname kann „-“ für Standardausgabe sein.

* **--import \<Distro> \<InstallLocation> \<FileName>**
  
  Importiert die angegebene TAR-Datei als neue Distribution. Der Dateiname kann „-“ für Standardeingabe sein.

* **--list, -l [Optionen]**
  
  Listet Distributionen auf.

  Optionen:
  * **--all**

    Listet alle Distributionen auf, einschließlich Distributionen, die zurzeit installiert oder deinstalliert werden.

  * **--running**

    Listet nur Distributionen auf, die zurzeit ausgeführt werden.

* **--set-default, -s \<Distro>**
  
  Legt die Distribution als Standard fest.

* **--terminate, -t \<Distro>**
  
  Beendet die angegebene Distribution.

* **--unregister \<Distro>**
  
  Hebt die Registrierung der Verteilung auf.

* **--help**: Zeigt Syntaxinformationen an.

## <a name="additional-commands"></a>Weitere Befehle

Es gibt auch historische Befehle für die Interaktion mit dem Windows-Subsystem für Linux. Ihre Funktionalität ist in `wsl.exe` enthalten, sie sind jedoch weiterhin zur Verwendung verfügbar.

### `wslconfig.exe`

Mit diesem Befehl können Sie Ihre WSL-Distribution konfigurieren. Es folgt eine Liste der zugehörigen Optionen.

Syntax: `wslconfig [Argument] [Options...]`

#### <a name="arguments"></a>Argumente

* **/l, /list [Optionen]**
  
  Listet registrierte Distributionen auf.
  
Optionen:

* **/all** Listet optional alle Verteilungen auf, einschließlich Verteilungen, die zurzeit installiert oder deinstalliert werden.

* **/running** Listet nur Verteilungen auf, die zurzeit ausgeführt werden.

* **/s, /setdefault \<Distro>** : Legtdie Distribution als Standard fest.

* **/t, /terminate \<Distro>** : Beendet die Distribution.

* **/u, /unregister \<Distro>** : Hebt die Registrierung der Distribution auf.

* **/upgrade \<Distro>** : Führt ein Upgrade der Distribution auf das WslFs-Dateisystemformat durch.

### `bash.exe`

Dieser Befehl wird verwendet, um eine Bash-Shell zu starten. Unten finden Sie die Optionen, die Sie mit diesem Befehl verwenden können.

Syntax: `bash [Options...]`

* **Keine Option angegeben**
  
  Startet die Bash-Shell im aktuellen Verzeichnis. Wenn die Bash-Shell nicht installiert ist, wird automatisch `lxrun /install` ausgeführt.

* **~**
  
  `bash ~` startet die Bash-Shell im Basisverzeichnis des Benutzers.  Vergleichbar mit der Ausführung von `cd ~`.

* **-c "\<command>"**
  
  Führt den Befehl aus, gibt die Ausgabe aus, und kehrt zur Windows-Eingabeaufforderung zurück.

  Beispiel: `bash -c "ls"`.

## <a name="deprecated-commands"></a>Veraltete Befehle

`lxrun.exe` war der erste Befehl, der zum Installieren und Verwalten des Windows-Subsystems für Linux verwendet wurde. Er gilt ab Windows 10 Version 1803 und höher als veraltet.

Der Befehl `lxrun.exe` kann verwendet werden, um direkt mit dem [Windows-Subsystem für Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) zu interagieren.  Diese Befehle werden im Verzeichnis `\Windows\System32` installiert und können in einer Windows-Eingabeaufforderung oder in PowerShell ausgeführt werden.

| Befehl                     | Beschreibung                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Der lxrun-Befehl wird verwendet, um die WSL-Instanz zu verwalten. |
| `lxrun /install`            | Startet den Download- und Installationsvorgang. <br/> **/y** kann hinzugefügt werden, um alle Eingabeaufforderungen zu umgehen.  Die Bestätigungsaufforderung wird automatisch akzeptiert, und der Standardbenutzer wird auf „root“ festgelegt.          |
| `lxrun /uninstall`          | Deinstalliert und löscht das Ubuntu-Image.  Standardmäßig wird hierdurch nicht das Ubuntu-Basisverzeichnis des Benutzers entfernt. <br/> **/y** kann hinzugefügt werden, um die Bestätigungsaufforderung automatisch zu akzeptieren. <br/>**/full** deinstalliert und löscht das Ubuntu-Basisverzeichnis des Benutzers.         |
| `lxrun /setdefaultuser <userName>`     | Legt die Standard-Bash für den Ubuntu-Benutzer fest. Fordert zur Eingabe eines Kennworts auf, wenn der angegebene Benutzer nicht vorhanden ist.  Weitere Informationen finden Sie unter https://aka.ms/wslusers. <br/> **/y** umgeht die Eingabeaufforderung für das Kennwort.  Der Benutzer wird ohne Kennwort erstellt.|
| `lxrun /update`            | Aktualisiert den Paketindex des Subsystems.          |
