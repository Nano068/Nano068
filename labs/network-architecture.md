# Home Lab — Network Architecture

**Last updated:** YYYY-MM-DD

## Overview

Brief description of the lab's purpose (e.g. "Isolated hypervisor environment for practicing AD attack paths and testing detection rules, fully segmented from the home network").

## Topology

```
                 ┌────────────────┐
                 │   Home Router   │
                 └───────┬────────┘
                         │
                 ┌───────┴────────┐
                 │  Lab Firewall   │  (pfSense/OPNsense)
                 └───────┬────────┘
              ┌──────────┼──────────┐
       ┌──────┴─────┐ ┌──┴───┐ ┌────┴─────┐
       │  Mgmt VLAN │ │ AD   │ │ Attacker │
       │            │ │ VLAN │ │  VLAN    │
       └────────────┘ └──────┘ └──────────┘
```

## Hardware / Virtualization

- Hypervisor: (e.g. Proxmox, ESXi)
- Host specs:
- Storage:

## Segmentation

| VLAN/Segment | Purpose | Access rules |
|---|---|---|
| Mgmt | Hypervisor/host management | Isolated from attacker VLAN |
| AD Range | Target domain environment | No outbound internet |
| Attacker | Kali/attack box | Access to AD range only |

## Safety notes

How the lab stays isolated from production/home devices (VLAN rules, no bridged NICs to home LAN, etc).
