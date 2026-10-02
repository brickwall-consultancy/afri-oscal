# Afri-OSCAL

**Open, machine-readable compliance catalogs for African regulations — in [NIST OSCAL](https://pages.nist.gov/OSCAL/) format.**

Maintained by [Brickwall Consultancy](https://brickwallconsult.com) (Nairobi, Kenya). Apache-2.0 licensed.

## Why

As of 2026, **no OSCAL catalog exists for any African regulation**. Every bank, SACCO, fintech, hospital and school that must comply with the Kenya Data Protection Act, CBK guidance, SASRA guidelines or the CMCA Critical Information Infrastructure Regulations starts from a PDF and a blank spreadsheet. This repository fixes that — once, in the open, for everyone.

Machine-readable catalogs mean:

- one control set, many tools — anything that speaks OSCAL can consume these
- crosswalks between frameworks become data, not consultancy folklore
- regulatory updates become diffs, not re-reads

## What's here

| Path | Contents | Status |
|---|---|---|
| `catalogs/kenya-dpa-2019/` | Kenya Data Protection Act 2019 + ODPC regulations as an OSCAL catalog | 🚧 in progress |
| `catalogs/sasra-ict/` | SASRA ICT guidelines for SACCOs | 📋 planned |
| `catalogs/ln44-cii/` | Legal Notice 44/2024 — Critical Information Infrastructure Regulations | 📋 planned |
| `profiles/sacco-baseline/` | Tailored baseline for deposit-taking SACCOs (DPA + SASRA) | 📋 planned |
| `profiles/fintech-baseline/` | Tailored baseline for fintechs/PSPs (DPA + CBK) | 📋 planned |
| `mappings/` | Crosswalks between frameworks (copyrighted standards: clause references only) | 📋 planned |
| `docs/` | Plain-English control explainers | 📋 planned |

Status legend: 🚧 actively being encoded · 📋 planned

## Principles

1. **Public law only, in full.** Statutes and regulator-issued guidance are encoded completely. Copyrighted standards (ISO 27001, PCI DSS, CIS) appear **only as clause-number mappings** — never their text.
2. **Traceable.** Every control cites the exact section of the source instrument. The source documents are listed in each catalog's README.
3. **Validated.** Every artefact must pass `compliance-trestle` / `oscal-cli` validation in CI before merge.
4. **Human-reviewed.** AI-assisted drafting is used to accelerate encoding; a named human reviews every control before it lands.

## Using the catalogs

Catalogs are standard OSCAL JSON. Example with [compliance-trestle](https://github.com/oscal-compass/compliance-trestle):

```bash
pip install compliance-trestle
trestle import -f catalogs/kenya-dpa-2019/catalog.json -o kenya-dpa
```

Or consume the raw JSON directly from any OSCAL-aware tool.

## Contributing

Corrections, mappings, and new-framework proposals are welcome — see [CONTRIBUTING.md](CONTRIBUTING.md). Lawyers and compliance practitioners are especially welcome: the hardest part is interpretation, not JSON.

## Disclaimer

These catalogs are a good-faith technical encoding of public legal instruments. They are **not legal advice**. Verify against the gazetted source text, which always prevails.

## License

[Apache-2.0](LICENSE) © Brickwall Consultancy
