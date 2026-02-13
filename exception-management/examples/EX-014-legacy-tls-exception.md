# Security Exception Record  
## EX-014 - Temporary TLS 1.0 Protocol Exception

---

## Exception Summary

| Attribute | Value |
|------------|--------|
| Exception ID | EX-014 |
| Related Decision ID | SAD-003 |
| Domain | Network / Application Security |
| Status | Approved (Active) |
| Requesting Owner | Application Platform Team |
| Approval Authority | CISO |
| Effective Date | 2026-02-12 |
| Expiry Date | 2026-12-31 |

---

## Business & Technical Context

| Category | Details |
|------------|----------|
| Control Impacted | Enforcement of TLS 1.2+ only standard |
| Reason for Exception | Legacy application integration requires TLS 1.0 support |
| Business Justification | Prevent disruption of critical partner integration and contractual obligations |
| Constraint Type | Vendor / Technical Limitation |

The vendor has committed to supporting TLS 1.2+ in the next major release. Upgrade timeline is currently Q4 2026.

---

## Risk Assessment

| Field | Details |
|--------|---------|
| Related Risk ID(s) | R-031 |
| Risk Description | Use of deprecated TLS protocol exposes system to cryptographic exploitation |
| Threat Exposure | Potential man-in-the-middle or downgrade attack on restricted endpoint |
| Risk Treatment | Accepted (Time-Bound) with Compensating Controls |

Residual exposure is limited to a single integration endpoint.

---

## Compensating Controls

| Control | Description | Owner |
|----------|------------|--------|
| Network Segmentation | Restrict TLS 1.0 endpoint to specific source IP ranges | Network Security Team |
| Firewall Enforcement | Explicit allow-list rules for partner IP addresses | Network Security Team |
| Enhanced Monitoring | Real-time alerting for abnormal connection attempts | Security Operations |
| Log Review | Weekly review of connection logs | Security Operations |

---

## Validation & Monitoring

| Element | Description |
|----------|-------------|
| Monitoring Method | SIEM alerting + firewall log review |
| Review Frequency | Monthly |
| Evidence Location | Network security audit repository |
| Escalation Path | Security Architecture → CISO |

---

## Review & Closure

| Field | Details |
|--------|---------|
| Next Review Date | 2026-05-12 |
| Revalidation Trigger | Vendor upgrade availability or security advisory |
| Closure Criteria | TLS 1.2+ enforced; TLS 1.0 disabled; verification test completed |

If expiry date is reached without remediation, exception must be escalated to CISO and Architecture Review Board.

---

## Related Artifacts

| Artifact Type | Reference |
|---------------|-----------|
| Linked Decision | SAD-003 - Legacy TLS Protocol Exception |
| Traceability Register Entry | EX-014 listed under SAD-003 |
| Supporting Documentation | Cryptographic Standards Policy |

---
