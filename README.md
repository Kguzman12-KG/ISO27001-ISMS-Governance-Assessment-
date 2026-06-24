<h1 align="center">🔐 Information Security Audit — ISO/IEC 27001</h1>

<p align="center"><em>A hands-on security &amp; compliance assessment of a fictional university — from first finding to fix-it plan.</em></p>

<p align="center">
  <img src="https://img.shields.io/badge/Assessed%20against-ISO%2FIEC%2027001%3A2022-1F3A5F?style=flat-square" alt="Assessed against ISO/IEC 27001:2022">
  <img src="https://img.shields.io/badge/Baseline-ISO%2FIEC%2027001%3A2013-6B7D9E?style=flat-square" alt="2013 baseline">
  <img src="https://img.shields.io/badge/Approach-2013%E2%86%922022%20Transition%20Gap%20Analysis-2E6E4F?style=flat-square" alt="Transition gap analysis">
  <img src="https://img.shields.io/badge/Scope-ISMS%20Tabletop%20Audit-4A4A4A?style=flat-square" alt="Scope">
</p>

---

> ### 📌 Scope &amp; versioning — read this first
> This project is a **transition-readiness gap analysis**, so two ISO 27001 versions appear **by design**:
>
> - **Current-state baseline → ISO/IEC 27001:2013.** Northgate's existing ISMS — the 11 policies — is 2013-aligned, reflecting an organisation that certified under the 2013 standard. The policies therefore cite 2013 Annex A control numbers (e.g., A.16, A.9, A.10).
> - **Assessment target → ISO/IEC 27001:2022.** The audit, Statement of Applicability, evidence tracker, and technical evidence assess readiness against the **current 2022 standard** and its 93 controls (e.g., 5.24–5.28, 8.16).
>
> Every 2013 baseline control is mapped to its 2022 equivalent in the **[2013 → 2022 Control Crosswalk](2013%To%2022/2013-to-2022-Crosswalk.md)**. The gap against the **11 controls new in 2022** is the core finding of the engagement.

---

## Reviewer Path

1. Start with the Assessment Report for the executive-level story.
2. Review the Risk Assessment & SoA to see risk scoring and ISO 27001 control decisions.
3. Review the Control Evidence Tracker to see how each control was evaluated.
4. Review the Nonconformity Log to see corrective action tracking.
5. Review the Policy Suite to see the supporting governance framework.

### What I did

I ran a full document based ISO 27001 audit simulation with risk assessment, SoA, evidence tracker, and corrective action plan of a (fictional) university: found where its data was exposed, scored each risk by the damage it could actually cause, and handed leadership a prioritized plan they could act on — plus the policy rulebook the whole program runs on. The work assesses a **2013-aligned ISMS for readiness against the ISO/IEC 27001:2022 update** — a transition gap analysis (see *Scope & versioning* above, and the [crosswalk](Assessment/2013-to-2022-Crosswalk.md)).

**At a glance:** &nbsp;`93 controls assessed`&nbsp; · &nbsp;`8 risks scored`&nbsp; · &nbsp;`5 findings (2 major)`&nbsp; · &nbsp;`11 policies authored`

### What I found

- **Strong on paper, weaker in practice.** The policies were solid, but several high-impact controls weren't actually enforced — the classic gap between *documented* and *done*.
- **Top exposures:** remote access without enforced multi-factor login, no security monitoring, and no vulnerability or patch management.
- **The output:** every gap mapped to a risk rating, a fix, and an owner — so leadership knows exactly what to tackle first.

> **Start here:** the **[Evidence Index](Assessment/Evidence_Index.md)** puts the entire assessment on one screen — every finding mapped to its control, evidence, gap, risk, and fix.

### Read the work

| Deliverable | What it actually does |
| --- | --- |
| **[Evidence Index](Assessment/Evidence_Index.md)** | The whole assessment on one screen — finding → control → evidence → gap → risk → fix. |
| **[Assessment Report](Assessment/ISO27001_ISMS_Assessment_Report.pdf)** | *"Here's what we found, and what to fix first"* — the full narrative in one document. |
| **[Risk Assessment & Statement of Applicability](Assessment/ISO27001_Risk_Assessment_and_SoA.xlsx)** | Every way things could go wrong, how bad each would be, and which of the 93 standard safeguards apply — with the reasoning. |
| **[Control Evidence Tracker](Assessment/ISO27001_Control_Evidence_Tracker.xlsx)** | What's genuinely in place versus what's missing. |
| **[Non-Conformity Log](Assessment/NonConformity_Log.xlsx)** | The official list of gaps — each with an owner and a path to "resolved." |
| **[2013 → 2022 Crosswalk](Assessment/2013-to-2022-Crosswalk.md)** | Every 2013 baseline control mapped to its 2022 equivalent — the transition map that ties the two layers together. |
| **[Technical Evidence](Technical%20Evidence/)** | Sample MFA, monitoring, and vulnerability reviews — how each finding is tested and concluded *(illustrative)*. |
| **[Policy Suite (×11)](Policies)** | The rulebook the entire program runs on. |

> 📊 **No download needed.** The spreadsheets are also published as **CSV** in the [`Assessment/`](Assessment) folder — GitHub renders them as sortable, searchable tables right in your browser.

### Why this is the job

Strong security isn't a pile of technical controls — it's being able to tell leadership, in plain language, **what could hurt the organization, how likely it is, and what to do about it.** That translation *is* the work. This project is a sample of it.

---

<sub>**Fictional by design.** "Northgate University" and every name, finding, and figure here is invented to demonstrate method and communication not to describe any real organization.</sub>

<sub>**Kelvin Guzman** · <a href="https://www.linkedin.com/in/kelvin-guzman-95896a215">LinkedIn</a></sub>
