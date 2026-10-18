# redcap-00 Test-D

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:37 KST · **max_tokens:** 16000

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

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

Your safety confirmation is noted. All inputs are summaries only, so I scored as submitted.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, with consistency checks for all 5 moves).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. Your estimated worst-case impact is about USD 2m, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distribution with about 400 staff, three warehouses in one country and about 300 business customers.
  - Tier-1 assets are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

---

## 2) How Scoring Works

- **Answer scores:** A=1 (none/unknown/ad hoc), B=2 (partial/informal/untested), C=3 (documented, owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA, alternates viable).
- **Evidence scores:** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months, logged, with CAPA).
- **Move score:** The mean of the four answer scores, rounded to the nearest whole number. Exact halves round down.
  - A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Hard caps:** If a move's evidence average is below 2, its score is capped at 2. If its prerequisite question is answered A, its score is also capped at 2. The final score is the lowest result.
- **Confidence:**
  - High: 3 or more of 4 answers at E3 and the consistency check passes.
  - Medium: 3 or more at E2/E3, at least one E3, and the check passes.
  - Low: anything else, or any failed consistency check.

---

## 3) Scorecard

| Move | Score (0–4) | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** (capped) | **High** | 0 | 1 | 0 | 3 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (score 2, High confidence)**
- **Calculation:** The provisional score is (1+4+4+4)/4 = 3.25, which rounds to 3. The evidence average is 2.5, so no evidence cap applies. Q1 (stop authority) was answered A, so the prerequisite cap brings the final score to **2**.
- **Confidence and an inconsistency to resolve:**
  - Confidence is High. Three of four answers are at E3. The check passes: the April 2026 drill has a log and a CAPA in the risk system, the Operations Director is named as approver, and artifacts are in the quality document system.
  - However, Q1 says stop authority is "none or unclear" (verbal only), while the consistency check names the Operations Director as approver. That approver role is not backed by a documented authority matrix.
  - The high confidence does not lift the cap.

**Move 2: Treasury reroute (score 3, Low confidence)**
- **Calculation:** The provisional score is 3.0, which rounds to 3. The evidence average is 2.0, which is not below 2, so no cap applies. Q1 was answered C, so there is no prerequisite cap. Final score: **3**.
- **Confidence:** Low, because there are no E3 answers and Medium requires at least one. The check passes: the CFO is approver with the Treasurer as backup, and artifacts are in the treasury system. "Execute within 72 hours" is rated "likely," not proven.

**Move 3: Data switchboard (score 3, Low confidence)**
- **Calculation:** The provisional score is 3.0. The evidence average is 2.0, so no cap applies. Q1 was answered C, so there is no prerequisite cap. Final score: **3**.
- **Confidence:** Low, because there are no E3 answers. The check passes: the CIO is approver and artifacts are in the IT service management tool. The shutdown runbook is untested, and it is the core control for this ransomware scenario.

**Move 4: Substitution (score 3, Low confidence)**
- **Calculation:** The provisional score is 3.0. The evidence average is 2.0, so no cap applies. Q2 was answered C, so there is no prerequisite cap. Final score: **3**.
- **Confidence:** Low, because there are no E3 answers. The check passes: the COO is approver and artifacts are in the procurement system. The ERP failover/portability plan is documented but not exercised.

**Move 5: Market exit (score 3, Low confidence)**
- **Calculation:** The provisional score is 3.0. The evidence average is 2.0, so no cap applies. Q1 was answered C, so there is no prerequisite cap. Final score: **3**.
- **Confidence:** Low, because there are no E3 answers. The check passes: the CEO is approver and artifacts are in the board portal. The exit plan has not been run as a tabletop.

---

## 4) Evidence Index

Labels map from your evidence levels: E1 = Claimed, E2 = Documented, E3 = Tested. Artifact types for Q5–Q7 were not asked in Fast Baseline and are marked Unknown.

**Move 1: Safe pause**
- Stop authority matrix: **Claimed**
- Safety/continuity checklist with rollback plan: **Tested**
- Communications templates (internal, customer, regulator): **Tested**
- Contractual suspension trigger and notice map: **Tested**
- Decision log: **Unknown**
- Resume plan: **Unknown**
- Escalation path: **Unknown**

**Move 2: Treasury reroute**
- Alternate bank/rail pre-clearance record: **Documented**
- Freeze/hold playbook: **Documented**
- Counterparty trigger and escalation definitions: **Documented**
- 72-hour reroute execution plan: **Documented**
- KYC/KYB bundle: **Unknown**
- Alternate settlement playbook: **Unknown**
- Treasury authority and backup delegation: **Unknown**

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): **Documented**
- Transfer mechanism options map: **Documented**
- Segmentation/shutdown runbook: **Documented**
- Privileged/emergency access logging control description: **Documented**
- Subprocessor list: **Unknown**
- OT/critical access boundary procedure: **Unknown**
- Stop-cleanly retention/deletion procedure: **Unknown**

**Move 4: Substitution**
- Ranked Tier-1 single-points-of-failure list: **Documented**
- Alternate qualification records: **Documented**
- Portability/failover plan: **Documented**
- Substitution/portability rights summary: **Documented**
- Concentration limits: **Unknown**
- Logistics reroute plan: **Unknown**
- Cutover gate checklist: **Unknown**

**Move 5: Market exit**
- Exit plan: **Documented**
- Termination/unwind path summary: **Documented**
- Customer obligations and support plan: **Documented**
- Data and people plan: **Documented**
- Distributor/JV obligations map: **Unknown**
- Assets/IP handling procedure: **Unknown**
- Regulator/customer comms workflow: **Unknown**

---

## 5) 72-Hour Breakpoints

All five breakpoints are **from answers, not exercised**. Moves 2–5 have tied weakest answers (all C/E2), so the breakpoint shown for each is the one most relevant to the scenario.

- **Move 1 (0–6 hours):** Missing authority.
  - Source: Q1, stop authority, A/E1.
  - Why it blocks: Without documented authority to stop order release and shipments, the first pause decision depends on whoever is reachable, which delays containment.
- **Move 2 (6–24 hours):** Operational infeasibility.
  - Source: Q4, execute within 72 hours, C/E2 "likely."
  - Why it blocks: The reroute has never been run end-to-end, so supplier payments and customer receipts may stall while ERP-fed payment files are unavailable.
- **Move 3 (0–6 hours):** Missing gate.
  - Source: Q3, segmentation/shutdown runbook, C/E2 untested.
  - Why it blocks: An unexercised isolation runbook risks incomplete segmentation of the ERP, the order portal and connected systems in the first hours.
- **Move 4 (24–72 hours):** Missing alternate.
  - Source: Q3, portability/failover plan, C/E2 untested.
  - Why it blocks: Without a proven ERP failover or manual operating mode, warehouse picking, dispatch and invoicing cannot continue through day 5.
- **Move 5 (24–72 hours):** Comms approval delay.
  - Source: Q3, customer obligations and support plan, C/E2 without ready scripts or workflow.
  - Why it blocks: The 300 business customers may not get timely, approved updates on order commitments, which escalates contract and relationship exposure.

---

## 6) Top Blockers and Fixes

1. **Stop authority unclear (Move 1, Q1).**
   - Evidence gap: Verbal only (E1). The approver named in the check is not backed by an authority matrix.
   - Minimal fix (2 weeks): Issue a one-page stop authority matrix with primary and backup roles, signed off by the CEO.
   - Proper fix (6–12 weeks): Add the matrix to delegations of authority. Exercise it in a drill, log the decision and raise a CAPA.
   - Owner role: Operations Director.

2. **72-hour treasury reroute unproven (Move 2, Q4).**
   - Evidence gap: E2 "likely," with no exercise.
   - Minimal fix (2 weeks): Walk through the reroute steps and the payment file workarounds without the ERP.
   - Proper fix (6–12 weeks): Run a live low-value reroute test with a log and a CAPA.
   - Owner role: Treasurer.

3. **Alternate banks/rails pre-cleared but untested (Move 2, Q1).**
   - Evidence gap: No test evidence.
   - Minimal fix (2 weeks): Confirm the activation steps and lead times with the alternate provider. Record these as summaries only.
   - Proper fix (6–12 weeks): Run a test transaction through the alternate path and keep an evidence pack.
   - Owner role: CFO.

4. **Counterparty tripwires defined but not monitored (Move 2, Q3).**
   - Evidence gap: No monitoring or exercised escalation.
   - Minimal fix (2 weeks): Assign a monitoring owner and a review frequency.
   - Proper fix (6–12 weeks): Automate the trigger alerts and exercise the escalation path.
   - Owner role: Treasurer.

5. **ERP isolation/shutdown runbook untested (Move 3, Q3).**
   - Evidence gap: E2 only, with no exercise date.
   - Minimal fix (2 weeks): Run a 45-minute runbook walk-through (Section 8).
   - Proper fix (6–12 weeks): Run a technical isolation exercise in a non-production environment, with a log and a CAPA.
   - Owner role: CIO.

6. **Emergency access logging not tested (Move 3, Q4).**
   - Evidence gap: Documented, with no audit-trail test.
   - Minimal fix (2 weeks): Confirm the break-glass procedure and log retention.
   - Proper fix (6–12 weeks): Test a break-glass use and review the resulting audit trail.
   - Owner role: CIO.

7. **Data flow map documented but currency unconfirmed (Move 3, Q1).**
   - Evidence gap: No reviewed or current status.
   - Minimal fix (2 weeks): Validate the ERP, portal, bank and logistics interfaces.
   - Proper fix (6–12 weeks): Set up a scheduled review cycle with a sign-off record.
   - Owner role: CIO.

8. **ERP failover/manual operating mode untested (Move 4, Q3).**
   - Evidence gap: E2 only.
   - Minimal fix (2 weeks): Define a minimum manual mode for order intake, pick/ship and invoicing.
   - Proper fix (6–12 weeks): Run a half-day manual-mode drill at one warehouse.
   - Owner role: COO.

9. **Alternates qualified but 72-hour viability unproven (Move 4, Q2).**
   - Evidence gap: Not shown to be operationally viable within 72 hours.
   - Minimal fix (2 weeks): Confirm activation lead times for the alternate suppliers and logistics provider.
   - Proper fix (6–12 weeks): Run a contract and operational activation test for one alternate.
   - Owner role: Procurement lead.

10. **Customer support plan has no ready scripts or workflow (Move 5, Q3).**
    - Evidence gap: Documented, not exercised.
    - Minimal fix (2 weeks): Draft outage holding statements for customers. Counsel should review them before use.
    - Proper fix (6–12 weeks): Build a pre-approved comms workflow and rehearse it with an exit/unwind tabletop.
    - Owner role: Commercial Director.

---

## 7) 30/60/90-Day Plan

**Workstream 1: Decision authority (Move 1)**
- **Outcome:** Stop and resume authority is documented, delegated and exercised.
- **Tasks:**
  - Draft the authority matrix.
  - Get CEO sign-off.
  - Brief backup role holders.
  - Add the matrix to the April 2026 drill CAPA follow-up.
  - Re-exercise within 90 days.
- **Gates:**
  - Matrix signed by day 30.
  - Drill log showing the authority exercised by day 90.
- **Owner roles:** Operations Director, CEO.
- **Stop rule:** Pause if the authority matrix conflicts with existing delegations until counsel and the board secretary reconcile it.

**Workstream 2: Ransomware ERP-outage readiness (Moves 3 and 4)**
- **Outcome:** The isolation runbook, emergency access and manual operating mode are each exercised once, with logs and CAPA.
- **Tasks:**
  - Validate the data flow map.
  - Walk through the isolation runbook.
  - Test break-glass access.
  - Define a minimum manual mode.
  - Run a manual-mode drill at one warehouse.
  - Confirm alternate activation lead times.
- **Gates:**
  - Runbook walk-through log by day 30.
  - Manual-mode drill with CAPA by day 90.
- **Owner roles:** CIO, COO, Procurement lead.
- **Stop rule:** Halt any test that risks production availability or hazardous-goods handling until safety sign-off is obtained.

**Workstream 3: Treasury and customer continuity (Moves 2 and 5)**
- **Outcome:** A proven 72-hour payment reroute and an approved customer comms workflow.
- **Tasks:**
  - Do a reroute walk-through without the ERP.
  - Run a live low-value test.
  - Assign a tripwire monitoring owner.
  - Draft customer holding statements.
  - Build the approval workflow.
- **Gates:**
  - Reroute test evidence pack by day 60.
  - Comms workflow approved by day 90.
- **Owner roles:** CFO, Treasurer, Commercial Director.
- **Stop rule:** Stop and escalate to counsel if any reroute raises counterparty or sanctions questions.

---

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator.
  - Operations Director as stop authority.
  - CIO.
  - COO.
  - CFO/Treasurer.
  - Commercial Director.
  - A scribe for the log.
  - Counsel as an observer.
- **Agenda:**
  - 0–5 min: Scenario brief. The ERP is encrypted and the portal status is unknown.
  - 5–15 min: Hours 0–6. Pause decisions, isolation steps and the first holding statement.
  - 15–30 min: Hours 6–24. Payment reroute, manual mode and alternate activation.
  - 30–40 min: Hours 24–72. Execution, monitoring and customer updates.
  - 40–45 min: Capture CAPA.
- **Decisions to log:** For each decision, record who approved it, when, and against which artifact:
  - Stop order release.
  - Isolate systems.
  - Activate the alternate payment path.
  - Enter manual mode.
  - Issue customer statements.
- **Evidence to capture:**
  - Timestamps.
  - Approver roles.
  - Artifacts used (by type only).
  - Gaps found.
  - Time taken versus target for each decision.
- **CAPA prompt:** "Which decision took longest or had no clear owner? What single artifact or authority would remove that delay? Who owns it, and by what date?"

---

## 9) Escalations

**ESCALATE: criminal activity.** Ransomware is a criminal extortion scenario. Planning for it should include an executive and counsel path covering:
- Law enforcement notification.
- Insurer notification.
- Ransom-payment decision governance.

**ESCALATE (conditional): sanctions.** If ransom payment is ever contemplated, counsel must address whether the recipient could be a sanctioned party. RedCap-00 makes no sanctions determination.

**Thresholds not met:** The estimated impact of about USD 2m is below the USD 10m threshold. The estimate of 2,000 or fewer people affected is below the 100,000 threshold.

**Recommended path:** CEO → General Counsel or external counsel → CIO/security lead → board risk committee. Counsel coordinates law enforcement, insurer and any regulator contact.

**Questions for counsel and safety leads:**
- What notification obligations apply in the operating jurisdiction?
- Does the ERP outage affect hazardous-goods documentation or safety data needed for warehouse and transport operations?

---

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification and contract considerations are untested.
- **Scenario simplification:** The 5-day ERP outage is a single scenario. It does not model concurrent failures at the bank, suppliers or logistics provider.
- **Mode limits:** Fast Baseline covers only Q1–Q4. Q5–Q7 artifacts are Unknown and no tabletop was run.
- **Move 1 inconsistency:** The unclear stop authority (Q1) conflicts with the named approver. Resolve this before relying on the High confidence rating.
- **Single source of E3 evidence:** Move 1's E3 evidence rests on one April 2026 drill. Confidence will drop once that drill is more than 12 months old.
- **Impact estimate:** The impact figure (about USD 2m, up to 2,000 people) is the user's estimate and was not verified.
- **Scope of this output:** It is informational planning output only. It does not replace counsel, sanctions screening or certification of any kind.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: score **2**, confidence **High**.

## Score

**Verdict: PASS.** The expected values reproduce from the reference pack. Move 1 is capped at 2 by the Q1 = A prerequisite cap, and confidence is High because 3 of 4 answers are E3 and the consistency check passes. The Scorecard states 2 and High. The Turn 2 follow-up repeats the same values unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
