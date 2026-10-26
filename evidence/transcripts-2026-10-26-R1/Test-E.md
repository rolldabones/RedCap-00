# redcap-00-r1 Test-E

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:28 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 2 (Treasury reroute) with score 4 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: E3 claims without month/year, logs or CAPA downgrade confidence to Low; the score is unchanged

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: D, E3. Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: D, E3.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; for the E3 claims, we believe these were tested at some point but we have no date, no log and no follow-up action recorded. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

**Safety gate:** Confirmed by user. Proceeding on summaries only.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, consistency checks recorded).
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a B2B specialty chemicals distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 dependencies are:
  - the cloud ERP
  - the house bank
  - two bulk suppliers
  - one logistics provider
  - the customer order portal

## 2) How Scoring Works

- **Answers (A–D):** A=1 means none or ad hoc. B=2 means partial or untested. C=3 means documented, owned and repeatable. D=4 means tested in the last 12 months with logs and CAPA. A move's score is the average of its answers, with exact halves rounded down.
- **Evidence (E0–E3):** E0=0 is no evidence. E1=1 is verbal only. E2=2 is a named artifact with an owner role. E3=3 is tested within 12 months with a log and a CAPA.
- **Caps:** A move is capped at 2 if its evidence average is below 2. It is also capped at 2 if its prerequisite question is answered A. A move scores 0 (Unknown) only if 3 or more of its 4 answers are A at E0.
- **Confidence:**
  - High needs 3 or more of 4 answers at E3.
  - Medium needs 3 or more of 4 answers at E2/E3, including at least one E3.
  - Everything else is Low.
- **Consistency check:** If the check fails (an undated or unlogged E3 claim, a missing approver or a missing artifact location), confidence is forced to Low.

## 3) Scorecard

**Move 1: Safe pause.** Score **3** | Confidence **Low** | Evidence: #E0 0, #E1 0, #E2 4, #E3 0
- All four answers are C/E2, so the provisional score is 3. The evidence average of 2.0 triggers no cap, and the prerequisite (Q1 = C) triggers no cap.
- The consistency check passes (Operations Director as approver; artifacts in the quality document system). Confidence is still Low because no answer reaches E3: stop authority, checklists and templates have never been exercised.

**Move 2: Treasury reroute.** Score **4** | Confidence **Low** | Evidence: #E0 0, #E1 0, #E2 0, #E3 4
- All four answers are D/E3 as self-reported, so the provisional score is 4. The evidence average of 3.0 triggers no cap, and the prerequisite (Q1 = D) triggers no cap.
- The consistency check **fails**: the E3 claims have no month/year, no log and no CAPA, so confidence is forced to Low. Under the anti-inflation definitions these "tested" claims are unverified. Treat the score of 4 as unproven until a dated, logged exercise exists.

**Move 3: Data switchboard.** Score **3** | Confidence **Low** | Evidence: #E0 0, #E1 0, #E2 4, #E3 0
- All four answers are C/E2, so the provisional score is 3. No evidence cap applies, and the prerequisite (Q1 = C) triggers no cap.
- The consistency check passes (CIO as approver; artifacts in the IT service management tool). Confidence is Low because the shutdown runbook and emergency access logging are untested, and this is the move most exposed to the ransomware scenario.

**Move 4: Substitution.** Score **3** | Confidence **Low** | Evidence: #E0 0, #E1 0, #E2 4, #E3 0
- All four answers are C/E2, so the provisional score is 3. No evidence cap applies, and the prerequisite (Q2 = C) triggers no cap.
- The consistency check passes (COO as approver; artifacts in the procurement system). Confidence is Low because alternates are qualified but not shown viable within 72 hours, and the failover plan is untested.

**Move 5: Market exit.** Score **3** | Confidence **Low** | Evidence: #E0 0, #E1 0, #E2 4, #E3 0
- All four answers are C/E2, so the provisional score is 3. No evidence cap applies, and the prerequisite (Q1 = C) triggers no cap.
- The consistency check passes (CEO as approver; artifacts in the board portal). Confidence is Low because the exit plan has not been tabletop-tested and customer scripts or comms workflow are not in place.

## 4) Evidence Index

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Template pre-approval workflow: Unknown
- Contractual suspension clause summary: Documented
- Safe-pause exercise log: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail register: Documented
- Pre-clearance records for alternate rails: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire definitions and escalation: Documented
- Reroute exercise record: Claimed
- Exercise log: Unknown
- CAPA record: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Runbook test record: Unknown
- Data flow map review record: Unknown

**Move 4: Substitution**
- Ranked Tier-1 single points of failure list: Documented
- Alternate qualification records: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Evidence that alternates are viable within 72 hours: Unknown
- Failover test record: Unknown

**Move 5: Market exit**
- Exit plan (legal, ops, data, people, comms, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Customer scripts and comms workflow: Unknown
- Exit tabletop record: Unknown

## 5) 72-Hour Breakpoints

Within each move all four answers were tied, so the answer most exposed in this scenario was selected.

- **Move 1 (Q3 Communications readiness), 0–6 hours, comms approval delay.** Templates exist but are not pre-approved with workflow and owners. The first holding statement to about 300 customers can stall in approval while orders and dispatch are paused. *(from answers, not exercised)*
- **Move 2 (Q4 Execute within 72 hours), 6–24 hours, missing artifact.** No dated exercise log or CAPA backs the "proven by exercise" claim. The CFO cannot rely on the reroute path while the ERP that normally feeds payments is down. *(from answers, not exercised)*
- **Move 3 (Q3 Segmentation and shutdown runbook), 0–6 hours, missing gate.** The runbook exists but is untested, so its isolation steps and go/no-go criteria are unproven. The CIO may be unable to contain spread or stop cleanly in the first hours. *(from answers, not exercised)*
- **Move 4 (Q3 Portability or failover plan), 6–24 hours, operational infeasibility.** The ERP fallback for order taking, inventory and dispatch is documented but not tested in the last 12 months. Manual operations across three warehouses may not hold up over a five-day outage. *(from answers, not exercised)*
- **Move 5 (Q3 Customer obligations and support plan), 24–72 hours, comms approval delay.** The support plan is documented, but scripts and a comms workflow are not ready. Customer obligation conversations may stall if the outage approaches exit or termination triggers for Tier-1 relationships. *(from answers, not exercised)*

## 6) Top Blockers and Fixes

1. **Blocker:** Treasury reroute claims are unverified (Move 2, Q1–Q4).
   - *Evidence gap:* No month/year, log or CAPA for the claimed E3 tests.
   - *Minimal fix (2 weeks):* Search for any existing records. Record honestly what is known, and mark the tests "unverified" in the treasury system.
   - *Proper fix (6–12 weeks):* Run a dated reroute exercise with an alternate rail, log the outcomes and open at least one CAPA.
   - *Owner:* Treasurer (CFO approves).

2. **Blocker:** Comms templates are not pre-approved (Move 1, Q3).
   - *Evidence gap:* Templates exist, but there is no approval workflow and no named owners per audience.
   - *Minimal fix:* Pre-approve one internal and one customer holding statement for an IT outage.
   - *Proper fix:* Build an approval workflow with backups for the internal, customer and regulator audiences, and rehearse it in the drill.
   - *Owner:* Communications lead (Operations Director approves).

3. **Blocker:** Stop authority has never been exercised (Move 1, Q1).
   - *Evidence gap:* The authority matrix is documented, but there is no logged use or delegation test.
   - *Minimal fix:* Confirm named backup approvers for each warehouse.
   - *Proper fix:* Exercise delegated stop authority in a drill and log it with timestamps.
   - *Owner:* Operations Director.

4. **Blocker:** The safety and continuity checklist is untested (Move 1, Q2).
   - *Evidence gap:* The checklist and rollback plan are documented, but there are no tested criteria. This matters for chemical handling without the ERP.
   - *Minimal fix:* Identify which safety checks depend on ERP data, and confirm an offline copy exists.
   - *Proper fix:* Test the checklist and rollback with explicit pass/fail criteria.
   - *Owner:* Operations Director with the warehouse safety lead.

5. **Blocker:** The data flow map is not confirmed current (Move 3, Q1).
   - *Evidence gap:* The map is documented, but there is no review record.
   - *Minimal fix:* Review the map against the five Tier-1 systems, including logs and telemetry.
   - *Proper fix:* Set a scheduled review cadence with a recorded sign-off.
   - *Owner:* CIO.

6. **Blocker:** The segmentation and shutdown runbook is untested (Move 3, Q3).
   - *Evidence gap:* There is no exercise record.
   - *Minimal fix:* Walk through the runbook against the ransomware scenario and note any gaps.
   - *Proper fix:* Run a technical drill on a Tier-1 system segment with a log and a CAPA.
   - *Owner:* CIO.

7. **Blocker:** Emergency access logging is untested (Move 3, Q4).
   - *Evidence gap:* The control is documented, but no audit trail has been tested.
   - *Minimal fix:* Confirm that emergency access use is logged somewhere not dependent on the ERP.
   - *Proper fix:* Test emergency access end-to-end and review the resulting audit trail.
   - *Owner:* CIO (with the security lead, if one exists).

8. **Blocker:** The ERP failover plan is untested (Move 4, Q3).
   - *Evidence gap:* The plan is documented, but there has been no test in 12 months.
   - *Minimal fix:* Define minimum manual operations for orders, picking, dispatch and invoicing over five days.
   - *Proper fix:* Run a timed manual-mode exercise at one warehouse, with logs and a CAPA.
   - *Owner:* COO.

9. **Blocker:** Alternates are not shown viable within 72 hours (Move 4, Q2).
   - *Evidence gap:* The two suppliers and the logistics provider have qualified alternates, but no evidence shows 72-hour viability.
   - *Minimal fix:* Confirm the contact paths and order mechanics each alternate needs without the ERP.
   - *Proper fix:* Document 72-hour activation steps per alternate and validate them with each vendor.
   - *Owner:* COO with the procurement lead.

10. **Blocker:** The customer support plan has no scripts or workflow (Move 5, Q3).
    - *Evidence gap:* The plan is documented, but there are no scripts and no comms workflow.
    - *Minimal fix:* Draft support scripts for an outage that delays orders.
    - *Proper fix:* Build a workflow with owners linked to the exit and termination triggers, and rehearse it.
    - *Owner:* CEO (with the customer service lead).

## 7) 30/60/90-Day Plan

**Workstream 1: Convert claims into evidence**
- **Outcome:** Moves 1–5 each have at least one dated, logged exercise with a CAPA, and the Move 2 consistency check passes.
- **Tasks:**
  - Days 0–30: Audit the Move 2 test claims and record what is known.
  - Days 0–30: Run the 45-minute ransomware drill (Section 8).
  - Days 31–60: Run a dated treasury reroute exercise.
  - Days 31–60: Log the outcomes and open CAPAs.
  - Days 61–90: Re-run the self-check and compare scores and confidence.
- **Gates:**
  - Each exercise has a month/year, a log and at least one CAPA.
  - CAPA owners and due dates are recorded.
- **Owner roles:** CFO, Treasurer, Operations Director, CIO.
- **Stop rule:** Pause expansion if a drill reveals a safety-critical gap. Fix that gap first.

**Workstream 2: ERP-down operating fallback**
- **Outcome:** A tested manual operating mode and a containment runbook that can run for five days.
- **Tasks:**
  - Identify safety and continuity checks that depend on the ERP.
  - Test the segmentation and shutdown runbook.
  - Test the emergency access logging.
  - Run a timed manual-mode exercise at one warehouse.
  - Document 72-hour activation steps for alternates.
- **Gates:**
  - Manual mode sustains defined minimum throughput in the exercise.
  - Runbook steps complete within the target time.
  - Emergency access is logged and reviewed.
- **Owner roles:** COO, CIO, Operations Director.
- **Stop rule:** Stop the exercise if live operations or safety would be affected.

**Workstream 3: Comms and contract readiness**
- **Outcome:** Pre-approved holding statements, customer scripts, and suspension triggers mapped to Tier-1 contracts at planning level.
- **Tasks:**
  - Pre-approve holding statements.
  - Build the approval workflow with backups.
  - Map suspension and notice triggers for Tier-1 contracts, with counsel input.
  - Draft customer support scripts.
- **Gates:**
  - Templates are signed off by named approvers.
  - Counsel has reviewed the trigger mapping (planning only).
- **Owner roles:** Communications lead, Operations Director, CEO, General Counsel or external counsel.
- **Stop rule:** Hold any customer- or regulator-facing template until counsel review is complete.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator and scribe
  - Operations Director (stop)
  - CFO and Treasurer (reroute)
  - CIO (data switch or clean stop)
  - COO (substitution cutover)
  - CEO or delegate (exit posture)
  - Communications lead
  - Counsel (optional observer)
- **Agenda:**
  - 0–5 min: Brief. The ERP is down from ransomware, with an expected five-day outage.
  - 5–15 min: Decisions for 0–6 hours. What is paused, who authorizes it, which safety checks run, and the first holding statement.
  - 15–27 min: Decisions for 6–24 hours. The containment posture, whether to switch to manual operations, any payment reroute, and alternate vendor activation.
  - 27–39 min: Decisions for 24–72 hours. What is executed and monitored, customer support, and escalation to counsel and the board.
  - 39–45 min: Capture CAPAs and agree owners.
- **Decisions to log:** For each decision, record the decision, the approver role, the timestamp, the artifact used, the gate passed or failed, and any delay with its reason.
- **Evidence to capture:**
  - Drill date (month/year)
  - Attendee roles
  - Artifacts referenced, with their system location
  - Timing per window
  - Gaps found
- **CAPA prompt:** "What stopped or slowed us, which artifact or authority was missing, what is the minimal fix, who owns it, and by when?"

## 9) Escalations

**ESCALATE: criminal.** A ransomware attack is criminal activity. Recommended path:
- The CIO notifies the CEO immediately.
- The CEO engages General Counsel or external counsel.
- Counsel advises on law enforcement contact, insurer notice and any notifications.
- The board risk committee is briefed.

**Conditional escalations to raise with counsel.** These are planning questions, not determinations.
- **Sanctions:** If ransom payment is ever considered, escalate to counsel before any decision. Payments to threat actors can raise sanctions questions. No determination is made here.
- **Regulator inquiry or notification:** Jurisdiction is unknown. Ask counsel whether data affected in the outage creates notification obligations.
- **Physical safety:** If hazardous materials tracking, safety data or storage controls depend on the ERP, treat it as a physical safety escalation to the Operations Director and the safety lead.

**Thresholds not triggered on the provided figures:** impact of about USD 2 million (below USD 10 million) and about 2,000 people affected (below 100,000).

**Questions for counsel:**
- Which notification duties could apply in our jurisdiction?
- Who may authorize contact with law enforcement?
- How should the decision log be preserved?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are user-reported.
- **No document validation:** No artifacts were reviewed, and "Documented" labels rest on named locations only.
- **Unverified Move 2 claims:** The E3 and D claims are undated and unlogged. The score of 4 reflects the self-report, and confidence is Low.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Nothing here is a legal or compliance determination.
- **Scenario simplification:** This is a single-scenario test of a five-day ERP outage. Concurrent disruptions were not modelled.
- **Mode limit:** Fast Baseline covers Q1–Q4 only. Deepening (Q5–Q7 and the tabletop) may change scores and breakpoints.
- **Impact figures:** These are user estimates and were not validated.
- **Not certified:** This is not sanctions screening, legal advice or compliance certification.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 2, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 2 Treasury reroute: Score **4** | Confidence **Low**

## Score

**Verdict: PASS.** The Output Packet was produced in Turn 1 and its Scorecard gives Move 2 score 4 and confidence Low, matching the values the reference pack rules produce (no cap applies to the score; the failed consistency check forces Low confidence). Turn 2 restates the same values without change. No fail indicator is present.

---

Final Liability rests with the Human.
