# Contributing to Afri-OSCAL

Thank you — this project only works as a community artefact.

## What we need most

1. **Legal/compliance review** — is a control encoding faithful to the source instrument?
2. **New framework proposals** — open an issue with the public source document first
3. **Crosswalk mappings** — control↔control links between frameworks (clause references only for copyrighted standards)
4. **Plain-English/Swahili explainers** for existing controls

## Ground rules

- **Public law only, in full; copyrighted standards as clause references only.** PRs that paste ISO/PCI/CIS text will be declined.
- **Cite your source.** Every control must reference the exact section/regulation of the gazetted instrument.
- **Validation must pass.** CI runs OSCAL validation on every PR; run `trestle validate` locally first.
- **One framework per PR** where possible.

## Workflow

1. Open an issue describing the change (template provided)
2. Fork, branch from `main`, make the change
3. PR with source citations in the description
4. A maintainer (human) reviews every control change — expect interpretation questions

## AI-assisted contributions

AI-drafted encodings are welcome **if** you declare the tool used and have personally verified every control against the source text. Undeclared or unverified AI dumps will be closed.

## Licence

By contributing you agree your contribution is licensed under Apache-2.0.
