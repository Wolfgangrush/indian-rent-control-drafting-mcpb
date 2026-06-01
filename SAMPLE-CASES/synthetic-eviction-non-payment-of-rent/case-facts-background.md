# Case Facts Background — Eviction Petition · Non-Payment of Rent

All party names, addresses, rent figures, dates of payment defaults, and case numbers are fictional placeholders. No real client / no real premises.

## Parties

- **Petitioner / Landlord:** [Landlord-A], aged about [Age-Placeholder] years, resident of [Landlord-Address-Placeholder], absolute owner of the demised premises.
- **Respondent / Tenant:** [Tenant-A], aged about [Tenant-Age-Placeholder] years, in occupation of the demised premises since 01 July 2018 under a registered tenancy agreement (see `02-tenancy-agreement-2018-07-01.docx`).

## Demised premises

- Description: [Premises-Description-Placeholder]
- Address: [Premises-Address-Placeholder-Full]
- Area: [Area-Placeholder] sq. ft.
- Municipal House No.: [House-No-Placeholder]
- Use: Residential

## Tenancy terms

- Monthly rent: Rs. [Monthly-Rent-Placeholder]/-
- Payable on or before 7th of every succeeding month.
- Tenancy created on 01 July 2018 under written agreement.

## Default chronology

- **April 2025** — tenant ceases payment of rent. (See ledger at `03-rent-default-ledger-2025-04-to-2025-12.docx`.)
- **12 July 2025** — landlord issues first written reminder.
- **18 September 2025** — landlord issues second written reminder.
- **02 November 2025** — landlord issues third written reminder.
- **31 December 2025** — total arrears stand at Rs. [Total-Arrears-Placeholder]/- (9 months × monthly rent).
- **05 January 2026** — § 106 TPA termination notice issued through counsel (`01-section-106-tpa-termination-notice-2026-01-05.docx`).
- **20 January 2026** — 15-day notice period expires; tenant fails to vacate and fails to clear arrears.
- **As on filing** — landlord approaches the appropriate forum (Rent Controller / Court of Small Causes / Civil Judge as Rent Controller, depending on State) for eviction.

## Forum and case type

- **Forum:** Forum-substituted per State Rent Control Act — Rent Controller (Delhi DRC Act) / Court of Small Causes (Maharashtra MRC Act) / Civil Judge as Rent Controller (UP Act) / Prescribed Authority (UP Act) — selected by `case-config.md` at runtime.
- **Case type:** `eviction-non-payment-of-rent`.
- **Statutory anchor:** State Rent Control Act non-payment-of-rent ground (operates by displacement of Section 106 TPA per V. Dhanapal Chettiar (1979) 4 SCC 214 in States where the SRCA has its own statutory-notice regime; § 106 TPA notice is included here as a defensive belt-and-braces measure).
- **Pecuniary jurisdiction:** to be determined per State Act + premises value.

## Reliefs sought

1. Eviction of the tenant from the demised premises.
2. Recovery of arrears of rent (Rs. [Total-Arrears-Placeholder]/- + post-notice arrears till date of decree).
3. Mesne profits from the date of termination of tenancy until delivery of vacant possession.
4. Interest under the Interest Act, 1978.
5. Costs of the proceedings.

## Ingredient check (Verifier-stage)

- ✅ Tenancy proved — written tenancy agreement on record.
- ✅ Rent quantum proved — clause 2 of tenancy agreement.
- ✅ Default proved — ledger + reminder letters + § 106 TPA notice.
- ✅ Statutory notice served — § 106 TPA notice + 15-day period expired.
- ✅ Cause of action — default + non-cure + expiry of notice.
- Limitation — within 3 years from date of accrual (Article 67, Limitation Act 1963).

## How to use this fixture

1. Point `read_case_folder(path)` at this directory.
2. Reader extracts facts from the 3 `.docx` files plus this `case-facts-background.md`.
3. Call `get_case_type_format("eviction-non-payment-of-rent")`.
4. The remaining 5 agents (Format → Drafter → Verifier → Refiner → Overseer) run end-to-end to produce `final-draft.docx` containing the eviction petition + Memo of Parties + List of Documents + Verification + Counsel block.
