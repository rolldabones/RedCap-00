# redcap-00 R1b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:39 KST · **max_tokens:** 16000

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

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

*For information and planning only. This is not advice from counsel, a certification, or a sanctions screening.*

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers) plus consistency checks.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. The user estimates worst-case impact at about USD 2m and no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor.
  - Three warehouses in one country.
  - About 300 business customers and about 400 staff.
  - Tier-1 dependencies: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

---

## 2) How Scoring Works

- **Answer scores:** A–D map to pattern scores 1–4 (A = none or ad hoc, B = partial, C = documented and owned, D = tested in the last 12 months with alternates viable). The move score is the mean, rounded to the nearest whole number. Exact halves round **down**.
- **Evidence scores:** E0 = none, E1 = verbal only, E2 = a named artifact plus an owner role, E3 = tested within 12 months with a log and a CAPA. E3 needs a month/year, a log and a CAPA.
- **Caps:** A move's score is capped at 2 if its evidence average is below E2. It is also capped at 2 if its prerequisite question is answered A.
- **Zero rule:** A move is scored 0 (Unknown) only if more than half of its answers are A at E0.
- **Confidence:**
  - **High** needs more than half of the move's answers at E3.
  - **Medium** needs more than half at E2 or E3 and at least one E3.
  - **Low** applies otherwise, or whenever the move's consistency check fails.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C at E2, so the provisional score is 3.0. The evidence average is 2.0, which does not trigger the cap, and the prerequisite Q1 is C, so neither cap applies. The final score is 3.
- There are no E3 answers, so confidence is Low. The consistency check passes: the approver is the Operations Director and artifacts are in the quality document system. Stop authority has never been exercised under a 72-hour clock.

**Move 2 Treasury reroute: 3, Low**
- All four answers are C at E2, so the provisional score is 3.0. The prerequisite Q1 (alternate banks and rails) is C, so no cap applies. The final score is 3.
- There are no E3 answers, so confidence is Low. The consistency check passes: the CFO approves, the Treasurer is backup, and artifacts are in the treasury system. "Execute within 72 hours" is rated "likely" and has not been proven by an exercise.

**Move 3 Data switchboard: 3, Low**
- All four answers are C at E2, so the provisional score is 3.0. The prerequisite Q1 (data flow map) is C, so no cap applies. The final score is 3.
- There are no E3 answers, so confidence is Low. The consistency check passes: the CIO approves and artifacts are in the ITSM tool. The shutdown runbook and emergency access logging are untested, and these are central to a ransomware response.

**Move 4 Substitution: 3, Low**
- The answers are D, D, C and C, giving a mean of 3.5, which rounds down to 3. The evidence average is 2.0 and the prerequisite Q2 is D, so no cap applies. The final score is 3.
- Both D answers sit at E2, with no test date, log or CAPA. Under the anti-inflation rule, "viable within 72 hours" needs verification. There are no E3 answers, so confidence is Low. The consistency check passes: the COO approves and artifacts are in the procurement system.

**Move 5 Market exit: 3, Low**
- All four answers are C at E2, so the provisional score is 3.0. The prerequisite Q1 (exit plan) is C, so no cap applies. The final score is 3.
- There are no E3 answers, so confidence is Low. The consistency check passes: the CEO approves and artifacts are in the board portal. Customer support scripts and the comms workflow are documented but not ready to use.

---

## 4) Evidence Index

**Move 1 Safe pause**
- Stop-authority matrix: Documented
- Safety/continuity checklist with rollback plan: Documented
- Comms templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path under conflict: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger definitions with escalation: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement or LC playbook: Unknown
- Treasury delegation and backup matrix: Claimed

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked single-point-of-failure list: Documented (quarterly review records not evidenced)
- Qualified alternates register: Documented (72-hour viability not tested)
- Portability or failover plan: Documented
- Substitution or portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligation map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

---

## 5) 72-Hour Breakpoints

- **Move 1** *(from answers, not exercised)*
  - **Time window:** 0–6 hours.
  - **What breaks:** Comms approval delay. The Q3 templates exist but are not pre-approved and have no workflow.
  - **Why it blocks execution:** The first holding statement to customers and staff can stall while wording and sign-off are negotiated in the middle of the outage.
- **Move 2** *(from answers, not exercised)*
  - **Time window:** 24–72 hours.
  - **What breaks:** Operational infeasibility. Q4 rates 72-hour execution only as "likely".
  - **Why it blocks execution:** No exercise has shown that payments and receipts can run through pre-cleared alternate rails while the ERP payment data is unavailable.
- **Move 3** *(from answers, not exercised)*
  - **Time window:** 0–6 hours.
  - **What breaks:** Missing gate. The Q3 shutdown and segmentation runbook is documented but untested.
  - **Why it blocks execution:** Untested isolation steps risk either over-shutting Tier-1 systems or leaving spread paths open in the first hours.
- **Move 4** *(from answers, not exercised)*
  - **Time window:** 6–24 hours.
  - **What breaks:** Missing gate. The Q3 failover plan is documented but not tested.
  - **Why it blocks execution:** Switching order-taking, picking and dispatch to a manual or alternate path has no proven sequence or go/no-go gates.
- **Move 5** *(from answers, not exercised)*
  - **Time window:** 24–72 hours.
  - **What breaks:** Comms approval delay. The Q3 customer support plan has no ready scripts or workflow.
  - **Why it blocks execution:** If the five-day outage forces a decision to stop serving selected customers, customer messaging cannot be issued consistently.

---

## 6) Top Blockers and Fixes

1. **Stop authority has never been exercised (M1 Q1)**
   - **Evidence gap:** E2. There is no exercise date, log or CAPA.
   - **Minimal fix (2 weeks):** Walk through the stop authority matrix against the ransomware scenario and confirm the named deputies.
   - **Proper fix (6–12 weeks):** Run a logged pause exercise at one warehouse, with a CAPA.
   - **Owner:** Operations Director.

2. **Comms templates are not pre-approved (M1 Q3)**
   - **Evidence gap:** E2. There is no approval workflow.
   - **Minimal fix:** Pre-approve one internal and one customer holding statement for a cyber outage.
   - **Proper fix:** Set up a template approval workflow with owners and backups, tested in a drill.
   - **Owner:** Communications lead with the Operations Director.

3. **Alternate rails are pre-cleared but untested (M2 Q1)**
   - **Evidence gap:** E2. There is no test evidence.
   - **Minimal fix:** Confirm the activation steps and contacts for the alternate rail, and confirm they are stored outside the ERP.
   - **Proper fix:** Run a small live test reroute with evidence captured.
   - **Owner:** Treasurer, approved by the CFO.

4. **72-hour treasury execution is only "likely" (M2 Q4)**
   - **Evidence gap:** E2. Execution has not been proven by an exercise.
   - **Minimal fix:** Map the hour-by-hour steps for payroll, supplier payments and receipts without the ERP.
   - **Proper fix:** Run a treasury tabletop with a log and a CAPA.
   - **Owner:** CFO.

5. **The shutdown and segmentation runbook is untested (M3 Q3)**
   - **Evidence gap:** E2. There is no drill record.
   - **Minimal fix:** Do a desk check of the runbook steps and the decision gates with IT operations.
   - **Proper fix:** Run a technical isolation drill in a test environment, with a log and a CAPA.
   - **Owner:** CIO.

6. **Emergency access logging is documented but not tested (M3 Q4)**
   - **Evidence gap:** E2. There is no audit-trail test.
   - **Minimal fix:** Confirm that break-glass access is logged somewhere outside the systems likely to be affected.
   - **Proper fix:** Test a break-glass session with a review of the audit trail.
   - **Owner:** CIO / Security lead.

7. **The "viable within 72h" alternates claim (M4 Q2) has no test record**
   - **Evidence gap:** The answer is D at E2, so the claim is unverified.
   - **Minimal fix:** Reconfirm with each alternate supplier and logistics provider their 72-hour activation steps and contacts.
   - **Proper fix:** Run a timed activation exercise with one alternate, with a log and a CAPA.
   - **Owner:** COO / Procurement lead.

8. **The failover plan for ERP-dependent operations is untested (M4 Q3)**
   - **Evidence gap:** E2.
   - **Minimal fix:** Prepare a manual order-to-dispatch fallback pack, including hazardous goods documentation needs. Its availability is currently Unknown.
   - **Proper fix:** Test the manual fallback at one warehouse for one shift.
   - **Owner:** COO.

9. **Customer support scripts and workflow are not ready (M5 Q3)**
   - **Evidence gap:** E2. The plan is documented, but there are no scripts.
   - **Minimal fix:** Draft scripts for the order portal outage and delayed deliveries.
   - **Proper fix:** Build a scripted workflow for prioritizing the roughly 300 customers, tested in a drill.
   - **Owner:** Commercial / Customer Service Director.

10. **The data and people plan has not been rehearsed (M5 Q4)**
    - **Evidence gap:** E2.
    - **Minimal fix:** Confirm role assignments and backups for a partial market or customer withdrawal.
    - **Proper fix:** Run a board-level exit tabletop with a CAPA.
    - **Owner:** CEO with the HR Director.

**Cross-cutting question:** It is Unknown whether the quality document system, treasury system, ITSM tool, procurement system and board portal stay reachable if the ERP or its identity layer is encrypted. Confirm this for all ten items above.

---

## 7) 30/60/90-Day Plan

**Workstream A: Ransomware pause and isolation readiness (Moves 1, 3)**
- **Outcome:** Moves 1 and 3 each have at least three answers at E3, with logs and CAPAs.
- **Tasks:**
  - Confirm offline access to the stop authority matrix and runbooks.
  - Pre-approve holding statements.
  - Desk check the isolation runbook.
  - Test break-glass logging.
  - Run the 45-minute drill (Section 8).
  - Close the first CAPAs.
- **Gates:**
  - Day 30: offline artifact access is confirmed.
  - Day 60: the drill has run and is logged.
  - Day 90: CAPAs are closed or scheduled.
- **Owner roles:** Operations Director, CIO, Communications lead.
- **Stop rule:** Pause the workstream if a real incident occurs. Switch to live response and capture its evidence instead.

**Workstream B: Treasury and supply substitution proof (Moves 2, 4)**
- **Outcome:** 72-hour execution is proven for one payment rail and one alternate supplier or logistics path.
- **Tasks:**
  - Map the hour-by-hour treasury steps without the ERP.
  - Run a small test reroute.
  - Reconfirm 72-hour activation with the alternates.
  - Build and test a manual order-to-dispatch fallback.
  - Log and assign CAPAs.
- **Gates:**
  - Day 45: the steps are mapped and reviewed.
  - Day 75: the test reroute and the supplier activation are complete with evidence.
  - Day 90: CAPAs are assigned.
- **Owner roles:** CFO, Treasurer, COO, Procurement lead.
- **Stop rule:** Halt any live test that would disrupt customer deliveries or payroll timing.

**Workstream C: Customer and exit comms readiness (Moves 1, 5)**
- **Outcome:** Scripts and an approval workflow are ready for customer, regulator and partner messaging.
- **Tasks:**
  - Draft outage and delay scripts.
  - Build the approval workflow with backups.
  - Set customer prioritization criteria.
  - Run a board exit tabletop.
  - Record CAPAs.
- **Gates:**
  - Day 30: the scripts are drafted.
  - Day 60: the workflow is approved.
  - Day 90: the tabletop is logged.
- **Owner roles:** CEO, Commercial / Customer Service Director, Communications lead.
- **Stop rule:** Stop and refer to counsel before finalizing any regulator-facing or contract-termination wording.

---

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (Risk / Continuity lead)
  - Operations Director
  - CFO / Treasurer
  - CIO
  - COO
  - Communications lead
  - Scribe
  - CEO, as observer and final approver
- **Agenda:**
  - **0–5 min:** Brief. The ERP is encrypted at 06:00 and is expected to be down for five days.
  - **5–15 min:** Pause and isolate. Decide what stops, who authorizes it, and when the first holding statement goes out.
  - **15–25 min:** Switch paths. Cover treasury rails, the manual order and dispatch fallback, and supplier and logistics alternates.
  - **25–35 min:** Customer impact. Prioritize customers and confirm portal messaging.
  - **35–42 min:** Inject. The house bank flags unusual activity and one bulk supplier cannot ship.
  - **42–45 min:** Capture CAPAs.
- **Decisions to log:** For each decision, record the timestamp, the approver role and the artifact used:
  - pause scope
  - isolation go/no-go
  - holding statement release
  - treasury reroute
  - fallback activation
  - customer prioritization
- **Evidence to capture:**
  - attendance by role
  - the decision log
  - which artifacts were reachable during the drill and which were not
  - time to each decision
  - gaps found
- **CAPA prompt:** "Which decision took longest or needed an artifact we couldn't reach? Who fixes it, and by what date?"

---

## 9) Escalations

**ESCALATE: Criminal**
- **Trigger:** The tested scenario is a ransomware attack, which is a criminal act.
- **Recommended path:** The CIO and CEO engage outside counsel and the incident response retainer, if one exists (currently Unknown). Counsel decides on any engagement with law enforcement and notifications. The board is informed through the CEO.

**ESCALATE if arises: Sanctions questions**
- **Trigger:** Any ransom payment is considered.
- **Recommended path:** Route the matter immediately to counsel. RedCap-00 makes no sanctions determination.

**ESCALATE if arises: Physical safety**
- **Trigger:** The ERP outage removes visibility of hazardous chemical stock locations, safety data or dangerous goods documentation. This is currently Unknown.
- **Recommended path:** Escalate via the Operations Director and the site safety lead.

**Questions for counsel:**
- What notification obligations and timelines apply in the operating jurisdiction?
- What constraints apply to contract suspension notices sent to customers and suppliers?

**Impact thresholds not triggered:** USD 2m is below USD 10m, and 2,000 people is below 100,000.

---

## 10) Known Limits + Version

- **Self-report bias:** All answers are self-assessed and were not independently verified.
- **No document validation:** "Documented" labels reflect claims that an artifact and an owner exist, not a review of their content.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown, so notification and suspension questions cannot be framed precisely.
- **Scenario simplification:** One five-day ransomware outage was tested. Concurrent supplier, bank or physical events were not modeled.
- **Unverified D answers:** The two D answers under Move 4 sit at E2. They are treated as unverified until test records exist.
- **Fast Baseline scope:** Q5–Q7 were not asked, so those artifacts appear as Unknown in the Evidence Index.
- **Breakpoints not exercised:** All breakpoints come from answers and have not been exercised. Deepening mode (35 questions plus the mini tabletop) would test them.
- **Uniform scores need testing:** All moves score 3 with Low confidence. Moving to Medium or High requires E3 evidence from logged exercises with CAPAs.
- **Artifact availability:** It is Unknown whether the five artifact systems stay reachable during the outage.
- **Nature of output:** This packet is planning guidance only. It is not advice from counsel, a certification or a sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Low.

## Score

**Verdict: PASS.** The expected value follows from the reference pack. Move 4 answers D, D, C, C sum to 14, so the mean is 3.5, which rounds down to 3 under section 8.1. The evidence average is 2.0, which does not trigger the cap (the cap applies only below 2). The prerequisite Q2 is D, so no cap applies. The zero rule is not met. There are no E3 answers, so confidence is Low. The packet reports 3 and Low, and the follow-up turn repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
