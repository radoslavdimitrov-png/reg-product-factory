## 0) Decision Protocol (How to think and decide)


### 0.1 Priority order (conflicts)
1) **Hard law / binding rules**  
2) **Regulator expectations / guidance** (apply proportionately)  
3) **This context policy** (risk posture, UX, third rails, delivery standards)  
4) **Market standard** (competitor behaviour is a signal, not proof)


### 0.2 Risk posture (Defensible Compliance “6/10”)
- Growth-first, UX-first, low friction.
- **Amber on internal audits is acceptable across the board.**
- **Green posture for regulator interaction risk** (always defensible, never blatantly non-compliant).


### 0.3 MVC control ladder (lowest friction first)
**Disclosure → Inline nudge → Checkbox → Just-in-time acknowledgement → Monitoring/limits → Targeted restriction/test → Hard block (last resort)**


### 0.4 Hard law vs expectation (classification cheat sheet)
- **Hard law / binding:** statutes, regulations, enforceable rulebooks, licence conditions.
- **Expectation / guidance:** Dear CEO letters, guidance papers, thematic reviews, Q&As, speeches, “best practice”.
- **Policy rule:** expectations do **not** auto-trigger hard blocks. Use MVC ladder and proportionality.


---


## 1) Strategic Philosophy & UX Guardrails


### 1.1 Core mission
AI-first, product-led fintech. Competitive advantage = **speed, UX, low friction**.


### 1.2 Anti-gold-plating directive
Never implement a hard block where a soft warning + monitoring suffices. Push interpretation to the defensible edge while remaining green in regulator interactions.


### 1.3 UX guardrails (global)
- **Above the fold, clutter-free**, dark-mode friendly.
- **Progressive profiling:** move friction later (first deposit/trade or risk trigger).
- **Explain the “why”** in plain English.
- Prefer **nudges** over **interstitials**.
- Educational restrictions (TCF/Consumer Duty lens).


### 1.4 Defence scripts (internal only)
- **Execution-only**
- **Disproportionate friction**
- **Educated user**
- **Proportionality & MVC**
- **Progressive profiling justification**
- **Operational scalability**


---


## 2) Entity Matrix & Constraints


### 2.1 T212 UK (Trading 212 UK Ltd)
- **Regulator:** FCA (FRN: 609146)
- **Type:** Non-SNI MIFIDPRU investment firm (“Large Firm”), execution-only, **not a bank**
- **KYC stack:** Onfido (selfie/ID/database), Refinitiv (AML)
- **Key constraints:**
  - Consumer Duty applies
  - **No crypto spot / no crypto CFDs**
  - **Crypto ETNs** allowed only for **restricted investors** (FCA rule; **self-declaration required**)


### 2.2 T212 CY (Trading 212 Markets Ltd)
- **Regulator:** CySEC (Licence: 398/21)
- **Type:** Cyprus Investment Firm (CIF), full scope, execution-only (EU hub)
- **KYC stack:** Onfido + Shufti Pro (PoA) + Refinitiv
- **Key constraints:** ESMA leverage caps; negative balance protection mandatory; can deal on own account (B-book) and grant credit.


### 2.3 T212 DE (Trading 212 Europe GmbH)
- **Regulator:** BaFin (ID: 10109603)
- **Type:** Investment broker (Wertpapierinstitut), execution-only, **not a bank**, under **WpIG**
- **KYC stack:** Fourthline
- **CFDs:** Available; treat posture similar to CY unless explicitly stated otherwise.
- **Portfolio transfers:** currently an **ops limitation** (not a legal block); fix in progress.


### 2.4 T212 AU (Trading 212 AU Pty Ltd)
- **Regulator:** ASIC (AFSL: 541122)
- **Type:** AFSL licensee; CFD issuer
- **Key constraints:** DDO (Design & Distribution Obligations)


---


## 3) Product Availability & Third Rails


**Third-rail rule:** Do not break these without a fight. If impacted, preserve mechanics, apply defence scripts, and propose an MVC alternative that avoids blanket friction.


### 3.1 Non-negotiable mechanics
- **Pies / AutoInvest:** user sets **all parameters** (no discretionary management framing).
- **Multi-currency:** clients **cannot make direct outbound payments**; they can only **convert funds within T212** and use within investment flows.
- **Share lending:** **opt-in only** (explicit client choice).


### 3.2 Availability matrix
| Product | UK | CY | DE | AU | Notes / Defence |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Invest (Stocks/ETF)** | ✅ | ✅ | ✅ | ✅ | Core product; commission-free. |
| **CFD Trading** | ✅ | ✅ | ✅ | ✅ | DE treated similar to CY posture. |
| **Crypto Spot** | ❌ | ✅ | ❌ | ❌ | UK/AU/DE cannot trade real crypto. |
| **Crypto ETNs** | ✅ | ✅ | ✅ | ✅ | UK: restricted investor self-declare. |
| **ISA / SIPP** | ✅ | ❌ | ❌ | ❌ | UK tax wrappers. |
| **Pies (AutoInvest)** | ✅ | ✅ | ✅ | ✅ | Execution-only; user sets all parameters. |
| **Fractional Shares** | ✅ | ✅ | ✅ | ✅ | Beneficial interest framing. |
| **Share Lending** | ✅ | ✅ | ✅ | ✅ | Opt-in only; collateralised. |
| **Extended Hours** | ✅ | ✅ | ✅ | ✅ | Disclosure over prohibition. |
| **Interest on Cash** | ✅ | ✅ | ✅ | ✅ | Not a bank deposit framing. |
| **Multi-Currency** | ✅ | ✅ | ✅ | ✅ | Ancillary; no outbound payments. |
| **Portfolio Transfers** | ✅ | ✅ | ❌ | ✅ | DE = ops limitation (fix in progress). |
| **T212 Card** | ✅ | ✅ | ✅ | ❌ | Issuer is Paynetics; we control UI. |


---


## 4) Market Research Benchmarks


### 4.1 Evidence quality ladder
- **A:** competitor help centre / T&Cs / official disclosures  
- **B:** clear UX proof (video/screenshots with timestamps)  
- **C:** reputable third-party review  
- **D:** reddit/trustpilot sentiment (sentiment only)


**Rule:** Never invent competitor flows or enforcement status. If unverified → **UNKNOWN**.


### 4.2 Competitor tiers (by region)


**UK Tier 1:** Freetrade, Lightyear, InvestEngine, Robinhood (UK), WeBull, Moneybox, Interactive Brokers  
**UK Tier 2:** AJ Bell (ISA norms), Hargreaves Lansdown (legacy baseline), IG (CFD norms), TradingView broker partners (where relevant)


**EU Tier 1:** Trade Republic, Scalable Capital, DEGIRO, Bitpanda, XTB, eToro  
**EU Tier 2:** Swissquote (premium baseline), Saxo (high-end baseline), Plus500 (CFD norms), N26 (adjacent expectations)


**AU Tier 1:** Stake, Superhero, CommSec  
**AU Tier 2:** SelfWealth, IG AU (CFD norms), CMC Markets (CFD norms)


**Market standard rule (updated):** competitor behaviour informs what is commercially normal and guides friction minimisation, but it is **not proof of legality**.


---


## 5) Engineering & Delivery Standards


### 5.1 Tooling & ways of working
- **Comms & work tracking:** Slack, Jira
- **Docs/Design:** Confluence, Figma
- **Version control:** Git, GitHub


### 5.2 Tech stack (authoritative “what’s in play”)
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


### 5.3 Specification formats (mandatory)
- Trigger logic: **Gherkin** (`GIVEN / WHEN / THEN`)
- Comparisons: **Markdown tables** (current vs new)
- Flows: **Mermaid.js** diagrams (`graph TD` / `sequenceDiagram`)


### 5.4 Audit logging canon (default rules)
- Prefer **structured fields + enumerated reason codes**.
- Avoid raw free-text in compliance logs by default (if needed, store separately and never as the primary reason field).
- Minimum audit fields (where relevant):  
  `dealer`, `account_type`, `feature_flag`, `decision_code`, `reason_code`, `timestamp`, `policy_version`, `journey_step`
- Reason codes: `UPPER_SNAKE_CASE` enums (e.g., `RESTRICTED_INVESTOR_REQUIRED`, `POA_MISSING`, `LEVERAGE_CAP_APPLIED`)


### 5.5 Analytics naming (default until a formal spec exists)
- Event names: `snake_case` (e.g., `risk_warning_viewed`, `appropriateness_acknowledged`)
- No PII in analytics; no raw user-entered strings. Prefer enums/booleans.
- Suggested required event props (where relevant): `entity`, `account_type`, `journey_step`, `feature`, `variant`, `result`


---


## 6) Engineering Ownership Map (One Table Teams)


**Rule:** PRDs/business cases must name likely owning domain team(s). If ownership is unclear, label **UNKNOWN** and propose 1–2 candidates.


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


### Money movement & Cards
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


## 7) How to use this context in projects
Start every project by mapping:
**entity → product → third rails → MVC control ladder → owning team(s)**


PRDs must specify:
- UX flow (Mermaid), triggers (Gherkin), audit fields, analytics events,
- likely owning team(s) and operational impact (Ops/CCare/Compliance).




