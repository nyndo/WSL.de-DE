---
title: Dateiberechtigungen
description: Grundlegendes dazu, wie WSL die Dateiberechtigungen in Windows bestimmt
keywords: BashOnWindows, Bash, WSL, WSL2, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Dateiberechtigungen
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.openlocfilehash: 81d4cfa1ae57cdd077ba8cbd614111881724718a
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336073"
---
# <a name="file-permissions-for-wsl"></a>Dateiberechtigungen für WSL

Auf dieser Seite wird erläutert, wie Linux-Dateiberechtigungen über das Windows-Subsystem für Linux interpretiert werden, insbesondere beim Zugriff auf Ressourcen innerhalb von Windows auf dem NT-Dateisystem. Diese Dokumentation setzt ein Grundwissen der [Berechtigungsstruktur des Linux-Dateisystems](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) und des [Befehls „umask“](https://en.wikipedia.org/wiki/Umask) voraus.

Beim Zugriff auf Windows-Dateien von WSL werden die Dateiberechtigungen entweder anhand der Windows-Berechtigungen berechnet oder aus Metadaten gelesen, die von WSL zur Datei hinzugefügt wurden. Diese Metadaten sind standardmäßig nicht aktiviert.

## <a name="wsl-metadata-on-windows-files"></a>WSL-Metadaten für Windows-Dateien

Wenn Metadaten als Bereitstellungsoption in WSL aktiviert sind, können erweiterte Attribute für Windows NT-Dateien hinzugefügt und interpretiert werden, um Linux-Dateisystemberechtigungen bereitzustellen.

WSL kann vier erweiterte NTFS-Attribute hinzufügen:

| Attributname | Beschreibung |
| --- | --- |
| $LXUID | Besitzer-ID des Benutzers |
| $LXGID | Besitzer-ID der Gruppe |
| $LXMOD | Dateimodus (Dateisystem-Berechtigungsoktale und -typ, z. B.: 0777) |
| $LXDEV | Gerät, falls es sich um eine Gerätedatei handelt |

Zusätzlich besitzen alle Dateien, die keine regulären Dateien oder Verzeichnisse sind (z. B. Symlinks, FIFOs, Blockgeräte, Unix-Sockets und Zeichengeräte) ebenfalls einen NTFS-[Analysepunkt](https://docs.microsoft.com/windows/win32/fileio/reparse-points). Dadurch lässt sich die Art der Datei in einem bestimmten Verzeichnis viel schneller bestimmen, ohne die erweiterten Attribute abfragen zu müssen.

## <a name="file-access-scenarios"></a>Dateizugriffsszenarien

Nachfolgend wird beschrieben, wie Berechtigungen bestimmt werden, wenn auf verschiedene Weise mithilfe des Windows-Subsystems für Linux auf Dateien zugegriffen wird.

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a>Zugreifen auf Dateien in Windows Drive File System (DrvFS) von Linux

Diese Szenarien liegen vor, wenn Sie von WSL aus auf Ihre Windows-Dateien zugreifen, höchstwahrscheinlich über `/mnt/c`.

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a>Lesen von Dateiberechtigungen aus einer vorhandenen Windows-Datei

Das Ergebnis hängt davon ab, ob die Datei bereits über Metadaten verfügt.

##### <a name="drvfs-file-does-not-have-metadata-default"></a>DrvFS-Datei enthält keine Metadaten (Standard)

Wenn der Datei keine Metadaten zugeordnet sind, werden die tatsächlichen Berechtigungen des Windows-Benutzers in Lesen/Schreiben/Ausführen-Berechtigungsbits übersetzt und die entsprechenden Wert für Benutzer, Gruppen und andere festgelegt. Wenn Ihr Windows-Benutzerkonto z. B. über Lese- und Ausführungszugriff, aber keinen Schreibzugriff für die Datei verfügt, wird dies als `r-x` für Benutzer, Gruppen und andere angezeigt. Wenn für die Datei das Schreibgeschützt-Attribut in Windows festgelegt ist, wird in Linux kein Schreibzugriff erteilt.

##### <a name="the-file-has-metadata"></a>Die Datei enthält Metadaten

Wenn in der Datei Metadaten vorhanden sind, werden anstelle der Übersetzung der tatsächlichen Berechtigungen des Windows-Benutzers einfach diese Metadatenwerte verwendet.

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a>Ändern von Dateiberechtigungen für eine vorhandene Windows-Datei unter Verwendung von „chmod“

Das Ergebnis hängt davon ab, ob die Datei bereits über Metadaten verfügt.

##### <a name="chmod-file-does-not-have-metadata-default"></a>chmod-Datei enthält keine Metadaten (Standard)

Chmod hat nur einen Effekt: Wenn Sie alle Schreibattribute einer Datei entfernen, wird das Schreibgeschützt-Attribut für die Windows-Datei festgelegt, da dies das gleiche Verhalten wie CIFS (Common Internet File System) ist, das der SMB-Client (Server Message Block) in Linux ist.

##### <a name="chmod-file-has-metadata"></a>Chmod-Datei enthält Metadaten

Chmod bewirkt das Ändern oder Hinzufügen von Metadaten in Abhängigkeit von den bereits vorhandenen Metadaten der Datei. 

Denken Sie daran, dass Sie sich nicht mehr Zugriff erteilen können, als Sie in Windows besitzen, auch wenn die Metadaten dies tun. Sie könnten die Metadaten beispielsweise mit `chmod 777` so festlegen, dass Sie Schreibberechtigungen für eine Datei erhalten. Wenn Sie aber versuchen, auf diese Datei zuzugreifen, können Sie trotzdem nicht in diese schreiben. Dies ist dank der Interoperabilität möglich, da alle Lese- oder Schreibbefehle für Windows-Dateien über Ihre Windows-Benutzerberechtigungen geleitet werden.

#### <a name="creating-a-file-in-drivefs"></a>Erstellen einer Datei in DriveFS

Das Ergebnis hängt davon ab, ob Metadaten aktiviert sind.

##### <a name="metadata-is-not-enabled-default"></a>Metadaten sind nicht aktiviert (Standard)

Die Windows-Berechtigungen der neu erstellten Datei sind identisch wie beim Erstellen der Datei in Windows ohne einen bestimmten Sicherheitsdeskriptor. Sie erben die Berechtigungen des übergeordneten Elements.

##### <a name="metadata-is-enabled"></a>Metadaten sind aktiviert

Die Berechtigungsbits der Datei sind so festgelegt, dass Sie der Linux-Umask folgen, und die Datei wird mit Metadaten gespeichert.

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a>Welcher Linux-Benutzer und welche Linux-Gruppe besitzt die Datei? 

Das Ergebnis hängt davon ab, ob die Datei bereits über Metadaten verfügt.

##### <a name="user-file-does-not-have-metadata-default"></a>Benutzerdatei enthält keine Metadaten (Standard)

Im Standardszenario legen wir beim Automatisieren von Windows-Laufwerken fest, dass die Benutzer-ID (UID) für jede Datei auf die Benutzer-ID des WSL-Benutzers und die Gruppen-ID (GID) auf die Prinzipalgruppen-ID des WSL-Benutzers festgelegt ist.

##### <a name="user-file-has-metadata"></a>Benutzerdatei enthält Metadaten

Die in den Metadaten angegebenen UID und GID werden als Benutzerbesitzer und Gruppenbesitzer der Datei angewendet.

### <a name="accessing-linux-files-from-windows-using-wsl"></a>Zugreifen auf Linux-Dateien von Windows aus mithilfe von `\\wsl$`

Wenn Sie über `\\wsl$` auf Linux-Dateien zugreifen, wird der Standardbenutzer der WSL-Verteilung verwendet. Daher hat jede Windows-App, die auf Linux-Dateien zugreift, dieselben Berechtigungen wie der Standardbenutzer.

#### <a name="creating-a-new-file"></a>Erstellen einer neuen Datei

Beim Erstellen einer neuen Datei in einer WSL-Verteilung von Windows wird die Standard-Umask angewendet. Die Standard-Umask ist `022`, d. h., es werden alle Berechtigungen mit Ausnahme von Schreibberechtigungen für Gruppen und andere zugelassen. 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a>Zugreifen auf Dateien im Linux-Stammdateisystem aus Linux

Alle Dateien, die im Linux-Stammdateisystem erstellt oder geändert bzw. auf die zugegriffen wird, folgen den Linux-Standardkonventionen, z. B. dass die Umask auf neu erstellte Dateien angewendet wird.

## <a name="configuring-file-permissions"></a>Konfigurieren von Dateiberechtigungen

Sie können Ihre Dateiberechtigungen innerhalb Ihrer Windows-Laufwerke mithilfe der Einbindungsoptionen in „WSL.conf“ konfigurieren. Mit den Einbindungsoptionen können Sie `umask`-, `dmask`- und `fmask`-Berechtigungsmasken festlegen. Die `umask` wird auf alle Dateien angewendet, die `dmask` wird nur auf Verzeichnisse angewendet, und die `fmask` wird nur auf Dateien angewendet. Diese Berechtigungsmasken werden dann durch eine logische ODER-Operation festgelegt, wenn sie auf Dateien angewendet werden. Beispiel: Wenn Sie über einen `umask`-Wert von `023` und einen `fmask`-Wert von `022` verfügen, wird die resultierende Berechtigungsmaske für Dateien auf `023` festgelegt.

Anweisungen zur Vorgehensweise finden Sie im Artikel [Konfigurieren von Starteinstellungen mit „wslconf“ für Verteilungen](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf).
