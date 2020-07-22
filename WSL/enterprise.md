---
title: Windows-Subsystem für Linux für Unternehmen
description: Ressourcen und Anweisungen zur optimalen Verwendung des Windows-Subsystems für Linux in einer Unternehmensumgebung.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Unternehmen, Bereitstellung, offline, Paket, Store, Distribution, Installation, installieren
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 02f4ff41614f78c0e588f329c777a87f8b416233
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235831"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>Einrichten des Windows-Subsystems für Linux für Ihr Unternehmen

Der Microsoft Store für Unternehmen bietet verschiedene Unternehmenslösungen, die WSL in Ihrem Unternehmen bereitstellen möchten. Die [Dokumentation im Microsoft Store für Unternehmen und Bildungseinrichtungen](https://docs.microsoft.com/microsoft-store/) stellt eine gute Ressource für allgemeine Informationen über die Store-Benutzeroberfläche dar.

Als Unternehmen, das nur sein System für die Bereitstellung von WSL einrichten möchte, führen Sie die folgenden Schritte aus:

* [Registrieren für Microsoft Store für Unternehmen und erste Schritte](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business-overview).
* [Verwalten Sie Ihre Produkte und Dienste (einschließlich der Benutzer, die auf die Apps in Ihrem privaten Store zugreifen können)](https://docs.microsoft.com/microsoft-store/manage-apps-microsoft-store-for-business-overview). Hier können Sie Ihrem Store WSL-Distributionen hinzufügen und steuern, wer diese installieren kann.
* [Verwenden einer Distributionsmethode Ihrer Wahl, um die Software in Ihrem Unternehmen bereitzustellen](https://docs.microsoft.com/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Informieren Sie die Mitarbeiter Ihres Unternehmens, dass sie diesen Dokumentationslink zum Installieren von WSL verwenden können: [Installieren des Windows-Subsystems für Linux](./install-win10.md)

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Offlineverteilen einer Linux-Distribution unter Windows

Wenn die Computer in Ihrem Unternehmen keinen Zugriff auf den Microsoft Store oder den Microsoft Store für Unternehmen haben, können Sie das Installationsprogramm einer Linux-Distribution mit einer Offline Lizenz herunterladen, indem Sie die folgenden Schritte ausführen.

### <a name="set-up-an-azure-active-directory-account"></a>Einrichten eines Azure Active Directory-Kontos

Sie müssen sich [für ein Azure AD-Konto registrieren](https://docs.microsoft.com/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) und der globale Administrator für Ihre Organisation sein, um das Installationsprogramm für Microsoft Store-Apps zu erhalten. Wenn Sie bereits ein Konto haben, können Sie diesen Schritt überspringen.

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>Einrichten von WSL mithilfe Ihres Microsoft Store für Unternehmen-Kontos

Die Anweisungen zum Registrieren eines Kontos finden Sie hier: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business

1. Melden Sie sich beim Store für Unternehmen an, und wechseln Sie zur Startseite: https://www.microsoft.com/business-store

    ![Microsoft Store für Unternehmen – Startseite](media/offlineinstallscreens/1-screen.png)

2. Wechseln Sie zu „Verwalten“ > „Einstellungen“, und aktivieren Sie „Offline-Apps anzeigen“.

    ![Seite mit den Einstellungen für den Microsoft Store für Unternehmen](media/offlineinstallscreens/2-screen.png)

3. Wechseln Sie zurück zur Hauptseite, indem Sie „Für meine Gruppe einkaufen“ auswählen.

    ![Microsoft Store für Unternehmen – Startseite](media/offlineinstallscreens/1-screen.png)

4. Suchen Sie nach der gewünschten Distribution, und wählen Sie sie aus.

    ![Microsoft Store für Unternehmen – Startseite mit aktiver Suche](media/offlineinstallscreens/3-screen.png)

5. Wählen Sie im Dropdownmenü „Lizenztyp“ eine Offlinelizenz und dann „App abrufen“ aus. (Einige Linux-Distributionen bieten möglicherweise keine Offlinelizenzen.)

    ![Microsoft Store für Unternehmen – Ubuntu-Produktseite](media/offlineinstallscreens/4-screen.png)

6. Wählen Sie die Schaltfläche „Verwalten“ aus, um zur Produktseite der App zu gelangen.

    ![Microsoft Store für Unternehmen – Ubuntu-Produktseite](media/offlineinstallscreens/5-screen.png)

7. Wählen Sie Ihre Architektur aus, und laden Sie das Paket zur Offlineverwendung herunter.

    ![Microsoft Store für Unternehmen – Seite der Ubuntu-Produktdetails](media/offlineinstallscreens/6-screen.png)

Dieses Installationsprogramm kann dann an jeden Computer verteilt werden, auf dem Sie WSL installieren möchten.
