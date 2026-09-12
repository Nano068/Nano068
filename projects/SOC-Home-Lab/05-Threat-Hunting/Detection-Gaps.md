# Detection Gaps

A running log of gaps identified through threat hunts, incidents, or alert investigations —
things the current environment *cannot* currently detect, and what it would take to close each gap.

| # | Gap | Discovered via | Impact if exploited | Proposed fix | Status |
|---|---|---|---|---|---|
| 1 | (e.g. No logging on PowerShell Script Block execution content, only process creation) | Hunt-001 | Encoded/obfuscated commands can't be inspected post-decode | Enable PowerShell Script Block Logging + ship to Wazuh | Open |
| | | | | | |

## Why this file matters

A portfolio that only shows clean detections looks incomplete to a hiring manager — knowing
what you *can't* see yet, and having a plan to fix it, demonstrates the same maturity a real
SOC team needs. Keep this file honest and current.
