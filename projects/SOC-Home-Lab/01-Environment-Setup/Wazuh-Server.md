# Wazuh Server — Build & Configuration

**Purpose:** the SIEM manager that ingests Sysmon/Windows event telemetry and generates alerts.

## Specs

| Item | Value |
|---|---|
| OS | Ubuntu Server (version) |
| Hypervisor | |
| RAM / vCPU | (Wazuh's all-in-one install is memory-hungry — note actual usage once running) |
| Disk | |
| Network adapter | Same isolated internal network as the Windows VM |

## Install

Document the actual install method used (all-in-one quickstart script vs. manual component
install) and the version installed:

```bash
# example — replace with the actual command used
curl -sO https://packages.wazuh.com/4.x/wazuh-install.sh
sudo bash wazuh-install.sh -a
```

Record the generated admin credentials location and how they were secured (not committed to this repo).

## Post-install configuration

- [ ] Confirm dashboard access over the internal network
- [ ] Enroll the Windows VM as an agent (record the enrollment command used)
- [ ] Verify agent shows "Active" in the Wazuh dashboard
- [ ] Configure log retention / index lifecycle to a size sane for a home lab
- [ ] Note which default rule sets are enabled and any custom rules added later
  (link forward to `03-Alert-Investigations/` once custom rules exist)

## Screenshots

See [`Screenshots/`](Screenshots/) for dashboard views, agent enrollment confirmation, etc.

## Notes / gotchas

Anything that didn't match the official docs, version-specific quirks, resource tuning done to
keep it running smoothly on lab hardware.
