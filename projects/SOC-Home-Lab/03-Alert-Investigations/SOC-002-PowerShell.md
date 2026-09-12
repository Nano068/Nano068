# SOC-002 — Suspicious PowerShell Activity

**Alert triggered:** YYYY-MM-DD HH:MM · **Analyst:** [Your name] · **Status:** Open / Resolved

## 1. Alert Summary

| Field | Value |
|---|---|
| Rule / Alert name | (e.g. custom rule on Sysmon Event ID 1 — encoded PowerShell command) |
| Source | Sysmon Event ID 1 (process creation) / PowerShell Script Block Logging |
| Affected host | |
| Parent process | |
| Alert severity (as raised) | |

## 2. Initial Triage

What the command line looked like at first glance — encoded/obfuscated arguments, unusual
flags (`-enc`, `-nop`, `-w hidden`, `-exec bypass`), or an unusual parent process spawning
PowerShell (e.g. Word or Excel rather than explorer.exe).

## 3. Investigation

- Full command line captured, and — if encoded — the decoded payload
  (document the decoding method, e.g. base64 → UTF-16LE)
- Parent/child process tree at the time of execution
- Any network connections spawned by the PowerShell process (Sysmon Event ID 3)
- Any files written/modified as a result (Sysmon Event ID 11)
- Comparison against baseline PowerShell usage in [`Windows-Baseline.md`](../02-Baseline/Windows-Baseline.md)

```powershell
# decoded payload (sanitized/summarized, not a literal copy of any external source)
```

## 4. Determination

**Verdict:** True Positive / False Positive / Benign True Positive

Reasoning, including what specifically distinguishes this from normal admin/scripting use.

## 5. Response Actions

- [ ] Process terminated / host isolated (if simulated in the lab, note what "response" meant here)
- [ ] IOC extracted (hash, decoded command pattern) and logged
- [ ] Detection rule added/tuned to catch this pattern going forward

## 6. Lessons Learned

What made this technique detectable (or nearly missed) — useful for tuning future rules.
