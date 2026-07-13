# Day 25: Backup & Recovery Strategies

> Understanding Linux backup methods, recovery strategies, rsync, tar, snapshots, disaster recovery, and business continuity.

---

# 🎯 Learning Objectives

- Understand Backup Strategies.
- Learn Recovery Methods.
- Explore rsync and tar.
- Understand Disaster Recovery.
- Prepare for Linux interviews.

---

# 📖 Introduction

Data loss can occur because of hardware failures, accidental deletion, ransomware, or natural disasters.

Regular backups are essential for maintaining business continuity.

---

# What is a Backup?

A Backup is a copy of important data that can be restored if the original data is lost or damaged.

---

# Types of Backups

## Full Backup

Copies all files.

Advantages:

- Simple recovery.

Disadvantages:

- Large storage requirement.

---

## Incremental Backup

Copies only files changed since the last backup.

Advantages:

- Faster
- Saves storage

---

## Differential Backup

Copies files changed since the last full backup.

---

# Backup Tools

- rsync
- tar
- cp
- dd

---

# rsync

Synchronizes files efficiently.

Example:

```bash
rsync -av /home/user /backup
```

---

# tar

Creates archive files.

Example:

```bash
tar -czvf backup.tar.gz /home/user
```

---

# Snapshots

Snapshots capture the state of a file system at a specific point in time.

Commonly used in:

- AWS EBS
- Azure Managed Disks
- VMware
- LVM

---

# Disaster Recovery

Recovery involves:

- Restoring backups
- Verifying data integrity
- Returning services to normal

---

# Backup Best Practices

- Follow the 3-2-1 Backup Rule.
- Encrypt backup files.
- Test recovery regularly.
- Store backups offsite.
- Automate backups using Cron.

---

# 3-2-1 Backup Rule

- 3 Copies of Data
- 2 Different Storage Media
- 1 Offsite Backup

---

# Real-World Example

A database server crashes.

The administrator restores the latest backup using rsync and cloud snapshots, minimizing downtime.

---

# 📌 Key Takeaways

- Backups protect against data loss.
- rsync synchronizes files efficiently.
- tar creates compressed archives.
- Snapshots simplify recovery.
- Test backups regularly.

---

# ❓ Interview Questions

### 1. What is a Full Backup?

A complete copy of all data.

### 2. What does rsync do?

Synchronizes files between locations.

### 3. What is the 3-2-1 Backup Rule?

3 copies, 2 storage types, 1 offsite copy.

### 4. Which command creates a compressed archive?

```bash
tar -czvf
```

### 5. Why should backups be tested?

To ensure they can be restored successfully.

---

# 📝 Summary

Today I learned about Linux backup strategies, recovery methods, rsync, tar, snapshots, disaster recovery, and the 3-2-1 backup rule. Reliable backups are critical for protecting systems and ensuring business continuity.
