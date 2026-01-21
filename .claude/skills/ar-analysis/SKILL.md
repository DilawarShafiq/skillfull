---
name: ar-analysis
description: Accounts receivable analysis and follow-up guidance. Use when analyzing A/R aging, prioritizing follow-up, or developing collection strategies.
user-invocable: true
argument-hint: [aging-bucket-or-analysis-type]
allowed-tools: mcp__mimilabs__mimilabs_data
---

# Accounts Receivable Analysis Skill

Expert guidance for A/R management and collection optimization.

## What I Can Do

1. **Analyze A/R aging**: Interpret aging buckets and trends
2. **Prioritize follow-up**: Recommend worklist strategies
3. **Calculate metrics**: Days in A/R, collection rates
4. **Identify issues**: Bad debt risk, payer trends

## A/R Aging Buckets

| Bucket | Priority | Typical Action |
|--------|----------|----------------|
| 0-30 days | Low | Monitor for payment |
| 31-60 days | Medium | Initial follow-up |
| 61-90 days | High | Active follow-up |
| 91-120 days | Critical | Escalated follow-up |
| 120+ days | Urgent | Final efforts/write-off review |

## Key Performance Indicators

### Days in A/R
```
Formula: (Total A/R / Average Daily Charges)

Benchmarks:
- Excellent: < 35 days
- Good: 35-45 days
- Needs Improvement: 45-55 days
- Poor: > 55 days
```

### Collection Rate
```
Net Collection Rate = (Payments / (Charges - Contractual Adjustments)) x 100

Target: > 95%
```

### A/R Over 120 Days
```
Target: < 15% of total A/R
```

## Follow-Up Prioritization

### High Priority
- High dollar claims
- Claims approaching timely filing
- Payers with payment patterns
- Claims with pending appeals

### Medium Priority
- Claims in 61-90 day bucket
- Claims with missing information
- Secondary billing pending

### Lower Priority
- Patient responsibility (small balance)
- Claims in early buckets
- Claims with expected processing time

## EDI 276/277 Claim Status

### Status Category Codes
- A = Acknowledgement
- P = Pending
- F = Finalized
- R = Rejected
- E = Error

### Common Status Codes
- 0 = Accepted for processing
- 4 = Pended for review
- 20 = Invalid data
- 33 = Claim not found
- 65 = Claim processing

## Payer Analysis

### Metrics by Payer
- Average days to payment
- Denial rate by payer
- Clean claim rate
- First-pass resolution rate

### Red Flags
- Increasing days to pay
- Rising denial rates
- Unusual adjustment patterns
- Payment timing changes

## Collection Strategies

### Payer Collections
1. Verify claim received
2. Obtain claim status
3. Identify delays/issues
4. Escalate as needed
5. Appeal if appropriate
6. Document all contacts

### Patient Collections
1. Clear statements
2. Multiple payment options
3. Payment plans
4. Financial assistance screening
5. Early intervention

## Write-Off Considerations

### When to Consider Write-Off
- Timely filing expired (all options exhausted)
- Patient deceased, no estate
- Balance below cost to collect
- Bankruptcy discharged debt
- Charity care qualified

### Documentation Required
- Collection efforts documented
- Approval per policy
- Reason code assignment
- Proper adjustment posting

For healthcare spending benchmarks and data analysis, I can query the mimilabs healthcare datasets.
