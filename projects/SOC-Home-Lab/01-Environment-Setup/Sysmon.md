# Sysmon — Deployment & Configuration

**Purpose:** high-fidelity endpoint telemetry on the Windows VM — the actual data source behind
every alert this lab produces.

## Version

- Sysmon version installed:
- Config template used as a base: (e.g. SwiftOnSecurity's `sysmonconfig-export.xml`, or Olaf Hartong's `sysmon-modular`)

## Install

```powershell
# example
.\Sysmon64.exe -accepteula -i sysmonconfig.xml
```

## Config decisions

Document deviations from the base template and *why* — this is the part that actually
demonstrates understanding rather than just following a guide:

| Event ID | What it captures | Included? | Reasoning |
|---|---|---|---|
| 1 | Process creation | Yes | Core signal for nearly every investigation below |
| 3 | Network connection | Yes | Needed to catch C2/beaconing-style behavior |
| 11 | File create | Yes | Useful for persistence/dropper detection |
| 13 | Registry value set | Yes | Common persistence mechanism |
| ... | | | |

## Verifying it's working

```powershell
Get-WinEvent -LogName "Microsoft-Windows-Sysmon/Operational" -MaxEvents 5
```

Confirm events are also arriving at the Wazuh manager before moving on to baselining.

## Screenshots

See [`Screenshots/`](Screenshots/) for install confirmation and sample event output.

## Notes / gotchas

Performance impact observed, any events that turned out too noisy and were filtered, etc.
