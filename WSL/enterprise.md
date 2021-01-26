---
title: WSL für Unternehmen
description: Ressourcen und Anweisungen zur optimalen Verwendung des WSL für Linux in einer Unternehmensumgebung.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Unternehmen, Bereitstellung, offline, Paket, Store, Verteilung, Installation, installieren
ms.date: 12/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a210268fb460a793fec2047c6d6678f92869ea16
ms.sourcegitcommit: 0523e6a2ca99f5f3b188d526afed3ce6ad7e3abb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "98766856"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>Windows-Subsystem für Linux für Unternehmen

Als Administrator oder Manager können Sie verlangen, dass alle Entwickler die gleiche genehmigte Software verwenden. Diese Konsistenz hilft beim Erstellen einer gut definierten Arbeitsumgebung. Das Windows-Subsystem für Linux trägt zu dieser Konsistenz bei, indem es Ihnen ermöglicht, benutzerdefinierte WSL-Images von einem Computer zum nächsten zu importieren und zu exportieren. Lesen Sie den folgenden Leitfaden, um mehr darüber zu erfahren:

* [Erstellen eines benutzerdefinierten WSL-Images](#creating-a-custom-wsl-image)
* [Verteilen eines WSL-Images](#distributing-your-wsl-image)
* [Aktualisieren und Patchen von Linux-Verteilungen und -Paketen](#update-and-patch-linux-distributions-and-packages)
* [Optionen für Sicherheit und Kontrolle im Unternehmen](#enterprise-security-and-control-options)

## <a name="creating-a-custom-wsl-image"></a>Erstellen eines benutzerdefinierten WSL-Images

Was gemeinhin als „Image“ bezeichnet wird, ist einfach eine in einer Datei gespeicherte Momentaufnahme Ihrer Software und deren Komponenten. Im Fall des Windows-Subsystems für Linux würde Ihr Image aus dem Subsystem, seinen Verteilungen sowie der in den Verteilungen installierten Software und den Paketen bestehen.

Um mit der Erstellung Ihres WSL-Images zu beginnen, müssen Sie zunächst [das Windows-Subsystem für Linux installieren](./install-win10.md).

Nach der Installation können Sie über den Microsoft Store für Unternehmen die für Sie passende Linux-Verteilung herunterladen und installieren. Erstellen eines Kontos über den [Microsoft Store für Unternehmen](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business.)

### <a name="exporting-your-wsl-image"></a>Exportieren Ihres WSL-Images

Exportieren Sie Ihr benutzerdefiniertes WSL-Image, indem Sie „wsl --export `<Distro> <FileName>`“ ausführen, wodurch das Image in eine TAR-Datei gepackt und für die Verteilung auf anderen Computern vorbereitet wird.

## <a name="distributing-your-wsl-image"></a>Verteilen Ihres WSL-Images

Verteilen Sie das WSL-Image von einer Freigabe oder einem Speichergerät aus, indem Sie „wsl --import `<Distro> <InstallLocation> <FileName>`“ ausführen, wodurch die angegebene TAR-Datei als neue Verteilung importiert wird.

## <a name="update-and-patch-linux-distributions-and-packages"></a>Aktualisieren und Patchen von Linux-Verteilungen und -Paketen

Die Verwendung von Linux-Konfigurations-Manager-Tools wird dringend empfohlen, um Linux-Benutzerspeicher zu überwachen und zu verwalten. Es gibt eine Vielzahl von Linux-Konfigurations-Managern, aus denen Sie auswählen können. Schauen Sie sich diesen [Blogbeitrag](http://www.craigloewen.com/blog/2019/12/04/running-puppet-quickly-in-wsl2/) über das Installieren von Puppet in WSL 2 an.

## <a name="enterprise-security-and-control-options"></a>Optionen für Sicherheit und Kontrolle im Unternehmen

Derzeit bietet lässt die Benutzererfahrung in einem Unternehmensszenario nur eingeschränkt durch WSL ändern. Die Unternehmensfeatures werden jedoch ständig weiterentwickelt. Nachfolgend sind die Bereiche der unterstützten und nicht unterstützten Features aufgeführt. Wenn Sie ein neues Feature anfordern möchten, das nicht in dieser Liste enthalten ist, melden Sie ein Problem in unserem [GitHub-Repository](https://github.com/microsoft/WSL/issues?q=is%3Aissue+is%3Aopen+enterprise).

### <a name="supported"></a>Unterstützt

* Internes Freigeben eines genehmigten Images mithilfe von `wsl --import` und `wsl --export`
* Erstellen einer eigenen WSL-Verteilung für Ihr Unternehmen mit dem [WSL Distro Launcher-Repository](https://github.com/microsoft/WSL-DistroLauncher)

Hier ist eine Liste von Features, für die noch keine Unterstützung besteht, die aber untersucht werden.

### <a name="unsupported"></a>Nicht unterstützt

* Synchronisieren des Benutzers innerhalb von WSL mit dem Windows-Benutzer auf dem Hostcomputer
* Verwalten von Updates und Patchen der Linux-Verteilungen und -Pakete mit Windows-Tools
* Verwenden von Windows Update auch für Inhalte von WSL-Verteilungen
* Steuern, auf welche Verteilungen Benutzer in Ihrem Unternehmen zugreifen können
* Ausführen obligatorischer Dienste (Protokollierung oder Überwachung) in WSL
* Überwachen von Linux-Instanzen mit Windows-Konfigurations-Manager-Tools wie SCCM oder Intune
* McAfee-Unterstützung
