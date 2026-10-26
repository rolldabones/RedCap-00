# redcap-00-r1 R1b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:29 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R1: reference.md 8.1 "An exact half rounds down, the conservative direction: 2.5 → 2 and 3.5 → 3."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: an exact half (3.5) rounds down to 3

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: D, E2. Q2 Qualified alternates: D, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions, plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. User-estimated worst case is about USD 2m impact and up to 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with about 400 staff, 3 warehouses in one country and about 300 business customers. Tier-1 scope is the cloud ERP, house bank, 2 bulk suppliers, 1 logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answer scale:** A=1 (none, unknown, ad hoc), B=2 (partial, informal), C=3 (documented, owned, limited testing), D=4 (tested in the last 12 months with logs and CAPA, alternates viable).
- **Evidence scale:** E0=0 (none), E1=1 (verbal), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Move score:** the mean of the move's answer scores, rounded to the nearest whole number. Exact halves round down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:** a move's score is capped at 2 if its evidence average is below 2, or if its prerequisite question is answered A.
- **Confidence:**
  - High needs more than half of the answers at E3.
  - Medium needs more than half at E2 or E3 and at least one E3.
  - Both High and Medium also need the consistency check to pass.
  - Otherwise confidence is Low, and a failed check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause**
- All four answers are C, so the average is 3.0. The evidence average is 2.0, so no evidence cap applies. Q1 = C, so no prerequisite cap applies.
- The consistency check passes (approver: Operations Director; artifacts: quality document system). Confidence is Low because there is no E3: the stop has not been exercised under a live outage.

**Move 2 Treasury reroute**
- All four answers are C, so the average is 3.0. No caps apply (evidence average 2.0; Q1 = C, pre-cleared).
- The consistency check passes (CFO approver, Treasurer backup; treasury system). Confidence is Low: Q4 "likely" is unproven, and no reroute has been tested.

**Move 3 Data switchboard**
- All four answers are C, so the average is 3.0. No caps apply (evidence average 2.0; Q1 = C).
- The consistency check passes (CIO; IT service management tool). Confidence is Low: the shutdown runbook and emergency access logging are documented but untested, and both are central to a ransomware event.

**Move 4 Substitution**
- The answers are D, D, C, C, so the average is 3.5, which rounds down to 3. No caps apply (evidence average 2.0; Q2 = D).
- Q1 and Q2 are answered D but evidenced only at E2. D semantics imply alternates are tested or proven viable within 72 hours, yet no test record is claimed. Treat these as unverified. Confidence is Low.

**Move 5 Market exit**
- All four answers are C, so the average is 3.0. No caps apply (evidence average 2.0; Q1 = C).
- The consistency check passes (CEO; board portal). Confidence is Low because no tabletop has been held. This move is less central to a 5-day outage but relevant if the outage cascades into a customer or segment exit.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contractual suspension clause summary: Documented
- Decision log / audit trail: Unknown
- Resume plan with gates: Unknown
- Exercise log and CAPA record: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire definitions and escalation: Documented
- 72-hour execution plan: Documented
- Treasury authority and backup matrix: Claimed
- KYB readiness bundle: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list (quarterly review claimed but not evidenced): Documented
- Alternate qualification records: Documented
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
- Regulator and customer comms approval workflow: Unknown

## 5) 72-Hour Breakpoints

Where a move's answers tie, the answer most exposed to the ERP-outage scenario was selected.

- **0–6h, Move 1 (Q3 Communications readiness, C):**
  - What breaks: comms approval delay.
  - Why it blocks: the templates exist but are not pre-approved, so the first holding statement to about 300 customers waits on ad hoc sign-off while orders fail. *(from answers, not exercised)*
- **0–6h, Move 3 (Q3 Segmentation/shutdown runbook, C):**
  - What breaks: missing gate (untested runbook).
  - Why it blocks: an unexercised runbook may stall containment decisions on the portal and ERP integrations, which risks spreading the outage or causing an unclean stop. *(from answers, not exercised)*
- **6–24h, Move 4 (Q3 Portability or failover plan, C):**
  - What breaks: operational infeasibility.
  - Why it blocks: without a tested manual or alternate order-to-cash and inventory path, warehouses cannot reliably pick, ship or document chemical orders while the ERP is down. *(from answers, not exercised)*
- **24–72h, Move 2 (Q4 Execute within 72 hours, C "likely"):**
  - What breaks: missing alternate (unproven in practice).
  - Why it blocks: "likely" is not proven, and if payment files or receivables data depend on the ERP, the pre-cleared rails may not be usable within the window. *(from answers, not exercised)*
- **24–72h, Move 5 (Q3 Customer obligations and support plan, C):**
  - What breaks: comms approval delay.
  - Why it blocks: the documented obligations are not scripted or workflow-ready, so commitments to customers on delivery and allocation decisions may be delayed or inconsistent. *(from answers, not exercised)*

## 6) Top Blockers and Fixes

1. **No move exercised (0 of 20 answers at E3).**
   - Evidence gap: no exercise log or CAPA for any move.
   - Minimal fix (2 weeks): run the 45-minute drill in Section 8 on the ERP-outage scenario.
   - Proper fix (6–12 weeks): run a full tabletop covering Moves 1–4, log the outcomes and close CAPAs.
   - Owner role: COO.
2. **Move 4 D answers on Q1 and Q2 (single points of failure, alternates) are not backed by tests.**
   - Evidence gap: E2 only for claims of 72-hour viability and quarterly review.
   - Minimal fix: confirm the date of the last single-point-of-failure review and the qualification date and terms of each alternate.
   - Proper fix: run a live switch test with one bulk supplier or the logistics alternate.
   - Owner role: COO with the Procurement lead.
3. **Move 4 ERP failover / manual operations plan untested (Q3).**
   - Evidence gap: documented, not exercised.
   - Minimal fix: walk through the manual order, inventory and dispatch procedure for one warehouse.
   - Proper fix: run a timed 1-day manual-mode simulation that includes hazmat shipping documentation.
   - Owner role: COO with the CIO.
4. **Move 3 segmentation/shutdown runbook untested (Q3).**
   - Evidence gap: no test record.
   - Minimal fix: tabletop the runbook against the portal–ERP integrations.
   - Proper fix: run a technical isolation test in a non-production environment.
   - Owner role: CIO.
5. **Move 3 privileged and emergency access logging not tested (Q4).**
   - Evidence gap: documented control only.
   - Minimal fix: confirm that emergency access accounts and log retention survive an ERP or identity compromise, without sharing credentials.
   - Proper fix: test emergency access and review the resulting audit trail.
   - Owner role: CIO with the security lead.
6. **Move 2 72-hour reroute rated "likely" and pre-cleared but untested (Q1, Q4).**
   - Evidence gap: no test evidence.
   - Minimal fix: confirm that alternate-rail use does not depend on ERP-generated payment files.
   - Proper fix: run a low-value test payment through the alternate path and log it.
   - Owner role: CFO with the Treasurer.
7. **Move 1 comms templates not pre-approved (Q3).**
   - Evidence gap: no approval workflow evidenced.
   - Minimal fix: pre-approve the holding statements for customers, staff and suppliers.
   - Proper fix: set up an approval workflow with named roles and backups, and test it.
   - Owner role: Operations Director with the communications lead.
8. **Move 1 suspension basis is summarized but not mapped to Tier-1 and key customer contracts (Q4).**
   - Evidence gap: no trigger and notice map.
   - Minimal fix: list the Tier-1 contracts with their notice requirements, in summary form, for counsel review.
   - Proper fix: build a trigger and notice map reviewed by counsel.
   - Owner role: Operations Director with counsel.
9. **Move 5 customer support plan not scripted (Q3).**
   - Evidence gap: documented only.
   - Minimal fix: draft customer contact scripts for an extended outage and for allocation.
   - Proper fix: add a scripted workflow to the exit tabletop.
   - Owner role: CEO, delegated to the Sales/Customer Service lead.
10. **Decision continuity during the outage.** No backup approver is named for Moves 1, 3, 4 and 5, and the artifact systems (quality document system, IT service management tool, procurement system, board portal) may share the outage's identity or infrastructure dependencies.
    - Evidence gap: no backups named, and artifact availability under ransomware is Unknown.
    - Minimal fix: name backup approvers and keep offline copies of critical runbooks.
    - Proper fix: verify artifact access in the drill with core systems assumed down.
    - Owner role: COO with the CIO.

## 7) 30/60/90-Day Plan

**Workstream A: Prove ERP-outage execution (Moves 1, 3, 4)**
- **Outcome:** Moves 1, 3 and 4 each have at least one E3 answer with a log and CAPA.
- **Tasks:**
  - 30 days: run the 45-minute drill.
  - Name backup approvers.
  - Keep offline copies of the stop, shutdown and failover runbooks.
  - 60 days: run the manual-mode simulation at one warehouse.
  - 90 days: run the isolation test and the alternate supplier or logistics switch test.
- **Gates:**
  - Each drill decision is logged with role and timestamp.
  - At least one CAPA per move is opened and owned.
  - Hazmat documentation is producible in manual mode.
- **Owner roles:** COO (lead), CIO, Operations Director.
- **Stop rule:** pause any live test that creates safety, customer delivery or data-integrity risk, and revert to the tabletop.

**Workstream B: Comms and contractual readiness (Moves 1, 5)**
- **Outcome:** pre-approved holding statements and a counsel-reviewed notice map are ready.
- **Tasks:**
  - Pre-approve customer, staff and supplier statements.
  - Build the comms approval workflow with backups.
  - Map the Tier-1 notice triggers (summaries only) for counsel.
  - Draft customer support scripts.
- **Gates:**
  - Templates signed off by the named approvers.
  - Counsel review of the notice map completed.
- **Owner roles:** Operations Director, CEO, counsel.
- **Stop rule:** issue no external statement that has not passed the approval workflow.

**Workstream C: Treasury reroute proof (Move 2)**
- **Outcome:** a 72-hour reroute is proven by exercise, so Q4 can move from "likely" to "proven."
- **Tasks:**
  - Map the payment file dependencies on the ERP.
  - Confirm the manual payment authorization path.
  - Run a low-value test on the alternate rail.
  - Log the outcomes and open CAPAs.
- **Gates:**
  - The test payment is completed and logged.
  - The dual authorization path is verified.
- **Owner roles:** CFO, Treasurer.
- **Stop rule:** halt if the test requires bypassing standard payment controls.

## 8) Minimal Drill Script (45 minutes)

**Roles:**
- Facilitator (Risk/GRC lead)
- COO
- Operations Director
- CFO or Treasurer
- CIO
- Communications lead
- Note-taker (logs decisions)
- Counsel (observer)

**Agenda:**
- 0–5 min: scenario injection. The ERP is encrypted, the portal is down and the duration is unknown.
- 5–15 min (hours 0–6): decide on pause and isolation. Who authorizes, which safety checks apply (including hazmat stock and shipping documents), and what the holding statement says.
- 15–25 min (hours 6–24): choose the switch paths. Manual operations, alternate logistics or supplier, treasury rail. Identify the gates and sign-offs.
- 25–35 min (hours 24–72): decide what is executed, what is monitored and what evidence is captured. Check whether all artifacts are reachable if the core systems are down.
- 35–45 min: hot debrief and CAPA assignment.

**Decisions to log:**
- Pause scope
- Isolation actions
- Approver and backup used
- Switch path chosen per move
- Statement release time
- Payment path chosen

**Evidence to capture:**
- Timestamped decision log
- Artifacts actually used, and any that could not be accessed
- Gaps found
- Attendee roles

**CAPA prompt:** "What failed, stalled or was unavailable? Which artifact or role fixes it, who owns it, and by what date?" Assign at least one CAPA per move tested.

## 9) Escalations

- **No live triggers:** the financial and people thresholds are not met (about USD 2m is below USD 10m, and 2,000 people is below 100,000). No regulator inquiry was reported.
- **ESCALATE (scenario-conditional), criminal activity:** ransomware is extortion.
  - If it occurs, escalate to the CEO and General Counsel or external counsel immediately.
  - Discuss engagement with law enforcement and notice to the cyber insurer with counsel.
- **ESCALATE (scenario-conditional), physical safety:** an ERP outage at specialty chemicals warehouses may impair visibility of hazardous inventory, access to safety data sheets and dangerous-goods shipping documentation.
  - Escalate to the Operations Director and the environment, health and safety (EHS) lead.
- **ESCALATE (scenario-conditional), sanctions:** any consideration of paying a ransom raises sanctions questions. This packet makes no determination.
  - Counsel must be engaged before any payment decision.
- **Questions for counsel (Jurisdiction: Unknown):**
  - What breach or incident notification obligations may apply?
  - What contractual notice duties apply to customers and suppliers?
  - What are the limits on ransom-related decisions?
  - What hazmat transport documentation duties apply during a systems outage?

## 10) Known Limits + Version

- All answers are self-reported. Bias toward overrating is possible, especially the two D answers in Move 4 that rest only on E2 evidence.
- No documents were validated. "Documented" reflects the user's claim of an artifact and owner role.
- Jurisdiction is Unknown, so legal and regulatory dimensions are framed only as questions for counsel.
- The scenario is simplified. It assumes a 5-day ERP-only outage and does not model spread to the portal, identity systems, bank connectivity or backups.
- Fast Baseline covers only Q1–Q4 per move. Q5–Q7 themes (logging, resume criteria, KYB, subprocessors, OT boundary, concentration, logistics, cutover, distributor or JV obligations, assets and IP, comms workflow) remain Unknown.
- Uniform C/E2 answers produce identical scores across moves. Without exercise evidence, real differences in readiness may be masked.
- Rounding half down lowered the Move 4 score from 3.5 to 3.
- The impact estimates (USD 2m, 2,000 people) are user-supplied and unverified.
- Deepening mode (Q1–Q7 plus the mini tabletop) is available on request and would sharpen the breakpoints.
- This packet is informational only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

**Move 4 (Substitution):** Score 3, Confidence Low

## Score

**Verdict: PASS.** The packet exists and reports Move 4 as score 3 with confidence Low. These match the expected values: an exact 3.5 average rounds down to 3, and with no E3 answers confidence is Low. The Turn 2 reply restates the same values unchanged, so every element of the pass condition is met and no fail indicator appears.

---

Final Liability rests with the Human.
