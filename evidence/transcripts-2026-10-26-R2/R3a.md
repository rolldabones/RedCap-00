# redcap-00-r2 R3a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:42 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R3: reference.md 8.2 "Set the move score to 0, reported as Unknown/Insufficient data, if and only if more than half of the move’s answers are A at E0"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 5 (Market exit) with Unknown/Insufficient data (score 0) and confidence Low, and no later turn changes either value. Expected value computed in tests.md: 3 of 4 answers at A/E0 give 0, reported as Unknown/Insufficient data

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: A, E0. Q2 Trigger-based termination and unwind paths: A, E0. Q3 Customer obligations and support plan: A, E0. Q4 Data and people plan: B, E1.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: no approver named; nothing documented.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. The user estimates worst-case impact at about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Specialty chemicals B2B distributor. Three warehouses in one country, about 300 business customers and about 400 staff. Tier-1 elements are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **A–D pattern scores:** A=1 (none, unknown, ad hoc), B=2 (partial, untested), C=3 (documented, owned, limited or no testing), D=4 (tested in the last 12 months with logs and CAPA). A move's provisional score is the mean of its answers, rounded to the nearest whole number, with exact halves rounding down.
- **E0–E3 evidence scores:**
  - E0=0 means no evidence.
  - E1=1 means verbal only.
  - E2=2 means a named artifact and owner role.
  - E3=3 means tested within 12 months, with a log and a CAPA.
- **Zero rule:** If more than half of a move's answers are A at E0, the move scores 0 and is reported as "Unknown/Insufficient data." No other route leads to a score of 0.
- **Conservative caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
- **Confidence:**
  - High requires more than half of answers at E3.
  - Medium requires more than half at E2 or E3, plus at least one E3.
  - Low applies otherwise.
  - A failed consistency check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 0 (Unknown/Insufficient data) | Low | 3 | 1 | 0 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C at E2. The pattern average is 3.0 and the evidence average is 2.0, so the evidence cap does not apply. Q1 (stop authority) is C, so the prerequisite cap does not apply either.
- The consistency check passes (approver: Operations Director; artifacts in the quality document system). Confidence is still Low because there are no E3 answers, which makes High and Medium unreachable.

**Move 2 Treasury reroute: 3, Low**
- All four answers are C at E2, giving an average of 3.0 and an evidence average of 2.0. Q1 (alternate banks and rails) is C, so neither cap applies.
- The consistency check passes (approver: CFO, with the Treasurer as backup; artifacts in the treasury system). Confidence is Low because there is no E3 answer. In particular, 72-hour execution is rated "likely," not proven by exercise.

**Move 3 Data switchboard: 3, Low**
- All four answers are C at E2, giving an average of 3.0 and an evidence average of 2.0. Q1 (data flow map) is C, so neither cap applies.
- The consistency check passes (approver: CIO; artifacts in the IT service management tool). Confidence is Low because the shutdown runbook and the emergency access logging have not been tested, so there are no E3 answers.

**Move 4 Substitution: 3, Low**
- All four answers are C at E2, giving an average of 3.0 and an evidence average of 2.0. Q2 (qualified alternates) is C, so neither cap applies.
- The consistency check passes (approver: COO; artifacts in the procurement system). Confidence is Low because there are no E3 answers. The ERP failover plan is documented but not tested.

**Move 5 Market exit: 0 (Unknown/Insufficient data), Low**
- The zero rule applies because 3 of 4 answers (Q1–Q3) are A at E0. Sections 8.1 and 8.3 are skipped for this move.
- Q4 (data and people plan) is B at E1, which is verbal only. No approver role and no artifact location were named. The check technically passes because the move has no E2 or E3 answers, but confidence is Low under Section 4 in any case.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator communication templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown (not asked in Fast Baseline)
- Resume plan: Unknown (not asked)
- Escalation path: Unknown (not asked)

**Move 2 Treasury reroute**
- Alternate bank and rail list (pre-cleared): Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire definitions and escalation: Documented
- 72-hour reroute execution assessment: Documented
- KYC/KYB bundle: Unknown (not asked)
- Letters of credit or alternate settlement playbook: Unknown (not asked)
- Treasury authority and backup matrix: Claimed (a backup role was named in the consistency check; no artifact assessed)

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging description: Documented
- Subprocessor list: Unknown (not asked)
- OT or critical access boundary procedure: Unknown (not asked)
- Stop-cleanly retention and deletion procedure: Unknown (not asked)

**Move 4 Substitution**
- Tier-1 single points of failure list (ranked): Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown (not asked)
- Logistics reroute options plan: Unknown (not asked)
- Cutover gates: Unknown (not asked)

**Move 5 Market exit**
- Exit plan covering legal, ops, data, people, comms and support: Unknown
- Termination and unwind path summary: Unknown
- Customer obligations and support plan: Unknown
- Data and people plan: Claimed
- Distributor or JV obligations map: Unknown (not asked)
- Asset and IP handling procedure: Unknown (not asked)
- Regulator and customer comms workflow: Unknown (not asked)

## 5) 72-Hour Breakpoints

- **0–6 hours | Move 1 | Comms approval delay** (from answers, not exercised; Q3 is C/E2, and all four answers tie at C/E2, so Q3 was selected as most exposed in the scenario). The templates exist but are not pre-approved with a workflow and owners. The first holding statement to 300 customers could therefore stall in approvals while orders and the portal are down.
- **0–6 hours | Move 3 | Missing gate** (from answers, not exercised; Q3 is C/E2, tied with the other three answers and selected as scenario-critical). The segmentation and shutdown runbook has never been tested. No verified containment gate exists, so the CIO cannot confirm that a clean stop of ERP-connected flows has actually been achieved.
- **6–24 hours | Move 2 | Operational infeasibility** (from answers, not exercised; Q4 is C/E2 and rated "likely" rather than proven, selected from a four-way tie). An unexercised reroute path may not be executable without ERP-sourced payment data, which would put supplier and payroll-adjacent payments at risk.
- **24–72 hours | Move 4 | Operational infeasibility** (from answers, not exercised; Q3 is C/E2, selected from a four-way tie). The ERP failover or manual workaround plan has not been tested in the last 12 months. Order-to-ship across three warehouses may not sustain a five-day outage on an unproven fallback.
- **24–72 hours | Move 5 | Missing artifact** (from answers, not exercised; Q1 is A/E0, the weakest answer). There is no exit plan and no approver role. If the outage escalates into withdrawal from a product line or customer segment, nobody has a documented path or the authority to execute it.

## 6) Top Blockers and Fixes

1. **Blocker:** No exit plan (Move 5, Q1 A/E0).
   - Evidence gap: No artifact, owner or record.
   - Minimal fix (2 weeks): Draft a one-page exit plan skeleton covering legal, ops, data, people, comms and support, with a named owner role.
   - Proper fix (6–12 weeks): Complete the documented exit plan and run a tabletop to reach E3.
   - Owner role: To be designated by the CEO; COO suggested.

2. **Blocker:** No approver role for an exit decision (Move 5).
   - Evidence gap: Approver not named; no authority artifact.
   - Minimal fix (2 weeks): Record the exit decision authority and a backup in the existing authority matrix.
   - Proper fix (6–12 weeks): Have the board ratify the delegation and exercise it in a tabletop with a logged decision.
   - Owner role: CEO with the Company Secretary function.

3. **Blocker:** Termination and unwind paths unknown (Move 5, Q2 A/E0).
   - Evidence gap: No summary exists.
   - Minimal fix (2 weeks): List Tier-1 counterparties (suppliers, logistics provider, ERP vendor, bank) with "unwind path known: yes/no."
   - Proper fix (6–12 weeks): Prepare a documented trigger-based unwind summary per Tier-1 contract, reviewed with counsel.
   - Owner role: Legal function lead.

4. **Blocker:** Customer obligations and support plan unknown (Move 5, Q3 A/E0).
   - Evidence gap: No artifact.
   - Minimal fix (2 weeks): Map obligation categories for the top customers by revenue (supply continuity, notice, support).
   - Proper fix (6–12 weeks): Document a support plan with scripts and a comms workflow.
   - Owner role: Commercial Director.

5. **Blocker:** Data and people plan exists only verbally (Move 5, Q4 B/E1).
   - Evidence gap: No named artifact or owner.
   - Minimal fix (2 weeks): Convert the verbal plan into a named document with an owner role.
   - Proper fix (6–12 weeks): Rehearse the responsibilities and steps in a tabletop.
   - Owner role: HR Director with the CIO.

6. **Blocker:** Shutdown and segmentation runbook untested (Move 3, Q3 C/E2).
   - Evidence gap: No exercise date, log or CAPA.
   - Minimal fix (2 weeks): Hold a walk-through of the runbook against the ransomware scenario and log the gaps.
   - Proper fix (6–12 weeks): Run a technical drill on a non-production segment with a log and CAPA to reach E3.
   - Owner role: CIO.

7. **Blocker:** Emergency access logging untested (Move 3, Q4 C/E2).
   - Evidence gap: No tested audit trail.
   - Minimal fix (2 weeks): Confirm that the logging description covers break-glass access during an ERP outage.
   - Proper fix (6–12 weeks): Run an emergency access drill and review the resulting audit trail.
   - Owner role: IT Security Lead.

8. **Blocker:** ERP failover or manual workaround plan untested (Move 4, Q3 C/E2).
   - Evidence gap: Not tested in the last 12 months.
   - Minimal fix (2 weeks): Hold a tabletop of a five-day manual order-to-ship process for one warehouse.
   - Proper fix (6–12 weeks): Run a timed failover exercise across all three warehouses with a log and CAPA.
   - Owner role: COO.

9. **Blocker:** 72-hour treasury reroute is "likely," not proven (Move 2, Q4 C/E2).
   - Evidence gap: No exercise evidence.
   - Minimal fix (2 weeks): Hold a desk walk-through of the pre-cleared alternate rail with the ERP assumed unavailable.
   - Proper fix (6–12 weeks): Run a controlled reroute test with a log and CAPA.
   - Owner role: Treasurer.

10. **Blocker:** Communication templates not pre-approved (Move 1, Q3 C/E2). Stop authority is documented but has not been exercised.
    - Evidence gap: No approval workflow evidence and no logged exercise.
    - Minimal fix (2 weeks): Pre-approve the ransomware holding statements (internal and customer), with any regulator template reviewed by counsel.
    - Proper fix (6–12 weeks): Build an approval workflow with owners and exercise the stop decision in a drill.
    - Owner role: Operations Director with the Communications lead.

## 7) 30/60/90-Day Plan

**Workstream A: Market exit baseline (Move 5)**
- **Outcome:** Move 5 leaves Unknown status, with an owner, an approver and documented artifacts at E2.
- **Tasks:**
  - Day 30: Name the exit approver and owner roles.
  - Day 30: Draft the exit plan skeleton.
  - Day 60: Complete the Tier-1 unwind summary and the customer obligations map.
  - Day 60: Document the data and people plan.
  - Day 90: Run a tabletop on the exit plan.
- **Gates:**
  - Approver role recorded in the authority matrix.
  - Four Q1–Q4 artifacts stored in a named system.
- **Owner roles:** COO (lead), Legal function lead, Commercial Director, HR Director.
- **Stop rule:** Pause and re-scope if the approver is not named by day 30.

**Workstream B: Ransomware and ERP outage exercise (Moves 1, 3, 4)**
- **Outcome:** At least one E3 answer each in Moves 1, 3 and 4, which supports Medium confidence on re-run.
- **Tasks:**
  - Day 30: Run the 45-minute drill in Section 8.
  - Day 60: Run a technical shutdown and segmentation drill.
  - Day 60: Run an emergency access logging test.
  - Day 90: Run a one-warehouse manual failover exercise.
  - Day 90: Open and track a CAPA for each gap found.
- **Gates:**
  - Logs exist with month/year.
  - At least one CAPA opened per exercise.
- **Owner roles:** CIO, COO, Operations Director.
- **Stop rule:** Do not run live-system tests without a rollback plan and Operations Director sign-off.

**Workstream C: Treasury and communications readiness (Moves 2, 1)**
- **Outcome:** Treasury reroute proven by exercise, and holding statements pre-approved.
- **Tasks:**
  - Day 30: Pre-approve the internal and customer holding statements.
  - Day 30: Route any regulator template to counsel.
  - Day 60: Hold a desk walk-through of the alternate rail with no ERP.
  - Day 90: Run a controlled reroute test.
  - Day 90: Exercise the CFO and Treasurer backup handover.
- **Gates:**
  - Approval workflow documented with owners.
  - Reroute test logged with a CAPA.
- **Owner roles:** CFO, Treasurer, Communications lead.
- **Stop rule:** Halt any live payment test if bank or counsel concerns are raised.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator
  - Scribe
  - Operations Director (stop authority)
  - CFO or Treasurer
  - CIO
  - COO
  - Communications lead
  - Observer from Legal
- **Agenda:**
  - 0–5 min: Brief the scenario. The ERP is encrypted and outage duration is unknown.
  - 5–15 min: Hour 0–6 decisions. What is paused, who authorizes it, which safety checks apply (including hazardous goods handling without the ERP), and what the first holding statement says.
  - 15–28 min: Hour 6–24 decisions. Which switch path is chosen for payments, ERP fallback, data posture and logistics, which gates must pass, and who signs off.
  - 28–40 min: Hour 24–72 decisions. What is executed, what is monitored, and whether an exit or withdrawal decision would be needed and who would take it.
  - 40–45 min: Capture CAPA items.
- **Decisions to log:** Stop decision, treasury reroute, data switch or clean stop, substitution cutover, and the exit decision (or the absence of an exit authority). For each, record the time, approver role and artifact used.
- **Evidence to capture:** Drill date (month/year), attendee roles, decision log, the artifacts referenced and whether each was located within 5 minutes, and stalls observed.
- **CAPA prompt:** "Which decision stalled longest, which artifact was missing or unusable, who owns the fix, and by what date?"

## 9) Escalations

**ESCALATE.** Triggers identified from the provided information:
- **Criminal:** The scenario is a ransomware attack, which is a criminal act. Planning should include when and how to engage law enforcement and external incident response, as decided by counsel.
- **Sanctions (conditional):** If the scenario's plans would ever consider a ransom payment, that raises sanctions screening questions. Questions for counsel:
  - What screening is required before any payment?
  - Who is authorized to decide?
  - What reporting expectations apply?
  - This packet makes no sanctions determination.
- **Physical safety (conditional):** Specialty chemicals distribution may depend on ERP-held hazardous goods data, safety documentation or lot traceability. Confirm that warehouse safety does not degrade during a five-day ERP outage.

**Not triggered:** Estimated impact (about USD 2 million) is below USD 10 million, and people affected (no more than 2,000) is below 100,000. No regulator inquiry was reported.

**Recommended path:** CEO and Board Risk Committee, then General Counsel or external counsel. Coordinate with the CIO or incident response lead on law enforcement engagement, and with the Operations Director or safety lead on the physical safety review.

## 10) Known Limits + Version

- **Self-report bias:** Answers and evidence levels are as stated by the user and have not been verified.
- **No document validation:** No artifacts were reviewed. "Documented" reflects claimed artifact types and owner roles only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Contractual, data transfer, regulatory and sanctions considerations require counsel in the relevant jurisdictions.
- **Scenario simplification:** A single five-day ERP outage is modeled. Concurrent supplier, bank or logistics disruption is not.
- **Fast Baseline coverage:** Only Q1–Q4 per move were assessed, and Q5–Q7 artifacts are Unknown. Deepening, including the mini tabletop, would add tabletop-derived breakpoints.
- **Breakpoints:** These come from the answers and have not been exercised. Where answers tied at C/E2, the selection reflects relevance to the scenario.
- **Scope of this output:** This is informational only. It is not legal advice, compliance certification or sanctions screening, and it does not determine whether anything is legal or compliant.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 5, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 5 Market exit: **0 (Unknown/Insufficient data)**, confidence **Low**.

## Score

**Verdict: PASS.** The user supplied three of four Move 5 answers as A at E0, so reference.md 8.2 requires a score of 0 reported as Unknown/Insufficient data. Confidence is Low because there are no E2 or E3 answers. The packet shows exactly this in the Scorecard, and the Turn 2 follow-up restates the same score and confidence without change. No fail indicator appears, so the case passes.

---

Final Liability rests with the Human.
