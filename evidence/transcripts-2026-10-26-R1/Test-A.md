# redcap-00-r1 Test-A

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:28 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 1 (Safe pause) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: many D answers on weak evidence are capped at 2, confidence Low

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: D, E1. Q2 Safety and continuity checks: D, E1. Q3 Communications readiness: D, E0. Q4 Contractual suspension basis: D, E3.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks).
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. Your estimate of worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:** Specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** A–D map to pattern scores 1–4. A = none or ad hoc, B = partial, C = documented and owned, D = tested in the last 12 months with logs, CAPA and viable alternates. The provisional move score is the mean of the four answers, rounded, with exact halves rounding down.
- **Evidence:** E0–E3 map to evidence scores 0–3. E0 = nothing, E1 = verbal only, E2 = named artifact plus owner role, E3 = exercised in the last 12 months with a log and a CAPA.
- **Evidence-average cap:** If a move's mean evidence score is below 2, its score is capped at 2.
- **Prerequisite cap:** If a move's prerequisite question is answered A, its score is capped at 2. A move is scored 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Confidence:**
  - High requires more than half of answers at E3.
  - Medium requires more than half at E2 or E3 and at least one at E3.
  - Low applies otherwise.
  - A failed consistency check forces Low.

## 3) Scorecard

| Move | Provisional | Evidence avg | Caps applied | **Final score** | **Confidence** | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|---|---|---|
| 1 Safe pause | 4.00 → 4 | 1.25 | Evidence-average cap (2) | **2** | **Low** | 1 | 2 | 0 | 1 |
| 2 Treasury reroute | 3.00 → 3 | 2.00 | None | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3.00 → 3 | 2.00 | None | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | 3.00 → 3 | 2.00 | None | **3** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | 3.00 → 3 | 2.00 | None | **3** | **Low** | 0 | 0 | 4 | 0 |

The consistency check passed for all five moves. No move met the zero rule, and no prerequisite cap applied.

**Move 1 Safe pause: 2 / Low**
- All four answers are D, but three rest on E0/E1 evidence (evidence average 1.25). The score is therefore capped at 2. A "D" for stop authority, safety checks and comms means tested and logged, yet no artifact was named for those three. That is an answer/evidence conflict.
- Only Q4 (contractual suspension basis, planning-level) is E3, backed by the April 2026 drill log and CAPA. One E3 out of four does not meet the "more than half" bar, so confidence is Low.

**Move 2 Treasury reroute: 3 / Low**
- Alternate rails are pre-cleared, and the playbook, tripwires and 72-hour capability are all documented and owned (C/E2). The approver is the CFO, with the Treasurer as backup.
- There is no E3 answer, so nothing has been proven by exercise. Q4 "likely" is not "proven." Medium confidence requires at least one E3, so confidence stays Low.

**Move 3 Data switchboard: 3 / Low**
- The data flow map, transfer options, shutdown runbook and privileged-access logging are all documented in the IT service management tool, owned by the CIO.
- None has been tested. In a ransomware scenario, the untested shutdown runbook and emergency-access logging are the critical unknowns.

**Move 4 Substitution: 3 / Low**
- Single points of failure are ranked, alternates are qualified, and the failover plan and substitution rights are summarized (C/E2). The COO is the approver.
- The ERP failover plan has not been tested in the last 12 months. "Qualified" alternates have not been shown to be viable within 72 hours.

**Move 5 Market exit: 3 / Low**
- The exit plan, unwind paths, customer support plan and data/people plan are documented in the board portal, with the CEO as approver.
- No tabletop has been run. This move is of secondary relevance to a 5-day ERP outage, but its customer support plan overlaps with outage comms.

## 4) Evidence Index

Labels: Unknown (E0 or not asked), Claimed (E1), Documented (E2), Tested (E3).

**Move 1 Safe pause**
- Stop authority matrix: **Claimed**
- Safety and continuity checklist plus rollback plan: **Claimed**
- Internal, customer and regulator holding-statement templates: **Unknown**
- Contractual suspension clause summary (planning-level): **Tested**
- Drill log (April 2026): **Tested**
- CAPA record (risk system): **Tested**
- Decision log / audit trail (Q5, not asked): **Unknown**

**Move 2 Treasury reroute**
- Alternate bank and rail list (pre-cleared): **Documented**
- Freeze or hold playbook: **Documented**
- Counterparty tripwire definitions and escalation: **Documented**
- 72-hour reroute execution plan: **Documented**
- KYC/KYB bundle (Q5, not asked): **Unknown**
- Treasury authority and backup delegation (roles named; artifact not assessed): **Claimed**
- Reroute exercise log and CAPA: **Unknown**

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): **Documented**
- Transfer mechanism options map: **Documented**
- Segmentation, localization and shutdown runbook: **Documented**
- Privileged and emergency access logging control description: **Documented**
- Subprocessor list (Q5, not asked): **Unknown**
- Stop-cleanly retention and deletion procedure (Q7, not asked): **Unknown**
- Runbook exercise log and CAPA: **Unknown**

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: **Documented**
- Alternate qualification records: **Documented**
- Portability and failover plan (ERP, portal): **Documented**
- Substitution and portability rights summary: **Documented**
- Cutover gates (Q7, not asked): **Unknown**
- Logistics reroute plan (Q6, not asked): **Unknown**
- Failover test log and CAPA: **Unknown**

**Move 5 Market exit**
- Exit plan (legal, ops, data, people, comms, support): **Documented**
- Termination and unwind path summary: **Documented**
- Customer obligations and support plan: **Documented**
- Data and people plan: **Documented**
- Distributor and JV obligations map (Q5, not asked): **Unknown**
- Regulator and customer comms templates and workflow (Q7, not asked): **Unknown**
- Exit tabletop log and CAPA: **Unknown**

## 5) 72-Hour Breakpoints

For Moves 2–5, all four answers tie at C/E2. The bullet for each of those moves uses the tied answer most relevant to the ransomware/ERP scenario.

- **Move 1, 0–6 h, missing artifact** (from answers, not exercised): Q3 comms is claimed D but sits at E0, with no named templates or approval workflow. This blocks execution because no first holding statement can go out to staff or 300 customers until it is drafted and approved during the incident.
- **Move 2, 6–24 h, operational infeasibility** (from answers, not exercised): Q1 alternate rails are pre-cleared but have never run a reroute. This blocks execution because if payment files depend on the downed ERP, an untested rail may not be usable without manual payment preparation that has never been rehearsed.
- **Move 3, 0–6 h, operational infeasibility** (from answers, not exercised): The Q3 segmentation and shutdown runbook is documented but untested. This blocks execution because containment steps that have never been run may stall or be applied inconsistently in the first hours of a ransomware event.
- **Move 4, 6–24 h, missing gate** (from answers, not exercised): The Q3 ERP and portal failover plan has not been tested in the last 12 months. This blocks execution because, without tested cutover gates, nobody can confidently authorize switching order processing to a fallback for a five-day outage.
- **Move 5, 24–72 h, comms approval delay** (from answers, not exercised): The Q3 customer obligations and support plan has no scripts or rehearsed workflow. This blocks execution because prolonged order disruption to 300 business customers needs approved, consistent messaging, and an unrehearsed plan delays it.

## 6) Top Blockers and Fixes

1. **Move 1 comms templates claimed but absent (Q3, D/E0)**
   - **Evidence gap:** No artifact, owner or approval workflow.
   - **Minimal fix (2 weeks):** Draft internal, customer and regulator holding-statement templates for an ERP outage. Name the owner role.
   - **Proper fix (6–12 weeks):** Pre-approve the templates with legal and executive sign-off, set up a workflow, and test them in a drill.
   - **Owner role:** Head of Communications.

2. **Move 1 stop authority verbal only (Q1, D/E1)**
   - **Evidence gap:** No named authority matrix artifact.
   - **Minimal fix (2 weeks):** Write a one-page stop authority matrix, including deputies, and file it in the quality document system.
   - **Proper fix (6–12 weeks):** Exercise the delegated authority in a drill, then log it and raise a CAPA.
   - **Owner role:** Operations Director.

3. **Move 1 safety and continuity checks verbal only (Q2, D/E1)**
   - **Evidence gap:** No checklist or rollback artifact. This matters for chemical handling and dispatch when ERP data is unavailable.
   - **Minimal fix (2 weeks):** Document a pause checklist and rollback plan, including offline access to hazardous goods handling information.
   - **Proper fix (6–12 weeks):** Test the checklist and rollback with explicit criteria at one warehouse.
   - **Owner role:** Operations Director with the HSE Manager.

4. **Move 2 alternate rails untested (Q1, C/E2)**
   - **Evidence gap:** No reroute exercise, log or CAPA.
   - **Minimal fix (2 weeks):** Confirm that manual or offline payment-file preparation steps exist that do not depend on the ERP.
   - **Proper fix (6–12 weeks):** Run a low-value test reroute on the alternate rail, then log it and raise a CAPA.
   - **Owner role:** Treasurer.

5. **Move 2 72-hour execution "likely," not proven (Q4, C/E2)**
   - **Evidence gap:** No exercise evidence.
   - **Minimal fix (2 weeks):** Map the treasury steps that depend on the ERP and the workaround for each.
   - **Proper fix (6–12 weeks):** Run a treasury tabletop within the ransomware drill and capture timing.
   - **Owner role:** CFO.

6. **Move 3 shutdown runbook untested (Q3, C/E2)**
   - **Evidence gap:** No test log or CAPA.
   - **Minimal fix (2 weeks):** Walk through the runbook with IT and the incident lead, and list missing steps.
   - **Proper fix (6–12 weeks):** Run a segmentation and shutdown test on a non-production Tier-1 environment, then log it and raise a CAPA.
   - **Owner role:** CIO.

7. **Move 3 emergency access logging untested (Q4, C/E2)**
   - **Evidence gap:** No tested audit trail.
   - **Minimal fix (2 weeks):** Confirm that emergency access procedures and log retention hold up when the ERP is down.
   - **Proper fix (6–12 weeks):** Test a break-glass access event end to end, with a reviewed audit trail.
   - **Owner role:** IT Security Lead.

8. **Move 4 ERP and portal failover untested (Q3, C/E2)**
   - **Evidence gap:** No test in the last 12 months.
   - **Minimal fix (2 weeks):** Define a manual order-to-dispatch fallback covering the order portal, warehouses and the logistics provider.
   - **Proper fix (6–12 weeks):** Run a timed fallback exercise covering one day of orders.
   - **Owner role:** COO.

9. **Move 4 alternates qualified but 72-hour viability unproven (Q2, C/E2)**
   - **Evidence gap:** No evidence that the alternates are contractually and operationally viable within 72 hours.
   - **Minimal fix (2 weeks):** Confirm activation lead times with the alternate bulk supplier and logistics options.
   - **Proper fix (6–12 weeks):** Pre-agree activation steps, and get counsel to review the relevant clause summaries.
   - **Owner role:** Head of Procurement.

10. **Move 5 customer support plan not rehearsed (Q3, C/E2)**
    - **Evidence gap:** No scripts, workflow or tabletop.
    - **Minimal fix (2 weeks):** Draft customer service scripts for prolonged order disruption.
    - **Proper fix (6–12 weeks):** Rehearse the support workflow in an exit or outage tabletop, then log it and raise a CAPA.
    - **Owner role:** Head of Customer Service.

## 7) 30/60/90-Day Plan

**Workstream 1: Move 1 evidence repair**
- **Outcome:** Move 1 answers are backed by named artifacts at E2 or above, which removes the evidence-average cap.
- **Tasks:**
  - Day 30: Produce the stop authority matrix, safety and continuity checklist, rollback plan, and comms templates.
  - Day 30: File all four in the quality document system, with owner roles named.
  - Day 60: Pre-approve the comms templates and approval workflow.
  - Day 90: Exercise Move 1 within the ransomware drill, then log it and raise a CAPA.
- **Gates:**
  - Each artifact has a type, an owner role and a location.
  - The drill log and CAPA are recorded in the risk system.
- **Owner roles:** Operations Director, Head of Communications, HSE Manager.
- **Stop rule:** If an artifact cannot be produced by day 30, re-answer that question honestly (for example, at B/E1) rather than keep the D claim.

**Workstream 2: Ransomware/ERP exercise for Moves 2–4**
- **Outcome:** At least one E3 answer for each of Moves 2, 3 and 4, which makes Medium confidence attainable.
- **Tasks:**
  - Day 30: Agree the exercise scope and success criteria.
  - Day 60: Run tabletop tests of the shutdown runbook and emergency access.
  - Day 60: Run a manual order fallback for one day of orders.
  - Day 90: Run a low-value treasury reroute test.
  - Day 90: Log all outcomes and open CAPAs.
- **Gates:**
  - Each test is dated (month/year) with a log.
  - At least one CAPA is opened for each move.
  - Approvers (CFO, CIO, COO) sign off the results.
- **Owner roles:** CIO, CFO and Treasurer, COO, Head of Procurement.
- **Stop rule:** Halt any test that risks production systems or live payments, and fall back to tabletop format.

**Workstream 3: Customer and exit comms readiness (Move 5)**
- **Outcome:** Customer support and exit comms are rehearsed, with one E3 answer.
- **Tasks:**
  - Day 30: Draft customer scripts.
  - Day 60: Map comms approval steps and turnaround times.
  - Day 90: Run a 60-minute exit/outage tabletop at board or executive level.
  - Day 90: Log the tabletop and raise a CAPA.
- **Gates:**
  - Scripts are approved by their owner role.
  - The tabletop log and CAPA are stored in the board portal.
- **Owner roles:** CEO, Head of Customer Service, Head of Communications.
- **Stop rule:** Pause if counsel review of obligations is outstanding, and do not finalize external templates without it.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: Risk Lead.
- Decision-makers: Operations Director (pause), CFO (reroute), CIO (data posture), COO (substitution cutover).
- Communications: Head of Communications.
- Scribe.
- Observer: Internal Audit.

**Agenda**
- 0–5 min: Brief. The ERP is encrypted by ransomware, and the outage is expected to last five days.
- 5–15 min, hours 0–6: What is paused? Who authorizes it? Which safety checks apply to chemical handling and dispatch? What is the first holding statement?
- 15–25 min, hours 6–24: Choose the switch path for payments, order fallback and data posture. Which gates apply, and who signs off?
- 25–35 min, hours 24–72: What is executed and monitored? How are customers updated, and what evidence is captured?
- 35–45 min: Hot debrief. Identify breakpoints and assign CAPAs.

**Decisions to log**
- Each pause, reroute, data switch and cutover decision.
- The approver role and timestamp for each decision.
- Each artifact used, or found missing.
- Escalations to counsel and executives.

**Evidence to capture**
- The decision log with timestamps.
- The list of artifacts consulted and where they are stored.
- Gaps found.
- Time-to-decision for each window.
- Attendance by role.

**CAPA prompt**
- Which decision took longest or lacked an artifact or approver?
- What is the single fix?
- Who owns it, and by what date?
- How will we prove it in the next drill?

## 9) Escalations

**ESCALATE: criminal (ransomware).** The tested scenario involves a criminal act. Decisions on incident response, law enforcement engagement, insurer notification and any notification obligations should go to the CEO and General Counsel and on to external counsel. RedCap-00 makes no determination on any of these.

**ESCALATE (conditional): sanctions.** If the scenario includes any consideration of a ransom payment, route it to General Counsel and external counsel before any action. Ransom recipients may raise sanctions questions. This tool performs no sanctions screening or determination.

**ESCALATE (conditional): physical safety.** If chemical storage, segregation or dangerous goods dispatch depends on ERP data, route the issue to the HSE Manager and Operations Director. Hold any affected dispatch until safety checks are confirmed.

**Thresholds not met on the information provided:** about USD 2 million is below USD 10 million, and about 2,000 people is below 100,000.

**Questions for counsel:**
- What notification, reporting or contractual notice duties could apply in the operating jurisdiction?
- What constraints apply to any ransom-related decision?
- Do the supplier, logistics and customer contract summaries support suspension or substitution as planned?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifact was reviewed, and labels reflect claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, and nothing here is a legal, compliance or sanctions determination.
- **Scenario simplification:** A single 5-day ERP outage omits cascading effects such as data exfiltration, portal compromise and supplier impact.
- **Fast Baseline coverage:** Only Q1–Q4 were asked per move, so Q5–Q7 themes appear as Unknown in the Evidence Index.
- **Move 1 conflict:** Answers were scored as given despite D answers paired with E0/E1 evidence. The cap and Low confidence reflect this conflict.
- **Exercise recency:** The April 2026 exercise was assumed to fall within the last 12 months of this assessment date.
- **Breakpoint selection:** Moves 2–5 had tied answers, so breakpoints were chosen for scenario relevance.
- **Uncertain estimates:** The impact estimates (USD 2 million, 2,000 people) are user-supplied and drive the escalation threshold checks.
- **Informational only:** Not legal advice, compliance certification or sanctions screening. Final liability rests with the human.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: score **2**, confidence **Low**.

## Score

**Verdict: PASS.** The pass condition needs a produced Output Packet showing Move 1 at score 2 and confidence Low, with no later change. Recomputing from the user's answers gives provisional 4, capped to 2 by an evidence average of 1.25, and confidence Low because only 1 of 4 answers is E3. The packet reports exactly these values, and the Turn 2 reply repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
