# Day 4: File Permissions and Ownership

> Understanding Linux file permissions, ownership, and access control to secure files and directories.

---

# 🎯 Learning Objectives

- Understand Linux file permissions.
- Learn about file ownership.
- Understand users, groups, and others.
- Learn symbolic and numeric permissions.
- Master chmod, chown, and chgrp commands.
- Learn Linux permission best practices.

---

# 📖 Introduction

Linux is a multi-user operating system where multiple users can access the same computer simultaneously. To protect files and maintain security, Linux uses a powerful permission system.

Every file and directory has an owner and specific permissions that determine who can read, modify, or execute it.

Understanding permissions is one of the most important Linux skills for System Administrators, Cloud Engineers, and Cybersecurity Professionals.

---

# 🔒 What are File Permissions?

File permissions define who can access a file and what actions they can perform.

Permissions determine whether a user can:

- Read a file
- Modify a file
- Execute a file

These permissions help prevent unauthorized access.

---

# 👤 File Ownership

Every file in Linux has:

- Owner (User)
- Group
- Others

### Owner (User)

The person who created the file.

---

### Group

A collection of users who share similar permissions.

---

### Others

Everyone else on the system.

---

# Permission Types

Linux has three basic permissions.

## 1. Read (r)

Allows viewing the contents of a file.

For directories:

Allows listing files inside the directory.

---

## 2. Write (w)

Allows modifying or deleting a file.

For directories:

Allows creating or deleting files inside the directory.

---

## 3. Execute (x)

Allows running a program or script.

For directories:

Allows entering the directory using the `cd` command.

---

# Understanding Permission Representation

Example:

```text
-rwxr-xr--
```

Breakdown:

```text
-
rwx
r-x
r--
```

The first character indicates the file type.

| Symbol | Meaning |
|---------|----------|
| - | Regular File |
| d | Directory |
| l | Symbolic Link |

---

Owner Permissions

```text
rwx
```

Read

Write

Execute

---

Group Permissions

```text
r-x
```

Read

Execute

No Write permission.

---

Others Permissions

```text
r--
```

Read only.

---

# Viewing File Permissions

Command:

```bash
ls -l
```

Example Output:

```bash
-rwxr-xr-- 1 nanditha users 1024 Jul 12 notes.txt
```

Explanation:

- File Type
- Permissions
- Number of Links
- Owner
- Group
- File Size
- Date
- File Name

---

# Numeric (Octal) Permissions

Linux also represents permissions using numbers.

| Permission | Value |
|------------|-------|
| Read | 4 |
| Write | 2 |
| Execute | 1 |

Examples:

| Number | Meaning |
|----------|---------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

---

Example

```bash
chmod 755 file.txt
```

Meaning:

Owner:

7 = rwx

Group:

5 = r-x

Others:

5 = r-x

---

Another Example

```bash
chmod 644 notes.txt
```

Owner

rw-

Group

r--

Others

r--

---

# Symbolic Permissions

Instead of numbers, Linux also supports symbolic notation.

| Symbol | Meaning |
|---------|----------|
| u | User (Owner) |
| g | Group |
| o | Others |
| a | All Users |

Examples

Add Execute Permission

```bash
chmod +x script.sh
```

Remove Write Permission

```bash
chmod g-w file.txt
```

Give Read Permission

```bash
chmod o+r file.txt
```

---

# chmod Command

The chmod command changes file permissions.

Syntax

```bash
chmod permissions filename
```

Examples

```bash
chmod 755 script.sh
```

```bash
chmod 644 notes.txt
```

```bash
chmod +x install.sh
```

---

# chown Command

Changes the owner of a file.

Syntax

```bash
sudo chown username filename
```

Example

```bash
sudo chown nanditha report.txt
```

Now

Owner becomes:

nanditha

---

# chgrp Command

Changes the group ownership.

Syntax

```bash
sudo chgrp developers report.txt
```

Now

Group becomes:

developers

---

# Recursive Permissions

Sometimes permissions need to be changed for an entire directory.

Use:

```bash
chmod -R 755 Projects/
```

The `-R` option means Recursive.

Every file and folder inside Projects will receive new permissions.

---

# Default File Permissions

Linux automatically assigns permissions.

Default File

```text
rw-r--r--
```

Equivalent:

```text
644
```

Default Directory

```text
rwxr-xr-x
```

Equivalent:

```text
755
```

---

# 🌍 Real-Life Example

A company stores employee salary information.

Permissions are set as:

Owner:

HR Manager

Group:

HR Team

Others:

No Access

Only HR staff can view or modify salary files, protecting confidential information.

---

# 💡 Best Practices

- Follow the Principle of Least Privilege.
- Never give unnecessary write permissions.
- Use 755 for most directories.
- Use 644 for normal files.
- Avoid using 777 unless absolutely necessary.
- Regularly review file permissions.
- Use groups to manage access efficiently.

---

# 📌 Key Takeaways

- Every Linux file has an Owner, Group, and Others.
- Linux permissions include Read, Write, and Execute.
- Permissions can be represented symbolically or numerically.
- chmod changes permissions.
- chown changes ownership.
- chgrp changes group ownership.
- Proper permissions improve system security.

---

# ❓ Interview Questions

### 1. What are Linux file permissions?

Linux file permissions determine who can read, write, or execute files and directories.

---

### 2. What does chmod do?

The chmod command changes file or directory permissions.

---

### 3. What does chown do?

The chown command changes the owner of a file or directory.

---

### 4. What does chgrp do?

The chgrp command changes the group ownership of a file or directory.

---

### 5. What does permission 755 mean?

Owner:

Read, Write, Execute

Group:

Read, Execute

Others:

Read, Execute

---

### 6. What does permission 644 mean?

Owner:

Read, Write

Group:

Read

Others:

Read

---

### 7. Why should we avoid using 777 permissions?

Because it grants Read, Write, and Execute permissions to everyone, creating serious security risks.

---

# 📝 Summary

Today I learned about Linux File Permissions and Ownership. I explored how Linux controls access using Owners, Groups, and Others, understood Read, Write, and Execute permissions, learned symbolic and numeric permission formats, and practiced using important commands such as `chmod`, `chown`, and `chgrp`. Proper permission management is essential for maintaining Linux system security.
