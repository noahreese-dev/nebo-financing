# NEBO UltraWash — 0% Financing Paper Form Spec

Plain-text source of truth for the physical paper form. Mirrors the digital flow.
Updated 2026-05-20.

## Logic check (what each thing IS)

There are three kinds of "content" on the form. Don't confuse them:

| Kind | Who fills it | Example |
|---|---|---|
| **User input** | The customer, with a pen | Name, address, vehicle Year/Make/Model |
| **Customer choice** | The customer, by ticking a box | Service selection, plan length |
| **Printed info** | NEBO (printed at press time) | Service price estimates, terms paragraph, instructions |
| **Staff fill** | NEBO specialist at drop-off | Deposit amount, monthly $, reference code, total |

**No "estimated total: $___" blank line.** That confused round 1 — it looked like the
customer should compute their own total. Pricing belongs in the **printed** column.
Totals get computed by the specialist; the customer just picks services + plan.

## Layout (top to bottom, single page, letter portrait)

### Brand header (printed)
- NEBO ULTRAWASH logo (cobalt + cyan + white, top-left)
- Title: **"0% FINANCING APPLICATION"**
- Tagline: "Get approved instantly. Pay 20% deposit. 0% interest on the rest."
- Helper line: "Takes about 3 minutes. Have your driver's license and insurance handy."

### 1 — Customer Information
*Subtitle (printed, italic):* "Tell us how to reach you. We'll text and email a confirmation."

User-input fields (blank lines):
- Full Name
- Date of Birth (D D / M M / Y Y Y Y)
- Address
- City + Postal
- Phone
- Email

### 2 — Vehicle Information
*Subtitle:* "So we can confirm pricing accurately at drop-off."

User-input fields (blank):
- Year + Make + Model
- VIN
- Colour + Plate

### 3 — Services Requested
*Subtitle:* "Check what you'd like financed. You can combine multiple."

Printed visual checkbox grid (2×2), each cell has ☐ + service name + brief
description + "from $X" estimate. **Estimates are printed information, not user
calculations.**

```
☐ CERAMIC COATING                  ☐ PPF
  Long-term paint protection         Self-healing paint protection film
  & gloss                            from $1,800
  from $1,200

☐ VINYL WRAP                        ☐ WINDOW TINTING
  Full or partial colour change      Heat & UV rejection
  from $1,200                        from $350
```

### 4 — Payment Plan
*Subtitle:* "Pick the plan that fits. 0% interest on all options. 20% deposit due today."

Customer choice (radio-style checkboxes — pick one):
- ☐ 3 months — Higher monthly
- ☐ 6 months — Balanced
- ☐ 12 months — **⭐ Most Popular** — Lowest monthly

Printed footer line: "Your deposit and monthly amount are calculated by your specialist."

### 5 — Terms & Acknowledgement (printed paragraph)

Small print, printed information the customer reads and acknowledges by signing:

> By signing below I confirm: I'm 18 or older and reside in Canada. I've read and agree to NEBO UltraWash's Terms & Privacy Policy. NEBO may contact me about this application by phone, text or email. 20% deposit secures my appointment and approves my 0% financing plan instantly. The remaining balance is split into equal monthly payments. No interest when paid on the agreed schedule. Final pricing confirmed at drop-off.

### 6 — Signature
*Subtitle:* "Sign here to lock in your 0% financing."

User-input:
- Signature (single long line)
- Date (D D / M M / Y Y Y Y)

### Footer (printed)
- Small NEBO logo
- "FORM-FIN-001 · Hand to your specialist when complete"

### Staff-fill section (printed but blank, small, bottom corner — staff use)
- Reference code: NEBO-_______
- Total: $______
- Deposit (20%): $______
- Monthly ($): ______
- Specialist initials: ____

## Visual rules

- Pure white paper, black ink for primary text, cobalt-blue for section
  numerals/accents/highlight pill on "Most Popular"
- Numbered section circles in cobalt-blue (1, 2, 3, 4, 5, 6)
- 2×2 visual checkbox grid for services (per Variant C, the locked direction)
- Helper-text under field labels in small italic gray
- Single page, portrait, letter-size
- Photographed FLAT top-down, paper fills the frame, no surrounding environment
