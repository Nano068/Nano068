# SOC Home Lab

A self-built Security Operations Center environment for practicing detection engineering,
log analysis, and incident response — end to end, from raw telemetry to a written incident report.

## Why this exists

Most CTF-style practice (HTB, etc.) trains the attacker's side. This project trains the
defender's side: standing up real endpoint logging, shipping it to a SIEM, writing detections,
and working alerts the way a SOC analyst would — triage, investigate, escalate, document.

## What's in here

| Folder | Contents |
|---|---|
| [`00-Project-Overview/`](00-Project-Overview/) | Goals, scope, and the lab's network diagram |
| [`01-Environment-Setup/`](01-Environment-Setup/) | Build docs for the Windows victim VM, Wazuh server, and Sysmon config |
| [`02-Baseline/`](02-Baseline/) | What "normal" looks like on the Windows host before any attack simulation |
| [`03-Alert-Investigations/`](03-Alert-Investigations/) | Individual alert write-ups (SOC-001, SOC-002, ...) — triage through resolution |
| [`04-Incident-Response/`](04-Incident-Response/) | Full incident case files with timelines, for alerts that escalated |
| [`05-Threat-Hunting/`](05-Threat-Hunting/) | Proactive hunts and the detection gaps they turned up |
| [`06-Metrics/`](06-Metrics/) | SOC metrics tracker (MTTD/MTTR, alert volume, false-positive rate) |

## Stack

- **Hypervisor:** (fill in — e.g. VirtualBox, VMware Workstation, Proxmox)
- **Victim endpoint:** Windows 10/11 VM with Sysmon
- **SIEM:** Wazuh (manager + agent)
- **Attack simulation:** (fill in — e.g. Atomic Red Team, manual technique reproduction)

## How to read this repo

Work through it in folder order — `00` through `06` — the way the lab was actually built:
environment stood up, baseline captured, then alerts investigated against that baseline.
Each alert investigation follows the same structure so they're easy to compare over time
(see the template note inside `03-Alert-Investigations/`).

## Status

🔧 In progress — see [`Objectives.md`](00-Project-Overview/Objectives.md) for what's built vs. planned.
