# 🌐 Home Lab Network Diagram

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
     eth0                   enp0s3                  eth0
     Security VM            Linux VM                Vulnerable Target
        │                     │                     │
        └─────────────────────┴─────────────────────┘
                              │
                         Gateway
                         10.0.2.1
```

## Address Table

| Device | Hostname | IP | Role |
|---|---|---|---|
| Kali | `kali` | `10.0.2.4` | Security workstation |
| Ubuntu | `Ubuntu` | `10.0.2.15` | Linux lab |
| Metasploitable 2 | `metasploitable` | `10.0.2.6` | Vulnerable target |
| Gateway | — | `10.0.2.1` | Virtual gateway |

> IP addresses are DHCP-assigned and may change.
