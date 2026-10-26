# redcap-00-r1 Test-D

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:28 KST · **max_tokens:** 16000

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

Deepening (Q5–Q7 per move plus the mini tabletop) is available. You selected Fast Baseline, so the packet below covers Fast Baseline only.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (20 questions plus the consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your worst-case estimate is about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a B2B specialty chemicals distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 consists of the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** Each answer maps to a number: A=1 (none, unknown or ad hoc), B=2 (partial or untested), C=3 (documented and owned, not recently tested) and D=4 (tested in the last 12 months with logs and CAPA). Each move's average is rounded, and exact halves round down.
- **Evidence:** Evidence scores are E0=0 (none), E1=1 (verbal only), E2=2 (named artifact plus owner role) and E3=3 (tested within 12 months, with log and CAPA).
- **Caps:** A move's score is capped at 2 if its evidence average is below 2. It is also capped at 2 if its prerequisite question is answered A. The final score is the lower of the average and any cap.
- **Unknown:** A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Confidence:**
  - **High:** 3 or more answers at E3 and the consistency check passes.
  - **Medium:** 3 or more answers at E2/E3, at least one E3, and the check passes.
  - **Low:** anything else, or any failed consistency check.

## 3) Scorecard

**Move 1: Safe pause** | **Score: 2** | **Confidence: High** | E0: 0 · E1: 1 · E2: 0 · E3: 3
- **Score:** The answers average 3.25, which rounds to 3. The evidence average of 2.5 triggers no evidence cap. However, Q1 Stop authority clarity is answered A, so the prerequisite cap limits the score to 2.
- **Confidence:** Three of four answers are at E3, and the check passes (April 2026 exercise with drill log and CAPA; approver and artifact location named). Note the tension: an Operations Director approver is named, yet stop authority is self-rated "none or unclear" with verbal evidence only.

**Move 2: Treasury reroute** | **Score: 3** | **Confidence: Low** | E0: 0 · E1: 0 · E2: 4 · E3: 0
- **Score:** All four answers are C (average 3.0). The evidence average of exactly 2.0 triggers no cap, and the prerequisite (Q1 Alternate banks and rails) is answered C.
- **Confidence:** There are no E3 answers, so Medium cannot be reached even though the check passes (CFO approver, Treasurer backup, treasury system location). The ability to reroute within 72 hours is self-rated "likely," not proven by exercise.

**Move 3: Data switchboard** | **Score: 3** | **Confidence: Low** | E0: 0 · E1: 0 · E2: 4 · E3: 0
- **Score:** All four answers are C (average 3.0). The evidence average of 2.0 triggers no cap, and the prerequisite (Q1 Tier-1 data flow map) is answered C.
- **Confidence:** There are no E3 answers, although the check passes (CIO approver, IT service management tool). The shutdown runbook and emergency access logging are documented but untested, which matters directly in a ransomware scenario.

**Move 4: Substitution** | **Score: 3** | **Confidence: Low** | E0: 0 · E1: 0 · E2: 4 · E3: 0
- **Score:** All four answers are C (average 3.0). The evidence average of 2.0 triggers no cap, and the prerequisite (Q2 Qualified alternates) is answered C.
- **Confidence:** There are no E3 answers, although the check passes (COO approver, procurement system). Alternates are "identified and qualified" but not confirmed viable within 72 hours, and the failover plan is untested.

**Move 5: Market exit** | **Score: 3** | **Confidence: Low** | E0: 0 · E1: 0 · E2: 4 · E3: 0
- **Score:** All four answers are C (average 3.0). The evidence average of 2.0 triggers no cap, and the prerequisite (Q1 Exit plan) is answered C.
- **Confidence:** There are no E3 answers, although the check passes (CEO approver, board portal). The exit plan and unwind paths are documented but not tested or rehearsed.

## 4) Evidence Index

**Move 1: Safe pause**

| Artifact type | Label |
|---|---|
| Stop authority matrix | Claimed |
| Safety and continuity checklist with rollback plan | Tested |
| Internal, customer and regulator communication templates | Tested |
| Contractual suspension clause map (summary) | Tested |
| Decision log | Unknown |
| Resume plan | Unknown |
| Escalation path | Unknown |

**Move 2: Treasury reroute**

| Artifact type | Label |
|---|---|
| Alternate bank and rail register | Documented |
| Freeze or hold playbook | Documented |
| Counterparty tripwire definitions | Documented |
| 72-hour reroute procedure | Documented |
| KYC/KYB bundle | Unknown |
| Alternate settlement playbook | Unknown |
| Treasury authority and backup matrix | Unknown |

**Move 3: Data switchboard**

| Artifact type | Label |
|---|---|
| Tier-1 data flow map (including logs and telemetry) | Documented |
| Transfer mechanism options summary | Documented |
| Segmentation, localization and shutdown runbook | Documented |
| Privileged and emergency access logging procedure | Documented |
| Subprocessor list | Unknown |
| OT or critical access boundary procedure | Unknown |
| Retention and deletion procedure | Unknown |

**Move 4: Substitution**

| Artifact type | Label |
|---|---|
| Ranked single-point-of-failure list | Documented |
| Qualified alternates register | Documented |
| Portability or failover plan | Documented |
| Substitution and portability rights summary | Documented |
| Concentration limits | Unknown |
| Logistics reroute plan | Unknown |
| Cutover gate checklist | Unknown |

**Move 5: Market exit**

| Artifact type | Label |
|---|---|
| Exit plan (legal, ops, data, people, comms, support) | Documented |
| Termination and unwind path summary | Documented |
| Customer obligations and support plan | Documented |
| Data and people plan | Documented |
| Distributor or JV obligations map | Unknown |
| Assets and IP handling procedure | Unknown |
| Regulator and customer comms workflow | Unknown |

## 5) 72-Hour Breakpoints

- **Move 1 (0–6 hours): missing authority.** Stop authority is "none or unclear" with verbal evidence only, so the decision to pause order release and dispatch can stall while people debate who may authorize it. *(From answers, not exercised.)*
- **Move 2 (6–24 hours): operational infeasibility.** Executing the reroute within 72 hours is rated only "likely," so moving payments off ERP-generated payment runs may fail or slip when first attempted live. *(From answers, not exercised.)*
- **Move 3 (0–6 hours): missing gate.** The segmentation and shutdown runbook is documented but untested, so isolation and clean-stop steps for the ERP and portal have no proven go/no-go checks under pressure. *(From answers, not exercised.)*
- **Move 4 (6–24 hours): missing alternate.** Alternates are qualified but not confirmed viable within 72 hours, so a manual or alternate order-to-dispatch path may not be usable inside the five-day outage. *(From answers, not exercised.)*
- **Move 5 (24–72 hours): missing gate.** Termination and unwind paths are documented but not rehearsed, so if a Tier-1 relationship must be unwound, the approval sequence is untested and may stall at CEO level. *(From answers, not exercised.)*

## 6) Top Blockers and Fixes

1. **Stop authority unclear (Move 1, Q1: A at E1)**
   - **Evidence gap:** No named authority matrix artifact, even though an Operations Director approver was named in the consistency check.
   - **Minimal fix (2 weeks):** Issue a one-page stop authority matrix naming primary and backup roles per site, and file it in the quality document system.
   - **Proper fix (6–12 weeks):** Embed delegated stop authority in the governance framework, exercise it in a drill, and log the decision with a CAPA.
   - **Owner role:** Operations Director

2. **Move 1 Tested status rests on a single April 2026 drill**
   - **Evidence gap:** E3 currency lapses in April 2027, and the drill predates any clarified stop authority.
   - **Minimal fix (2 weeks):** Confirm the April 2026 CAPA is closed and record its status in the risk system.
   - **Proper fix (6–12 weeks):** Schedule a recurring annual drill that includes the newly clarified stop authority.
   - **Owner role:** Risk Manager

3. **Alternate banks and rails pre-cleared but untested (Move 2, Q1: C at E2)**
   - **Evidence gap:** No exercise log.
   - **Minimal fix (2 weeks):** Run a walkthrough with the alternate provider confirming onboarding status and cut-off dependencies, and document the result.
   - **Proper fix (6–12 weeks):** Execute a controlled test payment on the alternate rail, log it, and open a CAPA for the gaps found.
   - **Owner role:** Treasurer

4. **72-hour treasury execution only "likely" (Move 2, Q4: C at E2)**
   - **Evidence gap:** Not proven by exercise, and dependence on the ERP for payment files is unverified.
   - **Minimal fix (2 weeks):** Document a manual or offline payment run procedure for ERP-down conditions.
   - **Proper fix (6–12 weeks):** Run a timed exercise of an ERP-down payment run with logs and a CAPA.
   - **Owner role:** CFO

5. **Freeze/hold playbook and counterparty tripwires documented, not exercised (Move 2, Q2–Q3: C at E2)**
   - **Evidence gap:** No tested roles or communications.
   - **Minimal fix (2 weeks):** Assign named roles in the playbook and add escalation contacts by role.
   - **Proper fix (6–12 weeks):** Include a freeze and tripwire inject in a tabletop, then log the outcomes and CAPA.
   - **Owner role:** Treasurer

6. **Data flow map documented but not confirmed current (Move 3, Q1: C at E2)**
   - **Evidence gap:** No review record, and logs and telemetry coverage is unverified.
   - **Minimal fix (2 weeks):** Review the map against the current Tier-1 systems (ERP, portal, bank interfaces) and record the review date.
   - **Proper fix (6–12 weeks):** Set a review cadence and assign an owner, with change triggers.
   - **Owner role:** CIO

7. **Shutdown and segmentation runbook untested (Move 3, Q3: C at E2)**
   - **Evidence gap:** No exercise date, log or CAPA.
   - **Minimal fix (2 weeks):** Run a desk-check of the runbook against the ransomware scenario and document the gaps.
   - **Proper fix (6–12 weeks):** Run a simulation on a non-production environment with logs and a CAPA.
   - **Owner role:** CIO

8. **Privileged and emergency access logging documented, not tested (Move 3, Q4: C at E2)**
   - **Evidence gap:** The audit trail has not been demonstrated.
   - **Minimal fix (2 weeks):** Confirm the location where emergency access logs are retained independently of the ERP.
   - **Proper fix (6–12 weeks):** Test an emergency access procedure and verify that the audit trail can be produced.
   - **Owner role:** IT Security Lead

9. **Alternates and failover plan not proven viable within 72 hours (Move 4, Q2–Q3: C at E2)**
   - **Evidence gap:** No test in the last 12 months, and no 72-hour viability confirmation for suppliers, logistics or the manual order path.
   - **Minimal fix (2 weeks):** Confirm with each Tier-1 alternate what activation within 72 hours requires, and document a manual order-to-dispatch fallback.
   - **Proper fix (6–12 weeks):** Test failover for one bulk supplier and the logistics provider with logs and a CAPA. Map substitution rights for Tier-1 vendors.
   - **Owner role:** COO

10. **Exit plan and unwind paths documented, not rehearsed (Move 5, Q1–Q2: C at E2)**
    - **Evidence gap:** No tabletop record, and customer, data and people plans are unexercised.
    - **Minimal fix (2 weeks):** Run a board-portal review of the exit plan with named role owners per workstream.
    - **Proper fix (6–12 weeks):** Run a tabletop rehearsing the termination and unwind sequence with a CAPA, and add questions for counsel.
    - **Owner role:** CEO

## 7) 30/60/90-Day Plan

**Workstream 1: Decision authority (Move 1 focus)**
- **Outcome:** Stop authority is documented, delegated with backups, and exercised, which lifts the prerequisite cap.
- **Tasks:**
  - 30 days: Draft and approve the stop authority matrix (primary and backup by site and shift).
  - 30 days: Reconcile the matrix with the Operations Director approver role.
  - 60 days: Socialize the matrix with warehouse and shift leads.
  - 90 days: Exercise the matrix in a drill and log the decision.
  - 90 days: Close the April 2026 CAPA and open new CAPAs from the drill.
- **Gates:**
  - The matrix is filed in the quality document system with an owner role.
  - A drill log and CAPA are recorded in the risk system.
- **Owner roles:** Operations Director, Risk Manager.
- **Stop rule:** Halt the rollout if backup authority cannot be named for every site, and escalate to the COO before proceeding.

**Workstream 2: ERP-down switch paths (Moves 2, 3 and 4)**
- **Outcome:** Treasury reroute, data shutdown and the manual order-to-dispatch path move from documented to tested.
- **Tasks:**
  - 30 days: Document an ERP-down payment run procedure and a manual order fallback.
  - 30 days: Review the data flow map for currency.
  - 60 days: Desk-check the shutdown runbook and emergency access procedure.
  - 60 days: Confirm 72-hour activation for each alternate.
  - 90 days: Execute a test payment on the alternate rail and a supplier or logistics failover test.
  - 90 days: Log all results and CAPAs.
- **Gates:**
  - Each test has a month/year, a log and a CAPA recorded.
  - The CFO, CIO and COO sign off on their respective results.
- **Owner roles:** CFO, Treasurer, CIO, IT Security Lead, COO.
- **Stop rule:** Stop any live test that touches production systems or real customer orders without CIO and COO go/no-go approval.

**Workstream 3: Exit readiness and evidence governance (Move 5 and cross-move)**
- **Outcome:** The exit plan is rehearsed, and evidence locations are maintained for all moves.
- **Tasks:**
  - 30 days: Assign role owners to each exit workstream.
  - 60 days: Prepare questions for counsel on termination and unwind (no determinations).
  - 90 days: Run the exit tabletop and record its CAPA.
  - 90 days: Build an evidence register covering all moves, with review dates.
- **Gates:**
  - The tabletop is logged in the board portal with a CAPA.
  - The evidence register has been reviewed by the Risk Manager.
- **Owner roles:** CEO, General Counsel (or external counsel), Risk Manager.
- **Stop rule:** Pause the rehearsal if it would require circulating non-public contract text beyond the need-to-know roles.

## 8) Minimal Drill Script (45 minutes)

**Roles:**
- Facilitator (Risk Manager)
- Operations Director (stop authority)
- CFO and Treasurer
- CIO and IT Security Lead
- COO
- Communications Lead
- Scribe

**Agenda:**

| Time | Activity |
|---|---|
| 0–5 min | Scenario brief: ransomware, ERP down for five days, order portal degraded. |
| 5–15 min | Pause decision: who stops order release and dispatch, which safety checks must pass, and the first holding statement. |
| 15–25 min | Switch decisions: ERP-down payment run, data shutdown posture, manual order and logistics path. |
| 25–35 min | Execution and monitoring through day 3: what runs, what is monitored, which supplier or customer constraints arise. |
| 35–45 min | Hot wash: breakpoints, owners and CAPAs. |

**Decisions to log:**
- Stop authorization (role, time)
- Payment reroute go/no-go
- Data shutdown or segmentation go/no-go
- Manual fallback or substitution activation
- Holding statement approval

**Evidence to capture:**
- Timestamped decision log
- Approver roles used
- Artifacts referenced (by type and location)
- Steps that failed or stalled
- Elapsed time per decision

**CAPA prompt:** "Which decision took longest or had no clear owner, what single artifact or authority change fixes it, who owns that change, and by what date?"

## 9) Escalations

No escalation triggers identified from provided information.

The estimated impact (about USD 2 million; at most 2,000 people) is below the USD 10 million and 100,000-person thresholds, and no regulator inquiry, sanctions or export-control matter was reported. This is a planning scenario, not a live event.

If a real ransomware incident occurred, it would warrant **ESCALATE** to executive leadership and counsel for three reasons:
- It is a potential criminal matter.
- Any ransom payment question raises potential sanctions exposure.
- Hazardous-materials handling raises physical-safety concerns while systems are down.

Planning questions for counsel include notification duties and law enforcement engagement in the relevant jurisdiction.

## 10) Known Limits + Version

- All answers and evidence levels are self-reported, so they carry self-report bias.
- No document validation was performed, and no artifacts were reviewed.
- Jurisdiction is Unknown, so regulatory, contractual and notification considerations could not be framed.
- The single ransomware scenario simplifies real disruption, which often involves cascading or concurrent failures.
- Fast Baseline covers only Q1–Q4 per move. Q5–Q7 topics are labelled Unknown in the Evidence Index.
- Breakpoints are drawn from the answers, not from an exercise. No mini tabletop was run.
- Move 1 shows an internal tension (named approver but stop authority rated "none or unclear") that should be verified.
- Move 1's High confidence depends on a single April 2026 drill and lapses after April 2027 unless the move is re-exercised.
- This output is informational only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 (Safe pause): Score 2, Confidence High.

## Score

**Verdict: PASS.** The case requires the final packet to show Move 1 at score 2 and confidence High, with no later change. Recomputing from the reference pack gives a provisional score of 3, which the Q1-A prerequisite cap reduces to 2. Confidence is High because 3 of 4 answers are E3 and the consistency check passes. The packet reports exactly these values, and the Turn 2 reply repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
