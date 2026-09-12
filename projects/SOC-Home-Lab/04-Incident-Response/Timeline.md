# Incident Timeline — Incident-001

Reconstructed from raw logs. Times in [timezone] — keep consistent throughout, and note if the
SIEM stores timestamps in UTC while local analysis used local time (a very common source of
timeline errors — call it out explicitly if it applies here).

| Timestamp | Source | Event | Notes |
|---|---|---|---|
| YYYY-MM-DD HH:MM:SS | Sysmon Event ID 1 | Initial process execution | |
| YYYY-MM-DD HH:MM:SS | Sysmon Event ID 3 | Outbound network connection | |
| YYYY-MM-DD HH:MM:SS | Windows Security 4720 | Account created | |
| YYYY-MM-DD HH:MM:SS | Wazuh alert | Detection fired | which rule, and the delay from first activity to detection |
| YYYY-MM-DD HH:MM:SS | Analyst action | Triage started | |
| YYYY-MM-DD HH:MM:SS | Analyst action | Containment action taken | |

## Detection latency

Time from first malicious activity to first alert firing: **_ minutes**
Time from alert firing to triage start: **_ minutes**
Time from triage start to containment: **_ minutes**

These three numbers feed directly into the MTTD/MTTR figures tracked in
[`06-Metrics/SOC-Metrics.xlsx`](../06-Metrics/SOC-Metrics.xlsx).
