# redcap-00 R5c

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:41 KST · **max_tokens:** 16000

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

- **Jurisdiction:** Unknown.
- **Mode:** Deepening. This covers 35 forced-choice answers, the consistency checks and the mini tabletop.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. Your estimates: worst-case impact about USD 2m, no more than 2,000 people affected.
- **Tier-1 scope:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with about 400 staff, 3 warehouses in one country and about 300 business customers. Tier-1 assets are:
  - cloud ERP
  - house bank
  - two bulk suppliers
  - one logistics provider
  - customer order portal

## 2) How Scoring Works

- Answers A–D map to pattern scores of 1–4. A means unknown or ad hoc. B means partial. C means documented and owned. D means tested in the last 12 months with logs and CAPA. Evidence E0–E3 maps to 0–3. E2 needs an artifact type and an owner role. E3 needs a month/year, a log and a CAPA.
- A move's score is the mean of its 7 pattern scores, rounded to the nearest whole number. A move scores 0 (Unknown/Insufficient data) only if 4 or more of its 7 answers are A at E0.
- **Evidence cap:** if a move's evidence average is below 2.0, its score is capped at 2.
- **Prerequisite cap:** if a move's prerequisite question is answered A, its score is capped at 2.
- **Confidence:**
  - High needs 4 or more of 7 answers at E3 and a passed consistency check.
  - Medium needs 4 or more at E2/E3, at least one E3, and a passed check.
  - Otherwise confidence is Low.
  - A failed consistency check forces Low.

## 3) Scorecard

**Move 1 — Safe pause** | Score **3** | Confidence **Low** | #E0 0 · #E1 0 · #E2 7 · #E3 0
- All 7 answers are C/E2. The pattern mean is 3.0 and the evidence average is 2.0, which is not below 2, so no evidence cap applies. Q1 Stop authority is C, so no prerequisite cap applies.
- The consistency check passes (approver: Operations Director; artifacts: quality document system). Confidence stays Low because no answer is at E3, so Medium is not reached.

**Move 2 — Treasury reroute** | Score **3** | Confidence **Low** | #E0 0 · #E1 0 · #E2 7 · #E3 0
- All 7 answers are C/E2. The pattern mean is 3.0, the evidence average is 2.0 and Q1 Alternate banks is C, so no caps apply. Q4 "Execute within 72 hours" is "likely", not proven.
- The consistency check passes (approver: CFO, backup Treasurer; artifacts: treasury system). Confidence is Low because there is no E3, and the reroute path is absent from your tabletop.

**Move 3 — Data switchboard** | Score **3** | Confidence **Low** | #E0 0 · #E1 0 · #E2 7 · #E3 0
- All 7 answers are C/E2. The pattern mean is 3.0, the evidence average is 2.0 and Q1 Data flow map is C, so no caps apply.
- The consistency check passes (approver: CIO; artifacts: IT service management tool). Confidence is Low because there is no E3. This matters most here because ransomware is primarily a Move 3 event, and the shutdown runbook and access logging are untested.

**Move 4 — Substitution** | Score **4** | Confidence **High** | #E0 0 · #E1 0 · #E2 3 · #E3 4
- The pattern mean is 25/7 = 3.57, which rounds to 4. The evidence average is 18/7 = 2.57, and Q2 Qualified alternates is D, so no caps apply.
- Four of 7 answers are at E3, and the check passes: the exercise was in April 2026, with a drill log and CAPA in the risk system, approver COO and artifacts in the procurement system. However, Q5–Q7 (concentration, logistics reroute, cutover governance) are documented only.

**Move 5 — Market exit** | Score **3** | Confidence **Low** | #E0 0 · #E1 0 · #E2 7 · #E3 0
- All 7 answers are C/E2. The pattern mean is 3.0, the evidence average is 2.0 and Q1 Exit plan is C, so no caps apply.
- The consistency check passes (approver: CEO; artifacts: board portal). Confidence is Low because there is no E3, and the exit plan has never been tabletopped. Its relevance to a 5-day ERP outage is indirect.

## 4) Evidence Index

Labels come from self-reported evidence levels: E0 = Unknown, E1 = Claimed, E2 = Documented, E3 = Tested. Nothing has been validated.

**Move 1 — Safe pause**
- Stop authority matrix — Documented
- Safety and continuity checklist plus rollback plan — Documented
- Communications templates (internal, customer, regulator) — Documented
- Contract suspension clause summary — Documented
- Decision log — Documented
- Resume plan — Documented
- Escalation path — Documented
- Exercise log plus CAPA record — Unknown

**Move 2 — Treasury reroute**
- Alternate bank and rail pre-clearance record — Documented
- Freeze or hold playbook — Documented
- Counterparty trigger and escalation definitions — Documented
- 72-hour execution plan — Documented
- KYC/KYB bundle — Documented
- Alternate settlement playbook — Documented
- Treasury authority and backup matrix — Documented
- Exercise log plus CAPA record — Unknown

**Move 3 — Data switchboard**
- Tier-1 data flow map (including logs and telemetry) — Documented
- Transfer mechanism options map — Documented
- Segmentation, localization and shutdown runbook — Documented
- Privileged and emergency access logging description — Documented
- Subprocessor list — Documented
- OT or critical access boundary description — Documented
- Retention and deletion procedure — Documented
- Exercise log plus CAPA record — Unknown

**Move 4 — Substitution**
- Ranked single-point-of-failure list — Tested
- Qualified alternates register — Tested
- Portability and failover plan — Tested
- Substitution rights summary for Tier-1 vendors — Tested
- Concentration limits description — Documented
- Logistics reroute plan — Documented
- Cutover gate definitions — Documented
- Drill log plus CAPA record (April 2026) — Tested

**Move 5 — Market exit**
- Exit plan — Documented
- Termination and unwind path summary — Documented
- Customer obligations and support plan — Documented
- Data and people plan — Documented
- Distributor/JV obligations map — Documented
- Assets and IP handling procedure — Documented
- Regulator and customer comms templates — Documented
- Exercise log plus CAPA record — Unknown

## 5) 72-Hour Breakpoints

These are drawn from the mini tabletop and the answers. They are candidates from a narrative walk-through, not exercised.

1. **0–6 h | Move 1 | Comms approval delay.** The holding statement template is "issued", but templates are C (not pre-approved), and the tabletop names no approver. Customer-facing release to about 300 accounts can stall waiting for sign-off.
2. **0–6 h | Move 1 | Missing authority.** Stop authority is documented but never exercised, and the tabletop names no backup if the Operations Director is unreachable. The 3-warehouse pause has no confirmed alternate authorizer.
3. **0–6 h | Move 3 | Missing gate.** The tabletop has no data-posture decision (isolate, segment or shut down) and no CIO authorization in the first 6 hours. The manual fallback could start while affected systems are still connected.
4. **0–6 h | Moves 1, 3 | Operational infeasibility.** The safety checklist (Move 1 Q2) and the OT/critical access boundary (Move 3 Q6) are untested. Whether they depend on ERP-held data, such as inventory locations or hazard information, is Unknown. If they do, the safety check cannot pass during the outage.
5. **6–24 h | Move 2 | Missing gate.** No treasury path is chosen and no CFO sign-off appears in the 6–24 h window, yet payment runs are monitored at 24–72 h. Alternate rails are pre-cleared but untested, so payments may have no proven route if house-bank initiation depends on the ERP.
6. **6–24 h | Move 4 | Missing gate.** The COO cutover gate relies on cutover governance that is documented (Q7 C/E2) but never tested with an evidence pack. Sign-off criteria may be disputed or improvised under pressure.
7. **6–24 h | Moves 4, 1 | Operational infeasibility.** Several capacities are Unknown:
   - manual order-intake capacity for about 300 customers over 5 days
   - the order portal's status during the ERP outage
   - fulfilment from the second supplier's portal

   The switch path may not sustain volume past day 1–2.
8. **6–24 h | Move 4 | Missing alternate.** There is one logistics provider, and the reroute options are planned (Q6 C), not exercised. Shipments stall if the provider's booking or labelling depends on ERP data.
9. **24–72 h | Move 1 | Missing artifact.** The resume plan is untested (Q6 C/E2), and the tabletop has no gate for returning from manual operations to the restored ERP. Reconciling manual orders and payments back into the ERP can block a clean restart.
10. **24–72 h | Move 3 | Missing artifact.** Privileged and emergency access logging is documented but untested (Q4 C/E2). The decision log alone may not provide the access trail needed for evidence capture and for safely restoring the system.

## 6) Top Blockers and Fixes

1. **Stop authority has no tested backup (Move 1)**
   - Evidence gap: E2 matrix; never exercised; alternate authorizer unnamed.
   - Minimal fix (2 weeks): name a deputy for the Operations Director per warehouse and record it in the matrix.
   - Proper fix (6–12 weeks): run a timed pause drill with the deputy authorizing, logged with CAPA.
   - Owner: Operations Director.

2. **Holding statement is not pre-approved (Moves 1, 5)**
   - Evidence gap: templates are C/E2, with no approval workflow.
   - Minimal fix (2 weeks): pre-approve one ransomware holding statement per audience and name its approver.
   - Proper fix (6–12 weeks): build a template approval workflow with time targets and exercise it in a drill.
   - Owner: Communications Lead with the CEO.

3. **Treasury reroute is untested and missing from the tabletop (Move 2)**
   - Evidence gap: Q1 and Q4 are C/E2; 72-hour execution is "likely", not proven; no CFO decision in 6–24 h.
   - Minimal fix (2 weeks): document how payment runs execute without the ERP and add a CFO decision at 6–24 h.
   - Proper fix (6–12 weeks): perform a low-value test payment via a pre-cleared alternate rail, logged with CAPA.
   - Owner: CFO, with the Treasurer.

4. **No containment decision; shutdown runbook untested (Move 3)**
   - Evidence gap: Q3 is C/E2, and there is no data-posture step in the tabletop.
   - Minimal fix (2 weeks): insert a CIO isolate/segment decision into the 0–6 h window with explicit gates.
   - Proper fix (6–12 weeks): test the segmentation and shutdown runbook on a Tier-1 system and log the outcomes.
   - Owner: CIO.

5. **Emergency access logging untested (Move 3)**
   - Evidence gap: Q4 is C/E2, so trail quality under incident conditions is unproven.
   - Minimal fix (2 weeks): confirm which logs sit outside the ERP blast radius and who retrieves them.
   - Proper fix (6–12 weeks): test break-glass access with audit-trail review and record a CAPA.
   - Owner: IT Security Lead.

6. **Manual order intake capacity is Unknown (Move 4, tabletop)**
   - Evidence gap: the fallback is named in the tabletop, but its volume, portal dependency and duration are not evidenced.
   - Minimal fix (2 weeks): estimate daily manual capacity against the 5-day order profile and define a triage rule.
   - Proper fix (6–12 weeks): run a timed manual-intake exercise for one warehouse.
   - Owner: COO, with the Customer Service Lead.

7. **Cutover governance gates untested (Move 4)**
   - Evidence gap: Q7 is C/E2, yet the COO sign-off depends on these gates.
   - Minimal fix (2 weeks): write gate criteria and the evidence-pack contents on one page.
   - Proper fix (6–12 weeks): exercise the cutover gates with a full evidence pack and follow up the CAPA.
   - Owner: COO.

8. **Single logistics provider (Move 4)**
   - Evidence gap: Q6 is C/E2 (planned, not exercised); dependence on ERP data is Unknown.
   - Minimal fix (2 weeks): identify a standby carrier and the manual booking steps.
   - Proper fix (6–12 weeks): carry out an exercised reroute with the standby, including any documentation the hazardous goods need.
   - Owner: Logistics Manager.

9. **Resume and reconciliation criteria untested (Move 1)**
   - Evidence gap: Q6 is C/E2, and there is no resume gate in the tabletop.
   - Minimal fix (2 weeks): define restore gates covering system integrity, data reconciliation and sign-off.
   - Proper fix (6–12 weeks): test a resume rehearsal that reconciles manual orders and payments back into the ERP.
   - Owner: Operations Director, with the CIO.

10. **No E3 evidence outside Move 4; exit plan never exercised (Move 5 and others)**
    - Evidence gap: 28 of 35 answers are E2, uniformly C, which suggests possible anchoring.
    - Minimal fix (2 weeks): spot-check 5 artifacts, one per move, for owner and currency.
    - Proper fix (6–12 weeks): put an annual exercise calendar in place so that each move reaches at least one E3.
    - Owner: Chief Risk Officer (or equivalent), with the CEO for Move 5.

## 7) 30/60/90-Day Plan

**Workstream 1: Pause, comms and resume (Moves 1, 5)**
- **Outcome:** Within 6 hours, the pause, holding statement and resume run with named primary and backup approvers, and the process is tested.
- **Tasks:**
  - 30 days: name deputies and pre-approve holding statements.
  - 30 days: define resume and reconciliation gates.
  - 60 days: confirm whether the safety checklist depends on the ERP and create an offline copy.
  - 60 days: build the comms approval workflow with time targets.
  - 90 days: run the 45-minute drill (Section 8) and log the CAPA.
- **Gates:**
  - Deputies are recorded in the authority matrix.
  - Statements are approved before day 30.
  - Drill log and CAPA exist by day 90.
- **Owners:** Operations Director, Communications Lead, CEO.
- **Stop rule:** Pause the workstream if the drill cannot be held by day 90. Escalate to the CEO rather than claiming E3.

**Workstream 2: Containment and data posture (Move 3)**
- **Outcome:** A CIO-authorized isolate/segment decision happens within 6 hours, with an access trail that is tested and preserved.
- **Tasks:**
  - 30 days: add the containment decision to the incident runbook.
  - 30 days: map the logs held outside the ERP blast radius.
  - 60 days: test break-glass access logging.
  - 90 days: test the segmentation and shutdown runbook on one Tier-1 system.
  - 90 days: brief counsel on notification questions (Jurisdiction Unknown).
- **Gates:**
  - The runbook step is approved by the CIO.
  - The test log and CAPA are recorded in the IT service management tool.
- **Owners:** CIO, IT Security Lead.
- **Stop rule:** Halt any test that risks production availability. Reschedule it to a non-production window.

**Workstream 3: Treasury and fulfilment continuity (Moves 2, 4)**
- **Outcome:** Payments and orders continue for 5 days without the ERP, through tested alternate paths.
- **Tasks:**
  - 30 days: document payment runs without the ERP and estimate manual intake capacity.
  - 60 days: identify a standby carrier and write cutover gate criteria.
  - 90 days: perform a low-value alternate-rail test payment.
  - 90 days: run a timed manual-intake exercise and an exercised logistics reroute.
- **Gates:**
  - CFO sign-off on the payment path.
  - COO sign-off on the cutover gates.
  - Test evidence filed in the treasury and procurement systems.
- **Owners:** CFO, Treasurer, COO, Logistics Manager.
- **Stop rule:** Stop the rail test if bank pre-clearance has lapsed. Re-clear before retrying.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Operations Director and deputy
- CFO or Treasurer
- CIO and IT Security Lead
- COO
- Communications Lead
- Logistics Manager
- Scribe and evidence keeper
- Counsel as observer

**Agenda**
- 0–5 min: brief the scenario (the ERP is encrypted and down for 5 days) and the ground rules.
- 5–15 min: work through the 0–6 h window, covering the pause, containment decision, safety checklist and holding statement approval.
- 15–25 min: work through the 6–24 h window, covering the treasury path, manual intake, supplier and carrier switch, and the cutover gate.
- 25–35 min: work through the 24–72 h window, covering execution, monitoring of the backlog and payments, and the resume gate.
- 35–42 min: hot wash, measured against the 10 breakpoints in Section 5.
- 42–45 min: assign CAPA owners and dates.

**Decisions to log**
- Who authorized the pause, and whether the deputy was used.
- Who authorized containment.
- Who approved the holding statement, with timestamp.
- Which treasury path was chosen, and the CFO decision.
- The COO cutover decision.
- The resume criteria.
- Questions routed to counsel.

**Evidence to capture**
- A timestamped decision log.
- Artifacts actually used, with their locations.
- Gaps found in artifacts.
- Time-to-decision for each window.
- Attendance and roles.

**CAPA prompt**
"Which decision took longest or lacked an artifact, approver or alternate? What is the fix, who owns it, and by what date?" Log at least one CAPA per move tested.

## 9) Escalations

**ESCALATE — Criminal.**
- Ransomware is a criminal act. Route to the CEO, counsel and the CIO/IT Security Lead.
- Counsel should decide on law enforcement engagement, insurer notification and evidence preservation.

**ESCALATE — Sanctions (conditional).**
- If any ransom payment were contemplated, it raises sanctions exposure questions. This packet makes no determination.
- Route to counsel and the board before any such decision.

**ESCALATE — Physical safety.**
- Handling specialty chemicals manually while the ERP is down may affect hazard data access, storage controls and transport documentation.
- Route to the EHS Lead and the Operations Director.

**Not triggered:**
- Estimated impact is about USD 2m, below the USD 10m threshold.
- No more than 2,000 people are affected, below the 100,000 threshold.
- No regulator inquiry has been reported.

**Questions for counsel (Jurisdiction Unknown):**
- What incident notification obligations and deadlines apply?
- Do contracts with customers and suppliers require notices during the pause?
- Which records must be preserved?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are as you stated them. No artifact was seen.
- **No document validation:** The "Documented" and "Tested" labels are unverified.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Notification, contract and data-transfer questions need counsel.
- **Scenario simplification:** The 5-day ERP outage assumes a single point of compromise. Spread to the portal, the bank interface or the logistics integration is not modeled.
- **Narrative tabletop:** The tabletop was a verbal walk-through, not an exercise. The breakpoints are candidates only.
- **Answer pattern:** 28 of 35 answers are identical (C/E2), which may reflect anchoring. Spot-checks are recommended.
- **E3 currency:** Move 4's E3 status depends on the April 2026 exercise staying within 12 months, which lapses in April 2027.
- **User estimates:** The impact figures (about USD 2m, no more than 2,000 people) are your estimates and were not tested.
- **Scope:** This packet is informational planning guidance only. It is not advice from counsel, not a certification and not sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

**Move 4: Score 4, Confidence High**

### Turn 3, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 3, assistant (stop_reason end_turn)

**Move 4: Score 4, Confidence High**

## Score

**Verdict: PASS.** The packet was produced in Turn 1. My own recomputation from the Reference Pack matches its Move 4 values: score 4 and confidence High. The two later turns repeat those values unchanged. Every element of the pass condition is met and no fail indicator appears.

---

Final Liability rests with the Human.
