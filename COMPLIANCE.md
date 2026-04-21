# Cardinal & Oak — Compliance & Audit Readiness Checklist

**Maintained:** Malik Frazier · Owner/Operator
**Last reviewed:** April 21, 2026
**Status legend:** `[ ]` not started · `[~]` in progress · `[x]` complete · `[N/A]` not applicable

---

## Priority framework

**P0 — Must be complete before first ad runs or first lead is captured.**
**P1 — Must be complete before first purchase offer is extended.**
**P2 — Must be complete before first closing.**
**P3 — Ongoing or post-launch.**

---

## § 1. Entity & Governance (P0)

| # | Control | Status | Evidence location | Owner | Notes |
|---|---|---|---|---|---|
| 1.01 | Cardinal & Oak, LLC filed with CT Secretary of State | `[ ]` | `/compliance/entity/cert-of-org.pdf` | Malik | Required before any ad |
| 1.02 | Annual report current with CT SOS | `[ ]` | `/compliance/entity/annual-report.pdf` | Malik | |
| 1.03 | EIN issued by IRS | `[ ]` | `/compliance/entity/ein.pdf` | Malik | |
| 1.04 | Operating Agreement drafted and executed | `[ ]` | `/compliance/entity/operating-agreement.pdf` | Malik + atty | |
| 1.05 | Registered agent designated and on file | `[ ]` | — | Malik | |
| 1.06 | Dedicated business bank account opened | `[ ]` | — | Malik | No commingling with personal or Financial Holding |
| 1.07 | CT DRS tax registration (Form REG-1) | `[ ]` | `/compliance/entity/ct-reg1.pdf` | Malik | |
| 1.08 | Beneficial Ownership Information (BOI) filed with FinCEN for the LLC | `[ ]` | `/compliance/entity/boi-filing.pdf` | Malik | Required under Corporate Transparency Act — separate from any property-level reporting |
| 1.09 | Business address established (PO box, UPS store, or physical) | `[ ]` | — | Malik | Must match Privacy Policy and footer |

---

## § 2. Marketing, Advertising & Consumer Protection (P0)

| # | Control | Status | Evidence | Notes |
|---|---|---|---|---|
| 2.01 | Substantiation file: every claim on site has a verifiable source | `[ ]` | `/compliance/marketing/substantiation/` | One folder per claim |
| 2.02 | Ad archive — every version of every ad, every placement, every date | `[ ]` | `/compliance/marketing/ad-archive/` | Retain 3+ years |
| 2.03 | Equal Housing Opportunity statement on all print ads | `[x]` | `newspaper-ad-copy.md` | Present on all ad variants |
| 2.04 | Equal Housing Opportunity statement on website | `[x]` | `index.html` footer | |
| 2.05 | Fair Housing policy page live at `/fair-housing` | `[x]` | `fair-housing.html` | |
| 2.06 | TCPA consent checkbox on intake form (not pre-checked) | `[x]` | `index.html` form | |
| 2.07 | TCPA consent timestamp captured in DB on submit | `[ ]` | Supabase schema | Add `tcpa_consent_at timestamptz not null` |
| 2.08 | SMS opt-out ("STOP") honored automatically | `[ ]` | Twilio config | |
| 2.09 | Do-Not-Call Registry scrub procedure (if ever calling cold leads) | `[ ]` | `/compliance/marketing/dnc-procedure.md` | |
| 2.10 | No cold texting without prior express written consent | `[ ]` | Policy doc | TCPA: $500–$1,500 per text statutory |
| 2.11 | Call recording disclosure ("This call may be recorded") if recording | `[ ]` | Phone system config | CT is a two-party consent state |
| 2.12 | Landing-page claim review cadence — quarterly | `[ ]` | Calendar recurring event | |

---

## § 3. Privacy & Data Protection (P0)

| # | Control | Status | Evidence | Notes |
|---|---|---|---|---|
| 3.01 | Privacy Policy published at `/privacy` | `[x]` | `privacy.html` | Review by counsel still needed |
| 3.02 | Terms of Use published at `/terms` | `[x]` | `terms.html` | Review by counsel still needed |
| 3.03 | Privacy Policy linked from footer of every page | `[x]` | — | |
| 3.04 | Privacy Policy linked from intake form consent text | `[x]` | — | |
| 3.05 | Data retention policy written | `[ ]` | `/compliance/privacy/retention-policy.md` | 3yr leads, 7yr transactions |
| 3.06 | Data breach response playbook documented | `[ ]` | `/compliance/privacy/breach-response.md` | CT: notification without unreasonable delay |
| 3.07 | Encryption at rest enabled (Supabase default) | `[ ]` | Supabase config screenshot | |
| 3.08 | Encryption in transit (HTTPS everywhere, auto-SSL via Vercel) | `[x]` | — | Vercel handles |
| 3.09 | RLS policies on all Supabase tables | `[ ]` | SQL migration | `anon` insert-only, `service_role` full |
| 3.10 | MFA enabled on Supabase admin account | `[ ]` | — | |
| 3.11 | MFA enabled on Vercel team | `[ ]` | — | |
| 3.12 | MFA enabled on GitHub org | `[ ]` | — | |
| 3.13 | MFA enabled on Gmail/Google Workspace | `[ ]` | — | |
| 3.14 | Vendor list maintained | `[ ]` | `/compliance/privacy/vendors.md` | Supabase, Vercel, SendGrid/Resend, Twilio |
| 3.15 | DPAs signed with each vendor handling PII | `[ ]` | `/compliance/privacy/dpas/` | |
| 3.16 | Access logs on Supabase enabled | `[ ]` | — | |
| 3.17 | Off-site backup of critical records | `[ ]` | — | Supabase backups + independent dump monthly |
| 3.18 | Data subject access / deletion request procedure | `[ ]` | `/compliance/privacy/dsar-procedure.md` | |

---

## § 4. CT Foreclosure-Rescue & Distressed-Seller Protections (P0 — if keeping "Behind on payments" on site)

| # | Control | Status | Evidence | Notes |
|---|---|---|---|---|
| 4.01 | CT real-estate attorney engaged for compliance review | `[ ]` | Engagement letter | **Do not skip** |
| 4.02 | Attorney-drafted purchase agreement template with all CT-required disclosures | `[ ]` | `/compliance/legal/purchase-agreement-template.pdf` | |
| 4.03 | Separate addendum / process for sellers in default or facing foreclosure | `[ ]` | `/compliance/legal/foreclosure-addendum.pdf` | CT has specific equity-purchaser rules |
| 4.04 | Cooling-off period honored where required | `[ ]` | Procedure doc | |
| 4.05 | Mandatory disclosures (non-waivable rights, right to cancel) included | `[ ]` | Template | |
| 4.06 | Written protocol: distressed-seller intake requires attorney review before offer sent | `[ ]` | Procedure doc | |
| 4.07 | Attorney review checkpoint documented on every distressed-seller file | `[ ]` | Per-transaction file | |
| 4.08 | If not keeping this situation: "Behind on payments" removed from site | `[ ]` | `index.html` | Alternative to 4.01–4.07 |

---

## § 5. Transaction Integrity & Anti–Money Laundering (P1)

| # | Control | Status | Evidence | Notes |
|---|---|---|---|---|
| 5.01 | Written AML policy (2–3 pages minimum) | `[ ]` | `/compliance/aml/aml-policy.md` | |
| 5.02 | OFAC SDN screening of every seller before closing | `[ ]` | Screening log per transaction | `sanctionssearch.ofac.treas.gov` |
| 5.03 | OFAC screening log retained per seller (5+ years) | `[ ]` | `/compliance/aml/ofac-log/` | |
| 5.04 | Red flags list documented (unusual payment instructions, rushed closings, suspicious behavior) | `[ ]` | `/compliance/aml/red-flags.md` | |
| 5.05 | SAR (Suspicious Activity Report) filing procedure if red flags hit | `[ ]` | Procedure doc | Voluntary but recommended |
| 5.06 | Source-of-funds documentation for each acquisition | `[ ]` | Per-transaction file | Where your money came from |
| 5.07 | Proof-of-funds available within 24hr of seller request | `[ ]` | Bank letter template | |
| 5.08 | Wire instruction verification procedure (callback to known number) | `[ ]` | Procedure doc | Coordinate with closing attorney |
| 5.09 | Wire fraud warning to sellers included in pre-closing communication | `[ ]` | Email template | |
| 5.10 | FinCEN RRE Rule monitoring (re-activation watch) | `[ ]` | Quarterly review item | Vacated Mar 19 2026; may be appealed |
| 5.11 | Beneficial ownership records kept internally regardless of RRE Rule status | `[ ]` | Per-transaction file | 5-year retention |

---

## § 6. Fair Housing (P1)

| # | Control | Status | Evidence | Notes |
|---|---|---|---|---|
| 6.01 | Non-discrimination policy written | `[x]` | `fair-housing.html` | Public-facing version done |
| 6.02 | Internal fair-housing training doc for anyone who takes calls | `[ ]` | `/compliance/fair-housing/training.md` | |
| 6.03 | Lead intake log shows consistent treatment regardless of protected class | `[ ]` | Supabase query + quarterly review | |
| 6.04 | No "targeting" ad creative implying discriminatory preference | `[ ]` | Quarterly review | |
| 6.05 | Equal Housing Opportunity statement on all print ads | `[x]` | `newspaper-ad-copy.md` | |
| 6.06 | Accessibility: site WCAG AA compliant | `[~]` | — | Run axe audit before ads |
| 6.07 | Response procedure if fair-housing complaint received | `[ ]` | Procedure doc | |

---

## § 7. Records Retention (P1)

| # | Record type | Retention | Location | Status |
|---|---|---|---|---|
| 7.01 | Lead intake records | 3 years minimum | Supabase + monthly export to S3/Drive | `[ ]` |
| 7.02 | TCPA consent records | 4 years minimum | DB column + form log | `[ ]` |
| 7.03 | Offer letters sent | 7 years | `/compliance/transactions/offers/` | `[ ]` |
| 7.04 | Executed purchase agreements | Perpetual | `/compliance/transactions/contracts/` | `[ ]` |
| 7.05 | Closing statements (HUD-1 / CD / ALTA) | Perpetual | Per-transaction file | `[ ]` |
| 7.06 | Marketing creative and placement records | 3 years | `/compliance/marketing/ad-archive/` | `[ ]` |
| 7.07 | Tax records | 7 years | `/compliance/financial/tax/` | `[ ]` |
| 7.08 | Complaint log with response and resolution | 5+ years | `/compliance/complaints/` | `[ ]` |
| 7.09 | OFAC screening logs | 5 years | `/compliance/aml/ofac-log/` | `[ ]` |
| 7.10 | Email records (seller correspondence) | 7 years | Google Workspace retention policy | `[ ]` |

---

## § 8. Insurance (P1 — bind before first closing)

| # | Coverage | Amount (suggested) | Carrier | Bound? |
|---|---|---|---|---|
| 8.01 | Commercial General Liability | $1M / $2M | — | `[ ]` |
| 8.02 | Errors & Omissions (professional liability) | $500K – $1M | — | `[ ]` |
| 8.03 | Cyber liability | $500K – $1M | — | `[ ]` |
| 8.04 | Property insurance on each held property | Replacement cost | — | `[ ]` Per property |
| 8.05 | Lead paint liability rider (pre-1978 homes) | As available | — | `[ ]` Often excluded from standard GL |
| 8.06 | Auto (if using personal vehicle to visit properties) | Standard | — | `[ ]` Confirm personal policy covers business use |

---

## § 9. CT-Specific Real Estate Compliance (P1 / P2)

| # | Control | Status | Trigger | Notes |
|---|---|---|---|---|
| 9.01 | Municipal lien search procedure pre-acquisition | `[ ]` | Every purchase | |
| 9.02 | Title search through CT title company or attorney | `[ ]` | Every purchase | |
| 9.03 | Owner's title insurance policy obtained | `[ ]` | Every purchase | |
| 9.04 | CT Residential Property Condition Disclosure Report process (when reselling) | `[ ]` | Every resale | CGS § 20-327b |
| 9.05 | Lead-based paint disclosure + EPA pamphlet delivery (pre-1978 homes) | `[ ]` | Every pre-1978 transaction | Federal + CT |
| 9.06 | CT conveyance tax filing at closing | `[ ]` | Every sale | |
| 9.07 | Tenant notification procedure if purchasing occupied rental | `[ ]` | Rental acquisitions | CGS tenant protection statutes |

---

## § 10. Incident Response & Complaints (P2)

| # | Control | Status | Evidence | Notes |
|---|---|---|---|---|
| 10.01 | Data breach response playbook (first 72hr actions) | `[ ]` | `/compliance/privacy/breach-response.md` | |
| 10.02 | Regulator contact list maintained | `[ ]` | `/compliance/contacts.md` | CT DCP, CT AG, HUD, CHRO, FinCEN, title insurer |
| 10.03 | Legal hold procedure for threatened litigation | `[ ]` | Procedure doc | |
| 10.04 | Complaint intake procedure (email + phone) | `[ ]` | Procedure doc | |
| 10.05 | Complaint response SLA (5 business days) | `[ ]` | Procedure doc | |
| 10.06 | Complaint log (every complaint, response, resolution) | `[ ]` | `/compliance/complaints/log.md` | |

---

## § 11. Ongoing Review (P3)

| # | Review | Frequency | Owner |
|---|---|---|---|
| 11.01 | Site claims re-reviewed for accuracy | Quarterly | Malik |
| 11.02 | Ad archive reconciled with placements | Quarterly | Malik |
| 11.03 | CT SOS annual report filed | Annual | Malik |
| 11.04 | CT DRS filings current | Quarterly/Annual | Malik + accountant |
| 11.05 | Vendor DPA renewals | Annual | Malik |
| 11.06 | Policy pages reviewed by counsel | Annual | Counsel |
| 11.07 | Insurance policies reviewed / renewed | Annual | Malik + broker |
| 11.08 | FinCEN RRE Rule status check (ongoing appeal) | Quarterly | Malik |
| 11.09 | Complaint log review — patterns? | Quarterly | Malik |

---

## Open action items — ordered by blocker status

### Before the first ad runs (P0 blockers)
1. File Cardinal & Oak, LLC with CT SOS
2. Open business bank account
3. Get CT attorney engaged for a compliance review (§ 4.01)
4. **Decide: keep "Behind on payments" situation or remove it?** If keeping, items 4.01–4.07 are mandatory first.
5. Deploy site with Privacy, Terms, Fair Housing pages live
6. Add `tcpa_consent_at` column to `seller_leads` Supabase table
7. File CTA BOI report for the LLC with FinCEN (§ 1.08)

### Before the first offer is extended (P1 blockers)
8. Attorney-drafted purchase agreement template
9. OFAC screening workflow live
10. Proof-of-funds letter template and source ready
11. Insurance bound (at minimum GL + E&O + Cyber)

### Before the first closing (P2 blockers)
12. Title / closing attorney retained
13. Closing checklist with all CT-specific items
14. Wire verification procedure documented and rehearsed

---

## Disclaimer

This checklist is a starting framework. It is not legal advice and does not cover every regulatory or legal obligation Cardinal & Oak may have. Retain a Connecticut real-estate attorney familiar with non-financed residential acquisitions and consumer-protection law for a formal compliance review before conducting business.
