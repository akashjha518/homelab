# 🔴 Kali Linux

## Purpose

Kali Linux is the primary security-focused machine in this home lab. It is used for learning cybersecurity concepts and performing authorized security testing against lab systems.

## System Configuration

| Specification | Value |
|---|---|
| VM Name | `kali-linux-2026.2-virtualbox-amd64` |
| OS | Kali Linux 2026.2 |
| VirtualBox | 7.2.14 r174565 |
| Hostname | `kali` |
| CPU | 2 vCPU |
| RAM | 4096 MB |
| Storage | 80.09 GB VDI |
| Graphics Memory | 128 MB |
| Graphics Controller | VMSVGA |
| Network Adapter | Intel PRO/1000 MT Desktop |
| Network Mode | NAT Network |
| Network | `TestNetwork` |
| IP Address | `10.0.2.4` |
| Subnet | `10.0.2.0/24` |
| Gateway | `10.0.2.1` |
| Interface | `eth0` |
| MAC Address | `08:00:27:5A:87:BC` |
| DHCP | Enabled |

## Network Information

Current route:

```text
default via 10.0.2.1 dev eth0
```

Current IPv4 address:

```text
10.0.2.4/24
```

## Useful Commands

```bash
cat /etc/os-release
hostnamectl
ip addr
ip route
free -h
df -h
```

## Planned Security Exercises

- Network reconnaissance
- Service enumeration
- Packet analysis
- Web security practice
- Vulnerability assessment
- CTF exercises
- Security tool experimentation

## Learning Log

For each exercise, record:

- Date
- Objective
- Target lab machine
- Commands used
- Result
- Findings
- Lessons learned
