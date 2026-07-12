# Day 5: Users and Groups

> Understanding how Linux manages users, groups, permissions, and administrative privileges to maintain a secure multi-user environment.

---

# 🎯 Learning Objectives

- Understand Linux Users and Groups.
- Learn different types of users.
- Understand the Root user.
- Learn how Linux manages user accounts.
- Master common user management commands.
- Understand group management.
- Learn about sudo privileges.
- Explore Linux security best practices.

---

# 📖 Introduction

Linux is a multi-user operating system, which means multiple users can work on the same system simultaneously.

Each user has their own:

- Username
- Password
- Home Directory
- Permissions
- Files

This ensures users work independently while maintaining system security.

---

# 👤 What is a User?

A User is an account that allows a person or service to access the Linux system.

Every user has:

- Username
- User ID (UID)
- Home Directory
- Login Shell
- Password

Example:

```
nanditha
```

is a user account.

---

# Types of Users

Linux mainly has three types of users.

## 1. Root User

The Root user is the superuser of Linux.

Characteristics:

- UID = 0
- Full system access
- Can modify any file
- Can install software
- Can manage users
- Can change system settings

Example:

```
root
```

The Root user should only be used for administrative tasks.

---

## 2. Regular User

A Regular User is created for daily activities.

Characteristics:

- Limited permissions
- Cannot modify system files
- Cannot install software without permission

Example:

```
nanditha
```

---

## 3. System User

System users are created automatically for running services and applications.

Examples:

- mysql
- nginx
- www-data
- nobody

They are generally not used for logging in.

---

# What is a Group?

A Group is a collection of users.

Groups make permission management easier.

Instead of assigning permissions to every user individually, administrators assign permissions to a group.

Example:

```
Developers
```

Users:

- Rahul
- Priya
- Nanditha

All members inherit the group's permissions.

---

# Primary Group

Every user has one Primary Group.

It is assigned when the user account is created.

Example:

```
User

↓

Primary Group

↓

nanditha
```

---

# Secondary Groups

A user can belong to multiple additional groups.

Example:

```
Developers

HR

Docker

Cloud-Team
```

This allows users to access multiple shared resources.

---

# User IDs (UID)

Each user has a unique User ID.

Examples:

| UID | Description |
|------|-------------|
| 0 | Root User |
| 1–999 | System Users |
| 1000+ | Regular Users |

Linux internally identifies users using the UID instead of the username.

---

# Group IDs (GID)

Each group also has a unique Group ID (GID).

Linux uses GIDs to identify groups internally.

---

# Home Directory

Each regular user has a Home Directory.

Example:

```
/home/nanditha
```

This directory stores:

- Documents
- Downloads
- Desktop Files
- Personal Configurations

---

# Important User Management Commands

## whoami

Displays the currently logged-in user.

```bash
whoami
```

Example Output:

```bash
nanditha
```

---

## id

Displays user and group information.

```bash
id
```

Example Output:

```bash
uid=1000(nanditha)
gid=1000(nanditha)
groups=1000(nanditha),27(sudo)
```

---

## who

Shows users currently logged into the system.

```bash
who
```

---

## users

Displays currently logged-in users.

```bash
users
```

---

## passwd

Changes the user's password.

```bash
passwd
```

---

## useradd

Creates a new user.

```bash
sudo useradd john
```

---

## adduser

Creates a new user interactively.

```bash
sudo adduser john
```

The system asks for:

- Password
- Full Name
- Phone Number
- Other details

---

## userdel

Deletes a user account.

```bash
sudo userdel john
```

Delete user with Home Directory:

```bash
sudo userdel -r john
```

---

## usermod

Modifies an existing user.

Example:

Add user to sudo group.

```bash
sudo usermod -aG sudo john
```

---

# Group Management Commands

## groupadd

Creates a new group.

```bash
sudo groupadd developers
```

---

## groupdel

Deletes a group.

```bash
sudo groupdel developers
```

---

## groups

Shows the groups a user belongs to.

```bash
groups
```

---

# What is sudo?

sudo stands for:

**Super User DO**

It allows a regular user to execute administrative commands.

Example:

```bash
sudo apt update
```

Instead of logging in as Root, Linux recommends using sudo.

Advantages:

- Better security
- Prevents accidental system damage
- Logs administrative actions

---

# Difference Between Root and sudo

| Root | sudo |
|------|------|
| Full-time administrator | Temporary administrative access |
| Unlimited permissions | Only for specific commands |
| Less secure for daily use | Recommended approach |

---

# User Account Files

Linux stores user information in important files.

## /etc/passwd

Contains user account details.

Example:

```
cat /etc/passwd
```

---

## /etc/shadow

Stores encrypted passwords.

Only Root can access it.

Example:

```
sudo cat /etc/shadow
```

---

## /etc/group

Contains group information.

Example:

```
cat /etc/group
```

---

# 🌍 Real-Life Example

A software company has three departments:

- Developers
- HR
- Finance

Each department has its own Linux group.

Employees receive access based on their group membership.

A developer cannot access HR salary files, while HR staff cannot modify application source code.

This improves security and simplifies permission management.

---

# 💡 Best Practices

- Use Regular User accounts for daily work.
- Avoid logging in as Root.
- Use sudo only when necessary.
- Assign permissions through groups.
- Remove inactive user accounts.
- Use strong passwords.
- Review user accounts regularly.

---

# 📌 Key Takeaways

- Linux is a multi-user operating system.
- Every user has a unique UID.
- Groups simplify permission management.
- Root has unrestricted access.
- sudo provides temporary administrative privileges.
- User information is stored in /etc/passwd.
- Passwords are stored securely in /etc/shadow.

---

# ❓ Interview Questions

### 1. What is a Linux User?

A Linux User is an account that allows access to the operating system.

---

### 2. What is the Root User?

The Root User is the superuser with complete administrative control over the system.

---

### 3. What is a Group?

A Group is a collection of users who share common permissions.

---

### 4. What is sudo?

sudo allows a regular user to execute commands with administrative privileges.

---

### 5. Difference between Root and sudo?

Root has permanent administrative access, while sudo grants temporary administrative privileges for specific commands.

---

### 6. Which file stores user account information?

```
/etc/passwd
```

---

### 7. Which file stores encrypted passwords?

```
/etc/shadow
```

---

### 8. Which command creates a new user?

```bash
sudo useradd username
```

or

```bash
sudo adduser username
```

---

# 📝 Summary

Today I learned how Linux manages users and groups in a secure multi-user environment. I explored different types of users, understood the importance of the Root user, learned how groups simplify permission management, and practiced essential commands such as `whoami`, `id`, `useradd`, `userdel`, `groupadd`, `groups`, and `sudo`. I also learned how Linux stores user and password information in system files like `/etc/passwd`, `/etc/shadow`, and `/etc/group`.
