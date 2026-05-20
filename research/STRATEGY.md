# NEBO Financing Form — Conversion Strategy

_Synthesized from 3 research streams (01-form-conversion, 02-pricing-psychology, 03-consultation-conversion). 2026-05-19._

## The structural decision (Noah's two-flow question, resolved)

**One form, two entry points. This is the industry answer, not a compromise.**

Wisetack, Sunbit, Hearth, GreenSky, Synchrony, Affirm all use a single shareable financing link with multiple entry contexts. Building two forms doubles maintenance and splits conversion data. Tag the link with `?ref=ad` (customer self-serve from advertising) vs `?ref=rep` (salesperson sends post- or mid-consultation). The form is identical; the source label tells you who's converting and where to optimize.

**The single highest lever found in the research:** send the prequal link *before* the consultation. Wisetack internal data: customers who prequalify before meeting the rep convert **+26% close rate, +30% ticket size** — because the "I can't afford it" objection is dead before the rep speaks. So this form's *primary* role is not "the post-consultation paperwork" but "the lead-qualifying prequal that primes the consultation."

The flow we are actually building:

```
Ad / website → form (prequal in ~90s) → auto-SMS confirmation →
NEBO calls within 5 min → consultation (vehicle assessed, real quote) →
Rep texts SAME form link if not already done → plan confirmed → payment setup
```

The form is the spine. The rep-flow is the same form, often pre-filled by the customer, used to convert at the table.

## The conversion stack (ranked by evidence × leverage)

**Tier 1 — peer-reviewed / replicated, no-regret to ship:**

1. **Drop the budget field.** Highest single-field conversion penalty in CRO data. Service/package selection does the qualifying work with zero friction. _Status:_ ship.
2. **Split into 3 steps.** Multi-step beats single-page for high-commitment forms. KlientBoost: +1,900%; Venture Harbour: +743%; Reform consensus. Step 1 Service → Step 2 Vehicle + Plan → Step 3 Contact (defer name/phone/email to the very end — MECLABS phone-field studies show this is the single biggest field-position lever). _Status:_ ship.
3. **3 plan options, pre-select the middle "Most Popular."** Iyengar & Lepper (peer-reviewed): 24 options 3% conversion vs 6 options 30%. Thaler/Sunstein defaults: 49% → 86%. _Status:_ ship.
4. **Monthly-payment reframing.** Gourville 1998 (JCR, peer-reviewed): "$129/mo" beats "$1,548" on willingness-to-pay. Affirm/Klarna report 20–37% conversion lift, 30–87% AOV lift when monthly framing is dominant. Show "from $X/mo" on every service card. _Status:_ ship (needs Mohammed's real per-service price ranges).
5. **Precise prices.** Janiszewski & Uy 2008 (Psych Science): $153/mo more credible than $150/mo. Use precise monthly amounts. _Status:_ ship.
6. **Front-load the engaging question.** Foot-in-the-door (Freedman & Fraser): 20% → 76% follow-through with prior small commitment. Start with "What service?" (visual, fun, low-stakes) — not "First name." _Status:_ ship.
7. **CTA copy: "Get My Financing Options"** not "Submit." Veeam +166%, Aagaard +90% on first-person CTAs. _Status:_ ship.
8. **Trust microcopy at the friction point** (directly under the CTA, not in footer): "No credit check. No impact to your credit. Takes 60 seconds." Soft-pull framing is the exact script Wisetack/Sunbit/Affirm use. _Status:_ ship.
9. **"Takes 90 seconds" header** directly counters the #1 self-reported abandonment reason ("form looks too long"). _Status:_ ship.
10. **Speed-to-lead auto-confirmation.** HBR/MIT 2.24M leads: under-5-minute response = 21x qualification, 100x contact rate. The average business takes 29+ hours. Auto-confirm + flag NEBO for immediate phone follow-up. _Status:_ wire (Resend or SMS at go-live; needs SiteGround PHP handler / form service).

**Tier 2 — strong evidence, policy-dependent (Mohammed call):**

11. **Tiered packages (ESSENTIALS / PROTECTION / ELITE per service) with the "premium decoy."** Ariely's mechanism: the high-anchor tier exists to make the middle feel reasonable. Needs Mohammed's package definitions + real prices.
12. **Live social-proof counter** ("X cars protected this month" / Google review count). Auto/detailing-specific lift 15–30%. Needs a number — start with a conservative real count from NEBO's actuals.
13. **Real promo deadline** ("0% standard rates after [date]"). Tversky/Kahneman prospect theory + Experian 2x transaction rate on urgency. Only if a real promo end exists — never fabricate.
14. **Refundable $25 consultation deposit.** OpenTable/Tock data: cuts no-shows from 10–15% down to 1.7–5% (–57 to –70%). Filters tire-kickers but adds top-of-funnel friction. **Policy call:** my recommendation = no deposit at application for v1 (maximize lead volume; rep handles deal close). Revisit if no-show rate becomes a problem.

**Tier 3 — UX/polish (already partly done):**

- Step labels visible during the journey ("Service / Vehicle / Plan / You") — goal-gradient theory; zero-cost.
- Mobile-first inputs (tel/number types, 44px tap targets, one cluster per screen).
- Radio cards beat dropdowns on mobile (HubSpot).
- Phone field placement: last screen only.

## What we currently have vs the target state

| Current build | Target |
|---|---|
| Single-page form, 4 sections visible at once | 3-step flow with progress, one section per screen on mobile |
| Budget field optional | **Drop entirely** |
| 3 plan radios, no default, no labels | 3 plans, **12-mo pre-selected, "Most Popular" badge**, precise monthly amounts |
| Generic "Apply Now" CTA | **"Get My Financing Options"** |
| Service multi-select cards | Service tiles + (later) tiered packages per service with "from $X/mo" |
| No trust microcopy near CTA | "No credit check. No credit impact. 60 seconds." right under it |
| No header reassurance | "Takes about 90 seconds" prominently in form head |
| No source tagging | UTM/`?ref=ad`/`?ref=rep` capture on submit |
| Demo-mode submit | Auto-confirm email + SMS lead to NEBO at go-live (SiteGround PHP handler) |
| No social proof | Live "X cars protected this month" + Google review count |

## What we need from Mohammed (the unblocking asks)

1. **Per-service starting prices** so we can show honest "from $X/mo" ranges. (We can't do the monthly-payment reframe without this — it's the single biggest conversion lever.)
2. **Plan term lengths** confirmed: 3 / 6 / 12 months as we have, or different? Any longer (24-mo)?
3. **BNPL partner or in-house?** (Standing question — gates the payment-setup step.)
4. **Real promo deadline** for the 0% offer, if any.
5. **Deposit at application: yes/no?** (Recommend no for v1.)

## What we ship in the next implementation pass (no-regret, no Mohammed dependency)

A. Restructure to 3-step flow with progress (#2)
B. Drop budget field (#1)
C. Pre-select 12-mo plan + "Most Popular" badge (#3)
D. CTA → "Get My Financing Options" (#7)
E. Trust microcopy under CTA + "90 seconds" header (#8, #9)
F. Front-load service question (#6)
G. UTM/`?ref` capture in payload (#1 structural)

The monthly-payment displays, tiered packages, deadline, and social-proof counter wait on Mohammed's data.
