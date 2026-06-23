# 01 — MFA & Conditional Access Review

**Finding reference:** F1 / NC-001 (Major) · **Controls:** 6.7 Remote working, 5.15 Access control, 8.5 Secure authentication

---

### Objective
Confirm that multi-factor authentication (MFA) is **enforced** — not merely required on paper — for all remote and administrative access, in line with the Remote Working Policy and Access Control Policy.

### Evidence requested
- Conditional Access policy export (Entra ID) covering remote / untrusted-network sign-ins
- Sign-in logs for a representative 30-day window
- Named-locations / trusted-network configuration
- List of any MFA exclusions or break-glass accounts

### What "good" looks like
- A Conditional Access policy in **`enabled`** state (not report-only) that requires MFA for all users from untrusted networks
- Sign-in logs showing the MFA claim satisfied on remote sessions
- Exclusions limited to monitored, justified break-glass accounts

### Sample evidence reviewed *(simulated)*

Conditional Access policy export — note the state:

```jsonc
{
  "displayName": "Require MFA for remote access",
  "state": "reportOnly",                 // ← not enforcing; report-only
  "conditions": {
    "users":        { "includeUsers": ["All"] },
    "applications": { "includeApplications": ["All"] },
    "locations":    { "includeLocations": ["All"],
                      "excludeLocations": ["Trusted-Campus-Network"] }
  },
  "grantControls": { "builtInControls": ["mfa"], "operator": "OR" }
}
```

Sign-in log review (KQL) — count remote sign-ins completed with single factor:

```kusto
SigninLogs
| where TimeGenerated > ago(30d)
| where NetworkLocationDetails !has "Trusted-Campus-Network"
| extend mfa = tostring(AuthenticationRequirement)
| where mfa == "singleFactorAuthentication"
| summarize remote_singlefactor_signins = count() by UserPrincipalName
| order by remote_singlefactor_signins desc
```

Representative result: **312 remote sign-ins over 30 days completed with single-factor authentication**; the Conditional Access policy intended to require MFA was left in **report-only** mode.

### Finding
The control exists in policy, but **enforcement is absent**. The Conditional Access policy that would require MFA is not enabled, and sign-in records show remote sessions authenticating with a single factor. This is the gap between *documented* and *operating*.

### Audit conclusion
**Major nonconformity (NC-001).** Remediation: move the Conditional Access policy from report-only to **enabled**; scope it to all users on untrusted networks; restrict and monitor exclusions; re-run the sign-in query to confirm 100% MFA coverage on remote access.

---

<sub>Illustrative content for a fictional organization. Configuration and log values are simulated for demonstration.</sub>
