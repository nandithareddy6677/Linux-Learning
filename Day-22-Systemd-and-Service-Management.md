# Day 22: systemd & Service Management

> Understanding systemd, Linux services, daemons, service management, startup processes, and system administration.

---

# 🎯 Learning Objectives

- Understand systemd.
- Learn Service Management.
- Manage Linux Services.
- Understand Boot Process.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux runs many background services continuously.

Examples:

- SSH
- Nginx
- Apache
- Docker

systemd manages these services.

---

# What is systemd?

systemd is the default service manager for most modern Linux distributions.

Responsibilities:

- Start Services
- Stop Services
- Manage Boot Process
- Handle Logging

---

# What is a Service?

A service is a background process (daemon) providing functionality.

Examples:

- SSH Server
- Web Server
- Database

---

# Service Management

Start service:

```bash
sudo systemctl start nginx
```

Stop service:

```bash
sudo systemctl stop nginx
```

Restart:

```bash
sudo systemctl restart nginx
```

---

# Enable Service

```bash
sudo systemctl enable nginx
```

---

# Disable Service

```bash
sudo systemctl disable nginx
```

---

# Service Status

```bash
systemctl status nginx
```

---

# List Running Services

```bash
systemctl list-units --type=service
```

---

# Boot Process

Power On

↓

Bootloader (GRUB)

↓

Kernel

↓

systemd

↓

Services

↓

Login

---

# Common Linux Services

- ssh
- nginx
- apache2
- mysql
- docker

---

# Best Practices

- Disable unused services.
- Monitor service status.
- Enable only required services.
- Keep services updated.

---

# 📌 Key Takeaways

- systemd manages Linux services.
- systemctl controls services.
- Services run in the background.
- Enable important services during boot.
- Monitor service health regularly.

---

# ❓ Interview Questions

### 1. What is systemd?

The default service manager in modern Linux.

### 2. Which command starts a service?

systemctl start

### 3. Which command checks service status?

systemctl status

### 4. What is a daemon?

A background service running continuously.

### 5. Which command enables a service at boot?

systemctl enable

---

# 📝 Summary

Today I learned about systemd, Linux services, daemons, and service management using systemctl. Managing services effectively is a core responsibility for Linux administrators, DevOps engineers, and cloud professionals.
