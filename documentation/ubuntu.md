# 🟢 Ubuntu Linux

## Purpose

Ubuntu is the Linux administration and security-experiment machine in this home lab. It can also be used as a controlled target for authorized exercises from Kali Linux.

## System Configuration

| Specification | Value |
|---|---|
| VM Name | `ubuntu` |
| OS | Ubuntu 26.04 LTS |
| Codename | Resolute Raccoon |
| VirtualBox | 7.2.14 r174565 |
| Hostname | `Ubuntu` |
| CPU | 2 vCPU |
| RAM | 4096 MB |
| Storage | 40.00 GB VDI |
| Network Adapter | Intel PRO/1000 MT Desktop (82540EM) |
| Network Mode | NAT Network |
| Network | `TestNetwork` |
| IP Address | `10.0.2.15` |
| Subnet | `10.0.2.0/24` |
| Gateway | `10.0.2.1` |
| Interface | `enp0s3` |
| MAC Address | `08:00:27:52:5B:39` |
| DHCP | Enabled |
| Promiscuous Mode | Deny |
| Virtual Cable | Connected |

## Network Information

Current route:

```text
default via 10.0.2.1 dev enp0s3
```

Current IPv4 address:

```text
10.0.2.15/24
```

## Useful Commands

```bash
cat /etc/os-release
hostnamectl
ip addr
ip route
free -h
df -h
journalctl
```

## Planned Uses

- Linux administration
- Networking
- Service deployment
- Log analysis
- Security configuration
- Testing security controls
- Controlled security exercises

## Learning Log

For each exercise, record:

- Date
- Objective
- Configuration
- Commands used
- Result
- Troubleshooting
- Lessons learned
