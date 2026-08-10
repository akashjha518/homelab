# 🖥️ VirtualBox Setup

## Hypervisor

- Product: Oracle VirtualBox
- Version: `7.2.14 r174565`
- Host platform: Windows

## VM Inventory

| VM | OS | CPU | RAM | Storage | Network |
|---|---|---:|---:|---:|---|
| `kali-linux-2026.2-virtualbox-amd64` | Kali Linux 2026.2 | 2 | 4 GB | 80.09 GB | NAT Network |
| `ubuntu` | Ubuntu 26.04 LTS | 2 | 4 GB | 40.00 GB | NAT Network |

## Network Configuration

Both VMs use:

- Adapter: Intel PRO/1000 MT Desktop family
- Attached to: NAT Network
- Network name: `TestNetwork`
- Network: `10.0.2.0/24`
- Gateway: `10.0.2.1`
- DHCP: Enabled

## Kali Virtual Machine

```text
Name:        kali-linux-2026.2-virtualbox-amd64
CPU:         2
RAM:         4096 MB
Disk:        80.09 GB VDI
Network:     TestNetwork
```

## Ubuntu Virtual Machine

```text
Name:        ubuntu
CPU:         2
RAM:         4096 MB
Disk:        40.00 GB VDI
Network:     TestNetwork
```

## Snapshots

Snapshots should be considered before major configuration changes or security experiments.

Recommended workflow:

```text
Known-good state
      ↓
Create snapshot
      ↓
Perform experiment
      ↓
Verify results
      ↓
Keep changes or roll back
```

## Security Note

Do not expose intentionally vulnerable services to the public Internet. Keep experiments within the controlled lab network whenever possible.
