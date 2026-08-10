# 🏠 Cybersecurity Home Lab

A personal cybersecurity home lab built for hands-on learning, experimentation, troubleshooting, and practical cybersecurity skill development.

The lab currently consists of **Kali Linux 2026.2** and **Ubuntu 26.04 LTS** virtual machines running in **Oracle VirtualBox 7.2.14**.

---

## 🎯 Objectives

The main goals of this home lab are to:

- Build practical Linux administration skills
- Understand networking and system communication
- Practice cybersecurity concepts in a controlled environment
- Develop hands-on skills for a **SOC Analyst** career
- Experiment with security tools and techniques
- Learn through practical troubleshooting
- Document technical work and lessons learned
- Gradually build a realistic SOC-style environment

---

## 🖥️ Current Lab Environment

| Machine | Operating System | Role | CPU | RAM | Storage | IP Address | Status |
|---|---|---|---:|---:|---:|---|---|
| 🔴 Kali | Kali Linux 2026.2 | Security workstation | 2 vCPU | 4 GB | 80.09 GB | `10.0.2.4` | 🟢 Active |
| 🟢 Ubuntu | Ubuntu 26.04 LTS | Linux lab / target | 2 vCPU | 4 GB | 40 GB | `10.0.2.15` | 🟢 Active |

> The IP addresses above are the current DHCP-assigned addresses and may change.

---

## 🏗️ Lab Architecture

```text
                         HOST MACHINE
                              │
                         VirtualBox
                       v7.2.14 r174565
                              │
                  ┌───────────┴───────────┐
                  │    TestNetwork        │
                  │    10.0.2.0/24        │
                  │    DHCP: Enabled      │
                  └───────────┬───────────┘
                              │
             ┌────────────────┴────────────────┐
             │                                 │
       🔴 KALI LINUX                     🟢 UBUNTU
       Host: kali                       Host: Ubuntu
       IP: 10.0.2.4                     IP: 10.0.2.15
       eth0                             enp0s3
       08:00:27:5A:87:BC                08:00:27:52:5B:39
       2 vCPU / 4 GB                    2 vCPU / 4 GB
       80.09 GB                         40 GB
             │                                 │
             └────────────────┬────────────────┘
                              │
                         Gateway
                         10.0.2.1
```

See the detailed [network diagram](network/network-diagram.md).

---

## 🌐 Network Configuration

| Component | Configuration |
|---|---|
| Network Name | `TestNetwork` |
| Network Type | NAT Network |
| Network Range | `10.0.2.0/24` |
| Subnet Mask | `255.255.255.0` |
| Gateway | `10.0.2.1` |
| DHCP | Enabled |
| Kali | `10.0.2.4` |
| Ubuntu | `10.0.2.15` |

Both VMs are connected to the same VirtualBox NAT Network.

This provides a controlled environment for testing communication, networking, enumeration, logging, and security concepts between the two machines.

> Because DHCP is enabled, the VM addresses should be treated as current addresses rather than permanent/static assignments.

---

## 🔴 Kali Linux

Kali Linux is the primary security-focused machine in the lab.

### Configuration

- **VM Name:** `kali-linux-2026.2-virtualbox-amd64`
- **OS:** Kali Linux 2026.2
- **Hostname:** `kali`
- **CPU:** 2 vCPU
- **RAM:** 4 GB
- **Storage:** 80.09 GB VDI
- **Network:** `TestNetwork`
- **IP:** `10.0.2.4`
- **Interface:** `eth0`
- **Gateway:** `10.0.2.1`

### Planned Uses

- Network reconnaissance
- Service enumeration
- Vulnerability assessment
- Network analysis
- Security tool experimentation
- Web security practice
- Capture-the-Flag exercises
- Authorized security testing

Detailed configuration: [Kali Linux documentation](documentation/kali-linux.md)

---

## 🟢 Ubuntu Linux

Ubuntu is the Linux administration and security-experiment machine in the lab.

It can also serve as a controlled target for authorized security exercises from Kali.

### Configuration

- **VM Name:** `ubuntu`
- **OS:** Ubuntu 26.04 LTS
- **Codename:** Resolute Raccoon
- **Hostname:** `Ubuntu`
- **CPU:** 2 vCPU
- **RAM:** 4 GB
- **Storage:** 40.00 GB VDI
- **Network:** `TestNetwork`
- **IP:** `10.0.2.15`
- **Interface:** `enp0s3`
- **Gateway:** `10.0.2.1`

### Planned Uses

- Linux administration
- Networking practice
- Service deployment
- Log analysis
- Security configuration
- Testing security controls
- Controlled security exercises

Detailed configuration: [Ubuntu documentation](documentation/ubuntu.md)

---

## 📚 Documentation

| Document | Description |
|---|---|
| [Lab Overview](documentation/lab-overview.md) | Complete overview of the current lab |
| [VirtualBox Setup](documentation/virtualbox-setup.md) | Virtual machine and hypervisor configuration |
| [Kali Linux](documentation/kali-linux.md) | Kali configuration and security role |
| [Ubuntu Linux](documentation/ubuntu.md) | Ubuntu configuration and lab role |
| [Networking](documentation/networking.md) | Network architecture and addressing |
| [Troubleshooting](documentation/troubleshooting.md) | Problems, investigation, solutions, and lessons learned |
| [Network Diagram](network/network-diagram.md) | Current lab topology |

---

## 🧪 Labs & Experiments

The lab will be used to document practical exercises rather than only installation steps.

### Current / Next Labs

- [ ] Verify Kali ↔ Ubuntu connectivity
- [ ] Basic Linux administration
- [ ] Linux networking fundamentals
- [ ] Network reconnaissance
- [ ] Service enumeration
- [ ] Packet analysis
- [ ] Linux log analysis
- [ ] Basic security hardening

### Future Labs

- [ ] Windows machine
- [ ] Vulnerable machines
- [ ] Centralized logging
- [ ] SIEM deployment
- [ ] Network monitoring
- [ ] IDS/IPS
- [ ] Detection engineering
- [ ] Attack → Detection → Investigation scenarios
- [ ] SOC-style investigations

---

## 📝 Troubleshooting & Learning

A major purpose of this repository is to document **what I actually encounter while building the lab**.

For significant problems, I will document:

1. What I was trying to accomplish
2. What went wrong
3. The exact error message
4. Investigation and troubleshooting steps
5. Root cause
6. Solution
7. Verification
8. What I learned

This makes the repository a record of practical hands-on learning rather than simply a collection of copied setup instructions.

See the [Troubleshooting documentation](documentation/troubleshooting.md).

---

## 🔐 Security & Ethics

This lab is intended for **educational purposes and authorized security testing only**.

All security testing will be performed against systems that I own, control, or have explicit permission to test.

No unauthorized systems or networks will be targeted.

Intentionally vulnerable services should remain inside the controlled lab environment and should not be exposed directly to the public Internet.

---

## 🚀 Roadmap

The lab will gradually evolve from a basic two-machine environment into a more complete cybersecurity/SOC training environment.

```text
Kali + Ubuntu
      │
      ▼
Networking Fundamentals
      │
      ▼
Linux & Windows Systems
      │
      ▼
Centralized Logging
      │
      ▼
SIEM
      │
      ▼
Detection Engineering
      │
      ▼
Incident Investigation
      │
      ▼
SOC Simulation Lab
```

---

## 📌 Current Status

**Lab Status:** 🟢 Active Development

**Virtual Machines:** 2

**Network:** `TestNetwork` (`10.0.2.0/24`)

**Hypervisor:** VirtualBox 7.2.14

**Current Focus:** Cybersecurity / SOC Analyst / Linux / Networking

---

## 👨‍💻 About This Project

This repository documents my journey of building and expanding a personal cybersecurity home lab while developing practical cybersecurity and SOC Analyst skills.

The lab will continuously evolve as I learn new technologies, tools, networking concepts, defensive techniques, and security investigation workflows.
