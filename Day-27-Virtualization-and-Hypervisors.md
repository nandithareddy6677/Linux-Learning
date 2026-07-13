# Day 27: Virtualization & Hypervisors

> Understanding virtualization, hypervisors, virtual machines, KVM, VMware, VirtualBox, and virtualization in cloud computing.

---

# 🎯 Learning Objectives

- Understand Virtualization.
- Learn Hypervisors.
- Explore Virtual Machines.
- Compare VMs and Containers.
- Prepare for Cloud interviews.

---

# 📖 Introduction

Before cloud computing became popular, organizations relied on virtualization to maximize hardware utilization.

Virtualization allows multiple operating systems to run on a single physical machine.

---

# 💻 What is Virtualization?

Virtualization creates virtual versions of physical computing resources.

Examples:

- Virtual Machines
- Virtual Networks
- Virtual Storage

---

# Virtual Machine (VM)

A VM is a software-based computer with its own:

- Operating System
- CPU
- RAM
- Storage

---

# What is a Hypervisor?

A Hypervisor manages Virtual Machines.

It allocates CPU, RAM, and storage.

---

# Types of Hypervisors

## Type 1

Runs directly on hardware.

Examples:

- VMware ESXi
- Microsoft Hyper-V
- Xen

---

## Type 2

Runs on top of an operating system.

Examples:

- VirtualBox
- VMware Workstation

---

# KVM

Kernel-based Virtual Machine (KVM) is the built-in virtualization solution for Linux.

---

# Virtualization vs Containers

| Virtual Machines | Containers |
|------------------|------------|
| Full Operating System | Shared Host Kernel |
| Higher Resource Usage | Lightweight |
| Slower Startup | Faster Startup |
| Strong Isolation | Efficient Resource Sharing |

---

# Virtualization in Cloud Computing

Cloud providers build services on virtualization technologies.

Examples:

- AWS EC2
- Azure Virtual Machines
- Google Compute Engine

---

# Benefits

- Better Hardware Utilization
- Isolation
- Scalability
- Cost Savings
- Disaster Recovery

---

# 🌍 Real-Life Example

A company hosts multiple Linux servers on a single physical machine using KVM, reducing hardware costs while maintaining isolated environments.

---

# 💡 Best Practices

- Allocate resources appropriately.
- Keep hypervisors updated.
- Monitor VM performance.
- Snapshot VMs before major changes.

---

# 📌 Key Takeaways

- Virtualization enables multiple VMs.
- Hypervisors manage VMs.
- KVM is Linux's virtualization technology.
- Containers are lighter than VMs.

---

# ❓ Interview Questions

### 1. What is Virtualization?

Running multiple virtual systems on one physical machine.

### 2. What is a Hypervisor?

Software that creates and manages Virtual Machines.

### 3. Difference between Type 1 and Type 2 Hypervisors?

Type 1 runs on hardware; Type 2 runs on an operating system.

### 4. What is KVM?

Kernel-based Virtual Machine for Linux.

### 5. Difference between Containers and VMs?

Containers share the host kernel, while VMs have separate operating systems.

---

# 📝 Summary

Today I learned about Virtualization, Hypervisors, Virtual Machines, KVM, VMware, VirtualBox, and how virtualization forms the foundation of modern cloud computing.
