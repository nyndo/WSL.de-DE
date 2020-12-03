---
title: Problembehandlung des Windows-Subsystems für Linux
description: Bietet ausführliche Informationen zu häufigen Fehlern und Problemen, die bei der Ausführung von Linux im Windows-Subsystem für Linux auftreten.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 09/28/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: f4040cbe9faf5d55324b56974dd5677052224dd1
ms.sourcegitcommit: d5d3dd8b91e93d46653f9512bceafd8b5340255f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "96443745"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="22395-104">Problembehandlung des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="22395-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="22395-105">Unterstützung bei Fragen im Zusammenhang mit WSL finden Sie in unserem [WSL-Produkt-Repository in GitHub](https://github.com/Microsoft/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="22395-105">For support with issues related to WSL, please see our [WSL product repo on GitHub](https://github.com/Microsoft/wsl/issues).</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="22395-106">Suchen nach vorhandenen Themen zu Ihrem Problem</span><span class="sxs-lookup"><span data-stu-id="22395-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="22395-107">Verwenden Sie für technische Probleme das [Produktrepository](https://github.com/Microsoft/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="22395-107">For technical issues, use the [product repo](https://github.com/Microsoft/wsl/issues).</span></span>

<span data-ttu-id="22395-108">Verwenden Sie für Probleme im Zusammenhang mit dem Inhalt dieser Dokumentation das [Dokumentrepository](https://github.com/MicrosoftDocs/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="22395-108">For issues related to the contents of this documentation, use the [docs repo](https://github.com/MicrosoftDocs/wsl/issues).</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="22395-109">Senden eines Fehlerberichts</span><span class="sxs-lookup"><span data-stu-id="22395-109">Submit a bug report</span></span>

<span data-ttu-id="22395-110">Bei Fehlern im Zusammenhang mit WSL-Funktionen oder -Features melden Sie ein Problem im Produktrepository: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="22395-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="22395-111">Übermitteln einer Featureanforderung</span><span class="sxs-lookup"><span data-stu-id="22395-111">Submit a feature request</span></span>

<span data-ttu-id="22395-112">Um ein neues Feature im Zusammenhang mit der WSL-Funktionalität oder -Kompatibilität anzufordern, [melden Sie ein Problem im Produktrepository](https://github.com/Microsoft/wsl/issues).</span><span class="sxs-lookup"><span data-stu-id="22395-112">To request a new feature related to WSL functionality or compatibility, [file an issue in the product repo](https://github.com/Microsoft/wsl/issues).</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="22395-113">Beiträge zu den Dokumenten leisten</span><span class="sxs-lookup"><span data-stu-id="22395-113">Contribute to the docs</span></span>

<span data-ttu-id="22395-114">Um einen Beitrag zur WSL-Dokumentation zu leisten, senden Sie ein Pull Request im Dokumentrepository: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="22395-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="22395-115">Terminal oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="22395-115">Terminal or Command Line</span></span>

<span data-ttu-id="22395-116">Wenn sich Ihr Problem auf den Windows-Terminal, die Windows-Konsole oder die Befehlszeilenschnittstelle bezieht, verwenden Sie schließlich das Windows-Terminal-Repository: https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="22395-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="22395-117">Allgemeine Probleme</span><span class="sxs-lookup"><span data-stu-id="22395-117">Common issues</span></span>

### <a name="im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2"></a><span data-ttu-id="22395-118">Ich verwende Windows 10, Version 1903, und es werden trotzdem keine Optionen für WSL 2 angezeigt</span><span class="sxs-lookup"><span data-stu-id="22395-118">I'm on Windows 10 version 1903 and I still do not see options for WSL 2</span></span>

<span data-ttu-id="22395-119">Dies liegt wahrscheinlich daran, dass auf Ihrem Computer der Backport für WSL 2 noch nicht eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="22395-119">This is likely because your machine has not yet taken the backport for WSL 2.</span></span> <span data-ttu-id="22395-120">Die einfachste Möglichkeit zur Lösung des Problems besteht darin, zu den Windows-Einstellungen zu wechseln und auf „Nach Updates suchen“ zu klicken, um die neuesten Updates auf Ihrem System zu installieren.</span><span class="sxs-lookup"><span data-stu-id="22395-120">The simplest way to resolve this is by going to Windows Settings and clicking 'Check for Updates' to install the latest updates on your system.</span></span> <span data-ttu-id="22395-121">Schauen Sie sich [die vollständigen Anweisungen zur Einrichtung des Backports finden](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it) an.</span><span class="sxs-lookup"><span data-stu-id="22395-121">See [the full instructions on taking the backport](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span></span>

<span data-ttu-id="22395-122">Wenn Sie auf „Nach Updates suchen“ klicken und das Update immer noch nicht erhalten, können Sie [KB4566116 manuell installieren](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).</span><span class="sxs-lookup"><span data-stu-id="22395-122">If you hit 'Check for Updates' and still do not receive the update you can [install KB KB4566116 manually](https://www.catalog.update.microsoft.com/Search.aspx?q=KB4566116).</span></span>  

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a><span data-ttu-id="22395-123">„Fehler: 0x1bc wenn `wsl --set-default-version 2`</span><span class="sxs-lookup"><span data-stu-id="22395-123">Error: 0x1bc when `wsl --set-default-version 2`</span></span>

<span data-ttu-id="22395-124">Dies kann vorkommen, wenn die Einstellung „Anzeigesprache“ oder „Systemgebietsschema“ nicht auf Englisch festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="22395-124">This may happen when 'Display Language' or 'System Locale' setting is not English.</span></span>

```powershell
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

<span data-ttu-id="22395-125">Der tatsächliche Fehler für `0x1bc` lautet:</span><span class="sxs-lookup"><span data-stu-id="22395-125">THe actual error for `0x1bc` is:</span></span>

```powershell
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

<span data-ttu-id="22395-126">Weitere Informationen finden Sie im Problem [5749](https://github.com/microsoft/WSL/issues/5749).</span><span class="sxs-lookup"><span data-stu-id="22395-126">For more information, please refer to issue [5749](https://github.com/microsoft/WSL/issues/5749)</span></span>

### <a name="cannot-access-wsl-files-from-windows"></a><span data-ttu-id="22395-127">Kein Zugriff auf WSL-Dateien von Windows aus möglich</span><span class="sxs-lookup"><span data-stu-id="22395-127">Cannot access WSL files from Windows</span></span>

<span data-ttu-id="22395-128">Ein 9p-Protokolldateiserver stellt den Dienst auf der Linux-Seite bereit, um Windows den Zugriff auf das Linux-Dateisystem zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="22395-128">A 9p protocol file server provides the service on the Linux side to allow Windows to access the Linux file system.</span></span> <span data-ttu-id="22395-129">Wenn Sie nicht über `\\wsl$` unter Windows auf WSL zugreifen können, kann dies daran liegen, dass 9P nicht ordnungsgemäß gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="22395-129">If you cannot access WSL using `\\wsl$` on Windows, it could be because 9P did not start correctly.</span></span>

<span data-ttu-id="22395-130">Um dies zu überprüfen, können Sie die Startprotokolle mit `dmesg |grep 9p` überprüfen. Dadurch werden Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="22395-130">To check this, you can check the start up logs using: `dmesg |grep 9p`, and this will show you any errors.</span></span> <span data-ttu-id="22395-131">Eine erfolgreiche Ausgabe sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="22395-131">A successfull output looks like the following:</span></span>

```bash
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

<span data-ttu-id="22395-132">Weitere Informationen zu diesem Problem finden Sie in [diesem GitHub-Thread](https://github.com/microsoft/wsl/issues/5307).</span><span class="sxs-lookup"><span data-stu-id="22395-132">Please see [this Github thread](https://github.com/microsoft/wsl/issues/5307) for further discussion on this issue.</span></span>

### <a name="cant-start-wsl-2-distribution-and-only-see-wsl-2-in-output"></a><span data-ttu-id="22395-133">WSL 2-Verteilung kann nicht gestartet werden, und in der Ausgabe wird nur "WSL 2" angezeigt</span><span class="sxs-lookup"><span data-stu-id="22395-133">Can't start WSL 2 distribution and only see 'WSL 2' in output</span></span>

<span data-ttu-id="22395-134">Wenn Ihre Anzeigesprache nicht Englisch ist, sehen Sie möglicherweise eine abgeschnittene Version eines Fehlertexts.</span><span class="sxs-lookup"><span data-stu-id="22395-134">If your display language is not English, then it is possible you are seeing a truncated version of an error text.</span></span>

```powershell
C:\Users\me>wsl
WSL 2
```

<span data-ttu-id="22395-135">Um dieses Problem zu beheben, navigieren Sie zu `https://aka.ms/wsl2kernel`, und installieren Sie den Kernel manuell, indem Sie die Anweisungen auf der doc-Seite befolgen.</span><span class="sxs-lookup"><span data-stu-id="22395-135">To resolve this issue, please visit `https://aka.ms/wsl2kernel` and install the kernel manually by following the directions on that doc page.</span></span> 

### <a name="command-not-found-when-executing-windows-exe-in-linux"></a><span data-ttu-id="22395-136">`command not found` beim Ausführen von „windows.exe“ unter Linux</span><span class="sxs-lookup"><span data-stu-id="22395-136">`command not found` when executing windows .exe in linux</span></span>

<span data-ttu-id="22395-137">Benutzer können ausführbare Windows-Programmdateien wie „notepad.exe“ direkt aus Linux ausführen.</span><span class="sxs-lookup"><span data-stu-id="22395-137">Users can run Windows executables like notepad.exe directly from Linux.</span></span> <span data-ttu-id="22395-138">Manchmal kann es vorkommen, dass "Befehl nicht gefunden" angezeigt wird, wie unten dargestellt:</span><span class="sxs-lookup"><span data-stu-id="22395-138">Sometimes, you may hit "command not found" like below:</span></span> 

```Bash
$ notepad.exe
-bash: notepad.exe: command not found
```

<span data-ttu-id="22395-139">Wenn es keine win32-Pfade in Ihrem $PATH gibt, findet interop die EXE-Datei nicht.</span><span class="sxs-lookup"><span data-stu-id="22395-139">If there are no win32 paths in your $PATH, interop isn't going to find the .exe.</span></span>
<span data-ttu-id="22395-140">Sie können dies überprüfen, indem Sie `echo $PATH` in Linux ausführen.</span><span class="sxs-lookup"><span data-stu-id="22395-140">You can verify it by running `echo $PATH` in Linux.</span></span> <span data-ttu-id="22395-141">In der Ausgabe sollte ein win32-Pfad (z. B. „/mnt/c/Windows“) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="22395-141">It's expected that you will see a win32 path (for example, /mnt/c/Windows) in the output.</span></span>
<span data-ttu-id="22395-142">Werden keine Windows-Pfade angezeigt, wird Ihr PATH höchstwahrscheinlich von Ihrer Linux-Shell außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="22395-142">If you can't see any Windows paths then most likely your PATH is being overwritten by your Linux shell.</span></span> 

<span data-ttu-id="22395-143">Im folgenden Beispiel hat „/etc/profile“ auf Debian zu diesem Problem beigetragen:</span><span class="sxs-lookup"><span data-stu-id="22395-143">Here is a an example that /etc/profile on Debian contributed to the problem:</span></span>

```Bash
if [ "`id -u`" -eq 0 ]; then
  PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin"
else
  PATH="/usr/local/bin:/usr/bin:/bin:/usr/local/games:/usr/games"
fi
```

<span data-ttu-id="22395-144">Die richtige Vorgehensweise unter Debian besteht darin, die obigen Zeilen zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="22395-144">The correct way on Debian is to remove above lines.</span></span>
<span data-ttu-id="22395-145">Sie können auch $PATH während der Zuweisung anhängen, wie unten beschrieben, aber das führt zu einigen [anderen Problemen](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) mit WSL und VSCode.</span><span class="sxs-lookup"><span data-stu-id="22395-145">You may also append $PATH during the assignment like below, but this lead to some [other problems](https://salsa.debian.org/debian/WSL/-/commit/7611edba482fd0b3f67143aa0fc1e2cc1d4100a6) with WSL and VSCode..</span></span>

<span data-ttu-id="22395-146">Weitere Informationen finden Sie unter den Problemen [5296](https://github.com/microsoft/WSL/issues/5296) und [5779](https://github.com/microsoft/WSL/issues/5779).</span><span class="sxs-lookup"><span data-stu-id="22395-146">For more information, see issue [5296](https://github.com/microsoft/WSL/issues/5296) and issue [5779](https://github.com/microsoft/WSL/issues/5779).</span></span>

### <a name="error-0x80370102-the-virtual-machine-could-not-be-started-because-a-required-feature-is-not-installed"></a><span data-ttu-id="22395-147">„Error: 0x80370102 Der virtuelle Computer konnte nicht gestartet werden, weil ein erforderliches Feature nicht installiert ist.“</span><span class="sxs-lookup"><span data-stu-id="22395-147">"Error: 0x80370102 The virtual machine could not be started because a required feature is not installed."</span></span>

<span data-ttu-id="22395-148">Aktivieren Sie das Windows-Feature "Virtual Machine Platform", und stellen Sie sicher, dass Virtualisierung im BIOS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="22395-148">Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</span></span>

1. <span data-ttu-id="22395-149">Klicken Sie auf [Systemanforderungen von Hyper-V](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.).</span><span class="sxs-lookup"><span data-stu-id="22395-149">Check the [Hyper-V system requirements](/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span></span>

2. <span data-ttu-id="22395-150">Wenn es sich bei dem Computer um einen virtuellen Computer handelt, aktivieren Sie die [geschachtelte Virtualisierung](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) manuell.</span><span class="sxs-lookup"><span data-stu-id="22395-150">If your machine is a VM, please enable [nested virtualization](./wsl2-faq.md#can-i-run-wsl-2-in-a-virtual-machine) manually.</span></span> <span data-ttu-id="22395-151">Starten Sie PowerShell als Administrator, und führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="22395-151">Launch powershell with admin, and run:</span></span>

    ```powershell
    Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
    ```

3. <span data-ttu-id="22395-152">Befolgen Sie die Richtlinien des Herstellers Ihres PCs, um zu erfahren, wie Sie die Virtualisierung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="22395-152">Please follow guidelines from your PC's manufacturer on how to enable virtualization.</span></span> <span data-ttu-id="22395-153">Dadurch müssen Sie möglicherweise den System-BIOS verwenden, um sicherzustellen, dass diese Features auf Ihrer CPU aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="22395-153">In general, this can involve using the system BIOS to ensure that these features are enabled on your CPU.</span></span> <span data-ttu-id="22395-154">Die Anweisungen für diesen Prozess können von Computer zu Computer variieren. In [diesem Artikel](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) von Bleeping Computer finden Sie ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="22395-154">Instructions for this process can vary from machine to machine, please see [this article](https://www.bleepingcomputer.com/tutorials/how-to-enable-cpu-virtualization-in-your-computer-bios/) from Bleeping Computer for an example.</span></span>

4. <span data-ttu-id="22395-155">Starten Sie den Computer neu, nachdem Sie die optionale `Virtual Machine Platform`-Komponente aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="22395-155">Restart your machine after enabling the `Virtual Machine Platform` optional component.</span></span>

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="22395-156">Bash verliert nach dem Herstellen einer Verbindung mit einem VPN die Netzwerkkonnektivität</span><span class="sxs-lookup"><span data-stu-id="22395-156">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="22395-157">Wenn Bash nach dem Herstellen einer Verbindung mit einem VPN unter Windows die Netzwerkkonnektivität verliert, können Sie diese Problemumgehung innerhalb von Bash versuchen.</span><span class="sxs-lookup"><span data-stu-id="22395-157">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="22395-158">Mit dieser Problemumgehung können Sie die DNS-Auflösung manuell durch `/etc/resolv.conf` außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="22395-158">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="22395-159">Notieren Sie sich den DNS-Server des VPN (`ipconfig.exe /all`).</span><span class="sxs-lookup"><span data-stu-id="22395-159">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="22395-160">Erstellen Sie eine Kopie der vorhandenen Datei „resolv.conf“ (`sudo cp /etc/resolv.conf /etc/resolv.conf.new`).</span><span class="sxs-lookup"><span data-stu-id="22395-160">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="22395-161">Heben Sie die Verknüpfung der aktuellen Datei „resolv.conf“ auf (`sudo unlink /etc/resolv.conf`).</span><span class="sxs-lookup"><span data-stu-id="22395-161">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="22395-162">Öffnen Sie `/etc/resolv.conf` und</span><span class="sxs-lookup"><span data-stu-id="22395-162">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="22395-163">ein.</span><span class="sxs-lookup"><span data-stu-id="22395-163">a.</span></span> <span data-ttu-id="22395-164">Löschen Sie die erste Zeile aus der Datei, die Folgendes besagt: „\#This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="22395-164">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="22395-165">To stop automatic generation of this file, remove this line.“ (Diese Datei wurde automatisch von WSL generiert. Um die automatische Generierung dieser Datei zu beenden, entfernen Sie diese Zeile.)</span><span class="sxs-lookup"><span data-stu-id="22395-165">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="22395-166">b.</span><span class="sxs-lookup"><span data-stu-id="22395-166">b.</span></span> <span data-ttu-id="22395-167">Fügen Sie den DNS-Eintrag aus (1) oben als ersten Eintrag in der Liste der DNS-Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="22395-167">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="22395-168">c.</span><span class="sxs-lookup"><span data-stu-id="22395-168">c.</span></span> <span data-ttu-id="22395-169">Schließen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="22395-169">Close the file.</span></span> <br/>

<span data-ttu-id="22395-170">Nachdem Sie die Verbindung mit dem VPN getrennt haben, müssen Sie die Änderungen auf `/etc/resolv.conf` zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="22395-170">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="22395-171">Gehen Sie dazu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="22395-171">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="22395-172">Beim Starten von WSL oder beim Installieren einer Distribution wird ein Fehlercode zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="22395-172">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="22395-173">Befolgen Sie [diese Anweisungen](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs), um detaillierte Protokolle zu erfassen und ein Issue auf GitHub zu melden.</span><span class="sxs-lookup"><span data-stu-id="22395-173">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="22395-174">Aktualisieren von Bash unter Ubuntu unter Windows</span><span class="sxs-lookup"><span data-stu-id="22395-174">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="22395-175">Es gibt zwei Komponenten von Bash unter Ubuntu unter Windows, die eine Aktualisierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="22395-175">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="22395-176">Das Windows-Subsystem für Linux</span><span class="sxs-lookup"><span data-stu-id="22395-176">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="22395-177">Durch das Upgrade dieses Teils von Bash unter Ubuntu unter Windows werden alle neuen Problembehandlungen aktiviert, die in den [Anmerkungen zu dieser Version](./release-notes.md) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="22395-177">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="22395-178">Stellen Sie sicher, dass Sie das Windows-Insider-Programm abonniert haben und dass Ihr Build auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="22395-178">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="22395-179">Informationen zu einer genaueren Steuerung (einschließlich des Zurücksetzens der Ubuntu-Instanz) finden Sie auf der [Befehlsreferenzseite](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="22395-179">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="22395-180">Die Ubuntu-Benutzerbinärdateien</span><span class="sxs-lookup"><span data-stu-id="22395-180">The Ubuntu user binaries</span></span>

   <span data-ttu-id="22395-181">Durch das Upgrade dieses Teils von Bash unter Ubuntu unter Windows werden alle Updates der Ubuntu-Benutzerbinärdateien einschließlich der Anwendungen installiert, die Sie über apt-get installiert haben.</span><span class="sxs-lookup"><span data-stu-id="22395-181">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="22395-182">Führen Sie die folgenden Befehle in Bash aus, um das Update auszuführen:</span><span class="sxs-lookup"><span data-stu-id="22395-182">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="22395-183">Apt-get-Upgradefehler</span><span class="sxs-lookup"><span data-stu-id="22395-183">Apt-get upgrade errors</span></span>

<span data-ttu-id="22395-184">In einigen Paketen werden Features verwendet, die noch nicht implementiert wurden.</span><span class="sxs-lookup"><span data-stu-id="22395-184">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="22395-185">`udev` wird z.B. noch nicht unterstützt und verursacht mehrere `apt-get upgrade`-Fehler.</span><span class="sxs-lookup"><span data-stu-id="22395-185">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="22395-186">Führen Sie die folgenden Schritte aus, um Probleme im Zusammenhang mit `udev` zu beheben:</span><span class="sxs-lookup"><span data-stu-id="22395-186">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="22395-187">Schreiben Sie Folgendes in `/usr/sbin/policy-rc.d`, und speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="22395-187">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="22395-188">Fügen Sie `/usr/sbin/policy-rc.d` Ausführungsberechtigungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="22395-188">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="22395-189">Führen Sie die folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="22395-189">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="22395-190">„Error: 0x80040306“ bei der Installation</span><span class="sxs-lookup"><span data-stu-id="22395-190">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="22395-191">Dies hat mit der Tatsache zu tun, dass die Legacykonsole nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="22395-191">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="22395-192">So deaktivieren Sie die Legacykonsole:</span><span class="sxs-lookup"><span data-stu-id="22395-192">To turn off legacy console:</span></span>

1. <span data-ttu-id="22395-193">Öffnen Sie „cmd. exe“.</span><span class="sxs-lookup"><span data-stu-id="22395-193">Open cmd.exe</span></span>
1. <span data-ttu-id="22395-194">Klicken Sie mit der rechten Maustaste auf der Titelleiste auf „Eigenschaften“. Deaktivieren Sie die Option „Legacykonsole verwenden“.</span><span class="sxs-lookup"><span data-stu-id="22395-194">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="22395-195">Auf "OK" klicken</span><span class="sxs-lookup"><span data-stu-id="22395-195">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="22395-196">„Error: 0x80040154“ nach Windows-Update</span><span class="sxs-lookup"><span data-stu-id="22395-196">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="22395-197">Das Feature „Windows-Subsystem für Linux“ ist möglicherweise während eines Windows-Updates deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="22395-197">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="22395-198">Wenn dies der Fall ist, muss das Windows-Feature erneut aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="22395-198">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="22395-199">Anweisungen zum Aktivieren des Windows-Subsystems für Linux finden Sie im [Installationsleitfaden](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="22395-199">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="22395-200">Ändern der Anzeigesprache</span><span class="sxs-lookup"><span data-stu-id="22395-200">Changing the display language</span></span>

<span data-ttu-id="22395-201">Die WSL-Installation versucht, das Ubuntu-Gebietsschema automatisch so zu ändern, dass es dem Gebietsschema Ihrer Windows-Installation entspricht.</span><span class="sxs-lookup"><span data-stu-id="22395-201">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="22395-202">Wenn Sie dieses Verhalten nicht wünschen, können Sie diesen Befehl ausführen, um das Ubuntu-Gebietsschema zu ändern, nachdem die Installation abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="22395-202">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="22395-203">Sie müssen „bash.exe“ neu starten, damit diese Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="22395-203">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="22395-204">Im folgenden Beispiel wird das Gebietsschema in „en-US“ geändert:</span><span class="sxs-lookup"><span data-stu-id="22395-204">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="22395-205">Installationsprobleme nach der Windows-Systemwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="22395-205">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="22395-206">Löschen Sie den Ordner `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="22395-206">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="22395-207">**Hinweis: Unterlassen Sie dies, wenn Ihre optionale Funktion vollständig installiert und funktionsfähig ist.**</span><span class="sxs-lookup"><span data-stu-id="22395-207">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="22395-208">Aktivieren Sie das optionale WSL-Feature (falls noch nicht geschehen).</span><span class="sxs-lookup"><span data-stu-id="22395-208">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="22395-209">Neustart</span><span class="sxs-lookup"><span data-stu-id="22395-209">Reboot</span></span>
4. <span data-ttu-id="22395-210">lxrun/uninstall/full</span><span class="sxs-lookup"><span data-stu-id="22395-210">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="22395-211">Installieren von Bash</span><span class="sxs-lookup"><span data-stu-id="22395-211">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="22395-212">Kein Internetzugriff in WSL</span><span class="sxs-lookup"><span data-stu-id="22395-212">No internet access in WSL</span></span>

<span data-ttu-id="22395-213">Einige Benutzer haben Probleme mit bestimmten Firewallanwendungen gemeldet, die den Internetzugriff in WSL blockieren.</span><span class="sxs-lookup"><span data-stu-id="22395-213">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="22395-214">Die gemeldeten Firewalls sind:</span><span class="sxs-lookup"><span data-stu-id="22395-214">The firewalls reported are:</span></span>

1. <span data-ttu-id="22395-215">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="22395-215">Kaspersky</span></span>
2. <span data-ttu-id="22395-216">AVG</span><span class="sxs-lookup"><span data-stu-id="22395-216">AVG</span></span>
3. <span data-ttu-id="22395-217">Avast</span><span class="sxs-lookup"><span data-stu-id="22395-217">Avast</span></span>

<span data-ttu-id="22395-218">In einigen Fällen ermöglicht das Deaktivieren der Firewall den Zugriff.</span><span class="sxs-lookup"><span data-stu-id="22395-218">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="22395-219">In einigen Fällen sieht es so aus, als ob bereits die Installation der Firewall den Zugriff blockiert.</span><span class="sxs-lookup"><span data-stu-id="22395-219">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="22395-220">Fehler des Typs „Berechtigung verweigert“ bei Verwendung von Ping</span><span class="sxs-lookup"><span data-stu-id="22395-220">Permission Denied error when using ping</span></span>

<span data-ttu-id="22395-221">Für [Windows Anniversary Update, Version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), sind **Administratorberechtigungen** in Windows erforderlich, um Ping in WSL auszuführen.</span><span class="sxs-lookup"><span data-stu-id="22395-221">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="22395-222">Um Ping auszuführen, führen Sie Bash unter Ubuntu unter Windows als Administrator aus, oder starten Sie „bash.exe“ über eine CMD-/PowerShell-Eingabeaufforderung mit Administratorrechten.</span><span class="sxs-lookup"><span data-stu-id="22395-222">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="22395-223">Für spätere Versionen von Windows, [ab Build 14926](./release-notes.md#build-14926), sind Administratorberechtigungen nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22395-223">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="22395-224">Bash reagiert nicht</span><span class="sxs-lookup"><span data-stu-id="22395-224">Bash is hung</span></span>

<span data-ttu-id="22395-225">Wenn Sie beim Arbeiten mit Bash feststellen, dass Bash hängt (oder blockiert ist) und nicht mehr auf Eingaben reagiert, helfen Sie uns, das Problem zu diagnostizieren, indem Sie ein Speicherabbild erfassen und melden.</span><span class="sxs-lookup"><span data-stu-id="22395-225">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="22395-226">Beachten Sie, dass diese Schritte zu einem Absturz Ihres Systems führen.</span><span class="sxs-lookup"><span data-stu-id="22395-226">Note that these steps will crash your system.</span></span> <span data-ttu-id="22395-227">Unterlassen Sie dies, wenn Sie damit nicht einverstanden sind, oder speichern Sie Ihre Arbeit zuvor.</span><span class="sxs-lookup"><span data-stu-id="22395-227">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="22395-228">So erfassen Sie ein Speicherabbild</span><span class="sxs-lookup"><span data-stu-id="22395-228">To collect a memory dump</span></span>

1. <span data-ttu-id="22395-229">Ändern Sie den Typ des Speicherabbilds in „Vollständiges Speicherabbild“.</span><span class="sxs-lookup"><span data-stu-id="22395-229">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="22395-230">Notieren Sie sich den aktuellen Typ, bevor Sie den Speicherabbildtyp ändern.</span><span class="sxs-lookup"><span data-stu-id="22395-230">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="22395-231">Verwenden Sie diese [Schritte](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) zum Konfigurieren von Abstürzen mithilfe der Tastatursteuerung.</span><span class="sxs-lookup"><span data-stu-id="22395-231">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="22395-232">Reproduzieren Sie das Hängen oder die Blockade.</span><span class="sxs-lookup"><span data-stu-id="22395-232">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="22395-233">Lassen Sie das System mithilfe der Tastensequenz aus (2) abstürzen.</span><span class="sxs-lookup"><span data-stu-id="22395-233">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="22395-234">Das System stürzt ab und erfasst das Speicherabbild.</span><span class="sxs-lookup"><span data-stu-id="22395-234">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="22395-235">Nachdem das System neu gestartet wurde, übermitteln Sie die Datei „memory.dmp“ an secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="22395-235">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="22395-236">Der Standardspeicherort der Speicherabbilddatei ist „%SystemRoot%\memory.dmp“ oder „C:\Windows\memory.dmp“, wenn „C:“ das Systemlaufwerk ist.</span><span class="sxs-lookup"><span data-stu-id="22395-236">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="22395-237">Geben Sie in der E-Mail an, dass das Speicherabbild für das WSL- oder Bash unter Windows-Team vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="22395-237">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="22395-238">Stellen Sie die ursprünglichen Einstellung für den Speicherabbildtyp wieder her.</span><span class="sxs-lookup"><span data-stu-id="22395-238">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="22395-239">Überprüfen der Buildnummer</span><span class="sxs-lookup"><span data-stu-id="22395-239">Check your build number</span></span>

<span data-ttu-id="22395-240">Um die Architektur des PCs und die Windows-Buildnummer zu ermitteln, öffnen Sie</span><span class="sxs-lookup"><span data-stu-id="22395-240">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="22395-241">**Einstellungen** > **System** > **Info**</span><span class="sxs-lookup"><span data-stu-id="22395-241">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="22395-242">Suchen Sie nach den Feldern **Betriebssystembuild** und **Systemtyp**.</span><span class="sxs-lookup"><span data-stu-id="22395-242">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="22395-243">![Screenshot der Felder „Betriebssystembuild“ und „Systemtyp“](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="22395-243">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="22395-244">Führen Sie Folgendes in PowerShell aus, um die Windows Server-Buildnummer zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="22395-244">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="22395-245">Bestätigen, dass WSL aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="22395-245">Confirm WSL is enabled</span></span>

<span data-ttu-id="22395-246">Sie können bestätigen, dass das Windows-Subsystem für Linux aktiviert ist, indem Sie Folgendes in PowerShell ausführen:</span><span class="sxs-lookup"><span data-stu-id="22395-246">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="22395-247">Verbindungsprobleme des OpenSSH-Servers</span><span class="sxs-lookup"><span data-stu-id="22395-247">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="22395-248">Beim Versuch, den SSH-Server zu verbinden, tritt ein Fehler auf: „Connection closed by 127.0.0.1 port 22“ (Verbindung wurde durch 127.0.0.1 Port 22 geschlossen).</span><span class="sxs-lookup"><span data-stu-id="22395-248">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="22395-249">Stellen Sie sicher, dass der OpenSSH-Server ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="22395-249">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="22395-250">und Sie dieses Tutorial befolgt haben: https://ubuntu.com/server/docs/service-openssh</span><span class="sxs-lookup"><span data-stu-id="22395-250">and you've followed this tutorial: https://ubuntu.com/server/docs/service-openssh</span></span>

2. <span data-ttu-id="22395-251">Beenden Sie den sshd-Dienst, und starten Sie sshd im Debugmodus:</span><span class="sxs-lookup"><span data-stu-id="22395-251">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="22395-252">Überprüfen Sie die Startprotokolle, und stellen Sie sicher, dass HostKeys verfügbar sind und keine Protokollmeldungen wie die folgenden angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="22395-252">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

   ```BASH
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

<span data-ttu-id="22395-253">Wenn solche Meldungen angezeigt werden und die Schlüssel unter `/etc/ssh/` fehlen, müssen Sie die Schlüssel neu generieren oder openssh-server einfach bereinigen und installieren:</span><span class="sxs-lookup"><span data-stu-id="22395-253">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="22395-254">"Die referenzierte Assembly konnte nicht gefunden werden."</span><span class="sxs-lookup"><span data-stu-id="22395-254">"The referenced assembly could not be found."</span></span> <span data-ttu-id="22395-255">beim Aktivieren des optionalen WSL-Features</span><span class="sxs-lookup"><span data-stu-id="22395-255">when enabling the WSL optional feature</span></span>

<span data-ttu-id="22395-256">Dieser Fehler bezieht sich auf einen fehlerhaften Installationsstatus.</span><span class="sxs-lookup"><span data-stu-id="22395-256">This error is related to being in a bad install state.</span></span> <span data-ttu-id="22395-257">Führen Sie die folgenden Schritte aus, um eine Behebung dieses Problems zu versuchen:</span><span class="sxs-lookup"><span data-stu-id="22395-257">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="22395-258">Wenn Sie den Befehl zum Aktivieren des WSL-Features aus PowerShell ausführen, versuchen Sie stattdessen, die grafische Benutzeroberfläche zu verwenden, indem Sie das Startmenü öffnen, nach „Windows-Features aktivieren oder deaktivieren“ suchen und dann in der Liste „Windows Subsystem für Linux“ auswählen, wodurch die optionale Komponente installiert wird.</span><span class="sxs-lookup"><span data-stu-id="22395-258">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="22395-259">Aktualisieren Sie Ihre Windows-Version, indem Sie zu „Einstellungen“, „Updates“ wechseln und dann auf „Nach Updates suchen“ klicken</span><span class="sxs-lookup"><span data-stu-id="22395-259">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="22395-260">Wenn beide Versuche erfolglos bleiben und Sie auf WSL zugreifen müssen, erwägen Sie, ein lokales Upgrade auszuführen, indem Sie Windows 10 mithilfe der Installationsmedien erneut installieren und „Alles beibehalten“ auswählen, um sicherzustellen, dass Ihre Apps und Dateien erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="22395-260">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="22395-261">Anweisungen dazu finden Sie auf der Seite [Erneutes Installieren von Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="22395-261">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="22395-262">Beheben von (SSH-bezogenen) Berechtigungsfehlern</span><span class="sxs-lookup"><span data-stu-id="22395-262">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="22395-263">Wenn dieser Fehler angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="22395-263">If you're seeing this error:</span></span>

```bash
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="22395-264">Um dieses Problem zu beheben, fügen Sie Folgendes an die ```/etc/wsl.conf```-Datei an:</span><span class="sxs-lookup"><span data-stu-id="22395-264">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```bash
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="22395-265">Beachten Sie, dass durch Hinzufügen dieses Befehls Metadaten hinzugefügt und die in WSL angezeigten Dateiberechtigungen für die Windows-Dateien geändert werden.</span><span class="sxs-lookup"><span data-stu-id="22395-265">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="22395-266">Weitere Informationen finden Sie in den [Dateisystemberechtigungen](./file-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="22395-266">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>

### <a name="running-windows-commands-fails-inside-a-distribution"></a><span data-ttu-id="22395-267">Fehler beim Ausführen von Windows-Befehlen innerhalb einer Verteilung</span><span class="sxs-lookup"><span data-stu-id="22395-267">Running Windows commands fails inside a distribution</span></span>

<span data-ttu-id="22395-268">Einige [im Microsoft Store verfügbare](install-win10.md#step-6---install-your-linux-distribution-of-choice) Verteilungen sind noch nicht vollständig kompatibel, um Windows-Befehle sofort in [Terminal](https://en.wikipedia.org/wiki/Linux_console) auszuführen.</span><span class="sxs-lookup"><span data-stu-id="22395-268">Some distributions [available in Microsoft Store](install-win10.md#step-6---install-your-linux-distribution-of-choice) are yet not fully compatible to run Windows commands in [Terminal](https://en.wikipedia.org/wiki/Linux_console) out of the box.</span></span> <span data-ttu-id="22395-269">Wenn Sie beim Ausführen von `powershell.exe /c start .` oder eines anderen Windows-Befehls der Fehler `-bash: powershell.exe: command not found` angezeigt wird, können Sie ihn mit den folgenden Schritten beheben:</span><span class="sxs-lookup"><span data-stu-id="22395-269">If you get an error `-bash: powershell.exe: command not found` running `powershell.exe /c start .` or any other Windows command, you can resolve it following these steps:</span></span>

1. <span data-ttu-id="22395-270">Führen Sie `echo $PATH` in Ihrer WSL-Verteilung aus.</span><span class="sxs-lookup"><span data-stu-id="22395-270">In your WSL distribution run `echo $PATH`.</span></span>  
   <span data-ttu-id="22395-271">Wenn `/mnt/c/Windows/system32` nicht enthalten ist, wird die PATH-Standardvariable von irgendeiner Komponente neu definiert.</span><span class="sxs-lookup"><span data-stu-id="22395-271">If it does not include: `/mnt/c/Windows/system32` something is redefining the standard PATH variable.</span></span>
2. <span data-ttu-id="22395-272">Prüfen Sie die Profileinstellungen mit `cat /etc/profile`.</span><span class="sxs-lookup"><span data-stu-id="22395-272">Check profile settings with `cat /etc/profile`.</span></span>  
   <span data-ttu-id="22395-273">Ist die Zuweisung der PATH-Variablen enthalten, bearbeiten Sie die Datei, um den PATH-Zuweisungsblock mit einem **#** -Zeichen auszukommentieren.</span><span class="sxs-lookup"><span data-stu-id="22395-273">If it contains assignment of the PATH variable, edit the file to comment out PATH assignment block with a **#** character.</span></span>
3. <span data-ttu-id="22395-274">Prüfen Sie, ob „wsl.conf“ vorhanden ist (`cat /etc/wsl.conf`), und stellen Sie sicher, dass `appendWindowsPath=false` nicht enthalten ist. Andernfalls kommentieren Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="22395-274">Check if wsl.conf is present `cat /etc/wsl.conf` and make sure it does not contain `appendWindowsPath=false`, otherwise comment it out.</span></span>
4. <span data-ttu-id="22395-275">Starten Sie die Verteilung neu, indem Sie `wsl -t ` eingeben, gefolgt vom Namen der Verteilung, oder indem Sie `wsl --shutdown` entweder in cmd oder PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="22395-275">Restart distribution by typing `wsl -t ` followed by distribution name or run `wsl --shutdown` either in cmd or PowerShell.</span></span>

### <a name="unable-to-boot-after-installing-wsl-2"></a><span data-ttu-id="22395-276">Starten nach der Installation von WSL 2 nicht möglich</span><span class="sxs-lookup"><span data-stu-id="22395-276">Unable to boot after installing WSL 2</span></span>

<span data-ttu-id="22395-277">Es ist ein Problem bekannt, das Benutzer betrifft, wenn Sie nach der Installation von WSL 2 nicht starten können.</span><span class="sxs-lookup"><span data-stu-id="22395-277">We are aware of an issue affecting users where they are unable to boot after installing WSL 2.</span></span> <span data-ttu-id="22395-278">Während unserer umfassenden Diagnose dieser Probleme haben Benutzer berichtet, dass [das Ändern der Puffergröße](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363) oder [das Installieren der richtigen Treiber](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244) helfen kann, dieses Problem zu beheben.</span><span class="sxs-lookup"><span data-stu-id="22395-278">While we fully diagnose those issue, users have reported that [changing the buffer size](https://github.com/microsoft/WSL/issues/4784#issuecomment-639219363) or [installing the right drivers](https://github.com/microsoft/WSL/issues/4784#issuecomment-675702244) can help address this.</span></span> <span data-ttu-id="22395-279">Im folgenden [GitHub-Artikel](https://github.com/microsoft/WSL/issues/4784) finden Sie die neuesten Updates zu diesem Problem.</span><span class="sxs-lookup"><span data-stu-id="22395-279">Please view this [Github issue](https://github.com/microsoft/WSL/issues/4784) to see the latest updates on this issue.</span></span> 
