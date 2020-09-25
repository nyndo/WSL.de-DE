---
title: Erstellen und Aktualisieren von Benutzerkonten für Linux-Verteilungen
description: Referenz für Benutzerkonten und Berechtigungsverwaltung mit dem Windows-Subsystem für Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, user accounts
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7f1ad56a6f4261ad0455ee93bdeb5e31d0ed10d1
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818722"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>Erstellen eines Benutzerkontos und Kennworts für Ihre neue Linux-Verteilung

Nachdem Sie [WSL aktiviert und eine Linux-Verteilung aus dem Microsoft Store installiert](./install-win10.md) haben, werden Sie beim Öffnen Ihrer neu installierten Linux-Verteilung zunächst aufgefordert, ein Konto zu erstellen, einschließlich **Benutzername** und **Kennwort**.

- Diese Kombination aus **Benutzername** und **Kennwort** ist spezifisch für jede einzelne Linux-Verteilung, die Sie installieren, und hat keinen Einfluss auf Ihren Windows-Benutzernamen.

- Nachdem Sie einen **Benutzernamen** und das **Kennwort** erstellt haben, ist das Konto Ihr Standardbenutzer für die Verteilung und wird beim Start automatisch angemeldet.

- Dieses Konto wird als Linux-Administrator angesehen, mit der Möglichkeit, administrative `sudo` (Super User Do)-Befehle auszuführen.

- Jede Linux-Distribution, die unter dem Windows-Subsystem für Linux ausgeführt wird, verfügt über eigene Linux-Benutzerkonten und -Kennwörter.  Jedes Mail, wenn Sie eine Verteilung hinzufügen, erneut installieren oder zurücksetzen, müssen Sie ein Linux-Benutzerkonto konfigurieren.

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>Update- und Upgradepakete

Die meisten Verteilungen werden mit einem leeren oder minimalen Paketkatalog ausgeliefert. Es wird dringend empfohlen, den Paketkatalog regelmäßig zu aktualisieren und ein Upgrade der installierten Pakete mit dem bevorzugten Paket-Manager Ihrer Verteilung auszuführen. Für Debian/Ubuntu verwenden Sie apt:

```bash
sudo apt update && sudo apt upgrade
```

Windows führt für Ihre Linux-Verteilung(en) nicht automatisch eine Aktualisierung oder ein Upgrade aus. Dies ist eine Aufgabe, die die meisten Linux-Benutzer lieber selbst in die Hand nehmen.

## <a name="reset-your-linux-password"></a>Zurücksetzen Ihres Linux-Kennworts

Um Ihr Kennwort zu ändern, öffnen Sie Ihre Linux-Verteilung (z. B. Ubuntu), und geben Sie den Befehl `passwd` ein.

Sie werden aufgefordert, Ihr aktuelles Kennwort und Ihr neues Kennwort einzugeben und anschließend Ihr neues Kennwort zu bestätigen.

## <a name="forgot-your-password"></a>Haben Sie Ihr Kennwort vergessen?

Wenn Sie das Kennwort für Ihre Linux-Verteilung vergessen haben:

1. Öffnen Sie PowerShell, und geben Sie mit dem Befehl `wsl -u root` das Stammverzeichnis Ihrer Standard-WSL-Verteilung ein.

    > Wenn Sie das vergessene Kennwort für eine Verteilung aktualisieren müssen, die nicht Ihre Standardverteilung ist, verwenden Sie den Befehl `wsl -d Debian -u root`, wobei Sie `Debian` durch den Namen Ihrer Zielverteilung ersetzen.

2. Sobald Ihre WSL-Verteilung auf der Root-Ebene innerhalb von PowerShell geöffnet wurde, können Sie den Befehl `passwd <WSLUsername>` verwenden, um Ihr Kennwort zu aktualisieren, wobei `<WSLUsername>` der Benutzername des Kontos in der Distribution ist, dessen Kennwort Sie vergessen haben.

3. Sie werden aufgefordert, ein neues UNIX-Kennwort einzugeben und dieses Kennwort anschließend zu bestätigen. Sobald Ihnen mitgeteilt wird, dass das Kennwort erfolgreich aktualisiert wurde, schließen Sie WSL in PowerShell mithilfe des Befehls `exit`.

> [!NOTE]
> Wenn Sie eine frühe Version des Windows-Betriebssystems ausführen, wie z. B. 1703 (Creators Update) oder 1709 (Fall Creators Update), finden Sie weitere Informationen in der [Dokumentation zur archivierten Version dieses Benutzerkontoupdates](./user-support-archived.md).
