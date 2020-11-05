---
title: Verwalten von Linux-Distributionen
description: Referenzliste und Konfigurieren mehrerer Linux-Distributionen, die unter dem Windows-Subsystem für Linux ausgeführt werden.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 05/12/2020
ms.topic: article
ms.openlocfilehash: 2a26795821162e91cb87825483426cd58aab8ac6
ms.sourcegitcommit: cc81ebc749cf84dd58e9f57ee4cc72b5c72be1fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "93352663"
---
# <a name="wsl-commands-and-launch-configurations"></a><span data-ttu-id="f988c-104">WSL-Befehle und Start Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="f988c-104">WSL commands and launch configurations</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="f988c-105">Möglichkeiten zum Ausführen von WSL</span><span class="sxs-lookup"><span data-stu-id="f988c-105">Ways to run WSL</span></span>

<span data-ttu-id="f988c-106">Es gibt mehrere Möglichkeiten, eine Linux-Distribution mit WSL auszuführen, nachdem Sie [installiert](install-win10.md)wurde.</span><span class="sxs-lookup"><span data-stu-id="f988c-106">There are several ways to run a Linux distribution with WSL once it's [installed](install-win10.md).</span></span>

1. <span data-ttu-id="f988c-107">Öffnen Sie die Linux-Distribution, indem Sie im Windows-Startmenü den Namen der installierten Verteilungen eingeben.</span><span class="sxs-lookup"><span data-stu-id="f988c-107">Open your Linux distribution by visiting the Windows Start menu and typing the name of your installed distributions.</span></span> <span data-ttu-id="f988c-108">Beispiel: "Ubuntu".</span><span class="sxs-lookup"><span data-stu-id="f988c-108">For example: "Ubuntu".</span></span>
2. <span data-ttu-id="f988c-109">Geben Sie an der Windows-Eingabeaufforderung oder in PowerShell den Namen der installierten Distribution ein.</span><span class="sxs-lookup"><span data-stu-id="f988c-109">From Windows Command Prompt or PowerShell, enter the name of your installed distribution.</span></span> <span data-ttu-id="f988c-110">Beispiel: `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="f988c-110">For example: `ubuntu`</span></span>
3. <span data-ttu-id="f988c-111">Geben Sie an der Windows-Eingabeaufforderung oder PowerShell Folgendes ein, um die Standard-Linux-Distribution in der aktuellen Befehlszeile zu öffnen: `wsl.exe` .</span><span class="sxs-lookup"><span data-stu-id="f988c-111">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter: `wsl.exe`.</span></span>
4. <span data-ttu-id="f988c-112">Geben Sie an der Windows-Eingabeaufforderung oder PowerShell Folgendes ein, um die Standard-Linux-Distribution in der aktuellen Befehlszeile zu öffnen: `wsl [command]` .</span><span class="sxs-lookup"><span data-stu-id="f988c-112">From Windows Command Prompt or PowerShell, to open your default Linux distribution inside your current command line, enter:`wsl [command]`.</span></span>

<span data-ttu-id="f988c-113">Welche Methode Sie verwenden sollten, hängt vom Anwendungsfall ab.</span><span class="sxs-lookup"><span data-stu-id="f988c-113">Which method you should use depends on what you're doing.</span></span> <span data-ttu-id="f988c-114">Wenn Sie in einer Windows-Eingabeaufforderung oder einem PowerShell-Fenster eine WSL-Befehlszeile geöffnet haben und den Vorgang beenden möchten, geben Sie den folgenden Befehl ein: `exit` .</span><span class="sxs-lookup"><span data-stu-id="f988c-114">If you've opened a WSL command line within a Windows Prompt or PowerShell window and want to exit, enter the command: `exit`.</span></span>

## <a name="launch-wsl-by-distribution"></a><span data-ttu-id="f988c-115">Starten von WSL nach Distribution</span><span class="sxs-lookup"><span data-stu-id="f988c-115">Launch WSL by distribution</span></span>

<span data-ttu-id="f988c-116">Durch das Ausführen einer Distribution mit ihrer distributionsspezifischen Anwendung wird diese Distribution in einem eigenen Konsolenfenster gestartet.</span><span class="sxs-lookup"><span data-stu-id="f988c-116">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![Starten von WSL aus dem Startmenü](media/start-launch.png)

<span data-ttu-id="f988c-118">Dies entspricht dem Klicken auf „Starten“ im Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="f988c-118">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![Starten von WSL aus dem Microsoft Store](media/store-launch.png)

<span data-ttu-id="f988c-120">Sie können die Distribution auch über die Befehlszeile ausführen, indem Sie `[distribution].exe` ausführen.</span><span class="sxs-lookup"><span data-stu-id="f988c-120">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="f988c-121">Der Nachteil, eine Distribution auf diese Weise über die Befehlszeile auszuführen, besteht darin, dass sich Ihr Arbeitsverzeichnis automatisch aus dem aktuellen Verzeichnis in das Startverzeichnis der Distribution ändert.</span><span class="sxs-lookup"><span data-stu-id="f988c-121">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="f988c-122">**Beispiel: (mithilfe von PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f988c-122">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="f988c-123">wsl und wsl [Befehl]</span><span class="sxs-lookup"><span data-stu-id="f988c-123">wsl and wsl [command]</span></span>

<span data-ttu-id="f988c-124">Die beste Methode zum Ausführen von WSL über die Befehlszeile ist die Verwendung von `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="f988c-124">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="f988c-125">**Beispiel: (mithilfe von PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f988c-125">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="f988c-126">`wsl` behält nicht nur das aktuelle Arbeitsverzeichnis bei, sondern ermöglicht es auch, einen einzelnen Befehl neben Windows-Befehlen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f988c-126">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="f988c-127">**Beispiel: (mithilfe von PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f988c-127">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:55:47 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:56:57 DST 2018
```

<span data-ttu-id="f988c-128">**Beispiel: (mithilfe von PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f988c-128">**Example: (using PowerShell)**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```

## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="f988c-129">Verwalten mehrerer Linux-Distributionen</span><span class="sxs-lookup"><span data-stu-id="f988c-129">Managing multiple Linux Distributions</span></span>

<span data-ttu-id="f988c-130">In Windows 10, Version 1903 [und](ms-settings:windowsupdate)höher, können Sie verwenden, `wsl.exe` um die Verteilungen im Windows-Subsystem für Linux (WSL) zu verwalten, einschließlich der Auflistung verfügbarer Verteilungen, der Festlegung einer Standardverteilung und der Deinstallieren von Verteilungen.</span><span class="sxs-lookup"><span data-stu-id="f988c-130">In Windows 10 Version 1903 [and later](ms-settings:windowsupdate), you can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="f988c-131">Jede Linux-Distribution verwaltet unabhängig ihre eigenen Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f988c-131">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="f988c-132">Führen Sie `[distro.exe] /?` aus, um distributionsspezifische Befehle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f988c-132">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="f988c-133">Beispiel: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="f988c-133">For example `ubuntu /?`.</span></span>

## <a name="list-distributions"></a><span data-ttu-id="f988c-134">Auflisten von Distributionen</span><span class="sxs-lookup"><span data-stu-id="f988c-134">List distributions</span></span>

<span data-ttu-id="f988c-135">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="f988c-135">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="f988c-136">Listet verfügbare Linux-Distributionen für WSL auf.</span><span class="sxs-lookup"><span data-stu-id="f988c-136">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="f988c-137">Wenn eine Distribution aufgeführt wird, ist sie installiert und einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="f988c-137">If a distribution is listed, it's installed and ready to use.</span></span>

<span data-ttu-id="f988c-138">`wsl --list --all` Listet alle Verteilungen auf, einschließlich derjenigen, die derzeit nicht verwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="f988c-138">`wsl --list --all` Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="f988c-139">Sie werden möglicherweise gerade installiert, deinstalliert oder sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="f988c-139">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="f988c-140">`wsl --list --running` Listet alle Verteilungen auf, die zurzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-140">`wsl --list --running` Lists all distributions that are currently running.</span></span>

## <a name="set-a-default-distribution"></a><span data-ttu-id="f988c-141">Festlegen einer Standarddistribution</span><span class="sxs-lookup"><span data-stu-id="f988c-141">Set a default distribution</span></span>

<span data-ttu-id="f988c-142">Die WSL-Standarddistribution ist die Distribution, die ausgeführt wird, wenn Sie `wsl` in einer Befehlszeile ausführen.</span><span class="sxs-lookup"><span data-stu-id="f988c-142">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="f988c-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="f988c-143">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="f988c-144">Legt die Standarddistribution auf `<DistributionName>` fest.</span><span class="sxs-lookup"><span data-stu-id="f988c-144">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="f988c-145">**Beispiel: (mithilfe von PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f988c-145">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="f988c-146">`wsl -s Ubuntu` würde die Standarddistribution auf Ubuntu festlegen.</span><span class="sxs-lookup"><span data-stu-id="f988c-146">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="f988c-147">Wenn jetzt `wsl npm init` ausgeführt wird, wird Ubuntu ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f988c-147">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="f988c-148">Wenn `wsl` ausgeführt wird, wird eine Ubuntu-Sitzung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f988c-148">If I run `wsl` it will open an Ubuntu session.</span></span>

## <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="f988c-149">Aufheben der Registrierung und Neuinstallation einer Distribution</span><span class="sxs-lookup"><span data-stu-id="f988c-149">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="f988c-150">Obwohl Linux-Distributionen über den Microsoft Store installiert werden können, können Sie nicht über den Store deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-150">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="f988c-151">WSL Config ermöglicht die Aufhebung der Registrierung/Deinstallation von Distributionen.</span><span class="sxs-lookup"><span data-stu-id="f988c-151">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="f988c-152">Durch das Aufheben der Registrierung können Distributionen auch erneut installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-152">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="f988c-153">**Vorsicht:** Nachdem die Registrierung aufgehoben wurde, gehen alle Daten, Einstellungen und Software, die dieser Verteilung zugeordnet sind, dauerhaft verloren.</span><span class="sxs-lookup"><span data-stu-id="f988c-153">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="f988c-154">Bei der erneuten Installation aus dem Store wird eine saubere Kopie der Distribution installiert.</span><span class="sxs-lookup"><span data-stu-id="f988c-154">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="f988c-155">Hebt die Registrierung der Distribution bei WSL auf, damit Sie erneut installiert oder bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f988c-155">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="f988c-156">Beispiel: `wsl --unregister Ubuntu` würde Ubuntu aus den in WSL verfügbaren Distributionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="f988c-156">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="f988c-157">Beim Ausführen von `wsl --list` würde diese Distribution nicht aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f988c-157">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="f988c-158">Zum erneuten Installieren suchen Sie die Distribution im Microsoft Store, und wählen Sie dann „Starten“ aus.</span><span class="sxs-lookup"><span data-stu-id="f988c-158">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="run-as-a-specific-user"></a><span data-ttu-id="f988c-159">Ausführen als ein bestimmter Benutzer</span><span class="sxs-lookup"><span data-stu-id="f988c-159">Run as a specific user</span></span>

<span data-ttu-id="f988c-160">`wsl -u <Username>`, `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="f988c-160">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="f988c-161">Führen Sie WSL als der angegebene Benutzer aus.</span><span class="sxs-lookup"><span data-stu-id="f988c-161">Run WSL as the specified user.</span></span> <span data-ttu-id="f988c-162">Beachten Sie, dass der Benutzer in der WSL-Distribution vorhanden sein muss.</span><span class="sxs-lookup"><span data-stu-id="f988c-162">Please note that user must exist inside of the WSL distribution.</span></span>

## <a name="change-the-default-user-for-a-distribution"></a><span data-ttu-id="f988c-163">Ändern des Standard Benutzers für eine Distribution</span><span class="sxs-lookup"><span data-stu-id="f988c-163">Change the default user for a distribution</span></span>

`<DistributionName> config --default-user <Username>`

<span data-ttu-id="f988c-164">Ändern Sie den Standardbenutzer für Ihre Verteilungs Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="f988c-164">Change the default user that for your distribution log-in.</span></span> <span data-ttu-id="f988c-165">Der Benutzer muss bereits innerhalb der Verteilung vorhanden sein, damit er der Standardbenutzer wird.</span><span class="sxs-lookup"><span data-stu-id="f988c-165">The user has to already exist inside the distribution in order to become the default user.</span></span> 

<span data-ttu-id="f988c-166">Beispiel: `ubuntu config --default-user johndoe` würde den Standardbenutzer für die Ubuntu-Distribution in den Benutzer "JohnDoe" ändern.</span><span class="sxs-lookup"><span data-stu-id="f988c-166">For example: `ubuntu config --default-user johndoe` would change the default user for the Ubuntu distribution to the "johndoe" user.</span></span>

> [!NOTE]
> <span data-ttu-id="f988c-167">Wenn Sie Probleme haben, den Namen der Verteilung herauszufinden, finden Sie weitere Informationen unter [Auflisten von Verteilungen](#list-distributions) für den Befehl zum Auflisten des offiziellen Namens der installierten Verteilungen.</span><span class="sxs-lookup"><span data-stu-id="f988c-167">If you are having trouble figuring out the name of your distribution, see [List distributions](#list-distributions) for the command to list the official name of the installed distributions.</span></span> 

## <a name="run-a-specific-distribution"></a><span data-ttu-id="f988c-168">Ausführen als eine bestimmte Distribution</span><span class="sxs-lookup"><span data-stu-id="f988c-168">Run a specific distribution</span></span>

<span data-ttu-id="f988c-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="f988c-169">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="f988c-170">Führen Sie eine angegebene Distribution von WSL aus. Kann zum Senden von Befehlen an eine bestimmte Distribution verwendet werden, ohne die Standardeinstellung ändern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f988c-170">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

## <a name="managing-multiple-linux-distributions-in-earlier-windows-versions"></a><span data-ttu-id="f988c-171">Verwalten von mehreren Linux-Distributionen in früheren Windows-Versionen</span><span class="sxs-lookup"><span data-stu-id="f988c-171">Managing multiple Linux Distributions in earlier Windows versions</span></span>

<span data-ttu-id="f988c-172">In Windows 10 vor Version 1903 sollte das Befehlszeilen Tool WSL config ( `wslconfig.exe` ) zum Verwalten von Linux-Distributionen verwendet werden, die unter dem Windows-Subsystem für Linux (WSL) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-172">In Windows 10 prior to version 1903, the WSL Config (`wslconfig.exe`) command-line tool should be used to manage Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="f988c-173">Damit können Sie verfügbare Distributionen auflisten, eine Standarddistribution festlegen und Distributionen deinstallieren.</span><span class="sxs-lookup"><span data-stu-id="f988c-173">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="f988c-174">Während WSL Config für Einstellungen nützlich ist, die Distributionen umspannen oder koordinieren, verwaltet jede Linux-Distribution unabhängig ihre eigenen Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="f988c-174">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="f988c-175">Führen Sie `[distro.exe] /?` aus, um distributionsspezifische Befehle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f988c-175">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="f988c-176">Beispiel: `ubuntu /?`.</span><span class="sxs-lookup"><span data-stu-id="f988c-176">For example `ubuntu /?`.</span></span>

<span data-ttu-id="f988c-177">Um alle verfügbaren Optionen für wslconfig anzuzeigen, führen Sie Folgendes aus: `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="f988c-177">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

<span data-ttu-id="f988c-178">Zum Auflisten von Verteilungen verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f988c-178">To list distributions, use:</span></span>

`wslconfig /list`  
<span data-ttu-id="f988c-179">Listet verfügbare Linux-Distributionen für WSL auf.</span><span class="sxs-lookup"><span data-stu-id="f988c-179">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="f988c-180">Wenn eine Distribution aufgeführt wird, ist sie installiert und einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="f988c-180">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="f988c-181">Listet alle Distributionen auf, einschließlich derjenigen, die zurzeit nicht verwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="f988c-181">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="f988c-182">Sie werden möglicherweise gerade installiert, deinstalliert oder sind beschädigt.</span><span class="sxs-lookup"><span data-stu-id="f988c-182">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

<span data-ttu-id="f988c-183">So legen Sie eine Standardverteilung fest, die ausgeführt wird, wenn Sie `wsl` in einer Befehlszeile ausführen:</span><span class="sxs-lookup"><span data-stu-id="f988c-183">To set a default distribution that runs when you run `wsl` on a command line:</span></span>

<span data-ttu-id="f988c-184">`wslconfig /setdefault <DistributionName>` Legt die Standardverteilung auf fest `<DistributionName>` .</span><span class="sxs-lookup"><span data-stu-id="f988c-184">`wslconfig /setdefault <DistributionName>` Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="f988c-185">**Beispiel: (mithilfe von PowerShell)**</span><span class="sxs-lookup"><span data-stu-id="f988c-185">**Example: (using PowerShell)**</span></span>  
<span data-ttu-id="f988c-186">`wslconfig /setdefault Ubuntu` würde die Standarddistribution auf Ubuntu festlegen.</span><span class="sxs-lookup"><span data-stu-id="f988c-186">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="f988c-187">Wenn jetzt `wsl npm init` ausgeführt wird, wird Ubuntu ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f988c-187">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="f988c-188">Wenn `wsl` ausgeführt wird, wird eine Ubuntu-Sitzung geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f988c-188">If I run `wsl` it will open an Ubuntu session.</span></span>

<span data-ttu-id="f988c-189">So heben Sie die Registrierung und die erneute Installation einer Verteilung auf:</span><span class="sxs-lookup"><span data-stu-id="f988c-189">To unregister and reinstall a distribution:</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="f988c-190">Hebt die Registrierung der Distribution bei WSL auf, damit Sie erneut installiert oder bereinigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="f988c-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="f988c-191">Beispiel: `wslconfig /unregister Ubuntu` würde Ubuntu aus den in WSL verfügbaren Distributionen entfernen.</span><span class="sxs-lookup"><span data-stu-id="f988c-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="f988c-192">Beim Ausführen von `wslconfig /list` würde diese Distribution nicht aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f988c-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="f988c-193">Zum erneuten Installieren suchen Sie die Distribution im Microsoft Store, und wählen Sie dann „Starten“ aus.</span><span class="sxs-lookup"><span data-stu-id="f988c-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="configure-per-distro-launch-settings-with-wslconf"></a><span data-ttu-id="f988c-194">Konfigurieren von pro-Distribution-Start Einstellungen mit wslconf</span><span class="sxs-lookup"><span data-stu-id="f988c-194">Configure per distro launch settings with wslconf</span></span>

> <span data-ttu-id="f988c-195">**Verfügbar in Windows Build 17093 und höher**</span><span class="sxs-lookup"><span data-stu-id="f988c-195">**Available in Windows Build 17093 and later**</span></span>

<span data-ttu-id="f988c-196">Konfigurieren Sie automatisch bestimmte Funktionen in WSL, die jedes Mal angewendet werden, wenn Sie das Subsystem mithilfe von `wsl.conf` starten.</span><span class="sxs-lookup"><span data-stu-id="f988c-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span>

<span data-ttu-id="f988c-197">Zurzeit umfasst dies Optionen für die automatische Einbindung und Netzwerkkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="f988c-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="f988c-198">`wsl.conf` befindet sich in jeder Linux-Distribution in `/etc/wsl.conf`.</span><span class="sxs-lookup"><span data-stu-id="f988c-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="f988c-199">Wenn die Datei nicht vorhanden ist, können Sie sie selbst erstellen.</span><span class="sxs-lookup"><span data-stu-id="f988c-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="f988c-200">WSL erkennt das Vorhandensein der Datei und liest ihren Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f988c-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="f988c-201">Wenn die Datei fehlt oder falsch formatiert ist (d.h. falsche Markupformatierung), wird WSL weiterhin normal gestartet.</span><span class="sxs-lookup"><span data-stu-id="f988c-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="f988c-202">Im folgenden finden Sie eine Beispiel `wsl.conf` Datei, die Sie Ihren Verteilungen hinzufügen können:</span><span class="sxs-lookup"><span data-stu-id="f988c-202">Here is a sample `wsl.conf` file you could add into your distributions:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we'll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="f988c-203">Konfigurationsoptionen</span><span class="sxs-lookup"><span data-stu-id="f988c-203">Configuration Options</span></span>

<span data-ttu-id="f988c-204">In Übereinstimmung mit INI-Konventionen werden Schlüssel in einem Abschnitt deklariert.</span><span class="sxs-lookup"><span data-stu-id="f988c-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="f988c-205">WSL unterstützt zwei Abschnitte: `automount` und `network`.</span><span class="sxs-lookup"><span data-stu-id="f988c-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="f988c-206">automount</span><span class="sxs-lookup"><span data-stu-id="f988c-206">automount</span></span>

<span data-ttu-id="f988c-207">Abschnitt: `[automount]`</span><span class="sxs-lookup"><span data-stu-id="f988c-207">Section: `[automount]`</span></span>

| <span data-ttu-id="f988c-208">key</span><span class="sxs-lookup"><span data-stu-id="f988c-208">key</span></span>        | <span data-ttu-id="f988c-209">value</span><span class="sxs-lookup"><span data-stu-id="f988c-209">value</span></span>                          | <span data-ttu-id="f988c-210">Standard</span><span class="sxs-lookup"><span data-stu-id="f988c-210">default</span></span>      | <span data-ttu-id="f988c-211">notes</span><span class="sxs-lookup"><span data-stu-id="f988c-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f988c-212">enabled</span><span class="sxs-lookup"><span data-stu-id="f988c-212">enabled</span></span>    | <span data-ttu-id="f988c-213">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-213">boolean</span></span>                        | <span data-ttu-id="f988c-214">wahr</span><span class="sxs-lookup"><span data-stu-id="f988c-214">true</span></span>         | <span data-ttu-id="f988c-215">`true` bewirkt, dass lokale Festplattenlaufwerke (d.h.</span><span class="sxs-lookup"><span data-stu-id="f988c-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="f988c-216">`C:/` oder `D:/`) mit DrvFs automatisch unter `/mnt` eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="f988c-217">`false` bedeutet, dass Laufwerke nicht automatisch bereitgestellt werden, aber Sie können Sie trotzdem manuell oder über bereitstellen `fstab` .</span><span class="sxs-lookup"><span data-stu-id="f988c-217">`false` means drives won't be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="f988c-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="f988c-218">mountFsTab</span></span> | <span data-ttu-id="f988c-219">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-219">boolean</span></span>                        | <span data-ttu-id="f988c-220">wahr</span><span class="sxs-lookup"><span data-stu-id="f988c-220">true</span></span>         | <span data-ttu-id="f988c-221">`true` legt fest, dass `/etc/fstab` beim WSL-Start verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f988c-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="f988c-222">Bei „/etc/fstab“ handelt es sich um eine Datei, in der Sie andere Dateisysteme wie eine SMB-Freigabe deklarieren können.</span><span class="sxs-lookup"><span data-stu-id="f988c-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="f988c-223">Daher können Sie diese Dateisysteme beim Start automatisch in WSL einbinden.</span><span class="sxs-lookup"><span data-stu-id="f988c-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="f988c-224">root</span><span class="sxs-lookup"><span data-stu-id="f988c-224">root</span></span>       | <span data-ttu-id="f988c-225">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f988c-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="f988c-226">Legt das Verzeichnis fest, in dem lokale Festplattenlaufwerke automatisch eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="f988c-227">Wenn Sie z.B. ein Verzeichnis unter `/windir/` in WSL verwenden und Sie dieses als Stammverzeichnis angeben, erwarten Sie, dass die lokalen Festplattenlaufwerke unter `/windir/c` eingebunden werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="f988c-228">Optionen</span><span class="sxs-lookup"><span data-stu-id="f988c-228">options</span></span>    | <span data-ttu-id="f988c-229">Durch Kommas getrennte Liste mit Werten</span><span class="sxs-lookup"><span data-stu-id="f988c-229">comma-separated list of values</span></span> | <span data-ttu-id="f988c-230">Leere Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f988c-230">empty string</span></span> | <span data-ttu-id="f988c-231">Dieser Wert wird an die Standardzeichenfolge der DrvFs-Einbindungsoptionen angefügt.</span><span class="sxs-lookup"><span data-stu-id="f988c-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="f988c-232">**Es können nur DrvFs-spezifische Optionen angegeben werden.**</span><span class="sxs-lookup"><span data-stu-id="f988c-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="f988c-233">Optionen, die die Einbindungsbinärdatei normalerweise in ein Flag analysieren würde, werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f988c-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="f988c-234">Wenn Sie diese Optionen explizit angeben möchten, müssen Sie jedes Laufwerk, für das dies gelten soll, in „/etc/fstab“ einschließen.</span><span class="sxs-lookup"><span data-stu-id="f988c-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="f988c-235">Standardmäßig legt WSL die UID und die GID auf den Wert des Standardbenutzers fest (in der Ubuntu-Distribution wird der Standardbenutzer mit „uid=1000,gid=1000“ erstellt).</span><span class="sxs-lookup"><span data-stu-id="f988c-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="f988c-236">Wenn der Benutzer eine GID-oder UID-Option explizit über diesen Schlüssel angibt, wird der zugehörige Wert überschrieben.</span><span class="sxs-lookup"><span data-stu-id="f988c-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="f988c-237">Andernfalls wird der Standardwert immer angefügt.</span><span class="sxs-lookup"><span data-stu-id="f988c-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="f988c-238">**Hinweis:** Diese Optionen werden als Einbindungsoptionen für alle automatisch eingebundenen Laufwerke angewendet.</span><span class="sxs-lookup"><span data-stu-id="f988c-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="f988c-239">Verwenden Sie stattdessen „/etc/fstab“, um die Optionen nur für ein bestimmtes Laufwerk zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f988c-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="mount-options"></a><span data-ttu-id="f988c-240">Einbindungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f988c-240">Mount options</span></span>

<span data-ttu-id="f988c-241">Durch Festlegen verschiedener Einbindungsoptionen für Windows-Laufwerke (DrvFs) kann gesteuert werden, wie Dateiberechtigungen für Windows-Dateien berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="f988c-242">Die folgenden Optionen sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f988c-242">The following options are available:</span></span>

| <span data-ttu-id="f988c-243">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f988c-243">Key</span></span> | <span data-ttu-id="f988c-244">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f988c-244">Description</span></span> | <span data-ttu-id="f988c-245">Standardwert</span><span class="sxs-lookup"><span data-stu-id="f988c-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="f988c-246">uid</span><span class="sxs-lookup"><span data-stu-id="f988c-246">uid</span></span>| <span data-ttu-id="f988c-247">Die Benutzer-ID, die für den Besitzer aller Dateien verwendet wird</span><span class="sxs-lookup"><span data-stu-id="f988c-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="f988c-248">Die Standard-Benutzer-ID Ihrer WSL-Distribution (bei der erstmaligen Installation ist der Standardwert 1000)</span><span class="sxs-lookup"><span data-stu-id="f988c-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="f988c-249">gid</span><span class="sxs-lookup"><span data-stu-id="f988c-249">gid</span></span>| <span data-ttu-id="f988c-250">Die Gruppen-ID, die für den Besitzer aller Dateien verwendet wird</span><span class="sxs-lookup"><span data-stu-id="f988c-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="f988c-251">Die Standard-Gruppen-ID Ihrer WSL-Distribution (bei der erstmaligen Installation ist der Standardwert 1000)</span><span class="sxs-lookup"><span data-stu-id="f988c-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="f988c-252">umask</span><span class="sxs-lookup"><span data-stu-id="f988c-252">umask</span></span> | <span data-ttu-id="f988c-253">Eine oktale Maske mit Berechtigungen, die für alle Dateien und Verzeichnisse ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="f988c-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="f988c-254">000</span><span class="sxs-lookup"><span data-stu-id="f988c-254">000</span></span>
|<span data-ttu-id="f988c-255">fmask</span><span class="sxs-lookup"><span data-stu-id="f988c-255">fmask</span></span> | <span data-ttu-id="f988c-256">Eine oktale Maske mit Berechtigungen, die für alle Dateien ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="f988c-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="f988c-257">000</span><span class="sxs-lookup"><span data-stu-id="f988c-257">000</span></span>
|<span data-ttu-id="f988c-258">dmask</span><span class="sxs-lookup"><span data-stu-id="f988c-258">dmask</span></span> | <span data-ttu-id="f988c-259">Eine oktale Maske mit Berechtigungen, die für alle Verzeichnisse ausgeschlossen werden sollen</span><span class="sxs-lookup"><span data-stu-id="f988c-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="f988c-260">000</span><span class="sxs-lookup"><span data-stu-id="f988c-260">000</span></span>
|<span data-ttu-id="f988c-261">metadata</span><span class="sxs-lookup"><span data-stu-id="f988c-261">metadata</span></span> | <span data-ttu-id="f988c-262">Ob Metadaten zu Windows-Dateien hinzugefügt werden, um Linux-System Berechtigungen zu unterstützen</span><span class="sxs-lookup"><span data-stu-id="f988c-262">Whether metadata is added to Windows files to support Linux system permissions</span></span> | <span data-ttu-id="f988c-263">enabled</span><span class="sxs-lookup"><span data-stu-id="f988c-263">enabled</span></span>

<span data-ttu-id="f988c-264">**Hinweis:** Die Berechtigungs Masken werden durch eine logische OR-Operation eingefügt, bevor Sie auf Dateien oder Verzeichnisse angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-264">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="f988c-265">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f988c-265">network</span></span>

<span data-ttu-id="f988c-266">Abschnittsbezeichnung: `[network]`</span><span class="sxs-lookup"><span data-stu-id="f988c-266">Section label: `[network]`</span></span>

| <span data-ttu-id="f988c-267">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f988c-267">key</span></span> | <span data-ttu-id="f988c-268">value</span><span class="sxs-lookup"><span data-stu-id="f988c-268">value</span></span> | <span data-ttu-id="f988c-269">default</span><span class="sxs-lookup"><span data-stu-id="f988c-269">default</span></span> | <span data-ttu-id="f988c-270">notes</span><span class="sxs-lookup"><span data-stu-id="f988c-270">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f988c-271">generateHosts</span><span class="sxs-lookup"><span data-stu-id="f988c-271">generateHosts</span></span> | <span data-ttu-id="f988c-272">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-272">boolean</span></span> | `true` | <span data-ttu-id="f988c-273">`true` legt fest, dass WSL `/etc/hosts` generiert.</span><span class="sxs-lookup"><span data-stu-id="f988c-273">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="f988c-274">Die Datei `hosts` enthält eine statische Zuordnung der entsprechenden IP-Adresse von Hostnamen.</span><span class="sxs-lookup"><span data-stu-id="f988c-274">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="f988c-275">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="f988c-275">generateResolvConf</span></span> | <span data-ttu-id="f988c-276">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-276">boolean</span></span> | `true` | <span data-ttu-id="f988c-277">`true` legt fest, dass WSL `/etc/resolv.conf` generiert.</span><span class="sxs-lookup"><span data-stu-id="f988c-277">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="f988c-278">`resolv.conf` enthält eine DNS-Liste, mit der ein angegebener Hostnamen in seine IP-Adresse aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="f988c-278">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="f988c-279">interop</span><span class="sxs-lookup"><span data-stu-id="f988c-279">interop</span></span>

<span data-ttu-id="f988c-280">Abschnittsbezeichnung: `[interop]`</span><span class="sxs-lookup"><span data-stu-id="f988c-280">Section label: `[interop]`</span></span>

<span data-ttu-id="f988c-281">Diese Optionen sind in Insider Build 17713 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f988c-281">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="f988c-282">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f988c-282">key</span></span> | <span data-ttu-id="f988c-283">value</span><span class="sxs-lookup"><span data-stu-id="f988c-283">value</span></span> | <span data-ttu-id="f988c-284">default</span><span class="sxs-lookup"><span data-stu-id="f988c-284">default</span></span> | <span data-ttu-id="f988c-285">notes</span><span class="sxs-lookup"><span data-stu-id="f988c-285">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f988c-286">enabled</span><span class="sxs-lookup"><span data-stu-id="f988c-286">enabled</span></span> | <span data-ttu-id="f988c-287">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-287">boolean</span></span> | `true` | <span data-ttu-id="f988c-288">Durch Festlegen dieses Schlüssels wird festgelegt, ob WSL das Starten von Windows-Prozessen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f988c-288">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="f988c-289">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="f988c-289">appendWindowsPath</span></span> | <span data-ttu-id="f988c-290">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-290">boolean</span></span> | `true` | <span data-ttu-id="f988c-291">Durch Festlegen dieses Schlüssels wird festgelegt, ob WSL der $PATH-Umgebungsvariablen Windows-Pfadelemente hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f988c-291">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> |

#### <a name="user"></a><span data-ttu-id="f988c-292">user</span><span class="sxs-lookup"><span data-stu-id="f988c-292">user</span></span>

<span data-ttu-id="f988c-293">Abschnittsbezeichnung: `[user]`</span><span class="sxs-lookup"><span data-stu-id="f988c-293">Section label: `[user]`</span></span>

<span data-ttu-id="f988c-294">Diese Optionen sind in Build 18980 und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f988c-294">These options are available in Build 18980 and later.</span></span>

| <span data-ttu-id="f988c-295">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f988c-295">key</span></span> | <span data-ttu-id="f988c-296">value</span><span class="sxs-lookup"><span data-stu-id="f988c-296">value</span></span> | <span data-ttu-id="f988c-297">default</span><span class="sxs-lookup"><span data-stu-id="f988c-297">default</span></span> | <span data-ttu-id="f988c-298">notes</span><span class="sxs-lookup"><span data-stu-id="f988c-298">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f988c-299">default</span><span class="sxs-lookup"><span data-stu-id="f988c-299">default</span></span> | <span data-ttu-id="f988c-300">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f988c-300">string</span></span> | <span data-ttu-id="f988c-301">Der anfängliche Benutzername, der bei der ersten Ausführen erstellt wurde</span><span class="sxs-lookup"><span data-stu-id="f988c-301">The initial username created on first run</span></span> | <span data-ttu-id="f988c-302">Durch Festlegen dieses Schlüssels wird angegeben, welcher Benutzer beim ersten Starten einer WSL-Sitzung ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f988c-302">Setting this key specifies which user to run as when first starting a WSL session.</span></span> |

## <a name="configure-global-options-with-wslconfig"></a><span data-ttu-id="f988c-303">Konfigurieren globaler Optionen mit wslconfig</span><span class="sxs-lookup"><span data-stu-id="f988c-303">Configure global options with .wslconfig</span></span>

> <span data-ttu-id="f988c-304">**Verfügbar in Windows Build 19041 und höher**</span><span class="sxs-lookup"><span data-stu-id="f988c-304">**Available in Windows Build 19041 and later**</span></span>

<span data-ttu-id="f988c-305">Sie können globale WSL-Optionen konfigurieren, indem Sie eine `.wslconfig` Datei in das Stammverzeichnis Ihres Benutzer Ordners einfügen: `C:\Users\<yourUserName>\.wslconfig` .</span><span class="sxs-lookup"><span data-stu-id="f988c-305">You can configure global WSL options by placing a `.wslconfig` file into the root directory of your users folder: `C:\Users\<yourUserName>\.wslconfig`.</span></span> <span data-ttu-id="f988c-306">Viele dieser Dateien beziehen sich auf WSL 2. Beachten Sie, dass Sie möglicherweise ausführen müssen `wsl --shutdown` , um die WSL 2-VM herunterzufahren, und dann die WSL-Instanz neu starten, damit diese Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="f988c-306">Many of these files are related to WSL 2, please keep in mind you may need to run `wsl --shutdown` to shut down the WSL 2 VM and then restart your WSL instance for these changes to take affect.</span></span>

<span data-ttu-id="f988c-307">Im folgenden finden Sie eine wslconfig-Beispieldatei:</span><span class="sxs-lookup"><span data-stu-id="f988c-307">Here is a sample .wslconfig file:</span></span>

```console
[wsl2]
kernel=C:\\temp\\myCustomKernel
memory=4GB # Limits VM memory in WSL 2 to 4 GB
processors=2 # Makes the WSL 2 VM use two virtual processors
```

<span data-ttu-id="f988c-308">Diese Datei kann die folgenden Optionen enthalten:</span><span class="sxs-lookup"><span data-stu-id="f988c-308">This file can contain the following options:</span></span>

### <a name="wsl-2-settings"></a><span data-ttu-id="f988c-309">WSL 2-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="f988c-309">WSL 2 Settings</span></span>

<span data-ttu-id="f988c-310">Abschnittsbezeichnung: `[wsl2]`</span><span class="sxs-lookup"><span data-stu-id="f988c-310">Section label: `[wsl2]`</span></span>

<span data-ttu-id="f988c-311">Diese Einstellungen wirken sich auf die VM aus, die jede WSL 2-Distribution unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f988c-311">These settings affect the VM that powers any WSL 2 distribution.</span></span>

| <span data-ttu-id="f988c-312">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f988c-312">key</span></span> | <span data-ttu-id="f988c-313">value</span><span class="sxs-lookup"><span data-stu-id="f988c-313">value</span></span> | <span data-ttu-id="f988c-314">default</span><span class="sxs-lookup"><span data-stu-id="f988c-314">default</span></span> | <span data-ttu-id="f988c-315">notes</span><span class="sxs-lookup"><span data-stu-id="f988c-315">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="f988c-316">kernel</span><span class="sxs-lookup"><span data-stu-id="f988c-316">kernel</span></span> | <span data-ttu-id="f988c-317">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f988c-317">string</span></span> | <span data-ttu-id="f988c-318">Der von Microsoft bereitgestellte Posteingang</span><span class="sxs-lookup"><span data-stu-id="f988c-318">The Microsoft built kernel provided inbox</span></span> | <span data-ttu-id="f988c-319">Ein absoluter Windows-Pfad zu einem benutzerdefinierten Linux-Kernel.</span><span class="sxs-lookup"><span data-stu-id="f988c-319">An absolute Windows path to a custom Linux kernel.</span></span> |
| <span data-ttu-id="f988c-320">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="f988c-320">memory</span></span> | <span data-ttu-id="f988c-321">size</span><span class="sxs-lookup"><span data-stu-id="f988c-321">size</span></span> | <span data-ttu-id="f988c-322">50% des Gesamt Arbeitsspeichers unter Windows oder 8 GB, je nachdem, welcher Wert kleiner ist. bei Builds vor 20175:80% ihres gesamten Arbeitsspeichers unter Windows</span><span class="sxs-lookup"><span data-stu-id="f988c-322">50% of total memory on Windows or 8GB, whichever is less; on builds before 20175: 80% of your total memory on Windows</span></span> | <span data-ttu-id="f988c-323">Wie viel Arbeitsspeicher für die WSL 2-VM zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f988c-323">How much memory to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="f988c-324">Prozessoren</span><span class="sxs-lookup"><span data-stu-id="f988c-324">processors</span></span> | <span data-ttu-id="f988c-325">number</span><span class="sxs-lookup"><span data-stu-id="f988c-325">number</span></span> | <span data-ttu-id="f988c-326">Die gleiche Anzahl von Prozessoren unter Windows</span><span class="sxs-lookup"><span data-stu-id="f988c-326">The same number of processors on Windows</span></span> | <span data-ttu-id="f988c-327">Gibt an, wie viele Prozessoren der WSL 2-VM zugewiesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f988c-327">How many processors to assign to the WSL 2 VM.</span></span> |
| <span data-ttu-id="f988c-328">localhostforwarding</span><span class="sxs-lookup"><span data-stu-id="f988c-328">localhostForwarding</span></span> | <span data-ttu-id="f988c-329">boolean</span><span class="sxs-lookup"><span data-stu-id="f988c-329">boolean</span></span> | `true` | <span data-ttu-id="f988c-330">Boolescher Wert, der angibt, ob an den Platzhalter oder localhost in der WSL 2-VM gebundene Ports über localhost: Port vom Host aus verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f988c-330">Boolean specifying if ports bound to wildcard or localhost in the WSL 2 VM should be connectable from the host via localhost:port.</span></span> |
| <span data-ttu-id="f988c-331">kernelcommandline</span><span class="sxs-lookup"><span data-stu-id="f988c-331">kernelCommandLine</span></span> | <span data-ttu-id="f988c-332">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f988c-332">string</span></span> | <span data-ttu-id="f988c-333">Leer</span><span class="sxs-lookup"><span data-stu-id="f988c-333">Blank</span></span> | <span data-ttu-id="f988c-334">Zusätzliche Kernel-Befehlszeilenargumente.</span><span class="sxs-lookup"><span data-stu-id="f988c-334">Additional kernel command line arguments.</span></span> |
| <span data-ttu-id="f988c-335">swap</span><span class="sxs-lookup"><span data-stu-id="f988c-335">swap</span></span> | <span data-ttu-id="f988c-336">size</span><span class="sxs-lookup"><span data-stu-id="f988c-336">size</span></span> | <span data-ttu-id="f988c-337">25% der Arbeitsspeicher Größe unter Windows auf das nächste GB aufgerundet</span><span class="sxs-lookup"><span data-stu-id="f988c-337">25% of memory size on Windows rounded up to the nearest GB</span></span> | <span data-ttu-id="f988c-338">Wie viel Auslagerungs Bereich zum virtuellen WSL 2-Computer hinzugefügt werden soll, 0 für keine Auslagerungs Datei.</span><span class="sxs-lookup"><span data-stu-id="f988c-338">How much swap space to add to the WSL 2 VM, 0 for no swap file.</span></span> |
| <span data-ttu-id="f988c-339">Auslagerungs Datei</span><span class="sxs-lookup"><span data-stu-id="f988c-339">swapFile</span></span> | <span data-ttu-id="f988c-340">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f988c-340">string</span></span> | <span data-ttu-id="f988c-341">%UserProfile%\appdata\local\temp\tauap.vhdx</span><span class="sxs-lookup"><span data-stu-id="f988c-341">%USERPROFILE%\AppData\Local\Temp\swap.vhdx</span></span> | <span data-ttu-id="f988c-342">Ein absoluter Windows-Pfad zu der virtuellen Auslagerungs-Festplatte.</span><span class="sxs-lookup"><span data-stu-id="f988c-342">An absolute Windows path to the swap virtual hard disk.</span></span> |

* <span data-ttu-id="f988c-343">Hinweis: dieser Wert gilt für Windows Build 19041 und unterscheidet sich möglicherweise in Windows-Builds im Insider-Programm.</span><span class="sxs-lookup"><span data-stu-id="f988c-343">Note: This value is true for Windows Build 19041 and may be different in Windows builds in the Insiders program</span></span>

<span data-ttu-id="f988c-344">Einträge mit dem `path` Wert müssen Windows-Pfade mit Escapezeichen mit Escapezeichen sein, z. b.: `C:\\Temp\\myCustomKernel`</span><span class="sxs-lookup"><span data-stu-id="f988c-344">Entries with the `path` value must be Windows paths with escaped backslashes, e.g: `C:\\Temp\\myCustomKernel`</span></span>

<span data-ttu-id="f988c-345">Einträge mit dem `size` Wert müssen eine Größe gefolgt von einer Einheit sein, z `8GB` . b `512MB` . oder.</span><span class="sxs-lookup"><span data-stu-id="f988c-345">Entries with the `size` value must be a size followed by a unit, for example `8GB` or `512MB`.</span></span>