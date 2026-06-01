# Wolfgang Rush — Indian Rent Control Drafting

**MCPB Desktop Extension** for Indian advocates using Claude Desktop App. Local-execution. Zero data collection.

> *Also available as a Claude Code Plugin:* *[github.com/Wolfgangrush/indian-rent-control-drafting](https://github.com/Wolfgangrush/indian-rent-control-drafting)*

## What this connector does

Eviction (non-payment / bona-fide / nuisance / sub-letting), standard-rent fixation, rent-deposit, Section 106 TPA notice, landlord recovery, tenant WS, revision/appeal, Model Tenancy Act 2021. 8 State exemplars across MRC / DRC / TN / KA / WB / UP / GJ / AP/TG.

## Case types

- `eviction-non-payment-of-rent` — Eviction on non-payment of rent under State Rent Control Act
- `eviction-bona-fide-personal-need` — Eviction on bona-fide personal need (Ragavendra Kumar / Akhileshwar Kumar framework)
- `eviction-nuisance-damage` — Eviction on nuisance / damage to premises
- `eviction-sub-letting-without-consent` — Eviction on sub-letting without consent (Resham Singh framework)
- `standard-rent-fixation-application` — Standard-rent / fair-rent fixation application
- `rent-deposit-application` — Rent deposit application (where landlord refuses receipt)
- `tenancy-termination-notice` — Section 106 TPA / Section 106 read with V. Dhanapal Chettiar termination notice
- `landlord-recovery-suit` — Landlord recovery suit for arrears
- `tenant-written-statement` — Tenant Written Statement to eviction petition
- `revision-appeal-rent-controller` — Revision / appeal from Rent Controller order
- `model-tenancy-act-2021-framework` — Model Tenancy Act 2021 framework pleading

## Install

1. Claude Desktop App → **Settings → Extensions → Install Extension**
2. Select `wolfgang-indian-rent-control-drafting.mcpb`
3. Enable

## System requirements

Claude Desktop App ≥ 0.10.0 · Python ≥ 3.10 · `pandoc` for .docx · `pdftotext` for PDF case-files (optional)

## Privacy

Zero data collection. Three-layer privacy firewall. Canonical policy: **<https://wolfgangrush.github.io/privacy/>**


## ⚠️ AI verification disclaimer · 🔒 Pseudonymisation procedure

> **⚠️ AI can make mistakes — please verify the information before filing.**
> Every draft produced by this connector is a STARTING POINT. The Verifier
> agent runs an anti-hallucination firewall and the Overseer agent runs an
> opposing-counsel review, but neither replaces an advocate's independent
> verification of statutory references, citation accuracy, factual fidelity,
> and Registry-formatting compliance with the user's High Court / forum.
> The advocate filing the pleading remains responsible for the contents.
>
> **🔒 Protected by pseudonymisation procedure.** The Reader agent applies a
> domain-specific privacy firewall as the first step of the pipeline — party
> names, addresses, identifying numbers (FIR / CR / Crime / Suit / Diary /
> SLP / lower-court case numbers), PAN / Aadhaar references, financial
> figures, witness names, and statutory-notice references are substituted
> with structural placeholders BEFORE any downstream agent sees the facts.
> The Drafter, Verifier, Refiner, and Overseer agents process placeholders
> only. Real values are re-substituted at the final docx render step on the
> user's local machine. No real identifying data leaves the case folder.

## License

MIT.

## Publisher

**Rushikesh R. Mahajan**, Advocate, Bombay HC Nagpur, publishing as **Wolfgang Rush**. advrushikeshravindramahajan@gmail.com

## Source

<https://github.com/Wolfgangrush/indian-rent-control-drafting-mcpb>

## Sample cases

See `SAMPLE-CASES/`.
