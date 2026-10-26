# redcap-00-r2 R5a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:42 KST · **max_tokens:** 16000

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

# RedCap-00 Optionality Self-Check: Output Packet

## 1) Snapshot

- **Jurisdiction:** Unknown. This packet makes no legal or compliance determinations. Questions for counsel are noted where relevant.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers) plus consistency checks.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days.
  - Estimated worst-case impact is about USD 2 million.
  - No more than 2,000 people are affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor.
  - It has three warehouses in one country, about 300 business customers and about 400 staff.
  - Tier-1 assets: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Pattern score (A–D):**
  - A=1 means none, unknown or ad hoc.
  - B=2 means partial or untested.
  - C=3 means documented, owned and repeatable.
  - D=4 means tested in the last 12 months with logs, CAPA and viable alternates.
  - The move score is the average of its answers, rounded, with exact halves rounding down.
- **Evidence (E0–E3):**
  - E0=0 means no evidence.
  - E1=1 means verbal only.
  - E2=2 means a named artifact with an owner role.
  - E3=3 means exercised within 12 months with a log and a CAPA.
- **Caps:**
  - A move's score is capped at 2 if its evidence average is below 2.
  - It is also capped at 2 if its prerequisite question is answered A.
  - A score of 0 (Unknown/Insufficient data) applies only if more than half of a move's answers are A at E0.
- **Confidence:**
  - **High** requires more than half of the answers at E3 and a passed consistency check.
  - **Medium** requires more than half at E2 or E3, at least one E3 and a passed check.
  - Otherwise confidence is **Low**.
- **Consistency checks** confirm the exercise date, log and CAPA for E3 answers, a named approver role and a named artifact location. If a move fails, its confidence is forced to Low.

## 3) Scorecard

| Move | Score (0–4) | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | **Medium** | 0 | 0 | 3 | 1 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (score 3, Low)**
- All four answers are C/E2, so the provisional score is 3.0. The evidence average is 2.0, so no evidence cap applies. Q1 Stop authority is C, so no prerequisite cap applies.
- Confidence is Low because there is no E3 answer. The consistency check passes: the approver is the Operations Director and artifacts are in the quality document system. Stop authority, safety checks, comms and suspension basis have not been exercised.

**Move 2: Treasury reroute (score 3, Low)**
- All four answers are C/E2, giving 3.0 with no caps. Q1 Alternate banks and rails is C (pre-cleared).
- Confidence is Low because there is no E3 answer. The check passes: the approver is the CFO, the Treasurer is backup and artifacts are in the treasury system. Q4 "Execute within 72 hours" is rated "likely," which has not been proven by exercise.

**Move 3: Data switchboard (score 3, Low)**
- All four answers are C/E2, giving 3.0 with no caps. Q1 Tier-1 data flow map is C.
- Confidence is Low because there is no E3 answer. The check passes: the approver is the CIO and artifacts are in the IT service management tool. The shutdown runbook and emergency access logging have not been tested, which matters most in a ransomware scenario.

**Move 4: Substitution (score 3, Medium)**
- The answers are C, C, C and D, giving an average of 3.25, which rounds to 3. The evidence average is 2.25, so no cap applies. Q2 Qualified alternates is C, so no prerequisite cap applies.
- Confidence is Medium because:
  - All four answers are at E2 or E3.
  - One answer is at E3 (Q4 rights mapping).
  - The check passes: an April 2026 exercise with a drill log and CAPA in the risk system, the COO as approver and artifacts in the procurement system.
- The move is not High because only 1 of 4 answers is at E3.

**Move 5: Market exit (score 3, Low)**
- All four answers are C/E2, giving 3.0 with no caps. Q1 Exit plan is C.
- Confidence is Low because there is no E3 answer. The check passes: the approver is the CEO and artifacts are in the board portal. The exit plan has not been tested in a tabletop.

## 4) Evidence Index

Labels reflect what you reported. No documents were inspected.

**Move 1: Safe pause**

| Artifact type | Label |
|---|---|
| Stop authority matrix | Documented |
| Safety/continuity checklist + rollback plan | Documented |
| Internal/customer/regulator comms templates | Documented |
| Contractual suspension clause summary | Documented |
| Decision log / audit trail | Unknown |
| Resume plan | Unknown |

**Move 2: Treasury reroute**

| Artifact type | Label |
|---|---|
| Alternate bank/rail pre-clearance record | Documented |
| Freeze/hold playbook | Documented |
| Counterparty tripwire definitions + escalation | Documented |
| 72-hour execution plan | Documented |
| KYC/KYB bundle | Unknown |
| Treasury delegation and backup register | Unknown |

**Move 3: Data switchboard**

| Artifact type | Label |
|---|---|
| Tier-1 data flow map (incl. logs/telemetry) | Documented |
| Transfer mechanism options map | Documented |
| Segmentation/localization/shutdown runbook | Documented |
| Privileged/emergency access logging procedure | Documented |
| Subprocessor list | Unknown |
| Retention/deletion (stop-cleanly) procedure | Unknown |

**Move 4: Substitution**

| Artifact type | Label |
|---|---|
| Ranked Tier-1 single-point-of-failure list | Documented |
| Qualified alternates register | Documented |
| Portability/failover plan | Documented |
| Substitution/portability rights map (Tier-1 vendors) | Tested |
| Drill log + CAPA record (April 2026) | Tested |
| Cutover governance gates | Unknown |

**Move 5: Market exit**

| Artifact type | Label |
|---|---|
| Exit plan (legal, ops, data, people, comms, support) | Documented |
| Termination/unwind path summary | Documented |
| Customer obligations and support plan | Documented |
| Data and people plan | Documented |
| Distributor/JV obligations map | Unknown |
| Regulator/customer comms workflow | Unknown |

## 5) 72-Hour Breakpoints

All answers in Moves 1, 2, 3 and 5 are tied at C/E2, and in Move 4 three are tied. The weakest answer for each move was therefore chosen as the one most exposed in the ransomware/ERP-down scenario.

- **0–6h | Move 1 | Comms approval delay (from answers, not exercised).** Q3 holding-statement templates exist but are not pre-approved with a workflow. The first internal and customer statement therefore waits on ad hoc approval while orders and deliveries stall.
- **6–24h | Move 2 | Operational infeasibility (from answers, not exercised).** Q4 execution within 72 hours is rated "likely," not proven. With the ERP down, payment files and supplier and payroll runs may have no tested manual or alternate-rail path.
- **0–6h | Move 3 | Missing gate (from answers, not exercised).** The Q3 segmentation/shutdown runbook has never been tested. Isolation decisions may be slow or incomplete, and there are no verified gates for deciding when segments are safe.
- **6–24h | Move 4 | Operational infeasibility (from answers, not exercised).** The Q3 portability/failover plan is documented but has not been tested in the last 12 months. Order, inventory and dispatch functions may not cut over to a fallback within the window.
- **24–72h | Move 5 | Comms approval delay (from answers, not exercised).** The Q3 customer obligations and support plan has no ready scripts or comms workflow. Commitments to about 300 customers on delayed or partial fulfilment cannot be issued consistently.

## 6) Top Blockers and Fixes

1. **Comms templates not pre-approved (M1 Q3)**
   - Evidence gap: E2 only; no approval workflow or tested release.
   - Minimal fix (2 weeks): Pre-approve one internal and one customer holding statement for "systems outage," and name the approvers.
   - Proper fix (6–12 weeks): Build a pre-approved template set with a sign-off workflow and exercise it in a drill.
   - Owner role: Communications Lead with Operations Director.

2. **Stop authority never exercised (M1 Q1)**
   - Evidence gap: Authority matrix documented; no logged delegation in use.
   - Minimal fix (2 weeks): Confirm the delegates and alternates for each warehouse in the matrix.
   - Proper fix (6–12 weeks): Exercise the stop decision in a drill, log it and raise a CAPA.
   - Owner role: Operations Director.

3. **Safety and continuity checklist untested (M1 Q2)**
   - Evidence gap: Checklist and rollback documented; no criteria tested.
   - Minimal fix (2 weeks): Add explicit pass/fail criteria for hazardous-goods handling when the ERP is unavailable.
   - Proper fix (6–12 weeks): Test the checklist at one warehouse and log the results.
   - Owner role: Operations Director with Health & Safety Lead.

4. **72-hour treasury execution unproven (M2 Q4)**
   - Evidence gap: E2 "likely"; no exercise.
   - Minimal fix (2 weeks): Document the manual or offline steps for critical payments when the ERP is down. No bank details go in this packet.
   - Proper fix (6–12 weeks): Run a reroute drill using test or nominal transactions, with a log and a CAPA.
   - Owner role: CFO; Treasurer as backup.

5. **Alternate rails pre-cleared but not tested (M2 Q1)**
   - Evidence gap: No evidence that the reroute path works end-to-end.
   - Minimal fix (2 weeks): Confirm the activation steps and contacts with the alternate provider.
   - Proper fix (6–12 weeks): Run a tested reroute with captured evidence.
   - Owner role: Treasurer.

6. **Shutdown and segmentation runbook untested (M3 Q3)**
   - Evidence gap: Runbook exists; no test.
   - Minimal fix (2 weeks): Walk through the runbook with the incident response team and identify unclear steps.
   - Proper fix (6–12 weeks): Run a controlled test on a non-production Tier-1 segment, with a log and a CAPA.
   - Owner role: CIO with Information Security Lead.

7. **Emergency access logging untested (M3 Q4)**
   - Evidence gap: Procedure documented; no audit trail proven.
   - Minimal fix (2 weeks): Confirm that break-glass use generates a reviewable record.
   - Proper fix (6–12 weeks): Test emergency access and review the resulting audit trail.
   - Owner role: Information Security Lead.

8. **ERP failover plan untested (M4 Q3)**
   - Evidence gap: Documented; not exercised in the last 12 months. The April 2026 drill covered rights mapping, not failover.
   - Minimal fix (2 weeks): Define a five-day manual order, inventory and dispatch fallback.
   - Proper fix (6–12 weeks): Run a failover test with the cloud ERP provider and the logistics provider.
   - Owner role: COO with CIO.

9. **Customer support plan lacks scripts and workflow (M5 Q3)**
   - Evidence gap: Plan documented; no scripts or approval flow.
   - Minimal fix (2 weeks): Draft order-delay scripts and assign an owner for customer contact.
   - Proper fix (6–12 weeks): Implement a scripted workflow and rehearse it with the customer service team.
   - Owner role: Commercial Director.

10. **Exit plan not exercised (M5 Q1)**
    - Evidence gap: E2 only; no tabletop.
    - Minimal fix (2 weeks): Confirm the owners for each exit workstream.
    - Proper fix (6–12 weeks): Run a board-level tabletop with a log and a CAPA.
    - Owner role: CEO.

## 7) 30/60/90-Day Plan

**Workstream 1: ERP-down operating continuity (Moves 1 and 4)**
- **Outcome:** The warehouses can pause safely and run a manual order and dispatch fallback for five days.
- **Tasks:**
  - Days 0–30: Add pass/fail safety criteria to the continuity checklist.
  - Days 0–30: Define the manual fallback for orders, inventory and dispatch.
  - Days 30–60: Test failover with the ERP and logistics providers.
  - Days 60–90: Exercise the stop decision, then log it and raise a CAPA.
- **Gates:**
  - Fallback signed off by the COO.
  - Failover test log and CAPA recorded in the risk system.
- **Owner roles:** COO, Operations Director, CIO.
- **Stop rule:** Pause if a test would touch production hazardous-goods operations without safety sign-off.

**Workstream 2: Treasury continuity (Move 2)**
- **Outcome:** Critical payments can be executed within 72 hours without the ERP.
- **Tasks:**
  - Document the offline payment steps.
  - Confirm activation of the alternate rails.
  - Run a reroute drill using nominal transactions.
  - Record the drill log and CAPA.
- **Gates:**
  - CFO sign-off on the procedure.
  - Drill evidence captured.
- **Owner roles:** CFO, Treasurer.
- **Stop rule:** Halt the drill if any step requires sharing credentials outside approved channels.

**Workstream 3: Cyber isolation and stakeholder comms (Moves 1, 3 and 5)**
- **Outcome:** The organization can isolate systems quickly and has pre-approved statements ready.
- **Tasks:**
  - Walk through the runbook.
  - Run a controlled segmentation test.
  - Test emergency access logging.
  - Pre-approve holding statements.
  - Draft customer scripts.
- **Gates:**
  - Runbook test logged.
  - Templates approved by named roles.
  - Counsel review of the regulator-facing templates.
- **Owner roles:** CIO, Information Security Lead, Communications Lead, Commercial Director.
- **Stop rule:** Stop if counsel review of the notification templates is outstanding.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator.
  - Decision-makers: Operations Director, CFO, CIO, COO, CEO.
  - Communications Lead, Information Security Lead and a scribe.
- **Agenda:**
  - 0–5 min: Scenario brief. Ransomware has taken the ERP down for an expected five days.
  - 5–15 min (0–6h decisions):
    - Pause and isolation calls.
    - Safety checks for chemical handling.
    - First holding statement.
  - 15–30 min (6–24h decisions):
    - Treasury path.
    - Manual fallback activation.
    - Logistics coordination.
  - 30–40 min (24–72h decisions):
    - Customer commitments.
    - What to monitor.
    - Evidence capture.
  - 40–45 min: CAPA capture and owner assignment.
- **Decisions to log:**
  - Who authorized each pause or isolation.
  - Which fallback path was chosen.
  - Which payments were prioritized.
  - Statement approval times.
  - Escalation to counsel and executives.
- **Evidence to capture:**
  - Timestamped decision log.
  - The artifacts actually used, including their location.
  - Gaps found.
  - Approval durations.
- **CAPA prompt:** "Which step took longest, depended on one person, or lacked an artifact? Assign an owner role and a due date."

## 9) Escalations

**ESCALATE (criminal):** The scenario is ransomware, which is a criminal act.
- Recommended path: CEO and CIO to engage external counsel and the incident response retainer.
- Counsel questions:
  - Is law enforcement notification required or advisable?
  - What are the cyber insurance notification duties?
  - What breach notification obligations apply, given that the jurisdiction is Unknown?

**ESCALATE (sanctions, conditional):** If any ransom payment is ever considered, it raises sanctions questions that this tool cannot assess.
- Route the decision to counsel and the board before any action. This tool provides no determination and no payment guidance.

**ESCALATE (physical safety, precautionary):** An ERP outage at specialty chemical warehouses may affect access to hazardous-goods handling and dispatch information.
- Route to the Operations Director and Health & Safety Lead. Confirm offline access to safety information.

**Financial and people thresholds:** Neither is triggered. The estimated USD 2m is below USD 10m, and 2,000 people is below 100,000.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are as you stated them.
- **No document validation:** No artifacts were inspected, and the "Documented" and "Tested" labels are unverified.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown, so legal, notification and contractual positions require counsel.
- **Scenario simplification:** This is a single scenario of a five-day ERP outage. Concurrent supplier or bank disruption was not modelled.
- **Fast Baseline only:**
  - Q5–Q7 were not asked, and the corresponding Evidence Index items are Unknown.
  - Deepening and the mini tabletop would refine the breakpoints.
- **Breakpoint selection:** Breakpoints come from answers, not exercises. Where answers tied, the weakest answer was chosen by relevance to the scenario.
- **E3 recency:** The Move 4 April 2026 exercise was treated as within 12 months, relative to the 18 October 2026 date of Reference Pack v1.2.0. It lapses after April 2027.
- **Not covered:** This packet is not legal advice, not compliance certification and not sanctions screening.
- **Impact estimates:** The USD 2m and 2,000-person figures are your estimates and were not assessed.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: score 3, confidence Medium.

## Score

**Verdict: PASS.** The pass condition needs a produced packet with Move 4 at score 3 and confidence Medium, unchanged afterward. Recomputing from the reference rules gives score 3 and Medium. The packet reports exactly these values, and the Turn 2 reply repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
