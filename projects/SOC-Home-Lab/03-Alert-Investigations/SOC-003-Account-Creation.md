# SOC-003 — Unauthorized Account Creation

**Alert triggered:** YYYY-MM-DD HH:MM · **Analyst:** [Your name] · **Status:** Open / Resolved

## 1. Alert Summary

| Field | Value |
|---|---|
| Rule / Alert name | (e.g. Wazuh rule on Event ID 4720 — "A user account was created") |
| Source | Windows Security Event Log (Event ID 4720 / 4732 for group membership) |
| Affected host | |
| New account name | |
| Alert severity (as raised) | |

## 2. Initial Triage

Compare the new account against the account list captured in
[`Windows-Baseline.md`](../02-Baseline/Windows-Baseline.md). Is this an account the baseline
didn't include? Was it added to any privileged groups (e.g. Administrators) at or near creation time?

## 3. Investigation

- Who/what created the account — the actor account and process involved (Event ID 4720's subject fields)
- Timing relative to any other suspicious activity already logged (cross-reference SOC-001/SOC-002 if related)
- Group memberships assigned (Event ID 4732 — "A member was added to a security-enabled local group")
- Any follow-on activity from the new account (first logon, processes spawned)

## 4. Determination

**Verdict:** True Positive / False Positive / Benign True Positive

Reasoning — including whether this fits a known persistence pattern (attacker creating a
backup account after initial access) versus legitimate administrative activity.

## 5. Response Actions

- [ ] Account disabled/removed
- [ ] Group membership reverted
- [ ] Root cause traced back to initial access vector (link to `04-Incident-Response/` if this
      escalated to a full incident)

## 6. Lessons Learned

Whether this alert fired promptly, and whether group-membership changes are being monitored
with the same rigor as account creation itself.
