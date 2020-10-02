---
title: Aktualisieren des WSL2-Linux-Kernels
description: Anweisungen zum manuellen Aktualisieren Ihres WSL2-Linux-Kernels
keywords: WSL, Windows, Linux-Kernel, Windows-Subsystem für Linux, Kernel
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7bf2ef606d0bd23083f323117348aeea87c52b10
ms.sourcegitcommit: f1996541005ae126ef379d8aebfe1abfcccb9ac9
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/25/2020
ms.locfileid: "91238796"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>Aktualisieren des WSL2-Linux-Kernels

Um den Linux-Kernel innerhalb von WSL2 manuell zu aktualisieren, führen Sie die folgenden Schritte aus.

> [!NOTE] 
> Wenn das Installationsprogramm WSL 1 nicht finden kann, klicken Sie mit der rechten Maustaste auf das Installationsprogramm für das Linux-Kernel-Update, wählen Sie „Deinstallieren“ aus, und starten Sie das Installationsprogramm erneut.

## <a name="download-the-linux-kernel-update-package"></a>Herunterladen des Updatepakets für den Linux-Kernel

[Laden Sie das neueste Updatepaket für den WSL2-Linux-Kernel für x64-Computer herunter](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi).

> [!NOTE]
> Wenn Sie einen ARM64-Computer verwenden, laden Sie stattdessen [das ARM64-Paket](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) herunter.

## <a name="install-the-linux-kernel-update-package"></a>Installieren des Updatepakets für den Linux-Kernel

So installieren Sie das Updatepaket für den Linux-Kernel

  1. Führen Sie das im vorherigen Schritt heruntergeladene Updatepaket aus.

  2. Sie werden zur Eingabe erhöhter Berechtigungen aufgefordert. Wählen Sie „Ja“, um diese Installation zu genehmigen.

  3. Sobald die Installation abgeschlossen ist, können Sie mit der Nutzung von WSL2 beginnen!

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>Zukünftige Pläne zur Aktualisierung des WSL2-Linux-Kernels

Weitere Informationen finden Sie im Artikel über die [Änderungen an der Aktualisierung des WSL2 Linux-Kernels](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) im [Blog zur Windows-Befehlszeile](https://aka.ms/cliblog).

## <a name="troubleshooting"></a>Problembehandlung

### <a name="this-update-only-applies-to-machines-with-the-windows-subsystem-for-linux"></a>Dieses Update gilt nur für Computer mit dem Windows-Subsystem für Linux.
Zum Installieren des MSI-Kernels ist WSL erforderlich und sollte zuerst aktiviert werden. Wenn ein Fehler auftritt, wird die folgende Meldung angezeigt: `This update only applies to machines with the Windows Subsystem for Linux`. 

Es gibt drei mögliche Gründe, warum diese Meldung angezeigt wird:

1. Sie befinden sich immer noch in der alten Version von Windows, die WSL 2 nicht unterstützt. Überprüfen Sie die [WSL 2-Anforderungen](https://docs.microsoft.com/windows/wsl/install-win10#update-to-wsl-2), und führen Sie ein Upgrade aus, um WSL 2 zu verwenden. 
2. `Windows Subsystem for Linux` ist nicht aktiviert. Folgen Sie dem [Installationsleitfaden für das Windows-Subsystem für Linux](https://docs.microsoft.com/windows/wsl/install-win10).
3. Nachdem Sie `Windows Subsystem for Linux` aktiviert haben, muss ein Neustart durchgeführt werden, damit es wirksam wird. Starten Sie den Computer neu, und wiederholen Sie den Vorgang.

### `WSL 2 requires an update to its kernel component. For information please visit https://aka.ms/wsl2kernel`

Jedes Mal, wenn der Kernel in „%SystemRoot%\system32\lxss\tools\,“ fehlt, wird möglicherweise der oben angegebene Fehler angezeigt.

Es folgen einige Möglichkeiten, um das Problem zu beheben:

1. Installieren Sie den Linux-Kernel manuell, indem Sie die Anweisungen auf dieser Seite befolgen.
2. Deinstallieren Sie den MSI über die Option „Software“, und installieren Sie ihn erneut.