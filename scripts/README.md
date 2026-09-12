# Scripts

Standalone scripts and utilities used across write-ups, labs, and projects — enumeration helpers, parsers, one-off automations that don't warrant their own project folder.

## Index

| Script | Purpose | Language |
|---|---|---|
| _Example: `nmap-to-md.py`_ | Converts nmap XML output into a markdown table for write-ups | Python |

## Conventions

- One script per file where possible; group tightly related scripts in a subfolder with their own mini-README.
- Every script gets a header comment: purpose, usage, and any dependencies.
- No hardcoded targets, credentials, or API keys — use placeholders/environment variables.

```bash
#!/usr/bin/env bash
# Purpose: <what this does>
# Usage:   ./script.sh <arg>
# Deps:    <tools required>
```
