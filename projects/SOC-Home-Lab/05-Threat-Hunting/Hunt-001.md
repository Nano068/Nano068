# Hunt-001 — [Hypothesis Title]

**Date:** YYYY-MM-DD · **Analyst:** [Your name]

## Hypothesis

State it as an actual hypothesis, not just a topic — e.g. *"If an attacker established
persistence via a scheduled task, it would show up as a Sysmon Event ID 1 spawning
`schtasks.exe` with unusual parameters, outside of normal administrative hours."*

## Why this hunt

What prompted it — a threat report technique, a gap noticed while writing up a prior alert,
or simply a technique not yet covered by any existing detection rule.

## Data sources queried

- Sysmon Event ID(s):
- Wazuh index / query used:

```
# example query
event.code:1 AND process.name:"schtasks.exe"
```

## Findings

What the query returned — even "nothing found" is a valid, useful finding (it either confirms
the environment is clean for this technique, or that logging doesn't currently capture it —
distinguish between these two outcomes explicitly).

## Outcome

- [ ] No findings — technique not present, logging confirmed adequate to detect it if it occurred
- [ ] No findings — but logging gap identified (log to [`Detection-Gaps.md`](Detection-Gaps.md))
- [ ] Findings — escalated to an alert investigation / incident (link it)

## New detection created?

If this hunt led to a new Wazuh rule, document the rule here and link back to it from
`01-Environment-Setup/Wazuh-Server.md`.
