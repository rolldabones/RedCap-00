# redcap-00 R6b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:41 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R6: reference.md 3.1 "If the evidence average is below 2 (below E2), cap that move’s score at 2."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: evidence average exactly 2.0 is not below 2: no cap

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E1. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E3.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers) plus consistency checks.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - B2B specialty chemicals distribution, about 400 staff.
  - Three warehouses in one country, about 300 business customers.
  - Tier-1 dependencies: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** Each answer maps to A=1, B=2, C=3, D=4. A means none or unknown. D means tested in the last 12 months with logs and a CAPA (corrective and preventive action), viable alternates, and approvals ready.
- **Evidence:**
  - E0 (0): none.
  - E1 (1): verbal only.
  - E2 (2): named artifact plus owner role.
  - E3 (3): exercised in the last 12 months, with a log and a CAPA.
- **Provisional score:** This is the mean of a move's answers, rounded, with exact halves rounding down. A move scores 0 (Unknown/Insufficient data) only if more than half its answers are A at E0.
- **Caps:**
  - A move is capped at 2 if its evidence average is below 2.0.
  - A move is also capped at 2 if its prerequisite question is answered A.
- **Confidence:**
  - High: more than half the answers at E3, and the consistency check passes.
  - Medium: more than half at E2 or E3, at least one E3, and the check passes.
  - Low: otherwise, or whenever the consistency check fails.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Medium | 0 | 1 | 2 | 1 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is exactly 2.0. Neither cap applies, and Q1 (stop authority) is C, not A.
- Confidence is Low because there is no E3 answer, which Medium requires. The consistency check passes (approver: Operations Director; artifacts: quality document system).

**Move 2: Treasury reroute (3, Low)**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (alternate banks and rails) is C, meaning pre-cleared.
- Confidence is Low because there is no E3. Q4 answered "likely", not "proven by exercise". The consistency check passes (approver: CFO, with the Treasurer as backup; artifacts: treasury system).

**Move 3: Data switchboard (3, Low)**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (data flow map) is C.
- Confidence is Low because there is no E3. The shutdown runbook (Q3) exists but is untested, which matters most in this scenario. The consistency check passes (approver: CIO; artifacts: IT service management tool).

**Move 4: Substitution (3, Medium)**
- All four answers are C, so the mean is 3.0. The evidence average is (1+2+2+3)/4 = 2.0, which is not below 2, so no cap applies. Q2 (qualified alternates) is C, so the prerequisite cap does not apply either.
- Confidence is Medium: 3 of 4 answers are at E2 or E3, one is at E3, and the consistency check passes. The April 2026 exercise has a drill log and a CAPA in the risk system, the approver is the COO, and artifacts are in the procurement system. Q1 (single points of failure) is verbal only (E1).

**Move 5: Market exit (3, Low)**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (exit plan) is C.
- Confidence is Low because there is no E3. This move is less central to a five-day ERP outage, but its customer and unwind paths are unrehearsed. The consistency check passes (approver: CEO; artifacts: board portal).

## 4) Evidence Index

Labels are mapped from answers: E1 = Claimed, E2 = Documented, E3 = Tested. Q5–Q7 were not asked in Fast Baseline, so their artifacts are Unknown.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Conflict escalation path: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB (know-your-customer / know-your-business) bundle: Unknown
- Alternate settlement or letter-of-credit playbook: Unknown
- Treasury authority and backup delegation: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT (operational technology) and critical access boundary procedure: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4: Substitution**
- Tier-1 single-point-of-failure ranked list: Claimed
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Tested
- Exercise log and CAPA record (April 2026): Tested
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5: Market exit**
- Exit plan (counsel, ops, data, people, comms, support): Documented
- Termination and unwind paths: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

For Moves 1, 2, 3 and 5, all answers tie at C/E2. In those cases the most scenario-critical answer was selected.

- **0–6 hours | Move 1 | Comms approval delay** (Q3, C/E2: templates exist but are not pre-approved with a workflow). The first holding statement to about 300 business customers waits on drafting and approval while order and dispatch status is unknown. *(from answers, not exercised)*
- **6–24 hours | Move 2 | Operational infeasibility** (Q4, C/E2: execution within 72 hours is "likely", not proven). The reroute through pre-cleared alternate rails has never been run, so it is unverified whether payments can move without ERP-generated payment runs. *(from answers, not exercised)*
- **0–6 hours | Move 3 | Missing gate** (Q3, C/E2: shutdown and segmentation runbook exists but is untested). The containment and isolation gate sequence has never been proven, so a clean stop of ERP-connected flows may stall or be incomplete. *(from answers, not exercised)*
- **6–24 hours | Move 4 | Missing artifact** (Q1, C/E1: the single-point-of-failure ranked list is claimed verbally, with no named artifact or owner). Without an agreed priority list, the COO has no reference for which supplier, lane or system to substitute first. *(from answers, not exercised)*
- **24–72 hours | Move 5 | Missing gate** (Q2, C/E2: termination and unwind paths are documented but not rehearsed). If the outage forces exiting a customer segment or product line, untested trigger gates leave the CEO decision without a proven sequence. *(from answers, not exercised)*

## 6) Top Blockers and Fixes

1. **Single-point-of-failure list is verbal only (Move 4, Q1)**
   - Evidence gap: E1, with no named artifact or owner role.
   - Minimal fix (2 weeks): Produce a ranked list of the six Tier-1 dependencies with a named owner role. Store it in the procurement system.
   - Proper fix (6–12 weeks): Set a quarterly review cadence with triggers, linked to the alternates register and covered in the next exercise.
   - Owner role: COO, delegated to the Head of Procurement.

2. **ERP isolation and shutdown runbook is untested (Move 3, Q3)**
   - Evidence gap: E2 only, with no drill log or CAPA.
   - Minimal fix (2 weeks): Run a walkthrough tabletop of the ERP isolation steps and log the outcome plus one CAPA.
   - Proper fix (6–12 weeks): Run a technical drill on a representative segment with logged timings and gate outcomes.
   - Owner role: CIO and Head of IT Security.

3. **Runbooks may be unreachable during the outage (all moves)**
   - Evidence gap: All E2 and E3 artifacts sit in online systems (quality document system, treasury system, IT service management tool, procurement system, board portal). Whether they are available during a ransomware event is Unknown.
   - Minimal fix (2 weeks): Create out-of-band copies of the authority matrix, shutdown runbook, comms templates and failover plan.
   - Proper fix (6–12 weeks): Test retrieval under simulated outage conditions during a drill, with a recurring refresh check.
   - Owner role: CIO, with each move approver.

4. **Communications templates are not pre-approved (Move 1, Q3)**
   - Evidence gap: E2, with no approval workflow or backups.
   - Minimal fix (2 weeks): Pre-approve a holding statement for internal, customer and regulator-type audiences, and name the approver and a backup.
   - Proper fix (6–12 weeks): Build an approval workflow with time targets and exercise it in a drill.
   - Owner role: Operations Director and Head of Communications.

5. **72-hour treasury reroute is unproven (Move 2, Q4)**
   - Evidence gap: E2 ("likely"), with no exercise evidence.
   - Minimal fix (2 weeks): Do a desk walkthrough of the reroute assuming no ERP payment files, and record the gaps.
   - Proper fix (6–12 weeks): Run a controlled test through the pre-cleared alternate path with an evidence pack and CAPA.
   - Owner role: CFO, with the Treasurer.

6. **ERP failover plan is untested (Move 4, Q3)**
   - Evidence gap: E2. The April 2026 exercise covered substitution rights, not ERP failover.
   - Minimal fix (2 weeks): Confirm a manual order-to-ship fallback (orders, picking, dispatch, invoicing) for five days.
   - Proper fix (6–12 weeks): Test the failover or manual mode on one warehouse with a log and CAPA.
   - Owner role: COO and CIO.

7. **Safety and continuity checks are untested for manual operations (Move 1, Q2)**
   - Evidence gap: E2. Rollback criteria have never been exercised.
   - Minimal fix (2 weeks): Verify the checklist covers hazardous-materials handling and access to safety data sheets when ERP inventory data is unavailable.
   - Proper fix (6–12 weeks): Drill the checklist with defined criteria and logged results.
   - Owner role: Operations Director and EHS Manager.

8. **Emergency access logging is untested (Move 3, Q4)**
   - Evidence gap: E2, with no tested audit trail.
   - Minimal fix (2 weeks): Confirm the break-glass access procedure and its logging are documented and reachable out of band.
   - Proper fix (6–12 weeks): Test break-glass use and review the audit trail, with a CAPA.
   - Owner role: CIO.

9. **Suspension basis is not mapped to Tier-1 contracts (Move 1, Q4)**
   - Evidence gap: E2. A clause summary exists but has no trigger or notice mapping.
   - Minimal fix (2 weeks): Map the summary to the five Tier-1 relationships and the top customers. List open questions for counsel.
   - Proper fix (6–12 weeks): Maintain a trigger and notice matrix reviewed by counsel.
   - Owner role: General Counsel and Contracts Manager.

10. **Customer obligations and unwind paths are unrehearsed (Move 5, Q2–Q3)**
    - Evidence gap: E2, with no rehearsal.
    - Minimal fix (2 weeks): Identify which customer commitments are at risk in a five-day fulfilment gap and who decides on remedies.
    - Proper fix (6–12 weeks): Rehearse the customer support and unwind steps in a tabletop with a log and CAPA.
    - Owner role: CEO and Head of Sales.

## 7) 30/60/90-Day Plan

**Workstream A: Evidence uplift (all moves)**
- **Outcome:** Every move has at least one E3 answer by day 90, which is the precondition for Medium confidence.
- **Tasks:**
  - Day 30: Produce the single-point-of-failure list artifact (Blocker 1).
  - Day 30: Create an exercise calendar per move.
  - Day 60: Run walkthrough tabletops for Moves 1, 3 and 5.
  - Day 60: Run the treasury desk test for Move 2.
  - Day 90: Log outcomes and open CAPAs in the risk system.
- **Gates:**
  - Each exercise has a month/year, a log and a CAPA recorded.
  - Each approver confirms their artifact location.
- **Owner roles:** Head of Risk, coordinating; the five move approvers.
- **Stop rule:** Pause the workstream if an exercise surfaces a physical-safety or criminal-matter issue. Escalate per Section 9 first.

**Workstream B: ERP-outage operating fallback (Moves 1, 3, 4)**
- **Outcome:** Five days of manual operation, plus ERP isolation, are proven at one warehouse.
- **Tasks:**
  - Day 30: Create out-of-band runbook copies (Blocker 3).
  - Day 30: Verify the safety checklist (Blocker 7).
  - Day 60: Drill the shutdown runbook (Blocker 2).
  - Day 60: Test break-glass access (Blocker 8).
  - Day 90: Test manual order-to-ship at one site (Blocker 6).
- **Gates:**
  - EHS sign-off on hazardous-materials checks before any manual-mode test.
  - CIO sign-off on isolation steps.
  - COO go/no-go for the site test.
- **Owner roles:** COO, CIO, Operations Director, EHS Manager.
- **Stop rule:** Halt any test that degrades live safety controls or customer deliveries beyond the agreed threshold.

**Workstream C: Decision and comms readiness (Moves 1, 2, 5)**
- **Outcome:** Holding statements are pre-approved, and the treasury reroute and customer remedy decisions have named approvers with backups.
- **Tasks:**
  - Day 30: Pre-approve the comms templates (Blocker 4).
  - Day 30: Prepare the contract trigger mapping and questions for counsel (Blocker 9).
  - Day 60: Run the treasury reroute test (Blocker 5).
  - Day 90: Rehearse customer obligations (Blocker 10).
- **Gates:**
  - Counsel review of the trigger mapping.
  - CFO approval of the test scope.
- **Owner roles:** Operations Director, CFO, CEO, General Counsel, Head of Communications.
- **Stop rule:** Stop if the work requires sharing non-public contract text outside the approved owner group.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: Head of Risk
- Decision owners:
  - Operations Director (pause)
  - CFO, or the Treasurer as backup (reroute)
  - CIO (data switch or clean stop)
  - COO (substitution cutover)
  - CEO (exit)
- Scribe
- Observer: Internal Audit
- Optional: EHS Manager and General Counsel

**Agenda**
- **0–5 minutes:** Brief the scenario. The ERP is encrypted and expected to be unavailable for five days.
- **5–15 minutes (0–6 hour window):** What do you pause, who authorizes it, which safety checks must pass, and what is the first holding statement?
- **15–25 minutes (6–24 hour window):** Choose the switch path (payment rail, manual operations, data posture, logistics). Which gates must pass, and who signs off?
- **25–35 minutes (24–72 hour window):** What is executed, what is monitored, and what evidence is captured?
- **35–45 minutes:** Hotwash, CAPA assignment, and evidence-level updates.

**Decisions to log**
- Time of the pause decision and the approver
- Holding statement approval time
- Reroute go/no-go
- ERP isolation confirmation
- Substitution priority order
- Customer remedy approach

**Evidence to capture**
- Timestamps
- Approver roles
- Artifacts used, and whether they were reachable out of band
- Gate outcomes
- Stalls and their causes

**CAPA prompt**
"Which decision took longest or lacked an artifact? What is the minimal fix, who owns it, and what is the due date?" Record at least one CAPA per move in the risk system.

## 9) Escalations

**ESCALATE.** These triggers apply at the scenario level, meaning they come from the scenario tested rather than a live incident.

- **Criminal matter:** Ransomware is criminal activity.
  - Executive escalation: CEO and the board risk committee.
  - Counsel: engage outside counsel early.
  - Questions for counsel: law-enforcement engagement, insurer notice, and evidence preservation.
- **Physical safety:** Specialty chemicals in three warehouses are handled without ERP inventory or dispatch data.
  - Escalation: Operations Director and EHS Manager to the CEO.
  - Questions for counsel: safety-related notification duties in the applicable (Unknown) jurisdiction.
- **Sanctions (conditional):** If any ransom payment were ever contemplated, sanctions considerations may arise. No determination is made here.
  - Escalation path: CEO, CFO and outside counsel before any decision.
- **Thresholds not met:** The estimated impact (about USD 2 million; no more than 2,000 people) is below the USD 10 million and 100,000-person triggers.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed, and "Documented" or "Tested" labels reflect claims only.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown, so notification and contractual questions are framed for counsel only.
- **Scenario simplification:** A single five-day ERP outage is modelled. Concurrent impacts on the portal, house bank or logistics provider are not tested.
- **Fast Baseline only:** Q5–Q7 per move were not asked, so those artifacts are Unknown and scores rest on 4 answers per move.
- **Exercise recency assumption:** April 2026 is treated as within the last 12 months, based on the Reference Pack date of October 2026. Re-check this against today's date.
- **Possible inflation:** Uniform C/E2 answers across Moves 1, 2, 3 and 5 may mask variation. Deepening mode and the mini tabletop would test this.
- **Artifact accessibility:** Whether artifacts can be reached during a ransomware event was not assessed.
- **Not advice:** This packet is informational only. It is not legal advice, compliance certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Medium.

## Score

**Verdict: PASS.** The packet was produced in Turn 1 and reports Move 4 as score 3, confidence Medium. Recomputing from the reference pack gives the same values: an evidence average of exactly 2.0 triggers no cap, the prerequisite Q2 is C, and the Medium confidence criteria are met. Turn 2 repeats the same values without change. No fail indicator appears.

---

Final Liability rests with the Human.
