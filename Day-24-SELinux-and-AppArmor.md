# Day 24: SELinux & AppArmor

> Understanding SELinux, AppArmor, Mandatory Access Control (MAC), security policies, and application confinement.

---

# 🎯 Learning Objectives

- Understand SELinux.
- Learn AppArmor.
- Explore Mandatory Access Control.
- Understand Security Policies.
- Prepare for Linux interviews.

---

# 📖 Introduction

Traditional Linux permissions are sometimes insufficient to protect critical systems.

SELinux and AppArmor provide an additional layer of security by restricting what applications can do.

---

# What is SELinux?

SELinux (Security-Enhanced Linux) is a Mandatory Access Control (MAC) system.

It restricts processes even if they have normal Linux permissions.

---

# What is Mandatory Access Control (MAC)?

MAC enforces security policies defined by the operating system.

Unlike traditional permissions, users cannot easily bypass these policies.

---

# SELinux Modes

## Enforcing

Security policies are enforced.

---

## Permissive

Violations are logged but not blocked.

---

## Disabled

SELinux is turned off.

---

# Check SELinux Status

```bash
getenforce
```

Detailed information:

```bash
sestatus
```

---

# What is AppArmor?

AppArmor provides application-level security using profiles.

Applications are restricted to only the resources they need.

---

# AppArmor Features

- Application Isolation
- Profile-Based Security
- Easy Configuration
- Lightweight

---

# SELinux vs AppArmor

| SELinux | AppArmor |
|----------|-----------|
| Label-Based | Path-Based |
| More Powerful | Easier to Configure |
| Common in RHEL | Common in Ubuntu |

---

# Benefits

- Better Security
- Prevents Privilege Escalation
- Limits Malware Impact
- Protects Sensitive Data

---

# Best Practices

- Keep SELinux enabled.
- Review security logs.
- Update security policies.
- Test applications before deployment.

---

# 📌 Key Takeaways

- SELinux uses Mandatory Access Control.
- AppArmor secures applications using profiles.
- Both improve Linux security.
- They reduce attack impact.

---

# ❓ Interview Questions

### 1. What is SELinux?

A Mandatory Access Control security framework.

### 2. What is AppArmor?

A profile-based application security framework.

### 3. Name the three SELinux modes.

- Enforcing
- Permissive
- Disabled

### 4. Which Linux distribution commonly uses AppArmor?

Ubuntu.

### 5. Why use SELinux?

To provide stronger security beyond standard Linux permissions.

---

# 📝 Summary

Today I learned about SELinux, AppArmor, Mandatory Access Control, security policies, and application isolation. These technologies provide advanced protection for Linux systems by limiting what applications can access.
