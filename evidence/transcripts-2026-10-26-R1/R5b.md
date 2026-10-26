# redcap-00-r1 R5b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:30 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R5: reference.md 4 "Raising the evidence level of any answer never lowers confidence."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: a profile stronger on every axis is also Medium, not Low as under the old majority wording

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: D, E3. Q2 Qualified alternates: D, E3. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Optionality Self-Check: Output Packet

**Safety gate:** Confirmed. Inputs are summaries only and no sensitive data was received. **Mode:** Fast Baseline, as you requested. Deepening (Q5–Q7 per move plus the mini tabletop) is available if you want it later.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (20 questions plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Organization: Larkspur Chemical Supply (fictional), a specialty chemicals B2B distributor.
  - Footprint: three warehouses in one country, about 300 business customers, about 400 staff.
  - Tier-1 systems and vendors: cloud ERP, house bank, two bulk suppliers, one logistics provider, and the customer order portal.

---

## 2) How Scoring Works

- **Answer levels:** A=1 (none or ad hoc), B=2 (partial or untested), C=3 (documented and owned, limited testing), D=4 (tested in the last 12 months with logs and CAPA, alternates viable).
- **Evidence levels:** E0=0 (none), E1=1 (verbal), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months, logged, with CAPA).
- **Score:** the mean of A–D scores per move, rounded with exact halves rounding down. A move scores 0 (Unknown) only if more than half its answers are A at E0.
- **Caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
- **Confidence:**
  - High needs more than half of answers at E3.
  - Medium needs more than half at E2 or E3 plus at least one E3.
  - Both require a passing consistency check. Otherwise confidence is Low.

---

## 3) Scorecard

| Move | Score (0–4) | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | **Medium** | 0 | 0 | 2 | 2 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C/E2, so the mean is 3.0. The evidence average is 2.0, so no evidence cap applies. Q1 is C, so no prerequisite cap applies.
- The consistency check passes (Operations Director; quality document system). Confidence is Low because there is no E3 answer: nothing has been exercised in the last 12 months.

**Move 2: Treasury reroute (3, Low)**
- All four answers are C/E2, so the mean is 3.0. There is no evidence cap, and no prerequisite cap because Q1 alternate rails is C.
- The consistency check passes (CFO with Treasurer as backup; treasury system). Confidence is Low because there is no E3 answer. Execution within 72 hours is "likely" but not proven.

**Move 3: Data switchboard (3, Low)**
- All four answers are C/E2, so the mean is 3.0. There is no evidence cap, and no prerequisite cap because Q1 data flow map is C.
- The consistency check passes (CIO; IT service management tool). Confidence is Low because the shutdown runbook and the emergency access logging are untested.

**Move 4: Substitution (3, Medium)**
- Answers are D, D, C, C, so the mean is 3.5, which rounds down to 3. The evidence average is 2.5, so there is no evidence cap. Q2 qualified alternates is D, so there is no prerequisite cap.
- Confidence is Medium rather than High: only 2 of 4 answers are E3, and High needs 3 or more.
- The consistency check passes:
  - The April 2026 exercise falls within 12 months of this pack's 18 October 2026 date, with a drill log and CAPA recorded in the risk system.
  - The approver is the COO.
  - Artifacts are in the procurement system.

**Move 5: Market exit (3, Low)**
- All four answers are C/E2, so the mean is 3.0. There is no evidence cap, and no prerequisite cap because Q1 exit plan is C.
- The consistency check passes (CEO; board portal). Confidence is Low because the exit plan has never been tested in a tabletop.

---

## 4) Evidence Index

Artifact types are categories only. Q5–Q7 artifacts were not asked in Fast Baseline, so they are labeled **Unknown**.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire definitions with escalation: Documented
- 72-hour execution procedure: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement path playbook: Unknown
- Treasury authority and backup delegation: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4: Substitution**
- Ranked Tier-1 single-point-of-failure list: Tested
- Qualified alternates register: Tested
- Drill log and CAPA record (April 2026): Tested
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown

**Move 5: Market exit**
- Exit plan covering legal, ops, data, people, comms and support: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

---

## 5) 72-Hour Breakpoints

All five are **from answers, not exercised**.

- **Move 1:** from Q3 Communications readiness (C/E2).
  - Time window: 0–6 h.
  - What breaks: comms approval delay.
  - Why it blocks execution: Templates exist but are not pre-approved, so the first customer holding statement waits on sign-off while 300 customers cannot place or track orders.
- **Move 2:** from Q4 Execute within 72 hours (C/E2).
  - Time window: 24–72 h.
  - What breaks: operational infeasibility.
  - Why it blocks execution: The reroute is "likely" but never exercised, so payment runs that normally come from ERP data may not be executable while the ERP is down.
- **Move 3:** from Q3 Segmentation and shutdown runbook (C/E2).
  - Time window: 0–6 h.
  - What breaks: missing gate.
  - Why it blocks execution: An untested runbook has no proven go/no-go gate for isolating the ERP integrations (order portal, bank, logistics), so containment decisions may stall or be inconsistent.
- **Move 4:** from Q3 Portability or failover plan (C/E2).
  - Time window: 6–24 h.
  - What breaks: operational infeasibility.
  - Why it blocks execution: The ERP failover plan is documented but untested, so the switch to a manual or alternate order-to-ship process for hazardous goods is unproven at volume.
- **Move 5:** from Q1 Exit plan (C/E2).
  - Time window: 24–72 h.
  - What breaks: missing gate.
  - Why it blocks execution: The exit plan has never been tabletop-tested, so there are no proven triggers for deciding when a prolonged outage warrants unwinding specific customer or supplier commitments.

---

## 6) Top Blockers and Fixes

1. **Stop authority never exercised (Move 1, Q1).**
   - Evidence gap: E2, with no exercise log or CAPA.
   - Minimal fix (2 weeks): Run a 30-minute walk-through of the authority matrix with the Operations Director and a named alternate. Log it.
   - Proper fix (6–12 weeks): Drill a delegated stop decision for an ERP outage, with timestamps, roles and a CAPA.
   - Owner: Operations Director.

2. **Comms templates not pre-approved (Move 1, Q3).**
   - Evidence gap: C/E2, with no approval workflow.
   - Minimal fix: Pre-approve one ERP-outage holding statement each for customers, suppliers and staff.
   - Proper fix: Build a template approval workflow with named owners, and agree in advance which notices go to counsel.
   - Owner: Head of Communications.

3. **Suspension basis summarized but not mapped to Tier-1 contracts (Move 1, Q4).**
   - Evidence gap: C/E2.
   - Minimal fix: List Tier-1 counterparties and flag open questions for counsel on notice timing and force majeure applicability.
   - Proper fix: Map triggers and notice steps per Tier-1 contract, reviewed by counsel.
   - Owner: General Counsel or legal lead.

4. **Alternate rails pre-cleared but untested (Move 2, Q1).**
   - Evidence gap: no E3.
   - Minimal fix: Confirm the alternate rail can initiate payments without ERP-generated files, as a desk check.
   - Proper fix: Run a test reroute with captured evidence and a CAPA.
   - Owner: Treasurer.

5. **72-hour execution unproven (Move 2, Q4).**
   - Evidence gap: "likely," at E2.
   - Minimal fix: Draft a manual priority-payments checklist (payroll, bulk suppliers, logistics) independent of the ERP.
   - Proper fix: Exercise a 72-hour manual payment cycle with dual approval.
   - Owner: CFO.

6. **Counterparty tripwires defined but not monitored or exercised (Move 2, Q3).**
   - Evidence gap: C/E2.
   - Minimal fix: Add an outage-period tripwire: any change to payee details triggers out-of-band verification and escalation.
   - Proper fix: Monitor the triggers and exercise the escalation in a drill.
   - Owner: Treasurer.

7. **Shutdown and segmentation runbook untested (Move 3, Q3).**
   - Evidence gap: E2.
   - Minimal fix: Do a tabletop read-through of the isolation steps for the ERP, portal and bank integrations. Keep a copy available offline, since the runbook lives in the ITSM tool, which may itself be impaired.
   - Proper fix: Run a technical test of the isolation steps in a non-production environment, with logs and a CAPA.
   - Owner: CIO.

8. **Emergency access logging not tested with an audit trail (Move 3, Q4).**
   - Evidence gap: C/E2.
   - Minimal fix: Confirm that break-glass access events are logged somewhere outside the ERP environment.
   - Proper fix: Test emergency access with an audit trail review.
   - Owner: CIO or Head of IT Security.

9. **ERP failover plan untested (Move 4, Q3).**
   - Evidence gap: C/E2, even though alternates are tested.
   - Minimal fix: Confirm offline access to the minimum dataset for 5 days of operation. This includes the customer and order backlog, stock by warehouse, and hazardous-goods shipping and safety documentation.
   - Proper fix: Test a manual or alternate order-to-ship cycle in the last 12 months, with a log and CAPA.
   - Owner: COO with CIO.

10. **Exit plan and unwind paths not tabletop-tested (Move 5, Q1–Q2).**
    - Evidence gap: all E2.
    - Minimal fix: Define outage-duration triggers (for example, day 5 or day 10) for escalating to partial unwind decisions, and note questions for counsel.
    - Proper fix: Run an exit tabletop with legal, ops, data, people and comms, ending with a CAPA.
    - Owner: CEO.

---

## 7) 30/60/90-Day Plan

**Workstream 1: Run without the ERP (Moves 2 and 4)**
- **Outcome:** Priority payments and hazardous-goods order-to-ship can run for 5 days without the ERP, with evidence.
- **Tasks:**
  - Define the minimum offline dataset and how often it is refreshed.
  - Write the manual priority-payments checklist.
  - Add the payee-change tripwire.
  - Desk-check the alternate rail.
  - By day 60, run a combined treasury and logistics drill.
  - By day 90, close the CAPA.
- **Gates:**
  - Offline dataset confirmed current within the agreed refresh window.
  - Drill log and CAPA recorded in the risk system.
- **Owner roles:** CFO, Treasurer, COO, CIO.
- **Stop rule:** If the drill shows hazardous-goods documentation is unavailable offline, pause the remaining tasks and fix that gap first.

**Workstream 2: Contain and stop cleanly (Move 3)**
- **Outcome:** ERP-linked integrations can be isolated using a tested runbook, with logged emergency access.
- **Tasks:**
  - Make offline copies of the runbook and data flow map.
  - Do the tabletop read-through.
  - Run the break-glass logging check.
  - Run the non-production isolation test.
  - Record the CAPA.
- **Gates:**
  - Runbook reachable without the ITSM tool.
  - Isolation test logged with at least one CAPA.
- **Owner roles:** CIO, Head of IT Security.
- **Stop rule:** If a live incident occurs, stop the exercise work and invoke incident response and the escalation path in Section 9.

**Workstream 3: Authority and comms (Moves 1 and 5)**
- **Outcome:** Pause decisions and first communications can be authorized within 6 hours, and exit triggers are defined.
- **Tasks:**
  - Pre-approve the holding statements.
  - Walk through the authority matrix with alternates.
  - Map the Tier-1 contract notice questions for counsel.
  - Define outage-duration exit triggers.
  - Run the 45-minute drill in Section 8.
- **Gates:**
  - Holding statements approved by named owners.
  - Drill completed with a decision log and CAPA.
- **Owner roles:** Operations Director, Head of Communications, General Counsel, CEO.
- **Stop rule:** If counsel flags notice obligations that cannot be met in 72 hours, escalate to the CEO before finalizing the templates.

---

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (risk lead)
  - Operations Director (stop authority)
  - CFO and Treasurer
  - CIO
  - COO
  - Head of Communications
  - Legal lead
  - Scribe
- **Agenda:**
  - 0–5 min: Inject. The ERP is encrypted by ransomware, recovery is estimated at 5 days, and the order portal is offline.
  - 5–15 min: Decide what pauses now, who authorizes it, and the first holding statement.
  - 15–25 min: Isolation decision and the integrations cut. Confirm runbook access without the ITSM tool.
  - 25–35 min: Priority payments path, manual order-to-ship for hazardous goods, and the logistics provider handoff.
  - 35–42 min: Day-5 checkpoint, covering resume versus extended-outage triggers.
  - 42–45 min: Capture CAPA items.
- **Decisions to log:**
  - Pause scope and approver.
  - Holding statement release.
  - Isolation go/no-go.
  - Payment reroute choice.
  - Failover cutover.
  - Day-5 trigger outcome.
- **Evidence to capture:**
  - Timestamped decision log.
  - Which artifacts were actually reachable during the outage, and where.
  - Approval times.
  - Any gaps in the offline dataset.
- **CAPA prompt:** "Which decision took longest or could not be made, what artifact or authority was missing, who owns the fix, and by what date?"

---

## 9) Escalations

**ESCALATE (scenario-conditional).** No live incident was reported, but the tested scenario carries these triggers:

- **Criminal:** Ransomware is criminal activity. Pre-plan who decides on law enforcement engagement.
- **Sanctions (potential):** Any consideration of a ransom payment may raise sanctions issues. RedCap-00 does not perform sanctions screening or determinations, so route this to counsel before any decision.
- **Physical safety:** For a chemicals distributor, losing ERP-held hazardous-goods, storage or shipping data could affect safe handling and transport.

**Below the thresholds:** Financial impact (about USD 2m versus USD 10m) and people affected (2,000 or fewer versus 100,000).

**Recommended path:** Incident lead → CIO and COO → CEO → General Counsel and external counsel → Board risk chair.

**Questions for counsel (Jurisdiction: Unknown):**
- Breach and regulator notification timing.
- Contractual notice duties.
- Law enforcement engagement.
- Constraints on any ransom-related decision.

---

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported. In particular, the D ratings on Move 4 ("viable within 72 hours") are unverified.
- **No document validation:** No artifact was reviewed. "Documented" and "Tested" reflect only your claims.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification, contract and sanctions points are framed as questions for counsel only.
- **Scenario simplification:** A single 5-day ERP outage leaves out compounding events such as data exfiltration, simultaneous bank or supplier disruption, and a longer outage.
- **Partial coverage:** Fast Baseline covers only Q1–Q4. Q5–Q7 themes remain Unknown, and Deepening may change the scores.
- **Exercise date assumption:** The April 2026 exercise was treated as within 12 months, relative to the pack date of 18 October 2026.
- **Artifact availability:** Artifacts in online systems (ITSM, treasury, procurement, board portal) may be unreachable during the scenario. This was not assessed.
- **Not legal advice:** This is informational planning only. It is not legal advice, compliance certification, or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Medium.

## Score

**Verdict: PASS.** The pass condition needs Move 4 at score 3 and confidence Medium in the final packet, with no later change. The packet's Scorecard reports exactly that, and independent recomputation from the Reference Pack rules agrees: the mean of 3.5 rounds down to 3, no caps apply, and the confidence rules give Medium. The Turn 2 reply restates the same values. No fail indicator appears.

---

Final Liability rests with the Human.
