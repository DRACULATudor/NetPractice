# NetPractice Project Notes

## Overview
**NetPractice** is a project focused on understanding and configuring network devices based on IP addressing and subnet masks. The goal is to apply networking principles to solve practical scenarios.

## Key Concepts

### 1. **IP Addressing**
- IPv4 addresses consist of 32 bits, divided into 4 octets (e.g., `192.168.1.1`).
- Each address has a **network portion** and a **host portion** determined by the subnet mask.

### 2. **Subnetting**
- A subnet mask defines how many bits are used for the network and how many for hosts.
- Example: 
  - `255.255.255.0` → 24-bit subnet mask (`/24`), leaving 8 bits for hosts.
  - `255.255.255.128` → 25-bit subnet mask (`/25`), leaving 7 bits for hosts.
- Subnetting helps divide a large network into smaller, manageable segments.

### 3. **CIDR Notation**
- CIDR (Classless Inter-Domain Routing) notation represents the subnet mask in a compact form.
- Example: `192.168.1.0/24` means the first 24 bits define the network, leaving the last 8 bits for host addresses.

### 4. **Routing**
- **Static Routing**: Manually defining routes in a routing table.
- **Dynamic Routing**: Using protocols like RIP, OSPF, or BGP to determine routes automatically.

### 5. **Private vs. Public IPs**
- **Private IP Ranges** (not routable on the public internet):
  - `10.0.0.0 - 10.255.255.255`
  - `172.16.0.0 - 172.31.255.255`
  - `192.168.0.0 - 192.168.255.255`
- Public IPs are assigned by ISPs for internet access.

![Screenshot from 2025-03-21 14-16-28](https://github.com/user-attachments/assets/2f764031-a5d6-4891-a198-c4189b4a595e)


## Common Tasks in NetPractice

### 1. **Converting Subnet Masks**
- Convert between decimal and CIDR notation.
- Example:
  - `255.255.255.0` → `/24`
  - `255.255.255.128` → `/25`

### 2. **Calculating Network Ranges**
- Given an IP and a subnet mask, determine:
  - Network Address
  - Broadcast Address
  - Usable Host Range
- Example:
  - IP: `192.168.1.100/26`
  - Network Address: `192.168.1.64`
  - Broadcast Address: `192.168.1.127`
  - Usable Hosts: `192.168.1.65 - 192.168.1.126`

### 3. **Troubleshooting Connectivity**
- Check for misconfigured subnet masks.
- Ensure devices are on the same network to communicate without a router.
- Use `ping`, `traceroute`, and `netstat` to diagnose issues.

## Useful Commands
- `ip a` → Show IP addresses on Linux.
- `ifconfig` → Check network interfaces (deprecated in favor of `ip` command).
- `route -n` → Display routing table.
- `traceroute <IP>` → Show the path packets take to a destination.

