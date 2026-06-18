# Compliance Context — T212 ME

**Entity:** Trading 212 ME Limited
**Maintained by:** Reg Product team
**Purpose:** Entity-specific regulatory context for the REG
Compliance Research tool. Holds what is true for ME only. The
cross-entity decision rules live in the tool's own instructions.

Language: British English. No em dashes.

---

## Regulatory identity

- **Regulator:** DFSA (Dubai Financial Services Authority)
- **Location:** Dubai International Financial Centre (DIFC)
- **Prudential category:** Category 2 (Matched Principal)
- **Entity type:** Authorised firm, execution-only
- **Service model:** Execution-only. No advice, no discretionary
  management. Retail clients only.

**Authorised activities:**
- Dealing in Investments as Principal (Matched Principal only)
- Dealing in Investments as Agent
- Arranging Deals in Investments
- Providing Custody

**Endorsements:** Retail Client Endorsement; Holding or
Controlling Client Assets.

---

## Regulatory lens — what makes ME distinct

Read ME through a DFSA Rulebook lens. This is not MiFID, not FCA,
not ASIC. Do not transfer rules from the other entities by
analogy. Where a DFSA-specific position is needed, verify it
against the DFSA Rulebook directly rather than assuming the EU or
UK rule applies.

Three structural features define ME:

- Retail only. No professional clients, market counterparties, or
  institutional clients.
- Matched Principal on CFDs. ME acts as counterparty but hedges
  100% back-to-back with T212 UK, so it carries no proprietary
  market risk.
- Strict US Persons exclusion under FATCA. Onboarding is blocked
  automatically on detection of US citizenship, birth, or address.

The DIFC brokerage sector is rated medium-high risk for money
laundering in the UAE National Risk Assessment, so AML controls
carry weight here.

---

## Product permissions — high level

ME is the least-confirmed entity for product availability. Many
permissions are genuinely unconfirmed. Where a product is marked
UNKNOWN below, the tool must treat it as UNKNOWN and not assume
availability either way. Verify against the DFSA position and the
current catalogue.

**Confirmed allowed in ME:**
- Invest: stocks and ETFs, on an agency basis executed via T212
  UK
- CFDs: matched principal, hedged 100% with T212 UK
- Complex ETPs, with mandatory appropriateness assessment before
  access
- Interest on cash via qualifying money market funds
- Client Trading API

**Confirmed not available in ME:**
- Crypto spot
- ISA and SIPP
- T212 Card

**UNKNOWN, verify before relying:**
- Crypto ETNs
- Pies and AutoInvest
- Fractional shares
- Share lending
- Extended hours and 24/5 trading
- Multi-currency account
- Portfolio transfers
- Model Portfolios

---

## Core mechanics to protect

Where these products turn out to be available in ME, the
group-wide mechanics apply: Pies execution-only with all
parameters client-set, multi-currency no outbound payments, share
lending opt-in only. But note all three are currently UNKNOWN for
ME availability, so confirm the product exists in ME before
applying its mechanic.

---

## Entity-specific regulatory constraints

Verify the precise current rule by browsing or against the DFSA
Rulebook before relying on any of these.

- **Appropriateness assessments:** mandatory for CFDs and complex
  ETPs. Failure results in denied access to those products.
- **No suitability assessments:** execution-only, no advice, so
  suitability obligations do not arise.
- **Client classification:** all clients default to Retail during
  digital onboarding.
- **AML:** medium-high ML risk rating for the DIFC brokerage
  sector means AML controls should be treated as a heightened
  area. Screening is via Refinitiv World-Check One.
- **US Persons:** strict zero-tolerance FATCA exclusion at
  onboarding.
- **Client assets:** ME is custodian, with T212 UK as
  sub-custodian. Client money is segregated at Barclays Bank PLC.

---

## Known open items to verify

- The majority of product availability for ME is unconfirmed, as
  marked above. This is the entity where guessing is most
  dangerous. Treat every UNKNOWN as a genuine gap requiring
  confirmation, not a default to yes or no.
- Specific DFSA Rulebook references should be verified directly,
  since DFSA rules do not map onto the EU or UK frameworks the
  other entities use.
