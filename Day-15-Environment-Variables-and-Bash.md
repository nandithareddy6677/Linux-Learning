# Day 15: Environment Variables & Bash

> Understanding Linux environment variables, Bash configuration files, PATH, aliases, and shell customization.

---

# 🎯 Learning Objectives

- Understand Environment Variables.
- Learn PATH.
- Explore Bash Configuration Files.
- Create Aliases.
- Customize the Linux Shell.

---

# 📖 Introduction

Linux stores important system information inside Environment Variables.

Applications use these variables to locate files, executables, and user settings.

---

# 🌍 What are Environment Variables?

Environment Variables are named values used by Linux programs.

Examples:

- HOME
- PATH
- USER
- SHELL
- HOSTNAME

---

# Viewing Variables

Display all:

```bash
printenv
```

Single variable:

```bash
echo $HOME
```

---

# PATH Variable

PATH stores directories searched for executable programs.

View:

```bash
echo $PATH
```

---

# Creating Variables

```bash
city="Hyderabad"

echo $city
```

---

# Export Variables

```bash
export PROJECT=Cloud
```

---

# Bash Configuration Files

User Configuration

```
~/.bashrc
```

System Configuration

```
/etc/profile
```

---

# Aliases

Create shortcut commands.

Example:

```bash
alias ll="ls -la"
```

Remove:

```bash
unalias ll
```

---

# Reload Bash

```bash
source ~/.bashrc
```

---

# Best Practices

- Keep PATH clean.
- Store custom aliases in .bashrc.
- Avoid duplicate variables.
- Secure sensitive environment variables.

---

# 📌 Key Takeaways

- Environment Variables store system information.
- PATH locates executable programs.
- .bashrc customizes Bash.
- Aliases simplify commands.

---

# ❓ Interview Questions

### 1. What is PATH?

A variable containing directories searched for executable programs.

### 2. Which file stores user Bash settings?

.bashrc

### 3. What does source ~/.bashrc do?

Reloads Bash configuration.

### 4. What is an alias?

A shortcut for a command.

### 5. Which command displays environment variables?

printenv

---

# 📝 Summary

Today I learned about Environment Variables, PATH, Bash configuration, aliases, and shell customization. These features make Linux more efficient and easier to use in daily administration.
