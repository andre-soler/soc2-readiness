# Data Classification Policy — taskflow

**Owner:** Security Lead · **Version:** 1.0 · **Effective date:** 2026-11-09 · **Next review:** 2027-11-09
**Maps to SOC 2 Common Criteria:** CC6.1, CC6.7 (data protection)

---

## 1. Purpose and scope

This policy defines how taskflow classifies data and the protection required for each class. It applies to all company and customer data, wherever it is stored or processed.

## 2. Classification levels

| Level | Definition | Examples |
| --- | --- | --- |
| Restricted | Most sensitive; serious harm if exposed | Credentials, secrets, customer personal data |
| Confidential | Internal; harmful if exposed | Source code, internal documents, business data |
| Internal | Not public, low sensitivity | Internal wikis, non-sensitive config |
| Public | Intended to be public | Marketing site, public documentation |

## 3. Handling requirements

| Level | Requirements |
| --- | --- |
| Restricted | Encrypted at rest and in transit; access on least-privilege and need-to-know; secrets stored in Key Vault; access logged |
| Confidential | Encrypted in transit; access limited by role; not shared externally without approval |
| Internal | Access limited to staff |
| Public | No restriction |

## 4. Data at rest and in transit

- All customer and company data is encrypted at rest by the cloud platform.
- All data in transit uses TLS.
- Secrets and keys are never stored in code or configuration files; they are kept in Azure Key Vault.

## 5. Retention and disposal

Data is retained only as long as needed for the service or as required by contract or law, and is securely deleted when no longer needed.

## 6. Roles and responsibilities

| Role | Responsibility |
| --- | --- |
| Security Lead | Owns this policy and the classification scheme |
| All staff | Classify and handle data according to this policy |

## 7. Review

This policy is reviewed at least annually by the Security Lead.

