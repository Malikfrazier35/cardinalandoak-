# Cardinal & Oak — Compliance Execution Plan

**Document ID:** EXECUTION-PLAN-v1
**Last updated:** April 21, 2026
**Owner:** Malik
**Supersedes:** Remediation roadmaps in AUDIT-002

This document converts the 11 remaining audit items into a concrete, sequenced plan — with real vendors, real links, real costs, and real dependencies. It is ordered so that completing tasks top-to-bottom unblocks the next task each time.

---

## § 0 — Structural decision (do this before anything else)

Financial Holding LLC already exists. That creates an option you should pick between before filing anything new.

### Option A: Form a separate Cardinal & Oak, LLC

- **Pro:** Full legal separation. If a Cardinal & Oak transaction ever draws litigation, Financial Holding and the other products (Vaultline, Castford, Ashford, etc.) are behind a different corporate veil.
- **Pro:** Matches the public-facing name exactly. "Cardinal & Oak, LLC" on every doc.
- **Con:** Separate EIN, separate bank account, separate tax filing, separate BOI, separate insurance policy. Real ongoing overhead.
- **Cost:** $120 filing + ~$100/yr annual report + insurance increment.

### Option B: File "Cardinal & Oak" as a DBA/Trade Name under Financial Holding LLC

- **Pro:** Lower overhead. One tax filing, one bank, one insurance umbrella.
- **Pro:** Faster — CT Trade Name Certificate filed at the municipal level (not state SOS), usually same-day.
- **Con:** **No liability separation.** A seller complaint or litigation against Cardinal & Oak pierces directly into Financial Holding and its other products. Given your product portfolio (Vaultline, Castford, Ashford all have their own seller/customer exposure), this concentrates risk.
- **Con:** Site footer and policy docs all say "Cardinal & Oak, LLC" — which would be factually wrong under a DBA. Those all need to change to "Cardinal & Oak, a trade name of Financial Holding LLC."

### Recommendation: **Option A — separate LLC.**

Real-estate transactions have outsized litigation exposure compared to SaaS. A seller dispute over a single $180K home sale can eat more in legal defense than the transaction itself made. Paying $120 + an extra insurance rider to keep that risk contained from your other four products is cheap insurance.

If you disagree, flag it and I'll rewrite the footer + policy docs to reflect DBA status.

**All tasks below assume Option A.**

---

## § 1 — Week 1: Entity formation & the things that depend on it

| Day | Task | Blocker for | URL | Cost | Time |
|---|---|---|---|---|---|
| D1 | Form Cardinal & Oak, LLC with CT SOS | Everything downstream | business.ct.gov/Account/Register | $120 | 30 min online, 1-3 biz days to process |
| D1 | Order LLC certified copy (optional but useful for bank) | Bank account smoother | Same portal | $55 | While filing |
| D1 | Apply for EIN with IRS | Bank acct, BOI, tax, insurance | irs.gov/businesses/small-businesses-self-employed/apply-for-an-employer-identification-number-ein-online | Free | 15 min, instant delivery |
| D2 | Draft & sign Operating Agreement | Bank acct may request | Template: [CT-specific free templates on LawDepot or Rocket Lawyer; have counsel review before relying on it] | Free template / $150 if attorney drafts | 1 hour |
| D2 | Open business bank account | Everything money-related | See § 1.1 | Usually $0 | 1-2 hours |
| D3 | File FinCEN BOI report | Federal compliance | boiefiling.fincen.gov | Free | 15 min |
| D3 | Register for CT DRS taxes (Form REG-1) | Tax compliance | portal.ct.gov/DRS/myconneCT | Free | 15 min |
| D4 | Secure real business address | Public-facing credibility | See § 1.2 | $15-$180/mo | 30 min |

### § 1.1 — Business bank account options

For a CT-based residential real-estate LLC, these are the pragmatic choices:

| Bank | Pros | Cons | Best for |
|---|---|---|---|
| **Webster Bank** (your employer — but maybe don't) | You know the products | Conflict-of-interest appearance; pending Santander acquisition | Probably skip |
| **Mercury** | 100% online, fast setup, no monthly fees, strong API | No cash deposits | If all deals are wire-in/wire-out |
| **Relay** | Free, multi-account (one per property), integrates QBO | Newer player | If you'll hold multiple properties |
| **Chase Business Complete** | Physical branches, brand gravitas | $15/mo fee unless $2K avg balance | If you want brick-and-mortar backup |
| **Bank of America Business Advantage** | Same as Chase, ubiquitous ATMs | $16/mo | Same use case |

**Recommendation:** **Mercury** for the initial phase. No monthly fee, same-day approval, instantly usable debit card, and their wire functionality is cleaner than any traditional bank I've worked with. Upgrade to a physical bank later if you ever need cash handling.

Required at application:
- Filed CT Cert of Organization
- EIN confirmation letter
- Your driver's license
- Cardinal & Oak business address

### § 1.2 — Real business address options

"Hartford, Connecticut" generically on your footer isn't workable long-term. Three realistic paths:

| Option | Price | Real mailbox? | Package receipt? | Looks credible? |
|---|---|---|---|---|
| **UPS Store Mailbox Plus** | $25-$40/mo | Yes | Yes | Yes — gets you a real street address, not "PO Box" |
| **Regus Virtual Office** (CT locations: Hartford, Stamford, New Haven) | $49-$199/mo | Yes + meeting room access | Yes | Yes + can actually meet sellers there |
| **iPostal1 CT locations** | $15-$25/mo | Yes, scans mail to you | Yes | Acceptable but check if LLC-compatible |

**Recommendation:** **UPS Store Mailbox Plus** at a Hartford-area location. $39/mo, real street address, accepts USPS and private couriers. File it as your CT LLC's registered business address. Use that address in the site footer, Privacy Policy, and all ad placements.

Find nearest store: theupsstore.com/mailboxes

---

## § 2 — Week 2: Insurance, legal, and real-world infrastructure

| Day | Task | Blocker for | Cost | Time |
|---|---|---|---|---|
| D8 | Contact 3 CT-based commercial insurance brokers for quotes | First offer | $0 to quote | 2 hrs |
| D8 | Identify 2-3 CT real-estate attorneys (for future closings) | First closing | $0 to call | 1 hr |
| D9-10 | Review insurance quotes, bind GL + Cyber (+ E&O if affordable) | First offer | See § 2.1 | Malik + broker |
| D10 | Obtain proof-of-funds letter from Mercury/bank | First offer | Free | 15 min |
| D11 | Enable MFA on Vercel, GitHub, Google Workspace | Ongoing hygiene | Free | 5 min total |
| D11 | Create ad archive folder on Google Drive | First ad | Free | 2 min |
| D12 | Do a final site & policy-page claim-accuracy scrub | First ad | Free | 30 min |

### § 2.1 — Insurance reality check

For a new home-buying LLC doing 0 transactions yet, the underwriting market is tight. Expect:

| Coverage | Typical annual premium (CT, new entity, <$1M revenue projection) | Why |
|---|---|---|
| Commercial General Liability ($1M/$2M) | $550-$1,200 | Baseline; every real-estate investor needs this |
| Cyber Liability ($500K-$1M) | $400-$900 | Form collects PII from sellers |
| Professional Liability / E&O ($500K-$1M) | $800-$1,800 | Some carriers won't write for new LLCs; defer if needed |
| Property insurance (per held property) | Varies, $1K-$3K/yr per property | Not needed until first acquisition |

**Recommended brokers (national, CT-licensed, real-estate friendly):**

- **Obie** (obieinsurance.com) — Specializes in real-estate investors. Online quote + instant bind for GL. Cyber is a separate product but they'll bundle.
- **NREIG** (National Real Estate Insurance Group) — Focused on non-owner-occupied investors. More expensive than Obie but better for when you own properties.
- **Travelers Select** through a local CT independent agent — More expensive but bigger carrier.

**Minimum-viable insurance stack before first ad:**
1. Commercial General Liability $1M/$2M — ~$65/mo
2. Cyber Liability $500K — ~$45/mo

Total: ~$110/mo. E&O and property insurance can wait until first offer is extended / first property acquired.

### § 2.2 — CT real-estate attorney identification

You don't need to *retain* an attorney yet. You need to know *who you'll call* when the first offer turns into a real contract. Target: 2-3 CT attorneys who handle residential closings for investors.

**How to find them:**
- CT Bar Association referral service: ctbar.org/for-the-public/find-a-lawyer
- BiggerPockets CT forum — filter by "Hartford attorney real estate" — local investors post recommendations regularly
- Review any CT real-estate wholesaler or flipper's LinkedIn — their recent posts usually mention the attorney they closed with

**What to ask on first call (15-min scoping call, usually free):**
1. Do you handle non-financed residential closings? *(Must be yes.)*
2. What's your flat fee for a standard cash purchase closing? (CT range: $750-$1,500)
3. Can you draft or review a CT-specific purchase agreement template we'd use for multiple deals?
4. Are you comfortable closing on properties bought as-is in distressed condition?
5. How quickly can you turn a clear-title closing once a signed PSA lands on your desk?

**Shortlist 2; retain 1.** Having a backup matters when the primary is unavailable and you need to close in 7 days.

### § 2.3 — Proof-of-funds letter

The site promises "proof of funds provided on request." You need to be able to produce one within 24 hours of a seller asking.

**Simplest path (Mercury or most banks):**
1. Sign into business banking
2. Go to **Account** → **Documents** / **Statements**
3. Look for "Proof of Funds" or "Account Verification Letter"
4. Request one — usually delivered to your email within 1 business day
5. Save a PDF template; you'll re-request (or re-use within 30 days) each time

**If you don't have enough capital in the business account to cover a purchase:**
- Partner with a hard-money lender or capital partner who can provide POF letters on demand (New Silver, Kiavi, LendingOne — all serve CT)
- Or be transparent in the offer letter: "Funded by [partner] — POF from them available on request"

**Never fabricate a POF.** That's securities fraud if the seller acts on it.

---

## § 3 — Pre-launch checklist

Before the first newspaper ad runs, every item below must be checked. If any are blank, pull the ad.

**Entity & legal**
- [ ] CT SOS Cert of Organization on file (status: active)
- [ ] EIN issued by IRS
- [ ] FinCEN BOI report filed
- [ ] Operating Agreement signed and filed internally
- [ ] CT DRS REG-1 filed

**Banking & money**
- [ ] Business bank account open and active
- [ ] At least one proof-of-funds source identified (bank, capital partner, or both)
- [ ] POF letter template obtained and filed

**Insurance**
- [ ] Commercial General Liability bound (certificate on file)
- [ ] Cyber Liability bound (certificate on file)

**Public-facing**
- [ ] Site footer shows real business address (not "Hartford, CT" generic)
- [ ] Privacy Policy updated with real address
- [ ] Site policy pages all resolve (no 404s)
- [ ] TCPA consent flow working end-to-end (test with form submission)
- [ ] Newspaper ad copy finalized with Equal Housing Opportunity line

**Operational**
- [ ] CT real-estate attorney identified + introductory call completed
- [ ] MFA enabled on Vercel, GitHub, Google Workspace
- [ ] Ad archive folder exists on Google Drive
- [ ] Phone `(475) 374-1073` rings to a real phone you answer during business hours

**Honesty scrub**
- [ ] No claims on the site that you can't substantiate in writing
- [ ] "Cardinal & Oak, LLC" on all docs only after LLC filing confirms active

---

## § 4 — Risk register

What each unaddressed item actually risks if you run ads without it:

| Unaddressed item | Risk severity | What specifically could happen |
|---|---|---|
| LLC not filed | **Critical** | Fraud claim: you're operating and collecting consent under a non-existent legal entity. Any contract signed is potentially voidable. |
| No POF letter available | **High** | Seller or their attorney asks for POF; you can't produce; they walk. Wasted lead + word spreads in small CT investor community. |
| No CT attorney identified | **High** | Your first time-sensitive deal comes in; no attorney available; you lose the deal or try to DIY the closing (illegal in CT). |
| No GL insurance | **High** | Single premises-liability claim from a property walk-through (slip and fall) could wipe you out personally. |
| No Cyber insurance | **Medium** | Formspree breach or seller PII leak — breach-notification costs alone run $10K-$50K. |
| No business address | **Medium** | Looks amateur on ads. A skeptical seller Googles you and finds no real office. Loses trust. |
| No FinCEN BOI | **Medium** | Federal civil penalty up to $500/day past the 30-day window. Also a compliance nightmare at first audit or bank KYC. |
| No ad archive | **Low** | Fine until a consumer-protection complaint. Then you can't produce the ad a complainant references. |
| No MFA | **Low** | Until account takeover happens. Then it's Critical. |
| Claim substantiation gaps | **Medium** | CUTPA or FTC challenge forces you to prove every claim. Stronger stance is to have the files ready. |

---

## § 5 — Budget summary

First 60 days of compliance setup:

| Category | One-time | Monthly | 90-day total |
|---|---|---|---|
| CT SOS LLC filing | $120 | — | $120 |
| Certified copy (optional) | $55 | — | $55 |
| EIN + BOI + DRS | Free | — | $0 |
| Operating Agreement (template) | Free | — | $0 |
| Business address (UPS Store) | — | $39 | $117 |
| Business bank (Mercury) | Free | Free | $0 |
| Commercial GL insurance | — | ~$65 | $195 |
| Cyber insurance | — | ~$45 | $135 |
| CT attorney intro calls | Free | — | $0 |
| First newspaper ad run (budget placeholder) | — | $600 | $600 |
| **Total** | **$175** | **~$149** | **~$1,222** |

Under $1,300 all-in to go from "we have a website" to "we are a fully-compliant-for-our-scale, real-world-bound-up, ad-ready CT home-buying firm."

---

## § 6 — What happens after Week 2

Once all of the above is done, compliance shifts from *setup* to *operations*. That's covered in the separate `OPERATIONAL-PLAYBOOK.md` document — the per-transaction compliance checklist for what runs at every lead, every offer, and every closing.

Don't start ads until § 3 (pre-launch checklist) is 100% checked. Every single ad dollar before that is buying liability, not leads.
