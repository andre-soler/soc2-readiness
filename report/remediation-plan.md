# Remediation Plan & Roadmap to Audit — taskflow

**Prepared by:** André Soler · **Date:** 2026-11-09
**Target:** SOC 2 Type I readiness (Security / Common Criteria)

---

## 1. Where taskflow stands

After this engagement, 13 of 22 assessed controls are **Met**, 4 are **Partial**, and 5 are **Not met**. The technical foundation (access control, secrets, change management, vulnerability detection) is strong. The remaining gaps are process and documentation items that accumulate over time.

| Status | Count |
| --- | --- |
| Met | 13 |
| Partial | 4 |
| Not met | 5 |

## 2. Remaining gaps

| Control | Gap | Effort | Owner | Target |
| --- | --- | --- | --- | --- |
| CC6.2 | Offboarding not recorded formally | Low | Security Lead | 2 weeks |
| CC7.2 | No SIEM / formal alert rules | Medium | Security Lead | 4–6 weeks |
| CC9.1 | RTO/RPO not documented | Low | Engineering Lead | 2 weeks |
| CC1.4 | No security awareness training | Medium | Security Lead | 4 weeks |
| CC1.2 | Roles documented only informally | Low | Management | 2 weeks |
| CC3.1 | No documented risk assessment process | Low | Security Lead | 2 weeks |
| CC2.2 | No formal onboarding/acknowledgement flow | Low | Security Lead | 3 weeks |
| CC4.1 | No formal control-review cadence | Low | Security Lead | 3 weeks |
| CC5.2 | Technical procedures undocumented | Medium | Engineering Lead | 4 weeks |

## 3. Path to SOC 2 Type I

Type I is a point-in-time assessment: the auditor checks that controls are **designed and in place** on a given date. The goal is to close the gaps above, then schedule.

| Phase | Weeks | Work |
| --- | --- | --- |
| Close low-effort gaps | 1–3 | Offboarding record, RTO/RPO, role documentation, onboarding flow, risk-assessment process |
| Close medium-effort gaps | 3–6 | SIEM alerting, security training, documented procedures |
| Internal readiness review | 7 | Confirm every control has current evidence |
| Select auditor & schedule | 7–8 | Engage a licensed CPA firm for the Type I examination |
| Type I examination | 9+ | Auditor reviews controls and evidence |

## 4. After Type I: the path to Type II

Type II is what most enterprise customers ultimately want. It observes that controls **operated effectively** over a period (typically 3–12 months). There is no extra implementation — it is about running the controls consistently and collecting evidence over time:

- Perform access reviews on the defined cadence and keep the records.
- Log any incidents through the Incident Response process.
- Keep change records (pull requests, approvals) flowing from the pipeline.
- Re-run vulnerability scans on schedule and retain results.

## 5. Recommendation: evidence automation

Collecting evidence by hand over a 3–12 month Type II window is error-prone.
