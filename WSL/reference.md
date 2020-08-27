---
title: 'Windows-Subsystem für Linux: Befehlsreferenz'
description: Zeigen Sie eine Liste von Befehlen an, die das Windows-Subsystem für Linux verwalten, z. B. Argumente für die Ausführung von Linux-Befehlen.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: fc5c9e06c597092a3790ba7f9eb06054a33450c1
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866130"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="d9626-104">Befehlsreferenz für das Windows-Subsystem für Linux</span><span class="sxs-lookup"><span data-stu-id="d9626-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="d9626-105">Die beste Möglichkeit, mit dem Windows-Subsystem für Linux zu interagieren, ist die Verwendung des Befehls `wsl.exe`.</span><span class="sxs-lookup"><span data-stu-id="d9626-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span>

## <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="d9626-106">Festlegen von WSL 2 als Standardversion</span><span class="sxs-lookup"><span data-stu-id="d9626-106">Set WSL 2 as your default version</span></span>

<span data-ttu-id="d9626-107">Führen Sie bei der Installation einer neuen Linux-Verteilung den folgenden Befehl in PowerShell aus, um WSL 2 als Standardversion festzulegen:</span><span class="sxs-lookup"><span data-stu-id="d9626-107">Run the following command in Powershell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="d9626-108">Festlegen der Verteilungsversion auf WSL 1 oder WSL 2</span><span class="sxs-lookup"><span data-stu-id="d9626-108">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="d9626-109">Sie können die den einzelnen installierten Linux-Verteilungen zugewiesenen WSL-Version überprüfen, indem Sie die PowerShell-Befehlszeile öffnen und den folgenden Befehl (nur verfügbar in [Windows Build 19041 oder höher](ms-settings:windowsupdate)) eingeben: `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="d9626-109">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```bash
wsl --list --verbose
```

<span data-ttu-id="d9626-110">Um eine Verteilung so einzurichten, dass sie von einer der beiden WSL-Versionen unterstützt wird, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="d9626-110">To set a distribution to be backed by either version of WSL please run:</span></span>

```bash
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="d9626-111">Ersetzen Sie hierbei `<distribution name>` durch den tatsächlichen Namen Ihrer Verteilung und `<versionNumber>` durch die Ziffer „1“ oder „2“.</span><span class="sxs-lookup"><span data-stu-id="d9626-111">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="d9626-112">Sie können jederzeit zu WSL 1 zurückwechseln, indem sie denselben Befehl wie oben ausführen, aber die 2 durch eine 1 ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d9626-112">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="d9626-113">Wenn Sie WSL 2 als Ihre Standardarchitektur festlegen möchten, ist dies über diesen Befehl möglich:</span><span class="sxs-lookup"><span data-stu-id="d9626-113">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```bash
wsl --set-default-version 2
```

<span data-ttu-id="d9626-114">Dadurch wird die Version jeder neu installierten Verteilung auf WSL 2 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9626-114">This will set the version of any new distribution installed to WSL 2.</span></span>

## `wsl.exe`

<span data-ttu-id="d9626-115">Unten finden Sie eine Liste mit allen Optionen, wenn Sie `wsl.exe` ab Windows Version 1903 verwenden.</span><span class="sxs-lookup"><span data-stu-id="d9626-115">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="d9626-116">Syntax: `wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="d9626-116">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-commands"></a><span data-ttu-id="d9626-117">Argumente für das Ausführen von Linux-Befehlen</span><span class="sxs-lookup"><span data-stu-id="d9626-117">Arguments for running Linux commands</span></span>

* <span data-ttu-id="d9626-118">**Ohne Argumente**</span><span class="sxs-lookup"><span data-stu-id="d9626-118">**Without arguments**</span></span>

  <span data-ttu-id="d9626-119">Wenn keine Befehlszeile angegeben wird, startet „wsl.exe“ die Standardshell.</span><span class="sxs-lookup"><span data-stu-id="d9626-119">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="d9626-120">**--exec, -e \<CommandLine>**</span><span class="sxs-lookup"><span data-stu-id="d9626-120">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="d9626-121">Führt den angegebenen Befehl ohne Verwendung der Linux-Standardshell aus.</span><span class="sxs-lookup"><span data-stu-id="d9626-121">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="d9626-122">Übergibt die verbleibende Befehlszeile unverändert.</span><span class="sxs-lookup"><span data-stu-id="d9626-122">Pass the remaining command line as is.</span></span>

<span data-ttu-id="d9626-123">Die oben genannten Befehle akzeptieren außerdem die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="d9626-123">The above commands also accept the following options:</span></span>

* <span data-ttu-id="d9626-124">**--distribution, -d \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="d9626-124">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="d9626-125">Führt die angegebene Distribution aus.</span><span class="sxs-lookup"><span data-stu-id="d9626-125">Run the specified distribution.</span></span>

* <span data-ttu-id="d9626-126">**--user, -u \<UserName>**</span><span class="sxs-lookup"><span data-stu-id="d9626-126">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="d9626-127">Ausführung als der angegebene Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d9626-127">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="d9626-128">Argumente für die Verwaltung des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="d9626-128">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="d9626-129">**--export \<Distro> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="d9626-129">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="d9626-130">Exportiert die Distribution in eine TAR-Datei.</span><span class="sxs-lookup"><span data-stu-id="d9626-130">Exports the distribution to a tar file.</span></span> <span data-ttu-id="d9626-131">Der Dateiname kann „-“ für Standardausgabe sein.</span><span class="sxs-lookup"><span data-stu-id="d9626-131">The filename can be - for standard output.</span></span>

* <span data-ttu-id="d9626-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span><span class="sxs-lookup"><span data-stu-id="d9626-132">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="d9626-133">Importiert die angegebene TAR-Datei als neue Distribution.</span><span class="sxs-lookup"><span data-stu-id="d9626-133">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="d9626-134">Der Dateiname kann „-“ für Standardeingabe sein.</span><span class="sxs-lookup"><span data-stu-id="d9626-134">The filename can be - for standard input.</span></span>

* <span data-ttu-id="d9626-135">**--list, -l [Optionen]**</span><span class="sxs-lookup"><span data-stu-id="d9626-135">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="d9626-136">Listet Distributionen auf.</span><span class="sxs-lookup"><span data-stu-id="d9626-136">Lists distributions.</span></span>

  <span data-ttu-id="d9626-137">Optionen:</span><span class="sxs-lookup"><span data-stu-id="d9626-137">Options:</span></span>
  * <span data-ttu-id="d9626-138">**--all**</span><span class="sxs-lookup"><span data-stu-id="d9626-138">**--all**</span></span>

    <span data-ttu-id="d9626-139">Listet alle Distributionen auf, einschließlich Distributionen, die zurzeit installiert oder deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="d9626-139">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="d9626-140">**--running**</span><span class="sxs-lookup"><span data-stu-id="d9626-140">**--running**</span></span>

    <span data-ttu-id="d9626-141">Listet nur Distributionen auf, die zurzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9626-141">List only distributions that are currently running.</span></span>

* <span data-ttu-id="d9626-142">**--set-default, -s \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="d9626-142">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="d9626-143">Legt die Distribution als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="d9626-143">Sets the distribution as the default.</span></span>

* <span data-ttu-id="d9626-144">**--terminate, -t \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="d9626-144">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="d9626-145">Beendet die angegebene Distribution.</span><span class="sxs-lookup"><span data-stu-id="d9626-145">Terminates the specified distribution.</span></span>

* <span data-ttu-id="d9626-146">**--unregister \<Distro>**</span><span class="sxs-lookup"><span data-stu-id="d9626-146">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="d9626-147">Hebt die Registrierung der Verteilung auf.</span><span class="sxs-lookup"><span data-stu-id="d9626-147">Un-register the distribution.</span></span>

* <span data-ttu-id="d9626-148">**--help**: Zeigt Syntaxinformationen an.</span><span class="sxs-lookup"><span data-stu-id="d9626-148">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="d9626-149">Weitere Befehle</span><span class="sxs-lookup"><span data-stu-id="d9626-149">Additional Commands</span></span>

<span data-ttu-id="d9626-150">Es gibt auch historische Befehle für die Interaktion mit dem Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="d9626-150">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="d9626-151">Ihre Funktionalität ist in `wsl.exe` enthalten, sie sind jedoch weiterhin zur Verwendung verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d9626-151">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span>

### `wslconfig.exe`

<span data-ttu-id="d9626-152">Mit diesem Befehl können Sie Ihre WSL-Distribution konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d9626-152">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="d9626-153">Es folgt eine Liste der zugehörigen Optionen.</span><span class="sxs-lookup"><span data-stu-id="d9626-153">Below is a list of its options.</span></span>

<span data-ttu-id="d9626-154">Syntax: `wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="d9626-154">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="d9626-155">Argumente</span><span class="sxs-lookup"><span data-stu-id="d9626-155">Arguments</span></span>

* <span data-ttu-id="d9626-156">**/l, /list [Optionen]**</span><span class="sxs-lookup"><span data-stu-id="d9626-156">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="d9626-157">Listet registrierte Distributionen auf.</span><span class="sxs-lookup"><span data-stu-id="d9626-157">Lists registered distributions.</span></span>
  
<span data-ttu-id="d9626-158">Optionen:</span><span class="sxs-lookup"><span data-stu-id="d9626-158">Options:</span></span>

* <span data-ttu-id="d9626-159">**/all** Listet optional alle Verteilungen auf, einschließlich Verteilungen, die zurzeit installiert oder deinstalliert werden.</span><span class="sxs-lookup"><span data-stu-id="d9626-159">**/all** Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

* <span data-ttu-id="d9626-160">**/running** Listet nur Verteilungen auf, die zurzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9626-160">**/running** List only distributions that are currently running.</span></span>

* <span data-ttu-id="d9626-161">**/s, /setdefault \<Distro>** : Legtdie Distribution als Standard fest.</span><span class="sxs-lookup"><span data-stu-id="d9626-161">**/s, /setdefault \<Distro>** Sets the distribution as the default.</span></span>

* <span data-ttu-id="d9626-162">**/t, /terminate \<Distro>** : Beendet die Distribution.</span><span class="sxs-lookup"><span data-stu-id="d9626-162">**/t, /terminate \<Distro>** Terminates the distribution.</span></span>

* <span data-ttu-id="d9626-163">**/u, /unregister \<Distro>** : Hebt die Registrierung der Distribution auf.</span><span class="sxs-lookup"><span data-stu-id="d9626-163">**/u, /unregister \<Distro>** Un-registers the distribution.</span></span>

* <span data-ttu-id="d9626-164">**/upgrade \<Distro>** : Führt ein Upgrade der Distribution auf das WslFs-Dateisystemformat durch.</span><span class="sxs-lookup"><span data-stu-id="d9626-164">**/upgrade \<Distro>** Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="d9626-165">Dieser Befehl wird verwendet, um eine Bash-Shell zu starten.</span><span class="sxs-lookup"><span data-stu-id="d9626-165">This command is used to start a bash shell.</span></span> <span data-ttu-id="d9626-166">Unten finden Sie die Optionen, die Sie mit diesem Befehl verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d9626-166">Below are the options you can use with this command.</span></span>

<span data-ttu-id="d9626-167">Syntax: `bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="d9626-167">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="d9626-168">**Keine Option angegeben**</span><span class="sxs-lookup"><span data-stu-id="d9626-168">**No Option given**</span></span>
  
  <span data-ttu-id="d9626-169">Startet die Bash-Shell im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="d9626-169">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="d9626-170">Wenn die Bash-Shell nicht installiert ist, wird automatisch `lxrun /install` ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9626-170">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="d9626-171">`bash ~` startet die Bash-Shell im Basisverzeichnis des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d9626-171">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="d9626-172">Vergleichbar mit der Ausführung von `cd ~`.</span><span class="sxs-lookup"><span data-stu-id="d9626-172">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="d9626-173">**-c "\<command>"**</span><span class="sxs-lookup"><span data-stu-id="d9626-173">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="d9626-174">Führt den Befehl aus, gibt die Ausgabe aus, und kehrt zur Windows-Eingabeaufforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="d9626-174">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>

  <span data-ttu-id="d9626-175">Beispiel: `bash -c "ls"`.</span><span class="sxs-lookup"><span data-stu-id="d9626-175">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="d9626-176">Veraltete Befehle</span><span class="sxs-lookup"><span data-stu-id="d9626-176">Deprecated Commands</span></span>

<span data-ttu-id="d9626-177">`lxrun.exe` war der erste Befehl, der zum Installieren und Verwalten des Windows-Subsystems für Linux verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d9626-177">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="d9626-178">Er gilt ab Windows 10 Version 1803 und höher als veraltet.</span><span class="sxs-lookup"><span data-stu-id="d9626-178">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="d9626-179">Der Befehl `lxrun.exe` kann verwendet werden, um direkt mit dem [Windows-Subsystem für Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) zu interagieren.</span><span class="sxs-lookup"><span data-stu-id="d9626-179">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="d9626-180">Diese Befehle werden im Verzeichnis `\Windows\System32` installiert und können in einer Windows-Eingabeaufforderung oder in PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d9626-180">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="d9626-181">Befehl</span><span class="sxs-lookup"><span data-stu-id="d9626-181">Command</span></span>                     | <span data-ttu-id="d9626-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9626-182">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="d9626-183">Der lxrun-Befehl wird verwendet, um die WSL-Instanz zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="d9626-183">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="d9626-184">Startet den Download- und Installationsvorgang.</span><span class="sxs-lookup"><span data-stu-id="d9626-184">Starts the download and install process.</span></span> <br/> <span data-ttu-id="d9626-185">**/y** kann hinzugefügt werden, um alle Eingabeaufforderungen zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="d9626-185">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="d9626-186">Die Bestätigungsaufforderung wird automatisch akzeptiert, und der Standardbenutzer wird auf „root“ festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d9626-186">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="d9626-187">Deinstalliert und löscht das Ubuntu-Image.</span><span class="sxs-lookup"><span data-stu-id="d9626-187">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="d9626-188">Standardmäßig wird hierdurch nicht das Ubuntu-Basisverzeichnis des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9626-188">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="d9626-189">**/y** kann hinzugefügt werden, um die Bestätigungsaufforderung automatisch zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d9626-189">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="d9626-190">**/full** deinstalliert und löscht das Ubuntu-Basisverzeichnis des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d9626-190">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="d9626-191">Legt die Standard-Bash für den Ubuntu-Benutzer fest.</span><span class="sxs-lookup"><span data-stu-id="d9626-191">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="d9626-192">Fordert zur Eingabe eines Kennworts auf, wenn der angegebene Benutzer nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d9626-192">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="d9626-193">Weitere Informationen finden Sie unter https://aka.ms/wslusers.</span><span class="sxs-lookup"><span data-stu-id="d9626-193">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="d9626-194">**/y** umgeht die Eingabeaufforderung für das Kennwort.</span><span class="sxs-lookup"><span data-stu-id="d9626-194">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="d9626-195">Der Benutzer wird ohne Kennwort erstellt.</span><span class="sxs-lookup"><span data-stu-id="d9626-195">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="d9626-196">Aktualisiert den Paketindex des Subsystems.</span><span class="sxs-lookup"><span data-stu-id="d9626-196">Updates the subsystem's package index</span></span>          |
