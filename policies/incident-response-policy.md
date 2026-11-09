# Incident Response Policy — taskflow

**Owner:** Security Lead · **Version:** 1.0 · **Effective date:** 2026-11-09 · **Next review:** 2027-11-09
**Maps to SOC 2 Common Criteria:** CC7.3, CC7.4

---

## 1. Purpose and scope

This policy defines how taskflow detects, responds to, and recovers from security incidents. It applies to all systems, staff and services.

## 2. What is a security incident

A security incident is any event that compromises, or threatens to compromise, the confidentiality, integrity or availability of company or customer data. Examples: unauthorized access, data leakage, malware, a leaked credential, or a successful attack against the application.

## 3. Severity levels

| Level | Definition | Example |
| --- | --- | --- |
| Critical | Confirmed breach of customer data or loss of a core system | Customer data exfiltrated |
| High | Likely compromise; contained but serious | Leaked production credential |
| Medium | Security event with limited impact | Suspicious login blocked by MFA |
| Low | Minor event, no data at risk | Isolated failed-login spike |

## 4. Response process

1. **Detect.** Events are surfaced through centralized logs, Microsoft Defender for Cloud alerts, and reports from staff.
2. **Report.** Anyone who suspects an incident notifies the Security Lead immediately through the agreed channel.
3. **Triage.** The Security Lead assigns a severity and decides the response.
4. **Contain.** Limit the damage: disable the affected account, rotate the exposed secret, isolate the affected resource.
5. **Eradicate and recover.** Remove the cause and restore normal operation from a known-good state.
6. **Communicate.** Notify affected parties and, where required by contract or law, customers and authorities, within the applicable timeframe.
7. **Review.** After resolution, hold a post-incident review and record lessons learned.

## 5. Roles and responsibilities

| Role | Responsibility |
| --- | --- |
| Security Lead | Leads the response; assigns severity; coordinates communication |
| All staff | Report suspected incidents promptly |
| Management | Approves external communication for Critical incidents |

## 6. Records

Every incident is logged with: date, severity, summary, actions taken, timeline (detection, containment, resolution), and the post-incident review. These records are retained as audit evidence.

## 7. Testing

The incident response process is tested at least annually through a tabletop exercise or a simulated incident, and the policy is updated based on the results.

## 8. Review

This policy is reviewed at least annually, or after a significant incident, by the Security Lead.
