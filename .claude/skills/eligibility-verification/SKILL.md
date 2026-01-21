---
name: eligibility-verification
description: Insurance eligibility and benefits verification guidance. Use when verifying patient coverage, investigating benefits, or checking prior authorization requirements.
user-invocable: true
argument-hint: [payer-or-service-type]
---

# Eligibility Verification Skill

Comprehensive guidance for insurance eligibility and benefits verification.

## When to Use

- Verifying patient insurance coverage
- Investigating specific benefits
- Checking prior authorization requirements
- Understanding coordination of benefits
- Pre-service financial clearance

## Verification Checklist

### Required Information to Verify

- [ ] Coverage effective dates
- [ ] Subscriber vs dependent status
- [ ] Primary vs secondary payer
- [ ] In-network vs out-of-network status
- [ ] Deductible (individual/family, met amount)
- [ ] Copay/coinsurance amounts
- [ ] Out-of-pocket maximum
- [ ] Benefit limitations/exclusions
- [ ] Prior authorization requirements
- [ ] Referral requirements

### Service-Specific Verification

- [ ] Covered service/benefit category
- [ ] Place of service restrictions
- [ ] Provider type restrictions
- [ ] Quantity/frequency limits
- [ ] Pre-existing condition exclusions
- [ ] Waiting periods

## EDI 270/271 Transactions

### 270 Request Elements
- Subscriber/dependent ID
- Provider NPI
- Date of service
- Service type code

### 271 Response Interpretation

| Code | Meaning |
|------|---------|
| 1 | Active coverage |
| 2 | Active, full risk capitation |
| 3 | Active, services capitated |
| 4 | Active, services not capitated |
| 5 | Active, pending investigation |
| 6 | Inactive |

## Prior Authorization Requirements

### Common Services Requiring Auth
- Advanced imaging (MRI, CT, PET)
- Specialty medications
- DME over threshold
- Outpatient surgery
- Physical/Occupational therapy
- Home health services
- Genetic testing

### Authorization Tracking
- Authorization number
- Effective dates
- Units/visits approved
- Specific codes authorized
- Expiration date

## Payer-Specific Considerations

### Medicare
- Part A: Inpatient, SNF, Home Health, Hospice
- Part B: Outpatient, Physician, DME
- Part C: Medicare Advantage plans
- Part D: Prescription drugs
- MSP (Medicare Secondary Payer) rules

### Medicaid
- State-specific benefits
- Managed care enrollment
- Spend-down requirements
- Retroactive eligibility

### Commercial
- Plan type (HMO, PPO, EPO, POS)
- Carve-out benefits
- Rider coverage
- COB rules

## Best Practices

1. Verify at scheduling AND day of service
2. Document verification details
3. Get authorization BEFORE service
4. Track authorization usage
5. Re-verify for recurring services
6. Confirm with patient on cost share

## Common Verification Errors

| Error | Prevention |
|-------|------------|
| Coverage terminated | Verify within 24-48 hours of service |
| Wrong subscriber ID | Confirm ID matches card |
| Authorization expired | Track auth dates |
| Out-of-network | Verify network status |
| Service not covered | Check specific benefits |

For detailed payer contacts and portal information, see [payer-contacts.md](payer-contacts.md).
