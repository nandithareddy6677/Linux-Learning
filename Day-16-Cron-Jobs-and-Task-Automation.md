# Day 16: Cron Jobs & Task Automation

> Understanding Cron, Crontab, scheduled tasks, automation, system maintenance, and job scheduling in Linux.

---

# 🎯 Learning Objectives

- Understand Cron.
- Learn Crontab.
- Schedule Tasks.
- Automate Linux Administration.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux can automatically execute commands at scheduled times.

This feature is provided by the Cron service.

---

# ⏰ What is Cron?

Cron is a background service that executes scheduled commands automatically.

Examples:

- Daily Backups
- Log Cleanup
- Database Maintenance
- System Updates

---

# Crontab

Crontab stores scheduled jobs.

Edit:

```bash
crontab -e
```

List jobs:

```bash
crontab -l
```

Remove jobs:

```bash
crontab -r
```

---

# Cron Format

```
Minute Hour Day Month DayOfWeek Command
```

Example:

```
0 2 * * * backup.sh
```

Runs every day at 2:00 AM.

---

# Common Schedules

Every Minute

```
* * * * *
```

Every Hour

```
0 * * * *
```

Every Day

```
0 0 * * *
```

Every Sunday

```
0 3 * * 0
```

---

# Benefits

- Automation
- Reduced Manual Work
- Consistent Execution
- Improved Productivity

---

# Common Automation Tasks

- Database Backups
- Security Scans
- System Monitoring
- Email Reports
- Log Rotation

---

# Best Practices

- Test scripts before scheduling.
- Use absolute file paths.
- Monitor Cron logs.
- Keep scheduled tasks documented.

---

# 📌 Key Takeaways

- Cron automates Linux tasks.
- Crontab stores scheduled jobs.
- Jobs execute automatically.
- Automation saves time.

---

# ❓ Interview Questions

### 1. What is Cron?

A Linux service that executes scheduled tasks.

### 2. Which command edits Cron jobs?

crontab -e

### 3. Which command lists Cron jobs?

crontab -l

### 4. Why use Cron?

To automate repetitive administrative tasks.

### 5. What is Crontab?

A configuration file used to schedule Cron jobs.

---

# 📝 Summary

Today I learned about Cron, Crontab, job scheduling, and Linux task automation. Cron is widely used by system administrators, DevOps engineers, and cloud professionals to automate maintenance, backups, monitoring, and other recurring tasks.
