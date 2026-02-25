<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/%E2%9A%95-SKILLFULL-00d4aa?style=for-the-badge&labelColor=0d1117&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0iIzAwZDRhYSI+PHBhdGggZD0iTTEyIDJMNCA3djEwbDggNSA4LTVWN3oiLz48L3N2Zz4=">
    <img alt="Skillfull" src="https://img.shields.io/badge/%E2%9A%95-SKILLFULL-00d4aa?style=for-the-badge&labelColor=1a1a2e">
  </picture>
</p>

<h3 align="center">AI-Powered Revenue Cycle Management for Claude Code</h3>

<p align="center">
  <em>16 skills. 4 live APIs. The entire US healthcare revenue cycle in your terminal.</em>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="MIT License"></a>
  <a href="https://claude.ai/claude-code"><img src="https://img.shields.io/badge/Claude_Code-Skills-8B5CF6" alt="Claude Code"></a>
  <a href="https://modelcontextprotocol.io"><img src="https://img.shields.io/badge/MCP-4_Servers-00d4aa" alt="MCP Enabled"></a>
  <a href=".claude/skills/"><img src="https://img.shields.io/badge/Healthcare-RCM-ef4444" alt="Healthcare RCM"></a>
  <a href=".claude/skills/claim-simulator/SKILL.md"><img src="https://img.shields.io/badge/NEW-Claim_Simulator-f59e0b" alt="Claim Simulator"></a>
</p>

---

## The Problem

Healthcare billing in the US is a **$4 trillion system** running on arcane codes, shifting payer rules, and manual lookups across dozens of disconnected databases. A single coding error can mean thousands in lost revenue. A missed LCD update can trigger months of denials.

**Skillfull brings the entire revenue cycle into your AI-powered terminal — with live data.**

## Try It Now

```bash
git clone https://github.com/DilawarShafiq/skillfull.git
cd skillfull
```

Then in Claude Code:

```
/rcm-copilot patient has diabetes with foot ulcer, need to code and check Medicare coverage

/claim-simulator coding-challenge +medicare

/icd10-lookup type 2 diabetes with peripheral angiopathy

/npi-verify 1234567893

/coverage-check continuous glucose monitoring

/denial-management CO-97 bundled arthroscopy codes
```

## The Pipeline

Skillfull covers every phase of the revenue cycle, with **live API validation** at every step:

```
                          THE REVENUE CYCLE
  ┌──────────────────────────────────────────────────────────┐
  │                                                          │
  │   FRONT END              MID CYCLE             BACK END  │
  │                                                          │
  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌─────────┐ │
  │  │ Register │─▶│  Verify  │─▶│   Code   │─▶│ Capture │ │
  │  │ Patient  │  │ Benefits │  │ Services │  │ Charges │ │
  │  └──────────┘  └──────────┘  └──────────┘  └────┬────┘ │
  │   /patient-     /eligibility-  /medical-     /charge-   │
  │   registration   verification   coding       capture    │
  │                                                  │       │
  │              ┌───────────────────────────────────┘       │
  │              ▼                                           │
  │  ┌──────────┐  ┌──────────┐  ┌──────────┐  ┌─────────┐ │
  │  │  Submit  │─▶│  Post    │─▶│ Manage   │─▶│ Collect │ │
  │  │  Claim   │  │ Payment  │  │ Denials  │  │  A/R    │ │
  │  └──────────┘  └──────────┘  └──────────┘  └─────────┘ │
  │   /claim-       /payment-     /denial-      /ar-        │
  │   submission     posting       management    analysis   │
  │                                                          │
  └──────────────────────────────────────────────────────────┘

  Live Data Layer:
  ╔════════════╗ ╔════════════╗ ╔════════════╗ ╔════════════╗
  ║ ICD-10     ║ ║ NPPES      ║ ║ Medicare   ║ ║ CMS/CDC    ║
  ║ 2026 Codes ║ ║ NPI Lookup ║ ║ NCDs/LCDs  ║ ║ 50+ Sets   ║
  ╚════════════╝ ╚════════════╝ ╚════════════╝ ╚════════════╝
```

## What's New: Innovation Skills

### `/rcm-copilot` — The Revenue Cycle Brain

One command to rule them all. Describe any billing situation in plain English — the Copilot identifies what you need, queries the right APIs, and delivers a structured analysis.

```
/rcm-copilot claim denied CO-50 for adalimumab J0135, patient has Medicare
```

The Copilot will:
1. Decode the denial reason (CO-50 = non-covered service)
2. Check if adalimumab is on the Self-Administered Drug exclusion list
3. Search for relevant Medicare coverage policies (NCDs/LCDs)
4. Determine Part B vs Part D billing path
5. Recommend appeal strategy or alternative approach

**No more guessing which tool to use. Just describe the problem.**

### `/claim-simulator` — Flight Simulator for Medical Billing

Interactive scenarios where you code real encounters, validated against live APIs. Every ICD-10 code you pick is checked in real time. Every claim decision has consequences.

```
/claim-simulator denial-gauntlet +medicare
```

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
│  KEY TAKEAWAY: Modifier 25 was needed       │
│                                             │
└─────────────────────────────────────────────┘
```

Scenario types: `beginner` · `coding-challenge` · `denial-gauntlet` · `coverage-maze` · `full-cycle` · `emergency`

## All 16 Skills

### Orchestration

| Command | What It Does |
|---------|-------------|
| **`/rcm-copilot`** | Intelligent orchestrator — describe any billing situation, get multi-step guidance |
| **`/claim-simulator`** | Interactive billing simulator with live API validation and scoring |

### Interactive (Live API)

| Command | Data Source | What It Does |
|---------|------------|-------------|
| `/icd10-lookup` | ICD-10 2026 | Search, validate, and explore diagnosis/procedure codes |
| `/npi-verify` | NPPES Registry | Validate provider credentials, search by name/specialty |
| `/coverage-check` | Medicare NCDs/LCDs | Research coverage policies, check medical necessity |
| `/claim-scrub` | Multiple APIs | Pre-submission validation across code, coverage, and provider data |

### Front-End RCM

| Command | What It Does |
|---------|-------------|
| `/patient-registration` | Demographics, scheduling, pre-registration workflows |
| `/eligibility-verification` | Insurance verification, benefits, prior authorization |

### Mid-Cycle RCM

| Command | What It Does |
|---------|-------------|
| `/medical-coding` | ICD-10-CM/PCS, CPT, HCPCS coding with guidelines |
| `/charge-capture` | Service documentation, revenue integrity, charge reconciliation |
| `/claim-submission` | CMS-1500, UB-04, EDI 837 form guidance |

### Back-End RCM

| Command | What It Does |
|---------|-------------|
| `/payment-posting` | ERA/835 processing, EOB interpretation, CARC/RARC codes |
| `/denial-management` | Denial analysis, appeal templates, root cause investigation |
| `/ar-analysis` | A/R aging analysis, collection strategies, KPI calculations |
| `/patient-collections` | Statements, payment plans, financial assistance programs |
| `/rcm-analytics` | Revenue cycle KPIs, dashboards, payer benchmarking |

## Architecture

```
┌─────────────────────────────────────────────────────────┐
│                    CLAUDE CODE                          │
│                                                         │
│  ┌───────────────────────────────────────────────────┐  │
│  │               SKILLFULL SKILLS                    │  │
│  │                                                   │  │
│  │  ┌─────────────┐  ┌──────────────────────────┐   │  │
│  │  │ RCM Copilot │──│ Routes to 14 RCM Skills  │   │  │
│  │  └──────┬──────┘  └──────────────────────────┘   │  │
│  │         │                                         │  │
│  │  ┌──────┴──────┐                                  │  │
│  │  │  Simulator  │─── Generates & Validates         │  │
│  │  └──────┬──────┘    Scenarios                     │  │
│  │         │                                         │  │
│  └─────────┼─────────────────────────────────────────┘  │
│            │                                             │
│  ┌─────────┴─────────────────────────────────────────┐  │
│  │          MODEL CONTEXT PROTOCOL (MCP)             │  │
│  │                                                   │  │
│  │  ┌───────────┐ ┌──────────┐ ┌─────────┐ ┌─────┐  │  │
│  │  │ ICD-10    │ │ NPPES    │ │ CMS     │ │Mimi │  │  │
│  │  │ Codes     │ │ NPI      │ │Coverage │ │Labs │  │  │
│  │  │           │ │ Registry │ │ DB      │ │     │  │  │
│  │  │ Diagnoses │ │ Provider │ │ NCDs    │ │ 50+ │  │  │
│  │  │ Procedure │ │ Lookup   │ │ LCDs    │ │Data │  │  │
│  │  │ Validate  │ │ Search   │ │ SAD     │ │Sets │  │  │
│  │  └───────────┘ └──────────┘ └─────────┘ └─────┘  │  │
│  └───────────────────────────────────────────────────┘  │
│                                                         │
└─────────────────────────────────────────────────────────┘
```

## Who This Is For

| Role | How You'll Use It |
|------|------------------|
| **Billing Specialists** | Real-time code lookup, denial resolution, claim scrubbing |
| **Revenue Cycle Managers** | KPI dashboards, A/R analysis, payer benchmarking |
| **Medical Coders** | ICD-10/CPT guidance, coding challenges, certification prep |
| **Practice Managers** | Coverage verification, financial projections, compliance checks |
| **Healthcare IT** | MCP integration patterns, API workflows, automation templates |
| **Students** | Interactive simulator, scenario-based learning, exam prep |

## Certification Alignment

Skill content aligns with competencies tested on:

| Certification | Organization | Skills Covered |
|--------------|--------------|----------------|
| CPC (Certified Professional Coder) | AAPC | medical-coding, icd10-lookup, claim-simulator |
| CCS (Certified Coding Specialist) | AHIMA | medical-coding, icd10-lookup, claim-simulator |
| CRCR (Certified Revenue Cycle Rep) | HFMA | All 16 skills |
| CPB (Certified Professional Biller) | AAPC | claim-submission, denial-management, payment-posting |

## Project Structure

```
skillfull/
├── .claude/
│   ├── settings.local.json          # MCP permissions
│   └── skills/                      # All 16 skills
│       ├── SKILLS.md                # Master index
│       ├── rcm-copilot/             # ★ Intelligent orchestrator
│       ├── claim-simulator/         # ★ Interactive simulator + scenarios
│       ├── icd10-lookup/            # ICD-10 code search (MCP)
│       ├── npi-verify/              # Provider verification (MCP)
│       ├── coverage-check/          # Medicare coverage (MCP)
│       ├── claim-scrub/             # Pre-submission validation (MCP)
│       ├── patient-registration/    # Demographics & scheduling
│       ├── eligibility-verification/# Insurance verification
│       ├── medical-coding/          # Coding guidance + reference
│       ├── charge-capture/          # Revenue integrity
│       ├── claim-submission/        # EDI 837, CMS-1500, UB-04
│       ├── payment-posting/         # ERA/835 processing
│       ├── denial-management/       # Appeals + templates
│       ├── ar-analysis/             # A/R management
│       ├── patient-collections/     # Patient responsibility
│       └── rcm-analytics/           # KPIs & reporting
├── .mcp.json                        # 4 MCP server connections
├── CONTRIBUTING.md                  # How to add skills
├── LICENSE                          # MIT
└── README.md                        # You are here
```

## Contributing

We welcome contributions. See [CONTRIBUTING.md](CONTRIBUTING.md) for skill format requirements, healthcare accuracy guidelines, and MCP integration patterns.

**Ideas for contributors:**
- Specialty-specific skills (Cardiology, Oncology, Orthopedics)
- Payer-specific rule engines (UnitedHealth, Aetna, Cigna)
- Additional simulator scenarios
- International billing adaptations (CPT → OPCS, ICD-10-CM → ICD-10-AM)

## Disclaimer

Educational and reference purposes only. Always verify against current CMS guidelines, payer policies, and applicable regulations. **Not a substitute for** official CMS documentation, professional coding certification, or legal/compliance advice.

## License

[MIT](LICENSE) — Use it, fork it, build on it.

---

<p align="center">
  <strong>Built for <a href="https://claude.ai/claude-code">Claude Code</a></strong> · <strong>Powered by <a href="https://modelcontextprotocol.io">MCP</a></strong>
  <br><br>
  <em>The revenue cycle never satisfies. Neither does your AI.</em>
</p>
