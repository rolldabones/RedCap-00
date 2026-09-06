# Changelog

All notable changes to this repository are documented here. Versioning follows [Semantic Versioning](https://semver.org/). The README and this file version in lockstep; prior versions are superseded, never silently overwritten.

## v1.1.3 (2026-09-06)

Citation infrastructure, doctrine citation line and lockstep maintenance. Session C of the September 2026 improvement pack, one patch release per repository across all 21 public repositories.

- **`CITATION.cff` added** in the house form settled at D-C1: no `type` field, `version` and `date-released` in lockstep with the README, `license` as the SPDX identifier for this repository's licence, `abstract` taken from this repository's ECOSYSTEM.md role line rather than newly written.
- **How to Cite block** aligned to this release and pointing at `CITATION.cff`.
- **Retired trademark rendering corrected in live text.** The prompt line read `by GRC next™`. The canonical closed-up form `GRCnext™` was adopted account-wide on 30 July 2026 and logged at ECOSYSTEM.md v1.7.2, which states the spaced form is no longer used anywhere. It survived here for thirty-eight days because the retirement was never registered. It is registered now.
- All other files in this repository are unchanged byte for byte.

## v1.1.2 (2026-08-13)

License metadata sweep. An `SPDX-License-Identifier: CC-BY-NC-SA-4.0` line and the canonical Creative Commons legal code are now carried inside the existing license file. The filename is unchanged and the human-readable summary is retained above the legal code.

- The primary audience is automated intake and provenance tooling, which reads the SPDX tag rather than prose. Automated license detection previously reported nothing across all twenty-one repositories in this account.
- No change to the licence in force. The identifier records what was already true.

## v1.1.1 (2026-07-30)

Patch release. Trademark rendering only.

### Changed
- Trademark rendering corrected to the canonical closed-up form GRCnext™. The retired spaced form "GRC next" is withdrawn from repository prose. One occurrence, in the opening description line.
- Version line updated in lockstep.

### Unchanged
- The instruction block under Build guide for custom GPT mirrors the deployed RedCap-00 Custom GPT and retains the spaced form as deployed. Correcting it here would break the mirror rule. It is carried as a documented pending production change and re-dates when the live GPT is edited.
- The v1.1.0 entry below records the earlier Unicode-bold heading fix in its original wording. Historical entries are not rewritten.

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
