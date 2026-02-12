# Security Architecture Decision Record  
## SAD-001 - Cloud Log Retention Strategy

---

## Decision Summary

| Attribute | Value |
|------------|--------|
| Decision ID | SAD-001 |
| Domain | Cloud / Logging |
| Status | Approved |
| Decision Owner | Head of Security Architecture |
| Approval Authority | Architecture Review Board |
| Effective Date | 2026-02-12 |
| Review Frequency | Annual |

---

## Business & Technical Context

| Category | Details |
|------------|----------|
| Problem Statement | Cloud log retention is inconsistent across services and insufficient for extended investigations. |
| Impacted Platforms | Cloud workloads, SIEM platform, archival storage |
| Business Drivers | Incident reconstruction capability, regulatory defensibility |
| Constraints | Increasing SIEM ingestion costs, storage growth, operational overhead |

---

## Risk Alignment

| Field | Details |
|--------|---------|
| Risk ID(s) | R-017, R-022 |
| Risk Description | Inability to reconstruct incidents due to insufficient historical logs |
| Threat Scenario | Delayed detection or incomplete forensic investigation following cloud compromise |
| Risk Impact | Operational disruption, regulatory exposure, investigative limitations |

---

## Options Analysis

| Option | Description | Benefits | Trade-offs / Risks |
|--------|------------|----------|--------------------|
| 1 - 90-Day Retention | Maintain short-term retention only | Lower cost | Limited forensic visibility |
| 2 - 365-Day in SIEM | Store one year of searchable logs | Full visibility | High cost, ingestion performance impact |
| 3 - Tiered Retention (Selected) | 90 days searchable + 365 days archived | Balanced cost & forensic coverage | Archived logs require restoration before analysis |

---

## Architectural Decision

| Field | Details |
|--------|----------|
| Selected Option | Option 3 - Tiered Retention Model |
| Rationale | Extends investigative window while maintaining cost control |
| Accepted Trade-offs | Archived logs are not immediately searchable; restoration required |

---

## Residual Risk Assessment

| Item | Details |
|------|----------|
| Remaining Risk | Investigation delay during archive retrieval |
| Risk Treatment | Mitigated; operational delay accepted |
| Risk Acceptance Authority | Security Architecture Lead |

---

## Control Implementation

| Control Component | Description |
|------------------|-------------|
| SIEM Retention Standard | 90-day searchable retention enforced across services |
| Log Archival | Automated export to secured, low-cost storage |
| Access Control | RBAC enforced on archive storage |
| Baseline Update | Cloud security standard updated to reflect retention policy |
| Implementation Owner | Cloud Platform Engineering |

---

## Validation & Assurance

| Validation Element | Description |
|-------------------|-------------|
| Validation Method | Quarterly configuration audit + annual archive restoration test |
| Validation Frequency | Quarterly / Annual |
| Evidence Repository | Security monitoring evidence repository |
| Escalation Path | Security Architecture → Cloud Platform Lead |

---

## Review & Re-Evaluation

| Field | Details |
|--------|---------|
| Next Review Date | 2027-02-12 |
| Review Cadence | Annual |
| Revalidation Triggers | Regulatory changes, major security incident, cost model shift, cloud platform capability changes |

---

## Related Artifacts

| Artifact Type | Reference |
|---------------|-----------|
| Architecture Diagram | Cloud Logging Architecture v1.1 |
| Policy Reference | Cloud Security Baseline Standard |
| Linked Decisions | None |
| Linked Exceptions | None |

---
