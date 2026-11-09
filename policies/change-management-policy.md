# Change Management Policy — taskflow

**Owner:** Engineering Lead · **Version:** 1.0 · **Effective date:** 2026-11-09 · **Next review:** 2027-11-09
**Maps to SOC 2 Common Criteria:** CC8.1

---

## 1. Purpose and scope

This policy defines how changes to taskflow's software and infrastructure are proposed, reviewed, tested and deployed. It applies to all production code and infrastructure-as-code.

## 2. Principles

- No change reaches production without review and approval.
- Changes are tested before deployment.
- Every change is traceable to who made it, who approved it, and when.
- Infrastructure is changed through code (Terraform), not by hand in the console.

## 3. Change process

1. **Propose.** Changes are made on a branch and submitted as a pull request. The pull request describes what changes and why.
2. **Automated checks.** The CI/CD pipeline runs on every pull request: static code analysis, dependency scanning, infrastructure-as-code scanning, and secret scanning. A change cannot be merged while these checks fail.
3. **Review.** At least one other engineer reviews and approves the pull request before it is merged.
4. **Deploy.** Merges to the main branch trigger an automated deployment. Deployment authenticates through OIDC; no long-lived secrets are stored in the pipeline.
5. **Record.** The pull request, its approvals, and the pipeline run serve as the record of the change.

## 4. Emergency changes

Urgent fixes follow the same process where possible. If an emergency change must bypass a step, it is documented and reviewed retroactively within one business day.

## 5. Separation of duties

The person who writes a change is not the only person who approves it. Pull request approval requires a different engineer.

## 6. Roles and responsibilities

| Role | Responsibility |
| --- | --- |
| Engineer | Proposes and tests changes |
| Reviewer | Reviews and approves pull requests |
| Engineering Lead | Owns the pipeline and this policy |

## 7. Review

This policy is reviewed at least annually, or after a significant change to the pipeline, by the Engineering Lead.
