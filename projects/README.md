# Projects

Home-built security projects: tools, detections, automations, and small research builds. Each project gets its own subfolder (code + a `README.md` for that project) or, for very small builds, a single write-up file here.

## Index

| Project | Description | Stack | Link |
|---|---|---|---|
| SOC Home Lab | End-to-end SOC build: Wazuh + Sysmon telemetry, alert investigations, incident response, and threat hunting against a documented baseline | Wazuh, Sysmon, Windows, VirtualBox/VMware | [folder](SOC-Home-Lab/) |
| _Example: log-triage-cli_ | CLI that ingests auth logs and flags brute-force patterns | Python, Click | [repo/folder](TEMPLATE.md) |

## Adding a project

1. If it's a real codebase, create `projects/<project-name>/` with its own code and `README.md` (use [`TEMPLATE.md`](TEMPLATE.md) as a starting point for that inner README).
2. If it's a smaller write-up-style project, just add a single markdown file here.
3. Add a row to the index above.

A good project entry covers: the problem you were solving, the design/architecture, what you'd improve, and a link to the code (this repo, or an external repo if it's large enough to live on its own).
