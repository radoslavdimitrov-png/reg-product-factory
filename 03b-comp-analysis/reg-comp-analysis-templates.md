# REG Comp Analysis — Output Templates

---

## 1) Executive feasibility verdict

> **Status:** GREEN (Clear to build) / AMBER (Buildable
> with controlled friction) / RED (Blocked in target
> entity)
> **One-line decision:** Proceed / Proceed with changes /
> Do not build (for entity X)
> **Summary:** 2-3 sentences. State feasibility, the key
> regulatory constraint, and the recommended path.

---

## 2) Regulatory map

Include only the entities that are in scope for this
initiative. Do not include entities that are not affected.

| Entity | Status | Hard law requirement | Citation | Classification |
| :--- | :--- | :--- | :--- | :--- |
| [UK/CY/DE/AU/ME] | Allowed / Blocked | [plain English] | [verified URL or UNKNOWN] | Hard Law / Expectation / Nice-to-have |

---

## 3) Regulatory triggers and what to build

For each regulatory trigger identified:

**Trigger:** [name of the regulatory obligation]
**Applies to:** [entity or entities]
**What the rule actually requires:** [plain English —
what must be done]
**What it does not require:** [explicit statement of
what would be gold-plating]
**Classification:** Hard Law / Regulator Expectation /
Nice-to-have
**Citation:** [verified URL or UNKNOWN]

**What to build:**
- **Control:** [specific control from MVC hierarchy]
- **Placement:** [where in the journey, when it appears]
- **UX mechanism:** [disclosure / nudge / checkbox /
  interstitial / hard block]
- **Monitoring rule:** [what automated check runs in
  the background, what threshold triggers escalation]

---

## 4) Risks and edge cases

For each edge case or risk identified:
- **Scenario:** [description]
- **Severity:** Blocker / Manageable
- **Mitigation:** [non-blocking approach where possible]

---

## 5) Final recommendation

- **Build:** [what we ship in plain English]
- **Controls:** [short list of what is being implemented
  and why]
- **Blocked entities:** [list or "None"]
- **Residual risk accepted:** [explicit statement of
  what risk remains and why it is acceptable at 6/10]

---

## Handover block
```
## Reg Product Factory — Handover Block
**From:** Comp Analysis (Step 03a)
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

### Feasibility verdict
- **Status:** GREEN / AMBER / RED
- **Decision:** [one-line decision]

---

### Confirmed regulatory position
- **What hard law requires:** [plain English summary
  per entity]
- **What has been scoped out as unnecessary:**
  [list or "none"]
- **Agreed control for each trigger:** [list]
- **Agreed friction level:**
  None / Inline nudge / Checkbox /
  Interstitial / Hard block

---

### Verified regulatory sources
- [Citation — entity — verified URL]
- [Or "None verified — see unknowns below"]

---

### What Market Research must find
- Competitors to benchmark by entity: [list from
  competitor tiers in context file]
- Specific UX patterns to look for: [e.g. "how do
  they handle this control — quiz, disclaimer,
  or checkbox?"]
- Specific friction points to validate against
  market standard: [list]

---

### Open unknowns
- [List all UNKNOWNs and ASSUMPTIONs carried forward]

---

### Attached documents
- [List or "None"]
```
