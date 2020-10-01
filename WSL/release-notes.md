---
title: Anmerkungen zu dieser Version des Windows-Subsystems für Linux
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux. Diese Versionsanmerkungen enthalten behobene Probleme und werden wöchentlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: d7b868f959c62879524dcbdad20509ef35fecfce
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413271"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="9b657-105">Anmerkungen zu dieser Version des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="9b657-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-20211"></a><span data-ttu-id="9b657-106">Build 20211</span><span class="sxs-lookup"><span data-stu-id="9b657-106">Build 20211</span></span>
<span data-ttu-id="9b657-107">Allgemeine Windows-Informationen zu Build 20211 finden Sie im [Windows-Blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).</span><span class="sxs-lookup"><span data-stu-id="9b657-107">For general Windows information on build 20211 visit the [Windows blog](https://blogs.windows.com/windows-insider/2020/09/10/announcing-windows-10-insider-preview-build-20211/).</span></span>

* <span data-ttu-id="9b657-108">Stellen Sie `wsl.exe --mount` bereit, um physische oder virtuelle Datenträger bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9b657-108">Introduce `wsl.exe --mount` for mounting physical or virtual disks.</span></span> <span data-ttu-id="9b657-109">Weitere Informationen finden Sie unter [Zugreifen auf Linux-Dateisysteme in Windows und WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).</span><span class="sxs-lookup"><span data-stu-id="9b657-109">For more information see [Access Linux filesystems in Windows and WSL 2](https://devblogs.microsoft.com/commandline/access-linux-filesystems-in-windows-and-wsl-2/).</span></span>
* <span data-ttu-id="9b657-110">Fix für den Absturz des LxssManager-Diensts beim Überprüfen, ob die VM im Leerlauf ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-110">Fix crash in LxssManager service when checking if the VM is idle.</span></span> <span data-ttu-id="9b657-111">[GH 5768]</span><span class="sxs-lookup"><span data-stu-id="9b657-111">[GH 5768]</span></span>
* <span data-ttu-id="9b657-112">Unterstützung für komprimierte VHD-Dateien.</span><span class="sxs-lookup"><span data-stu-id="9b657-112">Support for compressed VHD files.</span></span> <span data-ttu-id="9b657-113">[GH 4103]</span><span class="sxs-lookup"><span data-stu-id="9b657-113">[GH 4103]</span></span>
* <span data-ttu-id="9b657-114">Stellen Sie sicher, dass die unter „C:\windows\system32\lxss\lib“ installierte Linux-Benutzermodusbibliotheken bei Betriebssystemupgrades erhalten bleiben.</span><span class="sxs-lookup"><span data-stu-id="9b657-114">Ensure that Linux user mode libs installed to c:\windows\system32\lxss\lib are preserved across OS upgrade.</span></span> <span data-ttu-id="9b657-115">[GH 5848]</span><span class="sxs-lookup"><span data-stu-id="9b657-115">[GH 5848]</span></span>
* <span data-ttu-id="9b657-116">Die Möglichkeit zum Auflisten verfügbarer Verteilungen, die mit `wsl --install --list-distributions` installiert werden können, wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b657-116">Added the ability to list available distributions that can be installed with `wsl --install --list-distributions`.</span></span>
* <span data-ttu-id="9b657-117">WSL-Instanzen werden nun beendet, wenn sich der Benutzer abmeldet.</span><span class="sxs-lookup"><span data-stu-id="9b657-117">WSL instances are now terminated when the user logs off.</span></span>

## <a name="build-20190"></a><span data-ttu-id="9b657-118">Build 20190</span><span class="sxs-lookup"><span data-stu-id="9b657-118">Build 20190</span></span>
<span data-ttu-id="9b657-119">Allgemeine Windows-Informationen zu Build 20190 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).</span><span class="sxs-lookup"><span data-stu-id="9b657-119">For general Windows information on build 20190 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/08/12/announcing-windows-10-insider-preview-build-20190/).</span></span>

* <span data-ttu-id="9b657-120">Fehler behoben, der den Start von WSL1-Instanzen verhinderte.</span><span class="sxs-lookup"><span data-stu-id="9b657-120">Fix bug preventing WSL1 instances from launching.</span></span> <span data-ttu-id="9b657-121">[GH 5633]</span><span class="sxs-lookup"><span data-stu-id="9b657-121">[GH 5633]</span></span>
* <span data-ttu-id="9b657-122">Hängenbleiben beim Umleiten der Windows-Prozessausgabe behoben.</span><span class="sxs-lookup"><span data-stu-id="9b657-122">Fix hang when redirecting Windows process output.</span></span> <span data-ttu-id="9b657-123">[GH 5648]</span><span class="sxs-lookup"><span data-stu-id="9b657-123">[GH 5648]</span></span>
* <span data-ttu-id="9b657-124">Option „%userprofile%\\.wslconfig“ zur Steuerung des VM-Leerlauftimeouts (wsl2.vmIdleTimeout=<Zeit_in_ms>) hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b657-124">Add %userprofile%\\.wslconfig option to control the VM idle timeout (wsl2.vmIdleTimeout=<time_in_ms>).</span></span>
* <span data-ttu-id="9b657-125">Unterstützung für das Starten von App-Ausführungsaliasen von WSL.</span><span class="sxs-lookup"><span data-stu-id="9b657-125">Support launching app execution aliases from WSL.</span></span>
* <span data-ttu-id="9b657-126">Unterstützung für die Installation des WSL2-Kernels und der Verteilungen zu „wsl.exe --install“ hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9b657-126">Added support for installing the WSL2 kernel and distributions to wsl.exe --install.</span></span>

## <a name="build-20175"></a><span data-ttu-id="9b657-127">Build 20175</span><span class="sxs-lookup"><span data-stu-id="9b657-127">Build 20175</span></span>
<span data-ttu-id="9b657-128">Allgemeine Windows-Informationen zu Build 20175 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).</span><span class="sxs-lookup"><span data-stu-id="9b657-128">For general Windows information on build 20175 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/07/22/announcing-windows-10-insider-preview-build-20175/).</span></span>

* <span data-ttu-id="9b657-129">Passen Sie die Standardspeicherzuweisung der WSL2-VM so an, dass sie 50 % des Hostspeichers oder 8 GB beträgt, je nachdem, welcher Wert kleiner ist [GH 4166].</span><span class="sxs-lookup"><span data-stu-id="9b657-129">Adjust default memory assignment of WSL2 VM to be 50% of host memory or 8GB, whichever is less [GH 4166].</span></span>
* <span data-ttu-id="9b657-130">Ändern Sie das \\\\wsl$-Präfix in \\\\wsl, um die URI-Analyse zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9b657-130">Change \\\\wsl$ prefix to \\\\wsl to support URI parsing.</span></span> <span data-ttu-id="9b657-131">Der alte \\\\wsl$-Pfad wird weiterhin unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-131">The old \\\\wsl$ path is still supported.</span></span>
* <span data-ttu-id="9b657-132">Aktivieren Sie die geschachtelte Virtualisierung für WSL2 standardmäßig auf amd64.</span><span class="sxs-lookup"><span data-stu-id="9b657-132">Enable nested virtualization for WSL2 by default on amd64.</span></span> <span data-ttu-id="9b657-133">Sie können dies über „%userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false)“ deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-133">You can disable this via %userprofile%\\.wslconfig ([wsl2] nestedVirtualization=false).</span></span>
* <span data-ttu-id="9b657-134">Lassen Sie die wsl.exe --update-Anforderung Microsoft Update starten.</span><span class="sxs-lookup"><span data-stu-id="9b657-134">Make wsl.exe --update demand start Microsoft Update.</span></span>
* <span data-ttu-id="9b657-135">Unterstützen Sie die Umbenennung über eine schreibgeschützte Datei in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9b657-135">Support renaming over a read-only file in DrvFs.</span></span>
* <span data-ttu-id="9b657-136">Stellen Sie sicher, dass Fehlermeldungen immer in der richtigen Codepage ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-136">Ensure error messages are always printed in the correct codepage.</span></span>

## <a name="build-20150"></a><span data-ttu-id="9b657-137">Build 20150</span><span class="sxs-lookup"><span data-stu-id="9b657-137">Build 20150</span></span>
<span data-ttu-id="9b657-138">Allgemeine Windows-Informationen zu Build 20150 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="9b657-138">For general Windows information on build 20150 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span></span>

* <span data-ttu-id="9b657-139">Informationen zu WSL2 GPU Compute finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="9b657-139">WSL2 GPU compute see [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/) for more information.</span></span>
* <span data-ttu-id="9b657-140">Führen Sie die Befehlszeilenoption „wsl.exe --install“ zum einfachen Einrichten von WSL ein.</span><span class="sxs-lookup"><span data-stu-id="9b657-140">Introduce wsl.exe --install command line option to easily set up WSL.</span></span>
* <span data-ttu-id="9b657-141">Führen Sie die Befehlszeilenoption „wsl.exe --update“ zum Verwalten von Updates für den WSL2-Kernel ein.</span><span class="sxs-lookup"><span data-stu-id="9b657-141">Introduce wsl.exe --update command line option to manage updates to the WSL2 kernel.</span></span> 
* <span data-ttu-id="9b657-142">Legen Sie WSL2 als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="9b657-142">Set WSL2 as the default.</span></span>
* <span data-ttu-id="9b657-143">Erhöhen Sie das Timeout für das kontrollierte Beenden der WSL2-VM.</span><span class="sxs-lookup"><span data-stu-id="9b657-143">Increase WSL2 vm graceful shutdown timeout.</span></span>
* <span data-ttu-id="9b657-144">Korrigieren Sie die virtio-9p-Racebedingung beim Zuordnen des Gerätespeichers.</span><span class="sxs-lookup"><span data-stu-id="9b657-144">Fix virtio-9p race condition when mapping device memory.</span></span>
* <span data-ttu-id="9b657-145">Führen Sie keinen 9p-Server mit erhöhten Rechten aus, wenn UAC deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-145">Don't run an elevated 9p server if UAC is disabled.</span></span>

## <a name="build-19640"></a><span data-ttu-id="9b657-146">Build 19640</span><span class="sxs-lookup"><span data-stu-id="9b657-146">Build 19640</span></span>
<span data-ttu-id="9b657-147">Allgemeine Windows-Informationen zu Build 19640 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span><span class="sxs-lookup"><span data-stu-id="9b657-147">For general Windows information on build 19640 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span></span>

* <span data-ttu-id="9b657-148">[WSL2] Stabilitätsverbesserungen für virtio-9p (drvfs).</span><span class="sxs-lookup"><span data-stu-id="9b657-148">[WSL2] Stability improvements for virtio-9p (drvfs).</span></span>

## <a name="build-19555"></a><span data-ttu-id="9b657-149">Build 19555</span><span class="sxs-lookup"><span data-stu-id="9b657-149">Build 19555</span></span>
<span data-ttu-id="9b657-150">Allgemeine Windows-Informationen zu Build 19555 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span><span class="sxs-lookup"><span data-stu-id="9b657-150">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="9b657-151">[WSL2] Verwenden einer Arbeitsspeicher-cgroup, um den von Installations- und Konvertierungsvorgängen verwendeten Speicherplatz zu begrenzen [GH 4669]</span><span class="sxs-lookup"><span data-stu-id="9b657-151">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="9b657-152">Verfügbarmachen von „wsl.exe“, wenn die optionale Komponente „Windows-Subsystem für Linux“ (WSL) nicht aktiviert ist, um die Auffindbarkeit von Features zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="9b657-152">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="9b657-153">Ändern von „wsl.exe“, um Hilfetext auszugeben, wenn die optionale Komponente WSL nicht installiert ist</span><span class="sxs-lookup"><span data-stu-id="9b657-153">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="9b657-154">Fehlerbehebung für die Racebedingung beim Erstellen von Instanzen</span><span class="sxs-lookup"><span data-stu-id="9b657-154">Fix race condition when creating instances</span></span>
* <span data-ttu-id="9b657-155">Erstellen von „wslclient.dll“ mit allen Befehlszeilenfunktionen</span><span class="sxs-lookup"><span data-stu-id="9b657-155">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="9b657-156">Verhindern eines Absturzes bei angehaltenem LxssManagerUser-Dienst</span><span class="sxs-lookup"><span data-stu-id="9b657-156">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="9b657-157">Fehlerbehebung für ein wslapi.dll-Fast-Fail, wenn der distroName-Parameter NULL ist</span><span class="sxs-lookup"><span data-stu-id="9b657-157">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="9b657-158">Build 19041</span><span class="sxs-lookup"><span data-stu-id="9b657-158">Build 19041</span></span>
<span data-ttu-id="9b657-159">Allgemeine Windows-Informationen zu Build 19041 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span><span class="sxs-lookup"><span data-stu-id="9b657-159">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="9b657-160">[WSL2] Löschen der Signalmaske vor dem Starten der Prozesse</span><span class="sxs-lookup"><span data-stu-id="9b657-160">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="9b657-161">[WSL2] Aktualisieren des Linux-Kernels auf 4.19.84</span><span class="sxs-lookup"><span data-stu-id="9b657-161">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="9b657-162">Verarbeiten der Erstellung der symbolischen Verknüpfung „/etc/resolv.conf“, wenn die symbolische Verknüpfung nicht relativ ist</span><span class="sxs-lookup"><span data-stu-id="9b657-162">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="9b657-163">Build 19028</span><span class="sxs-lookup"><span data-stu-id="9b657-163">Build 19028</span></span>
<span data-ttu-id="9b657-164">Allgemeine Windows-Informationen zu Build 19028 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="9b657-164">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="9b657-165">[WSL2] Aktualisieren des Linux-Kernels auf 4.19.81</span><span class="sxs-lookup"><span data-stu-id="9b657-165">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="9b657-166">[WSL2] Ändern der Standardberechtigung von /dev/net/tun in 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="9b657-166">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="9b657-167">[WSL2] Optimieren der Standard-Arbeitsspeichergröße, die dem virtuellen Linux-Computer zugewiesen ist, auf 80% des Hostarbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="9b657-167">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="9b657-168">[WSL2] Fehlerbehebung für den Interop-Server, um Anforderungen mit einem Timeout zu verarbeiten, damit sich der Server bei ungültigen Aufrufern nicht aufhängt</span><span class="sxs-lookup"><span data-stu-id="9b657-168">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="9b657-169">Build 19018</span><span class="sxs-lookup"><span data-stu-id="9b657-169">Build 19018</span></span>
<span data-ttu-id="9b657-170">Allgemeine Windows-Informationen zu Build 19018 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="9b657-170">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="9b657-171">[WSL2] Verwenden Sie cache=mmap als Standardeinstellung für 9p-Einbindungen, um Probleme mit Dotnet-Apps zu beheben</span><span class="sxs-lookup"><span data-stu-id="9b657-171">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="9b657-172">[WSL2] Korrekturen für localhost-Relay [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="9b657-172">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="9b657-173">[WSL2] Einführen einer distributionsübergreifenden, gemeinsam genutzten tmpfs-Einbindung für den Freigabezustand zwischen Distributionen</span><span class="sxs-lookup"><span data-stu-id="9b657-173">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="9b657-174">Korrektur der Wiederherstellung des permanenten Netzwerklaufwerks für \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="9b657-174">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="9b657-175">Build 19013</span><span class="sxs-lookup"><span data-stu-id="9b657-175">Build 19013</span></span>
<span data-ttu-id="9b657-176">Allgemeine Windows-Informationen zu Build 19013 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="9b657-176">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="9b657-177">[WSL2] Verbesserte Arbeitsspeicherleistung der VM des WSL-Hilfsprogramms</span><span class="sxs-lookup"><span data-stu-id="9b657-177">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="9b657-178">Arbeitsspeicher, der nicht mehr verwendet wird, wird an den Host zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b657-178">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="9b657-179">[WSL2] Aktualisieren der Kernelversion auf 4.19.79</span><span class="sxs-lookup"><span data-stu-id="9b657-179">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="9b657-180">(CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK und CONFIG_BRIDGE_VLAN_FILTERING hinzugefügt).</span><span class="sxs-lookup"><span data-stu-id="9b657-180">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="9b657-181">[WSL2] Korrigiertes Eingaberelay zur Behandlung von Fällen, in denen stdin ein nicht geschlossenes Pipehandle ist [GH 4424]</span><span class="sxs-lookup"><span data-stu-id="9b657-181">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="9b657-182">Die Überprüfung auf \\\\wsl$ unterscheidet nicht mehr zwischen Groß- und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="9b657-182">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="9b657-183">Build 19002</span><span class="sxs-lookup"><span data-stu-id="9b657-183">Build 19002</span></span>
<span data-ttu-id="9b657-184">Allgemeine Windows-Informationen zu Build 19002 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="9b657-184">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="9b657-185">[WSL] Beheben von Problemen bei der Behandlung einiger Unicode-Zeichen: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="9b657-185">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="9b657-186">[WSL] Korrektur seltener Fälle, in denen die Registrierung von Distributionen aufgehoben werden kann, wenn sie unmittelbar nach einem Build-zu-Build-Upgrade gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-186">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="9b657-187">[WSL] Korrektur eines kleinen Problems beim Herunterfahren mit „wsl.exe“, bei dem Leerlaufzeitgeber von Instanzen nicht abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="9b657-187">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="9b657-188">Build 18995</span><span class="sxs-lookup"><span data-stu-id="9b657-188">Build 18995</span></span>
<span data-ttu-id="9b657-189">Allgemeine Windows-Informationen zu Build 18995 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="9b657-189">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="9b657-190">[WSL2] Korrektur eines Problems, bei dem DrvFs-Einbindungen nach dem Abbruch eines Vorgangs (z.B. STRG-C) zu funktionieren aufhörten [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="9b657-190">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="9b657-191">[WSL2] Korrektur der Verarbeitung sehr großer hvsocket-Nachrichten [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="9b657-191">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="9b657-192">[WSL2] Korrektur eines Interop-Problems, wenn stdin eine Datei ist [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="9b657-192">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="9b657-193">[WSL2] Korrektur eines Absturzes, wenn ein unerwarteter Netzwerkstatus festgestellt wird [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="9b657-193">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="9b657-194">[WSL2] Abfragen des Namens der Distribution beim Interopserver, wenn der aktuelle Prozess nicht über die Umgebungsvariable verfügt</span><span class="sxs-lookup"><span data-stu-id="9b657-194">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="9b657-195">[WSL2] Korrektur eines Interop-Problems, wenn stdin eine Datei ist</span><span class="sxs-lookup"><span data-stu-id="9b657-195">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="9b657-196">[WSL2] Aktualisieren der Linux-Kernelversion auf 4.19.72</span><span class="sxs-lookup"><span data-stu-id="9b657-196">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="9b657-197">[WSL2] Neu hinzugefügte Möglichkeit zum Angeben weiterer Kernelbefehle in der Befehlszeile mithilfe von WSLCONFIG</span><span class="sxs-lookup"><span data-stu-id="9b657-197">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="9b657-198">Build 18990</span><span class="sxs-lookup"><span data-stu-id="9b657-198">Build 18990</span></span>
<span data-ttu-id="9b657-199">Allgemeine Windows-Informationen zu Build 18990 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="9b657-199">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="9b657-200">Verbesserte Leistung für Verzeichnisauflistungen in \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="9b657-200">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="9b657-201">[WSL2] Einführen zusätzlicher Entropie beim Systemstart [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="9b657-201">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="9b657-202">[WSL2] Problembehebung für Windows-Interop bei der Verwendung von „su“ / „sudo“ [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="9b657-202">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="9b657-203">Build 18980</span><span class="sxs-lookup"><span data-stu-id="9b657-203">Build 18980</span></span>
<span data-ttu-id="9b657-204">Allgemeine Windows-Informationen zu Build 18980 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="9b657-204">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="9b657-205">Korrektur des Lesen von symbolischen Verknüpfungen, die FILE_READ_DATA verweigern.</span><span class="sxs-lookup"><span data-stu-id="9b657-205">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="9b657-206">Dies umfasst alle symbolischen Verknüpfungen, die von Windows aus Gründen der Abwärtskompatibilität erstellt werden, z.B. „C:\Dokumente und Einstellungen“ und eine Reihe von symbolischen Verknüpfungen im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9b657-206">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="9b657-207">Festlegen eines unerwarteten Dateisystemzustands als nicht schwerwiegend [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="9b657-207">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="9b657-208">[WSL2] Hinzufügen von Unterstützung für arm64, wenn Ihre CPU/Firmware Virtualisierung unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b657-208">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="9b657-209">[WSL2] Zulassen der Anzeige von Kernelprotokollen durch nicht berechtigte Benutzer</span><span class="sxs-lookup"><span data-stu-id="9b657-209">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="9b657-210">[WSL2] Korrigieren des Ausgaberelays, wenn stdout/stderr-Sockets geschlossen wurden [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="9b657-210">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="9b657-211">[WSL2] Unterstützung von Akku- und AC-Adapter-Passthrough</span><span class="sxs-lookup"><span data-stu-id="9b657-211">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="9b657-212">[WSL2] Aktualisieren des Linux-Kernels auf 4.19.67</span><span class="sxs-lookup"><span data-stu-id="9b657-212">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="9b657-213">Hinzufügen der Möglichkeit, den Standardbenutzernamen in „/etc/wsl.conf“ festzulegen:</span><span class="sxs-lookup"><span data-stu-id="9b657-213">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="9b657-214">Build 18975</span><span class="sxs-lookup"><span data-stu-id="9b657-214">Build 18975</span></span>
<span data-ttu-id="9b657-215">Allgemeine Windows-Informationen zu Build 18975 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="9b657-215">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="9b657-216">[WSL2] Korrektur einer Reihe von Problemen mit der localhost-Zuverlässigkeit [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="9b657-216">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="9b657-217">Build 18970</span><span class="sxs-lookup"><span data-stu-id="9b657-217">Build 18970</span></span>
<span data-ttu-id="9b657-218">Allgemeine Windows-Informationen zu Build 18970 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="9b657-218">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="9b657-219">[WSL2] Synchronisierung der Uhrzeit mit der Hostzeit, wenn das System nach dem Ruhezustand fortgesetzt wird [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="9b657-219">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="9b657-220">[WSL2] Nach Möglichkeit Erstellen symbolischer NT-Verknüpfungen auf den Windows-Volumes</span><span class="sxs-lookup"><span data-stu-id="9b657-220">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="9b657-221">[WSL2] Erstellen von Distributionen in den UTS-, IPC-, PID- und Mount-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="9b657-221">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="9b657-222">[WSL2] Korrigieren des localhost-Portrelays, wenn der Server direkt an localhost gebunden wird [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="9b657-222">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="9b657-223">[WSL2] Korrigieren von Interop, wenn die Ausgabe umgeleitet wird [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="9b657-223">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="9b657-224">[WSL2] Unterstützung der Übersetzung absoluter symbolischer NT-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-224">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="9b657-225">[WSL2] Aktualisieren des Kernels auf 4.19.59</span><span class="sxs-lookup"><span data-stu-id="9b657-225">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="9b657-226">[WSL2] Ordnungsgemäße Festlegung der Subnetzmaske für eth0.</span><span class="sxs-lookup"><span data-stu-id="9b657-226">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="9b657-227">[WSL2] Ändern der Logik, um die Konsolenworkerschleife zu verlassen, wenn das Beendigungsereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-227">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="9b657-228">[WSL2] Auswerfen der Distributions-VHD, wenn die Distribution nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-228">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="9b657-229">[WSL2] Korrigieren der Analysebibliothek, um leere Werte ordnungsgemäß zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="9b657-229">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="9b657-230">[WSL2] Unterstützung von Docker Desktop durch Erstellen von distributionsübergreifenden Einbindungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-230">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="9b657-231">Dieses Verhalten kann durch eine Distribution übernommen werden, indem die folgende Zeile der Datei „/etc/wsl.conf“ hinzugefügt wird:</span><span class="sxs-lookup"><span data-stu-id="9b657-231">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="9b657-232">Build 18945</span><span class="sxs-lookup"><span data-stu-id="9b657-232">Build 18945</span></span>
<span data-ttu-id="9b657-233">Allgemeine Windows-Informationen zu Build 18945 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="9b657-233">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-234">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-234">WSL</span></span>
* <span data-ttu-id="9b657-235">[WSL2] Zulassen, dass der Zugriff auf lauschende TCP-Sockets in WSL2 über „localhost:port“ vom Host erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="9b657-235">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="9b657-236">[WSL2] Korrekturen für Installations- und Konvertierungsfehler und zusätzliche Diagnose zur Nachverfolgung zukünftiger Probleme [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="9b657-236">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="9b657-237">[WSL2] Verbessern der Diagnose von WSL2-Netzwerkproblemen</span><span class="sxs-lookup"><span data-stu-id="9b657-237">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="9b657-238">[WSL2] Aktualisieren der Kernelversion auf 4.19.55</span><span class="sxs-lookup"><span data-stu-id="9b657-238">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="9b657-239">[WSL2] Aktualisieren des Kernels mit Konfigurationsoptionen, die für Docker erforderlich sind [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="9b657-239">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="9b657-240">[WSL2] Erhöhen der Anzahl der CPUs, die der Lightweight Utility-VM zugeordnet sind, um eine mit dem Host identische Anzahl zu erreichen (wurde zuvor durch CONFIG_NR_CPUS in der Kernelkonfiguration auf 8 begrenzt) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="9b657-240">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="9b657-241">[WSL2] Erstellen einer Auslagerungsdatei für die WSL2-Lightweight-VM</span><span class="sxs-lookup"><span data-stu-id="9b657-241">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="9b657-242">[WSL2] Zulassen, dass Benutzereinbindungen über die \\\\wsl$\\-Distribution (z.B. sshfs) sichtbar sind [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="9b657-242">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="9b657-243">[WSL2] Verbessern der Leistung des 9P-Dateisystems</span><span class="sxs-lookup"><span data-stu-id="9b657-243">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="9b657-244">[WSL2] Sicherstellen, dass die VHD-ACL nicht unbegrenzt anwächst [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="9b657-244">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="9b657-245">[WSL2] Aktualisieren der Kernelkonfiguration für die Unterstützung von squashfs und xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="9b657-245">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="9b657-246">[WSL2] Korrektur für interopaktivierte „/etc/wsl.conf“-Option [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="9b657-246">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="9b657-247">[WSL2] Rückgabe von ENOTSUP, wenn das Dateisystem EAS nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b657-247">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="9b657-248">[WSL2] Korrigieren von CopyFile-Hänger mit \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="9b657-248">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="9b657-249">Umschalten von Standard-umask in 0022 und Hinzufügen der filesystem.umask-Einstellung zu „/etc/wsl.conf“</span><span class="sxs-lookup"><span data-stu-id="9b657-249">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="9b657-250">Korrigieren von wslpath, um symbolische Verknüpfungen ordnungsgemäß aufzulösen, dies wurde in 19h1 zurückgesetzt [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="9b657-250">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="9b657-251">Einführung der Datei „%UserProfile%\\.wslconfig“ für die Optimierung der WSL2-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9b657-251">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="9b657-252">Build 18917</span><span class="sxs-lookup"><span data-stu-id="9b657-252">Build 18917</span></span>
<span data-ttu-id="9b657-253">Allgemeine Windows-Informationen zu Build 18917 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="9b657-253">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-254">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-254">WSL</span></span>
* <span data-ttu-id="9b657-255">WSL 2 ist Jetzt verfügbar!</span><span class="sxs-lookup"><span data-stu-id="9b657-255">WSL 2 is now available!</span></span> <span data-ttu-id="9b657-256">Weitere Informationen finden Sie im [Blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="9b657-256">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="9b657-257">Korrektur einer Regression, bei der das Starten von Windows-Prozessen über symbolische Verknüpfungen nicht ordnungsgemäß funktioniert hat [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="9b657-257">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="9b657-258">Hinzufügen der Optionen wsl.exe --list --verbose, wsl.exe --list --quiet und wsl.exe --import --version zu „wsl.exe“</span><span class="sxs-lookup"><span data-stu-id="9b657-258">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="9b657-259">Hinzufügen der Option wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="9b657-259">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="9b657-260">Plan 9: Zulassen des Öffnend eines Verzeichnisses für einen erfolgreichen Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="9b657-260">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="9b657-261">Build 18890</span><span class="sxs-lookup"><span data-stu-id="9b657-261">Build 18890</span></span>
<span data-ttu-id="9b657-262">Allgemeine Windows-Informationen zu Build 18890 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="9b657-262">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-263">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-263">WSL</span></span>
* <span data-ttu-id="9b657-264">Nicht blockierender Socketverlust [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="9b657-264">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="9b657-265">EOF-Eingabe für Terminal kann nachfolgende Lesevorgänge blockieren [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="9b657-265">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="9b657-266">Aktualisieren des resolv.conf-Headers, damit er auf „wsl.conf“ verweist [in GH 3928 beschrieben].</span><span class="sxs-lookup"><span data-stu-id="9b657-266">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="9b657-267">Deadlock im epoll-Löschcode [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="9b657-267">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="9b657-268">Verarbeiten von Leerzeichen in Argumenten für --import und --export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="9b657-268">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="9b657-269">Erweitern von mit mmap behandelten Dateien funktioniert nicht ordnungsgemäß [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="9b657-269">Extending mmap'd files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="9b657-270">Korrektur eines Problems mit ARM64 \\\\wsl$-Zugriff funktioniert nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="9b657-270">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="9b657-271">Hinzufügen eines besseren Standardsymbols für „wsl.exe“</span><span class="sxs-lookup"><span data-stu-id="9b657-271">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="9b657-272">Build 18342</span><span class="sxs-lookup"><span data-stu-id="9b657-272">Build 18342</span></span>
<span data-ttu-id="9b657-273">Allgemeine Windows-Informationen zu Build 18342 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="9b657-273">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-274">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-274">WSL</span></span>
* <span data-ttu-id="9b657-275">Wir haben für Benutzer die Möglichkeit hinzugefügt, auf Linux-Dateien in einer WSL-Distribution aus Windows zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9b657-275">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="9b657-276">Auf diese Dateien kann über die Befehlszeile zugegriffen werden. Außerdem können Windows-Apps wie der Datei-Explorer, VSCode usw. mit diesen Dateien interagieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-276">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="9b657-277">Greifen Sie auf Ihre Dateien zu, indem Sie zu \\\\wsl$\\<distributions_name> navigieren, oder zeigen Sie eine Liste der ausgeführten Distributionen an, indem Sie zu \\\\wsl$ navigieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-277">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="9b657-278">Hinzufügen zusätzlicher CPU-Infotags und Korrigieren der Cpus_allowed[_list]-Werte [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="9b657-278">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="9b657-279">Unterstützung der Ausführung aus Nicht-Leaderthread [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="9b657-279">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="9b657-280">Behandeln von Konfigurationsupdatefehlern als nicht schwerwiegend [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="9b657-280">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="9b657-281">Aktualisieren von binfmt für die ordnungsgemäße Verarbeitung von Offsets [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="9b657-281">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="9b657-282">Aktivieren der Zuordnung von Netzlaufwerken für Plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="9b657-282">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="9b657-283">Unterstützung von Windows -> Linux und Linux -> Windows-Pfadübersetzung für Bindungseinbindungen</span><span class="sxs-lookup"><span data-stu-id="9b657-283">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="9b657-284">Erstellen schreibgeschützter Abschnitte für Zuordnungen für Dateien, die schreibgeschützt geöffnet sind</span><span class="sxs-lookup"><span data-stu-id="9b657-284">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="9b657-285">Build 18334</span><span class="sxs-lookup"><span data-stu-id="9b657-285">Build 18334</span></span>
<span data-ttu-id="9b657-286">Allgemeine Windows-Informationen zu Build 18334 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="9b657-286">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-287">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-287">WSL</span></span>
* <span data-ttu-id="9b657-288">Umgestalten der Art und Weise, in der die Windows-Zeitzone einer Linux-Zeitzone zugeordnet wird [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="9b657-288">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="9b657-289">Beheben von Speicherverlusten und Hinzufügen neuer Zeichenfolgenübersetzungsfunktionen [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="9b657-289">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="9b657-290">SIGCONT für eine Threadgruppe ohne Threads ist eine Nulloperation [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="9b657-290">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="9b657-291">Richtige Anzeige von Socket- und Epoll-Dateideskriptoren in „/proc/self/fd“</span><span class="sxs-lookup"><span data-stu-id="9b657-291">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="9b657-292">Build 18305</span><span class="sxs-lookup"><span data-stu-id="9b657-292">Build 18305</span></span>
<span data-ttu-id="9b657-293">Allgemeine Windows-Informationen zu Build 18305 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="9b657-293">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-294">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-294">WSL</span></span>
* <span data-ttu-id="9b657-295">pthreads verlieren den Zugriff auf Dateien, wenn der primäre Thread beendet wird [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="9b657-295">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="9b657-296">TIOCSCTTY sollte den Parameter „force“ ignorieren, wenn er nicht erforderlich ist [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="9b657-296">TIOCSCTTY should ignore the "force" parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="9b657-297">Verbesserungen an der Befehlszeile von „wsl.exe“ und Hinzufügung von Import-/Exportfunktionen.</span><span class="sxs-lookup"><span data-stu-id="9b657-297">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="9b657-298">Build 18277</span><span class="sxs-lookup"><span data-stu-id="9b657-298">Build 18277</span></span>
<span data-ttu-id="9b657-299">Allgemeine Windows-Informationen zu Build 18277 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="9b657-299">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-300">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-300">WSL</span></span>
* <span data-ttu-id="9b657-301">Korrektur des Fehlers „no such interface supported“ in Build 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="9b657-301">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="9b657-302">Ignorieren des MNT_FORCE-Flags für Systemaufruf zum Aufheben der Einbindung [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="9b657-302">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="9b657-303">Umschalten von WSL-Interop für die Verwendung der offiziellen CreatePseudoConsole-API</span><span class="sxs-lookup"><span data-stu-id="9b657-303">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="9b657-304">Keinen Timeoutwert beibehalten, wenn FUTEX_WAIT neu gestartet wird</span><span class="sxs-lookup"><span data-stu-id="9b657-304">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="9b657-305">Build 18272</span><span class="sxs-lookup"><span data-stu-id="9b657-305">Build 18272</span></span>
<span data-ttu-id="9b657-306">Allgemeine Windows-Informationen zu Build 18272 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="9b657-306">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-307">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-307">WSL</span></span>
* <span data-ttu-id="9b657-308">**WARNUNG:** In diesem Build liegt ein Problem vor, durch das WSL nicht funktionsfähig wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-308">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="9b657-309">Wenn Sie versuchen, die Verteilung zu starten, wird der Fehler „Schnittstelle nicht unterstützt“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b657-309">When trying to launch your distribution you will see a "No such interface supported" error.</span></span> <span data-ttu-id="9b657-310">Das Problem wurde behoben und ist im Insider Fast-Build der nächsten Woche nicht mehr enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b657-310">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="9b657-311">Wenn Sie diesen Build installiert haben, können Sie ein Rollback auf den vorherigen Windows-Build durchführen, indem Sie unter „Einstellungen > Update und Sicherheit > Wiederherstellung“ die Option „Zur vorherigen Version von Windows 10 zurückkehren“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="9b657-311">If you've installed this build you can roll back to the previous Windows build using "Go back to the previous version of Windows 10" in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="9b657-312">Build 18267</span><span class="sxs-lookup"><span data-stu-id="9b657-312">Build 18267</span></span>
<span data-ttu-id="9b657-313">Allgemeine Windows-Informationen zu Build 18267 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="9b657-313">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-314">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-314">WSL</span></span>
* <span data-ttu-id="9b657-315">Korrektur eines Problems, bei dem der Zombieprozess möglicherweise nicht beendet und unbegrenzt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-315">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="9b657-316">WslRegisterDistribution hängt, wenn die Fehlermeldung die maximale Länge überschreitet [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="9b657-316">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="9b657-317">Zulassen der erfolgreichen Ausführung von fsync für schreibgeschützte Dateien auf DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="9b657-317">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="9b657-318">Sicherstellen, dass die Verzeichnisse „/bin“ und „/sbin“ vorhanden sind, bevor symbolische Verknüpfungen darin erstellt werden [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="9b657-318">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="9b657-319">Hinzufügen eines Instanztimeoutmechanismus für WSL-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="9b657-319">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="9b657-320">Der Timeoutwert ist derzeit auf 15 Sekunden festgelegt. Das bedeutet, dass die Instanz 15 Sekunden nach Beendigung des letzten WSL-Prozesses beendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-320">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="9b657-321">Um eine Distribution sofort zu beenden, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9b657-321">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="9b657-322">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="9b657-322">Build 17763 (1809)</span></span>
<span data-ttu-id="9b657-323">Allgemeine Windows-Informationen zu Build 17763 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="9b657-323">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-324">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-324">WSL</span></span>
* <span data-ttu-id="9b657-325">Berechtigungsüberprüfung für Setpriority-Systemaufruf ist zu streng, um die gleiche Threadpriorität zu ändern[GH 1838].</span><span class="sxs-lookup"><span data-stu-id="9b657-325">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="9b657-326">Stellen Sie sicher, dass die unbeeinflusste Interruptzeit für die Startzeit verwendet wird, um zu vermeiden, dass negative Werte für clock_gettime (CLOCK_BOOTTIME) zurückgegeben werden [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="9b657-326">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="9b657-327">Verarbeiten von symbolischen Verknüpfungen im WSL-binfmt-Interpreter [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="9b657-327">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="9b657-328">Bessere Verarbeitung der Bereinigung des Threadgruppen-Leaderdateideskriptors.</span><span class="sxs-lookup"><span data-stu-id="9b657-328">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="9b657-329">Umschalten von WSL für die Verwendung von KeQueryInterruptTimePrecise anstelle von KeQueryPerformanceCounter zur Vermeidung eines Überlaufs [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="9b657-329">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="9b657-330">Ptrace-Anfügevorgang kann zu einem ungültigen Rückgabewert von Systemaufrufen führen [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="9b657-330">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="9b657-331">Korrektur mehrerer Probleme, die sich auf AF_UNIX beziehen [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="9b657-331">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="9b657-332">Korrektur eines Problems, das dazu führen kann, dass WSL-Interop fehlschlägt, wenn das aktuelle Arbeitsverzeichnis weniger als 5 Zeichen lang ist [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="9b657-332">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="9b657-333">Vermeiden von einer Sekunde Verzögerung bei Ausfall von Loopbackverbindungen mit nicht vorhandenen Ports [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="9b657-333">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="9b657-334">Hinzufügen der Stubdatei „/proc/sys/fs/file-max“ [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="9b657-334">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="9b657-335">Genauere IPv6-Bereichsinformationen.</span><span class="sxs-lookup"><span data-stu-id="9b657-335">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="9b657-336">PR_SET_PTRACER-Unterstützung [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="9b657-336">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="9b657-337">Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="9b657-337">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="9b657-338">Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="9b657-338">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="9b657-339">Verbesserte Zombieunterstützung [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="9b657-339">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="9b657-340">Hinzufügen von wsl.conf-Einträgen zum Steuern des Windows-Interop-Verhaltens [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="9b657-340">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="9b657-341">Korrektur des Verhaltens, dass getsockname nicht immer den Porduktfamilientyp des UNIX-Sockets zurückgibt [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="9b657-341">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="9b657-342">Hinzufügen von Unterstützung für TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="9b657-342">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="9b657-343">Nicht blockierende Sockets beim Verbindungsaufbau sollten für Schreibversuche EAGAIN zurückgeben [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="9b657-343">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="9b657-344">Unterstützung von Interop auf eingebundenen VHDs [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="9b657-344">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="9b657-345">Korrektur von Problem mit der Berechtigungsüberprüfung im Stammordner [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="9b657-345">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="9b657-346">Eingeschränkte Unterstützung für die TTY-Tastatur-ioctls KDGKBTYPE, KDGKBMODE und KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="9b657-346">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="9b657-347">Windows-UI-Apps sollten ausgeführt selbst dann werden, wenn Sie im Hintergrund gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-347">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="9b657-348">Hinzufügen der Option wsl -u oder--user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="9b657-348">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="9b657-349">Korrektur von WSL-Startproblemen, wenn der Schnellstart aktiviert ist [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="9b657-349">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="9b657-350">Unix-Sockets müssen getrennte Peeranmelde Informationen beibehalten [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="9b657-350">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="9b657-351">Nicht blockierende Unix-Sockets, die unbegrenzt EAGAIN-Fehler ausgeben [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="9b657-351">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="9b657-352">case=off ist der neue standardmäßige drvfs-Einbindungstyp [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="9b657-352">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="9b657-353">Weitere Informationen finden Sie im [Blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="9b657-353">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="9b657-354">Hinzufügen von wslconfig/terminate zum Beenden ausgeführter Distributionen</span><span class="sxs-lookup"><span data-stu-id="9b657-354">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="9b657-355">Korrektur des Problems mit den Kontextmenüeinträgen der WSL-Shell, die Pfade mit Leerzeichen nicht ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="9b657-355">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="9b657-356">Bereitstellen von Unterscheidung von Groß-/Kleinschreibung pro Verzeichnis als erweitertes Attribut</span><span class="sxs-lookup"><span data-stu-id="9b657-356">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="9b657-357">ARM64: Emulieren von Cacheverwaltungsvorgängen.</span><span class="sxs-lookup"><span data-stu-id="9b657-357">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="9b657-358">Beheben von [dotnet-Problem](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="9b657-358">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="9b657-359">DrvFs: Nur Escapezeichen im privaten Bereich, die einem mit Escapezeichen versehenen Zeichen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b657-359">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="9b657-360">Korrektur eines Off-by-one-Fehlers in der Längenüberprüfung des ELF Parserinterpreters [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="9b657-360">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="9b657-361">Absolute WSL-Timer mit einer Zeitangabe in der Vergangenheit werden nicht ausgelöst [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="9b657-361">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="9b657-362">Sicherstellen, dass neu erstellte Analysepunkte als solche im übergeordneten Verzeichnis aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-362">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="9b657-363">Atomarisches Erstellen von Verzeichnissen mit Berücksichtigung von Groß- und Kleinschreibung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9b657-363">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="9b657-364">Korrektur eines zusätzlichen Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-364">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="9b657-365">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="9b657-365">[GH 2712]</span></span>
* <span data-ttu-id="9b657-366">Korrektur eines WSL-Startfehlers, wenn UMCI aktiviert ist.-</span><span class="sxs-lookup"><span data-stu-id="9b657-366">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="9b657-367">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="9b657-367">[GH 3020]</span></span>
* <span data-ttu-id="9b657-368">Hinzufügen des Explorer-Kontextmenüs zum Starten von WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="9b657-368">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="9b657-369">Halten Sie in einem Explorer-Fenster die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste, um diese Option zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b657-369">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="9b657-370">Korrektur des nicht blockierenden UNIX-Socketverhaltens [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="9b657-370">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="9b657-371">Korrigieren des hängenden NETLINK-Befehls, wie in GH 2026 gemeldet.</span><span class="sxs-lookup"><span data-stu-id="9b657-371">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="9b657-372">Hinzufügen von Unterstützung für Einbindungsweitergabeflags [GH 2911]</span><span class="sxs-lookup"><span data-stu-id="9b657-372">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="9b657-373">Korrektur von Problem mit truncate, das keine inotify-Ereignisse verursacht [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="9b657-373">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="9b657-374">Hinzufügen der Option --exec für „wsl.exe“ zum Aufrufen eine einzelne Binärdatei ohne Shell.</span><span class="sxs-lookup"><span data-stu-id="9b657-374">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="9b657-375">Hinzufügen der Option --distribution für „wsl.exe“, um eine bestimmte Distribution auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9b657-375">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="9b657-376">Eingeschränkte Unterstützung für dmesg.</span><span class="sxs-lookup"><span data-stu-id="9b657-376">Limited support for dmesg.</span></span> <span data-ttu-id="9b657-377">Anwendungen können sich jetzt in dmesg protokollieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-377">Applications can now log to dmesg.</span></span> <span data-ttu-id="9b657-378">Der WSL-Treiber protokolliert eingeschränkte Informationen in dmesg.</span><span class="sxs-lookup"><span data-stu-id="9b657-378">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="9b657-379">In Zukunft kann dies so erweitert werden, dass andere Informationen/Diagnoseinhalte vom Treiber erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-379">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="9b657-380">Hinweis: dmesg wird derzeit über die `/dev/kmsg`-Geräteschnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-380">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="9b657-381">`syslog`-Systemaufrufschnittstelle wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-381">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="9b657-382">Daher funktionieren einige der `dmesg`-Befehlszeilenoptionen (z.B. `-S`, `-C`) nicht.</span><span class="sxs-lookup"><span data-stu-id="9b657-382">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="9b657-383">Änderung der Standard-GID und des Modus von seriellen Geräten entsprechend den nativen Einstellungen [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="9b657-383">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="9b657-384">DrvFs unterstützt jetzt erweiterte Attribute.</span><span class="sxs-lookup"><span data-stu-id="9b657-384">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="9b657-385">Hinweis: Für DrvFs gelten einige Einschränkungen für den Namen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="9b657-385">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="9b657-386">Einige Zeichen (etwa „/“, „:“ und „\*“) sind unzulässig, und für Namen erweiterter Attribute wird in DrvFs keine Groß- und Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-386">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="9b657-387">Build 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="9b657-387">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="9b657-388">Allgemeine Windows-Informationen zu Build 18252 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="9b657-388">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-389">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-389">WSL</span></span>
* <span data-ttu-id="9b657-390">Verschieben von init- und bsdtar-Binärdateien aus der lxssmanager-DLL in einen separaten Toolsordner</span><span class="sxs-lookup"><span data-stu-id="9b657-390">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="9b657-391">Korrektur von Racebedingung um schließenden Dateideskriptor bei Verwendung von CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="9b657-391">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="9b657-392">Verarbeiten optionaler Felder in „/proc/pid/mountinfo“ bei der Übersetzung von DrvFs-Pfaden</span><span class="sxs-lookup"><span data-stu-id="9b657-392">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="9b657-393">Zulassen, dass DrvFs mklod ohne Metadatenunterstützung für S_IFREG erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="9b657-393">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="9b657-394">Für schreibgeschützte Dateien, die auf DrvFs erstellt wurden, muss das schreibgeschützte Attribut festgelegt werden [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="9b657-394">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="9b657-395">Hinzufügen von /sbin/mount.drvfs-Hilfsprogramm zur Verarbeitung der DrvFs-Einbindung</span><span class="sxs-lookup"><span data-stu-id="9b657-395">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="9b657-396">Verwenden der POSIX-Umbenennung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9b657-396">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="9b657-397">Ermöglichen der Pfadübersetzung für Volumes ohne Volume-GUID.</span><span class="sxs-lookup"><span data-stu-id="9b657-397">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="9b657-398">Build 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="9b657-398">Build 17738 (Fast)</span></span>
<span data-ttu-id="9b657-399">Allgemeine Windows-Informationen zu Build 17738 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="9b657-399">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-400">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-400">WSL</span></span>
* <span data-ttu-id="9b657-401">Berechtigungsüberprüfung für Setpriority-Systemaufruf ist zu streng, um die gleiche Threadpriorität zu ändern[GH 1838].</span><span class="sxs-lookup"><span data-stu-id="9b657-401">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="9b657-402">Stellen Sie sicher, dass die unbeeinflusste Interruptzeit für die Startzeit verwendet wird, um zu vermeiden, dass negative Werte für clock_gettime (CLOCK_BOOTTIME) zurückgegeben werden [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="9b657-402">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="9b657-403">Verarbeiten von symbolischen Verknüpfungen im WSL-binfmt-Interpreter [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="9b657-403">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="9b657-404">Bessere Verarbeitung der Bereinigung des Threadgruppen-Leaderdateideskriptors.</span><span class="sxs-lookup"><span data-stu-id="9b657-404">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="9b657-405">Build 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="9b657-405">Build 17728 (Fast)</span></span>
<span data-ttu-id="9b657-406">Allgemeine Windows-Informationen zu Build 17728 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="9b657-406">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-407">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-407">WSL</span></span>
* <span data-ttu-id="9b657-408">Umschalten von WSL für die Verwendung von KeQueryInterruptTimePrecise anstelle von KeQueryPerformanceCounter zur Vermeidung eines Überlaufs [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="9b657-408">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="9b657-409">Ptrace-Anfügevorgang kann zu einem ungültigen Rückgabewert von Systemaufrufen führen [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="9b657-409">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="9b657-410">Korrektur mehrerer Probleme, die sich auf AF_UNIX beziehen [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="9b657-410">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="9b657-411">Korrektur eines Problems, das dazu führen kann, dass WSL-Interop fehlschlägt, wenn das aktuelle Arbeitsverzeichnis weniger als 5 Zeichen lang ist [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="9b657-411">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="9b657-412">Build 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="9b657-412">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="9b657-413">Allgemeine Windows-Informationen zu Build 18204 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="9b657-413">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-414">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-414">WSL</span></span>
* <span data-ttu-id="9b657-415">Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="9b657-415">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="9b657-416">Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="9b657-416">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="9b657-417">Build 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="9b657-417">Build 17723 (Fast)</span></span>
<span data-ttu-id="9b657-418">Allgemeine Windows-Informationen zu Build 17723 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="9b657-418">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-419">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-419">WSL</span></span>
* <span data-ttu-id="9b657-420">Vermeiden von einer Sekunde Verzögerung bei Ausfall von Loopbackverbindungen mit nicht vorhandenen Ports [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="9b657-420">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="9b657-421">Hinzufügen der Stubdatei „/proc/sys/fs/file-max“ [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="9b657-421">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="9b657-422">Genauere IPv6-Bereichsinformationen.</span><span class="sxs-lookup"><span data-stu-id="9b657-422">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="9b657-423">PR_SET_PTRACER-Unterstützung [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="9b657-423">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="9b657-424">Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="9b657-424">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="9b657-425">Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="9b657-425">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="9b657-426">Build 17713</span><span class="sxs-lookup"><span data-stu-id="9b657-426">Build 17713</span></span>
<span data-ttu-id="9b657-427">Allgemeine Windows-Informationen zu Build 17713 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="9b657-427">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-428">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-428">WSL</span></span>
* <span data-ttu-id="9b657-429">Verbesserte Zombieunterstützung [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="9b657-429">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="9b657-430">Hinzufügen von wsl.conf-Einträgen zum Steuern des Windows-Interop-Verhaltens [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="9b657-430">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="9b657-431">Korrektur des Verhaltens, dass getsockname nicht immer den Porduktfamilientyp des UNIX-Sockets zurückgibt [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="9b657-431">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="9b657-432">Hinzufügen von Unterstützung für TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="9b657-432">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="9b657-433">Nicht blockierende Sockets beim Verbindungsaufbau sollten für Schreibversuche EAGAIN zurückgeben [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="9b657-433">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="9b657-434">Unterstützung von Interop auf eingebundenen VHDs [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="9b657-434">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="9b657-435">Korrektur von Problem mit der Berechtigungsüberprüfung im Stammordner [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="9b657-435">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="9b657-436">Eingeschränkte Unterstützung für die TTY-Tastatur-ioctls KDGKBTYPE, KDGKBMODE und KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="9b657-436">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="9b657-437">Windows-UI-Apps sollten ausgeführt selbst dann werden, wenn Sie im Hintergrund gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-437">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="9b657-438">Build 17704</span><span class="sxs-lookup"><span data-stu-id="9b657-438">Build 17704</span></span>
<span data-ttu-id="9b657-439">Allgemeine Windows-Informationen zu Build 17704 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="9b657-439">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-440">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-440">WSL</span></span>
* <span data-ttu-id="9b657-441">Hinzufügen der Option wsl -u oder--user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="9b657-441">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="9b657-442">Korrektur von WSL-Startproblemen, wenn der Schnellstart aktiviert ist [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="9b657-442">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="9b657-443">Unix-Sockets müssen getrennte Peeranmelde Informationen beibehalten [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="9b657-443">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="9b657-444">Nicht blockierende Unix-Sockets, die unbegrenzt EAGAIN-Fehler ausgeben [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="9b657-444">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="9b657-445">case=off ist der neue standardmäßige drvfs-Einbindungstyp [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="9b657-445">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="9b657-446">Weitere Informationen finden Sie im [Blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="9b657-446">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="9b657-447">Hinzufügen von wslconfig/terminate zum Beenden ausgeführter Distributionen</span><span class="sxs-lookup"><span data-stu-id="9b657-447">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="9b657-448">Build 17692</span><span class="sxs-lookup"><span data-stu-id="9b657-448">Build 17692</span></span>
<span data-ttu-id="9b657-449">Allgemeine Windows-Informationen zu Build 17692 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="9b657-449">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-450">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-450">WSL</span></span>
* <span data-ttu-id="9b657-451">Korrektur des Problems mit den Kontextmenüeinträgen der WSL-Shell, die Pfade mit Leerzeichen nicht ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="9b657-451">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="9b657-452">Bereitstellen von Unterscheidung von Groß-/Kleinschreibung pro Verzeichnis als erweitertes Attribut</span><span class="sxs-lookup"><span data-stu-id="9b657-452">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="9b657-453">ARM64: Emulieren von Cacheverwaltungsvorgängen.</span><span class="sxs-lookup"><span data-stu-id="9b657-453">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="9b657-454">Beheben von [dotnet-Problem](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="9b657-454">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="9b657-455">DrvFs: Nur Escapezeichen im privaten Bereich, die einem mit Escapezeichen versehenen Zeichen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9b657-455">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="9b657-456">Build 17686</span><span class="sxs-lookup"><span data-stu-id="9b657-456">Build 17686</span></span>
<span data-ttu-id="9b657-457">Allgemeine Windows-Informationen zu Build 17686 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="9b657-457">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-458">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-458">WSL</span></span>
* <span data-ttu-id="9b657-459">Korrektur eines Off-by-one-Fehlers in der Längenüberprüfung des ELF Parserinterpreters [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="9b657-459">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="9b657-460">Absolute WSL-Timer mit einer Zeitangabe in der Vergangenheit werden nicht ausgelöst [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="9b657-460">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="9b657-461">Sicherstellen, dass neu erstellte Analysepunkte als solche im übergeordneten Verzeichnis aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-461">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="9b657-462">Atomarisches Erstellen von Verzeichnissen mit Berücksichtigung von Groß- und Kleinschreibung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9b657-462">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="9b657-463">Build 17677</span><span class="sxs-lookup"><span data-stu-id="9b657-463">Build 17677</span></span>
<span data-ttu-id="9b657-464">Allgemeine Windows-Informationen zu Build 17677 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="9b657-464">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-465">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-465">WSL</span></span>
* <span data-ttu-id="9b657-466">Korrektur eines zusätzlichen Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-466">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="9b657-467">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="9b657-467">[GH 2712]</span></span>
* <span data-ttu-id="9b657-468">Korrektur eines WSL-Startfehlers, wenn UMCI aktiviert ist.-</span><span class="sxs-lookup"><span data-stu-id="9b657-468">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="9b657-469">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="9b657-469">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="9b657-470">Build 17666</span><span class="sxs-lookup"><span data-stu-id="9b657-470">Build 17666</span></span>
<span data-ttu-id="9b657-471">Allgemeine Windows-Informationen zu Build 17666 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="9b657-471">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-472">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-472">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="9b657-473">WARNUNG: Es gibt ein Problem, das das Ausführen von WSL in einigen AMD-Chipsätzen verhindert [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="9b657-473">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="9b657-474">Eine Korrektur ist verfügbar und wird in den Insider Build-Branch integriert.</span><span class="sxs-lookup"><span data-stu-id="9b657-474">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="9b657-475">Hinzufügen des Explorer-Kontextmenüs zum Starten von WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="9b657-475">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="9b657-476">Halten Sie in einem Explorer-Fenster die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste, um diese Option zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="9b657-476">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="9b657-477">Korrektur des nicht blockierenden UNIX-Socketverhaltens [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="9b657-477">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="9b657-478">Korrigieren des hängenden NETLINK-Befehls, wie in GH 2026 gemeldet.</span><span class="sxs-lookup"><span data-stu-id="9b657-478">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="9b657-479">Hinzufügen von Unterstützung für Einbindungsweitergabeflags [GH 2911]</span><span class="sxs-lookup"><span data-stu-id="9b657-479">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="9b657-480">Korrektur von Problem mit truncate, das keine inotify-Ereignisse verursacht [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="9b657-480">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="9b657-481">Hinzufügen der Option --exec für „wsl.exe“ zum Aufrufen eine einzelne Binärdatei ohne Shell.</span><span class="sxs-lookup"><span data-stu-id="9b657-481">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="9b657-482">Hinzufügen der Option --distribution für „wsl.exe“, um eine bestimmte Distribution auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9b657-482">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="9b657-483">Build 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="9b657-483">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="9b657-484">Allgemeine Windows-Informationen zu Build 17655 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9b657-484">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-485">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-485">WSL</span></span>
* <span data-ttu-id="9b657-486">Eingeschränkte Unterstützung für dmesg.</span><span class="sxs-lookup"><span data-stu-id="9b657-486">Limited support for dmesg.</span></span> <span data-ttu-id="9b657-487">Anwendungen können sich jetzt in dmesg protokollieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-487">Applications can now log to dmesg.</span></span> <span data-ttu-id="9b657-488">Der WSL-Treiber protokolliert eingeschränkte Informationen in dmesg.</span><span class="sxs-lookup"><span data-stu-id="9b657-488">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="9b657-489">In Zukunft kann dies so erweitert werden, dass andere Informationen/Diagnoseinhalte vom Treiber erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-489">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="9b657-490">Hinweis: dmesg wird derzeit über die `/dev/kmsg`-Geräteschnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-490">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="9b657-491">`syslog`-Systemaufrufschnittstelle wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-491">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="9b657-492">Daher funktionieren einige der `dmesg`-Befehlszeilenoptionen (z.B. `-S`, `-C`) nicht.</span><span class="sxs-lookup"><span data-stu-id="9b657-492">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="9b657-493">Korrektur eines Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-493">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="9b657-494">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="9b657-494">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="9b657-495">Build 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="9b657-495">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="9b657-496">Allgemeine Windows-Informationen zu Build 17639 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9b657-496">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-497">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-497">WSL</span></span>
* <span data-ttu-id="9b657-498">Änderung der Standard-GID und des Modus von seriellen Geräten entsprechend den nativen Einstellungen [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="9b657-498">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="9b657-499">DrvFs unterstützt jetzt erweiterte Attribute.</span><span class="sxs-lookup"><span data-stu-id="9b657-499">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="9b657-500">Hinweis: Für DrvFs gelten einige Einschränkungen für den Namen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="9b657-500">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="9b657-501">Insbesondere sind einige Zeichen (etwa „/“, „:“ und „\*“) unzulässig, und für Namen erweiterter Attribute wird in DrvFs keine Groß- und Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-501">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="9b657-502">Build 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="9b657-502">Build 17133 (Fast)</span></span>
<span data-ttu-id="9b657-503">Allgemeine Windows-Informationen zu Build 17133 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="9b657-503">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-504">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-504">WSL</span></span>
* <span data-ttu-id="9b657-505">Fehlerbehebung für Hängen in WSL.</span><span class="sxs-lookup"><span data-stu-id="9b657-505">Fix for hang in WSL.</span></span> <span data-ttu-id="9b657-506">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="9b657-506">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="9b657-507">Build 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="9b657-507">Build 17128 (Fast)</span></span>
<span data-ttu-id="9b657-508">Allgemeine Windows-Informationen zu Build 17128 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="9b657-508">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-509">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-509">WSL</span></span>
* <span data-ttu-id="9b657-510">Keine</span><span class="sxs-lookup"><span data-stu-id="9b657-510">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="9b657-511">Build 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="9b657-511">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="9b657-512">Allgemeine Windows-Informationen zu Build 17627 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9b657-512">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-513">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-513">WSL</span></span>
* <span data-ttu-id="9b657-514">Hinzufügen von Unterstützung für futex-pi-fähige Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="9b657-514">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="9b657-515">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="9b657-515">[GH 1006]</span></span>
    * <span data-ttu-id="9b657-516">Beachten Sie, dass Prioritäten derzeit keine unterstützte WSL-Funktion sind, sodass Einschränkungen bestehen. Die Standardverwenund sollte jedoch aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-516">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="9b657-517">Windows-Firewallunterstützung für WSL-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="9b657-517">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="9b657-518">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="9b657-518">[GH 1852]</span></span>
    * <span data-ttu-id="9b657-519">Um beispielsweise zuzulassen, dass der WSL python-Prozess an einem beliebigen Port lauschen kann, verwenden Sie Windows-CMD mit erhöhten Rechten: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="9b657-519">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="9b657-520">Weitere Informationen zum Hinzufügen von Firewallregeln finden Sie unter [Link.](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="9b657-520">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="9b657-521">Beachten der Standardshell des Benutzers bei der Verwendung von „wsl.exe“.</span><span class="sxs-lookup"><span data-stu-id="9b657-521">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="9b657-522">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="9b657-522">[GH 2372]</span></span>
* <span data-ttu-id="9b657-523">Melden aller Netzwerkschnittstellen als Ethernet.</span><span class="sxs-lookup"><span data-stu-id="9b657-523">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="9b657-524">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="9b657-524">[GH 2996]</span></span>
* <span data-ttu-id="9b657-525">Bessere Verarbeitung von beschädigten /etc/passwd-Dateien.</span><span class="sxs-lookup"><span data-stu-id="9b657-525">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="9b657-526">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="9b657-526">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="9b657-527">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-527">Console</span></span>
* <span data-ttu-id="9b657-528">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-528">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-529">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-529">LTP Results:</span></span>
<span data-ttu-id="9b657-530">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-530">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="9b657-531">Build 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="9b657-531">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="9b657-532">Allgemeine Windows-Informationen zu Build 17618 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9b657-532">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-533">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-533">WSL</span></span>
* <span data-ttu-id="9b657-534">Einführung in Pseudoconsolenfunktionalität für NT-Interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="9b657-534">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="9b657-535">Der Legacyinstallationsmechanismus („lxrun.exe“) ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="9b657-535">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="9b657-536">Der unterstützte Mechanismus zum Installieren von Distributionen ist der Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9b657-536">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="9b657-537">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-537">Console</span></span>
* <span data-ttu-id="9b657-538">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-538">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-539">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-539">LTP Results:</span></span>
<span data-ttu-id="9b657-540">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-540">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="9b657-541">Build 17110</span><span class="sxs-lookup"><span data-stu-id="9b657-541">Build 17110</span></span>
<span data-ttu-id="9b657-542">Allgemeine Windows-Informationen zu Build 17110 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="9b657-542">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-543">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-543">WSL</span></span>
* <span data-ttu-id="9b657-544">Zulassen, dass /init aus Windows beendet wird [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="9b657-544">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="9b657-545">DrvFs verwendet nun standardmäßig Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis (entspricht der Einbindungsoption „case=dir“).</span><span class="sxs-lookup"><span data-stu-id="9b657-545">DrvFs now uses per-directory case sensitivity by default (equivalent to the "case=dir" mount option).</span></span>
    * <span data-ttu-id="9b657-546">Wenn Sie „case=force“ verwenden (das alte Verhalten), muss ein Registrierungsschlüssel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-546">Using "case=force" (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="9b657-547">Führen Sie den folgenden Befehl aus, um „case=force“ zu aktivieren, wenn Sie diese Option verwenden müssen: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="9b657-547">Run the following command to enable "case=force" if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="9b657-548">Wenn Sie über vorhandene Verzeichnisse verfügen, die mit WSL in einer älteren Version von Windows erstellt wurden, bei denen die Groß-/Kleinschreibung beachtet werden muss, verwenden Sie „fsutil.exe“, um sie für Unterscheidung von Groß-/Kleinschreibung zu markieren: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="9b657-548">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="9b657-549">NULL-Beendigungszeichenfolgen werden vom uname-Systemaufruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9b657-549">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="9b657-550">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-550">Console</span></span>
* <span data-ttu-id="9b657-551">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-551">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-552">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-552">LTP Results:</span></span>
<span data-ttu-id="9b657-553">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-553">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="9b657-554">Build 17107</span><span class="sxs-lookup"><span data-stu-id="9b657-554">Build 17107</span></span>
<span data-ttu-id="9b657-555">Allgemeine Windows-Informationen zu Build 17107 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="9b657-555">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-556">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-556">WSL</span></span>
* <span data-ttu-id="9b657-557">Unterstützung von TCSETSF und TCSETSW für pty-Masterendpunkte [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="9b657-557">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="9b657-558">Starten von gleichzeitigen Interop-Prozessen kann zu EINVAL führen [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="9b657-558">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="9b657-559">Korrektur von PTRACE_ATTACH, um den richtigen Ablaufverfolgungsstatus in „/proc/pid/status“ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b657-559">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="9b657-560">Korrektur der Racebedingung, bei der kurzlebige Prozesse, die mit den CLEARTID- und SETTID-Flags geklont wurden, ohne Löschen der TID-Adresse beendet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="9b657-560">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="9b657-561">Anzeigen einer Meldung beim Aktualisieren der Linux-Dateisystemverzeichnisse beim Umstieg von einem Build vor 17093.</span><span class="sxs-lookup"><span data-stu-id="9b657-561">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="9b657-562">Weitere Informationen zu den Änderungen für das 17093-Dateisystem finden Sie in den Anmerkungen zur Version für [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="9b657-562">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="9b657-563">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-563">Console</span></span>
* <span data-ttu-id="9b657-564">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-564">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-565">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-565">LTP Results:</span></span>
<span data-ttu-id="9b657-566">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-566">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="9b657-567">Build 17101</span><span class="sxs-lookup"><span data-stu-id="9b657-567">Build 17101</span></span>
<span data-ttu-id="9b657-568">Allgemeine Windows-Informationen zu Build 17101 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="9b657-568">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-569">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-569">WSL</span></span>
* <span data-ttu-id="9b657-570">Unterstützung für signalfd.</span><span class="sxs-lookup"><span data-stu-id="9b657-570">Support for signalfd.</span></span> <span data-ttu-id="9b657-571">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="9b657-571">[GH 129]</span></span>
* <span data-ttu-id="9b657-572">Unterstützung von Dateinamen, die ungültige NTFS-Zeichen enthalten, durch Codieren als private Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="9b657-572">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="9b657-573">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="9b657-573">[GH 1514]</span></span>
* <span data-ttu-id="9b657-574">Automatisches Einbinden greift auf den schreibgeschützten Modus zurück, wenn Schreibvorgänge nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-574">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="9b657-575">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="9b657-575">[GH 2603]</span></span>
* <span data-ttu-id="9b657-576">Ermöglichen des Einfügens von Unicode-Ersatzzeichenpaaren (z.B. Emojis).</span><span class="sxs-lookup"><span data-stu-id="9b657-576">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="9b657-577">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="9b657-577">[GH 2765]</span></span>
* <span data-ttu-id="9b657-578">Pseudodateien in „/proc“ und „/sys“ sollten „read“ und „write ready“ aus select, poll, epoll, usw. zurückgeben [GH 2838].</span><span class="sxs-lookup"><span data-stu-id="9b657-578">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="9b657-579">Korrektur eines Problems, das dazu führen kann, dass der Dienst in eine Endlosschleife übergeht, wenn die Registrierung manipuliert wurde oder beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-579">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="9b657-580">Korrektur von Netlink-Nachrichten, sodass sie mit neueren Versionen von iproute2 (upstream 4.14) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-580">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="9b657-581">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-581">Console</span></span>
* <span data-ttu-id="9b657-582">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-582">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-583">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-583">LTP Results:</span></span>
<span data-ttu-id="9b657-584">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-584">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="9b657-585">Build 17093</span><span class="sxs-lookup"><span data-stu-id="9b657-585">Build 17093</span></span>
<span data-ttu-id="9b657-586">Allgemeine Windows-Informationen zu Build 17093 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-586">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="9b657-587">Wichtig:</span><span class="sxs-lookup"><span data-stu-id="9b657-587">Important:</span></span>
<span data-ttu-id="9b657-588">Wenn Sie WSL zum ersten Mal nach dem Upgrade auf diesen Build starten, müssen Sie einige Aufgaben durchführen, um die Linux-Dateisystemverzeichnisse zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-588">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="9b657-589">Dieser Vorgang kann einige Minuten in Anspruch nehmen, sodass WSL möglicherweise langsam zu starten scheint.</span><span class="sxs-lookup"><span data-stu-id="9b657-589">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="9b657-590">Dies sollte nur ein Mal für jede Distribution erfolgen, die Sie aus dem Store installiert haben.</span><span class="sxs-lookup"><span data-stu-id="9b657-590">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="9b657-591">Verbesserte Unterscheidung von Groß-/Kleinschreibung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="9b657-591">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="9b657-592">DrvFs unterstützt jetzt Berücksichtigung von Groß-/Kleinschreibung pro Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="9b657-592">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="9b657-593">Dies ist ein neues Flag, das für Verzeichnisse festgelegt werden kann, um anzugeben, dass alle Vorgänge in diesen Verzeichnissen mit Unterscheidung zwischen Groß-/Kleinschreibung behandelt werden sollen, sodass sogar Windows-Anwendungen Dateien ordnungsgemäß öffnen können, bei denen sich nur die Groß-/Kleinschreibung unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="9b657-593">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="9b657-594">DrvFs verfügt über neue Einbindungsoptionen, die die Berücksichtigung von Groß-/Kleinschreibung pro Verzeichnis steuern.</span><span class="sxs-lookup"><span data-stu-id="9b657-594">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="9b657-595">case=force: Für alle Verzeichnisse wird zwischen Groß-/Kleinschreibung unterschieden (mit Ausnahme des Laufwerkstamms).</span><span class="sxs-lookup"><span data-stu-id="9b657-595">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="9b657-596">Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-596">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="9b657-597">Dies ist das Legacyverhalten (ausgenommen, wenn neue Verzeichnisse für Unterscheidung zwischen Groß-/Kleinschreibung markiert werden).</span><span class="sxs-lookup"><span data-stu-id="9b657-597">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="9b657-598">case=dir: Nur für Verzeichnisse mit dem Flag für Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis wird Groß-/Kleinschreibung beachtet, für alle anderen Verzeichnisse nicht.</span><span class="sxs-lookup"><span data-stu-id="9b657-598">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="9b657-599">Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-599">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="9b657-600">case=dir: Nur für Verzeichnisse mit dem Flag für Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis wird Groß-/Kleinschreibung beachtet, für alle anderen Verzeichnisse nicht.</span><span class="sxs-lookup"><span data-stu-id="9b657-600">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="9b657-601">Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-601">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="9b657-602">Hinweis: Für Verzeichnisse, die in früheren Versionen von WSL erstellt wurden, ist dieses Flag nicht festgelegt, sodass bei Verwendung der Option „case=dir“ keine Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-602">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the "case=dir" option.</span></span> <span data-ttu-id="9b657-603">Eine Möglichkeit, dieses Flag für vorhandene Verzeichnisse festzulegen, ist in Kürze verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b657-603">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="9b657-604">Beispiel für die Einbindung mit diesen Optionen (für vorhandene Laufwerke müssen Sie zuerst die Einbindung aufheben, bevor Sie die Einbindung mit anderen Optionen ausführen können): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="9b657-604">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="9b657-605">Momentan ist case=force immer noch die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="9b657-605">For now, case=force is still the default option.</span></span> <span data-ttu-id="9b657-606">Dies wird in Zukunft in case=dir geändert.</span><span class="sxs-lookup"><span data-stu-id="9b657-606">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="9b657-607">Sie können jetzt Schrägstriche in Windows-Pfaden verwenden, wenn Sie DrvFs einbinden, z.B. sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="9b657-607">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="9b657-608">WSL verarbeitet nun die /etc/fstab-Datei während des Instanzstarts [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="9b657-608">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="9b657-609">Dies erfolgt vor der automatischen Einbindung von DrvFs-Laufwerken. Alle Laufwerke, die bereits von fstab eingebunden wurden, werden nicht automatisch erneut eingebunden, sodass Sie den Einbindungspunkt für bestimmte Laufwerke ändern können.</span><span class="sxs-lookup"><span data-stu-id="9b657-609">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="9b657-610">Dieses Verhalten kann mithilfe von „wsl.conf“ deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-610">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="9b657-611">Die mount, mountinfo- und mountstats-Dateien in „/proc“ versehen Sonderzeichen wie umgekehrte Schrägstriche und Leerzeichen ordnungsgemäß mit Escapezeichen [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="9b657-611">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="9b657-612">Spezielle Dateien, die mit DrvFs erstellt werden (z.B. symbolische WSL-Verknüpfungen oder Fifos und Sockets, wenn Metadaten aktiviert sind), können nun aus Windows kopiert und verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-612">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="9b657-613">WSL ist mit „wsl.conf“ besser konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="9b657-613">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="9b657-614">Es wurde eine Methode zum automatischen Konfigurieren bestimmter Funktionen in WSL hinzugefügt, die jedes Mal angewendet wird, wenn Sie das Subsystem starten.</span><span class="sxs-lookup"><span data-stu-id="9b657-614">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="9b657-615">Dies umfasst Optionen für die automatische Einbindung und Netzwerkkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="9b657-615">This includes automount options and network configuration.</span></span> <span data-ttu-id="9b657-616">Weitere Informationen hierzu finden Sie in unserem Blogbeitrag unter: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="9b657-616">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="9b657-617">AF_UNIX ermöglicht Socketverbindungen zwischen Linux-Prozessen für WSL- und native Windows-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="9b657-617">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="9b657-618">WSL- und Windows-Anwendungen können nun über Unix-Sockets miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-618">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="9b657-619">Stellen Sie sich vor, Sie möchten einen Dienst in Windows ausführen und sowohl für Windows- als auch für WSL-Apps verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="9b657-619">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="9b657-620">Das ist nun mit UNIX-Sockets möglich.</span><span class="sxs-lookup"><span data-stu-id="9b657-620">Now, that's possible with Unix sockets.</span></span> <span data-ttu-id="9b657-621">Weitere Informationen finden Sie in unserem Blogbeitrag unter https://aka.ms/afunixinterop.</span><span class="sxs-lookup"><span data-stu-id="9b657-621">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-622">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-622">WSL</span></span>
* <span data-ttu-id="9b657-623">Unterstützung von mmap() mit MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="9b657-623">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="9b657-624">Unterstützung von CLONE_PTRACE und CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="9b657-624">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="9b657-625">Verarbeiten eines Nicht-SIGCHLD-Beendigungssignals im Klon [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="9b657-625">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="9b657-626">Stub für /proc/sys/fs/inotify/max_user_instances und /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="9b657-626">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="9b657-627">Fehler beim Laden von ELF-Binärdateien, die Ladeheader mit Offsets ungleich NULL enthalten [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="9b657-627">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="9b657-628">Eliminieren von nachfolgenden Seitenbytes beim Laden von Images.</span><span class="sxs-lookup"><span data-stu-id="9b657-628">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="9b657-629">Verringern der Fälle, in denen execve den Prozess automatisch beendet</span><span class="sxs-lookup"><span data-stu-id="9b657-629">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="9b657-630">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-630">Console</span></span>
* <span data-ttu-id="9b657-631">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-631">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-632">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-632">LTP Results:</span></span>
<span data-ttu-id="9b657-633">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-633">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="9b657-634">Build 17083</span><span class="sxs-lookup"><span data-stu-id="9b657-634">Build 17083</span></span>
<span data-ttu-id="9b657-635">Allgemeine Windows-Informationen zu Build 17083 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-635">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-636">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-636">WSL</span></span>
* <span data-ttu-id="9b657-637">Korrektur der Fehlerüberprüfung für epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="9b657-637">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="9b657-638">Korrektur von Hängern beim Deaktivieren von ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="9b657-638">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="9b657-639">Sicherstellen, dass mmap-Vorgänge atomarisch erscheinen [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="9b657-639">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="9b657-640">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-640">Console</span></span>
* <span data-ttu-id="9b657-641">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-641">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-642">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-642">LTP Results:</span></span>
<span data-ttu-id="9b657-643">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-643">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="9b657-644">Build 17074</span><span class="sxs-lookup"><span data-stu-id="9b657-644">Build 17074</span></span>
<span data-ttu-id="9b657-645">Allgemeine Windows-Informationen zu Build 17074 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-645">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-646">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-646">WSL</span></span>
* <span data-ttu-id="9b657-647">Festes Speicherformat von DrvFs-Metadaten [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="9b657-647">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="9b657-648">**Wichtig:** Die vor diesem Build erstellten DrvFs-Metadaten werden falsch oder überhaupt nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b657-648">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="9b657-649">Um betroffene Dateien zu korrigieren, verwenden Sie chmod und chown zum erneuten Anwenden der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="9b657-649">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="9b657-650">Korrektur eines Problems mit mehreren Signalen und neu startbaren Systemaufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b657-650">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="9b657-651">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-651">Console</span></span>
* <span data-ttu-id="9b657-652">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-652">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-653">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-653">LTP Results:</span></span>
<span data-ttu-id="9b657-654">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-654">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="9b657-655">Build 17063</span><span class="sxs-lookup"><span data-stu-id="9b657-655">Build 17063</span></span>
<span data-ttu-id="9b657-656">Allgemeine Windows-Informationen zu Build 17063 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-656">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="9b657-657">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-657">WSL</span></span>
* <span data-ttu-id="9b657-658">DrvFs unterstützt zusätzliche Linux-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="9b657-658">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="9b657-659">Dies ermöglicht das Festlegen des Besitzers und des Dateimodus mit chmod/chown sowie das Erstellen spezieller Dateien, etwa Fifos, Unix-Sockets und Gerätedateien.</span><span class="sxs-lookup"><span data-stu-id="9b657-659">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="9b657-660">Diese Option ist zurzeit standardmäßig deaktiviert, da Sie noch experimentell ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-660">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="9b657-661">**Hinweis:**  Wir haben einen Fehler im Metadatenformat behoben, das von DrvFs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-661">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="9b657-662">Obwohl Metadaten in diesem Build für Experimente funktionieren, lesen zukünftige Builds die von diesem Build erstellten Metadaten nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="9b657-662">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="9b657-663">Möglicherweise müssen Sie den Besitzer für geänderte Dateien manuell aktualisieren, und Geräte mit einer benutzerdefinierten Geräte-ID müssen neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-663">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="9b657-664">Um diese Funktion zu aktivieren, binden Sie DrvFs mit der Metadatenoption ein (um sie für eine vorhandene Einbindung zu aktivieren, müssen Sie die Einbindung zunächst aufheben):</span><span class="sxs-lookup"><span data-stu-id="9b657-664">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="9b657-665">Linux-Berechtigungen werden der Datei als zusätzliche Metadaten hinzugefügt. Sie wirken sich nicht auf die Windows-Berechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="9b657-665">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="9b657-666">Beachten Sie, dass beim Bearbeiten einer Datei mithilfe eines Windows-Editors die Metadaten möglicherweise entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-666">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="9b657-667">In diesem Fall wird die Datei auf die Standardberechtigungen zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9b657-667">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="9b657-668">Hinzufügen von Einbindungsoptionen zu DrvFs, um Dateien ohne Metadaten zu steuern.</span><span class="sxs-lookup"><span data-stu-id="9b657-668">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="9b657-669">uid: die Benutzer-ID, die für den Besitzer aller Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-669">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="9b657-670">gid: die Gruppen-ID, die für den Besitzer aller Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-670">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="9b657-671">umask: Eine oktale Maske mit Berechtigungen, die für alle Dateien und Verzeichnisse ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b657-671">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="9b657-672">fmask: Eine oktale Maske mit Berechtigungen, die für alle regulären Dateien ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b657-672">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="9b657-673">dmask: Eine oktale Maske mit Berechtigungen, die für alle Verzeichnisse ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b657-673">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="9b657-674">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b657-674">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="9b657-675">Kombinieren Sie dies mit der Metadatenoption, um Standardberechtigungen für Dateien ohne Metadaten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9b657-675">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="9b657-676">Wird in einer neuen Umgebungsvariablen (`WSLENV`) eingeführt, um zu konfigurieren, wie Umgebungsvariablen zwischen WSL und Win32 ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-676">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="9b657-677">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9b657-677">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="9b657-678">`WSLENV` eine durch Doppelpunkte getrennte Liste von Umgebungsvariablen, die beim Starten von WSL-Prozessen aus Win32 oder Win32-Prozessen aus WSL eingeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="9b657-678">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="9b657-679">Jeder Variablen kann ein Schrägstrich als Suffix vorangestellt werden, gefolgt von Flags, um anzugeben, wie sie übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b657-679">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="9b657-680">p: Der Wert ist ein Pfad, der zwischen WSL-Pfaden und Win32-Pfaden übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9b657-680">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="9b657-681">l: Der Wert ist eine Liste von Pfaden.</span><span class="sxs-lookup"><span data-stu-id="9b657-681">l: The value is a list of paths.</span></span> <span data-ttu-id="9b657-682">In WSL ist es eine durch Doppelpunkte getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="9b657-682">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="9b657-683">In Win32 ist es eine durch Semikolons getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="9b657-683">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="9b657-684">u: Der Wert sollte nur beim Aufrufen von WSL aus Win32 eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-684">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="9b657-685">w: Der Wert sollte nur beim Aufrufen von Win32 aus WSL eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-685">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="9b657-686">Sie können `WSLENV` in der BASHRC-Datei oder in der benutzerdefinierten Windows-Umgebung für Ihren Benutzer festlegen.</span><span class="sxs-lookup"><span data-stu-id="9b657-686">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="9b657-687">drvfs wird ordnungsgemäß eingebunden und behält Zeitstempel aus from tar, cp -p bei (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="9b657-687">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="9b657-688">Symbolische drvfs-Verknüpfungen geben die richtige Größe an (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="9b657-688">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="9b657-689">Lese-/Schreibvorgänge funktionieren für sehr große E/A-Größen (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="9b657-689">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="9b657-690">waitpid funktioniert mit Prozessgruppen-IDs (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="9b657-690">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="9b657-691">Erheblich verbesserte mmap-Leistung für große reserve-Regionen, Verbesserung der ghc-Leistung (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="9b657-691">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="9b657-692">personality unterstützt READ_IMPLIES_EXEC, Korrekturen maxima und clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="9b657-692">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="9b657-693">mprotect unterstützt PROT_GROWSDOWN,;Korrekturen clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="9b657-693">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="9b657-694">Seitenfehlerkorrekturen im Overcommitmodus, Korrekturen sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="9b657-694">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="9b657-695">clone unterstützt weitere Flagkombinationen</span><span class="sxs-lookup"><span data-stu-id="9b657-695">clone supports more flags combinations</span></span>
* <span data-ttu-id="9b657-696">Unterstützung von select/epoll von epoll-Dateien (zuvor eine Nulloperation).</span><span class="sxs-lookup"><span data-stu-id="9b657-696">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="9b657-697">Benachrichtigen von ptrace über nicht implementierte Systemaufrufe.</span><span class="sxs-lookup"><span data-stu-id="9b657-697">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="9b657-698">Ignorieren von Schnittstellen, die nicht aktiv sind, beim Generieren von resolv.conf-Namenservern [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="9b657-698">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="9b657-699">Aufzählen von Netzwerkschnittstellen ohne physische Adresse.</span><span class="sxs-lookup"><span data-stu-id="9b657-699">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="9b657-700">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="9b657-700">[GH 2685]</span></span>
* <span data-ttu-id="9b657-701">Zusätzliche Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-701">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="9b657-702">Linux-Tools für Entwickler unter Windows verfügbar</span><span class="sxs-lookup"><span data-stu-id="9b657-702">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="9b657-703">Windows-Befehlszeilen-Toolkette enthält bsdtar (tar) und curl.</span><span class="sxs-lookup"><span data-stu-id="9b657-703">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="9b657-704">Lesen Sie [diesen Blog](https://aka.ms/tarcurlwindows), um mehr über das Hinzufügen dieser beiden neuen Tools zu erfahren, und sehen Sie, wie Sie das Entwicklererlebnis unter Windows formen.</span><span class="sxs-lookup"><span data-stu-id="9b657-704">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they're shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="9b657-705">`AF_UNIX` ist im Windows Insider SDK (17061 und höher) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b657-705">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="9b657-706">Lesen Sie [diesen Blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), um weitere Informationen zu `AF_UNIX` zu erhalten und mehr über die Verwendung in Windows durch Entwickler zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="9b657-706">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="9b657-707">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-707">Console</span></span>
* <span data-ttu-id="9b657-708">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-708">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-709">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-709">LTP Results:</span></span>
<span data-ttu-id="9b657-710">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-710">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="9b657-711">Build 17046</span><span class="sxs-lookup"><span data-stu-id="9b657-711">Build 17046</span></span>

<span data-ttu-id="9b657-712">Allgemeine Windows-Informationen zu Build 17046 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="9b657-712">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="9b657-713">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-713">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-714">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-714">WSL</span></span>
- <span data-ttu-id="9b657-715">Ermöglicht das Ausführen von Prozessen ohne ein aktives Terminal.</span><span class="sxs-lookup"><span data-stu-id="9b657-715">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="9b657-716">[GH 709, 1007, 1511, 2252, 2391 usw.]</span><span class="sxs-lookup"><span data-stu-id="9b657-716">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="9b657-717">Bessere Unterstützung von CLONE_VFORK und CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="9b657-717">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="9b657-718">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="9b657-718">[GH 1878, 2615]</span></span>
- <span data-ttu-id="9b657-719">Überspringen der TDI-Filtertreiber für WSL-Netzwerkvorgänge.</span><span class="sxs-lookup"><span data-stu-id="9b657-719">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="9b657-720">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="9b657-720">[GH 1554]</span></span>
- <span data-ttu-id="9b657-721">DrvFs erstellt symbolische NT-Verknüpfungen, wenn bestimmte Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="9b657-721">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="9b657-722">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="9b657-722">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="9b657-723">Das Verknüpfungsziel muss relativ sein, darf keine Einbindungspunkte oder symbolische Verknüpfungen kreuzen und muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="9b657-723">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="9b657-724">Der Benutzer muss über SE_CREATE_SYMBOLIC_LINK_PRIVILEGE verfügen (dies erfordert normalerweise, dass Sie „wsl.exe“ mit erhöhten Rechten starten), sofern der Entwicklermodus nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-724">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="9b657-725">Unter allen anderen Umständen erstellt DrvFs weiterhin symbolische WSL-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-725">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="9b657-726">Ermöglichen der gleichzeitigen Ausführung von WSL-Instanzen mit und ohne erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="9b657-726">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="9b657-727">Unterstützung von /proc/sys/kernel/Yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="9b657-727">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="9b657-728">Hinzufügen von wslpath zum Durchführen von Konvertierungen von WSL-<- >Windows-Pfaden.</span><span class="sxs-lookup"><span data-stu-id="9b657-728">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="9b657-729">[GH 522, 1243, 1834, 2327 usw.]</span><span class="sxs-lookup"><span data-stu-id="9b657-729">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a><span data-ttu-id="9b657-730">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-730">Console</span></span>
- <span data-ttu-id="9b657-731">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="9b657-731">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-732">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-732">LTP Results:</span></span>
<span data-ttu-id="9b657-733">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-733">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="9b657-734">Build 17040</span><span class="sxs-lookup"><span data-stu-id="9b657-734">Build 17040</span></span>

<span data-ttu-id="9b657-735">Allgemeine Windows-Informationen zu Build 17040 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="9b657-735">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-736">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-737">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-737">WSL</span></span>
- <span data-ttu-id="9b657-738">Keine Korrekturen seit 17035.</span><span class="sxs-lookup"><span data-stu-id="9b657-738">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-739">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-739">Console</span></span>
- <span data-ttu-id="9b657-740">Keine Korrekturen seit 17035.</span><span class="sxs-lookup"><span data-stu-id="9b657-740">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-741">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-741">LTP Results:</span></span>
<span data-ttu-id="9b657-742">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-742">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="9b657-743">Build 17035</span><span class="sxs-lookup"><span data-stu-id="9b657-743">Build 17035</span></span>

<span data-ttu-id="9b657-744">Allgemeine Windows-Informationen zu Build 17035 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="9b657-744">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-745">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-746">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-746">WSL</span></span>
- <span data-ttu-id="9b657-747">Der Zugriff auf Dateien auf DrvFs kann gelegentlich mit EINVAL fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="9b657-747">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="9b657-748">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="9b657-748">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-749">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-749">Console</span></span>
- <span data-ttu-id="9b657-750">Farbverlust beim Einfügen/Löschen von Zeilen im VT-Modus.</span><span class="sxs-lookup"><span data-stu-id="9b657-750">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-751">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-751">LTP Results:</span></span>
<span data-ttu-id="9b657-752">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-752">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="9b657-753">Build 17025</span><span class="sxs-lookup"><span data-stu-id="9b657-753">Build 17025</span></span>

<span data-ttu-id="9b657-754">Allgemeine Windows-Informationen zu Build 17025 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="9b657-754">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-755">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-755">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-756">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-756">WSL</span></span>
- <span data-ttu-id="9b657-757">Starten anfänglicher Prozesse in einer neuen Vordergrundprozessgruppe [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="9b657-757">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="9b657-758">Korrekturen der SIGHUP-Übermittlung [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="9b657-758">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="9b657-759">Generieren eines Standardnamens für virtuelle Bridge generieren, wenn keine Angabe erfolgt [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="9b657-759">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="9b657-760">Implementieren von /proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="9b657-760">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="9b657-761">Weitere Interop-Pipekorrekturen für stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="9b657-761">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="9b657-762">Stub für syncfs-Systemaufruf.</span><span class="sxs-lookup"><span data-stu-id="9b657-762">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-763">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-763">Console</span></span>
- <span data-ttu-id="9b657-764">Korrektur der VT-Eingabeübersetzung für Drittanbieterkonsolen [GH 111]</span><span class="sxs-lookup"><span data-stu-id="9b657-764">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-765">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-765">LTP Results:</span></span>
<span data-ttu-id="9b657-766">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-766">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="9b657-767">Build 17017</span><span class="sxs-lookup"><span data-stu-id="9b657-767">Build 17017</span></span>

<span data-ttu-id="9b657-768">Allgemeine Windows-Informationen zu Build 17017 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="9b657-768">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-769">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-769">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-770">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-770">WSL</span></span>
- <span data-ttu-id="9b657-771">Ignorieren leerer ELF-Programmheader [GH 330].</span><span class="sxs-lookup"><span data-stu-id="9b657-771">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="9b657-772">Ermöglichen, dass LxssManager WSL-Instanzen für nicht interaktive Benutzer erstellt (Unterstützung für SSH und geplante Aufgaben) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="9b657-772">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="9b657-773">Unterstützung von WSL->Win32->WSL-Szenarien („Inception“) [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="9b657-773">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="9b657-774">Eingeschränkte Unterstützung für das Beenden von Konsolen-Apps, die über Interop aufgerufen wurden [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="9b657-774">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="9b657-775">Unterstützung von Einbindungsoptionen für devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="9b657-775">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="9b657-776">Ptrace blockiert den Start untergeordneter Prozesse [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="9b657-776">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="9b657-777">EPOLLET fehlen einige Ereignisse [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="9b657-777">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="9b657-778">Rückgabe einer größeren Anzahl von Daten für PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="9b657-778">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="9b657-779">Getdents mit lseek liefert falsche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9b657-779">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="9b657-780">Korrektur einiger Hänger von Win32-Interop-Apps, die auf Eingaben in einer Pipe warten, die keine weiteren Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="9b657-780">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="9b657-781">O_ASYNC-Unterstützung für tty/pty-Dateien.</span><span class="sxs-lookup"><span data-stu-id="9b657-781">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="9b657-782">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-782">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-783">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-783">Console</span></span>
- <span data-ttu-id="9b657-784">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-784">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-785">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-785">LTP Results:</span></span>
<span data-ttu-id="9b657-786">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b657-786">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="9b657-787">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="9b657-787">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="9b657-788">Build 16288</span><span class="sxs-lookup"><span data-stu-id="9b657-788">Build 16288</span></span>

<span data-ttu-id="9b657-789">Allgemeine Windows-Informationen zu Build 16288 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="9b657-789">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-790">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-790">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-791">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-791">WSL</span></span>
- <span data-ttu-id="9b657-792">Ordnungsgemäße Initialisierung und Meldung von uid, gid und Modus für Socketdateideskriptoren [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="9b657-792">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="9b657-793">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-793">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-794">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-794">Console</span></span>
- <span data-ttu-id="9b657-795">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-795">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-796">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-796">LTP Results:</span></span>
<span data-ttu-id="9b657-797">Keine Änderung seit 16273</span><span class="sxs-lookup"><span data-stu-id="9b657-797">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="9b657-798">Build 16278</span><span class="sxs-lookup"><span data-stu-id="9b657-798">Build 16278</span></span>

<span data-ttu-id="9b657-799">Allgemeine Windows-Informationen zu Build 162738 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="9b657-799">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-800">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-800">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-801">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-801">WSL</span></span>
- <span data-ttu-id="9b657-802">Explizite Aufhebung der Zuordnung zugeordneter Ansichten von dateigestützten Abschnitten beim Beenden des LX MM-Status [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="9b657-802">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="9b657-803">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-803">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-804">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-804">Console</span></span>
- <span data-ttu-id="9b657-805">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-805">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-806">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-806">LTP Results:</span></span>
<span data-ttu-id="9b657-807">Keine Änderung seit 16273</span><span class="sxs-lookup"><span data-stu-id="9b657-807">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="9b657-808">Build 16275</span><span class="sxs-lookup"><span data-stu-id="9b657-808">Build 16275</span></span>

<span data-ttu-id="9b657-809">Allgemeine Windows-Informationen zu Build 162735 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="9b657-809">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-810">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-810">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-811">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-811">WSL</span></span>
- <span data-ttu-id="9b657-812">In diesem Release gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-812">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-813">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-813">Console</span></span>
- <span data-ttu-id="9b657-814">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-814">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-815">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-815">LTP Results:</span></span>
<span data-ttu-id="9b657-816">Keine Änderung seit 16273</span><span class="sxs-lookup"><span data-stu-id="9b657-816">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="9b657-817">Build 16273</span><span class="sxs-lookup"><span data-stu-id="9b657-817">Build 16273</span></span>

<span data-ttu-id="9b657-818">Allgemeine Windows-Informationen zu Build 16273 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-818">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-819">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-819">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-820">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-820">WSL</span></span>
- <span data-ttu-id="9b657-821">Korrektur eines Problems, bei dem DrvFs manchmal den falschen Dateityp für Verzeichnisse gemeldet hat [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="9b657-821">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="9b657-822">Ermöglichen der Erstellung von NETLINK_KOBJECT_UEVENT-Sockets zum Entsperren von Programmen, die uevent verwenden [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="9b657-822">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="9b657-823">Hinzufügen von Unterstützung für nicht blockierende Verbindungen [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="9b657-823">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="9b657-824">Implementieren des CLONE_FS-Klonsystem-Aufrufflags [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="9b657-824">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="9b657-825">Korrektur von Problemen im Zusammenhang mit der nicht ordnungsgemäßen Behandlung von Registerkarten oder Anführungszeichen in NT-Interop [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="9b657-825">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="9b657-826">Beheben des Fehlers „Zugriff verweigert“ beim Versuch, WSL-Instanzen erneut zu starten [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="9b657-826">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="9b657-827">Implementieren von Futex-Vorgängen FUTEX_REQUEUE und FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="9b657-827">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="9b657-828">Korrigieren von Berechtigungen für verschiedene SysFs-Dateien [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="9b657-828">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="9b657-829">Korrigieren des Hängens des Haskell-Stapels während des Setups [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="9b657-829">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="9b657-830">Implementieren der Flags „C“, „O“ und „P“ von binfmt_misc [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="9b657-830">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="9b657-831">Hinzufügen von /proc/sys/kernel/shmmax/shmmni und /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="9b657-831">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="9b657-832">Hinzufügen partieller Unterstützung für den ioprio_set-Systemaufruf [GH 498]</span><span class="sxs-lookup"><span data-stu-id="9b657-832">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="9b657-833">Stub für SO_REUSEPORT und Hinzufügen von Unterstützung für SO_PASSCRED für netlink-Sockets [GH 69]</span><span class="sxs-lookup"><span data-stu-id="9b657-833">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="9b657-834">Rückgabe anderer Fehlercodes aus RegisterDistribuiton, wenn zurzeit eine Distribution installiert oder deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-834">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="9b657-835">Ermöglichen des Aufhebens der Registrierung von teilweise installierten WSL-Distributionen über „wslconfig.exe“</span><span class="sxs-lookup"><span data-stu-id="9b657-835">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="9b657-836">Korrektur des Hängens des Python-Sockettests von udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="9b657-836">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="9b657-837">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-837">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-838">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-838">Console</span></span>
- <span data-ttu-id="9b657-839">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-839">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-840">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-840">LTP Results:</span></span>
<span data-ttu-id="9b657-841">Tests gesamt: 1904</span><span class="sxs-lookup"><span data-stu-id="9b657-841">Total Tests: 1904</span></span><br/>
<span data-ttu-id="9b657-842">Übersprungene Tests gesamt: 209</span><span class="sxs-lookup"><span data-stu-id="9b657-842">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="9b657-843">Fehler gesamt: 229</span><span class="sxs-lookup"><span data-stu-id="9b657-843">Total Failures: 229</span></span><br/>
[<span data-ttu-id="9b657-844">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-844">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="9b657-845">Build 16257</span><span class="sxs-lookup"><span data-stu-id="9b657-845">Build 16257</span></span>

<span data-ttu-id="9b657-846">Allgemeine Windows-Informationen zu Build 16257 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-846">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-847">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-847">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-848">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-848">WSL</span></span>
- <span data-ttu-id="9b657-849">Implementieren des prlimit64-Systemaufrufs</span><span class="sxs-lookup"><span data-stu-id="9b657-849">Implement prlimit64 system call</span></span>
- <span data-ttu-id="9b657-850">Hinzufügen von Unterstützung für ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="9b657-850">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="9b657-851">Stub für MSG_MORE für TCP-Sockets [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="9b657-851">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="9b657-852">Korrektur des ungültigen Verhaltens des AT_EXECFN-Hilfsvektors [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="9b657-852">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="9b657-853">Korrektur des Kopier-/Einfügeverhalten für Konsole/TTY und Hinzufügen einer besseren Verarbeitung voller Puffer [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="9b657-853">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="9b657-854">Festlegen von T_SECURE im Hilfsvektor für set-user-ID- und set-group-ID-Programme [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="9b657-854">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="9b657-855">Psuedoterminal-Masterendpunkt verarbeitet TIOCPGRP nicht [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="9b657-855">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="9b657-856">Korrektur des Nichtzurückspulens von Verzeichnissen in LxFs durch lseek [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="9b657-856">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="9b657-857">/dev/ptmx wird nach hoher Auslastung gesperrt [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="9b657-857">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="9b657-858">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-858">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-859">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-859">Console</span></span>
- <span data-ttu-id="9b657-860">Korrektur für horizontale Linien/Unterstriche überall [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="9b657-860">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="9b657-861">Korrektur der Änderung der Prozessreihenfolge, wodurch das Schließen von NPM erschwert wird [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="9b657-861">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="9b657-862">Hinzufügen des neuen Farbschemas: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="9b657-862">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-863">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-863">LTP Results:</span></span>
<span data-ttu-id="9b657-864">Keine Änderung seit 16251</span><span class="sxs-lookup"><span data-stu-id="9b657-864">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-865">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-865">Syscall Support</span></span>
<span data-ttu-id="9b657-866">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-866">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-867">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-867">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="9b657-868">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="9b657-868">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="9b657-869">[GitHub-Issue 2392: Windows-Ordner werden von WSL nicht erkannt (](https://github.com/Microsoft/BashOnWindows/issues/2392))</span><span class="sxs-lookup"><span data-stu-id="9b657-869">[GitHub Issue 2392: Windows Folders not recognized by WSL ...](https://github.com/Microsoft/BashOnWindows/issues/2392)</span></span>
<span data-ttu-id="9b657-870">In Build 16257 hat WSL beim Aufzählen von Windows-Dateien/-Ordnern über `/mnt/c/...` Probleme.</span><span class="sxs-lookup"><span data-stu-id="9b657-870">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="9b657-871">Dieses Problem wurde behoben und sollte im Insider-Builds in der Woche ab dem 14.08.2017 veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-871">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="9b657-872">Build 16251</span><span class="sxs-lookup"><span data-stu-id="9b657-872">Build 16251</span></span>

<span data-ttu-id="9b657-873">Allgemeine Windows-Informationen zu Build 16251 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-873">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-874">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-874">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-875">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-875">WSL</span></span>
- <span data-ttu-id="9b657-876">Entfernen des Beta-Tags aus der optionalen WSL-Komponente. Weitere Informationen finden Sie im [Blogbeitrag](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="9b657-876">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="9b657-877">Ordnungsgemäße Initialisierung der saved-set uid und gid für set-user-ID- and set-group-ID-Binärdateien bei der Ausführung [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="9b657-877">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="9b657-878">Hinzufügen von Unterstützung für PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="9b657-878">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="9b657-879">Hinzufügen von Unterstützung für PTRACE_GETFPREGS und PTRACE_GETREGSET mit NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="9b657-879">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="9b657-880">Korrektur von ptrace, um bei ignorierten Signalen anzuhalten</span><span class="sxs-lookup"><span data-stu-id="9b657-880">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="9b657-881">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-881">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-882">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-882">Console</span></span>
- <span data-ttu-id="9b657-883">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-883">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-884">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-884">LTP Results:</span></span>
<span data-ttu-id="9b657-885">Anzahl bestandener Tests: 768</span><span class="sxs-lookup"><span data-stu-id="9b657-885">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="9b657-886">Anzahl fehlgeschlagener Tests: 244</span><span class="sxs-lookup"><span data-stu-id="9b657-886">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="9b657-887">Anzahl übersprungener Tests: 96</span><span class="sxs-lookup"><span data-stu-id="9b657-887">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="9b657-888">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="9b657-889">Build 16241</span><span class="sxs-lookup"><span data-stu-id="9b657-889">Build 16241</span></span>

<span data-ttu-id="9b657-890">Allgemeine Windows-Informationen zu Build 16241 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-890">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-891">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-891">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="9b657-892">WSL</span><span class="sxs-lookup"><span data-stu-id="9b657-892">WSL</span></span>
- <span data-ttu-id="9b657-893">In diesem Release gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-893">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="9b657-894">Konsole</span><span class="sxs-lookup"><span data-stu-id="9b657-894">Console</span></span>
- <span data-ttu-id="9b657-895">Korrektur für die Ausgabe des falschen Zeichens für Schnittlinien-DEC, ursprünglich [hier](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) gemeldet</span><span class="sxs-lookup"><span data-stu-id="9b657-895">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="9b657-896">Korrektur, dass kein Ausgabetext in Codepage 65001 (UTF8) angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="9b657-896">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="9b657-897">Übertragen Sie an den RGB-Werten einer Farbe vorgenommene Änderungen nicht an andere Teile der Palette bei Änderungen der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="9b657-897">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="9b657-898">Dadurch wird die Verwendung des Konsoleneigenschaftenblatts erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="9b657-898">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="9b657-899">STRG+S funktioniert anscheinend nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="9b657-899">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="9b657-900">Un-Bold/-Dim fehlt in ANSI-Escapecodes vollständig [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="9b657-900">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="9b657-901">Die Konsole unterstützt VIM-Farbdesigns nicht ordnungsgemäß [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="9b657-901">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="9b657-902">Bestimmte Zeichen können nicht eingefügt werden [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="9b657-902">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="9b657-903">Die Größenänderung von dynamischem Umbruch interagiert seltsam mit der Größenänderung eines Bash-Fensters, wenn sich die Inhalte in der Bearbeitungs-/Befehlszeile befinden [GH-Verbindung 1123]</span><span class="sxs-lookup"><span data-stu-id="9b657-903">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="9b657-904">STRG+L hinterlässt Fragmente auf dem Bildschirm [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="9b657-904">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="9b657-905">Konsolenrenderingfehler bei der Anzeige von VT für HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="9b657-905">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="9b657-906">Japanische Zeichen sehen mit dem Unicode-Zeichen U+30FB seltsam aus [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="9b657-906">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="9b657-907">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-907">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="9b657-908">Build 16237</span><span class="sxs-lookup"><span data-stu-id="9b657-908">Build 16237</span></span>

<span data-ttu-id="9b657-909">Allgemeine Windows-Informationen zu Build 16237 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-909">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-910">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-910">Fixed</span></span>
- <span data-ttu-id="9b657-911">Verwenden von Standardattributen für Dateien ohne E/As in lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="9b657-911">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="9b657-912">Hinzufügen von Unterstützung für Distributionen, die erweiterte Attribute verwenden</span><span class="sxs-lookup"><span data-stu-id="9b657-912">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="9b657-913">Korrektur des Auffüllens für von getdents und getdents64 zurückgegebene Einträge</span><span class="sxs-lookup"><span data-stu-id="9b657-913">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="9b657-914">Korrektur der Berechtigungsüberprüfung für den SHM_STAT-Systemaufruf [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="9b657-914">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="9b657-915">Korrektur des falschen anfänglichen epoll-Zustands für ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="9b657-915">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="9b657-916">Korrektur, dass DrvFs readdir nicht alle Einträge zurückgibt [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="9b657-916">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="9b657-917">Korrektur von LxFs readdir, wenn Dateien nicht verknüpft sind [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="9b657-917">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="9b657-918">Ermöglichen des erneuten Öffnens von nicht verknüpfter drvfs-Dateien über procfs</span><span class="sxs-lookup"><span data-stu-id="9b657-918">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="9b657-919">Hinzufügen einer Außerkraftsetzung des globalen Registrierungsschlüssels zum Deaktivieren von WSL-Features (Interop/Laufwerkeinbindung)</span><span class="sxs-lookup"><span data-stu-id="9b657-919">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="9b657-920">Korrektur falscher Blockanzahl in „stat“ für DrvFs (und LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="9b657-920">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="9b657-921">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-921">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="9b657-922">Build 16232</span><span class="sxs-lookup"><span data-stu-id="9b657-922">Build 16232</span></span>

<span data-ttu-id="9b657-923">Allgemeine Windows-Informationen zu Build 16232 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-923">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-924">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-924">Fixed</span></span>
- <span data-ttu-id="9b657-925">In diesem Release gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-925">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="9b657-926">Build 16226</span><span class="sxs-lookup"><span data-stu-id="9b657-926">Build 16226</span></span>

<span data-ttu-id="9b657-927">Allgemeine Windows-Informationen zu Build 16226 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-927">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-928">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-928">Fixed</span></span>
- <span data-ttu-id="9b657-929">Unterstützung von auf xattr bezogenen Systemaufrufen (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="9b657-929">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="9b657-930">xattr-Unterstützung für security.capablity.</span><span class="sxs-lookup"><span data-stu-id="9b657-930">security.capablity xattr support.</span></span>
- <span data-ttu-id="9b657-931">Verbesserte Kompatibilität mit bestimmten Dateisystemen und Filtern, einschließlich Nicht-MS-SMB-Servern.</span><span class="sxs-lookup"><span data-stu-id="9b657-931">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="9b657-932">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="9b657-932">[GH #1952]</span></span>
- <span data-ttu-id="9b657-933">Verbesserte Unterstützung für OneDrive-Platzhalter, GVFS-Platzhalter und komprimierte Compact OS-Dateien.</span><span class="sxs-lookup"><span data-stu-id="9b657-933">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="9b657-934">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-934">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="9b657-935">Build 16215</span><span class="sxs-lookup"><span data-stu-id="9b657-935">Build 16215</span></span>

<span data-ttu-id="9b657-936">Allgemeine Windows-Informationen zu Build 16215 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-936">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-937">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-937">Fixed</span></span>
- <span data-ttu-id="9b657-938">Für WSL ist der Entwicklermodus nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9b657-938">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="9b657-939">Unterstützung von Verzeichnisverbindungen in drvfs.</span><span class="sxs-lookup"><span data-stu-id="9b657-939">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="9b657-940">Verarbeiten der Deinstallation von appx-Paketen der WSL-Distribution.</span><span class="sxs-lookup"><span data-stu-id="9b657-940">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="9b657-941">Aktualisieren von procfs, um private und freigegebene Zuordnungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9b657-941">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="9b657-942">Hinzufügen einer Möglichkeit für „wslconfig.exe“ zum Bereinigen von Distributionen, die teilweise installiert oder deinstalliert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b657-942">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="9b657-943">Hinzufügen von Unterstützung für IP_MTU_DISCOVER für TCP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="9b657-943">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="9b657-944">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="9b657-944">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="9b657-945">Ableiten der Protokollfamilie für Routen zu AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="9b657-945">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="9b657-946">Verbesserungen an seriellen Geräten [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="9b657-946">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="9b657-947">Build 16199</span><span class="sxs-lookup"><span data-stu-id="9b657-947">Build 16199</span></span>

<span data-ttu-id="9b657-948">Allgemeine Windows-Informationen zu Build 16199 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-948">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-949">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-949">Fixed</span></span>
- <span data-ttu-id="9b657-950">In diesen Releases gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-950">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="9b657-951">Build 16193</span><span class="sxs-lookup"><span data-stu-id="9b657-951">Build 16193</span></span>

<span data-ttu-id="9b657-952">Allgemeine Windows-Informationen zu Build 16193 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-952">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-953">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-953">Fixed</span></span>
- <span data-ttu-id="9b657-954">Racebedingung zwischen dem Senden von SIGCONT und einer Threadgruppe, die beendet wird [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="9b657-954">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="9b657-955">Ändern von TTY-und PTY-Geräten zum Melden von FILE_DEVICE_NAMED_PIPE anstelle von FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="9b657-955">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="9b657-956">SSH-Korrektur für IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="9b657-956">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="9b657-957">Verschieben der DrvFs-Einbindung in den init-Daemon [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="9b657-957">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="9b657-958">Hinzufügen von Unterstützung in DrvFs für die folgenden symbolischen NT-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-958">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="9b657-959">Build 16184</span><span class="sxs-lookup"><span data-stu-id="9b657-959">Build 16184</span></span>

<span data-ttu-id="9b657-960">Allgemeine Windows-Informationen zu Build 16184 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-960">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-961">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-961">Fixed</span></span>
- <span data-ttu-id="9b657-962">Entfernen des apt-Paketverwaltungstasks (lxrun.exe /update) wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="9b657-962">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="9b657-963">Korrektur der Nichtanzeige der Ausgabe aus Windows-Prozessen in node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="9b657-963">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="9b657-964">Lockern der Ausrichtungsanforderungen in lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="9b657-964">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="9b657-965">Korrektur der Verarbeitung des AT_EMPTY_PATH-Flags in mehreren Systemaufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b657-965">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="9b657-966">Korrektur eines Problems, bei dem das Löschen von DrvFs-Dateien mit geöffneten Handles bewirkt, dass die Datei nicht definiertes Verhalten aufweist [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="9b657-966">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="9b657-967">„/etc/hosts“ erbt nun Einträge von der Windows-Hostdatei (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="9b657-967">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="9b657-968">Build 16179</span><span class="sxs-lookup"><span data-stu-id="9b657-968">Build 16179</span></span>

<span data-ttu-id="9b657-969">Allgemeine Windows-Informationen zu Build 16179 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-969">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-970">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-970">Fixed</span></span>
- <span data-ttu-id="9b657-971">Keine WSL-Änderungen in dieser Woche.</span><span class="sxs-lookup"><span data-stu-id="9b657-971">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="9b657-972">Build 16176</span><span class="sxs-lookup"><span data-stu-id="9b657-972">Build 16176</span></span>

<span data-ttu-id="9b657-973">Allgemeine Windows-Informationen zu Build 16176 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-973">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-974">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-974">Fixed</span></span>

- [<span data-ttu-id="9b657-975">Aktivierte serielle Unterstützung</span><span class="sxs-lookup"><span data-stu-id="9b657-975">Enabled serial support</span></span>](/archive/blogs/wsl/serial-support-on-the-windows-subsystem-for-linux)
- <span data-ttu-id="9b657-976">Hinzufügen der IP-Socketoption IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="9b657-976">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="9b657-977">Implementierung der pwritev-Funktion (beim Hochladen der Datei nach nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="9b657-977">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="9b657-978">Hinzufügen der IP-Socket-Optionen IP_MULTICAST_IF und IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="9b657-978">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="9b657-979">Unterstützung für Socketoption IP_MULTICAST_LOOP und IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="9b657-979">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="9b657-980">Hinzufügen von IP(V6)_MTU-Socketoption für den Knoten apps, traceroute, dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="9b657-980">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="9b657-981">Hinzufügen der IP-Socketoption IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="9b657-981">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="9b657-982">Verbesserungen des Dateisystems</span><span class="sxs-lookup"><span data-stu-id="9b657-982">Filesystem Improvements</span></span>](/archive/blogs/wsl/file-system-improvements-to-the-windows-subsystem-for-linux)
    * <span data-ttu-id="9b657-983">Ermöglichen der Einbindung von UNC-Pfaden</span><span class="sxs-lookup"><span data-stu-id="9b657-983">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="9b657-984">Ermöglichen von CDFS-Unterstützung in drvfs</span><span class="sxs-lookup"><span data-stu-id="9b657-984">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="9b657-985">Ordnungsgemäße Verarbeitung von Berechtigungen für Netzwerkdateisysteme in drvfs</span><span class="sxs-lookup"><span data-stu-id="9b657-985">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="9b657-986">Hinzufügen von Unterstützung für Remotelaufwerke zu drvfs</span><span class="sxs-lookup"><span data-stu-id="9b657-986">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="9b657-987">Ermöglichen von FAT-Unterstützung in drvfs</span><span class="sxs-lookup"><span data-stu-id="9b657-987">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="9b657-988">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-988">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-989">LTP-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="9b657-989">LTP Results</span></span>
<span data-ttu-id="9b657-990">Keine Änderungen seit 15042</span><span class="sxs-lookup"><span data-stu-id="9b657-990">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="9b657-991">Build 16170</span><span class="sxs-lookup"><span data-stu-id="9b657-991">Build 16170</span></span>

<span data-ttu-id="9b657-992">Allgemeine Windows-Informationen zu Build 16170 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-992">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="9b657-993">Wir haben einen neuen [Blogbeitrag](/archive/blogs/wsl/testing-the-windows-subsystem-for-linux) veröffentlicht, in dem unsere Anstrengungen beim Testen von WSL erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-993">We released a new [blog post](/archive/blogs/wsl/testing-the-windows-subsystem-for-linux) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="9b657-994">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-994">Fixed</span></span>

- <span data-ttu-id="9b657-995">Unterstützung für Socketoption IP_ADD_MEMBERSHIP und IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="9b657-995">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="9b657-996">Hinzufügen von Unterstützung für PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="9b657-996">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="9b657-997">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="9b657-997">[GH 1692]</span></span>
- <span data-ttu-id="9b657-998">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-998">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-999">LTP-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="9b657-999">LTP Results</span></span>
<span data-ttu-id="9b657-1000">Keine Änderungen seit 15042</span><span class="sxs-lookup"><span data-stu-id="9b657-1000">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="9b657-1001">Build 15046 für Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="9b657-1001">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="9b657-1002">Es gibt keine weiteren WSL-Korrekturen oder-Funktionen, die für die Einbindung in das Creators Update in Windows 10 geplant sind.</span><span class="sxs-lookup"><span data-stu-id="9b657-1002">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="9b657-1003">Die Anmerkungen zu dieser Version von WSL werden in den kommenden Wochen fortgesetzt, um Ergänzungen für das nächste Hauptupdate von Windows aufzuführen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1003">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="9b657-1004">Allgemeine Windows-Informationen zu Build 15046 und zukünftigen Insider Releases finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1004">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="9b657-1005">Build 15042</span><span class="sxs-lookup"><span data-stu-id="9b657-1005">Build 15042</span></span>

<span data-ttu-id="9b657-1006">Allgemeine Windows-Informationen zu Build 15042 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1006">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1007">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1007">Fixed</span></span>

- <span data-ttu-id="9b657-1008">Korrektur eines Deadlocks beim Entfernen eines Pfades, der auf „..“ endet</span><span class="sxs-lookup"><span data-stu-id="9b657-1008">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="9b657-1009">Korrektur eines Problems, bei dem FIONBIO bei Erfolg 0 zurückgibt [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="9b657-1009">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="9b657-1010">Korrektur eines Problems bei Lesevorgängen mit einer Länge von Null von Internetdatagrammsockets</span><span class="sxs-lookup"><span data-stu-id="9b657-1010">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="9b657-1011">Korrektur eines möglichen Deadlocks aufgrund einer Racebedingung bei der drvfs inode-Suche [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="9b657-1011">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="9b657-1012">Erweiterte Unterstützung für Hilfsdaten von Unix-Sockets, SCM_CREDENTIALS und SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="9b657-1012">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="9b657-1013">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1013">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1014">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1014">LTP Results:</span></span>
<span data-ttu-id="9b657-1015">Anzahl bestandener Tests: 737</span><span class="sxs-lookup"><span data-stu-id="9b657-1015">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="9b657-1016">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="9b657-1016">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="9b657-1017">Build 15031</span><span class="sxs-lookup"><span data-stu-id="9b657-1017">Build 15031</span></span>

<span data-ttu-id="9b657-1018">Allgemeine Windows-Informationen zu Build 15031 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1018">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1019">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1019">Fixed</span></span>

- <span data-ttu-id="9b657-1020">Korrektur eines Fehlers, bei dem sich time(2) sporadisch falsch verhielt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1020">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="9b657-1021">Korrektur eines Problems, bei dem \*SIGPROCMASK-Systemaufrufe die Signalmaske beschädigen konnten.</span><span class="sxs-lookup"><span data-stu-id="9b657-1021">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="9b657-1022">Jetzt Rückgabe der vollständigen Länge der Befehlszeile in WSL-Benachrichtigung zur Prozesserstellung.</span><span class="sxs-lookup"><span data-stu-id="9b657-1022">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="9b657-1023">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="9b657-1023">[GH 1632]</span></span>
- <span data-ttu-id="9b657-1024">WSL meldet jetzt die Threadbeendigung über ptrace für GDB-Hänger.</span><span class="sxs-lookup"><span data-stu-id="9b657-1024">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="9b657-1025">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="9b657-1025">[GH 1196]</span></span>
- <span data-ttu-id="9b657-1026">Korrektur eines Fehlers, bei dem ptys nach hoher tmux-E/A nicht mehr reagiert</span><span class="sxs-lookup"><span data-stu-id="9b657-1026">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="9b657-1027">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="9b657-1027">[GH 1358]</span></span>
- <span data-ttu-id="9b657-1028">Korrektur der Timeoutüberprüfung in zahlreichen Systemaufrufen (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="9b657-1028">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="9b657-1029">Hinzufügen von eventfd EFD_SEMAPHORE-Unterstützung [GH 452]</span><span class="sxs-lookup"><span data-stu-id="9b657-1029">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="9b657-1030">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1030">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1031">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1031">LTP Results:</span></span>
<span data-ttu-id="9b657-1032">Anzahl bestandener Tests: 737</span><span class="sxs-lookup"><span data-stu-id="9b657-1032">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="9b657-1033">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="9b657-1033">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9b657-1034">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1034">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="9b657-1035">Build 15025</span><span class="sxs-lookup"><span data-stu-id="9b657-1035">Build 15025</span></span>

<span data-ttu-id="9b657-1036">Allgemeine Windows-Informationen zu Build 15025 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1036">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1037">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1037">Fixed</span></span>

- <span data-ttu-id="9b657-1038">Korrektur eines Fehlers, bei dem grep 2.27 nicht mehr funktioniert [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="9b657-1038">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="9b657-1039">Implementierung des EFD_SEMAPHORE-Flags für den eventfd2-Systemaufruf [GH 452]</span><span class="sxs-lookup"><span data-stu-id="9b657-1039">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="9b657-1040">Implementierung von /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="9b657-1040">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="9b657-1041">Signalgestützte E/A-Unterstützung für Unix-Streamsockets [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="9b657-1041">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="9b657-1042">Unterstützung für F_GETPIPE_SZ und F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="9b657-1042">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="9b657-1043">Implementierung des recvmmsg()-Systemaufrufs [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="9b657-1043">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="9b657-1044">Korrektur eines Fehlers, bei dem epoll_wait() nicht gewartet hat [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="9b657-1044">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="9b657-1045">Implementierung von /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="9b657-1045">Implement /proc/version_signature</span></span>
- <span data-ttu-id="9b657-1046">Tee-Systemaufruf gibt jetzt einen Fehler zurück, wenn beide Dateideskriptoren auf dieselbe Pipe verweisen</span><span class="sxs-lookup"><span data-stu-id="9b657-1046">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="9b657-1047">Implementierung des richtigen Verhaltens für SO_PEERCRED für Unix-Sockets</span><span class="sxs-lookup"><span data-stu-id="9b657-1047">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="9b657-1048">Korrektur der Verarbeitung ungültiger Parameter des tkill-Systemaufrufs</span><span class="sxs-lookup"><span data-stu-id="9b657-1048">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="9b657-1049">Änderungen zum Verbessern der Leistung von drvfs</span><span class="sxs-lookup"><span data-stu-id="9b657-1049">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="9b657-1050">Kleinere Korrektur für Ruby-E/A-Blockierung</span><span class="sxs-lookup"><span data-stu-id="9b657-1050">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="9b657-1051">Korrektur von recvmsg() beim Zurückgeben von EINVAL für das MSG_DONTWAIT-Flag für Inet-Sockets [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="9b657-1051">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="9b657-1052">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1052">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1053">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1053">LTP Results:</span></span>
<span data-ttu-id="9b657-1054">Anzahl bestandener Tests: 732</span><span class="sxs-lookup"><span data-stu-id="9b657-1054">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="9b657-1055">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="9b657-1055">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9b657-1056">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1056">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="9b657-1057">Build 15019</span><span class="sxs-lookup"><span data-stu-id="9b657-1057">Build 15019</span></span>

<span data-ttu-id="9b657-1058">Allgemeine Windows-Informationen zu Build 15019 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1058">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1059">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1059">Fixed</span></span>

- <span data-ttu-id="9b657-1060">Korrektur eines Fehlers, der fälschlicherweise die CPU-Auslastung in procfs für Tools wie htop gemeldet hat [GH 823, 945, 971]</span><span class="sxs-lookup"><span data-stu-id="9b657-1060">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="9b657-1061">Beim Aufrufen von open() mit O_TRUNC für eine vorhandene Datei „inotify“ wird nun IN_MODIFY vor IN_OPEN generiert</span><span class="sxs-lookup"><span data-stu-id="9b657-1061">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="9b657-1062">Korrekturen für den Unix-Socket getsockopt SO_ERROR zum Aktivieren von Postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="9b657-1062">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="9b657-1063">Implementierung von /proc/sys/net/core/somaxconn für die Sprache GO</span><span class="sxs-lookup"><span data-stu-id="9b657-1063">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="9b657-1064">Der Apt-get-Packageupdate-Hintergrundtask wird jetzt aus der Ansicht ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="9b657-1064">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="9b657-1065">Löschen des Bereichs für ipv6 localhost (Fehler Spring-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="9b657-1065">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="9b657-1066">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1066">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1067">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1067">LTP Results:</span></span>
<span data-ttu-id="9b657-1068">Anzahl bestandener Tests: 714</span><span class="sxs-lookup"><span data-stu-id="9b657-1068">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="9b657-1069">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 249</span><span class="sxs-lookup"><span data-stu-id="9b657-1069">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="9b657-1070">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1070">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="9b657-1071">Build 15014</span><span class="sxs-lookup"><span data-stu-id="9b657-1071">Build 15014</span></span>

<span data-ttu-id="9b657-1072">Allgemeine Windows-Informationen zu Build 15014 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="9b657-1072">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1073">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1073">Fixed</span></span>

- <span data-ttu-id="9b657-1074">STRG+C funktioniert nun wie beabsichtigt</span><span class="sxs-lookup"><span data-stu-id="9b657-1074">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="9b657-1075">htop und ps auxw zeigen jetzt die richtige Ressourcenverwendung an (GH #516)</span><span class="sxs-lookup"><span data-stu-id="9b657-1075">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="9b657-1076">Grundlegende Übersetzung von NT-Ausnahmen in Signale.</span><span class="sxs-lookup"><span data-stu-id="9b657-1076">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="9b657-1077">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="9b657-1077">(GH #513)</span></span>
- <span data-ttu-id="9b657-1078">fallocate schlägt nun mit ENOSPC anstatt mit EINVAL fehl, wenn nicht genügend Speicherplatz verfügbar ist (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="9b657-1078">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="9b657-1079">Hinzufügen von /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="9b657-1079">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="9b657-1080">Implementierung der semop- und semtimedop-Systemaufrufe</span><span class="sxs-lookup"><span data-stu-id="9b657-1080">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="9b657-1081">Korrektur von nslookup-Fehlern mit der IP_RECVTOS- und IPV6_RECVTCLASS-Socketoption (GH 69)</span><span class="sxs-lookup"><span data-stu-id="9b657-1081">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="9b657-1082">Unterstützung für Socketoptionen IP_RECVTTL und IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="9b657-1082">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="9b657-1083">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1083">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1084">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1084">LTP Results:</span></span>
<span data-ttu-id="9b657-1085">Anzahl bestandener Tests: 709</span><span class="sxs-lookup"><span data-stu-id="9b657-1085">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="9b657-1086">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="9b657-1086">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9b657-1087">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1087">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="9b657-1088">Zusammenfassung der Systemaufrufe</span><span class="sxs-lookup"><span data-stu-id="9b657-1088">Syscall Summary</span></span>
<span data-ttu-id="9b657-1089">Systemaufrufe gesamt: 384</span><span class="sxs-lookup"><span data-stu-id="9b657-1089">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="9b657-1090">Implementiert gesamt: 235</span><span class="sxs-lookup"><span data-stu-id="9b657-1090">Total Implemented: 235</span></span> </br>
<span data-ttu-id="9b657-1091">Mit Stub versehen gesamt: 22</span><span class="sxs-lookup"><span data-stu-id="9b657-1091">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="9b657-1092">Nicht implementiert gesamt: 127</span><span class="sxs-lookup"><span data-stu-id="9b657-1092">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="9b657-1093">Ausführliche Aufschlüsselung</span><span class="sxs-lookup"><span data-stu-id="9b657-1093">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="9b657-1094">Build 15007</span><span class="sxs-lookup"><span data-stu-id="9b657-1094">Build 15007</span></span>

<span data-ttu-id="9b657-1095">Allgemeine Windows-Informationen zu Build 15007 finden Sie im [Windows-Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="9b657-1095">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="9b657-1096">Bekanntes Problem</span><span class="sxs-lookup"><span data-stu-id="9b657-1096">Known Issue</span></span>

- <span data-ttu-id="9b657-1097">Es gibt einen bekannten Fehler, bei dem die Konsole einige Eingaben über STRG+<key> nicht erkennt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1097">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="9b657-1098">Dies schließt den Befehl STRG+C ein, der als normaler C-Tastendruck fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b657-1098">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="9b657-1099">Problemumgehung: Ordnen Sie STRG+C eine alternative Taste zu.</span><span class="sxs-lookup"><span data-stu-id="9b657-1099">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="9b657-1100">Gehen Sie beispielsweise folgendermaßen vor, um STRG+K der Tastenkombination STRG+C zuzuordnen: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="9b657-1100">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="9b657-1101">Diese Zuordnung erfolgt pro Terminal und muss *jedes* Mal ausgeführt werden, wenn Bash gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-1101">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="9b657-1102">Benutzer können die Option zum Einbeziehen in ihre `.bashrc`-Datei untersuchen</span><span class="sxs-lookup"><span data-stu-id="9b657-1102">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="9b657-1103">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1103">Fixed</span></span>

- <span data-ttu-id="9b657-1104">Korrektur eines Problems, bei dem die Ausführung von WSL 100 % eines CPU-Kerns verbraucht</span><span class="sxs-lookup"><span data-stu-id="9b657-1104">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="9b657-1105">Socketoption IP_PKTINFO, IPV6_RECVPKTINFO wird jetzt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1105">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="9b657-1106">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="9b657-1106">(GH #851, 987)</span></span>
- <span data-ttu-id="9b657-1107">Abschneiden der physischen Adresse der Netzwerkschnittstelle auf 16 Bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="9b657-1107">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="9b657-1108">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1108">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1109">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1109">LTP Results:</span></span>
<span data-ttu-id="9b657-1110">Anzahl bestandener Tests: 709</span><span class="sxs-lookup"><span data-stu-id="9b657-1110">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="9b657-1111">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="9b657-1111">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="9b657-1112">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1112">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="9b657-1113">Build 15002</span><span class="sxs-lookup"><span data-stu-id="9b657-1113">Build 15002</span></span>

<span data-ttu-id="9b657-1114">Allgemeine Windows-Informationen zu Build 15002 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1114">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="9b657-1115">Bekanntes Problem</span><span class="sxs-lookup"><span data-stu-id="9b657-1115">Known Issue</span></span>

<span data-ttu-id="9b657-1116">Zwei bekannte Probleme:</span><span class="sxs-lookup"><span data-stu-id="9b657-1116">Two known issues:</span></span>
- <span data-ttu-id="9b657-1117">Es gibt einen bekannten Fehler, bei dem die Konsole einige Eingaben über STRG+<key> nicht erkennt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1117">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="9b657-1118">Dies schließt den Befehl STRG+C ein, der als normaler C-Tastendruck fungiert.</span><span class="sxs-lookup"><span data-stu-id="9b657-1118">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="9b657-1119">Problemumgehung: Ordnen Sie STRG+C eine alternative Taste zu.</span><span class="sxs-lookup"><span data-stu-id="9b657-1119">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="9b657-1120">Gehen Sie beispielsweise folgendermaßen vor, um STRG+K der Tastenkombination STRG+C zuzuordnen: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="9b657-1120">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="9b657-1121">Diese Zuordnung erfolgt pro Terminal und muss *jedes* Mal ausgeführt werden, wenn Bash gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-1121">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="9b657-1122">Benutzer können die Option zum Einbeziehen in ihre `.bashrc`-Datei untersuchen</span><span class="sxs-lookup"><span data-stu-id="9b657-1122">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="9b657-1123">Während der Ausführung von WSL werden von einem Systemthread 100 % eines CPU-Kerns beansprucht.</span><span class="sxs-lookup"><span data-stu-id="9b657-1123">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="9b657-1124">Die Ursache wurde untersucht und intern behoben.</span><span class="sxs-lookup"><span data-stu-id="9b657-1124">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="9b657-1125">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1125">Fixed</span></span>

- <span data-ttu-id="9b657-1126">Alle Bash-Sitzungen müssen jetzt auf derselben Berechtigungsebene erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1126">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="9b657-1127">Der Versuch, eine Sitzung auf einer anderen Ebene zu starten, wird blockiert.</span><span class="sxs-lookup"><span data-stu-id="9b657-1127">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="9b657-1128">Dies bedeutet, dass Administrator-und Nicht-Administratorkonsolen nicht gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9b657-1128">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="9b657-1129">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="9b657-1129">(GH #626)</span></span>
<br/>
- <span data-ttu-id="9b657-1130">Implementierung der folgenden NETLINK_ROUTE-Meldungen (erfordert Windows-Administrator)</span><span class="sxs-lookup"><span data-stu-id="9b657-1130">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="9b657-1131">RTM_NEWADDR (unterstützt `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="9b657-1131">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="9b657-1132">RTM_NEWROUTE (unterstützt `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="9b657-1132">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="9b657-1133">RTM_DELADDR (unterstützt `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="9b657-1133">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="9b657-1134">RTM_DELROUTE (unterstützt `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="9b657-1134">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="9b657-1135">Die geplante Tasküberprüfung für zu aktualisierende Pakete wird nicht mehr über eine getaktete Verbindung ausgeführt (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="9b657-1135">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="9b657-1136">Korrektur eines Fehlers, bei dem die Weiterleitung unterbrochen wird. Beispiel: bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="9b657-1136">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="9b657-1137">Implementierung der TCP_KEEPCNT-Socketoption (GH #843)</span><span class="sxs-lookup"><span data-stu-id="9b657-1137">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="9b657-1138">Implementierung der IP_MTU_DISCOVER INET-Socketoption (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="9b657-1138">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="9b657-1139">Entfernen der Legacyfnktionalität zum Ausführen von NT-Binärdateien aus init mit NT-Pfadsuche.</span><span class="sxs-lookup"><span data-stu-id="9b657-1139">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="9b657-1140">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="9b657-1140">(GH #1325)</span></span>
- <span data-ttu-id="9b657-1141">Korrektur des Modus von /dev/kmsg zum Zulassen von Gruppen-/sonstigem Lesezugriff (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="9b657-1141">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="9b657-1142">Implementierung von /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="9b657-1142">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="9b657-1143">Korrektur eines Fehlers, bei dem die Startzeit des Prozesses als Jahr 2432 angezeigt wurde (GH #974)</span><span class="sxs-lookup"><span data-stu-id="9b657-1143">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="9b657-1144">Wechseln der TERM-Standardumgebungsvariablen in xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="9b657-1144">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="9b657-1145">Änderung der Art und Weise, in der der Prozesscommit während des Prozessforks berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="9b657-1145">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="9b657-1146">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="9b657-1146">(GH #1286)</span></span>
- <span data-ttu-id="9b657-1147">Implementierung von /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="9b657-1147">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="9b657-1148">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="9b657-1148">(GH #1286)</span></span>
- <span data-ttu-id="9b657-1149">Implementierung der /proc/net/route-Datei (GH #69)</span><span class="sxs-lookup"><span data-stu-id="9b657-1149">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="9b657-1150">Korrektur eines Fehlers, bei dem der Verknüpfungsname falsch lokalisiert wurde (GH #696)</span><span class="sxs-lookup"><span data-stu-id="9b657-1150">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="9b657-1151">Korrektur der fehlerhaften ELF-Verarbeitungslogik, die die Programmheader nicht ordnungsgemäß so überprüft, dass sie kleiner als (oder gleich) PATH_MAX sein müssen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1151">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="9b657-1152">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="9b657-1152">(GH #1048)</span></span>
- <span data-ttu-id="9b657-1153">Implementierung des statfs-Rückrufs für procfs, sysfs, cgroupfs und binfmts (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="9b657-1153">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="9b657-1154">Korrektur der AptPackageIndexUpdate-Fenster, die nicht geschlossen werden (GH #1184, auch in GH #1193 beschrieben)</span><span class="sxs-lookup"><span data-stu-id="9b657-1154">Fixed AptPackageIndexUpdate windows that won't close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="9b657-1155">Hinzufügen von ASLR-Personality, ADDR_NO_RANDOMIZE-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="9b657-1155">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="9b657-1156">[GH #1148, 1128]</span><span class="sxs-lookup"><span data-stu-id="9b657-1156">(GH #1148, 1128)</span></span>
- <span data-ttu-id="9b657-1157">Verbesserung von PTRACE_GETSIGINFO, SIGSEGV für ordnungsgemäße gdb-Stapelüberwachungen während AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="9b657-1157">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="9b657-1158">Elf-Verarbeitung schlägt für patchelf-Binärdateien nicht mehr fehl.</span><span class="sxs-lookup"><span data-stu-id="9b657-1158">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="9b657-1159">[GH #471]</span><span class="sxs-lookup"><span data-stu-id="9b657-1159">(GH #471)</span></span>
- <span data-ttu-id="9b657-1160">VPN DNS-Weitergabe an /etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="9b657-1160">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="9b657-1161">Verbesserungen an TCP Close für eine zuverlässigere Datenübertragung.</span><span class="sxs-lookup"><span data-stu-id="9b657-1161">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="9b657-1162">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="9b657-1162">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="9b657-1163">Jetzt Rückgabe des richtigen Fehlercodes, wenn zu viele Dateien geöffnet werden (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="9b657-1163">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="9b657-1164">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="9b657-1164">(GH #1126, 2090)</span></span>
- <span data-ttu-id="9b657-1165">Windows-Überwachungsprotokoll erfasst jetzt den Imagenamen in Process Create Audit.</span><span class="sxs-lookup"><span data-stu-id="9b657-1165">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="9b657-1166">Jetzt normaler Fehler beim Starten von „bash.exe“ in einem Bash-Fenster.</span><span class="sxs-lookup"><span data-stu-id="9b657-1166">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="9b657-1167">Hinzufügen einer Fehlermeldung, wenn Interop nicht auf ein Arbeitsverzeichnis unter LxFs zugreifen kann (z.B. BASHRC-Datei von „notepad.exe“).</span><span class="sxs-lookup"><span data-stu-id="9b657-1167">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="9b657-1168">Korrektur eines Problems, bei dem der Windows-Pfad in WSL abgeschnitten wurde</span><span class="sxs-lookup"><span data-stu-id="9b657-1168">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="9b657-1169">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1169">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1170">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1170">LTP Results:</span></span>
<span data-ttu-id="9b657-1171">Anzahl bestandener Tests: 690</span><span class="sxs-lookup"><span data-stu-id="9b657-1171">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="9b657-1172">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 274</span><span class="sxs-lookup"><span data-stu-id="9b657-1172">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="9b657-1173">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1173">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1174">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1174">Syscall Support</span></span>
<span data-ttu-id="9b657-1175">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1175">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1176">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1176">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="9b657-1177">Build 14986</span><span class="sxs-lookup"><span data-stu-id="9b657-1177">Build 14986</span></span>

<span data-ttu-id="9b657-1178">Allgemeine Windows-Informationen zu Build 14986 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1178">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1179">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1179">Fixed</span></span>

- <span data-ttu-id="9b657-1180">Korrektur von Fehlerüberprüfungen mit Netlink und Pty IOCTLs</span><span class="sxs-lookup"><span data-stu-id="9b657-1180">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="9b657-1181">Kernel Version meldet nun 4.4.0-43 aus Gründen der Konsistenz mit Xenial</span><span class="sxs-lookup"><span data-stu-id="9b657-1181">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="9b657-1182">„Bash.exe“ wird jetzt gestartet, wenn die Eingabe an „nul:“ gerichtet ist (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="9b657-1182">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="9b657-1183">Thread-IDs werden nun ordnungsgemäß in procfs erfasst (GH #967)</span><span class="sxs-lookup"><span data-stu-id="9b657-1183">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="9b657-1184">Flags IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR werden jetzt in inotify_add_watch() unterstützt (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="9b657-1184">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="9b657-1185">Implementierung von timer_create und verwandten Systemaufrufen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1185">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="9b657-1186">Dies ermöglicht die GHC-Unterstützung (GH #307).</span><span class="sxs-lookup"><span data-stu-id="9b657-1186">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="9b657-1187">Korrektur eines Problems, bei dem Ping eine Zeitangabe von 0,000 ms zurückgab (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="9b657-1187">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="9b657-1188">Rückgabe des richtigen Fehlercodes, wenn zu viele Dateien geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1188">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="9b657-1189">Korrektur eines Problems in WSL, bei dem die Netlink-Anforderung für Netzwerkschnittstellendaten mit EINVAL fehlschlägt, wenn die Hardwareadresse der Schnittstelle 32 Bytes groß ist (z.B. die Teredo-Schnittstelle)</span><span class="sxs-lookup"><span data-stu-id="9b657-1189">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="9b657-1190">Beachten Sie, dass das Linux-Hilfsprogramm „ip“ einen Fehler enthält, bei dem ein Absturz erfolgt, wenn WSL eine 32-Byte-Hardwareadresse meldet.</span><span class="sxs-lookup"><span data-stu-id="9b657-1190">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="9b657-1191">Dies ist ein Fehler in „ip“, nicht in WSL.</span><span class="sxs-lookup"><span data-stu-id="9b657-1191">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="9b657-1192">Mit dem Hilfsprogramm „ip“ wird die Länge des Zeichenfolgenpuffers fest codiert, der zum Ausgeben der Hardwareadresse verwendet wird, und dieser Puffer ist zu klein, um eine 32-Byte-Hardwareadresse auszugeben.</span><span class="sxs-lookup"><span data-stu-id="9b657-1192">The "ip" utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="9b657-1193">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1193">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1194">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1194">LTP Results:</span></span>
<span data-ttu-id="9b657-1195">Anzahl bestandener Tests: 669</span><span class="sxs-lookup"><span data-stu-id="9b657-1195">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="9b657-1196">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 258</span><span class="sxs-lookup"><span data-stu-id="9b657-1196">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="9b657-1197">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1197">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1198">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1198">Syscall Support</span></span>
<span data-ttu-id="9b657-1199">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1199">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1200">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1200">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="9b657-1201">Build 14971</span><span class="sxs-lookup"><span data-stu-id="9b657-1201">Build 14971</span></span>

<span data-ttu-id="9b657-1202">Allgemeine Windows-Informationen zu Build 14971 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1202">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1203">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1203">Fixed</span></span>

 - <span data-ttu-id="9b657-1204">Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="9b657-1204">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="9b657-1205">Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1205">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1206">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1206">LTP Results:</span></span>
<span data-ttu-id="9b657-1207">Keine Änderungen seit 14965</span><span class="sxs-lookup"><span data-stu-id="9b657-1207">Unchanged from 14965</span></span> </br>
<span data-ttu-id="9b657-1208">Anzahl bestandener Tests: 664</span><span class="sxs-lookup"><span data-stu-id="9b657-1208">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="9b657-1209">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1209">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1210">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1210">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="9b657-1211">Build 14965</span><span class="sxs-lookup"><span data-stu-id="9b657-1211">Build 14965</span></span>

<span data-ttu-id="9b657-1212">Allgemeine Windows-Informationen zu Build 14965 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1212">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1213">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1213">Fixed</span></span>

- <span data-ttu-id="9b657-1214">Unterstützung für Netlink-Sockets RTM_GETLINK und RTM_GETADDR des NETLINK_ROUTE-Protokolls (GH #468)</span><span class="sxs-lookup"><span data-stu-id="9b657-1214">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="9b657-1215">Aktiviert ifconfig- und ip-Befehle für die Netzwerkenumeration.</span><span class="sxs-lookup"><span data-stu-id="9b657-1215">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="9b657-1216">Weitere Informationen finden Sie in unserem [Blogbeitrag zu WSL-Netzwerken](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1216">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="9b657-1217">„/sbin“ befindet sich jetzt standardmäßig im Pfad des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9b657-1217">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="9b657-1218">Der NT-Benutzerpfad wird jetzt standardmäßig an den WSL-Pfad angefügt (Sie können nun also „notepad.exe“ eingeben, ohne dem Linux-Pfad System32 hinzuzufügen).</span><span class="sxs-lookup"><span data-stu-id="9b657-1218">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="9b657-1219">Hinzufügen von Unterstützung für /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="9b657-1219">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="9b657-1220">NT-Binärdateien können nun aus WSL gestartet werden, wenn das aktuelle Arbeitsverzeichnis Nicht-ANSI-Zeichen enthält (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="9b657-1220">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="9b657-1221">Ermöglichen des Herunterfahrens für getrennten UNIX-Streamsocket</span><span class="sxs-lookup"><span data-stu-id="9b657-1221">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="9b657-1222">Hinzufügen von Unterstützung für PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="9b657-1222">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="9b657-1223">Hinzufügen von Unterstützung für CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="9b657-1223">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="9b657-1224">Korrektur eines Fehlers, bei dem die Weiterleitung unterbrochen wird. Beispiel: bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="9b657-1224">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="9b657-1225">Verarbeiten von Anforderungen zum Herstellen einer Verbindung mit dem aktuellen Terminal.</span><span class="sxs-lookup"><span data-stu-id="9b657-1225">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="9b657-1226">Markieren von /proc/<pid>/oom_score_adj als beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="9b657-1226">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="9b657-1227">Hinzufügen des Ordners „/sys/fs/cgroup“.</span><span class="sxs-lookup"><span data-stu-id="9b657-1227">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="9b657-1228">sched_setaffinity sollte den Wert der Affinitätsbitsmaske zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="9b657-1228">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="9b657-1229">Korrektur der ELF-Validierungslogik, die fälschlicherweise annimmt, dass Interpreterpfade weniger als 64 Zeichen lang sein müssen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1229">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="9b657-1230">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="9b657-1230">(GH #743)</span></span>
- <span data-ttu-id="9b657-1231">Geöffnete Dateideskriptoren können das Konsolenfenster geöffnet lassen (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="9b657-1231">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="9b657-1232">Korrektur eines Fehlers, bei dem rename() mit einem nachgestellten Schrägstrich für den Zielnamen fehlschlägt (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="9b657-1232">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="9b657-1233">Implementierung der/proc/net/dev-Datei</span><span class="sxs-lookup"><span data-stu-id="9b657-1233">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="9b657-1234">Korrektur von Pings mit 0,000 ms aufgrund der Timerauflösung.</span><span class="sxs-lookup"><span data-stu-id="9b657-1234">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="9b657-1235">Implementierung von /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="9b657-1235">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="9b657-1236">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1236">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1237">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1237">LTP Results:</span></span>
<span data-ttu-id="9b657-1238">Anzahl bestandener Tests: 664</span><span class="sxs-lookup"><span data-stu-id="9b657-1238">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="9b657-1239">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1239">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1240">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1240">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="9b657-1241">Build 14959</span><span class="sxs-lookup"><span data-stu-id="9b657-1241">Build 14959</span></span>

<span data-ttu-id="9b657-1242">Allgemeine Windows-Informationen zu Build 14959 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="9b657-1242">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1243">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1243">Fixed</span></span>

- <span data-ttu-id="9b657-1244">Verbesserte Pico-Prozessbenachrichtigung für Windows.</span><span class="sxs-lookup"><span data-stu-id="9b657-1244">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="9b657-1245">Weitere Informationen finden Sie im [WSL-Blog](/archive/blogs/wsl/wsl-antivirus-and-firewall-compatibility).</span><span class="sxs-lookup"><span data-stu-id="9b657-1245">Additional information found on the [WSL Blog](/archive/blogs/wsl/wsl-antivirus-and-firewall-compatibility).</span></span>
- <span data-ttu-id="9b657-1246">Verbesserte Stabilität mit Windows-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9b657-1246">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="9b657-1247">Korrektur von Fehler 0x80070057 beim Starten von „bash.exe“, wenn der Enterprise Data Protection (EDP) aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="9b657-1247">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="9b657-1248">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1248">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1249">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1249">LTP Results:</span></span>
<span data-ttu-id="9b657-1250">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="9b657-1250">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9b657-1251">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1251">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1252">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1252">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="9b657-1253">Build 14955</span><span class="sxs-lookup"><span data-stu-id="9b657-1253">Build 14955</span></span>

<span data-ttu-id="9b657-1254">Allgemeine Windows-Informationen zu Build 14955 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="9b657-1254">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1255">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1255">Fixed</span></span>

 - <span data-ttu-id="9b657-1256">Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="9b657-1256">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="9b657-1257">Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1257">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1258">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1258">LTP Results:</span></span>
<span data-ttu-id="9b657-1259">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="9b657-1259">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9b657-1260">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1260">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1261">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1261">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="9b657-1262">Build 14951</span><span class="sxs-lookup"><span data-stu-id="9b657-1262">Build 14951</span></span>

<span data-ttu-id="9b657-1263">Allgemeine Windows-Informationen zu Build 14951 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1263">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="9b657-1264">Neues Feature: Windows-/Ubuntu-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9b657-1264">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="9b657-1265">Windows-Binärdateien können jetzt direkt über die WSL-Befehlszeile aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1265">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="9b657-1266">Dadurch haben Benutzer die Möglichkeit, mit Ihrer Windows-Umgebung und dem -System auf eine Weise zu interagieren, die bisher nicht möglich war.</span><span class="sxs-lookup"><span data-stu-id="9b657-1266">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="9b657-1267">Als kurzes Beispiel können Benutzer nun die folgenden Befehle ausführen:</span><span class="sxs-lookup"><span data-stu-id="9b657-1267">As a quick example, it is now possible for users to run the following commands:</span></span>

```bash
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="9b657-1268">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="9b657-1268">More information can be found at:</span></span>

- [<span data-ttu-id="9b657-1269">WSL-Teamblog für Interop</span><span class="sxs-lookup"><span data-stu-id="9b657-1269">WSL Team Blog for Interop</span></span>](/archive/blogs/wsl/windows-and-ubuntu-interoperability)<br/>
- [<span data-ttu-id="9b657-1270">MSDN-Interop-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9b657-1270">MSDN Interop Documentation</span></span>](./interop.md)<br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1271">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1271">Fixed</span></span>

- <span data-ttu-id="9b657-1272">Ubuntu 16.04 (Xenial) wird jetzt für alle neuen WSL-Instanzen installiert.</span><span class="sxs-lookup"><span data-stu-id="9b657-1272">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="9b657-1273">Benutzer mit vorhandenen 14.04-Instanzen (Trusty) erhalten kein automatisches Upgrade.</span><span class="sxs-lookup"><span data-stu-id="9b657-1273">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="9b657-1274">Das während der Installation festgelegte Gebietsschema wird jetzt angezeigt</span><span class="sxs-lookup"><span data-stu-id="9b657-1274">Locale set during install is now displayed</span></span>
- <span data-ttu-id="9b657-1275">Terminalverbesserungen, einschließlich des Fehlers bei der Umleitung eines WSL-Prozesses an eine Datei, funktionieren nicht immer</span><span class="sxs-lookup"><span data-stu-id="9b657-1275">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="9b657-1276">Die Konsolenlebensdauer muss an die Lebensdauer von „bash.exe“ gebunden sein</span><span class="sxs-lookup"><span data-stu-id="9b657-1276">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="9b657-1277">Die Größe des Konsolenfensters sollte die sichtbare Größe und nicht die Puffergröße verwenden</span><span class="sxs-lookup"><span data-stu-id="9b657-1277">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="9b657-1278">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1278">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1279">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1279">LTP Results:</span></span>
<span data-ttu-id="9b657-1280">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="9b657-1280">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9b657-1281">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1281">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1282">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1282">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="9b657-1283">Build 14946</span><span class="sxs-lookup"><span data-stu-id="9b657-1283">Build 14946</span></span>

<span data-ttu-id="9b657-1284">Allgemeine Windows-Informationen zu Build 14946 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="9b657-1284">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1285">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1285">Fixed</span></span>

- <span data-ttu-id="9b657-1286">Korrektur eines Problems, das das Erstellen von WSL-Benutzerkonten für Benutzer mit NT-Benutzernamen verhindert hat, die Leerzeichen oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b657-1286">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="9b657-1287">Änderung von VolFs und DrvFs, damit 0 für die Verknüpfungsanzahl des Verzeichnisses im Status zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="9b657-1287">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="9b657-1288">Unterstützung der IPV6_MULTICAST_HOPS-Socketoption.</span><span class="sxs-lookup"><span data-stu-id="9b657-1288">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="9b657-1289">Einschränkung auf eine einzige Konsolen-E/A-Schleife pro TTY.</span><span class="sxs-lookup"><span data-stu-id="9b657-1289">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="9b657-1290">Der folgende Befehl ist beispielsweise möglich:</span><span class="sxs-lookup"><span data-stu-id="9b657-1290">Example: the following command is possible:</span></span>
  - <span data-ttu-id="9b657-1291">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="9b657-1291">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="9b657-1292">Ersetzen von Leerzeichen durch Tabstoppzeichen in /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="9b657-1292">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="9b657-1293">DrvFs wird jetzt in den Einbindungsinformationen mit einem Namen angezeigt, der dem eingebundenen Windows-Volume entspricht</span><span class="sxs-lookup"><span data-stu-id="9b657-1293">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="9b657-1294">/home und/root werden nun in den Einbindungsinformationen mit den richtigen Namen angezeigt</span><span class="sxs-lookup"><span data-stu-id="9b657-1294">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="9b657-1295">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1295">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1296">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1296">LTP Results:</span></span>
<span data-ttu-id="9b657-1297">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="9b657-1297">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9b657-1298">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1298">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1299">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1299">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="9b657-1300">Build 14942</span><span class="sxs-lookup"><span data-stu-id="9b657-1300">Build 14942</span></span>

<span data-ttu-id="9b657-1301">Allgemeine Windows-Informationen zu Build 14942 finden Sie im [Windows-Blog](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="9b657-1301">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1302">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1302">Fixed</span></span>

- <span data-ttu-id="9b657-1303">Eine Reihe von Fehlerüberprüfungen, einschließlich des Netzwerkabsturzes durch „ATTEMPTED EXECUTE OF NOEXECUTE MEMORY“, der SSH blockiert hat</span><span class="sxs-lookup"><span data-stu-id="9b657-1303">A number of bugchecks addressed, including the "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" networking crash which was blocking SSH</span></span>
- <span data-ttu-id="9b657-1304">inotify-Unterstützung für Benachrichtigungen, die von Windows-Anwendungen auf DrvFs generiert werden</span><span class="sxs-lookup"><span data-stu-id="9b657-1304">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="9b657-1305">Implementierung von TCP_KEEPIDLE und TCP_KEEPINTVL für mongod.</span><span class="sxs-lookup"><span data-stu-id="9b657-1305">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="9b657-1306">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="9b657-1306">(GH #695)</span></span>
- <span data-ttu-id="9b657-1307">Implementierung des pivot_root-Systemaufrufs</span><span class="sxs-lookup"><span data-stu-id="9b657-1307">Implement the pivot_root system call</span></span>
- <span data-ttu-id="9b657-1308">Implementierung der Socketoption für SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="9b657-1308">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="9b657-1309">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1309">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="9b657-1310">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1310">LTP Results:</span></span>
<span data-ttu-id="9b657-1311">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="9b657-1311">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="9b657-1312">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="9b657-1312">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="9b657-1313">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1313">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1314">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1314">Syscall Support</span></span>
<span data-ttu-id="9b657-1315">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1315">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1316">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1316">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="9b657-1317">Build 14936</span><span class="sxs-lookup"><span data-stu-id="9b657-1317">Build 14936</span></span>

<span data-ttu-id="9b657-1318">Allgemeine Windows-Informationen zu Build 14936 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1318">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="9b657-1319">Hinweis: WSL wird in einem zukünftigen Release Ubuntu Version 16.04 (Xenial) anstelle von Ubuntu 14.04 (Trusty) installieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-1319">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="9b657-1320">Diese Änderung gilt für Insider, die neue Instanzen installieren (lxrun.exe /install oder erste Ausführung von „bash.exe“).</span><span class="sxs-lookup"><span data-stu-id="9b657-1320">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="9b657-1321">Vorhandene Instanzen mit Trusty werden nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9b657-1321">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="9b657-1322">Benutzer können mit dem Befehl „do-release-upgrade“ Ihr Trusty-Image auf Xenial aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9b657-1322">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="9b657-1323">Bekanntes Problem</span><span class="sxs-lookup"><span data-stu-id="9b657-1323">Known Issue</span></span>
<span data-ttu-id="9b657-1324">Bei WSL treten Probleme mit einigen Socketimplementierungen auf.</span><span class="sxs-lookup"><span data-stu-id="9b657-1324">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="9b657-1325">Die Fehlerüberprüfung manifestiert sich als Absturz mit dem Fehler „ATTEMPTED EXECUTE OF NOEXECUTE MEMORY“.</span><span class="sxs-lookup"><span data-stu-id="9b657-1325">The bugcheck manifests itself as a crash with the error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span></span>  <span data-ttu-id="9b657-1326">Die häufigste Variante dieses Problems ist ein Absturz bei der Verwendung von SSH.</span><span class="sxs-lookup"><span data-stu-id="9b657-1326">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="9b657-1327">Die Ursache ist bei internen Builds korrigiert und wird so bald wie möglich in Insider gepusht.</span><span class="sxs-lookup"><span data-stu-id="9b657-1327">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="9b657-1328">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1328">Fixed</span></span>

- <span data-ttu-id="9b657-1329">Der chroot-Systemaufruf wurde implementiert.</span><span class="sxs-lookup"><span data-stu-id="9b657-1329">Implemented the chroot system call</span></span>
- <span data-ttu-id="9b657-1330">Verbesserungen in inotify ~~einschließlich Unterstützung für Benachrichtigungen, die von Windows-Anwendungen auf DrvFs generiert werden~~</span><span class="sxs-lookup"><span data-stu-id="9b657-1330">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="9b657-1331">Korrektur: Inotify-Unterstützung von Änderungen, die von Windows-Anwendungen stammen, ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9b657-1331">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="9b657-1332">Die Socketbindung an IPv6::<port n> unterstützt jetzt IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="9b657-1332">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="9b657-1333">Implementierung des WNOWAIT-Verhaltens für den waitid-Systemaufruf (GH #638)</span><span class="sxs-lookup"><span data-stu-id="9b657-1333">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="9b657-1334">Unterstützung für IP-Socketoptionen IP_HDRINCL und IP_TTL</span><span class="sxs-lookup"><span data-stu-id="9b657-1334">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="9b657-1335">read() der Länge Null sollte sofort zurückgegeben werden (GH #975)</span><span class="sxs-lookup"><span data-stu-id="9b657-1335">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="9b657-1336">Ordnungsgemäße Verarbeitung von Dateinamen und Dateinamenpräfixen, die keinen NULL-Terminator in einer TAR-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="9b657-1336">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="9b657-1337">epoll-Unterstützung für/dev/null</span><span class="sxs-lookup"><span data-stu-id="9b657-1337">epoll support for /dev/null</span></span>
- <span data-ttu-id="9b657-1338">Korrektur der /dev/alarm-Zeitquelle</span><span class="sxs-lookup"><span data-stu-id="9b657-1338">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="9b657-1339">Bash -c kann nun in eine Datei umgeleitet werden</span><span class="sxs-lookup"><span data-stu-id="9b657-1339">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="9b657-1340">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1340">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1341">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1341">LTP Results:</span></span>
<span data-ttu-id="9b657-1342">Anzahl bestandener Tests: 664</span><span class="sxs-lookup"><span data-stu-id="9b657-1342">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="9b657-1343">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 264</span><span class="sxs-lookup"><span data-stu-id="9b657-1343">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="9b657-1344">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1344">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1345">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1345">Syscall Support</span></span>
<span data-ttu-id="9b657-1346">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1346">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1347">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1347">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="9b657-1348">Build 14931</span><span class="sxs-lookup"><span data-stu-id="9b657-1348">Build 14931</span></span>

<span data-ttu-id="9b657-1349">Allgemeine Windows-Informationen zu Build 14931 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1349">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1350">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1350">Fixed</span></span>

 - <span data-ttu-id="9b657-1351">Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="9b657-1351">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="9b657-1352">Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1352">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="9b657-1353">Build 14926</span><span class="sxs-lookup"><span data-stu-id="9b657-1353">Build 14926</span></span>

<span data-ttu-id="9b657-1354">Allgemeine Windows-Informationen zu Build 14926 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1354">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1355">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1355">Fixed</span></span>

- <span data-ttu-id="9b657-1356">Ping funktioniert nun in Konsolen, die nicht über Administratorberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1356">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="9b657-1357">Ping6 wird jetzt auch ohne Administratorberechtigungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1357">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="9b657-1358">Inotify-Unterstützung für Dateien, die über WSL geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1358">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="9b657-1359">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="9b657-1359">(GH #216)</span></span>
  - <span data-ttu-id="9b657-1360">Unterstützte Flags:</span><span class="sxs-lookup"><span data-stu-id="9b657-1360">Flags supported:</span></span>
    - <span data-ttu-id="9b657-1361">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="9b657-1361">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="9b657-1362">inotify_add_watchEreignisse: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="9b657-1362">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="9b657-1363">inotify_add_watch-Attribute: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="9b657-1363">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="9b657-1364">Lesen der Ausgabe: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="9b657-1364">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="9b657-1365">Bekanntes Problem: Durch das Ändern von Dateien aus Windows-Anwendungen werden keine Ereignisse generiert</span><span class="sxs-lookup"><span data-stu-id="9b657-1365">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="9b657-1366">Unix-Socket unterstützt jetzt SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="9b657-1366">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="9b657-1367">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="9b657-1367">LTP Results:</span></span>
<span data-ttu-id="9b657-1368">Anzahl bestandener Tests: 651</span><span class="sxs-lookup"><span data-stu-id="9b657-1368">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="9b657-1369">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 258</span><span class="sxs-lookup"><span data-stu-id="9b657-1369">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="9b657-1370">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="9b657-1370">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="9b657-1371">Build 14915</span><span class="sxs-lookup"><span data-stu-id="9b657-1371">Build 14915</span></span>

<span data-ttu-id="9b657-1372">Allgemeine Windows-Informationen zu Build 14915 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="9b657-1372">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1373">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1373">Fixed</span></span>
-  <span data-ttu-id="9b657-1374">Socketpair für Unix-Datagrammsockets (GH #262)</span><span class="sxs-lookup"><span data-stu-id="9b657-1374">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="9b657-1375">Unix-Socketunterstützung für SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="9b657-1375">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="9b657-1376">Unix-Socketunterstützung für SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="9b657-1376">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="9b657-1377">Unix-Socketunterstützung für SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="9b657-1377">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="9b657-1378">Hinzufügen von Unterstützung für unix datagram socket send, recv und shutdown</span><span class="sxs-lookup"><span data-stu-id="9b657-1378">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="9b657-1379">Korrektur einer Fehlerüberprüfung aufgrund einer ungültigen Überprüfung des mmap-Parameters für nicht feste Adressen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1379">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="9b657-1380">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="9b657-1380">(GH #847)</span></span>
- <span data-ttu-id="9b657-1381">Unterstützung für das Anhalten/Fortsetzen von Terminalzuständen</span><span class="sxs-lookup"><span data-stu-id="9b657-1381">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="9b657-1382">Unterstützung für TIOCPKT ioctl zum Entsperren des Bildschirmhilfsprogramms (GH #774)</span><span class="sxs-lookup"><span data-stu-id="9b657-1382">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="9b657-1383">Bekanntes Problem: Funktionstasten sind nicht funktionsfähig</span><span class="sxs-lookup"><span data-stu-id="9b657-1383">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="9b657-1384">Korrektur einer Racebedingung in TimerFd, die dazu führen konnte, dass auf einen freigegebenen Member „ReaderReady“ durch LxpTimerFdWorkerRoutine zugegriffen wurde (GH #814)</span><span class="sxs-lookup"><span data-stu-id="9b657-1384">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="9b657-1385">Aktivieren der Unterstützung für erneut startbaren Systemaufruf für futex, poll und clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="9b657-1385">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="9b657-1386">Hinzufügen von Unterstützung für Bindungseinbindung</span><span class="sxs-lookup"><span data-stu-id="9b657-1386">Added bind mount support</span></span>
- <span data-ttu-id="9b657-1387">Unterstützung für Aufheben der Freigabe für Einbindungsnamespace</span><span class="sxs-lookup"><span data-stu-id="9b657-1387">unshare for mount namespace support</span></span>
    - <span data-ttu-id="9b657-1388">Bekanntes Problem: Beim Erstellen eines neuen Einbindngsnamespace mit `unshare(CLONE_NEWNS)` zeigt das aktuelle Arbeitsverzeichnis weiterhin auf den alten Namespace</span><span class="sxs-lookup"><span data-stu-id="9b657-1388">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="9b657-1389">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1389">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="9b657-1390">Build 14905</span><span class="sxs-lookup"><span data-stu-id="9b657-1390">Build 14905</span></span>

<span data-ttu-id="9b657-1391">Allgemeine Windows-Informationen zu Build 14905 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1391">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1392">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1392">Fixed</span></span>
- <span data-ttu-id="9b657-1393">Erneut startbare Systemaufrufe werden jetzt unterstützt (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="9b657-1393">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="9b657-1394">Symbolische Verknüpfungen mit Verzeichnissen, die auf / wenden, sind jetzt funktionstüchtig (GH #650)</span><span class="sxs-lookup"><span data-stu-id="9b657-1394">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="9b657-1395">Implementierung von RNDGETENTCNT ioctl für „/dev/random“</span><span class="sxs-lookup"><span data-stu-id="9b657-1395">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="9b657-1396">Implementierung der /proc/[pid]/mounts, /proc/[pid]/mountinfo- und /proc/[pid]/mountstats-Dateien</span><span class="sxs-lookup"><span data-stu-id="9b657-1396">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="9b657-1397">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1397">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="9b657-1398">Build 14901</span><span class="sxs-lookup"><span data-stu-id="9b657-1398">Build 14901</span></span>
<span data-ttu-id="9b657-1399">Der erste Insider-Build für das Windows 10 Anniversary Update-Release.</span><span class="sxs-lookup"><span data-stu-id="9b657-1399">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="9b657-1400">Allgemeine Windows-Informationen zu Build 14901 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1400">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1401">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1401">Fixed</span></span>
- <span data-ttu-id="9b657-1402">Korrektur eines Problems mit nachfolgenden Schrägstrichen</span><span class="sxs-lookup"><span data-stu-id="9b657-1402">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="9b657-1403">Befehle wie `$ mv a/c/ a/b/` funktionieren jetzt</span><span class="sxs-lookup"><span data-stu-id="9b657-1403">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="9b657-1404">Installation von Eingabeaufforderungen, wenn das Ubuntu-Gebietsschema auf das Windows-Gebietsschema festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="9b657-1404">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="9b657-1405">Procfs-Unterstützung für den Ordner „ns“</span><span class="sxs-lookup"><span data-stu-id="9b657-1405">Procfs support for ns folder</span></span>
- <span data-ttu-id="9b657-1406">Hinzufügen von „mount“ und „unmount“ für tmpfs-, procfs-und sysfs-Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="9b657-1406">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="9b657-1407">Korrektur der 32-Bit-ABI-Signatur von mklod [at]</span><span class="sxs-lookup"><span data-stu-id="9b657-1407">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="9b657-1408">Verschieben von Unix-Sockets in Dispatchmodell</span><span class="sxs-lookup"><span data-stu-id="9b657-1408">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="9b657-1409">Mit setsockopt festgelegte recv-Puffergröße von INET-Socket muss berücksichtigt werden</span><span class="sxs-lookup"><span data-stu-id="9b657-1409">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="9b657-1410">Implementierung des MSG_CMSG_CLOEXEC-Unis-Socket-Empfangsnachrichtenflags</span><span class="sxs-lookup"><span data-stu-id="9b657-1410">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="9b657-1411">stdin/stdout-Pipeumleitung des Linux-Prozesses (GH #2)</span><span class="sxs-lookup"><span data-stu-id="9b657-1411">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="9b657-1412">Ermöglicht das Weiterleiten von bash -c-Befehlen in CMD.</span><span class="sxs-lookup"><span data-stu-id="9b657-1412">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="9b657-1413">Beispiel: >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="9b657-1413">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="9b657-1414">Bash kann nun auf Systemen mit mehreren Auslagerungsdateien installiert werden (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="9b657-1414">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="9b657-1415">Standardpuffergröße des INET-Sockets sollte mit der Größe des Ubuntu- Standardsetups übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="9b657-1415">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="9b657-1416">Ausrichten von xattr-Systemaufrufen an listxattr</span><span class="sxs-lookup"><span data-stu-id="9b657-1416">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="9b657-1417">Nur Rückgabe von Schnittstellen mit einer gültigen IPv4-Adresse von SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="9b657-1417">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="9b657-1418">Korrektur der Signalatandardaktion, wenn von ptrace eingefügt</span><span class="sxs-lookup"><span data-stu-id="9b657-1418">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="9b657-1419">Implementierung von /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="9b657-1419">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="9b657-1420">Verwenden der Computerkontext-Registerwerte beim Wiederherstellen von Kontext in sigreturn</span><span class="sxs-lookup"><span data-stu-id="9b657-1420">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="9b657-1421">Dadurch wird das Problem behoben, dass Java und javac bei einigen Benutzern nicht mehr reagiert haben</span><span class="sxs-lookup"><span data-stu-id="9b657-1421">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="9b657-1422">Implementierung von /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="9b657-1422">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1423">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1423">Syscall Support</span></span>
<span data-ttu-id="9b657-1424">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1424">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1425">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1425">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="9b657-1426">Update von Build 14388 auf Windows 10 Anniversary Update</span><span class="sxs-lookup"><span data-stu-id="9b657-1426">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="9b657-1427">Allgemeine Windows-Informationen zu Build 14388 finden Sie im [Windows-Blog](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="9b657-1427">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1428">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1428">Fixed</span></span>
- <span data-ttu-id="9b657-1429">Korrekturen als Vorbereitung auf das Windows 10 Anniversary Update am 02.08.</span><span class="sxs-lookup"><span data-stu-id="9b657-1429">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="9b657-1430">Weitere Informationen zu WSL im Anniversary Update finden Sie in unserem [Blog](/archive/blogs/wsl/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1430">More information about WSL in the Anniversary Update can be found on our [blog](/archive/blogs/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="9b657-1431">Build 14376</span><span class="sxs-lookup"><span data-stu-id="9b657-1431">Build 14376</span></span>
<span data-ttu-id="9b657-1432">Allgemeine Windows-Informationen zu Build 14376 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1432">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1433">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1433">Fixed</span></span>
- <span data-ttu-id="9b657-1434">Entfernen einiger Instanzen, in denen apt-get nicht mehr reagiert (GH #493)</span><span class="sxs-lookup"><span data-stu-id="9b657-1434">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="9b657-1435">Korrektur eines Problems, bei dem leere Einbindungen nicht ordnungsgemäß verarbeitet wurden</span><span class="sxs-lookup"><span data-stu-id="9b657-1435">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="9b657-1436">Korrektur eines Problems, bei dem Ramdisks nicht ordnungsgemäß eingebunden wurden</span><span class="sxs-lookup"><span data-stu-id="9b657-1436">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="9b657-1437">Änderung von „unix socket accept“ für die Unterstützung von Flags (Teil von GH #451)</span><span class="sxs-lookup"><span data-stu-id="9b657-1437">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="9b657-1438">Korrektur eines allgemeinen netzwerkbezogenen Bluescreens</span><span class="sxs-lookup"><span data-stu-id="9b657-1438">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="9b657-1439">Korrektur des Bluescreens beim Zugriff auf /proc/[pid]/task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="9b657-1439">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="9b657-1440">Korrektur hoher CPU-Auslastung für einige Pty-Szenarien (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="9b657-1440">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="9b657-1441">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1441">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="9b657-1442">Build 14371</span><span class="sxs-lookup"><span data-stu-id="9b657-1442">Build 14371</span></span>
<span data-ttu-id="9b657-1443">Allgemeine Windows-Informationen zu Build 14371 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1443">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1444">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1444">Fixed</span></span>
- <span data-ttu-id="9b657-1445">Korrektur der Timingracebedingung mit SIGCHLD und wait() bei Verwendung von ptrace</span><span class="sxs-lookup"><span data-stu-id="9b657-1445">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="9b657-1446">Korrektur von Verhalten, wenn Pfade ein nachfolgendes Zeichen / aufweisen (GH #432)</span><span class="sxs-lookup"><span data-stu-id="9b657-1446">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="9b657-1447">Korrektur eines Problems, bei dem Umbenennen/Aufheben der Verknüpfung aufgrund von geöffneten Handles für untergeordnete Elemente fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="9b657-1447">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="9b657-1448">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1448">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="9b657-1449">Build 14366</span><span class="sxs-lookup"><span data-stu-id="9b657-1449">Build 14366</span></span>
<span data-ttu-id="9b657-1450">Allgemeine Windows-Informationen zu Build 14366 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1450">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1451">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1451">Fixed</span></span>
- <span data-ttu-id="9b657-1452">Korrektur der Dateierstellung durch symbolische Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1452">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="9b657-1453">Hinzugefügter von listxattr für Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="9b657-1453">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="9b657-1454">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1454">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1455">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1455">Syscall Support</span></span>
-   <span data-ttu-id="9b657-1456">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1456">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1457">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1457">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="9b657-1458">Build 14361</span><span class="sxs-lookup"><span data-stu-id="9b657-1458">Build 14361</span></span>
<span data-ttu-id="9b657-1459">Allgemeine Windows-Informationen zu Build 14361 finden Sie im [Windows-Blog](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="9b657-1459">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1460">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1460">Fixed</span></span>
- <span data-ttu-id="9b657-1461">Für DrvFs wird nun bei der Ausführung in Bash unter Ubuntu unter Windows die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-1461">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="9b657-1462">Benutzer können case.txt und CASE.TXT auf Ihren /mnt/c-Laufwerken verwenden</span><span class="sxs-lookup"><span data-stu-id="9b657-1462">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="9b657-1463">Die Beachtung von Groß-/Kleinschreibung wird nur in Bash unter Ubuntu unter Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1463">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="9b657-1464">Außerhalb von Bash zeigt NTFS die Dateien richtig an, aber es kann zu unerwartetem Verhalten bei der Interaktion mit den Dateien von Windows kommen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1464">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="9b657-1465">Für den Stamm der einzelnen Volumes (d.h. /mnt/c) wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="9b657-1465">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="9b657-1466">Weitere Informationen zum Verarbeiten dieser Dateien in Windows finden Sie [hier](https://support.microsoft.com/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="9b657-1466">More information on handling these files in Windows can be found [here](https://support.microsoft.com/kb/100625).</span></span>
- <span data-ttu-id="9b657-1467">Stark verbesserte PTY-/TTY-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="9b657-1467">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="9b657-1468">Anwendungen wie TMUX werden jetzt unterstützt (GH #40)</span><span class="sxs-lookup"><span data-stu-id="9b657-1468">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="9b657-1469">Korrektur eines Installationsproblems, bei dem Benutzerkonten nicht immer erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="9b657-1469">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="9b657-1470">Optimierte Befehlszeilen-Argumentstruktur, die eine extrem lange Argumentliste zulässt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1470">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="9b657-1471">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="9b657-1471">(GH #153)</span></span>
- <span data-ttu-id="9b657-1472">Jetzt können chmod read_only-Dateien aus DrvFs gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1472">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="9b657-1473">Korrektur einiger Instanzen, bei denen das Terminal beim Trennen nicht mehr reagiert (GH #43)</span><span class="sxs-lookup"><span data-stu-id="9b657-1473">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="9b657-1474">chmod und chown funktionieren jetzt auf TTY-Geräten</span><span class="sxs-lookup"><span data-stu-id="9b657-1474">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="9b657-1475">Verbindung mit 0.0.0.0 und :: as localhost zulassen (GH #388)</span><span class="sxs-lookup"><span data-stu-id="9b657-1475">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="9b657-1476">Sendmsg/recvmsg verarbeitet nun eine E/A-Vektorlänge > 1 (Teil von GH #376)</span><span class="sxs-lookup"><span data-stu-id="9b657-1476">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="9b657-1477">Benutzer können jetzt die automatisch generierte Hostdatei ablehnen (GH #398)</span><span class="sxs-lookup"><span data-stu-id="9b657-1477">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="9b657-1478">Automatisches Zuordnen des Linux-Gebietsschemas zum NT-Gebietsschema während der Installation (GH #11)</span><span class="sxs-lookup"><span data-stu-id="9b657-1478">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="9b657-1479">Hinzufügen der /proc/sys/vm/swappiness-Datei (GH #306)</span><span class="sxs-lookup"><span data-stu-id="9b657-1479">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="9b657-1480">strace wird jetzt ordnungsgemäß beendet</span><span class="sxs-lookup"><span data-stu-id="9b657-1480">strace now exits correctly</span></span>
- <span data-ttu-id="9b657-1481">Ermöglichen des erneuten Öffnens von Pipes über /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="9b657-1481">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="9b657-1482">Ausblenden von Verzeichnissen unter „%LOCALAPPDATA%\lxss“ aus DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="9b657-1482">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="9b657-1483">Bessere Verarbeitung von bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="9b657-1483">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="9b657-1484">Befehle wie „bash ~ -c ls“ werden jetzt unterstützt (GH #467)</span><span class="sxs-lookup"><span data-stu-id="9b657-1484">Commands like "bash ~ -c ls" now supported (GH #467)</span></span>
- <span data-ttu-id="9b657-1485">Sockets benachrichtigen nun darüber, dass epoll read beim Herunterfahren verfügbar ist (GH #271)</span><span class="sxs-lookup"><span data-stu-id="9b657-1485">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="9b657-1486">lxrun/uninstall arbeitet besser beim Löschen der Dateien und Ordner.</span><span class="sxs-lookup"><span data-stu-id="9b657-1486">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="9b657-1487">Korrektur für ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="9b657-1487">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="9b657-1488">Verbesserte Unterstützung für X11-Apps, z.B. xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="9b657-1488">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="9b657-1489">Aktualisierte anfängliche Threadstapelgröße, um der standardmäßigen Ubuntu-Einstellung zu entsprechen und die Größe ordnungsgemäß an den get_rlimit-Systemaufruf zu melden (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="9b657-1489">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="9b657-1490">Verbesserte Berichterstellung von Pico-Prozessimagenamen (z.B. für die Überwachung)</span><span class="sxs-lookup"><span data-stu-id="9b657-1490">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="9b657-1491">Implementierung von /proc/mountinfo für df-Befehl</span><span class="sxs-lookup"><span data-stu-id="9b657-1491">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="9b657-1492">Korrektur des Fehlercodes der symbolischen Verknüpfung für den untergeordneten Namen .</span><span class="sxs-lookup"><span data-stu-id="9b657-1492">Fixed symlink error code for child name .</span></span> <span data-ttu-id="9b657-1493">und .</span><span class="sxs-lookup"><span data-stu-id="9b657-1493">and ..</span></span>
- <span data-ttu-id="9b657-1494">Weitere optimierende Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1494">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1495">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1495">Syscall Support</span></span>
<span data-ttu-id="9b657-1496">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1496">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1497">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1497">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="9b657-1498">Build 14352</span><span class="sxs-lookup"><span data-stu-id="9b657-1498">Build 14352</span></span>
<span data-ttu-id="9b657-1499">Allgemeine Windows-Informationen zu Build 14352 finden Sie im [Windows-Blog](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="9b657-1499">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1500">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1500">Fixed</span></span>
- <span data-ttu-id="9b657-1501">Korrektur eines Problems, bei dem große Dateien nicht ordnungsgemäß heruntergeladen bzw. ordnungsgemäß erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1501">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="9b657-1502">Dadurch sollte die Blockierung von npm und anderen Szenarien aufgehoben werden (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="9b657-1502">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="9b657-1503">Entfernen einiger Instanzen, in denen Sockets nicht mehr reagieren</span><span class="sxs-lookup"><span data-stu-id="9b657-1503">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="9b657-1504">Korrektur einiger ptrace-Fehler</span><span class="sxs-lookup"><span data-stu-id="9b657-1504">Corrected some ptrace errors</span></span>
- <span data-ttu-id="9b657-1505">Korrektur eines Problems, bei dem WSL Dateinamen mit mehr als 255 Zeichen zuließ</span><span class="sxs-lookup"><span data-stu-id="9b657-1505">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="9b657-1506">Verbesserte Unterstützung nicht-englischer Zeichen</span><span class="sxs-lookup"><span data-stu-id="9b657-1506">Improved support for non-English characters</span></span>
- <span data-ttu-id="9b657-1507">Hinzufügen aktueller Windows-Zeitzonendaten und Festlegen als Standard</span><span class="sxs-lookup"><span data-stu-id="9b657-1507">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="9b657-1508">Eindeutige Geräte-IDs für jeden Einbindungspunkt (jre-Korrektur – GH #49)</span><span class="sxs-lookup"><span data-stu-id="9b657-1508">Unique device id's for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="9b657-1509">Korrektur eines Problems mit Pfaden, die „.“ und „..“ enthalten</span><span class="sxs-lookup"><span data-stu-id="9b657-1509">Correct issue with paths containing "." and ".."</span></span>
- <span data-ttu-id="9b657-1510">Hinzufügen von FIFO-Unterstützung (GH #71)</span><span class="sxs-lookup"><span data-stu-id="9b657-1510">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="9b657-1511">Aktualisiertes Format von „resolv.conf“ entsprechend dem nativen Ubuntu-Format</span><span class="sxs-lookup"><span data-stu-id="9b657-1511">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="9b657-1512">procfs-Bereinigung</span><span class="sxs-lookup"><span data-stu-id="9b657-1512">Some procfs cleanup</span></span>
- <span data-ttu-id="9b657-1513">Aktivierten von Ping für Administratorkonsolen (GH #18)</span><span class="sxs-lookup"><span data-stu-id="9b657-1513">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1514">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1514">Syscall Support</span></span>
<span data-ttu-id="9b657-1515">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1515">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1516">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1516">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="9b657-1517">Build 14342</span><span class="sxs-lookup"><span data-stu-id="9b657-1517">Build 14342</span></span>
<span data-ttu-id="9b657-1518">Allgemeine Windows-Informationen zu Build 14342 finden Sie im [Windows-Blog](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="9b657-1518">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="9b657-1519">Informationen zu VolFs und DriveFs finden Sie im [WSL-Blog](/archive/blogs/wsl/).</span><span class="sxs-lookup"><span data-stu-id="9b657-1519">Information on VolFs and DriveFs can be found on the [WSL Blog](/archive/blogs/wsl/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="9b657-1520">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1520">Fixed</span></span>
- <span data-ttu-id="9b657-1521">Korrektur eines Installationsproblems, wenn der Windows-Benutzer Unicode-Zeichen im Benutzernamen enthielt</span><span class="sxs-lookup"><span data-stu-id="9b657-1521">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="9b657-1522">Die Problemumgehung „apt-get update udev“ in den FAQ wird jetzt standardmäßig bei der ersten Ausführung bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="9b657-1522">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="9b657-1523">Aktivierte symbolische Verknüpfungen in DriveFs-Verzeichnissen (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="9b657-1523">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="9b657-1524">Symbolische Verknüpfungen funktionieren nun zwischen DriveFs und VolFs</span><span class="sxs-lookup"><span data-stu-id="9b657-1524">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="9b657-1525">Korrektur des Pfadanalyseproblems auf oberster Ebene: ls .// funktioniert jetzt wie erwartet</span><span class="sxs-lookup"><span data-stu-id="9b657-1525">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="9b657-1526">npm install auf DriveFs und die -g-Optionen funktionieren jetzt</span><span class="sxs-lookup"><span data-stu-id="9b657-1526">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="9b657-1527">Korrektur eines Problems, das den Start des PHP-Servers verhinderte</span><span class="sxs-lookup"><span data-stu-id="9b657-1527">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="9b657-1528">Aktualisierte Standardumgebungswerte, z.B. $PATH, um nativem Ubuntu besser zu entsprechen</span><span class="sxs-lookup"><span data-stu-id="9b657-1528">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="9b657-1529">Hinzufügen eines wöchentlichen Wartungstasks in Windows zum Aktualisieren des apt-Paketcaches</span><span class="sxs-lookup"><span data-stu-id="9b657-1529">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="9b657-1530">Korrektur eines Problems bei der Überprüfung von ELF-Headern, WSL unterstützt jetzt alle Melkor-Optionen</span><span class="sxs-lookup"><span data-stu-id="9b657-1530">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="9b657-1531">Zsh-Shell ist funktionsfähig</span><span class="sxs-lookup"><span data-stu-id="9b657-1531">Zsh shell is functional</span></span>
- <span data-ttu-id="9b657-1532">Vorkompilierte Go-Binärdateien werden jetzt unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b657-1532">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="9b657-1533">Eingabeaufforderung bei der ersten Ausführung von „bash.exe“ ist nun richtig lokalisiert</span><span class="sxs-lookup"><span data-stu-id="9b657-1533">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="9b657-1534">/proc/meminfo gibt jetzt richtige Informationen zurück</span><span class="sxs-lookup"><span data-stu-id="9b657-1534">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="9b657-1535">Sockets werden jetzt in VFS unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b657-1535">Sockets now supported in VFS</span></span>
- <span data-ttu-id="9b657-1536">/dev jetzt als tempfs eingebunden</span><span class="sxs-lookup"><span data-stu-id="9b657-1536">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="9b657-1537">Fifo wird jetzt unterstützt</span><span class="sxs-lookup"><span data-stu-id="9b657-1537">Fifo now supported</span></span>
- <span data-ttu-id="9b657-1538">Mehrkernsysteme werden nun ordnungsgemäß in /proc/cpuinfo angezeigt</span><span class="sxs-lookup"><span data-stu-id="9b657-1538">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="9b657-1539">Weitere Verbesserungen und Fehlermeldungen, die während der ersten Ausführung heruntergeladen werden</span><span class="sxs-lookup"><span data-stu-id="9b657-1539">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="9b657-1540">Systemaufrufverbesserungen und -fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1540">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="9b657-1541">Unterstützte Systemaufrufliste unten.</span><span class="sxs-lookup"><span data-stu-id="9b657-1541">Supported syscall list below.</span></span>
- <span data-ttu-id="9b657-1542">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1542">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="9b657-1543">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="9b657-1543">Known Issues</span></span>
- <span data-ttu-id="9b657-1544">„.“ wird in einigen Fällen nicht</span><span class="sxs-lookup"><span data-stu-id="9b657-1544">Not resolving '..'</span></span> <span data-ttu-id="9b657-1545">ordnungsgemäß auf DriveFs aufgelöst</span><span class="sxs-lookup"><span data-stu-id="9b657-1545">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1546">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1546">Syscall Support</span></span>
<span data-ttu-id="9b657-1547">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1547">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="9b657-1548">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1548">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="9b657-1549">Build 14332</span><span class="sxs-lookup"><span data-stu-id="9b657-1549">Build 14332</span></span>

<span data-ttu-id="9b657-1550">Allgemeine Windows-Informationen zu Build 14332 finden Sie im [Windows-Blog](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="9b657-1550">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="9b657-1551">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1551">Fixed</span></span>
- <span data-ttu-id="9b657-1552">Bessere resolv.conf-Generierung einschließlich Priorisieren von DNS-Einträgen</span><span class="sxs-lookup"><span data-stu-id="9b657-1552">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="9b657-1553">Problem beim Verschieben von Dateien und Verzeichnissen zwischen/mnt- und Nicht-/mnt-Laufwerken</span><span class="sxs-lookup"><span data-stu-id="9b657-1553">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="9b657-1554">TAR-Dateien können jetzt mit symbolischen Verknüpfungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1554">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="9b657-1555">Hinzufügen des /run/lock-Standardverzeichnisses bei der Instanzerstellung</span><span class="sxs-lookup"><span data-stu-id="9b657-1555">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="9b657-1556">Aktualisieren von /dev/null, um die richtigen Statusinformationen zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="9b657-1556">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="9b657-1557">Weitere Fehler beim Herunterladen während der ersten Ausführung</span><span class="sxs-lookup"><span data-stu-id="9b657-1557">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="9b657-1558">Systemaufrufverbesserungen und -fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1558">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="9b657-1559">Unterstützte Systemaufrufliste unten.</span><span class="sxs-lookup"><span data-stu-id="9b657-1559">Supported syscall list below.</span></span>
- <span data-ttu-id="9b657-1560">Weitere optimierende Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1560">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1561">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1561">Syscall Support</span></span>
<span data-ttu-id="9b657-1562">Im folgenden finden Sie den neuen Systemaufruf, der in WSL implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="9b657-1562">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="9b657-1563">Der Systemaufruf in dieser Liste wird in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1563">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="9b657-1564">Build 14328</span><span class="sxs-lookup"><span data-stu-id="9b657-1564">Build 14328</span></span>

<span data-ttu-id="9b657-1565">Allgemeine Windows-Informationen zu Build 14332 finden Sie im [Windows-Blog](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="9b657-1565">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="9b657-1566">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="9b657-1566">New Features</span></span>
* <span data-ttu-id="9b657-1567">Jetzt werden Linux-Benutzer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1567">Now support Linux users.</span></span>  <span data-ttu-id="9b657-1568">Bei der Installation von Bash unter Ubuntu unter Windows werden Sie aufgefordert, einen Linux-Benutzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1568">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="9b657-1569">Weitere Informationen finden Sie unter https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="9b657-1569">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="9b657-1570">Der Hostname ist jetzt auf den Windows-Computernamen festgelegt, nicht mehr auf @localhost</span><span class="sxs-lookup"><span data-stu-id="9b657-1570">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="9b657-1571">Weitere Informationen zu Build 14328 finden Sie unter: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="9b657-1571">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="9b657-1572">Fest</span><span class="sxs-lookup"><span data-stu-id="9b657-1572">Fixed</span></span>
* <span data-ttu-id="9b657-1573">Verbesserungen von symbolischen Verknüpfungen für Nicht-/mnt/<drive>-Dateien</span><span class="sxs-lookup"><span data-stu-id="9b657-1573">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="9b657-1574">Die npm-Installation funktioniert jetzt</span><span class="sxs-lookup"><span data-stu-id="9b657-1574">npm install now works</span></span>
    * <span data-ttu-id="9b657-1575">jdk/jre kann nun mithilfe der Anweisungen installiert werden, die Sie [hier](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html) finden.</span><span class="sxs-lookup"><span data-stu-id="9b657-1575">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="9b657-1576">Bekanntes Problem: Symbolische Verknüpfungen funktionieren für Windows-Einbindungen nicht.</span><span class="sxs-lookup"><span data-stu-id="9b657-1576">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="9b657-1577">Diese Funktionen werden in einem späteren Build verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="9b657-1577">Functionality will be available in a later build</span></span>
* <span data-ttu-id="9b657-1578">top und htop werden jetzt angezeigt</span><span class="sxs-lookup"><span data-stu-id="9b657-1578">top and htop now display</span></span>
* <span data-ttu-id="9b657-1579">Zusätzliche Fehlermeldungen bei einigen Installationsfehlern</span><span class="sxs-lookup"><span data-stu-id="9b657-1579">Additional error messages for some install failures</span></span>
* <span data-ttu-id="9b657-1580">Systemaufrufverbesserungen und -fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1580">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="9b657-1581">Unterstützte Systemaufrufliste unten.</span><span class="sxs-lookup"><span data-stu-id="9b657-1581">Supported syscall list below.</span></span>
* <span data-ttu-id="9b657-1582">Weitere optimierende Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="9b657-1582">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="9b657-1583">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="9b657-1583">Syscall Support</span></span>
<span data-ttu-id="9b657-1584">Im folgenden finden Sie eine Liste der Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="9b657-1584">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="9b657-1585">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9b657-1585">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>