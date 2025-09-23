# Playbook — Multiple Failed Logons (T1110)

## Where to Look
- Wazuh → Security Events → Windows logons (4625/4624)
- Correlate by username, source IP, and time window

## Triage Steps
1. Check spike of **4625** (failed) followed by **4624** (success) on same account.
2. Review source IP(s) and geolocation (if available).
3. Scope across hosts (last 24–48h) for same account/IP.
4. Contain (lab): lock account or block offending IP; document IOCs.

## MITRE
- T1110 — Brute Force
