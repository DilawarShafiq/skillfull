---
name: claim-simulator
description: Interactive healthcare billing simulator. Practice coding, claim submission, and denial resolution with realistic patient scenarios validated against live APIs. Learn by doing.
user-invocable: true
disable-model-invocation: false
argument-hint: [scenario-type-or-difficulty]
allowed-tools: Read, mcp__icd10-codes__search_codes, mcp__icd10-codes__lookup_code, mcp__icd10-codes__validate_code, mcp__icd10-codes__get_hierarchy, mcp__npi-registry__npi_validate, mcp__npi-registry__npi_lookup, mcp__npi-registry__npi_search, mcp__cms-coverage__search_national_coverage, mcp__cms-coverage__search_local_coverage, mcp__cms-coverage__sad_exclusion_list
---

# Claim Simulator

> *A flight simulator for medical billing. Crash here, not in production.*

Practice the entire revenue cycle with realistic patient scenarios. Every code you choose is validated against live APIs. Every decision has consequences.

## What I Can Do

Generate interactive billing scenarios where you:
1. **Read** a clinical encounter note
2. **Code** the diagnoses and procedures
3. **Build** the claim with correct modifiers and payer info
4. **Submit** and face realistic adjudication outcomes
5. **Resolve** denials if they occur
6. **Score** your performance against best practices

All ICD-10 codes are validated in real-time. Coverage is checked against actual Medicare policies. NPI numbers are verified against NPPES.

## Usage

```
/claim-simulator                           # Random scenario
/claim-simulator beginner                  # Straightforward visit
/claim-simulator coding-challenge          # Complex coding puzzle
/claim-simulator denial-gauntlet           # Denial resolution practice
/claim-simulator coverage-maze             # Coverage determination puzzle
/claim-simulator full-cycle                # Complete revenue cycle walkthrough
/claim-simulator emergency                 # High-acuity ED scenario
```

## How It Works

When you run `/claim-simulator $ARGUMENTS`, I:

### Phase 1: Scenario Generation

I generate (or load from scenarios) a realistic patient encounter including:

```
┌─────────────────────────────────────────────┐
│              PATIENT ENCOUNTER              │
├─────────────────────────────────────────────┤
│                                             │
│  DEMOGRAPHICS                               │
│  Name, DOB, Insurance, Member ID            │
│                                             │
│  CLINICAL NOTE                              │
│  Chief complaint, HPI, exam, assessment,    │
│  plan — written like a real provider note   │
│                                             │
│  PROVIDER                                   │
│  Name, NPI (real, verifiable), specialty     │
│                                             │
│  SETTING                                    │
│  Office / ED / Inpatient / ASC              │
│                                             │
└─────────────────────────────────────────────┘
```

### Phase 2: Interactive Challenges

I walk you through each step, asking you to make decisions:

**Round 1 — Diagnosis Coding**
> "Based on the clinical note, what ICD-10-CM codes would you assign?"
> "Which code should be sequenced first?"

I validate your answers against the ICD-10 API and explain any issues.

**Round 2 — Procedure Coding**
> "What CPT/HCPCS codes describe the services rendered?"
> "Are any modifiers needed?"

I check for NCCI edits, bundling issues, and MUE limits.

**Round 3 — Claim Building**
> "What claim form is appropriate? (CMS-1500 vs UB-04)"
> "What place of service code?"
> "What's the billing provider NPI?"

I verify the NPI against NPPES and check payer requirements.

**Round 4 — Adjudication**
Based on your coding and claim decisions, the scenario generates realistic outcomes:
- **Clean claim**: Paid correctly — great work!
- **Partial denial**: Some lines denied — can you identify why?
- **Full denial**: What went wrong and how do you appeal?

**Round 5 — Resolution** (if denied)
> "The claim was denied with CARC CO-11. What's your next step?"

I guide you through the appeal or correction process.

### Phase 3: Scoring & Debrief

```
┌─────────────────────────────────────────────┐
│             SIMULATION RESULTS              │
├─────────────────────────────────────────────┤
│                                             │
│  Coding Accuracy ........... ██████████ 95% │
│  Sequencing ................ █████████░ 90% │
│  Modifier Usage ............ ████████░░ 80% │
│  Claim Accuracy ............ ██████████ 100%│
│  Denial Resolution ......... █████████░ 90% │
│                                             │
│  REVENUE CAPTURED: $342.00 / $385.00        │
│  REVENUE LEAKAGE: $43.00 (11.2%)            │
│                                             │
│  KEY TAKEAWAYS:                             │
│  1. Remember to code CKD stage with DM      │
│  2. Modifier 25 was needed for separate E/M │
│  3. Good catch on the bundling edit          │
│                                             │
│  CERTIFICATION PREP:                        │
│  This scenario tests CPC domains:           │
│  - ICD-10-CM Guidelines (Section I.A)       │
│  - E/M Coding (CPT Guidelines)              │
│  - NCCI Edits (CMS Policy)                  │
│                                             │
└─────────────────────────────────────────────┘
```

## Scenario Types

### Beginner — "The Clean Claim"
- Established patient, single problem
- Standard commercial insurance
- Teaches: Basic E/M coding, ICD-10 selection, claim form basics

### Coding Challenge — "The Coding Trap"
- Complex patient with multiple comorbidities
- Combination codes, manifestation codes, external causes
- Teaches: Sequencing rules, specificity, coding guidelines

### Denial Gauntlet — "Run the Gauntlet"
- Scenario designed to trigger common denial reasons
- CO-4, CO-11, CO-16, CO-50, CO-97 challenges
- Teaches: Denial prevention, root cause analysis, appeal strategies

### Coverage Maze — "The Coverage Puzzle"
- Service with complex Medicare coverage requirements
- LCD/NCD conditions, prior authorization traps
- Teaches: Coverage research, medical necessity, documentation

### Full Cycle — "From Cradle to Grave"
- Complete revenue cycle from registration to final payment
- Multiple payer scenarios, coordination of benefits
- Teaches: End-to-end RCM workflow, handoff points

### Emergency — "The ED Gauntlet"
- High-acuity emergency department visit
- Critical care, procedures, split billing, observation
- Teaches: ED coding, facility vs professional billing, time-based coding

## Difficulty Modifiers

Add these to any scenario type:

| Modifier | Effect |
|----------|--------|
| `+medicare` | Patient has Medicare (adds coverage complexity) |
| `+dual-eligible` | Medicare + Medicaid (coordination of benefits) |
| `+workers-comp` | Workers' compensation scenario |
| `+surgical` | Add surgical procedure to encounter |
| `+pediatric` | Pediatric patient (age-specific codes) |
| `+mental-health` | Behavioral health components |

Example: `/claim-simulator coding-challenge +medicare +surgical`

## Learning Modes

### Practice Mode (default)
- Hints available on request
- Explanations after each round
- No time pressure

### Exam Mode
Add `exam` to simulate certification testing:
- No hints
- Timed responses
- Final score mapped to CPC/CCS exam domains

Example: `/claim-simulator exam coding-challenge`

## Validation Pipeline

Every scenario uses **live API validation**:

```
Your Answer
    │
    ▼
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│  ICD-10 API  │     │  NPI API     │     │  CMS API     │
│              │     │              │     │              │
│ Code exists? │     │ NPI valid?   │     │ Covered?     │
│ Billable?    │     │ Active?      │     │ LCD/NCD?     │
│ Sequencing?  │     │ Specialty?   │     │ SAD list?    │
└──────┬───────┘     └──────┬───────┘     └──────┬───────┘
       │                    │                    │
       ▼                    ▼                    ▼
┌─────────────────────────────────────────────────────────┐
│                   ADJUDICATION ENGINE                   │
│                                                         │
│  Applies: NCCI edits, MUE limits, LCD conditions,       │
│  payer rules, modifier logic, bundling checks           │
└─────────────────────────────────────────────────────────┘
       │
       ▼
   RESULT: Pay / Deny / Reduce
```

## Tips

- Read the clinical note carefully — every detail matters
- Think about specificity: laterality, severity, episode of care
- Consider what documentation would support your coding choices
- Remember: the simulator uses real codes, real policies, real NPI data
- Use `/icd10-lookup`, `/coverage-check`, or `/npi-verify` anytime for help

For pre-built scenarios, see [scenarios.md](scenarios.md).
