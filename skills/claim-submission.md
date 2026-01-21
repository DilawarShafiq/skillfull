# Claim Submission Skill

## Overview
This skill covers the preparation and submission of clean claims to payers, including electronic and paper claim processes for US healthcare providers.

## Key Competencies

### Claim Form Types

#### CMS-1500 (Professional Claims)
- Used by physicians and non-institutional providers
- 33 data fields (boxes)
- Key fields:
  - Box 1: Type of insurance
  - Box 11: Insured's policy/group number
  - Box 21: ICD-10-CM diagnosis codes (A-L)
  - Box 24: Service line details (DOS, POS, CPT, modifiers, charges)
  - Box 31: Provider signature
  - Box 33: Billing provider information

#### UB-04/CMS-1450 (Institutional Claims)
- Used by hospitals and institutional providers
- Form Locators (FL) structure
- Key fields:
  - FL 4: Type of Bill (TOB)
  - FL 42-43: Revenue codes and descriptions
  - FL 44: HCPCS/CPT codes
  - FL 67: Principal diagnosis
  - FL 74: Principal procedure

### Electronic Claim Submission (EDI)

#### ANSI X12 837 Transactions
- 837P: Professional claims
- 837I: Institutional claims
- 837D: Dental claims

#### Clearinghouse Functions
- Claim scrubbing and editing
- Payer-specific formatting
- Claim status tracking
- Rejection management
- Remittance receipt (835)

### Place of Service (POS) Codes
| Code | Description |
|------|-------------|
| 11 | Office |
| 21 | Inpatient Hospital |
| 22 | Outpatient Hospital |
| 23 | Emergency Room - Hospital |
| 24 | Ambulatory Surgical Center |
| 31 | Skilled Nursing Facility |
| 32 | Nursing Facility |
| 81 | Independent Laboratory |
| 02 | Telehealth |

### Type of Bill (TOB) Codes
- First digit: Type of facility
- Second digit: Bill classification
- Third digit: Frequency
- Example: 131 = Hospital Outpatient, Admit through Discharge

### Timely Filing Requirements
| Payer | Filing Deadline |
|-------|-----------------|
| Medicare | 12 months from DOS |
| Medicaid | Varies by state (90 days - 1 year) |
| Commercial | 90 days - 1 year (per contract) |
| Workers' Comp | Varies by state |

## Clean Claim Requirements
- Complete and accurate patient demographics
- Valid insurance information
- Correct provider identifiers (NPI, Tax ID)
- Appropriate diagnosis codes linked to services
- Correct CPT/HCPCS codes with modifiers
- Valid place of service
- Authorization numbers when required
- Timely submission

## Common Claim Rejections
- Invalid/missing member ID
- Invalid/missing NPI
- Duplicate claim
- Invalid diagnosis code
- Missing/invalid authorization
- Timely filing exceeded
- Invalid CPT/revenue code combination

## Claim Scrubbing Rules
- NCCI edits compliance
- Age/gender diagnosis conflicts
- Code-specific modifiers
- Units of service validation
- Diagnosis pointer verification
- Revenue code/CPT compatibility

## Submission Workflow
1. Charge entry and coding complete
2. Claim generation from billing system
3. Pre-submission claim scrubbing
4. Electronic submission to clearinghouse
5. Clearinghouse validation
6. Payer receipt confirmation
7. Status monitoring
8. Rejection/denial management

## Key Performance Indicators (KPIs)
- Clean claim rate (target: >95%)
- First-pass resolution rate
- Claim rejection rate
- Days in A/R
- Electronic claim submission rate

## Compliance Considerations
- False Claims Act
- Anti-Kickback Statute
- Accurate billing representations
- Medical necessity documentation
- Proper use of modifiers
