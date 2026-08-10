# 🏠 Lab Overview

## Purpose

This home lab is a personal cybersecurity environment for hands-on learning, experimentation, troubleshooting, and development of practical cybersecurity and SOC Analyst skills.

## Current Environment

| Component | Details |
|---|---|
| Hypervisor | Oracle VirtualBox 7.2.14 r174565 |
| Virtual Network | `TestNetwork` |
| Network Type | NAT Network |
| Network Range | `10.0.2.0/24` |
| Gateway | `10.0.2.1` |
| DHCP | Enabled |
| Virtual Machines | Kali Linux + Ubuntu |

## Virtual Machines

### 🔴 Kali Linux

- VM name: `kali-linux-2026.2-virtualbox-amd64`
- OS: Kali Linux 2026.2
- Hostname: `kali`
- CPU: 2 vCPU
- RAM: 4 GB
- Storage: 80.09 GB VDI
- Interface: `eth0`
- IP: `10.0.2.4`
- MAC: `08:00:27:5A:87:BC`

### 🟢 Ubuntu

- VM name: `ubuntu`
- OS: Ubuntu 26.04 LTS
- Codename: Resolute Raccoon
- Hostname: `Ubuntu`
- CPU: 2 vCPU
- RAM: 4 GB
- Storage: 40.00 GB VDI
- Interface: `enp0s3`
- IP: `10.0.2.15`
- MAC: `08:00:27:52:5B:39`

## Lab Design

Both virtual machines are attached to the same VirtualBox NAT Network, allowing them to communicate within the lab network while using the configured virtual gateway.

The IP addresses shown above are DHCP-assigned and may change.

## Documentation Method

For each lab exercise, document:

1. Objective
2. Environment
3. Configuration
4. Commands/actions
5. Results
6. Troubleshooting
7. Lessons learned
