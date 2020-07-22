---
title: Erstellen und Aktualisieren von Benutzerkonten für Linux-Distributionen
description: Referenz für Benutzerkonten und Berechtigungsverwaltung mit dem Windows-Subsystem für Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, user accounts
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 551cc66b1648a66717163d1d8e19a78d28bff342
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235912"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a>Erstellen eines Benutzerkontos und Kennworts für Ihre neue Linux-Distribution

Nachdem Sie [WSL aktiviert und eine Linux-Distribution aus dem Microsoft Store installiert](./install-win10.md) haben, werden Sie beim Öffnen Ihrer neu installierten Linux-Distribution zunächst aufgefordert, ein Konto zu erstellen, einschließlich **Benutzername** und **Kennwort**.

- Diese Kombination aus **Benutzername** und **Kennwort** ist spezifisch für Ihre Linux-Distribution und hat keinen Einfluss auf Ihren Windows-Benutzernamen.

- Nachdem Sie den **Benutzernamen** und das **Kennwort** erstellt haben, ist das Konto Ihr Standardbenutzer für die Distribution und wird beim Start automatisch angemeldet.

- Dieses Konto wird als Linux-Administrator angesehen, mit der Möglichkeit, administrative `sudo` (Super User Do)-Befehle auszuführen.

- Jede Linux-Distribution, die unter dem Windows-Subsystem für Linux ausgeführt wird, verfügt über eigene Linux-Benutzerkonten und -Kennwörter.  Jedes Mail, wenn Sie eine Distribution hinzufügen, erneut installieren oder zurücksetzen, müssen Sie ein Linux-Benutzerkonto konfigurieren.

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a>Update- und Upgradepakete

Die meisten Distributionen werden mit einem leeren oder minimalen Paketkatalog ausgeliefert. Es wird dringend empfohlen, den Paketkatalog regelmäßig zu aktualisieren und ein Upgrade der installierten Pakete mit dem bevorzugten Paket-Manager Ihrer Distribution auszuführen. Für Debian/Ubuntu verwenden Sie apt:

```bash
sudo apt update && sudo apt upgrade
```

Windows führt für Ihre Linux-Distribution(en) nicht automatisch eine Aktualisierung oder ein Upgrade aus. Dies ist eine Aufgabe, die die meisten Linux-Benutzer lieber selbst in die Hand nehmen.

## <a name="reset-your-linux-password"></a>Zurücksetzen Ihres Linux-Kennworts

Um Ihr Kennwort zu ändern, öffnen Sie Ihre Linux-Distribution (z. B. Ubuntu), und geben Sie den Befehl `passwd` ein.

Sie werden aufgefordert, Ihr aktuelles Kennwort und Ihr neues Kennwort einzugeben und anschließend Ihr neues Kennwort zu bestätigen.

## <a name="forgot-your-password"></a>Haben Sie Ihr Kennwort vergessen?

Wenn Sie das Kennwort für Ihre Linux-Distribution vergessen haben:

1. Öffnen Sie PowerShell, und geben Sie mit dem Befehl `wsl -u root` das Stammverzeichnis Ihrer Standard-WSL-Distribution ein.

    > Wenn Sie das vergessene Kennwort für eine Distribution aktualisieren müssen, die nicht Ihre StandardDistribution ist, verwenden Sie den Befehl `wsl -d Debian -u root`, wobei Sie `Debian` durch den Namen Ihrer ZielDistribution ersetzen.

2. Sobald Ihre WSL-Distribution auf der Root-Ebene innerhalb von PowerShell geöffnet wurde, können Sie den Befehl `passwd` verwenden, um Ihr Kennwort zu aktualisieren.

3. Sie werden aufgefordert, ein neues UNIX-Kennwort einzugeben und dieses Kennwort anschließend zu bestätigen. Sobald Ihnen mitgeteilt wird, dass das Kennwort erfolgreich aktualisiert wurde, schließen Sie WSL in PowerShell mithilfe des Befehls `exit`.

> [!NOTE]
> Wenn Sie eine frühe Version des Windows-Betriebssystems ausführen, wie z. B. 1703 (Creators Update) oder 1709 (Fall Creators Update), finden Sie weitere Informationen in der [Dokumentation zur archivierten Version dieses Benutzerkontoupdates](./user-support-archived.md).
