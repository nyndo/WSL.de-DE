---
title: Windows-Subsystem für Linux für Unternehmen
description: Ressourcen und Anweisungen zur optimalen Verwendung des Windows-Subsystems für Linux in einer Unternehmensumgebung.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Unternehmen, Bereitstellung, offline, Paket, Store, Verteilung, Installation, installieren
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ac0025257ae70547c5b20d89535510a8b8bb006c
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413101"
---
# <a name="set-up-windows-subsystem-for-linux-for-your-enterprise-company"></a>Einrichten des Windows-Subsystems für Linux für Ihr Unternehmen

Der Microsoft Store für Unternehmen bietet verschiedene Unternehmenslösungen, die WSL in Ihrem Unternehmen bereitstellen möchten. Die [Dokumentation im Microsoft Store für Unternehmen und Bildungseinrichtungen](/microsoft-store/) stellt eine gute Ressource für allgemeine Informationen über die Store-Benutzeroberfläche dar.

Als Unternehmen, das nur sein System für die Bereitstellung von WSL einrichten möchte, führen Sie die folgenden Schritte aus:

* [Registrieren für Microsoft Store für Unternehmen und erste Schritte](/microsoft-store/sign-up-microsoft-store-for-business-overview).
* [Verwalten Sie Ihre Produkte und Dienste (einschließlich der Benutzer, die auf die Apps in Ihrem privaten Store zugreifen können)](/microsoft-store/manage-apps-microsoft-store-for-business-overview). Hier können Sie Ihrem Store WSL-Verteilungen hinzufügen und steuern, wer diese installieren kann.
* [Verwenden einer Verteilungsmethode Ihrer Wahl, um die Software in Ihrem Unternehmen bereitzustellen](/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* Informieren Sie die Mitarbeiter Ihres Unternehmens, dass sie diesen Dokumentationslink zum Installieren von WSL verwenden können: [Installieren des Windows-Subsystems für Linux](./install-win10.md)

## <a name="how-to-distribute-a-linux-distribution-on-windows-offline"></a>Offlineverteilen einer Linux-Verteilung unter Windows

Wenn die Computer in Ihrem Unternehmen keinen Zugriff auf den Microsoft Store oder den Microsoft Store für Unternehmen haben, können Sie das Installationsprogramm einer Linux-Verteilung mit einer Offline Lizenz herunterladen, indem Sie die folgenden Schritte ausführen.

### <a name="set-up-an-azure-active-directory-account"></a>Einrichten eines Azure Active Directory-Kontos

Sie müssen sich [für ein Azure AD-Konto registrieren](/azure/active-directory/fundamentals/sign-up-organization?WT.mc_id=windows-c9-niner) und der globale Administrator für Ihre Organisation sein, um das Installationsprogramm für Microsoft Store-Apps zu erhalten. Wenn Sie bereits ein Konto haben, können Sie diesen Schritt überspringen.

### <a name="set-up-wsl-using-your-microsoft-store-for-business-account"></a>Einrichten von WSL mithilfe Ihres Microsoft Store für Unternehmen-Kontos

Die Anweisungen zum Registrieren eines Kontos finden Sie hier: https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business

1. Melden Sie sich beim Store für Unternehmen an, und wechseln Sie zur Startseite: https://www.microsoft.com/business-store

    ![Microsoft Store für Unternehmen – Startseite](media/offlineinstallscreens/1-screen.png)

2. Wechseln Sie zu „Verwalten“ > „Einstellungen“, und aktivieren Sie „Offline-Apps anzeigen“.

    ![Seite mit den Einstellungen für den Microsoft Store für Unternehmen](media/offlineinstallscreens/2-screen.png)

3. Wechseln Sie zurück zur Hauptseite, indem Sie „Für meine Gruppe einkaufen“ auswählen.

    ![Microsoft Store für Unternehmen – Startseite](media/offlineinstallscreens/1-screen.png)

4. Suchen Sie nach der gewünschten Verteilung, und wählen Sie sie aus.

    ![Microsoft Store für Unternehmen – Startseite mit aktiver Suche](media/offlineinstallscreens/3-screen.png)

5. Wählen Sie im Dropdownmenü „Lizenztyp“ eine Offlinelizenz und dann „App abrufen“ aus. (Einige Linux-Verteilungen bieten möglicherweise keine Offlinelizenzen.)

    ![Microsoft Store für Unternehmen – „Offline“ auswählen](media/offlineinstallscreens/4-screen.png)

6. Wählen Sie die Schaltfläche „Verwalten“ aus, um zur Produktseite der App zu gelangen.

    ![Microsoft Store für Unternehmen – „Verwalten“ auswählen](media/offlineinstallscreens/5-screen.png)

7. Wählen Sie Ihre Architektur aus, und laden Sie das Paket zur Offlineverwendung herunter.

    ![Microsoft Store für Unternehmen – Architektur auswählen](media/offlineinstallscreens/6-screen.png)

Dieses Installationsprogramm kann dann an jeden Computer verteilt werden, auf dem Sie WSL installieren möchten.
