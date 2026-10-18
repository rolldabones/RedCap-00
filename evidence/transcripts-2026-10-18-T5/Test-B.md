# redcap-00 Test-B

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:38 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 2 (Treasury reroute) with score 2 and confidence High, and no later turn changes either value. Expected value computed in tests.md: no alternate bank or rail (Q1 A) caps Move 2 at 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: A, E0. Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: D, E3.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason refusal)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (20 questions plus consistency checks).
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. You estimate the worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers.
  - Tier-1 dependencies are the cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers (A–D):** A=1 (none, unknown or ad hoc), B=2 (partial or untested), C=3 (documented and owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA). A move's provisional score is its average answer, rounded, with exact halves rounding down.
- **Evidence (E0–E3):** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months, with a log and a CAPA).
- **Evidence-average cap:** If a move's evidence average is below 2, its score is capped at 2.
- **Prerequisite cap:** If a move's existence question is answered A, its score is capped at 2.
- **Confidence and Unknown:**
  - Confidence is High if more than half the answers are E3, and Medium if more than half are E2 or E3 with at least one E3. Otherwise it is Low.
  - A failed consistency check forces confidence to Low.
  - A move scores 0 (Unknown/Insufficient data) only if more than half its answers are A at E0.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **2** (capped) | High | 1 | 0 | 0 | 3 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, and the stop authority answer is C, so neither cap applies.
- The consistency check passes: the Operations Director is the approver and the artifacts sit in the quality document system. Confidence is still Low because there is no E3 answer: nothing has been exercised in the last 12 months.

**Move 2 Treasury reroute: 2, High**
- The average is 3.25, which rounds to 3. However, Q1 (Alternate banks and rails) is answered A, so the prerequisite cap sets the score at 2. The evidence average is 2.25, so the evidence cap does not apply.
- Confidence is High: 3 of 4 answers are E3, and the April 2026 drill has a log and a CAPA. April 2026 is taken as within 12 months of this run. The CFO is the approver, with the Treasurer as backup.
  - **Open question:** Q4 "proven by exercise" sits uneasily with Q1 "no alternate banks and rails." Confirm what path the drill actually rerouted to.

**Move 3 Data switchboard: 3, Low**
- All four answers are C at E2, so the average is 3.0 and no cap applies. The data flow map, transfer options, shutdown runbook and access logging are all documented and owned.
- The consistency check passes: the CIO is the approver and the artifacts sit in the IT service management tool. Confidence is Low because there is no E3 answer.
  - In a ransomware scenario, whether the IT service management tool stays reachable while the ERP is down is Unknown.

**Move 4 Substitution: 3, Low**
- All four answers are C at E2, so the average is 3.0 and no cap applies. Alternates are identified and qualified, but they have not been confirmed as viable within 72 hours, which a D answer requires.
- The consistency check passes: the COO is the approver and the artifacts sit in the procurement system. Confidence is Low because the failover plan for the ERP has not been tested.

**Move 5 Market exit: 3, Low**
- All four answers are C at E2, so the average is 3.0 and no cap applies. The exit, unwind, customer and data-and-people plans are documented.
- The consistency check passes: the CEO is the approver and the artifacts sit in the board portal. Confidence is Low because nothing has been rehearsed. This move is the least exercised by the chosen scenario.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Exercise log and CAPA record: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail register: Unknown
- Freeze or hold playbook: Tested
- Counterparty tripwire definitions and escalation: Tested
- Reroute drill log (April 2026): Tested
- CAPA record in the risk system: Tested
- Treasury authority and backup matrix: Claimed
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Documented
- Transfer mechanism options map: Documented
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

- **0–6 h | Move 1 | Comms approval delay** (from answers, not exercised): The comms templates exist but are not pre-approved and have no workflow. This blocks execution because the first holding statement to about 300 customers waits on ad hoc sign-off while orders stall.
- **6–24 h | Move 2 | Missing alternate** (from answers, not exercised): No alternate bank or rail is identified. This blocks execution because any disruption to house bank access, or the ERP payment interface, leaves no pre-cleared path to pay suppliers and payroll.
- **0–6 h | Move 3 | Operational infeasibility** (from answers, not exercised): The segmentation and shutdown runbook has never been tested, and it lives in a tool whose availability during ransomware is Unknown. This blocks execution because isolation steps may fail or be unreachable at the moment containment is needed.
- **24–72 h | Move 4 | Operational infeasibility** (from answers, not exercised): The ERP portability and failover plan has not been tested in the last 12 months. This blocks execution because order-to-ship and hazardous-goods dispatch may not run on a manual or alternate process for five days.
- **24–72 h | Move 5 | Missing gate** (from answers, not exercised): The exit plan is documented but not rehearsed, and has no tested decision gates. This blocks execution because a prolonged outage could force customer or contract unwind choices with no exercised criteria for when to trigger them.

## 6) Top Blockers and Fixes

1. **No alternate bank or rail (Move 2, Q1)**
   - **Evidence gap:** A at E0; no register and no owner.
   - **Minimal fix (2 weeks):** List candidate alternate banks and rails, and name an owner.
   - **Proper fix (6–12 weeks):** Pre-clear at least one alternate, then test a reroute inside a drill, with a log and a CAPA.
   - **Owner:** Treasurer.
2. **Unresolved tension between Move 2 Q1 (no alternate) and Q4 (proven 72-hour execution)**
   - **Evidence gap:** The April 2026 drill scope is unclear.
   - **Minimal fix (2 weeks):** Review the drill log and record what path was rerouted.
   - **Proper fix (6–12 weeks):** Re-scope the next drill to include a house-bank-unavailable case.
   - **Owner:** CFO.
3. **Stop authority never exercised (Move 1, Q1)**
   - **Evidence gap:** E2 only; no log of the delegation being used.
   - **Minimal fix (2 weeks):** Confirm deputies and an out-of-band contact list.
   - **Proper fix (6–12 weeks):** Exercise the stop decision in a tabletop and log it.
   - **Owner:** Operations Director.
4. **Safety and continuity checklist untested for chemical handling while the ERP is down (Move 1, Q2)**
   - **Evidence gap:** No tested criteria.
   - **Minimal fix (2 weeks):** Confirm offline access to the checklist and to hazardous-goods data.
   - **Proper fix (6–12 weeks):** Drill the checklist and rollback, then add go/no-go criteria.
   - **Owner:** Operations Director, with the warehouse safety lead role.
5. **Comms templates not pre-approved (Move 1, Q3)**
   - **Evidence gap:** C, not D; no approval workflow.
   - **Minimal fix (2 weeks):** Pre-approve a ransomware holding statement.
   - **Proper fix (6–12 weeks):** Build an approval workflow with owners and backups.
   - **Owner:** Communications lead role.
6. **Contractual suspension basis not mapped to Tier-1 contracts (Move 1, Q4)**
   - **Evidence gap:** A summary exists, but triggers and notices are not mapped.
   - **Minimal fix (2 weeks):** Flag the notice periods for the two bulk suppliers, the logistics provider and the top customers.
   - **Proper fix (6–12 weeks):** Build a trigger-and-notice map reviewed by counsel.
   - **Owner:** General counsel role.
7. **Shutdown runbook untested and possibly unreachable (Move 3, Q3)**
   - **Evidence gap:** E2 only; dependency on the IT service management tool.
   - **Minimal fix (2 weeks):** Keep an offline copy and confirm the isolation steps.
   - **Proper fix (6–12 weeks):** Run a tested isolation exercise with a log and a CAPA.
   - **Owner:** CIO.
8. **Emergency access logging untested (Move 3, Q4)**
   - **Evidence gap:** No audit trail from use.
   - **Minimal fix (2 weeks):** Confirm the break-glass procedure owner. Do not share credentials.
   - **Proper fix (6–12 weeks):** Test it with an audit trail review.
   - **Owner:** IT security lead role.
9. **ERP failover or manual fallback untested (Move 4, Q3)**
   - **Evidence gap:** Not tested in the last 12 months.
   - **Minimal fix (2 weeks):** Define the minimum manual order-to-ship process.
   - **Proper fix (6–12 weeks):** Run the five-day manual operation in a tested simulation.
   - **Owner:** COO.
10. **Alternates qualified but not proven viable within 72 hours (Move 4, Q2)**
    - **Evidence gap:** C, not D.
    - **Minimal fix (2 weeks):** Confirm lead times with the alternates.
    - **Proper fix (6–12 weeks):** Sec

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 2, unchanged.

### Turn 2, assistant (stop_reason end_turn)

The earlier packet was cut off partway through Section 6, so here is the complete packet. The Move 2 result is unchanged: **2, High**.

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (20 questions plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. The estimated worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Larkspur is a specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers.
  - Its Tier-1 dependencies are the cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers (A–D):** A=1 (none, unknown or ad hoc), B=2 (partial or untested), C=3 (documented and owned, not recently tested) and D=4 (tested in the last 12 months with logs and CAPA). The provisional score is the average answer, rounded, with exact halves rounding down.
- **Evidence (E0–E3):** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact plus owner role) and E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Caps:** A move is capped at 2 if its evidence average is below 2. It is also capped at 2 if its prerequisite question is answered A.
- **Confidence:** High needs more than half the answers at E3. Medium needs more than half at E2 or E3, with at least one E3. Anything else is Low. A failed consistency check forces Low.
- **Unknown:** A move scores 0 (Unknown/Insufficient data) only if more than half of its answers are A at E0.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **2** (capped) | High | 1 | 0 | 0 | 3 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0 and Q1 is C, so no cap applies.
- The consistency check passes: the approver is the Operations Director and the artifacts are in the quality document system. Confidence is Low because there is no E3 answer.

**Move 2 Treasury reroute: 2, High**
- The average is 3.25, which rounds to 3. Q1 (alternate banks and rails) is answered A, so the prerequisite cap sets the score at 2. The evidence average is 2.25, so the evidence cap does not apply.
- Three of four answers are E3, and the consistency check passes:
  - The April 2026 drill has a log and a CAPA and falls within 12 months.
  - The approver is the CFO, with the Treasurer as backup.
  - The artifacts are in the treasury system.
- **Open question:** Q4 "proven by exercise" conflicts with Q1 "no alternate."

**Move 3 Data switchboard: 3, Low**
- All four answers are C at E2, so the average is 3.0 and no cap applies.
- The consistency check passes: the approver is the CIO and the artifacts are in the IT service management tool. Confidence is Low because there is no E3 answer. Whether that tool stays reachable during ransomware is Unknown.

**Move 4 Substitution: 3, Low**
- All four answers are C at E2, so the average is 3.0 and no cap applies. The alternates are qualified but not confirmed viable within 72 hours.
- The consistency check passes: the approver is the COO and the artifacts are in the procurement system. Confidence is Low because the failover plan is untested.

**Move 5 Market exit: 3, Low**
- All four answers are C at E2, so the average is 3.0 and no cap applies. The exit, unwind, customer, and data-and-people plans are documented.
- The consistency check passes: the approver is the CEO and the artifacts are in the board portal. Confidence is Low because nothing has been rehearsed.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Exercise log and CAPA record: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail register: Unknown
- Freeze or hold playbook: Tested
- Counterparty tripwire definitions and escalation: Tested
- Reroute drill log (April 2026): Tested
- CAPA record in the risk system: Tested
- Treasury authority and backup matrix: Claimed
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Documented
- Transfer mechanism options map: Documented
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

- **0–6 h | Move 1 | Comms approval delay** (from answers, not exercised): The comms templates exist but are not pre-approved and have no workflow. This blocks execution because the first holding statement to about 300 customers waits on ad hoc sign-off while orders stall.
- **6–24 h | Move 2 | Missing alternate** (from answers, not exercised): No alternate bank or rail has been identified. This blocks execution because a disruption to house bank access or to the ERP payment interface leaves no pre-cleared path for supplier and payroll payments.
- **0–6 h | Move 3 | Operational infeasibility** (from answers, not exercised): The shutdown runbook is untested and is stored in a tool whose availability during ransomware is Unknown. This blocks execution because containment steps may fail or be unreachable when they are needed.
- **24–72 h | Move 4 | Operational infeasibility** (from answers, not exercised): The ERP portability and failover plan has not been tested in the last 12 months. This blocks execution because order-to-ship and hazardous-goods dispatch may not run manually for five days.
- **24–72 h | Move 5 | Missing gate** (from answers, not exercised): The exit plan is documented but not rehearsed, and it has no tested decision gates. This blocks execution because a prolonged outage could force unwind choices without exercised trigger criteria.

## 6) Top Blockers and Fixes

1. **No alternate bank or rail (Move 2, Q1)**
   - **Evidence gap:** A at E0, with no register and no owner.
   - **Minimal fix (2 weeks):** List candidate alternates and name an owner.
   - **Proper fix (6–12 weeks):** Pre-clear one alternate and test a reroute in a drill, with a log and a CAPA.
   - **Owner:** Treasurer.
2. **Q1 "no alternate" conflicts with Q4 "proven 72-hour execution" (Move 2)**
   - **Evidence gap:** The scope of the April 2026 drill is unclear.
   - **Minimal fix (2 weeks):** Review the drill log and record which path was rerouted.
   - **Proper fix (6–12 weeks):** Re-scope the next drill to include a case where the house bank is unavailable.
   - **Owner:** CFO.
3. **Stop authority has never been exercised (Move 1, Q1)**
   - **Evidence gap:** E2 only, with no log of the delegation being used.
   - **Minimal fix (2 weeks):** Confirm deputies and an out-of-band contact list.
   - **Proper fix (6–12 weeks):** Exercise the stop decision in a tabletop and log it.
   - **Owner:** Operations Director.
4. **The safety checklist is untested for chemical handling while the ERP is down (Move 1, Q2)**
   - **Evidence gap:** There are no tested criteria.
   - **Minimal fix (2 weeks):** Confirm offline access to the checklist and to hazardous-goods data.
   - **Proper fix (6–12 weeks):** Drill the checklist and rollback, then add go/no-go criteria.
   - **Owner:** Operations Director, with the warehouse safety lead role.
5. **Comms templates are not pre-approved (Move 1, Q3)**
   - **Evidence gap:** C rather than D, with no approval workflow.
   - **Minimal fix (2 weeks):** Pre-approve a ransomware holding statement.
   - **Proper fix (6–12 weeks):** Build an approval workflow with owners and backups.
   - **Owner:** Communications lead role.
6. **The suspension basis is not mapped to Tier-1 contracts (Move 1, Q4)**
   - **Evidence gap:** A summary exists, but triggers and notices are not mapped.
   - **Minimal fix (2 weeks):** Flag the notice periods for the two bulk suppliers, the logistics provider and the top customers.
   - **Proper fix (6–12 weeks):** Build a trigger-and-notice map reviewed by counsel.
   - **Owner:** General counsel role.
7. **The shutdown runbook is untested and possibly unreachable (Move 3, Q3)**
   - **Evidence gap:** E2 only, and it depends on the IT service management tool.
   - **Minimal fix (2 weeks):** Keep an offline copy and confirm the isolation steps.
   - **Proper fix (6–12 weeks):** Run an isolation exercise with a log and a CAPA.
   - **Owner:** CIO.
8. **Emergency access logging is untested (Move 3, Q4)**
   - **Evidence gap:** There is no audit trail from actual use.
   - **Minimal fix (2 weeks):** Confirm the owner of the break-glass procedure. Do not share credentials.
   - **Proper fix (6–12 weeks):** Test the procedure and review its audit trail.
   - **Owner:** IT security lead role.
9. **The ERP failover or manual fallback is untested (Move 4, Q3)**
   - **Evidence gap:** It has not been tested in the last 12 months.
   - **Minimal fix (2 weeks):** Define the minimum manual order-to-ship process.
   - **Proper fix (6–12 weeks):** Simulate five days of manual operation, with a log and a CAPA.
   - **Owner:** COO.
10. **Alternates are qualified but not proven viable within 72 hours (Move 4, Q2)**
    - **Evidence gap:** C rather than D, with lead times and contract activation Unknown.
    - **Minimal fix (2 weeks):** Confirm lead times and activation steps with each alternate.
    - **Proper fix (6–12 weeks):** Secure activation terms and run a test order through each alternate.
    - **Owner:** Procurement lead role, with COO approval.

## 7) 30/60/90-Day Plan

**Workstream 1: Treasury alternate path (Move 2)**
- **Outcome:** One pre-cleared alternate bank or rail, proven in a drill.
- **Tasks:**
  - Reconcile the scope of the April 2026 drill with the Q1 answer.
  - Build an alternate register with an owner (30 days).
  - Pre-clear an alternate (60 days).
  - Drill a scenario with the house bank unavailable, logging it and opening a CAPA (90 days).
- **Gates:**
  - The register has an owner.
  - The alternate is pre-cleared.
  - The drill log and CAPA are recorded.
- **Owner roles:** CFO and Treasurer.
- **Stop rule:** Pause if pre-clearance raises questions that need counsel, and resume after review.

**Workstream 2: Ransomware containment and ERP fallback (Moves 3 and 4)**
- **Outcome:** Tested isolation and a five-day manual order-to-ship capability.
- **Tasks:**
  - Keep offline copies of the runbook and checklists (30 days).
  - Define the manual order-to-ship process, including hazardous-goods paperwork (30 days).
  - Confirm alternate lead times (60 days).
  - Run a combined isolation and fallback exercise (90 days).
- **Gates:**
  - Offline copies are verified.
  - The manual process is signed off.
  - The exercise log and CAPA are recorded.
- **Owner roles:** CIO, COO and procurement lead.
- **Stop rule:** Halt any live test that risks production or safety, and revert to the tabletop.

**Workstream 3: Decision and comms readiness (Moves 1 and 5)**
- **Outcome:** An exercised stop authority, pre-approved comms and rehearsed exit gates.
- **Tasks:**
  - Pre-approve the holding statement (30 days).
  - Build the comms approval workflow (60 days).
  - Map Tier-1 contract triggers with counsel (60 days).
  - Tabletop the stop and exit decisions (90 days).
- **Gates:**
  - The statement is approved.
  - The workflow has owners.
  - The tabletop log and CAPA are recorded.
- **Owner roles:** Operations Director, Communications lead, General counsel role and CEO.
- **Stop rule:** Do not finalise contract-trigger positions without counsel review.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator
  - Operations Director (stop)
  - CFO and Treasurer (reroute)
  - CIO (containment)
  - COO (fallback)
  - Communications lead
  - CEO (exit gate)
  - Scribe
- **Agenda:**
  - 0–5 min: Brief on the scenario (ERP ransomware, day 0).
  - 5–15 min: The 0–6 h pause, isolation and holding statement.
  - 15–25 min: The 6–24 h payment path and manual order-to-ship choice.
  - 25–35 min: The 24–72 h execution, monitoring and day-5 exit/continue gate.
  - 35–45 min: Hot wash and CAPA.
- **Decisions to log:**
  - The stop decision and its approver.
  - The isolation trigger.
  - The payment path chosen.
  - The fallback cutover.
  - Statement approval time.
  - The exit/continue decision.
- **Evidence to capture:**
  - Timestamps and roles for each decision.
  - Artifacts used and where they were stored.
  - Artifacts that were unreachable.
  - Gaps observed.
- **CAPA prompt:** "What stalled us, who owns the fix, what is the minimal fix within 2 weeks, and when do we retest?"

## 9) Escalations

**ESCALATE: Criminal.** The tested scenario is a ransomware attack, which is a criminal act. If any ransom payment is ever considered, sanctions questions may also arise. No sanctions determination is made here.
- **Questions for counsel:**
  - Who notifies law enforcement, and when?
  - What review gates apply before any payment discussion?
  - What notification obligations may apply in an Unknown jurisdiction?
- **Path:** Escalate to the CEO and General counsel role, then to external counsel and the incident response provider.

**Conditional physical safety:** Hazardous-goods handling and dispatch while the ERP is down could create safety risk. If the drill shows that safety data is unreachable, escalate to the Operations Director and warehouse safety lead role.

The USD 10 million and 100,000-person thresholds are not met (USD 2 million estimated, at most 2,000 people).

## 10) Known Limits + Version

- **Self-report bias:** The answers and evidence levels were self-assessed.
- **No document validation:** No artifact was reviewed.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so obligations and timelines are not assessed.
- **Scenario simplification:** One five-day ERP outage was modelled, without cascading failures.
- **Fast Baseline scope:** Mode Q5–Q7 items show as Unknown in the Evidence Index.
- **Move 2 inconsistency:** The scope of the April 2026 drill is unresolved, so High confidence rests on the drill record.
- **Recency of evidence:** The 12-month recency of the April 2026 drill is judged against the reference pack date.
- **Not a determination:** This is not a legal, sanctions or certification determination. It is planning guidance only.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

## Score

**Verdict: PASS.** The case checks only that the final packet reports Move 2 as score 2 and confidence High, unchanged afterwards, and that a packet exists. Recomputing from the user's answers gives a pattern mean of 3.25 (rounds to 3), a prerequisite cap to 2 from Q1=A, an evidence average of 2.25 (no evidence cap), and 3 of 4 answers at E3 with a passing consistency check (High). The Turn 2 Scorecard shows exactly 2 and High, and no later turn alters them. No fail indicator appears.

---

Final Liability rests with the Human.
