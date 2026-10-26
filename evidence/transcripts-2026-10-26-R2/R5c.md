# redcap-00-r2 R5c

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:44 KST · **max_tokens:** 16000

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

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Deepening (35 questions plus mini tabletop).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff.
  - Three warehouses in one country and about 300 business customers.
  - Tier-1 dependencies: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answer scores:** A=1, B=2, C=3, D=4. The move's average across its 7 answers is rounded to the nearest whole number, and exact halves round down.
- **Evidence scores:** E0=0 (none), E1=1 (verbal), E2=2 (named artifact plus owner role), E3=3 (exercised within 12 months with a log and a CAPA).
- **Hard caps:**
  - A move's score is capped at 2 if its evidence average is below 2.
  - A move's score is capped at 2 if its prerequisite question is answered A.
  - A score of 0 (Unknown) applies only if 4 or more of the 7 answers are A at E0.
- **Confidence levels:**
  - High: 4 or more of 7 answers at E3, and the consistency check passes.
  - Medium: 4 or more at E2 or E3, at least one E3, and the check passes.
  - Low: anything else, including any move that fails its consistency check.
- **Reading the results:** A high score with Low confidence means the answers describe documented capability that has not been proven under exercise.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 7 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 7 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 7 | 0 |
| 4 Substitution | 4 | High | 0 | 0 | 3 | 4 |
| 5 Market exit | 3 | Low | 0 | 0 | 7 | 0 |

**Move 1 Safe pause**
- All 7 answers are C/E2, so the average is 3.0 and the score is 3. The evidence average is 2.00, which is not below 2, so no evidence cap applies. Q1 is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passes: the approver is the Operations Director and artifacts are in the quality document system.

**Move 2 Treasury reroute**
- All 7 answers are C/E2, giving a score of 3. No evidence cap applies (evidence average 2.00), and Q1 (alternate banks and rails) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The check passes: the approver is the CFO with the Treasurer as backup, and artifacts are in the treasury system. However, Q4 "likely" means the reroute is not proven within 72 hours.

**Move 3 Data switchboard**
- All 7 answers are C/E2, giving a score of 3. No evidence cap applies (evidence average 2.00), and Q1 (data flow map) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The check passes: the approver is the CIO and artifacts are in the IT service management tool. The shutdown runbook (Q3) and emergency access logging (Q4) are untested, which matters most in a ransomware scenario.

**Move 4 Substitution**
- Answers Q1–Q4 are D/E3 and Q5–Q7 are C/E2. The pattern average is 25/7 ≈ 3.57, giving a score of 4. The evidence average is 18/7 ≈ 2.57, so no evidence cap applies. Q2 is D, so no prerequisite cap applies.
- Confidence is High: 4 of 7 answers are E3 and the check passes. The April 2026 exercise has a drill log and a CAPA in the risk system, the approver is the COO, and artifacts are in the procurement system.
  - This assumes April 2026 falls within 12 months of the assessment date.
  - Cutover governance (Q7), logistics reroute (Q6) and concentration limits (Q5) remain untested.

**Move 5 Market exit**
- All 7 answers are C/E2, giving a score of 3. No evidence cap applies (evidence average 2.00), and Q1 (exit plan) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The check passes: the approver is the CEO and artifacts are in the board portal. The regulator and customer comms workflow (Q7) has templates but no approval workflow.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist plus rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contract suspension clause summary: Documented
- Decision log: Documented
- Resume plan: Documented
- Escalation path: Documented

**Move 2 Treasury reroute**
- Alternate bank and rail register (pre-cleared): Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire definitions: Documented
- 72-hour reroute procedure: Documented
- KYC/KYB bundle: Documented
- Alternate settlement playbook: Documented
- Treasury authority and backup matrix: Documented

**Move 3 Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options summary: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Documented
- OT or critical access boundary description: Documented
- Retention and deletion procedure: Documented

**Move 4 Substitution**
- Ranked single-point-of-failure list (quarterly review): Tested
- Qualified alternates register: Tested
- Portability and failover plan: Tested
- Substitution and portability rights map: Tested
- Concentration limits policy: Documented
- Logistics reroute plan: Documented
- Cutover gate criteria: Documented
- Drill log and CAPA record (April 2026): Tested

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor/JV obligations map: Documented
- Assets and IP handling procedure: Documented
- Regulator and customer comms templates: Documented

## 5) 72-Hour Breakpoints

1. **0–6h | Move 1 | Missing authority:** Only the Operations Director is named as approver for the pause, with no backup. If that role is unreachable during the outage, the warehouse pause stalls without a documented, tested delegate.
2. **0–6h | Moves 1, 5 | Comms approval delay:** The comms templates exist but are not pre-approved (Move 1 Q3 C; Move 5 Q7 C). Issuing the holding statement then waits on ad hoc approval while customers and the order portal go dark.
3. **0–6h | Move 3 | Missing artifact:** The containment and shutdown runbook lives in the IT service management tool, and whether it is available offline is unknown. If ransomware affects that tool or the identity layer behind it, the runbook cannot be retrieved when it is needed.
4. **6–24h | Move 3 | Missing gate:** Emergency and privileged access logging is documented but untested (Q4 C). Granting emergency access to restore or isolate systems without a proven audit trail risks reinfection and leaves the decision undefended.
5. **6–24h | Move 3 | Operational infeasibility:** The manual order-intake fallback needs customer, order and hazardous-product data that sits in the ERP. The data flow map is documented but not "current and reviewed," so the source of offline data is unconfirmed.
6. **6–24h | Move 4 | Missing gate:** The COO signs off at the cutover gate, but the gates are untested (Q7 C). It is unknown whether the April 2026 drill covered manual intake with the second supplier's portal, so the gate criteria may not be decidable under time pressure.
7. **6–24h | Move 2 | Operational infeasibility:** Payment runs normally originate from the ERP, and the reroute is only "likely" within 72 hours (Q4 C, untested). Paying suppliers and the logistics provider without ERP payables data has no proven path.
8. **24–72h | Move 2 | Missing gate:** Counterparty tripwires are defined but not monitored (Q3 C), and the freeze or hold playbook is untested. Manual payment changes during an outage would therefore have no proven control against payment diversion.
9. **24–72h | Move 4 | Missing alternate:** Logistics reroute options are planned but not exercised (Q6 C), and there is a single Tier-1 logistics provider. If that provider's dispatch depends on ERP feeds, outbound deliveries stop even after cutover.
10. **24–72h | Moves 1, 5 | Missing gate:** The resume criteria (Move 1 Q6 C) and the customer obligations plan (Move 5 Q3 C) are untested. Restarting order release after ERP restore, or deciding whether to escalate toward exit-level actions if recovery slips past day five, lacks proven gates.

## 6) Top Blockers and Fixes

1. **Pause authority has no tested delegate**
   - Evidence gap: Move 1 Q1 and Q7 are E2. No exercise and no named backup.
   - Minimal fix (2 weeks): Name a backup approver for each warehouse and add them to the authority matrix.
   - Proper fix (6–12 weeks): Exercise the delegation in a drill, log it and open a CAPA.
   - Owner role: Operations Director.

2. **Holding statements are not pre-approved**
   - Evidence gap: Move 1 Q3 and Move 5 Q7 are C/E2.
   - Minimal fix (2 weeks): Pre-approve a ransomware holding statement for customers and staff.
   - Proper fix (6–12 weeks): Build an approval workflow with owners and service times, and test it in a drill.
   - Owner role: Communications lead, with the CEO approving.

3. **Containment and shutdown runbook is untested**
   - Evidence gap: Move 3 Q3 is E2.
   - Minimal fix (2 weeks): Walk through the runbook against the ERP-ransomware scenario.
   - Proper fix (6–12 weeks): Run a technical isolation drill on a Tier-1 system with a log and a CAPA.
   - Owner role: CIO.

4. **Offline availability of critical artifacts is unknown**
   - Evidence gap: Artifact locations are named, but their outage availability is Unknown.
   - Minimal fix (2 weeks): Create a controlled offline set covering the authority matrix, checklists, runbooks and contact roles.
   - Proper fix (6–12 weeks): Add an offline-access check to every exercise and review the set quarterly.
   - Owner role: CIO, with the Quality lead.

5. **Emergency access logging is unproven**
   - Evidence gap: Move 3 Q4 is E2.
   - Minimal fix (2 weeks): Confirm a break-glass procedure and a log owner role.
   - Proper fix (6–12 weeks): Test break-glass use with an audit trail review and a CAPA.
   - Owner role: CIO.

6. **Treasury reroute is not proven within 72 hours**
   - Evidence gap: Move 2 Q1 and Q4 are C/E2.
   - Minimal fix (2 weeks): Document an ERP-independent payment-run procedure for critical payees, at category level only.
   - Proper fix (6–12 weeks): Exercise a low-value reroute through a pre-cleared path, then log it and open a CAPA.
   - Owner role: CFO, with the Treasurer.

7. **Tripwires and the freeze playbook are not monitored or exercised**
   - Evidence gap: Move 2 Q2 and Q3 are E2.
   - Minimal fix (2 weeks): Add outage-specific triggers, such as payee-detail change requests, with dual approval.
   - Proper fix (6–12 weeks): Run a tabletop that injects a payment-diversion attempt.
   - Owner role: Treasurer.

8. **Data needed for manual fallback is unconfirmed**
   - Evidence gap: Move 3 Q1 is C, not current and reviewed.
   - Minimal fix (2 weeks): Identify the minimum offline dataset for order intake and hazardous-goods handling.
   - Proper fix (6–12 weeks): Review the data flow map and test retrieval of that dataset with the ERP unavailable.
   - Owner role: CIO, with the Operations Director.

9. **Cutover gates and logistics reroute are untested**
   - Evidence gap: Move 4 Q6 and Q7 are E2. The April 2026 drill's scope relative to this scenario is Unknown.
   - Minimal fix (2 weeks): Write pass/fail criteria for the manual-intake cutover and confirm the logistics provider's ERP dependency.
   - Proper fix (6–12 weeks): Run a cutover drill with an evidence pack that includes the logistics reroute.
   - Owner role: COO.

10. **Resume and extended-outage gates are untested**
    - Evidence gap: Move 1 Q6 and Move 5 Q1 and Q3 are E2.
    - Minimal fix (2 weeks): Define restart gates after ERP restore and a decision point for outages beyond five days.
    - Proper fix (6–12 weeks): Exercise restart and customer-obligation steps in a tabletop.
    - Owner role: Operations Director, with the CEO.

## 7) 30/60/90-Day Plan

### Workstream 1: First 6 hours (Moves 1, 3)

- **Outcome:** The pause, holding statement and containment steps run without the ERP or online tools, with E3 evidence.
- **Tasks:**
  - Name backup approvers for the pause decision.
  - Pre-approve holding statements.
  - Build the offline artifact set.
  - Walk through the containment runbook.
  - Define the break-glass access procedure.
  - Run the 45-minute drill (Section 8).
- **Gates:**
  - Backup approvers are recorded in the matrix (day 30).
  - The drill log and at least one CAPA exist (day 60).
  - The offline set is retrieved successfully during the drill.
- **Owner roles:** Operations Director, CIO, Communications lead.
- **Stop rule:** Pause the workstream if containment work conflicts with a live incident response. Live response takes priority.

### Workstream 2: Treasury continuity (Move 2)

- **Outcome:** Critical payments run without the ERP within 72 hours, and diversion controls are proven.
- **Tasks:**
  - Write the ERP-independent payment-run procedure.
  - Confirm pre-cleared paths are still usable.
  - Add outage tripwires and dual approval.
  - Exercise a low-value reroute.
  - Inject a diversion attempt in a tabletop.
- **Gates:**
  - The procedure is approved by the CFO (day 30).
  - The reroute exercise is logged with a CAPA (day 90).
- **Owner roles:** CFO, Treasurer.
- **Stop rule:** Do not move live funds in an exercise without dual approval and the bank's confirmation of the test arrangement.

### Workstream 3: Order and logistics cutover (Moves 3, 4, 5)

- **Outcome:** Manual intake, the second supplier's portal and the logistics reroute are proven, and restart and extended-outage gates are defined.
- **Tasks:**
  - Define the minimum offline dataset.
  - Write cutover pass/fail criteria.
  - Confirm the logistics provider's ERP dependency.
  - Run a cutover drill.
  - Define restart gates and the decision point for outages beyond five days.
- **Gates:**
  - The cutover criteria are signed by the COO (day 30).
  - The drill evidence pack and CAPA exist (day 90).
  - Restart gates are approved by the CEO (day 90).
- **Owner roles:** COO, Operations Director, CIO, CEO.
- **Stop rule:** Halt any drill step involving hazardous-goods handling if the safety checklist cannot be fully verified.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Operations Director (pause)
- CFO or Treasurer (payments)
- CIO (containment and data)
- COO (cutover)
- Communications lead
- CEO (extended-outage decision)
- Scribe (decision log)

**Agenda**
- 0–5 min: Inject. The ERP is encrypted at 06:00 and the order portal is down. Rule: online documents are unavailable.
- 5–15 min (0–6h window): Pause order release, retrieve the safety checklist offline, issue the holding statement, start containment. Absence inject: the primary pause approver is unreachable.
- 15–28 min (6–24h window): Choose manual intake and the second supplier's portal, choose the payment-run path, decide on emergency access. The COO applies the cutover gate.
- 28–40 min (24–72h window): Execute and monitor the backlog and payments. Inject: a payee-detail change request arrives. The logistics provider reports a dispatch issue.
- 40–45 min: Hot debrief and CAPA capture.

**Decisions to log**
- Pause approver and time
- Holding statement approver and time
- Containment and emergency access decision
- Cutover gate pass/fail
- Payment path chosen
- Response to the payment-change request
- Logistics decision
- Restart or extended-outage decision point

**Evidence to capture**
- Timestamped decision log
- Which artifacts were retrievable offline and which were not
- Approval timings
- Gates applied and outcomes
- Stalls observed

**CAPA prompt**
- For each stall: What blocked us? Which artifact, authority, alternate or gate was missing? What is the 2-week fix? Who owns it? When will we re-test it?

## 9) Escalations

**ESCALATE: Criminal matter.** Ransomware is a criminal act. Planning should route the decision on law enforcement contact and any notification questions to executive leadership and counsel.

**ESCALATE (conditional): Sanctions.** If the organization ever considers a ransom payment, the sanctions questions involved require counsel review before any action. This packet makes no sanctions determination.

**ESCALATE (potential): Physical safety.** Handling specialty chemicals during an ERP outage with manual processes may affect physical safety, for example because hazardous-goods data is unavailable. Safety decisions route to the Operations Director, the EHS function (if it exists, Unknown) and executive leadership.

**Thresholds not met:**
- USD 2 million is below USD 10 million.
- 2,000 people is below 100,000.
- No regulator inquiry was reported.

**Recommended path:** Incident lead → CEO plus counsel (internal or external) → board notification per your governance. Questions for counsel:
- Notification obligations in your jurisdiction (Unknown).
- Law enforcement engagement.
- Ransom-payment restrictions.
- Contractual notice to Tier-1 customers and suppliers.

## 10) Known Limits + Version

- **Self-report bias:** All answers are self-assessed. Four moves rated every question C/E2, a uniform pattern worth independent challenge.
- **No document validation:** No artifacts were reviewed, so "Documented" and "Tested" reflect claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Notification, data and contractual questions require counsel.
- **Scenario simplification:** A single 5-day ERP outage does not capture concurrent data exfiltration, an extended outage or supplier-side compromise.
- **Exercise date assumption:** Move 4 High confidence assumes the April 2026 exercise is within 12 months of the assessment date. Its scope relative to this scenario is Unknown.
- **Tabletop limits:** The mini tabletop was a narrative walk-through, not a live exercise. Its breakpoints are candidates, not observed failures.
- **Impact figures:** Impact and population figures are your estimates and were not validated.
- **Scope of this packet:** This is informational planning output. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

**Move 4 Substitution:** Score 4, Confidence High

### Turn 3, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 3, assistant (stop_reason end_turn)

**Move 4 Substitution:** Score 4, Confidence High

## Score

**Verdict: PASS.** Move 4's score and confidence match the values computed independently from the Reference Pack (score 4, High). The packet reports both in its Scorecard, and the two follow-up turns restate them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
