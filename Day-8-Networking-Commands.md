# Day 8: Networking Commands

> Understanding essential Linux networking commands used to troubleshoot, monitor, and manage network connectivity.

---

# 🎯 Learning Objectives

- Understand basic Linux networking.
- Learn important networking commands.
- Verify network connectivity.
- Diagnose network issues.
- Learn IP configuration commands.
- Understand DNS lookup tools.
- Explore real-world networking scenarios.

---

# 📖 Introduction

Networking is one of the most important aspects of Linux. Whether you're a System Administrator, Cloud Engineer, DevOps Engineer, or Cybersecurity Professional, you'll frequently work with Linux networking commands.

Linux provides powerful command-line tools that help users monitor, troubleshoot, and configure networks efficiently.

---

# 🌐 What is Networking?

Networking is the process of connecting computers and devices so they can communicate and share resources.

Examples include:

- Browsing websites
- Sending emails
- Video conferencing
- File sharing
- Cloud computing

Linux provides several built-in commands to monitor and troubleshoot these connections.

---

# IP Address

An IP Address (Internet Protocol Address) is a unique identifier assigned to every device connected to a network.

Example:

```
192.168.1.10
```

Types:

- IPv4
- IPv6

---

# Viewing Network Configuration

## ip

The `ip` command is the modern tool for displaying and configuring network interfaces.

Display IP addresses:

```bash
ip addr
```

Display routing table:

```bash
ip route
```

Display network interfaces:

```bash
ip link
```

---

## ifconfig

`ifconfig` is an older networking command used to display and configure network interfaces.

```bash
ifconfig
```

Although still available on many systems, the `ip` command is recommended because it is more powerful and actively maintained.

---

# ping

The `ping` command checks whether another system is reachable over the network.

Syntax:

```bash
ping google.com
```

Example Output:

```
64 bytes from google.com
```

Purpose:

- Test Internet connectivity
- Measure response time
- Verify remote server availability

Stop Ping:

```
Ctrl + C
```

---

# traceroute

The `traceroute` command shows the path packets take from your computer to a destination.

Example:

```bash
traceroute google.com
```

Uses:

- Diagnose routing problems
- Identify slow network paths
- Troubleshoot connectivity issues

---

# hostname

Displays the computer's hostname.

```bash
hostname
```

Example Output:

```
ubuntu-server
```

---

# nslookup

Queries DNS servers to obtain domain information.

Example:

```bash
nslookup google.com
```

Displays:

- IP Address
- DNS Server
- Domain Information

---

# dig

`dig` (Domain Information Groper) provides detailed DNS information.

Example:

```bash
dig google.com
```

Useful for:

- DNS troubleshooting
- Domain verification
- DNS record lookup

---

# curl

Transfers data between systems using URLs.

Example:

```bash
curl https://google.com
```

Common Uses:

- Test APIs
- Download webpage content
- Check HTTP responses

---

# wget

Downloads files from the Internet.

Example:

```bash
wget https://example.com/file.zip
```

Features:

- Resume downloads
- Download websites
- Download large files

---

# netstat

Displays network statistics and active connections.

Example:

```bash
netstat -tuln
```

Shows:

- Listening Ports
- Active Connections
- Routing Information

Although still widely used, `ss` is now the recommended replacement.

---

# ss

Displays socket statistics.

Example:

```bash
ss -tuln
```

Advantages:

- Faster than netstat
- More detailed information
- Modern Linux utility

---

# arp

Displays the Address Resolution Protocol (ARP) table.

Example:

```bash
arp -a
```

Shows:

- IP Address
- MAC Address
- Connected Devices

---

# Route

Displays the routing table.

Example:

```bash
route
```

Shows:

- Default Gateway
- Network Routes
- Interface Information

---

# Important Networking Commands Summary

| Command | Purpose |
|----------|---------|
| ip | Display and configure network interfaces |
| ifconfig | Display network configuration |
| ping | Test network connectivity |
| traceroute | Show packet path |
| hostname | Display system hostname |
| nslookup | Query DNS information |
| dig | Detailed DNS lookup |
| curl | Transfer data from URLs |
| wget | Download files |
| netstat | Display network connections |
| ss | Display socket statistics |
| arp | Display ARP table |
| route | Display routing table |

---

# 🌍 Real-Life Example

A company's web server suddenly becomes unreachable.

The Linux administrator performs the following steps:

1. Uses `ping` to check connectivity.
2. Runs `traceroute` to identify where the connection fails.
3. Uses `ip addr` to verify the server's IP address.
4. Checks listening ports using `ss -tuln`.
5. Confirms DNS records using `dig`.

Within a few minutes, the administrator identifies the issue and restores connectivity.

---

# 💡 Best Practices

- Learn both `ip` and `ifconfig`.
- Use `ss` instead of `netstat` on modern systems.
- Verify DNS before troubleshooting applications.
- Use `ping` as the first connectivity test.
- Keep networking tools updated.
- Monitor active ports regularly.

---

# 📌 Key Takeaways

- Linux provides powerful networking tools.
- `ip` is the modern replacement for `ifconfig`.
- `ping` tests network connectivity.
- `traceroute` shows packet routes.
- `curl` and `wget` transfer data.
- `dig` and `nslookup` troubleshoot DNS.
- `ss` displays active network connections.
- Networking commands are essential for Linux, Cloud, DevOps, and Cybersecurity professionals.

---

# ❓ Interview Questions

### 1. What is the purpose of the `ip` command?

The `ip` command is used to display and configure network interfaces, IP addresses, and routing information.

---

### 2. What is the difference between `ip` and `ifconfig`?

`ifconfig` is an older networking tool, while `ip` is the modern and recommended replacement with more advanced features.

---

### 3. What does the `ping` command do?

It checks network connectivity by sending ICMP Echo Requests to a remote host.

---

### 4. What is `traceroute` used for?

It shows the path that network packets take from the source to the destination.

---

### 5. What is the purpose of `curl`?

`curl` transfers data between systems using URLs and is commonly used for testing APIs and downloading webpage content.

---

### 6. What is the difference between `wget` and `curl`?

`wget` is mainly used for downloading files, whereas `curl` is more flexible for transferring data and interacting with APIs.

---

### 7. What is the purpose of `dig`?

`dig` performs detailed DNS lookups and helps troubleshoot DNS-related issues.

---

### 8. Why is `ss` preferred over `netstat`?

`ss` is faster, provides more detailed information, and is the recommended modern replacement for `netstat`.

---

# 📝 Summary

Today I learned about Linux Networking Commands, which are essential for troubleshooting and managing network connections. I explored commands such as `ip`, `ifconfig`, `ping`, `traceroute`, `hostname`, `nslookup`, `dig`, `curl`, `wget`, `netstat`, `ss`, `arp`, and `route`. These tools help diagnose connectivity problems, monitor active connections, verify DNS records, and manage Linux network configurations.
