---
name: npi-verify
description: Verify and look up National Provider Identifiers (NPI). Use to validate provider credentials, find provider information, or search for providers by name/specialty/location.
user-invocable: true
disable-model-invocation: false
argument-hint: [npi-or-provider-name]
allowed-tools: mcp__npi-registry__npi_validate, mcp__npi-registry__npi_lookup, mcp__npi-registry__npi_search
---

# NPI Verification Tool

Verify and search the NPPES National Provider registry.

## What I Can Do

1. **Validate NPI format**: Check if an NPI has valid format and check digit
2. **Look up provider by NPI**: Get full provider details
3. **Search by name**: Find providers by name
4. **Search by specialty**: Find providers by taxonomy/specialty
5. **Search by location**: Find providers in a geographic area

## Usage

```
/npi-verify 1234567893
/npi-verify Dr. John Smith cardiologist
/npi-verify Mayo Clinic
/npi-verify oncologists in Boston MA
```

## Workflow

Based on your input `$ARGUMENTS`:

### If 10-digit number provided:
1. Validate NPI format and Luhn check digit
2. If valid format, look up in NPPES registry
3. Return provider details:
   - Name and credentials
   - Primary specialty
   - Practice address
   - License information
   - Active/Deactivated status

### If name/search terms provided:
1. Parse search criteria (name, specialty, location)
2. Search NPPES registry
3. Return matching providers with key details

## Provider Types

| Type | Description | Example |
|------|-------------|---------|
| NPI-1 | Individual | Physicians, nurses, therapists |
| NPI-2 | Organization | Hospitals, clinics, pharmacies |

## Important Notes

- NPI issuance does NOT guarantee current licensure
- Provider self-reports data to NPPES
- Verify credentials through state licensing boards
- Deactivated NPIs should not be used for billing

## Common Specialty Searches

- "Internal Medicine"
- "Family Practice"
- "Cardiology"
- "Oncology"
- "Orthopedic Surgery"
- "Pharmacy"
- "General Acute Care Hospital"
