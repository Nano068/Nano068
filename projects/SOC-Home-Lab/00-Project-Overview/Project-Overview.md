# Project Overview — SOC Home Lab

**Status:** In progress · **Last updated:** YYYY-MM-DD

## What this is

A home-built Security Operations Center: a Windows endpoint generating telemetry, a Wazuh
SIEM ingesting and alerting on that telemetry, and a documented workflow for triaging,
investigating, and reporting on what the SIEM surfaces.

## Scope

- One Windows victim endpoint (domain-joined or standalone — note which)
- One Wazuh manager (single-node)
- Sysmon deployed on the endpoint with a tuned config (not default)
- Manual attack simulation to generate realistic alert data
- Full write-up per alert/incident, plus periodic threat hunts

## Out of scope (for now)

- Multi-host / Active Directory environment
- Network-layer detection (IDS/NSM) — endpoint-focused only at this stage
- Automated response / SOAR

## Architecture at a glance

See [`Network-Diagram.png`](Network-Diagram.png) for the full topology. Summary:

```
[Windows 10 VM] --Sysmon events--> [Wazuh Agent] --> [Wazuh Manager] --> Alerts / Dashboards
```

Both VMs sit on an isolated internal virtual network, separate from the home LAN.

## Why these tool choices

- **Wazuh** — free, open-source, includes a full SIEM + agent stack without a licensing wall,
  and its rule syntax is a reasonable stepping stone toward commercial SIEMs.
- **Sysmon** — the de facto standard for high-fidelity Windows endpoint telemetry; learning to
  tune it (not just install it) is itself a core skill this project targets.
