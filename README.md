# Skillfull

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skills-purple)](https://claude.ai/claude-code)
[![MCP Enabled](https://img.shields.io/badge/MCP-Enabled-green)](https://modelcontextprotocol.io)
[![Healthcare](https://img.shields.io/badge/US%20Healthcare-RCM-red)](skills/)

**Revenue Cycle Management Skills for Claude Code**

A comprehensive collection of Claude Code skills for US healthcare billing, coding, and revenue cycle operations. Integrates with live healthcare data APIs via Model Context Protocol (MCP).

## Quick Start

```bash
# Clone the repository
git clone https://github.com/yourusername/skillfull.git

# Skills are auto-detected by Claude Code from .claude/skills/
```

**Try a skill:**
```
/icd10-lookup type 2 diabetes
/npi-verify 1234567893
/coverage-check continuous glucose monitoring
/denial-management CO-16
```

## Features

- **Interactive Skills**: Real-time lookups using live healthcare APIs
- **Reference Skills**: Expert guidance for RCM workflows
- **MCP Integration**: Connected to ICD-10, NPI, and CMS databases
- **Progressive Disclosure**: Efficient context usage with supporting files
- **HIPAA Aligned**: Best practices for compliant billing operations

## Skills

### Interactive (MCP-Powered)

| Command | Description | Data Source |
|---------|-------------|-------------|
| `/icd10-lookup` | Search/validate ICD-10-CM/PCS codes | ICD-10 2026 |
| `/npi-verify` | Verify provider credentials | NPPES Registry |
| `/coverage-check` | Research Medicare coverage policies | CMS LCD/NCD |
| `/claim-scrub` | Pre-submission claim validation | Multiple APIs |

### Reference

| Command | Description |
|---------|-------------|
| `/medical-coding` | ICD-10, CPT, HCPCS coding guidance |
| `/denial-management` | Denial analysis and appeal templates |
| `/eligibility-verification` | Insurance verification workflows |
| `/ar-analysis` | A/R aging and collection strategies |

## RCM Knowledge Base

The `skills/` directory contains detailed documentation for all 10 RCM components:

| Component | Description |
|-----------|-------------|
| [Patient Registration](skills/patient-registration-scheduling.md) | Demographics, scheduling, pre-registration |
| [Eligibility Verification](skills/insurance-eligibility-verification.md) | Coverage, benefits, prior authorization |
| [Charge Capture](skills/charge-capture.md) | Clinical documentation, charge entry |
| [Medical Coding](skills/medical-coding.md) | ICD-10, CPT, HCPCS, NCCI compliance |
| [Claim Submission](skills/claim-submission.md) | CMS-1500, UB-04, EDI 837 |
| [Payment Posting](skills/payment-posting.md) | ERA/835, EOB, adjustments |
| [Denial Management](skills/denial-management.md) | Analysis, appeals, prevention |
| [A/R Follow-up](skills/accounts-receivable-followup.md) | Aging, claim status, worklists |
| [Patient Collections](skills/patient-collections.md) | Statements, payment plans, financial assistance |
| [RCM Analytics](skills/rcm-reporting-analytics.md) | KPIs, benchmarks, dashboards |

## MCP Integration

This project connects to live healthcare data sources:

```json
{
  "mcpServers": {
    "icd10-codes": "ICD-10-CM/PCS code lookup and validation",
    "npi-registry": "National Provider Identifier search",
    "cms-coverage": "Medicare NCDs and LCDs",
    "mimilabs": "50+ CMS/CDC/FDA datasets"
  }
}
```

See [.mcp.json](.mcp.json) for configuration.

## Project Structure

```
skillfull/
├── .claude/
│   └── skills/              # Claude Code skills (SKILL.md format)
│       ├── icd10-lookup/    # Interactive ICD-10 lookup
│       ├── npi-verify/      # Provider verification
│       ├── coverage-check/  # Medicare coverage research
│       ├── claim-scrub/     # Pre-submission validation
│       ├── medical-coding/  # Coding guidance
│       ├── denial-management/  # Denials and appeals
│       ├── eligibility-verification/
│       ├── ar-analysis/
│       └── SKILLS.md        # Skills index
├── skills/                  # RCM reference documentation
├── .mcp.json               # MCP server configuration
├── CONTRIBUTING.md         # Contribution guidelines
├── LICENSE                 # MIT License
└── README.md
```

## Target Audience

- Medical Billing Specialists
- Revenue Cycle Managers
- Healthcare Administrators
- Practice Managers
- Health Information Management (HIM) Professionals
- Healthcare IT Developers
- AI/ML Engineers

## Certification Alignment

Content aligns with competencies for:

| Certification | Organization |
|--------------|--------------|
| CPC (Certified Professional Coder) | AAPC |
| CCS (Certified Coding Specialist) | AHIMA |
| CRCR (Certified Revenue Cycle Representative) | HFMA |
| CPB (Certified Professional Biller) | AAPC |

## Contributing

We welcome contributions. See [CONTRIBUTING.md](CONTRIBUTING.md) for:

- Skill format requirements
- Healthcare accuracy guidelines
- MCP integration patterns
- Submission process

## Disclaimer

This repository is for educational and reference purposes only. Always verify information against current CMS guidelines, payer policies, and applicable regulations. Healthcare billing rules change frequently.

**This is NOT a substitute for:**
- Official CMS/payer documentation
- Professional medical coding certification
- Legal or compliance advice
- Clinical decision-making

## License

[MIT License](LICENSE)

---

**Built for [Claude Code](https://claude.ai/claude-code)** | **Powered by [MCP](https://modelcontextprotocol.io)**
