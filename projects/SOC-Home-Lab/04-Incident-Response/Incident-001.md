# Incident-001 — [Short Title]

**Declared:** YYYY-MM-DD · **Closed:** YYYY-MM-DD · **Severity:** Low / Medium / High
**Related alerts:** (link to SOC-00X entries in `03-Alert-Investigations/` that fed into this incident)

## Executive Summary

Two or three sentences a non-technical reader could understand: what happened, what was the
impact, and what was done about it.

## Scope

- Affected host(s):
- Affected account(s):
- Time window of the incident (first observed activity → containment):

## Timeline

See [`Timeline.md`](Timeline.md) for the full minute-by-minute reconstruction. Key milestones:

| Time | Event |
|---|---|
| T+0:00 | Initial access / first anomalous event observed |
| T+0:xx | Detection — which alert fired and when |
| T+0:xx | Triage began |
| T+0:xx | Containment action taken |
| T+0:xx | Incident closed |

## Root Cause

What allowed this to happen — technical root cause, not just "attacker did X."

## Impact

What was actually affected — be honest about scope, including if the answer is "contained
before any real impact" (a fast, clean containment is a good outcome worth documenting as such).

## Containment & Eradication

Steps taken to stop the activity and remove any persistence/artifacts left behind.

## Recovery

Steps taken to return the affected host/account to a known-good state.

## Lessons Learned / Follow-up Actions

- [ ] Detection gap identified and addressed (link to `05-Threat-Hunting/Detection-Gaps.md` if applicable)
- [ ] Process improvement identified
- [ ] Any other follow-up items
