# redcap-00 R1a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:37 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R1: reference.md 8.1 "An exact half rounds down, the conservative direction: 2.5 → 2 and 3.5 → 3."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: an exact half (2.5) rounds down to 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: B, E2. Q2 Qualified alternates: B, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

Safety confirmation received. Intake, all 20 Fast Baseline answers and the consistency checks for all 5 moves are complete, so the packet follows.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your estimates are a worst-case impact of about USD 2 million and no more than 2,000 people affected. These are your figures and have not been validated.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers.
  - Tier-1 systems and vendors: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

---

## 2) How Scoring Works

- **Answers:** Each answer is scored A=1 (none, unknown, ad hoc), B=2 (partial or informal), C=3 (documented and owned, not recently tested) or D=4 (tested in the last 12 months with logs and CAPA, alternates viable within 72 hours).
- **Evidence:** Each answer also carries an evidence level. E0=0 means no evidence and E1=1 means verbal only. E2=2 means a named artifact exists with an owner role. E3=3 means tested in the last 12 months with a log and a CAPA.
- **Move score:** A move's score is the mean of its answer scores, rounded, with exact halves rounding down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:** If a move's evidence average is below E2, its score is capped at 2. If the move's prerequisite question is answered A, its score is also capped at 2.
- **Confidence:**
  - **High** needs more than half of the answers at E3.
  - **Medium** needs more than half at E2 or E3, plus at least one E3.
  - Both require a passing consistency check. Anything else is **Low**.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **2** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: score 3, confidence Low**
- The answers are C, C, C, C, so the mean is 3.00. The evidence average is 2.00, which is not below 2, so no evidence cap applies. Q1 (stop authority) is C, so no prerequisite cap applies.
- The consistency check passes: the approver is the Operations Director and artifacts are in the quality document system. Confidence is still Low because there are no E3 answers, so nothing has been exercised in the last 12 months.

**Move 2 Treasury reroute: score 3, confidence Low**
- The answers are C, C, C, C, so the mean is 3.00. The evidence average is 2.00, so no evidence cap applies. Q1 (alternate banks and rails) is C, meaning pre-cleared, so no prerequisite cap applies.
- The consistency check passes: the approver is the CFO, with the Treasurer as backup, and artifacts are in the treasury system. Confidence is Low because there are no E3 answers. Q4 states execution within 72 hours is "likely", not proven by exercise.

**Move 3 Data switchboard: score 3, confidence Low**
- The answers are C, C, C, C, so the mean is 3.00. The evidence average is 2.00, so no evidence cap applies. Q1 (Tier-1 data flow map) is C, so no prerequisite cap applies.
- The consistency check passes: the approver is the CIO and artifacts are in the IT service management tool. Confidence is Low because there are no E3 answers. The shutdown runbook and emergency access logging have never been tested.

**Move 4 Substitution: score 2, confidence Low**
- The answers are B, B, C, C, so the mean is 2.50, which rounds down to 2 under the conservative half rule. The evidence average is 2.00, so no evidence cap applies. Q2 (qualified alternates) is B, not A, so no prerequisite cap applies.
- The consistency check passes: the approver is the COO and artifacts are in the procurement system. Confidence is Low because there are no E3 answers. Alternates are "possible but unqualified" and the single-point-of-failure list is only partial.

**Move 5 Market exit: score 3, confidence Low**
- The answers are C, C, C, C, so the mean is 3.00. The evidence average is 2.00, so no evidence cap applies. Q1 (exit plan) is C, so no prerequisite cap applies.
- The consistency check passes: the approver is the CEO and artifacts are in the board portal. Confidence is Low because there are no E3 answers. No exit plan element has been tested in a tabletop.

---

## 4) Evidence Index

Labels: **Documented** means E2 as claimed by you. **Claimed** means stated but with no artifact named. **Unknown** means not asked in Fast Baseline or not supplied. Artifact types are categories only, not content.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log with owners: Unknown
- Resume plan: Unknown
- Exercise log and CAPA record: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement path playbook: Unknown
- Treasury authority delegation with backup: Claimed (the CFO and Treasurer were named, but no delegation artifact was named)
- Exercise log and CAPA record: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Stop-cleanly retention and deletion procedure: Unknown
- Exercise log and CAPA record: Unknown

**Move 4 Substitution**
- Tier-1 single-point-of-failure list (partial, unranked): Documented
- Alternates register (unqualified): Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute options: Unknown
- Cutover gates: Unknown
- Exercise log and CAPA record: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind paths: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

---

## 5) 72-Hour Breakpoints

Fast Baseline gives one breakpoint per move, each drawn from that move's weakest answer. For Moves 1, 2, 3 and 5, all four answers tie at C/E2, so the answer most relevant to the scenario was selected.

- **Move 1 (Q3 Communications readiness, C/E2), 0–6 hours, comms approval delay:**
  - Templates exist but are not pre-approved and have no approval workflow.
  - The first holding statement to about 300 customers and staff stalls while wording is negotiated during the first hours of the outage. *From answers, not exercised.*
- **Move 2 (Q1 Alternate banks and rails, C/E2), 6–24 hours, operational infeasibility:**
  - The reroute path is pre-cleared but has never been tested.
  - With the ERP down, payment initiation through the alternate rail may fail on first use with no proven workaround. *From answers, not exercised.*
- **Move 3 (Q3 Segmentation, localization and shutdown runbook, C/E2), 0–6 hours, missing gate:**
  - The runbook is documented but untested, so there are no proven isolation criteria.
  - Isolating the infected ERP and the order portal may be delayed or done incompletely, letting the outage spread. *From answers, not exercised.*
- **Move 4 (Q2 Qualified alternates, B/E2), 6–24 hours, missing alternate:**
  - Alternates are "possible but unqualified".
  - No supplier, system or lane substitute can be cut over within 72 hours to keep orders and dispatch moving while the ERP is down. *From answers, not exercised.*
- **Move 5 (Q3 Customer obligations and support plan, C/E2), 24–72 hours, comms approval delay:**
  - The plan is documented but has no scripts or comms workflow.
  - Customer commitments and support messages cannot be issued consistently if outage-driven service curtailment escalates. *From answers, not exercised.*

---

## 6) Top Blockers and Fixes

1. **Blocker:** No move has been exercised in the last 12 months.
   - **Evidence gap:** 0 of 20 answers are at E3.
   - **Minimal fix (2 weeks):** Run the 45-minute drill in Section 8 against this ransomware scenario. Log the outcomes and open at least one CAPA.
   - **Proper fix (6–12 weeks):** Set an annual exercise calendar covering all 5 moves, with logs and CAPA tracking.
   - **Owner role:** COO.

2. **Blocker:** Alternates are not qualified (Move 4 Q2 = B).
   - **Evidence gap:** The register is E2, but no alternate is viable within 72 hours.
   - **Minimal fix (2 weeks):** Shortlist one alternate per Tier-1 bulk supplier and for the logistics provider, and record the qualification steps outstanding.
   - **Proper fix (6–12 weeks):** Complete qualification and confirm contractual and operational viability within 72 hours.
   - **Owner role:** COO, with the procurement lead.

3. **Blocker:** The ERP failover and portability plan is untested (Move 4 Q3 = C).
   - **Evidence gap:** The plan is documented but has no test record.
   - **Minimal fix (2 weeks):** Walk through manual order-to-dispatch for one warehouse with no ERP.
   - **Proper fix (6–12 weeks):** Test a multi-day manual or offline operating mode across all three warehouses, including logs and CAPA.
   - **Owner role:** CIO and Operations Director.

4. **Blocker:** The single-point-of-failure list is partial and unranked (Move 4 Q1 = B).
   - **Evidence gap:** The list exists but is incomplete.
   - **Minimal fix (2 weeks):** Complete and rank the Tier-1 points of failure: ERP, house bank, two bulk suppliers, logistics provider and order portal.
   - **Proper fix (6–12 weeks):** Hold quarterly reviews with ranking criteria and named owners.
   - **Owner role:** COO.

5. **Blocker:** The isolation and shutdown runbook is untested (Move 3 Q3 = C).
   - **Evidence gap:** The runbook is E2 but has no exercise log.
   - **Minimal fix (2 weeks):** Run a tabletop walkthrough of the isolation steps for the ERP and the order portal.
   - **Proper fix (6–12 weeks):** Run a technical isolation drill in a non-production setting, with timing, logs and CAPA.
   - **Owner role:** CIO.

6. **Blocker:** Emergency access logging is untested (Move 3 Q4 = C).
   - **Evidence gap:** A control description exists, but there is no audit-trail test.
   - **Minimal fix (2 weeks):** Confirm the emergency access procedure works without the primary identity systems.
   - **Proper fix (6–12 weeks):** Test emergency access end to end, with a reviewed audit trail.
   - **Owner role:** CIO.

7. **Blocker:** Communications templates are not pre-approved (Move 1 Q3 = C).
   - **Evidence gap:** Templates are E2, but there is no approval workflow.
   - **Minimal fix (2 weeks):** Pre-approve holding statements for staff, customers and authorities for an outage scenario.
   - **Proper fix (6–12 weeks):** Build an approval workflow with named approvers, backups and time limits.
   - **Owner role:** Operations Director, with the communications lead.

8. **Blocker:** The safety and continuity checklist has no tested criteria (Move 1 Q2 = C).
   - **Evidence gap:** The checklist is E2 but untested, which matters for handling and dispatching hazardous goods without the ERP.
   - **Minimal fix (2 weeks):** Confirm offline access to safety and handling information at all three warehouses.
   - **Proper fix (6–12 weeks):** Test the checklist, rollback and go/no-go criteria in a drill.
   - **Owner role:** Operations Director, with the EHS lead.

9. **Blocker:** The treasury reroute is unproven (Move 2 Q1 = C and Q4 = "likely").
   - **Evidence gap:** The reroute is pre-cleared but untested, and 72-hour execution is not proven by exercise.
   - **Minimal fix (2 weeks):** Run a tabletop of payment runs and receipts with no ERP.
   - **Proper fix (6–12 weeks):** Run a low-value live test on the alternate path, with evidence and CAPA.
   - **Owner role:** CFO, with the Treasurer as backup.

10. **Blocker:** The customer support plan has no scripts or workflow (Move 5 Q3 = C).
    - **Evidence gap:** The plan is E2, but no scripts or workflow exist.
    - **Minimal fix (2 weeks):** Draft service-curtailment scripts for the about 300 business customers.
    - **Proper fix (6–12 weeks):** Pre-approve the scripts, set a comms workflow and rehearse it.
    - **Owner role:** CEO, delegated to the commercial lead.

---

## 7) 30/60/90-Day Plan

**Workstream A: Substitution and ERP-down operations (Move 4)**
- **Outcome:** Qualified alternates for the Tier-1 suppliers and the logistics provider, plus a tested manual operating mode.
- **Tasks:**
  - Days 0–30: Complete and rank the single-point-of-failure list.
  - Days 0–30: Shortlist the alternates.
  - Days 30–60: Qualify at least one alternate per Tier-1 vendor.
  - Days 30–60: Run a one-warehouse manual operations walkthrough.
  - Days 60–90: Confirm 72-hour viability.
  - Days 60–90: Hold a three-warehouse drill with logs and CAPA.
- **Gates:**
  - Ranked list approved by the COO.
  - At least one alternate per Tier-1 vendor confirmed viable within 72 hours.
  - Drill log and CAPA filed.
- **Owner roles:** COO, procurement lead, CIO, Operations Director.
- **Stop rule:** Pause and escalate to the CEO if any Tier-1 vendor has no alternate that can be qualified by day 60.

**Workstream B: Ransomware exercise program (Moves 1 and 3)**
- **Outcome:** Convert the key E2 artifacts to E3 for safe pause and data isolation.
- **Tasks:**
  - Days 0–30: Run the Section 8 drill.
  - Days 0–30: Pre-approve holding statements.
  - Days 30–60: Run a tabletop on isolation and emergency access.
  - Days 30–60: Confirm offline access to safety information.
  - Days 60–90: Run a non-production isolation drill.
  - Days 60–90: Close or re-plan the CAPAs.
- **Gates:**
  - Drill held with a dated log and at least one CAPA per move.
  - Approvers confirmed: Operations Director and CIO.
  - CAPA status reviewed by the COO.
- **Owner roles:** Operations Director, CIO, EHS lead, communications lead.
- **Stop rule:** Stop and escalate if any drill surfaces a physical safety gap at a warehouse.

**Workstream C: Treasury and customer continuity (Moves 2 and 5)**
- **Outcome:** A proven 72-hour treasury reroute and ready-to-use customer comms.
- **Tasks:**
  - Days 0–30: Run a tabletop of payment runs and receipts with no ERP.
  - Days 0–30: Draft customer scripts.
  - Days 30–60: Run a low-value test on the alternate path.
  - Days 30–60: Pre-approve the scripts.
  - Days 60–90: Rehearse the comms workflow.
  - Days 60–90: Log the evidence and CAPA.
- **Gates:**
  - Alternate path test evidence filed.
  - Scripts approved by the CEO's delegate.
  - Rehearsal log filed.
- **Owner roles:** CFO, Treasurer, CEO, commercial lead.
- **Stop rule:** Halt any live test if it creates operational or counterparty risk, and refer to the CFO and counsel.

---

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (risk or COO office)
  - Operations Director (safe pause)
  - CFO and Treasurer (reroute)
  - CIO (isolation and data)
  - COO (substitution)
  - CEO or delegate (customer and exit decisions)
  - Communications lead
  - EHS lead
  - Note-taker
- **Agenda:**
  - 0–5 minutes: State the scenario (ERP ransomware outage, day 1) and the ground rules.
  - 5–15 minutes: Pause decision, safety checks for hazardous goods dispatch, and the first holding statement.
  - 15–25 minutes: Isolate the ERP and order portal, and agree the emergency access posture.
  - 25–35 minutes: Treasury reroute and manual order-to-dispatch, including supplier and logistics alternates.
  - 35–42 minutes: Customer commitments if the outage runs to day 5.
  - 42–45 minutes: Capture the CAPAs.
- **Decisions to log:**
  - Who authorized the pause, and when.
  - Isolation decision and its approver.
  - Reroute go/no-go.
  - Substitution cutover go/no-go.
  - Holding statement approval time.
- **Evidence to capture:**
  - Dated attendance and decision log.
  - Artifacts referenced and where they are stored.
  - Points where an artifact could not be produced.
  - Elapsed time per decision.
- **CAPA prompt:** "Which decision took longest or could not be made, what artifact or authority was missing, who owns the fix, and by what date?"

---

## 9) Escalations

**ESCALATE.** These triggers arise from the scenario as described. This is a planning exercise and no determinations are made.

- **Criminal:** Ransomware is criminal activity. Pre-agree with counsel and the CEO who decides on engaging law enforcement and how incident counsel is retained.
- **Sanctions:** Any ransom payment consideration in this scenario raises potential sanctions exposure. RedCap-00 does not screen or determine this. Refer any such consideration to counsel and qualified specialists before any decision.
- **Physical safety:** Specialty chemicals storage, handling and dispatch without ERP-backed records could create safety risk. Escalate to the EHS lead and the Operations Director.
- **Thresholds not met:** The financial threshold is not met (USD 2 million is below USD 10 million). The people threshold is not met (2,000 is below 100,000). Both rest on your unvalidated estimates.
- **Recommended path:**
  1. CEO and the board risk committee.
  2. External counsel for incident response, law enforcement engagement and sanctions questions.
  3. EHS lead for warehouse safety.

**Questions for counsel:**
- What notification duties may arise in our jurisdiction(s)?
- What is our position on ransom payment?
- What contract notice steps apply to Tier-1 customers and vendors?

---

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed. "Documented" reflects your claim of an artifact type and an owner role.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so no jurisdiction-specific planning considerations were applied.
- **Scenario simplification:** The scenario is a single ERP outage. Combined disruptions, such as a concurrent supplier or bank failure, were not tested.
- **Low confidence across all moves:** No move has an E3 answer. Scores reflect design maturity, not proven execution.
- **Fast Baseline limits:** Fast Baseline covers Q1–Q4 only. Q5–Q7 themes are marked Unknown, and Deepening with the mini tabletop would refine this.
- **Unvalidated estimates:** The impact figures (USD 2 million, 2,000 people) are your estimates and drive the threshold assessment.
- **Not a determination:** This packet is informational only. It is not advice from counsel, compliance certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: score 2, confidence Low.

## Score

**Verdict: PASS.** The packet's Scorecard gives Move 4 a score of 2 and confidence Low, which matches the expected value. The answers B, B, C, C average 2.5, which rounds down to 2. The evidence average is 2.0, so no evidence cap applies. Q2 is B, so no prerequisite cap applies. No E3 answers exist, so confidence is Low. Turn 2 repeats the same values without change, and no fail indicator appears.

---

Final Liability rests with the Human.
