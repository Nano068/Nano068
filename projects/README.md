# Projects
# PROJECTNAME

## Objective
[Brief Objective - Remove this afterwards]

The Detection Lab project aimed to establish a controlled environment for simulating and detecting cyber attacks. The primary focus was to ingest and analyze logs within a Security Information and Event Management (SIEM) system, generating test telemetry to mimic real-world attack scenarios. This hands-on experience was designed to deepen understanding of network security, attack patterns, and defensive strategies.

### Skills Learned
[Bullet Points - Remove this afterwards]

- Advanced understanding of SIEM concepts and practical application.
- Proficiency in analyzing and interpreting network logs.
- Ability to generate and recognize attack signatures and patterns.
- Enhanced knowledge of network protocols and security vulnerabilities.
- Development of critical thinking and problem-solving skills in cybersecurity.

### Tools Used
[Bullet Points - Remove this afterwards]

- Security Information and Event Management (SIEM) system for log ingestion and analysis.
- Network analysis tools (such as Wireshark) for capturing and examining network traffic.
- Telemetry generation tools to create realistic network traffic and attack scenarios.

## Steps
drag & drop screenshots here or use imgur and reference them using imgsrc

Every screenshot should have some text explaining what the screenshot is about.

Example below.

*Ref 1: Network Diagram*
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
