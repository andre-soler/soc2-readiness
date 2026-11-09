# Access Control Policy — taskflow

**Owner:** Security Lead · **Version:** 1.0 · **Effective date:** 2026-11-09 · **Next review:** 2027-11-09
**Maps to SOC 2 Common Criteria:** CC6.1, CC6.2, CC6.3

---

## 1. Purpose and scope

This policy defines how access to taskflow's systems and data is granted, reviewed and removed. It applies to all employees, contractors and services that access company systems, including the Azure environment, the GitHub repositories, the CI/CD pipeline and the production application.

## 2. Principles

- **Least privilege.** Every user and service is granted the minimum access required to perform its function, and nothing more.
- **Need to know.** Access to sensitive data is limited to those who require it for their role.
- **Deny by default.** Access is granted explicitly; anything not granted is denied.
- **Accountability.** Every action is tied to an individual identity. Shared accounts are prohibited.

## 3. Authentication

- **Multi-factor authentication (MFA) is mandatory** for all users accessing company systems, enforced through Microsoft Entra ID.
- Conditional access policies restrict sign-in by risk level and block legacy authentication.
- Passwords follow the identity provider's complexity and rotation requirements. Where possible, phishing-resistant methods are preferred for administrators.
- Service-to-service authentication uses managed identities and OIDC, not stored credentials. Secrets, where unavoidable, are stored in Azure Key Vault and rotated.

## 4. Access provisioning and deprovisioning

- **Granting access.** New access is requested by the person's manager and approved by the Security Lead before it is granted. Access is assigned by role, not individually.
- **Changing access.** When a person changes role, their access is reviewed and adjusted to match the new role.
- **Removing access.** On termination or contract end, all access is revoked within one business day. This includes Entra ID accounts, GitHub access, and any third-party tools.
- Each provisioning and deprovisioning action is recorded for audit evidence.

## 5. Access review

- User access and role assignments are reviewed **quarterly**.
- Privileged access is reviewed **monthly**.
- Reviews are performed by the Security Lead; findings and any removals are recorded.

## 6. Privileged access

- Administrative access is **not permanent**. Privileged roles are activated on demand, with justification and a time limit, using Entra ID Privileged Identity Management (PIM).
- The number of standing administrators is kept to a minimum, with emergency ("break-glass") accounts held securely and monitored for any use.

## 7. Roles and responsibilities

| Role | Responsibility |
| --- | --- |
| Manager | Requests access for their reports |
| Security Lead | Approves, reviews and removes access |
| All staff | Follow this policy; do not share credentials |

## 8. Enforcement and review

- Violations of this policy may result in access removal and disciplinary action.
- This policy is reviewed at least annually, or after a significant change to the environment, by the Security Lead.
