# Changelog

All notable changes to this repository are documented here. Versioning follows [Semantic Versioning](https://semver.org/). The README, `CITATION.cff` and this file version in lockstep; prior versions are superseded, never silently overwritten.

## v1.2.4 (2026-10-20, KST)

Patch. Independent review of 20 October 2026; changes made with Claude, approved by Michael Paik. `reference.md` is unchanged, so its run T5 digest still holds; the instruction block changed and is not accepted pending a logged run.

### Instrument
- **JURISDICTION rule (RC0-02).** `instructions.md`: "Never say “legal” or “compliant.”" is replaced by "Never declare anything legal or compliant.", which the MISSION line, the question bank and the example can follow. Block header to v1.2.4 with an Acceptance note: not accepted pending a logged run. `tests.md` records that the T5 digests describe the v1.2.0 block and gives the current block's digest.

### Accuracy and disclosure
- **README Change control (RC0-01, RC0-06).** The T5 run is recorded as reviewed by Michael Paik on 19 October 2026 (KST), not accepted on open cases FMT-FB and FMT-DP; only FMT-FB is attributed to K1, and FMT-DP is model behavior, over the cap on either reading.
- **Acceptance caution (RC0-03).** Run it in three steps now says that the current block is not accepted under this repository's change control.
- **K1 both counts (RC0-04).** `tests.md` reports the section 2 bullet count of every final T5 packet both ways; K1 stays open.
- **Confidence Low explained (RC0-08).** The README says Low means untested evidence, not weak evidence, with the all-C/E2 case.
- **Incomplete first turns (RC0-09).** `tests.md` records the two first turns that ended with stop_reason `refusal` as incomplete; the README run steps say what to do when a reply stops before the packet.
- **Known defects disclosed, not changed (RC0-07, RC0-10, RC0-12, RC0-14).** `tests.md` K2 (the monotonic confidence claim holds only while the consistency check passes), K3 (a serial comma and unexpanded acronyms in `reference.md`) and K4 (the example packet departs from the section 7 schema and does not offer Deepening). The Reference Pack is the text of run T5, and the example's packet and input are a produced output and a run input, so they are left as they are.
- **Erratum to v1.2.0 (RC0-07).** That entry says "strengthening any answer can no longer lower confidence". This holds only while the move's consistency check passes (`tests.md` K2). The shipped entry stays as cut.
- **Evidence index (RC0-16, RC0-19).** S4 carries a verdict with no reasoning; `summary.json` keys the instructions file by the maintainer's local path. The T5 runner is not shipped, so the run cannot be reproduced from this repository alone.
- **Citation (RC0-17).** The README says `CITATION.cff` names no publisher because the Citation File Format has no top-level publisher field.

### Readability
- **Internal references (RC0-11).** "ruling 9", "report 11, Test 4" and "session T5" in `tests.md`, `example.md` and the evidence index are replaced with plain statements. Shipped CHANGELOG entries stay as cut.
- **House style (RC0-12, RC0-13, RC0-18).** CAPA (corrective and preventive action), ERM (enterprise risk management) and KST (Korea Standard Time) spelled out at first use in the README and `tests.md`; "as at" to "as of"; "on the device" to "in the same agent session" in `example.md`.
- **Version convention (RC0-15).** README Change control explains that each file header carries the release at which that file last changed.

### Versions
- README masthead, How to Cite, `CITATION.cff` and this file to v1.2.4. `instructions.md`, `tests.md` and `example.md` headers to v1.2.4, the release at which they last changed. `reference.md` and the output footer stay at v1.2.0.

Not changed: the retirement line (RC0-05; kept as recorded). SPDX tag in `LICENSE.md` (correct syntax).

## v1.2.3 (2026-10-20, KST)

- LICENSE: two defects against the Creative Commons legal code corrected (the space in 'ShareAlike. In'; the CC0 sentence of the closing notice). Operative terms unchanged.
- README masthead, How to Cite and `CITATION.cff` to v1.2.3.

## v1.2.2 (2026-10-19, KST)

Patch, from the weekly maintenance sweep of 19 October 2026 (KST) and Michael Paik's review of the T5 runs, completed 19 October 2026 (KST), on which he concurs with the scoring as recorded. No change to `instructions.md` or `reference.md`.

- **Run T5 reviewed.** `tests.md` Acceptance records the reviewer. Not accepted, as before: FMT-FB and FMT-DP open.
- README masthead, `tests.md` masthead, How to Cite and `CITATION.cff` to v1.2.2.

## v1.2.1 (2026-10-18, KST)

Records-only patch: the ruling 9 logged run. Session T5 of the whole-account review of 15 October 2026 (doc section 5, RedCap-00 harness row; the T5 row of the session plan, ruling 9 runs added 18 October 2026). No wording of `instructions.md`, `reference.md` or `example.md` changes; the instruction block, the Reference Pack and the output footer stay at v1.2.0, the release at which they last changed.

### What changed and why
- **The ruling 9 run (README Change control: "A changed block is accepted only after one logged run of the published instructions as a system prompt on a current frontier model, recorded in `tests.md`").** The harness in `tests.md` was encoded as 26 cases: Tests A to E (section 2), the fifteen fixed-defect cases R1a to R7-5 (section 4), the four refusal and safety tests (section 3; the missing Reference Pack test runs with `instructions.md` alone) and the five format checks (section 1) as one case per mode, the Fast Baseline case on the fictional input published in `example.md`. Each scoring case supplies the whole intake, the answers and the consistency checks in one turn, and passes only on the score and confidence the table computes. Tested model `claude-opus-5-5`, the block and `reference.md` as the system prompt; scored by `claude-sonnet-5-5`, a different model. **Result:** scorer 24 PASS, 2 FAIL (FMT-FB, FMT-DP, both on check F2, the section 2 cap of five bullets); every expected score and confidence reproduced (20 of 20). Session review of the two FAILs: FMT-FB concur, instrument defect (the cap does not say whether nested bullets count; new known defect K1, not fixed in this release because a changed Reference Pack needs its own run); FMT-DP concur, model behavior (six top-level bullets). Not accepted: open cases FMT-FB and FMT-DP; reviewer pending (Michael Paik). Observation: turn 1 of Test-B and Test-E stopped with stop_reason `refusal`; cause Unknown.
- **Evidence.** `evidence/transcripts-2026-10-18-T5/`: the 26 transcripts copied byte for byte with the closing line appended, the runner's `summary.json` and an index.
- **`tests.md`:** Last run section (configuration, per-case table, counts, acceptance) and known defect K1; header to v1.2.1. README: Change control sentence and Files list.
- README masthead, How to Cite, `CITATION.cff` and this file move to v1.2.1 in lockstep.

### Findings by class
- Confirmed: no run record (doc section 5); the run is the fix. New from the run: K1 (instrument defect).
- Already fixed in v1.2.0: R1 to R7, Test B, the uncomputable evidence cap and the asymmetric prerequisite caps (doc section 5 row; section 4 item 5).
- Not reproducible: none. Outside the review: none edited.

### Deferred
- K1, the bullet-cap wording in reference.md section 9: an instrument change, for a later release with its own run.
- Acceptance: Michael Paik's review of the run.

## v1.2.0 (2026-10-18, KST)

Minor release: Reference split, R1 to R7 fixed, evidence scale numbered, worked scorecard. Session T4 of the whole-account review of 15 October 2026 (doc section 4, item 5, and items 2 and 3 as the template; reviewer report 11, items R1 to R7, A9, A13, B1, B3, B4, C1, C3 and idea 3), under determination D5 and ruling 9. Dated amendment, 18 October 2026 (KST); no earlier entry is re-dated or rewritten.

**What the self-check measures is unchanged:** whether the organization can execute five critical moves (safe pause, treasury reroute, data switchboard, substitution, market exit) within 72 hours under disruption, on the same question bank, the same A to D and E0 to E3 scales and the same output packet. The rule fixes remove contradictions only: each makes a rule computable or makes two statements of one rule agree.

### What changed and why

- **Single-file layout split (doc §4 item 2; report 11 B1, C1, C3).** The README carried the instruction block unfenced and the Reference file unfenced, its boundary stated only in prose, with H2 sections under an H3 file title. Now: `instructions.md` (the block, fenced and self-contained), `reference.md` (the Reference Pack under its own H1 title, sections at H2 and H3), `example.md`, `tests.md` and a README in the post-retirement template (masthead, retirement line, What it does, Run it in three steps, the repository's own method sections, Files, Change control, ecosystem, cite, license).
- **R1 to R7 fixed (report 11 Test 4; R1 to R4 first logged 5 October 2026 in IMPROVEMENT-REGISTER row 1).** Each is itemized old → new below and listed with its old wording and a proving case in `tests.md`.
- **Regression harness moved to `tests.md` (report 11 B3).** Test B corrected to A on Q1, so it agrees with the prerequisite cap (R2). One computed case per defect added. The expected values were computed by a short Python implementation of the rules, run on the device: a rule check by computation, not a model run. `tests.md` records that no logged run of the published instructions exists yet (ruling 9).
- **Known defects in the repository (report 11 B4).** R1 to R7 are now listed in `tests.md`, fixed, with their old wording; none remains only in the private register.
- **Worked scorecard (idea 3; doc §4 item 5).** `example.md`: one fictional organization, all five moves, Fast Baseline answers, the arithmetic, caps and confidence, computed with Python on the device.
- **"Public" self-check (report 11 A9).** README:5 called it "a free public self-check" while :9 said the repository links no hosted instance and the plug-in is private. Now "published as text with no hosted instance". The same word is removed from this repository's neighbor line for GRCnext-Copilot.
- **Notice wording (report 11 A13).** The retirement notice, whose wording differed from the other six repositories, is replaced by the standard retirement line under the masthead (D5). The 11 December 2026 date leaves the notice.
- **Build guide heading.** "Build guide for custom GPT" and "What to put in the Knowledge “Reference” file" are struck; Run it in three steps with `instructions.md` and `reference.md` replace them.
- **Ecosystem snippet (report 11 C1): not reproducible.** ECOSYSTEM.md protocol item 3 prescribes no exact form ("see the snippet in any current repository README"), and this repository's lead sentence and ":" separators match the form in `grc` and `origami-method`. Unchanged. T3 reached the same finding on 17 October 2026.
- **Version string.** The pack's internal version string `v0.1` is retired. The instruction block and the Reference Pack now carry v1.2.0, the repository release at which they last changed, in their status lines, in the REFERENCE PACK RULE and in the output footer (`RedCap-00 v1.2.0 | Evidence-capped scoring`). They keep that version until a later release changes them.
- **Masthead** in the template form; the last-verified element reads "Instructions last mirrored from the GPT on 15 July 2026 (no verification date recorded), before the conversion", because no verification date was ever recorded.
- **History carried.** The v1.1.4 entry records that the first instruction line may differ from the GPT as last deployed by one token (the spaced trademark form); that remains Unknown and is carried in `instructions.md` and `tests.md` as history. The published block is the text of record.
- README masthead, How to Cite, `CITATION.cff` and this file move to v1.2.0 in lockstep. `LICENSE.md` is unchanged byte for byte and describes no deployed GPT.

### Choices made inside the fixes

Each fix had more than one consistent reading. The one taken, and why:

- **R1, rounding direction.** An exact half rounds down, the conservative direction the instrument already states for its scoring. Rounding up would credit a move with a level it has not reached on half its answers.
- **R2 and R7, which answers fire a prerequisite cap.** The answer A on the move's prerequisite question, and nothing else. The old Move 1 ("not delegated") and Move 5 ("OR exit plan untested") wording capped documented, owned profiles, so an all-C/E2 profile scored 2 on Moves 1 and 5 and 3 on Moves 2 to 4. A weaker but documented answer is now handled by the evidence cap and by confidence, as on every other move.
- **R7, Move 4's prerequisite question is Q2, not Q1.** Report 11 proposed "A on Q1" for every move. Move 4's cap names a qualified alternate, which is Q2 (Qualified alternates); Q1 is the single-point-of-failure list. Moving the cap to Q1 would change what the cap tests, so it stays on the question it named. Under the old wording a Q2 answer of B ("possible but unqualified") also fired the cap; it no longer does.
- **R3, the zero rule.** The old "Majority of that move's answers are A AND evidence is E0 for those answers" is restated in counts (more than half of the answers at A/E0) and made the only route to a score of 0 and to an Unknown score. An unanswered question is recorded as A at E0, since A already covers "unknown"; before, "answered questions" left the denominator open.
- **R4, counts per mode.** Fast Baseline lists 5 breakpoints, one per move, inferred from the answers and marked as such; Deepening lists 10, drawn from the tabletop. Top Blockers stay at 10 in both modes because they are drawn from the answers.
- **R5, the consistency check.** Asked for every move rather than for "the strongest move" and "stop/reroute/exit decisions" only, so that "consistency checks pass" is defined for Moves 3 and 4. This adds up to two questions per move to the intake; it changes confidence only, never a score. "More than half" (3 of 4, 4 of 7) keeps the old word "majority"; the change is that Medium counts E2 or E3 together, so strengthening any answer can no longer lower confidence.
- **Instruction block, missing Reference Pack.** The block now says so and stops if the Reference Pack is not supplied; the GPT had the knowledge file attached and needed no such rule. A matching safety test is added in `tests.md`.

### Configuration as last deployed, Locked 1 October 2026

- **Name:** RedCap-00 (the block names itself "RedCap-00 Optionality Self-Check by GRCnext™")
- **Description:** Unknown (not recorded)
- **Conversation starters:** Unknown (not recorded)
- **Capabilities:** Unknown (not recorded)
- **Knowledge files:** one, "RedCap-00_Reference_v0.1", named by the instruction block and published in the README until v1.1.4 as `RedCap-00_Reference_v0.1.md`
- **Model:** Unknown (not recorded)
- **Instructions:** as last mirrored on 15 July 2026 (v1.1.0), no verification date recorded; the text is at tag `v1.1.4`, `README.md` lines 50 to 99 (block) and 105 to 584 (Reference file). Whether the first line matched the GPT at the trademark token is Unknown (v1.1.4).
- **Status:** converted to a private plug-in on the OpenAI platform on 1 October 2026; the custom GPT is retired.

### Struck from the README, 18 October 2026 (KST)

- ~~"RedCap-00 is the first tool in **GRCnext™**: a free public self-check, evidence-capped and conservative by design."~~ **STRUCK 18 October 2026 (KST).** Replaced by What it does.
- ~~"RedCap-00 is a free self-check to evaluate whether your organization can make real operational choices inside 72 hours under disruption. It focuses on five moves: safe pause, treasury reroute, data switchboard, substitution of critical dependencies and clean market exit. This repository links no hosted instance of the self-check: to run it, build it from the build guide below."~~ **STRUCK 18 October 2026 (KST).** Replaced by What it does and Run it in three steps. (Quoted without its link to the struck heading Build guide for custom GPT.)
- ~~"## Build guide for custom GPT"~~ **STRUCK 18 October 2026 (KST).** Heading.
- ~~"**Retirement notice, 5 October 2026 (KST).** OpenAI is retiring custom GPTs. Its [Custom GPT retirement and migration FAQ](https://help.openai.com/en/articles/20001519-custom-gpt-retirement-and-migration-faq), read on 5 October 2026, states that custom GPTs are scheduled to retire on **11 December 2026**, or 11 February 2027 for Enterprise workspaces with an approved deferral, and that a migrated GPT stays usable until retirement but becomes read-only. The RedCap-00 custom GPT was converted to a ChatGPT plugin on 1 October 2026, and the plugin is private and not publicly listed. This repository carries no link to the GPT, so no link here breaks."~~ **STRUCK 18 October 2026 (KST).**
- ~~"Everything needed to build your own stays published here: the instruction block and the Reference file. OpenAI's replacement is the ChatGPT plugin, in which a GPT's instructions become a Skill and its knowledge files become reference files. Its [Plugins in ChatGPT and Codex](https://help.openai.com/en/articles/20001256-plugins-in-chatgpt-and-codex) article, read on 28 September 2026 and not re-read since, offers plugin creation in supported ChatGPT Business and Enterprise workspaces, so check what your plan allows. The instruction block is not tied to ChatGPT and also serves as the custom instructions of any assistant that accepts them. A plugin does not inherit a GPT's selected model and custom actions do not transfer, so choose the model yourself and test before you rely on the output."~~ **STRUCK 18 October 2026 (KST).** The two paragraphs above were the retirement notice; the standard retirement line replaces them.
- ~~"The Instructions block below mirrors the RedCap-00 custom GPT and is edited here only to follow a change made in production; the one known exception is recorded in [CHANGELOG.md](CHANGELOG.md) at v1.1.4. The Reference file is the Knowledge file that block names."~~ **STRUCK 18 October 2026 (KST).** Mirror sentence; the published block is the text of record.
- ~~"## What to put in the Knowledge “Reference” file"~~ **STRUCK 18 October 2026 (KST).** Heading.
- ~~"The Reference file is everything from the `RedCap-00_Reference_v0.1.md` heading below to the end of section 10.3; it stops before Part of the ecosystem. Its `v0.1` is the pack's own version string, printed in the output footer, and is separate from this repository's version."~~ **STRUCK 18 October 2026 (KST).** Boundary prose; the Reference Pack is now its own file.
- ~~"The tool scores conservatively and applies evidence-capped scoring when evidence is weak. It also shows confidence and an evidence index so uncertainty is explicit. A score of 0 means “Unknown/Insufficient data.”"~~ **STRUCK 18 October 2026 (KST).** R3: How to use it well now states the caps and the zero rule.
- ~~"RedCap-00 is the free public self-check of the same question"~~ **STRUCK 18 October 2026 (KST).** GRCnext-Copilot neighbor line, now "the free text-only self-check of the same question".

### Instruction block changes, old → new

1. House style: serial comma removed (T3 deferral).

```text
physical safety, >USD10m impact, or >100,000 people affected.
```

becomes

```text
physical safety, >USD10m impact or >100,000 people affected.
```

2. GPT-only dependency recast (report 11 B1): the attached Knowledge file becomes the Reference Pack supplied with the instructions.

```text
Use the attached Knowledge file “RedCap-00_Reference_v0.1” exactly for:
```

becomes

```text
Use the RedCap-00 Reference Pack v1.2.0 (reference.md), supplied with these instructions, exactly for:
```

3. R6: the list names the numeric evidence scores.

```text
- A–D semantics, evidence levels E0–E3

```

becomes

```text
- A–D semantics, evidence levels E0–E3 and their numeric scores

```

4. Regression harness moved to `tests.md`; GPT-only dependency recast: the block stops if the Reference Pack is missing.

```text
- Output packet structure and exact counts
- Regression harness rules

Do not invent new question themes or new sections.
```

becomes

```text
- Output packet structure and exact counts per mode

Do not invent new question themes or new sections. If the Reference Pack has not been supplied with these instructions, say so and stop.
```

5. GPT-only dependency recast ("per reference") and R5: consistency checks for every move.

```text
3. Ask Fast Baseline questions (per reference). Then run consistency checks.
```

becomes

```text
3. Ask the Fast Baseline questions (Reference Pack section 5.1). Then run the consistency checks for every move (section 5.2).
```

6. GPT-only dependency recast ("per reference").

```text
4. Offer Deepening (per reference) including mini tabletop if user opts in.
```

becomes

```text
4. Offer Deepening (Reference Pack sections 5.1 and 6), including the mini tabletop, if the user opts in.
```

7. GPT-only dependency recast ("per reference") and R4: counts per mode.

```text
5. Produce the Output Packet with exact headings and exact counts (per reference), then STOP.
```

becomes

```text
5. Produce the Output Packet with the exact headings and the counts for the mode run (Reference Pack section 9), then STOP.
```

8. R3: one Unknown rule.

```text
Always use “Unknown/Insufficient data” when evidence is weak.  
```

becomes

```text
Report a move as “Unknown/Insufficient data” only under the zero rule (Reference Pack section 8.2); otherwise weak evidence caps the score (section 3) and lowers confidence (section 4). Use “Unknown” for any fact the user has not supplied.  
```

9. GPT-only dependency recast ("version string from the reference"); the footer now carries v1.2.0.

```text
End output with version string from the reference.
```

becomes

```text
End output with the exact footer in Reference Pack section 9.
```

### Reference file changes, old → new

The Reference file's section 10 (Regression Harness, 10.1 to 10.3) moved whole to `tests.md`, with Test B changed from "(A or B on Q1, E0/E1)" to A on Q1 (R2) and section 10.1's counts stated per mode (R4).

1. Header: version string, purpose (serial comma removed, T3 deferral; harness moved to `tests.md`) and use rule (GPT wording recast).

```text
**Artifact:** RedCap-00 Reference Pack  
**Version:** v0.1  
**Purpose:** Canonical question bank, scoring, output schema, and regression harness for RedCap-00 Optionality Self-Check.  
**Use rule:** The GPT must follow this file exactly. No new sections. No new question themes.
```

becomes

```text
**Artifact:** RedCap-00 Reference Pack  
**Version:** v1.2.0 (formerly v0.1; see [CHANGELOG.md](CHANGELOG.md) v1.2.0)  
**Purpose:** Canonical question bank, scoring method and output schema for the RedCap-00 Optionality Self-Check. The regression harness is in [tests.md](tests.md).  
**Use rule:** The assistant running [instructions.md](instructions.md) must follow this file exactly. No new sections. No new question themes.
```

2. F10: en dash removed from heading (T3 deferral).

```text
## 1) A–D Semantics (consistent across all questions)
```

becomes

```text
## 1) A to D Semantics (consistent across all questions)
```

3. F10: en dash removed from heading (T3 deferral).

```text
## 2) Evidence Levels E0–E3 (strict definitions)
```

becomes

```text
## 2) Evidence Levels E0 to E3 (strict definitions)
```

4. R6: E0 numbered.

```text
- **E0 No evidence:**
```

becomes

```text
- **E0 (evidence score = 0) No evidence:**
```

5. R6: E1 numbered.

```text
- **E1 Verbal only:**
```

becomes

```text
- **E1 (evidence score = 1) Verbal only:**
```

6. R6: E2 numbered.

```text
- **E2 Documented + owned:**
```

becomes

```text
- **E2 (evidence score = 2) Documented + owned:**
```

7. R6: E3 numbered.

```text
- **E3 Tested + logged + CAPA:**
```

becomes

```text
- **E3 (evidence score = 3) Tested + logged + CAPA:**
```

8. R6: evidence average defined and computable.

```text
- If **average evidence for a move < E2**, cap that move’s score at **2**.
```

becomes

```text
- Compute the move’s **evidence average**: the mean of its evidence scores (Section 2: E0=0, E1=1, E2=2, E3=3) across all of the move’s answers, not rounded.
- If the **evidence average is below 2** (below E2), cap that move’s score at **2**.
```

9. R7 and R2: every prerequisite cap is an existence test (prerequisite question answered A).

```text
### 3.2 Prerequisite caps (cap at 2 if any apply)

- **Move 1 Safe pause:** stop authority unclear or not delegated
- **Move 2 Treasury reroute:** no alternate bank or rail identified
- **Move 3 Data switchboard:** Tier-1 data flows not mapped including logs and telemetry
- **Move 4 Substitution:** no qualified alternate for a Tier-1 dependency
- **Move 5 Market exit:** exit obligations unclear OR exit plan untested
```

becomes

```text
### 3.2 Prerequisite caps (existence tests)

Each move has one prerequisite question. If that question is answered **A**, cap the move’s score at **2**. Any other answer leaves the move uncapped by this section.

- **Move 1 Safe pause:** Q1 Stop authority clarity answered A (none or unclear)
- **Move 2 Treasury reroute:** Q1 Alternate banks and rails answered A (none)
- **Move 3 Data switchboard:** Q1 Tier-1 data flow map answered A (none)
- **Move 4 Substitution:** Q2 Qualified alternates answered A (none)
- **Move 5 Market exit:** Q1 Exit plan answered A (none)
```

10. R5: confidence thresholds in counts; monotonic.

```text
- **High:** Majority **E3** and consistency checks pass
- **Medium:** Majority **E2** and at least one **E3**
- **Low:** Otherwise

**Confidence downgrade rule:**

- If consistency checks conflict with E3 claims, set confidence to **Low** for the affected move(s).
```

becomes

```text
Counts are taken over the move’s answers: 4 in Fast Baseline, 7 in Deepening. “More than half” means 3 or more of 4, or 4 or more of 7.

- **High:** more than half of the answers at **E3** and the move’s consistency check passes (Section 5.2)
- **Medium:** not High; more than half of the answers at **E2 or E3**, at least one answer at **E3**, and the move’s consistency check passes
- **Low:** otherwise

Raising the evidence level of any answer never lowers confidence.

**Confidence downgrade rule:**

- If the move’s consistency check fails (Section 5.2), set confidence to **Low** for that move.
```

11. R5: consistency check defined for every move.

```text
Ask and record:

1. **Last exercise date** for the strongest move (month/year)
2. **Approver role** for stop/reroute/exit decisions
3. **Artifact location** (general system, no links)

If inconsistent with E3 claims, downgrade confidence accordingly.
```

becomes

```text
Ask and record, for each move:

1. **Last exercise date** (month/year) and whether a log and a CAPA exist, for each move with any **E3** answer
2. **Approver role** for the move’s decision (Move 1 stop, Move 2 reroute, Move 3 data switch or clean stop, Move 4 substitution cutover, Move 5 exit)
3. **Artifact location** (general system, no links) for the move’s E2 and E3 artifacts

A move’s consistency check **passes** unless one of these holds:

- an E3 answer lacks a month/year within the last 12 months, a log or a CAPA
- the move has an E2 or E3 answer and no approver role can be named
- the move has an E2 or E3 answer and no artifact location can be named

A move with no E2 or E3 answer passes; its confidence is Low under Section 4 in any case. If a move’s check fails, downgrade that move’s confidence to Low (Section 4).
```

12. R1 and R3: exact half rounds down; an unanswered question is A at E0.

```text
- Map answers to numeric: **A=1, B=2, C=3, D=4**.
- Compute the **rounded average** across that move’s answered questions.
```

becomes

```text
- Map answers to numeric: **A=1, B=2, C=3, D=4**.
- A question the user cannot or will not answer is recorded as **A** at **E0** (A covers unknown) and counts as an answer.
- Compute the **average** (arithmetic mean) of the move’s pattern scores across all of its answers.
- Round it to the nearest whole number. An exact half rounds **down**, the conservative direction: 2.5 → 2 and 3.5 → 3. Exact halves arise only in Fast Baseline (four answers); seven answers never average to an exact half.
```

13. R3: one zero rule, in counts, the only route to Unknown.

```text
Set the move score to **0** only if:

- **Majority** of that move’s answers are **A** AND evidence is **E0** for those answers.
```

becomes

```text
Set the move score to **0**, reported as **Unknown/Insufficient data**, if and only if more than half of the move’s answers are **A** at **E0** (3 or more of 4 in Fast Baseline; 4 or more of 7 in Deepening). When this zero rule applies, skip 8.1 and 8.3 for that move.

This is the only route to a score of 0 and the only case in which a move’s score is reported as Unknown/Insufficient data. Weak evidence that does not meet the zero rule is handled by the caps (Section 3) and by confidence (Section 4).
```

14. R3: bounds restated.

```text
- Final score is the provisional score after caps, bounded 0–4.
```

becomes

```text
- Final score is the lower of the provisional score and any cap that applies. A move not zeroed under 8.2 therefore scores 1 to 4.
```

15. R4: count rules stated per mode (serial comma removed).

```text
The model output must contain **exactly 10 sections** with the headings below, in order, and must meet the count rules.
```

becomes

```text
In both modes the model output must contain **exactly 10 sections** with the headings below in order and must meet the count rules. Where a count differs by mode, both counts are stated.
```

16. R4: breakpoints per mode.

```text
   - Exactly **10 bullets**
   - Each bullet includes: time window, impacted move(s), what breaks, why it blocks execution
```

becomes

```text
   - Fast Baseline: exactly **5 bullets**, one per move, each drawn from that move’s weakest answer and marked “from answers, not exercised”
   - Deepening: exactly **10 bullets**, drawn from the mini tabletop (Section 6) and the answers
   - Each bullet includes: time window, impacted move(s), what breaks, why it blocks execution
```

17. R4: blockers stated for both modes.

```text
   - Exactly **10 numbered items**
   - Each includes:
```

becomes

```text
   - Exactly **10 numbered items** in both modes, drawn from the answers (and in Deepening also from the tabletop)
   - Each includes:
```

18. Footer version string.

```text
`RedCap-00 v0.1 | Evidence-capped scoring`
```

becomes

```text
`RedCap-00 v1.2.0 | Evidence-capped scoring`
```


## v1.1.4 (2026-10-05)

Retirement notice, and the first slot of the continuous improvement rotation. Patch: companions and corrections only. The self-check, the Instructions block and the Reference file are unchanged.

- **Retirement notice added** under Build guide for custom GPT. The RedCap-00 custom GPT was converted to a private ChatGPT plugin on 1 October 2026. OpenAI's Custom GPT retirement and migration FAQ, read on 5 October 2026, gives 11 December 2026 as the retirement date and states that a migrated GPT stays usable until then but becomes read-only. The account's notices of 28 September 2026 reached six repositories and not this one, because this repository recorded its deployed GPT in this file (v1.1.0, v1.1.1) and nowhere in the README. The notice's sentence on which workspaces can create plugins is carried at its 28 September 2026 read date; the plugins article returned a server error twice on 5 October 2026.
- **The README now says the Instructions block is a mirror.** Until this release that rule lived only in this file.
- **Correction to the record, itemized separately.** The v1.1.1 entry says the instruction block retains the retired spaced form of the mark as deployed and that correcting it would break the mirror rule. The v1.1.3 entry corrected that same line as live text and did not say that it superseded the v1.1.1 statement. It did. Whether the same edit was made in the GPT before it became read-only is Unknown, so the first instruction line may differ from the deployed GPT by that one token. Both entries are shipped history and are unchanged.
- **Doctrine rendering:** Limitations read "Final liability rests with the Human." It now carries the capital L of the closing line and of `DOCTRINE.md` section 3.
- **House style:** four serial commas removed from the author's own prose, in What this is, What not to paste, What you get and Limitations. The Instructions block and the Reference file are untouched, their serial commas included.
- **Entry path:** What this is now says that this repository links no hosted instance and points to the build guide. How to use it well gives D the Reference file's fuller wording, so that D and E3 no longer read identically.
- **Reference file boundary stated,** with a note that `v0.1` is the pack's own version string and is separate from the repository version.
- **Lockstep sentence** at the head of this file now names `CITATION.cff`, which has moved with the README since v1.1.3.
- Masthead, How to Cite and `CITATION.cff` move to this release in lockstep. `LICENSE.md` is unchanged byte for byte.

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
