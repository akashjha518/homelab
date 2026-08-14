# 🌐 Lab Networking

## Overview

All three virtual machines are connected to the VirtualBox NAT Network `TestNetwork`.

## Current Topology

```text
                 TestNetwork
                  10.0.2.0/24
                       │
       ┌───────────────┼────────────────┐
       │               │                │
      Kali            Ubuntu       Metasploitable 2
    10.0.2.4        10.0.2.15          10.0.2.6
      eth0           enp0s3              eth0
       │               │                │
       └───────────────┼────────────────┘
                       │
                   Gateway
                   10.0.2.1
```

## Addressing

| Device | IP | Interface | Role |
|---|---|---|---|
| Kali | `10.0.2.4` | `eth0` | Security workstation |
| Ubuntu | `10.0.2.15` | `enp0s3` | Linux lab |
| Metasploitable 2 | `10.0.2.6` | `eth0` | Vulnerable target |
| Gateway | `10.0.2.1` | — | Virtual gateway |

## Connectivity Tests

From Kali:

```bash
ping 10.0.2.6
ping 10.0.2.15
```

Record the actual results in the relevant lab report.

## DHCP

The current VM addresses are DHCP-assigned. Update this documentation if the leases change.

## Security Boundary

Keep intentionally vulnerable systems within the controlled lab network. Do not expose Metasploitable 2 directly to the public Internet.
