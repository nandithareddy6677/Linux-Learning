# Day 19: System Logs & Log Management

> Understanding Linux logging, system logs, journalctl, syslog, log rotation, and troubleshooting using log files.

---

# 🎯 Learning Objectives

- Understand Linux Logging.
- Learn System Logs.
- Explore journalctl.
- Understand Log Rotation.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux records system events inside log files.

Logs help administrators troubleshoot problems, monitor activity, and investigate security incidents.

---

# What are System Logs?

System Logs record:

- Login Attempts
- Errors
- Application Events
- Security Events
- System Startup

---

# Common Log Locations

```
/var/log/
```

Examples:

- syslog
- auth.log
- kern.log
- messages
- dmesg

---

# journalctl

Displays systemd logs.

Example:

```bash
journalctl
```

Latest logs:

```bash
journalctl -xe
```

---

# View Log Files

```bash
cat

less

tail

head
```

---

# tail Command

View recent log entries:

```bash
tail -f /var/log/syslog
```

---

# dmesg

Displays kernel boot messages.

```bash
dmesg
```

---

# Log Rotation

Linux automatically rotates logs.

Managed by:

```
logrotate
```

Benefits:

- Saves Disk Space
- Prevents Large Log Files
- Improves Performance

---

# Security Logs

Useful logs:

- Authentication Logs
- SSH Login Logs
- Failed Login Attempts
- sudo Activity

---

# Best Practices

- Monitor logs regularly.
- Archive important logs.
- Protect sensitive log files.
- Configure log rotation.

---

# 📌 Key Takeaways

- Linux stores logs in /var/log.
- journalctl reads systemd logs.
- tail monitors live logs.
- logrotate manages log files.
- Logs are essential for troubleshooting.

---

# ❓ Interview Questions

### 1. Where are Linux logs stored?

/var/log

### 2. What does journalctl do?

Displays systemd logs.

### 3. Which command monitors live logs?

tail -f

### 4. What is logrotate?

A tool that manages log rotation.

### 5. Why are logs important?

They help troubleshoot, monitor, and investigate systems.

---

# 📝 Summary

Today I learned about Linux system logs, journalctl, log management, log rotation, and troubleshooting using log files. Proper log management is essential for maintaining system health, auditing activities, and identifying security incidents.
