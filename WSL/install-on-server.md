---
title: Installieren des Linux-Subsystems unter Windows Server
description: Installationsanweisungen für das Linux-Subsystem unter Windows Server.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, windows server
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: ebcd7f6b10d2b734b1f2a66f64a5e3292855bcf4
ms.sourcegitcommit: 5d3898772851e6ac9a310f219cc0d71278f95d22
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2020
ms.locfileid: "84671020"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="8cb92-104">Windows Server-Installationsleitfaden</span><span class="sxs-lookup"><span data-stu-id="8cb92-104">Windows Server Installation Guide</span></span>

<span data-ttu-id="8cb92-105">Das Windows-Subsystem für Linux ist für die Installation unter Windows Server 2019 (Version 1709) und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8cb92-105">The Windows Subsystem for Linux is available for installation on Windows Server 2019 (version 1709) and later.</span></span> <span data-ttu-id="8cb92-106">Diese Anleitung führt Sie durch die Schritte zum Aktivieren von WSL auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="8cb92-106">This guide will walk through the steps of enabling WSL on your machine.</span></span>

## <a name="enable-the-windows-subsystem-for-linux"></a><span data-ttu-id="8cb92-107">Aktivieren des Windows-Subsystems für Linux</span><span class="sxs-lookup"><span data-stu-id="8cb92-107">Enable the Windows Subsystem for Linux</span></span>

<span data-ttu-id="8cb92-108">Damit Sie Linux-Distributionen unter Windows ausführen können, müssen Sie das optionale Feature „Windows-Subsystem für Linux“ aktivieren und das System neu starten.</span><span class="sxs-lookup"><span data-stu-id="8cb92-108">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

<span data-ttu-id="8cb92-109">Öffnen Sie PowerShell als Administrator, und führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8cb92-109">Open PowerShell as Administrator and run:</span></span>

```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

```

## <a name="download-a-linux-distribution"></a><span data-ttu-id="8cb92-110">Herunterladen einer Linux-Verteilung</span><span class="sxs-lookup"><span data-stu-id="8cb92-110">Download a Linux distribution</span></span>

<span data-ttu-id="8cb92-111">Befolgen Sie [diese Anweisungen](install-manual.md), um Ihre bevorzugte Linux-Distribution herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="8cb92-111">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distribution"></a><span data-ttu-id="8cb92-112">Extrahieren und Installieren einer Linux-Verteilung</span><span class="sxs-lookup"><span data-stu-id="8cb92-112">Extract and install a Linux distribution</span></span>

<span data-ttu-id="8cb92-113">Nachdem Sie nun eine Linux-Verteilung heruntergeladen haben, um ihren Inhalt zu extrahieren und manuell zu installieren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="8cb92-113">Now that you've downloaded a Linux distribution, in order to extract its contents and manually install, follow these steps:</span></span>

1. <span data-ttu-id="8cb92-114">Extrahieren Sie den Inhalt des `<distro>.appx`-Pakets mithilfe von PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8cb92-114">Extract the `<distro>.appx` package's contents, using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="8cb92-115">Führen Sie die Startanwendung der Verteilung im Zielordner aus.</span><span class="sxs-lookup"><span data-stu-id="8cb92-115">Run the distribution launcher application in the target folder.</span></span> <span data-ttu-id="8cb92-116">Die Startanwendung heißt normalerweise `<distro>.exe` (z. B. `ubuntu.exe`).</span><span class="sxs-lookup"><span data-stu-id="8cb92-116">The launcher is typically named `<distro>.exe` (for example, `ubuntu.exe`).</span></span>

    ![Aufgeklappte Ubuntu-Distribution unter Windows Server](media/server-appx-expand.png)

> [!CAUTION]
> <span data-ttu-id="8cb92-118">**Installation failed with error 0x8007007e** (Installationsfehler mit Fehlercode 0x8007007e): Sie erhalten diesen Fehler, wenn das System WSL nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb92-118">**Installation failed with error 0x8007007e**: If you receive this error, then your system doesn't support WSL.</span></span> <span data-ttu-id="8cb92-119">Stellen Sie sicher, dass Sie Windows-Build 16215 oder höher aus führen.</span><span class="sxs-lookup"><span data-stu-id="8cb92-119">Ensure that you're running Windows build 16215 or later.</span></span> <span data-ttu-id="8cb92-120">[Überprüfen Sie Ihren Build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="8cb92-120">[Check your build](troubleshooting.md#check-your-build-number).</span></span> <span data-ttu-id="8cb92-121">[Vergewissern Sie sich auch, dass die WSL aktiviert ist](troubleshooting.md#confirm-wsl-is-enabled) und Ihr Computer neu gestartet wurde, nachdem das Feature aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb92-121">Also check to [confirm that WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled) and your computer was restarted after the feature was enabled.</span></span>  

<span data-ttu-id="8cb92-122">3. Fügen Sie der Windows-Umgebungsvariablen PATH den Pfad der Verteilung hinzu (in diesem Beispiel `C:\Users\Administrator\Ubuntu`), mithilfe von PowerShell:</span><span class="sxs-lookup"><span data-stu-id="8cb92-122">3.Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), using PowerShell:</span></span>

```powershell
$userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
[System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
```

<span data-ttu-id="8cb92-123">Sie können Ihre Verteilung nun über einen beliebigen Pfad starten, indem Sie `<distro>.exe`eingeben.</span><span class="sxs-lookup"><span data-stu-id="8cb92-123">You can now launch your distribution from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="8cb92-124">Beispiel: `ubuntu.exe`.</span><span class="sxs-lookup"><span data-stu-id="8cb92-124">For example: `ubuntu.exe`.</span></span>

<span data-ttu-id="8cb92-125">Nachdem der Installation müssen Sie [Ihre neue Verteilungsinstanz initialisieren](initialize-distro.md), bevor Sie sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="8cb92-125">Now that it is installed, you must [initialize your new distribution instance](initialize-distro.md) before using it.</span></span>
