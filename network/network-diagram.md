# 🌐 Home Lab Network Diagram

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

## Address Table

| Device | Hostname | IP | Interface | Role |
|---|---|---|---|---|
| Kali | `kali` | `10.0.2.4` | `eth0` | Security workstation |
| Ubuntu | `Ubuntu` | `10.0.2.15` | `enp0s3` | Linux lab/target |
| Gateway | — | `10.0.2.1` | — | Virtual network gateway |

> IP addresses are DHCP-assigned and may change.
