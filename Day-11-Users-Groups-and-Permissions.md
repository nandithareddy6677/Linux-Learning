# Day 11: Users, Groups & File Permissions

> Understanding Linux users, groups, ownership, file permissions, chmod, chown, and access control.

---

# 🎯 Learning Objectives

- Understand Linux Users.
- Learn Groups.
- Understand File Ownership.
- Learn File Permissions.
- Use chmod and chown.
- Prepare for Linux interviews.

---

# 📖 Introduction

Linux is a multi-user operating system.

Every user has specific permissions that determine which files and directories they can access or modify.

Proper permission management improves system security.

---

# 👤 Linux Users

Linux supports multiple users.

Common user types:

- Root User
- Regular User
- System User

---

# Root User

The Root User has complete administrative privileges.

Example:

```
root
```

Root can:

- Install software
- Create users
- Delete files
- Change permissions

---

# Groups

Groups allow multiple users to share permissions.

Example:

```
Developers

↓

Alice

Bob

Charlie
```

---

# File Ownership

Every file has:

- Owner (User)
- Group
- Others

View ownership:

```bash
ls -l
```

---

# File Permissions

Linux permissions:

- Read (r)
- Write (w)
- Execute (x)

Displayed as:

```
-rwxr-xr--
```

---

# Permission Breakdown

```
Owner

↓

rwx

Group

↓

r-x

Others

↓

r--
```

---

# chmod

Changes permissions.

Example:

```bash
chmod 755 file.txt
```

---

# Numeric Permissions

| Number | Permission |
|---------|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |

---

# chown

Changes ownership.

Example:

```bash
sudo chown alice file.txt
```

---

# chgrp

Changes group ownership.

```bash
sudo chgrp developers file.txt
```

---

# Best Practices

- Apply Least Privilege.
- Avoid using Root unnecessarily.
- Regularly review permissions.
- Secure sensitive files.

---

# 📌 Key Takeaways

- Linux supports multiple users.
- Every file has an owner and a group.
- chmod changes permissions.
- chown changes ownership.
- Proper permissions improve security.

---

# ❓ Interview Questions

### 1. What are Linux file permissions?

Read, Write, and Execute permissions.

### 2. What does chmod do?

Changes file permissions.

### 3. What does chown do?

Changes file ownership.

### 4. What is the Root user?

The administrator with full system access.

### 5. Which command displays permissions?

ls -l

---

# 📝 Summary

Today I learned about Linux users, groups, file ownership, permissions, chmod, chown, and how Linux controls access to files and directories.
