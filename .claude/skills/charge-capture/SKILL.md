---
name: charge-capture
description: Charge capture and revenue integrity guidance. Use when documenting billable services, reviewing charge entry, or preventing revenue leakage.
user-invocable: true
argument-hint: [service-type]
---

# Charge Capture Skill

Expert guidance for accurate documentation and capture of billable services.

## When to Use

- Documenting billable services
- Reviewing charge entry workflows
- Preventing unbilled services (revenue leakage)
- CDM (Charge Description Master) management
- Charge reconciliation

## Quick Reference

### Charge Capture Workflow

1. Provider documents service in EHR
2. Charges generated from documentation
3. Charge review and validation
4. Charge posting to billing system
5. Claim generation

### Common Charge Types

| Category | Examples |
|----------|----------|
| E/M Services | 99202-99215 (Office), 99221-99223 (Hospital) |
| Procedures | Based on CPT code range |
| Ancillary | Labs, radiology, therapy |
| Supplies | DME, drugs, materials |

### Revenue Integrity Checklist

- [ ] All services documented are charged
- [ ] Charges match documentation
- [ ] Correct CPT/HCPCS codes used
- [ ] Appropriate modifiers applied
- [ ] Units of service accurate
- [ ] Date of service correct

## Common Errors

| Error | Impact | Prevention |
|-------|--------|------------|
| Missing charges | Revenue loss | Reconciliation reports |
| Duplicate charges | Compliance risk | Edit checks |
| Wrong codes | Denials | Encoder validation |
| Missing modifiers | Underpayment | Auto-prompts |

## KPIs

- Charge lag: <3 days from DOS
- Charge capture rate: >98%
- Charge error rate: <2%

For detailed charge capture guidelines, see [reference.md](reference.md).
