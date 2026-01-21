# Payment Posting Skill

## Overview
This skill covers the accurate posting of payments, adjustments, and remittance information to patient accounts for US healthcare providers.

## Key Competencies

### Electronic Remittance Advice (ERA/835)
- Receive and process 835 transactions
- Auto-posting rules and exceptions
- Reconcile ERA to EFT deposits
- Handle split payments and take-backs
- Manage ERA enrollment with payers

### Explanation of Benefits (EOB) Processing
- Manual posting from paper EOBs
- Interpret payer payment decisions
- Post allowed amounts and adjustments
- Apply patient responsibility
- Identify denial reason codes

### Payment Types

#### Insurance Payments
- Primary payer payments
- Secondary/tertiary payer payments
- Coordination of Benefits (COB) processing
- Capitation payments
- Value-based payments

#### Patient Payments
- Copayments
- Coinsurance
- Deductible payments
- Self-pay/uninsured payments
- Payment plans

### Adjustment Codes and Categories

#### Claim Adjustment Reason Codes (CARC)
| Code | Category | Description |
|------|----------|-------------|
| CO | Contractual Obligation | Provider write-off per contract |
| PR | Patient Responsibility | Patient owes this amount |
| OA | Other Adjustment | Other reasons |
| PI | Payer Initiated | Payer-initiated reductions |
| CR | Correction/Reversal | Corrects previous payment |

#### Common CARCs
- CO-45: Charge exceeds fee schedule/maximum allowable
- CO-97: Payment included in another service
- PR-1: Deductible amount
- PR-2: Coinsurance amount
- PR-3: Copayment amount
- CO-4: Procedure code inconsistent with modifier

### Remittance Advice Remark Codes (RARC)
- Provides additional explanation
- N-codes: General information
- M-codes: Alert
- MA-codes: Medicare specific

### Posting Workflow
1. Receive remittance (ERA or paper EOB)
2. Reconcile to bank deposit
3. Post payments to patient accounts
4. Apply contractual adjustments
5. Transfer balance to secondary payer or patient
6. Identify and flag denials for follow-up
7. Balance batch and close

### Contractual Adjustment Calculations
```
Billed Amount - Allowed Amount = Contractual Adjustment
Allowed Amount - Insurance Payment = Patient Responsibility
Patient Responsibility = Deductible + Coinsurance + Copay + Non-Covered
```

### Common Posting Errors
- Posting to wrong patient account
- Incorrect adjustment codes
- Missing contractual adjustments
- Incorrect patient balance transfers
- Posting wrong payment amount
- Not identifying denials
- Batch out of balance

## Payment Reconciliation
- Daily deposit reconciliation
- Bank statement matching
- Unidentified payment resolution
- Credit balance identification
- Refund processing

## Secondary Billing
- Automatic crossover (Medicare/Medicaid)
- Manual secondary claim submission
- COB payment posting
- Tertiary payer processing

## Key Performance Indicators (KPIs)
- Payment posting lag (target: <2 days)
- Posting accuracy rate
- Unposted payments
- Credit balance aging
- Auto-posting rate (for ERAs)

## Technology Solutions
- ERA auto-posting rules
- Payment matching algorithms
- Batch posting tools
- Lockbox integration
- Credit card processing integration

## Compliance Considerations
- Accurate contractual adjustments
- Proper credit balance management
- Timely refund processing
- Audit trail maintenance
- HIPAA security for payment data
