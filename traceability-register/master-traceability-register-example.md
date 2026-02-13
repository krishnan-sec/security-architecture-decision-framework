# Master Traceability Register (Enterprise Example)

| Risk ID | Risk Treatment | Decision ID | Control Name | Domain | Control Owner | Validation Method | Last Review Date | Next Review Date | Status | Exception ID |
|----------|----------------|------------|--------------|--------|----------------|------------------|------------------|------------------|--------|--------------|
| R-017, R-022 | Mitigated | SAD-001 | Tiered Cloud Log Retention (90-Day Hot + 365-Day Archive) | Cloud | Cloud Platform Engineering | Quarterly configuration audit + Annual archive restoration test | 2026-02-12 | 2027-02-12 | Active | N/A |
| R-004, R-011 | Mitigated | SAD-002 | Federated Privileged Access with JIT Elevation | Identity | IAM Team | Quarterly privileged access review + Role assignment audit | 2026-02-12 | 2027-02-12 | Active | N/A |
| R-031 | Accepted (Time-Bound) | SAD-003 | Restricted TLS 1.0 Endpoint with Compensating Controls | Network / Application | Network Security Team | Monthly configuration audit + Log review | 2026-02-12 | 2026-05-12 | Exception (Exp: 2026-12-31) | EX-014 |
