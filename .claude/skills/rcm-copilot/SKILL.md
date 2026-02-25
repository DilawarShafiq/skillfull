---
name: rcm-copilot
description: Intelligent revenue cycle copilot. Describe any healthcare billing situation in plain English and get orchestrated, multi-step guidance using all available RCM skills and live APIs. The single entry point for the entire revenue cycle.
user-invocable: true
disable-model-invocation: false
argument-hint: [describe your billing situation]
allowed-tools: Read, Grep, Glob, mcp__icd10-codes__search_codes, mcp__icd10-codes__lookup_code, mcp__icd10-codes__validate_code, mcp__icd10-codes__get_hierarchy, mcp__icd10-codes__get_by_category, mcp__npi-registry__npi_validate, mcp__npi-registry__npi_lookup, mcp__npi-registry__npi_search, mcp__cms-coverage__search_national_coverage, mcp__cms-coverage__search_local_coverage, mcp__cms-coverage__get_coverage_document, mcp__cms-coverage__get_contractors, mcp__cms-coverage__batch_get_ncds, mcp__cms-coverage__sad_exclusion_list, mcp__mimilabs__mimilabs_data
---

# RCM Copilot

> *One command. The entire revenue cycle at your fingertips.*

The RCM Copilot is the intelligent orchestration layer for all 14 Skillfull skills. Describe any healthcare billing scenario in plain English — the Copilot figures out what you need, pulls from the right tools, and delivers a comprehensive answer.

## What Makes This Different

Traditional approach: You need to know *which* skill to use, *which* code system to check, *which* API to query.

Copilot approach: **Just describe the problem.** The Copilot handles the rest.

## What I Can Do

### 1. Scenario Analysis
Describe a patient encounter and get end-to-end guidance:
- Correct diagnosis and procedure codes (live ICD-10 validation)
- Provider credential verification (live NPI lookup)
- Medicare coverage determination (live NCD/LCD search)
- Claim form requirements and payer rules
- Denial risk assessment with prevention strategies
- Expected reimbursement analysis

### 2. Problem Resolution
Describe a billing problem and get a resolution path:
- "Claim denied for CO-16, patient has Medicare, procedure was CT abdomen"
- "Provider says they did a level 4 E/M but chart shows 2 systems reviewed"
- "Patient has both Medicare and Medicaid, had outpatient surgery"

### 3. Revenue Optimization
Ask strategic questions:
- "What's the best way to code a diabetic patient with foot ulcer and PVD?"
- "How do I maximize reimbursement for a complex wound care visit?"
- "What documentation do I need for a higher E/M level?"

### 4. Compliance Check
Verify billing decisions:
- "Can I bill 99214 and 99354 together?"
- "Is modifier 25 appropriate for this scenario?"
- "Does Medicare cover this service for this diagnosis?"

## Usage

```
/rcm-copilot patient came in for annual wellness, also had knee pain evaluated
/rcm-copilot claim denied CO-97 for CPT 29881 with 29880
/rcm-copilot new Medicare patient needs CGM coverage, what do I need?
/rcm-copilot help me code a complex laceration repair with foreign body removal
```

## How I Work

When you give me `$ARGUMENTS`, I follow this decision engine:

### Step 1: Classify the Request

I analyze your input and classify it into one or more categories:

| Category | Signals | Actions |
|----------|---------|---------|
| **Coding** | Diagnosis/procedure names, clinical terms | Search ICD-10, suggest CPT/HCPCS, check bundling |
| **Coverage** | "Does Medicare cover...", payer questions | Query NCDs/LCDs, check SAD list, verify benefits |
| **Claims** | Denial codes, form questions, submission issues | Analyze CARC/RARC, check claim requirements |
| **Provider** | NPI numbers, provider names, credentials | Validate NPI, verify taxonomy, check enrollment |
| **Financial** | Reimbursement, A/R, collections, payment | Analyze payment data, calculate KPIs |
| **Compliance** | Bundling, modifiers, medical necessity | Check NCCI edits, review documentation requirements |

### Step 2: Gather Intelligence

For each identified category, I query the relevant live APIs:

```
Coding       → icd10-codes MCP (search, validate, hierarchy)
Coverage     → cms-coverage MCP (NCDs, LCDs, SAD list)
Provider     → npi-registry MCP (validate, lookup, search)
Analytics    → mimilabs MCP (CMS datasets, benchmarks)
```

### Step 3: Synthesize & Deliver

I combine all findings into a structured response:

```
┌─────────────────────────────────────────┐
│           RCM COPILOT ANALYSIS          │
├─────────────────────────────────────────┤
│                                         │
│  SITUATION ASSESSMENT                   │
│  What's happening and why it matters    │
│                                         │
│  FINDINGS                               │
│  Live data from relevant APIs           │
│                                         │
│  RECOMMENDATIONS                        │
│  Specific, actionable next steps        │
│                                         │
│  RISK FLAGS                             │
│  Compliance or denial risks identified  │
│                                         │
│  RELATED SKILLS                         │
│  Deep-dive commands for follow-up       │
│                                         │
└─────────────────────────────────────────┘
```

## Example Scenarios

### "Patient has type 2 diabetes with CKD stage 3, coming for annual checkup"

The Copilot will:
1. Search ICD-10 for the correct combination codes (E11.22 for DM with CKD)
2. Identify proper CKD staging code (N18.3)
3. Note sequencing rules (diabetes code first per guidelines)
4. Check Medicare coverage for annual wellness visit
5. Suggest appropriate E/M level with chronic care management
6. Flag documentation requirements for HCC coding

### "Claim denied CO-50 for HCPCS J0135 adalimumab"

The Copilot will:
1. Decode CO-50 (non-covered service) and RARC implications
2. Check if adalimumab is on the SAD exclusion list
3. Search for relevant LCDs/NCDs for biologic coverage
4. Determine if Part B vs Part D is the correct billing path
5. Draft appeal strategy if Part B billing is appropriate
6. Identify alternative billing approaches

## Response Format

Every Copilot response includes:

- **Assessment**: Plain-English summary of the situation
- **Data**: Live API results with validated codes and policies
- **Action Items**: Numbered, specific steps to take
- **Warnings**: Compliance risks, denial triggers, documentation gaps
- **Go Deeper**: Specific `/skill-name` commands for detailed follow-up

## Tips

- Be specific: include payer, CPT codes, diagnosis, and setting of service
- Mention the problem: "denied", "need to code", "coverage question", "how to bill"
- Include context: Medicare vs commercial, inpatient vs outpatient, new vs established patient
- Ask follow-ups: the Copilot remembers context within the conversation
