---
name: payment-posting
description: Payment posting and remittance processing guidance. Use when posting ERA/835 payments, interpreting EOBs, or managing adjustment codes.
user-invocable: true
argument-hint: [carc-code-or-scenario]
---

# Payment Posting Skill

Expert guidance for accurate posting of payments, adjustments, and remittance information.

## When to Use

- Processing ERA/835 transactions
- Interpreting EOBs
- Posting adjustments
- Reconciling deposits
- Secondary billing

## Adjustment Code Categories

| Group Code | Category | Responsibility |
|------------|----------|----------------|
| CO | Contractual Obligation | Provider write-off |
| PR | Patient Responsibility | Patient owes |
| OA | Other Adjustment | Other reasons |
| PI | Payer Initiated | Payer reduction |
| CR | Correction/Reversal | Corrects previous |

## Common CARCs

| Code | Meaning |
|------|---------|
| CO-45 | Exceeds fee schedule |
| CO-97 | Bundled with another service |
| PR-1 | Deductible |
| PR-2 | Coinsurance |
| PR-3 | Copayment |
| CO-4 | Code/modifier mismatch |

## Payment Calculation

```
Billed Amount - Allowed Amount = Contractual Adjustment
Allowed Amount - Insurance Payment = Patient Responsibility
Patient Responsibility = Deductible + Coinsurance + Copay
```

## Posting Workflow

1. Receive remittance (ERA or EOB)
2. Reconcile to bank deposit
3. Post payments to accounts
4. Apply contractual adjustments
5. Transfer to secondary or patient
6. Flag denials for follow-up
7. Balance and close batch

## KPIs

- Posting lag: <2 days
- Posting accuracy: >99%
- Auto-post rate: >80% (ERA)

For detailed CARC/RARC reference, see [reference.md](reference.md).
