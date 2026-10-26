# redcap-00-r2 Test-D

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:40 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 1 (Safe pause) with score 2 and confidence High, and no later turn changes either value. Expected value computed in tests.md: stop authority unclear (Q1 A) caps Move 1 at 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: A, E1. Q2 Safety and continuity checks: D, E3. Q3 Communications readiness: D, E3. Q4 Contractual suspension basis: D, E3.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Optionality Self-Check: Output Packet

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers), plus consistency checks.
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. Your estimate of worst-case impact is about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) distributes specialty chemicals B2B. It has 3 warehouses in one country, about 300 business customers and about 400 staff. Tier-1 consists of the cloud ERP, the house bank, 2 bulk suppliers, 1 logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answer patterns:** A=1 (none, unknown, ad hoc), B=2 (partial, untested), C=3 (documented, owned, not recently tested), D=4 (tested within 12 months, with logs, CAPA and viable alternates).
- **Evidence:** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact and owner role), E3=3 (exercised within 12 months, with a log and at least one CAPA).
- **Score:** the move's provisional score is the mean of its answer scores. Exact halves round down. The move scores 0 (Unknown) only if 3 or more of its 4 answers are A at E0.
- **Caps:**
  - If the move's evidence average is below 2, its score is capped at 2.
  - If the move's prerequisite question is answered A, its score is capped at 2.
- **Confidence:**
  - High: 3 or more of 4 answers at E3, and the consistency check passes.
  - Medium: 3 or more of 4 answers at E2 or E3, at least one at E3, and the check passes.
  - Low: everything else, including any move that fails its check.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | High | 0 | 1 | 0 | 3 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (score 2, confidence High)**
- The provisional score is (1+4+4+4)/4 = 3.25, which rounds to 3. The evidence average is 2.5, so the evidence cap does not apply. Q1 Stop authority was answered A, so the prerequisite cap limits the score to **2**.
- Confidence is High because 3 of 4 answers are E3. The April 2026 drill falls within 12 months and has a log and a CAPA. An approver (Operations Director) and an artifact location (quality document system) are named, so the check passes. Checklists, comms and suspension mapping are tested, but authority to trigger the pause is verbal only. The approver named in the checks is not backed by a documented authority matrix.

**Move 2: Treasury reroute (score 3, confidence Low)**
- The provisional score is 3 and the evidence average is exactly 2.0, so no evidence cap applies. Q1 was answered C, so no prerequisite cap applies. The final score is **3**.
- The consistency check passes: the CFO is the approver, the Treasurer is the backup and artifacts are in the treasury system. Confidence is still Low because no answer is E3. Rails are pre-cleared but the reroute has never been exercised, so execution within 72 hours is only "likely."

**Move 3: Data switchboard (score 3, confidence Low)**
- The provisional score is 3, the evidence average is 2.0 and Q1 was answered C, so no caps apply. The final score is **3**.
- The check passes: the CIO is the approver and artifacts are in the ITSM tool. Confidence is Low because there is no E3 evidence. The shutdown and segmentation runbook and the emergency access logging are documented but untested. These are the controls most exposed in a ransomware scenario.

**Move 4: Substitution (score 3, confidence Low)**
- The provisional score is 3, the evidence average is 2.0 and Q2 was answered C, so no caps apply. The final score is **3**.
- The check passes: the COO is the approver and artifacts are in the procurement system. Confidence is Low because there is no E3 evidence. Alternates are qualified but not shown to be viable within 72 hours, and the ERP failover plan has not been tested in the last 12 months.

**Move 5: Market exit (score 3, confidence Low)**
- The provisional score is 3, the evidence average is 2.0 and Q1 was answered C, so no caps apply. The final score is **3**.
- The check passes: the CEO is the approver and artifacts are in the board portal. Confidence is Low because there is no E3 evidence. The exit plan has never been tabletop-tested, so the customer support and data/people steps are unproven.

## 4) Evidence Index

Labels: E1 = Claimed, E2 = Documented, E3 = Tested. Items not asked in Fast Baseline are Unknown.

**Move 1: Safe pause**
- Stop authority matrix: Claimed
- Safety/continuity checklist with rollback plan: Tested
- Internal/customer/regulator comms templates: Tested
- Contract suspension trigger and notice map: Tested
- Drill log and CAPA record: Tested
- Resume plan with gates: Unknown
- Escalation path under conflict: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail register: Documented
- Freeze/hold playbook: Documented
- Counterparty tripwire definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury delegation with backup: Claimed

**Move 3: Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options map: Documented
- Segmentation/localization/shutdown runbook: Documented
- Privileged/emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT/critical access boundary procedure: Unknown
- Retention/deletion procedure: Unknown

**Move 4: Substitution**
- Tier-1 single-point-of-failure ranked list: Documented
- Qualified alternates register: Documented
- Portability/failover plan: Documented
- Substitution/portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gate checklist: Unknown

**Move 5: Market exit**
- Exit plan: Documented
- Termination/unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor/JV obligations map: Unknown
- Assets/IP handling procedure: Unknown
- Regulator/customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

Moves 2–5 have all four answers tied at C/E2. For each of those moves, the answer most exposed to the ERP-outage scenario was selected.

- **0–6 hours | Move 1 | Missing authority (Q1 A/E1).** No documented stop authority exists, so pausing dispatch or loading of chemicals while the ERP goes down depends on whoever is reachable. That person may hesitate or be challenged, which delays a safe pause. *From answers, not exercised.*
- **6–24 hours | Move 2 | Operational infeasibility (Q4 C/E2).** The house-bank reroute has never been exercised. Without ERP-generated payment files, staff must work out manual payment and collection steps under time pressure, so supplier and payroll runs may miss cut-offs. *From answers, not exercised.*
- **0–6 hours | Move 3 | Missing gate (Q3 C/E2).** The segmentation and shutdown runbook is untested. Nobody has confirmed that isolation steps, sequencing and pass/fail gates actually contain spread to the portal and other systems, so containment may be partial or may disrupt clean systems. *From answers, not exercised.*
- **6–24 hours | Move 4 | Operational infeasibility (Q3 C/E2).** The ERP failover plan has not been tested in the last 12 months. Order capture, stock visibility and picking must run on a fallback nobody has operated, so warehouse throughput may stall. *From answers, not exercised.*
- **24–72 hours | Move 5 | Comms approval delay (Q3 C/E2).** The customer obligations and support plan is documented but unrehearsed. Commitments to about 300 customers on delayed or partial deliveries need CEO-level sign-off through an unpractised path, so customer notices may lag behind service failures. *From answers, not exercised.*

## 6) Top Blockers and Fixes

1. **Stop authority is verbal only (Move 1, Q1).**
   - Evidence gap: E1. No authority matrix artifact exists, even though the Operations Director is named as approver.
   - Minimal fix (2 weeks): Issue a one-page stop-authority matrix covering roles, deputies, scope (dispatch, loading, portal) and how to invoke it.
   - Proper fix (6–12 weeks): Formalise delegation in the quality system, then exercise it in a drill with a logged decision and CAPA.
   - Owner role: Operations Director.
2. **72-hour treasury execution unproven (Move 2, Q4).**
   - Evidence gap: E2 plan, no exercise.
   - Minimal fix: Walk through an ERP-down payment day covering priority payees, manual file preparation and dual approval.
   - Proper fix: Run a timed reroute test with the alternate rail, then log it and open CAPA.
   - Owner role: Treasurer.
3. **Alternate rails pre-cleared but untested (Move 2, Q1).**
   - Evidence gap: E2. No evidence that the rails work end to end.
   - Minimal fix: Confirm onboarding status and cut-off times with each alternate provider (summary only).
   - Proper fix: Run a low-value test transaction on each alternate rail and retain the evidence.
   - Owner role: CFO.
4. **Freeze/hold playbook and tripwires untested (Move 2, Q2–Q3).**
   - Evidence gap: E2. Roles and escalation have never been rehearsed.
   - Minimal fix: Add an ERP-outage trigger and named escalation contacts to the playbook.
   - Proper fix: Include freeze/hold decisions in a quarterly tabletop with a logged outcome.
   - Owner role: Treasurer.
5. **Shutdown and segmentation runbook untested (Move 3, Q3).**
   - Evidence gap: E2, no test.
   - Minimal fix: Run a desk-check of isolation steps against the current architecture and add explicit pass/fail gates.
   - Proper fix: Run a technical isolation exercise on a non-production segment, logged with CAPA.
   - Owner role: CIO.
6. **Emergency and privileged access logging untested (Move 3, Q4).**
   - Evidence gap: E2. No audit trail has been proven.
   - Minimal fix: Verify that break-glass access is logged somewhere outside the ERP and the identity platform likely to be affected.
   - Proper fix: Test break-glass access with an audit-trail review and record CAPA.
   - Owner role: CIO.
7. **Data flow map documented but not confirmed current (Move 3, Q1–Q2).**
   - Evidence gap: E2 rather than "current and reviewed." Transfer options have never been exercised.
   - Minimal fix: Review the map for the ERP, portal and logistics integrations, including logs and telemetry.
   - Proper fix: Set up a scheduled review cycle with sign-off. Ask counsel about transfer options once jurisdiction is known.
   - Owner role: CIO.
8. **ERP failover plan not tested within 12 months (Move 4, Q3).**
   - Evidence gap: E2.
   - Minimal fix: Define a minimum viable manual operating mode covering order intake, stock, dispatch documentation and safety data sheets.
   - Proper fix: Run a timed failover or manual-mode drill in one warehouse, logged with CAPA.
   - Owner role: COO.
9. **Alternates qualified but not proven viable within 72 hours (Move 4, Q2/Q4).**
   - Evidence gap: E2. Rights are summarised rather than mapped per vendor.
   - Minimal fix: Confirm lead time and activation steps with alternate suppliers and logistics providers.
   - Proper fix: Map substitution rights and activation runbooks for each Tier-1 vendor, then test one activation.
   - Owner role: Head of Procurement.
10. **Exit and customer plans never tabletop-tested (Move 5, Q1/Q3/Q4).**
    - Evidence gap: E2 across the board.
    - Minimal fix: Hold a 60-minute board-level walkthrough of the customer support and data/people steps.
    - Proper fix: Run a full exit tabletop with logged decisions and CAPA, and pre-approve customer scripts.
    - Owner role: CEO.

## 7) 30/60/90-Day Plan

**Workstream 1: Decision authority and safe pause**
- **Outcome:** Move 1 prerequisite cleared, raising the potential score above 2.
- **Tasks:**
  - Days 1–30: Draft the stop-authority matrix with deputies.
  - Days 1–30: Store it in the quality document system.
  - Days 31–60: Brief warehouse leads.
  - Days 31–60: Add resume criteria and an escalation path.
  - Days 61–90: Exercise the matrix in a drill.
- **Gates:**
  - Matrix approved by the CEO.
  - Drill log and CAPA recorded.
- **Owner roles:** Operations Director, Quality Manager.
- **Stop rule:** Pause the workstream if the matrix conflicts with site safety obligations until the conflict is reviewed with counsel.

**Workstream 2: ERP-down switch drills (Moves 2, 3, 4)**
- **Outcome:** Treasury, data and substitution moves each gain E3 evidence.
- **Tasks:**
  - Days 1–30: Desk-check the shutdown runbook and manual operating mode.
  - Days 31–60: Run an alternate-rail test transaction.
  - Days 31–60: Test break-glass logging.
  - Days 61–90: Run a combined drill with one warehouse in manual mode.
- **Gates:**
  - Each drill has a dated log.
  - At least one CAPA is opened per move.
- **Owner roles:** CFO, CIO, COO.
- **Stop rule:** Stop any live test that risks production data or real payments beyond the agreed test limits.

**Workstream 3: Customer, vendor and exit readiness**
- **Outcome:** Customer commitments and vendor activations are rehearsable.
- **Tasks:**
  - Days 1–30: Confirm alternate lead times.
  - Days 31–60: Map per-vendor substitution rights.
  - Days 31–60: Pre-approve customer scripts.
  - Days 61–90: Run the exit tabletop.
- **Gates:**
  - Scripts approved.
  - Tabletop log and CAPA recorded.
- **Owner roles:** CEO, Head of Procurement, Head of Customer Service.
- **Stop rule:** Stop if questions about contract interpretation arise, and route them to counsel.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (Risk Manager)
  - Operations Director
  - CFO
  - CIO
  - COO
  - Head of Customer Service
  - Scribe
- **Agenda:**
  - 0–5 min: Inject: "ERP encrypted at 06:00; portal unreachable."
  - 5–15 min: Pause decision. Who invokes it, and which safety checks apply?
  - 15–25 min: Isolation posture and manual operating mode.
  - 25–35 min: Payment day without the ERP, including alternate rail activation.
  - 35–40 min: Customer holding statement and supplier/logistics activation.
  - 40–45 min: Hotwash.
- **Decisions to log:**
  - Who authorised the pause.
  - The isolation decision.
  - The payment reroute choice.
  - Vendor activation.
  - Customer notice approval.
- **Evidence to capture:**
  - Timestamps and approver roles.
  - Artifacts referenced and any that were missing.
  - Time-to-decision for each move.
- **CAPA prompt:** "Which decision took longest or had no named owner? What single action, owner and due date closes that gap?"

## 9) Escalations

No escalation triggers identified from provided information.

The estimated impact is about USD 2 million, under USD 10 million, and no more than 2,000 people are affected, under 100,000.

If this scenario occurred for real, a ransomware incident would be a criminal matter and could raise physical safety issues for chemical handling. Either would then be an ESCALATE trigger, routed to executive leadership and counsel.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed, and labels reflect claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Ask counsel about the following:
  - Incident notification duties.
  - Contract suspension notices.
  - Data transfer options.
- **Scenario simplification:** The five-day ERP-only outage excludes concurrent bank, portal or supplier failures.
- **Fast Baseline limits:** Only Q1–Q4 per move were scored. No tabletop was run, so breakpoints are inferred.
- **Tie-breaking:** Several Move 2–5 answers were tied. Breakpoint selection there was based on scenario relevance.
- **Confidence vs score:** Move 1 shows High confidence but a capped score. Both are correct under the rules: the evidence is strong, but the prerequisite is missing.
- **Scope of this output:** It is informational only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: Score 2, Confidence High.

## Score

**Verdict: PASS.** The packet was produced in Turn 1 and shows Move 1 at score 2 with High confidence. Independent recomputation under the reference pack gives the same values. The score is capped from 3 to 2 because Q1 is A, and confidence is High because 3 of 4 answers are E3 and the consistency check passes. The Turn 2 reply repeats these values unchanged, and no fail indicator appears.

---

Final Liability rests with the Human.
