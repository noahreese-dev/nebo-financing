# NEBO UltraWash — Web Properties

Umbrella repo for all NEBO UltraWash customer-facing web pages. Owned by Hadi (build),
Ali Haidar (visual direction), Mohammed Ghaddar (client).

**Live:** https://nebo-financing-form.vercel.app

## Surfaces

| Path | Purpose | Status |
|------|---------|--------|
| `/` | 0% Financing application form | live |
| `/detailing` | Detailing appointment booking | scaffold — booking flow in progress |
| `/iterations.html` | Internal hero design comparison | internal |

## Repo tree

```
.
├── index.html              # /  → 0% financing form (multi-step, 20% deposit + monthly plan + payment)
├── detailing/
│   └── index.html          # /detailing → detailing appointment booking
├── iterations.html         # internal hero design comparison
├── assets/                 # shared brand assets
│   ├── nebo-logo.png
│   ├── badge-{ceramic-coating,ppf,vinyl-wrap,window-tinting}.png
│   ├── bg-bubbles.jpg
│   ├── nebo-financing-banner.jpg
│   ├── nebo-financing-poster.jpg
│   └── email-confirmation.html
├── research/               # CRO + pricing-psychology + consultation research + STRATEGY
├── ASSETS.md               # brand-asset inventory
├── SPEC.md                 # financing-page spec
└── README.md
```

## Flow (financing form)

Per Mohammed (2026-05-20):

```
Pick service(s) → service total → 20% deposit shown → pick monthly plan (3/6/12)
                                                                ↓
   credit-card / PayPal (instant approval after 20% paid)
                                                                ↓
       confirmation screen + email with reference code
```

No human consultation step. Driver's license + extras captured in-person at drop-off.

## Tech

Plain HTML/CSS/JS, deployed static to Vercel. Production target: SiteGround
(static deploy via git push + PHP submit handler at go-live).

Brand artwork: NEBO logo + service badges sourced from UltraWash mobile app + NEBO
marketing creatives. Logo and badges refined via Gemini 2.5 Flash Image edit-mode.

## Open decisions (Mohammed)

- **Per-service real prices** for ceramic, tint, PPF, wraps — required for accurate
  20% deposit + monthly installment math
- Real promo deadline (if any)
- Whether the 20% deposit is fully refundable / under what conditions
