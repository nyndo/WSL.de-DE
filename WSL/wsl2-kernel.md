---
title: Aktualisieren des WSL2-Linux-Kernels
description: Anweisungen zum manuellen Aktualisieren Ihres WSL2-Linux-Kernels
keywords: WSL, Windows, Linux-Kernel, Windows-Subsystem für Linux, Kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7bf2ef606d0bd23083f323117348aeea87c52b10
ms.sourcegitcommit: 609850fadd20687636b8486264e87af47c538111
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/23/2020
ms.locfileid: "92444806"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="ef4b3-104">Aktualisieren des WSL2-Linux-Kernels</span><span class="sxs-lookup"><span data-stu-id="ef4b3-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="ef4b3-105">Um den Linux-Kernel innerhalb von WSL2 manuell zu aktualisieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span>

> [!NOTE] 
> <span data-ttu-id="ef4b3-106">Wenn das Installationsprogramm WSL 1 nicht finden kann, klicken Sie mit der rechten Maustaste auf das Installationsprogramm für das Linux-Kernel-Update, wählen Sie „Deinstallieren“ aus, und starten Sie das Installationsprogramm erneut.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-106">If the installer can't find WSL 1, right-click the Linux kernel update installer and press "Uninstall", then rerun the installer.</span></span>

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="ef4b3-107">Herunterladen des Updatepakets für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="ef4b3-107">Download the Linux kernel update package</span></span>

<span data-ttu-id="ef4b3-108">[Laden Sie das neueste Updatepaket für den WSL2-Linux-Kernel für x64-Computer herunter](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi).</span><span class="sxs-lookup"><span data-stu-id="ef4b3-108">Please [download the latest WSL2 Linux kernel](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) update package for x64 machines.</span></span>

> [!NOTE]
> <span data-ttu-id="ef4b3-109">Wenn Sie einen ARM64-Computer verwenden, laden Sie stattdessen [das ARM64-Paket](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) herunter.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-109">If you're using an ARM64 machine, please download the [ARM64 package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="ef4b3-110">Installieren des Updatepakets für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="ef4b3-110">Install the Linux kernel update package</span></span>

<span data-ttu-id="ef4b3-111">So installieren Sie das Updatepaket für den Linux-Kernel</span><span class="sxs-lookup"><span data-stu-id="ef4b3-111">To install the Linux kernel update package:</span></span>

  1. <span data-ttu-id="ef4b3-112">Führen Sie das im vorherigen Schritt heruntergeladene Updatepaket aus.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-112">Run the update package downloaded in the previous step.</span></span>

  2. <span data-ttu-id="ef4b3-113">Sie werden zur Eingabe erhöhter Berechtigungen aufgefordert. Wählen Sie „Ja“, um diese Installation zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-113">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>

  3. <span data-ttu-id="ef4b3-114">Sobald die Installation abgeschlossen ist, können Sie mit der Nutzung von WSL2 beginnen!</span><span class="sxs-lookup"><span data-stu-id="ef4b3-114">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="ef4b3-115">Zukünftige Pläne zur Aktualisierung des WSL2-Linux-Kernels</span><span class="sxs-lookup"><span data-stu-id="ef4b3-115">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="ef4b3-116">Weitere Informationen finden Sie im Artikel über die [Änderungen an der Aktualisierung des WSL2 Linux-Kernels](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) im [Blog zur Windows-Befehlszeile](https://aka.ms/cliblog).</span><span class="sxs-lookup"><span data-stu-id="ef4b3-116">For more information, read the article [changes to updating the WSL2 Linux kernel](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004), available on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ef4b3-117">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="ef4b3-117">Troubleshooting</span></span>

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a><span data-ttu-id="ef4b3-118">Dieses Update gilt nur für Computer mit dem Windows-Subsystem für Linux.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-118">This update only applies to machines with the Windows Subsystem for Linux</span></span>
<span data-ttu-id="ef4b3-119">Zum Installieren des MSI-Kernels ist WSL erforderlich und sollte zuerst aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-119">To install MSI kernel, WSL is required and should be enabled first.</span></span> <span data-ttu-id="ef4b3-120">Wenn ein Fehler auftritt, wird die folgende Meldung angezeigt: `This update only applies to machines with the Windows Subsystem for Linux`.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-120">If it fails, it you will see the message: `This update only applies to machines with the Windows Subsystem for Linux`.</span></span> 

<span data-ttu-id="ef4b3-121">Es gibt drei mögliche Gründe, warum diese Meldung angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="ef4b3-121">There are three possible reason you see this message:</span></span>

1. <span data-ttu-id="ef4b3-122">Sie befinden sich immer noch in der alten Version von Windows, die WSL 2 nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-122">You are still in old version of Windows which doesn't support WSL 2.</span></span> <span data-ttu-id="ef4b3-123">Überprüfen Sie die [WSL 2-Anforderungen](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2), und führen Sie ein Upgrade aus, um WSL 2 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-123">Please check the [WSL 2 requirements](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2) and upgrade to use WSL 2.</span></span> 
2. <span data-ttu-id="ef4b3-124">`Windows Subsystem for Linux` ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-124">`Windows Subsystem for Linux` is not enabled.</span></span> <span data-ttu-id="ef4b3-125">Folgen Sie dem [Installationsleitfaden für das Windows-Subsystem für Linux](https://docs.microsoft.com/windows/wsl/install-win10).</span><span class="sxs-lookup"><span data-stu-id="ef4b3-125">Please follow the [Windows Subsystem for Linux Installation Guide](https://docs.microsoft.com/windows/wsl/install-win10).</span></span>
3. <span data-ttu-id="ef4b3-126">Nachdem Sie `Windows Subsystem for Linux` aktiviert haben, muss ein Neustart durchgeführt werden, damit es wirksam wird. Starten Sie den Computer neu, und wiederholen Sie den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-126">After you enabled `Windows Subsystem for Linux`, a reboot is required to take into effect, please reboot your machine and try again.</span></span>

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

<span data-ttu-id="ef4b3-127">Jedes Mal, wenn der Kernel in „%SystemRoot%\system32\lxss\tools\,“ fehlt, wird möglicherweise der oben angegebene Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-127">Each time kernel is missing in %SystemRoot%\system32\lxss\tools\, you may run into the above error.</span></span>

<span data-ttu-id="ef4b3-128">Es folgen einige Möglichkeiten, um das Problem zu beheben:</span><span class="sxs-lookup"><span data-stu-id="ef4b3-128">Here are some possible ways to resolve it:</span></span>

1. <span data-ttu-id="ef4b3-129">Installieren Sie den Linux-Kernel manuell, indem Sie die Anweisungen auf dieser Seite befolgen.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-129">Install the Linux kernel manually following the instructions on this page.</span></span>
2. <span data-ttu-id="ef4b3-130">Deinstallieren Sie den MSI über die Option „Software“, und installieren Sie ihn erneut.</span><span class="sxs-lookup"><span data-stu-id="ef4b3-130">Uninstall the MSI from 'Add or Remove Programs', and install it again.</span></span>