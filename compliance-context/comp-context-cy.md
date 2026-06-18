# Compliance Context — T212 CY

**Entity:** Trading 212 Markets Ltd
**Maintained by:** Reg Product team
**Purpose:** Entity-specific regulatory context for the REG
Compliance Research tool. Holds what is true for CY only. The
cross-entity decision rules live in the tool's own instructions,
not here.

Language: British English. No em dashes.

---

## Regulatory identity

- **Regulator:** CySEC (Cyprus Securities and Exchange Commission)
- **Licence number:** 398/21
- **Entity type:** Cyprus Investment Firm (CIF), full scope
- **Framework:** MiFID II, as implemented in Cyprus, plus ESMA
  measures
- **Service model:** Execution-only. No investment advice, no
  discretionary management.
- **Role in the group:** EU hub. Passports into other EU and EEA
  states under Freedom of Services.

---

## Regulatory lens — what makes CY distinct

Read CY through a MiFID II and ESMA lens, not a UK FCA one.
Consumer Duty does not apply here; that is a UK concept. The
equivalent pressure points in CY are MiFID II conduct rules,
ESMA product intervention measures, and CySEC supervisory
expectations.

Two structural permissions set CY apart from the UK and DE
entities and matter for analysis:

- CY can deal on its own account, including running a B-book.
- CY can grant credit to clients.

These are genuine permissions, not assumptions. They widen what
is commercially possible in CY relative to the execution-only,
agency-only posture elsewhere. Where an analysis turns on whether
T212 can take the other side of a trade or extend credit, CY is
usually the entity where the answer is yes.

---

## Product permissions — high level

CY is the broadest product entity in the group. The following is
the high-level picture for compliance scoping. For the
authoritative live matrix, the user should confirm against the
current product catalogue, since availability changes.

**Allowed in CY:**
- Invest: stocks and ETFs, including fractional
- CFDs across the full range: shares, ETFs, indices, commodities,
  FX, and crypto
- Crypto spot. CY is the only T212 entity offering real crypto
  spot trading.
- Crypto on the Invest account (multi-currency wallet). CY only.
- Crypto ETNs
- Complex and leveraged and inverse ETPs
- Pies and AutoInvest, and Model Portfolios
- Share lending (opt-in only)
- Extended hours and 24/5 trading
- Multi-currency account
- Interest on cash via qualifying money market funds
- Spending Pot, and Spare Change and Cashback (Spare Change and
  Cashback is CY only)
- T212 Card
- Portfolio transfers
- CFD futures rollover

**Not available in CY:**
- ISA and SIPP. These are UK tax wrappers and do not exist in CY.

---

## Core mechanics to protect

The same non-negotiable mechanics apply in CY as group-wide.
Where an analysis touches these, protect the mechanic and find a
lower-friction path rather than breaking it:

- Pies and AutoInvest are execution-only with the client setting
  all parameters. No discretionary management framing.
- The multi-currency account does not permit outbound payments.
  Clients convert within T212 and use funds within investment
  flows only.
- Share lending is opt-in only, on explicit client choice.

---

## Entity-specific regulatory constraints

These are the CY-specific obligations most likely to bear on a
compliance analysis. Verify the precise current rule by browsing
before relying on any of them; this list is a pointer, not a
substitute for the primary source.

- **ESMA CFD measures:** leverage caps by asset class, and
  mandatory negative balance protection on CFD accounts. These
  are the binding constraints on the CFD offering.
- **Appropriateness for complex products:** MiFID II requires an
  appropriateness assessment for complex instruments. CFDs and
  complex ETPs fall here.
- **Article 25(4) execution-only exemption:** for non-complex
  instruments such as mainstream equities and ETFs, the
  appropriateness assessment can be waived where the client
  initiates and is clearly informed. This is the basis on which
  the Invest appropriateness test can be removed for non-complex
  products.
- **Freedom of Services restrictions by state:** when CY passports
  into other EU states, local overlays can apply. Known position
  to verify: CFDs are offered with restrictions in Spain and
  France, and are not offered in Belgium. Confirm the current
  per-state position before relying on it, as these change.

---

## Known open items to verify

Flagged honestly so the tool does not treat gaps as settled fact:

- The precise current ESMA leverage caps by asset class should be
  verified against the live ESMA or CySEC source at the time of
  analysis rather than assumed.
- The per-state Freedom of Services overlays change over time.
  Treat the Spain, France, and Belgium positions above as last
  known, not current, until verified.
- Any CySEC supervisory expectation or inspection-driven
  requirement specific to a given product should be checked
  against current CySEC publications, not inferred.
