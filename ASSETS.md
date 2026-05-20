# NEBO UltraWash — Brand Assets Inventory

_Last updated: 2026-05-19. Source of truth for every brand asset used by the financing page (and future UltraWash mini-site)._

## Folder layout
```
financing-page/
├── index.html              # the form
├── assets/                 # all brand assets
│   ├── nebo-logo.png       # NEBO ULTRAWASH wordmark, transparent, trimmed
│   ├── nebo-financing-banner.jpg  # wide hero creative (2000×1000)
│   ├── nebo-financing-poster.jpg  # vertical social/poster creative
│   ├── badge-ceramic-coating.png  # approved service badge, transparent
│   ├── badge-ppf.png              # approved service badge, transparent
│   ├── badge-vinyl-wrap.png       # approved service badge, transparent
│   ├── badge-window-tinting.png   # approved service badge, transparent
│   └── whatsapp-thread.jpg # internal — NEBO group thread, NOT for deploy
├── research/               # CRO + pricing + consultation research + STRATEGY
└── ASSETS.md               # this file
```

## Assets

### Logo — `nebo-logo.png`
- Native: 239×114, transparent PNG, RGBA.
- Source: lifted from the UltraWash mobile app (`UltrawashApp/assets/screenshot-2026-01-06-232900-removebg-preview.png`), then trimmed to alpha bbox to remove ~18px of transparent margin so sizing reflects real content.
- Usage: hero (top-left of cobalt brand panel, height 64px / 56px mobile) and the cinematic loader (width clamp 220–320px).
- Color: white wordmark + cyan electric bolt; works on cobalt/dark backgrounds. Has its own glow built-in; we add a subtle drop-shadow.
- If a higher-res vector/PNG arrives, drop into this filename to upgrade crispness.

### Service badges — `badge-{ceramic-coating,ppf,vinyl-wrap,window-tinting}.png`
- Native: ~600×160 each, transparent PNG (background-removed via alpha masking).
- Source: cropped from the right column of `nebo-financing-banner.jpg` (the four NEBO-approved badge marks). Standalone horizontal strip was also sent; we'll re-cut from that cleaner source once available.
- Approved by NEBO (Noah confirmed direct from the team). Each badge is the canonical visual mark for its service — do not substitute with generic icons.
- Usage: step 1 of the financing form, one per service card. Set `object-fit:contain` so the landscape ratio sits cleanly inside the dimensional `.svc` card.

### Marketing creatives — `nebo-financing-banner.jpg`, `nebo-financing-poster.jpg`
- Banner: 2000×1000 wide format. "0% FINANCING" on left + four badge column on right. Source of badge crops. Also used as `og:image` for the page (social share preview).
- Poster: vertical format. NEBO logo + 0% FINANCING + gold pill ("Upgrade your ride. Pay over time.") + service row + magenta "APPLY IN-STORE" CTA + trust row (Fast Approval / Easy Payments / No Interest). Reference for layout and visual language; not embedded in the page directly.

### WhatsApp thread — `whatsapp-thread.jpg`
- Internal context only. Conversation between Mohammed Ghaddar / Ali Haidar / Hadi about the financing-page build. **Do not deploy publicly.** Kept here as project context.

## Brand system extracted from the creatives

| Token | Value | Used as |
|---|---|---|
| Primary cobalt | `#0d3fd6` | `--blue` (primary brand) |
| Deep navy | `#06208f` | `--blue-deep` (hero base) |
| Bright blue | `#1f63ff` | `--blue-bright` (CTAs, plan default) |
| Electric cyan | `#36ccff` | `--cyan` (accents, glow) |
| Gold | `#ffc21a` | `--gold` (the "UPGRADE YOUR RIDE" pill) |
| Magenta | `#ff2e6e` | `--magenta` ("APPLY IN-STORE" CTA, "Most Popular" badge) |
| Ink (dark text) | `#0a1530` | `--ink` |

| Type | Where |
|---|---|
| **Archivo Black Italic** (900 italic) | Display headlines, hero "0% FINANCING", section titles, badges |
| **Inter** (400–700) | Form fields, body copy, UI labels |
| **Newsreader Italic** | Editorial accents only (used on reference brief, not the form) |

## Notes on the deploy
Public deploy includes only `index.html` + the assets referenced by it (logo, the four badges, banner used as `og:image`). The poster and the whatsapp thread are kept locally for reference and never pushed to Vercel.
