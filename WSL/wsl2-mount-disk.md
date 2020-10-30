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
# <a name="get-started-mounting-a-linux-disk-in-wsl-2-preview"></a>Einstieg in die Einbindung eines Linux-Datenträgers in WSL 2 (Vorschau)

Wenn Sie auf ein Linux-Datenträgerformat zugreifen möchten, das von Windows nicht unterstützt wird, können Sie mit WSL 2 Ihren Datenträger einbinden und auf dessen Inhalte zugreifen.

In diesem Tutorial werden die Schritte beschrieben, mit denen der Datenträger und die Partition identifiziert werden, die an WSL2 angefügt werden sollen, und wie Sie darauf zugreifen können.

> [!NOTE]
> Für den Zugriff auf dieses Feature müssen Sie unter Windows 10 Build 20211 oder höher sein. Sie können das [Windows Insider-Programm](https://insider.windows.com/) beitreten, um die neuesten Vorschau Versionen zu erhalten.
> Der Administrator Zugriff ist erforderlich, um einen Datenträger an WSL 2 anzufügen.

## <a name="identify-the-disk"></a>Identifizieren des Datenträgers

Führen Sie Folgendes aus, um die verfügbaren Datenträger in Windows aufzulisten:

```powershell
wmic diskdrive list brief
```

Die Datenträger Pfade sind unter den ' de viceid '-Spalten verfügbar. Normalerweise im `\\.\PHYSICALDRIVE*` Format.

## <a name="list-and-select-the-partitions-to-mount-in-wsl-2"></a>Auflisten und Auswählen der Partitionen zum Einbinden in WSL 2

Nachdem der Datenträger identifiziert wurde, führen Sie Folgendes aus:

```powershell
wsl --mount <DiskPath> --bare
```

Dadurch wird der Datenträger in WSL 2 verfügbar.

Nach dem anfügen kann die Partition aufgelistet werden, indem Sie den folgenden Befehl in WSL 2 ausführen:

```powershell
lsblk
```

Dadurch werden die verfügbaren Blockgeräte und Ihre Partitionen angezeigt.

Innerhalb von Linux wird ein Blockgerät als bezeichnet  `/dev/<Device><Partition>` . Beispielsweise ist/dev/sdb3 die Partitionsnummer 3 des Datenträgers `sdb` .

Beispielausgabe:

```powershell
NAME   MAJ:MIN RM  SIZE RO TYPE MOUNTPOINT
sdb      8:16   0    1G  0 disk
├─sdb2   8:18   0   50M  0 part
├─sdb3   8:19   0  873M  0 part
└─sdb1   8:17   0  100M  0 part
sdc      8:32   0  256G  0 disk /
sda      8:0    0  256G  0 disk
```

## <a name="identifying-the-filesystem-type"></a>Identifizieren des Dateisystem Typs

Wenn Sie den Typ des Dateisystems eines Datenträgers oder einer Partition nicht kennen, können Sie diesen Befehl verwenden:

```powershell
blkid <BlockDevice>
```

Dadurch wird der erkannte File System-Typ ausgegeben (im `TYPE="<Filesystem>"` Format).

## <a name="mount-the-selected-partitions"></a>Ausgewählte Partitionen einbinden

Nachdem Sie die Partitionen identifiziert haben, die Sie einbinden möchten, führen Sie diesen Befehl für jede Partition aus: 

```powershell
wsl --mount <DiskPath> --partition <PartitionNumber> --type <Filesystem>
```

> [!NOTE]
> Wenn Sie den gesamten Datenträger als einzelnes Volume einbinden möchten (d. h., wenn der Datenträger nicht partitioniert ist), `--partition` kann weggelassen werden.
> 
> Wenn keine Angabe erfolgt, ist der Standard dateidateityp "ext4".

## <a name="access-the-disk-content"></a>Zugreifen auf den Datenträger Inhalt

Nach der Bereitstellung kann auf den Datenträger unter dem Pfad zugegriffen werden, auf den durch den Konfigurations Wert verwiesen wird: `automount.root` . Standardwert: `/mnt/wsl`.

Aus Windows kann auf den Datenträger über den Datei-Explorer zugegriffen werden, indem Sie zu navigieren: `\\wsl$\\<Distro>\\<Mountpoint>` (beliebige Linux-Distribution auswählen).

## <a name="unmount-the-disk"></a>Aufheben der Bereitstellung des Datenträgers

Wenn Sie die Bereitstellung des Datenträgers von WSL 2 entfernen und den Datenträger trennen möchten, führen Sie Folgendes aus:

```powershell
wsl --unmount <DiskPath>
```

## <a name="command-line-reference"></a>Befehlszeilenreferenz

### <a name="mouting-a-specific-filesystem"></a>Mouting eines bestimmten Dateisystems

Standardmäßig wird von WSL 2 versucht, das Gerät als ext4 zu einbinden. Führen Sie zum Angeben eines anderen Dateisystems Folgendes aus:

```powershell
wsl --mount <DiskPath> -t <FileSystem>
```

Wenn Sie beispielsweise einen Datenträger als FAT einbinden möchten, führen Sie Folgendes aus:

```
wsl --mount <Diskpath> -t vfat
```

> [!NOTE]
> Führen Sie Folgendes aus, um die verfügbaren Dateisysteme in WSL2 aufzulisten: `cat /proc/filesystems`

### <a name="mouting-a-specific-partition"></a>Mouting für eine bestimmte Partition

Standardmäßig versucht WSL 2, den gesamten Datenträger einbinden. Führen Sie zum Einbinden einer bestimmten Partition Folgendes aus:

```
wsl --mount <Diskpath> -p <PartitionIndex>
```

Dies funktioniert nur, wenn es sich bei dem Datenträger um MBR (Master Boot Record) oder GPT (GUID-Partitionstabelle) handelt. [Informieren Sie sich über die Partitions Stile MBR und GPT](/windows-server/storage/disk-management/initialize-new-disks#about-partition-styles---gpt-and-mbr).

### <a name="specifying-mount-options"></a>Angeben von Optionen

Führen Sie zum Angeben der Einstellungsoptionen Folgendes aus:

```powershell
wsl --mount <DiskPath> -o <MountOptions>
```

Beispiel:

```powershell
wsl --mount <DiskPath> -o "data=ordered"
```

> [!NOTE]
> Zurzeit werden nur Dateisystem spezifische Optionen unterstützt. Generische Optionen wie `ro, rw, noatime, ...` werden nicht unterstützt.

### <a name="attaching-the-disk-without-mounting-it"></a>Anfügen des Datenträgers ohne Einbindung

Wenn das Datenträger Schema von keiner der oben aufgeführten Optionen unterstützt wird, können Sie den Datenträger an WSL 2 anfügen, ohne ihn bereitzustellen, indem Sie Folgendes ausführen:

```powershell
wsl --mount <DiskPath> --bare
```

Dadurch wird das Blockgerät in WSL 2 zur Verfügung gestellt, sodass es von dort aus manuell eingebunden werden kann. Verwenden `lsblk` Sie, um die verfügbaren Blockgeräte in WSL 2 aufzulisten.

### <a name="detaching-a-disk"></a>Trennen eines Datenträgers

Führen Sie zum Trennen eines Datenträgers von WSL 2 Folgendes aus:

```powershell
wsl --unmount [DiskPath]
```

Wenn `Diskpath` weggelassen wird, werden alle angefügten Datenträger nicht bereitgestellt und getrennt.

> [!NOTE]
> Wenn die Bereitstellung eines Datenträgers nicht rückgängig gemacht werden kann, kann WSL 2 durch Ausführen von erzwungen werden, wodurch der Datenträger getrennt `wsl --shutdown` wird.

## <a name="limitations"></a>Einschränkungen

- Zu diesem Zeitpunkt können nur ganze Datenträger an WSL 2 angefügt werden. Dies bedeutet, dass es nicht möglich ist, nur eine Partition anzufügen. Konkret bedeutet dies, dass es nicht möglich ist, `wsl --mount` eine Partition auf dem Startgerät zu lesen, da dieses Gerät nicht von Windows getrennt werden kann.

- USB-Flash Laufwerke werden zurzeit nicht unterstützt und können nicht an WSL 2 angefügt werden. USB-Datenträger werden jedoch unterstützt.

- Nur Dateisysteme, die im Kernel nativ unterstützt werden, können von bereitgestellt werden `wsl --mount` . Dies bedeutet, dass es nicht möglich ist, installierte Dateisystem Treiber (z. b. NTFS-3G) zu verwenden, indem aufgerufen wird `wsl --mount` .
