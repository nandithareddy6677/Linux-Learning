# Day 20: Linux Networking Commands & SSH

> Understanding Linux networking commands, SSH, remote access, network diagnostics, and secure communication.

---

# 🎯 Learning Objectives

- Understand Linux Networking.
- Learn SSH.
- Explore Network Commands.
- Diagnose Network Issues.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux systems often communicate over networks.

Administrators use networking commands to troubleshoot connectivity, manage remote systems, and verify network configurations.

---

# 🌐 Check IP Address

Display IP information:

```bash
ip addr
```

or

```bash
hostname -I
```

---

# Check Network Interfaces

```bash
ip link
```

---

# Test Connectivity

```bash
ping google.com
```

---

# DNS Lookup

```bash
nslookup google.com
```

or

```bash
dig google.com
```

---

# Check Open Ports

```bash
ss -tuln
```

or

```bash
netstat -tuln
```

---

# View Routing Table

```bash
ip route
```

---

# What is SSH?

SSH (Secure Shell) is a secure protocol used to remotely access Linux systems.

Default Port:

```
22
```

---

# Connect Using SSH

```bash
ssh username@server_ip
```

Example:

```bash
ssh ubuntu@192.168.1.10
```

---

# SSH Key Authentication

Generate keys:

```bash
ssh-keygen
```

Copy key:

```bash
ssh-copy-id username@server_ip
```

---

# Secure Copy (SCP)

Transfer files securely.

```bash
scp file.txt user@server:/home/user/
```

---

# Common Networking Commands

- ping
- traceroute
- curl
- wget
- ssh
- scp
- ip
- ss

---

# Best Practices

- Disable root SSH login.
- Use SSH keys.
- Change default passwords.
- Enable firewalls.
- Monitor SSH logs.

---

# 📌 Key Takeaways

- SSH enables secure remote access.
- ip addr displays network configuration.
- ping checks connectivity.
- scp securely transfers files.
- SSH keys improve security.

---

# ❓ Interview Questions

### 1. What is SSH?

A secure protocol for remote system access.

### 2. Which port does SSH use?

22

### 3. Which command generates SSH keys?

ssh-keygen

### 4. Which command copies files securely?

scp

### 5. Which command shows IP addresses?

ip addr

---

# 📝 Summary

Today I learned about Linux networking commands, SSH, remote access, SSH key authentication, and secure file transfers using SCP. These tools are fundamental for Linux administration and cloud infrastructure management.
