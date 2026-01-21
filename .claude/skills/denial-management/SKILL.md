---
name: denial-management
description: Analyze and resolve claim denials. Use when investigating denial reasons, drafting appeals, or implementing denial prevention strategies.
user-invocable: true
argument-hint: [carc-code-or-denial-type]
allowed-tools: Read, mcp__icd10-codes__search_codes, mcp__cms-coverage__search_national_coverage, mcp__cms-coverage__search_local_coverage
---

# Denial Management Skill

Expert guidance for analyzing, appealing, and preventing claim denials.

## What I Can Do

1. **Analyze CARC codes**: Explain denial reasons and corrective actions
2. **Draft appeal letters**: Generate appeal language with supporting arguments
3. **Identify root causes**: Track patterns and recommend prevention
4. **Research coverage**: Find LCD/NCD support for appeals

## Usage

```
/denial-management CO-16
/denial-management medical necessity denial
/denial-management appeal letter for prior auth denial
```

## Quick CARC Reference

| CARC | Reason | Action |
|------|--------|--------|
| CO-4 | Modifier/code mismatch | Review modifier usage |
| CO-11 | Dx inconsistent with procedure | Check medical necessity linkage |
| CO-16 | Missing information | Resubmit with required data |
| CO-18 | Duplicate claim | Verify original payment |
| CO-29 | Timely filing expired | Appeal with proof of submission |
| CO-45 | Exceeds fee schedule | Verify contracted rate |
| CO-50 | Non-covered service | Appeal with medical necessity |
| CO-97 | Bundled service | Review NCCI edits |
| CO-197 | No authorization | Obtain retro-auth or appeal |

## Denial Categories

### Hard Denials
Cannot be corrected; must appeal or write off
- Coverage terminated
- Non-covered benefit
- Timely filing (without proof)

### Soft Denials
Can be corrected and resubmitted
- Missing information
- Coding errors
- Duplicate claims

## Appeal Process

### Medicare Appeal Levels
1. Redetermination (MAC) - 120 days
2. Reconsideration (QIC) - 180 days
3. ALJ Hearing - 60 days
4. Medicare Appeals Council - 60 days
5. Federal District Court - 60 days

### Commercial Appeals
- Follow contract-specific timelines
- Typically 60-180 days from denial

## Appeal Letter Template

See [appeal-templates.md](appeal-templates.md) for:
- Medical necessity appeal
- Prior authorization denial
- Coding error correction
- Timely filing exception

For detailed denial workflows, see [reference.md](reference.md).
