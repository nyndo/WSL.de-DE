---
title: Informationen zu WSL 2
description: Informationen zu WSL 2, der neuen Architektur für das Windows-Subsystem für Linux. Erhalten Sie eine Übersicht über die Architektur und Informationen zum Linux-Kernel.
keywords: BashOnWindows, Bash, WSL, WSL2, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Installation, installieren
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: bfb0e14ce53d3022dba06340630cc97a1286a13f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866122"
---
# <a name="about-wsl-2"></a>Informationen zu WSL 2

WSL 2 ist eine neue Version der Architektur, die es dem Windows-Subsystem für Linux ermöglicht, ELF64-Linux-Binärdateien unter Windows auszuführen. Die Hauptziele sind eine gesteigerte Leistung des Dateisystems sowie das Hinzufügen vollständiger Kompatibilität von Systemaufrufen. Diese neue Architektur führt zu einer Änderung der Interaktion dieser Linux-Binärdateien mit Windows und der Hardware Ihres Computers, bietet aber die gleiche Benutzererfahrung wie WSL 1 (die aktuelle, allgemein verfügbar Version). Einzelne Linux-Distributionen können entweder als WSL 1-Distribution oder als WSL 2-Distribution ausgeführt werden, Upgrades oder Downgrades sind jederzeit möglich, und WSL 1- und WSL 2-Distributionen können parallel ausgeführt werden. WSL 2 verwendet eine völlig neue Architektur, die einen echten Linux-Kernel verwendet.

## <a name="linux-kernel-in-wsl-2"></a>Linux-Kernel in WSL 2

Der Linux-Kernel in WSL 2 wird auf der Grundlage der Quellen auf kernel.org In-House aus dem aktuellsten stabilen Zweig erstellt. Dieser Kernel wurde speziell für WSL 2 optimiert. Er wurde im Hinblick auf Größe und Leistung optimiert, um unter Windows eine beeindruckende Linux-Benutzererfahrung zu bieten, und wird über Windows-Updates gewartet, was bedeutet, dass Sie die neuesten Sicherheitskorrekturen und Kernelverbesserungen erhalten, ohne sie selbst verwalten zu müssen.

Außerdem ist dieser Kernel Open Source. Den vollständigen Quellcode für den Linux-Kernel finden Sie [hier](https://github.com/microsoft/WSL2-Linux-Kernel). Wenn Sie mehr über diesen Kernel erfahren möchten, lesen Sie [diesen Blogbeitrag](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/), der von dem Team geschrieben wurde, das ihn erstellt hat.

## <a name="brief-overview-of-the-wsl-2-architecture"></a>Kurze Übersicht über die Architektur von WSL 2

WSL 2 verwendet das Neueste und Beste an Virtualisierungstechnologie, um seinen Linux-Kernel innerhalb einer schlanken Hilfsprogramms-VM auszuführen. WSL 2 stellt jedoch KEINE herkömmliche VM-Benutzererfahrung dar. Eine herkömmliche VM-Benutzerumgebung lässt sich unter Umständen nur langsam starten, verbraucht viele Ressourcen und nimmt für die Verwaltung Ihre Zeit in Anspruch. WSL 2 weist diese Merkmale nicht auf. Es bietet weiterhin die bemerkenswerten Vorteile von WSL 1: Ein hohes Maß an Integration zwischen Windows und Linux, extrem kurze Startzeiten, geringen Ressourcenbedarf und vor allem: keine Konfiguration oder Verwaltung einer VM. Zwar verwendet WSL 2 eine VM, diese wird jedoch hinter den Kulissen verwaltet und ausgeführt, und Ihnen bleibt die Benutzererfahrung von WSL 1 erhalten.

## <a name="increased-file-io-performance"></a>Verbesserte E/A-Leistung für Dateien

Dateiintensive Vorgänge, wie `git clone`, `npm install`, `apt update`, `apt upgrade` und mehr, werden alle spürbar schneller ausgeführt. Die tatsächliche Geschwindigkeitssteigerung hängt davon ab, welche App Sie ausführen und wie sie mit dem Dateisystem interagiert. Anfängliche Versionen von WSL 2 werden im Vergleich mit WSL 1 bis zu 20mal schneller ausgeführt (Entpacken eines gezippten Tarballs) und 2–5mal schneller beim Verwenden von `git clone`, `npm install` und `cmake` in verschiedenen Projekten.

## <a name="full-system-call-compatibility"></a>Vollständige Kompatibilität von Systemaufrufen

Linux-Binärdateien verwenden Systemaufrufe für viele Funktionen, wie den Zugriff auf Dateien, das Anfordern von Arbeitsspeicher, das Erstellen von Prozessen und mehr. Während WSL 1 eine Übersetzungsschicht verwendete, die vom WSL-Team erstellt wurde, enthält WSL 2 seinen eigenen Linux-Kernel mit vollständiger Kompatibilität der Systemaufrufe. Dadurch wird eine ganz neue Reihe von Apps eingeführt, die Sie in WSL ausführen können, wie etwa Docker und mehr. Darüber hinaus wurde erreicht, dass Updates des Linux-Kernels jetzt sofort zu Ihrem Computer hinzugefügt werden können, statt abwarten zu müssen, bis das WSL-Team die Änderungen implementiert und sie dann hinzufügt.
