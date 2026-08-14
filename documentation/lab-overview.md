# 🏠 Lab Overview

## Purpose

This home lab is a controlled environment for practical cybersecurity, Linux, networking, vulnerability-assessment, troubleshooting, and SOC Analyst learning.

## Current Environment

| Component | Details |
|---|---|
| Hypervisor | Oracle VirtualBox 7.2.14 r174565 |
| Virtual Network | `TestNetwork` |
| Network Type | NAT Network |
| Network | `10.0.2.0/24` |
| Gateway | `10.0.2.1` |
| DHCP | Enabled |
| VMs | Kali, Ubuntu, Metasploitable 2 |

## Machines

### 🔴 Kali Linux

- VM: `kali-linux-2026.2-virtualbox-amd64`
- OS: Kali Linux 2026.2
- Hostname: `kali`
- CPU: 2 vCPU
- RAM: 4 GB
- Storage: 80.09 GB VDI
- IP: `10.0.2.4`
- Interface: `eth0`
- MAC: `08:00:27:5A:87:BC`

### 🟢 Ubuntu

- VM: `ubuntu`
- OS: Ubuntu 26.04 LTS
- Hostname: `Ubuntu`
- CPU: 2 vCPU
- RAM: 4 GB
- Storage: 40.00 GB VDI
- IP: `10.0.2.15`
- Interface: `enp0s3`
- MAC: `08:00:27:52:5B:39`

### 🟠 Metasploitable 2

- VM: `metasploitable2`
- VirtualBox OS type: Ubuntu (64-bit)
- Hostname: `metasploitable`
- CPU: 1 vCPU
- RAM: 512 MB
- Storage: 8.00 GB VMDK
- IP: `10.0.2.6`
- Interface: `eth0`
- MAC: `08:00:27:4E:D9:5E`
- Role: Intentionally vulnerable training target

## Documentation Method

Each lab should document:

1. Objective
2. Environment
3. Methodology
4. Commands and tools
5. Evidence
6. Findings
7. Analysis
8. Troubleshooting
9. Lessons learned
