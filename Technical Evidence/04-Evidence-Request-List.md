# 04 — Evidence Request List

The evidence an auditor would request to move each finding from *documented* to *verified*. Status reflects this tabletop engagement, where technical artifacts were **not available for review** — which is itself the basis for several findings.

| # | Control area | Evidence requested | Format | Status | Finding |
|---|--------------|--------------------|--------|--------|---------|
| 1 | Remote access (MFA) | Conditional Access policy export; 30-day sign-in logs | JSON / CSV | Not provided | F1 |
| 2 | Endpoint compliance | Device-compliance report for remote endpoints | CSV / dashboard | Not provided | F1 |
| 3 | Asset management | Asset inventory with assigned owners and classification | Register / CSV | Partial — roles defined, inventory not evidenced | F2 |
| 4 | Information classification | Sample labelled documents; handling matrix | Samples | Not provided | F2 |
| 5 | Risk management | Live risk register with dated entries and owner | Register | Not provided — methodology only | F3 |
| 6 | Monitoring & logging | SIEM log-source list; analytic rules; review records | Export / screenshots | Not provided | F4 |
| 7 | Vulnerability management | Latest authenticated scan report | PDF / CSV | Not provided | 8.8 / R07 |
| 8 | Patch management | Patch-compliance report; remediation SLAs | Report | Not provided | 8.8 / R07 |
| 9 | Cloud security | Cloud-security policy; tenant configuration baseline | Policy / export | Not provided | 5.23 |
| 10 | Information deletion | Retention schedule; secure-deletion procedure | Procedure | Not provided | 8.10 / R08 |
| 11 | Configuration management | Secure-baseline / hardening standard | Standard | Not provided | 8.9 |
| 12 | Business continuity | ICT continuity / DR plan and test records | Plan / records | Not provided | 5.30 |
| 13 | Incident management | Incident records; post-incident reviews | Tickets / reports | Not assessed | A.16 |
| 14 | Supplier security | Supplier register; security clauses; assessments | Register / contracts | Not assessed | 5.19–5.22 |

**How to read "Status."** *Not provided* means the evidence was requested but not available during a documentation-level review — the gap between policy and operating practice that this assessment is designed to surface. In a full engagement, each row would be re-tested with the artifact in hand.

---

<sub>Illustrative content for a fictional organization. See the repository [README](../README.md) for context.</sub>
