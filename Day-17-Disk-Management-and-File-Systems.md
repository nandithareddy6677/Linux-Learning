# Day 17: Disk Management & File Systems

> Understanding Linux disk management, partitions, file systems, mounting, storage management, and essential disk commands.

---

# 🎯 Learning Objectives

- Understand Disk Management.
- Learn Linux File Systems.
- Explore Disk Partitions.
- Understand Mounting.
- Learn Storage Commands.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux stores all data on storage devices such as HDDs, SSDs, and cloud volumes.

Before using a storage device, Linux partitions, formats, and mounts it.

---

# 💾 What is Disk Management?

Disk Management refers to creating, organizing, formatting, and maintaining storage devices.

Tasks include:

- Creating Partitions
- Formatting Drives
- Mounting File Systems
- Monitoring Disk Usage

---

# Linux File Systems

Common File Systems:

- ext4
- XFS
- Btrfs
- FAT32
- NTFS

---

# Disk Partitions

A disk can be divided into multiple logical sections called partitions.

Example:

```
Disk

↓

Partition 1

Partition 2

Partition 3
```

---

# Mounting

Linux mounts storage devices into the file system.

Mount command:

```bash
mount
```

Manual mount:

```bash
sudo mount /dev/sdb1 /mnt/data
```

---

# Unmounting

```bash
sudo umount /mnt/data
```

---

# Viewing Disk Usage

```bash
df -h
```

Displays:

- Total Space
- Used Space
- Available Space

---

# Directory Size

```bash
du -sh folder
```

---

# List Block Devices

```bash
lsblk
```

---

# File System Information

```bash
blkid
```

---

# Disk Partition Tools

- fdisk
- parted
- gparted

---

# Best Practices

- Monitor disk usage regularly.
- Avoid filling disks to 100%.
- Use reliable file systems.
- Backup important data.

---

# 📌 Key Takeaways

- Linux uses file systems to organize storage.
- Mounting makes storage accessible.
- df shows disk usage.
- du shows directory size.
- lsblk lists storage devices.

---

# ❓ Interview Questions

### 1. What does df -h do?

Displays disk usage.

### 2. Which command lists block devices?

lsblk

### 3. What is mounting?

Attaching a file system to the Linux directory structure.

### 4. Which Linux file system is most commonly used?

ext4

### 5. What does du -sh display?

The size of a directory.

---

# 📝 Summary

Today I learned about Linux disk management, file systems, partitions, mounting, and disk usage commands such as df, du, lsblk, and mount. These tools help administrators manage storage efficiently.
