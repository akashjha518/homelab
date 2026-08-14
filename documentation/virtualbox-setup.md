# 🖥️ VirtualBox Setup

## Hypervisor

- Oracle VirtualBox
- Version: `7.2.14 r174565`
- Host platform: Windows

## VM Inventory

| VM | CPU | RAM | Storage | Network |
|---|---:|---:|---:|---|
| Kali | 2 | 4 GB | 80.09 GB VDI | `TestNetwork` |
| Ubuntu | 2 | 4 GB | 40.00 GB VDI | `TestNetwork` |
| Metasploitable 2 | 1 | 512 MB | 8.00 GB VMDK | `TestNetwork` |

## Shared Network

- Type: NAT Network
- Name: `TestNetwork`
- Network: `10.0.2.0/24`
- Gateway: `10.0.2.1`
- DHCP: Enabled

## Security Note

Metasploitable 2 is intentionally vulnerable. Keep it isolated from untrusted networks and do not expose it directly to the public Internet.
