# Accounts Receivable Follow-Up Skill

## Overview
This skill covers the management and collection of outstanding insurance and patient balances to optimize cash flow for US healthcare providers.

## Key Competencies

### A/R Aging Analysis

#### Aging Buckets
| Bucket | Status | Action Priority |
|--------|--------|-----------------|
| 0-30 days | Current | Monitor |
| 31-60 days | Aging | Begin follow-up |
| 61-90 days | Delinquent | Intensive follow-up |
| 91-120 days | Seriously delinquent | Escalated action |
| 120+ days | Bad debt risk | Final efforts/write-off consideration |

#### Aging by Payer Type
- Medicare
- Medicaid
- Commercial
- Workers' Compensation
- Self-Pay
- Other government

### Insurance Follow-Up Strategies

#### Prioritization Methods
- Dollar value (high to low)
- Age (oldest first)
- Payer (by payment patterns)
- Claim status
- Likelihood of collection

#### Follow-Up Actions
1. Verify claim receipt
2. Check claim status
3. Identify pend reasons
4. Provide requested information
5. Escalate stalled claims
6. Resubmit if necessary
7. Appeal if appropriate

### Claim Status Inquiry

#### EDI 276/277 Transactions
- 276: Claim Status Request
- 277: Claim Status Response

#### Status Categories
- A0: Acknowledgment - Forwarded
- A1: Acknowledgment - Receipt
- A2: Acknowledgment - Acceptance
- A3: Acknowledgment - Rejection
- P0-P5: Pending statuses
- F0-F4: Finalized statuses
- R0-R5: Rejection statuses

### Payer Portal Utilization
- Check claim status online
- View EOBs and remittances
- Submit appeals electronically
- Request authorization status
- Verify eligibility
- Download reports

### Common A/R Issues and Resolutions

| Issue | Cause | Resolution |
|-------|-------|------------|
| No response | Claim not received | Resubmit with proof |
| In process | Pending review | Document, follow up |
| Additional info needed | Missing documentation | Submit requested items |
| Coding review | Clinical audit | Provide supporting docs |
| Authorization pending | Auth not verified | Submit auth proof |
| COB hold | Primary payment needed | Bill primary first |

### Worklist Management
- Assign accounts by payer expertise
- Set follow-up dates
- Document all actions
- Escalate unresolved issues
- Track productivity

### Phone Follow-Up Best Practices
- Prepare before calling (account info, history)
- Document payer rep name and reference number
- Ask specific questions about claim status
- Request supervisor for unresolved issues
- Confirm next steps and timeline
- Document call outcomes immediately

### Written Follow-Up
- Tracers for unresponded claims
- Demand letters for aged accounts
- Appeal letters for denials
- Provider dispute requests
- Overpayment disputes

## A/R Management Metrics

### Key Performance Indicators (KPIs)
| Metric | Target | Calculation |
|--------|--------|-------------|
| Days in A/R | <35 days | (Total A/R / Average Daily Charges) |
| A/R > 90 days | <20% | (A/R > 90 days / Total A/R) |
| Collection Rate | >95% | (Payments / Adjusted Charges) |
| Clean Claim Rate | >95% | (Clean Claims / Total Claims) |
| Denial Rate | <5% | (Denied Claims / Total Claims) |

### Productivity Standards
- Accounts worked per day
- Dollars resolved per day
- Follow-up call volume
- Appeals submitted

## Write-Off Procedures
- Timely filing write-offs
- Contractual adjustments
- Small balance write-offs
- Bad debt transfers
- Charity care adjustments

### Write-Off Authorization Levels
- Small balances: Collector approval
- Mid-range: Supervisor approval
- Large amounts: Director/CFO approval
- Bad debt: Policy-defined process

## Technology Solutions
- A/R management software
- Automated worklist generation
- Predictive analytics
- Robotic Process Automation (RPA)
- Payer portal integration
- Automated claim status checking

## Compliance Considerations
- Consistent collection efforts
- Proper bad debt procedures
- Write-off documentation
- Anti-Kickback compliance
- Fair Debt Collection Practices Act (patient balances)
