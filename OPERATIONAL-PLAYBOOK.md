# Cardinal & Oak — Operational Compliance Playbook

**Document ID:** OPERATIONAL-PLAYBOOK-v1
**Last updated:** April 21, 2026
**Purpose:** Once launch prep is done, compliance stops being something you *set up* and becomes something you *run* — on every lead, every offer, every closing. This is the checklist for each stage.

---

## The five stages of a Cardinal & Oak transaction

Every deal moves through the same five stages. Each stage has its own compliance triggers. The point of this playbook is that **no stage is skippable** and **every stage produces evidence** you keep in the transaction file.

```
STAGE 1        STAGE 2        STAGE 3        STAGE 4        STAGE 5
Lead In   →    Pre-Offer  →   Offer Out  →   Under PSA  →   Close
```

Each transaction gets a dedicated folder on Google Drive:

```
/transactions/2026/2026-05-[property-street-address]/
  01-intake/
  02-pre-offer/
  03-offer/
  04-contract/
  05-closing/
  99-correspondence/
```

All evidence for each stage lives in its numbered folder. At audit or litigation time, this folder is the entire record.

---

## STAGE 1 — Lead In

**Trigger:** Phone rings at (475) 374-1073, Formspree email arrives, or cold inquiry by other channel.

### What runs automatically

| Thing | Where it lives | Retention |
|---|---|---|
| Formspree submission (all form fields + TCPA consent) | `office@cardinalandoak.com` inbox | 4 years minimum |
| Submitter IP + timestamp | Formspree dashboard → Submissions | 4 years |
| Call log (who/when/duration) | Google Voice or phone carrier log | 3 years |

### What Malik does within 4 business hours

- [ ] Save the Formspree email to the transaction folder: `01-intake/lead.eml`
- [ ] Create the transaction folder using the property address
- [ ] Log the lead in the lead log (see `/compliance/leads/2026-leads.md`)
- [ ] Return the call or email — this is the 5-minute intake conversation
- [ ] Save call notes to `01-intake/notes.md`

### What Malik does **not** do at this stage

- ❌ Ask for Social Security number
- ❌ Ask for bank account information
- ❌ Ask for credit card / upfront payment
- ❌ Sign or email anything legally binding
- ❌ Say "we will pay you $X" verbally — all pricing is in writing only

### Red flags to note (but don't refuse the call yet)

- Caller pushes hard for an immediate price over the phone → note it, but say "offers always go out in writing within one business day"
- Caller asks Cardinal & Oak to pay off a lien / bail them out of something unusual → document carefully, may require attorney consult pre-offer
- Property is clearly out of CT → be upfront it's not a fit
- Caller mentions "my attorney is..." or "my trustee is..." → note; probate or fiduciary sales have extra procedure
- Caller mentions foreclosure, auction date, or notice of default → **stop the intake, do not proceed to offer.** This is the exact scenario we removed "Behind on payments" for. Thank them, politely decline, and note in the log. Reconsider only after CT counsel has drafted the foreclosure addendum.

---

## STAGE 2 — Pre-Offer

**Trigger:** Intake conversation ends, Malik intends to prepare an offer.

**Time budget:** Must complete within 1 business day of intake (so written offer lands in seller's inbox within 24 hours of first contact).

### Verification steps

| Step | Check | Source | Save to |
|---|---|---|---|
| 1 | Confirm CT property | Property address is in Connecticut | `02-pre-offer/address-verify.md` |
| 2 | Ownership check | Town/city property records (free via CT municipal GIS) | `02-pre-offer/ownership.png` |
| 3 | Tax & lien quick-look | Town assessor site + CT judicial lookup | `02-pre-offer/liens-check.md` |
| 4 | Recent comparables | Look up 3-5 comp sales on Zillow/Redfin or town records | `02-pre-offer/comps.md` |
| 5 | Condition estimate | From seller's description + Google Street View + any photos they sent | `02-pre-offer/condition.md` |
| 6 | OFAC SDN screen on seller name | sanctionssearch.ofac.treas.gov (free) | `02-pre-offer/ofac-check.pdf` |
| 7 | Offer math | Comps – rehab – margin = your offer | `02-pre-offer/offer-math.md` |

### OFAC screening — how to actually do it

It takes 30 seconds. Every offer. No exceptions.

1. Go to **sanctionssearch.ofac.treas.gov**
2. Enter seller's full legal name
3. Click Search
4. Screenshot the results page (even if zero hits — especially if zero hits)
5. Save as `02-pre-offer/ofac-[lastname].png` with date stamp

If there's any hit, **stop immediately** and call counsel. Do not proceed under any circumstance.

### Exit options at Stage 2

If pre-offer verification shows the deal doesn't work, the protocol is:
- Email the seller a short, respectful "we can't make an offer on this property" message
- Note the reason in the transaction folder
- Log the outcome in the lead log

---

## STAGE 3 — Offer Out

**Trigger:** Pre-offer verification complete; offer is ready to send.

### What goes in the offer letter (every time)

The offer letter is the single most legally-consequential document at this stage. Every one should contain:

1. **Header:** Cardinal & Oak, LLC legal name + real business address + phone + email
2. **Subject:** "Written Cash Offer — [Property Address] — [Date]"
3. **Opening:** "As a follow-up to our conversation on [date], below is our formal all-cash offer on the property referenced above."
4. **The offer:**
   - Offer price: $X
   - Earnest money: $Y (typical: $500-$1,000)
   - Closing date: on or before [date] (or "on your selected date, no more than [N] days from signature")
   - Condition: "as-is, in current condition, no seller-funded repairs"
   - Closing costs: "Cardinal & Oak to cover standard closing costs"
   - Financing: "All cash — no financing contingency"
5. **Expiration:** "This offer is valid for 10 calendar days from the date above."
6. **How to accept:** "Reply to this email confirming acceptance, or sign and return the attached purchase agreement. Nothing is binding until both parties have executed the attached agreement."
7. **Signed by:** Malik Frazier, Managing Member, Cardinal & Oak, LLC
8. **Attached:** Draft purchase agreement (attorney-drafted template with this specific property's details filled in)

### File the offer

- [ ] Save the sent offer as `03-offer/offer-letter.pdf`
- [ ] Save the attached PSA as `03-offer/psa-draft.pdf`
- [ ] Save the send timestamp (email header or screenshot)
- [ ] Log in lead log: status → `OFFER_SENT`

### What you do NOT do at this stage

- ❌ Text the offer — always email, always in writing
- ❌ Give verbal pricing outside of the written offer
- ❌ Call-campaign the seller if you don't hear back — **one polite follow-up at day 7, then silence until expiration**

### If seller accepts

Advance to Stage 4 (Under PSA).

### If seller asks for POF

Pull your current POF letter (≤ 30 days old) from `compliance/financial/pof-current.pdf` and email it. If the one on file is older than 30 days, request a fresh one from Mercury before sending.

---

## STAGE 4 — Under PSA (Purchase & Sale Agreement signed)

**Trigger:** Both parties have signed the PSA.

### Handoff to attorney

Within 1 business day of the fully-executed PSA:

- [ ] Email the executed PSA to your CT closing attorney
- [ ] CC `office@cardinalandoak.com` on everything
- [ ] Save fully-executed PSA to `04-contract/psa-executed.pdf`

### What the attorney handles (so you don't have to)

Your attorney now drives the checklist. Their job includes:
- Municipal lien search
- Title search & issuance of owner's title insurance
- CT conveyance tax calculation & filing
- Wire instruction verification (callback protocol to bank)
- Preparation of closing package (deed, transfer tax forms, closing disclosure)
- Lead-paint disclosure delivery if pre-1978 home
- CT Residential Property Condition Disclosure (seller's responsibility, attorney confirms it)

### What you handle

- [ ] Wire earnest money to attorney's escrow account within 48 hours of PSA execution (per PSA terms)
- [ ] Review anything the attorney sends for your signature before wiring any money
- [ ] Forward the wire-fraud warning email to the seller (see template in `compliance/aml/wire-warning-template.md`)
- [ ] If property inspection is happening, schedule with seller directly, attend if possible
- [ ] Finalize POF letter (fresh copy, dated within 30 days of closing) and send to attorney

### Red flag check at Stage 4

If *anything* about the PSA or closing doesn't match what was agreed in the offer:
- Stop the wire
- Call the attorney
- Do not sign under pressure
- If the seller is suddenly requesting changed wire instructions: **wire fraud attempt.** Full stop. Call seller at a known phone number to verify (never the phone number in the email).

---

## STAGE 5 — Close

**Trigger:** Closing day scheduled by attorney.

### At closing

The attorney runs this. Your role:
- [ ] Sign documents the attorney presents
- [ ] Confirm wire for purchase price has been initiated from your bank
- [ ] Confirm receipt of signed deed
- [ ] Confirm recording at town registry

### Post-closing (within 7 days)

- [ ] Save complete closing package to `05-closing/` (deed, CD, wire confirmations, title policy, attorney's closing statement)
- [ ] Save the recorded deed to `05-closing/deed-recorded.pdf` once it's back from the town
- [ ] Update the lead log: status → `CLOSED`
- [ ] File any CT- or federal-required post-closing reports (attorney advises)
- [ ] Update financial records (bank transactions tagged with property address)
- [ ] If this was the firm's first closing: update site to remove "as our transaction history builds" from FAQ language — now you have history

### Beneficial ownership record-keeping

If the FinCEN RRE Rule gets reinstated on appeal, reportable transactions will need beneficial-ownership details on the transferee (you). Even before that, maintain:
- [ ] Your own BOI on file with FinCEN (already done Week 1)
- [ ] Capital source documentation per-deal (`05-closing/source-of-funds.pdf`)

---

## Operational compliance — what happens every week, month, quarter

### Every week

- Check `office@cardinalandoak.com` for complaints, FOI requests, or regulator letters
- Review new Formspree submissions; move each to a transaction folder
- Update lead log

### Every month

- Reconcile ad archive — ensure every insertion from the month is saved with a dated PDF
- Run `bank statement ↔ transaction folder` reconciliation

### Every quarter

- Re-read every claim on the website. Can each still be substantiated?
- Re-read every ad placement from the quarter. Same check.
- Review the complaint log (even if it's empty, document "no complaints this quarter")
- Check FinCEN RRE Rule status (currently vacated; monitor for appeal)
- Confirm all insurance certificates still active and not lapsed
- MFA audit — still enabled on Vercel, GitHub, Google Workspace?

### Every year

- File CT SOS annual report (online, $80 current fee, due in the formation-month each year)
- Review policy pages with counsel (Privacy, Terms, Fair Housing)
- Refresh retention audit — delete leads over 3 years old that never converted
- Renew insurance policies (usually the broker reaches out 45 days before)

---

## What to do when something goes wrong

### A seller complains (email, phone, or social media)

1. Acknowledge in writing within 24 hours: "We received your concern. A member of our firm will respond substantively within 5 business days."
2. Create `/compliance/complaints/2026/YYYY-MM-DD-[lastname]/` folder
3. Save the original complaint + your acknowledgment
4. Determine what happened: pull the transaction folder
5. Respond substantively in writing; if needed, involve counsel
6. Save the full back-and-forth
7. Log in the complaint log

### A regulator calls or sends a letter

1. **Do not respond substantively without counsel.**
2. Acknowledge receipt only.
3. Call your CT real-estate attorney immediately.
4. Do not delete anything, anywhere, ever. Institute a legal hold.
5. Save all communications to `/compliance/regulator-correspondence/YYYY-MM-DD-[agency]/`

### A data incident (Formspree breach, leaked email, lost laptop with unencrypted files)

1. Call your cyber-insurance carrier first (they assign counsel and a breach coach)
2. Identify scope: what data, how many people
3. Under CT statute: notify affected individuals "without unreasonable delay"
4. Document everything: root cause, scope, timeline, notifications sent
5. Post-incident: update breach-response playbook with lessons learned

### A seller can't be reached post-offer and the contract is expiring

1. One polite follow-up email on day 7
2. Silence from day 8 onward
3. Offer expires at day 10; no further contact
4. Log in lead log: status → `OFFER_EXPIRED`
5. Do not re-engage unless seller reaches out first

---

## The one sentence to remember

**Every transaction produces a complete, contemporaneous paper trail — because the only defense against a complaint, an audit, or a lawsuit is the documentation you created before the complaint arrived.**

If it isn't in the transaction folder, it didn't happen.
