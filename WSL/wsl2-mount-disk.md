---
title: Einstieg in die Einbindung eines Linux-Datenträgers in WSL 2 (Vorschau)
description: Erfahren Sie, wie Sie eine Datenträger Bereitlegung in WSL 2 einrichten und wie Sie darauf zugreifen können.
keywords: WSL, Windows, windowssubsystem, GNU, Linux, bash, Disk, ext4, File System, Mount
ms.date: 06/08/2020
ms.topic: article
ms.localizationpriority: medium
ms.openlocfilehash: 9ee71d7f76a9fd0e6b20293ef30b0808d56c43a1
ms.sourcegitcommit: cfb6c254322b8eb9c2c26e19ce970d4c046bc352
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2020
ms.locfileid: "93035726"
---
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a><span data-ttu-id="24865-104">Einstieg in die Einbindung eines Linux-Datenträgers in WSL 2 (Vorschau)</span><span class="sxs-lookup"><span data-stu-id="24865-104">Get started mounting a Linux disk in WSL 2 (preview)</span></span>

<span data-ttu-id="24865-105">Wenn Sie auf ein Linux-Datenträgerformat zugreifen möchten, das von Windows nicht unterstützt wird, können Sie mit WSL 2 Ihren Datenträger einbinden und auf dessen Inhalte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="24865-105">If you want to access a Linux disk format that isn't supported by Windows, you can use WSL 2 to mount your disk and access its content.</span></span>

<span data-ttu-id="24865-106">In diesem Tutorial werden die Schritte beschrieben, mit denen der Datenträger und die Partition identifiziert werden, die an WSL2 angefügt werden sollen, und wie Sie darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="24865-106">This tutorial will cover the steps to identify the disk and partition to attach to WSL2, how to mount them, and how to access them.</span></span>

> [!NOTE]
> <span data-ttu-id="24865-107">Für den Zugriff auf dieses Feature müssen Sie unter Windows 10 Build 20211 oder höher sein.</span><span class="sxs-lookup"><span data-stu-id="24865-107">You will need to be on Windows 10 Build 20211 or higher to access this feature.</span></span> <span data-ttu-id="24865-108">Sie können das [Windows Insider-Programm](https://insider.windows.com/) beitreten, um die neuesten Vorschau Versionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="24865-108">You can join the [Windows Insiders Program](https://insider.windows.com/) to get the latest preview builds.</span></span>
> <span data-ttu-id="24865-109">Der Administrator Zugriff ist erforderlich, um einen Datenträger an WSL 2 anzufügen.</span><span class="sxs-lookup"><span data-stu-id="24865-109">Administrator access is required to attach a disk to WSL 2.</span></span>

## <a name="identify-the-disk"></a><span data-ttu-id="24865-110">Identifizieren des Datenträgers</span><span class="sxs-lookup"><span data-stu-id="24865-110">Identify the disk</span></span>

<span data-ttu-id="24865-111">Führen Sie Folgendes aus, um die verfügbaren Datenträger in Windows aufzulisten:</span><span class="sxs-lookup"><span data-stu-id="24865-111">To list the available disks in Windows, run:</span></span>

```powershell
wmic diskdrive list brief
```

<span data-ttu-id="24865-112">Die Datenträger Pfade sind unter den ' de viceid '-Spalten verfügbar.</span><span class="sxs-lookup"><span data-stu-id="24865-112">The disks paths are available under the 'DeviceID' columns.</span></span> <span data-ttu-id="24865-113">Normalerweise im `\\.\PHYSICALDRIVE*` Format.</span><span class="sxs-lookup"><span data-stu-id="24865-113">Usually under the `\\.\PHYSICALDRIVE*` format.</span></span>

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a><span data-ttu-id="24865-114">Auflisten und Auswählen der Partitionen zum Einbinden in WSL 2</span><span class="sxs-lookup"><span data-stu-id="24865-114">List and select the partitions to mount in WSL 2</span></span>

<span data-ttu-id="24865-115">Nachdem der Datenträger identifiziert wurde, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-115">Once the disk is identified, run:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="24865-116">Dadurch wird der Datenträger in WSL 2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="24865-116">This will make the disk available in WSL 2.</span></span>

<span data-ttu-id="24865-117">Nach dem anfügen kann die Partition aufgelistet werden, indem Sie den folgenden Befehl in WSL 2 ausführen:</span><span class="sxs-lookup"><span data-stu-id="24865-117">Once attached, the partition can be listed by running the following command inside WSL 2:</span></span>

```powershell
lsblk
```

<span data-ttu-id="24865-118">Dadurch werden die verfügbaren Blockgeräte und Ihre Partitionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24865-118">This will display the available block devices and their partitions.</span></span>

<span data-ttu-id="24865-119">Innerhalb von Linux wird ein Blockgerät als bezeichnet  `/dev/<Device><Partition>` .</span><span class="sxs-lookup"><span data-stu-id="24865-119">Inside Linux, a block device is identified as  `/dev/<Device><Partition>`.</span></span> <span data-ttu-id="24865-120">Beispielsweise ist/dev/sdb3 die Partitionsnummer 3 des Datenträgers `sdb` .</span><span class="sxs-lookup"><span data-stu-id="24865-120">For example, /dev/sdb3, is the partition number 3 of disk `sdb`.</span></span>

<span data-ttu-id="24865-121">Beispielausgabe:</span><span class="sxs-lookup"><span data-stu-id="24865-121">Example output:</span></span>

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a><span data-ttu-id="24865-122">Identifizieren des Dateisystem Typs</span><span class="sxs-lookup"><span data-stu-id="24865-122">Identifying the filesystem type</span></span>

<span data-ttu-id="24865-123">Wenn Sie den Typ des Dateisystems eines Datenträgers oder einer Partition nicht kennen, können Sie diesen Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="24865-123">If you don't know the type of filesystem of a disk or partition, you can use this command:</span></span>

```powershell
blkid <BlockDevice>
```

<span data-ttu-id="24865-124">Dadurch wird der erkannte File System-Typ ausgegeben (im `TYPE="<Filesystem>"` Format).</span><span class="sxs-lookup"><span data-stu-id="24865-124">This will output the detected filesystem type (under the `TYPE="<Filesystem>"` format).</span></span>

## <a name="mount-the-selected-partitions"></a><span data-ttu-id="24865-125">Ausgewählte Partitionen einbinden</span><span class="sxs-lookup"><span data-stu-id="24865-125">Mount the selected partitions</span></span>

<span data-ttu-id="24865-126">Nachdem Sie die Partitionen identifiziert haben, die Sie einbinden möchten, führen Sie diesen Befehl für jede Partition aus:</span><span class="sxs-lookup"><span data-stu-id="24865-126">Once you have identified the partitions you want to mount, run this command on each partition:</span></span> 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> <span data-ttu-id="24865-127">Wenn Sie den gesamten Datenträger als einzelnes Volume einbinden möchten (d. h., wenn der Datenträger nicht partitioniert ist), `--partition` kann weggelassen werden.</span><span class="sxs-lookup"><span data-stu-id="24865-127">If you wish to mount the entire disk as a single volume (i.e. if the disk isn't partitioned), `--partition` can be omitted.</span></span>
> 
> <span data-ttu-id="24865-128">Wenn keine Angabe erfolgt, ist der Standard dateidateityp "ext4".</span><span class="sxs-lookup"><span data-stu-id="24865-128">If omitted, the default filesystem type is "ext4".</span></span>

## <a name="access-the-disk-content"></a><span data-ttu-id="24865-129">Zugreifen auf den Datenträger Inhalt</span><span class="sxs-lookup"><span data-stu-id="24865-129">Access the disk content</span></span>

<span data-ttu-id="24865-130">Nach der Bereitstellung kann auf den Datenträger unter dem Pfad zugegriffen werden, auf den durch den Konfigurations Wert verwiesen wird: `automount.root` .</span><span class="sxs-lookup"><span data-stu-id="24865-130">Once mounted, the disk can be accessed under the path pointed to by the config value: `automount.root`.</span></span> <span data-ttu-id="24865-131">Standardwert: `/mnt/wsl`.</span><span class="sxs-lookup"><span data-stu-id="24865-131">The default value is `/mnt/wsl`.</span></span>

<span data-ttu-id="24865-132">Aus Windows kann auf den Datenträger über den Datei-Explorer zugegriffen werden, indem Sie zu navigieren: `\\wsl$\\<Distro>\\<Mountpoint>` (beliebige Linux-Distribution auswählen).</span><span class="sxs-lookup"><span data-stu-id="24865-132">From Windows, the disk can be accessed from File Explorer by navigating to: `\\wsl$\\<Distro>\\<Mountpoint>` (pick any Linux distribution).</span></span>

## <a name="unmount-the-disk"></a><span data-ttu-id="24865-133">Aufheben der Bereitstellung des Datenträgers</span><span class="sxs-lookup"><span data-stu-id="24865-133">Unmount the disk</span></span>

<span data-ttu-id="24865-134">Wenn Sie die Bereitstellung des Datenträgers von WSL 2 entfernen und den Datenträger trennen möchten, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-134">If you want to unmount and detach the disk from WSL 2, run:</span></span>

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a><span data-ttu-id="24865-135">Befehlszeilenreferenz</span><span class="sxs-lookup"><span data-stu-id="24865-135">Command line reference</span></span>

### <a name="mouting-a-specific-filesystem"></a><span data-ttu-id="24865-136">Mouting eines bestimmten Dateisystems</span><span class="sxs-lookup"><span data-stu-id="24865-136">Mouting a specific filesystem</span></span>

<span data-ttu-id="24865-137">Standardmäßig wird von WSL 2 versucht, das Gerät als ext4 zu einbinden.</span><span class="sxs-lookup"><span data-stu-id="24865-137">By default, WSL 2 will attempt to mount the device as ext4.</span></span> <span data-ttu-id="24865-138">Führen Sie zum Angeben eines anderen Dateisystems Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-138">To specify another filesystem, run:</span></span>

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

<span data-ttu-id="24865-139">Wenn Sie beispielsweise einen Datenträger als FAT einbinden möchten, führen Sie Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-139">For example, to mount a disk as fat, run:</span></span>

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> <span data-ttu-id="24865-140">Führen Sie Folgendes aus, um die verfügbaren Dateisysteme in WSL2 aufzulisten: `cat /proc/filesystems`</span><span class="sxs-lookup"><span data-stu-id="24865-140">To list the available filesystems in WSL2, run: `cat /proc/filesystems`</span></span>

### <a name="mouting-a-specific-partition"></a><span data-ttu-id="24865-141">Mouting für eine bestimmte Partition</span><span class="sxs-lookup"><span data-stu-id="24865-141">Mouting a specific partition</span></span>

<span data-ttu-id="24865-142">Standardmäßig versucht WSL 2, den gesamten Datenträger einbinden.</span><span class="sxs-lookup"><span data-stu-id="24865-142">By default, WSL 2 attempts to mount the entire disk.</span></span> <span data-ttu-id="24865-143">Führen Sie zum Einbinden einer bestimmten Partition Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-143">To mount a specific partition, run:</span></span>

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

<span data-ttu-id="24865-144">Dies funktioniert nur, wenn es sich bei dem Datenträger um MBR (Master Boot Record) oder GPT (GUID-Partitionstabelle) handelt.</span><span class="sxs-lookup"><span data-stu-id="24865-144">This only works if the disk is either MBR (Master Boot Record) or GPT (GUID Partition Table).</span></span> <span data-ttu-id="24865-145">[Informieren Sie sich über die Partitions Stile MBR und GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span><span class="sxs-lookup"><span data-stu-id="24865-145">[Read about partition styles - MBR and GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).</span></span>

### <a name="specifying-mount-options"></a><span data-ttu-id="24865-146">Angeben von Optionen</span><span class="sxs-lookup"><span data-stu-id="24865-146">Specifying mount options</span></span>

<span data-ttu-id="24865-147">Führen Sie zum Angeben der Einstellungsoptionen Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-147">To specify mount options, run:</span></span>

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

<span data-ttu-id="24865-148">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="24865-148">Example:</span></span>

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> <span data-ttu-id="24865-149">Zurzeit werden nur Dateisystem spezifische Optionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24865-149">Only filesystem specific options are supported at this time.</span></span> <span data-ttu-id="24865-150">Generische Optionen wie `ro, rw, noatime, ...` werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24865-150">Generic options such as `ro, rw, noatime, ...` are not supported.</span></span>

### <a name="attaching-the-disk-without-mounting-it"></a><span data-ttu-id="24865-151">Anfügen des Datenträgers ohne Einbindung</span><span class="sxs-lookup"><span data-stu-id="24865-151">Attaching the disk without mounting it</span></span>

<span data-ttu-id="24865-152">Wenn das Datenträger Schema von keiner der oben aufgeführten Optionen unterstützt wird, können Sie den Datenträger an WSL 2 anfügen, ohne ihn bereitzustellen, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="24865-152">If the disk scheme isn't supported by any of the above options, you can attach the disk to WSL 2 without mounting it by running:</span></span>

```powershell
wsl --mount <DiskPath> --bare
```

<span data-ttu-id="24865-153">Dadurch wird das Blockgerät in WSL 2 zur Verfügung gestellt, sodass es von dort aus manuell eingebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="24865-153">This will make the block device available inside WSL 2 so it can be mounted manually from there.</span></span> <span data-ttu-id="24865-154">Verwenden `lsblk` Sie, um die verfügbaren Blockgeräte in WSL 2 aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="24865-154">Use `lsblk` to list the available block devices inside WSL 2.</span></span>

### <a name="detaching-a-disk"></a><span data-ttu-id="24865-155">Trennen eines Datenträgers</span><span class="sxs-lookup"><span data-stu-id="24865-155">Detaching a disk</span></span>

<span data-ttu-id="24865-156">Führen Sie zum Trennen eines Datenträgers von WSL 2 Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="24865-156">To detach a disk from WSL 2, run:</span></span>

```powershell
wsl --unmount [DiskPath]
```

<span data-ttu-id="24865-157">Wenn `Diskpath` weggelassen wird, werden alle angefügten Datenträger nicht bereitgestellt und getrennt.</span><span class="sxs-lookup"><span data-stu-id="24865-157">If `Diskpath` is omitted, all attached disks are unmounted and detached.</span></span>

> [!NOTE]
> <span data-ttu-id="24865-158">Wenn die Bereitstellung eines Datenträgers nicht rückgängig gemacht werden kann, kann WSL 2 durch Ausführen von erzwungen werden, wodurch der Datenträger getrennt `wsl --shutdown` wird.</span><span class="sxs-lookup"><span data-stu-id="24865-158">If one disk fails to unmount, WSL 2 can be forced to exit by running `wsl --shutdown`, which will detach the disk.</span></span>

## <a name="limitations"></a><span data-ttu-id="24865-159">Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="24865-159">Limitations</span></span>

- <span data-ttu-id="24865-160">Zu diesem Zeitpunkt können nur ganze Datenträger an WSL 2 angefügt werden. Dies bedeutet, dass es nicht möglich ist, nur eine Partition anzufügen.</span><span class="sxs-lookup"><span data-stu-id="24865-160">At this time, only entire disks can be attached to WSL 2, meaning that it's not possible to attach only a partition.</span></span> <span data-ttu-id="24865-161">Konkret bedeutet dies, dass es nicht möglich ist, `wsl --mount` eine Partition auf dem Startgerät zu lesen, da dieses Gerät nicht von Windows getrennt werden kann.</span><span class="sxs-lookup"><span data-stu-id="24865-161">Concretely, this means that it's not possible to use `wsl --mount` to read a partition on the boot device, because that device can't be detached from Windows.</span></span>

- <span data-ttu-id="24865-162">USB-Flash Laufwerke werden zurzeit nicht unterstützt und können nicht an WSL 2 angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="24865-162">USB flash drives are not supported at this time and will fail to attach to WSL 2.</span></span> <span data-ttu-id="24865-163">USB-Datenträger werden jedoch unterstützt.</span><span class="sxs-lookup"><span data-stu-id="24865-163">USB disks are supported though.</span></span>

- <span data-ttu-id="24865-164">Nur Dateisysteme, die im Kernel nativ unterstützt werden, können von bereitgestellt werden `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="24865-164">Only filesystems that are natively supported in the kernel can be mounted by `wsl --mount`.</span></span> <span data-ttu-id="24865-165">Dies bedeutet, dass es nicht möglich ist, installierte Dateisystem Treiber (z. b. NTFS-3G) zu verwenden, indem aufgerufen wird `wsl --mount` .</span><span class="sxs-lookup"><span data-stu-id="24865-165">This means that it's not possible to use installed filesystem drivers (such as ntfs-3g for example) by calling `wsl --mount`.</span></span>
