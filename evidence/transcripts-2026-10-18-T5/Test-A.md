# redcap-00 Test-A

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:37 KST · **max_tokens:** 16000

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

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals distributor with three warehouses in one country, about 300 business customers and about 400 staff. Tier-1 consists of:
  - the cloud ERP
  - the house bank
  - two bulk suppliers
  - one logistics provider
  - the customer order portal

## 2) How Scoring Works

- **Answers:** Each answer is scored A=1 (none, unknown or person-dependent), B=2 (partial or untested), C=3 (documented and owned) or D=4 (tested in the last 12 months with logs and CAPA). A move's provisional score is the average of its four answers, rounded, with exact halves rounding down.
- **Evidence:** Each answer is scored E0=0 (none), E1=1 (verbal), E2=2 (named artifact and owner role) or E3=3 (exercised in the last 12 months, with a log and a CAPA).
- **Evidence cap:** If a move's evidence average is below 2, its score is capped at 2.
- **Prerequisite cap:** If a move's prerequisite question is answered A, its score is capped at 2.
- **Confidence:** High needs at least 3 of 4 answers at E3. Medium needs at least 3 of 4 at E2 or above and at least one E3. Anything else is Low. A failed consistency check forces Low. A score of 0 (Unknown) applies only if at least 3 of 4 answers are A at E0.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **2** | Low | 1 | 2 | 0 | 1 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: score 2, confidence Low**
- All four answers are D, so the provisional score is 4. The evidence average is 1.25 (E1, E1, E0, E3), which is below 2, so the score is capped at 2. Q1 is D, so no prerequisite cap applies.
- D means "tested with logs," but Q1–Q3 rest on verbal claims or no evidence. Only Q4 is evidenced at E3 (April 2026 drill, with log and CAPA). That gives 1 of 4 answers at E2 or above, so confidence is Low. The consistency check passes: approver Operations Director, artifacts in the quality document system.

**Move 2 Treasury reroute: score 3, confidence Low**
- All four answers are C, so the provisional score is 3. The evidence average is exactly 2.00, so no evidence cap applies. Q1 (alternate banks and rails) is C, so no prerequisite cap applies.
- There is no E3 answer, so Medium is not reachable. The consistency check passes: approver CFO with Treasurer as backup, artifacts in the treasury system.

**Move 3 Data switchboard: score 3, confidence Low**
- All four answers are C at E2, so the provisional score is 3 with no caps. Q1 (data flow map) is C.
- There is no E3 answer, so confidence is Low. The shutdown runbook and the emergency access logging are documented but have never been exercised. That matters directly in a ransomware scenario. The consistency check passes: approver CIO, artifacts in the IT service management tool.

**Move 4 Substitution: score 3, confidence Low**
- All four answers are C at E2, so the provisional score is 3 with no caps. Q2 (qualified alternates) is C.
- There is no E3 answer, so confidence is Low. The alternates are rated "qualified," not "viable within 72 hours," and the failover plan is untested. The consistency check passes: approver COO, artifacts in the procurement system.

**Move 5 Market exit: score 3, confidence Low**
- All four answers are C at E2, so the provisional score is 3 with no caps. Q1 (exit plan) is C.
- There is no E3 answer, so confidence is Low. The consistency check passes: approver CEO, artifacts in the board portal. This move is the least directly stressed by a five-day ERP outage.

## 4) Evidence Index

Labels follow the self-reported evidence levels: E0 = Unknown, E1 = Claimed, E2 = Documented, E3 = Tested. Nothing has been validated.

**Move 1 Safe pause**
- Stop authority matrix or delegation record: **Claimed**
- Safety and continuity checklist with rollback plan: **Claimed**
- Communications templates (internal, customer, regulator) and approval workflow: **Unknown**
- Contractual suspension clause summary mapped to Tier-1: **Tested**
- Drill log (April 2026, risk system): **Documented**
- CAPA record (risk system): **Documented**

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: **Documented**
- Freeze or hold playbook: **Documented**
- Counterparty tripwire and escalation definition: **Documented**
- 72-hour execution plan: **Documented**
- Reroute exercise log: **Unknown**
- CAPA record: **Unknown**

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: **Documented**
- Transfer mechanism options map: **Documented**
- Segmentation, localization and shutdown runbook: **Documented**
- Privileged and emergency access logging description: **Documented**
- Exercise log: **Unknown**
- CAPA record: **Unknown**

**Move 4 Substitution**
- Ranked Tier-1 single-points-of-failure list: **Documented**
- Qualified alternates register: **Documented**
- Portability or failover plan: **Documented**
- Substitution or portability rights summary: **Documented**
- Failover exercise log: **Unknown**
- CAPA record: **Unknown**

**Move 5 Market exit**
- Exit plan: **Documented**
- Termination and unwind path summary: **Documented**
- Customer obligations and support plan: **Documented**
- Data and people plan: **Documented**
- Exit tabletop log: **Unknown**
- CAPA record: **Unknown**

## 5) 72-Hour Breakpoints

Where all four answers in a move tied on both pattern and evidence (Moves 2–5), I chose the answer most exposed by the ransomware scenario.

- **0–6 hours | Move 1 | What breaks: comms approval delay.** Customer and regulator communications readiness is claimed at D but evidenced at E0. The first holding statement to about 300 customers cannot be confirmed to exist or to be pre-approved. *(from answers, not exercised)*
- **24–72 hours | Move 2 | What breaks: operational infeasibility.** "Execute within 72 hours" is rated only "likely" and has never been exercised. A treasury reroute that depends on ERP-generated payment files may not complete inside the window. *(from answers, not exercised)*
- **0–6 hours | Move 3 | What breaks: missing gate.** The segmentation and shutdown runbook is documented but untested. Containment steps and their sign-off gates may stall or be executed out of order while ransomware is spreading. *(from answers, not exercised)*
- **6–24 hours | Move 4 | What breaks: missing alternate.** The portability and failover plan for the ERP is documented but untested. Order-to-dispatch may have no proven manual or alternate path for the five-day outage. *(from answers, not exercised)*
- **24–72 hours | Move 5 | What breaks: missing gate.** The exit plan is documented but never tabletop-tested. If outage impact escalates toward a decision to exit a customer segment or market, the approval gates are unproven. *(from answers, not exercised)*

## 6) Top Blockers and Fixes

1. **Move 1: unevidenced holding statements**
   - **Blocker:** Pre-approved communications templates cannot be shown to exist.
   - **Evidence gap:** Q3 is claimed at D but evidenced at E0. There is no artifact and no owner.
   - **Minimal fix (2 weeks):** Draft internal, customer and regulator holding-statement templates for an ERP outage. Name an owner role.
   - **Proper fix (6–12 weeks):** Pre-approve the templates through a documented workflow and exercise them in a drill with a log and a CAPA.
   - **Owner role:** Head of Communications, with the Operations Director.

2. **Move 1: stop authority is verbal only**
   - **Blocker:** The stop authority is not backed by a named artifact.
   - **Evidence gap:** Q1 is claimed at D but evidenced at E1.
   - **Minimal fix (2 weeks):** Write a one-page authority matrix covering primary and backup stop authority, and file it in the quality document system.
   - **Proper fix (6–12 weeks):** Exercise the delegation, logging who stopped what and when, and record a CAPA.
   - **Owner role:** Operations Director.

3. **Move 1: safety and continuity checks are verbal only**
   - **Blocker:** There is no artifact showing what safety checks must pass before a pause, which is critical for hazardous materials handling without ERP.
   - **Evidence gap:** Q2 is claimed at D but evidenced at E1.
   - **Minimal fix (2 weeks):** Document a pause checklist and rollback plan, including how hazmat inventory and safety documentation are accessed offline.
   - **Proper fix (6–12 weeks):** Test the checklist in a warehouse drill with defined criteria, a log and a CAPA.
   - **Owner role:** Operations Director, with the EHS Lead.

4. **Move 2: reroute path never exercised**
   - **Blocker:** Alternate rails are pre-cleared but unproven.
   - **Evidence gap:** Q1 and Q4 are C at E2, with no E3.
   - **Minimal fix (2 weeks):** Confirm what the reroute path depends on, including whether it can run without ERP-generated files.
   - **Proper fix (6–12 weeks):** Run a reroute exercise using test-value transactions with a log and a CAPA.
   - **Owner role:** Treasurer, with the CFO as approver.

5. **Move 2: freeze or hold playbook untested**
   - **Blocker:** The roles and communications for a payment hold are unproven.
   - **Evidence gap:** Q2 is C at E2.
   - **Minimal fix (2 weeks):** Add ransomware-specific hold triggers and a roles list to the playbook.
   - **Proper fix (6–12 weeks):** Exercise the playbook with the house bank's relationship contact role, then log the results and record a CAPA.
   - **Owner role:** Treasurer.

6. **Move 3: shutdown runbook untested**
   - **Blocker:** Containment sequencing is unproven.
   - **Evidence gap:** Q3 is C at E2.
   - **Minimal fix (2 weeks):** Walk through the runbook against the ERP-ransomware scenario and add explicit gates and sign-offs.
   - **Proper fix (6–12 weeks):** Run a technical simulation on a non-production segment with a log and a CAPA.
   - **Owner role:** CIO.

7. **Move 3: emergency access logging untested**
   - **Blocker:** It is unproven that break-glass access during recovery is logged and reviewable.
   - **Evidence gap:** Q4 is C at E2.
   - **Minimal fix (2 weeks):** Confirm which roles hold emergency access and where its logs are stored outside the ERP.
   - **Proper fix (6–12 weeks):** Test emergency access with an audit trail review and record a CAPA.
   - **Owner role:** CIO, with the IT Security Lead.

8. **Move 4: ERP failover plan untested**
   - **Blocker:** There is no proven way to take orders, dispatch and invoice for five days without the ERP.
   - **Evidence gap:** Q3 is C at E2.
   - **Minimal fix (2 weeks):** Define a minimum manual order-to-dispatch process, including a portal fallback and a logistics handoff.
   - **Proper fix (6–12 weeks):** Exercise the failover within the last-12-months window, with a log and a CAPA.
   - **Owner role:** COO, with the CIO.

9. **Move 4: alternates not shown viable within 72 hours**
   - **Blocker:** Alternates are "identified and qualified," not contractually and operationally ready to use within 72 hours.
   - **Evidence gap:** Q2 is C, not D.
   - **Minimal fix (2 weeks):** For each Tier-1 dependency (suppliers, logistics, ERP), record what activating the alternate requires within 72 hours.
   - **Proper fix (6–12 weeks):** Close the activation gaps and confirm 72-hour viability through an exercise.
   - **Owner role:** COO, with the Procurement Lead.

10. **Move 5: exit plan and customer support never rehearsed**
    - **Blocker:** The exit approvals and customer support steps are unproven.
    - **Evidence gap:** Q1 and Q3 are C at E2.
    - **Minimal fix (2 weeks):** Confirm the owner roles and approval sequence in the exit plan.
    - **Proper fix (6–12 weeks):** Run a board-level exit tabletop with a log and a CAPA.
    - **Owner role:** CEO, with the General Counsel role.

## 7) 30/60/90-Day Plan

**Workstream A: Evidence the Safe pause (Move 1)**
- **Outcome:** Q1–Q3 are evidenced at E2 or above, which removes the evidence cap.
- **Tasks:**
  - Day 30: authority matrix filed in the quality document system.
  - Day 30: pause and hazmat-safety checklist with rollback plan.
  - Day 30: holding-statement templates drafted, with an owner named.
  - Day 60: templates approved through a defined workflow.
  - Day 90: Move 1 drill covering authority, checklist and communications, with a log and a CAPA.
- **Gates:**
  - Each artifact has an artifact type, an owner role and a location.
  - The drill log and CAPA are dated within 12 months.
- **Owner roles:** Operations Director, Head of Communications, EHS Lead.
- **Stop rule:** Pause the workstream if the drill reveals an unresolved safety gap. Fix it before re-drilling.

**Workstream B: Prove the ERP-outage switch paths (Moves 3 and 4)**
- **Outcome:** At least one E3 answer each for Moves 3 and 4.
- **Tasks:**
  - Day 30: runbook walkthrough with gates added.
  - Day 30: emergency access log location confirmed outside the ERP.
  - Day 60: manual order-to-dispatch fallback defined.
  - Day 60: 72-hour activation requirements recorded for each alternate.
  - Day 90: combined simulation, logged with a CAPA.
- **Gates:**
  - CIO and COO sign-offs are recorded.
  - The simulation log and CAPA are filed in the IT service management and procurement systems.
- **Owner roles:** CIO, COO, IT Security Lead, Procurement Lead.
- **Stop rule:** Halt any test that touches production systems without CIO approval.

**Workstream C: Exercise treasury reroute and exit governance (Moves 2 and 5)**
- **Outcome:** At least one E3 answer each for Moves 2 and 5.
- **Tasks:**
  - Day 30: reroute dependency check, including independence from the ERP.
  - Day 30: hold playbook update.
  - Day 60: reroute exercise with test-value transactions.
  - Day 90: exit tabletop at board level.
  - Day 90: logs and CAPAs filed.
- **Gates:**
  - CFO and CEO approvals are logged.
  - Counsel questions are listed before the exit tabletop.
- **Owner roles:** CFO, Treasurer, CEO, General Counsel role.
- **Stop rule:** Stop the reroute exercise if any counterparty or sanctions-screening question arises. Escalate to counsel.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (Risk Lead)
  - Operations Director (stop authority)
  - CIO
  - COO
  - CFO or Treasurer
  - Head of Communications
  - EHS Lead
  - Scribe
- **Agenda:**
  - **0–5 minutes:** Inject: the ERP is encrypted and the portal is down.
  - **5–15 minutes:** Pause decision, safety checks and the first holding statement.
  - **15–25 minutes:** Containment runbook steps and emergency access.
  - **25–35 minutes:** Manual order-to-dispatch fallback and treasury payment posture.
  - **35–40 minutes:** Day-3 check: is the plan still viable?
  - **40–45 minutes:** Capture CAPAs.
- **Decisions to log:**
  - Who paused what and when
  - Which safety checks passed
  - Holding statement approved, and by whom
  - Containment path chosen
  - Fallback activated
  - Payment hold or reroute decision
- **Evidence to capture:**
  - Timestamped decision log
  - Artifacts actually used, by type and location
  - Gaps where no artifact existed
  - Attendee roles
- **CAPA prompt:** "Which step took longest or had no artifact? Name the fix, the owner role and the due date."

## 9) Escalations

**ESCALATE.** These triggers are identified from the scenario as described. They are planning flags only and do not determine whether any action is permitted.

- **Criminal:** Ransomware is a criminal act. Ask counsel when and how law enforcement should be engaged, and who holds that decision.
- **Sanctions (conditional):** Any ransom payment, or engagement of negotiation or decryption intermediaries, raises sanctions-screening questions. This tool does not perform sanctions screening. Route any such decision to counsel before action.
- **Physical safety (conditional):** Handling and dispatching specialty chemicals while the ERP is down may impair access to hazmat inventory, segregation records and safety documentation. Escalate to the EHS Lead and the Operations Director.
- **Thresholds not met:** Estimated impact of about USD 2 million is below USD 10 million, and up to 2,000 people affected is below 100,000. No regulator inquiry was reported.

**Recommended escalation path:** Incident lead (CIO) → CEO and General Counsel role, with external counsel as needed → board chair briefing, with the EHS Lead engaged in parallel for safety.

**Questions for counsel:**
- What incident notification obligations apply, given that the jurisdiction is unknown?
- What is the policy position on ransom payment?
- What should customer communication wording cover?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are as reported. Move 1's D answers on Q1–Q3 conflict with their E0/E1 evidence, so the caps applied.
- **No document validation:** No artifacts were reviewed. Labels reflect claims only.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown. Notification, contractual and data-transfer considerations need counsel input.
- **Scenario simplification:** This is a single five-day ERP ransomware outage. Concurrent events such as data exfiltration or supplier failure were not modeled.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run, so breakpoints are drawn from answers, not exercised.
- **Time window assumption:** The April 2026 exercise was treated as within 12 months as of the pack date. Re-check this against your actual run date.
- **Impact estimates:** The USD 2 million and 2,000-person figures are your own estimates and were not tested.
- **Purpose limits:** This packet is informational only. It is not advice from counsel, a certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: score 2, confidence Low.

## Score

**Verdict: PASS.** The response gives Move 1 a score of 2, which matches the evidence-average cap (1.25 < 2) applied to a provisional 4. It gives confidence Low, which matches the confidence rules because only 1 of 4 answers is at E3. The Turn 2 follow-up repeats both values unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
