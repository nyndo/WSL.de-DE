---
title: Beginnen Sie mit der Verwendung von MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server oder redis zum Einrichten einer Datenbank unter Windows-Subsystem für Linux.
description: Erfahren Sie, wie Sie MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server oder redis im Windows-Subsystem für Linux einrichten.
keywords: WSL, Windows, windowssubsystem, MySQL MongoDB, PostgreSQL, SQLite, Microsoft SQL Server, redis, Windows 10
ms.date: 07/07/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: b7e4f7477741a931c4ee71e07736bac115443ac9
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413301"
---
# <a name="get-started-with-databases-on-windows-subsystem-for-linux"></a>Einstieg in Datenbanken unter Windows-Subsystem für Linux

Diese Schritt-für-Schritt-Anleitung hilft Ihnen beim Einstieg in die Verbindung Ihres Projekts in WSL mit einer-Datenbank. Beginnen Sie mit MySQL, PostgreSQL, MongoDB, redis, Microsoft SQL Server oder SQLite.

## <a name="prerequisites"></a>Voraussetzungen

- Ausgeführt unter Windows 10, [aktualisiert auf Version 2004](ms-settings:windowsupdate), **Build 19041** oder höher.
- [WSL wurde aktiviert und installiert und auf WSL 2 aktualisiert](../install-win10.md).
- [Linux-Distribution installiert](../install-win10.md#step-6---install-your-linux-distribution-of-choice) (für unsere Beispiele Ubuntu 18,04).
- Stellen Sie sicher, dass die Ubuntu 18,04-Distribution [im WSL 2-Modus ausgeführt](../install-win10.md#set-your-distribution-version-to-wsl-1-or-wsl-2)wird. (WSL kann Verteilungen im v1-oder V2-Modus ausführen.) Sie können dies überprüfen, indem Sie PowerShell öffnen und Folgendes eingeben: `wsl -l -v`

## <a name="differences-between-database-systems"></a>Unterschiede zwischendatenbanksystemen

Zu den [beliebtesten Optionen](https://insights.stackoverflow.com/survey/2019#technology-_-databases) für ein Datenbanksystem gehören:

- [MySQL](https://www.mysql.com/why-mysql/) (SQL)
- [PostgreSQL](https://www.postgresql.org/about/) (SQL)
- [Microsoft SQL Server](/sql) (SQL)
- [SQLite](https://www.sqlite.org/about.html) (SQL)
- [MongoDB](https://www.mongodb.com/what-is-mongodb) (nosql)
- [Redis](https://redis.io/topics/introduction) (nosql)

**MySQL** ist eine relationale SQL-Datenbank, die Daten in einer oder mehreren Tabellen organisiert, in denen Datentypen miteinander verknüpft werden können. Es ist vertikal skalierbar, was bedeutet, dass ein endgültiger Computer die Arbeit für Sie übernimmt. Dies ist derzeit die am häufigsten verwendete der vier Datenbanksysteme.

**PostgreSQL** (auch als Postgres bezeichnet) ist eine Open-Source-relationale SQL-Datenbank mit dem Schwerpunkt auf Erweiterbarkeit und Einhaltung von Standards. Sie kann jetzt auch JSON verarbeiten, ist jedoch im Allgemeinen besser für strukturierte Daten, vertikale Skalierung und ACID-kompatible Anforderungen wie eCommerce und Finanztransaktionen geeignet.

**Microsoft SQL Server** umfasst SQL Server unter Windows, SQL Server für Linux und SQL in Azure. Dies sind auch Verwaltungssysteme für relationale Datenbanken, die auf Servern mit der primären Funktion zum Speichern und Abrufen von Daten gemäß der Anforderung von Softwareanwendungen eingerichtet sind.

**SQLite** ist eine eigenständige, dateibasierte, "Server lose" Open Source-Datenbank, die für die Portabilität, Zuverlässigkeit und gute Leistung, auch in Umgebungen mit geringem Arbeitsspeicher, bekannt ist.

**MongoDB** ist eine Open-Source-nosql-dokumentdatenbank, die für die Arbeit mit JSON und das Speichern von Schema freien Daten konzipiert ist. Es ist horizontal skalierbar, was bedeutet, dass mehrere kleinere Computer die Arbeit für Sie erledigen. Es eignet sich gut für Flexibilität und unstrukturierte Daten sowie für das Zwischenspeichern von Echtzeitanalysen.

**Redis** ist ein nosql-Speicher im Arbeitsspeicher im Datenstruktur Speicher von nosql. Es verwendet Schlüssel-Wert-Paare für die Speicherung anstelle von Dokumenten. Redis ist für die Flexibilität, Leistung und weite Sprachunterstützung bekannt. Es ist flexibel genug, um als Cache-oder Nachrichten Broker verwendet zu werden, und kann Datenstrukturen wie Listen, Sets und Hashes verwenden.

Welche Art von Datenbank Sie auswählen sollten, hängt von der Art der Anwendung ab, mit der Sie die Datenbank verwenden werden. Sie sollten sich über die Vor- und Nachteile von strukturierten und unstrukturierten Datenbanken informieren und die geeignete Auswahl für Ihren Anwendungsfall treffen.

## <a name="install-mysql"></a>Installieren von MySQL

So installieren Sie MySQL auf WSL (Ubuntu 18,04):

1. Öffnen Sie das WSL-Terminal (d. h. Ubuntu 18.04).
2. Aktualisieren Sie Ihre Ubuntu-Pakete: `sudo apt update`.
3. Nachdem die Pakete aktualisiert wurden, installieren Sie MySQL mit: `sudo apt install mysql-server`
4. Bestätigen Sie die Installation, und rufen Sie die Versionsnummer ab: `mysql --version`.

Möglicherweise möchten Sie auch das enthaltene Sicherheits Skript ausführen. Dies ändert einige der weniger sicheren Standardoptionen für Dinge wie Remote-Stamm Anmeldungen und Beispiel Benutzer. So führen Sie das Sicherheits Skript aus:

1. Starten eines MySQL-Servers: `sudo /etc/init.d/mysql start`
2. Starten Sie die Sicherheits Skript Aufforderungen: `sudo mysql_secure_installation`
3. In der ersten Aufforderung werden Sie gefragt, ob Sie das Kennwort für die Kenn Wort Validierung einrichten möchten, mit dem Sie die Stärke des MySQL-Kennworts testen können. Anschließend legen Sie ein Kennwort für den MySQL-root-Benutzer fest, entscheiden, ob anonyme Benutzer entfernt werden sollen, und entscheiden, ob der root-Benutzer sich sowohl lokal als auch remote anmelden darf, ob die Testdatenbank entfernt werden soll, und schließlich entscheiden Sie, ob die Berechtigungs Tabellen sofort erneut geladen werden sollen.

Geben Sie zum Öffnen der MySQL-Eingabeaufforderung Folgendes ein: `sudo mysql`

Geben Sie in der MySQL-Eingabeaufforderung Folgendes ein, um die verfügbaren Datenbanken anzuzeigen: `SHOW DATABASES;`

Geben Sie Folgendes ein, um eine neue Datenbank zu erstellen: `CREATE DATABASE database_name;`

Geben Sie Folgendes ein, um eine Datenbank zu löschen: ` DROP DATABASE database_name;`

Weitere Informationen zum Arbeiten mit MySQL-Datenbanken finden Sie in der [MySQL](https://dev.mysql.com/doc/mysql-getting-started/en/)-Dokumentation.

Wenn Sie mit MySQL-Datenbanken in vs Code arbeiten möchten, testen Sie die [MySQL-Erweiterung](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-mysql-client2).

## <a name="install-postgresql"></a>Installieren von PostgreSQL

So installieren Sie PostgreSQL auf WSL (Ubuntu 18,04):

1. Öffnen Sie das WSL-Terminal (d. h. Ubuntu 18.04).
2. Aktualisieren Sie Ihre Ubuntu-Pakete: `sudo apt update`.
3. Nachdem die Pakete aktualisiert wurden, installieren Sie PostgreSQL (und das -contrib-Paket mit einigen nützlichen Dienstprogrammen) mit: `sudo apt install postgresql postgresql-contrib`.
4. Bestätigen Sie die Installation, und rufen Sie die Versionsnummer ab: `psql --version`.

Es gibt drei Befehle, die Sie nach der Installation von PostgreSQL kennen müssen:

- `sudo service postgresql status` zum Überprüfen des Status Ihrer Datenbank.
- `sudo service postgresql start`, um die Ausführung der Datenbank zu starten.
- `sudo service postgresql stop`, um die Ausführung der Datenbank zu stoppen.

Der standardmäßige Administratorbenutzer (`postgres`) benötigt ein zugewiesenes Kennwort, um eine Verbindung mit einer Datenbank herzustellen. So legen Sie ein Kennwort fest:

1. Geben Sie den Befehl `sudo passwd postgres` ein.
2. Sie erhalten eine Aufforderung, Ihr neues Kennwort einzugeben.
3. Schließen Sie das Terminal, und öffnen Sie es erneut.

So führen Sie PostgreSQL mit [psql](https://www.postgresql.org/docs/10/app-psql.html) -Shell aus:

1. Starten Ihres Postgres-Diensts: `sudo service postgresql start`.
2. Verbinden Sie sich mit dem Postgres-Dienst, und öffnen Sie die psql-Shell: `sudo -u postgres psql`.

Nachdem Sie die psql-Shell erfolgreich eingegeben haben, sehen Sie, dass die Befehlszeile sich wie folgt ändert: `postgres=#`.

> [!NOTE]
> Alternativ dazu können Sie die psql-Shell öffnen, indem Sie mit `su - postgres` zum Postgres-Benutzer wechseln und dann den folgenden Befehl eingeben: `psql`.

Um Postgres = # Enter: zu beenden, `\q` oder verwenden Sie die Tastenkombination: STRG + D

Um anzuzeigen, welche Benutzerkonten in Ihrer PostgreSQL-Installation erstellt wurden, geben Sie `psql -c "\du"` in Ihr WSL-Terminal ein, oder einfach `\du`, wenn die psql-Shell geöffnet ist. Mit diesem Befehl werden Spalten angezeigt: Benutzer Name des Kontos, Liste der Rollen Attribute und Mitglied der Rollen Gruppe (n). Um zur Befehlszeile zurückzukehren, geben Sie `q` ein.

Weitere Informationen zum Arbeiten mit PostgreSQL-Datenbanken finden Sie in der [PostgreSQL](https://www.postgresql.org/docs/13/tutorial-createdb.html)-Dokumentation.

Wenn Sie mit PostgreSQL-Datenbanken in vs Code arbeiten möchten, testen Sie die [PostgreSQL-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-ossdata.vscode-postgresql).

## <a name="install-mongodb"></a>Installieren von MongoDB

So installieren Sie MongoDB auf WSL (Ubuntu 18,04):

1. Öffnen Sie das WSL-Terminal (d. h. Ubuntu 18.04).
2. Aktualisieren Sie Ihre Ubuntu-Pakete: `sudo apt update`.
3. Nachdem die Pakete aktualisiert wurden, installieren Sie MongoDB wie folgt: `sudo apt-get install mongodb`.
4. Bestätigen Sie die Installation, und rufen Sie die Versionsnummer ab: `mongod --version`.

Nach der Installation von MongoDB müssen Sie drei Befehle kennen:

- `sudo service mongodb status` zum Überprüfen des Status Ihrer Datenbank.
- `sudo service mongodb start`, um die Ausführung der Datenbank zu starten.
- `sudo service mongodb stop`, um die Ausführung der Datenbank zu stoppen.

> [!NOTE]
> Möglicherweise wird in Tutorials oder Artikeln der Befehl `sudo systemctl status mongodb` verwendet. Damit das Paket nicht zu groß wird, ist `systemd` (ein Dienstverwaltungssystem unter Linux) in WSL nicht enthalten. Stattdessen wird SysVinit verwendet, um Dienste auf Ihrem Computer zu starten. Sie sollten keinen Unterschied bemerken, aber wenn in einem Tutorial die Verwendung von `sudo systemctl` empfohlen wird, verwenden Sie stattdessen `sudo /etc/init.d/`. Beispiel: `sudo systemctl status mongodb` entspricht in WSL `sudo /etc/inid.d/mongodb status`. Sie können jedoch auch `sudo service mongodb status` verwenden.

So führen Sie die Mongo-Datenbank auf einem lokalen Server aus:

1. Überprüfen Sie den Status der Datenbank: `sudo service mongodb status` Sie sollten eine [FAIL]-Antwort sehen, es sei denn, Sie haben die Datenbank bereits gestartet.

2. Starten Sie die Datenbank: es `sudo service mongodb start` sollte nun eine [OK]-Antwort angezeigt werden.

3. Überprüfen Sie, ob Sie eine Verbindung mit dem Datenbankserver herstellen, und führen Sie einen Diagnose Befehl `mongo --eval 'db.runCommand({ connectionStatus: 1 })'` aus: Dadurch werden die aktuelle Datenbankversion, die Server Adresse und der Port sowie die Ausgabe des Status-Befehls ausgegeben. Der Wert `1` für das Feld „ok“ in der Antwort gibt an, dass der Server funktioniert.

4. Wenn Sie die Ausführung des MongoDB-Diensts unterbinden möchten, geben Sie Folgendes ein: `sudo service mongodb stop`

> [!NOTE]
> MongoDB verfügt über mehrere Standardparameter, darunter die Speicherung von Daten in „/data/db“ und die Ausführung an Port 27017. Außerdem ist `mongod` der Daemon (Hostprozess für die Datenbank), und `mongo` ist die Befehlszeilenshell, die eine Verbindung mit einer bestimmten Instanz von `mongod` herstellt.

VS Code die Arbeit mit MongoDB-Datenbanken über die [Azure Cosmos DB-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-cosmosdb)unterstützt, können Sie MongoDB-Datenbanken in vs Code erstellen, verwalten und Abfragen. Weitere Informationen finden Sie in der vs Code docs: [Arbeiten mit MongoDB](https://code.visualstudio.com/docs/azure/mongodb).

Weitere Informationen finden Sie in der MongoDB-Dokumentation:

- [Einführung in die Verwendung von MongoDB](https://docs.mongodb.com/manual/introduction/)
- [Erstellen von Benutzern](https://docs.mongodb.com/manual/tutorial/create-users/)
- [Herstellen einer Verbindung mit einer MongoDB-Instanz auf einem Remote Host](https://docs.mongodb.com/manual/mongo/#mongodb-instance-on-a-remote-host)
- [CRUD: erstellen, lesen, aktualisieren, löschen](https://docs.mongodb.com/manual/crud/)
- [Referenzdokumente](https://docs.mongodb.com/manual/reference/)

## <a name="install-microsoft-sql-server"></a>Installieren von Microsoft SQL Server

Um SQL Server auf WSL (Ubuntu 18,04) zu installieren, führen Sie diesen Schnellstart aus: [Installieren Sie SQL Server, und erstellen Sie eine Datenbank unter Ubuntu](/sql/linux/quickstart-install-connect-ubuntu).

Wenn Sie mit Microsoft SQL Server Datenbanken in vs Code arbeiten möchten, testen Sie die [MSSQL-Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-mssql.mssql).

## <a name="install-sqlite"></a>Installieren von SQLite

So installieren Sie SQLite auf WSL (Ubuntu 18,04):

1. Öffnen Sie das WSL-Terminal (d. h. Ubuntu 18.04).
2. Aktualisieren Sie Ihre Ubuntu-Pakete: `sudo apt update`.
3. Sobald die Pakete aktualisiert wurden, installieren Sie sqlite3 mit: `sudo apt install sqlite3`
4. Bestätigen Sie die Installation, und rufen Sie die Versionsnummer ab: `sqlite3 --version`.

Geben Sie Folgendes ein, um eine Testdatenbank mit dem Namen "example. DB" zu erstellen: `sqlite3 example.db`

Geben Sie Folgendes ein, um eine Liste Ihrer SQLite-Datenbanken anzuzeigen: `.databases`

Geben Sie Folgendes ein, um den Status der Datenbank anzuzeigen: `.dbinfo ?DB?`

Geben Sie zum Beenden der SQLite-Eingabeaufforderung Folgendes ein: `.exit`

Weitere Informationen zum Arbeiten mit einer SQLite-Datenbank finden Sie in der [SQLite](https://www.sqlite.org/quickstart.html)-Dokumentation.

Wenn Sie in vs Code mit SQLite-Datenbanken arbeiten möchten, testen Sie die [SQLite-Erweiterung](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools).

## <a name="install-redis"></a>Installieren von redis

So installieren Sie redis auf WSL (Ubuntu 18,04):

1. Öffnen Sie das WSL-Terminal (d. h. Ubuntu 18.04).
2. Aktualisieren Sie Ihre Ubuntu-Pakete: `sudo apt update`.
3. Nachdem die Pakete aktualisiert wurden, installieren Sie redis wie folgt: `sudo apt install redis-server`
4. Bestätigen Sie die Installation, und rufen Sie die Versionsnummer ab: `redis-server --version`.

So beginnen Sie mit der Ausführung des redis-Servers: `sudo service redis-server start`

Überprüfen Sie, ob redis funktioniert (redis-cli ist das Befehlszeilenschnittstelle-Hilfsprogramm für die Kommunikation mit redis): Hiermit `redis-cli ping` sollte die Antwort "Pong" zurückgegeben werden.

So können Sie den redis-Server nicht mehr ausführen: `sudo service redis-server stop`

Weitere Informationen zum Arbeiten mit einer redis-Datenbank finden Sie in der [redis](https://redis.io/topics/quickstart)-Dokumentation.

Wenn Sie in vs Code mit redis-Datenbanken arbeiten möchten, verwenden Sie die [redis-Erweiterung](https://marketplace.visualstudio.com/items?itemName=cweijan.vscode-redis-client).

## <a name="see-services-running-and-set-up-profile-aliases"></a>Anzeigen von Diensten, die ausgeführt werden, und Einrichten von Profil Aliasen

Geben Sie Folgendes ein, um die Dienste anzuzeigen, die Sie zurzeit in der WSL-Distribution ausgeführt haben: `service --status-all`

Das Eingeben von `sudo service mongodb start` oder `sudo service postgres start` und `sudo -u postgrest psql` kann mühsam werden.  Sie können jedoch in Betracht ziehen, Aliase in Ihrer Datei `.profile` unter WSL einzurichten, um diese Befehle einfacher verwenden zu können und sie sich besser zu merken.

So richten Sie einen eigenen benutzerdefinierten Alias oder eine Verknüpfung für die Ausführung dieser Befehle ein

1. Öffnen Sie das WSL-Terminal, und geben Sie `cd ~` ein, um sicherzustellen, dass Sie sich im Stammverzeichnis befinden.
2. Öffnen Sie die Datei `.profile`, in der die Einstellungen für das Terminal gesteuert werden, mit dem Terminal-Text-Editor nano: `sudo nano .profile`.
3. Fügen Sie am Ende der Datei Folgendes hinzu (ohne die `# set PATH`-Einstellungen zu ändern):

    ```bash
    # My Aliases
    alias start-pg='sudo service postgresql start'
    alias run-pg='sudo -u postgres psql'
    ```

    Dadurch können Sie `start-pg` eingeben, um den PostgreSQL-Dienst zu starten, und `run-pg`, um die psql-Shell zu öffnen. Sie können `start-pg` und `run-pg` in beliebige Namen ändern. Achten Sie jedoch darauf, keinen Befehl zu überschreiben, der von Postgres bereits verwendet wird.

4. Nachdem Sie die neuen Aliase hinzugefügt haben, beenden Sie den Text-Editor nano, indem Sie **STRG+X** drücken, `Y` (Ja) auswählen, wenn Sie gefragt werden, ob Sie speichern möchten, und die EINGABETASTE drücken (wobei Sie den Dateinamen `.profile`beibehalten).
5. Schließen Sie das WSL-Terminal, öffnen Sie es erneut, und probieren Sie dann die neuen Aliasbefehle aus.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

- [Einrichten Ihrer Entwicklungsumgebung unter Windows 10](/windows/dev-environment/)