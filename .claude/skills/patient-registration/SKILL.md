---
name: patient-registration
description: Patient registration and scheduling guidance. Use when managing patient demographics, appointment scheduling, or pre-registration workflows.
user-invocable: true
argument-hint: [registration-scenario]
---

# Patient Registration Skill

Expert guidance for patient registration, scheduling, and pre-service workflows.

## When to Use

- Collecting patient demographics
- Scheduling appointments
- Pre-registration workflows
- Insurance card capture
- HIPAA consent management

## Registration Data Elements

### Required Demographics
- [ ] Full legal name
- [ ] Date of birth
- [ ] Social Security Number (optional)
- [ ] Address (street, city, state, ZIP)
- [ ] Phone numbers (home, cell, work)
- [ ] Email address
- [ ] Emergency contact
- [ ] Employer information

### Insurance Information
- [ ] Insurance card (front and back)
- [ ] Subscriber name and DOB
- [ ] Subscriber ID / Member ID
- [ ] Group number
- [ ] Payer name and phone
- [ ] Primary vs secondary designation

### Consent and Compliance
- [ ] HIPAA Notice of Privacy Practices
- [ ] Assignment of Benefits
- [ ] Financial responsibility acknowledgment
- [ ] Release of information authorization

## Pre-Registration Workflow

1. Patient schedules appointment
2. Pre-registration form sent (portal/email)
3. Patient completes demographics online
4. Insurance cards uploaded
5. Eligibility verified
6. Estimated costs communicated
7. Pre-authorization obtained (if needed)

## Scheduling Best Practices

- Capture chief complaint/reason for visit
- Verify provider availability
- Confirm insurance network status
- Estimate visit duration accurately
- Send appointment reminders
- Enable self-scheduling when appropriate

## Common Registration Errors

| Error | Impact | Prevention |
|-------|--------|------------|
| Wrong DOB | Eligibility failures | ID verification |
| Typo in subscriber ID | Claim denials | Card imaging |
| Wrong payer selected | Rejected claims | Payer verification |
| Missing consent | Compliance risk | Checklist workflow |

## KPIs

| Metric | Target |
|--------|--------|
| Pre-registration rate | >80% |
| Registration accuracy | >98% |
| No-show rate | <10% |
| Eligibility verification | >98% |

For detailed registration guidelines, see [reference.md](reference.md).
