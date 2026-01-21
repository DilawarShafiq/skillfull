---
name: claim-scrub
description: Pre-submission claim validation and scrubbing. Use to check claims for common errors before submission, verify coding compliance, and identify potential denial risks.
user-invocable: true
disable-model-invocation: true
argument-hint: [claim-details]
allowed-tools: mcp__icd10-codes__validate_code, mcp__icd10-codes__lookup_code, mcp__npi-registry__npi_validate, mcp__cms-coverage__search_national_coverage, mcp__cms-coverage__search_local_coverage
---

# Claim Scrub Tool

Pre-submission validation to catch errors before claim submission.

## What I Check

1. **Code Validity**
   - ICD-10-CM/PCS codes exist and are billable
   - CPT/HCPCS codes are current
   - Codes are valid for date of service

2. **Medical Necessity**
   - Diagnosis supports procedure
   - LCD/NCD requirements met
   - Appropriate linkage

3. **Provider Validation**
   - NPI format valid
   - Provider active in NPPES

4. **Compliance Checks**
   - Modifier appropriateness
   - Units within MUE limits
   - NCCI bundling concerns

5. **Claim Completeness**
   - Required fields present
   - Date logic valid
   - Patient/subscriber info complete

## Usage

```
/claim-scrub
Patient: John Smith DOB: 01/15/1960
DOS: 01/20/2026
Provider NPI: 1234567893
Dx: E11.9, I10
CPT: 99214-25, 93000
```

## Scrub Workflow

For provided claim details:

1. **Validate all ICD-10 codes**
   - Check each code exists in 2026 code set
   - Verify billable (not header-only)
   - Check for required 7th characters

2. **Validate provider NPI**
   - Format and check digit validation
   - Look up in NPPES if needed

3. **Check medical necessity**
   - Search for applicable LCD/NCD
   - Verify diagnosis supports procedure

4. **Identify risks**
   - Common denial patterns
   - Missing information
   - Modifier issues

5. **Generate report**
   - Pass/Fail for each check
   - Recommendations for issues
   - Risk assessment

## Common Scrub Findings

| Issue | Risk | Resolution |
|-------|------|------------|
| Non-specific diagnosis | High | Code to highest specificity |
| Missing modifier | Medium | Add appropriate modifier |
| No LCD/NCD support | Medium | Ensure documentation supports |
| Invalid NPI format | High | Verify provider NPI |
| Unspecified laterality | Medium | Add laterality to code |

## Output Format

```
CLAIM SCRUB RESULTS
===================
Overall Status: [PASS/FAIL/WARNINGS]

CODES VALIDATED:
- E11.9 [VALID] Type 2 diabetes without complications
- I10   [VALID] Essential hypertension
- 99214 [VALID] Office visit, established, moderate MDM

MEDICAL NECESSITY:
- 99214 supported by E11.9, I10 [PASS]

PROVIDER:
- NPI 1234567893 [VALID FORMAT]

WARNINGS:
- Consider E11.65 if hyperglycemia documented
- Modifier -25 appropriate if procedure same day

RISK ASSESSMENT: LOW
```
