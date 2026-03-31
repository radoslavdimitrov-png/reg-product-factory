```markdown
# Detailed Compliance and AML Setup: Trading 212 ME Limited (T212 ME)

This document provides a highly detailed, comprehensive overview of the regulatory, operational, and compliance framework for Trading 212 ME Limited (T212 ME). It is designed to be fed into LLMs (like GPT or Claude) for detailed gap analysis, risk assessments, and the drafting of Compliance and AML onboarding procedures.

---

## 1. Corporate Profile and Regulatory Permissions
*   **Entity Location:** Dubai International Financial Centre (DIFC).
*   **Regulator:** Dubai Financial Services Authority (DFSA).
*   **Prudential Category:** Category 2 (Matched Principal).
*   **Authorised Financial Services:** 
    *   Dealing in Investments as Principal (Restricted to Matched Principal basis only).
    *   Dealing in Investments as Agent.
    *   Arranging Deals in Investments.
    *   Providing Custody.
*   **Endorsements:** 
    *   Retail Client Endorsement (to deal with Retail Clients).
    *   Holding or Controlling Client Assets (Client Money and Client Investments).
*   **Governance & Three Lines of Defence:** 
    *   **First Line:** Business units, Finance (Head of Finance: Ivan Goranov), and Operations.
    *   **Second Line:** Compliance & AML (CO/MLRO: Phil Whittaker, outsourced to ACA Effecta until a permanent hire in Dec 2025; Deputy MLRO: Jamie Martin) and Risk (Head of Risk: Michael Worms). Governed by the Risk and Compliance Committee (RCC).
    *   **Third Line:** Internal Audit (outsourced to Crowe Mak Limited). External Audit is handled by PwC.

## 2. Business Model and Target Market
*   **Execution-Only Model:** The firm operates strictly on an execution-only basis. It provides no investment advice, no discretionary portfolio management, and no recommendations.
*   **Target Market Profile:** 100% Retail Clients. The firm will exclusively onboard natural persons and will **not** accept Professional Clients, Market Counterparties, or corporate/institutional entities.
*   **Digital Delivery:** Services are delivered entirely via a proprietary mobile-first and web-based trading platform developed by Trading 212 Bulgaria (T212 BG). 

## 3. Products and Service Flows
The firm offers two distinct account types with different execution models:

*   **T212 INVEST Account (Dealing as Agent):** 
    *   **Products:** Equities, Exchange Traded Funds (ETFs) from major exchanges (US, Canada, UK, EU, Swiss), and complex Exchange Traded Products (ETCs, Leveraged/Inverse ETPs).
    *   **Execution:** Executed on an agency basis via Trading 212 UK Ltd (T212 UK), which may use third-party external brokers (TPEBs) like Interactive Brokers.
*   **T212 CFD Account (Dealing as Matched Principal):**
    *   **Products:** Contracts for Difference (CFDs) traded OTC, referencing equities, indices, index futures, commodity futures, and FX. **No crypto products are offered.**
    *   **Execution:** T212 ME acts as the principal counterparty to the retail client, but automatically hedges 100% of trades back-to-back with T212 UK to ensure zero proprietary market risk. 

## 4. Digital Onboarding, KYC, and AML Controls
The firm’s digital onboarding journey incorporates stringent automated controls to prevent the onboarding of out-of-appetite clients.

*   **Inherent Risk Profile:** The UAE's 2024 National Risk Assessment (NRA) rates the brokerage sector in financial free zones as having a "medium-high" inherent money laundering risk.
*   **Identity & Verification (ID&V):** Automated screening is conducted using **Refinitiv World-Check One** to screen for Sanctions, Politically Exposed Persons (PEPs), and Adverse Media. Additional background screening tools like Zinc Work are used for employee vetting.
*   **FATCA & US Persons Strict Prohibition:** The firm has a zero-tolerance policy for U.S. Persons. The system automatically blocks onboarding if a client declares U.S. citizenship, a U.S. address, or a U.S. place of birth. 
*   **Common Reporting Standard (CRS):** Clients must provide all tax residencies and Tax Identification Numbers (TINs). They must also sign an IRS Form W-8BEN (certifying non-U.S. status) under penalty of perjury.
*   **Client Classification & Suitability:** Because no advice is given, no suitability assessments are conducted. All clients are defaulted to Retail Clients by the system.
*   **Appropriateness Assessment:** Access to complex products (CFDs and complex ETPs) requires passing a mandatory electronic Appropriateness Assessment (knowledge and experience test) during onboarding. If a client fails, the system automatically denies them access to the product.

## 5. Market Abuse and Transaction Monitoring
*   **Transaction Surveillance:** To mitigate the risk of market abuse (insider dealing, market manipulation, fictitious devices), T212 ME utilizes a third-party automated transaction monitoring system called **Eflow**.
*   **Alert Management:** Eflow categorizes alerts into three main buckets: Market Manipulation, Insider Trading, and Trading Pattern. The Compliance Team reviews these daily.
*   **Reporting:** Where suspicion remains, a Suspicious Transaction and Order Report (STOR) is documented and submitted to the DFSA.

## 6. Client Money and Asset Protection (CASS)
The firm enforces strict separation of client assets from house assets.

*   **Client Money:** Client funds are deposited into segregated, multi-currency accounts held with **Barclays Bank PLC** within one business day of receipt. Barclays provides a formal acknowledgement letter confirming the funds are free from lien, set-off, or counterclaim.
*   **Client Investments (Safe Custody):** T212 ME is the primary Custodian. T212 UK acts as the Sub-Custodian, holding assets in omnibus accounts with ultimate Third-Party External Brokers (TPEBs) like Interactive Brokers Ireland and BNY Mellon.
*   **Margin & Leverage:** T212 ME does not offer traditional equity margin lending. Leverage is only available on CFDs. Clients must use cash as collateral; no securities are accepted. Clients benefit from Negative Balance Protection, and an automated system closes out positions if net account equity drops below 50% of required margin.
*   **Reconciliations:** Finance and Operations teams conduct dual-control daily internal and external reconciliations. Exceptions must be investigated within 24 hours and escalated to the SEO if unresolved within T+2.

## 7. Third-Party Risk Management (TPRM) and Outsourcing
T212 ME leverages an extensive intra-group outsourcing model governed by a strict TPRM framework aligned with EBA and DORA guidelines.

*   **Trading 212 BG (Bulgaria):** Regulated by the FSC, T212 BG provides the proprietary trading platform, IT maintenance, client onboarding/offboarding, customer support, complaint handling, and AML/Fraud monitoring support.
*   **Trading 212 UK Ltd (UK):** Regulated by the FCA, T212 UK provides trade execution, sub-custody, CFD hedging, and advisory support on IT governance and cyber resilience.
*   **Oversight:** Any sub-outsourcing by T212 BG requires prior written approval from T212 ME. T212 ME retains full accountability for compliance, exercises independent monitoring, and retains full audit and inspection rights.

## 8. Conduct, Complaints, and Record Keeping
*   **Complaints Handling:** Managed centrally via Zendesk. The firm must acknowledge complaints within 7 days, provide updates every 4 weeks, and issue a final written response within 8 weeks.
*   **Whistleblowing:** A robust policy exists protecting employees from liability or detriment when reporting suspected financial crime, DFSA rule breaches, or misconduct directly to the CO, SEO, or the DFSA.
*   **Conflicts of Interest & Personal Dealing:** Employees are subject to a strict Personal Account Transactions Policy, requiring CO approval (valid for 3 days) prior to any personal trades. Gifts above $300 (or $250 annually, according to differing manual appendices) must be declared and approved.
*   **Record Retention:** All records (Client agreements, ID&V data, trading history, reconciliations, marketing materials, and complaints) are securely maintained electronically for a minimum of 6 years. Voice recordings for trade negotiations are kept for a minimum of 6 months.
```
