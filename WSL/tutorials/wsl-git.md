---
title: Einstieg in die Verwendung von git unter Windows-Subsystem für Linux
description: Erfahren Sie, wie Sie git für die Versionskontrolle im Windows-Subsystem für Linux einrichten.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, git, GitHub, Versionskontrolle
ms.date: 06/04/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 2d05e83d4c87b1b03028856bcec9d5205205535a
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413351"
---
# <a name="get-started-using-git-on-windows-subsystem-for-linux"></a>Einstieg in die Verwendung von git unter Windows-Subsystem für Linux

Git ist das am häufigsten verwendete Versionskontrollsystem. Mit git können Sie Änderungen nachverfolgen, die Sie an Dateien vornehmen, sodass Sie einen Datensatz darüber haben, was geschehen ist, und die Möglichkeit haben, bei Bedarf auf frühere Versionen der Dateien zurückzugreifen. Git erleichtert auch die Zusammenarbeit, sodass Änderungen durch mehrere Personen in einer einzigen Quelle zusammengeführt werden können.

## <a name="git-can-be-installed-on-windows-and-on-wsl"></a>Git kann unter Windows und auf WSL installiert werden.

Ein wichtiger Aspekt: Wenn Sie WSL aktivieren und eine Linux-Distribution installieren, installieren Sie ein neues Dateisystem, das von Windows NTFS C:\ getrennt ist. Laufwerk auf Ihrem Computer. Unter Linux werden Laufwerke nicht als Buchstaben angegeben. Ihnen werden Einstellungspunkte zugewiesen. Der Stamm des Dateisystems `/` ist der Bereitstellungs Punkt der Stamm Partition (oder des Ordners) im Fall von WSL. Nicht alles unter `/` ist dasselbe Laufwerk. Auf meinem Laptop habe ich beispielsweise zwei Versionen von Ubuntu (20,04 und 18,04) sowie Debian installiert. Wenn Sie diese Verteilungen öffnen, wählen Sie das Stammverzeichnis mit dem Befehl aus `cd ~` , und geben Sie dann den Befehl ein `explorer.exe .` . der Windows-Datei-Explorer wird geöffnet und zeigt den Verzeichnispfad für die Verteilung an.

| Linux-Distribution | Windows-Pfad für den Zugriff auf den Basisordner |
| ----------- | ----------- |
| Ubuntu 20.04 | `\\wsl$\Ubuntu-20.04\home\username` |
| Ubuntu 18.04 | `\\wsl$\Ubuntu-18.04\home\username` |
| Debian | `\\wsl$\Debian\home\username` |
| Windows PowerShell | `C:\Users\username` |

> [!TIP]
> Wenn Sie von der WSL-Verteilungs Befehlszeile aus auf das Windows-Datei Verzeichnis zugreifen möchten, erfolgt der Zugriff auf `C:\Users\username` das Verzeichnis mithilfe von `/mnt/c/Users/username` , da die Linux-Distribution Ihr Windows-Dateisystem als ein bereitgestelltes Laufwerk ansieht.

Sie müssen git auf jedem Dateisystem installieren, mit dem Sie es verwenden möchten.

![Anzeige von git-Versionen nach Distribution](../media/git-versions.gif)

## <a name="installing-git"></a>Installieren von Git

Git ist bereits mit dem größten Teil des Windows-Subsystems für Linux-Distributionen installiert, Sie möchten jedoch möglicherweise auf die neueste Version aktualisieren. Außerdem müssen Sie Ihre git-Konfigurationsdatei einrichten.

Informationen zur Installation von git finden Sie auf der Website zum [git-Download für Linux](https://git-scm.com/download/linux) . Jede Linux-Distribution verfügt über einen eigenen Paket-Manager und Installations Befehl.

Geben Sie für die neueste stabile git-Version in Ubuntu/Debian den folgenden Befehl ein:

```bash
sudo apt-get install git
```

> [!NOTE]
> Möglicherweise möchten Sie auch [git für Windows installieren](https://git-scm.com/download/win) , falls Sie dies noch nicht getan haben.

## <a name="git-config-file-setup"></a>Setup der git-Konfigurationsdatei

Öffnen Sie zum Einrichten der git-Konfigurationsdatei eine Befehlszeile für die Distribution, in der Sie arbeiten, und legen Sie Ihren Namen mit diesem Befehl fest (ersetzen Sie "Your Name" durch ihren git-Benutzernamen):

```bash
git config --global user.name "Your Name"
```

Legen Sie Ihre e-Mail mit diesem Befehl fest (ersetzen youremail@domain.com Sie "" durch die e-Mail, die Sie in Ihrem git-Konto verwenden):

```bash
git config --global user.email "youremail@domain.com"
```

> [!TIP]
> Wenn du noch kein Git-Konto hast, kannst du [dich bei GitHub registrieren](https://github.com/join). Wenn Sie noch nie zuvor mit Git gearbeitet haben, können Sie [GitHub-Leitfäden](https://guides.github.com/) für den Einstieg nutzen. Wenn du die Git-Konfiguration bearbeiten möchtest, kannst du dafür einen integrierten Text-Editor wie nano verwenden: `nano ~/.gitconfig`.

Es wird empfohlen, dass Sie [Ihr Konto mit zweistufiger Authentifizierung (2FA) sichern](https://help.github.com/en/github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa).

## <a name="git-credential-manager-setup"></a>Setup für git Credential Manager

Git Credential Manager ermöglicht Ihnen das Authentifizieren eines Remote-git-Servers, auch wenn Sie über ein komplexes Authentifizierungs Muster wie zweistufige Authentifizierung, Azure Active Directory oder über SSH-Remote-URLs verfügen, die für jeden git-Push ein SSH-Schlüssel Kennwort erfordern. Die Git-Anmeldeinformationsverwaltung kann in den Authentifizierungsablauf für Dienste wie GitHub integriert werden, und sobald Sie bei Ihrem Hostinganbieter authentifiziert sind, fordert sie ein neues Authentifizierungstoken an. Anschließend wird das Token sicher in der Windows-Anmelde Informations [Verwaltung](https://support.microsoft.com/help/4026814/windows-accessing-credential-manager)gespeichert. Nach dem ersten Mal können Sie Git verwenden, um mit Ihrem Hostinganbieter zu kommunizieren, ohne sich erneut authentifizieren zu müssen. Er greift einfach auf das Token in Windows-Anmeldeinformationsverwaltung zu.

Zum Einrichten der Git-Anmeldeinformationsverwaltung für die Verwendung mit einer WSL-Distribution öffnen Sie die Distribution, und geben Sie den folgenden Befehl ein:

```Bash
git config --global credential.helper "/mnt/c/Program\ Files/Git/mingw64/libexec/git-core/git-credential-manager.exe"
```

Nun wird für jeden Git-Vorgang, den Sie in der WSL-Distribution ausführen, die Anmeldeinformationsverwaltung verwendet. Wenn Sie bereits Anmeldeinformationen für einen Host zwischengespeichert haben, greifen Sie über die Anmeldeinformationsverwaltung auf diese zu. Andernfalls erhalten Sie eine Dialogfeldantwort, in der Ihre Anmeldeinformationen angefordert werden, auch wenn Sie sich in einer Linux-Konsole befinden.

> [!NOTE]
> Wenn Sie einen GPG-Schlüssel für die Code Signatur Sicherheit verwenden, müssen Sie [ggf. ihren GPG-Schlüssel Ihrer GitHub-e-Mail zuordnen](https://help.github.com/en/github/authenticating-to-github/associating-an-email-with-your-gpg-key).

## <a name="adding-a-git-ignore-file"></a>Hinzufügen einer git-Datei zum ignorieren

Es wird empfohlen, Ihren Projekten eine [gitignore-Datei](https://help.github.com/en/articles/ignoring-files) hinzuzufügen. GitHub bietet [eine Sammlung nützlicher gitignore-Vorlagen](https://github.com/github/gitignore) mit empfohlenen gitignore-Datei Setups, die entsprechend Ihrem Anwendungsfall organisiert sind. Hier finden Sie beispielsweise [die gitignore-Standardvorlage von GitHub für ein Node.js Projekt](https://github.com/github/gitignore/blob/master/Node.gitignore).

Wenn Sie [ein neues Repository mithilfe der GitHub-Website erstellen](https://help.github.com/articles/create-a-repo), sind Kontrollkästchen verfügbar, mit denen Sie Ihr Repository mit einer Infodatei, einer gitignore-Datei für Ihren spezifischen Projekttyp und den Optionen zum Hinzufügen einer Lizenz bei Bedarf initialisieren können.

## <a name="git-and-vs-code"></a>Git und vs Code

Visual Studio Code verfügt über integrierte Unterstützung für git, einschließlich einer Registerkarte für die Quell Code Verwaltung, auf der Ihre Änderungen angezeigt werden und eine Vielzahl von git-Befehlen für Sie behandelt werden. Erfahren Sie mehr über [die git-Unterstützung von vs Code](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support).

## <a name="git-line-endings"></a>Git-Zeilenenden

Wenn Sie mit dem gleichen Repository-Ordner zwischen Windows, WSL oder einem Container arbeiten, stellen Sie sicher, dass Sie konsistente Zeilenenden einrichten.

Da unter Windows und Linux andere Standardzeilen enden verwendet werden, kann git eine große Anzahl geänderter Dateien melden, die nicht von ihren Zeilenenden abweichen. Um dies zu verhindern, können Sie die Konvertierung von Zeilenenden mithilfe einer `.gitattributes` Datei oder global auf der Windows-Seite deaktivieren. [Informationen zum Beheben von Problemen bei der git-Zeilen Beendigung](https://code.visualstudio.com/docs/remote/troubleshooting#_resolving-git-line-ending-issues-in-containers-resulting-in-many-modified-files)finden Sie in diesem vs Code

## <a name="additional-resources"></a>Zusätzliche Ressourcen

* [WSL-& vs Code](./wsl-vscode.md)
* [GitHub-Lernlabor: Online Kurse](https://lab.github.com/)
* [Git-Visualisierungs Tool](http://git-school.github.io/visualizing-git/)
* [Git-Tools: Speicherung von Anmelde Informationen](https://git-scm.com/book/it/v2/Git-Tools-Credential-Storage)
