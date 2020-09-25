---
title: Erstellen und Aktualisieren von Benutzerkonten für Linux-Verteilungen
description: Referenz für Benutzerkonten und Berechtigungsverwaltung mit dem Windows-Subsystem für Linux.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, user accounts
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 7f1ad56a6f4261ad0455ee93bdeb5e31d0ed10d1
ms.sourcegitcommit: 69fc9d3ca22cf3f07622db4cdf80c8ec751fe620
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2020
ms.locfileid: "90818722"
---
# <a name="create-a-user-account-and-password-for-your-new-linux-distribution"></a><span data-ttu-id="3ac34-104">Erstellen eines Benutzerkontos und Kennworts für Ihre neue Linux-Verteilung</span><span class="sxs-lookup"><span data-stu-id="3ac34-104">Create a user account and password for your new Linux distribution</span></span>

<span data-ttu-id="3ac34-105">Nachdem Sie [WSL aktiviert und eine Linux-Verteilung aus dem Microsoft Store installiert](./install-win10.md) haben, werden Sie beim Öffnen Ihrer neu installierten Linux-Verteilung zunächst aufgefordert, ein Konto zu erstellen, einschließlich **Benutzername** und **Kennwort**.</span><span class="sxs-lookup"><span data-stu-id="3ac34-105">Once you have [enabled WSL and installed a Linux distribution from the Microsoft Store](./install-win10.md), the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="3ac34-106">Diese Kombination aus **Benutzername** und **Kennwort** ist spezifisch für jede einzelne Linux-Verteilung, die Sie installieren, und hat keinen Einfluss auf Ihren Windows-Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-106">This **User Name** and **Password** is specific to each separate Linux distribution that you install and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="3ac34-107">Nachdem Sie einen **Benutzernamen** und das **Kennwort** erstellt haben, ist das Konto Ihr Standardbenutzer für die Verteilung und wird beim Start automatisch angemeldet.</span><span class="sxs-lookup"><span data-stu-id="3ac34-107">Once you create a **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="3ac34-108">Dieses Konto wird als Linux-Administrator angesehen, mit der Möglichkeit, administrative `sudo` (Super User Do)-Befehle auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="3ac34-109">Jede Linux-Distribution, die unter dem Windows-Subsystem für Linux ausgeführt wird, verfügt über eigene Linux-Benutzerkonten und -Kennwörter.</span><span class="sxs-lookup"><span data-stu-id="3ac34-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="3ac34-110">Jedes Mail, wenn Sie eine Verteilung hinzufügen, erneut installieren oder zurücksetzen, müssen Sie ein Linux-Benutzerkonto konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3ac34-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

## <a name="update-and-upgrade-packages"></a><span data-ttu-id="3ac34-112">Update- und Upgradepakete</span><span class="sxs-lookup"><span data-stu-id="3ac34-112">Update and upgrade packages</span></span>

<span data-ttu-id="3ac34-113">Die meisten Verteilungen werden mit einem leeren oder minimalen Paketkatalog ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="3ac34-113">Most distributions ship with an empty or minimal package catalog.</span></span> <span data-ttu-id="3ac34-114">Es wird dringend empfohlen, den Paketkatalog regelmäßig zu aktualisieren und ein Upgrade der installierten Pakete mit dem bevorzugten Paket-Manager Ihrer Verteilung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-114">We strongly recommend regularly updating your package catalog and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="3ac34-115">Für Debian/Ubuntu verwenden Sie apt:</span><span class="sxs-lookup"><span data-stu-id="3ac34-115">For Debian/Ubuntu, use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

<span data-ttu-id="3ac34-116">Windows führt für Ihre Linux-Verteilung(en) nicht automatisch eine Aktualisierung oder ein Upgrade aus.</span><span class="sxs-lookup"><span data-stu-id="3ac34-116">Windows does not automatically update or upgrade your Linux distribution(s).</span></span> <span data-ttu-id="3ac34-117">Dies ist eine Aufgabe, die die meisten Linux-Benutzer lieber selbst in die Hand nehmen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-117">This is a task that most Linux users prefer to control themselves.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="3ac34-118">Zurücksetzen Ihres Linux-Kennworts</span><span class="sxs-lookup"><span data-stu-id="3ac34-118">Reset your Linux password</span></span>

<span data-ttu-id="3ac34-119">Um Ihr Kennwort zu ändern, öffnen Sie Ihre Linux-Verteilung (z. B. Ubuntu), und geben Sie den Befehl `passwd` ein.</span><span class="sxs-lookup"><span data-stu-id="3ac34-119">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="3ac34-120">Sie werden aufgefordert, Ihr aktuelles Kennwort und Ihr neues Kennwort einzugeben und anschließend Ihr neues Kennwort zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-120">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

## <a name="forgot-your-password"></a><span data-ttu-id="3ac34-121">Haben Sie Ihr Kennwort vergessen?</span><span class="sxs-lookup"><span data-stu-id="3ac34-121">Forgot your password</span></span>

<span data-ttu-id="3ac34-122">Wenn Sie das Kennwort für Ihre Linux-Verteilung vergessen haben:</span><span class="sxs-lookup"><span data-stu-id="3ac34-122">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="3ac34-123">Öffnen Sie PowerShell, und geben Sie mit dem Befehl `wsl -u root` das Stammverzeichnis Ihrer Standard-WSL-Verteilung ein.</span><span class="sxs-lookup"><span data-stu-id="3ac34-123">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

    > <span data-ttu-id="3ac34-124">Wenn Sie das vergessene Kennwort für eine Verteilung aktualisieren müssen, die nicht Ihre Standardverteilung ist, verwenden Sie den Befehl `wsl -d Debian -u root`, wobei Sie `Debian` durch den Namen Ihrer Zielverteilung ersetzen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-124">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="3ac34-125">Sobald Ihre WSL-Verteilung auf der Root-Ebene innerhalb von PowerShell geöffnet wurde, können Sie den Befehl `passwd <WSLUsername>` verwenden, um Ihr Kennwort zu aktualisieren, wobei `<WSLUsername>` der Benutzername des Kontos in der Distribution ist, dessen Kennwort Sie vergessen haben.</span><span class="sxs-lookup"><span data-stu-id="3ac34-125">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd <WSLUsername>` where `<WSLUsername>` is the username of the account in the DISTRO whose password you've forgotten.</span></span>

3. <span data-ttu-id="3ac34-126">Sie werden aufgefordert, ein neues UNIX-Kennwort einzugeben und dieses Kennwort anschließend zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="3ac34-126">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="3ac34-127">Sobald Ihnen mitgeteilt wird, dass das Kennwort erfolgreich aktualisiert wurde, schließen Sie WSL in PowerShell mithilfe des Befehls `exit`.</span><span class="sxs-lookup"><span data-stu-id="3ac34-127">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="3ac34-128">Wenn Sie eine frühe Version des Windows-Betriebssystems ausführen, wie z. B. 1703 (Creators Update) oder 1709 (Fall Creators Update), finden Sie weitere Informationen in der [Dokumentation zur archivierten Version dieses Benutzerkontoupdates](./user-support-archived.md).</span><span class="sxs-lookup"><span data-stu-id="3ac34-128">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
