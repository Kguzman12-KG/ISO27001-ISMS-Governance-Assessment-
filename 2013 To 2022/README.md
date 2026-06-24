# ISO/IEC 27001 — 2013 → 2022 Control Crosswalk
### Northgate University ISMS · Transition-Readiness Assessment

**Why this document exists.** This engagement is a **transition-readiness gap analysis**. Northgate's existing ISMS is **ISO/IEC 27001:2013-aligned** — its governance policies were written against the 2013 standard, reflecting an organisation that certified under 2013. The assessment evaluates that baseline against the current **ISO/IEC 27001:2022** standard to identify the work required to transition.

Because of that, two control-numbering schemes appear in this repository **by design**:

| Layer | Standard | Where it appears |
| --- | --- | --- |
| **Current-state baseline** | ISO/IEC 27001:**2013** | The 11 policies (cite A.16, A.9, A.10, …) |
| **Assessment target** | ISO/IEC 27001:**2022** | Report, Statement of Applicability, evidence tracker, technical evidence (cite 5.24–5.28, 8.16, …) |

This crosswalk maps every 2013 control used in the policy suite to its 2022 equivalent, so nothing is orphaned across the two layers.

> ISO/IEC 27001:2013 was withdrawn on **31 October 2025**. Organisations certified under 2013 were required to transition to 2022 — exactly the scenario modelled here.

---

## 1 · Policy suite → version mapping

| # | Policy (2013 baseline) | 2013 reference | 2022 target control(s) |
| --- | --- | --- | --- |
| 01 | Information Security Policy | Clause 5.2 · A.5.1.1 | Clause 5.2 · A.5.1 |
| 02 | Risk Management Policy | Clauses 6.1.2, 6.1.3, 8.2, 8.3 | *Unchanged* — Clauses 6.1.2, 6.1.3, 8.2, 8.3 |
| 03 | Risk Management Methodology | Clauses 6.1.2, 6.1.3 | *Unchanged* — Clauses 6.1.2, 6.1.3 |
| 04 | Information Classification Policy | A.8.2 | A.5.12, A.5.13 |
| 05 | Information Asset Owners Handbook | A.8.1 | A.5.9, A.5.10 |
| 06 | Access Control Policy | A.9 | A.5.15–A.5.18, A.8.2, A.8.3, A.8.5 |
| 07 | Cryptographic Policy | A.10 | A.8.24 |
| 08 | Acceptable Use Policy | A.8.1.3 | A.5.10 |
| 09 | Remote Working Policy | A.6.2 | A.6.7, A.8.1 |
| 10 | Supplier Security Policy | A.15 | A.5.19–A.5.22 (+ A.5.23 cloud) |
| 11 | Incident Management Policy | A.16 | A.5.24–A.5.28, A.6.8 |

> Risk management (policies 02–03) is governed by the management-system **clauses**, which keep the same numbering in 2013 and 2022; only the Annex A control catalogue was restructured.

---

## 2 · Control-level crosswalk (controls cited across the suite)

| 2013 control | Title | → | 2022 control | Title |
| --- | --- | :-: | --- | --- |
| A.5.1.1 / A.5.1.2 | Policies for information security | → | A.5.1 | Policies for information security |
| A.6.2.1 | Mobile device policy | → | A.8.1 | User endpoint devices |
| A.6.2.2 | Teleworking | → | A.6.7 | Remote working |
| A.8.1.1 | Inventory of assets | → | A.5.9 | Inventory of information & associated assets |
| A.8.1.2 | Ownership of assets | → | A.5.9 | (ownership consolidated into A.5.9) |
| A.8.1.3 | Acceptable use of assets | → | A.5.10 | Acceptable use of information & associated assets |
| A.8.2.1 | Classification of information | → | A.5.12 | Classification of information |
| A.8.2.2 | Labelling of information | → | A.5.13 | Labelling of information |
| A.8.2.3 | Handling of assets | → | A.5.10 | Acceptable use of information & associated assets |
| A.8.3.2 | Disposal of media | → | A.7.10 / A.8.10 | Storage media / Information deletion |
| A.9.1.x | Business requirement for access control | → | A.5.15 | Access control |
| A.9.2.x | User access management | → | A.5.16 / A.5.18 | Identity management / Access rights |
| A.9.3.1 | Use of secret authentication information | → | A.5.17 | Authentication information |
| A.9.4.x | System & application access control | → | A.8.3 / A.8.5 | Information access restriction / Secure authentication |
| A.10.1.1 | Policy on the use of cryptographic controls | → | A.8.24 | Use of cryptography |
| A.10.1.2 | Key management | → | A.8.24 | Use of cryptography |
| A.11.2.6 | Security of equipment & assets off-premises | → | A.7.9 | Security of assets off-premises |
| A.12.4.1 / A.12.4.3 | Event logging / administrator & operator logs | → | A.8.15 | Logging |
| A.12.6.1 | Management of technical vulnerabilities | → | A.8.8 | Management of technical vulnerabilities |
| A.15.1.x | Information security in supplier relationships | → | A.5.19–A.5.21 | Supplier relationships / agreements / ICT supply chain |
| A.15.2.x | Supplier service delivery management | → | A.5.22 | Monitoring & review of supplier services |
| A.16.1.1 | Responsibilities and procedures | → | A.5.24 | Incident management planning & preparation |
| A.16.1.2 / A.16.1.3 | Reporting security events / weaknesses | → | A.6.8 | Information security event reporting |
| A.16.1.4 | Assessment of & decision on security events | → | A.5.25 | Assessment & decision on information security events |
| A.16.1.5 | Response to information security incidents | → | A.5.26 | Response to information security incidents |
| A.16.1.6 | Learning from information security incidents | → | A.5.27 | Learning from information security incidents |
| A.16.1.7 | Collection of evidence | → | A.5.28 | Collection of evidence |
| A.18.1.1 | Identification of applicable legislation | → | A.5.31 | Legal, statutory, regulatory & contractual requirements |
| A.18.1.2 | Intellectual property rights | → | A.5.32 | Intellectual property rights |
| A.18.1.4 | Privacy & protection of PII | → | A.5.34 | Privacy & protection of PII |

---

## 3 · New in 2022 — no 2013 equivalent (the transition-gap targets)

The 2022 standard introduced **11 new controls**. The assessment evaluates Northgate against these; the ones not yet met form the transition gap.

| 2022 control | Title | In Northgate's 7 gaps? |
| --- | --- | :-: |
| A.5.7 | Threat intelligence | — |
| A.5.23 | Information security for use of cloud services | ✅ |
| A.5.30 | ICT readiness for business continuity | ✅ |
| A.7.4 | Physical security monitoring | — |
| A.8.9 | Configuration management | ✅ |
| A.8.10 | Information deletion | ✅ |
| A.8.11 | Data masking | — |
| A.8.12 | Data leakage prevention | — |
| A.8.16 | Monitoring activities | ✅ |
| A.8.23 | Web filtering | ✅ |
| A.8.28 | Secure coding | — |

> **A.8.8 (Management of technical vulnerabilities)** is also one of Northgate's seven gaps. It is **not** new in 2022 — it is the renumbered 2013 control **A.12.6.1** — but it remains an open gap and is tracked alongside the new-control gaps.

---

## 4 · Structural summary

| | ISO/IEC 27001:2013 | ISO/IEC 27001:2022 |
| --- | --- | --- |
| Annex A controls | 114 | 93 |
| Control groupings | 14 domains (A.5–A.18) | 4 themes (Organizational · People · Physical · Technological) |
| New controls | — | 11 |
| Transition deadline | — | 31 October 2025 |

---

<sub>Prepared for the Northgate University ISMS transition-readiness assessment. Control titles and correspondences follow **ISO/IEC 27002:2022, Annex B**. "Northgate University" is fictional — see the repository [README](README.md).</sub>

