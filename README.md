# RedCap-00

**Version 1.2.3 · 20 October 2026 · Instrument, formerly the RedCap-00 custom GPT (retired 1 October 2026) · Instructions last mirrored from the GPT on 15 July 2026 (no verification date recorded), before the conversion · License: [CC BY-NC-SA 4.0](LICENSE.md) · Changes: [CHANGELOG.md](CHANGELOG.md)**

> **Retired 1 October 2026 (KST).** The RedCap-00 custom GPT was retired on 1 October 2026 and converted to a private plug-in on the OpenAI platform. The instructions published in this repository are the text of record and suffice for anyone who wants to build their own. History and sources: [RETIREMENT.md](https://github.com/rolldabones/rolldabones/blob/main/RETIREMENT.md).

## What it does

RedCap-00 is the first tool in **GRCnext™**: a self-check, published as text with no hosted instance, of whether your organization can make real operational choices inside 72 hours under disruption. It tests five moves: safe pause, treasury reroute, data switchboard, substitution of critical dependencies and clean market exit. You answer forced-choice questions (A to D) and give an evidence level (E0 to E3) for each. The instrument scores each move from 0 to 4, caps a score where evidence or a prerequisite is missing and reports confidence and an evidence index, so uncertainty is explicit. The output is a board-ready packet. Scoring is evidence-capped and conservative by design.

## Run it in three steps

1. Paste the fenced block in [instructions.md](instructions.md), followed by the whole of [reference.md](reference.md), into the system prompt, custom instructions or project instructions of any current assistant. In a project, `reference.md` can be attached as a project file instead.
2. Give it the inputs it asks for (a safety confirmation, a short intake, 20 Fast Baseline answers and the consistency checks), or start from the fictional inputs in [example.md](example.md).
3. Review the output yourself and check it against [tests.md](tests.md). You own sign-off.

## How to use it well

Answer using high-level summaries. For each question, pick A–D and an evidence level.

- **A–D**
  - **A** = ad hoc or unknown
  - **B** = partial or informal
  - **C** = documented and owned
  - **D** = tested in the last 12 months with logs and follow-up actions, with alternates viable and approvals and communications ready
- **Evidence levels**
  - **E0** (0) no evidence
  - **E1** (1) verbal only
  - **E2** (2) documented artifact with an owner role
  - **E3** (3) tested in the last 12 months with logs and follow-up actions (corrective and preventive action, CAPA)

The tool scores conservatively. A move is capped at 2 when its average evidence is below E2 or when its prerequisite question is answered A. It also shows confidence and an evidence index so uncertainty is explicit. A score of 0 means “Unknown/Insufficient data” and is given only when more than half of a move’s answers are A with no evidence (E0).

## What not to paste

Do not paste confidential information, personal data, credentials, bank details, wiring instructions, sensitive contract text, regulator correspondence or security vulnerabilities. Use redacted summaries only.

## What you get

A board-ready packet: scorecard, evidence index, 72-hour breakpoints, top blockers with fixes and a 30/60/90-day plan, plus a simple drill script. In Fast Baseline the packet lists five breakpoints inferred from your answers, one per move. In Deepening mode the tool also runs a short 72-hour tabletop simulation and lists ten breakpoints drawn from it.

## Limitations

This is not legal advice, not a compliance determination and not sanctions screening. Jurisdiction is treated as unknown unless you specify it. Final Liability rests with the Human.

## Files

- [instructions.md](instructions.md): the instruction block, fenced and self-contained
- [reference.md](reference.md): the Reference Pack (question bank, scoring, confidence, tabletop, output schema)
- [example.md](example.md): one illustrative Fast Baseline run on a fictional organization, with the scorecard arithmetic
- [tests.md](tests.md): the regression harness, the scoring defects fixed in v1.2.0 and the run record
- [evidence/transcripts-2026-10-18-T5/](evidence/transcripts-2026-10-18-T5/README.md): the transcripts of run T5, copied byte for byte

## Change control

The configuration is Locked as of 1 October 2026. Changes are made in `instructions.md` and `reference.md` under this repository's version rule (Semantic Versioning; the README, `CITATION.cff` and `CHANGELOG.md` move in lockstep). A changed block is accepted only after one logged run of the published instructions as a system prompt on a current frontier model, recorded in `tests.md`. Each file's own header carries the release at which that file last changed, not the current release, which only the README masthead carries; the instruction block, the Reference Pack and the output footer keep the release at which the block last changed, until a later release changes it (CHANGELOG, Version string). The block fixes seven scoring defects (R1 to R7, listed in `tests.md` with their old wording and a case proving each fix). Its first logged run, T5 on 18 October 2026 (KST) on `claude-opus-5-5`, reproduced every expected score and confidence and failed the section 2 bullet cap in both modes: in Fast Baseline (case FMT-FB) through known defect K1, and in Deepening (case FMT-DP) by model behavior, over the cap on either reading of K1. Michael Paik reviewed the run on 19 October 2026 (KST) and concurs; it is not accepted, on open cases FMT-FB and FMT-DP (`tests.md`, Last run).

## Part of the ecosystem

This tool is one component of a larger body of AI governance, risk management and compliance work. The canonical map of all repositories is [ECOSYSTEM.md](https://github.com/rolldabones/rolldabones/blob/main/ECOSYSTEM.md) in the profile repository.

Nearest neighbors:
- [RedCap-01](https://github.com/rolldabones/RedCap-01): the companion diagnostic one level upstream, testing whether enterprise risk management (ERM) improves the decisions that determine objective achievement
- [GRCnext-Copilot](https://github.com/rolldabones/GRCnext-Copilot): the full optionality assessor; RedCap-00 is the free text-only self-check of the same question, whether Pipes, Switches and Exits would execute within tolerance
- [risk-informed-decision-making-prompt](https://github.com/rolldabones/risk-informed-decision-making-prompt): structures the decisions a failed move or a 72-hour breakpoint forces
- [grc](https://github.com/rolldabones/grc): the governance, risk management and compliance method the five moves and their evidence report into

## How to Cite

> Paik, Son-U Michael. *RedCap-00*, v1.2.3. GRC Solutions Korea, 2026. https://github.com/rolldabones/RedCap-00

A machine-readable citation is in [CITATION.cff](CITATION.cff).

## License

Released under [CC BY-NC-SA 4.0](LICENSE.md). Share and adapt non-commercially with attribution, under the same license.

---

Final Liability rests with the Human.
