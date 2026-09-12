# Windows VM — Build & Configuration

**Purpose:** the "victim" endpoint that generates telemetry for the SOC to monitor.

## Specs

| Item | Value |
|---|---|
| OS | Windows 10/11 (edition, build) |
| Hypervisor | (VirtualBox / VMware / Proxmox) |
| RAM / vCPU | |
| Disk | |
| Network adapter | Internal/host-only — isolated virtual network, no bridge to home LAN |

## Build steps

1. Install OS from ISO — note version/build here for reproducibility.
2. Install hypervisor guest additions/tools.
3. Set network adapter to the isolated internal network (see [Network-Diagram.png](../00-Project-Overview/Network-Diagram.png)).
4. Disable Windows Defender real-time protection *only if* it interferes with the deliberate attack
   simulations planned later — document exactly what was disabled and why, since this is a detail
   a real SOC engagement would flag.
5. Create a local admin account and a standard user account (most alerts will center on the standard user).
6. Snapshot the VM at this clean state before installing Sysmon or the Wazuh agent — this becomes
   the rollback point between attack simulation rounds.

## Screenshots

See [`Screenshots/`](Screenshots/) for build evidence (VM settings, network config, snapshot list).

## Notes / gotchas

Document anything that didn't go as expected here — these notes are often the most useful part
of this file to a future reader (including future you).
