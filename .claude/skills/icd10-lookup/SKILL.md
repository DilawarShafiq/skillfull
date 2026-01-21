---
name: icd10-lookup
description: Look up ICD-10 diagnosis or procedure codes. Use when you need to find, validate, or get details on specific ICD-10-CM or ICD-10-PCS codes.
user-invocable: true
disable-model-invocation: false
argument-hint: [code-or-description]
allowed-tools: mcp__icd10-codes__search_codes, mcp__icd10-codes__lookup_code, mcp__icd10-codes__validate_code, mcp__icd10-codes__get_hierarchy, mcp__icd10-codes__get_by_category
---

# ICD-10 Code Lookup

Interactive tool for searching and validating ICD-10 codes.

## What I Can Do

1. **Search by description**: Find codes matching clinical terms
2. **Look up specific code**: Get full details for a known code
3. **Validate billability**: Check if code is valid for HIPAA transactions
4. **Explore hierarchy**: See related codes in a category

## Usage

```
/icd10-lookup diabetes with complications
/icd10-lookup E11.65
/icd10-lookup appendectomy procedure
```

## Workflow

Based on your input `$ARGUMENTS`:

1. If it looks like a code (alphanumeric 3-7 chars):
   - Look up the specific code
   - Validate billability status
   - Show full description and hierarchy

2. If it's a description:
   - Search ICD-10-CM for diagnosis matches
   - Search ICD-10-PCS if procedure-related
   - Return top matches with billability status

3. Show related codes in the same category

## Code Types

| Type | Use | Example |
|------|-----|---------|
| ICD-10-CM | Diagnoses | E11.65 (Type 2 diabetes with hyperglycemia) |
| ICD-10-PCS | Inpatient procedures | 0DTJ4ZZ (Resection of appendix, percutaneous endoscopic) |

## Tips

- Use specific terms for better results
- Include laterality (left, right, bilateral)
- Specify acute vs chronic
- Include complication details

## Common Searches

- "type 2 diabetes" - Endocrine diagnoses
- "hypertension" - Cardiovascular conditions
- "appendectomy" - Surgical procedures
- "fracture femur" - Injury codes
