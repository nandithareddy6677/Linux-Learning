# Day 29: Linux Troubleshooting & System Recovery

> Understanding Linux troubleshooting techniques, boot recovery, system diagnostics, log analysis, and essential administrative commands.

---

# 🎯 Learning Objectives

- Understand Linux Troubleshooting.
- Learn Boot Recovery.
- Analyze System Logs.
- Diagnose Performance Issues.
- Prepare for Linux interviews.

---

# 📖 Introduction

Even well-maintained Linux systems can experience hardware failures, software issues, network problems, or boot errors.

Linux administrators use a structured troubleshooting process to quickly identify and resolve these issues.

---

# 🔧 Linux Troubleshooting Methodology

```
Identify Problem

↓

Collect Information

↓

Analyze Logs

↓

Test Solution

↓

Verify

↓

Document
```

---

# Common Linux Problems

- System won't boot
- Disk Full
- High CPU Usage
- Memory Exhaustion
- Service Failure
- Network Issues
- Permission Errors

---

# Boot Recovery

Useful boot options:

- Recovery Mode
- Emergency Mode
- Rescue Mode

Common recovery tasks:

- Reset Password
- Repair File System
- Fix Boot Loader
- Restart Services

---

# Essential Diagnostic Commands

Check disk usage:

```bash
df -h
```

Memory usage:

```bash
free -h
```

Running processes:

```bash
top
```

System logs:

```bash
journalctl
```

Network connectivity:

```bash
ping google.com
```

---

# File System Check

```bash
fsck
```

Used to repair file system errors.

---

# Check Running Services

```bash
systemctl status
```

---

# Monitor Logs

```bash
tail -f /var/log/syslog
```

---

# Troubleshooting Tips

- Check logs first.
- Verify network connectivity.
- Check available disk space.
- Monitor CPU and memory.
- Restart failed services.

---

# 🌍 Real-Life Example

A web server becomes unavailable.

The administrator checks:

- Service Status
- Logs
- Disk Space
- Network Connectivity

The issue is identified as a full disk, cleaned up, and the service is restarted.

---

# 💡 Best Practices

- Monitor systems regularly.
- Keep backups.
- Document incidents.
- Update software.
- Test recovery procedures.

---

# 📌 Key Takeaways

- Troubleshooting follows a structured process.
- Logs provide valuable diagnostic information.
- Linux includes powerful troubleshooting tools.
- Regular monitoring prevents many issues.

---

# ❓ Interview Questions

### 1. Which command checks disk usage?

df -h

### 2. Which command checks memory usage?

free -h

### 3. Which command displays system logs?

journalctl

### 4. What does fsck do?

Checks and repairs file systems.

### 5. Why are logs important?

They help identify and diagnose system problems.

---

# 📝 Summary

Today I learned about Linux troubleshooting, recovery modes, diagnostic commands, log analysis, and system recovery techniques. Effective troubleshooting is essential for maintaining reliable Linux servers in production environments.
