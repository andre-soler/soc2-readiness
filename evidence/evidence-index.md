# Evidence Index — taskflow SOC 2 Readiness

This index maps each technical control to the evidence that supports it. Evidence
was produced across prior security engagements on taskflow's environment. In a
live engagement, each item would be a current screenshot or export; here, items
reference the project where the evidence was produced (this is a portfolio lab).

| Control | Status | Evidence | Source |
| --- | --- | --- | --- |
| CC6.1 — MFA & authentication | Met | MFA and conditional access enforced in Microsoft Entra ID; legacy auth blocked | Identity hardening project |
| CC6.2 — provisioning/deprovisioning | Partial | Access granted by role; formal offboarding record to be added | Identity project + Access Control Policy |
| CC6.3 — least privilege & review | Met | Reader-only service principal for assessments; privileged roles via PIM, activated on demand | Cloud assessment + identity project |
| CC6.6 — external access protection | Met | Network rules and Microsoft Defender for Cloud; web/API penetration test performed | Cloud assessment + app pentest |
| CC6.7 — credentials & keys | Met | Secrets stored in Azure Key Vault; app authenticates via managed identity; key rotation performed and old keys proven invalid | Secrets remediation project |
| CC6.8 — malicious/vulnerable software | Met | Container and dependency scanning (Trivy); cloud posture scanning (Prowler) | Cloud assessment + pipeline |
| CC7.1 — vulnerability detection | Met | Documented vulnerability scans: Prowler (cloud), ZAP (web/API) with triaged results | Cloud assessment + app pentest |
| CC7.2 — monitoring & alerting | Partial | Centralized logging and Defender for Cloud in place; formal SIEM and alert rules pending | Cloud assessment |
| CC7.3 — incident response | Met (policy) | Incident Response Policy defines detection, triage, containment, communication | Incident Response Policy |
| CC7.4 — containment & communication | Met (policy) | Containment runbook: disable account, rotate secret, isolate resource; demonstrated in secrets project | Incident Response Policy + secrets project |
| CC8.1 — change management | Met | CI/CD pipeline enforces code review, static analysis, dependency/IaC/secret scanning; deploy via OIDC with no stored secrets | Secrets remediation project (pipeline) |

## Notes

- "Met (policy)" means the control is now documented; the operating evidence
  (an actual incident log) accumulates over time and is what a SOC 2 Type II
  examination would review.
- Process controls (CC1–CC5, CC9) are supported by the six policies in
  `policies/`, not by technical evidence.
- Remaining gaps (CC6.2 offboarding records, CC7.2 SIEM/alerts) are tracked in
  the remediation plan.
