---
title: Initialisieren einer neuen WSL Linux-Verteilung
description: Nach dem Installieren einer Linux-Verteilung für WSL führen Sie die folgenden einfachen Schritte aus, um die Initialisierung abzuschließen.
keywords: BashOnWindows, bash, wsl, windows, windows subsystem for linux, windowssubsystem, ubuntu, debian, suse, windows 10
ms.date: 07/24/2018
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 11dc84d3a58b51241c7c63e8ca35eba94a12508b
ms.sourcegitcommit: b15b847b87d29a40de4a1517315949bce9c7a3d5
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "91413211"
---
# <a name="initializing-a-newly-installed-distribution"></a><span data-ttu-id="4ad07-104">Initialisieren einer neu installierten Verteilung</span><span class="sxs-lookup"><span data-stu-id="4ad07-104">Initializing a newly installed distribution</span></span>

<span data-ttu-id="4ad07-105">Nachdem Sie Ihre Verteilung heruntergeladen und installiert haben, müssen Sie die Initialisierung der neuen Verteilung abschließen:</span><span class="sxs-lookup"><span data-stu-id="4ad07-105">Once your distribution has been downloaded and installed, you'll need to complete initialization of the new distribution:</span></span>

## <a name="launch-a-distribution"></a><span data-ttu-id="4ad07-106">Starten einer Verteilung</span><span class="sxs-lookup"><span data-stu-id="4ad07-106">Launch a distribution</span></span>

<span data-ttu-id="4ad07-107">Um die Initialisierung der neu installierten Verteilung abzuschließen, starten Sie eine neue Instanz.</span><span class="sxs-lookup"><span data-stu-id="4ad07-107">To complete the initialization of your newly installed distribution, launch a new instance.</span></span> <span data-ttu-id="4ad07-108">Klicken Sie hierzu in der Microsoft Store-App auf die Schaltfläche „Starten“, oder starten Sie die Verteilung über das Startmenü:</span><span class="sxs-lookup"><span data-stu-id="4ad07-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distribution from the Start menu:</span></span>

> <span data-ttu-id="4ad07-109">Tipp: Möglicherweise möchten Sie Ihre am häufigsten verwendeten Verteilungen an das Startmenü und/oder an die Taskleiste anheften.</span><span class="sxs-lookup"><span data-stu-id="4ad07-109">Tip: You might want to pin your most frequently used distributions to your Start menu, and/or to your taskbar!</span></span>

![Starten von Verteilungen über das Startmenü](media/start-menu.png)

> <span data-ttu-id="4ad07-111">Unter Windows Server können Sie die ausführbare Startprogrammdatei `<distribution>.exe` Ihrer Verteilung über dem Verteilungsinstallationsordner starten.</span><span class="sxs-lookup"><span data-stu-id="4ad07-111">On Windows Server, you can launch your distribution's launcher executable `<distribution>.exe` from the distribution installation folder.</span></span>

<span data-ttu-id="4ad07-112">Wenn eine neu installierte Verteilung zum ersten Mal ausgeführt wird, wird ein Konsolenfenster geöffnet, und Sie werden aufgefordert, bis zum Abschluss der Installation wenige Minuten zu warten.</span><span class="sxs-lookup"><span data-stu-id="4ad07-112">The first time a newly installed distribution runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="4ad07-113">In dieser letzten Phase der Installation werden die Dateien der Verteilung dekomprimiert und auf Ihrem PC gespeichert. Sie sind dann einsatzbereit.</span><span class="sxs-lookup"><span data-stu-id="4ad07-113">During this final stage of installation, the distribution's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="4ad07-114">Dies kann je nach Leistung der Speichergeräte Ihres PCs etwa eine Minute oder ggf. auch länger dauern.</span><span class="sxs-lookup"><span data-stu-id="4ad07-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="4ad07-115">Diese erste Installationsphase ist nur erforderlich, wenn eine „saubere“ Verteilung installiert wird. Alle zukünftigen Starts sollten weniger als eine Sekunde in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="4ad07-115">This initial installation phase is only required when a distribution is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="4ad07-116">Einrichten eines neuen Linux-Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="4ad07-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="4ad07-117">Nach Abschluss der Installation werden Sie aufgefordert, ein neues Benutzerkonto (und das zugehörige Kennwort) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4ad07-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span>

![Entpacken von Ubuntu in der Windows-Konsole](media/UbuntuInstall.png)

<span data-ttu-id="4ad07-119">Dieses Benutzerkonto gilt für den normalen Benutzer ohne Administratorrechte, als der Sie beim Starten einer Verteilung standardmäßig angemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="4ad07-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distribution.</span></span>

> <span data-ttu-id="4ad07-120">Sie können einen beliebigen Benutzernamen und ein gewünschtes Kennwort auswählen. Beides hat keinen Einfluss auf Ihren Windows-Benutzernamen.</span><span class="sxs-lookup"><span data-stu-id="4ad07-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span>

<span data-ttu-id="4ad07-121">Wenn Sie eine neue Verteilungsinstanz öffnen, werden Sie nicht zur Eingabe Ihres Kennworts aufgefordert. Wenn Sie jedoch **einen Prozess mit `sudo` heraufstufen, müssen Sie Ihr Kennwort eingeben**. Stellen Sie also sicher, dass Sie ein Kennwort auswählen, das Sie sich leicht merken können.</span><span class="sxs-lookup"><span data-stu-id="4ad07-121">When you open a new distribution instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="4ad07-122">Weitere Informationen finden Sie auf der Seite [Benutzersupport](user-support.md).</span><span class="sxs-lookup"><span data-stu-id="4ad07-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distributions-packages"></a><span data-ttu-id="4ad07-123">Aktualisieren und Upgraden der Pakete Ihrer Verteilung</span><span class="sxs-lookup"><span data-stu-id="4ad07-123">Update & upgrade your distribution's packages</span></span>

<span data-ttu-id="4ad07-124">Die meisten Verteilungen werden mit einem leeren/minimalen Paketkatalog ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="4ad07-124">Most distributions ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="4ad07-125">Es wird dringend empfohlen, den Paketkatalog regelmäßig zu aktualisieren und ein Upgrade der installierten Pakete mit dem bevorzugten Paket-Manager Ihrer Verteilung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4ad07-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distribution's preferred package manager.</span></span> <span data-ttu-id="4ad07-126">Unter Debian/Ubuntu verwenden Sie apt:</span><span class="sxs-lookup"><span data-stu-id="4ad07-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="4ad07-127">Windows führt für Ihre Linux-Verteilung(en) nicht automatisch eine Aktualisierung oder ein Upgrade aus: Linux-Benutzer ziehen es vor, diese Aufgabe selbst zu steuern.</span><span class="sxs-lookup"><span data-stu-id="4ad07-127">Windows does not automatically update or upgrade your Linux distribution(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="4ad07-128">Fertig!</span><span class="sxs-lookup"><span data-stu-id="4ad07-128">You're done!</span></span> <span data-ttu-id="4ad07-129">Viel Spaß bei der Verwendung Ihrer neuen Linux-Verteilung unter WSL!</span><span class="sxs-lookup"><span data-stu-id="4ad07-129">Enjoy using your new Linux distribution on WSL!</span></span> <span data-ttu-id="4ad07-130">Weitere Informationen zu WSL finden Sie in der weiteren [WSL-Dokumentation](./index.md) oder auf der [Seite mit den WSL-Lernressourcen](https://aka.ms/learnwsl).</span><span class="sxs-lookup"><span data-stu-id="4ad07-130">To learn more about WSL, review the other [WSL docs](./index.md), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![Viel Spaß bei der Verwendung von Linux unter WSL!](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="4ad07-132">Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="4ad07-132">Troubleshooting</span></span>

<span data-ttu-id="4ad07-133">Nachfolgend werden einige Fehler und vorgeschlagene Korrekturen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ad07-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="4ad07-134">Weitere allgemeine Fehler und zugehörige Lösungen finden Sie auf der [Seite für die WSL-Problembehandlung](troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="4ad07-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="4ad07-135">**Fehler bei der Installation: 0x8007007e**: Dieser Fehler tritt auf, wenn das System Linux aus dem Store nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4ad07-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="4ad07-136">Stellen Sie Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="4ad07-136">Make sure that:</span></span>
> * <span data-ttu-id="4ad07-137">Sie führen Windows-Build 16215 oder höher aus.</span><span class="sxs-lookup"><span data-stu-id="4ad07-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="4ad07-138">[Überprüfen Sie Ihren Build](troubleshooting.md#check-your-build-number).</span><span class="sxs-lookup"><span data-stu-id="4ad07-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="4ad07-139">Die optionale Komponente des Windows-Subsystems für Linux ist aktiviert, und der Computer wurde neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="4ad07-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="4ad07-140">[Stellen Sie sicher, dass WSL aktiviert ist](troubleshooting.md#confirm-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="4ad07-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>