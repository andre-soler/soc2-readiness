# SOC 2 Readiness Report — taskflow

**Prepared by:** André Soler · **Date:** 2026-11-09
**Scope:** SOC 2 Security criterion (Common Criteria), Type I readiness
**Client:** taskflow (fictional — portfolio lab)

---

## 1. Executive summary

taskflow engaged a security consultant to assess its readiness for a SOC 2 Type I examination, driven by an enterprise customer that requires a SOC 2 report before signing.

The assessment covered the **Security** criterion (the Common Criteria), which is mandatory for every SOC 2 report. Twenty-two controls were assessed against what an auditor would expect to see.

**Result: taskflow has a strong technical security foundation and is close to Type I readiness.** The gaps that remain are documentation and process, not technology — and most can be closed in six to eight weeks.

| Status | Count | Meaning |
| --- | --- | --- |
| Met | 13 | Control in place with evidence |
| Partial | 4 | Partially in place; needs formalizing |
| Not met | 5 | Needs to be implemented |

Technical controls — access, secrets, change management, vulnerability detection — are largely **Met**, backed by real evidence from prior security work. The open items are process controls: formal risk assessment cadence, security training, SIEM alerting, and a few records.

## 2. What was assessed

The engagement delivered:

- A **control matrix** mapping all nine Common Criteria groups (CC1–CC9) to what the auditor expects (`controls/control-matrix.csv`).
- A **gap analysis** rating each control Met / Partial / Not met.
- Six **core policies** (`policies/`): Information Security, Access Control, Incident Response, Change Management, Vendor Management, Data Classification.
- An **evidence index** linking technical controls to real proof (`evidence/evidence-index.md`).
- A **risk register** and **vendor list** (`evidence/`).
- A **remediation plan and roadmap to audit** (`report/remediation-plan.md`).

## 3. Strengths

taskflow already meets the controls that are hardest to retrofit:

- **Access control (CC6):** MFA enforced via Entra ID, least privilege, privileged access through PIM, secrets in Key Vault with rotation.
- **Change management (CC8):** every change goes through pull-request review and an automated pipeline that scans code, dependencies, IaC and secrets, and deploys without stored credentials.
- **Vulnerability detection (CC6.8, CC7.1):** documented cloud and application scanning.

These are supported by evidence from prior engagements, not just by policy.

## 4. Gaps and plan

Nine gaps remain, each with an owner and a target date in the remediation plan. The highest-value next steps:

1. Document the risk-assessment process and role responsibilities (low effort).
2. Record offboarding and RTO/RPO (low effort).
3. Stand up SIEM alerting and a security-training flow (medium effort).

Full detail, timeline and the path to the Type I examination are in `report/remediation-plan.md`.

## 5. Recommendations

- **Close the low-effort gaps first** to maximize the Met count quickly.
- **Engage a licensed CPA firm** for the Type I examination once the internal readiness review passes. (The audit itself is performed by a CPA, not by this consultant.)
- **Plan for Type II**: adopt a compliance-automation platform (Vanta, Drata) to collect operating evidence continuously over the observation window.

## 6. Scope and limitations

- This engagement covered the Security criterion only. The other four Trust Services Criteria (Availability, Processing Integrity, Confidentiality, Privacy) were out of scope.
- This is a readiness assessment, not an audit. The SOC 2 report is issued by a licensed CPA firm.
- taskflow is a fictional client used for a portfolio project; the environment and evidence come from related lab engagements.
