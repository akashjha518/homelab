# 🟠 Metasploitable 2

## Purpose

Metasploitable 2 is an intentionally vulnerable Linux virtual machine used as a controlled target for cybersecurity training.

It provides a safe environment for practicing reconnaissance, service enumeration, vulnerability identification, exploitation concepts, and security analysis.

## Configuration

| Specification | Value |
|---|---|
| VM Name | `metasploitable2` |
| VirtualBox OS Type | Ubuntu (64-bit) |
| Hostname | `metasploitable` |
| CPU | 1 vCPU |
| RAM | 512 MB |
| Storage | 8.00 GB VMDK |
| Network Adapter | Intel PRO/1000 MT Desktop |
| Network Mode | NAT Network |
| NAT Network | `TestNetwork` |
| IPv4 | `10.0.2.6` |
| Subnet | `10.0.2.0/24` |
| Mask | `255.255.255.0` |
| Gateway | `10.0.2.1` |
| Interface | `eth0` |
| MAC | `08:00:27:4E:D9:5E` |
| DHCP | Enabled |

## Network Role

Metasploitable 2 is the primary intentionally vulnerable target in the current lab.

```text
Kali 10.0.2.4
     │
     │ authorized testing
     ▼
Metasploitable 2 10.0.2.6
```

## Verified Routing

```text
10.0.2.0    0.0.0.0    255.255.255.0    eth0
0.0.0.0     10.0.2.1   0.0.0.0          eth0
```

## Intended Workflow

```text
Reconnaissance
      ↓
Service Enumeration
      ↓
Vulnerability Identification
      ↓
Controlled Testing
      ↓
Evidence Collection
      ↓
Analysis
      ↓
Lessons Learned
```

## Security Boundary

Metasploitable 2 is intentionally vulnerable.

- Keep it on the controlled lab network.
- Do not expose it directly to the public Internet.
- Test only from authorized systems.
- Document findings responsibly.

