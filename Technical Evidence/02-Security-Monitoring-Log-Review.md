# 02 — Security Monitoring & Log Review

**Finding reference:** F4 / NC-004 (Minor) · **Controls:** 8.15 Logging, 8.16 Monitoring activities, Clause 9.1

---

### Objective
Determine whether security-relevant events are **collected, monitored, and reviewed** — and whether detections can actually fire — rather than assuming the ISMS's controls operate unseen.

### Evidence requested
- List of log sources connected to the SIEM (e.g., Microsoft Sentinel)
- Active analytic / detection rules
- Alert and incident history for the review window
- Records of periodic log review (who reviews what, how often)

### What "good" looks like
- Key sources ingested: identity sign-ins, audit logs, endpoint, and network
- Detection rules mapped to priority risks, with a tuned alert history
- Documented, scheduled review with named owners and KRIs/KCIs

### Sample evidence reviewed *(simulated)*

Detection logic an auditor would expect to see in place — e.g., failed-logon spikes:

```kusto
SigninLogs
| where TimeGenerated > ago(1h)
| where ResultType != 0                       // failed sign-ins
| summarize failures = count() by UserPrincipalName, IPAddress, bin(TimeGenerated, 5m)
| where failures >= 10                         // brute-force / password-spray signal
| order by failures desc
```

…and privileged-role changes:

```kusto
AuditLogs
| where TimeGenerated > ago(24h)
| where OperationName has "Add member to role"
| project TimeGenerated, InitiatedBy, TargetResources, Result
```

Representative result: **no SIEM workspace, no analytic rules, and no log-review records were provided.** Logs may exist at source, but nothing evidences they are aggregated, monitored, or reviewed.

### Finding
Controls are defined across the policy suite, but there is **no visibility into whether they operate**. Without log aggregation, detections, or KRIs/KCIs, control failures would go unnoticed — the issue raised as F4.

### Audit conclusion
**Minor nonconformity (NC-004).** Remediation: connect priority log sources to a SIEM; deploy detections for the highest risks (failed-logon spikes, privileged-role changes, impossible travel); define a KRI/KCI framework and a monthly review with named owners. This also closes 2022 control **8.16 (Monitoring activities)**.

---

<sub>Illustrative content for a fictional organization. Queries are representative; results are simulated for demonstration.</sub>
