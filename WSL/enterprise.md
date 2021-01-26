---
title: WSL für Unternehmen
description: Ressourcen und Anweisungen zur optimalen Verwendung des WSL für Linux in einer Unternehmensumgebung.
keywords: BashOnWindows, Bash, WSL, Windows, Windows-Subsystem für Linux, Windows-Subsystem, Ubuntu, Debian, Suse, Windows 10, Unternehmen, Bereitstellung, offline, Paket, Store, Verteilung, Installation, installieren
ms.date: 12/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a210268fb460a793fec2047c6d6678f92869ea16
ms.sourcegitcommit: 0523e6a2ca99f5f3b188d526afed3ce6ad7e3abb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/25/2021
ms.locfileid: "98766856"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="aa2f6-104">Windows-Subsystem für Linux für Unternehmen</span><span class="sxs-lookup"><span data-stu-id="aa2f6-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="aa2f6-105">Als Administrator oder Manager können Sie verlangen, dass alle Entwickler die gleiche genehmigte Software verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-105">As an administrator or manager, you may require all developers to use the same approved software.</span></span> <span data-ttu-id="aa2f6-106">Diese Konsistenz hilft beim Erstellen einer gut definierten Arbeitsumgebung.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-106">This consistency helps to create a well-defined work environment.</span></span> <span data-ttu-id="aa2f6-107">Das Windows-Subsystem für Linux trägt zu dieser Konsistenz bei, indem es Ihnen ermöglicht, benutzerdefinierte WSL-Images von einem Computer zum nächsten zu importieren und zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-107">The Windows Subsystem for Linux aids in this consistency by allowing you to import and export custom WSL images from one machine to the next.</span></span> <span data-ttu-id="aa2f6-108">Lesen Sie den folgenden Leitfaden, um mehr darüber zu erfahren:</span><span class="sxs-lookup"><span data-stu-id="aa2f6-108">Read the guide below to learn more about:</span></span>

* [<span data-ttu-id="aa2f6-109">Erstellen eines benutzerdefinierten WSL-Images</span><span class="sxs-lookup"><span data-stu-id="aa2f6-109">Creating a custom WSL image</span></span>](#creating-a-custom-wsl-image)
* [<span data-ttu-id="aa2f6-110">Verteilen eines WSL-Images</span><span class="sxs-lookup"><span data-stu-id="aa2f6-110">Distributing a WSL image</span></span>](#distributing-your-wsl-image)
* [<span data-ttu-id="aa2f6-111">Aktualisieren und Patchen von Linux-Verteilungen und -Paketen</span><span class="sxs-lookup"><span data-stu-id="aa2f6-111">Update and patch Linux distributions and packages</span></span>](#update-and-patch-linux-distributions-and-packages)
* [<span data-ttu-id="aa2f6-112">Optionen für Sicherheit und Kontrolle im Unternehmen</span><span class="sxs-lookup"><span data-stu-id="aa2f6-112">Enterprise security and control options</span></span>](#enterprise-security-and-control-options)

## <a name="creating-a-custom-wsl-image"></a><span data-ttu-id="aa2f6-113">Erstellen eines benutzerdefinierten WSL-Images</span><span class="sxs-lookup"><span data-stu-id="aa2f6-113">Creating a custom WSL image</span></span>

<span data-ttu-id="aa2f6-114">Was gemeinhin als „Image“ bezeichnet wird, ist einfach eine in einer Datei gespeicherte Momentaufnahme Ihrer Software und deren Komponenten.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-114">What is commonly referred to as an "image", is simply a snapshot of your software and its components saved to a file.</span></span> <span data-ttu-id="aa2f6-115">Im Fall des Windows-Subsystems für Linux würde Ihr Image aus dem Subsystem, seinen Verteilungen sowie der in den Verteilungen installierten Software und den Paketen bestehen.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-115">In the case of the Windows Subsystem for Linux, your image would consist of the subsystem, its distributions, and whatever software and packages are installed on the distribution.</span></span>

<span data-ttu-id="aa2f6-116">Um mit der Erstellung Ihres WSL-Images zu beginnen, müssen Sie zunächst [das Windows-Subsystem für Linux installieren](./install-win10.md).</span><span class="sxs-lookup"><span data-stu-id="aa2f6-116">To begin creating your WSL image, first [install the Windows Subsystem for Linux](./install-win10.md).</span></span>

<span data-ttu-id="aa2f6-117">Nach der Installation können Sie über den Microsoft Store für Unternehmen die für Sie passende Linux-Verteilung herunterladen und installieren.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-117">Once installed, use The Microsoft Store for Business to download and install the Linux distribution that’s right for you.</span></span> <span data-ttu-id="aa2f6-118">Erstellen eines Kontos über den [Microsoft Store für Unternehmen](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business.)</span><span class="sxs-lookup"><span data-stu-id="aa2f6-118">Create an account with the [Microsoft Store for Business](https://docs.microsoft.com/microsoft-store/sign-up-microsoft-store-for-business.)</span></span>

### <a name="exporting-your-wsl-image"></a><span data-ttu-id="aa2f6-119">Exportieren Ihres WSL-Images</span><span class="sxs-lookup"><span data-stu-id="aa2f6-119">Exporting your WSL image</span></span>

<span data-ttu-id="aa2f6-120">Exportieren Sie Ihr benutzerdefiniertes WSL-Image, indem Sie „wsl --export `<Distro> <FileName>`“ ausführen, wodurch das Image in eine TAR-Datei gepackt und für die Verteilung auf anderen Computern vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-120">Export your custom WSL image by running wsl --export `<Distro> <FileName>`, which will wrap your image in a tar file and make it ready for distribution on to other machines.</span></span>

## <a name="distributing-your-wsl-image"></a><span data-ttu-id="aa2f6-121">Verteilen Ihres WSL-Images</span><span class="sxs-lookup"><span data-stu-id="aa2f6-121">Distributing your WSL image</span></span>

<span data-ttu-id="aa2f6-122">Verteilen Sie das WSL-Image von einer Freigabe oder einem Speichergerät aus, indem Sie „wsl --import `<Distro> <InstallLocation> <FileName>`“ ausführen, wodurch die angegebene TAR-Datei als neue Verteilung importiert wird.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-122">Distribute the WSL image from a share or storage device by running wsl --import `<Distro> <InstallLocation> <FileName>`, which will import the specified tar file as a new distribution.</span></span>

## <a name="update-and-patch-linux-distributions-and-packages"></a><span data-ttu-id="aa2f6-123">Aktualisieren und Patchen von Linux-Verteilungen und -Paketen</span><span class="sxs-lookup"><span data-stu-id="aa2f6-123">Update and patch Linux distributions and packages</span></span>

<span data-ttu-id="aa2f6-124">Die Verwendung von Linux-Konfigurations-Manager-Tools wird dringend empfohlen, um Linux-Benutzerspeicher zu überwachen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-124">Using Linux configuration manager tools is strongly recommended for monitoring and managing Linux user space.</span></span> <span data-ttu-id="aa2f6-125">Es gibt eine Vielzahl von Linux-Konfigurations-Managern, aus denen Sie auswählen können.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-125">There are a host of Linux configuration managers to choose from.</span></span> <span data-ttu-id="aa2f6-126">Schauen Sie sich diesen [Blogbeitrag](http://www.craigloewen.com/blog/2019/12/04/running-puppet-quickly-in-wsl2/) über das Installieren von Puppet in WSL 2 an.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-126">Check out this [blog post](http://www.craigloewen.com/blog/2019/12/04/running-puppet-quickly-in-wsl2/) on how to install Puppet in WSL 2.</span></span>

## <a name="enterprise-security-and-control-options"></a><span data-ttu-id="aa2f6-127">Optionen für Sicherheit und Kontrolle im Unternehmen</span><span class="sxs-lookup"><span data-stu-id="aa2f6-127">Enterprise security and control options</span></span>

<span data-ttu-id="aa2f6-128">Derzeit bietet lässt die Benutzererfahrung in einem Unternehmensszenario nur eingeschränkt durch WSL ändern.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-128">Currently, WSL offers limited control mechanisms in regard to modifying the user experience in an Enterprise scenario.</span></span> <span data-ttu-id="aa2f6-129">Die Unternehmensfeatures werden jedoch ständig weiterentwickelt. Nachfolgend sind die Bereiche der unterstützten und nicht unterstützten Features aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-129">Enterprise features continue in development however, below are the areas of supported and unsupported features.</span></span> <span data-ttu-id="aa2f6-130">Wenn Sie ein neues Feature anfordern möchten, das nicht in dieser Liste enthalten ist, melden Sie ein Problem in unserem [GitHub-Repository](https://github.com/microsoft/WSL/issues?q=is%3Aissue+is%3Aopen+enterprise).</span><span class="sxs-lookup"><span data-stu-id="aa2f6-130">To request a new feature not covered in this list, file an issue in our [GitHub repo](https://github.com/microsoft/WSL/issues?q=is%3Aissue+is%3Aopen+enterprise).</span></span>

### <a name="supported"></a><span data-ttu-id="aa2f6-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa2f6-131">Supported</span></span>

* <span data-ttu-id="aa2f6-132">Internes Freigeben eines genehmigten Images mithilfe von `wsl --import` und `wsl --export`</span><span class="sxs-lookup"><span data-stu-id="aa2f6-132">Sharing an approved image internally using `wsl --import` and `wsl --export`</span></span>
* <span data-ttu-id="aa2f6-133">Erstellen einer eigenen WSL-Verteilung für Ihr Unternehmen mit dem [WSL Distro Launcher-Repository](https://github.com/microsoft/WSL-DistroLauncher)</span><span class="sxs-lookup"><span data-stu-id="aa2f6-133">Creating your own WSL distro for your Enterprise using the [WSL Distro Launcher repo](https://github.com/microsoft/WSL-DistroLauncher)</span></span>

<span data-ttu-id="aa2f6-134">Hier ist eine Liste von Features, für die noch keine Unterstützung besteht, die aber untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="aa2f6-134">Here's a list of features for which we don't yet have support for, but are investigating.</span></span>

### <a name="unsupported"></a><span data-ttu-id="aa2f6-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="aa2f6-135">Unsupported</span></span>

* <span data-ttu-id="aa2f6-136">Synchronisieren des Benutzers innerhalb von WSL mit dem Windows-Benutzer auf dem Hostcomputer</span><span class="sxs-lookup"><span data-stu-id="aa2f6-136">Synchronizing the user inside WSL with the Windows user on the host machine</span></span>
* <span data-ttu-id="aa2f6-137">Verwalten von Updates und Patchen der Linux-Verteilungen und -Pakete mit Windows-Tools</span><span class="sxs-lookup"><span data-stu-id="aa2f6-137">Managing updates and patching of the Linux distributions and packages using Windows tools</span></span>
* <span data-ttu-id="aa2f6-138">Verwenden von Windows Update auch für Inhalte von WSL-Verteilungen</span><span class="sxs-lookup"><span data-stu-id="aa2f6-138">Having Windows update also update WSL distro contents</span></span>
* <span data-ttu-id="aa2f6-139">Steuern, auf welche Verteilungen Benutzer in Ihrem Unternehmen zugreifen können</span><span class="sxs-lookup"><span data-stu-id="aa2f6-139">Controlling which distributions users in your Enterprise can access</span></span>
* <span data-ttu-id="aa2f6-140">Ausführen obligatorischer Dienste (Protokollierung oder Überwachung) in WSL</span><span class="sxs-lookup"><span data-stu-id="aa2f6-140">Running mandatory services (logging or monitoring) inside of WSL</span></span>
* <span data-ttu-id="aa2f6-141">Überwachen von Linux-Instanzen mit Windows-Konfigurations-Manager-Tools wie SCCM oder Intune</span><span class="sxs-lookup"><span data-stu-id="aa2f6-141">Monitoring Linux instances using Windows configuration manager tools such as SCCM or Intune</span></span>
* <span data-ttu-id="aa2f6-142">McAfee-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="aa2f6-142">McAfee support</span></span>
