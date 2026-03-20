# REG Comp Audit — Output Templates

---

## 1) Executive verdict

> **Status:** GREEN / AMBER / RED
> **Decision:** Approve as-is / Approve with changes / 
> Reject and replace
> **Summary:** 2-3 sentences. Overall quality of analysis, 
> most significant finding, recommended path.

---

## 2) Scorecard

| Dimension | Score (0-3) | Rationale |
| :--- | :---: | :--- |
| Binding legal mandate strength | | |
| Consumer harm / mis-selling risk | | |
| Enforcement likelihood | | |
| Commercial friction cost | | |
| Third-rail impact | | |

---

## 3) Citation audit

| Citation | Status | Source URL | Notes |
| :--- | :--- | :--- | :--- |
| [citation] | VERIFIED / UNKNOWN / DISPUTED | [URL or "No verified source available"] | [notes] |

---

## 4) Hard law vs guidance breakdown

| Requirement | Classification | What it actually requires | What it does NOT require |
| :--- | :--- | :--- | :--- |
| [requirement] | Hard Law / Expectation / Nice-to-have | [plain English] | [anti-creep] |

---

## 5) Gold-plating findings

For each instance found:

- **Claim in analysis:** [quote the specific claim]
- **Gold-plating type:** Scope creep / Early adoption / 
  Over-engineering / Friction without obligation
- **Why it exceeds hard law:** [explanation with citation]
- **MVC alternative:** [lowest-friction defensible 
  replacement]

If none found: state "No gold-plating identified" and 
explain why the analysis is considered proportionate.

---

## 6) Competitor benchmark

| Competitor | UX pattern | Evidence grade | Source |
| :--- | :--- | :--- | :--- |
| [name] | [what they do] | A / B / C / D | [URL or UNKNOWN] |

**Opportunity:** how can T212 match or beat the market 
standard while remaining defensible?

---

## 7) T212 defence arsenal

Quote the relevant excerpts from the context file that 
support the MVC counterproposal. Explain how each excerpt 
justifies the recommended position.

Relevant defence scripts to consider:
- Execution-only
- Disproportionate friction
- Educated user
- Proportionality and MVC
- Progressive profiling justification
- Operational scalability

---

## 8) Edge cases and risks

For each edge case:
- Scenario description
- Blocker or manageable
- Non-blocking mitigation

---

## 9) Final counterproposal

- **Replace:** [current demand or control]
- **With:** [MVC alternative]
- **Because:** [hard law reasoning and disproportionate 
  friction argument]
- **Residual risk accepted:** [explicit statement]
- **Monitoring and backstop:** [how we catch the 1% 
  without blocking 100%]

---

## Handover block
```
## Reg Product Factory — Handover Block
**From:** Comp Audit (Step 03b)
**To:** Market Research (Step 04)
**Date:** [today's date]

---

### Initiative summary
- **Initiative:** [name]
- **Entities:** [list]
- **Account types:** [list]
- **Driver:** [driver]
- **Deadline:** [deadline or "none"]

---

### Audit verdict
- **Status:** GREEN / AMBER / RED
- **Decision:** [one-line decision]

---

### Confirmed MVC path
- **What hard law actually requires:** [plain English]
- **What has been rejected as gold-plating:** [list]
- **Agreed friction level:** 
  None / Inline nudge / Checkbox / 
  Interstitial / Hard block

---

### Third-rail flags
- [List or "None identified"]
- [Include agreed defence if applicable]

---

### Citation status
- **Verified:** [list with sources]
- **Disputed or unknown:** [list with notes]

---

### What Market Research must find
- Competitors to benchmark by entity: [list]
- UX patterns to look for: [list]
- Friction points to validate: [list]

---

### Open unknowns
- [List all UNKNOWNs and ASSUMPTIONs]

---

### Attached documents
- [List or "None"]
```
