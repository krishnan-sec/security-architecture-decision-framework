# Decision Records

This folder contains Security Architecture Decision Records (SAD).

A Security Architecture Decision Record documents the rationale, risk linkage, trade-offs, implementation expectations, and validation approach for a significant security decision.

It ensures that security controls are deliberate, traceable, and defensible over time.

---

## When to Create a Decision Record

A Decision Record should be created when:

- Introducing a new security control  
- Making a material change to an existing control  
- Accepting or transferring risk  
- Choosing between competing architectural approaches  
- Granting a structural (non-temporary) exception  

If a decision impacts risk posture, architecture, or control behavior, it should be documented.

---

## Identification & Naming

Decision Records follow the format:

SAD-### (Security Architecture Decision)

Example:
- SAD-001
- SAD-002

Each Decision ID should be unique and referenced in the Traceability Register.

---

## Lifecycle States

Each Decision Record progresses through defined states:

- Proposed  
- Under Review  
- Approved  
- Implemented  
- Validated  
- Retired  

Status should be clearly indicated within each document.

---

## Relationship to Risk & Controls

Each Decision Record must:

- Reference an existing Risk ID  
- Define the selected architectural approach  
- Identify control ownership  
- Specify validation requirements  
- Define review cadence  

Decision Records serve as the architectural layer between risk identification and control implementation.

---

This folder includes:
- The standard decision template  
- Lifecycle guidance  
- Naming conventions  
- Practical examples  
