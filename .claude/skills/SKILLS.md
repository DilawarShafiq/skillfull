# Skillfull — Skills Index

16 Claude Code skills for US Healthcare Revenue Cycle Management.

## Orchestration Skills

These skills coordinate across the entire RCM workflow:

| Skill | Command | Description |
|-------|---------|-------------|
| [RCM Copilot](rcm-copilot/SKILL.md) | `/rcm-copilot` | Intelligent orchestrator — describe any billing situation, get multi-step analysis |
| [Claim Simulator](claim-simulator/SKILL.md) | `/claim-simulator` | Interactive billing simulator with live API validation and scoring |

## Interactive Skills (MCP-Powered)

These skills query live healthcare data APIs:

| Skill | Command | Description | MCP Server |
|-------|---------|-------------|------------|
| [ICD-10 Lookup](icd10-lookup/SKILL.md) | `/icd10-lookup` | Search and validate ICD-10-CM/PCS codes | icd10-codes |
| [NPI Verify](npi-verify/SKILL.md) | `/npi-verify` | Validate and look up provider NPIs | npi-registry |
| [Coverage Check](coverage-check/SKILL.md) | `/coverage-check` | Research Medicare NCDs and LCDs | cms-coverage |
| [Claim Scrub](claim-scrub/SKILL.md) | `/claim-scrub` | Pre-submission claim validation | Multiple |

## Front-End RCM Skills

| Skill | Command | Description |
|-------|---------|-------------|
| [Patient Registration](patient-registration/SKILL.md) | `/patient-registration` | Demographics, scheduling, pre-registration |
| [Eligibility Verification](eligibility-verification/SKILL.md) | `/eligibility-verification` | Insurance verification, benefits, prior auth |

## Mid-Cycle RCM Skills

| Skill | Command | Description |
|-------|---------|-------------|
| [Medical Coding](medical-coding/SKILL.md) | `/medical-coding` | ICD-10, CPT, HCPCS coding guidance |
| [Charge Capture](charge-capture/SKILL.md) | `/charge-capture` | Service documentation, revenue integrity |
| [Claim Submission](claim-submission/SKILL.md) | `/claim-submission` | CMS-1500, UB-04, EDI 837 |

## Back-End RCM Skills

| Skill | Command | Description |
|-------|---------|-------------|
| [Payment Posting](payment-posting/SKILL.md) | `/payment-posting` | ERA/835, EOB, CARC/RARC codes |
| [Denial Management](denial-management/SKILL.md) | `/denial-management` | Denial analysis, appeals |
| [A/R Analysis](ar-analysis/SKILL.md) | `/ar-analysis` | Aging, follow-up, collections strategy |
| [Patient Collections](patient-collections/SKILL.md) | `/patient-collections` | Statements, payment plans, financial assistance |
| [RCM Analytics](rcm-analytics/SKILL.md) | `/rcm-analytics` | KPIs, dashboards, benchmarking |

## MCP Server Integrations

| Server | Data Source | Skills Using It |
|--------|-------------|-----------------|
| `icd10-codes` | ICD-10-CM/PCS 2026 | icd10-lookup, medical-coding, claim-scrub, rcm-copilot, claim-simulator |
| `npi-registry` | NPPES Provider Registry | npi-verify, claim-scrub, rcm-copilot, claim-simulator |
| `cms-coverage` | Medicare Coverage DB | coverage-check, denial-management, rcm-copilot, claim-simulator |
| `mimilabs` | CMS/CDC/FDA Datasets | rcm-analytics, rcm-copilot |

## Skill Architecture

```
                    ┌──────────────┐
                    │  RCM Copilot │ ◄── Intelligent entry point
                    └──────┬───────┘
                           │
              ┌────────────┼────────────┐
              ▼            ▼            ▼
        ┌──────────┐ ┌──────────┐ ┌──────────┐
        │Front-End │ │Mid-Cycle │ │Back-End  │
        │ 2 skills │ │ 3 skills │ │ 5 skills │
        └──────────┘ └──────────┘ └──────────┘
              │            │            │
              └────────────┼────────────┘
                           ▼
                    ┌──────────────┐
                    │  4 MCP APIs  │ ◄── Live healthcare data
                    └──────────────┘
```

Each skill follows the SKILL.md format with:
- **SKILL.md**: Main skill file with YAML frontmatter
- **reference.md**: Detailed reference documentation (where applicable)
- **Additional files**: Templates, scenarios, examples

## Usage

Skills are auto-detected by Claude Code. Use slash commands:

```
/rcm-copilot patient has Medicare, need CGM coverage determination
/claim-simulator coding-challenge +medicare
/icd10-lookup diabetes type 2
/npi-verify 1234567893
/denial-management CO-16
```

Or let Claude auto-invoke skills based on conversation context.
