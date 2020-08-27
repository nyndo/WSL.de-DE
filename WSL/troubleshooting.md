---
title: Problembehandlung des Windows-Subsystems für Linux
description: Bietet ausführliche Informationen zu häufigen Fehlern und Problemen, die bei der Ausführung von Linux im Windows-Subsystem für Linux auftreten.
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, ubuntu
ms.date: 01/20/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 84aecf4f6111cca47ece3c2421be659fb5a27771
ms.sourcegitcommit: a5534257c236cefeebe86e6b3fc4be0be8fac24e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "88714847"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a><span data-ttu-id="bc6b4-104">Problembehandlung des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="bc6b4-104">Troubleshooting Windows Subsystem for Linux</span></span>

<span data-ttu-id="bc6b4-105">Unterstützung bei Fragen im Zusammenhang mit WSL finden Sie in unserem GitHub-Repository:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-105">For support with issues related to WSL, please see our GitHub repo:</span></span>

## <a name="search-for-any-existing-issues-related-to-your-problem"></a><span data-ttu-id="bc6b4-106">Suchen nach vorhandenen Themen zu Ihrem Problem</span><span class="sxs-lookup"><span data-stu-id="bc6b4-106">Search for any existing issues related to your problem</span></span>

<span data-ttu-id="bc6b4-107">Verwenden Sie für technische Probleme das Produktrepository: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="bc6b4-107">For technical issues, use the product repo: https://github.com/Microsoft/wsl/issues</span></span>

<span data-ttu-id="bc6b4-108">Verwenden Sie für Probleme im Zusammenhang mit dem Inhalt dieser Dokumentation das Dokumentrepository: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="bc6b4-108">For issues related to the contents of this documentation, use the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="submit-a-bug-report"></a><span data-ttu-id="bc6b4-109">Senden eines Fehlerberichts</span><span class="sxs-lookup"><span data-stu-id="bc6b4-109">Submit a bug report</span></span>

<span data-ttu-id="bc6b4-110">Bei Fehlern im Zusammenhang mit WSL-Funktionen oder -Features melden Sie ein Problem im Produktrepository: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="bc6b4-110">For bugs related to WSL functions or features, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="submit-a-feature-request"></a><span data-ttu-id="bc6b4-111">Übermitteln einer Featureanforderung</span><span class="sxs-lookup"><span data-stu-id="bc6b4-111">Submit a feature request</span></span>

<span data-ttu-id="bc6b4-112">Um ein neues Feature im Zusammenhang mit der WSL-Funktionalität oder -Kompatibilität anzufordern, melden Sie ein Problem im Produktrepository: https://github.com/Microsoft/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="bc6b4-112">To request a new feature related to WSL functionality or compatibility, file an issue in the product repo: https://github.com/Microsoft/wsl/issues</span></span>

## <a name="contribute-to-the-docs"></a><span data-ttu-id="bc6b4-113">Beiträge zu den Dokumenten leisten</span><span class="sxs-lookup"><span data-stu-id="bc6b4-113">Contribute to the docs</span></span>

<span data-ttu-id="bc6b4-114">Um einen Beitrag zur WSL-Dokumentation zu leisten, senden Sie ein Pull Request im Dokumentrepository: https://github.com/MicrosoftDocs/wsl/issues</span><span class="sxs-lookup"><span data-stu-id="bc6b4-114">To contribute to the WSL documentation, submit a pull request in the docs repo: https://github.com/MicrosoftDocs/wsl/issues</span></span>

## <a name="terminal-or-command-line"></a><span data-ttu-id="bc6b4-115">Terminal oder Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="bc6b4-115">Terminal or Command Line</span></span>

<span data-ttu-id="bc6b4-116">Wenn sich Ihr Problem auf den Windows-Terminal, die Windows-Konsole oder die Befehlszeilenschnittstelle bezieht, verwenden Sie schließlich das Windows-Terminal-Repository: https://github.com/microsoft/terminal</span><span class="sxs-lookup"><span data-stu-id="bc6b4-116">Lastly, if your issue is related to the Windows Terminal, Windows Console, or the command-line UI, use the Windows terminal repo: https://github.com/microsoft/terminal</span></span>

## <a name="common-issues"></a><span data-ttu-id="bc6b4-117">Allgemeine Probleme</span><span class="sxs-lookup"><span data-stu-id="bc6b4-117">Common issues</span></span>

### <a name="error-0x1bc-when-wsl---set-default-version-2"></a><span data-ttu-id="bc6b4-118">„Fehler: 0x1bc wenn `wsl --set-default-version 2`</span><span class="sxs-lookup"><span data-stu-id="bc6b4-118">Error: 0x1bc when `wsl --set-default-version 2`</span></span>
<span data-ttu-id="bc6b4-119">Dies kann vorkommen, wenn die Einstellung „Anzeigesprache“ oder „Systemgebietsschema“ nicht auf Englisch festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-119">This may happen when 'Display Language' or 'System Locale' setting is not English.</span></span>
```
wsl --set-default-version 2
Error: 0x1bc
For information on key differences with WSL 2 please visit https://aka.ms/wsl2
```

<span data-ttu-id="bc6b4-120">Der tatsächliche Fehler für `0x1bc` lautet:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-120">THe actual error for `0x1bc` is:</span></span>
```
WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel
```

<span data-ttu-id="bc6b4-121">Weitere Informationen finden Sie im Problem [5749](https://github.com/microsoft/WSL/issues/5749).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-121">For more information, please refer to issue [5749](https://github.com/microsoft/WSL/issues/5749)</span></span>


### <a name="cannot-access-wsl-files-from-windows"></a><span data-ttu-id="bc6b4-122">Kein Zugriff auf WSL-Dateien von Windows aus möglich</span><span class="sxs-lookup"><span data-stu-id="bc6b4-122">Cannot access WSL files from Windows</span></span>
<span data-ttu-id="bc6b4-123">Ein 9p-Protokolldateiserver stellt den Dienst auf der Linux-Seite bereit, um Windows den Zugriff auf das Linux-Dateisystem zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-123">A 9p protocol file server provides the service on the Linux side to allow Windows to access the Linux file system.</span></span> <span data-ttu-id="bc6b4-124">Wenn Sie nicht über `\\wsl$` unter Windows auf WSL zugreifen können, kann dies daran liegen, dass 9P nicht ordnungsgemäß gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-124">If you cannot access WSL using `\\wsl$` on Windows, it could be because 9P did not start correctly.</span></span>

<span data-ttu-id="bc6b4-125">Um dies zu überprüfen, können Sie die Startprotokolle mit `dmesg |grep 9p` überprüfen. Dadurch werden Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-125">To check this, you can check the start up logs using: `dmesg |grep 9p`, and this will show you any errors.</span></span> <span data-ttu-id="bc6b4-126">Eine erfolgreiche Ausgabe sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-126">A successfull output looks like the following:</span></span> 

```
[    0.363323] 9p: Installing v9fs 9p2000 file system support
[    0.363336] FS-Cache: Netfs '9p' registered for caching
[    0.398989] 9pnet: Installing 9P2000 support
```

<span data-ttu-id="bc6b4-127">Weitere Informationen zu diesem Problem finden Sie in [diesem GitHub-Thread](https://github.com/microsoft/wsl/issues/5307).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-127">Please see [this Github thread](https://github.com/microsoft/wsl/issues/5307) for further discussion on this issue.</span></span>

### <a name="cant-start-wsl-2-distro-and-only-see-wsl-2-in-output"></a><span data-ttu-id="bc6b4-128">WSL 2-Verteilung kann nicht gestartet werden, und in der Ausgabe wird nur "WSL 2" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-128">Can't start WSL 2 distro and only see 'WSL 2' in output</span></span>
<span data-ttu-id="bc6b4-129">Wenn Ihre Anzeigesprache nicht Englisch ist, sehen Sie möglicherweise eine abgeschnittene Version eines Fehlertexts.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-129">If your display language is not English, then it is possible you are seeing a truncated version of an error text.</span></span>

```powershell
C:\Users\me>wsl
WSL 2
```

<span data-ttu-id="bc6b4-130">Um dieses Problem zu beheben, navigieren Sie zu `https://aka.ms/wsl2kernel`, und installieren Sie den Kernel manuell, indem Sie die Anweisungen auf der doc-Seite befolgen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-130">To resolve this issue, please visit `https://aka.ms/wsl2kernel` and install the kernel manually by following the directions on that doc page.</span></span> 

### <a name="please-enable-the-virtual-machine-platform-windows-feature-and-ensure-virtualization-is-enabled-in-the-bios"></a><span data-ttu-id="bc6b4-131">Aktivieren Sie das Windows-Feature "Virtual Machine Platform", und stellen Sie sicher, dass Virtualisierung im BIOS aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-131">Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.</span></span>

1. <span data-ttu-id="bc6b4-132">Klicken Sie auf [Systemanforderungen von Hyper-V](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-132">Check the [Hyper-V system requirements](https://docs.microsoft.com/windows-server/virtualization/hyper-v/system-requirements-for-hyper-v-on-windows#:~:text=on%20Windows%20Server.-,General%20requirements,the%20processor%20must%20have%20SLAT.)</span></span>
2. <span data-ttu-id="bc6b4-133">Wenn es sich bei dem Computer um einen virtuellen Computer handelt, aktivieren Sie die [geschachtelte Virtualisierung](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manuell.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-133">If your machine is a VM, please enable [nested virtualization](https://docs.microsoft.com/windows/wsl/wsl2-faq#can-i-run-wsl-2-in-a-virtual-machine) manually.</span></span> <span data-ttu-id="bc6b4-134">Starten Sie PowerShell als Administrator, und führen Sie folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-134">Launch powershell with admin, and run:</span></span> 

```powershell
Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true
```

3. <span data-ttu-id="bc6b4-135">Befolgen Sie die Richtlinien des Herstellers Ihres PCs, um zu erfahren, wie Sie die Virtualisierung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-135">Please follow guidelines from your PC's manufacturer on how to enable virtualization.</span></span> <span data-ttu-id="bc6b4-136">Dadurch müssen Sie möglicherweise den System-BIOS verwenden, um sicherzustellen, dass diese Features auf Ihrer CPU aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-136">In general, this can involve using the system BIOS to ensure that these features are enabled on your CPU.</span></span> 
4. <span data-ttu-id="bc6b4-137">Starten Sie den Computer neu, nachdem Sie die optionale `Virtual Machine Platform`-Komponente aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-137">Restart your machine after enabling the `Virtual Machine Platform` optional component.</span></span> 

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a><span data-ttu-id="bc6b4-138">Bash verliert nach dem Herstellen einer Verbindung mit einem VPN die Netzwerkkonnektivität</span><span class="sxs-lookup"><span data-stu-id="bc6b4-138">Bash loses network connectivity once connected to a VPN</span></span>

<span data-ttu-id="bc6b4-139">Wenn Bash nach dem Herstellen einer Verbindung mit einem VPN unter Windows die Netzwerkkonnektivität verliert, können Sie diese Problemumgehung innerhalb von Bash versuchen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-139">If after connecting to a VPN on Windows, bash loses network connectivity, try this workaround from within bash.</span></span> <span data-ttu-id="bc6b4-140">Mit dieser Problemumgehung können Sie die DNS-Auflösung manuell durch `/etc/resolv.conf` außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-140">This workaround will allow you to manually override the DNS resolution through `/etc/resolv.conf`.</span></span>

1. <span data-ttu-id="bc6b4-141">Notieren Sie sich den DNS-Server des VPN (`ipconfig.exe /all`).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-141">Take a note of the DNS server of the VPN from doing `ipconfig.exe /all`</span></span>
2. <span data-ttu-id="bc6b4-142">Erstellen Sie eine Kopie der vorhandenen Datei „resolv.conf“ (`sudo cp /etc/resolv.conf /etc/resolv.conf.new`).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-142">Make a copy of the existing resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`</span></span>
3. <span data-ttu-id="bc6b4-143">Heben Sie die Verknüpfung der aktuellen Datei „resolv.conf“ auf (`sudo unlink /etc/resolv.conf`).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-143">Unlink the current resolv.conf `sudo unlink /etc/resolv.conf`</span></span>
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. <span data-ttu-id="bc6b4-144">Öffnen Sie `/etc/resolv.conf` und</span><span class="sxs-lookup"><span data-stu-id="bc6b4-144">Open `/etc/resolv.conf` and</span></span> <br/>
   <span data-ttu-id="bc6b4-145">ein.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-145">a.</span></span> <span data-ttu-id="bc6b4-146">Löschen Sie die erste Zeile aus der Datei, die Folgendes besagt: „\#This file was automatically generated by WSL.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-146">Delete the first line from the file, which says "\# This file was automatically generated by WSL.</span></span> <span data-ttu-id="bc6b4-147">To stop automatic generation of this file, remove this line.“ (Diese Datei wurde automatisch von WSL generiert. Um die automatische Generierung dieser Datei zu beenden, entfernen Sie diese Zeile.)</span><span class="sxs-lookup"><span data-stu-id="bc6b4-147">To stop automatic generation of this file, remove this line.".</span></span> <br/>
   <span data-ttu-id="bc6b4-148">b.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-148">b.</span></span> <span data-ttu-id="bc6b4-149">Fügen Sie den DNS-Eintrag aus (1) oben als ersten Eintrag in der Liste der DNS-Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-149">Add the DNS entry from (1) above as the very first entry in the list of DNS servers.</span></span> <br/>
   <span data-ttu-id="bc6b4-150">c.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-150">c.</span></span> <span data-ttu-id="bc6b4-151">Schließen Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-151">Close the file.</span></span> <br/>

<span data-ttu-id="bc6b4-152">Nachdem Sie die Verbindung mit dem VPN getrennt haben, müssen Sie die Änderungen auf `/etc/resolv.conf` zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-152">Once you have disconnected the VPN, you will have to revert the changes to `/etc/resolv.conf`.</span></span> <span data-ttu-id="bc6b4-153">Gehen Sie dazu folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-153">To do this, do:</span></span>

1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a><span data-ttu-id="bc6b4-154">Beim Starten von WSL oder beim Installieren einer Distribution wird ein Fehlercode zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="bc6b4-154">Starting WSL or installing a distribution returns an error code</span></span>

<span data-ttu-id="bc6b4-155">Befolgen Sie [diese Anweisungen](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs), um detaillierte Protokolle zu erfassen und ein Issue auf GitHub zu melden.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-155">Follow [these instructions](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs) to collect detailed logs and file an issue on our GitHub.</span></span>

### <a name="updating-bash-on-ubuntu-on-windows"></a><span data-ttu-id="bc6b4-156">Aktualisieren von Bash unter Ubuntu unter Windows</span><span class="sxs-lookup"><span data-stu-id="bc6b4-156">Updating Bash on Ubuntu on Windows</span></span>

<span data-ttu-id="bc6b4-157">Es gibt zwei Komponenten von Bash unter Ubuntu unter Windows, die eine Aktualisierung erfordern.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-157">There are two components of Bash on Ubuntu on Windows that can require updating.</span></span>

1. <span data-ttu-id="bc6b4-158">Das Windows-Subsystem für Linux</span><span class="sxs-lookup"><span data-stu-id="bc6b4-158">The Windows Subsystem for Linux</span></span>
  
   <span data-ttu-id="bc6b4-159">Durch das Upgrade dieses Teils von Bash unter Ubuntu unter Windows werden alle neuen Problembehandlungen aktiviert, die in den [Anmerkungen zu dieser Version](./release-notes.md) beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-159">Upgrading this portion of Bash on Ubuntu on Windows will enable any new fixes outlines in the [release notes](./release-notes.md).</span></span> <span data-ttu-id="bc6b4-160">Stellen Sie sicher, dass Sie das Windows-Insider-Programm abonniert haben und dass Ihr Build auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-160">Ensure that you are subscribed to the Windows Insider Program and that your build is up to date.</span></span> <span data-ttu-id="bc6b4-161">Informationen zu einer genaueren Steuerung (einschließlich des Zurücksetzens der Ubuntu-Instanz) finden Sie auf der [Befehlsreferenzseite](./reference.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-161">For finer grain control including resetting your Ubuntu instance check out the [command reference page](./reference.md).</span></span>

2. <span data-ttu-id="bc6b4-162">Die Ubuntu-Benutzerbinärdateien</span><span class="sxs-lookup"><span data-stu-id="bc6b4-162">The Ubuntu user binaries</span></span>

   <span data-ttu-id="bc6b4-163">Durch das Upgrade dieses Teils von Bash unter Ubuntu unter Windows werden alle Updates der Ubuntu-Benutzerbinärdateien einschließlich der Anwendungen installiert, die Sie über apt-get installiert haben.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-163">Upgrading this portion of Bash on Ubuntu on Windows will install any updates to the Ubuntu user binaries including applications that you have installed via apt-get.</span></span> <span data-ttu-id="bc6b4-164">Führen Sie die folgenden Befehle in Bash aus, um das Update auszuführen:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-164">To update run the following commands in Bash:</span></span>
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a><span data-ttu-id="bc6b4-165">Apt-get-Upgradefehler</span><span class="sxs-lookup"><span data-stu-id="bc6b4-165">Apt-get upgrade errors</span></span>

<span data-ttu-id="bc6b4-166">In einigen Paketen werden Features verwendet, die noch nicht implementiert wurden.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-166">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="bc6b4-167">`udev` wird z.B. noch nicht unterstützt und verursacht mehrere `apt-get upgrade`-Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-167">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="bc6b4-168">Führen Sie die folgenden Schritte aus, um Probleme im Zusammenhang mit `udev` zu beheben:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-168">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="bc6b4-169">Schreiben Sie Folgendes in `/usr/sbin/policy-rc.d`, und speichern Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-169">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>
  
   ```bash
   #!/bin/sh
   exit 101
   ```
  
2. <span data-ttu-id="bc6b4-170">Fügen Sie `/usr/sbin/policy-rc.d` Ausführungsberechtigungen hinzu:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-170">Add execute permissions to `/usr/sbin/policy-rc.d`:</span></span>

   ```bash
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. <span data-ttu-id="bc6b4-171">Führen Sie die folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-171">Run the following commands:</span></span>

   ```bash
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a><span data-ttu-id="bc6b4-172">„Error: 0x80040306“ bei der Installation</span><span class="sxs-lookup"><span data-stu-id="bc6b4-172">"Error: 0x80040306" on installation</span></span>

<span data-ttu-id="bc6b4-173">Dies hat mit der Tatsache zu tun, dass die Legacykonsole nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-173">This has to do with the fact that we do not support legacy console.</span></span>
<span data-ttu-id="bc6b4-174">So deaktivieren Sie die Legacykonsole:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-174">To turn off legacy console:</span></span>

1. <span data-ttu-id="bc6b4-175">Öffnen Sie „cmd. exe“.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-175">Open cmd.exe</span></span>
1. <span data-ttu-id="bc6b4-176">Klicken Sie mit der rechten Maustaste auf der Titelleiste auf „Eigenschaften“. Deaktivieren Sie die Option „Legacykonsole verwenden“.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-176">Right click title bar -> Properties -> Uncheck Use legacy console</span></span>
1. <span data-ttu-id="bc6b4-177">Auf "OK" klicken</span><span class="sxs-lookup"><span data-stu-id="bc6b4-177">Click OK</span></span>

### <a name="error-0x80040154-after-windows-update"></a><span data-ttu-id="bc6b4-178">„Error: 0x80040154“ nach Windows-Update</span><span class="sxs-lookup"><span data-stu-id="bc6b4-178">"Error: 0x80040154" after Windows update</span></span>

<span data-ttu-id="bc6b4-179">Das Feature „Windows-Subsystem für Linux“ ist möglicherweise während eines Windows-Updates deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-179">The Windows Subsystem for Linux feature may be disabled during a Windows update.</span></span> <span data-ttu-id="bc6b4-180">Wenn dies der Fall ist, muss das Windows-Feature erneut aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-180">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="bc6b4-181">Anweisungen zum Aktivieren des Windows-Subsystems für Linux finden Sie im [Installationsleitfaden](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-181">Instructions for enabling the Windows Subsystem for Linux can be found in the [Installation Guide](./install-win10.md).</span></span>

### <a name="changing-the-display-language"></a><span data-ttu-id="bc6b4-182">Ändern der Anzeigesprache</span><span class="sxs-lookup"><span data-stu-id="bc6b4-182">Changing the display language</span></span>

<span data-ttu-id="bc6b4-183">Die WSL-Installation versucht, das Ubuntu-Gebietsschema automatisch so zu ändern, dass es dem Gebietsschema Ihrer Windows-Installation entspricht.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-183">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span>  <span data-ttu-id="bc6b4-184">Wenn Sie dieses Verhalten nicht wünschen, können Sie diesen Befehl ausführen, um das Ubuntu-Gebietsschema zu ändern, nachdem die Installation abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-184">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span>  <span data-ttu-id="bc6b4-185">Sie müssen „bash.exe“ neu starten, damit diese Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-185">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="bc6b4-186">Im folgenden Beispiel wird das Gebietsschema in „en-US“ geändert:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-186">The below example changes to locale to en-US:</span></span>

```bash
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a><span data-ttu-id="bc6b4-187">Installationsprobleme nach der Windows-Systemwiederherstellung</span><span class="sxs-lookup"><span data-stu-id="bc6b4-187">Installation issues after Windows system restore</span></span>

1. <span data-ttu-id="bc6b4-188">Löschen Sie den Ordner `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-188">Delete the `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux` folder.</span></span> <br/>
  <span data-ttu-id="bc6b4-189">**Hinweis: Unterlassen Sie dies, wenn Ihre optionale Funktion vollständig installiert und funktionsfähig ist.**</span><span class="sxs-lookup"><span data-stu-id="bc6b4-189">**Note: Do not do this if your optional feature is fully installed and working.**</span></span>
2. <span data-ttu-id="bc6b4-190">Aktivieren Sie das optionale WSL-Feature (falls noch nicht geschehen).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-190">Enable the WSL optional feature (if not already)</span></span>
3. <span data-ttu-id="bc6b4-191">Neustart</span><span class="sxs-lookup"><span data-stu-id="bc6b4-191">Reboot</span></span>
4. <span data-ttu-id="bc6b4-192">lxrun/uninstall/full</span><span class="sxs-lookup"><span data-stu-id="bc6b4-192">lxrun /uninstall /full</span></span>
5. <span data-ttu-id="bc6b4-193">Installieren von Bash</span><span class="sxs-lookup"><span data-stu-id="bc6b4-193">Install bash</span></span>

### <a name="no-internet-access-in-wsl"></a><span data-ttu-id="bc6b4-194">Kein Internetzugriff in WSL</span><span class="sxs-lookup"><span data-stu-id="bc6b4-194">No internet access in WSL</span></span>

<span data-ttu-id="bc6b4-195">Einige Benutzer haben Probleme mit bestimmten Firewallanwendungen gemeldet, die den Internetzugriff in WSL blockieren.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-195">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span>  <span data-ttu-id="bc6b4-196">Die gemeldeten Firewalls sind:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-196">The firewalls reported are:</span></span>

1. <span data-ttu-id="bc6b4-197">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="bc6b4-197">Kaspersky</span></span>
2. <span data-ttu-id="bc6b4-198">AVG</span><span class="sxs-lookup"><span data-stu-id="bc6b4-198">AVG</span></span>
3. <span data-ttu-id="bc6b4-199">Avast</span><span class="sxs-lookup"><span data-stu-id="bc6b4-199">Avast</span></span>

<span data-ttu-id="bc6b4-200">In einigen Fällen ermöglicht das Deaktivieren der Firewall den Zugriff.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-200">In some cases turning off the firewall allows for access.</span></span>  <span data-ttu-id="bc6b4-201">In einigen Fällen sieht es so aus, als ob bereits die Installation der Firewall den Zugriff blockiert.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-201">In some cases simply having the firewall installed looks to block access.</span></span>

### <a name="permission-denied-error-when-using-ping"></a><span data-ttu-id="bc6b4-202">Fehler des Typs „Berechtigung verweigert“ bei Verwendung von Ping</span><span class="sxs-lookup"><span data-stu-id="bc6b4-202">Permission Denied error when using ping</span></span>

<span data-ttu-id="bc6b4-203">Für [Windows Anniversary Update, Version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), sind **Administratorberechtigungen** in Windows erforderlich, um Ping in WSL auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-203">For [Windows Anniversary Update, version 1607](./release-notes.md#build-14388-to-windows-10-anniversary-update), **administrator privileges** in Windows are required to run ping in WSL.</span></span>  <span data-ttu-id="bc6b4-204">Um Ping auszuführen, führen Sie Bash unter Ubuntu unter Windows als Administrator aus, oder starten Sie „bash.exe“ über eine CMD-/PowerShell-Eingabeaufforderung mit Administratorrechten.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-204">To run ping, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

<span data-ttu-id="bc6b4-205">Für spätere Versionen von Windows, [ab Build 14926](./release-notes.md#build-14926), sind Administratorberechtigungen nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-205">For later versions of Windows, [Build 14926+](./release-notes.md#build-14926), administrator privileges are no longer required.</span></span>

### <a name="bash-is-hung"></a><span data-ttu-id="bc6b4-206">Bash reagiert nicht</span><span class="sxs-lookup"><span data-stu-id="bc6b4-206">Bash is hung</span></span>

<span data-ttu-id="bc6b4-207">Wenn Sie beim Arbeiten mit Bash feststellen, dass Bash hängt (oder blockiert ist) und nicht mehr auf Eingaben reagiert, helfen Sie uns, das Problem zu diagnostizieren, indem Sie ein Speicherabbild erfassen und melden.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-207">If while working with bash, you find that bash is hung (or deadlocked) and not responding to inputs, help us diagnose the issue by collecting and reporting a memory dump.</span></span> <span data-ttu-id="bc6b4-208">Beachten Sie, dass diese Schritte zu einem Absturz Ihres Systems führen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-208">Note that these steps will crash your system.</span></span> <span data-ttu-id="bc6b4-209">Unterlassen Sie dies, wenn Sie damit nicht einverstanden sind, oder speichern Sie Ihre Arbeit zuvor.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-209">Do not do this if you are not comfortable with that or save your work prior to doing this.</span></span>

<span data-ttu-id="bc6b4-210">So erfassen Sie ein Speicherabbild</span><span class="sxs-lookup"><span data-stu-id="bc6b4-210">To collect a memory dump</span></span>

1. <span data-ttu-id="bc6b4-211">Ändern Sie den Typ des Speicherabbilds in „Vollständiges Speicherabbild“.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-211">Change the memory dump type to "complete memory dump".</span></span> <span data-ttu-id="bc6b4-212">Notieren Sie sich den aktuellen Typ, bevor Sie den Speicherabbildtyp ändern.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-212">While changing the dump type, take a note of your current type.</span></span>

2. <span data-ttu-id="bc6b4-213">Verwenden Sie diese [Schritte](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) zum Konfigurieren von Abstürzen mithilfe der Tastatursteuerung.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-213">Use the [steps](https://techcommunity.microsoft.com/t5/Core-Infrastructure-and-Security/How-to-Force-a-Diagnostic-Memory-Dump-When-a-Computer-Hangs/ba-p/257809) to configure crash using keyboard control.</span></span>

3. <span data-ttu-id="bc6b4-214">Reproduzieren Sie das Hängen oder die Blockade.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-214">Repro the hang or deadlock.</span></span>

4. <span data-ttu-id="bc6b4-215">Lassen Sie das System mithilfe der Tastensequenz aus (2) abstürzen.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-215">Crash the system using the key sequence from (2).</span></span>

5. <span data-ttu-id="bc6b4-216">Das System stürzt ab und erfasst das Speicherabbild.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-216">The system will crash and collect the memory dump.</span></span>

6. <span data-ttu-id="bc6b4-217">Nachdem das System neu gestartet wurde, übermitteln Sie die Datei „memory.dmp“ an secure@microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-217">Once the system reboots, report the memory.dmp to secure@microsoft.com.</span></span> <span data-ttu-id="bc6b4-218">Der Standardspeicherort der Speicherabbilddatei ist „%SystemRoot%\memory.dmp“ oder „C:\Windows\memory.dmp“, wenn „C:“ das Systemlaufwerk ist.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-218">The default location of the dump file is %SystemRoot%\memory.dmp or C:\Windows\memory.dmp if C: is the system drive.</span></span> <span data-ttu-id="bc6b4-219">Geben Sie in der E-Mail an, dass das Speicherabbild für das WSL- oder Bash unter Windows-Team vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-219">In the email, note that the dump is for the WSL or Bash on Windows team.</span></span>

7. <span data-ttu-id="bc6b4-220">Stellen Sie die ursprünglichen Einstellung für den Speicherabbildtyp wieder her.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-220">Restore the memory dump type to the original setting.</span></span>

### <a name="check-your-build-number"></a><span data-ttu-id="bc6b4-221">Überprüfen der Buildnummer</span><span class="sxs-lookup"><span data-stu-id="bc6b4-221">Check your build number</span></span>

<span data-ttu-id="bc6b4-222">Um die Architektur des PCs und die Windows-Buildnummer zu ermitteln, öffnen Sie</span><span class="sxs-lookup"><span data-stu-id="bc6b4-222">To find your PC's architecture and Windows build number, open</span></span>  
<span data-ttu-id="bc6b4-223">**Einstellungen** > **System** > **Info**</span><span class="sxs-lookup"><span data-stu-id="bc6b4-223">**Settings** > **System** > **About**</span></span>

<span data-ttu-id="bc6b4-224">Suchen Sie nach den Feldern **Betriebssystembuild** und **Systemtyp**.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-224">Look for the **OS Build** and **System Type** fields.</span></span>  
    <span data-ttu-id="bc6b4-225">![Screenshot der Felder „Betriebssystembuild“ und „Systemtyp“](media/system.png)</span><span class="sxs-lookup"><span data-stu-id="bc6b4-225">![Screenshot of Build and System Type fields](media/system.png)</span></span>

<span data-ttu-id="bc6b4-226">Führen Sie Folgendes in PowerShell aus, um die Windows Server-Buildnummer zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-226">To find your Windows Server build number, run the following in PowerShell:</span></span>  

``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a><span data-ttu-id="bc6b4-227">Bestätigen, dass WSL aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="bc6b4-227">Confirm WSL is enabled</span></span>

<span data-ttu-id="bc6b4-228">Sie können bestätigen, dass das Windows-Subsystem für Linux aktiviert ist, indem Sie Folgendes in PowerShell ausführen:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-228">You can confirm that the Windows Subsystem for Linux is enabled by running the following in PowerShell:</span></span>  

``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a><span data-ttu-id="bc6b4-229">Verbindungsprobleme des OpenSSH-Servers</span><span class="sxs-lookup"><span data-stu-id="bc6b4-229">OpenSSH-Server connection issues</span></span>

<span data-ttu-id="bc6b4-230">Beim Versuch, den SSH-Server zu verbinden, tritt ein Fehler auf: „Connection closed by 127.0.0.1 port 22“ (Verbindung wurde durch 127.0.0.1 Port 22 geschlossen).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-230">Trying to connect your SSH server is failed with the following error: "Connection closed by 127.0.0.1 port 22".</span></span>

1. <span data-ttu-id="bc6b4-231">Stellen Sie sicher, dass der OpenSSH-Server ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-231">Make sure your OpenSSH Server is running:</span></span>

   ```bash
   sudo service ssh status
   ```

   <span data-ttu-id="bc6b4-232">und Sie dieses Tutorial befolgt haben: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span><span class="sxs-lookup"><span data-stu-id="bc6b4-232">and you've followed this tutorial: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en</span></span>

2. <span data-ttu-id="bc6b4-233">Beenden Sie den sshd-Dienst, und starten Sie sshd im Debugmodus:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-233">Stop the sshd service and start sshd in debug mode:</span></span>

   ```bash
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```

3. <span data-ttu-id="bc6b4-234">Überprüfen Sie die Startprotokolle, und stellen Sie sicher, dass HostKeys verfügbar sind und keine Protokollmeldungen wie die folgenden angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-234">Check the startup logs and make sure HostKeys are available and you don't see log messages such as:</span></span>

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

<span data-ttu-id="bc6b4-235">Wenn solche Meldungen angezeigt werden und die Schlüssel unter `/etc/ssh/` fehlen, müssen Sie die Schlüssel neu generieren oder openssh-server einfach bereinigen und installieren:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-235">If you do see such messages and the keys are missing under `/etc/ssh/`, you will have to regenerate the keys or just purge&install openssh-server:</span></span>

```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

### <a name="the-referenced-assembly-could-not-be-found-when-enabling-the-wsl-optional-feature"></a><span data-ttu-id="bc6b4-236">"Die referenzierte Assembly konnte nicht gefunden werden."</span><span class="sxs-lookup"><span data-stu-id="bc6b4-236">"The referenced assembly could not be found."</span></span> <span data-ttu-id="bc6b4-237">beim Aktivieren des optionalen WSL-Features</span><span class="sxs-lookup"><span data-stu-id="bc6b4-237">when enabling the WSL optional feature</span></span>

<span data-ttu-id="bc6b4-238">Dieser Fehler bezieht sich auf einen fehlerhaften Installationsstatus.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-238">This error is related to being in a bad install state.</span></span> <span data-ttu-id="bc6b4-239">Führen Sie die folgenden Schritte aus, um eine Behebung dieses Problems zu versuchen:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-239">Please complete the following steps to try and fix this issue:</span></span>

- <span data-ttu-id="bc6b4-240">Wenn Sie den Befehl zum Aktivieren des WSL-Features aus PowerShell ausführen, versuchen Sie stattdessen, die grafische Benutzeroberfläche zu verwenden, indem Sie das Startmenü öffnen, nach „Windows-Features aktivieren oder deaktivieren“ suchen und dann in der Liste „Windows Subsystem für Linux“ auswählen, wodurch die optionale Komponente installiert wird.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-240">If you are running the enable WSL feature command from PowerShell, try using the GUI instead by opening the start menu, searching for 'Turn Windows features on or off' and then in the list select 'Windows Subsystem for Linux' which will install the optional component.</span></span>

- <span data-ttu-id="bc6b4-241">Aktualisieren Sie Ihre Windows-Version, indem Sie zu „Einstellungen“, „Updates“ wechseln und dann auf „Nach Updates suchen“ klicken</span><span class="sxs-lookup"><span data-stu-id="bc6b4-241">Update your version of Windows by going to Settings, Updates, and clicking 'Check for Updates'</span></span>

- <span data-ttu-id="bc6b4-242">Wenn beide Versuche erfolglos bleiben und Sie auf WSL zugreifen müssen, erwägen Sie, ein lokales Upgrade auszuführen, indem Sie Windows 10 mithilfe der Installationsmedien erneut installieren und „Alles beibehalten“ auswählen, um sicherzustellen, dass Ihre Apps und Dateien erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-242">If both of those fail and you need to access WSL please consider upgrading in place by reinstalling Windows 10 using installation media and selecting 'Keep Everything' to ensure your apps and files are preserved.</span></span> <span data-ttu-id="bc6b4-243">Anweisungen dazu finden Sie auf der Seite [Erneutes Installieren von Windows 10](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-243">You can find instructions on how to do so at the [Reinstall Windows 10 page](https://support.microsoft.com/help/4000735/windows-10-reinstall).</span></span>

### <a name="correct-ssh-related-permission-errors"></a><span data-ttu-id="bc6b4-244">Beheben von (SSH-bezogenen) Berechtigungsfehlern</span><span class="sxs-lookup"><span data-stu-id="bc6b4-244">Correct (SSH related) permission errors</span></span>

<span data-ttu-id="bc6b4-245">Wenn dieser Fehler angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-245">If you're seeing this error:</span></span>

```
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
@         WARNING: UNPROTECTED PRIVATE KEY FILE!          @
@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@@
Permissions 0777 for '/home/artur/.ssh/private-key.pem' are too open.
```

<span data-ttu-id="bc6b4-246">Um dieses Problem zu beheben, fügen Sie Folgendes an die ```/etc/wsl.conf```-Datei an:</span><span class="sxs-lookup"><span data-stu-id="bc6b4-246">To fix this, append the following to the the ```/etc/wsl.conf``` file:</span></span>

```
[automount]
enabled = true
options = metadata,uid=1000,gid=1000,umask=0022
```

<span data-ttu-id="bc6b4-247">Beachten Sie, dass durch Hinzufügen dieses Befehls Metadaten hinzugefügt und die in WSL angezeigten Dateiberechtigungen für die Windows-Dateien geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bc6b4-247">Please note that adding this command will include metadata and modify the file permissions on the Windows files seen from WSL.</span></span> <span data-ttu-id="bc6b4-248">Weitere Informationen finden Sie in den [Dateisystemberechtigungen](./file-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="bc6b4-248">Please see the [File System Permissions](./file-permissions.md) for more information.</span></span>
