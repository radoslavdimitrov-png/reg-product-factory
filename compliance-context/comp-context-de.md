# Compliance Context — T212 DE

**Entity:** Trading 212 Europe GmbH
**Maintained by:** Reg Product team
**Purpose:** Entity-specific regulatory context for the REG
Compliance Research tool. Holds what is true for DE only. The
cross-entity decision rules live in the tool's own instructions.

Language: British English. No em dashes.

---

## Regulatory identity

- **Regulator:** BaFin (Bundesanstalt für
  Finanzdienstleistungsaufsicht)
- **ID:** 10109603
- **Entity type:** Investment broker (Wertpapierinstitut) under
  the WpIG
- **Service model:** Execution-only. Not a bank.
- **Framework:** WpIG, German implementation of MiFID II, ESMA
  measures.

---

## Regulatory lens — what makes DE distinct

The single most important DE-specific point: T212 DE is an
investment broker under the WpIG (Wertpapierinstitutsgesetz), not
a bank under the KWG (Kreditwesengesetz). Apply the WpIG lens, not
the KWG lens. Analyses that treat DE as a bank are wrong at the
foundation. DE is not a deposit-taking institution and cash
interest must never be framed as a bank deposit.

Beyond that, treat DE's posture as similar to CY on CFDs unless a
German-specific rule says otherwise, since both sit under MiFID II
and ESMA, but always check for German overlays.

---

## Product permissions — high level

For compliance scoping. Confirm against the current product
catalogue for the authoritative live position.

**Allowed in DE:**
- Invest: stocks and ETFs, including fractional
- CFDs across shares, ETFs, indices, commodities, FX, and crypto.
  Crypto CFDs are live in DE.
- Crypto ETNs
- Complex and leveraged and inverse ETPs
- Pies and AutoInvest, and Model Portfolios
- Share lending (opt-in only)
- Extended hours and 24/5 trading
- Multi-currency account
- Interest on cash via qualifying money market funds
- Direct Debit AutoInvest into a Pie. DE only.
- Spending Pot
- T212 Card
- CFD futures rollover

**Not available in DE:**
- Crypto spot. Not offered.
- ISA and SIPP. UK only.

**Operational limitation, not a legal block:**
- Portfolio transfers are currently an operational limitation in
  DE, with a fix in progress. This is an ops constraint, not a
  regulatory prohibition. Treat it as such in any analysis.

---

## Core mechanics to protect

- Pies and AutoInvest are execution-only with the client setting
  all parameters.
- The multi-currency account does not permit outbound payments.
- Share lending is opt-in only.

---

## Entity-specific regulatory constraints

Verify the precise current rule by browsing before relying on
any of these.

- **WpIG framing:** the binding structural constraint. Broker, not
  bank. Cash interest is not a deposit.
- **ESMA CFD measures:** leverage caps by asset class and
  mandatory negative balance protection, as for CY.
- **BaFin overlays:** Germany sometimes applies national overlays
  on top of ESMA measures. Where CFDs or marketing are in scope,
  check for a BaFin-specific position rather than assuming the CY
  rule transfers directly. There has historically been a BaFin
  CFD general administrative act (Einzelverfügung) relevant to
  CFD marketing and leverage. Verify its current form.
- **Appropriateness for complex products:** required for complex
  instruments. CFDs and complex ETPs fall here.

---

## Known open items to verify

- The current BaFin CFD position and any active general
  administrative act should be verified against current BaFin
  publications.
- ESMA leverage caps should be verified live rather than assumed.
