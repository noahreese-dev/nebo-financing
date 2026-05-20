# 0% Financing Page — SPEC (draft)

**Deadline:** June 1, 2026 (hard, set by Mohammed Ghaddar 2026-05-19)
**Status:** Awaiting reference forms + financing-mechanics clarification before build.

## What Mohammed asked for (verbatim intent)
- A page for the 0% Financing with **payment and monthly plan** customers can access **right away by June 1st**.
- A **0% Financing Form for customers to fill out online**.
- Use **furniture companies that offer monthly payment plans / "don't pay until 1 year" / 0% financing** as reference (The Brick, Leons, Tepperman).
- Visual template built with AI first (Ali Haidar + Hadi), then Hadi codes & launches.

## Open questions that block the build
1. **Transactional vs lead-capture?** Does the page charge a card on June 1, or collect an application UltraWash processes manually? Determines whether we need full payment plumbing by deadline.
2. **Who carries the financing?** A lender (3rd party financing partner) or UltraWash itself? Changes the form fields (credit info? just contact + service?) and legal copy.
3. **Payment stack:** reuse MYFC Stripe+Resend pattern, or new UltraWash merchant account? Stripe supports installments/subscriptions but needs its own account + onboarding lead time (could itself threaten June 1).

## Reference targets (for Ahmad/Khalife to source, Ali/Hadi to study)
- The Brick — financing application flow
- Leon's — "do not pay" / monthly plan flow
- Tepperman's — financing form fields + approval UX

What to extract from each: form fields collected, how the plan is presented (term lengths, $/mo), trust/legal copy, approval flow (instant vs reviewed), mobile layout.

## Recommended build path (pending answers)
- **Fastest safe June 1 deliverable:** a polished application/lead-capture page (form + plan presentation + email confirmation), NOT live card-charging — unless Stripe account already exists. De-risk plumbing before design.
- Reuse MYFC infrastructure where possible (Resend confirmation email, form → email pattern) to hit the date.
- Ali's AI visual template → Hadi codes → staging URL first → Mohammed approves → launch.

## Next actions
- [ ] Get Mohammed's answers to the 3 blocking questions
- [ ] Receive reference forms from Hajj Ahmad / Khalife
- [ ] Ali Haidar produces AI visual template
- [ ] Hadi builds on staging
- [ ] Mohammed approves → launch before June 1
