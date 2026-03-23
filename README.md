# 🏭 T212 Reg Product Factory

Welcome to the Trading 212 Reg Product Factory. This
repository contains the system instructions, context
files, and automation skills that power our regulatory
product development pipeline.

---

## 📂 Repository Structure

**`00-global-context/`**
The single source of truth for all agents. Contains
`T212-group-context.md`, which defines our risk
appetite, entity permissions, UX guardrails, product
availability, engineering ownership, and the
zero-hallucination policy. Every agent loads this
file before reasoning. Update it when regulations,
product permissions, or company policies change.

**`01-intake/`**
The first step of every initiative. Contains the
ChatGPT Custom GPT instructions for the Intake Brief
agent, which collects and structures initiative
information before the pipeline begins.

**`03a-comp-audit/`**
Path A — used when Compliance or Legal have provided
an existing analysis that needs to be stress-tested.
Contains the ChatGPT Custom GPT instructions and
output templates for the REG Comp Audit agent.

**`03b-comp-analysis/`**
Path B — used when no external analysis exists and
we need to build the compliance picture from scratch.
Contains the ChatGPT Custom GPT instructions and
output templates for the REG Comp Analysis agent.

**`04-market-research/`**
Benchmarks how Tier 1 competitors handle the
specific regulatory friction point identified in the
compliance step. Contains the ChatGPT Custom GPT
instructions and output templates for the REG Market
Research agent.

**`05-prd/`**
Turns the research and compliance findings into an
approved PRD and publishes it to Confluence. Contains:
- Claude Project instructions for the REG Product
  PRD agent (drafting and self-critique)
- Output templates for the PRD agent
- Cowork skill for writing the approved PRD to
  Confluence in the correct format

---

## 🔄 The Pipeline

Every initiative follows one of two paths depending
on whether Compliance have already produced an
analysis.
```
01 — INTAKE BRIEF (ChatGPT)
Collect and structure the initiative information.
Output: structured brief + REG and STRAT ticket drafts
        |
        ├── PATH A: External compliance analysis exists
        |         |
        |    03a — COMP AUDIT (ChatGPT)
        |    Stress-test the analysis for gold-plating.
        |         |
        └── PATH B: No analysis exists
                  |
             03b — COMP ANALYSIS (ChatGPT)
             Build the MVC compliance picture
             from scratch.
                  |
        Both paths reconverge here:
                  |
        04 — MARKET RESEARCH (ChatGPT)
        Benchmark Tier 1 competitors and define
        the lowest-friction market standard.
                  |
        05 — PRD DRAFT (Claude Projects)
        Draft the plain English business case
        and PRD. Self-critique runs automatically.
                  |
        05 — CONFLUENCE (Claude Cowork)
        Publish the approved PRD to the existing
        Confluence page in the correct format.
```

---

## 🤖 The Agents

| Step | Agent | Tool | Path |
| :--- | :--- | :--- | :--- |
| 01 | REG Intake Brief | ChatGPT Custom GPT | All |
| 03a | REG Comp Audit | ChatGPT Custom GPT | A only |
| 03b | REG Comp Analysis | ChatGPT Custom GPT | B only |
| 04 | REG Market Research | ChatGPT Custom GPT | All |
| 05 | REG Product PRD | Claude Project | All |
| 05 | REG PRD to Confluence | Claude Cowork Skill | All |

---

## 🚀 Quick Start Guide

### Before you begin
Every agent loads `T212-group-context.md` as its
policy document. For ChatGPT Custom GPTs this happens
automatically via auto-fetch at the start of each
session. For the Claude Project, the file is uploaded
once to the project knowledge.

You do not need to upload or paste the context file
manually each time.

### Running an initiative

**Step 1 — Open the Intake GPT in ChatGPT**
- Open your ChatGPT Project for this initiative
- Start a new chat with the REG Intake Brief GPT
- Give it a one or two sentence description of the
  initiative
- Answer its clarifying questions
- It will produce a structured brief and draft REG
  and STRAT ticket names and descriptions
- Create the two Jira tickets manually using the
  drafts

**Step 2 — Run the compliance step**
- Start a new chat in the same ChatGPT Project
- If Path A: open the REG Comp Audit GPT and paste
  the intake handover block plus the external
  compliance analysis
- If Path B: open the REG Comp Analysis GPT and
  paste the intake handover block
- Review the output and iterate as needed

**Step 3 — Run market research**
- Start a new chat in the same ChatGPT Project
- Open the REG Market Research GPT
- Paste the handover block from Step 2
- Review the benchmark and iterate as needed

**Step 4 — Draft the PRD in Claude**
- Open the REG Product Factory project in Claude
- Start a new chat thread named after the initiative
- Paste the cross-model handover block from ChatGPT
- Claude will draft the PRD and automatically
  self-critique it
- Iterate until the critique verdict is
  "Ready to proceed"

**Step 5 — Publish to Confluence**
- Open Claude Cowork
- Say: "Run the reg-prd-confluence skill"
- Paste the Confluence page URL (created automatically
  when you raised the STRAT Jira ticket)
- Paste the approved PRD markdown
- Cowork will update the page in the correct format

---

## ⚠️ Zero Hallucination Policy

All agents operate under a strict zero-hallucination
policy defined in `T212-group-context.md`. No agent
will fabricate regulatory citations, competitor
behaviour, or internal system details. If something
cannot be verified, it is labelled UNKNOWN.

Any output that contains fabricated citations or
invented facts is considered invalid and must be
discarded and regenerated.
