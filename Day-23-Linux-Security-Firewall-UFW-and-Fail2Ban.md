# Day 23: Linux Security – Firewall, UFW & Fail2Ban

> Understanding Linux security, firewalls, UFW, Fail2Ban, SSH protection, and server hardening.

---

# 🎯 Learning Objectives

- Understand Linux Security.
- Learn Firewalls.
- Configure UFW.
- Understand Fail2Ban.
- Secure SSH Servers.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux servers are often exposed to the Internet.

Without proper security, attackers can exploit open ports, weak passwords, and vulnerable services.

Linux provides built-in tools to strengthen server security.

---

# 🔐 Linux Security

Linux security focuses on:

- Access Control
- Firewall Protection
- User Permissions
- Secure Authentication
- Service Hardening

---

# 🔥 What is a Firewall?

A Firewall controls incoming and outgoing network traffic based on predefined security rules.

It helps:

- Block unauthorized access
- Allow trusted traffic
- Reduce attack surface

---

# UFW (Uncomplicated Firewall)

UFW is an easy-to-use firewall for Ubuntu and Debian systems.

---

# Check Firewall Status

```bash
sudo ufw status
```

---

# Enable Firewall

```bash
sudo ufw enable
```

---

# Disable Firewall

```bash
sudo ufw disable
```

---

# Allow SSH

```bash
sudo ufw allow 22
```

---

# Allow HTTP

```bash
sudo ufw allow 80
```

---

# Allow HTTPS

```bash
sudo ufw allow 443
```

---

# Deny a Port

```bash
sudo ufw deny 23
```

---

# Delete a Rule

```bash
sudo ufw delete allow 80
```

---

# What is Fail2Ban?

Fail2Ban protects Linux servers from brute-force attacks.

It monitors log files and temporarily blocks suspicious IP addresses.

---

# How Fail2Ban Works

```
Failed Login Attempts

↓

Log Monitoring

↓

Detect Attack

↓

Block IP Address
```

---

# Common Services Protected

- SSH
- FTP
- Apache
- Nginx
- Mail Servers

---

# SSH Hardening

Best practices:

- Disable Root Login
- Use SSH Keys
- Disable Password Authentication
- Change Default Port (optional)
- Enable Fail2Ban

---

# Best Practices

- Enable UFW.
- Install Fail2Ban.
- Keep software updated.
- Use strong passwords.
- Enable MFA where possible.

---

# 📌 Key Takeaways

- Firewalls protect Linux servers.
- UFW simplifies firewall management.
- Fail2Ban blocks brute-force attacks.
- SSH should be hardened.
- Linux security requires multiple layers.

---

# ❓ Interview Questions

### 1. What is UFW?

A simple firewall management tool for Linux.

### 2. What does Fail2Ban do?

Blocks IP addresses after repeated failed login attempts.

### 3. Which command enables UFW?

```bash
sudo ufw enable
```

### 4. Which port does SSH use?

22

### 5. Why use a firewall?

To control network access and improve security.

---

# 📝 Summary

Today I learned about Linux security, UFW, firewalls, Fail2Ban, and SSH hardening. These tools help protect Linux servers from unauthorized access and common network attacks.
