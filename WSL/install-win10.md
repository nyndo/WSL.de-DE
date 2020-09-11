---
title: Installieren des Windows-Subsystems für Linux (WSL) unter Windows 10
description: Erfahren Sie, wie Sie das Windows-Subsystem für Linux unter Windows 10 installieren. Windows 10 muss auf Version 2004, Build 19041 oder höher aktualisiert werden.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Installieren, Aktivieren, WSL2, Version 2
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 50b434e288ba90173875cf5e7cd5fe9e6c3d8a16
ms.sourcegitcommit: 498592fa4b09015be3ee9a8913e5e3cf755de24b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "89559290"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="7a16d-105">Windows-Subsystem für Linux: Installationsleitfaden für Windows 10</span><span class="sxs-lookup"><span data-stu-id="7a16d-105">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="7a16d-106">Installieren des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="7a16d-106">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="7a16d-107">Bevor Sie eine Linux-Verteilung unter Windows installieren können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a16d-107">Before installing any Linux distributions on Windows, you must enable the "Windows Subsystem for Linux" optional feature.</span></span>

<span data-ttu-id="7a16d-108">Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7a16d-108">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

<span data-ttu-id="7a16d-109">Um nur WSL 1 zu installieren, sollten Sie nun den Computer neu starten und mit dem [Installieren der Linux-Verteilung Ihrer Wahl](./install-win10.md#install-your-linux-distribution-of-choice) fortfahren. Andernfalls warten Sie auf den Neustart, und fahren Sie mit dem Update auf WSL 2 fort.</span><span class="sxs-lookup"><span data-stu-id="7a16d-109">To only install WSL 1, you should now restart your machine and move on to [Install your Linux distribution of choice](./install-win10.md#install-your-linux-distribution-of-choice), otherwise wait to restart and move on to update to WSL 2.</span></span> <span data-ttu-id="7a16d-110">Erfahren Sie mehr über den [Vergleich zwischen WSL 2 und WSL 1](./compare-versions.md).</span><span class="sxs-lookup"><span data-stu-id="7a16d-110">Read more about [Comparing WSL 2 and WSL 1](./compare-versions.md).</span></span>

## <a name="update-to-wsl-2"></a><span data-ttu-id="7a16d-111">Aktualisieren auf WSL 2</span><span class="sxs-lookup"><span data-stu-id="7a16d-111">Update to WSL 2</span></span>

<span data-ttu-id="7a16d-112">Um ein Update auf WSL 2 durchführen zu können, müssen die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="7a16d-112">To update to WSL 2, you must meet the following criteria:</span></span>

- <span data-ttu-id="7a16d-113">Ausführen von Windows 10, [aktualisiert auf Version 1903 oder höher](ms-settings:windowsupdate), **Build 18362** oder höher, für x64-Systeme.</span><span class="sxs-lookup"><span data-stu-id="7a16d-113">Running Windows 10, [updated to version 1903 or higher](ms-settings:windowsupdate), **Build 18362** or higher for x64 systems.</span></span>
   - <span data-ttu-id="7a16d-114">Wenn Sie Windows 10, Version 1903 oder 1909, verwenden, stellen Sie sicher, dass die Buildnummer Ihrer Nebenversion 1049 oder höher ist.</span><span class="sxs-lookup"><span data-stu-id="7a16d-114">If you are on Windows 10 version 1903 or 1909 make sure your minor build number is 1049 or higher.</span></span> <span data-ttu-id="7a16d-115">Ausführliche Informationen zur Problembehandlung finden Sie [hier](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2).</span><span class="sxs-lookup"><span data-stu-id="7a16d-115">See [full troubleshooting instructions here](https://docs.microsoft.com/windows/wsl/troubleshooting#im-on-windows-10-version-1903-and-i-still-do-not-see-options-for-wsl-2)</span></span>
- <span data-ttu-id="7a16d-116">Ausführen von Windows 10, aktualisiert auf Version 2004 oder höher, **Build 19041**, für ARM64-Systeme.</span><span class="sxs-lookup"><span data-stu-id="7a16d-116">Running Windows 10, updated to version 2004 or higher, **build 19041**, for ARM64 systems.</span></span>
- <span data-ttu-id="7a16d-117">Beachten Sie, dass Sie unter Windows 10, Version 1903 oder 1909, sicherstellen müssen, dass Sie über den richtigen Backport verfügen. Anweisungen finden Sie [hier](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span><span class="sxs-lookup"><span data-stu-id="7a16d-117">Please note if you are on Windows 10 version 1903 or 1909 you will need to ensure that you have the proper backport, instructions can be [found here](https://devblogs.microsoft.com/commandline/wsl-2-support-is-coming-to-windows-10-versions-1903-and-1909/#how-do-i-get-it).</span></span> 

- <span data-ttu-id="7a16d-118">Überprüfen Sie Ihre Windows-Version, indem Sie die **Windows-Logo-Taste+R** auswählen, **winver** eingeben und **OK** auswählen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-118">Check your Windows version by selecting the **Windows logo key + R**, type **winver**, select **OK**.</span></span> <span data-ttu-id="7a16d-119">(Oder geben Sie den Befehl `ver` an der Windows-Eingabeaufforderung ein.)</span><span class="sxs-lookup"><span data-stu-id="7a16d-119">(Or enter the `ver` command in Windows Command Prompt).</span></span> <span data-ttu-id="7a16d-120">[Aktualisieren Sie auf die neueste Windows-Version](ms-settings:windowsupdate), wenn Ihr Build niedriger als 18361 ist.</span><span class="sxs-lookup"><span data-stu-id="7a16d-120">Please [update to the latest Windows version](ms-settings:windowsupdate) if your build is lower than 18361.</span></span> <span data-ttu-id="7a16d-121">[Holen Sie sich den Windows Update-Assistenten](https://www.microsoft.com/software-download/windows10).</span><span class="sxs-lookup"><span data-stu-id="7a16d-121">[Get Windows Update Assistant](https://www.microsoft.com/software-download/windows10).</span></span>

### <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="7a16d-122">Aktivieren Sie die optionale Komponente „Virtual Machine Platform“.</span><span class="sxs-lookup"><span data-stu-id="7a16d-122">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="7a16d-123">Vor der Installation von WSL 2 müssen Sie das optionale Feature „Virtual Machine Platform“ aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a16d-123">Before installing WSL 2, you must enable the "Virtual Machine Platform" optional feature.</span></span>

<span data-ttu-id="7a16d-124">Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7a16d-124">Open PowerShell as Administrator and run:</span></span>

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="7a16d-125">**Starten Sie Ihrem Computer neu**, um die WSL-Installation und das Update auf WSL 2 abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-125">**Restart** your machine to complete the WSL install and update to WSL 2.</span></span>

### <a name="set-wsl-2-as-your-default-version"></a><span data-ttu-id="7a16d-126">Festlegen von WSL 2 als Standardversion</span><span class="sxs-lookup"><span data-stu-id="7a16d-126">Set WSL 2 as your default version</span></span>

<span data-ttu-id="7a16d-127">Öffnen Sie PowerShell als Administrator und führen Sie den folgenden Befehl aus, um WSL 2 als Standardversion bei der Installation einer neuen Linux-Verteilung festzulegen:</span><span class="sxs-lookup"><span data-stu-id="7a16d-127">Open PowerShell as Administrator and run this command to set WSL 2 as the default version when installing a new Linux distribution:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="7a16d-128">Diese Meldung wird möglicherweise nach dem Ausführen des folgenden Befehls angezeigt: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span><span class="sxs-lookup"><span data-stu-id="7a16d-128">You might see this message after running that command: `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`.</span></span> <span data-ttu-id="7a16d-129">Befolgen Sie den Link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)), und installieren Sie die MSI von dieser Seite in unserer Dokumentation, um einen Linux-Kernel auf Ihrem Computer zu installieren, der von WSL 2 verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7a16d-129">Please follow the link ([https://aka.ms/wsl2kernel](https://aka.ms/wsl2kernel)) and install the MSI from that page on our documentation to install a Linux kernel on your machine for WSL 2 to use.</span></span> <span data-ttu-id="7a16d-130">Sobald Sie den Kernel installiert haben, führen Sie den Befehl erneut aus. Er sollte nun erfolgreich abgeschlossen werden, ohne dass die Meldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7a16d-130">Once you have the kernel installed, please run the command again and it should complete successfully without showing the message.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a16d-131">Die Aktualisierung von WSL 1 auf WSL 2 kann je nach Umfang Ihrer Zielverteilung mehrere Minuten dauern.</span><span class="sxs-lookup"><span data-stu-id="7a16d-131">The update from WSL 1 to WSL 2 may take several minutes to complete depending on the size of your targeted distribution.</span></span> <span data-ttu-id="7a16d-132">Wenn Sie eine ältere (Legacy) Installation der WSL 1 von Windows 10 Anniversary Update oder Creators Update aus ausführen, kann ein Updatefehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="7a16d-132">If you are running an older (legacy) installation of WSL 1 from Windows 10 Anniversary Update or Creators Update, you may encounter an update error.</span></span> <span data-ttu-id="7a16d-133">Befolgen Sie diese Anweisungen, um [alle Legacyverteilungen zu deinstallieren und zu entfernen](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span><span class="sxs-lookup"><span data-stu-id="7a16d-133">Follow these instructions to [uninstall and remove any legacy distributions](https://docs.microsoft.com/windows/wsl/install-legacy#uninstallingremoving-the-legacy-distro).</span></span> 
>
> <span data-ttu-id="7a16d-134">Wenn `wsl --set-default-version` als ungültiger Befehl angezeigt wird, geben Sie `wsl --help` ein.</span><span class="sxs-lookup"><span data-stu-id="7a16d-134">If `wsl --set-default-version` results as an invalid command, enter `wsl --help`.</span></span> <span data-ttu-id="7a16d-135">Wenn die `--set-default-version` nicht aufgeführt ist, bedeutet dies, dass Ihr Betriebssystem sie nicht unterstützt und Sie auf Version 1903, Build 18362 oder höher, aktualisieren müssen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-135">If the `--set-default-version` is not listed, it means that your OS doesn't support it and you need to update to version 1903, Build 18362 or higher.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="7a16d-136">Installieren der Linux-Verteilung Ihrer Wahl</span><span class="sxs-lookup"><span data-stu-id="7a16d-136">Install your Linux distribution of choice</span></span>

1. <span data-ttu-id="7a16d-137">Öffnen Sie den [Microsoft Store](https://aka.ms/wslstore), und wählen Sie Ihre bevorzugte Linux-Verteilung aus.</span><span class="sxs-lookup"><span data-stu-id="7a16d-137">Open the [Microsoft Store](https://aka.ms/wslstore) and select your favorite Linux distribution.</span></span>

    ![Ansicht der Linux-Verteilungen im Microsoft Store](media/store.png)

    <span data-ttu-id="7a16d-139">Über die folgenden Links wird die Seite des Microsoft Store für jede Distribution geöffnet:</span><span class="sxs-lookup"><span data-stu-id="7a16d-139">The following links will open the Microsoft store page for each distribution:</span></span>

    - [<span data-ttu-id="7a16d-140">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="7a16d-140">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    - [<span data-ttu-id="7a16d-141">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="7a16d-141">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    - [<span data-ttu-id="7a16d-142">Ubuntu 20.04 LTS</span><span class="sxs-lookup"><span data-stu-id="7a16d-142">Ubuntu 20.04 LTS</span></span>](https://www.microsoft.com/store/apps/9n6svws3rx71)
    - [<span data-ttu-id="7a16d-143">openSUSE Leap 15.1</span><span class="sxs-lookup"><span data-stu-id="7a16d-143">openSUSE Leap 15.1</span></span>](https://www.microsoft.com/store/apps/9NJFZK00FGKV)
    - [<span data-ttu-id="7a16d-144">SUSE Linux Enterprise Server 12 SP5</span><span class="sxs-lookup"><span data-stu-id="7a16d-144">SUSE Linux Enterprise Server 12 SP5</span></span>](https://www.microsoft.com/store/apps/9MZ3D1TRP8T1)
    - [<span data-ttu-id="7a16d-145">SUSE Linux Enterprise Server 15 SP1</span><span class="sxs-lookup"><span data-stu-id="7a16d-145">SUSE Linux Enterprise Server 15 SP1</span></span>](https://www.microsoft.com/store/apps/9PN498VPMF3Z)
    - [<span data-ttu-id="7a16d-146">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="7a16d-146">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    - [<span data-ttu-id="7a16d-147">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="7a16d-147">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    - [<span data-ttu-id="7a16d-148">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="7a16d-148">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    - [<span data-ttu-id="7a16d-149">Pengwin</span><span class="sxs-lookup"><span data-stu-id="7a16d-149">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    - [<span data-ttu-id="7a16d-150">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="7a16d-150">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    - [<span data-ttu-id="7a16d-151">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="7a16d-151">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

2. <span data-ttu-id="7a16d-152">Wählen Sie auf der Seite der Verteilung die Option „Get“ (Abrufen) aus.</span><span class="sxs-lookup"><span data-stu-id="7a16d-152">From the distribution's page, select "Get".</span></span>

    ![Linux-Verteilungen im Microsoft Store](media/UbuntuStore.png)

## <a name="set-up-a-new-distribution"></a><span data-ttu-id="7a16d-154">Einrichten einer neuen Verteilung</span><span class="sxs-lookup"><span data-stu-id="7a16d-154">Set up a new distribution</span></span>

<span data-ttu-id="7a16d-155">Wenn Sie eine neu installierte Linux-Verteilung zum ersten Mal starten, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, ein oder zwei Minuten zu warten, bis die Dateien dekomprimiert und auf dem PC gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="7a16d-155">The first time you launch a newly installed Linux distribution, a console window will open and you'll be asked to wait for a minute or two for files to de-compress and be stored on your PC.</span></span> <span data-ttu-id="7a16d-156">Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-156">All future launches should take less than a second.</span></span>

<span data-ttu-id="7a16d-157">Anschließend müssen Sie [ein Benutzerkonto und Kennwort für Ihre neue Linux-Verteilung erstellen](./user-support.md).</span><span class="sxs-lookup"><span data-stu-id="7a16d-157">You will then need to [create a user account and password for your new Linux distribution](./user-support.md).</span></span>

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

## <a name="set-your-distribution-version-to-wsl-1-or-wsl-2"></a><span data-ttu-id="7a16d-159">Festlegen der Verteilungsversion auf WSL 1 oder WSL 2</span><span class="sxs-lookup"><span data-stu-id="7a16d-159">Set your distribution version to WSL 1 or WSL 2</span></span>

<span data-ttu-id="7a16d-160">Sie können die den einzelnen installierten Linux-Distributionen zugewiesenen WSL-Version überprüfen, indem Sie die PowerShell-Befehlszeile öffnen und den folgenden Befehl (nur verfügbar in [Windows Build 18362 oder höher](ms-settings:windowsupdate)) eingeben: `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="7a16d-160">You can check the WSL version assigned to each of the Linux distributions you have installed by opening the PowerShell command line and entering the command (only available in [Windows Build 18362 or higher](ms-settings:windowsupdate)): `wsl -l -v`</span></span>

```powershell
wsl --list --verbose
```

<span data-ttu-id="7a16d-161">Um eine Verteilung so einzurichten, dass sie von einer der beiden WSL-Versionen unterstützt wird, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7a16d-161">To set a distribution to be backed by either version of WSL please run:</span></span>

```powershell
wsl --set-version <distribution name> <versionNumber>
```

<span data-ttu-id="7a16d-162">Ersetzen Sie hierbei `<distribution name>` durch den tatsächlichen Namen Ihrer Verteilung und `<versionNumber>` durch die Ziffer „1“ oder „2“.</span><span class="sxs-lookup"><span data-stu-id="7a16d-162">Make sure to replace `<distribution name>` with the actual name of your distribution and `<versionNumber>` with the number '1' or '2'.</span></span> <span data-ttu-id="7a16d-163">Sie können jederzeit zu WSL 1 zurückwechseln, indem sie denselben Befehl wie oben ausführen, aber die 2 durch eine 1 ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-163">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="7a16d-164">Wenn Sie WSL 2 als Ihre Standardarchitektur festlegen möchten, ist dies über diesen Befehl möglich:</span><span class="sxs-lookup"><span data-stu-id="7a16d-164">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```powershell
wsl --set-default-version 2
```

<span data-ttu-id="7a16d-165">Dadurch wird die Version jeder neu installierten Verteilung auf WSL 2 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7a16d-165">This will set the version of any new distribution installed to WSL 2.</span></span>

## <a name="troubleshooting-installation"></a><span data-ttu-id="7a16d-166">Problembehandlung bei der Installation</span><span class="sxs-lookup"><span data-stu-id="7a16d-166">Troubleshooting installation</span></span>

<span data-ttu-id="7a16d-167">Nachfolgend werden einige Fehler und vorgeschlagene Korrekturen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7a16d-167">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="7a16d-168">Weitere allgemeine Fehler und zugehörige Lösungen finden Sie auf der [Seite für die WSL-Problembehandlung](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="7a16d-168">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

- <span data-ttu-id="7a16d-169">**Installation failed with error 0x80070003 (Installationsfehler mit Fehlercode 0x80070003)**</span><span class="sxs-lookup"><span data-stu-id="7a16d-169">**Installation failed with error 0x80070003**</span></span>
  - <span data-ttu-id="7a16d-170">Das Windows-Subsystem für Linux wird nur auf dem Systemlaufwerk ausgeführt (in der Regel ist dies Ihr Laufwerk `C:`).</span><span class="sxs-lookup"><span data-stu-id="7a16d-170">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="7a16d-171">Stellen Sie sicher, dass die Verteilungen auf dem Systemlaufwerk gespeichert sind:</span><span class="sxs-lookup"><span data-stu-id="7a16d-171">Make sure that distributions are stored on your system drive:</span></span>  
  - <span data-ttu-id="7a16d-172">Öffnen Sie **Einstellungen** -> **Speicher** -> **Weitere Speichereinstellungen: Ändern Sie den Speicherort für neue Inhalte**
    ![Abbildung der Systemeinstellungen für die Installation von Apps auf dem Laufwerk C:](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="7a16d-172">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>

- <span data-ttu-id="7a16d-173">**WslRegisterDistribution failed with error 0x8007019e (WslRegisterDistribution-Fehler mit Fehlercode 0x8007019e)**</span><span class="sxs-lookup"><span data-stu-id="7a16d-173">**WslRegisterDistribution failed with error 0x8007019e**</span></span>
  - <span data-ttu-id="7a16d-174">Die optionale Komponente des Windows-Subsystems für Linux ist nicht aktiviert:</span><span class="sxs-lookup"><span data-stu-id="7a16d-174">The Windows Subsystem for Linux optional component is not enabled:</span></span>
  - <span data-ttu-id="7a16d-175">Öffnen Sie **Systemsteuerung** -> **Programme und Funktionen** -> **Windows-Funktion aktivieren oder deaktivieren**. Aktivieren Sie die Option **Windows-Subsystem für Linux**, oder verwenden Sie das PowerShell-Cmdlet, das am Anfang dieses Artikels erwähnt wurde.</span><span class="sxs-lookup"><span data-stu-id="7a16d-175">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the beginning of this article.</span></span>

- <span data-ttu-id="7a16d-176">**Fehler 0x80070003 oder Fehler 0x80370102 während der Installation**</span><span class="sxs-lookup"><span data-stu-id="7a16d-176">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
  - <span data-ttu-id="7a16d-177">Stellen Sie sicher, dass im BIOS Ihres Computers die Virtualisierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7a16d-177">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="7a16d-178">Die Anweisungen zur Aktivierung variieren je nach Computer. Die entsprechenden Optionen befinden sich wahrscheinlich in den CPU-bezogenen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-178">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>

- <span data-ttu-id="7a16d-179">**Fehler beim Upgradeversuch: `Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="7a16d-179">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
  - <span data-ttu-id="7a16d-180">Stellen Sie sicher, dass das Windows-Subsystem für Linux aktiviert wurde und Sie die Windows-Buildversion 18362 oder höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a16d-180">Enure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18362 or higher.</span></span> <span data-ttu-id="7a16d-181">Führen Sie zum Aktivieren von WSL in einer PowerShell-Eingabeaufforderung mit Administratorberechtigungen diesen Befehl aus: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span><span class="sxs-lookup"><span data-stu-id="7a16d-181">To enable WSL run this command in a PowerShell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span>

- <span data-ttu-id="7a16d-182">**Der angeforderte Vorgang konnte aufgrund einer Einschränkung des virtuellen Dateisystems nicht abgeschlossen werden. Dateien für virtuelle Festplatten müssen unkomprimiert und unverschlüsselt sein und dürfen keine geringe Dichte aufweisen.**</span><span class="sxs-lookup"><span data-stu-id="7a16d-182">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
  - <span data-ttu-id="7a16d-183">Zum Deaktivieren von „Inhalte komprimieren“ (sowie „Inhalte verschlüsseln“, falls aktiviert), öffnen Sie den Profilordner Ihrer Linux-Verteilung.</span><span class="sxs-lookup"><span data-stu-id="7a16d-183">Deselect “Compress contents” (as well as “Encrypt contents” if that’s checked) by opening the profile folder for your Linux distribution.</span></span> <span data-ttu-id="7a16d-184">Er sollte sich in einem Ordner auf Ihrem Windows-Dateisystem befinden, der etwa folgendermaßen heißt: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`.</span><span class="sxs-lookup"><span data-stu-id="7a16d-184">It should be located in a folder on your Windows file system, something like: `USERPROFILE%\AppData\Local\Packages\CanonicalGroupLimited...`</span></span>
  - <span data-ttu-id="7a16d-185">In diesem Linux-Verteilungsprofil sollte ein Ordner "LocalState" vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="7a16d-185">In this Linux distro profile, there should be a LocalState folder.</span></span> <span data-ttu-id="7a16d-186">Klicken Sie mit der rechten Maustaste auf diesen Ordner, um ein Menü mit Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-186">Right-click this folder to display a menu of options.</span></span> <span data-ttu-id="7a16d-187">Wählen Sie „Eigenschaften“ > „Erweitert“ aus, und stellen Sie dann sicher, dass die Kontrollkästchen „Inhalt komprimieren, um Speicherplatz zu sparen“ und „Inhalt verschlüsseln, um Daten zu schützen“ nicht aktiviert (nicht ausgewählt) sind.</span><span class="sxs-lookup"><span data-stu-id="7a16d-187">Select Properties > Advanced and then ensure that the “Compress contents to save disk space” and “Encrypt contents to secure data” checkboxes are unselected (not checked).</span></span> <span data-ttu-id="7a16d-188">Wenn Sie gefragt werden, ob Sie diese Einstellung nur auf den aktuellen Ordner oder auf alle Unterordner und Dateien anwenden möchten, wählen Sie „Nur dieser Ordner“ aus, da Sie nur das Komprimierungsflag löschen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-188">If you are asked whether to apply this to just to the current folder or to all subfolders and files, select “just this folder” because you are only clearing the compress flag.</span></span> <span data-ttu-id="7a16d-189">Danach sollte der Befehl `wsl --set-version` funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7a16d-189">After this, the `wsl --set-version` command should work.</span></span>

![Screenshot der Eigenschafteneinstellungen der WSL-Verteilung](media/troubleshooting-virtualdisk-compress.png)

> [!NOTE]
> <span data-ttu-id="7a16d-191">In meinem Fall befand sich der Ordner „LocalState“ für meine Ubuntu 18.04-Verteilung unter „C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc“.</span><span class="sxs-lookup"><span data-stu-id="7a16d-191">In my case, the LocalState folder for my Ubuntu 18.04 distribution was located at C:\Users\<my-user-name>\AppData\Local\Packages\CanonicalGroupLimited.Ubuntu18.04onWindows_79rhkp1fndgsc</span></span>
>
> <span data-ttu-id="7a16d-192">Prüfen Sie den [GitHub-Thread #4103 in der WSL-Dokumentation](https://github.com/microsoft/WSL/issues/4103), der diesem Thema gewidmet ist, auf aktualisierte Informationen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-192">Check [WSL Docs GitHub thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

- <span data-ttu-id="7a16d-193">**Der Ausdruck 'wsl' wurde nicht als Name eines Cmdlets, einer Funktion, einer Skriptdatei oder eines ausführbaren Programms erkannt.**</span><span class="sxs-lookup"><span data-stu-id="7a16d-193">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span>
  - <span data-ttu-id="7a16d-194">Vergewissern Sie sich, dass die [optionale Komponente Windows-Subsystem für Linux installiert ist](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span><span class="sxs-lookup"><span data-stu-id="7a16d-194">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./install-win10.md#enable-the-virtual-machine-platform-optional-component).</span></span> <span data-ttu-id="7a16d-195">Außerdem wird dieser Fehler angezeigt, wenn Sie ein ARM64-Gerät verwenden und diesen Befehl aus PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="7a16d-195">Additionally, if you are using an ARM64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="7a16d-196">Führen Sie stattdessen `wsl.exe` in [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) oder einer Eingabeaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="7a16d-196">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span>
