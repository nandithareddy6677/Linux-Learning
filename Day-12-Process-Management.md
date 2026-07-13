# Day 12: Process Management

> Understanding Linux processes, process states, foreground and background processes, process monitoring, and process control commands.

---

# 🎯 Learning Objectives

- Understand Processes.
- Learn Process States.
- Monitor Processes.
- Manage Running Programs.
- Prepare for Linux interviews.

---

# 📖 Introduction

Every running application in Linux is called a process.

Linux allows users to monitor, control, and terminate processes efficiently.

---

# What is a Process?

A Process is a running instance of a program.

Example:

```
Firefox

↓

Running Process
```

---

# Process States

- Running
- Sleeping
- Stopped
- Zombie

---

# Process ID (PID)

Every process has a unique Process ID.

Example:

```bash
ps
```

---

# Process Monitoring

View running processes:

```bash
top
```

or

```bash
htop
```

---

# ps Command

Displays process information.

Example:

```bash
ps aux
```

---

# kill

Terminates a process.

```bash
kill PID
```

---

# kill -9

Forcefully stops a process.

```bash
kill -9 PID
```

---

# Background Processes

Run a program in the background:

```bash
command &
```

---

# jobs

Displays background jobs.

```bash
jobs
```

---

# fg

Moves a background process to the foreground.

```bash
fg
```

---

# bg

Continues a stopped process in the background.

```bash
bg
```

---

# nice

Changes process priority.

```bash
nice
```

---

# System Monitoring

Useful commands:

- top
- htop
- uptime
- free
- vmstat

---

# Best Practices

- Monitor CPU usage.
- Kill unnecessary processes.
- Use background jobs efficiently.
- Avoid force-killing unless required.

---

# 📌 Key Takeaways

- Every running application is a process.
- PID uniquely identifies processes.
- top monitors running processes.
- kill terminates processes.
- Background jobs improve productivity.

---

# ❓ Interview Questions

### 1. What is a Process?

A running instance of a program.

### 2. Which command shows running processes?

ps

### 3. Which command monitors system processes?

top

### 4. What does kill do?

Terminates a process.

### 5. What is PID?

Process ID.

---

# 📝 Summary

Today I learned about Linux process management, process monitoring, foreground and background execution, process IDs, and commands such as ps, top, kill, jobs, bg, and fg.
