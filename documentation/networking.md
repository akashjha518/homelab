# 🌐 Lab Networking

## Network Overview

The current home lab uses a VirtualBox **NAT Network** named `TestNetwork`.

```text
                    VirtualBox
                         │
                 TestNetwork
                  10.0.2.0/24
                         │
                ┌────────┴────────┐
                │                 │
              Kali             Ubuntu
            10.0.2.4          10.0.2.15
             eth0              enp0s3
                │                 │
                └────────┬────────┘
                         │
                     Gateway
                     10.0.2.1
```

## Addressing

| Component | Address |
|---|---|
| Network | `10.0.2.0/24` |
| Subnet Mask | `255.255.255.0` |
| Gateway | `10.0.2.1` |
| Kali | `10.0.2.4` |
| Ubuntu | `10.0.2.15` |
| DHCP | Enabled |

## Interfaces

| VM | Interface | MAC |
|---|---|---|
| Kali | `eth0` | `08:00:27:5A:87:BC` |
| Ubuntu | `enp0s3` | `08:00:27:52:5B:39` |

## Connectivity Testing

From Kali:

```bash
ping 10.0.2.15
```

From Ubuntu:

```bash
ping 10.0.2.4
```

Record the results of these tests in a lab exercise rather than assuming connectivity.

## Network Discovery

Once connectivity is confirmed, controlled discovery can be performed against the lab network.

Example:

```bash
ip route
```

For authorized discovery exercises from Kali, document the exact target and command used.

## Important Note

Both IP addresses are currently DHCP-assigned. They may change after lease renewal or network changes. Update this documentation if the addresses change.

Do not expose intentionally vulnerable systems or services directly to the public Internet.
