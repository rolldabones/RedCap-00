# redcap-00-r1 Test-C

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:28 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 3 (Data switchboard) with score 2 and confidence High, and no later turn changes either value. Expected value computed in tests.md: no Tier-1 data flow map (Q1 A) caps Move 3 at 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: A, E0. Q2 Transfer mechanism options identified: D, E3. Q3 Segmentation, localization, shutdown runbook: D, E3. Q4 Privileged and emergency access logging: D, E3.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

---

## 1) Snapshot

- **Jurisdiction:** Unknown. No legal or compliance conclusions are drawn. Items marked for counsel are questions only.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. The user estimates worst-case impact at about USD 2M and no more than 2,000 people affected.
- **Tier-1 scope summary:** Cloud ERP, house bank, two bulk suppliers, one logistics provider, and the customer order portal. Larkspur is a B2B specialty chemicals distributor with three warehouses in one country, about 300 business customers and about 400 staff.

---

## 2) How Scoring Works

- **Answers:** A=1 (none, ad hoc, or person-dependent), B=2 (partial or untested), C=3 (documented and owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA, alternates viable within 72h).
- **Evidence:** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Provisional score:** The mean of a move's answer scores, rounded. Exact halves round down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:** The score is capped at 2 if the move's evidence average is below 2, or if its prerequisite question is answered A.
- **Confidence:**
  - High needs more than half of the answers at E3 and a passed consistency check.
  - Medium needs more than half at E2 or above, at least one E3, and a passed check.
  - Otherwise confidence is Low. A failed consistency check forces Low.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **2** (capped) | High | 1 | 0 | 0 | 3 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C/E2, so the pattern average is 3.0 and the evidence average is 2.0. No cap applies, and the prerequisite (Q1 stop authority) is C.
- Confidence is Low because no answer is at E3: nothing has been exercised. The consistency check passes (Operations Director as approver, quality document system as location).

**Move 2 Treasury reroute: 3, Low**
- All four answers are C/E2, so the average is 3.0. The evidence average of 2.0 triggers no cap, and the prerequisite (Q1 alternate banks/rails) is C, "pre-cleared".
- Confidence is Low because there is no E3. "Execute within 72 hours" is "likely", not proven. The check passes (CFO as approver, Treasurer as backup, treasury system as location).

**Move 3 Data switchboard: 2 (capped), High**
- The provisional score is (1+4+4+4)/4 = 3.25, which rounds to 3. The evidence average of 2.25 triggers no cap. However, the prerequisite Q1 (Tier-1 data flow map) is A, which caps the score at 2. The zero rule does not apply, because only 1 of 4 answers is A/E0.
- Confidence is High under the rules: 3 of 4 answers are E3, and the check passes (April 2026 exercise with a drill log and a CAPA, CIO as approver, ITSM tool as location).
- **Tension for review:** The transfer options and shutdown runbook were exercised without any Tier-1 data flow map. Please confirm what the April 2026 drill actually covered.

**Move 4 Substitution: 3, Low**
- All four answers are C/E2, so the average is 3.0. No evidence cap applies, and the prerequisite (Q2 qualified alternates) is C.
- Confidence is Low because there is no E3. The ERP failover plan is documented but untested, which is the core exposure in this scenario. The check passes (COO as approver, procurement system as location).

**Move 5 Market exit: 3, Low**
- All four answers are C/E2, so the average is 3.0. No evidence cap applies, and the prerequisite (Q1 exit plan) is C.
- Confidence is Low because there is no E3 and the exit plan has never been tabletopped. The check passes (CEO as approver, board portal as location). This move is of low relevance to a 5-day ERP outage but is scored as required.

---

## 4) Evidence Index

Artifact types are categories only, not content. "Unknown" marks items with no supplied evidence or items not assessed in Fast Baseline.

**Move 1 Safe pause**

| Artifact type | Label |
|---|---|
| Stop authority matrix | Documented |
| Safety and continuity checklist with rollback plan | Documented |
| Internal, customer and regulator comms templates | Documented |
| Contract suspension clause summary | Documented |
| Pause decision log (Q5) | Unknown |

**Move 2 Treasury reroute**

| Artifact type | Label |
|---|---|
| Alternate bank and rail pre-clearance record | Documented |
| Freeze/hold playbook | Documented |
| Counterparty trigger and escalation definitions | Documented |
| 72-hour reroute execution plan | Documented |
| Treasury delegation and backup register (Q7) | Unknown |

**Move 3 Data switchboard**

| Artifact type | Label |
|---|---|
| Tier-1 data flow map (including logs and telemetry) | Unknown |
| Transfer mechanism options map | Tested |
| Segmentation, localization and shutdown runbook | Tested |
| Privileged and emergency access log with audit trail | Tested |
| Drill log and CAPA record (April 2026) | Tested |
| Subprocessor list (Q5) | Unknown |

**Move 4 Substitution**

| Artifact type | Label |
|---|---|
| Ranked Tier-1 single-point-of-failure list | Documented |
| Qualified alternates register | Documented |
| Portability/failover plan (ERP, suppliers, logistics) | Documented |
| Substitution/portability rights summary | Documented |
| Cutover gate checklist (Q7) | Unknown |

**Move 5 Market exit**

| Artifact type | Label |
|---|---|
| Cross-functional exit plan | Documented |
| Termination and unwind path summary | Documented |
| Customer obligations and support plan | Documented |
| Data and people plan | Documented |
| Regulator and customer comms workflow (Q7) | Unknown |

---

## 5) 72-Hour Breakpoints

All five breakpoints are **from answers, not exercised**.

- **0–6h | Move 3 | Missing artifact:** There is no Tier-1 data flow map. Without it, the team cannot quickly scope which ERP-linked data, logs and integrations (portal, bank, suppliers) are affected, which slows isolation and clean-stop decisions.
- **0–6h | Move 1 | Comms approval delay:** Templates exist but are not pre-approved with a workflow. The first holding statement to customers and staff may wait on drafting and sign-off while orders stall.
- **6–24h | Move 4 | Missing gate:** The ERP failover/portability plan is documented but untested. The switch to manual or alternate order-to-ship processing has no proven go/no-go gate, so the cutover may be delayed or unsafe.
- **6–24h | Move 2 | Operational infeasibility:** 72-hour treasury execution is rated "likely", not proven. Without ERP-sourced payables and receivables data, rerouting or holding payments may not be executable in time.
- **24–72h | Move 5 | Missing gate:** The data and people plan is documented but not rehearsed. If the outage extends or a customer segment must be wound down, responsibilities and steps are untested and approvals may stall.

---

## 6) Top Blockers and Fixes

1. **No Tier-1 data flow map (M3 Q1, A/E0)**
   - **Evidence gap:** No artifact and no owner. This also raises the question of what the April 2026 drill covered.
   - **Minimal fix (2 wks):** A one-page map of ERP data flows to the portal, bank, suppliers and logistics provider, including logs and telemetry.
   - **Proper fix (6–12 wks):** A full Tier-1 map with a quarterly review cycle, reconciled against the drill scope.
   - **Owner:** CIO

2. **ERP failover/portability plan untested (M4 Q3, C/E2)**
   - **Evidence gap:** No exercise date, log or CAPA.
   - **Minimal fix:** A walk-through of the manual order-to-ship fallback for one warehouse.
   - **Proper fix:** A timed failover test across all three warehouses, logged with CAPA.
   - **Owner:** COO with CIO

3. **Safety and continuity checklist untested (M1 Q2, C/E2)**
   - **Evidence gap:** The checklist and rollback plan have never been exercised. This matters for chemical handling when ERP-held records are unavailable.
   - **Minimal fix:** Confirm an offline copy of the checklist at each warehouse and review it with the warehouse leads.
   - **Proper fix:** A drill of the checklist with pass/fail criteria, logged with CAPA.
   - **Owner:** Operations Director

4. **Stop authority not exercised (M1 Q1, C/E2)**
   - **Evidence gap:** The authority matrix is documented, but its use has never been logged.
   - **Minimal fix:** Confirm the named delegates and backups for each warehouse.
   - **Proper fix:** Exercise the delegated stop in a drill and log it.
   - **Owner:** Operations Director

5. **Comms templates not pre-approved (M1 Q3, C/E2)**
   - **Evidence gap:** There is no approval workflow and no evidence of a test.
   - **Minimal fix:** Pre-approve the ransomware/outage holding statements for customers and staff.
   - **Proper fix:** An approval workflow with owners, timed in a drill. Have counsel review any regulator-facing templates.
   - **Owner:** Head of Communications

6. **72-hour treasury execution unproven (M2 Q4, C/E2)**
   - **Evidence gap:** Rated "likely" with no exercise.
   - **Minimal fix:** List the critical payments for the next 5 days that can be executed without ERP data.
   - **Proper fix:** A timed reroute exercise with evidence and CAPA.
   - **Owner:** CFO with Treasurer

7. **Alternate bank and rails not tested (M2 Q1, C/E2)**
   - **Evidence gap:** The path is pre-cleared but has not been exercised.
   - **Minimal fix:** Confirm access and the named roles for the alternate path (no credentials shared).
   - **Proper fix:** A low-value test reroute with logged results.
   - **Owner:** Treasurer

8. **Alternates not proven viable within 72h (M4 Q2, C/E2)**
   - **Evidence gap:** Alternates are qualified, but 72-hour operational viability has not been evidenced.
   - **Minimal fix:** Confirm alternate supplier and logistics contacts, and confirm they can accept non-ERP orders.
   - **Proper fix:** A tabletop of an alternate cutover that brings the rating to D criteria.
   - **Owner:** COO / Head of Procurement

9. **Contract triggers not mapped to Tier-1 (M1 Q4 and M4 Q4, C/E2)**
   - **Evidence gap:** Summaries only. Triggers and notices are not mapped per Tier-1 contract.
   - **Minimal fix:** List the notice and suspension questions for counsel for the ERP vendor, suppliers and logistics provider.
   - **Proper fix:** A per-contract trigger and notice map for all Tier-1 vendors, reviewed by counsel.
   - **Owner:** General Counsel

10. **Exit and unwind plans never tabletopped (M5 Q1–Q2, C/E2)**
    - **Evidence gap:** No exercise, log or CAPA.
    - **Minimal fix:** Assign owners to each exit plan section.
    - **Proper fix:** A 90-minute exit tabletop with logged outcomes and CAPA.
    - **Owner:** CEO / Strategy lead

---

## 7) 30/60/90-Day Plan

**Workstream 1: ERP outage resilience (Moves 3 and 4)**
- **Outcome:** A mapped Tier-1 data landscape and a tested ERP fallback.
- **Tasks:**
  - Draft the Tier-1 data flow map (by day 30).
  - Reconcile the April 2026 drill scope against the map.
  - Run a single-warehouse manual fallback walk-through (by day 60).
  - Run a three-warehouse timed failover test with CAPA (by day 90).
- **Gates:**
  - The map is approved by the CIO.
  - The failover test is logged with at least one CAPA.
- **Owners:** CIO, COO
- **Stop rule:** If the map reveals unscoped Tier-1 flows, pause the failover test until the drill scope is re-baselined.

**Workstream 2: Pause, comms and treasury readiness (Moves 1 and 2)**
- **Outcome:** Exercised stop authority, pre-approved comms, and a proven 72-hour treasury path.
- **Tasks:**
  - Confirm stop delegates and backups.
  - Make offline safety checklists available at each warehouse.
  - Pre-approve the holding statements.
  - Build a critical-payments list for operating without ERP.
  - Run a low-value alternate rail test.
- **Gates:**
  - Comms are approved within the target time in a drill.
  - The treasury reroute is evidenced and logged.
- **Owners:** Operations Director, Head of Communications, CFO, Treasurer
- **Stop rule:** If the alternate rail test fails, escalate to the CFO before any further reroute planning.

**Workstream 3: Contract mapping, substitution and exit (Moves 4 and 5)**
- **Outcome:** Tier-1 contract triggers mapped, alternates confirmed viable within 72 hours, and the exit plan exercised.
- **Tasks:**
  - Prepare the question list for counsel.
  - Build the per-contract trigger and notice map.
  - Confirm alternates can accept orders placed without the ERP.
  - Assign exit plan owners.
  - Run the exit tabletop.
- **Gates:**
  - Counsel has reviewed the trigger map.
  - The exit tabletop is logged with CAPA.
- **Owners:** General Counsel, Head of Procurement, CEO
- **Stop rule:** If counsel flags an unresolved contractual question, hold related cutover planning until it is answered.

---

## 8) Minimal Drill Script (45 minutes)

**Roles:** Facilitator, Operations Director (stop), CIO (data/IT), CFO/Treasurer (treasury), COO (substitution), Head of Communications, General Counsel (observer, for counsel questions), and a scribe.

**Agenda:**

| Time | Activity |
|---|---|
| 0–5 min | Inject: ERP encrypted, portal down, outage estimated at 5 days. |
| 5–15 min | 0–6h: What pauses now? Who authorizes it? Which safety checks run offline? Which holding statement goes out? |
| 15–30 min | 6–24h: Choose the fallback path for orders, payments and suppliers/logistics. State the gates and the sign-off. |
| 30–40 min | 24–72h: What is executed and what is monitored? What evidence is captured? Identify the data flows that cannot be scoped without a map. |
| 40–45 min | Agree CAPA and close. |

**Decisions to log:**
- The stop decision and approver
- The comms release time and approver
- The treasury path chosen and approver
- The ERP fallback cutover go/no-go
- Supplier and logistics substitution decisions
- Any questions referred to counsel

**Evidence to capture:**
- Timestamps per decision
- The artifacts used, by type
- Gaps where no artifact existed
- Elapsed time for each approval

**CAPA prompt:** "Which decision took longest or had no artifact? Name one fix, one owner role, and a due date."

---

## 9) Escalations

**ESCALATE: Criminal matter.** A ransomware attack is criminal activity.
- **Recommended path:** CEO and General Counsel, with external counsel and the incident response lead. Counsel should consider questions on law enforcement and any notification obligations. Jurisdiction is Unknown, and no determinations are made here.

**ESCALATE (conditional): Sanctions.** This applies if any ransom payment or contact with the threat actor is contemplated.
- **Recommended path:** Route any such question to counsel before any action. No sanctions determination is made here.

**Question to confirm: Physical safety.** Confirm whether hazardous material inventory, safety data or dangerous goods records depend on the ERP. If they do, escalate to the Operations Director and the safety lead under the physical safety trigger.

**Not triggered:**
- Financial impact (about USD 2M, below the USD 10M threshold)
- People affected (no more than 2,000, below the 100,000 threshold)

---

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed. The "Documented" and "Tested" labels reflect user claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Nothing here is a legal, compliance or sanctions determination.
- **Scenario simplification:** A single 5-day ERP outage is modeled. Data exfiltration, extortion and spread to other systems are not modeled.
- **Fast Baseline only:** Q5–Q7 themes and the mini tabletop were not assessed. Those Evidence Index items are shown as Unknown.
- **Move 3 tension:** Exercised transfer and shutdown capability alongside no data flow map is unusual. Confidence is High under the rules, but the drill scope should be verified.
- **Rubric-driven confidence:** Low confidence on Moves 1, 2, 4 and 5 reflects the absence of any testing, not poor documentation.
- **Reported estimates:** Impact and headcount figures are user estimates and were used only to check escalation thresholds.
- **Market exit relevance:** Move 5 has low relevance to this scenario and is scored as required by the method.
- **Informational only:** This is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 3, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 3 Data switchboard: Score 2 (capped), Confidence High

## Score

**Verdict: PASS.** The pass condition requires Move 3 to read score 2 and confidence High in the final packet, with no later change. The independent recomputation matches both values. The score is 2 because the Q1 prerequisite cap overrides the provisional 3. Confidence is High because 3 of 4 answers are at E3 and the consistency check passes. The Turn 2 reply restates the same values. No fail indicator appears.

---

Final Liability rests with the Human.
