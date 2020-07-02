---
title: Installieren des Windows-Subsystems für Linux (WSL) unter Windows 10
description: Installationsanweisungen für das Windows-Subsystem für Linux unter Windows 10.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Installieren, Aktivieren, WSL2, Version 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 0f59fda8aa093487f09c1817acf47bd88eaae8cc
ms.sourcegitcommit: f1b049a1276782d4f2754f46a8d2025b598a0784
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "85336093"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="28b70-104">Windows-Subsystem für Linux: Installationsleitfaden für Windows 10</span><span class="sxs-lookup"><span data-stu-id="28b70-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="28b70-105">Installieren des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="28b70-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="28b70-106">Bevor Sie eine Linux-Verteilung unter Windows installieren können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ aktivieren.</span><span class="sxs-lookup"><span data-stu-id="28b70-106">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="28b70-107">Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="28b70-107">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="28b70-108">Um nur WSL 1 zu installieren, sollten Sie nun den Computer neu starten und mit dem [Installieren der Linux-Verteilung Ihrer Wahl](./install-win10.md#install-your-linux-distribution-of-choice) fortfahren. Andernfalls warten Sie auf den Neustart, und fahren Sie mit dem Update auf WSL 2 fort.</span><span class="sxs-lookup"><span data-stu-id="28b70-108">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="28b70-109">Erfahren Sie mehr über den [Vergleich zwischen WSL 2 und WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="28b70-109">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="28b70-110">Aktualisieren auf WSL 2</span><span class="sxs-lookup"><span data-stu-id="28b70-110">Update to WSL 2</span></span>

<span data-ttu-id="28b70-111">Um ein Update auf WSL 2 durchführen zu können, müssen die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="28b70-111">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="28b70-112">Ausgeführt unter Windows 10, [aktualisiert auf Version 2004](ms-settings:windowsupdate), **Build 19041** oder höher.</span><span class="sxs-lookup"><span data-stu-id="28b70-112">Running Windows 10, [updated to version 2004](ms-settings:windowsupdate), **Build 19041** or higher.</span></span>

- <span data-ttu-id="28b70-113">Überprüfen Sie Ihre Windows-Version, indem Sie die **Windows-Logo-Taste+R** auswählen, **winver** eingeben und **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="28b70-113">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="28b70-114">(Oder geben Sie den Befehl `ver` an der Windows-Eingabeaufforderung ein.)</span><span class="sxs-lookup"><span data-stu-id="28b70-114">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="28b70-115">[Aktualisieren Sie auf die neueste Windows-Version](ms-settings:windowsupdate), wenn Ihr Build niedriger als 19041 ist.</span><span class="sxs-lookup"><span data-stu-id="28b70-115">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 19041.</span></span> <span data-ttu-id="28b70-116">[Holen Sie sich den Windows Update-Assistenten](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="28b70-116">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="28b70-117">Aktivieren Sie die optionale Komponente „Virtual Machine Platform“.</span><span class="sxs-lookup"><span data-stu-id="28b70-117">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="28b70-118">Vor der Installation von WSL 2 müssen Sie das optionale Feature „Virtual Machine Platform“ aktivieren.</span><span class="sxs-lookup"><span data-stu-id="28b70-118">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="28b70-119">Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="28b70-119">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="28b70-120">**Starten Sie Ihrem Computer neu**, um die WSL-Installation und das Update auf WSL 2 abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="28b70-120">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="28b70-121">Festlegen von WSL 2 als Standardversion</span><span class="sxs-lookup"><span data-stu-id="28b70-121">Set WSL 2 as your default version</span></span>

<span data-ttu-id="28b70-122">Führen Sie bei der Installation einer neuen Linux-Verteilung den folgenden Befehl in PowerShell aus, um WSL 2 als Standardversion festzulegen:</span><span class="sxs-lookup"><span data-stu-id="28b70-122">Run the following command in PowerShell to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="28b70-123">Diese Meldung wird möglicherweise nach dem Ausführen des folgenden Befehls angezeigt: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="28b70-123">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="28b70-124">Befolgen Sie den Link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)), und installieren Sie die MSI von dieser Seite in unserer Dokumentation, um einen Linux-Kernel auf Ihrem Computer zu installieren, der von WSL 2 verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="28b70-124">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="28b70-125">Sobald Sie den Kernel installiert haben, führen Sie den Befehl erneut aus. Er sollte nun erfolgreich abgeschlossen werden, ohne dass die Meldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="28b70-125">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="28b70-126">Die Aktualisierung von WSL 1 auf WSL 2 kann je nach Umfang Ihrer Zielverteilung mehrere Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="28b70-126">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="28b70-127">Wenn Sie eine ältere (Legacy) Installation der WSL 1 von Windows 10 Anniversary Update oder Creators Update aus ausführen, kann ein Updatefehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="28b70-127">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="28b70-128">Befolgen Sie diese Anweisungen, um [alle Legacyverteilungen zu deinstallieren und zu entfernen](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="28b70-128">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="28b70-129">Installieren der Linux-Verteilung Ihrer Wahl</span><span class="sxs-lookup"><span data-stu-id="28b70-129">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="28b70-130">Öffnen Sie den [Microsoft Store](https://aka.ms/wslstore), und wählen Sie Ihre bevorzugte Linux-Verteilung aus.</span><span class="sxs-lookup"><span data-stu-id="28b70-130">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Ansicht der Linux-Verteilungen im Microsoft Store](media/store.png)

    <span data-ttu-id="28b70-132">Über die folgenden Links wird die Seite des Microsoft Store für jede Distribution geöffnet:</span><span class="sxs-lookup"><span data-stu-id="28b70-132">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="28b70-133">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="28b70-133">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="28b70-134">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="28b70-134">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="28b70-135">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="28b70-135">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="28b70-136">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="28b70-136">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="28b70-137">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="28b70-137">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="28b70-138">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="28b70-138">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="28b70-139">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="28b70-139">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="28b70-140">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="28b70-140">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="28b70-141">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="28b70-141">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="28b70-142">Pengwin</span><span class="sxs-lookup"><span data-stu-id="28b70-142">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="28b70-143">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="28b70-143">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="28b70-144">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="28b70-144">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="28b70-145">Wählen Sie auf der Seite der Verteilung die Option „Get“ (Abrufen) aus.</span><span class="sxs-lookup"><span data-stu-id="28b70-145">From the distribution's page, select "Get".</span></span>

    ![Linux-Verteilungen im Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="28b70-147">Einrichten einer neuen Verteilung</span><span class="sxs-lookup"><span data-stu-id="28b70-147">Set up a new distribution</span></span>

<span data-ttu-id="28b70-148">Wenn Sie eine neu installierte Linux-Verteilung zum ersten Mal starten, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, ein oder zwei Minuten zu warten, bis die Dateien dekomprimiert und auf dem PC gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="28b70-148">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="28b70-149">Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="28b70-149">All future launches should take less than a second.</span></span>

<span data-ttu-id="28b70-150">Anschließend müssen Sie [ein Benutzerkonto und Kennwort für Ihre neue Linux-Verteilung erstellen](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="28b70-150">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="28b70-152">Festlegen der Verteilungsversion auf WSL 1 oder WSL 2</span><span class="sxs-lookup"><span data-stu-id="28b70-152">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="28b70-153">Sie können die den einzelnen installierten Linux-Verteilungen zugewiesenen WSL-Version überprüfen, indem Sie die PowerShell-Befehlszeile öffnen und den folgenden Befehl (nur verfügbar in [Windows Build 19041 oder höher](ms-settings:windowsupdate)) eingeben: `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="28b70-153">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 19041 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="28b70-154">Um eine Verteilung so einzurichten, dass sie von einer der beiden WSL-Versionen unterstützt wird, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="28b70-154">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="28b70-155">Ersetzen Sie hierbei `<distribution name>` durch den tatsächlichen Namen Ihrer Verteilung und `<versionNumber>` durch die Ziffer „1“ oder „2“.</span><span class="sxs-lookup"><span data-stu-id="28b70-155">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="28b70-156">Sie können jederzeit zu WSL 1 zurückwechseln, indem sie denselben Befehl wie oben ausführen, aber die 2 durch eine 1 ersetzen.</span><span class="sxs-lookup"><span data-stu-id="28b70-156">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="28b70-157">Wenn Sie WSL 2 als Ihre Standardarchitektur festlegen möchten, ist dies über diesen Befehl möglich:</span><span class="sxs-lookup"><span data-stu-id="28b70-157">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="28b70-158">Dadurch wird die Version jeder neu installierten Verteilung auf WSL 2 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="28b70-158">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="28b70-159">Problembehandlung bei der Installation</span><span class="sxs-lookup"><span data-stu-id="28b70-159">Troubleshooting installation</span></span>

<span data-ttu-id="28b70-160">Nachfolgend werden einige Fehler und vorgeschlagene Korrekturen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28b70-160">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="28b70-161">Weitere allgemeine Fehler und zugehörige Lösungen finden Sie auf der [Seite für die WSL-Problembehandlung](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="28b70-161">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="28b70-162">**Installation failed with error 0x80070003 (Installationsfehler mit Fehlercode 0x80070003)**</span><span class="sxs-lookup"><span data-stu-id="28b70-162">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="28b70-163">Das Windows-Subsystem für Linux wird nur auf dem Systemlaufwerk ausgeführt (in der Regel ist dies Ihr Laufwerk `C:`).</span><span class="sxs-lookup"><span data-stu-id="28b70-163">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="28b70-164">Stellen Sie sicher, dass die Verteilungen auf dem Systemlaufwerk gespeichert sind:</span><span class="sxs-lookup"><span data-stu-id="28b70-164">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="28b70-165">Öffnen Sie **Einstellungen** -> **Speicher** -> **Weitere Speichereinstellungen: Ändern Sie den Speicherort für neue Inhalte**
    ![Abbildung der Systemeinstellungen für die Installation von Apps auf dem Laufwerk C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="28b70-165">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="28b70-166">**WslRegisterDistribution failed with error 0x8007019e (WslRegisterDistribution-Fehler mit Fehlercode 0x8007019e)**</span><span class="sxs-lookup"><span data-stu-id="28b70-166">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="28b70-167">Die optionale Komponente des Windows-Subsystems für Linux ist nicht aktiviert:</span><span class="sxs-lookup"><span data-stu-id="28b70-167">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="28b70-168">Öffnen Sie **Systemsteuerung** -> **Programme und Funktionen** -> **Windows-Funktion aktivieren oder deaktivieren**. Aktivieren Sie die Option **Windows-Subsystem für Linux**, oder verwenden Sie das PowerShell-Cmdlet, das am Anfang dieses Artikels erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="28b70-168">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="28b70-169">**Fehler 0x80070003 oder Fehler 0x80370102 während der Installation**</span><span class="sxs-lookup"><span data-stu-id="28b70-169">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="28b70-170">Stellen Sie sicher, dass im BIOS Ihres Computers die Virtualisierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="28b70-170">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="28b70-171">Die Anweisungen zur Aktivierung variieren je nach Computer. Die entsprechenden Optionen befinden sich wahrscheinlich in den CPU-bezogenen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="28b70-171">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="28b70-172">**Fehler beim Upgradeversuch: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="28b70-172">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="28b70-173">Stellen Sie sicher, dass das Windows-Subsystem für Linux aktiviert wurde und Sie Windows-Build 19041 oder höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="28b70-173">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 19041 or higher.</span></span> <span data-ttu-id="28b70-174">Führen Sie zum Aktivieren von WSL in einer PowerShell-Eingabeaufforderung mit Administratorberechtigungen diesen Befehl aus: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="28b70-174">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="28b70-175">Die vollständigen Anweisungen zur WSL-Installation finden Sie [hier](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="28b70-175">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

- <span data-ttu-id="28b70-176">**Der angeforderte Vorgang konnte aufgrund einer Einschränkung des virtuellen Dateisystems nicht abgeschlossen werden. Dateien für virtuelle Festplatten müssen unkomprimiert und unverschlüsselt sein und dürfen keine geringe Dichte aufweisen.**</span><span class="sxs-lookup"><span data-stu-id="28b70-176">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="28b70-177">Prüfen Sie den [WSL GitHub-Thread #4103](https://github.com/microsoft/WSL/issues/4103), der diesem Thema gewidmet ist, auf aktualisierte Informationen.</span><span class="sxs-lookup"><span data-stu-id="28b70-177">Please check [WSL GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="28b70-178">**Der Ausdruck 'wsl' wurde nicht als Name eines Cmdlets, einer Funktion, einer Skriptdatei oder eines ausführbaren Programms erkannt.**</span><span class="sxs-lookup"><span data-stu-id="28b70-178">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="28b70-179">Vergewissern Sie sich, dass die [optionale Komponente Windows-Subsystem für Linux installiert ist](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="28b70-179">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="28b70-180">Außerdem wird dieser Fehler angezeigt, wenn Sie ein ARM64-Gerät verwenden und diesen Befehl aus PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="28b70-180">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="28b70-181">Führen Sie stattdessen `wsl.exe` in [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) oder einer Eingabeaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="28b70-181">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
