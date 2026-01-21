# Contributing to Skillfull

Thank you for your interest in contributing to the Skillfull RCM skills collection.

## Types of Contributions

### 1. New Skills
Add new skills for healthcare RCM workflows:
- Additional specialty coding guides
- Payer-specific billing skills
- Compliance and audit skills
- Reporting and analytics skills

### 2. Skill Improvements
Enhance existing skills:
- Updated regulatory information
- Additional code tables or references
- New appeal templates
- Enhanced MCP tool integrations

### 3. Documentation
Improve documentation:
- Clearer explanations
- Additional examples
- Error corrections
- Reference updates

## Skill Format Requirements

### Directory Structure
```
.claude/skills/
└── your-skill-name/
    ├── SKILL.md          # Required: Main skill file
    ├── reference.md      # Optional: Detailed reference
    ├── examples.md       # Optional: Usage examples
    └── templates.md      # Optional: Templates/checklists
```

### SKILL.md Format
```markdown
---
name: your-skill-name
description: Clear description of what this skill does and when to use it
user-invocable: true
argument-hint: [optional-arguments]
allowed-tools: Tool1, Tool2
---

# Skill Title

Brief overview of the skill.

## When to Use

Clear guidance on skill applicability.

## Content

Main skill content...
```

### Required Frontmatter
- `name`: Lowercase, hyphens only (max 64 chars)
- `description`: 1-2 sentences explaining purpose

### Optional Frontmatter
- `user-invocable`: Set `false` for background knowledge only
- `disable-model-invocation`: Set `true` for manual-only skills
- `argument-hint`: Help text for parameters
- `allowed-tools`: Comma-separated MCP tools

## Content Guidelines

### Healthcare Accuracy
- Reference official CMS guidelines
- Include effective dates for rules
- Note state-specific variations
- Use current code sets (2026)

### Compliance Considerations
- Follow HIPAA guidelines
- Reference False Claims Act implications
- Include appropriate disclaimers
- Note payer-specific requirements

### Code Tables
Use tables for quick reference:
```markdown
| Code | Description | Common Use |
|------|-------------|------------|
| -25 | Significant E/M | E/M with procedure |
```

### MCP Tool Integration
Reference available MCP servers:
- `mcp__icd10-codes__*` - ICD-10 lookups
- `mcp__npi-registry__*` - Provider verification
- `mcp__cms-coverage__*` - Medicare coverage
- `mcp__mimilabs__*` - Healthcare datasets

## Submission Process

1. **Fork** the repository
2. **Create** a feature branch
3. **Add** your skill following the format above
4. **Test** the skill with Claude Code
5. **Submit** a pull request

### PR Requirements
- Clear description of the skill
- Confirmation of accuracy review
- Note any regulatory references
- List MCP tools used

## Review Criteria

Skills are reviewed for:
- [ ] Healthcare billing accuracy
- [ ] Current regulatory compliance
- [ ] Proper SKILL.md format
- [ ] Clear and actionable content
- [ ] Appropriate MCP tool usage
- [ ] No PHI or sensitive data

## Questions?

Open an issue for:
- Clarification on format requirements
- Healthcare content questions
- MCP integration help
- General contribution questions

## License

Contributions are licensed under MIT License.
