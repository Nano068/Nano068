# Windows Baseline

**Purpose:** establish what "normal" looks like on the endpoint *before* any attack simulation,
so later alerts can be judged against a real baseline instead of guesswork.

**Baseline capture date:** YYYY-MM-DD (should be a period of ordinary, unscripted use)

## Process activity

- Typical parent/child process patterns during normal use (list the common ones observed)
- Any processes that run frequently and could be mistaken for suspicious activity later
  (document these explicitly — they're your future false-positive candidates)

## Logon activity

- Normal logon types observed (interactive, network, service)
- Typical logon times / frequency for the standard user account
- Any expected failed logons (e.g. mistyped password during testing) — note the baseline
  failure rate so `SOC-001-Failed-Logins.md` has something real to compare against

## Network activity

- Expected outbound connections (Windows Update, NTP, etc.)
- Anything on the isolated network that looks unusual even at baseline — investigate before
  moving on, since an inaccurate baseline undermines every later investigation

## PowerShell usage

- Baseline PowerShell activity, if any, during normal use
- Execution policy setting

## Account/group activity

- Existing local accounts and group memberships at baseline (used later to detect
  unauthorized account creation in `SOC-003-Account-Creation.md`)

## Screenshots

See [`Screenshots/`](Screenshots/) for baseline dashboard views and event samples.

## How this gets used

Every entry in `03-Alert-Investigations/` should reference this file when arguing that an
observed event is anomalous — "anomalous compared to what" is the question a baseline answers.
