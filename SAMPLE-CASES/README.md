# Sample Cases — Reviewer Examples

Three anonymised fact patterns. All party names are placeholders.

## Example 1 — eviction-non-payment-of-rent

> *"Use the connector to draft a eviction non payment of rent (Eviction on non-payment of rent under State Rent Control Act). Use anonymised placeholders for party names and figures."*

Tool sequence: list_case_types → get_case_type_format("eviction-non-payment-of-rent") → get_pleading_base → draft → save_draft_as_docx

## Example 2 — eviction-bona-fide-personal-need

> *"Use the connector to draft a eviction bona fide personal need (Eviction on bona-fide personal need (Ragavendra Kumar / Akhileshwar Kumar framework)). Use anonymised placeholders for party names and figures."*

Tool sequence: list_case_types → get_case_type_format("eviction-bona-fide-personal-need") → get_pleading_base → draft → save_draft_as_docx

## Example 3 — eviction-nuisance-damage

> *"Use the connector to draft a eviction nuisance damage (Eviction on nuisance / damage to premises). Use anonymised placeholders for party names and figures."*

Tool sequence: list_case_types → get_case_type_format("eviction-nuisance-damage") → get_pleading_base → draft → save_draft_as_docx

## Notes for the reviewer

- All examples use placeholders.
- No external API keys / accounts required.
- `save_draft_as_docx` requires `pandoc`.
- Three-layer privacy firewall applies throughout.

---

## Synthetic case folder for Anthropic reviewer

A fully-fictional, AAAK-pseudonymised case folder is bundled at:

`SAMPLE-CASES/synthetic-eviction-non-payment-of-rent/`

It contains 3 source documents (.docx) plus a `case-facts-background.md` narrative.

**To exercise the pipeline end-to-end**, point `read_case_folder(path)` at this folder and follow the orchestration script returned by `get_agent_instructions()`. The Reader stage will extract facts, the Format stage will load the case-type SKILL.md template, and the remaining four agents (Drafter → Verifier → Refiner → Overseer) will produce `final-draft.docx`.

All identifiers in the bundled documents are structural placeholders (`[Petitioner-A]`, `[Premises-Address-Placeholder]`, `[Monthly-Rent-Placeholder]`, `[PAN-PLACEHOLDER-10-CHAR]`, `[DIN-PLACEHOLDER-19-DIGIT]`, `[Total-Arrears-Placeholder]`, etc.). The Pseudonymisation Gateway is therefore exercising against pre-pseudonymised content; reviewers seeking to test re-substitution may replace placeholders with their own fictional values before invoking the pipeline.

