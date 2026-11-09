# Briefing — taskflow SOC 2 Readiness

> Fictional client (lab project). Discovery notes — November 9, 2026.

## 1. The client

- **Product:** taskflow — a project-management SaaS (B2B).
- **Team:** small startup, a handful of developers, no dedicated security or compliance staff.
- **Stack:** runs in the cloud (Azure), CI/CD on GitHub, data in a managed database.

## 2. Why now

- An enterprise customer requires a **SOC 2 report** before signing.
- The deal is on hold until taskflow can show it is on the path to SOC 2.
- No formal security program exists yet: practices are in people's heads, not written down.

## 3. Current state

- Some strong technical controls are already in place from earlier work:
  - MFA and least-privilege access (Entra ID).
  - Secrets in Key Vault, no credentials in code, rotation in place.
  - Centralized logging and Microsoft Defender for Cloud.
  - Secure CI/CD pipeline with secret scanning and OIDC (no stored secrets).
- What is missing: written policies, a control matrix, evidence organized for an auditor, and a formal gap assessment.

## 4. Goal of this engagement

- **SOC 2 Type I readiness** for the **Security** criterion (Common Criteria).
- Deliverables: control matrix with gap analysis, core policies, evidence mapped to controls, and a roadmap to the audit.
- Out of scope: the audit itself (performed by a licensed CPA), and the other four Trust Services Criteria.

## 5. Open questions

- Which enterprise customer, and what is their deadline?
- Is the company aiming for Type I first, then Type II? (Assumed yes.)
- Who will own each policy after the engagement?
- Is there a target date to schedule the audit?
