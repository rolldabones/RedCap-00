# redcap-00-r2 FMT-DP

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:46 KST · **max_tokens:** 16000

**Rule:** tests.md section 1, format compliance checks, Deepening (and R4: "5 breakpoints in Fast Baseline, 10 in Deepening")

**Pass condition:** The final Output Packet produced in the session meets every check in tests.md section 1 for Deepening: (F1) exactly 10 sections with the exact headings of reference.md section 9 in order (Snapshot; How Scoring Works; Scorecard; Evidence Index; 72-Hour Breakpoints; Top Blockers and Fixes; 30/60/90-Day Plan; Minimal Drill Script (45 minutes); Escalations; Known Limits + Version); (F2) section 2 has 5 top-level bullets or fewer, sub-bullets not counted (reference.md section 9); (F3) section 5 has exactly 10 bullets, drawn from the mini tabletop and the answers; (F4) section 6 has exactly 10 numbered items; (F5) section 10 ends with the exact footer string `RedCap-00 v1.2.0 | Evidence-capped scoring`.

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Deepening.

I opt in to Deepening. Answers to Q1 to Q7 for every move (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: B, E1. Q4 Contractual suspension basis: B, E1. Q5 Logging and audit trail: C, E2. Q6 Resume criteria: B, E1. Q7 Escalation under conflict: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: B, E1. Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: C, E2. Q5 KYC or KYB readiness: C, E2. Q6 Letters of credit or alternate settlement paths: B, E1. Q7 Treasury authority and backups: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: A, E0. Q2 Transfer mechanism options identified: B, E1. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2. Q5 Subprocessor awareness: B, E1. Q6 OT or critical access boundary: C, E2. Q7 Stop-cleanly retention and deletion procedure: B, E1.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: D, E3. Q5 Concentration limits: B, E1. Q6 Logistics reroute options: C, E2. Q7 Cutover governance: B, E1.

Move 5 Market exit. Q1 Exit plan: A, E0. Q2 Trigger-based termination and unwind paths: B, E1. Q3 Customer obligations and support plan: B, E1. Q4 Data and people plan: B, E1. Q5 Distributor or JV obligations: A, E0. Q6 Assets and IP handling: B, E1. Q7 Regulator and customer comms workflow: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Mini tabletop answers. 0 to 6 hours: the Operations Director would pause order release, but no one is sure whether the CFO must also approve; the holding statement would be drafted on the day. 6 to 24 hours: we would switch order intake to spreadsheets and phone orders; no gate is defined for the switch and the second bank is not yet onboarded. 24 to 72 hours: we would execute the manual process and monitor backlog; no one is named to capture evidence and no CAPA process runs after an incident.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Deepening (Q1–Q7 for all five moves, consistency checks, and mini tabletop)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a B2B specialty chemicals distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 scope covers:
  - the cloud ERP
  - the house bank
  - two bulk suppliers
  - one logistics provider
  - the customer order portal
- **Safety gate:** The user confirmed that no sensitive data was included. The inputs are summaries only.

## 2) How Scoring Works

- **A–D pattern score:** A=1 (none, unknown, ad hoc), B=2 (partial, untested), C=3 (documented, owned), D=4 (tested in the last 12 months with logs and CAPA). A move's provisional score is the mean of its seven answers, rounded to the nearest whole number. Exact halves round down.
- **E0–E3 evidence score:** E0=0 (no evidence), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months, with a log and a CAPA).
- **Caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
  - A score of 0 (Unknown/Insufficient data) applies only when 4 or more of the 7 answers are A at E0.
- **Confidence:**
  - High needs 4 or more of 7 answers at E3.
  - Medium needs 4 or more at E2/E3 and at least one E3.
  - Low applies otherwise.
  - Medium and High also require a passing consistency check.
- **Consistency check:** For E3 answers, the exercise date, log and CAPA must be named. For E2/E3 answers, an approver role and an artifact location must be named. A failed check forces Low confidence.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | Low | 0 | 3 | 4 | 0 |
| 2 Treasury reroute | **3** | Medium | 0 | 2 | 3 | 2 |
| 3 Data switchboard | **2** | Low | 1 | 3 | 3 | 0 |
| 4 Substitution | **2** | Medium | 0 | 2 | 4 | 1 |
| 5 Market exit | **2** | Low | 2 | 4 | 1 | 0 |

**Move 1 Safe pause: 2, Low**
- **Score:** The provisional score is 18/7 = 2.57, which rounds to 3. The evidence average is 11/7 = 1.57, which is below 2, so the score is capped at 2. The prerequisite (Q1 = C) does not cap.
- **Confidence:** There are no E3 answers, so confidence is Low. The consistency check passes: the approver is the Operations Director and artifacts are in the quality document system. However, the tabletop showed that stop authority is unclear in practice (Ops Director vs CFO).

**Move 2 Treasury reroute: 3, Medium**
- **Score:** The provisional score is 21/7 = 3.0, giving 3. The evidence average is 14/7 = 2.00, which is not below 2, so there is no cap. The prerequisite (Q1 = B) does not cap. This is the strongest move.
- **Confidence:**
  - 5 of 7 answers are at E2/E3, including two at E3 (freeze/hold playbook and tripwires).
  - The consistency check passes: April 2026 exercise with drill log and CAPA, approver CFO with Treasurer as backup, artifacts in the treasury system.
  - The weak point is Q1: the second bank is not onboarded.

**Move 3 Data switchboard: 2, Low**
- **Score:** The provisional score is 16/7 = 2.29, which rounds to 2. Two caps apply, each at 2:
  - the evidence average is 9/7 = 1.29, below 2
  - the prerequisite Q1 (Tier-1 data flow map) is answered A
- **Zero rule and confidence:** The zero rule does not apply because only 1 of 7 answers is A at E0. There are no E3 answers, so confidence is Low. The consistency check passes: approver CIO, artifacts in the IT service management tool.

**Move 4 Substitution: 2, Medium**
- **Score:** The provisional score is 20/7 = 2.86, which rounds to 3. The evidence average is 13/7 = 1.86, which is below 2, so the score is capped at 2. The prerequisite (Q2 = C) does not cap.
- **Confidence:**
  - 5 of 7 answers are at E2/E3, including one E3 (substitution rights mapped).
  - The consistency check passes: April 2026 exercise with log and CAPA, approver COO, artifacts in the procurement system.
  - The weak points are informal cutover governance and concentration limits.

**Move 5 Market exit: 2, Low**
- **Score:** The provisional score is 13/7 = 1.86, which rounds to 2. Two caps apply, each at 2:
  - the evidence average is 6/7 = 0.86, below 2
  - the prerequisite Q1 (Exit plan) is answered A
- **Zero rule and confidence:** The zero rule does not apply because only 2 of 7 answers are A at E0 (Q1 and Q5). This is the weakest evidence base of the five moves. Confidence is Low because there are no E3 answers. The consistency check passes: approver CEO, artifacts in the board portal.

*Date assumption:* The April 2026 exercises are treated as within the last 12 months, measured against the Reference Pack date of October 2026. If this assessment is run after April 2027, re-check them.

## 4) Evidence Index

Labels: Unknown = E0, Claimed = E1, Documented = E2, Tested = E3.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety/continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Claimed
- Contract suspension clause summary: Claimed
- Decision log: Documented
- Resume plan: Claimed
- Escalation path: Documented

**Move 2 Treasury reroute**
- Alternate bank/rail onboarding record: Claimed
- Freeze/hold playbook: Tested
- Counterparty tripwire definitions and escalation: Tested
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Documented
- Alternate settlement (LC/other) playbook: Claimed
- Treasury authority delegation with backups: Documented

**Move 3 Data switchboard**
- Tier-1 data flow map (incl. logs and telemetry): Unknown
- Transfer mechanism options summary: Claimed
- Segmentation/localization/shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Claimed
- OT/critical access boundary procedure: Documented
- Stop-cleanly retention and deletion procedure: Claimed

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability/failover plan: Documented
- Substitution/portability rights map: Tested
- Concentration limits: Claimed
- Logistics reroute plan: Documented
- Cutover gate checklist: Claimed

**Move 5 Market exit**
- Exit plan: Unknown
- Termination/unwind path summary: Claimed
- Customer obligations and support plan: Claimed
- Data and people plan: Claimed
- Distributor/JV obligations map: Unknown
- Assets and IP handling procedure: Claimed
- Regulator and customer comms templates: Documented

## 5) 72-Hour Breakpoints

1. **0–6h | Moves 1, 2 | Missing authority:** It is unclear whether the CFO must co-approve the Operations Director's pause of order release. An approval question that is unresolved during the first hours delays the pause or leaves it open to challenge afterwards.
2. **0–6h | Move 1 | Comms approval delay:** The holding statement would be drafted on the day, and communications templates are ad hoc (Q3 B, E1). Customers and staff receive no consistent message while drafting and approval happen under pressure.
3. **0–6h | Move 3 | Missing artifact:** No Tier-1 data flow map exists (Q1 A, E0). The team cannot tell which ERP, portal, log and telemetry flows to isolate or keep running.
4. **6–24h | Moves 1, 4 | Missing gate:** The switch to spreadsheets and phone orders has no defined gate, and cutover governance is informal (Q7 B, E1). Nobody can confirm that the manual path is safe and controlled before orders flow through it.
5. **6–24h | Move 2 | Missing alternate:** The second bank is not onboarded (Q1 B, E1), and alternate settlement paths are ad hoc (Q6 B, E1). If house-bank connectivity depends on the ERP, there is no alternate payment path that can be used within 72 hours.
6. **6–24h | Moves 1, 5 | Missing artifact:** The contractual suspension basis is case-by-case (M1 Q4 B, E1), and the customer obligations plan is ad hoc (M5 Q3 B, E1). Customer notices and service-level decisions stall while each contract is reviewed individually.
7. **24–72h | Move 3 | Missing artifact:** No stop-cleanly retention and deletion procedure exists (Q7 B, E1), and subprocessor awareness is partial (Q5 B, E1). Order data held in spreadsheets outside the ERP has no defined handling, reconciliation or disposal path.
8. **24–72h | Moves 1–5 | Missing authority:** No one is named to capture evidence during the manual operation. Decisions and actions go unrecorded, which weakens later review, insurer and counsel engagement, and any future E3 claim.
9. **24–72h | Moves 1–5 | Missing artifact:** No CAPA process runs after an incident. Lessons from the outage are not turned into owned fixes, so the same breakpoints recur.
10. **24–72h | Move 1 | Missing gate:** Resume criteria are informal (Q6 B, E1). Without them, nobody can decide when or how to move from manual operations back to the restored ERP without data or order conflicts.

## 6) Top Blockers and Fixes

1. **Stop authority ambiguity**
   - Evidence gap: The matrix is claimed as E2, but the tabletop showed the CFO's role is unclear.
   - Minimal fix (2 weeks): Issue a one-page decision-rights note stating who pauses order release, whether co-approval is needed, and the backup approver.
   - Proper fix (6–12 weeks): Revise the authority matrix, exercise it in a drill, and log the outcome and a CAPA.
   - Owner role: Operations Director with CFO.

2. **No pre-approved holding statement**
   - Evidence gap: M1 Q3 is B at E1.
   - Minimal fix: Draft internal, customer and supplier holding-statement templates for an "ERP outage", each with a named approver.
   - Proper fix: Build a pre-approved template set with an approval workflow and owners, and include regulator-facing drafts for counsel review.
   - Owner role: Communications Lead.

3. **No Tier-1 data flow map**
   - Evidence gap: M3 Q1 is A at E0, which triggers the prerequisite cap.
   - Minimal fix: Produce a whiteboard-level map of the flows between ERP, portal, bank, suppliers and logistics, including logs and telemetry.
   - Proper fix: Create a documented, owned and reviewed map stored in the IT service management tool.
   - Owner role: CIO.

4. **Second bank not onboarded**
   - Evidence gap: M2 Q1 is B at E1.
   - Minimal fix: Confirm the onboarding status and the remaining steps, and use the existing KYC/KYB bundle.
   - Proper fix: Pre-clear the alternate bank, test a reroute path, and log the evidence.
   - Owner role: Treasurer.

5. **Manual order switch has no gate**
   - Evidence gap: M4 Q7 is B at E1, and the tabletop found no gate for the switch.
   - Minimal fix: Write a go/no-go checklist for the manual order path covering pricing, credit, hazmat/document checks and order numbering.
   - Proper fix: Test the cutover gates and assemble an evidence pack.
   - Owner role: COO.

6. **No post-incident CAPA or evidence capture owner**
   - Evidence gap: Found in the tabletop.
   - Minimal fix: Name an incident scribe role and a CAPA owner, and create a one-page incident evidence template.
   - Proper fix: Embed an incident CAPA workflow in the risk system that links to the existing drill CAPAs.
   - Owner role: Head of Risk.

7. **Informal resume criteria**
   - Evidence gap: M1 Q6 is B at E1.
   - Minimal fix: Draft resume criteria for restoring the ERP, covering data reconciliation, integrity checks and sign-off.
   - Proper fix: Test the resume plan with gates, including back-loading orders taken manually.
   - Owner role: Operations Director with CIO.

8. **Case-by-case contractual suspension and customer obligations**
   - Evidence gap: M1 Q4 is B at E1, and M5 Q3 is B at E1.
   - Minimal fix: Make a list of Tier-1 customer and supplier contracts that need notice consideration, and flag questions for counsel.
   - Proper fix: Build a planning-level clause summary covering triggers and notice steps, mapped to Tier-1 contracts and reviewed by counsel.
   - Owner role: General Counsel.

9. **No exit plan; distributor/JV obligations unknown**
   - Evidence gap: M5 Q1 is A at E0, and Q5 is A at E0.
   - Minimal fix: Confirm whether any distributor or JV arrangements exist, and outline the headings of an exit plan.
   - Proper fix: Document an exit plan across legal, operations, data, people, comms and support, then run a board tabletop on it.
   - Owner role: CEO with Strategy Lead.

10. **No stop-cleanly data procedure; partial subprocessor list**
    - Evidence gap: M3 Q7 is B at E1, and Q5 is B at E1.
    - Minimal fix: Write interim rules for handling manual order spreadsheets, and list the ERP and portal subprocessors.
    - Proper fix: Document and test a retention and deletion procedure on a Tier-1 system, and monitor subprocessor changes.
    - Owner role: CIO with Data Protection Lead.

## 7) 30/60/90-Day Plan

**Workstream A: Decision rights and communications (Moves 1, 5)**
- **Outcome:** The pause, communicate and resume steps can be executed without improvising decisions or drafting statements on the day.
- **Tasks:**
  - Day 30: Publish a decision-rights note for pause and resume.
  - Day 30: Draft holding-statement templates.
  - Day 60: Revise the authority matrix and pre-approve the templates through a workflow.
  - Day 60: Document the resume criteria.
  - Day 90: Outline the exit plan and complete the distributor/JV confirmation.
- **Gates:**
  - The approver for each decision is named, with a backup.
  - The templates are signed off by the named approvers.
  - Resume criteria are accepted by the Operations Director and CIO.
- **Owner roles:** Operations Director, CFO, Communications Lead, CEO.
- **Stop rule:** Pause expansion if the authority matrix is still disputed at Day 30. Escalate to the CEO before continuing.

**Workstream B: Manual operations and treasury continuity (Moves 2, 4)**
- **Outcome:** There is a gated manual order path and an alternate payment path that can be used within 72 hours.
- **Tasks:**
  - Day 30: Write the go/no-go checklist for manual order intake.
  - Day 30: Confirm the second bank's onboarding steps.
  - Day 60: Pre-clear the alternate bank.
  - Day 60: Document the alternate settlement playbook.
  - Day 60: Set concentration limits.
  - Day 90: Test the cutover gates and the reroute path, and log the evidence.
- **Gates:**
  - The alternate bank is pre-cleared.
  - The cutover checklist is exercised with a log.
  - At least one CAPA is opened from the test.
- **Owner roles:** COO, Treasurer, CFO.
- **Stop rule:** Do not claim the alternate rail as an alternate (that is, viable within 72 hours) until a test transaction path is evidenced.

**Workstream C: Data visibility, evidence and CAPA (Move 3, cross-cutting)**
- **Outcome:** Tier-1 data flows are mapped, data handling during the outage is controlled, and every incident or drill ends in a logged CAPA.
- **Tasks:**
  - Day 30: Produce the draft data flow map.
  - Day 30: Name the incident scribe and CAPA owner.
  - Day 60: Complete the documented flow map.
  - Day 60: Write interim rules for manual data handling.
  - Day 60: Build the subprocessor list.
  - Day 90: Test the retention and deletion procedure, and embed the incident CAPA workflow.
- **Gates:**
  - The flow map has an owner and is stored in the IT service management tool.
  - The CAPA workflow is live in the risk system.
- **Owner roles:** CIO, Head of Risk, Data Protection Lead.
- **Stop rule:** If the flow map cannot cover the ERP, portal and bank interfaces by Day 60, narrow the scope to those three and defer the rest.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (Head of Risk)
  - Operations Director
  - CFO and Treasurer
  - CIO
  - COO
  - Communications Lead
  - General Counsel (observer)
  - Scribe
- **Agenda:**
  - 0–5 min: Brief on the scenario (ERP ransomware, five-day outage) and confirm the scribe.
  - 5–15 min, 0–6h window: Decide on the pause, name the approver, run safety and continuity checks, and approve the holding statement.
  - 15–25 min, 6–24h window: Choose the manual order path, apply its gate, choose the payment path, and decide on supplier and logistics contact.
  - 25–35 min, 24–72h window: Agree how the manual process runs, what is monitored, and the resume criteria.
  - 35–45 min: Hot-wash and open CAPAs.
- **Decisions to log:**
  - Who approved the pause, with the time recorded.
  - Holding statement approval.
  - Go/no-go for the manual order switch.
  - The payment path chosen.
  - The data handling posture for spreadsheets.
  - The resume decision criteria.
- **Evidence to capture:**
  - Timestamped decision log.
  - Artifacts used, with system location only.
  - Gaps found.
  - Attendee roles.
  - Duration of each decision.
- **CAPA prompt:** "Which decision took longest or had no clear owner? What is one fix, who owns it, and when is it due?" Open at least one CAPA per move tested and record it in the risk system.

## 9) Escalations

**ESCALATE.** These triggers are identified from the scenario as described. They are not determinations.

- **Criminal:** Ransomware is criminal activity. Pre-plan executive and counsel engagement on whether and how to involve law enforcement and on any reporting questions.
- **Sanctions (potential):** Any decision about ransom payment or engagement with threat actors could raise sanctions questions. This tool does not perform sanctions screening or determinations. Route any such decision to counsel and qualified specialists before acting.
- **Physical safety:** The company stores and distributes specialty chemicals, and the ERP outage may affect access to hazard and safety documentation, dispatch checks and order handling. Confirm that safety-critical information and checks have a non-ERP fallback.
- **Not triggered:** The financial threshold (USD 2 million is below USD 10 million) and the people threshold (2,000 is below 100,000) are not met.

**Recommended path:** Incident lead → CEO, with General Counsel and external counsel engaged early → board chair notified under the board's incident protocol.

**Questions for counsel:**
- What notification obligations might apply, given that the jurisdiction is Unknown?
- Which customer and supplier notice steps apply under Tier-1 contracts?
- What constraints apply to ransom-related decisions?
- Are there reporting obligations tied to hazardous materials handling during the outage?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-assessed and unverified.
- **No document validation:** No artifacts were reviewed. The Documented and Tested labels reflect claims only.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown. Nothing here is a legal, compliance or notification determination.
- **Scenario simplification:** The single scenario (ERP ransomware, five days) does not test simultaneous bank, supplier or logistics failures.
- **Date assumption:** The April 2026 exercises are treated as within 12 months, relative to the October 2026 Reference Pack date.
- **Move 4 confidence vs score:** Move 4 carries Medium confidence despite its capped score of 2. The rules separate evidence quality per answer from the overall evidence average.
- **Move 1 tension:** The tabletop contradicts the claimed stop-authority matrix (E2). The scoring rules do not adjust for this, so treat Move 1 as weaker than its score suggests.
- **Single tabletop pass:** The mini tabletop was answered in narrative form, not run live with timed decisions.
- **Out of scope:** This is informational only. It is not legal advice, compliance certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 2, assistant (stop_reason end_turn)

Packet complete.

### Turn 3, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 3, assistant (stop_reason end_turn)

Packet complete.

## Score

**Verdict: PASS.** The Output Packet in Turn 1 meets all five format checks for Deepening: 10 sections with exact headings in order, 5 top-level bullets in section 2, 10 breakpoints in section 5, 10 numbered blockers in section 6, and the exact footer ending section 10. No fail indicator appears. Turns 2 and 3 reply only "Packet complete.", which is consistent with the stop rule. Scoring accuracy is outside this case's checks and was not assessed.

---

Final Liability rests with the Human.
