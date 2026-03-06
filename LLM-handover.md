You are producing a **CROSS-MODEL HANDOFF DOCUMENT** so I can transfer this project to **[TARGET LLM]**.


My next goal with the receiving AI is:
**[NEXT TASK / OUTCOME]**


I will attach an additional business context file to the receiving AI:
- **File name:** T212_Product_Contex.docx
- **Role:** Authoritative product philosophy + compliance/UX guardrails + constraints. Must be treated as **policy** for decisions.


## Hard Rules (must follow)
- **Do NOT invent** anything that was not explicitly stated or created in this session.
- If information is missing/uncertain, write **UNKNOWN** (do not guess).
- **No conversational filler.** Only project-relevant state.
- Preserve exact names, IDs, requirements, constraints, and wording where possible.
- **Artefacts must be copied verbatim** as they exist now (no paraphrase, no “cleanup,” no reformatting beyond Markdown fences).
- If artefacts are too large, include the most recent authoritative version and list the rest under **Omitted Artefacts** with a reason and where they appeared.
- Prefer atomic state over prose: constraints, decisions, definitions, TODOs, artefacts.


Format the output in **strict Markdown** using exactly this structure and headings:


# CROSS-MODEL HANDOFF STATE


## 0) External Context File (Must Read)
- **File:** T212_Product_Contex.docx
- **How it should be used:** Treat as authoritative business guardrails for UX, compliance posture, risk appetite, and product constraints. If any instructions conflict, prioritise: (1) system/developer policies, (2) the context file, (3) this handoff document, (4) user instructions.


## 1) Persona & Operating Protocol
- **Role/persona in this session:** [concise]
- **Decision-making rules:** [bullets]
- **Style constraints (tone/format):** [bullets]
- **Non-goals / forbidden actions:** [bullets]


## 2) Immutable Constraints & Definitions
- **Hard constraints:** [bullets]
- **Key definitions/terms of art:** [bullets]
- **Assumptions:** [bullets]
- **Unknowns / open questions:** [bullets]


## 3) Project Status Snapshot
- **What is done (outcomes):** [bullets]
- **What is partially done (work in progress):** [bullets]
- **What is not started:** [bullets]
- **Current best plan (1–5 steps):** [numbered]


## 4) Decisions Log (with rationale)
List important decisions in this format:
- **Decision:** …
  - **Reason:** …
  - **Alternatives considered:** …
  - **Implications/dependencies:** …


## 5) Working Artefacts (VERBATIM)
For each artefact, include:
- **Artefact name:**
- **Purpose:** [1 line]
- **Status:** [draft/review/final/unknown]
- **Content (verbatim):**
```[language-or-text]
[PASTE EXACT CONTENT HERE]




