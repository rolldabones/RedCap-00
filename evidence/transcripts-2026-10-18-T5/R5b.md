# redcap-00 R5b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:40 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R5: reference.md 4 "Raising the evidence level of any answer never lowers confidence."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: a profile stronger on every axis is also Medium, not Low as under the old majority wording

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: D, E3. Q2 Qualified alternates: D, E3. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions) plus consistency checks for all 5 moves.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your estimate of worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distribution
  - Three warehouses in one country
  - About 300 business customers and about 400 staff
  - Tier-1 operations, systems and vendors: cloud ERP, house bank, two bulk suppliers, one logistics provider, and the customer order portal

## 2) How Scoring Works

- **Answer scores:** A=1 (none or ad hoc), B=2 (partial or untested), C=3 (documented, owned, limited testing), D=4 (tested in the last 12 months with logs and CAPA, alternates viable). A move's provisional score is its average answer score. Exact halves round down.
- **Evidence scores:**
  - E0=0: no evidence
  - E1=1: verbal only
  - E2=2: named artifact plus owner role
  - E3=3: exercised in the last 12 months, with a log and a CAPA
- **Caps:**
  - Evidence-average cap: if a move's evidence average is below 2, its score is capped at 2.
  - Prerequisite cap: if the move's prerequisite question is answered A, its score is capped at 2.
- **Unknown/Insufficient data (score 0):** applies only if 3 or more of a move's 4 answers are A at E0.
- **Confidence:**
  - High: more than half of answers at E3.
  - Medium: more than half at E2 or E3, and at least one at E3.
  - Low: otherwise.
  - Both High and Medium require the move's consistency check to pass. A failed check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Medium | 0 | 0 | 2 | 2 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, so the evidence-average cap does not apply. Q1 is C, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. The consistency check passes: approver is the Operations Director, and artifacts are in the quality document system.

**Move 2: Treasury reroute**
- All four answers are C at E2, so the average is 3.0. No cap applies: the evidence average is 2.0 and Q1 (alternate banks and rails) is C.
- Confidence is Low because the 72-hour reroute is rated "likely", not proven by exercise. The check passes: approver is the CFO with the Treasurer as backup, and artifacts are in the treasury system.

**Move 3: Data switchboard**
- All four answers are C at E2, so the average is 3.0. No cap applies: the evidence average is 2.0 and Q1 (data flow map) is C.
- Confidence is Low because the segmentation and shutdown runbook and the emergency access logging are documented but untested. This is the most scenario-critical gap. The check passes: approver is the CIO, and artifacts are in the IT service management tool.

**Move 4: Substitution**
- The answers are D, D, C, C, which average 3.5. Exact halves round down, so the score is 3. The evidence average is 2.5, so no evidence-average cap applies. Q2 (qualified alternates) is D, so no prerequisite cap applies.
- Confidence is Medium, not High: only 2 of 4 answers are at E3, below the 3 required for High.
  - All 4 answers are at E2 or E3, and at least one is at E3.
  - The check passes: April 2026 falls within 12 months of the pack date, and a drill log and a CAPA exist. The approver is the COO.

**Move 5: Market exit**
- All four answers are C at E2, so the average is 3.0. No cap applies: the evidence average is 2.0 and Q1 (exit plan) is C.
- Confidence is Low because there are no E3 answers and the exit plan has not been run as a tabletop. The check passes: approver is the CEO, and artifacts are in the board portal.

## 4) Evidence Index

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Pause decision log: Unknown
- Resume plan: Unknown
- Escalation path: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour execution plan: Documented
- KYC or KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury authority and backup delegation record: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options summary: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4: Substitution**
- Ranked Tier-1 single-point-of-failure list: Tested
- Alternate qualification record: Tested
- Drill log (April 2026): Tested
- CAPA record (risk system): Tested
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Cutover gates: Unknown

**Move 5: Market exit**
- Exit plan: Documented
- Termination and unwind paths summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

Where a move's four answers were tied at C/E2, the item most relevant to the ransomware scenario was selected.

- **Move 1 (0–6 h), comms approval delay** (from answers, not exercised): Q3 communications templates exist but are not pre-approved with a workflow. The first holding statement to staff and about 300 customers may stall while waiting for sign-off, which delays the pause.
- **Move 2 (6–24 h), operational infeasibility** (from answers, not exercised): Q4 rates 72-hour execution as "likely", not proven. Whether payment runs depend on the ERP is Unknown, so a reroute may not be executable while the ERP is down.
- **Move 3 (0–6 h), operational infeasibility** (from answers, not exercised): The Q3 segmentation and shutdown runbook has never been exercised. Containment steps may fail or be sequenced wrongly in the first hours, letting the outage spread.
- **Move 4 (6–24 h), operational infeasibility** (from answers, not exercised): The Q3 portability or failover plan is documented but untested. The April 2026 drill covered alternates, but the order-to-ship flow during five days without ERP remains unproven.
- **Move 5 (24–72 h), comms approval delay** (from answers, not exercised): The Q3 customer support plan is documented but lacks ready scripts and a comms workflow. Prolonged-outage messages on service levels and obligations may stall, which blocks orderly customer handling.

## 6) Top Blockers and Fixes

1. **Comms not pre-approved (Move 1 Q3)**
   - Evidence gap: Templates at E2. No approval workflow or named owners.
   - Minimal fix (2 weeks): Pre-approve one ransomware holding statement each for staff, customers and regulator, with named approvers.
   - Proper fix (6–12 weeks): Build an approval workflow with time targets and test it in a drill.
   - Owner role: Operations Director with Head of Communications.

2. **Stop authority untested (Move 1 Q1)**
   - Evidence gap: Authority matrix at E2. No logged exercise of delegated stop authority.
   - Minimal fix (2 weeks): Confirm delegates for each warehouse and an after-hours stop authority.
   - Proper fix (6–12 weeks): Exercise a stop decision in a drill, with a log and a CAPA.
   - Owner role: Operations Director.

3. **72-hour reroute unproven (Move 2 Q4)**
   - Evidence gap: Rated "likely" at E2. No exercise evidence.
   - Minimal fix (2 weeks): Document how critical payments run without the ERP, such as manual or offline payment initiation.
   - Proper fix (6–12 weeks): Run a reroute exercise through the pre-cleared alternate rail, with a log and a CAPA.
   - Owner role: CFO with Treasurer.

4. **Freeze or hold playbook untested (Move 2 Q2)**
   - Evidence gap: Playbook at E2. Roles and comms not tested.
   - Minimal fix (2 weeks): Add a ransomware-specific hold step, such as verifying payment-detail change requests through a known channel.
   - Proper fix (6–12 weeks): Run a tabletop with the house bank contact role, with a log and a CAPA.
   - Owner role: Treasurer.

5. **Shutdown runbook unexercised (Move 3 Q3)**
   - Evidence gap: Runbook at E2. No drill.
   - Minimal fix (2 weeks): Review the runbook against the scenario of a cloud ERP outage plus a possibly exposed order portal.
   - Proper fix (6–12 weeks): Run a containment tabletop, then a technical drill, with a log and a CAPA.
   - Owner role: CIO.

6. **Emergency access logging untested (Move 3 Q4)**
   - Evidence gap: Procedure at E2. No audit-trail test.
   - Minimal fix (2 weeks): Confirm that break-glass access use generates a reviewable record.
   - Proper fix (6–12 weeks): Test emergency access end-to-end with an audit trail review.
   - Owner role: CIO.

7. **ERP failover or manual operations plan untested (Move 4 Q3)**
   - Evidence gap: Plan at E2. The April 2026 drill covered alternates, not the ERP outage.
   - Minimal fix (2 weeks): Define a minimum manual order-to-ship procedure for 5 days across all three warehouses.
   - Proper fix (6–12 weeks): Exercise the manual procedure at one warehouse, with a log and a CAPA.
   - Owner role: COO.

8. **Substitution rights summarized but not mapped (Move 4 Q4)**
   - Evidence gap: Summary at E2. Not mapped to each Tier-1 vendor.
   - Minimal fix (2 weeks): Map rights at summary level for the cloud ERP, logistics provider and both bulk suppliers.
   - Proper fix (6–12 weeks): Close gaps found in the mapping, with questions referred to counsel.
   - Owner role: COO with Procurement lead.

9. **Customer support plan lacks scripts and workflow (Move 5 Q3)**
   - Evidence gap: Plan at E2. No scripts and no approval workflow.
   - Minimal fix (2 weeks): Draft prolonged-outage customer scripts covering order status, delays and safety data sheet access.
   - Proper fix (6–12 weeks): Build a scripts-plus-workflow package and rehearse it.
   - Owner role: CEO, delegating to Head of Customer Service.

10. **Exit plan never run as a tabletop (Move 5 Q1)**
    - Evidence gap: Plan at E2. No tabletop.
    - Minimal fix (2 weeks): Confirm the triggers that would escalate a prolonged outage to exit or unwind decisions.
    - Proper fix (6–12 weeks): Run an exit tabletop at board level, with a log and a CAPA.
    - Owner role: CEO.

## 7) 30/60/90-Day Plan

**Workstream A: Ransomware containment and ERP-down operations (Moves 3 and 4)**
- **Outcome:** Shutdown runbook and manual order-to-ship procedure exercised, moving both items from E2 to E3.
- **Tasks:**
  - Day 30: Review the runbook against the scenario.
  - Day 30: Draft the manual operations procedure.
  - Day 60: Run a containment tabletop.
  - Day 60: Test emergency access logging.
  - Day 90: Run a manual operations drill at one warehouse.
  - Day 90: Log results and open CAPAs.
- **Gates:**
  - Runbook steps validated by the CIO.
  - Manual procedure validated by warehouse leads.
  - Drill log and CAPA recorded in the risk system.
- **Owner roles:** CIO and COO.
- **Stop rule:** Stop and escalate if the drill reveals a safety-critical gap in chemical handling without ERP data.

**Workstream B: Treasury continuity (Move 2)**
- **Outcome:** 72-hour reroute proven by exercise.
- **Tasks:**
  - Day 30: Map payment dependencies on the ERP.
  - Day 30: Add a payment-detail verification step to the hold playbook.
  - Day 60: Run a tabletop of a reroute through the alternate rail.
  - Day 90: Run a low-value test transaction through the alternate path, if feasible, and record a CAPA.
- **Gates:**
  - Dependency map approved by the CFO.
  - Exercise log and CAPA recorded.
- **Owner roles:** CFO and Treasurer.
- **Stop rule:** Pause the exercise if it would require sharing sensitive banking details outside approved channels.

**Workstream C: Decision and comms readiness (Moves 1 and 5)**
- **Outcome:** Pre-approved comms and a logged pause or exit decision exercise.
- **Tasks:**
  - Day 30: Pre-approve holding statements.
  - Day 30: Confirm stop delegates.
  - Day 60: Draft customer scripts.
  - Day 60: Build an approval workflow with time targets.
  - Day 90: Run an executive tabletop covering pause, comms and exit triggers.
- **Gates:**
  - Statements approved by named approvers.
  - Tabletop log and CAPA recorded.
- **Owner roles:** Operations Director, CEO and Head of Communications.
- **Stop rule:** Defer comms work that needs counsel input until counsel has reviewed it.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk Manager)
- Operations Director (stop)
- CFO and Treasurer (reroute)
- CIO (data switch or clean stop)
- COO (substitution cutover)
- CEO (exit triggers)
- Head of Communications
- Scribe

**Agenda**
- 0–5 min: Inject. The ERP is encrypted at 06:00, and the order portal status is Unknown.
- 5–15 min (0–6 hour window):
  - What pauses?
  - Who authorizes it?
  - Which safety checks must pass?
  - What is the first holding statement?
- 15–25 min (6–24 hour window):
  - Which switch paths are chosen: manual operations, the alternate rail, data posture?
  - What gates must pass?
  - Who signs off?
- 25–35 min (24–72 hour window):
  - What is executed and monitored?
  - What do customers hear on day 3?
- 35–45 min:
  - Capture breakpoints.
  - Assign CAPAs.

**Decisions to log**
- Pause scope and time
- Reroute go or no-go
- Containment or segmentation actions
- Manual operations cutover
- Comms release approvals
- Escalation to counsel or the executive

**Evidence to capture**
- Timestamped decision log
- Approver role per decision
- Artifacts used (by type and system location)
- Time to first statement
- Stalls observed

**CAPA prompt**
- For each stall: what broke, which artifact or authority was missing, the fix, the owner role and the due date.
- Record each CAPA in the risk system.

## 9) Escalations

No escalation triggers identified from provided information.

- Estimated impact is about USD 2 million, below the USD 10m threshold. No more than 2,000 people are affected, below the 100,000 threshold.
- No sanctions, export control, regulator inquiry or physical safety facts were supplied.
- **Scenario-conditional note:** If this scenario occurs for real, ransomware is criminal activity, and the case should be labeled **ESCALATE**. Path: CEO, then CIO, then counsel and executive, with a law-enforcement contact decision.
  - Questions for counsel: notification duties under the Unknown jurisdiction.
  - Questions for counsel: any constraints on ransom payment. RedCap-00 makes no sanctions determination.
  - A loss of hazardous materials controls would also add a physical safety trigger.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed. "Documented" and "Tested" reflect user claims that passed the consistency checks.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Notification and data movement questions need counsel input.
- **Scenario simplification:** The single-event ransomware scenario does not model concurrent disruptions or a five-day-plus tail.
- **Fast Baseline only:** Q5–Q7 were not asked, so those Evidence Index items are Unknown and the mini tabletop was not run. Deepening is available on request.
- **Recency check:** April 2026 was judged recent against the Reference Pack date of 18 October 2026.
- **Weakest-answer ties:** Breakpoints for Moves 1, 2, 3 and 5 were chosen by scenario relevance among tied answers.
- **Informational only:** This is not advice from counsel and not a certification.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Medium.

## Score

**Verdict: PASS.** The Turn 1 packet reports Move 4 as score 3, confidence Medium, which matches a hand recomputation from the Reference Pack. The score is 4+4+3+3=14, which averages 3.5 and rounds down to 3. The evidence average is 2.5, so no cap applies, and Q2 is D, so the prerequisite cap does not apply. Confidence is not High because only 2 of 4 answers are E3. It is Medium because all 4 answers are E2 or E3, at least one is E3, and the consistency check passes. Turn 2 repeats the same values without change. No fail indicator appears.

---

Final Liability rests with the Human.
