---
name: medical-coding
description: US healthcare medical coding guidance for ICD-10-CM/PCS, CPT, and HCPCS. Use when working on diagnosis/procedure coding, modifier application, or NCCI compliance.
user-invocable: true
argument-hint: [code-type] [specialty]
allowed-tools: Read, Grep, mcp__icd10-codes__search_codes, mcp__icd10-codes__lookup_code, mcp__icd10-codes__validate_code
---

# Medical Coding Skill

Expert guidance for US healthcare coding using ICD-10-CM/PCS, CPT, and HCPCS code sets.

## When to Use This Skill

- Assigning diagnosis codes (ICD-10-CM)
- Coding inpatient procedures (ICD-10-PCS)
- Selecting CPT/HCPCS codes for billing
- Applying modifiers correctly
- Checking NCCI edits and bundling rules

## Quick Reference

### Code Set Overview

| Code Set | Use | Structure |
|----------|-----|-----------|
| ICD-10-CM | Diagnoses | 3-7 alphanumeric |
| ICD-10-PCS | Inpatient procedures | 7 alphanumeric |
| CPT | Outpatient procedures | 5 numeric |
| HCPCS II | DME, drugs, supplies | 1 letter + 4 digits |

### Key Modifiers

| Modifier | Description |
|----------|-------------|
| -25 | Significant, separately identifiable E/M |
| -59 | Distinct procedural service |
| -26 | Professional component |
| -TC | Technical component |
| -76/-77 | Repeat procedure same/different physician |
| -LT/-RT | Left/Right side |

## Coding Workflow

1. Review clinical documentation
2. Identify principal diagnosis/procedure
3. Select codes to highest specificity
4. Apply 7th character extensions (ICD-10)
5. Check excludes notes
6. Verify NCCI edits
7. Link diagnosis to procedure for medical necessity

## Available Actions

Use the ICD-10 lookup tools to:
- Search codes by description
- Validate code billability
- Explore code hierarchies

For detailed coding guidelines, see [reference.md](reference.md).
For specialty-specific guidance, see [specialties.md](specialties.md).
