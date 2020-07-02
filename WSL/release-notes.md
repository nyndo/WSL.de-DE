---
title: Anmerkungen zu dieser Version des Windows-Subsystems für Linux
description: Anmerkungen zu dieser Version des Windows-Subsystems für Linux  Wöchentlich aktualisiert.
keywords: Versionshinweise, WSL, Windows, Windows Subsystem für Linux, Windows-Subsystem, Ubuntu
author: benhillis
ms.date: 05/15/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 2fcf24719f037a29bab7652fc75ac82cc0b6176a
ms.sourcegitcommit: 031a74801e03a90aed4b34c4fd5bfe964fc30994
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "84942594"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="7a11e-105">Anmerkungen zu dieser Version des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="7a11e-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-20150"></a><span data-ttu-id="7a11e-106">Build 20150</span><span class="sxs-lookup"><span data-stu-id="7a11e-106">Build 20150</span></span>
<span data-ttu-id="7a11e-107">Allgemeine Windows-Informationen zu Build 20150 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-107">For general Windows information on build 20150 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span></span>

* <span data-ttu-id="7a11e-108">Informationen zu WSL2 GPU Compute finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-108">WSL2 GPU compute see [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/17/announcing-windows-10-insider-preview-build-20150/) for more information.</span></span>
* <span data-ttu-id="7a11e-109">Führen Sie die Befehlszeilenoption „wsl.exe --install“ zum einfachen Einrichten von WSL ein.</span><span class="sxs-lookup"><span data-stu-id="7a11e-109">Introduce wsl.exe --install command line option to easily set up WSL.</span></span>
* <span data-ttu-id="7a11e-110">Führen Sie die Befehlszeilenoption „wsl.exe --update“ zum Verwalten von Updates für den WSL2-Kernel ein.</span><span class="sxs-lookup"><span data-stu-id="7a11e-110">Introduce wsl.exe --update command line option to manage updates to the WSL2 kernel.</span></span> 
* <span data-ttu-id="7a11e-111">Legen Sie WSL2 als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="7a11e-111">Set WSL2 as the default.</span></span>
* <span data-ttu-id="7a11e-112">Erhöhen Sie das Timeout für das kontrollierte Beenden der WSL2-VM.</span><span class="sxs-lookup"><span data-stu-id="7a11e-112">Increase WSL2 vm graceful shutdown timeout.</span></span>
* <span data-ttu-id="7a11e-113">Korrigieren Sie die virtio-9p-Racebedingung beim Zuordnen des Gerätespeichers.</span><span class="sxs-lookup"><span data-stu-id="7a11e-113">Fix virtio-9p race condition when mapping device memory.</span></span>
* <span data-ttu-id="7a11e-114">Führen Sie keinen 9p-Server mit erhöhten Rechten aus, wenn UAC deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-114">Don't run an elevated 9p server if UAC is disabled.</span></span>

## <a name="build-19640"></a><span data-ttu-id="7a11e-115">Build 19640</span><span class="sxs-lookup"><span data-stu-id="7a11e-115">Build 19640</span></span>
<span data-ttu-id="7a11e-116">Allgemeine Windows-Informationen zu Build 19640 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-116">For general Windows information on build 19640 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/06/03/announcing-windows-10-insider-preview-build-19640/).</span></span>

* <span data-ttu-id="7a11e-117">[WSL2] Stabilitätsverbesserungen für virtio-9p (drvfs).</span><span class="sxs-lookup"><span data-stu-id="7a11e-117">[WSL2] Stability improvements for virtio-9p (drvfs).</span></span>

## <a name="build-19555"></a><span data-ttu-id="7a11e-118">Build 19555</span><span class="sxs-lookup"><span data-stu-id="7a11e-118">Build 19555</span></span>
<span data-ttu-id="7a11e-119">Allgemeine Windows-Informationen zu Build 19555 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-119">For general Windows information on build 19555 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2020/01/30/announcing-windows-10-insider-preview-build-19555/).</span></span>

* <span data-ttu-id="7a11e-120">[WSL2] Verwenden einer Arbeitsspeicher-cgroup, um den von Installations- und Konvertierungsvorgängen verwendeten Speicherplatz zu begrenzen [GH 4669]</span><span class="sxs-lookup"><span data-stu-id="7a11e-120">[WSL2] Use a memory cgroup to limit the amount of memory used by install and conversion operations [GH 4669]</span></span>
* <span data-ttu-id="7a11e-121">Verfügbarmachen von „wsl.exe“, wenn die optionale Komponente „Windows-Subsystem für Linux“ (WSL) nicht aktiviert ist, um die Auffindbarkeit von Features zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="7a11e-121">Make wsl.exe present when the Windows Subsystem for Linux optional component is not enabled to improve feature discoverability.</span></span>
* <span data-ttu-id="7a11e-122">Ändern von „wsl.exe“, um Hilfetext auszugeben, wenn die optionale Komponente WSL nicht installiert ist</span><span class="sxs-lookup"><span data-stu-id="7a11e-122">Change wsl.exe to print help text if the WSL optional component is not installed</span></span>
* <span data-ttu-id="7a11e-123">Fehlerbehebung für die Racebedingung beim Erstellen von Instanzen</span><span class="sxs-lookup"><span data-stu-id="7a11e-123">Fix race condition when creating instances</span></span>
* <span data-ttu-id="7a11e-124">Erstellen von „wslclient.dll“ mit allen Befehlszeilenfunktionen</span><span class="sxs-lookup"><span data-stu-id="7a11e-124">Create wslclient.dll that contains all command line functionality</span></span>
* <span data-ttu-id="7a11e-125">Verhindern eines Absturzes bei angehaltenem LxssManagerUser-Dienst</span><span class="sxs-lookup"><span data-stu-id="7a11e-125">Prevent crash during LxssManagerUser service stop</span></span>
* <span data-ttu-id="7a11e-126">Fehlerbehebung für ein wslapi.dll-Fast-Fail, wenn der distroName-Parameter NULL ist</span><span class="sxs-lookup"><span data-stu-id="7a11e-126">Fix wslapi.dll fast fail when distroName parameter is NULL</span></span>

## <a name="build-19041"></a><span data-ttu-id="7a11e-127">Build 19041</span><span class="sxs-lookup"><span data-stu-id="7a11e-127">Build 19041</span></span>
<span data-ttu-id="7a11e-128">Allgemeine Windows-Informationen zu Build 19041 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-128">For general Windows information on build 19041 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/12/10/announcing-windows-10-insider-preview-build-19041/).</span></span>

* <span data-ttu-id="7a11e-129">[WSL2] Löschen der Signalmaske vor dem Starten der Prozesse</span><span class="sxs-lookup"><span data-stu-id="7a11e-129">[WSL2] Clear the signal mask before launching the processes</span></span>
* <span data-ttu-id="7a11e-130">[WSL2] Aktualisieren des Linux-Kernels auf 4.19.84</span><span class="sxs-lookup"><span data-stu-id="7a11e-130">[WSL2] Update Linux kernel to 4.19.84</span></span>
* <span data-ttu-id="7a11e-131">Verarbeiten der Erstellung der symbolischen Verknüpfung „/etc/resolv.conf“, wenn die symbolische Verknüpfung nicht relativ ist</span><span class="sxs-lookup"><span data-stu-id="7a11e-131">Handle creation of /etc/resolv.conf symlink when the symlink is non-relative</span></span>

## <a name="build-19028"></a><span data-ttu-id="7a11e-132">Build 19028</span><span class="sxs-lookup"><span data-stu-id="7a11e-132">Build 19028</span></span>
<span data-ttu-id="7a11e-133">Allgemeine Windows-Informationen zu Build 19028 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-133">For general Windows information on build 19028 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/19/announcing-windows-10-insider-preview-build-19028/).</span></span>

* <span data-ttu-id="7a11e-134">[WSL2] Aktualisieren des Linux-Kernels auf 4.19.81</span><span class="sxs-lookup"><span data-stu-id="7a11e-134">[WSL2] Update Linux kernel to 4.19.81</span></span>
* <span data-ttu-id="7a11e-135">[WSL2] Ändern der Standardberechtigung von /dev/net/tun in 0666 [GH 4629]</span><span class="sxs-lookup"><span data-stu-id="7a11e-135">[WSL2] Change the default permission of /dev/net/tun to 0666 [GH 4629]</span></span>
* <span data-ttu-id="7a11e-136">[WSL2] Optimieren der Standard-Arbeitsspeichergröße, die dem virtuellen Linux-Computer zugewiesen ist, auf 80% des Hostarbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="7a11e-136">[WSL2] Tweak default amount of memory assigned to Linux VM to be 80% of host memory</span></span>
* <span data-ttu-id="7a11e-137">[WSL2] Fehlerbehebung für den Interop-Server, um Anforderungen mit einem Timeout zu verarbeiten, damit sich der Server bei ungültigen Aufrufern nicht aufhängt</span><span class="sxs-lookup"><span data-stu-id="7a11e-137">[WSL2] fix interop server to handle requests with a timeout so bad callers cannot hang the server</span></span>

## <a name="build-19018"></a><span data-ttu-id="7a11e-138">Build 19018</span><span class="sxs-lookup"><span data-stu-id="7a11e-138">Build 19018</span></span>
<span data-ttu-id="7a11e-139">Allgemeine Windows-Informationen zu Build 19018 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-139">For general Windows information on build 19018 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/11/05/announcing-windows-10-insider-preview-build-19018/).</span></span>

* <span data-ttu-id="7a11e-140">[WSL2] Verwenden Sie cache=mmap als Standardeinstellung für 9p-Einbindungen, um Probleme mit Dotnet-Apps zu beheben</span><span class="sxs-lookup"><span data-stu-id="7a11e-140">[WSL2] Use cache=mmap as the default for 9p mounts to fix dotnet apps</span></span>
* <span data-ttu-id="7a11e-141">[WSL2] Korrekturen für localhost-Relay [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="7a11e-141">[WSL2] Fixes for localhost relay [GH 4340]</span></span>
* <span data-ttu-id="7a11e-142">[WSL2] Einführen einer distributionsübergreifenden, gemeinsam genutzten tmpfs-Einbindung für den Freigabezustand zwischen Distributionen</span><span class="sxs-lookup"><span data-stu-id="7a11e-142">[WSL2] Introduce a cross-distro shared tmpfs mount for sharing state between distros</span></span>
* <span data-ttu-id="7a11e-143">Korrektur der Wiederherstellung des permanenten Netzwerklaufwerks für \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="7a11e-143">Fix restoring persistent network drive for \\\\wsl$</span></span>

## <a name="build-19013"></a><span data-ttu-id="7a11e-144">Build 19013</span><span class="sxs-lookup"><span data-stu-id="7a11e-144">Build 19013</span></span>
<span data-ttu-id="7a11e-145">Allgemeine Windows-Informationen zu Build 19013 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-145">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="7a11e-146">[WSL2] Verbesserte Arbeitsspeicherleistung der VM des WSL-Hilfsprogramms</span><span class="sxs-lookup"><span data-stu-id="7a11e-146">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="7a11e-147">Arbeitsspeicher, der nicht mehr verwendet wird, wird an den Host zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-147">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="7a11e-148">[WSL2] Aktualisieren der Kernelversion auf 4.19.79</span><span class="sxs-lookup"><span data-stu-id="7a11e-148">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="7a11e-149">(CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK und CONFIG_BRIDGE_VLAN_FILTERING hinzugefügt).</span><span class="sxs-lookup"><span data-stu-id="7a11e-149">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="7a11e-150">[WSL2] Korrigiertes Eingaberelay zur Behandlung von Fällen, in denen stdin ein nicht geschlossenes Pipehandle ist [GH 4424]</span><span class="sxs-lookup"><span data-stu-id="7a11e-150">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="7a11e-151">Die Überprüfung auf \\\\wsl$ unterscheidet nicht mehr zwischen Groß- und Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="7a11e-151">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="7a11e-152">Build 19002</span><span class="sxs-lookup"><span data-stu-id="7a11e-152">Build 19002</span></span>
<span data-ttu-id="7a11e-153">Allgemeine Windows-Informationen zu Build 19002 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-153">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="7a11e-154">[WSL] Beheben von Problemen bei der Behandlung einiger Unicode-Zeichen: https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="7a11e-154">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="7a11e-155">[WSL] Korrektur seltener Fälle, in denen die Registrierung von Distributionen aufgehoben werden kann, wenn sie unmittelbar nach einem Build-zu-Build-Upgrade gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-155">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="7a11e-156">[WSL] Korrektur eines kleinen Problems beim Herunterfahren mit „wsl.exe“, bei dem Leerlaufzeitgeber von Instanzen nicht abgebrochen wurden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-156">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="7a11e-157">Build 18995</span><span class="sxs-lookup"><span data-stu-id="7a11e-157">Build 18995</span></span>
<span data-ttu-id="7a11e-158">Allgemeine Windows-Informationen zu Build 18995 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-158">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="7a11e-159">[WSL2] Korrektur eines Problems, bei dem DrvFs-Einbindungen nach dem Abbruch eines Vorgangs (z.B. STRG-C) zu funktionieren aufhörten [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="7a11e-159">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="7a11e-160">[WSL2] Korrektur der Verarbeitung sehr großer hvsocket-Nachrichten [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="7a11e-160">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="7a11e-161">[WSL2] Korrektur eines Interop-Problems, wenn stdin eine Datei ist [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="7a11e-161">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="7a11e-162">[WSL2] Korrektur eines Absturzes, wenn ein unerwarteter Netzwerkstatus festgestellt wird [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="7a11e-162">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="7a11e-163">[WSL2] Abfragen des Namens der Distribution beim Interopserver, wenn der aktuelle Prozess nicht über die Umgebungsvariable verfügt</span><span class="sxs-lookup"><span data-stu-id="7a11e-163">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="7a11e-164">[WSL2] Korrektur eines Interop-Problems, wenn stdin eine Datei ist</span><span class="sxs-lookup"><span data-stu-id="7a11e-164">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="7a11e-165">[WSL2] Aktualisieren der Linux-Kernelversion auf 4.19.72</span><span class="sxs-lookup"><span data-stu-id="7a11e-165">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="7a11e-166">[WSL2] Neu hinzugefügte Möglichkeit zum Angeben weiterer Kernelbefehle in der Befehlszeile mithilfe von WSLCONFIG</span><span class="sxs-lookup"><span data-stu-id="7a11e-166">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="7a11e-167">Build 18990</span><span class="sxs-lookup"><span data-stu-id="7a11e-167">Build 18990</span></span>
<span data-ttu-id="7a11e-168">Allgemeine Windows-Informationen zu Build 18990 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-168">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="7a11e-169">Verbesserte Leistung für Verzeichnisauflistungen in \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="7a11e-169">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="7a11e-170">[WSL2] Einführen zusätzlicher Entropie beim Systemstart [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="7a11e-170">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="7a11e-171">[WSL2] Problembehebung für Windows-Interop bei der Verwendung von „su“ / „sudo“ [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="7a11e-171">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="7a11e-172">Build 18980</span><span class="sxs-lookup"><span data-stu-id="7a11e-172">Build 18980</span></span>
<span data-ttu-id="7a11e-173">Allgemeine Windows-Informationen zu Build 18980 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-173">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="7a11e-174">Korrektur des Lesen von symbolischen Verknüpfungen, die FILE_READ_DATA verweigern.</span><span class="sxs-lookup"><span data-stu-id="7a11e-174">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="7a11e-175">Dies umfasst alle symbolischen Verknüpfungen, die von Windows aus Gründen der Abwärtskompatibilität erstellt werden, z.B. „C:\Dokumente und Einstellungen“ und eine Reihe von symbolischen Verknüpfungen im Benutzerprofilverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7a11e-175">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="7a11e-176">Festlegen eines unerwarteten Dateisystemzustands als nicht schwerwiegend [GH 4334, 4305]</span><span class="sxs-lookup"><span data-stu-id="7a11e-176">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="7a11e-177">[WSL2] Hinzufügen von Unterstützung für arm64, wenn Ihre CPU/Firmware Virtualisierung unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a11e-177">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="7a11e-178">[WSL2] Zulassen der Anzeige von Kernelprotokollen durch nicht berechtigte Benutzer</span><span class="sxs-lookup"><span data-stu-id="7a11e-178">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="7a11e-179">[WSL2] Korrigieren des Ausgaberelays, wenn stdout/stderr-Sockets geschlossen wurden [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="7a11e-179">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="7a11e-180">[WSL2] Unterstützung von Akku- und AC-Adapter-Passthrough</span><span class="sxs-lookup"><span data-stu-id="7a11e-180">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="7a11e-181">[WSL2] Aktualisieren des Linux-Kernels auf 4.19.67</span><span class="sxs-lookup"><span data-stu-id="7a11e-181">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="7a11e-182">Hinzufügen der Möglichkeit, den Standardbenutzernamen in „/etc/wsl.conf“ festzulegen:</span><span class="sxs-lookup"><span data-stu-id="7a11e-182">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="7a11e-183">Build 18975</span><span class="sxs-lookup"><span data-stu-id="7a11e-183">Build 18975</span></span>
<span data-ttu-id="7a11e-184">Allgemeine Windows-Informationen zu Build 18975 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-184">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="7a11e-185">[WSL2] Korrektur einer Reihe von Problemen mit der localhost-Zuverlässigkeit [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="7a11e-185">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="7a11e-186">Build 18970</span><span class="sxs-lookup"><span data-stu-id="7a11e-186">Build 18970</span></span>
<span data-ttu-id="7a11e-187">Allgemeine Windows-Informationen zu Build 18970 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-187">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="7a11e-188">[WSL2] Synchronisierung der Uhrzeit mit der Hostzeit, wenn das System nach dem Ruhezustand fortgesetzt wird [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="7a11e-188">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="7a11e-189">[WSL2] Nach Möglichkeit Erstellen symbolischer NT-Verknüpfungen auf den Windows-Volumes</span><span class="sxs-lookup"><span data-stu-id="7a11e-189">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="7a11e-190">[WSL2] Erstellen von Distributionen in den UTS-, IPC-, PID- und Mount-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="7a11e-190">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="7a11e-191">[WSL2] Korrigieren des localhost-Portrelays, wenn der Server direkt an localhost gebunden wird [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="7a11e-191">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="7a11e-192">[WSL2] Korrigieren von Interop, wenn die Ausgabe umgeleitet wird [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="7a11e-192">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="7a11e-193">[WSL2] Unterstützung der Übersetzung absoluter symbolischer NT-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-193">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="7a11e-194">[WSL2] Aktualisieren des Kernels auf 4.19.59</span><span class="sxs-lookup"><span data-stu-id="7a11e-194">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="7a11e-195">[WSL2] Ordnungsgemäße Festlegung der Subnetzmaske für eth0.</span><span class="sxs-lookup"><span data-stu-id="7a11e-195">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="7a11e-196">[WSL2] Ändern der Logik, um die Konsolenworkerschleife zu verlassen, wenn das Beendigungsereignis signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-196">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="7a11e-197">[WSL2] Auswerfen der Distributions-VHD, wenn die Distribution nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-197">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="7a11e-198">[WSL2] Korrigieren der Analysebibliothek, um leere Werte ordnungsgemäß zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-198">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="7a11e-199">[WSL2] Unterstützung von Docker Desktop durch Erstellen von distributionsübergreifenden Einbindungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-199">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="7a11e-200">Dieses Verhalten kann durch eine Distribution übernommen werden, indem die folgende Zeile der Datei „/etc/wsl.conf“ hinzugefügt wird:</span><span class="sxs-lookup"><span data-stu-id="7a11e-200">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="7a11e-201">Build 18945</span><span class="sxs-lookup"><span data-stu-id="7a11e-201">Build 18945</span></span>
<span data-ttu-id="7a11e-202">Allgemeine Windows-Informationen zu Build 18945 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-202">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-203">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-203">WSL</span></span>
* <span data-ttu-id="7a11e-204">[WSL2] Zulassen, dass der Zugriff auf lauschende TCP-Sockets in WSL2 über „localhost:port“ vom Host erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="7a11e-204">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="7a11e-205">[WSL2] Korrekturen für Installations- und Konvertierungsfehler und zusätzliche Diagnose zur Nachverfolgung zukünftiger Probleme [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="7a11e-205">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="7a11e-206">[WSL2] Verbessern der Diagnose von WSL2-Netzwerkproblemen</span><span class="sxs-lookup"><span data-stu-id="7a11e-206">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="7a11e-207">[WSL2] Aktualisieren der Kernelversion auf 4.19.55</span><span class="sxs-lookup"><span data-stu-id="7a11e-207">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="7a11e-208">[WSL2] Aktualisieren des Kernels mit Konfigurationsoptionen, die für Docker erforderlich sind [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="7a11e-208">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="7a11e-209">[WSL2] Erhöhen der Anzahl der CPUs, die der Lightweight Utility-VM zugeordnet sind, um eine mit dem Host identische Anzahl zu erreichen (wurde zuvor durch CONFIG_NR_CPUS in der Kernelkonfiguration auf 8 begrenzt) [GH 4137]</span><span class="sxs-lookup"><span data-stu-id="7a11e-209">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="7a11e-210">[WSL2] Erstellen einer Auslagerungsdatei für die WSL2-Lightweight-VM</span><span class="sxs-lookup"><span data-stu-id="7a11e-210">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="7a11e-211">[WSL2] Zulassen, dass Benutzereinbindungen über die \\\\wsl$\\-Distribution (z.B. sshfs) sichtbar sind [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="7a11e-211">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="7a11e-212">[WSL2] Verbessern der Leistung des 9P-Dateisystems</span><span class="sxs-lookup"><span data-stu-id="7a11e-212">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="7a11e-213">[WSL2] Sicherstellen, dass die VHD-ACL nicht unbegrenzt anwächst [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="7a11e-213">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="7a11e-214">[WSL2] Aktualisieren der Kernelkonfiguration für die Unterstützung von squashfs und xt_conntrack [GH 4107, 4123]</span><span class="sxs-lookup"><span data-stu-id="7a11e-214">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="7a11e-215">[WSL2] Korrektur für interopaktivierte „/etc/wsl.conf“-Option [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="7a11e-215">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="7a11e-216">[WSL2] Rückgabe von ENOTSUP, wenn das Dateisystem EAS nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a11e-216">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="7a11e-217">[WSL2] Korrigieren von CopyFile-Hänger mit \\\\wsl$</span><span class="sxs-lookup"><span data-stu-id="7a11e-217">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="7a11e-218">Umschalten von Standard-umask in 0022 und Hinzufügen der filesystem.umask-Einstellung zu „/etc/wsl.conf“</span><span class="sxs-lookup"><span data-stu-id="7a11e-218">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="7a11e-219">Korrigieren von wslpath, um symbolische Verknüpfungen ordnungsgemäß aufzulösen, dies wurde in 19h1 zurückgesetzt [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="7a11e-219">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="7a11e-220">Einführung der Datei „%UserProfile%\\.wslconfig“ für die Optimierung der WSL2-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-220">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="7a11e-221">Build 18917</span><span class="sxs-lookup"><span data-stu-id="7a11e-221">Build 18917</span></span>
<span data-ttu-id="7a11e-222">Allgemeine Windows-Informationen zu Build 18917 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-222">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-223">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-223">WSL</span></span>
* <span data-ttu-id="7a11e-224">WSL 2 ist Jetzt verfügbar!</span><span class="sxs-lookup"><span data-stu-id="7a11e-224">WSL 2 is now available!</span></span> <span data-ttu-id="7a11e-225">Weitere Informationen finden Sie im [Blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-225">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="7a11e-226">Korrektur einer Regression, bei der das Starten von Windows-Prozessen über symbolische Verknüpfungen nicht ordnungsgemäß funktioniert hat [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="7a11e-226">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="7a11e-227">Hinzufügen der Optionen wsl.exe --list --verbose, wsl.exe --list --quiet und wsl.exe --import --version zu „wsl.exe“</span><span class="sxs-lookup"><span data-stu-id="7a11e-227">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="7a11e-228">Hinzufügen der Option wsl.exe --shutdown</span><span class="sxs-lookup"><span data-stu-id="7a11e-228">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="7a11e-229">Plan 9: Zulassen des Öffnend eines Verzeichnisses für einen erfolgreichen Schreibvorgang</span><span class="sxs-lookup"><span data-stu-id="7a11e-229">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="7a11e-230">Build 18890</span><span class="sxs-lookup"><span data-stu-id="7a11e-230">Build 18890</span></span>
<span data-ttu-id="7a11e-231">Allgemeine Windows-Informationen zu Build 18890 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-231">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-232">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-232">WSL</span></span>
* <span data-ttu-id="7a11e-233">Nicht blockierender Socketverlust [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="7a11e-233">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="7a11e-234">EOF-Eingabe für Terminal kann nachfolgende Lesevorgänge blockieren [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="7a11e-234">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="7a11e-235">Aktualisieren des resolv.conf-Headers, damit er auf „wsl.conf“ verweist [in GH 3928 beschrieben].</span><span class="sxs-lookup"><span data-stu-id="7a11e-235">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="7a11e-236">Deadlock im epoll-Löschcode [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="7a11e-236">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="7a11e-237">Verarbeiten von Leerzeichen in Argumenten für --import und --export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="7a11e-237">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="7a11e-238">Erweitern von mit mmap behandelten Dateien funktioniert nicht ordnungsgemäß [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="7a11e-238">Extending mmap'd files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="7a11e-239">Korrektur eines Problems mit ARM64 \\\\wsl$-Zugriff funktioniert nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="7a11e-239">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="7a11e-240">Hinzufügen eines besseren Standardsymbols für „wsl.exe“</span><span class="sxs-lookup"><span data-stu-id="7a11e-240">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="7a11e-241">Build 18342</span><span class="sxs-lookup"><span data-stu-id="7a11e-241">Build 18342</span></span>
<span data-ttu-id="7a11e-242">Allgemeine Windows-Informationen zu Build 18342 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-242">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-243">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-243">WSL</span></span>
* <span data-ttu-id="7a11e-244">Wir haben für Benutzer die Möglichkeit hinzugefügt, auf Linux-Dateien in einer WSL-Distribution aus Windows zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-244">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="7a11e-245">Auf diese Dateien kann über die Befehlszeile zugegriffen werden. Außerdem können Windows-Apps wie der Datei-Explorer, VSCode usw. mit diesen Dateien interagieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-245">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="7a11e-246">Greifen Sie auf Ihre Dateien zu, indem Sie zu \\\\wsl$\\<distributions_name> navigieren, oder zeigen Sie eine Liste der ausgeführten Distributionen an, indem Sie zu \\\\wsl$ navigieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-246">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="7a11e-247">Hinzufügen zusätzlicher CPU-Infotags und Korrigieren der Cpus_allowed[_list]-Werte [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="7a11e-247">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="7a11e-248">Unterstützung der Ausführung aus Nicht-Leaderthread [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="7a11e-248">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="7a11e-249">Behandeln von Konfigurationsupdatefehlern als nicht schwerwiegend [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="7a11e-249">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="7a11e-250">Aktualisieren von binfmt für die ordnungsgemäße Verarbeitung von Offsets [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="7a11e-250">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="7a11e-251">Aktivieren der Zuordnung von Netzlaufwerken für Plan 9 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="7a11e-251">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="7a11e-252">Unterstützung von Windows -> Linux und Linux -> Windows-Pfadübersetzung für Bindungseinbindungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-252">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="7a11e-253">Erstellen schreibgeschützter Abschnitte für Zuordnungen für Dateien, die schreibgeschützt geöffnet sind</span><span class="sxs-lookup"><span data-stu-id="7a11e-253">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="7a11e-254">Build 18334</span><span class="sxs-lookup"><span data-stu-id="7a11e-254">Build 18334</span></span>
<span data-ttu-id="7a11e-255">Allgemeine Windows-Informationen zu Build 18334 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-255">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-256">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-256">WSL</span></span>
* <span data-ttu-id="7a11e-257">Umgestalten der Art und Weise, in der die Windows-Zeitzone einer Linux-Zeitzone zugeordnet wird [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="7a11e-257">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="7a11e-258">Beheben von Speicherverlusten und Hinzufügen neuer Zeichenfolgenübersetzungsfunktionen [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="7a11e-258">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="7a11e-259">SIGCONT für eine Threadgruppe ohne Threads ist eine Nulloperation [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="7a11e-259">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="7a11e-260">Richtige Anzeige von Socket- und Epoll-Dateideskriptoren in „/proc/self/fd“</span><span class="sxs-lookup"><span data-stu-id="7a11e-260">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="7a11e-261">Build 18305</span><span class="sxs-lookup"><span data-stu-id="7a11e-261">Build 18305</span></span>
<span data-ttu-id="7a11e-262">Allgemeine Windows-Informationen zu Build 18305 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-262">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-263">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-263">WSL</span></span>
* <span data-ttu-id="7a11e-264">pthreads verlieren den Zugriff auf Dateien, wenn der primäre Thread beendet wird [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="7a11e-264">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="7a11e-265">TIOCSCTTY sollte den Parameter „force“ ignorieren, wenn er nicht erforderlich ist [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="7a11e-265">TIOCSCTTY should ignore the "force" parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="7a11e-266">Verbesserungen an der Befehlszeile von „wsl.exe“ und Hinzufügung von Import-/Exportfunktionen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-266">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="7a11e-267">Build 18277</span><span class="sxs-lookup"><span data-stu-id="7a11e-267">Build 18277</span></span>
<span data-ttu-id="7a11e-268">Allgemeine Windows-Informationen zu Build 18277 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-268">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-269">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-269">WSL</span></span>
* <span data-ttu-id="7a11e-270">Korrektur des Fehlers „no such interface supported“ in Build 18272 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="7a11e-270">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="7a11e-271">Ignorieren des MNT_FORCE-Flags für Systemaufruf zum Aufheben der Einbindung [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="7a11e-271">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="7a11e-272">Umschalten von WSL-Interop für die Verwendung der offiziellen CreatePseudoConsole-API</span><span class="sxs-lookup"><span data-stu-id="7a11e-272">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="7a11e-273">Keinen Timeoutwert beibehalten, wenn FUTEX_WAIT neu gestartet wird</span><span class="sxs-lookup"><span data-stu-id="7a11e-273">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="7a11e-274">Build 18272</span><span class="sxs-lookup"><span data-stu-id="7a11e-274">Build 18272</span></span>
<span data-ttu-id="7a11e-275">Allgemeine Windows-Informationen zu Build 18272 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-275">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-276">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-276">WSL</span></span>
* <span data-ttu-id="7a11e-277">**WARNUNG:** In diesem Build liegt ein Problem vor, durch das WSL nicht funktionsfähig wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-277">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="7a11e-278">Wenn Sie versuchen, die Verteilung zu starten, wird der Fehler „Schnittstelle nicht unterstützt“ angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-278">When trying to launch your distribution you will see a "No such interface supported" error.</span></span> <span data-ttu-id="7a11e-279">Das Problem wurde behoben und ist im Insider Fast-Build der nächsten Woche nicht mehr enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-279">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="7a11e-280">Wenn Sie diesen Build installiert haben, können Sie ein Rollback auf den vorherigen Windows-Build durchführen, indem Sie unter „Einstellungen > Update und Sicherheit > Wiederherstellung“ die Option „Zur vorherigen Version von Windows 10 zurückkehren“ auswählen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-280">If you've installed this build you can roll back to the previous Windows build using "Go back to the previous version of Windows 10" in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="7a11e-281">Build 18267</span><span class="sxs-lookup"><span data-stu-id="7a11e-281">Build 18267</span></span>
<span data-ttu-id="7a11e-282">Allgemeine Windows-Informationen zu Build 18267 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-282">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-283">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-283">WSL</span></span>
* <span data-ttu-id="7a11e-284">Korrektur eines Problems, bei dem der Zombieprozess möglicherweise nicht beendet und unbegrenzt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-284">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="7a11e-285">WslRegisterDistribution hängt, wenn die Fehlermeldung die maximale Länge überschreitet [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="7a11e-285">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="7a11e-286">Zulassen der erfolgreichen Ausführung von fsync für schreibgeschützte Dateien auf DrvFs [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="7a11e-286">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="7a11e-287">Sicherstellen, dass die Verzeichnisse „/bin“ und „/sbin“ vorhanden sind, bevor symbolische Verknüpfungen darin erstellt werden [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="7a11e-287">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="7a11e-288">Hinzufügen eines Instanztimeoutmechanismus für WSL-Instanzen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-288">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="7a11e-289">Der Timeoutwert ist derzeit auf 15 Sekunden festgelegt. Das bedeutet, dass die Instanz 15 Sekunden nach Beendigung des letzten WSL-Prozesses beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-289">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="7a11e-290">Um eine Distribution sofort zu beenden, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7a11e-290">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="7a11e-291">Build 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="7a11e-291">Build 17763 (1809)</span></span>
<span data-ttu-id="7a11e-292">Allgemeine Windows-Informationen zu Build 17763 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-292">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-293">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-293">WSL</span></span>
* <span data-ttu-id="7a11e-294">Berechtigungsüberprüfung für Setpriority-Systemaufruf ist zu streng, um die gleiche Threadpriorität zu ändern[GH 1838].</span><span class="sxs-lookup"><span data-stu-id="7a11e-294">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="7a11e-295">Stellen Sie sicher, dass die unbeeinflusste Interruptzeit für die Startzeit verwendet wird, um zu vermeiden, dass negative Werte für clock_gettime (CLOCK_BOOTTIME) zurückgegeben werden [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="7a11e-295">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="7a11e-296">Verarbeiten von symbolischen Verknüpfungen im WSL-binfmt-Interpreter [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="7a11e-296">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="7a11e-297">Bessere Verarbeitung der Bereinigung des Threadgruppen-Leaderdateideskriptors.</span><span class="sxs-lookup"><span data-stu-id="7a11e-297">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="7a11e-298">Umschalten von WSL für die Verwendung von KeQueryInterruptTimePrecise anstelle von KeQueryPerformanceCounter zur Vermeidung eines Überlaufs [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="7a11e-298">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="7a11e-299">Ptrace-Anfügevorgang kann zu einem ungültigen Rückgabewert von Systemaufrufen führen [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="7a11e-299">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="7a11e-300">Korrektur mehrerer Probleme, die sich auf AF_UNIX beziehen [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="7a11e-300">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="7a11e-301">Korrektur eines Problems, das dazu führen kann, dass WSL-Interop fehlschlägt, wenn das aktuelle Arbeitsverzeichnis weniger als 5 Zeichen lang ist [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="7a11e-301">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="7a11e-302">Vermeiden von einer Sekunde Verzögerung bei Ausfall von Loopbackverbindungen mit nicht vorhandenen Ports [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="7a11e-302">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="7a11e-303">Hinzufügen der Stubdatei „/proc/sys/fs/file-max“ [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="7a11e-303">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="7a11e-304">Genauere IPv6-Bereichsinformationen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-304">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="7a11e-305">PR_SET_PTRACER-Unterstützung [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="7a11e-305">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="7a11e-306">Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="7a11e-306">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="7a11e-307">Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="7a11e-307">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="7a11e-308">Verbesserte Zombieunterstützung [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="7a11e-308">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="7a11e-309">Hinzufügen von wsl.conf-Einträgen zum Steuern des Windows-Interop-Verhaltens [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="7a11e-309">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="7a11e-310">Korrektur des Verhaltens, dass getsockname nicht immer den Porduktfamilientyp des UNIX-Sockets zurückgibt [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="7a11e-310">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="7a11e-311">Hinzufügen von Unterstützung für TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="7a11e-311">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="7a11e-312">Nicht blockierende Sockets beim Verbindungsaufbau sollten für Schreibversuche EAGAIN zurückgeben [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="7a11e-312">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="7a11e-313">Unterstützung von Interop auf eingebundenen VHDs [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="7a11e-313">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="7a11e-314">Korrektur von Problem mit der Berechtigungsüberprüfung im Stammordner [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="7a11e-314">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="7a11e-315">Eingeschränkte Unterstützung für die TTY-Tastatur-ioctls KDGKBTYPE, KDGKBMODE und KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="7a11e-315">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="7a11e-316">Windows-UI-Apps sollten ausgeführt selbst dann werden, wenn Sie im Hintergrund gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-316">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="7a11e-317">Hinzufügen der Option wsl -u oder--user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="7a11e-317">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="7a11e-318">Korrektur von WSL-Startproblemen, wenn der Schnellstart aktiviert ist [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="7a11e-318">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="7a11e-319">Unix-Sockets müssen getrennte Peeranmelde Informationen beibehalten [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="7a11e-319">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="7a11e-320">Nicht blockierende Unix-Sockets, die unbegrenzt EAGAIN-Fehler ausgeben [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="7a11e-320">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="7a11e-321">case=off ist der neue standardmäßige drvfs-Einbindungstyp [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="7a11e-321">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="7a11e-322">Weitere Informationen finden Sie im [Blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-322">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="7a11e-323">Hinzufügen von wslconfig/terminate zum Beenden ausgeführter Distributionen</span><span class="sxs-lookup"><span data-stu-id="7a11e-323">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="7a11e-324">Korrektur des Problems mit den Kontextmenüeinträgen der WSL-Shell, die Pfade mit Leerzeichen nicht ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="7a11e-324">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="7a11e-325">Bereitstellen von Unterscheidung von Groß-/Kleinschreibung pro Verzeichnis als erweitertes Attribut</span><span class="sxs-lookup"><span data-stu-id="7a11e-325">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="7a11e-326">ARM64: Emulieren von Cacheverwaltungsvorgängen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-326">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="7a11e-327">Beheben von [dotnet-Problem](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="7a11e-327">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="7a11e-328">DrvFs: Nur Escapezeichen im privaten Bereich, die einem mit Escapezeichen versehenen Zeichen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-328">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="7a11e-329">Korrektur eines Off-by-one-Fehlers in der Längenüberprüfung des ELF Parserinterpreters [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="7a11e-329">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="7a11e-330">Absolute WSL-Timer mit einer Zeitangabe in der Vergangenheit werden nicht ausgelöst [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="7a11e-330">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="7a11e-331">Sicherstellen, dass neu erstellte Analysepunkte als solche im übergeordneten Verzeichnis aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-331">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="7a11e-332">Atomarisches Erstellen von Verzeichnissen mit Berücksichtigung von Groß- und Kleinschreibung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="7a11e-332">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="7a11e-333">Korrektur eines zusätzlichen Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-333">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="7a11e-334">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="7a11e-334">[GH 2712]</span></span>
* <span data-ttu-id="7a11e-335">Korrektur eines WSL-Startfehlers, wenn UMCI aktiviert ist.-</span><span class="sxs-lookup"><span data-stu-id="7a11e-335">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="7a11e-336">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="7a11e-336">[GH 3020]</span></span>
* <span data-ttu-id="7a11e-337">Hinzufügen des Explorer-Kontextmenüs zum Starten von WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="7a11e-337">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="7a11e-338">Halten Sie in einem Explorer-Fenster die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste, um diese Option zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-338">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="7a11e-339">Korrektur des nicht blockierenden UNIX-Socketverhaltens [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="7a11e-339">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="7a11e-340">Korrigieren des hängenden NETLINK-Befehls, wie in GH 2026 gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-340">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="7a11e-341">Hinzufügen von Unterstützung für Einbindungsweitergabeflags [GH 2911]</span><span class="sxs-lookup"><span data-stu-id="7a11e-341">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="7a11e-342">Korrektur von Problem mit truncate, das keine inotify-Ereignisse verursacht [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="7a11e-342">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="7a11e-343">Hinzufügen der Option --exec für „wsl.exe“ zum Aufrufen eine einzelne Binärdatei ohne Shell.</span><span class="sxs-lookup"><span data-stu-id="7a11e-343">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="7a11e-344">Hinzufügen der Option --distribution für „wsl.exe“, um eine bestimmte Distribution auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-344">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="7a11e-345">Eingeschränkte Unterstützung für dmesg.</span><span class="sxs-lookup"><span data-stu-id="7a11e-345">Limited support for dmesg.</span></span> <span data-ttu-id="7a11e-346">Anwendungen können sich jetzt in dmesg protokollieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-346">Applications can now log to dmesg.</span></span> <span data-ttu-id="7a11e-347">Der WSL-Treiber protokolliert eingeschränkte Informationen in dmesg.</span><span class="sxs-lookup"><span data-stu-id="7a11e-347">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="7a11e-348">In Zukunft kann dies so erweitert werden, dass andere Informationen/Diagnoseinhalte vom Treiber erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-348">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="7a11e-349">Hinweis: dmesg wird derzeit über die `/dev/kmsg`-Geräteschnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-349">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="7a11e-350">`syslog`-Systemaufrufschnittstelle wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-350">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="7a11e-351">Daher funktionieren einige der `dmesg`-Befehlszeilenoptionen (z.B. `-S`, `-C`) nicht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-351">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="7a11e-352">Änderung der Standard-GID und des Modus von seriellen Geräten entsprechend den nativen Einstellungen [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="7a11e-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="7a11e-353">DrvFs unterstützt jetzt erweiterte Attribute.</span><span class="sxs-lookup"><span data-stu-id="7a11e-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="7a11e-354">Hinweis: Für DrvFs gelten einige Einschränkungen für den Namen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="7a11e-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="7a11e-355">Einige Zeichen (etwa „/“, „:“ und „\*“) sind unzulässig, und für Namen erweiterter Attribute wird in DrvFs keine Groß- und Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-355">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="7a11e-356">Build 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="7a11e-356">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="7a11e-357">Allgemeine Windows-Informationen zu Build 18252 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-357">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-358">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-358">WSL</span></span>
* <span data-ttu-id="7a11e-359">Verschieben von init- und bsdtar-Binärdateien aus der lxssmanager-DLL in einen separaten Toolsordner</span><span class="sxs-lookup"><span data-stu-id="7a11e-359">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="7a11e-360">Korrektur von Racebedingung um schließenden Dateideskriptor bei Verwendung von CLONE_FILES</span><span class="sxs-lookup"><span data-stu-id="7a11e-360">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="7a11e-361">Verarbeiten optionaler Felder in „/proc/pid/mountinfo“ bei der Übersetzung von DrvFs-Pfaden</span><span class="sxs-lookup"><span data-stu-id="7a11e-361">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="7a11e-362">Zulassen, dass DrvFs mklod ohne Metadatenunterstützung für S_IFREG erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="7a11e-362">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="7a11e-363">Für schreibgeschützte Dateien, die auf DrvFs erstellt wurden, muss das schreibgeschützte Attribut festgelegt werden [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="7a11e-363">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="7a11e-364">Hinzufügen von /sbin/mount.drvfs-Hilfsprogramm zur Verarbeitung der DrvFs-Einbindung</span><span class="sxs-lookup"><span data-stu-id="7a11e-364">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="7a11e-365">Verwenden der POSIX-Umbenennung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="7a11e-365">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="7a11e-366">Ermöglichen der Pfadübersetzung für Volumes ohne Volume-GUID.</span><span class="sxs-lookup"><span data-stu-id="7a11e-366">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="7a11e-367">Build 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="7a11e-367">Build 17738 (Fast)</span></span>
<span data-ttu-id="7a11e-368">Allgemeine Windows-Informationen zu Build 17738 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-368">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-369">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-369">WSL</span></span>
* <span data-ttu-id="7a11e-370">Berechtigungsüberprüfung für Setpriority-Systemaufruf ist zu streng, um die gleiche Threadpriorität zu ändern[GH 1838].</span><span class="sxs-lookup"><span data-stu-id="7a11e-370">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="7a11e-371">Stellen Sie sicher, dass die unbeeinflusste Interruptzeit für die Startzeit verwendet wird, um zu vermeiden, dass negative Werte für clock_gettime (CLOCK_BOOTTIME) zurückgegeben werden [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="7a11e-371">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="7a11e-372">Verarbeiten von symbolischen Verknüpfungen im WSL-binfmt-Interpreter [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="7a11e-372">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="7a11e-373">Bessere Verarbeitung der Bereinigung des Threadgruppen-Leaderdateideskriptors.</span><span class="sxs-lookup"><span data-stu-id="7a11e-373">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="7a11e-374">Build 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="7a11e-374">Build 17728 (Fast)</span></span>
<span data-ttu-id="7a11e-375">Allgemeine Windows-Informationen zu Build 17728 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-375">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-376">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-376">WSL</span></span>
* <span data-ttu-id="7a11e-377">Umschalten von WSL für die Verwendung von KeQueryInterruptTimePrecise anstelle von KeQueryPerformanceCounter zur Vermeidung eines Überlaufs [GH 3252].</span><span class="sxs-lookup"><span data-stu-id="7a11e-377">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="7a11e-378">Ptrace-Anfügevorgang kann zu einem ungültigen Rückgabewert von Systemaufrufen führen [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="7a11e-378">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="7a11e-379">Korrektur mehrerer Probleme, die sich auf AF_UNIX beziehen [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="7a11e-379">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="7a11e-380">Korrektur eines Problems, das dazu führen kann, dass WSL-Interop fehlschlägt, wenn das aktuelle Arbeitsverzeichnis weniger als 5 Zeichen lang ist [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="7a11e-380">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="7a11e-381">Build 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="7a11e-381">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="7a11e-382">Allgemeine Windows-Informationen zu Build 18204 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-382">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-383">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-383">WSL</span></span>
* <span data-ttu-id="7a11e-384">Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="7a11e-384">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="7a11e-385">Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="7a11e-385">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="7a11e-386">Build 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="7a11e-386">Build 17723 (Fast)</span></span>
<span data-ttu-id="7a11e-387">Allgemeine Windows-Informationen zu Build 17723 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-387">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-388">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-388">WSL</span></span>
* <span data-ttu-id="7a11e-389">Vermeiden von einer Sekunde Verzögerung bei Ausfall von Loopbackverbindungen mit nicht vorhandenen Ports [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="7a11e-389">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="7a11e-390">Hinzufügen der Stubdatei „/proc/sys/fs/file-max“ [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="7a11e-390">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="7a11e-391">Genauere IPv6-Bereichsinformationen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-391">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="7a11e-392">PR_SET_PTRACER-Unterstützung [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="7a11e-392">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="7a11e-393">Versehentliches Löschen eines edge-ausgelösten epoll-Ereignisses durch das Pipedateisystem [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="7a11e-393">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="7a11e-394">Ausführbare Win32-Datei, die über die symbolische NTFS-Verknüpfung gestartet wurde, respektiert den Namen der symbolischen Verknüpfung nicht [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="7a11e-394">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="7a11e-395">Build 17713</span><span class="sxs-lookup"><span data-stu-id="7a11e-395">Build 17713</span></span>
<span data-ttu-id="7a11e-396">Allgemeine Windows-Informationen zu Build 17713 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-396">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-397">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-397">WSL</span></span>
* <span data-ttu-id="7a11e-398">Verbesserte Zombieunterstützung [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="7a11e-398">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="7a11e-399">Hinzufügen von wsl.conf-Einträgen zum Steuern des Windows-Interop-Verhaltens [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="7a11e-399">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="7a11e-400">Korrektur des Verhaltens, dass getsockname nicht immer den Porduktfamilientyp des UNIX-Sockets zurückgibt [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="7a11e-400">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="7a11e-401">Hinzufügen von Unterstützung für TIOCSTI [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="7a11e-401">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="7a11e-402">Nicht blockierende Sockets beim Verbindungsaufbau sollten für Schreibversuche EAGAIN zurückgeben [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="7a11e-402">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="7a11e-403">Unterstützung von Interop auf eingebundenen VHDs [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="7a11e-403">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="7a11e-404">Korrektur von Problem mit der Berechtigungsüberprüfung im Stammordner [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="7a11e-404">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="7a11e-405">Eingeschränkte Unterstützung für die TTY-Tastatur-ioctls KDGKBTYPE, KDGKBMODE und KDSKBMODE.</span><span class="sxs-lookup"><span data-stu-id="7a11e-405">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="7a11e-406">Windows-UI-Apps sollten ausgeführt selbst dann werden, wenn Sie im Hintergrund gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-406">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="7a11e-407">Build 17704</span><span class="sxs-lookup"><span data-stu-id="7a11e-407">Build 17704</span></span>
<span data-ttu-id="7a11e-408">Allgemeine Windows-Informationen zu Build 17704 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-408">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-409">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-409">WSL</span></span>
* <span data-ttu-id="7a11e-410">Hinzufügen der Option wsl -u oder--user [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="7a11e-410">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="7a11e-411">Korrektur von WSL-Startproblemen, wenn der Schnellstart aktiviert ist [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="7a11e-411">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="7a11e-412">Unix-Sockets müssen getrennte Peeranmelde Informationen beibehalten [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="7a11e-412">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="7a11e-413">Nicht blockierende Unix-Sockets, die unbegrenzt EAGAIN-Fehler ausgeben [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="7a11e-413">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="7a11e-414">case=off ist der neue standardmäßige drvfs-Einbindungstyp [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="7a11e-414">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="7a11e-415">Weitere Informationen finden Sie im [Blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-415">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="7a11e-416">Hinzufügen von wslconfig/terminate zum Beenden ausgeführter Distributionen</span><span class="sxs-lookup"><span data-stu-id="7a11e-416">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="7a11e-417">Build 17692</span><span class="sxs-lookup"><span data-stu-id="7a11e-417">Build 17692</span></span>
<span data-ttu-id="7a11e-418">Allgemeine Windows-Informationen zu Build 17692 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span><span class="sxs-lookup"><span data-stu-id="7a11e-418">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-419">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-419">WSL</span></span>
* <span data-ttu-id="7a11e-420">Korrektur des Problems mit den Kontextmenüeinträgen der WSL-Shell, die Pfade mit Leerzeichen nicht ordnungsgemäß behandeln.</span><span class="sxs-lookup"><span data-stu-id="7a11e-420">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="7a11e-421">Bereitstellen von Unterscheidung von Groß-/Kleinschreibung pro Verzeichnis als erweitertes Attribut</span><span class="sxs-lookup"><span data-stu-id="7a11e-421">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="7a11e-422">ARM64: Emulieren von Cacheverwaltungsvorgängen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-422">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="7a11e-423">Beheben von [dotnet-Problem](https://github.com/dotnet/core/issues/1561).</span><span class="sxs-lookup"><span data-stu-id="7a11e-423">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="7a11e-424">DrvFs: Nur Escapezeichen im privaten Bereich, die einem mit Escapezeichen versehenen Zeichen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-424">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="7a11e-425">Build 17686</span><span class="sxs-lookup"><span data-stu-id="7a11e-425">Build 17686</span></span>
<span data-ttu-id="7a11e-426">Allgemeine Windows-Informationen zu Build 17686 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span><span class="sxs-lookup"><span data-stu-id="7a11e-426">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-427">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-427">WSL</span></span>
* <span data-ttu-id="7a11e-428">Korrektur eines Off-by-one-Fehlers in der Längenüberprüfung des ELF Parserinterpreters [GH 3154].</span><span class="sxs-lookup"><span data-stu-id="7a11e-428">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="7a11e-429">Absolute WSL-Timer mit einer Zeitangabe in der Vergangenheit werden nicht ausgelöst [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="7a11e-429">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="7a11e-430">Sicherstellen, dass neu erstellte Analysepunkte als solche im übergeordneten Verzeichnis aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-430">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="7a11e-431">Atomarisches Erstellen von Verzeichnissen mit Berücksichtigung von Groß- und Kleinschreibung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="7a11e-431">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="7a11e-432">Build 17677</span><span class="sxs-lookup"><span data-stu-id="7a11e-432">Build 17677</span></span>
<span data-ttu-id="7a11e-433">Allgemeine Windows-Informationen zu Build 17677 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-433">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-434">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-434">WSL</span></span>
* <span data-ttu-id="7a11e-435">Korrektur eines zusätzlichen Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-435">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="7a11e-436">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="7a11e-436">[GH 2712]</span></span>
* <span data-ttu-id="7a11e-437">Korrektur eines WSL-Startfehlers, wenn UMCI aktiviert ist.-</span><span class="sxs-lookup"><span data-stu-id="7a11e-437">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="7a11e-438">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="7a11e-438">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="7a11e-439">Build 17666</span><span class="sxs-lookup"><span data-stu-id="7a11e-439">Build 17666</span></span>
<span data-ttu-id="7a11e-440">Allgemeine Windows-Informationen zu Build 17666 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-440">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-441">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-441">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="7a11e-442">WARNUNG: Es gibt ein Problem, das das Ausführen von WSL in einigen AMD-Chipsätzen verhindert [GH 3134].</span><span class="sxs-lookup"><span data-stu-id="7a11e-442">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="7a11e-443">Eine Korrektur ist verfügbar und wird in den Insider Build-Branch integriert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-443">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="7a11e-444">Hinzufügen des Explorer-Kontextmenüs zum Starten von WSL [GH 437, 603, 1836].</span><span class="sxs-lookup"><span data-stu-id="7a11e-444">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="7a11e-445">Halten Sie in einem Explorer-Fenster die UMSCHALTTASTE gedrückt, und klicken Sie mit der rechten Maustaste, um diese Option zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-445">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="7a11e-446">Korrektur des nicht blockierenden UNIX-Socketverhaltens [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="7a11e-446">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="7a11e-447">Korrigieren des hängenden NETLINK-Befehls, wie in GH 2026 gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-447">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="7a11e-448">Hinzufügen von Unterstützung für Einbindungsweitergabeflags [GH 2911]</span><span class="sxs-lookup"><span data-stu-id="7a11e-448">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="7a11e-449">Korrektur von Problem mit truncate, das keine inotify-Ereignisse verursacht [GH 2978].</span><span class="sxs-lookup"><span data-stu-id="7a11e-449">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="7a11e-450">Hinzufügen der Option --exec für „wsl.exe“ zum Aufrufen eine einzelne Binärdatei ohne Shell.</span><span class="sxs-lookup"><span data-stu-id="7a11e-450">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="7a11e-451">Hinzufügen der Option --distribution für „wsl.exe“, um eine bestimmte Distribution auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-451">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="7a11e-452">Build 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="7a11e-452">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="7a11e-453">Allgemeine Windows-Informationen zu Build 17655 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-453">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-454">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-454">WSL</span></span>
* <span data-ttu-id="7a11e-455">Eingeschränkte Unterstützung für dmesg.</span><span class="sxs-lookup"><span data-stu-id="7a11e-455">Limited support for dmesg.</span></span> <span data-ttu-id="7a11e-456">Anwendungen können sich jetzt in dmesg protokollieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-456">Applications can now log to dmesg.</span></span> <span data-ttu-id="7a11e-457">Der WSL-Treiber protokolliert eingeschränkte Informationen in dmesg.</span><span class="sxs-lookup"><span data-stu-id="7a11e-457">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="7a11e-458">In Zukunft kann dies so erweitert werden, dass andere Informationen/Diagnoseinhalte vom Treiber erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-458">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="7a11e-459">Hinweis: dmesg wird derzeit über die `/dev/kmsg`-Geräteschnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-459">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="7a11e-460">`syslog`-Systemaufrufschnittstelle wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-460">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="7a11e-461">Daher funktionieren einige der `dmesg`-Befehlszeilenoptionen (z.B. `-S`, `-C`) nicht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-461">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="7a11e-462">Korrektur eines Problems, bei dem Multithreadingvorgänge ENOENT zurückgeben konnten, obwohl die Datei vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-462">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="7a11e-463">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="7a11e-463">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="7a11e-464">Build 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="7a11e-464">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="7a11e-465">Allgemeine Windows-Informationen zu Build 17639 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-465">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-466">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-466">WSL</span></span>
* <span data-ttu-id="7a11e-467">Änderung der Standard-GID und des Modus von seriellen Geräten entsprechend den nativen Einstellungen [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="7a11e-467">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="7a11e-468">DrvFs unterstützt jetzt erweiterte Attribute.</span><span class="sxs-lookup"><span data-stu-id="7a11e-468">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="7a11e-469">Hinweis: Für DrvFs gelten einige Einschränkungen für den Namen erweiterter Attribute.</span><span class="sxs-lookup"><span data-stu-id="7a11e-469">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="7a11e-470">Insbesondere sind einige Zeichen (etwa „/“, „:“ und „\*“) unzulässig, und für Namen erweiterter Attribute wird in DrvFs keine Groß- und Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-470">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="7a11e-471">Build 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="7a11e-471">Build 17133 (Fast)</span></span>
<span data-ttu-id="7a11e-472">Allgemeine Windows-Informationen zu Build 17133 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-472">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-473">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-473">WSL</span></span>
* <span data-ttu-id="7a11e-474">Fehlerbehebung für Hängen in WSL.</span><span class="sxs-lookup"><span data-stu-id="7a11e-474">Fix for hang in WSL.</span></span> <span data-ttu-id="7a11e-475">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="7a11e-475">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="7a11e-476">Build 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="7a11e-476">Build 17128 (Fast)</span></span>
<span data-ttu-id="7a11e-477">Allgemeine Windows-Informationen zu Build 17128 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-477">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-478">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-478">WSL</span></span>
* <span data-ttu-id="7a11e-479">Keine</span><span class="sxs-lookup"><span data-stu-id="7a11e-479">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="7a11e-480">Build 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="7a11e-480">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="7a11e-481">Allgemeine Windows-Informationen zu Build 17627 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-481">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-482">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-482">WSL</span></span>
* <span data-ttu-id="7a11e-483">Hinzufügen von Unterstützung für futex-pi-fähige Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="7a11e-483">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="7a11e-484">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="7a11e-484">[GH 1006]</span></span>
    * <span data-ttu-id="7a11e-485">Beachten Sie, dass Prioritäten derzeit keine unterstützte WSL-Funktion sind, sodass Einschränkungen bestehen. Die Standardverwenund sollte jedoch aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-485">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="7a11e-486">Windows-Firewallunterstützung für WSL-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="7a11e-486">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="7a11e-487">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="7a11e-487">[GH 1852]</span></span>
    * <span data-ttu-id="7a11e-488">Um beispielsweise zuzulassen, dass der WSL python-Prozess an einem beliebigen Port lauschen kann, verwenden Sie Windows-CMD mit erhöhten Rechten: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="7a11e-488">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="7a11e-489">Weitere Informationen zum Hinzufügen von Firewallregeln finden Sie unter [Link.](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="7a11e-489">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="7a11e-490">Beachten der Standardshell des Benutzers bei der Verwendung von „wsl.exe“.</span><span class="sxs-lookup"><span data-stu-id="7a11e-490">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="7a11e-491">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="7a11e-491">[GH 2372]</span></span>
* <span data-ttu-id="7a11e-492">Melden aller Netzwerkschnittstellen als Ethernet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-492">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="7a11e-493">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="7a11e-493">[GH 2996]</span></span>
* <span data-ttu-id="7a11e-494">Bessere Verarbeitung von beschädigten /etc/passwd-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7a11e-494">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="7a11e-495">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="7a11e-495">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-496">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-496">Console</span></span>
* <span data-ttu-id="7a11e-497">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-498">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-498">LTP Results:</span></span>
<span data-ttu-id="7a11e-499">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-499">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="7a11e-500">Build 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="7a11e-500">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="7a11e-501">Allgemeine Windows-Informationen zu Build 17618 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-501">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-502">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-502">WSL</span></span>
* <span data-ttu-id="7a11e-503">Einführung in Pseudoconsolenfunktionalität für NT-Interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span><span class="sxs-lookup"><span data-stu-id="7a11e-503">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="7a11e-504">Der Legacyinstallationsmechanismus („lxrun.exe“) ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-504">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="7a11e-505">Der unterstützte Mechanismus zum Installieren von Distributionen ist der Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="7a11e-505">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-506">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-506">Console</span></span>
* <span data-ttu-id="7a11e-507">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-507">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-508">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-508">LTP Results:</span></span>
<span data-ttu-id="7a11e-509">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-509">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="7a11e-510">Build 17110</span><span class="sxs-lookup"><span data-stu-id="7a11e-510">Build 17110</span></span>
<span data-ttu-id="7a11e-511">Allgemeine Windows-Informationen zu Build 17110 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-511">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-512">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-512">WSL</span></span>
* <span data-ttu-id="7a11e-513">Zulassen, dass /init aus Windows beendet wird [GH 2928].</span><span class="sxs-lookup"><span data-stu-id="7a11e-513">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="7a11e-514">DrvFs verwendet nun standardmäßig Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis (entspricht der Einbindungsoption „case=dir“).</span><span class="sxs-lookup"><span data-stu-id="7a11e-514">DrvFs now uses per-directory case sensitivity by default (equivalent to the "case=dir" mount option).</span></span>
    * <span data-ttu-id="7a11e-515">Wenn Sie „case=force“ verwenden (das alte Verhalten), muss ein Registrierungsschlüssel festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-515">Using "case=force" (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="7a11e-516">Führen Sie den folgenden Befehl aus, um „case=force“ zu aktivieren, wenn Sie diese Option verwenden müssen: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="7a11e-516">Run the following command to enable "case=force" if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="7a11e-517">Wenn Sie über vorhandene Verzeichnisse verfügen, die mit WSL in einer älteren Version von Windows erstellt wurden, bei denen die Groß-/Kleinschreibung beachtet werden muss, verwenden Sie „fsutil.exe“, um sie für Unterscheidung von Groß-/Kleinschreibung zu markieren: fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="7a11e-517">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="7a11e-518">NULL-Beendigungszeichenfolgen werden vom uname-Systemaufruf zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-518">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-519">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-519">Console</span></span>
* <span data-ttu-id="7a11e-520">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-520">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-521">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-521">LTP Results:</span></span>
<span data-ttu-id="7a11e-522">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-522">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="7a11e-523">Build 17107</span><span class="sxs-lookup"><span data-stu-id="7a11e-523">Build 17107</span></span>
<span data-ttu-id="7a11e-524">Allgemeine Windows-Informationen zu Build 17107 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-524">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-525">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-525">WSL</span></span>
* <span data-ttu-id="7a11e-526">Unterstützung von TCSETSF und TCSETSW für pty-Masterendpunkte [GH 2552].</span><span class="sxs-lookup"><span data-stu-id="7a11e-526">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="7a11e-527">Starten von gleichzeitigen Interop-Prozessen kann zu EINVAL führen [GH 2813].</span><span class="sxs-lookup"><span data-stu-id="7a11e-527">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="7a11e-528">Korrektur von PTRACE_ATTACH, um den richtigen Ablaufverfolgungsstatus in „/proc/pid/status“ anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-528">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="7a11e-529">Korrektur der Racebedingung, bei der kurzlebige Prozesse, die mit den CLEARTID- und SETTID-Flags geklont wurden, ohne Löschen der TID-Adresse beendet werden konnten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-529">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="7a11e-530">Anzeigen einer Meldung beim Aktualisieren der Linux-Dateisystemverzeichnisse beim Umstieg von einem Build vor 17093.</span><span class="sxs-lookup"><span data-stu-id="7a11e-530">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="7a11e-531">Weitere Informationen zu den Änderungen für das 17093-Dateisystem finden Sie in den Anmerkungen zur Version für [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span><span class="sxs-lookup"><span data-stu-id="7a11e-531">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-532">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-532">Console</span></span>
* <span data-ttu-id="7a11e-533">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-533">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-534">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-534">LTP Results:</span></span>
<span data-ttu-id="7a11e-535">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-535">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="7a11e-536">Build 17101</span><span class="sxs-lookup"><span data-stu-id="7a11e-536">Build 17101</span></span>
<span data-ttu-id="7a11e-537">Allgemeine Windows-Informationen zu Build 17101 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-537">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-538">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-538">WSL</span></span>
* <span data-ttu-id="7a11e-539">Unterstützung für signalfd.</span><span class="sxs-lookup"><span data-stu-id="7a11e-539">Support for signalfd.</span></span> <span data-ttu-id="7a11e-540">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="7a11e-540">[GH 129]</span></span>
* <span data-ttu-id="7a11e-541">Unterstützung von Dateinamen, die ungültige NTFS-Zeichen enthalten, durch Codieren als private Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-541">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="7a11e-542">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="7a11e-542">[GH 1514]</span></span>
* <span data-ttu-id="7a11e-543">Automatisches Einbinden greift auf den schreibgeschützten Modus zurück, wenn Schreibvorgänge nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-543">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="7a11e-544">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="7a11e-544">[GH 2603]</span></span>
* <span data-ttu-id="7a11e-545">Ermöglichen des Einfügens von Unicode-Ersatzzeichenpaaren (z.B. Emojis).</span><span class="sxs-lookup"><span data-stu-id="7a11e-545">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="7a11e-546">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="7a11e-546">[GH 2765]</span></span>
* <span data-ttu-id="7a11e-547">Pseudodateien in „/proc“ und „/sys“ sollten „read“ und „write ready“ aus select, poll, epoll, usw. zurückgeben [GH 2838].</span><span class="sxs-lookup"><span data-stu-id="7a11e-547">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="7a11e-548">Korrektur eines Problems, das dazu führen kann, dass der Dienst in eine Endlosschleife übergeht, wenn die Registrierung manipuliert wurde oder beschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-548">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="7a11e-549">Korrektur von Netlink-Nachrichten, sodass sie mit neueren Versionen von iproute2 (upstream 4.14) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-549">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-550">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-550">Console</span></span>
* <span data-ttu-id="7a11e-551">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-551">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-552">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-552">LTP Results:</span></span>
<span data-ttu-id="7a11e-553">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-553">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="7a11e-554">Build 17093</span><span class="sxs-lookup"><span data-stu-id="7a11e-554">Build 17093</span></span>
<span data-ttu-id="7a11e-555">Allgemeine Windows-Informationen zu Build 17093 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-555">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="7a11e-556">Wichtig:</span><span class="sxs-lookup"><span data-stu-id="7a11e-556">Important:</span></span>
<span data-ttu-id="7a11e-557">Wenn Sie WSL zum ersten Mal nach dem Upgrade auf diesen Build starten, müssen Sie einige Aufgaben durchführen, um die Linux-Dateisystemverzeichnisse zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-557">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="7a11e-558">Dieser Vorgang kann einige Minuten in Anspruch nehmen, sodass WSL möglicherweise langsam zu starten scheint.</span><span class="sxs-lookup"><span data-stu-id="7a11e-558">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="7a11e-559">Dies sollte nur ein Mal für jede Distribution erfolgen, die Sie aus dem Store installiert haben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-559">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="7a11e-560">Verbesserte Unterscheidung von Groß-/Kleinschreibung in DrvFs.</span><span class="sxs-lookup"><span data-stu-id="7a11e-560">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="7a11e-561">DrvFs unterstützt jetzt Berücksichtigung von Groß-/Kleinschreibung pro Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7a11e-561">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="7a11e-562">Dies ist ein neues Flag, das für Verzeichnisse festgelegt werden kann, um anzugeben, dass alle Vorgänge in diesen Verzeichnissen mit Unterscheidung zwischen Groß-/Kleinschreibung behandelt werden sollen, sodass sogar Windows-Anwendungen Dateien ordnungsgemäß öffnen können, bei denen sich nur die Groß-/Kleinschreibung unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-562">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="7a11e-563">DrvFs verfügt über neue Einbindungsoptionen, die die Berücksichtigung von Groß-/Kleinschreibung pro Verzeichnis steuern.</span><span class="sxs-lookup"><span data-stu-id="7a11e-563">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="7a11e-564">case=force: Für alle Verzeichnisse wird zwischen Groß-/Kleinschreibung unterschieden (mit Ausnahme des Laufwerkstamms).</span><span class="sxs-lookup"><span data-stu-id="7a11e-564">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="7a11e-565">Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-565">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="7a11e-566">Dies ist das Legacyverhalten (ausgenommen, wenn neue Verzeichnisse für Unterscheidung zwischen Groß-/Kleinschreibung markiert werden).</span><span class="sxs-lookup"><span data-stu-id="7a11e-566">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="7a11e-567">case=dir: Nur für Verzeichnisse mit dem Flag für Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis wird Groß-/Kleinschreibung beachtet, für alle anderen Verzeichnisse nicht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-567">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="7a11e-568">Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-568">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="7a11e-569">case=dir: Nur für Verzeichnisse mit dem Flag für Unterscheidung zwischen Groß-/Kleinschreibung pro Verzeichnis wird Groß-/Kleinschreibung beachtet, für alle anderen Verzeichnisse nicht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-569">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="7a11e-570">Für neue Verzeichnisse, die mit WSL erstellt werden, wird Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-570">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="7a11e-571">Hinweis: Für Verzeichnisse, die in früheren Versionen von WSL erstellt wurden, ist dieses Flag nicht festgelegt, sodass bei Verwendung der Option „case=dir“ keine Groß-/Kleinschreibung beachtet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-571">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the "case=dir" option.</span></span> <span data-ttu-id="7a11e-572">Eine Möglichkeit, dieses Flag für vorhandene Verzeichnisse festzulegen, ist in Kürze verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a11e-572">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="7a11e-573">Beispiel für die Einbindung mit diesen Optionen (für vorhandene Laufwerke müssen Sie zuerst die Einbindung aufheben, bevor Sie die Einbindung mit anderen Optionen ausführen können): sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="7a11e-573">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="7a11e-574">Momentan ist case=force immer noch die Standardoption.</span><span class="sxs-lookup"><span data-stu-id="7a11e-574">For now, case=force is still the default option.</span></span> <span data-ttu-id="7a11e-575">Dies wird in Zukunft in case=dir geändert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-575">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="7a11e-576">Sie können jetzt Schrägstriche in Windows-Pfaden verwenden, wenn Sie DrvFs einbinden, z.B. sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="7a11e-576">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="7a11e-577">WSL verarbeitet nun die /etc/fstab-Datei während des Instanzstarts [GH 2636].</span><span class="sxs-lookup"><span data-stu-id="7a11e-577">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="7a11e-578">Dies erfolgt vor der automatischen Einbindung von DrvFs-Laufwerken. Alle Laufwerke, die bereits von fstab eingebunden wurden, werden nicht automatisch erneut eingebunden, sodass Sie den Einbindungspunkt für bestimmte Laufwerke ändern können.</span><span class="sxs-lookup"><span data-stu-id="7a11e-578">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="7a11e-579">Dieses Verhalten kann mithilfe von „wsl.conf“ deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-579">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="7a11e-580">Die mount, mountinfo- und mountstats-Dateien in „/proc“ versehen Sonderzeichen wie umgekehrte Schrägstriche und Leerzeichen ordnungsgemäß mit Escapezeichen [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="7a11e-580">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="7a11e-581">Spezielle Dateien, die mit DrvFs erstellt werden (z.B. symbolische WSL-Verknüpfungen oder Fifos und Sockets, wenn Metadaten aktiviert sind), können nun aus Windows kopiert und verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-581">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="7a11e-582">WSL ist mit „wsl.conf“ besser konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="7a11e-582">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="7a11e-583">Es wurde eine Methode zum automatischen Konfigurieren bestimmter Funktionen in WSL hinzugefügt, die jedes Mal angewendet wird, wenn Sie das Subsystem starten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-583">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="7a11e-584">Dies umfasst Optionen für die automatische Einbindung und Netzwerkkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="7a11e-584">This includes automount options and network configuration.</span></span> <span data-ttu-id="7a11e-585">Weitere Informationen hierzu finden Sie in unserem Blogbeitrag unter: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="7a11e-585">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="7a11e-586">AF_UNIX ermöglicht Socketverbindungen zwischen Linux-Prozessen für WSL- und native Windows-Prozesse.</span><span class="sxs-lookup"><span data-stu-id="7a11e-586">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="7a11e-587">WSL- und Windows-Anwendungen können nun über Unix-Sockets miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-587">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="7a11e-588">Stellen Sie sich vor, Sie möchten einen Dienst in Windows ausführen und sowohl für Windows- als auch für WSL-Apps verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-588">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="7a11e-589">Das ist nun mit UNIX-Sockets möglich.</span><span class="sxs-lookup"><span data-stu-id="7a11e-589">Now, that's possible with Unix sockets.</span></span> <span data-ttu-id="7a11e-590">Weitere Informationen finden Sie in unserem Blogbeitrag unter https://aka.ms/afunixinterop.</span><span class="sxs-lookup"><span data-stu-id="7a11e-590">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-591">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-591">WSL</span></span>
* <span data-ttu-id="7a11e-592">Unterstützung von mmap() mit MAP_NORESERVE [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="7a11e-592">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="7a11e-593">Unterstützung von CLONE_PTRACE und CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="7a11e-593">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="7a11e-594">Verarbeiten eines Nicht-SIGCHLD-Beendigungssignals im Klon [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="7a11e-594">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="7a11e-595">Stub für /proc/sys/fs/inotify/max_user_instances und /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="7a11e-595">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="7a11e-596">Fehler beim Laden von ELF-Binärdateien, die Ladeheader mit Offsets ungleich NULL enthalten [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="7a11e-596">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="7a11e-597">Eliminieren von nachfolgenden Seitenbytes beim Laden von Images.</span><span class="sxs-lookup"><span data-stu-id="7a11e-597">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="7a11e-598">Verringern der Fälle, in denen execve den Prozess automatisch beendet</span><span class="sxs-lookup"><span data-stu-id="7a11e-598">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-599">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-599">Console</span></span>
* <span data-ttu-id="7a11e-600">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-600">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-601">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-601">LTP Results:</span></span>
<span data-ttu-id="7a11e-602">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-602">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="7a11e-603">Build 17083</span><span class="sxs-lookup"><span data-stu-id="7a11e-603">Build 17083</span></span>
<span data-ttu-id="7a11e-604">Allgemeine Windows-Informationen zu Build 17083 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-604">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-605">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-605">WSL</span></span>
* <span data-ttu-id="7a11e-606">Korrektur der Fehlerüberprüfung für epoll [GH 2798, 2801, 2857]</span><span class="sxs-lookup"><span data-stu-id="7a11e-606">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="7a11e-607">Korrektur von Hängern beim Deaktivieren von ASLR [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="7a11e-607">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="7a11e-608">Sicherstellen, dass mmap-Vorgänge atomarisch erscheinen [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="7a11e-608">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-609">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-609">Console</span></span>
* <span data-ttu-id="7a11e-610">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-610">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-611">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-611">LTP Results:</span></span>
<span data-ttu-id="7a11e-612">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-612">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="7a11e-613">Build 17074</span><span class="sxs-lookup"><span data-stu-id="7a11e-613">Build 17074</span></span>
<span data-ttu-id="7a11e-614">Allgemeine Windows-Informationen zu Build 17074 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-614">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-615">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-615">WSL</span></span>
* <span data-ttu-id="7a11e-616">Festes Speicherformat von DrvFs-Metadaten [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="7a11e-616">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="7a11e-617">**Wichtig:** Die vor diesem Build erstellten DrvFs-Metadaten werden falsch oder überhaupt nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-617">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="7a11e-618">Um betroffene Dateien zu korrigieren, verwenden Sie chmod und chown zum erneuten Anwenden der Metadaten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-618">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="7a11e-619">Korrektur eines Problems mit mehreren Signalen und neu startbaren Systemaufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-619">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-620">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-620">Console</span></span>
* <span data-ttu-id="7a11e-621">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-621">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-622">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-622">LTP Results:</span></span>
<span data-ttu-id="7a11e-623">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-623">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="7a11e-624">Build 17063</span><span class="sxs-lookup"><span data-stu-id="7a11e-624">Build 17063</span></span>
<span data-ttu-id="7a11e-625">Allgemeine Windows-Informationen zu Build 17063 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-625">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="7a11e-626">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-626">WSL</span></span>
* <span data-ttu-id="7a11e-627">DrvFs unterstützt zusätzliche Linux-Metadaten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-627">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="7a11e-628">Dies ermöglicht das Festlegen des Besitzers und des Dateimodus mit chmod/chown sowie das Erstellen spezieller Dateien, etwa Fifos, Unix-Sockets und Gerätedateien.</span><span class="sxs-lookup"><span data-stu-id="7a11e-628">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="7a11e-629">Diese Option ist zurzeit standardmäßig deaktiviert, da Sie noch experimentell ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-629">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="7a11e-630">**Hinweis:**  Wir haben einen Fehler im Metadatenformat behoben, das von DrvFs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-630">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="7a11e-631">Obwohl Metadaten in diesem Build für Experimente funktionieren, lesen zukünftige Builds die von diesem Build erstellten Metadaten nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="7a11e-631">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="7a11e-632">Möglicherweise müssen Sie den Besitzer für geänderte Dateien manuell aktualisieren, und Geräte mit einer benutzerdefinierten Geräte-ID müssen neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-632">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="7a11e-633">Um diese Funktion zu aktivieren, binden Sie DrvFs mit der Metadatenoption ein (um sie für eine vorhandene Einbindung zu aktivieren, müssen Sie die Einbindung zunächst aufheben):</span><span class="sxs-lookup"><span data-stu-id="7a11e-633">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="7a11e-634">Linux-Berechtigungen werden der Datei als zusätzliche Metadaten hinzugefügt. Sie wirken sich nicht auf die Windows-Berechtigungen aus.</span><span class="sxs-lookup"><span data-stu-id="7a11e-634">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="7a11e-635">Beachten Sie, dass beim Bearbeiten einer Datei mithilfe eines Windows-Editors die Metadaten möglicherweise entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-635">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="7a11e-636">In diesem Fall wird die Datei auf die Standardberechtigungen zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-636">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="7a11e-637">Hinzufügen von Einbindungsoptionen zu DrvFs, um Dateien ohne Metadaten zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7a11e-637">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="7a11e-638">uid: die Benutzer-ID, die für den Besitzer aller Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-638">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="7a11e-639">gid: die Gruppen-ID, die für den Besitzer aller Dateien verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-639">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="7a11e-640">umask: Eine oktale Maske mit Berechtigungen, die für alle Dateien und Verzeichnisse ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-640">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="7a11e-641">fmask: Eine oktale Maske mit Berechtigungen, die für alle regulären Dateien ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-641">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="7a11e-642">dmask: Eine oktale Maske mit Berechtigungen, die für alle Verzeichnisse ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-642">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="7a11e-643">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7a11e-643">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="7a11e-644">Kombinieren Sie dies mit der Metadatenoption, um Standardberechtigungen für Dateien ohne Metadaten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-644">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="7a11e-645">Wird in einer neuen Umgebungsvariablen (`WSLENV`) eingeführt, um zu konfigurieren, wie Umgebungsvariablen zwischen WSL und Win32 ausgetauscht werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-645">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="7a11e-646">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7a11e-646">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="7a11e-647">`WSLENV` eine durch Doppelpunkte getrennte Liste von Umgebungsvariablen, die beim Starten von WSL-Prozessen aus Win32 oder Win32-Prozessen aus WSL eingeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="7a11e-647">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="7a11e-648">Jeder Variablen kann ein Schrägstrich als Suffix vorangestellt werden, gefolgt von Flags, um anzugeben, wie sie übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a11e-648">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="7a11e-649">p: Der Wert ist ein Pfad, der zwischen WSL-Pfaden und Win32-Pfaden übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7a11e-649">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="7a11e-650">l: Der Wert ist eine Liste von Pfaden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-650">l: The value is a list of paths.</span></span> <span data-ttu-id="7a11e-651">In WSL ist es eine durch Doppelpunkte getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="7a11e-651">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="7a11e-652">In Win32 ist es eine durch Semikolons getrennte Liste.</span><span class="sxs-lookup"><span data-stu-id="7a11e-652">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="7a11e-653">u: Der Wert sollte nur beim Aufrufen von WSL aus Win32 eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-653">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="7a11e-654">w: Der Wert sollte nur beim Aufrufen von Win32 aus WSL eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-654">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="7a11e-655">Sie können `WSLENV` in der BASHRC-Datei oder in der benutzerdefinierten Windows-Umgebung für Ihren Benutzer festlegen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-655">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="7a11e-656">drvfs wird ordnungsgemäß eingebunden und behält Zeitstempel aus from tar, cp -p bei (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="7a11e-656">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="7a11e-657">Symbolische drvfs-Verknüpfungen geben die richtige Größe an (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="7a11e-657">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="7a11e-658">Lese-/Schreibvorgänge funktionieren für sehr große E/A-Größen (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="7a11e-658">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="7a11e-659">waitpid funktioniert mit Prozessgruppen-IDs (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="7a11e-659">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="7a11e-660">Erheblich verbesserte mmap-Leistung für große reserve-Regionen, Verbesserung der ghc-Leistung (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="7a11e-660">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="7a11e-661">personality unterstützt READ_IMPLIES_EXEC, Korrekturen maxima und clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="7a11e-661">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="7a11e-662">mprotect unterstützt PROT_GROWSDOWN,;Korrekturen clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="7a11e-662">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="7a11e-663">Seitenfehlerkorrekturen im Overcommitmodus, Korrekturen sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="7a11e-663">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="7a11e-664">clone unterstützt weitere Flagkombinationen</span><span class="sxs-lookup"><span data-stu-id="7a11e-664">clone supports more flags combinations</span></span>
* <span data-ttu-id="7a11e-665">Unterstützung von select/epoll von epoll-Dateien (zuvor eine Nulloperation).</span><span class="sxs-lookup"><span data-stu-id="7a11e-665">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="7a11e-666">Benachrichtigen von ptrace über nicht implementierte Systemaufrufe.</span><span class="sxs-lookup"><span data-stu-id="7a11e-666">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="7a11e-667">Ignorieren von Schnittstellen, die nicht aktiv sind, beim Generieren von resolv.conf-Namenservern [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="7a11e-667">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="7a11e-668">Aufzählen von Netzwerkschnittstellen ohne physische Adresse.</span><span class="sxs-lookup"><span data-stu-id="7a11e-668">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="7a11e-669">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="7a11e-669">[GH 2685]</span></span>
* <span data-ttu-id="7a11e-670">Zusätzliche Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-670">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="7a11e-671">Linux-Tools für Entwickler unter Windows verfügbar</span><span class="sxs-lookup"><span data-stu-id="7a11e-671">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="7a11e-672">Windows-Befehlszeilen-Toolkette enthält bsdtar (tar) und curl.</span><span class="sxs-lookup"><span data-stu-id="7a11e-672">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="7a11e-673">Lesen Sie [diesen Blog](https://aka.ms/tarcurlwindows), um mehr über das Hinzufügen dieser beiden neuen Tools zu erfahren, und sehen Sie, wie Sie das Entwicklererlebnis unter Windows formen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-673">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they're shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="7a11e-674">`AF_UNIX` ist im Windows Insider SDK (17061 und höher) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a11e-674">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="7a11e-675">Lesen Sie [diesen Blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), um weitere Informationen zu `AF_UNIX` zu erhalten und mehr über die Verwendung in Windows durch Entwickler zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-675">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="7a11e-676">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-676">Console</span></span>
* <span data-ttu-id="7a11e-677">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-677">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-678">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-678">LTP Results:</span></span>
<span data-ttu-id="7a11e-679">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-679">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="7a11e-680">Build 17046</span><span class="sxs-lookup"><span data-stu-id="7a11e-680">Build 17046</span></span>

<span data-ttu-id="7a11e-681">Allgemeine Windows-Informationen zu Build 17046 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span><span class="sxs-lookup"><span data-stu-id="7a11e-681">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="7a11e-682">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-682">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-683">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-683">WSL</span></span>
- <span data-ttu-id="7a11e-684">Ermöglicht das Ausführen von Prozessen ohne ein aktives Terminal.</span><span class="sxs-lookup"><span data-stu-id="7a11e-684">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="7a11e-685">[GH 709, 1007, 1511, 2252, 2391 usw.]</span><span class="sxs-lookup"><span data-stu-id="7a11e-685">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="7a11e-686">Bessere Unterstützung von CLONE_VFORK und CLONE_VM.</span><span class="sxs-lookup"><span data-stu-id="7a11e-686">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="7a11e-687">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="7a11e-687">[GH 1878, 2615]</span></span>
- <span data-ttu-id="7a11e-688">Überspringen der TDI-Filtertreiber für WSL-Netzwerkvorgänge.</span><span class="sxs-lookup"><span data-stu-id="7a11e-688">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="7a11e-689">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="7a11e-689">[GH 1554]</span></span>
- <span data-ttu-id="7a11e-690">DrvFs erstellt symbolische NT-Verknüpfungen, wenn bestimmte Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="7a11e-690">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="7a11e-691">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="7a11e-691">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="7a11e-692">Das Verknüpfungsziel muss relativ sein, darf keine Einbindungspunkte oder symbolische Verknüpfungen kreuzen und muss vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7a11e-692">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="7a11e-693">Der Benutzer muss über SE_CREATE_SYMBOLIC_LINK_PRIVILEGE verfügen (dies erfordert normalerweise, dass Sie „wsl.exe“ mit erhöhten Rechten starten), sofern der Entwicklermodus nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-693">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="7a11e-694">Unter allen anderen Umständen erstellt DrvFs weiterhin symbolische WSL-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-694">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="7a11e-695">Ermöglichen der gleichzeitigen Ausführung von WSL-Instanzen mit und ohne erhöhten Rechten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-695">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="7a11e-696">Unterstützung von /proc/sys/kernel/Yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="7a11e-696">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="7a11e-697">Hinzufügen von wslpath zum Durchführen von Konvertierungen von WSL-<- >Windows-Pfaden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-697">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="7a11e-698">[GH 522, 1243, 1834, 2327 usw.]</span><span class="sxs-lookup"><span data-stu-id="7a11e-698">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with '/' instead of '\\'

      EX: wslpath 'c:\users'
  ```
  #### <a name="console"></a><span data-ttu-id="7a11e-699">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-699">Console</span></span>
- <span data-ttu-id="7a11e-700">Keine Korrekturen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-700">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-701">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-701">LTP Results:</span></span>
<span data-ttu-id="7a11e-702">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-702">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="7a11e-703">Build 17040</span><span class="sxs-lookup"><span data-stu-id="7a11e-703">Build 17040</span></span>

<span data-ttu-id="7a11e-704">Allgemeine Windows-Informationen zu Build 17040 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span><span class="sxs-lookup"><span data-stu-id="7a11e-704">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-705">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-705">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-706">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-706">WSL</span></span>
- <span data-ttu-id="7a11e-707">Keine Korrekturen seit 17035.</span><span class="sxs-lookup"><span data-stu-id="7a11e-707">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-708">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-708">Console</span></span>
- <span data-ttu-id="7a11e-709">Keine Korrekturen seit 17035.</span><span class="sxs-lookup"><span data-stu-id="7a11e-709">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-710">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-710">LTP Results:</span></span>
<span data-ttu-id="7a11e-711">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-711">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="7a11e-712">Build 17035</span><span class="sxs-lookup"><span data-stu-id="7a11e-712">Build 17035</span></span>

<span data-ttu-id="7a11e-713">Allgemeine Windows-Informationen zu Build 17035 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span><span class="sxs-lookup"><span data-stu-id="7a11e-713">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-714">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-714">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-715">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-715">WSL</span></span>
- <span data-ttu-id="7a11e-716">Der Zugriff auf Dateien auf DrvFs kann gelegentlich mit EINVAL fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-716">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="7a11e-717">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="7a11e-717">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-718">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-718">Console</span></span>
- <span data-ttu-id="7a11e-719">Farbverlust beim Einfügen/Löschen von Zeilen im VT-Modus.</span><span class="sxs-lookup"><span data-stu-id="7a11e-719">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-720">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-720">LTP Results:</span></span>
<span data-ttu-id="7a11e-721">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-721">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="7a11e-722">Build 17025</span><span class="sxs-lookup"><span data-stu-id="7a11e-722">Build 17025</span></span>

<span data-ttu-id="7a11e-723">Allgemeine Windows-Informationen zu Build 17025 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span><span class="sxs-lookup"><span data-stu-id="7a11e-723">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-724">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-724">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-725">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-725">WSL</span></span>
- <span data-ttu-id="7a11e-726">Starten anfänglicher Prozesse in einer neuen Vordergrundprozessgruppe [GH 1653, 2510].</span><span class="sxs-lookup"><span data-stu-id="7a11e-726">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="7a11e-727">Korrekturen der SIGHUP-Übermittlung [GH 2496].</span><span class="sxs-lookup"><span data-stu-id="7a11e-727">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="7a11e-728">Generieren eines Standardnamens für virtuelle Bridge generieren, wenn keine Angabe erfolgt [GH 2497].</span><span class="sxs-lookup"><span data-stu-id="7a11e-728">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="7a11e-729">Implementieren von /proc/sys/kernel/Random/boot_id [GH 2518].</span><span class="sxs-lookup"><span data-stu-id="7a11e-729">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="7a11e-730">Weitere Interop-Pipekorrekturen für stdout/stderr.</span><span class="sxs-lookup"><span data-stu-id="7a11e-730">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="7a11e-731">Stub für syncfs-Systemaufruf.</span><span class="sxs-lookup"><span data-stu-id="7a11e-731">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-732">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-732">Console</span></span>
- <span data-ttu-id="7a11e-733">Korrektur der VT-Eingabeübersetzung für Drittanbieterkonsolen [GH 111]</span><span class="sxs-lookup"><span data-stu-id="7a11e-733">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-734">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-734">LTP Results:</span></span>
<span data-ttu-id="7a11e-735">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-735">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="7a11e-736">Build 17017</span><span class="sxs-lookup"><span data-stu-id="7a11e-736">Build 17017</span></span>

<span data-ttu-id="7a11e-737">Allgemeine Windows-Informationen zu Build 17017 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span><span class="sxs-lookup"><span data-stu-id="7a11e-737">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-738">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-738">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-739">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-739">WSL</span></span>
- <span data-ttu-id="7a11e-740">Ignorieren leerer ELF-Programmheader [GH 330].</span><span class="sxs-lookup"><span data-stu-id="7a11e-740">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="7a11e-741">Ermöglichen, dass LxssManager WSL-Instanzen für nicht interaktive Benutzer erstellt (Unterstützung für SSH und geplante Aufgaben) [GH 777, 1602].</span><span class="sxs-lookup"><span data-stu-id="7a11e-741">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="7a11e-742">Unterstützung von WSL->Win32->WSL-Szenarien („Inception“) [GH 1228].</span><span class="sxs-lookup"><span data-stu-id="7a11e-742">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="7a11e-743">Eingeschränkte Unterstützung für das Beenden von Konsolen-Apps, die über Interop aufgerufen wurden [GH 1614].</span><span class="sxs-lookup"><span data-stu-id="7a11e-743">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="7a11e-744">Unterstützung von Einbindungsoptionen für devpts [GH 1948].</span><span class="sxs-lookup"><span data-stu-id="7a11e-744">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="7a11e-745">Ptrace blockiert den Start untergeordneter Prozesse [GH 2333].</span><span class="sxs-lookup"><span data-stu-id="7a11e-745">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="7a11e-746">EPOLLET fehlen einige Ereignisse [GH 2462].</span><span class="sxs-lookup"><span data-stu-id="7a11e-746">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="7a11e-747">Rückgabe einer größeren Anzahl von Daten für PTRACE_GETSIGINFO.</span><span class="sxs-lookup"><span data-stu-id="7a11e-747">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="7a11e-748">Getdents mit lseek liefert falsche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="7a11e-748">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="7a11e-749">Korrektur einiger Hänger von Win32-Interop-Apps, die auf Eingaben in einer Pipe warten, die keine weiteren Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="7a11e-749">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="7a11e-750">O_ASYNC-Unterstützung für tty/pty-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7a11e-750">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="7a11e-751">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-751">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-752">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-752">Console</span></span>
- <span data-ttu-id="7a11e-753">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-753">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-754">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-754">LTP Results:</span></span>
<span data-ttu-id="7a11e-755">Tests werden zurzeit ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-755">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="7a11e-756">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="7a11e-756">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="7a11e-757">Build 16288</span><span class="sxs-lookup"><span data-stu-id="7a11e-757">Build 16288</span></span>

<span data-ttu-id="7a11e-758">Allgemeine Windows-Informationen zu Build 16288 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-758">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-759">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-759">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-760">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-760">WSL</span></span>
- <span data-ttu-id="7a11e-761">Ordnungsgemäße Initialisierung und Meldung von uid, gid und Modus für Socketdateideskriptoren [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="7a11e-761">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="7a11e-762">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-762">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-763">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-763">Console</span></span>
- <span data-ttu-id="7a11e-764">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-764">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-765">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-765">LTP Results:</span></span>
<span data-ttu-id="7a11e-766">Keine Änderung seit 16273</span><span class="sxs-lookup"><span data-stu-id="7a11e-766">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="7a11e-767">Build 16278</span><span class="sxs-lookup"><span data-stu-id="7a11e-767">Build 16278</span></span>

<span data-ttu-id="7a11e-768">Allgemeine Windows-Informationen zu Build 162738 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-768">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-769">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-769">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-770">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-770">WSL</span></span>
- <span data-ttu-id="7a11e-771">Explizite Aufhebung der Zuordnung zugeordneter Ansichten von dateigestützten Abschnitten beim Beenden des LX MM-Status [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="7a11e-771">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="7a11e-772">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-772">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-773">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-773">Console</span></span>
- <span data-ttu-id="7a11e-774">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-774">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-775">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-775">LTP Results:</span></span>
<span data-ttu-id="7a11e-776">Keine Änderung seit 16273</span><span class="sxs-lookup"><span data-stu-id="7a11e-776">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="7a11e-777">Build 16275</span><span class="sxs-lookup"><span data-stu-id="7a11e-777">Build 16275</span></span>

<span data-ttu-id="7a11e-778">Allgemeine Windows-Informationen zu Build 162735 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-778">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-779">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-779">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-780">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-780">WSL</span></span>
- <span data-ttu-id="7a11e-781">In diesem Release gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-781">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-782">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-782">Console</span></span>
- <span data-ttu-id="7a11e-783">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-783">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-784">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-784">LTP Results:</span></span>
<span data-ttu-id="7a11e-785">Keine Änderung seit 16273</span><span class="sxs-lookup"><span data-stu-id="7a11e-785">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="7a11e-786">Build 16273</span><span class="sxs-lookup"><span data-stu-id="7a11e-786">Build 16273</span></span>

<span data-ttu-id="7a11e-787">Allgemeine Windows-Informationen zu Build 16273 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-787">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-788">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-788">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-789">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-789">WSL</span></span>
- <span data-ttu-id="7a11e-790">Korrektur eines Problems, bei dem DrvFs manchmal den falschen Dateityp für Verzeichnisse gemeldet hat [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="7a11e-790">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="7a11e-791">Ermöglichen der Erstellung von NETLINK_KOBJECT_UEVENT-Sockets zum Entsperren von Programmen, die uevent verwenden [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span><span class="sxs-lookup"><span data-stu-id="7a11e-791">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="7a11e-792">Hinzufügen von Unterstützung für nicht blockierende Verbindungen [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span><span class="sxs-lookup"><span data-stu-id="7a11e-792">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="7a11e-793">Implementieren des CLONE_FS-Klonsystem-Aufrufflags [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="7a11e-793">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="7a11e-794">Korrektur von Problemen im Zusammenhang mit der nicht ordnungsgemäßen Behandlung von Registerkarten oder Anführungszeichen in NT-Interop [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="7a11e-794">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="7a11e-795">Beheben des Fehlers „Zugriff verweigert“ beim Versuch, WSL-Instanzen erneut zu starten [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="7a11e-795">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="7a11e-796">Implementieren von Futex-Vorgängen FUTEX_REQUEUE und FUTEX_CMP_REQUEUE [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="7a11e-796">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="7a11e-797">Korrigieren von Berechtigungen für verschiedene SysFs-Dateien [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="7a11e-797">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="7a11e-798">Korrigieren des Hängens des Haskell-Stapels während des Setups [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="7a11e-798">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="7a11e-799">Implementieren der Flags „C“, „O“ und „P“ von binfmt_misc [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="7a11e-799">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="7a11e-800">Hinzufügen von /proc/sys/kernel/shmmax/shmmni und /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="7a11e-800">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="7a11e-801">Hinzufügen partieller Unterstützung für den ioprio_set-Systemaufruf [GH 498]</span><span class="sxs-lookup"><span data-stu-id="7a11e-801">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="7a11e-802">Stub für SO_REUSEPORT und Hinzufügen von Unterstützung für SO_PASSCRED für netlink-Sockets [GH 69]</span><span class="sxs-lookup"><span data-stu-id="7a11e-802">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="7a11e-803">Rückgabe anderer Fehlercodes aus RegisterDistribuiton, wenn zurzeit eine Distribution installiert oder deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-803">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="7a11e-804">Ermöglichen des Aufhebens der Registrierung von teilweise installierten WSL-Distributionen über „wslconfig.exe“</span><span class="sxs-lookup"><span data-stu-id="7a11e-804">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="7a11e-805">Korrektur des Hängens des Python-Sockettests von udp::msg_peek</span><span class="sxs-lookup"><span data-stu-id="7a11e-805">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="7a11e-806">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-806">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-807">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-807">Console</span></span>
- <span data-ttu-id="7a11e-808">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-808">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-809">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-809">LTP Results:</span></span>
<span data-ttu-id="7a11e-810">Tests gesamt: 1904</span><span class="sxs-lookup"><span data-stu-id="7a11e-810">Total Tests: 1904</span></span><br/>
<span data-ttu-id="7a11e-811">Übersprungene Tests gesamt: 209</span><span class="sxs-lookup"><span data-stu-id="7a11e-811">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="7a11e-812">Fehler gesamt: 229</span><span class="sxs-lookup"><span data-stu-id="7a11e-812">Total Failures: 229</span></span><br/>
[<span data-ttu-id="7a11e-813">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-813">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="7a11e-814">Build 16257</span><span class="sxs-lookup"><span data-stu-id="7a11e-814">Build 16257</span></span>

<span data-ttu-id="7a11e-815">Allgemeine Windows-Informationen zu Build 16257 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-815">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-816">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-816">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-817">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-817">WSL</span></span>
- <span data-ttu-id="7a11e-818">Implementieren des prlimit64-Systemaufrufs</span><span class="sxs-lookup"><span data-stu-id="7a11e-818">Implement prlimit64 system call</span></span>
- <span data-ttu-id="7a11e-819">Hinzufügen von Unterstützung für ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="7a11e-819">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="7a11e-820">Stub für MSG_MORE für TCP-Sockets [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="7a11e-820">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="7a11e-821">Korrektur des ungültigen Verhaltens des AT_EXECFN-Hilfsvektors [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="7a11e-821">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="7a11e-822">Korrektur des Kopier-/Einfügeverhalten für Konsole/TTY und Hinzufügen einer besseren Verarbeitung voller Puffer [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="7a11e-822">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="7a11e-823">Festlegen von T_SECURE im Hilfsvektor für set-user-ID- und set-group-ID-Programme [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="7a11e-823">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="7a11e-824">Psuedoterminal-Masterendpunkt verarbeitet TIOCPGRP nicht [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="7a11e-824">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="7a11e-825">Korrektur des Nichtzurückspulens von Verzeichnissen in LxFs durch lseek [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="7a11e-825">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="7a11e-826">/dev/ptmx wird nach hoher Auslastung gesperrt [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="7a11e-826">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="7a11e-827">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-827">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-828">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-828">Console</span></span>
- <span data-ttu-id="7a11e-829">Korrektur für horizontale Linien/Unterstriche überall [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="7a11e-829">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="7a11e-830">Korrektur der Änderung der Prozessreihenfolge, wodurch das Schließen von NPM erschwert wird [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="7a11e-830">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="7a11e-831">Hinzufügen des neuen Farbschemas: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="7a11e-831">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-832">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-832">LTP Results:</span></span>
<span data-ttu-id="7a11e-833">Keine Änderung seit 16251</span><span class="sxs-lookup"><span data-stu-id="7a11e-833">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-834">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-834">Syscall Support</span></span>
<span data-ttu-id="7a11e-835">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-835">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-836">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-836">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="7a11e-837">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="7a11e-837">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-"></a><span data-ttu-id="7a11e-838">[GitHub-Issue 2392: Windows-Ordner werden von WSL nicht erkannt (](https://github.com/Microsoft/BashOnWindows/issues/2392))</span><span class="sxs-lookup"><span data-stu-id="7a11e-838">[GitHub Issue 2392: Windows Folders not recognized by WSL ...](https://github.com/Microsoft/BashOnWindows/issues/2392)</span></span>
<span data-ttu-id="7a11e-839">In Build 16257 hat WSL beim Aufzählen von Windows-Dateien/-Ordnern über `/mnt/c/...` Probleme.</span><span class="sxs-lookup"><span data-stu-id="7a11e-839">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="7a11e-840">Dieses Problem wurde behoben und sollte im Insider-Builds in der Woche ab dem 14.08.2017 veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-840">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="7a11e-841">Build 16251</span><span class="sxs-lookup"><span data-stu-id="7a11e-841">Build 16251</span></span>

<span data-ttu-id="7a11e-842">Allgemeine Windows-Informationen zu Build 16251 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-842">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-843">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-843">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-844">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-844">WSL</span></span>
- <span data-ttu-id="7a11e-845">Entfernen des Beta-Tags aus der optionalen WSL-Komponente. Weitere Informationen finden Sie im [Blogbeitrag](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-845">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="7a11e-846">Ordnungsgemäße Initialisierung der saved-set uid und gid für set-user-ID- and set-group-ID-Binärdateien bei der Ausführung [GH 962, 1415, 2072]</span><span class="sxs-lookup"><span data-stu-id="7a11e-846">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="7a11e-847">Hinzufügen von Unterstützung für PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="7a11e-847">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="7a11e-848">Hinzufügen von Unterstützung für PTRACE_GETFPREGS und PTRACE_GETREGSET mit NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="7a11e-848">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="7a11e-849">Korrektur von ptrace, um bei ignorierten Signalen anzuhalten</span><span class="sxs-lookup"><span data-stu-id="7a11e-849">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="7a11e-850">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-850">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-851">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-851">Console</span></span>
- <span data-ttu-id="7a11e-852">Keine konsolenbezogenen Änderungen in diesem Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-852">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-853">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-853">LTP Results:</span></span>
<span data-ttu-id="7a11e-854">Anzahl bestandener Tests: 768</span><span class="sxs-lookup"><span data-stu-id="7a11e-854">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="7a11e-855">Anzahl fehlgeschlagener Tests: 244</span><span class="sxs-lookup"><span data-stu-id="7a11e-855">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="7a11e-856">Anzahl übersprungener Tests: 96</span><span class="sxs-lookup"><span data-stu-id="7a11e-856">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="7a11e-857">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-857">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="7a11e-858">Build 16241</span><span class="sxs-lookup"><span data-stu-id="7a11e-858">Build 16241</span></span>

<span data-ttu-id="7a11e-859">Allgemeine Windows-Informationen zu Build 16241 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-859">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-860">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-860">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="7a11e-861">WSL</span><span class="sxs-lookup"><span data-stu-id="7a11e-861">WSL</span></span>
- <span data-ttu-id="7a11e-862">In diesem Release gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-862">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="7a11e-863">Konsole</span><span class="sxs-lookup"><span data-stu-id="7a11e-863">Console</span></span>
- <span data-ttu-id="7a11e-864">Korrektur für die Ausgabe des falschen Zeichens für Schnittlinien-DEC, ursprünglich [hier](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/) gemeldet</span><span class="sxs-lookup"><span data-stu-id="7a11e-864">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="7a11e-865">Korrektur, dass kein Ausgabetext in Codepage 65001 (UTF8) angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="7a11e-865">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="7a11e-866">Übertragen Sie an den RGB-Werten einer Farbe vorgenommene Änderungen nicht an andere Teile der Palette bei Änderungen der Auswahl.</span><span class="sxs-lookup"><span data-stu-id="7a11e-866">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="7a11e-867">Dadurch wird die Verwendung des Konsoleneigenschaftenblatts erheblich vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-867">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="7a11e-868">STRG+S funktioniert anscheinend nicht ordnungsgemäß</span><span class="sxs-lookup"><span data-stu-id="7a11e-868">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="7a11e-869">Un-Bold/-Dim fehlt in ANSI-Escapecodes vollständig [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="7a11e-869">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="7a11e-870">Die Konsole unterstützt VIM-Farbdesigns nicht ordnungsgemäß [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="7a11e-870">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="7a11e-871">Bestimmte Zeichen können nicht eingefügt werden [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="7a11e-871">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="7a11e-872">Die Größenänderung von dynamischem Umbruch interagiert seltsam mit der Größenänderung eines Bash-Fensters, wenn sich die Inhalte in der Bearbeitungs-/Befehlszeile befinden [GH-Verbindung 1123]</span><span class="sxs-lookup"><span data-stu-id="7a11e-872">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="7a11e-873">STRG+L hinterlässt Fragmente auf dem Bildschirm [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="7a11e-873">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="7a11e-874">Konsolenrenderingfehler bei der Anzeige von VT für HDPI [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="7a11e-874">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="7a11e-875">Japanische Zeichen sehen mit dem Unicode-Zeichen U+30FB seltsam aus [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="7a11e-875">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="7a11e-876">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-876">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="7a11e-877">Build 16237</span><span class="sxs-lookup"><span data-stu-id="7a11e-877">Build 16237</span></span>

<span data-ttu-id="7a11e-878">Allgemeine Windows-Informationen zu Build 16237 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-878">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-879">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-879">Fixed</span></span>
- <span data-ttu-id="7a11e-880">Verwenden von Standardattributen für Dateien ohne E/As in lxfs (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="7a11e-880">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="7a11e-881">Hinzufügen von Unterstützung für Distributionen, die erweiterte Attribute verwenden</span><span class="sxs-lookup"><span data-stu-id="7a11e-881">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="7a11e-882">Korrektur des Auffüllens für von getdents und getdents64 zurückgegebene Einträge</span><span class="sxs-lookup"><span data-stu-id="7a11e-882">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="7a11e-883">Korrektur der Berechtigungsüberprüfung für den SHM_STAT-Systemaufruf [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="7a11e-883">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="7a11e-884">Korrektur des falschen anfänglichen epoll-Zustands für ttys [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="7a11e-884">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="7a11e-885">Korrektur, dass DrvFs readdir nicht alle Einträge zurückgibt [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="7a11e-885">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="7a11e-886">Korrektur von LxFs readdir, wenn Dateien nicht verknüpft sind [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="7a11e-886">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="7a11e-887">Ermöglichen des erneuten Öffnens von nicht verknüpfter drvfs-Dateien über procfs</span><span class="sxs-lookup"><span data-stu-id="7a11e-887">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="7a11e-888">Hinzufügen einer Außerkraftsetzung des globalen Registrierungsschlüssels zum Deaktivieren von WSL-Features (Interop/Laufwerkeinbindung)</span><span class="sxs-lookup"><span data-stu-id="7a11e-888">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="7a11e-889">Korrektur falscher Blockanzahl in „stat“ für DrvFs (und LxFs) [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="7a11e-889">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="7a11e-890">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-890">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="7a11e-891">Build 16232</span><span class="sxs-lookup"><span data-stu-id="7a11e-891">Build 16232</span></span>

<span data-ttu-id="7a11e-892">Allgemeine Windows-Informationen zu Build 16232 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-892">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-893">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-893">Fixed</span></span>
- <span data-ttu-id="7a11e-894">In diesem Release gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-894">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="7a11e-895">Build 16226</span><span class="sxs-lookup"><span data-stu-id="7a11e-895">Build 16226</span></span>

<span data-ttu-id="7a11e-896">Allgemeine Windows-Informationen zu Build 16226 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-896">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-897">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-897">Fixed</span></span>
- <span data-ttu-id="7a11e-898">Unterstützung von auf xattr bezogenen Systemaufrufen (getxattr, setxattr, listxattr, removexattr).</span><span class="sxs-lookup"><span data-stu-id="7a11e-898">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="7a11e-899">xattr-Unterstützung für security.capablity.</span><span class="sxs-lookup"><span data-stu-id="7a11e-899">security.capablity xattr support.</span></span>
- <span data-ttu-id="7a11e-900">Verbesserte Kompatibilität mit bestimmten Dateisystemen und Filtern, einschließlich Nicht-MS-SMB-Servern.</span><span class="sxs-lookup"><span data-stu-id="7a11e-900">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="7a11e-901">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="7a11e-901">[GH #1952]</span></span>
- <span data-ttu-id="7a11e-902">Verbesserte Unterstützung für OneDrive-Platzhalter, GVFS-Platzhalter und komprimierte Compact OS-Dateien.</span><span class="sxs-lookup"><span data-stu-id="7a11e-902">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="7a11e-903">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-903">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="7a11e-904">Build 16215</span><span class="sxs-lookup"><span data-stu-id="7a11e-904">Build 16215</span></span>

<span data-ttu-id="7a11e-905">Allgemeine Windows-Informationen zu Build 16215 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-905">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-906">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-906">Fixed</span></span>
- <span data-ttu-id="7a11e-907">Für WSL ist der Entwicklermodus nicht mehr erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a11e-907">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="7a11e-908">Unterstützung von Verzeichnisverbindungen in drvfs.</span><span class="sxs-lookup"><span data-stu-id="7a11e-908">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="7a11e-909">Verarbeiten der Deinstallation von appx-Paketen der WSL-Distribution.</span><span class="sxs-lookup"><span data-stu-id="7a11e-909">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="7a11e-910">Aktualisieren von procfs, um private und freigegebene Zuordnungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-910">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="7a11e-911">Hinzufügen einer Möglichkeit für „wslconfig.exe“ zum Bereinigen von Distributionen, die teilweise installiert oder deinstalliert wurden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-911">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="7a11e-912">Hinzufügen von Unterstützung für IP_MTU_DISCOVER für TCP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="7a11e-912">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="7a11e-913">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="7a11e-913">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="7a11e-914">Ableiten der Protokollfamilie für Routen zu AF_INADDR.</span><span class="sxs-lookup"><span data-stu-id="7a11e-914">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="7a11e-915">Verbesserungen an seriellen Geräten [GH 1929].</span><span class="sxs-lookup"><span data-stu-id="7a11e-915">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="7a11e-916">Build 16199</span><span class="sxs-lookup"><span data-stu-id="7a11e-916">Build 16199</span></span>

<span data-ttu-id="7a11e-917">Allgemeine Windows-Informationen zu Build 16199 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-917">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-918">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-918">Fixed</span></span>
- <span data-ttu-id="7a11e-919">In diesen Releases gibt es keine WSL-bezogenen Änderungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-919">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="7a11e-920">Build 16193</span><span class="sxs-lookup"><span data-stu-id="7a11e-920">Build 16193</span></span>

<span data-ttu-id="7a11e-921">Allgemeine Windows-Informationen zu Build 16193 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-921">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-922">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-922">Fixed</span></span>
- <span data-ttu-id="7a11e-923">Racebedingung zwischen dem Senden von SIGCONT und einer Threadgruppe, die beendet wird [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="7a11e-923">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="7a11e-924">Ändern von TTY-und PTY-Geräten zum Melden von FILE_DEVICE_NAMED_PIPE anstelle von FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="7a11e-924">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="7a11e-925">SSH-Korrektur für IP_OPTIONS</span><span class="sxs-lookup"><span data-stu-id="7a11e-925">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="7a11e-926">Verschieben der DrvFs-Einbindung in den init-Daemon [GH 1862, 1968, 1767, 1933]</span><span class="sxs-lookup"><span data-stu-id="7a11e-926">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="7a11e-927">Hinzufügen von Unterstützung in DrvFs für die folgenden symbolischen NT-Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-927">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="7a11e-928">Build 16184</span><span class="sxs-lookup"><span data-stu-id="7a11e-928">Build 16184</span></span>

<span data-ttu-id="7a11e-929">Allgemeine Windows-Informationen zu Build 16184 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-929">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-930">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-930">Fixed</span></span>
- <span data-ttu-id="7a11e-931">Entfernen des apt-Paketverwaltungstasks (lxrun.exe /update) wurde entfernt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-931">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="7a11e-932">Korrektur der Nichtanzeige der Ausgabe aus Windows-Prozessen in node.js [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="7a11e-932">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="7a11e-933">Lockern der Ausrichtungsanforderungen in lxcore [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="7a11e-933">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="7a11e-934">Korrektur der Verarbeitung des AT_EMPTY_PATH-Flags in mehreren Systemaufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-934">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="7a11e-935">Korrektur eines Problems, bei dem das Löschen von DrvFs-Dateien mit geöffneten Handles bewirkt, dass die Datei nicht definiertes Verhalten aufweist [GH 544, 966, 1357, 1535, 1615]</span><span class="sxs-lookup"><span data-stu-id="7a11e-935">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="7a11e-936">„/etc/hosts“ erbt nun Einträge von der Windows-Hostdatei (%windir%\system32\drivers\etc\hosts) [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="7a11e-936">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="7a11e-937">Build 16179</span><span class="sxs-lookup"><span data-stu-id="7a11e-937">Build 16179</span></span>

<span data-ttu-id="7a11e-938">Allgemeine Windows-Informationen zu Build 16179 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-938">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-939">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-939">Fixed</span></span>
- <span data-ttu-id="7a11e-940">Keine WSL-Änderungen in dieser Woche.</span><span class="sxs-lookup"><span data-stu-id="7a11e-940">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="7a11e-941">Build 16176</span><span class="sxs-lookup"><span data-stu-id="7a11e-941">Build 16176</span></span>

<span data-ttu-id="7a11e-942">Allgemeine Windows-Informationen zu Build 16176 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-942">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-943">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-943">Fixed</span></span>

- [<span data-ttu-id="7a11e-944">Aktivierte serielle Unterstützung</span><span class="sxs-lookup"><span data-stu-id="7a11e-944">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="7a11e-945">Hinzufügen der IP-Socketoption IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="7a11e-945">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="7a11e-946">Implementierung der pwritev-Funktion (beim Hochladen der Datei nach nginx/PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="7a11e-946">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="7a11e-947">Hinzufügen der IP-Socket-Optionen IP_MULTICAST_IF und IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="7a11e-947">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="7a11e-948">Unterstützung für Socketoption IP_MULTICAST_LOOP und IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="7a11e-948">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="7a11e-949">Hinzufügen von IP(V6)_MTU-Socketoption für den Knoten apps, traceroute, dig, nslookup, host</span><span class="sxs-lookup"><span data-stu-id="7a11e-949">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="7a11e-950">Hinzufügen der IP-Socketoption IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="7a11e-950">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="7a11e-951">Verbesserungen des Dateisystems</span><span class="sxs-lookup"><span data-stu-id="7a11e-951">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="7a11e-952">Ermöglichen der Einbindung von UNC-Pfaden</span><span class="sxs-lookup"><span data-stu-id="7a11e-952">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="7a11e-953">Ermöglichen von CDFS-Unterstützung in drvfs</span><span class="sxs-lookup"><span data-stu-id="7a11e-953">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="7a11e-954">Ordnungsgemäße Verarbeitung von Berechtigungen für Netzwerkdateisysteme in drvfs</span><span class="sxs-lookup"><span data-stu-id="7a11e-954">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="7a11e-955">Hinzufügen von Unterstützung für Remotelaufwerke zu drvfs</span><span class="sxs-lookup"><span data-stu-id="7a11e-955">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="7a11e-956">Ermöglichen von FAT-Unterstützung in drvfs</span><span class="sxs-lookup"><span data-stu-id="7a11e-956">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="7a11e-957">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-957">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-958">LTP-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="7a11e-958">LTP Results</span></span>
<span data-ttu-id="7a11e-959">Keine Änderungen seit 15042</span><span class="sxs-lookup"><span data-stu-id="7a11e-959">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="7a11e-960">Build 16170</span><span class="sxs-lookup"><span data-stu-id="7a11e-960">Build 16170</span></span>

<span data-ttu-id="7a11e-961">Allgemeine Windows-Informationen zu Build 16170 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-961">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="7a11e-962">Wir haben einen neuen [Blogbeitrag](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) veröffentlicht, in dem unsere Anstrengungen beim Testen von WSL erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-962">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="7a11e-963">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-963">Fixed</span></span>

- <span data-ttu-id="7a11e-964">Unterstützung für Socketoption IP_ADD_MEMBERSHIP und IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="7a11e-964">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="7a11e-965">Hinzufügen von Unterstützung für PTRACE_OLDSETOPTIONS.</span><span class="sxs-lookup"><span data-stu-id="7a11e-965">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="7a11e-966">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="7a11e-966">[GH 1692]</span></span>
- <span data-ttu-id="7a11e-967">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-967">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-968">LTP-Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="7a11e-968">LTP Results</span></span>
<span data-ttu-id="7a11e-969">Keine Änderungen seit 15042</span><span class="sxs-lookup"><span data-stu-id="7a11e-969">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="7a11e-970">Build 15046 für Windows 10 Creators Update</span><span class="sxs-lookup"><span data-stu-id="7a11e-970">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="7a11e-971">Es gibt keine weiteren WSL-Korrekturen oder-Funktionen, die für die Einbindung in das Creators Update in Windows 10 geplant sind.</span><span class="sxs-lookup"><span data-stu-id="7a11e-971">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="7a11e-972">Die Anmerkungen zu dieser Version von WSL werden in den kommenden Wochen fortgesetzt, um Ergänzungen für das nächste Hauptupdate von Windows aufzuführen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-972">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="7a11e-973">Allgemeine Windows-Informationen zu Build 15046 und zukünftigen Insider Releases finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-973">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="7a11e-974">Build 15042</span><span class="sxs-lookup"><span data-stu-id="7a11e-974">Build 15042</span></span>

<span data-ttu-id="7a11e-975">Allgemeine Windows-Informationen zu Build 15042 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-975">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-976">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-976">Fixed</span></span>

- <span data-ttu-id="7a11e-977">Korrektur eines Deadlocks beim Entfernen eines Pfades, der auf „..“ endet</span><span class="sxs-lookup"><span data-stu-id="7a11e-977">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="7a11e-978">Korrektur eines Problems, bei dem FIONBIO bei Erfolg 0 zurückgibt [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="7a11e-978">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="7a11e-979">Korrektur eines Problems bei Lesevorgängen mit einer Länge von Null von Internetdatagrammsockets</span><span class="sxs-lookup"><span data-stu-id="7a11e-979">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="7a11e-980">Korrektur eines möglichen Deadlocks aufgrund einer Racebedingung bei der drvfs inode-Suche [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="7a11e-980">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="7a11e-981">Erweiterte Unterstützung für Hilfsdaten von Unix-Sockets, SCM_CREDENTIALS und SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="7a11e-981">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="7a11e-982">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-982">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-983">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-983">LTP Results:</span></span>
<span data-ttu-id="7a11e-984">Anzahl bestandener Tests: 737</span><span class="sxs-lookup"><span data-stu-id="7a11e-984">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="7a11e-985">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="7a11e-985">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="7a11e-986">Build 15031</span><span class="sxs-lookup"><span data-stu-id="7a11e-986">Build 15031</span></span>

<span data-ttu-id="7a11e-987">Allgemeine Windows-Informationen zu Build 15031 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-987">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-988">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-988">Fixed</span></span>

- <span data-ttu-id="7a11e-989">Korrektur eines Fehlers, bei dem sich time(2) sporadisch falsch verhielt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-989">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="7a11e-990">Korrektur eines Problems, bei dem \*SIGPROCMASK-Systemaufrufe die Signalmaske beschädigen konnten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-990">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="7a11e-991">Jetzt Rückgabe der vollständigen Länge der Befehlszeile in WSL-Benachrichtigung zur Prozesserstellung.</span><span class="sxs-lookup"><span data-stu-id="7a11e-991">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="7a11e-992">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="7a11e-992">[GH 1632]</span></span>
- <span data-ttu-id="7a11e-993">WSL meldet jetzt die Threadbeendigung über ptrace für GDB-Hänger.</span><span class="sxs-lookup"><span data-stu-id="7a11e-993">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="7a11e-994">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="7a11e-994">[GH 1196]</span></span>
- <span data-ttu-id="7a11e-995">Korrektur eines Fehlers, bei dem ptys nach hoher tmux-E/A nicht mehr reagiert</span><span class="sxs-lookup"><span data-stu-id="7a11e-995">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="7a11e-996">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="7a11e-996">[GH 1358]</span></span>
- <span data-ttu-id="7a11e-997">Korrektur der Timeoutüberprüfung in zahlreichen Systemaufrufen (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span><span class="sxs-lookup"><span data-stu-id="7a11e-997">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="7a11e-998">Hinzufügen von eventfd EFD_SEMAPHORE-Unterstützung [GH 452]</span><span class="sxs-lookup"><span data-stu-id="7a11e-998">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="7a11e-999">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-999">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1000">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1000">LTP Results:</span></span>
<span data-ttu-id="7a11e-1001">Anzahl bestandener Tests: 737</span><span class="sxs-lookup"><span data-stu-id="7a11e-1001">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="7a11e-1002">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="7a11e-1002">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7a11e-1003">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1003">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="7a11e-1004">Build 15025</span><span class="sxs-lookup"><span data-stu-id="7a11e-1004">Build 15025</span></span>

<span data-ttu-id="7a11e-1005">Allgemeine Windows-Informationen zu Build 15025 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1005">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1006">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1006">Fixed</span></span>

- <span data-ttu-id="7a11e-1007">Korrektur eines Fehlers, bei dem grep 2.27 nicht mehr funktioniert [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1007">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="7a11e-1008">Implementierung des EFD_SEMAPHORE-Flags für den eventfd2-Systemaufruf [GH 452]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1008">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="7a11e-1009">Implementierung von /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1009">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="7a11e-1010">Signalgestützte E/A-Unterstützung für Unix-Streamsockets [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1010">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="7a11e-1011">Unterstützung für F_GETPIPE_SZ und F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1011">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="7a11e-1012">Implementierung des recvmmsg()-Systemaufrufs [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1012">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="7a11e-1013">Korrektur eines Fehlers, bei dem epoll_wait() nicht gewartet hat [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1013">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="7a11e-1014">Implementierung von /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="7a11e-1014">Implement /proc/version_signature</span></span>
- <span data-ttu-id="7a11e-1015">Tee-Systemaufruf gibt jetzt einen Fehler zurück, wenn beide Dateideskriptoren auf dieselbe Pipe verweisen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1015">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="7a11e-1016">Implementierung des richtigen Verhaltens für SO_PEERCRED für Unix-Sockets</span><span class="sxs-lookup"><span data-stu-id="7a11e-1016">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="7a11e-1017">Korrektur der Verarbeitung ungültiger Parameter des tkill-Systemaufrufs</span><span class="sxs-lookup"><span data-stu-id="7a11e-1017">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="7a11e-1018">Änderungen zum Verbessern der Leistung von drvfs</span><span class="sxs-lookup"><span data-stu-id="7a11e-1018">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="7a11e-1019">Kleinere Korrektur für Ruby-E/A-Blockierung</span><span class="sxs-lookup"><span data-stu-id="7a11e-1019">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="7a11e-1020">Korrektur von recvmsg() beim Zurückgeben von EINVAL für das MSG_DONTWAIT-Flag für Inet-Sockets [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1020">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="7a11e-1021">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1021">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1022">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1022">LTP Results:</span></span>
<span data-ttu-id="7a11e-1023">Anzahl bestandener Tests: 732</span><span class="sxs-lookup"><span data-stu-id="7a11e-1023">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="7a11e-1024">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="7a11e-1024">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7a11e-1025">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1025">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="7a11e-1026">Build 15019</span><span class="sxs-lookup"><span data-stu-id="7a11e-1026">Build 15019</span></span>

<span data-ttu-id="7a11e-1027">Allgemeine Windows-Informationen zu Build 15019 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1027">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1028">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1028">Fixed</span></span>

- <span data-ttu-id="7a11e-1029">Korrektur eines Fehlers, der fälschlicherweise die CPU-Auslastung in procfs für Tools wie htop gemeldet hat [GH 823, 945, 971]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1029">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="7a11e-1030">Beim Aufrufen von open() mit O_TRUNC für eine vorhandene Datei „inotify“ wird nun IN_MODIFY vor IN_OPEN generiert</span><span class="sxs-lookup"><span data-stu-id="7a11e-1030">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="7a11e-1031">Korrekturen für den Unix-Socket getsockopt SO_ERROR zum Aktivieren von Postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1031">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="7a11e-1032">Implementierung von /proc/sys/net/core/somaxconn für die Sprache GO</span><span class="sxs-lookup"><span data-stu-id="7a11e-1032">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="7a11e-1033">Der Apt-get-Packageupdate-Hintergrundtask wird jetzt aus der Ansicht ausgeblendet</span><span class="sxs-lookup"><span data-stu-id="7a11e-1033">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="7a11e-1034">Löschen des Bereichs für ipv6 localhost (Fehler Spring-Framework (Java)).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1034">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="7a11e-1035">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1035">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1036">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1036">LTP Results:</span></span>
<span data-ttu-id="7a11e-1037">Anzahl bestandener Tests: 714</span><span class="sxs-lookup"><span data-stu-id="7a11e-1037">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="7a11e-1038">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 249</span><span class="sxs-lookup"><span data-stu-id="7a11e-1038">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="7a11e-1039">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1039">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="7a11e-1040">Build 15014</span><span class="sxs-lookup"><span data-stu-id="7a11e-1040">Build 15014</span></span>

<span data-ttu-id="7a11e-1041">Allgemeine Windows-Informationen zu Build 15014 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1041">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1042">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1042">Fixed</span></span>

- <span data-ttu-id="7a11e-1043">STRG+C funktioniert nun wie beabsichtigt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1043">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="7a11e-1044">htop und ps auxw zeigen jetzt die richtige Ressourcenverwendung an (GH #516)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1044">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="7a11e-1045">Grundlegende Übersetzung von NT-Ausnahmen in Signale.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1045">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="7a11e-1046">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1046">(GH #513)</span></span>
- <span data-ttu-id="7a11e-1047">fallocate schlägt nun mit ENOSPC anstatt mit EINVAL fehl, wenn nicht genügend Speicherplatz verfügbar ist (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1047">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="7a11e-1048">Hinzufügen von /proc/sys/kernel/sem.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1048">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="7a11e-1049">Implementierung der semop- und semtimedop-Systemaufrufe</span><span class="sxs-lookup"><span data-stu-id="7a11e-1049">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="7a11e-1050">Korrektur von nslookup-Fehlern mit der IP_RECVTOS- und IPV6_RECVTCLASS-Socketoption (GH 69)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1050">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="7a11e-1051">Unterstützung für Socketoptionen IP_RECVTTL und IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="7a11e-1051">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="7a11e-1052">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1052">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1053">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1053">LTP Results:</span></span>
<span data-ttu-id="7a11e-1054">Anzahl bestandener Tests: 709</span><span class="sxs-lookup"><span data-stu-id="7a11e-1054">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="7a11e-1055">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="7a11e-1055">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7a11e-1056">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1056">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="7a11e-1057">Zusammenfassung der Systemaufrufe</span><span class="sxs-lookup"><span data-stu-id="7a11e-1057">Syscall Summary</span></span>
<span data-ttu-id="7a11e-1058">Systemaufrufe gesamt: 384</span><span class="sxs-lookup"><span data-stu-id="7a11e-1058">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="7a11e-1059">Implementiert gesamt: 235</span><span class="sxs-lookup"><span data-stu-id="7a11e-1059">Total Implemented: 235</span></span> </br>
<span data-ttu-id="7a11e-1060">Mit Stub versehen gesamt: 22</span><span class="sxs-lookup"><span data-stu-id="7a11e-1060">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="7a11e-1061">Nicht implementiert gesamt: 127</span><span class="sxs-lookup"><span data-stu-id="7a11e-1061">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="7a11e-1062">Ausführliche Aufschlüsselung</span><span class="sxs-lookup"><span data-stu-id="7a11e-1062">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="7a11e-1063">Build 15007</span><span class="sxs-lookup"><span data-stu-id="7a11e-1063">Build 15007</span></span>

<span data-ttu-id="7a11e-1064">Allgemeine Windows-Informationen zu Build 15007 finden Sie im [Windows-Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1064">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="7a11e-1065">Bekanntes Problem</span><span class="sxs-lookup"><span data-stu-id="7a11e-1065">Known Issue</span></span>

- <span data-ttu-id="7a11e-1066">Es gibt einen bekannten Fehler, bei dem die Konsole einige Eingaben über STRG+<key> nicht erkennt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1066">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="7a11e-1067">Dies schließt den Befehl STRG+C ein, der als normaler C-Tastendruck fungiert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1067">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="7a11e-1068">Problemumgehung: Ordnen Sie STRG+C eine alternative Taste zu.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1068">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="7a11e-1069">Gehen Sie beispielsweise folgendermaßen vor, um STRG+K der Tastenkombination STRG+C zuzuordnen: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1069">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="7a11e-1070">Diese Zuordnung erfolgt pro Terminal und muss *jedes* Mal ausgeführt werden, wenn Bash gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1070">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="7a11e-1071">Benutzer können die Option zum Einbeziehen in ihre `.bashrc`-Datei untersuchen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1071">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="7a11e-1072">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1072">Fixed</span></span>

- <span data-ttu-id="7a11e-1073">Korrektur eines Problems, bei dem die Ausführung von WSL 100 % eines CPU-Kerns verbraucht</span><span class="sxs-lookup"><span data-stu-id="7a11e-1073">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="7a11e-1074">Socketoption IP_PKTINFO, IPV6_RECVPKTINFO wird jetzt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1074">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="7a11e-1075">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1075">(GH #851, 987)</span></span>
- <span data-ttu-id="7a11e-1076">Abschneiden der physischen Adresse der Netzwerkschnittstelle auf 16 Bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1076">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="7a11e-1077">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1077">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1078">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1078">LTP Results:</span></span>
<span data-ttu-id="7a11e-1079">Anzahl bestandener Tests: 709</span><span class="sxs-lookup"><span data-stu-id="7a11e-1079">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="7a11e-1080">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 255</span><span class="sxs-lookup"><span data-stu-id="7a11e-1080">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="7a11e-1081">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1081">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="7a11e-1082">Build 15002</span><span class="sxs-lookup"><span data-stu-id="7a11e-1082">Build 15002</span></span>

<span data-ttu-id="7a11e-1083">Allgemeine Windows-Informationen zu Build 15002 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1083">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="7a11e-1084">Bekanntes Problem</span><span class="sxs-lookup"><span data-stu-id="7a11e-1084">Known Issue</span></span>

<span data-ttu-id="7a11e-1085">Zwei bekannte Probleme:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1085">Two known issues:</span></span>
- <span data-ttu-id="7a11e-1086">Es gibt einen bekannten Fehler, bei dem die Konsole einige Eingaben über STRG+<key> nicht erkennt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1086">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="7a11e-1087">Dies schließt den Befehl STRG+C ein, der als normaler C-Tastendruck fungiert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1087">This includes the ctrl-c command which will act as a normal 'c' keypress.</span></span>

  - <span data-ttu-id="7a11e-1088">Problemumgehung: Ordnen Sie STRG+C eine alternative Taste zu.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1088">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="7a11e-1089">Gehen Sie beispielsweise folgendermaßen vor, um STRG+K der Tastenkombination STRG+C zuzuordnen: `stty intr \^k`.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1089">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="7a11e-1090">Diese Zuordnung erfolgt pro Terminal und muss *jedes* Mal ausgeführt werden, wenn Bash gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1090">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="7a11e-1091">Benutzer können die Option zum Einbeziehen in ihre `.bashrc`-Datei untersuchen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1091">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="7a11e-1092">Während der Ausführung von WSL werden von einem Systemthread 100 % eines CPU-Kerns beansprucht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1092">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="7a11e-1093">Die Ursache wurde untersucht und intern behoben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1093">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="7a11e-1094">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1094">Fixed</span></span>

- <span data-ttu-id="7a11e-1095">Alle Bash-Sitzungen müssen jetzt auf derselben Berechtigungsebene erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1095">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="7a11e-1096">Der Versuch, eine Sitzung auf einer anderen Ebene zu starten, wird blockiert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1096">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="7a11e-1097">Dies bedeutet, dass Administrator-und Nicht-Administratorkonsolen nicht gleichzeitig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1097">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="7a11e-1098">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1098">(GH #626)</span></span>
<br/>
- <span data-ttu-id="7a11e-1099">Implementierung der folgenden NETLINK_ROUTE-Meldungen (erfordert Windows-Administrator)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1099">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="7a11e-1100">RTM_NEWADDR (unterstützt `ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1100">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="7a11e-1101">RTM_NEWROUTE (unterstützt `ip route add`)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1101">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="7a11e-1102">RTM_DELADDR (unterstützt `ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1102">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="7a11e-1103">RTM_DELROUTE (unterstützt `ip route del`)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1103">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="7a11e-1104">Die geplante Tasküberprüfung für zu aktualisierende Pakete wird nicht mehr über eine getaktete Verbindung ausgeführt (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1104">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="7a11e-1105">Korrektur eines Fehlers, bei dem die Weiterleitung unterbrochen wird. Beispiel: bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1105">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="7a11e-1106">Implementierung der TCP_KEEPCNT-Socketoption (GH #843)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1106">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="7a11e-1107">Implementierung der IP_MTU_DISCOVER INET-Socketoption (GH #720, 717, 170, 69)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1107">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="7a11e-1108">Entfernen der Legacyfnktionalität zum Ausführen von NT-Binärdateien aus init mit NT-Pfadsuche.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1108">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="7a11e-1109">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1109">(GH #1325)</span></span>
- <span data-ttu-id="7a11e-1110">Korrektur des Modus von /dev/kmsg zum Zulassen von Gruppen-/sonstigem Lesezugriff (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1110">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="7a11e-1111">Implementierung von /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1111">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="7a11e-1112">Korrektur eines Fehlers, bei dem die Startzeit des Prozesses als Jahr 2432 angezeigt wurde (GH #974)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1112">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="7a11e-1113">Wechseln der TERM-Standardumgebungsvariablen in xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1113">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="7a11e-1114">Änderung der Art und Weise, in der der Prozesscommit während des Prozessforks berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1114">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="7a11e-1115">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1115">(GH #1286)</span></span>
- <span data-ttu-id="7a11e-1116">Implementierung von /proc/sys/vm/overcommit_memory.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1116">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="7a11e-1117">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1117">(GH #1286)</span></span>
- <span data-ttu-id="7a11e-1118">Implementierung der /proc/net/route-Datei (GH #69)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1118">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="7a11e-1119">Korrektur eines Fehlers, bei dem der Verknüpfungsname falsch lokalisiert wurde (GH #696)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1119">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="7a11e-1120">Korrektur der fehlerhaften ELF-Verarbeitungslogik, die die Programmheader nicht ordnungsgemäß so überprüft, dass sie kleiner als (oder gleich) PATH_MAX sein müssen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1120">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="7a11e-1121">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1121">(GH #1048)</span></span>
- <span data-ttu-id="7a11e-1122">Implementierung des statfs-Rückrufs für procfs, sysfs, cgroupfs und binfmts (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1122">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="7a11e-1123">Korrektur der AptPackageIndexUpdate-Fenster, die nicht geschlossen werden (GH #1184, auch in GH #1193 beschrieben)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1123">Fixed AptPackageIndexUpdate windows that won't close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="7a11e-1124">Hinzufügen von ASLR-Personality, ADDR_NO_RANDOMIZE-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1124">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="7a11e-1125">[GH #1148, 1128]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1125">(GH #1148, 1128)</span></span>
- <span data-ttu-id="7a11e-1126">Verbesserung von PTRACE_GETSIGINFO, SIGSEGV für ordnungsgemäße gdb-Stapelüberwachungen während AV (GH #875)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1126">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="7a11e-1127">Elf-Verarbeitung schlägt für patchelf-Binärdateien nicht mehr fehl.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1127">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="7a11e-1128">[GH #471]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1128">(GH #471)</span></span>
- <span data-ttu-id="7a11e-1129">VPN DNS-Weitergabe an /etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1129">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="7a11e-1130">Verbesserungen an TCP Close für eine zuverlässigere Datenübertragung.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1130">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="7a11e-1131">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1131">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="7a11e-1132">Jetzt Rückgabe des richtigen Fehlercodes, wenn zu viele Dateien geöffnet werden (EMFILE).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1132">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="7a11e-1133">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1133">(GH #1126, 2090)</span></span>
- <span data-ttu-id="7a11e-1134">Windows-Überwachungsprotokoll erfasst jetzt den Imagenamen in Process Create Audit.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1134">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="7a11e-1135">Jetzt normaler Fehler beim Starten von „bash.exe“ in einem Bash-Fenster.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1135">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="7a11e-1136">Hinzufügen einer Fehlermeldung, wenn Interop nicht auf ein Arbeitsverzeichnis unter LxFs zugreifen kann (z.B. BASHRC-Datei von „notepad.exe“).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1136">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="7a11e-1137">Korrektur eines Problems, bei dem der Windows-Pfad in WSL abgeschnitten wurde</span><span class="sxs-lookup"><span data-stu-id="7a11e-1137">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="7a11e-1138">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1138">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1139">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1139">LTP Results:</span></span>
<span data-ttu-id="7a11e-1140">Anzahl bestandener Tests: 690</span><span class="sxs-lookup"><span data-stu-id="7a11e-1140">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="7a11e-1141">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 274</span><span class="sxs-lookup"><span data-stu-id="7a11e-1141">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="7a11e-1142">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1142">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1143">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1143">Syscall Support</span></span>
<span data-ttu-id="7a11e-1144">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1144">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1145">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1145">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="7a11e-1146">Build 14986</span><span class="sxs-lookup"><span data-stu-id="7a11e-1146">Build 14986</span></span>

<span data-ttu-id="7a11e-1147">Allgemeine Windows-Informationen zu Build 14986 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1147">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1148">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1148">Fixed</span></span>

- <span data-ttu-id="7a11e-1149">Korrektur von Fehlerüberprüfungen mit Netlink und Pty IOCTLs</span><span class="sxs-lookup"><span data-stu-id="7a11e-1149">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="7a11e-1150">Kernel Version meldet nun 4.4.0-43 aus Gründen der Konsistenz mit Xenial</span><span class="sxs-lookup"><span data-stu-id="7a11e-1150">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="7a11e-1151">„Bash.exe“ wird jetzt gestartet, wenn die Eingabe an „nul:“ gerichtet ist (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1151">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="7a11e-1152">Thread-IDs werden nun ordnungsgemäß in procfs erfasst (GH #967)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1152">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="7a11e-1153">Flags IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR werden jetzt in inotify_add_watch() unterstützt (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1153">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="7a11e-1154">Implementierung von timer_create und verwandten Systemaufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1154">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="7a11e-1155">Dies ermöglicht die GHC-Unterstützung (GH #307).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1155">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="7a11e-1156">Korrektur eines Problems, bei dem Ping eine Zeitangabe von 0,000 ms zurückgab (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1156">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="7a11e-1157">Rückgabe des richtigen Fehlercodes, wenn zu viele Dateien geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1157">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="7a11e-1158">Korrektur eines Problems in WSL, bei dem die Netlink-Anforderung für Netzwerkschnittstellendaten mit EINVAL fehlschlägt, wenn die Hardwareadresse der Schnittstelle 32 Bytes groß ist (z.B. die Teredo-Schnittstelle)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1158">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="7a11e-1159">Beachten Sie, dass das Linux-Hilfsprogramm „ip“ einen Fehler enthält, bei dem ein Absturz erfolgt, wenn WSL eine 32-Byte-Hardwareadresse meldet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1159">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="7a11e-1160">Dies ist ein Fehler in „ip“, nicht in WSL.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1160">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="7a11e-1161">Mit dem Hilfsprogramm „ip“ wird die Länge des Zeichenfolgenpuffers fest codiert, der zum Ausgeben der Hardwareadresse verwendet wird, und dieser Puffer ist zu klein, um eine 32-Byte-Hardwareadresse auszugeben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1161">The "ip" utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="7a11e-1162">Zusätzliche Korrekturen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1162">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1163">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1163">LTP Results:</span></span>
<span data-ttu-id="7a11e-1164">Anzahl bestandener Tests: 669</span><span class="sxs-lookup"><span data-stu-id="7a11e-1164">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="7a11e-1165">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 258</span><span class="sxs-lookup"><span data-stu-id="7a11e-1165">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="7a11e-1166">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1166">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1167">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1167">Syscall Support</span></span>
<span data-ttu-id="7a11e-1168">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1168">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1169">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1169">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="7a11e-1170">Build 14971</span><span class="sxs-lookup"><span data-stu-id="7a11e-1170">Build 14971</span></span>

<span data-ttu-id="7a11e-1171">Allgemeine Windows-Informationen zu Build 14971 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1171">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1172">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1172">Fixed</span></span>

 - <span data-ttu-id="7a11e-1173">Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1173">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="7a11e-1174">Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1174">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1175">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1175">LTP Results:</span></span>
<span data-ttu-id="7a11e-1176">Keine Änderungen seit 14965</span><span class="sxs-lookup"><span data-stu-id="7a11e-1176">Unchanged from 14965</span></span> </br>
<span data-ttu-id="7a11e-1177">Anzahl bestandener Tests: 664</span><span class="sxs-lookup"><span data-stu-id="7a11e-1177">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="7a11e-1178">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1178">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1179">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1179">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="7a11e-1180">Build 14965</span><span class="sxs-lookup"><span data-stu-id="7a11e-1180">Build 14965</span></span>

<span data-ttu-id="7a11e-1181">Allgemeine Windows-Informationen zu Build 14965 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1181">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1182">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1182">Fixed</span></span>

- <span data-ttu-id="7a11e-1183">Unterstützung für Netlink-Sockets RTM_GETLINK und RTM_GETADDR des NETLINK_ROUTE-Protokolls (GH #468)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1183">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="7a11e-1184">Aktiviert ifconfig- und ip-Befehle für die Netzwerkenumeration.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1184">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="7a11e-1185">Weitere Informationen finden Sie in unserem [Blogbeitrag zu WSL-Netzwerken](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1185">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="7a11e-1186">„/sbin“ befindet sich jetzt standardmäßig im Pfad des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1186">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="7a11e-1187">Der NT-Benutzerpfad wird jetzt standardmäßig an den WSL-Pfad angefügt (Sie können nun also „notepad.exe“ eingeben, ohne dem Linux-Pfad System32 hinzuzufügen).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1187">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="7a11e-1188">Hinzufügen von Unterstützung für /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="7a11e-1188">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="7a11e-1189">NT-Binärdateien können nun aus WSL gestartet werden, wenn das aktuelle Arbeitsverzeichnis Nicht-ANSI-Zeichen enthält (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1189">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="7a11e-1190">Ermöglichen des Herunterfahrens für getrennten UNIX-Streamsocket</span><span class="sxs-lookup"><span data-stu-id="7a11e-1190">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="7a11e-1191">Hinzufügen von Unterstützung für PR_GET_PDEATHSIG.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1191">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="7a11e-1192">Hinzufügen von Unterstützung für CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="7a11e-1192">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="7a11e-1193">Korrektur eines Fehlers, bei dem die Weiterleitung unterbrochen wird. Beispiel: bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1193">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="7a11e-1194">Verarbeiten von Anforderungen zum Herstellen einer Verbindung mit dem aktuellen Terminal.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1194">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="7a11e-1195">Markieren von /proc/<pid>/oom_score_adj als beschreibbar.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1195">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="7a11e-1196">Hinzufügen des Ordners „/sys/fs/cgroup“.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1196">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="7a11e-1197">sched_setaffinity sollte den Wert der Affinitätsbitsmaske zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1197">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="7a11e-1198">Korrektur der ELF-Validierungslogik, die fälschlicherweise annimmt, dass Interpreterpfade weniger als 64 Zeichen lang sein müssen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1198">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="7a11e-1199">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1199">(GH #743)</span></span>
- <span data-ttu-id="7a11e-1200">Geöffnete Dateideskriptoren können das Konsolenfenster geöffnet lassen (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1200">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="7a11e-1201">Korrektur eines Fehlers, bei dem rename() mit einem nachgestellten Schrägstrich für den Zielnamen fehlschlägt (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1201">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="7a11e-1202">Implementierung der/proc/net/dev-Datei</span><span class="sxs-lookup"><span data-stu-id="7a11e-1202">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="7a11e-1203">Korrektur von Pings mit 0,000 ms aufgrund der Timerauflösung.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1203">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="7a11e-1204">Implementierung von /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1204">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="7a11e-1205">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1205">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1206">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1206">LTP Results:</span></span>
<span data-ttu-id="7a11e-1207">Anzahl bestandener Tests: 664</span><span class="sxs-lookup"><span data-stu-id="7a11e-1207">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="7a11e-1208">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1208">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1209">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1209">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="7a11e-1210">Build 14959</span><span class="sxs-lookup"><span data-stu-id="7a11e-1210">Build 14959</span></span>

<span data-ttu-id="7a11e-1211">Allgemeine Windows-Informationen zu Build 14959 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1211">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1212">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1212">Fixed</span></span>

- <span data-ttu-id="7a11e-1213">Verbesserte Pico-Prozessbenachrichtigung für Windows.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1213">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="7a11e-1214">Weitere Informationen finden Sie im [WSL-Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1214">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="7a11e-1215">Verbesserte Stabilität mit Windows-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="7a11e-1215">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="7a11e-1216">Korrektur von Fehler 0x80070057 beim Starten von „bash.exe“, wenn der Enterprise Data Protection (EDP) aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="7a11e-1216">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="7a11e-1217">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1217">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1218">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1218">LTP Results:</span></span>
<span data-ttu-id="7a11e-1219">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="7a11e-1219">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7a11e-1220">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1220">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1221">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1221">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="7a11e-1222">Build 14955</span><span class="sxs-lookup"><span data-stu-id="7a11e-1222">Build 14955</span></span>

<span data-ttu-id="7a11e-1223">Allgemeine Windows-Informationen zu Build 14955 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1223">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1224">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1224">Fixed</span></span>

 - <span data-ttu-id="7a11e-1225">Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1225">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="7a11e-1226">Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1226">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1227">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1227">LTP Results:</span></span>
<span data-ttu-id="7a11e-1228">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="7a11e-1228">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7a11e-1229">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1229">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1230">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1230">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="7a11e-1231">Build 14951</span><span class="sxs-lookup"><span data-stu-id="7a11e-1231">Build 14951</span></span>

<span data-ttu-id="7a11e-1232">Allgemeine Windows-Informationen zu Build 14951 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1232">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="7a11e-1233">Neues Feature: Windows-/Ubuntu-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="7a11e-1233">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="7a11e-1234">Windows-Binärdateien können jetzt direkt über die WSL-Befehlszeile aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1234">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="7a11e-1235">Dadurch haben Benutzer die Möglichkeit, mit Ihrer Windows-Umgebung und dem -System auf eine Weise zu interagieren, die bisher nicht möglich war.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1235">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="7a11e-1236">Als kurzes Beispiel können Benutzer nun die folgenden Befehle ausführen:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1236">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="7a11e-1237">Weitere Informationen finden Sie hier:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1237">More information can be found at:</span></span>

- [<span data-ttu-id="7a11e-1238">WSL-Teamblog für Interop</span><span class="sxs-lookup"><span data-stu-id="7a11e-1238">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="7a11e-1239">MSDN-Interop-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7a11e-1239">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1240">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1240">Fixed</span></span>

- <span data-ttu-id="7a11e-1241">Ubuntu 16.04 (Xenial) wird jetzt für alle neuen WSL-Instanzen installiert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1241">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="7a11e-1242">Benutzer mit vorhandenen 14.04-Instanzen (Trusty) erhalten kein automatisches Upgrade.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1242">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="7a11e-1243">Das während der Installation festgelegte Gebietsschema wird jetzt angezeigt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1243">Locale set during install is now displayed</span></span>
- <span data-ttu-id="7a11e-1244">Terminalverbesserungen, einschließlich des Fehlers bei der Umleitung eines WSL-Prozesses an eine Datei, funktionieren nicht immer</span><span class="sxs-lookup"><span data-stu-id="7a11e-1244">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="7a11e-1245">Die Konsolenlebensdauer muss an die Lebensdauer von „bash.exe“ gebunden sein</span><span class="sxs-lookup"><span data-stu-id="7a11e-1245">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="7a11e-1246">Die Größe des Konsolenfensters sollte die sichtbare Größe und nicht die Puffergröße verwenden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1246">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="7a11e-1247">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1247">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1248">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1248">LTP Results:</span></span>
<span data-ttu-id="7a11e-1249">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="7a11e-1249">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7a11e-1250">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1250">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1251">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1251">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="7a11e-1252">Build 14946</span><span class="sxs-lookup"><span data-stu-id="7a11e-1252">Build 14946</span></span>

<span data-ttu-id="7a11e-1253">Allgemeine Windows-Informationen zu Build 14946 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1253">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1254">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1254">Fixed</span></span>

- <span data-ttu-id="7a11e-1255">Korrektur eines Problems, das das Erstellen von WSL-Benutzerkonten für Benutzer mit NT-Benutzernamen verhindert hat, die Leerzeichen oder Anführungszeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1255">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="7a11e-1256">Änderung von VolFs und DrvFs, damit 0 für die Verknüpfungsanzahl des Verzeichnisses im Status zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="7a11e-1256">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="7a11e-1257">Unterstützung der IPV6_MULTICAST_HOPS-Socketoption.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1257">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="7a11e-1258">Einschränkung auf eine einzige Konsolen-E/A-Schleife pro TTY.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1258">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="7a11e-1259">Der folgende Befehl ist beispielsweise möglich:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1259">Example: the following command is possible:</span></span>
  - <span data-ttu-id="7a11e-1260">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="7a11e-1260">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="7a11e-1261">Ersetzen von Leerzeichen durch Tabstoppzeichen in /proc/cpuinfo (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1261">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="7a11e-1262">DrvFs wird jetzt in den Einbindungsinformationen mit einem Namen angezeigt, der dem eingebundenen Windows-Volume entspricht</span><span class="sxs-lookup"><span data-stu-id="7a11e-1262">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="7a11e-1263">/home und/root werden nun in den Einbindungsinformationen mit den richtigen Namen angezeigt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1263">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="7a11e-1264">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1264">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1265">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1265">LTP Results:</span></span>
<span data-ttu-id="7a11e-1266">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="7a11e-1266">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7a11e-1267">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1267">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1268">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1268">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="7a11e-1269">Build 14942</span><span class="sxs-lookup"><span data-stu-id="7a11e-1269">Build 14942</span></span>

<span data-ttu-id="7a11e-1270">Allgemeine Windows-Informationen zu Build 14942 finden Sie im [Windows-Blog](https://aka.ms/onefourninefourtwoooooo).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1270">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1271">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1271">Fixed</span></span>

- <span data-ttu-id="7a11e-1272">Eine Reihe von Fehlerüberprüfungen, einschließlich des Netzwerkabsturzes durch „ATTEMPTED EXECUTE OF NOEXECUTE MEMORY“, der SSH blockiert hat</span><span class="sxs-lookup"><span data-stu-id="7a11e-1272">A number of bugchecks addressed, including the "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY" networking crash which was blocking SSH</span></span>
- <span data-ttu-id="7a11e-1273">inotify-Unterstützung für Benachrichtigungen, die von Windows-Anwendungen auf DrvFs generiert werden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1273">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="7a11e-1274">Implementierung von TCP_KEEPIDLE und TCP_KEEPINTVL für mongod.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1274">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="7a11e-1275">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1275">(GH #695)</span></span>
- <span data-ttu-id="7a11e-1276">Implementierung des pivot_root-Systemaufrufs</span><span class="sxs-lookup"><span data-stu-id="7a11e-1276">Implement the pivot_root system call</span></span>
- <span data-ttu-id="7a11e-1277">Implementierung der Socketoption für SO_DONTROUTE</span><span class="sxs-lookup"><span data-stu-id="7a11e-1277">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="7a11e-1278">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1278">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="7a11e-1279">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1279">LTP Results:</span></span>
<span data-ttu-id="7a11e-1280">Anzahl bestandener Tests: 665</span><span class="sxs-lookup"><span data-stu-id="7a11e-1280">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="7a11e-1281">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 263</span><span class="sxs-lookup"><span data-stu-id="7a11e-1281">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="7a11e-1282">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1282">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1283">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1283">Syscall Support</span></span>
<span data-ttu-id="7a11e-1284">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1284">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1285">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1285">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="7a11e-1286">Build 14936</span><span class="sxs-lookup"><span data-stu-id="7a11e-1286">Build 14936</span></span>

<span data-ttu-id="7a11e-1287">Allgemeine Windows-Informationen zu Build 14936 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1287">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="7a11e-1288">Hinweis: WSL wird in einem zukünftigen Release Ubuntu Version 16.04 (Xenial) anstelle von Ubuntu 14.04 (Trusty) installieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1288">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="7a11e-1289">Diese Änderung gilt für Insider, die neue Instanzen installieren (lxrun.exe /install oder erste Ausführung von „bash.exe“).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1289">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="7a11e-1290">Vorhandene Instanzen mit Trusty werden nicht automatisch aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1290">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="7a11e-1291">Benutzer können mit dem Befehl „do-release-upgrade“ Ihr Trusty-Image auf Xenial aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1291">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="7a11e-1292">Bekanntes Problem</span><span class="sxs-lookup"><span data-stu-id="7a11e-1292">Known Issue</span></span>
<span data-ttu-id="7a11e-1293">Bei WSL treten Probleme mit einigen Socketimplementierungen auf.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1293">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="7a11e-1294">Die Fehlerüberprüfung manifestiert sich als Absturz mit dem Fehler „ATTEMPTED EXECUTE OF NOEXECUTE MEMORY“.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1294">The bugcheck manifests itself as a crash with the error "ATTEMPTED EXECUTE OF NOEXECUTE MEMORY".</span></span>  <span data-ttu-id="7a11e-1295">Die häufigste Variante dieses Problems ist ein Absturz bei der Verwendung von SSH.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1295">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="7a11e-1296">Die Ursache ist bei internen Builds korrigiert und wird so bald wie möglich in Insider gepusht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1296">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="7a11e-1297">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1297">Fixed</span></span>

- <span data-ttu-id="7a11e-1298">Der chroot-Systemaufruf wurde implementiert.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1298">Implemented the chroot system call</span></span>
- <span data-ttu-id="7a11e-1299">Verbesserungen in inotify ~~einschließlich Unterstützung für Benachrichtigungen, die von Windows-Anwendungen auf DrvFs generiert werden~~</span><span class="sxs-lookup"><span data-stu-id="7a11e-1299">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="7a11e-1300">Korrektur: Inotify-Unterstützung von Änderungen, die von Windows-Anwendungen stammen, ist zurzeit nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1300">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="7a11e-1301">Die Socketbindung an IPv6::<port n> unterstützt jetzt IPV6_V6ONLY (GH #68, #157, #393, #460, #674, #740, #982, #996)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1301">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="7a11e-1302">Implementierung des WNOWAIT-Verhaltens für den waitid-Systemaufruf (GH #638)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1302">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="7a11e-1303">Unterstützung für IP-Socketoptionen IP_HDRINCL und IP_TTL</span><span class="sxs-lookup"><span data-stu-id="7a11e-1303">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="7a11e-1304">read() der Länge Null sollte sofort zurückgegeben werden (GH #975)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1304">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="7a11e-1305">Ordnungsgemäße Verarbeitung von Dateinamen und Dateinamenpräfixen, die keinen NULL-Terminator in einer TAR-Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1305">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="7a11e-1306">epoll-Unterstützung für/dev/null</span><span class="sxs-lookup"><span data-stu-id="7a11e-1306">epoll support for /dev/null</span></span>
- <span data-ttu-id="7a11e-1307">Korrektur der /dev/alarm-Zeitquelle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1307">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="7a11e-1308">Bash -c kann nun in eine Datei umgeleitet werden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1308">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="7a11e-1309">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1309">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1310">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1310">LTP Results:</span></span>
<span data-ttu-id="7a11e-1311">Anzahl bestandener Tests: 664</span><span class="sxs-lookup"><span data-stu-id="7a11e-1311">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="7a11e-1312">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 264</span><span class="sxs-lookup"><span data-stu-id="7a11e-1312">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="7a11e-1313">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1313">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1314">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1314">Syscall Support</span></span>
<span data-ttu-id="7a11e-1315">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1315">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1316">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1316">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="7a11e-1317">Build 14931</span><span class="sxs-lookup"><span data-stu-id="7a11e-1317">Build 14931</span></span>

<span data-ttu-id="7a11e-1318">Allgemeine Windows-Informationen zu Build 14931 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1318">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1319">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1319">Fixed</span></span>

 - <span data-ttu-id="7a11e-1320">Aufgrund von Umständen, die sich unserer Kontrolle entziehen, gibt es in diesem Build keine Updates für das Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1320">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="7a11e-1321">Regelmäßig geplante Updates werden mit dem nächsten Release fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1321">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="7a11e-1322">Build 14926</span><span class="sxs-lookup"><span data-stu-id="7a11e-1322">Build 14926</span></span>

<span data-ttu-id="7a11e-1323">Allgemeine Windows-Informationen zu Build 14926 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1323">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1324">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1324">Fixed</span></span>

- <span data-ttu-id="7a11e-1325">Ping funktioniert nun in Konsolen, die nicht über Administratorberechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1325">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="7a11e-1326">Ping6 wird jetzt auch ohne Administratorberechtigungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1326">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="7a11e-1327">Inotify-Unterstützung für Dateien, die über WSL geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1327">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="7a11e-1328">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1328">(GH #216)</span></span>
  - <span data-ttu-id="7a11e-1329">Unterstützte Flags:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1329">Flags supported:</span></span>
    - <span data-ttu-id="7a11e-1330">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="7a11e-1330">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="7a11e-1331">inotify_add_watchEreignisse: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="7a11e-1331">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="7a11e-1332">inotify_add_watch-Attribute: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="7a11e-1332">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="7a11e-1333">Lesen der Ausgabe: LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="7a11e-1333">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="7a11e-1334">Bekanntes Problem: Durch das Ändern von Dateien aus Windows-Anwendungen werden keine Ereignisse generiert</span><span class="sxs-lookup"><span data-stu-id="7a11e-1334">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="7a11e-1335">Unix-Socket unterstützt jetzt SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="7a11e-1335">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="7a11e-1336">LTP-Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="7a11e-1336">LTP Results:</span></span>
<span data-ttu-id="7a11e-1337">Anzahl bestandener Tests: 651</span><span class="sxs-lookup"><span data-stu-id="7a11e-1337">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="7a11e-1338">Anzahl nicht bestandener Tests (fehlerhaft, übersprungen usw.): 258</span><span class="sxs-lookup"><span data-stu-id="7a11e-1338">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="7a11e-1339">LTP-Testlaufprotokolle</span><span class="sxs-lookup"><span data-stu-id="7a11e-1339">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="7a11e-1340">Build 14915</span><span class="sxs-lookup"><span data-stu-id="7a11e-1340">Build 14915</span></span>

<span data-ttu-id="7a11e-1341">Allgemeine Windows-Informationen zu Build 14915 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1341">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1342">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1342">Fixed</span></span>
-  <span data-ttu-id="7a11e-1343">Socketpair für Unix-Datagrammsockets (GH #262)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1343">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="7a11e-1344">Unix-Socketunterstützung für SO_REUSEADDR</span><span class="sxs-lookup"><span data-stu-id="7a11e-1344">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="7a11e-1345">Unix-Socketunterstützung für SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1345">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="7a11e-1346">Unix-Socketunterstützung für SOCK_SEQPACKET (GH #758, #546)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1346">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="7a11e-1347">Hinzufügen von Unterstützung für unix datagram socket send, recv und shutdown</span><span class="sxs-lookup"><span data-stu-id="7a11e-1347">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="7a11e-1348">Korrektur einer Fehlerüberprüfung aufgrund einer ungültigen Überprüfung des mmap-Parameters für nicht feste Adressen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1348">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="7a11e-1349">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1349">(GH #847)</span></span>
- <span data-ttu-id="7a11e-1350">Unterstützung für das Anhalten/Fortsetzen von Terminalzuständen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1350">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="7a11e-1351">Unterstützung für TIOCPKT ioctl zum Entsperren des Bildschirmhilfsprogramms (GH #774)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1351">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="7a11e-1352">Bekanntes Problem: Funktionstasten sind nicht funktionsfähig</span><span class="sxs-lookup"><span data-stu-id="7a11e-1352">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="7a11e-1353">Korrektur einer Racebedingung in TimerFd, die dazu führen konnte, dass auf einen freigegebenen Member „ReaderReady“ durch LxpTimerFdWorkerRoutine zugegriffen wurde (GH #814)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1353">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="7a11e-1354">Aktivieren der Unterstützung für erneut startbaren Systemaufruf für futex, poll und clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="7a11e-1354">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="7a11e-1355">Hinzufügen von Unterstützung für Bindungseinbindung</span><span class="sxs-lookup"><span data-stu-id="7a11e-1355">Added bind mount support</span></span>
- <span data-ttu-id="7a11e-1356">Unterstützung für Aufheben der Freigabe für Einbindungsnamespace</span><span class="sxs-lookup"><span data-stu-id="7a11e-1356">unshare for mount namespace support</span></span>
    - <span data-ttu-id="7a11e-1357">Bekanntes Problem: Beim Erstellen eines neuen Einbindngsnamespace mit `unshare(CLONE_NEWNS)` zeigt das aktuelle Arbeitsverzeichnis weiterhin auf den alten Namespace</span><span class="sxs-lookup"><span data-stu-id="7a11e-1357">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="7a11e-1358">Weitere Verbesserungen und Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1358">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="7a11e-1359">Build 14905</span><span class="sxs-lookup"><span data-stu-id="7a11e-1359">Build 14905</span></span>

<span data-ttu-id="7a11e-1360">Allgemeine Windows-Informationen zu Build 14905 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1360">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1361">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1361">Fixed</span></span>
- <span data-ttu-id="7a11e-1362">Erneut startbare Systemaufrufe werden jetzt unterstützt (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1362">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="7a11e-1363">Symbolische Verknüpfungen mit Verzeichnissen, die auf / wenden, sind jetzt funktionstüchtig (GH #650)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1363">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="7a11e-1364">Implementierung von RNDGETENTCNT ioctl für „/dev/random“</span><span class="sxs-lookup"><span data-stu-id="7a11e-1364">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="7a11e-1365">Implementierung der /proc/[pid]/mounts, /proc/[pid]/mountinfo- und /proc/[pid]/mountstats-Dateien</span><span class="sxs-lookup"><span data-stu-id="7a11e-1365">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="7a11e-1366">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1366">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="7a11e-1367">Build 14901</span><span class="sxs-lookup"><span data-stu-id="7a11e-1367">Build 14901</span></span>
<span data-ttu-id="7a11e-1368">Der erste Insider-Build für das Windows 10 Anniversary Update-Release.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1368">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="7a11e-1369">Allgemeine Windows-Informationen zu Build 14901 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1369">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1370">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1370">Fixed</span></span>
- <span data-ttu-id="7a11e-1371">Korrektur eines Problems mit nachfolgenden Schrägstrichen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1371">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="7a11e-1372">Befehle wie `$ mv a/c/ a/b/` funktionieren jetzt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1372">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="7a11e-1373">Installation von Eingabeaufforderungen, wenn das Ubuntu-Gebietsschema auf das Windows-Gebietsschema festgelegt werden soll</span><span class="sxs-lookup"><span data-stu-id="7a11e-1373">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="7a11e-1374">Procfs-Unterstützung für den Ordner „ns“</span><span class="sxs-lookup"><span data-stu-id="7a11e-1374">Procfs support for ns folder</span></span>
- <span data-ttu-id="7a11e-1375">Hinzufügen von „mount“ und „unmount“ für tmpfs-, procfs-und sysfs-Dateisysteme</span><span class="sxs-lookup"><span data-stu-id="7a11e-1375">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="7a11e-1376">Korrektur der 32-Bit-ABI-Signatur von mklod [at]</span><span class="sxs-lookup"><span data-stu-id="7a11e-1376">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="7a11e-1377">Verschieben von Unix-Sockets in Dispatchmodell</span><span class="sxs-lookup"><span data-stu-id="7a11e-1377">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="7a11e-1378">Mit setsockopt festgelegte recv-Puffergröße von INET-Socket muss berücksichtigt werden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1378">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="7a11e-1379">Implementierung des MSG_CMSG_CLOEXEC-Unis-Socket-Empfangsnachrichtenflags</span><span class="sxs-lookup"><span data-stu-id="7a11e-1379">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="7a11e-1380">stdin/stdout-Pipeumleitung des Linux-Prozesses (GH #2)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1380">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="7a11e-1381">Ermöglicht das Weiterleiten von bash -c-Befehlen in CMD.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1381">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="7a11e-1382">Beispiel: >dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="7a11e-1382">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="7a11e-1383">Bash kann nun auf Systemen mit mehreren Auslagerungsdateien installiert werden (GH #538, #358)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1383">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="7a11e-1384">Standardpuffergröße des INET-Sockets sollte mit der Größe des Ubuntu- Standardsetups übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1384">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="7a11e-1385">Ausrichten von xattr-Systemaufrufen an listxattr</span><span class="sxs-lookup"><span data-stu-id="7a11e-1385">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="7a11e-1386">Nur Rückgabe von Schnittstellen mit einer gültigen IPv4-Adresse von SIOCGIFCONF</span><span class="sxs-lookup"><span data-stu-id="7a11e-1386">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="7a11e-1387">Korrektur der Signalatandardaktion, wenn von ptrace eingefügt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1387">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="7a11e-1388">Implementierung von /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="7a11e-1388">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="7a11e-1389">Verwenden der Computerkontext-Registerwerte beim Wiederherstellen von Kontext in sigreturn</span><span class="sxs-lookup"><span data-stu-id="7a11e-1389">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="7a11e-1390">Dadurch wird das Problem behoben, dass Java und javac bei einigen Benutzern nicht mehr reagiert haben</span><span class="sxs-lookup"><span data-stu-id="7a11e-1390">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="7a11e-1391">Implementierung von /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="7a11e-1391">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1392">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1392">Syscall Support</span></span>
<span data-ttu-id="7a11e-1393">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1394">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="7a11e-1395">Update von Build 14388 auf Windows 10 Anniversary Update</span><span class="sxs-lookup"><span data-stu-id="7a11e-1395">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="7a11e-1396">Allgemeine Windows-Informationen zu Build 14388 finden Sie im [Windows-Blog](https://aka.ms/14388wip).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1396">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1397">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1397">Fixed</span></span>
- <span data-ttu-id="7a11e-1398">Korrekturen als Vorbereitung auf das Windows 10 Anniversary Update am 02.08.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1398">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="7a11e-1399">Weitere Informationen zu WSL im Anniversary Update finden Sie in unserem [Blog](https://blogs.msdn.microsoft.com/wsl/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1399">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="7a11e-1400">Build 14376</span><span class="sxs-lookup"><span data-stu-id="7a11e-1400">Build 14376</span></span>
<span data-ttu-id="7a11e-1401">Allgemeine Windows-Informationen zu Build 14376 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1401">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1402">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1402">Fixed</span></span>
- <span data-ttu-id="7a11e-1403">Entfernen einiger Instanzen, in denen apt-get nicht mehr reagiert (GH #493)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1403">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="7a11e-1404">Korrektur eines Problems, bei dem leere Einbindungen nicht ordnungsgemäß verarbeitet wurden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1404">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="7a11e-1405">Korrektur eines Problems, bei dem Ramdisks nicht ordnungsgemäß eingebunden wurden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1405">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="7a11e-1406">Änderung von „unix socket accept“ für die Unterstützung von Flags (Teil von GH #451)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1406">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="7a11e-1407">Korrektur eines allgemeinen netzwerkbezogenen Bluescreens</span><span class="sxs-lookup"><span data-stu-id="7a11e-1407">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="7a11e-1408">Korrektur des Bluescreens beim Zugriff auf /proc/[pid]/task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1408">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="7a11e-1409">Korrektur hoher CPU-Auslastung für einige Pty-Szenarien (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1409">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="7a11e-1410">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1410">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="7a11e-1411">Build 14371</span><span class="sxs-lookup"><span data-stu-id="7a11e-1411">Build 14371</span></span>
<span data-ttu-id="7a11e-1412">Allgemeine Windows-Informationen zu Build 14371 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1412">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1413">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1413">Fixed</span></span>
- <span data-ttu-id="7a11e-1414">Korrektur der Timingracebedingung mit SIGCHLD und wait() bei Verwendung von ptrace</span><span class="sxs-lookup"><span data-stu-id="7a11e-1414">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="7a11e-1415">Korrektur von Verhalten, wenn Pfade ein nachfolgendes Zeichen / aufweisen (GH #432)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1415">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="7a11e-1416">Korrektur eines Problems, bei dem Umbenennen/Aufheben der Verknüpfung aufgrund von geöffneten Handles für untergeordnete Elemente fehlschlägt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1416">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="7a11e-1417">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1417">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="7a11e-1418">Build 14366</span><span class="sxs-lookup"><span data-stu-id="7a11e-1418">Build 14366</span></span>
<span data-ttu-id="7a11e-1419">Allgemeine Windows-Informationen zu Build 14366 finden Sie im [Windows-Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1419">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1420">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1420">Fixed</span></span>
- <span data-ttu-id="7a11e-1421">Korrektur der Dateierstellung durch symbolische Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1421">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="7a11e-1422">Hinzugefügter von listxattr für Python (GH 385)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1422">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="7a11e-1423">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1423">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1424">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1424">Syscall Support</span></span>
-   <span data-ttu-id="7a11e-1425">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1425">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1426">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1426">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="7a11e-1427">Build 14361</span><span class="sxs-lookup"><span data-stu-id="7a11e-1427">Build 14361</span></span>
<span data-ttu-id="7a11e-1428">Allgemeine Windows-Informationen zu Build 14361 finden Sie im [Windows-Blog](https://aka.ms/wip14361).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1428">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1429">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1429">Fixed</span></span>
- <span data-ttu-id="7a11e-1430">Für DrvFs wird nun bei der Ausführung in Bash unter Ubuntu unter Windows die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1430">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="7a11e-1431">Benutzer können case.txt und CASE.TXT auf Ihren /mnt/c-Laufwerken verwenden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1431">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="7a11e-1432">Die Beachtung von Groß-/Kleinschreibung wird nur in Bash unter Ubuntu unter Windows unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1432">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="7a11e-1433">Außerhalb von Bash zeigt NTFS die Dateien richtig an, aber es kann zu unerwartetem Verhalten bei der Interaktion mit den Dateien von Windows kommen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1433">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="7a11e-1434">Für den Stamm der einzelnen Volumes (d.h. /mnt/c) wird die Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1434">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="7a11e-1435">Weitere Informationen zum Verarbeiten dieser Dateien in Windows finden Sie [hier](https://support.microsoft.com/kb/100625).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1435">More information on handling these files in Windows can be found [here](https://support.microsoft.com/kb/100625).</span></span>
- <span data-ttu-id="7a11e-1436">Stark verbesserte PTY-/TTY-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1436">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="7a11e-1437">Anwendungen wie TMUX werden jetzt unterstützt (GH #40)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1437">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="7a11e-1438">Korrektur eines Installationsproblems, bei dem Benutzerkonten nicht immer erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1438">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="7a11e-1439">Optimierte Befehlszeilen-Argumentstruktur, die eine extrem lange Argumentliste zulässt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1439">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="7a11e-1440">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1440">(GH #153)</span></span>
- <span data-ttu-id="7a11e-1441">Jetzt können chmod read_only-Dateien aus DrvFs gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1441">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="7a11e-1442">Korrektur einiger Instanzen, bei denen das Terminal beim Trennen nicht mehr reagiert (GH #43)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1442">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="7a11e-1443">chmod und chown funktionieren jetzt auf TTY-Geräten</span><span class="sxs-lookup"><span data-stu-id="7a11e-1443">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="7a11e-1444">Verbindung mit 0.0.0.0 und :: as localhost zulassen (GH #388)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1444">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="7a11e-1445">Sendmsg/recvmsg verarbeitet nun eine E/A-Vektorlänge > 1 (Teil von GH #376)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1445">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="7a11e-1446">Benutzer können jetzt die automatisch generierte Hostdatei ablehnen (GH #398)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1446">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="7a11e-1447">Automatisches Zuordnen des Linux-Gebietsschemas zum NT-Gebietsschema während der Installation (GH #11)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1447">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="7a11e-1448">Hinzufügen der /proc/sys/vm/swappiness-Datei (GH #306)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1448">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="7a11e-1449">strace wird jetzt ordnungsgemäß beendet</span><span class="sxs-lookup"><span data-stu-id="7a11e-1449">strace now exits correctly</span></span>
- <span data-ttu-id="7a11e-1450">Ermöglichen des erneuten Öffnens von Pipes über /proc/self/fd (GH #222)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1450">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="7a11e-1451">Ausblenden von Verzeichnissen unter „%LOCALAPPDATA%\lxss“ aus DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1451">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="7a11e-1452">Bessere Verarbeitung von bash.exe ~.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1452">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="7a11e-1453">Befehle wie „bash ~ -c ls“ werden jetzt unterstützt (GH #467)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1453">Commands like "bash ~ -c ls" now supported (GH #467)</span></span>
- <span data-ttu-id="7a11e-1454">Sockets benachrichtigen nun darüber, dass epoll read beim Herunterfahren verfügbar ist (GH #271)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1454">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="7a11e-1455">lxrun/uninstall arbeitet besser beim Löschen der Dateien und Ordner.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1455">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="7a11e-1456">Korrektur für ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1456">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="7a11e-1457">Verbesserte Unterstützung für X11-Apps, z.B. xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1457">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="7a11e-1458">Aktualisierte anfängliche Threadstapelgröße, um der standardmäßigen Ubuntu-Einstellung zu entsprechen und die Größe ordnungsgemäß an den get_rlimit-Systemaufruf zu melden (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1458">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="7a11e-1459">Verbesserte Berichterstellung von Pico-Prozessimagenamen (z.B. für die Überwachung)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1459">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="7a11e-1460">Implementierung von /proc/mountinfo für df-Befehl</span><span class="sxs-lookup"><span data-stu-id="7a11e-1460">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="7a11e-1461">Korrektur des Fehlercodes der symbolischen Verknüpfung für den untergeordneten Namen .</span><span class="sxs-lookup"><span data-stu-id="7a11e-1461">Fixed symlink error code for child name .</span></span> <span data-ttu-id="7a11e-1462">und .</span><span class="sxs-lookup"><span data-stu-id="7a11e-1462">and ..</span></span>
- <span data-ttu-id="7a11e-1463">Weitere optimierende Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1463">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1464">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1464">Syscall Support</span></span>
<span data-ttu-id="7a11e-1465">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1465">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1466">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1466">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="7a11e-1467">Build 14352</span><span class="sxs-lookup"><span data-stu-id="7a11e-1467">Build 14352</span></span>
<span data-ttu-id="7a11e-1468">Allgemeine Windows-Informationen zu Build 14352 finden Sie im [Windows-Blog](https://aka.ms/wip14352).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1468">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1469">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1469">Fixed</span></span>
- <span data-ttu-id="7a11e-1470">Korrektur eines Problems, bei dem große Dateien nicht ordnungsgemäß heruntergeladen bzw. ordnungsgemäß erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1470">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="7a11e-1471">Dadurch sollte die Blockierung von npm und anderen Szenarien aufgehoben werden (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1471">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="7a11e-1472">Entfernen einiger Instanzen, in denen Sockets nicht mehr reagieren</span><span class="sxs-lookup"><span data-stu-id="7a11e-1472">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="7a11e-1473">Korrektur einiger ptrace-Fehler</span><span class="sxs-lookup"><span data-stu-id="7a11e-1473">Corrected some ptrace errors</span></span>
- <span data-ttu-id="7a11e-1474">Korrektur eines Problems, bei dem WSL Dateinamen mit mehr als 255 Zeichen zuließ</span><span class="sxs-lookup"><span data-stu-id="7a11e-1474">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="7a11e-1475">Verbesserte Unterstützung nicht-englischer Zeichen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1475">Improved support for non-English characters</span></span>
- <span data-ttu-id="7a11e-1476">Hinzufügen aktueller Windows-Zeitzonendaten und Festlegen als Standard</span><span class="sxs-lookup"><span data-stu-id="7a11e-1476">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="7a11e-1477">Eindeutige Geräte-IDs für jeden Einbindungspunkt (jre-Korrektur – GH #49)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1477">Unique device id's for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="7a11e-1478">Korrektur eines Problems mit Pfaden, die „.“ und „..“ enthalten</span><span class="sxs-lookup"><span data-stu-id="7a11e-1478">Correct issue with paths containing "." and ".."</span></span>
- <span data-ttu-id="7a11e-1479">Hinzufügen von FIFO-Unterstützung (GH #71)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1479">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="7a11e-1480">Aktualisiertes Format von „resolv.conf“ entsprechend dem nativen Ubuntu-Format</span><span class="sxs-lookup"><span data-stu-id="7a11e-1480">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="7a11e-1481">procfs-Bereinigung</span><span class="sxs-lookup"><span data-stu-id="7a11e-1481">Some procfs cleanup</span></span>
- <span data-ttu-id="7a11e-1482">Aktivierten von Ping für Administratorkonsolen (GH #18)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1482">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1483">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1483">Syscall Support</span></span>
<span data-ttu-id="7a11e-1484">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1484">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1485">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1485">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="7a11e-1486">Build 14342</span><span class="sxs-lookup"><span data-stu-id="7a11e-1486">Build 14342</span></span>
<span data-ttu-id="7a11e-1487">Allgemeine Windows-Informationen zu Build 14342 finden Sie im [Windows-Blog](https://aka.ms/wip14342).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1487">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="7a11e-1488">Informationen zu VolFs und DriveFs finden Sie im [WSL-Blog](https://blogs.msdn.microsoft.com/wsl).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1488">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="7a11e-1489">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1489">Fixed</span></span>
- <span data-ttu-id="7a11e-1490">Korrektur eines Installationsproblems, wenn der Windows-Benutzer Unicode-Zeichen im Benutzernamen enthielt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1490">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="7a11e-1491">Die Problemumgehung „apt-get update udev“ in den FAQ wird jetzt standardmäßig bei der ersten Ausführung bereitgestellt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1491">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="7a11e-1492">Aktivierte symbolische Verknüpfungen in DriveFs-Verzeichnissen (/mnt/<drive>)</span><span class="sxs-lookup"><span data-stu-id="7a11e-1492">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="7a11e-1493">Symbolische Verknüpfungen funktionieren nun zwischen DriveFs und VolFs</span><span class="sxs-lookup"><span data-stu-id="7a11e-1493">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="7a11e-1494">Korrektur des Pfadanalyseproblems auf oberster Ebene: ls .// funktioniert jetzt wie erwartet</span><span class="sxs-lookup"><span data-stu-id="7a11e-1494">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="7a11e-1495">npm install auf DriveFs und die -g-Optionen funktionieren jetzt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1495">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="7a11e-1496">Korrektur eines Problems, das den Start des PHP-Servers verhinderte</span><span class="sxs-lookup"><span data-stu-id="7a11e-1496">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="7a11e-1497">Aktualisierte Standardumgebungswerte, z.B. $PATH, um nativem Ubuntu besser zu entsprechen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1497">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="7a11e-1498">Hinzufügen eines wöchentlichen Wartungstasks in Windows zum Aktualisieren des apt-Paketcaches</span><span class="sxs-lookup"><span data-stu-id="7a11e-1498">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="7a11e-1499">Korrektur eines Problems bei der Überprüfung von ELF-Headern, WSL unterstützt jetzt alle Melkor-Optionen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1499">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="7a11e-1500">Zsh-Shell ist funktionsfähig</span><span class="sxs-lookup"><span data-stu-id="7a11e-1500">Zsh shell is functional</span></span>
- <span data-ttu-id="7a11e-1501">Vorkompilierte Go-Binärdateien werden jetzt unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1501">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="7a11e-1502">Eingabeaufforderung bei der ersten Ausführung von „bash.exe“ ist nun richtig lokalisiert</span><span class="sxs-lookup"><span data-stu-id="7a11e-1502">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="7a11e-1503">/proc/meminfo gibt jetzt richtige Informationen zurück</span><span class="sxs-lookup"><span data-stu-id="7a11e-1503">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="7a11e-1504">Sockets werden jetzt in VFS unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1504">Sockets now supported in VFS</span></span>
- <span data-ttu-id="7a11e-1505">/dev jetzt als tempfs eingebunden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1505">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="7a11e-1506">Fifo wird jetzt unterstützt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1506">Fifo now supported</span></span>
- <span data-ttu-id="7a11e-1507">Mehrkernsysteme werden nun ordnungsgemäß in /proc/cpuinfo angezeigt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1507">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="7a11e-1508">Weitere Verbesserungen und Fehlermeldungen, die während der ersten Ausführung heruntergeladen werden</span><span class="sxs-lookup"><span data-stu-id="7a11e-1508">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="7a11e-1509">Systemaufrufverbesserungen und -fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1509">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="7a11e-1510">Unterstützte Systemaufrufliste unten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1510">Supported syscall list below.</span></span>
- <span data-ttu-id="7a11e-1511">Weitere Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1511">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="7a11e-1512">Bekannte Probleme</span><span class="sxs-lookup"><span data-stu-id="7a11e-1512">Known Issues</span></span>
- <span data-ttu-id="7a11e-1513">„.“ wird in einigen Fällen nicht</span><span class="sxs-lookup"><span data-stu-id="7a11e-1513">Not resolving '..'</span></span> <span data-ttu-id="7a11e-1514">ordnungsgemäß auf DriveFs aufgelöst</span><span class="sxs-lookup"><span data-stu-id="7a11e-1514">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1515">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1515">Syscall Support</span></span>
<span data-ttu-id="7a11e-1516">Im folgenden finden Sie eine Liste der neuen oder verbesserten Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1516">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1517">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1517">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="7a11e-1518">Build 14332</span><span class="sxs-lookup"><span data-stu-id="7a11e-1518">Build 14332</span></span>

<span data-ttu-id="7a11e-1519">Allgemeine Windows-Informationen zu Build 14332 finden Sie im [Windows-Blog](https://aka.ms/wip14332).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1519">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="7a11e-1520">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1520">Fixed</span></span>
- <span data-ttu-id="7a11e-1521">Bessere resolv.conf-Generierung einschließlich Priorisieren von DNS-Einträgen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1521">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="7a11e-1522">Problem beim Verschieben von Dateien und Verzeichnissen zwischen/mnt- und Nicht-/mnt-Laufwerken</span><span class="sxs-lookup"><span data-stu-id="7a11e-1522">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="7a11e-1523">TAR-Dateien können jetzt mit symbolischen Verknüpfungen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1523">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="7a11e-1524">Hinzufügen des /run/lock-Standardverzeichnisses bei der Instanzerstellung</span><span class="sxs-lookup"><span data-stu-id="7a11e-1524">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="7a11e-1525">Aktualisieren von /dev/null, um die richtigen Statusinformationen zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="7a11e-1525">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="7a11e-1526">Weitere Fehler beim Herunterladen während der ersten Ausführung</span><span class="sxs-lookup"><span data-stu-id="7a11e-1526">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="7a11e-1527">Systemaufrufverbesserungen und -fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1527">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="7a11e-1528">Unterstützte Systemaufrufliste unten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1528">Supported syscall list below.</span></span>
- <span data-ttu-id="7a11e-1529">Weitere optimierende Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1529">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1530">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1530">Syscall Support</span></span>
<span data-ttu-id="7a11e-1531">Im folgenden finden Sie den neuen Systemaufruf, der in WSL implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1531">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="7a11e-1532">Der Systemaufruf in dieser Liste wird in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1532">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="7a11e-1533">Build 14328</span><span class="sxs-lookup"><span data-stu-id="7a11e-1533">Build 14328</span></span>

<span data-ttu-id="7a11e-1534">Allgemeine Windows-Informationen zu Build 14332 finden Sie im [Windows-Blog](https://aka.ms/wip14328).</span><span class="sxs-lookup"><span data-stu-id="7a11e-1534">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="7a11e-1535">Neue Funktionen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1535">New Features</span></span>
* <span data-ttu-id="7a11e-1536">Jetzt werden Linux-Benutzer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1536">Now support Linux users.</span></span>  <span data-ttu-id="7a11e-1537">Bei der Installation von Bash unter Ubuntu unter Windows werden Sie aufgefordert, einen Linux-Benutzer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1537">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="7a11e-1538">Weitere Informationen finden Sie unter https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1538">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="7a11e-1539">Der Hostname ist jetzt auf den Windows-Computernamen festgelegt, nicht mehr auf @localhost</span><span class="sxs-lookup"><span data-stu-id="7a11e-1539">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="7a11e-1540">Weitere Informationen zu Build 14328 finden Sie unter: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="7a11e-1540">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="7a11e-1541">Fest</span><span class="sxs-lookup"><span data-stu-id="7a11e-1541">Fixed</span></span>
* <span data-ttu-id="7a11e-1542">Verbesserungen von symbolischen Verknüpfungen für Nicht-/mnt/<drive>-Dateien</span><span class="sxs-lookup"><span data-stu-id="7a11e-1542">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="7a11e-1543">Die npm-Installation funktioniert jetzt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1543">npm install now works</span></span>
    * <span data-ttu-id="7a11e-1544">jdk/jre kann nun mithilfe der Anweisungen installiert werden, die Sie [hier](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html) finden.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1544">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="7a11e-1545">Bekanntes Problem: Symbolische Verknüpfungen funktionieren für Windows-Einbindungen nicht.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1545">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="7a11e-1546">Diese Funktionen werden in einem späteren Build verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1546">Functionality will be available in a later build</span></span>
* <span data-ttu-id="7a11e-1547">top und htop werden jetzt angezeigt</span><span class="sxs-lookup"><span data-stu-id="7a11e-1547">top and htop now display</span></span>
* <span data-ttu-id="7a11e-1548">Zusätzliche Fehlermeldungen bei einigen Installationsfehlern</span><span class="sxs-lookup"><span data-stu-id="7a11e-1548">Additional error messages for some install failures</span></span>
* <span data-ttu-id="7a11e-1549">Systemaufrufverbesserungen und -fehlerbehebungen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1549">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="7a11e-1550">Unterstützte Systemaufrufliste unten.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1550">Supported syscall list below.</span></span>
* <span data-ttu-id="7a11e-1551">Weitere optimierende Fehlerbehebungen und Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1551">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="7a11e-1552">Unterstützung von Systemaufrufen</span><span class="sxs-lookup"><span data-stu-id="7a11e-1552">Syscall Support</span></span>
<span data-ttu-id="7a11e-1553">Im folgenden finden Sie eine Liste der Systemaufrufe, die einige Implementierungen in WSL aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1553">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="7a11e-1554">Die Systemaufrufe in dieser Liste werden in mindestens einem Szenario unterstützt, aber möglicherweise werden zurzeit nicht alle Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7a11e-1554">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
