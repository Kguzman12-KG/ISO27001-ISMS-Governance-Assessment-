# Evidence Index

A one-page map of the entire assessment: every finding, the control it tests, the evidence reviewed, the gap, its risk rating, and the fix. For the full narrative, see the [Assessment Report](ISO27001_ISMS_Assessment_Report.pdf); for the underlying data, see the workbooks in this folder.

> Risk is scored on a 5×5 likelihood × impact matrix — **Low (1–6) · Medium (7–12) · High (13–25)**. IDs in parentheses (`R01`, `NC-001`) cross-reference the Risk Assessment workbook and the Non-Conformity Log.

## Audit findings

| # | Finding | ISO 27001:2022 control(s) | Evidence reviewed | Gap identified | Risk | Remediation |
|---|---------|---------------------------|-------------------|----------------|------|-------------|
| **F1** | Remote access not enforced with MFA *(NC-001, Major)* | 6.7 Remote working · 5.15 Access control · 8.5 Secure authentication · 8.1 User endpoint devices | Remote Working Policy; Access Control Policy | Policy mandates MFA and secure remote access, but **enforcement is not evidenced** — no configuration or sign-in records confirming MFA on remote sessions | **High** (R01 · 20/25) | Enforce MFA centrally for all remote access; collect authentication logs; validate endpoint compliance |
| **F2** | Asset ownership & classification not operational *(NC-002, Major)* | 5.9 Inventory of assets · 5.12 Classification · 5.13 Labelling · 5.10 Acceptable use | Information Asset Owners Handbook; Information Classification Policy | Ownership roles and a four-tier scheme are **defined but not applied** — asset inventory, active owner assignment, and consistent classification are not evidenced | **High** (R02 · 16/25) | Complete the asset inventory; assign active owners; apply classification labels; stand up quarterly IAO reporting |
| **F3** | Risk management not operationalised *(NC-003, Minor)* | Clause 6.1.2 / 8.2 Risk assessment · 5.1 Policies | Risk Management Policy; Risk Management Methodology | A 5×5 methodology is **documented but not running** — no live, owned risk register with dated entries | **Medium** (R05 · 12/25) | Designate a Risk Register Owner; maintain a live register; run quarterly risk reviews |
| **F4** | No monitoring of control performance *(NC-004, Minor)* | 8.15 Logging · 8.16 Monitoring activities · Clause 9.1 Performance evaluation | Incident Management Policy *(no KRI/KCI definitions found)* | Controls are defined, but **nothing evidences they operate** — no logging/monitoring, no KRIs or KCIs | **Medium** (R04 · 12/25) | Define a KRI/KCI framework; implement log review and monitoring; report monthly |
| **F5** | Strong policy framework — *positive observation* *(OBS-001, OFI)* | Clauses 4–10 ISMS integration · 5.1 Policies | Full 11-document policy suite | **Not a nonconformity.** Policy coverage is comprehensive but documents are standalone — opportunity to integrate under a single governance view | **Low** (improvement) | Align the suite under a centralised governance framework / dashboard |

## ISO 27001:2022 transition gaps

The 2022 revision introduced controls with no 2013 equivalent. These were assessed against current documentation and flagged for the transition. *(Mirrored in the Statement of Applicability and the Control Evidence Tracker.)*

| Control | Gap identified | Risk | Remediation |
|---------|----------------|------|-------------|
| **5.23** Cloud services security | No cloud-security policy in scope despite likely Microsoft 365 / SaaS dependency | **High** | Author a cloud-security policy; assess cloud platforms against it |
| **5.30** ICT readiness for continuity | ICT continuity / disaster recovery not covered in reviewed documentation | **High** | Develop and test an ICT continuity / DR plan |
| **8.8** Vulnerability management | No patch-management or vulnerability-scanning programme evidenced *(see Technical-Evidence)* | **High** (R07) | Implement authenticated scanning and SLA-based patch management |
| **8.9** Configuration management | No secure-baseline / hardening standard evidenced | **High** | Define and enforce secure configuration baselines |
| **8.10** Information deletion | Data retention and secure deletion not addressed — UK GDPR Art. 17 exposure | **High** (R08) | Define retention schedules and secure-deletion procedures |
| **8.16** Monitoring activities | No security monitoring evidenced *(see F4)* | **High** | Stand up monitoring and detection aligned to the SIEM |
| **8.23** Web filtering | Not referenced in the Acceptable Use or Remote Working policies | **High** | Define web-filtering controls for remote endpoints |

---

<sub>Northgate University is fictional; all findings and figures are illustrative. See the repository [README](../README.md) for context.</sub>
