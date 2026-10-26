# redcap-00-r1 R5c

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:31 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R5: reference.md 4 "High: more than half of the answers at E3 and the move’s consistency check passes"; "4 or more of 7"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 4 and confidence High, and no later turn changes either value. Expected value computed in tests.md: Deepening threshold: 4 of 7 at E3 gives High

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Deepening.

I opt in to Deepening. Answers to Q1 to Q7 for every move (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2. Q5 Logging and audit trail: C, E2. Q6 Resume criteria: C, E2. Q7 Escalation under conflict: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2. Q5 KYC or KYB readiness: C, E2. Q6 Letters of credit or alternate settlement paths: C, E2. Q7 Treasury authority and backups: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2. Q5 Subprocessor awareness: C, E2. Q6 OT or critical access boundary: C, E2. Q7 Stop-cleanly retention and deletion procedure: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: D, E3. Q2 Qualified alternates: D, E3. Q3 Portability or failover plan: D, E3. Q4 Substitution or portability rights: D, E3. Q5 Concentration limits: C, E2. Q6 Logistics reroute options: C, E2. Q7 Cutover governance: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2. Q5 Distributor or JV obligations: C, E2. Q6 Assets and IP handling: C, E2. Q7 Regulator and customer comms workflow: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Mini tabletop answers. 0 to 6 hours: the Operations Director pauses order release at all three warehouses; the safety checklist must pass; the holding statement template is issued. 6 to 24 hours: we switch order intake to the manual fallback and the second bulk supplier's portal; the COO signs off at the cutover gate. 24 to 72 hours: we execute the cutover, monitor order backlog and payment runs, capture the decision log and open a CAPA for every gap.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Deepening (35 questions, consistency checks and mini tabletop)
- **Scenario tested:** Ransomware outage takes the cloud ERP down for 5 days. Your estimate of worst-case impact is about USD 2M, with no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a B2B specialty chemicals distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 scope covers the cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** Each answer maps to a pattern score: A=1 (none or ad hoc), B=2 (partial or untested), C=3 (documented and owned), D=4 (tested in the last 12 months, with viable alternates). A move's score is its average, rounded, with exact halves rounded down.
- **Evidence:** E0 means no evidence, E1 verbal only, E2 documented with an owner, and E3 tested, logged and followed by a CAPA in the last 12 months. These score 0 to 3.
- **Caps:** A move's score is capped at 2 in two cases: its evidence average is below 2, or its prerequisite question is answered A. A score of 0 (Unknown) applies only if more than half of a move's answers are A at E0.
- **Confidence:**
  - High: more than half of answers at E3 and the consistency check passes.
  - Medium: more than half at E2 or E3, at least one E3, and the check passes.
  - Low: all other cases.
- **Downgrade:** If a move fails its consistency check (exercise date, log and CAPA; approver role; artifact location), its confidence drops to Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 7 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 7 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 7 | 0 |
| 4 Substitution | 4 | High | 0 | 0 | 3 | 4 |
| 5 Market exit | 3 | Low | 0 | 0 | 7 | 0 |

**Move 1 Safe pause: 3 / Low**
- All 7 answers are C at E2, so the average is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (stop authority) is C, so the prerequisite is met.
- Confidence is Low because no answer is at E3, and Medium requires at least one. The consistency check passes (approver: Operations Director; artifact location: quality document system).

**Move 2 Treasury reroute: 3 / Low**
- All 7 answers are C at E2, so the average is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (alternate banks and rails) is C.
- Confidence is Low because there is no E3 evidence. Q4 ("execute within 72 hours") is only "likely." The consistency check passes (approver: CFO, with Treasurer as backup; artifact location: treasury system).

**Move 3 Data switchboard: 3 / Low**
- All 7 answers are C at E2, so the average is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (data flow map) is C.
- Confidence is Low because there is no E3 evidence. The segmentation and shutdown runbook (Q3) and emergency access logging (Q4) are untested, which matters directly in a ransomware scenario. The consistency check passes (approver: CIO; artifact location: IT service management tool).

**Move 4 Substitution: 4 / High**
- The answers are four D and three C, averaging 3.57, which rounds to 4. The evidence average is 18/7 ≈ 2.57, so no cap applies, and Q2 (qualified alternates) is D.
- Confidence is High because 4 of 7 answers are at E3. The consistency check passes: the exercise was in April 2026, which is within 12 months as of the Reference Pack date of 18 Oct 2026, and a drill log and CAPA exist in the risk system. The approver is the COO, and artifacts are in the procurement system. The weak spots are concentration limits, logistics reroute and cutover governance (Q5 to Q7, all C at E2).

**Move 5 Market exit: 3 / Low**
- All 7 answers are C at E2, so the average is 3.0 and the evidence average is 2.0. No cap applies, and Q1 (exit plan) is C.
- Confidence is Low because there is no E3 evidence. The regulator and customer comms workflow (Q7) is templates only, with no approval workflow. The consistency check passes (approver: CEO; artifact location: board portal).

## 4) Evidence Index

Artifact types are categories only.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator holding statement templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Documented
- Resume plan: Documented
- Escalation path: Documented

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour execution procedure: Documented
- KYC or KYB bundle: Documented
- Alternate settlement playbook: Documented
- Treasury authority and backup matrix: Documented

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Documented
- OT and critical access boundary description: Documented
- Retention and deletion (stop-cleanly) procedure: Documented

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Tested
- Qualified alternates register: Tested
- Portability or failover plan: Tested
- Substitution and portability rights summary: Tested
- Concentration limits: Documented
- Logistics reroute plan: Documented
- Cutover gates: Documented

**Move 5 Market exit**
- Cross-functional exit plan: Documented
- Termination and unwind paths: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Documented
- Assets and IP handling procedure: Documented
- Regulator and customer comms templates: Documented

## 5) 72-Hour Breakpoints

1. **0–6h, Move 1, comms approval delay:** The holding statement templates exist (Q3 C) but are not pre-approved with a workflow, so the first statement waits on ad hoc sign-off while the warehouse pause is already live.
2. **0–6h, Move 1, missing gate:** The safety checklist must pass before the pause is complete, but it is documented and untested (Q2 C). Hazardous-goods holds could therefore stall on unclear pass/fail criteria.
3. **0–6h, Moves 1 and 3, missing artifact:** It is Unknown whether the quality document system and the IT service management tool are reachable during the ERP compromise. A runbook nobody can open cannot be followed.
4. **0–6h, Move 3, missing gate:** The segmentation and shutdown runbook is untested (Q3 C), so the CIO cannot confirm in the window that the ERP is isolated from the order portal and other Tier-1 systems.
5. **6–24h, Moves 3 and 4, operational infeasibility:** No answer or exercise record specifically evidences the manual order-intake fallback named in the tabletop. If it was outside the scope of the April 2026 drill, handling orders from about 300 customers manually is unproven.
6. **6–24h, Move 2, operational infeasibility:** Alternate rails are pre-cleared, but 72-hour execution is only "likely" (Q1 and Q4 C). The payment runs monitored in the 24–72h window would depend on an unexercised path while ERP payables data is unavailable.
7. **6–24h, Move 4, missing gate:** The COO signs off at the cutover gate, but the gates are untested and have no evidence pack (Q7 C). Sign-off may stall for lack of proof that gate criteria are met.
8. **24–72h, Move 4, missing alternate:** Logistics reroute options are planned but not exercised (Q6 C). If the logistics provider's integration depends on the ERP, goods from the second bulk supplier may not move within the window.
9. **24–72h, Moves 1 and 5, comms approval delay:** Customer comms on backlog and delays rely on templates with no approval workflow (Move 5 Q7 C), so updates to about 300 customers queue behind executive review.
10. **24–72h, Move 1, missing gate:** The resume criteria are documented but untested (Q6 C), so the decision to restart order release after the cutover has no proven gates and may be delayed or contested.

## 6) Top Blockers and Fixes

1. **Stop authority and safety checklist never exercised (Move 1 Q1, Q2)**
   - Evidence gap: E2, with no test date, log or CAPA.
   - Minimal fix (2 weeks): Hold a 30-minute walkthrough of the warehouse pause with the safety checklist, naming a backup authority for the Operations Director.
   - Proper fix (6–12 weeks): Run a timed pause drill at one warehouse, with logged outcomes and a CAPA.
   - Owner role: Operations Director.
2. **Holding statements not pre-approved (Move 1 Q3; Move 5 Q7)**
   - Evidence gap: templates exist, but there is no approval workflow.
   - Minimal fix (2 weeks): Pre-approve three ransomware holding statements (internal, customer, regulator placeholder) with named approver roles.
   - Proper fix (6–12 weeks): Build an approval workflow with time limits and test it in a drill.
   - Owner role: Head of Communications, with General Counsel.
3. **Decision log not tamper-evident (Move 1 Q5)**
   - Evidence gap: the log exists but lacks timestamps, roles and immutability.
   - Minimal fix (2 weeks): Create an offline, timestamped decision log template with role fields.
   - Proper fix (6–12 weeks): Implement an append-only log stored outside the ERP environment and test it in a drill.
   - Owner role: Head of Risk.
4. **Resume criteria untested (Move 1 Q6)**
   - Evidence gap: E2 only.
   - Minimal fix (2 weeks): Define three to five go/no-go resume gates for order release after an ERP outage.
   - Proper fix (6–12 weeks): Test the resume gates in a tabletop and record a CAPA.
   - Owner role: Operations Director.
5. **Treasury reroute unexercised (Move 2 Q1, Q4)**
   - Evidence gap: pre-cleared only, and 72-hour execution is "likely."
   - Minimal fix (2 weeks): Hold a desk check confirming alternate-rail steps that do not depend on ERP data.
   - Proper fix (6–12 weeks): Run a low-value test of the reroute path with a log and a CAPA.
   - Owner role: Treasurer, with CFO approval.
6. **Freeze/hold playbook and treasury backups not drilled (Move 2 Q2, Q7)**
   - Evidence gap: E2, with no exercised roles.
   - Minimal fix (2 weeks): Confirm the delegation chain from CFO to Treasurer to a named third role.
   - Proper fix (6–12 weeks): Drill the freeze/hold playbook, including payment-run approvals during an ERP outage.
   - Owner role: CFO.
7. **Segmentation and shutdown runbook untested (Move 3 Q3)**
   - Evidence gap: E2 only.
   - Minimal fix (2 weeks): Walk through the ERP isolation steps against the Tier-1 data flow map.
   - Proper fix (6–12 weeks): Run an isolation exercise in a non-production setting with a log and a CAPA.
   - Owner role: CIO.
8. **Emergency access logging and the OT boundary untested (Move 3 Q4, Q6)**
   - Evidence gap: E2 only.
   - Minimal fix (2 weeks): Confirm that break-glass access requests are logged outside the affected environment.
   - Proper fix (6–12 weeks): Test the emergency access procedure, including the warehouse control boundary, and keep the audit trail.
   - Owner role: CIO, with the IT security lead.
9. **Cutover gates and logistics reroute not exercised (Move 4 Q6, Q7)**
   - Evidence gap: these are C at E2, while the stronger Move 4 answers (Q1 to Q4) are at E3.
   - Minimal fix (2 weeks): Define the evidence pack for the cutover gate and confirm the logistics provider's non-ERP order handoff.
   - Proper fix (6–12 weeks): Extend the April 2026 drill to cover logistics reroute and gate sign-off.
   - Owner role: COO.
10. **Artifact access during the outage and manual fallback unevidenced (tabletop)**
    - Evidence gap: artifact reachability is Unknown, and the manual fallback has no recorded test.
    - Minimal fix (2 weeks): Keep an offline or out-of-band copy of the Move 1, 3 and 4 runbooks and confirm the manual intake form.
    - Proper fix (6–12 weeks): Run a timed manual order-intake test against expected daily volume, with a CAPA.
    - Owner role: COO, with the CIO.

## 7) 30/60/90-Day Plan

**Workstream A: Ransomware pause and isolation to E3 (Moves 1 and 3)**
- **Outcome:** Move 1 and Move 3 each have at least one E3 answer and an exercise logged with a CAPA.
- **Tasks:**
  - Days 0–30: Make offline copies of the runbooks and define resume gates.
  - Days 0–30: Name backup stop authorities.
  - Days 30–60: Run a combined pause and isolation tabletop.
  - Days 60–90: Close or track every CAPA and re-score Moves 1 and 3.
- **Gates:**
  - Runbooks are accessible with the ERP and ITSM tool assumed down.
  - The exercise log and CAPA are recorded with month/year.
- **Owner roles:** Operations Director, CIO, Head of Risk.
- **Stop rule:** If isolation steps cannot be exercised safely in a non-production setting, stop and re-scope with the CIO before any live test.

**Workstream B: Treasury continuity and comms approval (Moves 2 and 5)**
- **Outcome:** The alternate rail is exercised, payment-run approvals work without the ERP, and holding statements are pre-approved.
- **Tasks:**
  - Days 0–30: Desk check of the reroute steps.
  - Days 0–30: Pre-approve the holding statements.
  - Days 30–60: Low-value reroute test.
  - Days 30–60: Freeze/hold drill.
  - Days 60–90: Test the comms approval workflow, then re-score.
- **Gates:**
  - CFO sign-off on the test scope.
  - Counsel review of the regulator and customer templates.
  - A logged test with a CAPA.
- **Owner roles:** CFO, Treasurer, Head of Communications, General Counsel.
- **Stop rule:** Halt any live payment test if bank or counsel questions remain open.

**Workstream C: Extend substitution evidence (Move 4, plus Move 5 exit tabletop)**
- **Outcome:** Logistics reroute and cutover gates reach E3, and the exit plan gets its first tabletop.
- **Tasks:**
  - Days 0–30: Define the cutover evidence pack.
  - Days 0–30: Confirm the logistics provider's non-ERP handoff.
  - Days 30–60: Re-drill substitution with logistics and the manual intake fallback.
  - Days 60–90: Run a 60-minute exit-plan tabletop.
- **Gates:**
  - COO approves the gate criteria.
  - The drill log and CAPA are recorded in the risk system.
- **Owner roles:** COO, CEO, Head of Procurement.
- **Stop rule:** Keep the April 2026 drill evidence current. If the re-drill slips beyond the 12-month window from April 2026, flag Move 4's E3 status for review.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (Head of Risk)
  - Operations Director (pause authority)
  - CIO (isolation and data posture)
  - CFO or Treasurer (payments)
  - COO (cutover gate)
  - Head of Communications
  - Scribe
- **Agenda:**
  - 0–5 min: Scenario brief. The ERP is encrypted, and the ERP and ITSM tool are assumed unavailable.
  - 5–15 min: The 0–6h window covers the pause decision, the safety checklist and the holding statement approval.
  - 15–28 min: The 6–24h window covers ERP isolation, the manual intake fallback, the alternate rail and the cutover gate.
  - 28–38 min: The 24–72h window covers execution, backlog and payment monitoring, customer updates and resume gates.
  - 38–45 min: Hot wash and CAPA assignment.
- **Decisions to log:**
  - Who authorized the pause and when.
  - Checklist pass/fail.
  - Statement approval time.
  - The isolation decision.
  - The payment path chosen.
  - The cutover gate result.
  - The resume decision.
- **Evidence to capture:**
  - The timestamped decision log.
  - Which artifacts were accessible offline.
  - Time-to-approval for comms.
  - Gate evidence pack completeness.
  - Unresolved questions for counsel.
- **CAPA prompt:** "Which decision took longest or lacked an artifact, and what single action, owner role and due date would close it?"

## 9) Escalations

**ESCALATE**

- **Criminal:** The scenario is a ransomware attack, which is a criminal act. Decisions on law-enforcement engagement and evidence preservation should go to counsel.
- **Physical safety:** Pausing specialty chemical warehouses involves hazardous-goods handling and safety checklists. Unsafe holds or uncontrolled restarts could create physical safety risk.
- **Sanctions (conditional):** If any ransom payment were ever contemplated, sanctions questions would arise. No determination is made here, and the question goes directly to counsel.
- **Thresholds not met:** The estimated impact (about USD 2M) is below USD 10M, and the people affected (≤2,000) are below 100,000.
- **Recommended path:**
  - The CEO and CIO notify the General Counsel or external counsel and the board risk chair.
  - The EHS or safety lead joins all pause and resume decisions.
- **Questions for counsel:**
  - Which notification duties (regulatory, customer, contractual) may apply, given that the jurisdiction is Unknown?
  - What is the law-enforcement engagement approach?
  - What is the process for any payment-related sanctions screening?
  - What evidence preservation duties apply?

## 10) Known Limits + Version

- **Self-report bias:** 28 of 35 answers are identical (C at E2), which may reflect uniform self-rating rather than verified maturity.
- **No document validation:** No artifacts were reviewed, and E2 and E3 ratings are taken as stated.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so no legal or compliance conclusions are drawn.
- **Scenario simplification:** A single 5-day ERP outage does not model data exfiltration, extortion or concurrent supplier failure.
- **E3 recency:** Move 4's E3 status assumes an assessment date on or near 18 Oct 2026. The April 2026 exercise falls outside the 12-month window after April 2027.
- **Unconfirmed availability:** It is Unknown whether artifact repositories stay reachable during the outage.
- **Scenario relevance:** Move 5 (market exit) is scored as asked but is only partly relevant to this scenario.
- **Not advice or certification:** This is informational only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: 4 / High

### Turn 3, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 3, assistant (stop_reason end_turn)

Move 4 Substitution: 4 / High

## Score

**Verdict: PASS.** The case tests only that the final packet's Scorecard shows Move 4 at score 4 and confidence High, and that later turns do not change this. I recomputed both values from the user's answers and the Reference Pack rules and they match the packet's. The packet was produced in Turn 1. Turns 2 and 3 repeat 4 / High without alteration. No fail indicator appears.

---

Final Liability rests with the Human.
