# redcap-00-r1 R3b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:30 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R3: reference.md 8.2 "This is the only route to a score of 0 and the only case in which a move’s score is reported as Unknown/Insufficient data."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 1 (Safe pause) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: weak evidence short of the zero rule is capped at 2 and is not reported as Unknown

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E1. Q2 Safety and continuity checks: C, E1. Q3 Communications readiness: C, E1. Q4 Contractual suspension basis: C, E1.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: no approver named; nothing documented. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks).
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. Your estimate is about USD 2 million worst-case impact and no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers.
  - Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** Each answer maps to a pattern score: A=1 (none or ad hoc), B=2 (partial), C=3 (documented, untested) and D=4 (tested in the last 12 months with logs and CAPA). The move score is the average of its four answers, rounded with exact halves rounded down.
- **Evidence:** Evidence levels score E0=0 (none), E1=1 (verbal only), E2=2 (named artifact plus owner role) and E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Caps:** A move whose evidence average is below 2 is capped at score 2. A move whose prerequisite question is answered A is also capped at 2. The final score is the lowest that applies.
- **Confidence:** High needs more than half of answers at E3. Medium needs more than half at E2 or E3 and at least one E3. Both require a passed consistency check. Anything else is Low.
- **Unknown:** A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | Low | 0 | 4 | 0 | 0 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 2, Low**
- The provisional score is 3 (all C), but the evidence average is 1.0 (all E1), so the evidence-average cap sets the score to 2. The prerequisite (Q1) is C, so no prerequisite cap applies.
- The C answers claim documentation, but the evidence is verbal and you report "nothing documented, no approver named." The consistency check passes only because there is no E2 or E3 answer. Confidence is Low under Section 4.

**Move 2 Treasury reroute: 3, Low**
- The provisional score is 3 and the evidence average is 2.0, so no cap applies. Q1 alternate banks and rails is C (pre-cleared), so the prerequisite is met.
- The consistency check passes: the approver is the CFO with the Treasurer as backup, and the artifacts are in the treasury system. Confidence is Low because there are no E3 answers, so the reroute path has never been exercised.

**Move 3 Data switchboard: 3, Low**
- The provisional score is 3 and the evidence average is 2.0, so no cap applies. Q1 Tier-1 data flow map is C, so the prerequisite is met.
- The consistency check passes: the approver is the CIO and the artifacts are in the IT service management tool. Confidence is Low because there are no E3 answers. The shutdown runbook and emergency access logging are untested, which is critical in a ransomware scenario.

**Move 4 Substitution: 3, Low**
- The provisional score is 3 and the evidence average is 2.0, so no cap applies. Q2 qualified alternates is C, so the prerequisite is met.
- The consistency check passes: the approver is the COO and the artifacts are in the procurement system. Confidence is Low because there are no E3 answers. "Qualified" alternates are not yet shown to be viable within 72 hours, which would be a D answer.

**Move 5 Market exit: 3, Low**
- The provisional score is 3 and the evidence average is 2.0, so no cap applies. Q1 exit plan is C, so the prerequisite is met.
- The consistency check passes: the approver is the CEO and the artifacts are in the board portal. Confidence is Low because there are no E3 answers and the exit plan has no tabletop record.

## 4) Evidence Index

Q1–Q4 artifacts are labelled from your answers. Q5–Q7 themes were not asked in Fast Baseline and are labelled Unknown.

**Move 1 Safe pause**
- Stop authority matrix: Claimed
- Safety and continuity checklist with rollback plan: Claimed
- Communications templates (internal, customer, regulator): Claimed
- Contractual suspension clause summary: Claimed
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path document: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail register (pre-cleared): Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury authority and backup delegation: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution or portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gate criteria: Unknown

**Move 5 Market exit**
- Exit plan (legal, ops, data, people, comms, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

All Q1–Q4 answers within each move scored the same pattern, so each bullet uses the answer most exposed in the ERP-ransomware scenario.

- **Move 1 (Q1 stop authority, C at E1, from answers, not exercised):**
  - **Time window:** 0–6 hours.
  - **What breaks:** Missing authority.
  - **Why it blocks execution:** No named approver can authorize pausing order release and warehouse dispatch, so the first containment decisions stall or are made by whoever is present.
- **Move 2 (Q4 execute within 72 hours, C at E2, from answers, not exercised):**
  - **Time window:** 24–72 hours.
  - **What breaks:** Operational infeasibility.
  - **Why it blocks execution:** Execution is rated "likely" but has never been exercised, so payment runs that normally originate from the ERP may fail on the alternate path at first use.
- **Move 3 (Q3 shutdown runbook, C at E2, from answers, not exercised):**
  - **Time window:** 0–6 hours.
  - **What breaks:** Missing gate.
  - **Why it blocks execution:** The untested runbook has no proven isolation sequence, so segmentation of ERP-connected systems such as the order portal may be delayed or incomplete while the threat spreads.
- **Move 4 (Q2 qualified alternates, C at E2, from answers, not exercised):**
  - **Time window:** 6–24 hours.
  - **What breaks:** Missing alternate.
  - **Why it blocks execution:** The alternates are qualified but not shown to be viable within 72 hours, so manual or alternate order and dispatch paths may not be ready before customer commitments lapse.
- **Move 5 (Q2 trigger-based termination and unwind, C at E2, from answers, not exercised):**
  - **Time window:** 24–72 hours.
  - **What breaks:** Comms approval delay.
  - **Why it blocks execution:** The unwind triggers are documented but not rehearsed, so decisions to suspend or exit affected customer arrangements depend on unscheduled CEO and counsel review.

## 6) Top Blockers and Fixes

1. **Stop authority is verbal only (Move 1 Q1)**
   - **Evidence gap:** E1. No authority matrix artifact and no approver role named.
   - **Minimal fix (2 weeks):** Name the stop approver and a backup for order release, dispatch and the portal. Record this in a one-page authority matrix.
   - **Proper fix (6–12 weeks):** Embed the matrix in the incident response plan and exercise delegated authority with a logged decision.
   - **Owner role:** COO, with General Counsel.

2. **Safety and continuity checks are verbal only (Move 1 Q2)**
   - **Evidence gap:** E1. No checklist or rollback artifact. This is material for chemical handling when the ERP is down.
   - **Minimal fix (2 weeks):** Write a pause checklist covering offline access to inventory, storage and hazard data, plus a rollback step.
   - **Proper fix (6–12 weeks):** Test the checklist at one warehouse with criteria, a log and a CAPA.
   - **Owner role:** EHS Lead, with Warehouse Operations Manager.

3. **Communications readiness is verbal only (Move 1 Q3)**
   - **Evidence gap:** E1. No named templates or owner.
   - **Minimal fix (2 weeks):** Draft internal, customer and regulator holding-statement templates and store them outside the ERP.
   - **Proper fix (6–12 weeks):** Pre-approve the templates with an approval workflow and named owners.
   - **Owner role:** Head of Communications, with General Counsel.

4. **Contractual suspension basis is verbal only (Move 1 Q4)**
   - **Evidence gap:** E1. No clause summary artifact.
   - **Minimal fix (2 weeks):** Produce a planning-level summary of suspension and force-majeure positions for the top customer and supplier contracts. Counsel should review it.
   - **Proper fix (6–12 weeks):** Map triggers and notice steps to all Tier-1 contracts.
   - **Owner role:** General Counsel.

5. **Shutdown and segmentation runbook is untested (Move 3 Q3)**
   - **Evidence gap:** E2 with no exercise log or CAPA.
   - **Minimal fix (2 weeks):** Run a walkthrough of the isolation steps for the ERP and portal, and log gaps.
   - **Proper fix (6–12 weeks):** Run a technical drill in a non-production environment with a logged outcome and CAPA.
   - **Owner role:** CIO, with the IT Security Lead.

6. **Privileged and emergency access logging is untested (Move 3 Q4)**
   - **Evidence gap:** E2 with no audit-trail test.
   - **Minimal fix (2 weeks):** Confirm that emergency access logs are retained outside the ERP environment.
   - **Proper fix (6–12 weeks):** Test emergency access with audit-trail review and a CAPA.
   - **Owner role:** IT Security Lead.

7. **Treasury reroute is unproven within 72 hours (Move 2 Q1 and Q4)**
   - **Evidence gap:** E2. The pre-cleared alternate path has never been exercised.
   - **Minimal fix (2 weeks):** Confirm the payment initiation path that does not depend on the ERP, and list the steps and approvers.
   - **Proper fix (6–12 weeks):** Run a low-value reroute test with evidence, a log and a CAPA.
   - **Owner role:** CFO, with the Treasurer.

8. **ERP failover and portability plan is untested (Move 4 Q3)**
   - **Evidence gap:** E2 with no test in the last 12 months.
   - **Minimal fix (2 weeks):** Verify that backup isolation and restore steps are documented and that recovery time objectives are stated.
   - **Proper fix (6–12 weeks):** Run a restore test against the five-day scenario and record the CAPA.
   - **Owner role:** CIO.

9. **Qualified alternates are not proven viable within 72 hours (Move 4 Q2)**
   - **Evidence gap:** E2. The register exists, but 72-hour viability is not shown.
   - **Minimal fix (2 weeks):** Confirm that the manual order-to-dispatch fallback and the backup logistics contact can activate within 72 hours.
   - **Proper fix (6–12 weeks):** Exercise the fallback with one supplier and the logistics provider and log the outcomes.
   - **Owner role:** COO, with the Procurement Lead.

10. **Exit and unwind paths are not rehearsed (Move 5 Q1 and Q2)**
    - **Evidence gap:** E2 with no tabletop record.
    - **Minimal fix (2 weeks):** Confirm that the decision triggers and approvers are current in the board portal.
    - **Proper fix (6–12 weeks):** Run a tabletop of the exit plan and log a CAPA.
    - **Owner role:** CEO, with General Counsel.

## 7) 30/60/90-Day Plan

**Workstream A: Safe pause foundation (Move 1)**
- **Outcome:** Move 1 evidence rises from E1 to E2 on all four Fast Baseline questions, with a named approver.
- **Tasks:**
  - Days 0–30: Publish the stop authority matrix with a backup.
  - Days 0–30: Publish the pause checklist with offline hazard-data access.
  - Days 30–60: Store comms templates outside the ERP.
  - Days 30–60: Have counsel review the suspension clause summary.
  - Days 60–90: Test the checklist at one site.
- **Gates:**
  - An approver is named and an artifact location is recorded.
  - All four artifacts can be produced by the owner role.
- **Owner roles:** COO, EHS Lead, Head of Communications, General Counsel.
- **Stop rule:** Pause the workstream if the authority matrix is not approved by day 30. Escalate to the CEO.

**Workstream B: Ransomware containment and continuity (Moves 3 and 4)**
- **Outcome:** The shutdown runbook, emergency access logging and ERP restore are each exercised once, with a log and a CAPA.
- **Tasks:**
  - Days 0–30: Walk through the runbook and confirm backup isolation.
  - Days 30–60: Run a restore test against the five-day target.
  - Days 30–60: Review the emergency access audit trail.
  - Days 60–90: Exercise the manual order-to-dispatch fallback.
- **Gates:**
  - A restore test log exists.
  - A CAPA is opened and assigned for each gap.
  - Fallback activation is confirmed within 72 hours.
- **Owner roles:** CIO, IT Security Lead, COO, Procurement Lead.
- **Stop rule:** Halt any test that risks production systems. Resume only with a CIO-approved rollback.

**Workstream C: Evidence uplift to E3 (Moves 2 and 5, and the program overall)**
- **Outcome:** At least one E3 answer per move, which is a prerequisite for Medium confidence.
- **Tasks:**
  - Days 0–30: Set up an exercise calendar and a CAPA register.
  - Days 30–60: Run a low-value treasury reroute test.
  - Days 60–90: Run the 45-minute drill (Section 8).
  - Days 60–90: Run the exit-plan tabletop.
  - Days 60–90: Re-run the self-check.
- **Gates:**
  - Every exercise has a month/year, a log and a CAPA.
  - Re-scoring is completed within 2 weeks of the final exercise.
- **Owner roles:** CFO, Treasurer, CEO, Risk Lead.
- **Stop rule:** Do not claim E3 for any exercise that lacks a log or a CAPA.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk Lead)
- Stop approver (COO)
- CIO
- CFO or Treasurer
- EHS Lead
- Head of Communications
- General Counsel
- Scribe

**Agenda**
- **0–5 minutes:** Inject. The ERP is encrypted and the order portal is degraded.
- **5–15 minutes:** Pause decision. What stops, who authorizes it, which safety checks run and what the holding statement says.
- **15–25 minutes:** Containment. Run through the segmentation runbook and confirm backup isolation.
- **25–35 minutes:** Switch paths. Decide on the treasury reroute, manual order and dispatch, and logistics contact.
- **35–42 minutes:** Day-3 check. Decide what is monitored and whether to escalate to the board and counsel.
- **42–45 minutes:** Close and assign CAPAs.

**Decisions to log**
- The pause decision and its approver.
- Containment actions.
- The treasury path chosen.
- Fallback activation.
- The holding statement approval.
- The escalation decision.

**Evidence to capture**
- Timestamps and roles for each decision.
- Artifacts used, and artifacts found missing.
- Delays over 15 minutes and their causes.

**CAPA prompt**
- "Which decision took longest or had no owner? What single artifact or authority would remove that delay? Who owns it, and by when?"

## 9) Escalations

**ESCALATE: Criminal.** Ransomware is criminal activity. Recommended path: CEO, General Counsel and external counsel, then a board briefing. Questions for counsel:
- Should the organization engage law enforcement, and at what point?
- Does the cyber insurance policy impose notice obligations?
- Does any ransom-payment consideration raise sanctions questions? This packet makes no sanctions determination.

**ESCALATE (conditional, please confirm): Physical safety.** If hazard data, storage-compatibility data or dangerous-goods documentation depends on the ERP, an outage can affect safe handling. Recommended path: EHS Lead to COO to CEO.

**Not triggered from provided information:**
- Impact is about USD 2 million, below the USD 10 million threshold.
- People affected are at most 2,000, below the 100,000 threshold.
- No regulator inquiry was reported. Notification obligations are Unknown and should go to counsel because jurisdiction is Unknown.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed or validated.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, and no legal or compliance determination is made.
- **Scenario simplification:** A single five-day ERP outage is modeled. Concurrent data exfiltration, extortion, or supplier and bank disruption are not modeled.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run, so breakpoints come from answers, not exercises. Deepening is available on request.
- **Answer and evidence tension in Move 1:** The C answers conflict with E1 evidence and "nothing documented." The cap absorbs this, but the C answers likely overstate maturity.
- **Confidence is Low for all moves:** No E3 evidence was reported, so the scores reflect documented capability, not demonstrated execution.
- **Planning aid only:** This is informational, not legal advice, compliance certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: **2**, Low confidence.

## Score

**Verdict: PASS.** The user supplied all four Move 1 answers as C at E1. The evidence average is 1.0, which is below 2, so the cap brings the provisional score of 3 down to 2. The zero rule is not met because no answers are A at E0. No answer is at E2 or E3, so confidence is Low. The packet's Scorecard shows 2 and Low. The Turn 2 reply repeats 2 and Low. No fail indicator is present.

---

Final Liability rests with the Human.
