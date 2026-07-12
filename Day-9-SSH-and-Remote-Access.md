# Day 9: SSH and Remote Access

> Understanding Secure Shell (SSH), remote access, file transfer, SSH keys, and secure remote administration in Linux.

---

# 🎯 Learning Objectives

- Understand what SSH is.
- Learn why SSH is used.
- Understand Remote Access.
- Learn how SSH works.
- Master common SSH commands.
- Learn SSH Key Authentication.
- Understand SCP and SFTP.
- Learn SSH security best practices.

---

# 📖 Introduction

Modern organizations often manage Linux servers that are located in different cities or even different countries. Instead of physically accessing these servers, administrators securely connect to them over a network.

Linux uses **SSH (Secure Shell)** as the standard protocol for secure remote access.

SSH allows administrators to manage servers, transfer files, execute commands, and troubleshoot systems securely from anywhere in the world.

---

# 🔐 What is SSH?

SSH (Secure Shell) is a secure network protocol that allows users to remotely access and manage another computer over a network.

Unlike older protocols such as Telnet, SSH encrypts all communication between the client and the server.

SSH is widely used by:

- Linux Administrators
- Cloud Engineers
- DevOps Engineers
- Cybersecurity Professionals

---

# Why is SSH Important?

SSH provides:

- Secure remote login
- Encrypted communication
- Remote command execution
- Secure file transfer
- Server administration

Without SSH, managing cloud servers would be extremely difficult.

---

# How SSH Works

SSH follows a Client-Server architecture.

```
Your Laptop

↓

SSH Client

↓

Encrypted Connection

↓

SSH Server

↓

Remote Linux Machine
```

The SSH Client initiates a secure connection with the SSH Server.

All data transmitted between them is encrypted.

---

# SSH Default Port

SSH uses:

```
Port 22
```

Administrators sometimes change the default port to improve security.

---

# SSH Authentication Methods

SSH supports two authentication methods.

## 1. Password Authentication

The user enters:

- Username
- Password

Example

```
ssh user@192.168.1.20
```

The server requests the user's password.

---

## 2. SSH Key Authentication

Instead of passwords, SSH can use cryptographic key pairs.

The user generates:

- Public Key
- Private Key

The Public Key is stored on the server.

The Private Key remains on the user's computer.

This method is much more secure than password authentication.

---

# Connecting to a Remote Server

Basic Syntax

```bash
ssh username@hostname
```

Example

```bash
ssh nanditha@192.168.1.50
```

Example using a domain name

```bash
ssh ubuntu@example.com
```

---

# Generating SSH Keys

Generate a new SSH key pair.

```bash
ssh-keygen
```

Files created:

```
~/.ssh/id_rsa

↓

Private Key

~/.ssh/id_rsa.pub

↓

Public Key
```

Never share your Private Key.

---

# Copying SSH Public Key

Copy the public key to the server.

```bash
ssh-copy-id username@hostname
```

Example

```bash
ssh-copy-id ubuntu@192.168.1.50
```

Now password-less login becomes possible.

---

# Secure Copy (SCP)

SCP is used to securely copy files between computers using SSH.

Copy local file to remote server

```bash
scp report.txt ubuntu@192.168.1.50:/home/ubuntu
```

Copy file from remote server

```bash
scp ubuntu@192.168.1.50:/home/ubuntu/report.txt .
```

---

# Secure File Transfer Protocol (SFTP)

SFTP allows secure file transfer using SSH.

Connect

```bash
sftp username@hostname
```

Useful Commands

Upload file

```bash
put notes.txt
```

Download file

```bash
get report.pdf
```

List files

```bash
ls
```

Exit

```bash
exit
```

---

# SSH Configuration File

SSH client configuration is stored in:

```
~/.ssh/config
```

Example

```
Host aws-server

HostName 54.23.45.10

User ubuntu

Port 22
```

Now connect using:

```bash
ssh aws-server
```

---

# Common SSH Commands

Check SSH version

```bash
ssh -V
```

Connect to server

```bash
ssh username@host
```

Generate keys

```bash
ssh-keygen
```

Copy public key

```bash
ssh-copy-id username@host
```

Exit SSH session

```bash
exit
```

---

# SSH Security Best Practices

- Use SSH Keys instead of passwords.
- Disable Root Login.
- Disable Password Authentication if possible.
- Use strong passphrases.
- Keep SSH updated.
- Change the default SSH port if appropriate.
- Allow only trusted users.
- Monitor SSH login attempts.

---

# 🌍 Real-Life Example

A Cloud Engineer needs to manage an AWS EC2 Linux server.

Instead of physically accessing the server, the engineer:

- Generates an SSH key pair.
- Uploads the public key to AWS.
- Connects using:

```bash
ssh -i mykey.pem ubuntu@54.120.xxx.xxx
```

The engineer securely updates software, monitors services, and deploys applications remotely.

---

# 📌 Key Takeaways

- SSH provides secure remote access.
- SSH encrypts communication.
- SSH uses Port 22 by default.
- SSH Keys are more secure than passwords.
- SCP securely copies files.
- SFTP securely transfers files.
- SSH is essential for Linux, Cloud, DevOps, and Cybersecurity.

---

# ❓ Interview Questions

### 1. What is SSH?

SSH (Secure Shell) is a secure protocol used for remote login and server administration.

---

### 2. Why is SSH preferred over Telnet?

SSH encrypts all communication, while Telnet sends data in plain text.

---

### 3. Which port does SSH use?

SSH uses Port 22 by default.

---

### 4. What are SSH Keys?

SSH Keys are a pair of cryptographic keys (Public Key and Private Key) used for secure authentication.

---

### 5. What is SCP?

SCP (Secure Copy Protocol) securely transfers files between systems using SSH.

---

### 6. What is SFTP?

SFTP (Secure File Transfer Protocol) securely transfers files using SSH.

---

### 7. Why should Private Keys never be shared?

Because anyone with the Private Key can authenticate as the owner and gain unauthorized access.

---

### 8. Which command generates SSH Keys?

```bash
ssh-keygen
```

---

# 📝 Summary

Today I learned about SSH (Secure Shell), the standard protocol used for secure remote access in Linux. I explored how SSH works, different authentication methods, SSH key generation, SCP, SFTP, SSH configuration, and best security practices. SSH is one of the most important tools used by Linux Administrators, Cloud Engineers, DevOps Engineers, and Cybersecurity Professionals for managing remote systems securely.
