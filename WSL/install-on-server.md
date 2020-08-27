---
title: Installieren des Linux-Subsystems unter Windows Server
description: Erfahren Sie, wie Sie das Linux-Subsystem unter Windows Server installieren. WSL ist für die Installation unter Windows Server 2019 (Version 1709) und höher verfügbar.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 501bbf78c2d9f59dad945af9c30571317240b79f
ms.sourcegitcommit: fb79750bd71d6ebaed5203b3de71ba85a67227b1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2020
ms.locfileid: "88866147"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="e6f70-105">Windows Server-Installationsleitfaden</span><span class="sxs-lookup"><span data-stu-id="e6f70-105">Windows Server Installation Guide</span></span>

<span data-ttu-id="e6f70-106">Das Windows-Subsystem für Linux ist für die Installation unter Windows Server 2019 (Version 1709) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e6f70-106">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="e6f70-107">Diese Anleitung führt Sie durch die Schritte zum Aktivieren von WSL auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="e6f70-107">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="e6f70-108">Aktivieren des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="e6f70-108">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="e6f70-109">Damit Sie Linux-Distributionen unter Windows ausführen können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ aktivieren und das System neu starten.</span><span class="sxs-lookup"><span data-stu-id="e6f70-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="e6f70-110">Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="e6f70-110">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="e6f70-111">Herunterladen einer Linux-Verteilung</span><span class="sxs-lookup"><span data-stu-id="e6f70-111">Download a Linux distribution</span></span>

<span data-ttu-id="e6f70-112">Befolgen Sie [diese Anweisungen](install-manual.md), um Ihre bevorzugte Linux-Distribution herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="e6f70-112">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="e6f70-113">Extrahieren und Installieren einer Linux-Verteilung</span><span class="sxs-lookup"><span data-stu-id="e6f70-113">Extract and install a Linux distribution</span></span>

<span data-ttu-id="e6f70-114">Nachdem Sie nun eine Linux-Verteilung heruntergeladen haben, um ihren Inhalt zu extrahieren und manuell zu installieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e6f70-114">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="e6f70-115">Extrahieren Sie den Inhalt des `<distro>.appx`-Pakets mithilfe von PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e6f70-115">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="e6f70-116">Führen Sie die Startanwendung der Verteilung im Zielordner aus.</span><span class="sxs-lookup"><span data-stu-id="e6f70-116">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="e6f70-117">Die Startanwendung heißt normalerweise `<distro>.exe` (z. B. `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="e6f70-117">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Aufgeklappte Ubuntu-Distribution unter Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="e6f70-119">**Installation failed with error 0x8007007e** (Installationsfehler mit Fehlercode 0x8007007e): Sie erhalten diesen Fehler, wenn das System WSL nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6f70-119">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="e6f70-120">Stellen Sie sicher, dass Sie Windows-Build 16215 oder höher aus führen.</span><span class="sxs-lookup"><span data-stu-id="e6f70-120">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="e6f70-121">[Überprüfen Sie Ihren Build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="e6f70-121">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="e6f70-122">[Vergewissern Sie sich auch, dass die WSL aktiviert ist](troubleshooting.md#confirm-wsl-is-enabled) und Ihr Computer neu gestartet wurde, nachdem das Feature aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="e6f70-122">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="e6f70-123">3. Fügen Sie der Windows-Umgebungsvariablen PATH den Pfad der Verteilung hinzu (in diesem Beispiel `C:\Users\Administrator\Ubuntu`), mithilfe von PowerShell:</span><span class="sxs-lookup"><span data-stu-id="e6f70-123">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="e6f70-124">Sie können Ihre Verteilung nun über einen beliebigen Pfad starten, indem Sie `<distro>.exe`eingeben.</span><span class="sxs-lookup"><span data-stu-id="e6f70-124">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="e6f70-125">Beispiel: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="e6f70-125">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="e6f70-126">Nachdem der Installation müssen Sie [Ihre neue Verteilungsinstanz initialisieren](initialize-distro.md), bevor Sie sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="e6f70-126">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
