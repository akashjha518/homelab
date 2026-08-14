# 🏠 Cybersecurity Home Lab

A personal cybersecurity home lab for hands-on learning, experimentation, troubleshooting, and practical cybersecurity skill development.

The lab currently contains **Kali Linux 2026.2**, **Ubuntu 26.04 LTS**, and **Metasploitable 2**, running in **Oracle VirtualBox 7.2.14**.

## 🎯 Objectives

- Build practical Linux administration skills
- Understand networking and system communication
- Practice authorized security testing in a controlled environment
- Develop SOC Analyst skills
- Learn reconnaissance, enumeration, vulnerability assessment, and defensive concepts
- Document configurations, evidence, troubleshooting, and lessons learned

## 🖥️ Current Lab

| Machine | OS | Role | CPU | RAM | Storage | Current IP |
|---|---|---|---:|---:|---:|---|
| 🔴 Kali | Kali Linux 2026.2 | Security workstation | 2 vCPU | 4 GB | 80.09 GB | `10.0.2.4` |
| 🟢 Ubuntu | Ubuntu 26.04 LTS | Linux lab / defensive system | 2 vCPU | 4 GB | 40 GB | `10.0.2.15` |
| 🟠 Metasploitable 2 | Intentionally vulnerable Linux VM | Training target | 1 vCPU | 512 MB | 8 GB | `10.0.2.6` |

> IP addresses are currently DHCP-assigned and may change.

## 🌐 Network

```text
                         HOST MACHINE
                              │
                         VirtualBox
                       v7.2.14 r174565
                              │
                  NAT Network: TestNetwork
                       10.0.2.0/24
                              │
        ┌─────────────────────┼─────────────────────┐
        │                     │                     │
     🔴 KALI               🟢 UBUNTU          🟠 METASPLOITABLE 2
     10.0.2.4               10.0.2.15              10.0.2.6
     Security VM             Linux VM              Vulnerable Target
        │                     │                     │
        └─────────────────────┴─────────────────────┘
                              │
                         Gateway
                         10.0.2.1
```

## 📚 Documentation

- [Lab Overview](documentation/lab-overview.md)
- [VirtualBox Setup](documentation/virtualbox-setup.md)
- [Kali Linux](documentation/kali-linux.md)
- [Ubuntu Linux](documentation/ubuntu.md)
- [Metasploitable 2](documentation/metasploitable2.md)
- [Networking](documentation/networking.md)
- [Troubleshooting](documentation/troubleshooting.md)
- [Network Diagram](network/network-diagram.md)

## 🧪 Labs

- [Lab 01 — Metasploitable 2 Connectivity](labs/01-metasploitable2-connectivity/README.md)

Future labs will cover reconnaissance, service enumeration, vulnerability assessment, logging, detection, and SOC-style investigations.

## 🔐 Security & Ethics

This repository documents an authorized personal lab. Metasploitable 2 is intentionally vulnerable and must remain inside the controlled lab environment. No unauthorized systems or networks will be targeted.

## 🚀 Roadmap

```text
Kali + Ubuntu + Metasploitable 2
              ↓
       Networking
              ↓
     Reconnaissance
              ↓
  Service Enumeration
              ↓
 Vulnerability Assessment
              ↓
 Logging & Monitoring
              ↓
            SIEM
              ↓
 Detection & Investigation
              ↓
      SOC Simulation
```
