# Compliance Context — T212 AU

**Entity:** Trading 212 AU Pty Ltd
**Maintained by:** Reg Product team
**Purpose:** Entity-specific regulatory context for the REG
Compliance Research tool. Holds what is true for AU only. The
cross-entity decision rules live in the tool's own instructions.

Language: British English. No em dashes.

---

## Regulatory identity

- **Regulator:** ASIC (Australian Securities and Investments
  Commission)
- **AFSL:** 541122
- **Entity type:** AFSL licensee, and CFD issuer
- **Service model:** Execution-only.
- **Framework:** Corporations Act, ASIC regulatory guides, Design
  and Distribution Obligations.

---

## Regulatory lens — what makes AU distinct

Read AU through an ASIC lens, with the Design and Distribution
Obligations (DDO) as the defining feature. DDO requires a target
market determination for products and an obligation to distribute
within that target market. Where an AU analysis touches a product
offering, DDO is almost always in scope.

AU is a CFD issuer, so the ASIC CFD product intervention order,
covering leverage limits and negative balance protection for
retail CFD clients, is the other central constraint.

AU is the newest and least-built-out entity for several products,
so expect more UNKNOWN permissions than UK, CY, or DE.

---

## Product permissions — high level

For compliance scoping. Confirm against the current product
catalogue for the authoritative live position.

**Allowed in AU:**
- Invest: stocks and ETFs, including fractional
- CFDs across shares, ETFs, indices, commodities, FX
- Crypto ETNs
- Pies and AutoInvest, and Model Portfolios
- Extended hours and 24/5 trading
- Spending Pot

**Not available in AU:**
- Crypto spot. Not offered.
- ISA and SIPP. UK only.
- US Treasuries. Not offered.
- Multi-currency account. Not available.
- Share lending. Not available in AU.
- T212 Card. Not available.
- Interest on cash. Not offered.

**Complex and leveraged ETPs:** treat as not available pending
confirmation. Verify before relying.

---

## Core mechanics to protect

- Pies and AutoInvest are execution-only with the client setting
  all parameters.

Note: multi-currency and share lending are not offered in AU, so
those mechanics do not arise here.

---

## Entity-specific regulatory constraints

Verify the precise current rule by browsing before relying on
any of these.

- **Design and Distribution Obligations (DDO):** target market
  determinations and distribution within target market. Central
  to any product offering in AU.
- **ASIC CFD product intervention order:** leverage limits and
  negative balance protection for retail CFD clients, plus
  restrictions on inducements. The binding CFD constraint.
- **AFSL conditions:** the licence carries specific conditions.
  Where an analysis touches the scope of what AU is authorised to
  do, check the current AFSL authorisations rather than assuming.

---

## Known open items to verify

- AU product availability is less settled than the other
  entities. Several permissions above are stated as not available
  based on the last known position; verify the current catalogue
  before relying, especially for complex ETPs.
- The current ASIC CFD product intervention order terms should be
  verified against current ASIC publications.
