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
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="5a1f8-104">Dateiberechtigungen für WSL</span><span class="sxs-lookup"><span data-stu-id="5a1f8-104">File Permissions for WSL</span></span>

<span data-ttu-id="5a1f8-105">Auf dieser Seite wird erläutert, wie Linux-Dateiberechtigungen über das Windows-Subsystem für Linux interpretiert werden, insbesondere beim Zugriff auf Ressourcen innerhalb von Windows auf dem NT-Dateisystem.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="5a1f8-106">Diese Dokumentation setzt ein Grundwissen der [Berechtigungsstruktur des Linux-Dateisystems](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) und des [Befehls „umask“](https://en.wikipedia.org/wiki/Umask) voraus.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes) and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="5a1f8-107">Beim Zugriff auf Windows-Dateien von WSL werden die Dateiberechtigungen entweder anhand der Windows-Berechtigungen berechnet oder aus Metadaten gelesen, die von WSL zur Datei hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-107">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="5a1f8-108">Diese Metadaten sind standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-108">This metadata is not enabled by default.</span></span>

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="5a1f8-109">WSL-Metadaten für Windows-Dateien</span><span class="sxs-lookup"><span data-stu-id="5a1f8-109">WSL metadata on Windows files</span></span>

<span data-ttu-id="5a1f8-110">Wenn Metadaten als Bereitstellungsoption in WSL aktiviert sind, können erweiterte Attribute für Windows NT-Dateien hinzugefügt und interpretiert werden, um Linux-Dateisystemberechtigungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-110">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span>

<span data-ttu-id="5a1f8-111">WSL kann vier erweiterte NTFS-Attribute hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="5a1f8-111">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="5a1f8-112">Attributname</span><span class="sxs-lookup"><span data-stu-id="5a1f8-112">Attribute Name</span></span> | <span data-ttu-id="5a1f8-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a1f8-113">Description</span></span> |
| --- | --- |
| <span data-ttu-id="5a1f8-114">$LXUID</span><span class="sxs-lookup"><span data-stu-id="5a1f8-114">$LXUID</span></span> | <span data-ttu-id="5a1f8-115">Besitzer-ID des Benutzers</span><span class="sxs-lookup"><span data-stu-id="5a1f8-115">User Owner ID</span></span> |
| <span data-ttu-id="5a1f8-116">$LXGID</span><span class="sxs-lookup"><span data-stu-id="5a1f8-116">$LXGID</span></span> | <span data-ttu-id="5a1f8-117">Besitzer-ID der Gruppe</span><span class="sxs-lookup"><span data-stu-id="5a1f8-117">Group Owner ID</span></span> |
| <span data-ttu-id="5a1f8-118">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="5a1f8-118">$LXMOD</span></span> | <span data-ttu-id="5a1f8-119">Dateimodus (Dateisystem-Berechtigungsoktale und -typ, z. B.: 0777)</span><span class="sxs-lookup"><span data-stu-id="5a1f8-119">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="5a1f8-120">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="5a1f8-120">$LXDEV</span></span> | <span data-ttu-id="5a1f8-121">Gerät, falls es sich um eine Gerätedatei handelt</span><span class="sxs-lookup"><span data-stu-id="5a1f8-121">Device, if it is a device file</span></span> |

<span data-ttu-id="5a1f8-122">Zusätzlich besitzen alle Dateien, die keine regulären Dateien oder Verzeichnisse sind (z. B. Symlinks, FIFOs, Blockgeräte, Unix-Sockets und Zeichengeräte) ebenfalls einen NTFS-[Analysepunkt](https://docs.microsoft.com/windows/win32/fileio/reparse-points).</span><span class="sxs-lookup"><span data-stu-id="5a1f8-122">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="5a1f8-123">Dadurch lässt sich die Art der Datei in einem bestimmten Verzeichnis viel schneller bestimmen, ohne die erweiterten Attribute abfragen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-123">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span>

## <a name="file-access-scenarios"></a><span data-ttu-id="5a1f8-124">Dateizugriffsszenarien</span><span class="sxs-lookup"><span data-stu-id="5a1f8-124">File Access Scenarios</span></span>

<span data-ttu-id="5a1f8-125">Nachfolgend wird beschrieben, wie Berechtigungen bestimmt werden, wenn auf verschiedene Weise mithilfe des Windows-Subsystems für Linux auf Dateien zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-125">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="5a1f8-126">Zugreifen auf Dateien in Windows Drive File System (DrvFS) von Linux</span><span class="sxs-lookup"><span data-stu-id="5a1f8-126">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="5a1f8-127">Diese Szenarien liegen vor, wenn Sie von WSL aus auf Ihre Windows-Dateien zugreifen, höchstwahrscheinlich über `/mnt/c`.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-127">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span>

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="5a1f8-128">Lesen von Dateiberechtigungen aus einer vorhandenen Windows-Datei</span><span class="sxs-lookup"><span data-stu-id="5a1f8-128">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="5a1f8-129">Das Ergebnis hängt davon ab, ob die Datei bereits über Metadaten verfügt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-129">The result depends on if the file already has existing metadata.</span></span>

##### <a name="drvfs-file-does-not-have-metadata-default"></a><span data-ttu-id="5a1f8-130">DrvFS-Datei enthält keine Metadaten (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a1f8-130">DrvFS file does not have metadata (default)</span></span>

<span data-ttu-id="5a1f8-131">Wenn der Datei keine Metadaten zugeordnet sind, werden die tatsächlichen Berechtigungen des Windows-Benutzers in Lesen/Schreiben/Ausführen-Berechtigungsbits übersetzt und die entsprechenden Wert für Benutzer, Gruppen und andere festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-131">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="5a1f8-132">Wenn Ihr Windows-Benutzerkonto z. B. über Lese- und Ausführungszugriff, aber keinen Schreibzugriff für die Datei verfügt, wird dies als `r-x` für Benutzer, Gruppen und andere angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-132">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="5a1f8-133">Wenn für die Datei das Schreibgeschützt-Attribut in Windows festgelegt ist, wird in Linux kein Schreibzugriff erteilt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-133">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="5a1f8-134">Die Datei enthält Metadaten</span><span class="sxs-lookup"><span data-stu-id="5a1f8-134">The file has metadata</span></span>

<span data-ttu-id="5a1f8-135">Wenn in der Datei Metadaten vorhanden sind, werden anstelle der Übersetzung der tatsächlichen Berechtigungen des Windows-Benutzers einfach diese Metadatenwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-135">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="5a1f8-136">Ändern von Dateiberechtigungen für eine vorhandene Windows-Datei unter Verwendung von „chmod“</span><span class="sxs-lookup"><span data-stu-id="5a1f8-136">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="5a1f8-137">Das Ergebnis hängt davon ab, ob die Datei bereits über Metadaten verfügt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-137">The result depends on if the file already has existing metadata.</span></span>

##### <a name="chmod-file-does-not-have-metadata-default"></a><span data-ttu-id="5a1f8-138">chmod-Datei enthält keine Metadaten (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a1f8-138">chmod file does not have metadata (default)</span></span>

<span data-ttu-id="5a1f8-139">Chmod hat nur einen Effekt: Wenn Sie alle Schreibattribute einer Datei entfernen, wird das Schreibgeschützt-Attribut für die Windows-Datei festgelegt, da dies das gleiche Verhalten wie CIFS (Common Internet File System) ist, das der SMB-Client (Server Message Block) in Linux ist.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-139">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="chmod-file-has-metadata"></a><span data-ttu-id="5a1f8-140">Chmod-Datei enthält Metadaten</span><span class="sxs-lookup"><span data-stu-id="5a1f8-140">chmod file has metadata</span></span>

<span data-ttu-id="5a1f8-141">Chmod bewirkt das Ändern oder Hinzufügen von Metadaten in Abhängigkeit von den bereits vorhandenen Metadaten der Datei.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-141">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="5a1f8-142">Denken Sie daran, dass Sie sich nicht mehr Zugriff erteilen können, als Sie in Windows besitzen, auch wenn die Metadaten dies tun.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-142">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="5a1f8-143">Sie könnten die Metadaten beispielsweise mit `chmod 777` so festlegen, dass Sie Schreibberechtigungen für eine Datei erhalten. Wenn Sie aber versuchen, auf diese Datei zuzugreifen, können Sie trotzdem nicht in diese schreiben.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-143">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="5a1f8-144">Dies ist dank der Interoperabilität möglich, da alle Lese- oder Schreibbefehle für Windows-Dateien über Ihre Windows-Benutzerberechtigungen geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-144">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="5a1f8-145">Erstellen einer Datei in DriveFS</span><span class="sxs-lookup"><span data-stu-id="5a1f8-145">Creating a file in DriveFS</span></span>

<span data-ttu-id="5a1f8-146">Das Ergebnis hängt davon ab, ob Metadaten aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-146">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="5a1f8-147">Metadaten sind nicht aktiviert (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a1f8-147">Metadata is not enabled (default)</span></span>

<span data-ttu-id="5a1f8-148">Die Windows-Berechtigungen der neu erstellten Datei sind identisch wie beim Erstellen der Datei in Windows ohne einen bestimmten Sicherheitsdeskriptor. Sie erben die Berechtigungen des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-148">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span>

##### <a name="metadata-is-enabled"></a><span data-ttu-id="5a1f8-149">Metadaten sind aktiviert</span><span class="sxs-lookup"><span data-stu-id="5a1f8-149">Metadata is enabled</span></span>

<span data-ttu-id="5a1f8-150">Die Berechtigungsbits der Datei sind so festgelegt, dass Sie der Linux-Umask folgen, und die Datei wird mit Metadaten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-150">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="5a1f8-151">Welcher Linux-Benutzer und welche Linux-Gruppe besitzt die Datei?</span><span class="sxs-lookup"><span data-stu-id="5a1f8-151">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="5a1f8-152">Das Ergebnis hängt davon ab, ob die Datei bereits über Metadaten verfügt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-152">The result depends on if the file already has existing metadata.</span></span>

##### <a name="user-file-does-not-have-metadata-default"></a><span data-ttu-id="5a1f8-153">Benutzerdatei enthält keine Metadaten (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a1f8-153">User file does not have metadata (default)</span></span>

<span data-ttu-id="5a1f8-154">Im Standardszenario legen wir beim Automatisieren von Windows-Laufwerken fest, dass die Benutzer-ID (UID) für jede Datei auf die Benutzer-ID des WSL-Benutzers und die Gruppen-ID (GID) auf die Prinzipalgruppen-ID des WSL-Benutzers festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-154">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span>

##### <a name="user-file-has-metadata"></a><span data-ttu-id="5a1f8-155">Benutzerdatei enthält Metadaten</span><span class="sxs-lookup"><span data-stu-id="5a1f8-155">User file has metadata</span></span>

<span data-ttu-id="5a1f8-156">Die in den Metadaten angegebenen UID und GID werden als Benutzerbesitzer und Gruppenbesitzer der Datei angewendet.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-156">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span>

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="5a1f8-157">Zugreifen auf Linux-Dateien von Windows aus mithilfe von `\\wsl$`</span><span class="sxs-lookup"><span data-stu-id="5a1f8-157">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="5a1f8-158">Wenn Sie über `\\wsl$` auf Linux-Dateien zugreifen, wird der Standardbenutzer der WSL-Verteilung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-158">Accessing Linux files via `\\wsl$` will use the default user of your WSL distribution.</span></span> <span data-ttu-id="5a1f8-159">Daher hat jede Windows-App, die auf Linux-Dateien zugreift, dieselben Berechtigungen wie der Standardbenutzer.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-159">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="5a1f8-160">Erstellen einer neuen Datei</span><span class="sxs-lookup"><span data-stu-id="5a1f8-160">Creating a new file</span></span>

<span data-ttu-id="5a1f8-161">Beim Erstellen einer neuen Datei in einer WSL-Verteilung von Windows wird die Standard-Umask angewendet.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-161">The default umask is applied when creating a new file inside of a WSL distribution from Windows.</span></span> <span data-ttu-id="5a1f8-162">Die Standard-Umask ist `022`, d. h., es werden alle Berechtigungen mit Ausnahme von Schreibberechtigungen für Gruppen und andere zugelassen.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-162">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="5a1f8-163">Zugreifen auf Dateien im Linux-Stammdateisystem aus Linux</span><span class="sxs-lookup"><span data-stu-id="5a1f8-163">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="5a1f8-164">Alle Dateien, die im Linux-Stammdateisystem erstellt oder geändert bzw. auf die zugegriffen wird, folgen den Linux-Standardkonventionen, z. B. dass die Umask auf neu erstellte Dateien angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-164">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="5a1f8-165">Konfigurieren von Dateiberechtigungen</span><span class="sxs-lookup"><span data-stu-id="5a1f8-165">Configuring file permissions</span></span>

<span data-ttu-id="5a1f8-166">Sie können Ihre Dateiberechtigungen innerhalb Ihrer Windows-Laufwerke mithilfe der Einbindungsoptionen in „WSL.conf“ konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-166">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="5a1f8-167">Mit den Einbindungsoptionen können Sie `umask`-, `dmask`- und `fmask`-Berechtigungsmasken festlegen.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-167">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="5a1f8-168">Die `umask` wird auf alle Dateien angewendet, die `dmask` wird nur auf Verzeichnisse angewendet, und die `fmask` wird nur auf Dateien angewendet.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-168">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="5a1f8-169">Diese Berechtigungsmasken werden dann durch eine logische ODER-Operation festgelegt, wenn sie auf Dateien angewendet werden. Beispiel: Wenn Sie über einen `umask`-Wert von `023` und einen `fmask`-Wert von `022` verfügen, wird die resultierende Berechtigungsmaske für Dateien auf `023` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a1f8-169">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span>

<span data-ttu-id="5a1f8-170">Anweisungen zur Vorgehensweise finden Sie im Artikel [Konfigurieren von Starteinstellungen mit „wslconf“ für Verteilungen](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf).</span><span class="sxs-lookup"><span data-stu-id="5a1f8-170">Please see the [Configure per distro launch settings with wslconf](./wsl-config.md#configure-per-distro-launch-settings-with-wslconf) article for instructions on how to do this.</span></span>
