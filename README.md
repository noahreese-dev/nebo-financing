# NEBO UltraWash — 0% Financing Form

Production-grade 0% financing application form for NEBO UltraWash.

**Live:** https://nebo-financing-form.vercel.app

## What's here

- `index.html` — the financing form (3-step flow, brand assets, Stripe-ready submit endpoint, structured data for SEO/AEO)
- `iterations.html` — hero design iterations showcase (A/B/C/D)
- `assets/` — brand artwork (NEBO logo, service badges, banner, bubble bg, email template)
- `research/` — CRO + pricing psychology + consultation-conversion research, strategy doc
- `ASSETS.md` — brand-asset inventory

## Stack

Plain HTML/CSS/JS, deployed static to Vercel for prototype. Production target: SiteGround
(static deploy via git push + PHP submit handler at go-live).

Brand assets sourced from the UltraWash mobile app + NEBO marketing creatives. Service
badges and logo refined via Gemini 2.5 Flash Image (nano-banana) edit-mode.

## Open decisions (Mohammed)

- Per-service starting prices (unblocks monthly-payment reframe authenticity)
- BNPL partner vs in-house split-pay (gates Stripe wiring)
- Plan term lengths
- Real promo deadline (if any)
- Deposit at application: yes/no
