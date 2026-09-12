# SOC-001 — Failed Logins

**Alert triggered:** YYYY-MM-DD HH:MM · **Analyst:** [Your name] · **Status:** Open / Resolved

## 1. Alert Summary

| Field | Value |
|---|---|
| Rule / Alert name | (e.g. Wazuh rule 60122 — "Multiple Windows logon failures") |
| Source | Windows Security Event Log (Event ID 4625) via Sysmon/Wazuh agent |
| Affected host | |
| Affected account | |
| Alert severity (as raised) | |

## 2. Initial Triage

What the raw alert showed, and the first read on whether this looks like noise, misconfiguration,
or a real attempt (brute force, password spray, lockout from an automated service, etc).

## 3. Investigation

Step through what was actually checked — the SIEM queries run, the fields examined, and the
reasoning at each step. Compare against [`Windows-Baseline.md`](../02-Baseline/Windows-Baseline.md)
to establish whether the failure rate/pattern is anomalous.

```
# example query / filter used
rule.id:60122 AND agent.name:"WIN10-VM" AND data.win.eventdata.logonType:"3"
```

- Source of the failed attempts (local console vs. network logon type)
- Timing pattern (single burst vs. spread out — suggests scripted vs. manual)
- Whether the account eventually succeeded, locked out, or the attempts stopped

## 4. Determination

**Verdict:** True Positive / False Positive / Benign True Positive

Reasoning for the verdict, referencing the evidence above.

## 5. Response Actions

- [ ] Action taken (e.g. account lockout confirmed, password reset recommended, IP/host isolated)
- [ ] Any detection tuning done as a result of this alert

## 6. Lessons Learned

What this alert revealed about the detection itself — was it well-tuned, too noisy, missing context?
