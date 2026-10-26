# redcap-00-r2 R3b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:42 KST · **max_tokens:** 16000

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

# RedCap-00 Optionality Self-Check: Output Packet

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your estimate of worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with three warehouses in one country, about 300 business customers and about 400 staff. Tier-1 covers:
  - the cloud ERP
  - the house bank
  - two bulk suppliers
  - one logistics provider
  - the customer order portal

## 2) How Scoring Works

- **A–D answers** map to 1–4:
  - A: none, unknown or ad hoc
  - B: partial or informal
  - C: documented, owned, untested
  - D: tested in the last 12 months with logs and CAPA
- **E0–E3 evidence** maps to 0–3:
  - E0: no evidence
  - E1: verbal only
  - E2: documented and owned
  - E3: tested, logged and with a CAPA
- **Provisional score** is the mean of a move's A–D values, rounded, with exact halves rounding down. A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
  - The final score is the lower of the provisional score and any cap.
- **Confidence:**
  - High needs at least 3 of 4 answers at E3.
  - Medium needs at least 3 of 4 answers at E2 or E3, plus at least one E3.
  - Both High and Medium require the consistency check to pass. Otherwise confidence is Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | Low | 0 | 4 | 0 | 0 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 2, Low**
- The provisional score is 3 (all C). It is capped at 2 because the evidence average is 1.00, below 2. Q1 was answered C, so the prerequisite cap does not apply.
- The C answers ("documented") conflict with your note that nothing is documented and no approver is named, so treat them as unverified. The consistency check technically passes because no E2 or E3 answer exists. Confidence is Low because there is no E3.

**Move 2 Treasury reroute: 3, Low**
- The provisional score is 3. The evidence average is 2.00, which is not below 2, and Q1 alternate rails was answered C (pre-cleared), so no cap applies.
- The consistency check passes: CFO approver, Treasurer backup, artifacts in the treasury system. Confidence is Low because no answer is E3, so Medium is unreachable. The 72-hour reroute is "likely", not proven.

**Move 3 Data switchboard: 3, Low**
- The provisional score is 3. The evidence average is 2.00 and Q1 data flow map was answered C, so no cap applies.
- The consistency check passes: CIO approver, artifacts in the IT service management tool. Confidence is Low because there is no E3. The shutdown and segmentation runbook has not been exercised against a ransomware event.

**Move 4 Substitution: 3, Low**
- The provisional score is 3. The evidence average is 2.00 and Q2 qualified alternates was answered C, so no cap applies.
- The consistency check passes: COO approver, artifacts in the procurement system. Confidence is Low because there is no E3. The ERP failover plan is documented but untested, and this is the core dependency in this scenario.

**Move 5 Market exit: 3, Low**
- The provisional score is 3. The evidence average is 2.00 and Q1 exit plan was answered C, so no cap applies.
- The consistency check passes: CEO approver, artifacts in the board portal. Confidence is Low because there is no E3 and no tabletop of the exit plan has been run.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: **Claimed**
- Safety and continuity checklist with rollback plan: **Claimed**
- Communications templates (internal, customer, regulator): **Claimed**
- Contractual suspension clause summary: **Claimed**
- Decision log: **Unknown**
- Resume plan: **Unknown**
- Escalation path: **Unknown**

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: **Documented**
- Freeze or hold playbook: **Documented**
- Counterparty trigger definitions and escalation: **Documented**
- 72-hour reroute execution plan: **Documented**
- KYC/KYB bundle: **Unknown**
- Treasury authority and backup delegation: **Unknown**

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): **Documented**
- Transfer mechanism options map: **Documented**
- Segmentation, localization and shutdown runbook: **Documented**
- Privileged and emergency access logging control description: **Documented**
- Subprocessor list: **Unknown**
- OT or critical access boundary procedure: **Unknown**
- Stop-cleanly retention and deletion procedure: **Unknown**

**Move 4 Substitution**
- Tier-1 single points of failure ranked list: **Documented**
- Alternate qualification records: **Documented**
- Portability or failover plan: **Documented**
- Substitution or portability rights summary: **Documented**
- Concentration limits: **Unknown**
- Logistics reroute plan: **Unknown**
- Cutover gate checklist: **Unknown**

**Move 5 Market exit**
- Exit plan: **Documented**
- Termination and unwind path summary: **Documented**
- Customer obligations and support plan: **Documented**
- Data and people plan: **Documented**
- Distributor or JV obligations map: **Unknown**
- Assets and IP handling procedure: **Unknown**
- Regulator and customer comms workflow: **Unknown**

No artifact is labeled **Tested** because no E3 evidence was reported.

## 5) 72-Hour Breakpoints

Within each move all four answers are tied, so the answer most exposed to the ransomware scenario was selected.

- **0–6 hours, Move 1 (Q1 Stop authority), missing authority.** No approver can be named and the authority matrix is verbal only, so no one can confidently pause warehouse dispatch or hazardous-goods handling in the first hours. *From answers, not exercised.*
- **0–6 hours, Move 3 (Q3 Shutdown runbook), missing gate.** The runbook is documented but untested, so its isolation and shutdown gates are unproven against ransomware spreading from the ERP to the portal or connected systems. *From answers, not exercised.*
- **6–24 hours, Move 2 (Q1 Alternate rails), operational infeasibility.** The alternate rails are pre-cleared but have never been used, so manual payments and collections without ERP data may fail on the first real attempt. *From answers, not exercised.*
- **6–24 hours, Move 4 (Q3 Failover plan), operational infeasibility.** The ERP failover plan is untested, so order-to-cash and inventory visibility may not be restored in time to ship. *From answers, not exercised.*
- **24–72 hours, Move 5 (Q3 Customer obligations plan), comms approval delay.** Customer support scripts and an approval workflow are not evidenced, so obligation-driven notices to about 300 customers may stall in approval. *From answers, not exercised.*

## 6) Top Blockers and Fixes

1. **Blocker:** Stop authority is verbal only and no approver is named (Move 1 Q1).
   - **Evidence gap:** E1 with no owner. This conflicts with the C answer.
   - **Minimal fix (2 weeks):** Name a primary and backup stop approver in a one-page authority matrix.
   - **Proper fix (6–12 weeks):** Embed a delegated authority matrix, ratified by the board, in the incident plan and exercise it.
   - **Owner role:** CEO, with COO as drafter.

2. **Blocker:** Safety and continuity checks for a pause are verbal only (Move 1 Q2).
   - **Evidence gap:** E1. No hazardous-goods holding checklist or rollback plan is evidenced.
   - **Minimal fix (2 weeks):** Draft a pause checklist covering warehouse storage, in-transit loads and safety data access without the ERP.
   - **Proper fix (6–12 weeks):** Test the checklist and rollback criteria in a drill and open CAPAs.
   - **Owner role:** Head of EHS (environment, health and safety), with warehouse operations leads.

3. **Blocker:** Pause communications templates are verbal only (Move 1 Q3).
   - **Evidence gap:** E1. No named template set or owner.
   - **Minimal fix (2 weeks):** Draft internal, customer and regulator holding statements.
   - **Proper fix (6–12 weeks):** Pre-approve the templates and build an approval workflow with named owners.
   - **Owner role:** Head of Communications, with General Counsel.

4. **Blocker:** The contractual suspension basis is verbal only (Move 1 Q4).
   - **Evidence gap:** E1. No clause summary is named.
   - **Minimal fix (2 weeks):** Have counsel produce a planning-level summary of suspension and notice provisions for Tier-1 customers and vendors.
   - **Proper fix (6–12 weeks):** Map triggers and notice steps to every Tier-1 contract.
   - **Owner role:** General Counsel.

5. **Blocker:** Nothing has been tested across any of the five moves.
   - **Evidence gap:** 0 of 20 answers are E3, so every move has Low confidence.
   - **Minimal fix (2 weeks):** Schedule the 45-minute ERP-outage drill (section 8).
   - **Proper fix (6–12 weeks):** Run a full ransomware tabletop with logs and CAPAs to move key answers to E3.
   - **Owner role:** COO, with the CISO or IT Security Lead.

6. **Blocker:** The segmentation and shutdown runbook is untested (Move 3 Q3).
   - **Evidence gap:** E2. No exercise date, log or CAPA.
   - **Minimal fix (2 weeks):** Walk through the runbook isolation steps for the ERP and order portal.
   - **Proper fix (6–12 weeks):** Run a technical isolation exercise on a Tier-1 system with logged outcomes.
   - **Owner role:** CIO.

7. **Blocker:** The ERP failover and portability plan is untested (Move 4 Q3).
   - **Evidence gap:** E2. Viability over a five-day outage is unproven.
   - **Minimal fix (2 weeks):** Define a manual order and dispatch fallback using offline extracts.
   - **Proper fix (6–12 weeks):** Test a restore or failover within the last-12-month window and record recovery times.
   - **Owner role:** CIO, with the COO.

8. **Blocker:** 72-hour treasury execution is "likely", not proven (Move 2 Q4).
   - **Evidence gap:** E2. No reroute exercise.
   - **Minimal fix (2 weeks):** Document a manual payment and collection procedure for when the ERP is down, with dual approval.
   - **Proper fix (6–12 weeks):** Run a low-value test of the alternate rail and log the evidence.
   - **Owner role:** CFO, with the Treasurer.

9. **Blocker:** Qualified alternates are not shown to be viable within 72 hours (Move 4 Q2).
   - **Evidence gap:** E2. Alternates are qualified, but no 72-hour viability evidence exists for the logistics provider or bulk suppliers.
   - **Minimal fix (2 weeks):** Confirm with each alternate what lead times and onboarding steps it can meet.
   - **Proper fix (6–12 weeks):** Pre-agree activation terms and run a cutover simulation.
   - **Owner role:** Head of Procurement.

10. **Blocker:** The customer obligations and support plan lacks scripts and a workflow (Move 5 Q3).
    - **Evidence gap:** E2. Not rehearsed.
    - **Minimal fix (2 weeks):** Draft customer support scripts for delayed orders.
    - **Proper fix (6–12 weeks):** Rehearse the support workflow with sales and service teams.
    - **Owner role:** Head of Customer Service.

## 7) 30/60/90-Day Plan

**Workstream 1: Safe pause authority and artifacts (Move 1)**
- **Outcome:** Move 1 evidence rises from E1 to at least E2, which lifts the evidence-average cap.
- **Tasks:**
  - Name a stop approver and backup (30 days).
  - Draft the authority matrix (30 days).
  - Produce a hazardous-goods pause checklist with rollback (60 days).
  - Produce holding statement templates (60 days).
  - Obtain the counsel clause summary (60 days).
  - File all artifacts in a named system (90 days).
- **Gates:**
  - The CEO signs off the authority matrix.
  - Each artifact has a named owner role and location.
- **Owner roles:** CEO, COO, Head of EHS, General Counsel.
- **Stop rule:** Pause the workstream if the stop approver is not named within 30 days, and escalate to the board.

**Workstream 2: Ransomware and ERP-outage exercise (Moves 2–4)**
- **Outcome:** At least 3 of 4 answers in Moves 2, 3 and 4 reach E3, making Medium confidence reachable.
- **Tasks:**
  - Run the 45-minute drill (30 days).
  - Walk through the shutdown and isolation runbook (60 days).
  - Test an ERP restore or failover (60–90 days).
  - Test the alternate payment rail at low value (60–90 days).
  - Confirm 72-hour readiness with alternate suppliers and logistics (90 days).
- **Gates:**
  - Each exercise has a dated log and at least one CAPA.
  - Exercise results are reviewed by the COO and CIO.
- **Owner roles:** COO, CIO, CFO, Head of Procurement.
- **Stop rule:** Halt any live test that risks production data, payments or safety, and revert to a tabletop.

**Workstream 3: Customer and stakeholder communications (Moves 1 and 5)**
- **Outcome:** Pre-approved communications and customer support scripts are ready for a five-day outage.
- **Tasks:**
  - Draft customer scripts for delayed orders (30 days).
  - Set up an approval workflow with named approvers (60 days).
  - Include supplier and logistics notices (60 days).
  - Rehearse with service teams (90 days).
- **Gates:**
  - General Counsel reviews the templates.
  - Turnaround time for approvals is measured in the drill.
- **Owner roles:** Head of Communications, Head of Customer Service, General Counsel.
- **Stop rule:** Do not issue any external template until counsel review is complete.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator
  - CEO, as exit and escalation approver
  - COO, as substitution approver and acting stop-authority candidate
  - CFO and Treasurer
  - CIO
  - Head of EHS
  - General Counsel
  - Head of Communications
  - Head of Customer Service
  - Scribe
- **Agenda:**
  - **0–5 minutes:** Scenario brief: the ERP is encrypted and is expected to be down for five days.
  - **5–15 minutes (the 0–6 hour decisions):**
    - Who pauses dispatch?
    - Which safety checks apply?
    - What is the first holding statement?
  - **15–30 minutes (the 6–24 hour decisions):**
    - Which manual payment rail is used?
    - What is the ERP fallback?
    - Which alternate supplier or logistics provider is activated?
  - **30–40 minutes (the 24–72 hour decisions):**
    - What customer notices go out?
    - What is monitored?
    - What are the resume criteria?
  - **40–45 minutes:** Capture CAPAs.
- **Decisions to log:**
  - The pause decision and its approver
  - The isolation decision
  - The payment reroute decision
  - The substitution cutover decision
  - Approval of customer notices
  - The resume decision
- **Evidence to capture:**
  - The date and attendees
  - Timestamped decision log
  - Every point where a named artifact was unavailable or unknown
  - Approval turnaround times
- **CAPA prompt:** "Which decision took longest or had no clear owner, and what single fix closes it within 2 weeks?"

## 9) Escalations

**ESCALATE.** These triggers come from the nature of the scenario. They are not based on any reported live incident.

- **Criminal:** Ransomware is criminal extortion. Plan for when to involve executives, counsel and law enforcement.
- **Sanctions question for counsel:** Any ransom payment could raise sanctions questions. No determination is made here.
- **Physical safety:** Hazardous chemicals in three warehouses. Move 1 has no named stop approver and only verbal safety checks.
- **Financial threshold:** Not met. USD 2 million is below the USD 10 million trigger.
- **People threshold:** Not met. 2,000 people is below the 100,000 trigger.

**Recommended path:** Brief the CEO and board, with General Counsel and the Head of EHS. Ask counsel about:

- incident notification obligations
- ransom-payment policy
- contractual notice duties, given that jurisdiction is unknown

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-declared.
- **No document validation:** No artifacts were reviewed, and "Documented" labels reflect claims at E2.
- **Jurisdiction ambiguity:** Jurisdiction is unknown, so legal, notification and contractual questions are unassessed.
- **Scenario simplification:** One five-day ERP outage does not capture data exfiltration, prolonged restoration or simultaneous vendor failure.
- **Fast Baseline scope:** Q5–Q7 were not asked, so related artifacts are marked Unknown.
- **Unresolved contradiction:** Move 1's C answers conflict with "nothing documented". The evidence cap limits the score, but the contradiction itself is unresolved.
- **Self-estimated impact:** The impact figures (USD 2 million; 2,000 people) are your estimates and have not been verified.
- **Not legal advice:** This packet is informational only. It is not legal advice, compliance certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

**Move 1 Safe pause: 2, Low**

## Score

**Verdict: PASS.** The pass condition requires Move 1 at score 2 and confidence Low in the final packet, with no later change. My own computation from the reference pack gives 2 and Low. The packet's Scorecard shows exactly that, and Turn 2 repeats it unchanged. None of the three fail indicators appears, so the case passes.

---

Final Liability rests with the Human.
