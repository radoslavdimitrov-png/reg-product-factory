# REG Product PRD — Output Templates

---

## Header

**[Initiative Name]**

| Field | Detail |
| :--- | :--- |
| **Owner** | Radoslav Dimitrov |
| **Slack channel** | [channel name or UNKNOWN] |
| **Jira ticket** | [STRAT-XXXX link or UNKNOWN] |
| **Design** | [Figma link or N/A] |

---

## Executive summary

2-4 sentences maximum. State:
- What is being built or changed
- Which entity or entities it applies to
- The driver and deadline if applicable

---

## Problem and opportunity statement

### Problem
- What the current situation is and why it is
  a problem
- The specific regulatory, operational, or
  commercial risk of not acting
- Who is affected and how many clients are
  impacted (if known)
- Any compliance, audit, or enforcement risk
  of maintaining the status quo
- Any internal inconsistency the change resolves

### Opportunity
- What we gain by doing this
- The commercial or UX benefit in plain English
- Any secondary benefits (ops efficiency,
  cross-entity consistency, reduced maintenance)

### Priority and timeline
- Why this is being prioritised now
- External deadline or regulatory trigger
  if applicable
- Consequence of missing the deadline

---

## Scope and requirements

### Applicability

State clearly:
- Which entities are in scope
- Which account types are affected
- Which user segments are affected
  (new users / existing users / both)
- The trigger condition (when does this apply?)
- Any explicit exclusions

---

### In scope

Bullet list. MVP only.
Each bullet must be a specific, deliverable item.
No vague or aspirational bullets.

---

### Out of scope

3-5 bullets maximum.
Be explicit about what is not being built to
prevent scope creep.

---

### [Detail section — name determined dynamically]

This section is named based on the type of change.
See Phase 2 of the instructions for naming rules.

For each component or change:
- Describe what is changing or being built in
  plain English
- State the trigger or condition if applicable
- State the user interaction if applicable
- State any audit trail or data storage
  requirement if applicable
- State any edge cases that must be handled

Keep this high-level. Engineering adds technical
detail during sprint planning.

---

### Rollout plan

| Milestone | Description | Target date | Owner |
| :--- | :--- | :--- | :--- |
| [milestone] | [what happens] | [date or TBC] | [team or UNKNOWN] |

Include:
- Key build and QA milestones
- Compliance and Legal sign-off points
- Release to production
- Post-launch monitoring window

---

### Competitor context

Only include if competitor data was gathered in
the Market Research step. Otherwise omit this
section entirely.

**What Tier 1 competitors do:**
- [Bullet per competitor — name, entity, approach
  in one sentence]

**Market standard conclusion:**
[One sentence on what the lowest-friction
defensible approach looks like]

**T212 opportunity:**
[One sentence on how T212 matches or beats it]

---

## Data and analytics

Amplitude focused. High-level only.
Engineering adds event-level detail during
sprint planning.

**What we need to measure:**
- [Metric and why it matters]
- [Metric and why it matters]

**Key questions this data must answer:**
- [Question]
- [Question]

**Monitoring triggers:**
- [What threshold or pattern triggers a review
  or escalation]

---

## Client-facing requirements

Only include subsections that are relevant to
this initiative. Omit any that do not apply.

### Help Centre
- [Article to create or update — topic and
  key message in one bullet per article]
- [What the article must not claim]

### Internal team knowledge
- [What Customer Care must know before launch]
- [Suggested response approach for expected
  queries]

### AI chatbot and phonebot
- [New intent to add]
- [Existing intent to update]
- [What the bot must not answer or claim]

### Communications
Only include if client-facing communications
are required.
- Email or in-app message required: yes / no
- If yes: [plain English summary of key message,
  marked "Requires Compliance sign-off"]

---

## References

List all relevant links:
- [Jira ticket — description]
- [Regulatory source — description]
- [Related initiative — description]
- [Data source or supporting document]

---

## Handover block
```
## Reg Product Factory — Handover Block
**From:** PRD (Step 05)
**To:** PRD Critique (Step 05b)
**Date:** [today's date]

---

### Initiative summary
- **Initiative:** [name]
- **Entities:** [list]
- **Account types:** [list]
- **Driver:** [driver]
- **Deadline:** [deadline or "none"]

---

### PRD status
- **Sections complete:** [list]
- **Open items:** [anything not yet resolved]
- **Detail section name used:** [confirm]

---

### Specific areas for critique
- [Sections you are uncertain about]
- [Scope decisions that need independent review]
- [Anything that felt ambiguous during drafting]

---

### Attached documents
- [List or "None"]
```
