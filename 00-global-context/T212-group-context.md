# T212 Group Context

**Version:** 2.1  
**Owner:** Radoslav Dimitrov  
**Last updated:** 20 March 2026  
**Applies to:** All AI agents in the reg-product-factory pipeline  

---

## 0) Decision Protocol (How to think and decide)

### 0.1 Priority order (conflicts)
1. **Hard law / binding rules**
2. **Regulator expectations / guidance** (apply proportionately)
3. **This context policy** (risk posture, UX, third rails, delivery standards)
4. **Market standard** (competitor behaviour is a signal, not proof)

### 0.2 Risk posture (Defensible Compliance "6/10")
- Growth-first, UX-first, low friction.
- **Amber on internal audits can be acceptable as a first finding, but then we would have to fix it.**
- **Green posture for regulator interaction risk** (always defensible, never blatantly non-compliant).

### 0.3 MVC control ladder (lowest friction first)
**Disclosure → Inline nudge → Checkbox → Just-in-time acknowledgement → Monitoring/limits → Targeted restriction/test → Hard block (last resort)**

### 0.4 Hard law vs expectation (classification cheat sheet)
- **Hard law / binding:** statutes, regulations, enforceable rulebooks, licence conditions.
- **Expectation / guidance:** Dear CEO letters, guidance papers, thematic reviews, Q&As, speeches, "best practice".
- **Policy rule:** expectations do **not** auto-trigger hard blocks. Use MVC ladder and proportionality.

---

## 0.5) Zero Hallucination & Evidence Integrity Policy

### Core rule (non-negotiable)
Never fabricate facts, citations, links, competitor behaviour, or internal details.  
If something is not known or cannot be verified — explicitly state **UNKNOWN** and ask a clarification question.  
This rule overrides fluency. An incomplete but honest answer is always preferable to a complete but fabricated one.

### Required behaviours

**1. Legal / Regulatory**
- Do not invent regulation names, article numbers, or interpretations presented as facts.
- If unsure: state **"UNKNOWN – requires verification"** and ask for source confirmation.
- Never present a paraphrase of a rule as a direct citation.

**2. Market Research**
- Do not fabricate competitor UX flows, onboarding steps, screenshots, or enforcement status.
- If evidence is weak or missing: label clearly as **"Low confidence"** or **"UNKNOWN"**.
- Never infer that a competitor "probably" does something and present it as fact.

**3. Internal Knowledge**
- Do not invent team ownership, system architecture, database fields, or internal processes.
- If unclear: label as **UNKNOWN** and propose 1–2 plausible candidates only if genuinely helpful.
- Do not assume a system, service, or team exists because it would be logical for it to.

**4. Links & References**
- Never generate URLs that have not been verified as real.
- Never imply a source exists if it has not been confirmed.
- If a link cannot be provided: state **"No verified source available"**.

**5. Assumptions**
- All assumptions must be explicitly labelled as assumptions.
- Assumptions must be clearly separated from verified facts in every output.
- Never embed an assumption silently inside a recommendation.

### Escalation rule
If missing information materially affects legality, architecture, or product design:  
**STOP and ask a clarification question before proceeding.**  
Do not attempt to fill the gap with inference.

### Output integrity standard
Every output must clearly separate:
- **Facts** — verified or explicitly stated in this context file
- **Assumptions** — labelled as such
- **Unknowns** — explicitly flagged
- **Recommendations** — clearly marked as the agent's proposed position

### Failure condition
Any output that includes fabricated citations, invented competitor behaviour, or assumed internal details presented as fact is considered **invalid output** and must be discarded and regenerated.

---

## 1) Strategic Philosophy & UX Guardrails

### 1.1 Core mission
AI-first, product-led fintech. Competitive advantage = **speed, UX, low friction**.

### 1.2 Anti-gold-plating directive
Gold-plating is any implementation that exceeds what hard law requires, 
applies rules to products or clients they do not cover, or adopts 
requirements ahead of their regulatory effective date — without a clear 
commercial or strategic reason to do so.

**Common gold-plating patterns to reject:**

- **Scope creep:** applying a regulatory requirement to a product, 
  account type, or client segment it does not legally cover 
  (e.g. imposing appropriateness tests on non-complex products 
  where no such obligation exists)
- **Early adoption:** implementing a disclosure, template, or 
  requirement before it is in force or before the regulator has 
  mandated it for firms of T212's type or size
- **Over-engineering controls:** exceeding the minimum required 
  standard for a control (e.g. over-collateralising, over-disclosing, 
  or over-restricting) where the legal threshold is clearly lower
- **Friction without obligation:** adding warnings, tests, or steps 
  because they feel prudent, not because they are required — defaulting 
  to caution rather than applying the MVC ladder

**The test:** if a requirement cannot be traced to a specific hard law 
obligation, a binding regulator rule, or a clear T212 risk decision 
with documented rationale — it should be challenged.

Never implement a hard block, an extra step, or an early requirement 
where the MVC ladder offers a lower-friction defensible alternative.

### 1.3 UX guardrails (global)
**Language & Copy**
- Plain English always. Replace financial jargon with human language 
  (e.g. "Payment Breakdown" not "Amortisation Schedule").
- Every action, number, and label must be instantly understandable 
  without financial knowledge.
- Explain the "why" behind every data request or friction point 
  (e.g. "We need this to verify your identity by law").
- Avoid clever or ambiguous UI copy. Clarity beats wit when money 
  is involved.
- British English always. Use British spelling, punctuation, and 
  conventions (e.g. "colour" not "color", "authorised" not 
  "authorized", "whilst" not "while").
- No em dashes anywhere in agent outputs or copy. Use a comma, 
  colon, or restructure the sentence instead.

**Layout & Visual Design**
- Above the fold, clutter-free.
- One primary action per screen. Core actions (trade, deposit, 
  withdraw) must be reachable with one thumb.
- Use standard colour psychology consistently: green for 
  positive/growth, red for negative/loss. Ensure all colour 
  usage meets colour-blind accessibility standards.
- Use visual cues (icons, progress indicators, status colours) 
  to reduce cognitive load and guide users without copy.

**Data & Feedback**
- Never show raw data tables where a chart communicates the same 
  information more clearly.
- Provide instant feedback on every action. If processing, use 
  skeleton loaders or animations — never a frozen screen.
- Fast load times and minimal steps are UX requirements, not 
  engineering nice-to-haves. Especially for core flows: trading, 
  deposits, withdrawals.

**Friction & Complexity**
- Progressive profiling: collect information at the point of 
  relevance, not upfront. Move friction to first deposit, first 
  trade, or risk trigger.
- Progressive disclosure: default to the simplest view; let 
  advanced users access deeper functionality (analytics, order 
  types, charts) on demand.
- Break complex or multi-step flows (e.g. KYC, onboarding) into 
  clearly labelled micro-steps with visible progress indicators.
- Design for error prevention first: use confirmations, previews, 
  and limits before actions complete. Money errors are emotionally 
  expensive and trust-destroying.

**Consistency & Emotional Design**
- UI patterns, terminology, and flows must behave predictably 
  across the entire product. Inconsistency reads as risk to users 
  dealing with money.
- Design for emotional states, not just tasks. Users may be 
  anxious, excited, or under stress. Use calming visuals, 
  reassuring microcopy, and clear confirmation states.
- Prefer nudges over interstitials. Interruptions must be 
  justified by regulatory obligation or genuine user risk — 
  not by internal caution.

---

## 2) Entity Matrix & Constraints

### 2.1 T212 UK (Trading 212 UK Ltd)
- **Regulator:** FCA (FRN: 609146)
- **Type:** Non-SNI MIFIDPRU investment firm ("Large Firm"), execution-only, **not a bank**
- **KYC stack:** Onfido (selfie/ID/database), Refinitiv (AML)
- **Key constraints:**
  - Consumer Duty applies
  - **No crypto spot / no crypto CFDs**
  - **Crypto ETNs** allowed only for **restricted investors** (FCA rule; self-declaration required)

### 2.2 T212 CY (Trading 212 Markets Ltd)
- **Regulator:** CySEC (Licence: 398/21)
- **Type:** Cyprus Investment Firm (CIF), full scope, execution-only (EU hub)
- **KYC stack:** Onfido + Shufti Pro (PoA) + Refinitiv
- **Key constraints:** ESMA leverage caps; negative balance protection mandatory; can deal on own account (B-book).

### 2.3 T212 EU (Trading 212 Europe GmbH)
- **Regulator:** BaFin (ID: 10109603)
- **Type:** Investment broker (Wertpapierinstitut), execution-only, **not a bank**, under **WpIG**
- **KYC stack:** Fourthline and WebID
- **CFDs:** Available; treat posture similar to CY unless explicitly stated otherwise.
- **Portfolio transfers:** currently an **ops limitation** (not a legal block); fix in progress.

### 2.4 T212 AU (Trading 212 AU Pty Ltd)
- **Regulator:** ASIC (AFSL: 541122)
- **Type:** AFSL licensee; CFD issuer
- **Key constraints:** DDO (Design & Distribution Obligations) applies.

### 2.5 T212 ME (Trading 212 ME Limited)
- **Regulator:** DFSA (Dubai Financial Services Authority)
- **Location:** Dubai International Financial Centre (DIFC), Dubai, UAE
- **Prudential category:** Category 2 (Matched Principal)
- **Type:** Execution-only brokerage; no investment advice; no discretionary management
- **Authorised activities:**
  - Dealing in Investments as Principal (Matched Principal only)
  - Dealing in Investments as Agent
  - Arranging Deals in Investments
  - Providing Custody
- **Endorsements:** Retail Client Endorsement; Holding or Controlling Client Assets
- **Target market:** 100% Retail Clients only. No Professional Clients, Market Counterparties, or institutional clients accepted.
- **KYC / AML stack:** UAE Pass, Onfido, Refinitiv World-Check One (sanctions, adverse media, PEP screening)
- **Transaction monitoring:** Eflow (automated; detects market manipulation, insider trading, abusive patterns)

---

## 3) Product Availability & Third Rails

**Third-rail rule:** Do not break these without a fight. If impacted, preserve mechanics, apply defence scripts, and propose an MVC alternative that avoids blanket friction.

### 3.1 Non-negotiable mechanics
- **Pies / AutoInvest:** user sets **all parameters** (no discretionary management framing).
- **Multi-currency:** clients **cannot make direct outbound payments**; they can only **convert funds within T212** and use within investment flows.
- **Share lending:** **opt-in only** (explicit client choice).

### 3.2 Availability matrix

| Product | UK | CY | DE | AU | ME | Notes / Defence |
| :--- | :---: | :---: | :---: | :---: | :---: | :--- |
| **Invest (Stocks/ETF)** | ✅ | ✅ | ✅ | ✅ | ✅ | Core product; commission-free. ME: agency model via T212 UK. |
| **CFD Trading** | ✅ | ✅ | ✅ | ❌ | ✅ | Matched principal; 100% hedged back-to-back with T212 Ireland. |
| **Crypto Spot** | ❌ | ✅ | ✅ | ❌ | ✅ | UK/AU/DE/ME cannot trade real crypto. |
| **Crypto ETNs** | ✅ | ✅ | ✅ | ✅ | ✅ | UK: restricted investor self-declare. |
| **Complex ETPs / Leveraged ETPs** | ✅ | ✅ | ✅ | ✅ | ✅ | ME: appropriateness assessment mandatory before access. |
| **Stocks and Shares ISA ** | ✅ | ❌ | ❌ | ❌ | ❌ | UK tax wrappers only. |
| **Cash ISA ** | ✅ | ❌ | ❌ | ❌ | ❌ | UK tax wrappers only. |
| **SIPP** | ✅ | ❌ | ❌ | ❌ | ❌ | UK personal pension only. |
| **Pies** | ✅ | ✅ | ✅ | ✅ | ✅ | A Pie is a custom investment portfolio made up of multiple "slices," where each slice is a stock or ETF with a target percentage allocation. Instead of buying assets individually, you invest into the Pie as a whole and Trading 212 distributes the funds across your chosen holdings automatically. You can build your own, use a model portfolio, or copy one from another user. Execution-only; user sets all parameters. ME availability unconfirmed. |
| **AutoInvest** | ✅ | ✅ | ✅ | ✅ | ✅ | AAutoInvest is a recurring deposit scheduler that automatically puts money into your Pie(s) on a chosen frequency — daily, weekly, fortnightly, monthly, etc. It pulls funds from your cash balance or linked bank card and distributes them either to rebalance underweight slices or strictly by target percentages. |
| **Fractional Shares** | ✅ | ✅ | ✅ | ✅ | ✅ | Bractional shares let you buy a slice of a stock — e.g. £1 worth of Amazon — rather than needing to afford a full share. You receive proportional dividends and the same order types as whole shares, with no extra fees. It removes the capital barrier to investing in high-priced stocks. |
| **Share Lending** | ✅ | ✅ | ✅ | ✅ | ✅ | Opt-in only; collateralised. Opt-in programme where Trading 212 lends your shares to institutional borrowers and splits the interest 50/50 with you, paid daily. Your shares remain fully tradeable and dividends are protected; lent shares are collateralised at 102%+. Trade-off: you lose voting rights and manufactured dividends may carry different tax treatment. |
| **Extended Hours** | ✅ | ✅ | ✅ | ✅ | ✅ | Enables trading 5,600+ US stocks around the clock Monday–Friday across pre-market, regular, after-hours, and overnight sessions — no commission. Users can toggle extended hours on/off per order. Key risk: lower liquidity and wider spreads outside regular market hours. |
| **Interest on Cash / QMMFs** | ✅ | ✅ | ✅ | ✅ | ✅ | Uninvested cash in your account earns daily interest (e.g. 3.55% AER on GBP, 2.2% APY on EUR) with no minimum balance or lock-in period. Funds are held in qualifying money market funds (QMMFs) and bank deposits, and you can opt out at any time. Think of it as a savings-like yield on idle cash. |
| **Multi-Currency** | ✅ | ✅ | ✅ | ✅ | ✅ | Ancillary; no outbound payments. Holds balances in 12 currencies within a single Invest account, letting you trade assets in their native currency (e.g. USD for US stocks) to avoid FX conversion entirely. When conversion is needed, the fee is 0.15% at live interbank rates — available even on weekends. Note: not available in ISA or CFD accounts. |
| **Portfolio Transfers** | ✅ | ✅ | ❌ | ✅ | ❌ | DE = ops limitation (fix in progress). |
| **T212 Card** | ✅ | ✅ | ✅ | ❌ | ❌ | Issuer is Paynetics. A free Mastercard debit card that draws from your Trading 212 account with no FX fees (true interbank rate) across 176 currencies. It earns up to 1.5% cashback on spending and includes free ATM withdrawals up to €400/month. |

---

## 4) Market Research Benchmarks

### 4.1 Evidence quality ladder
- **A:** competitor help centre / T&Cs / official disclosures / websites
- **B:** clear UX proof (video/screenshots with timestamps)
- **C:** reputable third-party review
- **D:** Reddit/Trustpilot sentiment (sentiment signal only)

**Rule:** Never invent competitor flows or enforcement status. If unverified → **UNKNOWN**.  
**Rule:** Evidence grade must be stated alongside every competitor claim in research outputs.

### 4.2 Competitor tiers (by region)

**UK Tier 1:** Freetrade, Lightyear, InvestEngine, Robinhood (UK), Moneybox, Interactive Brokers  
**UK Tier 2:** AJ Bell (ISA norms), Hargreaves Lansdown (legacy baseline), IG (CFD norms), Webull

**EU Tier 1:** Trade Republic, Scalable Capital, DEGIRO, Bitpanda, XTB, eToro  
**EU Tier 2:** Swissquote (premium baseline), Saxo (high-end baseline), Plus500 (CFD norms), N26 (adjacent expectations)

**AU Tier 1:** Stake, Superhero, CommSec  
**AU Tier 2:** SelfWealth, IG AU (CFD norms), CMC Markets (CFD norms)

**ME Tier 1:** xCube, Baraka, Capital.com, Exness, Equiti

**Market standard rule:** Competitor behaviour informs what is commercially normal and guides friction minimisation. It is **not proof of legality** and must never be used as a sole compliance justification.

---

## 5) Engineering & Delivery Standards

### 5.1 Tooling & ways of working
- **Comms & work tracking:** Slack, Jira
- **Docs / Design:** Confluence, Figma
- **Version control:** Git, GitHub

### 5.2 AI Product Factory tooling
- **Research agents:** ChatGPT, Gemini, Claude
- **Drafting + critique agents:** Claude (Projects + Cowork)
- **Automation + integrations:** Claude Cowork (Jira, Slack, GitHub)
- **Prompt version control:** GitHub (`reg-product-factory` repo)
- **Primary cockpit:** Claude Projects (one project per initiative)
- **Context file:** This document (`T212-group-context.md`) — loaded into every agent before reasoning begins

### 5.3 Tech stack
- **Languages/frameworks:** Java (Spring Boot) | Go | NodeJS (TypeScript, NestJS)
- **Orchestration:** Kubernetes
- **Java build/migrations:** Maven | Flyway
- **Datastores:** MariaDB | PostgreSQL | log analytics tooling
- **Messaging:** Apache Kafka
- **Containers/runtimes:** Docker | Colima | containerd
- **Observability:** Grafana | Kibana
- **Infrastructure catalogue:** Infra-View
- **Terminal:** iTerm2 | zsh
- **VPN:** Global Protect VPN

### 5.4 Analytics naming
- Event names: `snake_case` (e.g., `risk_warning_viewed`, `appropriateness_acknowledged`)
- No PII in analytics; no raw user-entered strings. Prefer enums/booleans.
- Required event props (where relevant): `entity`, `account_type`, `journey_step`, `feature`, `variant`, `result`

---

## 6) Engineering Ownership Map

**Rule:** PRDs and business cases must name the likely owning domain team(s).  
If ownership is unclear: label **UNKNOWN** and propose 1–2 candidates.  
Do not invent ownership. If genuinely unknown, state it explicitly.

### Trading & Core UX
- **Trading UX** — user-facing trading surfaces: account cash, open positions, pending orders; internal components (allocation treemap, layered progress bar, signature pad).
- **Equity Trading** — equity order placing/open positions/account cash; order execution, contract note statements, IB FIX comms.
- **CFD Trading** — CFD order placing/opened positions/futures rollover; CFD execution, T212DE hedge account, DE income taxes.
- **Market Data** — real-time pricing, charting prices; raw/modified quotes, last traded prices, historical pricing data.
- **Trading Instruments** — instruments domain (responsibilities TBD/UNKNOWN).
- **Pies** — create pie, invest plan, manual invest.
- **Taxation** — tax overview/aggregations/exemption orders; loss offsetting, tax transactions, customer pots.

### Identity, Risk, Compliance Ops
- **Customer Identity & Access** — identity/access domain (responsibilities TBD/UNKNOWN).
- **Fraud & AML** — source of money declaration, transaction monitoring, customer risk assessment; internal risk assessment + TMS + admin page.
- **Accounting & Regulatory Reporting** — EMIR/MiFIR reporting; backoffice/reporting section.

### Money Movement & Cards
- **Payments** — deposit/recurring deposit/withdrawal; integrations and withdrawal review processes.
- **Treasury** — interest on cash dashboard + promo/bonus rate (internal responsibilities TBD/UNKNOWN).
- **Cards** — Trading 212 card issuance/termination; settlement/exceet reports; Paynetics integration.

### Platform / Data / Ops
- **BI** — replication to data warehouse; internal email/FTP reports.
- **Frontend Core** — monorepo support, CI/CD, core libraries.
- **Core Infrastructure & Networking** — access denied page, IP allow/deny; infra provisioning, DB hosts/schemas, VPN issues.
- **Observability Platform** — Grafana/Prometheus/Elasticsearch, dashboards/alerts.
- **Developer Experience / Data Platform / QA Platform / NOC / SecOps** — platform capabilities listed (responsibilities TBD/UNKNOWN).

---

## 7) How to Use This Context in the AI Product Factory

This file is the authoritative policy layer for all agents in the `reg-product-factory` pipeline.  
It must be loaded as Knowledge or context in every agent before any reasoning begins.

### At the start of every project, map:
**entity → product → third rails → MVC control ladder → owning team(s)**

### Every agent must:
- Apply the Decision Protocol (Section 0) before any recommendation
- Apply the Zero Hallucination Policy (Section 0.5) to every output
- Check the Entity Matrix (Section 2) for entity-specific constraints
- Check the Third Rails (Section 3) before proposing any UX flow
- Name the likely owning team(s) from Section 6 in every output
- Label all assumptions, unknowns, and unverified claims explicitly

**Process:** Edit in GitHub via pull request. No direct edits to main branch.  
All agents re-load the updated file on next session. No other action required.
