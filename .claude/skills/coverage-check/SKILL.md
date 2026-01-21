---
name: coverage-check
description: Check Medicare coverage policies (NCDs and LCDs). Use when determining if a service is covered by Medicare, finding coverage requirements, or researching prior authorization needs.
user-invocable: true
disable-model-invocation: false
argument-hint: [service-or-diagnosis]
allowed-tools: mcp__cms-coverage__search_national_coverage, mcp__cms-coverage__search_local_coverage, mcp__cms-coverage__get_coverage_document, mcp__cms-coverage__batch_get_ncds, mcp__cms-coverage__get_contractors
---

# Medicare Coverage Check

Research Medicare Part B coverage policies for medical services.

## What I Can Do

1. **Search NCDs**: Find National Coverage Determinations
2. **Search LCDs**: Find Local Coverage Determinations by region
3. **Get coverage details**: Full policy text and requirements
4. **Find contractors**: Identify regional MACs

## Usage

```
/coverage-check continuous glucose monitoring
/coverage-check hyperbaric oxygen therapy
/coverage-check cardiac rehabilitation
/coverage-check DME wheelchair
```

## Workflow

For `$ARGUMENTS`:

1. Search National Coverage Determinations (NCDs)
2. Search Local Coverage Determinations (LCDs)
3. Compile coverage requirements:
   - Covered indications
   - Medical necessity criteria
   - Documentation requirements
   - Frequency limitations
   - Prior authorization needs

## Coverage Scope

### Part B (What This Tool Covers)
- Outpatient procedures
- Durable Medical Equipment (DME)
- Lab tests and diagnostics
- Injectable drugs (J-codes)
- Physician services

### NOT Covered Here
- Part D oral prescription drugs
- Part A inpatient hospital stays
- Part C Medicare Advantage specifics

## Document Types

| Type | Scope | Description |
|------|-------|-------------|
| NCD | National | CMS-wide coverage policy |
| LCD | Regional | MAC-specific coverage |
| Article | Regional | Billing/coding guidance |
| CAL | National | Coverage advisory letter |

## Common Coverage Questions

- "Is [service] covered by Medicare?"
- "What are the medical necessity requirements for [procedure]?"
- "What diagnosis codes support coverage for [service]?"
- "Are there frequency limitations for [treatment]?"

## Tips

- NCDs override LCDs when both exist
- LCDs can be more restrictive than NCDs
- Check both national and local policies
- Review associated billing articles for coding guidance
