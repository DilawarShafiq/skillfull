# Skillfull

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skills-purple)](https://claude.ai/claude-code)
[![MCP Enabled](https://img.shields.io/badge/MCP-Enabled-green)](https://modelcontextprotocol.io)
[![Healthcare](https://img.shields.io/badge/US%20Healthcare-RCM-red)](.claude/skills/)

**Revenue Cycle Management Skills for Claude Code**

A comprehensive collection of 14 Claude Code skills covering the complete US healthcare revenue cycle. Integrates with live healthcare data APIs via Model Context Protocol (MCP).

## Quick Start

```bash
# Clone the repository
git clone https://github.com/DilawarShafiq/skillfull.git

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

- **14 RCM Skills**: Complete revenue cycle coverage
- **MCP Integration**: Real-time healthcare API lookups
- **SKILL.md Format**: Proper Claude Code skill structure
- **Progressive Disclosure**: Reference docs load on-demand
- **HIPAA Aligned**: Best practices for compliant billing

## Skills

### Interactive (MCP-Powered)

| Command | Description | Data Source |
|---------|-------------|-------------|
| `/icd10-lookup` | Search/validate ICD-10-CM/PCS codes | ICD-10 2026 |
| `/npi-verify` | Verify provider credentials | NPPES Registry |
| `/coverage-check` | Research Medicare coverage policies | CMS LCD/NCD |
| `/claim-scrub` | Pre-submission claim validation | Multiple APIs |

### Front-End RCM

| Command | Description |
|---------|-------------|
| `/patient-registration` | Demographics, scheduling, pre-registration |
| `/eligibility-verification` | Insurance verification, benefits, prior auth |

### Mid-Cycle RCM

| Command | Description |
|---------|-------------|
| `/medical-coding` | ICD-10, CPT, HCPCS coding guidance |
| `/charge-capture` | Service documentation, revenue integrity |
| `/claim-submission` | CMS-1500, UB-04, EDI 837 |

### Back-End RCM

| Command | Description |
|---------|-------------|
| `/payment-posting` | ERA/835, EOB, CARC/RARC codes |
| `/denial-management` | Denial analysis and appeal templates |
| `/ar-analysis` | A/R aging and collection strategies |
| `/patient-collections` | Statements, payment plans, financial assistance |
| `/rcm-analytics` | KPIs, dashboards, benchmarking |

## MCP Integration

Connected to live healthcare data sources:

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

## Project Structure

```
skillfull/
├── .claude/
│   └── skills/                    # All 14 Claude Code skills
│       ├── icd10-lookup/          # Interactive ICD-10 lookup
│       ├── npi-verify/            # Provider verification
│       ├── coverage-check/        # Medicare coverage research
│       ├── claim-scrub/           # Pre-submission validation
│       ├── patient-registration/  # Demographics & scheduling
│       ├── eligibility-verification/
│       ├── medical-coding/        # Coding guidance + reference
│       ├── charge-capture/        # Revenue integrity
│       ├── claim-submission/      # EDI 837, CMS-1500, UB-04
│       ├── payment-posting/       # ERA/835, adjustments
│       ├── denial-management/     # Appeals + templates
│       ├── ar-analysis/           # A/R management
│       ├── patient-collections/   # Patient responsibility
│       ├── rcm-analytics/         # KPIs & reporting
│       └── SKILLS.md              # Skills index
├── .mcp.json                      # MCP server configuration
├── CONTRIBUTING.md                # Contribution guidelines
├── LICENSE                        # MIT License
└── README.md
```

## Target Audience

- Medical Billing Specialists
- Revenue Cycle Managers
- Healthcare Administrators
- Practice Managers
- Health Information Management (HIM) Professionals
- Healthcare IT Developers

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

This repository is for educational and reference purposes only. Always verify information against current CMS guidelines, payer policies, and applicable regulations.

**This is NOT a substitute for:**
- Official CMS/payer documentation
- Professional medical coding certification
- Legal or compliance advice

## License

[MIT License](LICENSE)

---

**Built for [Claude Code](https://claude.ai/claude-code)** | **Powered by [MCP](https://modelcontextprotocol.io)**
