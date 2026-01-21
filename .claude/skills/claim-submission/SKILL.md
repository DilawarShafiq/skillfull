---
name: claim-submission
description: Claim submission guidance for CMS-1500, UB-04, and EDI 837 transactions. Use when submitting claims, troubleshooting rejections, or understanding payer requirements.
user-invocable: true
argument-hint: [claim-type-or-issue]
---

# Claim Submission Skill

Expert guidance for submitting clean claims to payers.

## When to Use

- Submitting professional (CMS-1500) claims
- Submitting institutional (UB-04) claims
- Troubleshooting claim rejections
- Understanding EDI 837 requirements
- Managing timely filing

## Claim Types

| Form | EDI | Use |
|------|-----|-----|
| CMS-1500 | 837P | Professional services |
| UB-04 | 837I | Institutional/facility |

## Clean Claim Requirements

### Required Elements
- [ ] Valid patient demographics
- [ ] Correct payer information
- [ ] Valid provider NPI
- [ ] Appropriate place of service
- [ ] Valid diagnosis codes (ICD-10)
- [ ] Valid procedure codes (CPT/HCPCS)
- [ ] Correct modifiers
- [ ] Dates of service
- [ ] Charges and units

### Common Rejection Reasons

| Code | Reason | Fix |
|------|--------|-----|
| Invalid member ID | Subscriber ID wrong | Verify with payer |
| Invalid NPI | Provider not enrolled | Check enrollment |
| Invalid diagnosis | Code doesn't exist | Verify ICD-10 |
| Duplicate claim | Already submitted | Check claim status |
| Timely filing | Past deadline | Appeal with proof |

## Timely Filing Limits

| Payer Type | Typical Limit |
|------------|---------------|
| Medicare | 12 months |
| Medicaid | Varies by state |
| Commercial | 90-365 days |

## Submission Workflow

1. Claim scrubbing (pre-submission edits)
2. Batch claims for submission
3. Submit via clearinghouse or direct
4. Receive acknowledgment (997/999)
5. Monitor for rejections
6. Correct and resubmit rejections
7. Track claim status

## KPIs

| Metric | Target |
|--------|--------|
| Clean claim rate | >95% |
| First pass resolution | >90% |
| Rejection rate | <3% |
| Timely filing compliance | 100% |

For detailed claim submission guidelines, see [reference.md](reference.md).
