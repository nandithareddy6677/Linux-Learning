# Day 14: Shell Scripting Basics

> Understanding Shell Scripting, Bash scripting fundamentals, variables, user input, loops, conditional statements, and automation in Linux.

---

# 🎯 Learning Objectives

- Understand Shell Scripting.
- Learn Bash Scripts.
- Create Variables.
- Use Conditional Statements.
- Implement Loops.
- Automate repetitive tasks.

---

# 📖 Introduction

Linux administrators often automate repetitive tasks using Shell Scripts.

Instead of manually typing commands every day, multiple commands can be stored in a script and executed automatically.

---

# 🐚 What is Shell Scripting?

Shell Scripting is the process of writing a sequence of Linux commands inside a text file that can be executed automatically.

---

# Bash Shell

Bash (Bourne Again Shell) is the default shell in most Linux distributions.

Check current shell:

```bash
echo $SHELL
```

---

# Creating a Script

Create a file:

```bash
nano hello.sh
```

Example:

```bash
#!/bin/bash

echo "Hello Linux"
```

---

# Making Script Executable

```bash
chmod +x hello.sh
```

Run:

```bash
./hello.sh
```

---

# Variables

Example:

```bash
name="Nanditha"

echo $name
```

---

# User Input

```bash
read name

echo "Hello $name"
```

---

# Conditional Statements

```bash
if [ $age -ge 18 ]
then
echo "Adult"
else
echo "Minor"
fi
```

---

# Loops

For Loop

```bash
for i in {1..5}
do
echo $i
done
```

While Loop

```bash
while true
do
echo "Running"
break
done
```

---

# Comments

```bash
# This is a comment
```

---

# Common Uses

- Backup Scripts
- Log Cleanup
- User Creation
- Server Monitoring
- Automation

---

# Best Practices

- Write readable scripts.
- Add comments.
- Test scripts before deployment.
- Use meaningful variable names.

---

# 📌 Key Takeaways

- Shell Scripts automate Linux tasks.
- Bash is the default Linux shell.
- Variables store values.
- Loops repeat tasks.
- Scripts improve productivity.

---

# ❓ Interview Questions

### 1. What is Shell Scripting?

Writing Linux commands into executable script files.

### 2. What is Bash?

The default Linux shell.

### 3. Which command makes a script executable?

chmod +x

### 4. Which line starts every Bash script?

#!/bin/bash

### 5. Why use Shell Scripts?

To automate repetitive tasks.

---

# 📝 Summary

Today I learned about Shell Scripting, Bash, variables, loops, conditional statements, and automation. Shell scripting is an essential skill for Linux administrators, DevOps engineers, and cloud professionals.
