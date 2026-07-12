# Day 6: Process Management

> Understanding how Linux manages running programs, processes, and system resources.

---

# 🎯 Learning Objectives

- Understand what a Process is.
- Learn the Process Life Cycle.
- Understand Process IDs (PID).
- Learn Foreground and Background Processes.
- Master common process management commands.
- Learn how to terminate processes safely.
- Understand process priority and scheduling.

---

# 📖 Introduction

Whenever you open an application, execute a command, or run a script in Linux, the operating system creates a **Process**.

A Process is simply a running instance of a program.

Linux constantly manages hundreds or even thousands of processes simultaneously while ensuring efficient CPU and memory utilization.

Understanding Process Management is essential for Linux administrators, Cloud Engineers, DevOps Engineers, and Cybersecurity Professionals.

---

# ⚙️ What is a Process?

A Process is a program that is currently being executed by the operating system.

Examples:

- Opening Firefox
- Running Google Chrome
- Executing a Python program
- Running a Bash script

Each running program becomes its own process.

---

# Process Life Cycle

Every process goes through different stages.

```
New

↓

Ready

↓

Running

↓

Waiting

↓

Terminated
```

### New

The operating system creates the process.

---

### Ready

The process is waiting for CPU time.

---

### Running

The CPU is executing the process.

---

### Waiting

The process waits for input/output operations or resources.

---

### Terminated

The process finishes execution.

---

# Process ID (PID)

Every process has a unique **Process ID (PID)**.

Linux uses the PID to identify and manage processes.

Example:

```
PID 2456
```

No two running processes have the same PID.

---

# Parent and Child Processes

Some processes create other processes.

Example:

```
Terminal

↓

Bash Shell

↓

Python Program
```

The original process is called the **Parent Process**.

The newly created process is called the **Child Process**.

---

# Foreground Process

A Foreground Process runs directly in the terminal.

You must wait until it finishes before executing another command.

Example:

```bash
python3 app.py
```

The terminal remains occupied until the program completes.

---

# Background Process

A Background Process runs independently while allowing you to continue using the terminal.

Example:

```bash
python3 app.py &
```

The `&` symbol starts the process in the background.

---

# Viewing Running Processes

## ps

Displays currently running processes.

```bash
ps
```

Example Output:

```bash
PID   TTY      TIME   CMD

2043  pts/0    00:00  bash

3120  pts/0    00:01  python3
```

---

## ps -ef

Displays detailed information about all running processes.

```bash
ps -ef
```

---

## top

Displays real-time information about running processes.

```bash
top
```

Shows:

- CPU Usage
- Memory Usage
- Running Processes
- Process IDs

---

## htop

An improved version of top with a more user-friendly interface.

```bash
htop
```

Features:

- Colorful interface
- Easy navigation
- Interactive process management

Note: htop may need to be installed separately.

---

# Managing Processes

## kill

Terminates a process using its PID.

```bash
kill 2541
```

---

## kill -9

Forcefully terminates a process.

```bash
kill -9 2541
```

Use only when the normal kill command does not work.

---

## killall

Terminates all processes with the specified name.

```bash
killall firefox
```

---

# Jobs Command

Displays background jobs running in the current terminal.

```bash
jobs
```

---

# bg Command

Moves a stopped process to the background.

```bash
bg
```

---

# fg Command

Brings a background process back to the foreground.

```bash
fg
```

---

# Process Priority

Linux assigns priorities to processes.

Higher-priority processes receive CPU time before lower-priority processes.

Priority is controlled using the **nice value**.

---

# nice Command

Starts a process with a specified priority.

```bash
nice -n 10 python3 app.py
```

Nice values range from:

```
-20  Highest Priority

↓

19  Lowest Priority
```

---

# renice Command

Changes the priority of a running process.

```bash
sudo renice 5 -p 2456
```

---

# Signals

Linux communicates with processes using signals.

Common signals include:

| Signal | Description |
|----------|-------------|
| SIGTERM | Gracefully terminate a process |
| SIGKILL | Forcefully terminate a process |
| SIGSTOP | Pause a process |
| SIGCONT | Resume a paused process |

---

# Checking System Load

## uptime

Displays system uptime and load average.

```bash
uptime
```

---

## free

Displays memory usage.

```bash
free -h
```

---

## vmstat

Displays system performance statistics.

```bash
vmstat
```

---

# 🌍 Real-Life Example

A web server becomes slow because one application is consuming excessive CPU resources.

The Linux administrator:

- Runs `top` to identify the problematic process.
- Finds the PID.
- Uses `kill` to stop the process.
- Restarts the application.
- Normal server performance is restored.

This demonstrates how process management helps maintain system stability.

---

# 💡 Best Practices

- Monitor running processes regularly.
- Avoid using `kill -9` unless necessary.
- Use `top` or `htop` to monitor resource usage.
- Remove unnecessary background processes.
- Assign proper process priorities.
- Restart services instead of forcefully killing them whenever possible.

---

# 📌 Key Takeaways

- A Process is a running program.
- Every process has a unique PID.
- Linux supports Foreground and Background processes.
- `ps`, `top`, and `htop` display running processes.
- `kill` terminates processes.
- `killall` terminates processes by name.
- `nice` and `renice` manage process priority.
- Signals control process behavior.

---

# ❓ Interview Questions

### 1. What is a Process?

A Process is a program that is currently being executed by the operating system.

---

### 2. What is a PID?

PID (Process ID) is the unique identifier assigned to every running process.

---

### 3. Difference between Foreground and Background Process?

Foreground processes occupy the terminal until completion, whereas Background processes run independently while allowing continued terminal use.

---

### 4. What does the `ps` command do?

It displays information about running processes.

---

### 5. What is the difference between `kill` and `kill -9`?

`kill` sends a SIGTERM signal, allowing the process to terminate gracefully. `kill -9` sends a SIGKILL signal, forcefully stopping the process immediately.

---

### 6. What is the purpose of the `top` command?

It displays real-time information about system performance and running processes.

---

### 7. What is the purpose of the `nice` command?

The `nice` command starts a process with a specified priority.

---

### 8. What does the `jobs` command display?

It displays background jobs running in the current terminal.

---

# 📝 Summary

Today I learned about Linux Process Management. I explored what processes are, how Linux manages them, and the different stages of a process life cycle. I learned how to view and control running processes using commands such as `ps`, `top`, `htop`, `kill`, `killall`, `jobs`, `bg`, `fg`, `nice`, and `renice`. Understanding process management is essential for maintaining system performance, troubleshooting issues, and administering Linux servers effectively.
