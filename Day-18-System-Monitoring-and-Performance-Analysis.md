# Day 18: System Monitoring & Performance Analysis

> Understanding Linux system monitoring, CPU usage, memory utilization, disk performance, and system performance tools.

---

# 🎯 Learning Objectives

- Understand System Monitoring.
- Monitor CPU Usage.
- Analyze Memory.
- Monitor Disk Performance.
- Learn Performance Tools.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux administrators continuously monitor system performance to identify bottlenecks and maintain system stability.

Monitoring helps detect resource shortages before they affect users.

---

# System Monitoring Tools

- top
- htop
- vmstat
- iostat
- free
- uptime
- sar

---

# CPU Monitoring

View CPU usage:

```bash
top
```

---

# Memory Usage

Display RAM:

```bash
free -h
```

---

# System Uptime

```bash
uptime
```

Displays:

- Current Time
- Running Time
- Load Average

---

# Virtual Memory

Monitor:

```bash
vmstat
```

---

# Disk Performance

Monitor:

```bash
iostat
```

---

# System Load

Load Average represents CPU demand.

Example:

```
1 Minute

5 Minutes

15 Minutes
```

---

# Process Monitoring

Useful commands:

- ps
- top
- htop

---

# Performance Bottlenecks

Common causes:

- High CPU Usage
- Low Memory
- Disk I/O
- Network Congestion

---

# Best Practices

- Monitor resources regularly.
- Investigate abnormal CPU usage.
- Keep sufficient free memory.
- Monitor disk performance.

---

# 📌 Key Takeaways

- top monitors CPU.
- free displays memory.
- uptime shows load.
- vmstat analyzes virtual memory.
- iostat monitors storage performance.

---

# ❓ Interview Questions

### 1. Which command displays RAM usage?

free -h

### 2. Which command monitors CPU?

top

### 3. What does uptime display?

System uptime and load average.

### 4. Which command monitors disk performance?

iostat

### 5. Why monitor system performance?

To detect bottlenecks and maintain stability.

---

# 📝 Summary

Today I learned about Linux system monitoring, CPU, memory, disk performance, load averages, and monitoring tools including top, free, uptime, vmstat, and iostat.
