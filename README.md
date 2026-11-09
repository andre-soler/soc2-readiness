# SOC 2 Readiness Assessment

A complete SOC 2 Type I readiness engagement for a SaaS startup: control matrix,
gap analysis, core policies, evidence mapping, and a roadmap to the audit —
delivered the way a compliance consultant would deliver it.

The client "taskflow" is fictional (a portfolio lab). The technical evidence
comes from related security engagements on the same environment.

## The engagement

An enterprise customer required a SOC 2 report before signing. This assessment
measured how ready taskflow is for a SOC 2 Type I examination against the
**Security** criterion (the Common Criteria), and laid out the path to the audit.

## Result

**13 of 22 controls Met, 4 Partial, 5 Not met.** Strong technical foundation;
the remaining gaps are documentation and process, closable in 6–8 weeks.

## What's inside

| Deliverable | Location |
| --- | --- |
| Client briefing | `docs/briefing.md` |
| Control matrix (CC1–CC9) with gap analysis | `controls/control-matrix.csv` |
| Core policies (6) | `policies/` |
| Evidence index (controls → real proof) | `evidence/evidence-index.md` |
| Risk register & vendor list | `evidence/` |
| Remediation plan & roadmap to audit | `report/remediation-plan.md` |
| SOC 2 readiness report | `report/soc2-readiness-report.md` |

## The differentiator

SOC 2 readiness is usually 80% documentation. What makes this engagement
stronger is that the technical controls are backed by **real evidence** — MFA and
least privilege, secrets in a vault with rotation, a secure CI/CD pipeline,
documented vulnerability scans — from hands-on security work, not just written
policy. The evidence index maps each control to the engagement that proves it.

## Scope note

This is a readiness assessment, not an audit. A SOC 2 report is issued by a
licensed CPA firm; this work prepares the company for that examination.

## Author

André Soler — Cloud & Application Security
[LinkedIn](https://linkedin.com/in/andresolereng) · [GitHub](https://github.com/andre-soler)
