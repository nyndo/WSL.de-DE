---
title: Einstieg in die Einbindung eines Linux-Datenträgers in WSL 2 (Vorschau)
description: Erfahren Sie, wie Sie eine Datenträger Bereitlegung in WSL 2 einrichten und wie Sie darauf zugreifen können.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, Disk, ext4, File System, Mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 8053b817dab0639789401e2fcfb116f6f8e722a7
ms.sourcegitcommit: a949595f3947c733f0bcdc54b30ccda5ae61577c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "89671203"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a><span data-ttu-id="7b5e0-104">Einstieg in die Einbindung eines Linux-Datenträgers in WSL 2 (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="7b5e0-104">Get started mounting a linux disk in WSL 2 (preview)</span></span>

<span data-ttu-id="7b5e0-105">Wenn Sie auf ein Linux-Datenträgerformat zugreifen möchten, das von Windows nicht unterstützt wird, können Sie mit WSL 2 Ihren Datenträger einbinden und auf dessen Inhalte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-105">If you want to access a Linux disk format that isn't supported by Windows, you can use WSL 2 to mount your disk and access its content.</span></span>

<span data-ttu-id="7b5e0-106">In diesem Tutorial werden die Schritte beschrieben, mit denen der Datenträger und die Partition identifiziert werden, die an WSL2 angefügt werden sollen, und wie Sie darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-106">This tutorial will cover the steps to identify the disk and partition to attach to WSL2, how to mount them, and how to access them.</span></span>

> [!NOTE]
> <span data-ttu-id="7b5e0-107">Der Administrator Zugriff ist erforderlich, um einen Datenträger an WSL 2 anzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-107">Administrator access is required to attach a disk to WSL 2.</span></span>

## <a name="identify-the-disk"></a><span data-ttu-id="7b5e0-108">Identifizieren des Datenträgers</span><span class="sxs-lookup"><span data-stu-id="7b5e0-108">Identify the disk</span></span>

<span data-ttu-id="7b5e0-109">Führen Sie Folgendes aus, um die verfügbaren Datenträger in Windows aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-109">To list the available disks in Windows, run:</span></span>

```powershell
wmic diskdrive list brief
```

<span data-ttu-id="7b5e0-110">Die Datenträger Pfade sind unter den ' de viceid '-Spalten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-110">The disks paths are available under the 'DeviceID' columns.</span></span> <span data-ttu-id="7b5e0-111">Normalerweise im `\\.\PHYSICALDRIVE*` Format.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-111">Usually under the `\\.\PHYSICALDRIVE*` format.</span></span>

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a><span data-ttu-id="7b5e0-112">Auflisten und Auswählen der Partitionen zum Einbinden in WSL 2</span><span class="sxs-lookup"><span data-stu-id="7b5e0-112">List and select the partitions to mount in WSL 2</span></span>

<span data-ttu-id="7b5e0-113">Nachdem der Datenträger identifiziert wurde, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-113">Once the disk is identified, run:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="7b5e0-114">Dadurch wird der Datenträger in WSL 2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-114">This will make the disk available in WSL 2.</span></span>

<span data-ttu-id="7b5e0-115">Nach dem anfügen kann die Partition aufgelistet werden, indem Sie den folgenden Befehl in WSL 2 ausführen:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-115">Once attached, the partition can be listed by running the following command inside WSL 2:</span></span>

```powershell
lsblk
```

<span data-ttu-id="7b5e0-116">Dadurch werden die verfügbaren Blockgeräte und Ihre Partitionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-116">This will display the available block devices and their partitions.</span></span>

<span data-ttu-id="7b5e0-117">Innerhalb von Linux wird ein Blockgerät als bezeichnet  `/dev/<Device><Partition>` .</span><span class="sxs-lookup"><span data-stu-id="7b5e0-117">Inside Linux, a block device is identified as  `/dev/<Device><Partition>`.</span></span> <span data-ttu-id="7b5e0-118">Beispielsweise ist/dev/sdb3 die Partitionsnummer 3 des Datenträgers `sdb` .</span><span class="sxs-lookup"><span data-stu-id="7b5e0-118">For example, /dev/sdb3, is the partition number 3 of disk `sdb`.</span></span>

<span data-ttu-id="7b5e0-119">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-119">Example output:</span></span>

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a><span data-ttu-id="7b5e0-120">Identifizieren des Dateisystem Typs</span><span class="sxs-lookup"><span data-stu-id="7b5e0-120">Identifying the filesystem type</span></span>

<span data-ttu-id="7b5e0-121">Wenn Sie den Typ des Dateisystems eines Datenträgers oder einer Partition nicht kennen, können Sie diesen Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-121">If you don't know the type of filesystem of a disk or partition, you can use this command:</span></span>

```powershell
blkid <BlockDevice>
```

<span data-ttu-id="7b5e0-122">Dadurch wird der erkannte File System-Typ ausgegeben (im `TYPE="<Filesystem>"` Format).</span><span class="sxs-lookup"><span data-stu-id="7b5e0-122">This will output the detected filesystem type (under the `TYPE="<Filesystem>"` format).</span></span>

## <a name="mount-the-selected-partitions"></a><span data-ttu-id="7b5e0-123">Ausgewählte Partitionen einbinden</span><span class="sxs-lookup"><span data-stu-id="7b5e0-123">Mount the selected partitions</span></span>

<span data-ttu-id="7b5e0-124">Nachdem Sie die Partitionen identifiziert haben, die Sie einbinden möchten, führen Sie diesen Befehl für jede Partition aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-124">Once you have identified the partitions you want to mount, run this command on each partition:</span></span> 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> <span data-ttu-id="7b5e0-125">Wenn Sie den gesamten Datenträger als einzelnes Volume einbinden möchten (d. h., wenn der Datenträger nicht partitioniert ist), `--partition` kann weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-125">If you wish to mount the entire disk as a single volume (i.e. if the disk isn't partitioned), `--partition` can be omitted.</span></span>
> 
> <span data-ttu-id="7b5e0-126">Wenn keine Angabe erfolgt, ist der Standard dateidateityp "ext4".</span><span class="sxs-lookup"><span data-stu-id="7b5e0-126">If omitted, the default filesystem type is "ext4".</span></span>

## <a name="access-the-disk-content"></a><span data-ttu-id="7b5e0-127">Zugreifen auf den Datenträger Inhalt</span><span class="sxs-lookup"><span data-stu-id="7b5e0-127">Access the disk content</span></span>

<span data-ttu-id="7b5e0-128">Nach der Bereitstellung kann auf den Datenträger unter dem Pfad zugegriffen werden, auf den durch den Konfigurations Wert verwiesen wird: `automount.root` .</span><span class="sxs-lookup"><span data-stu-id="7b5e0-128">Once mounted, the disk can be accessed under the path pointed to by the config value: `automount.root`.</span></span> <span data-ttu-id="7b5e0-129">Standardwert: `/mnt/wsl`.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-129">The default value is `/mnt/wsl`.</span></span>

<span data-ttu-id="7b5e0-130">Aus Windows kann auf den Datenträger über den Datei-Explorer zugegriffen werden, indem Sie zu navigieren: `\\wsl$\\<Distro>\\<Mountpoint>` (beliebige Linux-Distribution auswählen).</span><span class="sxs-lookup"><span data-stu-id="7b5e0-130">From Windows, the disk can be accessed from File Explorer by navigating to: `\\wsl$\\<Distro>\\<Mountpoint>` (pick any Linux distribution).</span></span>

## <a name="unmount-the-disk"></a><span data-ttu-id="7b5e0-131">Aufheben der Bereitstellung des Datenträgers</span><span class="sxs-lookup"><span data-stu-id="7b5e0-131">Unmount the disk</span></span>

<span data-ttu-id="7b5e0-132">Wenn Sie die Bereitstellung des Datenträgers von WSL 2 entfernen und den Datenträger trennen möchten, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-132">If you want to unmount and detach the disk from WSL 2, run:</span></span>

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a><span data-ttu-id="7b5e0-133">Befehlszeilenreferenz</span><span class="sxs-lookup"><span data-stu-id="7b5e0-133">Command line reference</span></span>

### <a name="mouting-a-specific-filesystem"></a><span data-ttu-id="7b5e0-134">Mouting eines bestimmten Dateisystems</span><span class="sxs-lookup"><span data-stu-id="7b5e0-134">Mouting a specific filesystem</span></span>

<span data-ttu-id="7b5e0-135">Standardmäßig wird von WSL 2 versucht, das Gerät als ext4 zu einbinden.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-135">By default, WSL 2 will attempt to mount the device as ext4.</span></span> <span data-ttu-id="7b5e0-136">Führen Sie zum Angeben eines anderen Dateisystems Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-136">To specify another filesystem, run:</span></span>

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

<span data-ttu-id="7b5e0-137">Wenn Sie beispielsweise einen Datenträger als FAT einbinden möchten, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-137">For example, to mount a disk as fat, run:</span></span>

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> <span data-ttu-id="7b5e0-138">Führen Sie Folgendes aus, um die verfügbaren Dateisysteme in WSL2 aufzulisten: `cat /proc/filesystems`</span><span class="sxs-lookup"><span data-stu-id="7b5e0-138">To list the available filesystems in WSL2, run: `cat /proc/filesystems`</span></span>

### <a name="mouting-a-specific-partition"></a><span data-ttu-id="7b5e0-139">Mouting für eine bestimmte Partition</span><span class="sxs-lookup"><span data-stu-id="7b5e0-139">Mouting a specific partition</span></span>

<span data-ttu-id="7b5e0-140">Standardmäßig versucht WSL 2, den gesamten Datenträger einbinden.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-140">By default, WSL 2 attempts to mount the entire disk.</span></span> <span data-ttu-id="7b5e0-141">Führen Sie zum Einbinden einer bestimmten Partition Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-141">To mount a specific partition, run:</span></span>

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

<span data-ttu-id="7b5e0-142">Dies funktioniert nur, wenn es sich bei dem Datenträger um MBR (Master Boot Record) oder GPT (GUID-Partitionstabelle) handelt.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-142">This only works if the disk is either MBR (Master Boot Record) or GPT (GUID Partition Table).</span></span> <span data-ttu-id="7b5e0-143">[Informieren Sie sich über die Partitions Stile MBR und GPT](https://docs.microsoft.com/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span><span class="sxs-lookup"><span data-stu-id="7b5e0-143">[Read about partition styles - MBR and GPT](https://docs.microsoft.com/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span></span>

### <a name="specifying-mount-options"></a><span data-ttu-id="7b5e0-144">Angeben von Optionen</span><span class="sxs-lookup"><span data-stu-id="7b5e0-144">Specifying mount options</span></span>

<span data-ttu-id="7b5e0-145">Führen Sie zum Angeben der Einstellungsoptionen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-145">To specify mount options, run:</span></span>

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

<span data-ttu-id="7b5e0-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-146">Example:</span></span>

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> <span data-ttu-id="7b5e0-147">Zurzeit werden nur Dateisystem spezifische Optionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-147">Only filesystem specific options are supported at this time.</span></span> <span data-ttu-id="7b5e0-148">Generische Optionen wie `ro, rw, noatime, ...` werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-148">Generic options such as `ro, rw, noatime, ...` are not supported.</span></span>

### <a name="attaching-the-disk-without-mounting-it"></a><span data-ttu-id="7b5e0-149">Anfügen des Datenträgers ohne Einbindung</span><span class="sxs-lookup"><span data-stu-id="7b5e0-149">Attaching the disk without mounting it</span></span>

<span data-ttu-id="7b5e0-150">Wenn das Datenträger Schema von keiner der oben aufgeführten Optionen unterstützt wird, können Sie den Datenträger an WSL 2 anfügen, ohne ihn bereitzustellen, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-150">If the disk scheme isn't supported by any of the above options, you can attach the disk to WSL 2 without mounting it by running:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="7b5e0-151">Dadurch wird das Blockgerät in WSL 2 zur Verfügung gestellt, sodass es von dort aus manuell eingebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-151">This will make the block device available inside WSL 2 so it can be mounted manually from there.</span></span> <span data-ttu-id="7b5e0-152">Verwenden `lsblk` Sie, um die verfügbaren Blockgeräte in WSL 2 aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-152">Use `lsblk` to list the available block devices inside WSL 2.</span></span>

### <a name="detaching-a-disk"></a><span data-ttu-id="7b5e0-153">Trennen eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="7b5e0-153">Detaching a disk</span></span>

<span data-ttu-id="7b5e0-154">Führen Sie zum Trennen eines Datenträgers von WSL 2 Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="7b5e0-154">To detach a disk from WSL 2, run:</span></span>

```powershell
wsl --unmount [DiskPath]
```

<span data-ttu-id="7b5e0-155">Wenn `Diskpath` weggelassen wird, werden alle angefügten Datenträger nicht bereitgestellt und getrennt.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-155">If `Diskpath` is omitted, all attached disks are unmounted and detached.</span></span>

> [!NOTE]
> <span data-ttu-id="7b5e0-156">Wenn die Bereitstellung eines Datenträgers nicht rückgängig gemacht werden kann, kann WSL 2 durch Ausführen von erzwungen werden, wodurch der Datenträger getrennt `wsl --shutdown` wird.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-156">If one disk fails to unmount, WSL 2 can be forced to exit by running `wsl --shutdown`, which will detach the disk.</span></span>

## <a name="limitations"></a><span data-ttu-id="7b5e0-157">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7b5e0-157">Limitations</span></span>

- <span data-ttu-id="7b5e0-158">Zu diesem Zeitpunkt können nur ganze Datenträger an WSL 2 angefügt werden. Dies bedeutet, dass es nicht möglich ist, nur eine Partition anzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-158">At this time, only entire disks can be attached to WSL 2, meaning that it's not possible to attach only a partition.</span></span> <span data-ttu-id="7b5e0-159">Konkret bedeutet dies, dass es nicht möglich ist, `wsl --mount` eine Partition auf dem Startgerät zu lesen, da dieses Gerät nicht von Windows getrennt werden kann.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-159">Concretely, this means that it's not possible to use `wsl --mount` to read a partition on the boot device, because that device can't be detached from Windows.</span></span>

- <span data-ttu-id="7b5e0-160">USB-Flash Laufwerke werden zurzeit nicht unterstützt und können nicht an WSL 2 angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-160">USB flash drives are not supported at this time and will fail to attach to WSL 2.</span></span> <span data-ttu-id="7b5e0-161">USB-Datenträger werden jedoch unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7b5e0-161">USB disks are supported though.</span></span>

- <span data-ttu-id="7b5e0-162">Nur Dateisysteme, die im Kernel nativ unterstützt werden, können von bereitgestellt werden `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="7b5e0-162">Only filesystems that are natively supported in the kernel can be mounted by `wsl --mount`.</span></span> <span data-ttu-id="7b5e0-163">Dies bedeutet, dass es nicht möglich ist, installierte Dateisystem Treiber (z. b. NTFS-3G) zu verwenden, indem aufgerufen wird `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="7b5e0-163">This means that it's not possible to use installed filesystem drivers (such as ntfs-3g for example) by calling `wsl --mount`.</span></span>
