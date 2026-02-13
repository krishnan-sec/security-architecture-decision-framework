# Security Architecture Governance Metrics

This document defines measurable indicators used to assess the health and effectiveness of the Security Architecture Decision Framework.

The objective is to detect architectural drift, unmanaged risk acceptance, and control lifecycle gaps.

---

## 1. Decision Governance Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| % Controls Without Decision ID | Controls implemented without linked SAD | 0% |
| Average Decision Age | Mean age of active SAD records | Monitored |
| Decisions Pending Review | SADs past their review date | < 5% |
| Decisions Without Validation | Approved decisions lacking validation evidence | 0% |

---

## 2. Exception Governance Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Active Exceptions | Total open EX records | Monitored |
| Expired Exceptions | Exceptions past expiry date | 0 |
| Exceptions Without Compensating Controls | Exceptions lacking mitigation controls | 0 |
| Average Exception Duration | Mean lifespan of time-bound exceptions | Decreasing trend |

---

## 3. Risk Alignment Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Risks Without Linked Decision | Risks not mapped to a SAD | 0 |
| Decisions Without Risk Linkage | SADs missing Risk ID | 0 |
| Risk Treatment Distribution | % Mitigated vs Accepted vs Transferred | Monitored |

---

## 4. Validation & Assurance Metrics

| Metric | Description | Target |
|--------|-------------|--------|
| Controls With Defined Validation | % of controls with documented validation method | 100% |
| Validation Overdue | Controls past validation frequency | 0 |
| Failed Validation Rate | % of controls failing validation tests | Monitored |

---

## 5. Reporting Cadence

Governance metrics are reviewed:

- Monthly by Security Architecture
- Quarterly by Architecture Review Board
- Quarterly summary provided to CISO

The Traceability Register is the authoritative data source for these metrics.
