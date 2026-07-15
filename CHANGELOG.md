# Changelog

All notable changes to this repository are documented here. Versioning follows [Semantic Versioning](https://semver.org/). The README and this file version in lockstep; prior versions are superseded, never silently overwritten.

## v1.1.0 (2026-07-15)

First versioned release under the repository improvement program. The pre-existing README is treated as implicit v1.0.0.

### Added
- Repository version header (v1.1.0, date, license, CHANGELOG link) under the title. The deployed custom GPT instruction inside the build guide carries its own internal version string (v0.1) and is unchanged; the repository version and the instruction version are separate identifiers until the production instruction is next revised.
- Part of the ecosystem section linking the canonical ECOSYSTEM.md in the profile repository plus four nearest neighbors (RedCap-01, GRCnext-Copilot, risk-informed-decision-making-prompt, grc), placed at the end of the README.
- LICENSE.md (CC BY-NC-SA 4.0, the ecosystem default) and a README License section.
- CHANGELOG.md (this file).

### Fixed
- Unicode mathematical-bold heading text ("GRC next" set in special characters) in the first line replaced with standard markdown bold; the special characters broke screen readers, in-page search, copy-paste and text matching (the same defect class fixed in origami-method v1.1.0). The deployed GPT instruction block is a production mirror and is not touched; if it carries the same characters in production, that is logged as a proposed production change, not edited here.

### Unchanged
- The self-check itself: the five moves, A to D and E0 to E3 scales, evidence-capped scoring, build guide, output contract and regression harness.

## v1.0.0 (implicit)

Pre-existing repository state, reconstructed: a single README containing the RedCap-00 self-check (five critical moves inside 72 hours under disruption), usage guidance, data hygiene rules, limitations and the full custom GPT build guide including instructions (internal version string v0.1), scoring method, output format and regression harness.

Final Liability rests with the Human.
