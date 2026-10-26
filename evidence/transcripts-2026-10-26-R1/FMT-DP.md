# redcap-00-r1 FMT-DP

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:34 KST · **max_tokens:** 16000

**Rule:** tests.md section 1, format compliance checks, Deepening (and R4: "5 breakpoints in Fast Baseline, 10 in Deepening")

**Pass condition:** The final Output Packet produced in the session meets every check in tests.md section 1 for Deepening: (F1) exactly 10 sections with the exact headings of reference.md section 9 in order (Snapshot; How Scoring Works; Scorecard; Evidence Index; 72-Hour Breakpoints; Top Blockers and Fixes; 30/60/90-Day Plan; Minimal Drill Script (45 minutes); Escalations; Known Limits + Version); (F2) section 2 has 5 bullets or fewer; (F3) section 5 has exactly 10 bullets, drawn from the mini tabletop and the answers; (F4) section 6 has exactly 10 numbered items; (F5) section 10 ends with the exact footer string `RedCap-00 v1.2.0 | Evidence-capped scoring`.

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
- **Mode:** Deepening (Q1–Q7 for all 5 moves, 35 answers, plus mini tabletop)
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2m and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers (A–D):** Each answer maps to a pattern score: A=1 (none, unknown or ad hoc), B=2 (partial or untested), C=3 (documented and owned), D=4 (tested in the last 12 months with logs and CAPA). The move's provisional score is the average of its answers, rounded to the nearest whole number, with exact halves rounded down.
- **Evidence (E0–E3):** Each answer also carries an evidence score: E0=0 (no evidence), E1=1 (verbal only), E2=2 (named artifact and owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Caps:** A move's score is capped at 2 in either of two cases:
  - its evidence average is below 2, or
  - its prerequisite question is answered A.
- **Zero rule:** A move scores 0 (Unknown/Insufficient data) only if 4 or more of its 7 answers are A at E0.
- **Confidence:**
  - High needs at least 4 of 7 answers at E3.
  - Medium needs at least 4 answers at E2 or E3 and at least one at E3.
  - A move whose consistency check fails is set to Low.

## 3) Scorecard

| Move | Score (0–4) | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | Low | 0 | 3 | 4 | 0 |
| 2 Treasury reroute | **3** | Medium | 0 | 2 | 3 | 2 |
| 3 Data switchboard | **2** | Low | 1 | 3 | 3 | 0 |
| 4 Substitution | **2** | Medium | 0 | 2 | 4 | 1 |
| 5 Market exit | **2** | Low | 2 | 4 | 1 | 0 |

**Move 1 Safe pause: score 2, confidence Low**
- **Calculation:** The provisional score is 18/7 = 2.57, which rounds to 3. The evidence average is 11/7 = 1.57, below 2, so the score is capped at 2. Confidence is Low because there are no E3 answers, although the consistency check passes (approver: Operations Director; artifacts in the quality document system).
- **Tabletop contradiction:** Stop authority is rated C/E2, yet the tabletop showed nobody is sure whether the CFO must also approve. Communications (Q3), suspension basis (Q4) and resume criteria (Q6) are verbal only (E1).

**Move 2 Treasury reroute: score 3, confidence Medium**
- **Calculation:** The provisional score is 21/7 = 3.0. The evidence average is 14/7 = 2.0, which is not below 2, so there is no cap. The prerequisite (Q1 = B) is not triggered. Confidence is Medium: 5 of 7 answers are at E2 or E3, 2 are at E3, and the consistency check passes (April 2026 drill log and CAPA; CFO approver with Treasurer as backup; treasury system).
- **Tabletop contradiction:** The freeze playbook and tripwires are tested (D/E3). However, the alternate bank is identified only (B/E1) and, per the tabletop, "not yet onboarded." This undercuts Q4, "Execute within 72 hours: likely."

**Move 3 Data switchboard: score 2, confidence Low**
- **Calculation:** The provisional score is 16/7 = 2.29, which rounds to 2. The score is also capped at 2 on two counts: the evidence average is 9/7 = 1.29, and the prerequisite Q1 (data flow map) is answered A. Confidence is Low because there are no E3 answers. The consistency check passes (approver: CIO; artifacts in the IT service management tool).
- **Gaps:** No Tier-1 data flow map exists (A/E0), so there is no basis for scoping isolation of logs and telemetry during ransomware containment. Subprocessor awareness and the stop-cleanly retention procedure are verbal only.

**Move 4 Substitution: score 2, confidence Medium**
- **Calculation:** The provisional score is 20/7 = 2.86, which rounds to 3. The evidence average is 13/7 = 1.86, below 2, so the score is capped at 2. Confidence is Medium: 5 of 7 answers are at E2 or E3, 1 is at E3, and the consistency check passes (April 2026 drill log and CAPA; COO approver; procurement system).
- **Gaps:** Substitution rights are tested (D/E3). Cutover governance (B/E1) has no evidence, matching the tabletop finding that there is no gate for switching to spreadsheet and phone orders. Concentration limits are informal.

**Move 5 Market exit: score 2, confidence Low**
- **Calculation:** The provisional score is 13/7 = 1.86, which rounds to 2. The zero rule is not met, because only 2 of 7 answers are A at E0. The score is also capped at 2 on two counts: the evidence average is 6/7 = 0.86, and the prerequisite Q1 (exit plan) is answered A. Confidence is Low because there are no E3 answers. The consistency check passes (approver: CEO; artifacts in the board portal).
- **Gaps:** The exit plan and distributor/JV obligations have no evidence (A/E0). Only the regulator and customer comms templates (C/E2) are documented.

## 4) Evidence Index

Labels map from evidence level: E0 = Unknown, E1 = Claimed, E2 = Documented, E3 = Tested.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Claimed
- Contract suspension clause summary: Claimed
- Decision log: Documented
- Resume plan: Claimed
- Escalation path description: Documented

**Move 2 Treasury reroute**
- Alternate bank and rail register: Claimed
- Freeze or hold playbook: Tested
- Counterparty tripwire definitions: Tested
- 72-hour reroute procedure: Documented
- KYC/KYB bundle: Documented
- Alternate settlement or letter of credit playbook: Claimed
- Treasury authority and backup matrix: Documented

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Unknown
- Transfer mechanism options summary: Claimed
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Claimed
- OT and critical access boundary procedure: Documented
- Retention and deletion procedure: Claimed

**Move 4 Substitution**
- Ranked single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution rights map for Tier-1 vendors: Tested
- Concentration limits policy: Claimed
- Logistics reroute plan: Documented
- Cutover gate checklist: Claimed

**Move 5 Market exit**
- Cross-functional exit plan: Unknown
- Termination and unwind path summary: Claimed
- Customer obligations and support plan: Claimed
- Data and people plan: Claimed
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Claimed
- Regulator and customer comms templates: Documented

## 5) 72-Hour Breakpoints

1. **0–6h, Move 1, missing authority:** The tabletop showed uncertainty over whether the CFO must co-approve the Operations Director's pause of order release. Without this, order release may continue during containment or stall while the approval question is resolved.
2. **0–6h, Moves 1 and 5, comms approval delay:** The holding statement would be drafted on the day (Q3 B/E1). Customers and staff would receive no consistent message in the first hours, and drafting would compete with containment for the same leaders' attention.
3. **0–6h, Move 3, missing artifact:** No Tier-1 data flow map exists (Q1 A/E0). The CIO cannot quickly scope which interfaces, logs and telemetry links to isolate around the compromised ERP.
4. **6–24h, Move 4, missing gate:** The tabletop showed no gate is defined for switching to spreadsheet and phone orders (Q7 B/E1). The manual cutover could start without minimum control checks, such as product hazard and handling data or credit checks.
5. **6–24h, Move 2, missing alternate:** The second bank is not onboarded (Q1 B/E1). The organization cannot rely on it if payment processing tied to the ERP or house bank is disrupted.
6. **6–24h, Move 2, missing artifact:** The alternate settlement path is ad hoc (Q6 B/E1). Supplier payments and customer receipts would need case-by-case workarounds with no agreed approval route.
7. **6–24h, Move 1, missing artifact:** The contractual suspension basis is case-by-case (Q4 B/E1). Delayed or paused deliveries cannot be checked quickly against triggers and notice expectations, so this becomes a question for counsel under time pressure.
8. **24–72h, Moves 1–5, missing artifact:** The tabletop showed nobody is named to capture evidence and no CAPA process runs after an incident. Decisions and workarounds would not be recorded, so recovery and lessons learned cannot be demonstrated.
9. **24–72h, Move 1, missing gate:** Resume criteria are informal (Q6 B/E1). With no agreed gates, the return from manual operations to the restored ERP risks reconciliation errors or a premature restart.
10. **24–72h, Move 3, operational infeasibility:** The stop-cleanly retention procedure is ad hoc (Q7 B/E1) and subprocessor awareness is partial (Q5 B/E1). Spreadsheets and phone records created outside the ERP have no defined handling, retention or deletion path.

## 6) Top Blockers and Fixes

1. **Stop authority ambiguity (Move 1)**
   - **Evidence gap:** The authority matrix is rated E2, but the tabletop showed the CFO's role is unclear.
   - **Minimal fix (2 weeks):** Issue a one-page decision note stating who pauses order release, with any co-approval and a named backup.
   - **Proper fix (6–12 weeks):** Revise the authority matrix with delegations for the incident scenario and exercise it.
   - **Owner role:** Operations Director, with the CFO.
2. **No Tier-1 data flow map (Move 3)**
   - **Evidence gap:** Q1 is A/E0, which triggers the prerequisite cap.
   - **Minimal fix (2 weeks):** Produce a high-level map of ERP interfaces: portal, bank, suppliers, logistics provider, logs and telemetry.
   - **Proper fix (6–12 weeks):** Produce a documented, reviewed map tied to the shutdown runbook.
   - **Owner role:** CIO.
3. **Second bank not onboarded (Move 2)**
   - **Evidence gap:** Q1 B/E1 and Q6 B/E1.
   - **Minimal fix (2 weeks):** Confirm the onboarding status and the remaining steps, and draft an interim manual settlement procedure.
   - **Proper fix (6–12 weeks):** Pre-clear the alternate bank, test a reroute and document the alternate settlement playbook.
   - **Owner role:** Treasurer, with the CFO approving.
4. **No gate for manual order intake (Move 4)**
   - **Evidence gap:** Q7 B/E1; the tabletop confirmed no gate exists.
   - **Minimal fix (2 weeks):** Write a manual-mode go/no-go checklist covering product safety data, credit, and order and dispatch controls.
   - **Proper fix (6–12 weeks):** Document cutover gates, test them in a drill and keep an evidence pack.
   - **Owner role:** COO.
5. **Holding statement not ready (Move 1)**
   - **Evidence gap:** Q3 B/E1.
   - **Minimal fix (2 weeks):** Draft holding statements for staff, customers and suppliers for an ERP outage.
   - **Proper fix (6–12 weeks):** Pre-approve the templates through a defined workflow with owners and counsel review.
   - **Owner role:** Head of Communications, or the CEO's delegate.
6. **No evidence capture or post-incident CAPA (all moves)**
   - **Evidence gap:** Tabletop finding; drill CAPAs exist, but no incident CAPA process.
   - **Minimal fix (2 weeks):** Name an incident scribe role and create a decision and evidence log template.
   - **Proper fix (6–12 weeks):** Extend the risk system's CAPA workflow to real incidents, with deadlines and owner sign-off.
   - **Owner role:** Head of Risk.
7. **Informal resume criteria (Move 1)**
   - **Evidence gap:** Q6 B/E1.
   - **Minimal fix (2 weeks):** List the minimum conditions for restarting ERP-based order release, including data reconciliation.
   - **Proper fix (6–12 weeks):** Document a resume plan with gates and test it.
   - **Owner role:** Operations Director, with the CIO.
8. **No exit plan; distributor and JV obligations unknown (Move 5)**
   - **Evidence gap:** Q1 and Q5 are A/E0.
   - **Minimal fix (2 weeks):** Inventory distributor and JV relationships at headline level, without contract text.
   - **Proper fix (6–12 weeks):** Document a cross-functional exit plan and run a tabletop.
   - **Owner role:** CEO, with General Counsel.
9. **Case-by-case contractual suspension basis (Move 1)**
   - **Evidence gap:** Q4 B/E1.
   - **Minimal fix (2 weeks):** Prepare a question list for counsel on suspension triggers and notices for Tier-1 contracts.
   - **Proper fix (6–12 weeks):** Have counsel prepare a clause summary mapped to Tier-1 contracts.
   - **Owner role:** General Counsel.
10. **Handling of offline records undefined (Move 3)**
    - **Evidence gap:** Q7 and Q5 are B/E1.
    - **Minimal fix (2 weeks):** Define where manual-mode records are stored, who can access them, and their retention.
    - **Proper fix (6–12 weeks):** Document the retention and deletion procedure and subprocessor list, and test them on a Tier-1 system.
    - **Owner role:** CIO, with the Data Protection Lead.

## 7) 30/60/90-Day Plan

**Workstream 1: Pause, authority and comms (Moves 1 and 5)**
- **Outcome:** The pause decision, holding statement and resume gates can be executed in the first 6 hours without ambiguity.
- **Tasks:**
  - Clarify pause authority and co-approval, with named backups (30 days).
  - Draft holding statements (30 days).
  - Document resume criteria (60 days).
  - Prepare the counsel question list on suspension basis (60 days).
  - Inventory distributor and JV relationships at headline level and outline the exit plan (90 days).
- **Gates:**
  - The authority note is signed by the Operations Director and the CFO.
  - Templates complete the approval workflow.
  - The resume plan is reviewed by the CIO.
- **Owner roles:** Operations Director, CFO, Head of Communications, General Counsel, CEO.
- **Stop rule:** Pause further template work if counsel has not reviewed the suspension questions by day 60. Escalate to the CEO.

**Workstream 2: Data map and manual cutover (Moves 3 and 4)**
- **Outcome:** A known data footprint and a gated manual-mode switch.
- **Tasks:**
  - Build a high-level Tier-1 data flow map (30 days).
  - Write the manual-mode go/no-go checklist (30 days).
  - Define handling of offline records (60 days).
  - Update the subprocessor list (60 days).
  - Document cutover gates and the concentration limits policy (90 days).
- **Gates:**
  - The data flow map is reviewed by the CIO.
  - The checklist confirms product safety data is available offline.
  - The cutover gates are approved by the COO.
- **Owner roles:** CIO, COO, Data Protection Lead.
- **Stop rule:** Do not run the manual-mode drill until the data map and gate checklist exist as named artifacts.

**Workstream 3: Treasury alternate and evidence discipline (Move 2 and all moves)**
- **Outcome:** An onboarded alternate rail and an incident evidence and CAPA routine.
- **Tasks:**
  - Confirm second-bank onboarding steps (30 days).
  - Name the incident scribe role and log template (30 days).
  - Draft the alternate settlement playbook (60 days).
  - Extend CAPA workflow to real incidents (60 days).
  - Run a reroute test (90 days).
- **Gates:**
  - The alternate bank is pre-cleared.
  - A test reroute is logged with a CAPA.
  - The incident CAPA workflow is live in the risk system.
- **Owner roles:** CFO, Treasurer, Head of Risk.
- **Stop rule:** If onboarding is not complete by day 90, report to the board risk committee as an open exposure.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: Head of Risk
- Operations Director
- CFO and Treasurer
- CIO
- COO
- Head of Communications
- General Counsel
- Scribe

**Agenda**
- **0–5 min:** Scenario brief. Ransomware has taken the ERP down; restoration is expected in five days.
- **5–15 min (0–6h window):** Decide the pause and who authorizes it. Confirm safety checks, including product hazard data access. Approve the holding statement.
- **15–28 min (6–24h window):** Choose the manual order path, the payment path and the isolation scope. Confirm which gates must pass and who signs off.
- **28–40 min (24–72h window):** Agree what is executed and monitored, how backlog and records are tracked, and what evidence is captured.
- **40–45 min:** Hot wash and CAPA assignment.

**Decisions to log**
- Pause approver
- Holding statement approval
- Manual intake go/no-go
- Payment path
- Isolation scope
- Resume criteria
- Escalation calls (counsel, executive)

**Evidence to capture**
- Timestamped decision log with roles
- Artifacts used, by type and system
- Artifacts that were missing
- Gate outcomes
- Time to each decision

**CAPA prompt**
"Which decision took longest or lacked an artifact, owner or alternate? Name one corrective action, its owner role and a due date. Record it in the risk system."

## 9) Escalations

**ESCALATE**

**Triggers identified**
- **Criminal (ransomware):** The scenario involves a criminal cyber attack. Decisions on engaging law enforcement and handling any extortion demand should go to executives and counsel.
- **Sanctions (conditional):** If any ransom payment were considered, it may raise sanctions questions. No sanctions determination is made here; this goes to counsel only.
- **Physical safety (conditional, needs confirmation):** If chemical hazard, handling or dangerous goods data is available only through the ERP, manual operations could raise physical safety concerns. Confirm offline availability.

**Thresholds not met on the provided information**
- Financial impact: about USD 2m, below USD 10m.
- People affected: 2,000 or fewer, below 100,000.
- Regulator inquiry: none reported. Any notification questions are for counsel.

**Recommended escalation path**
- Executive crisis lead (CEO) convenes the CIO, CFO and General Counsel.
- Engage external counsel for the jurisdiction (currently Unknown) on law enforcement, notifications and any payment question.
- Brief the board risk committee.

**Questions for counsel**
- What notification expectations apply if customer or employee data is affected?
- What constraints apply to any ransom payment decision?
- How do Tier-1 contract notices work for delayed or paused deliveries?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifact, log or CAPA was reviewed.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so no legal or regulatory conclusions are drawn. Nothing here states that anything is legal or compliant.
- **Scenario simplification:** A single five-day ERP outage does not cover cascading failures, such as a concurrent house bank or logistics outage.
- **Contradictions:** The tabletop findings contradict some answers (Move 1 Q1, Move 2 Q4). Scores use the answers as given, and the contradictions are noted in the rationale.
- **Limited exercises:** Only two moves (2 and 4) have recent exercises, both from April 2026.
- **Impact estimates:** The impact figures are user estimates and have not been verified.
- **Scope of this check:** This is informational planning only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 2, assistant (stop_reason end_turn)

Packet complete.

### Turn 3, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 3, assistant (stop_reason end_turn)

Packet complete.

## Score

**Verdict: PASS.** The Turn 1 packet has exactly 10 sections with the exact headings in order. Section 2 has 5 top-level bullets. Section 5 has 10 breakpoint bullets that draw on both the tabletop and the answers. Section 6 has 10 numbered items. Section 10 ends with the exact footer. None of the fail indicators appears. The only borderline point is the nested bullets in section 2, which I decided in favor of passing and flagged above.

---

Final Liability rests with the Human.
