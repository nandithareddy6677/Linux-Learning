# Day 21: User Administration & sudo

> Understanding Linux user administration, account management, groups, password management, sudo privileges, and administrative access.

---

# 🎯 Learning Objectives

- Manage Users.
- Manage Groups.
- Learn sudo.
- Secure User Accounts.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux allows multiple users to work on the same system securely.

Administrators manage user accounts, permissions, and privileges.

---

# Create User

```bash
sudo adduser john
```

or

```bash
sudo useradd john
```

---

# Delete User

```bash
sudo userdel john
```

---

# Change Password

```bash
passwd john
```

---

# View Current User

```bash
whoami
```

---

# Display User Information

```bash
id john
```

---

# Groups

Create group:

```bash
groupadd developers
```

Add user:

```bash
usermod -aG developers john
```

---

# What is sudo?

sudo allows a regular user to execute commands with administrative privileges.

Example:

```bash
sudo apt update
```

---

# sudo Benefits

- Better Security
- Accountability
- Reduced Root Usage

---

# User Account Files

```
/etc/passwd

/etc/shadow

/etc/group
```

---

# Lock User

```bash
passwd -l john
```

---

# Unlock User

```bash
passwd -u john
```

---

# Best Practices

- Use sudo instead of Root.
- Apply Least Privilege.
- Disable inactive accounts.
- Use strong passwords.

---

# 📌 Key Takeaways

- adduser creates users.
- userdel removes users.
- sudo grants temporary admin access.
- Groups simplify permission management.
- User information is stored in /etc.

---

# ❓ Interview Questions

### 1. What does sudo do?

Allows users to execute administrative commands.

### 2. Which file stores user information?

/etc/passwd

### 3. Which file stores encrypted passwords?

/etc/shadow

### 4. Which command displays the current user?

whoami

### 5. Which command creates a new user?

adduser

---

# 📝 Summary

Today I learned about Linux user administration, groups, password management, sudo, and account security. Proper user management is essential for maintaining secure Linux systems.
