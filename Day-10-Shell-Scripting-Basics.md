# Day 10: Shell Scripting Basics

> Understanding Shell Scripting, Bash fundamentals, variables, conditions, loops, functions, and automation in Linux.

---

# 🎯 Learning Objectives

- Understand Shell Scripting.
- Learn what Bash is.
- Write your first Shell Script.
- Understand Variables.
- Learn User Input.
- Understand Conditional Statements.
- Learn Loops.
- Understand Functions.
- Learn Shell Scripting Best Practices.

---

# 📖 Introduction

Linux allows users to automate repetitive tasks using Shell Scripts.

Instead of typing multiple commands repeatedly, we can write them into a script and execute them whenever needed.

Shell Scripting is one of the most valuable skills for:

- Linux Administrators
- Cloud Engineers
- DevOps Engineers
- Cybersecurity Professionals

Automation saves time, reduces human errors, and increases productivity.

---

# 🐚 What is a Shell?

A Shell is a command-line interpreter that acts as a bridge between the user and the Linux operating system.

It receives commands from the user and passes them to the Linux kernel for execution.

Popular Linux Shells include:

- Bash (Bourne Again Shell)
- Zsh
- Fish
- Ksh
- Tcsh

Among these, **Bash** is the most commonly used shell.

---

# What is Bash?

Bash (Bourne Again SHell) is the default shell for most Linux distributions.

Features:

- Command execution
- Automation
- Variables
- Loops
- Functions
- Scripting

Most Linux automation tasks are written using Bash.

---

# What is a Shell Script?

A Shell Script is a text file containing a sequence of Linux commands.

Instead of entering commands one by one, the operating system executes all commands in the script automatically.

Shell scripts usually have the extension:

```
.sh
```

Example:

```
backup.sh
```

---

# Creating Your First Shell Script

Create a new file:

```bash
nano hello.sh
```

Add the following code:

```bash
#!/bin/bash

echo "Hello, Linux!"
```

Save the file.

Give execute permission:

```bash
chmod +x hello.sh
```

Run the script:

```bash
./hello.sh
```

Output:

```
Hello, Linux!
```

---

# Shebang (#!)

The first line of a shell script is called the **Shebang**.

Example:

```bash
#!/bin/bash
```

It tells Linux which interpreter should execute the script.

---

# Variables

Variables store data.

Example:

```bash
name="Nanditha"

echo $name
```

Output:

```
Nanditha
```

Variables make scripts flexible and reusable.

---

# User Input

The `read` command accepts input from the user.

Example:

```bash
echo "Enter your name:"

read name

echo "Welcome $name"
```

Output:

```
Enter your name:

Nanditha

Welcome Nanditha
```

---

# Comments

Comments improve readability.

Single-line comment:

```bash
# This is a comment
```

Comments are ignored during execution.

---

# Conditional Statements

Linux uses the `if` statement to make decisions.

Example:

```bash
age=20

if [ $age -ge 18 ]

then

echo "Adult"

fi
```

Output:

```
Adult
```

---

# If-Else Statement

Example:

```bash
marks=70

if [ $marks -ge 35 ]

then

echo "Pass"

else

echo "Fail"

fi
```

---

# Loops

Loops execute commands repeatedly.

## For Loop

Example:

```bash
for i in 1 2 3 4 5

do

echo $i

done
```

Output:

```
1

2

3

4

5
```

---

## While Loop

Example:

```bash
count=1

while [ $count -le 5 ]

do

echo $count

count=$((count+1))

done
```

---

# Functions

Functions help organize code.

Example:

```bash
greet(){

echo "Welcome to Linux"

}

greet
```

Output:

```
Welcome to Linux
```

---

# Exit Status

Linux commands return an Exit Status.

```
0

↓

Success
```

```
Non-zero

↓

Failure
```

Check exit status:

```bash
echo $?
```

---

# Useful Shell Script Commands

Print text

```bash
echo
```

Read input

```bash
read
```

Display current directory

```bash
pwd
```

List files

```bash
ls
```

Current user

```bash
whoami
```

Current date

```bash
date
```

---

# Practical Example

Backup Script

```bash
#!/bin/bash

echo "Starting Backup..."

cp -r Documents Backup

echo "Backup Completed."
```

This script copies the Documents folder into a Backup directory automatically.

---

# Real-World Uses of Shell Scripting

Shell scripting is commonly used for:

- System Administration
- Automated Backups
- Log Monitoring
- User Management
- Software Installation
- Server Maintenance
- Security Audits
- Cloud Automation

---

# 💡 Best Practices

- Add comments to improve readability.
- Use meaningful variable names.
- Test scripts before deployment.
- Handle errors properly.
- Avoid running scripts as Root unless necessary.
- Keep scripts simple and modular.
- Use functions to organize large scripts.

---

# 📌 Key Takeaways

- Bash is the default shell in most Linux distributions.
- Shell Scripts automate repetitive tasks.
- Variables store data.
- `read` accepts user input.
- `if` statements make decisions.
- Loops repeat tasks.
- Functions organize code.
- Shell scripting is widely used in Linux administration, DevOps, Cloud Computing, and Cybersecurity.

---

# ❓ Interview Questions

### 1. What is a Shell?

A Shell is a command-line interpreter that allows users to interact with the Linux operating system.

---

### 2. What is Bash?

Bash (Bourne Again SHell) is the default command-line shell used in most Linux distributions.

---

### 3. What is a Shell Script?

A Shell Script is a file containing Linux commands that are executed sequentially.

---

### 4. What is the purpose of the Shebang?

The Shebang (`#!/bin/bash`) specifies which interpreter should execute the script.

---

### 5. Which command gives execute permission to a script?

```bash
chmod +x filename.sh
```

---

### 6. How do you run a shell script?

```bash
./filename.sh
```

---

### 7. What does the `read` command do?

It accepts input from the user.

---

### 8. What is the purpose of Functions in Shell Scripting?

Functions organize code into reusable blocks, making scripts easier to manage and maintain.

---

# 📝 Summary

Today I learned the fundamentals of Shell Scripting using Bash. I explored how to create and execute shell scripts, use variables, accept user input, write conditional statements, use loops and functions, and automate repetitive Linux tasks. Shell scripting is an essential skill for Linux Administration, Cloud Computing, DevOps, and Cybersecurity because it enables efficient automation and system management.
