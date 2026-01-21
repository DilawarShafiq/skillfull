# Skillfull - RCM Skills Index

A collection of Claude Code skills for US Healthcare Revenue Cycle Management.

## Interactive Skills (MCP-Powered)

These skills leverage real-time healthcare data APIs:

| Skill | Command | Description |
|-------|---------|-------------|
| [ICD-10 Lookup](icd10-lookup/SKILL.md) | `/icd10-lookup` | Search and validate ICD-10-CM/PCS codes |
| [NPI Verify](npi-verify/SKILL.md) | `/npi-verify` | Validate and look up provider NPIs |
| [Coverage Check](coverage-check/SKILL.md) | `/coverage-check` | Research Medicare NCDs and LCDs |
| [Claim Scrub](claim-scrub/SKILL.md) | `/claim-scrub` | Pre-submission claim validation |

## Reference Skills

Expert guidance for RCM workflows:

| Skill | Command | Description |
|-------|---------|-------------|
| [Medical Coding](medical-coding/SKILL.md) | `/medical-coding` | ICD-10, CPT, HCPCS coding guidance |
| [Denial Management](denial-management/SKILL.md) | `/denial-management` | Denial analysis and appeals |
| [Eligibility Verification](eligibility-verification/SKILL.md) | `/eligibility-verification` | Insurance verification workflows |
| [A/R Analysis](ar-analysis/SKILL.md) | `/ar-analysis` | Accounts receivable management |

## Skill Categories

### Front-End RCM
- Patient Registration & Scheduling
- Eligibility Verification
- Prior Authorization

### Mid-Cycle RCM
- Medical Coding
- Charge Capture
- Claim Submission
- Claim Scrubbing

### Back-End RCM
- Payment Posting
- Denial Management
- A/R Follow-up
- Patient Collections

## MCP Server Integrations

These skills connect to live healthcare data sources:

| Server | Data Source | Used By |
|--------|-------------|---------|
| `icd10-codes` | ICD-10-CM/PCS 2026 | icd10-lookup, medical-coding, claim-scrub |
| `npi-registry` | NPPES Provider Registry | npi-verify, claim-scrub |
| `cms-coverage` | Medicare Coverage DB | coverage-check, denial-management |
| `mimilabs` | CMS/CDC/FDA Datasets | ar-analysis |

## Installation

These skills are included with the Skillfull project. To use:

1. Clone or copy the repository
2. Claude Code will automatically detect skills in `.claude/skills/`
3. Use slash commands (e.g., `/icd10-lookup diabetes`) or let Claude auto-invoke

## Skill Development

To add new skills:

1. Create a directory in `.claude/skills/<skill-name>/`
2. Add a `SKILL.md` with YAML frontmatter
3. Include supporting files for progressive disclosure
4. Reference MCP tools as needed

See [CONTRIBUTING.md](../../../CONTRIBUTING.md) for guidelines.
