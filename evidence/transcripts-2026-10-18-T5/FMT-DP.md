# redcap-00 FMT-DP

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:43 KST · **max_tokens:** 16000

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

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Deepening. All 35 questions were answered, the mini tabletop was run, and the consistency checks were recorded.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate the worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, about 300 business customers and three warehouses in one country.
  - Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Pattern scores:** Answers map to A=1 (none or ad hoc), B=2 (partial or untested), C=3 (documented and owned), and D=4 (tested in the last 12 months with logs and a CAPA). The move score is the mean of the 7 answers, rounded, with exact halves rounding down.
- **Evidence scores:** E0=0 (no evidence), E1=1 (verbal only), E2=2 (named artifact and owner role) and E3=3 (tested, logged, with a CAPA, within 12 months).
- **Evidence-average cap:** If a move's evidence average is below 2.0, the move score is capped at 2.
- **Prerequisite cap:** If a move's prerequisite question is answered A, the move score is capped at 2.
- **Unknown score:** A score of 0 ("Unknown") applies only when 4 or more of the 7 answers are A at E0.
- **Confidence:**
  - **High** needs 4 or more E3 answers.
  - **Medium** needs 4 or more answers at E2 or E3, at least one E3, and a passed consistency check.
  - **Low** applies otherwise. A failed consistency check always forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | Low | 0 | 3 | 4 | 0 |
| 2 Treasury reroute | **3** | Medium | 0 | 2 | 3 | 2 |
| 3 Data switchboard | **2** | Low | 1 | 3 | 3 | 0 |
| 4 Substitution | **2** | Medium | 0 | 2 | 4 | 1 |
| 5 Market exit | **2** | Low | 2 | 4 | 1 | 0 |

**Move 1 Safe pause: score 2, Low**
- The provisional score was 3 (pattern average 2.57). The evidence average of 1.57 is below 2, so the score is capped at 2. Q1 is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passed: the approver is the Operations Director and artifacts sit in the quality document system. However, the tabletop showed that the documented authority matrix does not settle whether the CFO must co-approve.

**Move 2 Treasury reroute: score 3, Medium**
- The pattern average is exactly 3.00. The evidence average is exactly 2.00, which is not below 2, so no cap applies. Q1 is B, so no prerequisite cap applies.
- Confidence is Medium: 5 of 7 answers are at E2 or E3, two are E3, and the consistency check passed (exercise April 2026, drill log and CAPA in the risk system, CFO as approver with the Treasurer as backup). The weakest points are the alternate rails (Q1, B/E1) and the alternate settlement paths (Q6, B/E1). The tabletop confirmed that the second bank is not yet onboarded.

**Move 3 Data switchboard: score 2, Low**
- The provisional score was 2 (pattern average 2.29). Two caps also apply: the evidence average of 1.29 caps the score at 2, and Q1 (data flow map) answered A caps it at 2.
- Confidence is Low because there are no E3 answers. The consistency check passed (CIO as approver, artifacts in the IT service management tool). Without a Tier-1 data flow map that includes logs and telemetry, you cannot scope what to isolate or what to run manually.

**Move 4 Substitution: score 2, Medium**
- The provisional score was 3 (pattern average 2.86). The evidence average of 1.86 is below 2, so the score is capped at 2. Q2 is C, so no prerequisite cap applies.
- Confidence is Medium: 5 of 7 answers are at E2 or E3, one is E3 (Q4), and the consistency check passed (April 2026, log and CAPA, COO as approver, procurement system). The weak points are cutover governance (Q7, B/E1) and concentration limits (Q5, B/E1). The tabletop confirmed there is no gate for the manual switch.

**Move 5 Market exit: score 2, Low**
- The provisional score was 2 (pattern average 1.86). Two caps also apply: the evidence average of 0.86 caps the score at 2, and Q1 (exit plan) answered A caps it at 2. Only 2 of 7 answers are A at E0, so the zero rule does not apply.
- Confidence is Low: there are no E3 answers and only one answer at E2. The consistency check passed (CEO as approver, board portal). The exit plan and the distributor or JV obligations are both A/E0.

## 4) Evidence Index

Labels: Unknown = E0, Claimed = E1, Documented = E2, Tested = E3.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Claimed
- Contract suspension clause summary: Claimed
- Decision log: Documented
- Resume plan: Claimed
- Escalation path: Documented

**Move 2 Treasury reroute**
- Alternate bank and rail register: Claimed
- Freeze or hold playbook: Tested
- Counterparty tripwire definitions: Tested
- 72-hour reroute runbook: Documented
- KYC or KYB bundle: Documented
- Alternate settlement playbook: Claimed
- Treasury delegation and backup register: Documented

**Move 3 Data switchboard**
- Tier-1 data flow map: Unknown
- Transfer mechanism options summary: Claimed
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access log procedure: Documented
- Subprocessor list: Claimed
- OT or critical access boundary procedure: Documented
- Retention and deletion procedure: Claimed

**Move 4 Substitution**
- Ranked single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution rights map for Tier-1 vendors: Tested
- Concentration limits statement: Claimed
- Logistics reroute plan: Documented
- Cutover gate checklist: Claimed

**Move 5 Market exit**
- Cross-functional exit plan: Unknown
- Termination and unwind path summary: Claimed
- Customer support plan: Claimed
- Data and people plan: Claimed
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Claimed
- Regulator and customer comms templates: Documented

## 5) 72-Hour Breakpoints

1. **0–6 h, Move 1, missing authority.** The Operations Director would pause order release, but no one knows whether the CFO must co-approve. The pause can stall while authority is debated during the first hours of the outage.
2. **0–6 h, Moves 1 and 5, comms approval delay.** The holding statement would be drafted on the day, and the templates are only claimed (M1 Q3 B/E1). Customers and staff receive no approved message while drafting and sign-off happen under pressure.
3. **6–24 h, Move 4, missing gate.** Order intake switches to spreadsheets and phone with no gate defined (M4 Q7 B/E1). Nothing confirms the manual process is controlled before live orders flow through it.
4. **6–24 h, Move 2, missing alternate.** The second bank is identified but not onboarded (M2 Q1 B/E1). If house-bank flows tied to the ERP are disrupted, there is no rail usable within 72 hours.
5. **6–24 h, Move 2, missing alternate.** Alternate settlement paths, such as letters of credit, are ad hoc (M2 Q6 B/E1). Supplier payments that depend on ERP-generated instructions have no planned fallback.
6. **6–24 h, Move 3, missing artifact.** There is no Tier-1 data flow map, including logs and telemetry (M3 Q1 A/E0). The team cannot confirm which systems and data to isolate or what data enters the manual spreadsheets.
7. **6–24 h, Move 3, missing artifact.** Subprocessor awareness for the cloud ERP and portal is only partial (M3 Q5 B/E1). The containment scope and third-party coordination needed for a clean stop or switch cannot be confirmed.
8. **24–72 h, Moves 1 and 4, missing authority.** No one is named to capture evidence during manual operations. Decisions, orders and exceptions go unrecorded, which blocks reconciliation and later review.
9. **24–72 h, Move 1, missing gate.** Resume criteria are informal (M1 Q6 B/E1). No agreed test decides when to return order release to the restored ERP, so resumption is delayed or happens unsafely.
10. **24–72 h, Move 5, missing artifact.** If the outage extends, there is no exit plan (M5 Q1 A/E0) and no map of distributor or JV obligations (M5 Q5 A/E0). Any decision to drop a product line, channel or customer segment would have to be built from scratch.

## 6) Top Blockers and Fixes

1. **Pause authority is ambiguous between the Operations Director and the CFO.**
   - **Evidence gap:** The matrix is documented (E2), but the tabletop showed it does not answer the co-approval question.
   - **Minimal fix (2 weeks):** Issue a one-page clarification naming the sole authority, the backup and the thresholds for joint approval.
   - **Proper fix (6–12 weeks):** Revise the authority matrix and exercise it in a drill to reach E3.
   - **Owner role:** Operations Director, with the CFO.
2. **Holding statement and comms templates do not exist.**
   - **Evidence gap:** Claimed only (M1 Q3 E1).
   - **Minimal fix:** Draft ransomware and outage holding statements for staff, customers, suppliers and regulators.
   - **Proper fix:** Pre-approve the templates with a defined approval workflow and owners, then rehearse them.
   - **Owner role:** Head of Communications, with General Counsel.
3. **Resume criteria are informal.**
   - **Evidence gap:** Claimed only (M1 Q6 E1).
   - **Minimal fix:** Write resume gates covering ERP integrity confirmation, data reconciliation and inventory accuracy.
   - **Proper fix:** Test the resume plan with gates in a drill.
   - **Owner role:** Operations Director, with the CIO.
4. **Contractual suspension basis is handled case by case.**
   - **Evidence gap:** Claimed only (M1 Q4 E1).
   - **Minimal fix:** Prepare redacted summaries of notice and suspension triggers for the top Tier-1 customer and supplier contracts.
   - **Proper fix:** Map triggers and notices across all Tier-1 contracts, with counsel input.
   - **Owner role:** General Counsel.
5. **Alternate bank, rails and settlement paths are not ready.**
   - **Evidence gap:** Claimed only (M2 Q1 and Q6 E1). The second bank is not onboarded.
   - **Minimal fix:** Start onboarding the second bank and list the settlement fallbacks.
   - **Proper fix:** Pre-clear the second bank, then test the reroute path and the settlement playbook.
   - **Owner role:** Treasurer.
6. **There is no Tier-1 data flow map.**
   - **Evidence gap:** Unknown (M3 Q1 E0). This is also the prerequisite cap for Move 3.
   - **Minimal fix:** Produce a draft map covering the ERP, portal, bank interfaces, logs and telemetry.
   - **Proper fix:** Maintain a current, reviewed map with a named owner and a review cadence.
   - **Owner role:** CIO.
7. **Subprocessor awareness, transfer options and stop-cleanly procedures are weak.**
   - **Evidence gap:** Claimed only (M3 Q2, Q5 and Q7 E1).
   - **Minimal fix:** Compile the subprocessor list for the ERP and portal and outline a retention and deletion procedure.
   - **Proper fix:** Map the transfer options with counsel and test the stop-cleanly procedure on one Tier-1 system.
   - **Owner role:** CIO, with the Data Protection Lead.
8. **Manual-mode cutover is ungated and concentration limits are informal.**
   - **Evidence gap:** Claimed only (M4 Q7 and Q5 E1).
   - **Minimal fix:** Write a manual-mode cutover gate checklist covering order validation, hazardous-goods documentation checks and backlog thresholds.
   - **Proper fix:** Test the gates with an evidence pack and document concentration limits with triggers, including the single logistics provider.
   - **Owner role:** COO.
9. **No incident evidence capture and no post-incident CAPA process.**
   - **Evidence gap:** The tabletop contradicts the drill CAPAs recorded for Moves 2 and 4. CAPA appears to exist for drills but not for real incidents.
   - **Minimal fix:** Name an incident scribe role and extend the risk-system CAPA workflow to cover live incidents.
   - **Proper fix:** Embed evidence capture and CAPA closure in the incident procedure and audit it.
   - **Owner role:** Chief Risk Officer or Head of Risk.
10. **There is no exit plan and no map of distributor or JV obligations.**
    - **Evidence gap:** Unknown (M5 Q1 and Q5 E0). This is also the prerequisite cap for Move 5.
    - **Minimal fix:** Prepare a skeleton exit plan outline and an obligations inventory using categories only.
    - **Proper fix:** Document the exit plan across operations, data, people, comms and support with counsel, then tabletop it.
    - **Owner role:** CEO, with the Strategy Lead and General Counsel.

## 7) 30/60/90-Day Plan

**Workstream A: Decide and communicate (Moves 1 and 5)**
- **Outcome:** Pause, resume and communication decisions can be made in the first 6 hours with no authority ambiguity.
- **Tasks:**
  - Days 0–30: Clarify pause authority and backups.
  - Days 0–30: Draft holding statements and templates.
  - Days 30–60: Write resume gates.
  - Days 30–60: Prepare redacted summaries of Tier-1 contract notice triggers.
  - Days 60–90: Pre-approve the templates and their workflow.
  - Days 60–90: Produce the exit plan skeleton and the distributor or JV obligations inventory.
- **Gates:**
  - Signed authority clarification by day 30.
  - Templates approved by named owners by day 60.
  - Pause-and-resume drill logged with a CAPA by day 90.
- **Owner roles:** Operations Director, CFO, Head of Communications, General Counsel, CEO.
- **Stop rule:** If authority is not signed by day 30, escalate to the CEO and pause the template work until it is resolved.

**Workstream B: Switch paths (Moves 2 and 4)**
- **Outcome:** Treasury and order intake can switch inside 72 hours through gated, pre-cleared paths.
- **Tasks:**
  - Complete onboarding of the second bank.
  - Document alternate settlement paths.
  - Write the manual-mode cutover gate checklist.
  - Document concentration limits and triggers, including logistics.
  - Run a manual-mode drill.
- **Gates:**
  - Second bank pre-cleared by day 60.
  - Cutover checklist approved by the COO by day 45.
  - Drill log and CAPA by day 90.
- **Owner roles:** Treasurer, CFO, COO, Procurement Lead.
- **Stop rule:** If the second bank is not pre-cleared by day 60, escalate to the CFO and record the gap on the risk register.

**Workstream C: Data and evidence (Move 3 plus incident CAPA)**
- **Outcome:** You know what data flows where, can stop or switch cleanly, and every incident produces evidence and a CAPA.
- **Tasks:**
  - Draft the Tier-1 data flow map, including logs and telemetry.
  - Compile the ERP and portal subprocessor list.
  - Outline the retention and deletion procedure.
  - Name the incident scribe role.
  - Extend the CAPA workflow to live incidents.
- **Gates:**
  - Map reviewed by the CIO by day 45.
  - Scribe role and CAPA workflow live by day 30.
  - Stop-cleanly test on one Tier-1 system by day 90.
- **Owner roles:** CIO, Data Protection Lead, Head of Risk.
- **Stop rule:** If the data flow map is not reviewed by day 45, escalate to the CEO and do not claim Move 3 improvement.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: Head of Risk.
- Decision makers: Operations Director, CFO, COO, CIO and CEO (the CEO joins for the final 10 minutes).
- Scribe: the named evidence role.
- Communications: Head of Communications.
- Counsel observer: General Counsel.

**Agenda**
- **0–5 min:** Brief the scenario: the ERP is encrypted and expected to be down for five days.
- **5–15 min (0–6 h window):** Decide the pause, name who authorizes it, confirm safety checks including hazardous-goods handling, and release the holding statement.
- **15–28 min (6–24 h window):**
  - Choose the manual intake path.
  - Choose the treasury path.
  - Choose the data isolation posture.
  - Confirm the gates and the sign-off.
- **28–40 min (24–72 h window):**
  - Agree what is executed and what is monitored, including backlog and reconciliation.
  - Agree the evidence to capture.
  - Agree the resume gates.
- **40–45 min:** Read back the decisions and open the CAPA.

**Decisions to log**
- Pause authority and timestamp.
- Holding statement approval.
- Manual cutover go or no-go.
- Treasury path choice.
- Data isolation scope.
- Resume decision criteria.

**Evidence to capture**
- Decision log with timestamps and roles.
- Artifacts referenced, with name and location only.
- Gaps found.
- Attendance.

**CAPA prompt**
- "Which decision took longest or had no owner, which artifact was missing, who fixes it, and by when?"
- Record at least one CAPA in the risk system.

## 9) Escalations

**ESCALATE: criminal matter.** Ransomware is a criminal act. Route the response through:
1. The CEO.
2. General Counsel and outside counsel.
3. The CIO or security lead.
4. The board risk or audit committee.

Decisions on engaging law enforcement and on any notifications should be made with counsel. Jurisdiction is Unknown.

**ESCALATE (conditional): sanctions.** If paying a ransom is ever considered, that raises sanctions and related questions. Take this to counsel before any action. This packet makes no sanctions determination.

**ESCALATE (conditional, confirm): physical safety.** Specialty chemicals storage and dispatch under manual processes may affect hazardous-goods documentation, safety data sheet access and stock location accuracy. Confirm this with your safety lead and escalate if a safety impact is plausible.

**Thresholds not met:** USD 2 million is below USD 10 million, and 2,000 people is below 100,000.

**Questions for counsel**
- Which notification obligations could apply to customers, regulators or other parties, and on what timelines?
- What are the constraints on any ransom-related decision?
- How do Tier-1 contract notice provisions interact with a declared pause?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifact was inspected, so "Documented" and "Tested" labels are claims you have recorded, not verified facts.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification, transfer and contract points are framed as questions for counsel only.
- **Scenario simplification:** A single five-day ERP outage was tested. Concurrent loss of the portal, the bank interfaces or a supplier was not modeled.
- **Tabletop contradictions:**
  - The Move 1 authority matrix (C/E2) did not resolve CFO co-approval.
  - The tabletop said "no CAPA after incidents," while drill CAPAs are recorded for Moves 2 and 4.
  - Scores follow the answers as given. Validate both points.
- **12-month window assumption:** The April 2026 exercises were treated as within the last 12 months, assuming this assessment runs before April 2027.
- **Move 4 score and confidence:** Medium confidence sits alongside a capped score of 2. Some evidence is strong, but too much of it is verbal.
- **Scope of the self-check:** It does not cover technical incident response or ransomware recovery steps.
- **Informational only:** Not advice from counsel, not a certification, not sanctions screening.
- **Liability:** Final liability rests with the human decision makers.

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

**Verdict: FAIL.** The pass condition requires every one of F1 to F5 to be met. F1, F3, F4 and F5 are met: the 10 headings are exact and in order, section 5 has 10 bullets, section 6 has 10 numbered items, and the footer is exact. F2 is not met, because section 2 contains six top-level bullets (nine with the nested ones) against a maximum of five. Under the strict rule, partial compliance fails, so the verdict is FAIL.

---

Final Liability rests with the Human.
