# Day 13: Linux Package Management

> Understanding package management, software installation, package repositories, updates, and package managers used in Linux distributions.

---

# 🎯 Learning Objectives

- Understand Package Management.
- Learn Package Managers.
- Install and Remove Software.
- Update Packages.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux distributions provide package managers to simplify software installation, updates, and removal.

Package managers automatically handle dependencies.

---

# What is a Package?

A Package is a compressed software bundle containing:

- Program Files
- Libraries
- Configuration Files
- Documentation

---

# Package Managers

Ubuntu/Debian:

- apt

RHEL/CentOS:

- yum
- dnf

Arch Linux:

- pacman

---

# Installing Software

Ubuntu:

```bash
sudo apt install nginx
```

---

# Updating Package List

```bash
sudo apt update
```

---

# Upgrading Packages

```bash
sudo apt upgrade
```

---

# Removing Packages

```bash
sudo apt remove nginx
```

---

# Searching Packages

```bash
apt search nginx
```

---

# Package Information

```bash
apt show nginx
```

---

# Repositories

Repositories are online storage locations containing software packages.

Benefits:

- Trusted Software
- Easy Updates
- Dependency Management

---

# Package Dependencies

Many applications require additional libraries.

Package managers automatically install required dependencies.

---

# Best Practices

- Keep packages updated.
- Install software from trusted repositories.
- Remove unused packages.
- Update regularly for security.

---

# 📌 Key Takeaways

- Package managers simplify software management.
- apt is used in Ubuntu.
- yum and dnf are used in RHEL-based systems.
- Repositories provide trusted software.
- Updates improve security.

---

# ❓ Interview Questions

### 1. What is apt?

A package manager for Debian-based Linux distributions.

### 2. Which command updates package information?

```bash
sudo apt update
```

### 3. Which command upgrades installed software?

```bash
sudo apt upgrade
```

### 4. What is a package repository?

A centralized location that stores software packages.

### 5. Why are package managers useful?

They simplify installation, updates, dependency management, and software removal.

---

# 📝 Summary

Today I learned about Linux package management, package repositories, software installation, updates, and package managers such as apt, yum, and dnf. Package managers simplify software maintenance while ensuring systems remain secure and up to date.
