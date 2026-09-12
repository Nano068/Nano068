# [Box Name] — [Easy/Medium/Hard/Insane] ([Linux/Windows])

**Retired:** YYYY-MM-DD · **Completed:** YYYY-MM-DD · **IP:** 10.10.10.x

## Summary

One or two sentences: what the box was about and the overall attack path, e.g.
*"Foothold via an exposed Gitea instance leaking credentials, then privesc through a misconfigured sudo rule on a backup script."*

## Skills / Techniques

`Tag`, `Tag`, `Tag` — e.g. `SQL Injection`, `Credential Reuse`, `Sudo Misconfiguration`

## Enumeration

```bash
nmap -sC -sV -oA nmap/initial 10.10.10.x
```

What the scan revealed, which ports/services stood out, and why.

## Foothold

Walk through how initial access was gained. Include the meaningful commands and *why* each step was taken, not just what was typed.

```bash
# example
curl -s http://10.10.10.x/api/endpoint
```

## Privilege Escalation

Same approach — command, output, reasoning.

```bash
sudo -l
```

## Root / System

Final step(s) to full compromise.

## Lessons Learned

- What made this box interesting
- What you'd do differently or faster next time
- Any tool/technique you want to remember for future engagements

## References

- Links to any external resources, CVEs, or tool docs used (no flag values, no box credentials).
