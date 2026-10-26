# redcap-00-r1 R5a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:30 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R5: reference.md 4 "Medium: not High; more than half of the answers at E2 or E3, at least one answer at E3, and the move’s consistency check passes"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: baseline profile: Medium

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: D, E3.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

**RedCap-00 Optionality Self-Check: Output Packet**
*Larkspur Chemical Supply (fictional). Informational only. Not legal advice, compliance certification or sanctions screening.*

---

### 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions) plus consistency checks.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2m, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distribution, about 400 staff.
  - Three warehouses in one country, about 300 business customers.
  - Tier-1 dependencies: cloud ERP, house bank, two bulk suppliers, one logistics provider, customer order portal.

---

### 2) How Scoring Works

- **Answers:** A–D map to 1–4 (A = none/unknown/ad hoc; B = partial/untested; C = documented, owned, repeatable; D = tested in the last 12 months with logs, CAPA and viable alternates).
- **Evidence:** E0–E3 map to 0–3 (none / verbal / documented and owned / tested, logged, with CAPA).
- **Provisional score:** The mean of the move's answer scores, rounded to the nearest whole number, with exact halves rounding down. A move scores 0 (Unknown) only if more than half its answers are A at E0.
- **Caps:**
  - If the evidence average is below 2, the move is capped at 2.
  - If the move's prerequisite question is answered A, the move is capped at 2.
  - The final score is the lower of the provisional score and any cap.
- **Confidence:**
  - High: more than half the answers at E3.
  - Medium: more than half at E2 or E3, with at least one E3.
  - Low: otherwise.
  - A failed consistency check forces Low.

---

### 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Medium | 0 | 0 | 3 | 1 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause**
- Scoring: all four answers are C, giving a pattern average of 3.00 and a provisional score of 3. The evidence average is 2.00, which is not below 2, so no evidence cap applies. Q1 (stop authority) is C, so no prerequisite cap applies.
- Confidence: Low. There are no E3 answers, and Medium requires at least one. The consistency check passes (approver: Operations Director; artifacts: quality document system).

**Move 2: Treasury reroute**
- Scoring: pattern average 3.00, giving 3. Evidence average 2.00, so no cap. Q1 (alternate banks and rails) is C ("pre-cleared"), so no prerequisite cap.
- Confidence: Low. There is no E3 answer, and Q4 (execute within 72 hours) is "likely", not proven. The consistency check passes (approver: CFO, Treasurer as backup; artifacts: treasury system).

**Move 3: Data switchboard**
- Scoring: pattern average 3.00, giving 3. Evidence average 2.00, so no cap. Q1 (Tier-1 data flow map) is C, so no prerequisite cap.
- Confidence: Low. There is no E3 answer, and the shutdown runbook and emergency access logging are documented but not exercised. The consistency check passes (approver: CIO; artifacts: IT service management tool).

**Move 4: Substitution**
- Scoring: answers C, C, C, D give a pattern average of 3.25, which rounds to 3. The evidence average is 2.25, so no cap. Q2 (qualified alternates) is C, so no prerequisite cap.
- Confidence: Medium. All 4 answers are at E2 or E3, with one E3 (Q4, April 2026 drill with log and CAPA), and the consistency check passes (approver: COO). It is not High because only 1 of 4 answers is at E3.

**Move 5: Market exit**
- Scoring: pattern average 3.00, giving 3. Evidence average 2.00, so no cap. Q1 (exit plan) is C, so no prerequisite cap.
- Confidence: Low. There is no E3 answer, and no exit tabletop is recorded. The consistency check passes (approver: CEO; artifacts: board portal).

---

### 4) Evidence Index

Labels: E2 = Documented, E3 = Tested, not asked in Fast Baseline = Unknown, stated but no artifact = Claimed.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log / audit trail: Unknown
- Resume plan and criteria: Unknown

**Move 2: Treasury reroute**
- Alternate bank/rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Treasury delegation and backup matrix: Claimed (backup role named; artifact not assessed)

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4: Substitution**
- Tier-1 single-point-of-failure ranked list: Documented
- Qualified alternates register: Documented
- Portability / failover plan: Documented
- Substitution and portability rights map (Tier-1 vendors): Tested
- Drill log and CAPA record (April 2026): Tested
- Concentration limits: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5: Market exit**
- Exit plan (legal, ops, data, people, comms, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor/JV obligations map: Unknown
- Regulator and customer comms workflow: Unknown

---

### 5) 72-Hour Breakpoints

Each move's answers tie at C, so each bullet uses the answer most relevant to the ransomware scenario.

- **0–6h, Move 1, comms approval delay** (from answers, not exercised): Q3 templates exist but are not pre-approved with a workflow. The first holding statement to staff and about 300 customers could stall while wording is approved during an active incident.
- **0–6h, Move 3, operational infeasibility** (from answers, not exercised): Q3 shutdown and segmentation runbook is documented but untested. Containment steps may not run as written under ransomware conditions, and nothing shows the run is achievable in the first hours.
- **6–24h, Move 2, operational infeasibility** (from answers, not exercised): Q4 execution within 72 hours is rated "likely", not proven. Payment and receivables processes tied to the downed ERP may not be runnable through the pre-cleared alternate path in time.
- **6–24h, Move 4, missing alternate** (from answers, not exercised): Q3 ERP failover plan is documented but not tested. An alternate counts only if viable within 72 hours, and none is shown for order, inventory and dispatch processing.
- **24–72h, Move 5, comms approval delay** (from answers, not exercised): Q3 customer obligations plan has no ready scripts or comms workflow. Customer notices about delayed or suspended supply could lag while obligations are interpreted case by case.

---

### 6) Top Blockers and Fixes

**1. Holding statements not pre-approved (Move 1 Q3)**
- Evidence gap: E2 templates; no approval workflow, no test.
- Minimal fix (2 weeks): Pre-approve a ransomware holding statement set (staff, customer, supplier) and name approvers plus one backup each.
- Proper fix (6–12 weeks): Build an approval workflow with time targets and exercise it in a drill, with log and CAPA.
- Owner: Operations Director with the communications lead.

**2. Stop authority never exercised (Move 1 Q1)**
- Evidence gap: E2 authority matrix; no E3.
- Minimal fix: Confirm delegates for each warehouse and shift; record them in the matrix.
- Proper fix: Exercise a delegated stop decision in a tabletop and log the timestamps, role and artifacts.
- Owner: Operations Director.

**3. Safety checks and rollback not tested for ERP-down operation (Move 1 Q2)**
- Evidence gap: E2 checklist; no tested criteria.
- Minimal fix: Add manual-mode checks to the checklist:
  - offline access to hazard information
  - inventory location records
  - dispatch holds
- Proper fix: Drill manual-mode warehouse operation with pass/fail criteria, log and CAPA.
- Owner: Operations Director with the EHS lead.

**4. 72-hour treasury execution unproven (Move 2 Q4)**
- Evidence gap: "Likely" at E2; no exercise.
- Minimal fix: Walk through critical payments (payroll, suppliers, tax) without ERP data and identify the data sources still needed.
- Proper fix: Run a timed reroute exercise with a log, a CAPA and a named backup executing.
- Owner: CFO with the Treasurer.

**5. Alternate rails pre-cleared but untested (Move 2 Q1)**
- Evidence gap: E2; no test evidence.
- Minimal fix: Confirm the pre-clearance is current and record which payment types each alternate path covers.
- Proper fix: Run a controlled low-value test through the alternate path and log the result and CAPA.
- Owner: Treasurer.

**6. Shutdown and segmentation runbook untested (Move 3 Q3)**
- Evidence gap: E2 runbook; no exercise.
- Minimal fix: Run a desk check of the runbook against the current Tier-1 data flow map and fix any mismatches.
- Proper fix: Exercise the runbook on a non-production Tier-1 segment, with log and CAPA.
- Owner: CIO.

**7. Emergency access logging not tested (Move 3 Q4)**
- Evidence gap: E2 control description; no tested audit trail.
- Minimal fix: Confirm that emergency and privileged access logs are retained outside the ERP environment.
- Proper fix: Test emergency access issuance and revocation with an audit trail review, with log and CAPA.
- Owner: CIO.

**8. ERP failover not shown viable within 72 hours (Move 4 Q3)**
- Evidence gap: E2 plan; the April 2026 drill covered rights mapping, not failover.
- Minimal fix: Define the minimum viable order-to-dispatch process without ERP, including manual or alternate tooling and data sources.
- Proper fix: Test the failover or manual mode end to end within 72 hours, with log and CAPA.
- Owner: COO with the CIO.

**9. Alternates qualified but 72-hour viability unconfirmed (Move 4 Q2)**
- Evidence gap: C at E2, not D.
- Minimal fix: For the logistics provider and both bulk suppliers, record whether each alternate can be activated within 72 hours and what that requires.
- Proper fix: Confirm activation steps operationally and contractually (with counsel input) and exercise one cutover.
- Owner: COO with the procurement lead.

**10. Customer support plan lacks scripts and workflow (Move 5 Q3)**
- Evidence gap: E2 plan; no scripts, no test.
- Minimal fix: Draft supply-delay and partial-suspension customer scripts tied to the plan.
- Proper fix: Build a comms workflow with approvals and rehearse it in an exit and prolonged-outage tabletop, with log and CAPA.
- Owner: CEO with the customer service lead.

---

### 7) 30/60/90-Day Plan

**Workstream 1: Pause, safety and communications (Moves 1 and 5)**
- **Outcome:** Within 6 hours, warehouses can pause safely and approved messages reach staff and customers.
- **Tasks:**
  - Day 30: Pre-approve holding statements and name approvers and backups.
  - Day 30: Add ERP-down safety checks to the checklist.
  - Day 60: Draft customer scripts and the approval workflow.
  - Day 90: Run the Section 8 drill on Moves 1 and 5 and log outcomes and CAPA.
- **Gates:**
  - Approver and backup named for every message type.
  - Safety checklist works without ERP access.
- **Owner roles:** Operations Director, CEO, communications lead, EHS lead.
- **Stop rule:** Pause expansion if the drill shows any safety check depends on ERP data. Fix that first.

**Workstream 2: ERP-down operations and data containment (Moves 3 and 4)**
- **Outcome:** The shutdown runbook and failover (or manual) mode are shown to work within 72 hours, with an audit trail.
- **Tasks:**
  - Day 30: Desk check of the runbook against the data flow map.
  - Day 30: Confirm log retention outside the ERP environment.
  - Day 60: Define the minimum viable order-to-dispatch process and record 72-hour viability for alternates.
  - Day 90: Run a non-production runbook test and a failover or manual-mode exercise, with log and CAPA.
- **Gates:**
  - Runbook steps verified against the current map.
  - Failover completes within 72 hours in the exercise.
  - Emergency access is logged end to end.
- **Owner roles:** CIO, COO, procurement lead.
- **Stop rule:** Halt the exercise if it risks production systems. Re-scope to non-production.

**Workstream 3: Treasury continuity without ERP (Move 2)**
- **Outcome:** Critical payments can be executed through a tested alternate path within 72 hours.
- **Tasks:**
  - Day 30: Walk through critical payments and their data sources.
  - Day 60: Confirm the pre-clearance and payment-type coverage of the alternate path.
  - Day 90: Run a controlled low-value test and a timed reroute exercise, with log and CAPA.
- **Gates:**
  - Backup executor named and present at the exercise.
  - Exercise completed within the target time.
- **Owner roles:** CFO, Treasurer.
- **Stop rule:** Stop any live test that has not been signed off under bank and internal controls.

---

### 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (risk lead)
- Operations Director (pause)
- CFO or Treasurer (reroute)
- CIO (containment)
- COO (substitution)
- CEO (exit and comms decision)
- Scribe
- EHS lead (observer)

**Agenda**
- 0–5 min: Scenario brief. ERP encrypted, five-day outage expected.
- 5–15 min: 0–6h decisions. Pause scope, safety checks, holding statement, containment start.
- 15–30 min: 6–24h decisions. Treasury path, ERP failover or manual mode, supplier and logistics alternates.
- 30–40 min: 24–72h decisions. Execution, monitoring, customer notices, evidence capture.
- 40–45 min: Hotwash and CAPA assignment.

**Decisions to log**
- Each decision with its timestamp, decider role, artifact used and any gate passed or failed.

**Evidence to capture**
- Which artifacts were opened and from which system.
- Time to each approval.
- Any step that relied on ERP data.
- Backups actually used.

**CAPA prompt**
- Which decision took longest or lacked an owner or artifact?
- What single fix closes it, who owns it, and by what date?

---

### 9) Escalations

**ESCALATE.** The following triggers are identified from the scenario. No determinations are made; these are planning items for executives and counsel.

- **Criminal activity:** Ransomware is criminal extortion. Recommend a pre-agreed path to counsel and law enforcement engagement.
- **Sanctions (potential):** Any consideration of a ransom payment may raise sanctions questions. This packet does not assess or screen this; refer to counsel.
- **Physical safety:** Specialty chemical storage and dispatch while the ERP is down (inventory location, hazard information, dispatch controls) bears on physical safety. Involve the EHS lead.
- **Not triggered from the information provided:**
  - The USD 2m estimate is below the USD 10m threshold.
  - The 2,000 people affected is below the 100,000 threshold.
  - No regulator inquiry was reported.
  - No export-control facts were given.

**Recommended path:** CEO and General Counsel or external counsel, then CIO and the security lead, then EHS lead, then the board risk committee.

**Questions for counsel:**
- What incident notification duties may apply in our jurisdiction(s)?
- Which ransom-payment considerations should our sanctions review cover?
- Do any controlled-chemical obligations persist during manual operation?

---

### 10) Known Limits + Version

- **Self-report bias:** Answers and evidence levels are self-reported, and a uniform C/E2 pattern may reflect optimistic grading.
- **No document validation:** No artifact, log or CAPA was inspected.
- **Jurisdiction ambiguity:** Jurisdiction is unknown, so obligations and options could not be framed for any legal system.
- **Scenario simplification:** A single five-day ERP outage is modelled. Concurrent loss of the order portal, bank access or communications channels was not modelled.
- **Coverage:** Fast Baseline covers Q1–Q4 only. Q5–Q7 items are Unknown, and no tabletop was run.
- **Breakpoint selection:** Fast Baseline breakpoints come from answers, not exercises. Where answers tied, the most scenario-relevant one was chosen.
- **Move 4 test date:** The April 2026 test was treated as within 12 months, relative to this pack's date (October 2026). It falls outside that window after April 2027.
- **Impact figures:** The USD 2m and 2,000-people estimates are user-supplied and unverified.
- **Scope of this packet:** Not legal advice, compliance certification or sanctions screening.
- **Deepening:** Q5–Q7 and the mini tabletop are available on request.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Medium.

## Score

**Verdict: PASS.** The packet was produced and the Scorecard shows Move 4 at score 3, confidence Medium. Independent recomputation from the stated answers and evidence levels under the Reference Pack gives the same values. The Turn 2 reply repeats them without change. No fail indicator appears.

---

Final Liability rests with the Human.
