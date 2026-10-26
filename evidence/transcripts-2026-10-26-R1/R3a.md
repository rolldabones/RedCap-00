# redcap-00-r1 R3a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:30 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R3: reference.md 8.2 "Set the move score to 0, reported as Unknown/Insufficient data, if and only if more than half of the move’s answers are A at E0"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 5 (Market exit) with Unknown/Insufficient data (score 0) and confidence Low, and no later turn changes either value. Expected value computed in tests.md: 3 of 4 answers at A/E0 give 0, reported as Unknown/Insufficient data

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: A, E0. Q2 Trigger-based termination and unwind paths: A, E0. Q3 Customer obligations and support plan: A, E0. Q4 Data and people plan: B, E1.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: no approver named; nothing documented.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Optionality Self-Check: Output Packet
**Larkspur Chemical Supply (fictional) · Fast Baseline**

---

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions, plus consistency checks)
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. Your estimate of worst-case impact is about USD 2m, with no more than 2,000 people affected.
- **Tier-1 scope summary:** Specialty chemicals B2B distribution, about 400 staff, three warehouses in one country, about 300 business customers. Tier-1 covers the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

---

## 2) How Scoring Works

- **Answers:** Each answer is scored A=1, B=2, C=3, D=4. The move's average is rounded, and an exact half rounds down. D requires testing in the last 12 months with logs and CAPA.
- **Evidence:** E0=0 (none), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised within 12 months with log and CAPA).
- **Caps:** If a move's evidence average is below 2, its score is capped at 2. If the move's prerequisite question is answered A, its score is also capped at 2.
- **Zero rule:** A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Confidence:**
  - High requires more than half of answers at E3.
  - Medium requires more than half at E2 or E3, at least one E3, and a passed consistency check.
  - Anything else is Low.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | **0: Unknown/Insufficient data** | **Low** | 3 | 1 | 0 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C at E2, giving an average of 3.00. The evidence average is 2.00, so no evidence cap applies. Q1 is not A, so no prerequisite cap applies. The final score is 3.
- Confidence is Low because there is no E3 answer. The consistency check passes: the Operations Director is named as approver and artifacts sit in the quality document system. The stop authority has not been exercised under test.

**Move 2: Treasury reroute (3, Low)**
- All four answers are C at E2, giving an average of 3.00. No cap applies, so the final score is 3. Alternate rails are pre-cleared, and 72-hour execution is rated "likely", not "proven".
- Confidence is Low because there is no E3 answer. The consistency check passes: the CFO is approver, the Treasurer is backup, and artifacts sit in the treasury system.

**Move 3: Data switchboard (3, Low)**
- All four answers are C at E2, giving an average of 3.00. No cap applies, so the final score is 3. The data flow map, transfer options, shutdown runbook and access logging are all documented but untested.
- Confidence is Low because there is no E3 answer. The consistency check passes: the CIO is approver and artifacts sit in the IT service management tool. This is the move under most stress in a ransomware scenario.

**Move 4: Substitution (3, Low)**
- All four answers are C at E2, giving an average of 3.00. No cap applies, so the final score is 3. Alternates are qualified, but they are not confirmed viable within 72 hours, and the failover plan is untested.
- Confidence is Low because there is no E3 answer. The consistency check passes: the COO is approver and artifacts sit in the procurement system.

**Move 5: Market exit (0, Low)**
- Three of four answers (Q1–Q3) are A at E0, so the zero rule applies. The score is 0 and is reported as Unknown/Insufficient data, and caps are not computed. Q4 (data and people plan) is B at E1, which means it is verbal only.
- Confidence is Low. The consistency check technically passes because there are no E2 or E3 answers, but no approver role is named and no artifact exists.

---

## 4) Evidence Index

Labels map to evidence levels as follows: Unknown = E0 or not asked, Claimed = E1, Documented = E2, Tested = E3. Q5–Q7 artifacts were not asked in Fast Baseline and are marked Unknown.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path under conflict: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire triggers and escalation: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement or letters of credit playbook: Unknown
- Treasury authority and backup delegation: Claimed (named in the consistency check; no artifact cited)

**Move 3: Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4: Substitution**
- Ranked Tier-1 single point of failure list: Documented
- Alternate qualification records: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5: Market exit**
- Exit plan covering legal, ops, data, people, comms and support: Unknown
- Termination and unwind paths summary: Unknown
- Customer obligations and support plan: Unknown
- Data and people plan: Claimed
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

---

## 5) 72-Hour Breakpoints

All five breakpoints are drawn from your answers and have not been exercised.

- **0–6h · Move 1 · Comms approval delay.**
  - Source: Q3 is C at E2. Templates exist but are not pre-approved with a workflow.
  - Why it blocks: the first holding statement to about 300 customers waits on ad hoc sign-off while the ERP and order portal are down.
- **6–24h · Move 2 · Operational infeasibility.**
  - Source: Q4 is C at E2. 72-hour execution is "likely", not proven by exercise.
  - Why it blocks: with the ERP down, an unrehearsed reroute through pre-cleared rails may fail on data, approval or format dependencies nobody has surfaced.
- **0–6h · Move 3 · Missing gate.**
  - Source: Q3 is C at E2. The segmentation and shutdown runbook has never been tested.
  - Why it blocks: without validated go/no-go criteria, the CIO cannot confidently isolate or stop cleanly in the first hours of a ransomware event.
- **24–72h · Move 4 · Operational infeasibility.**
  - Source: Q3 is C at E2. The failover plan is documented but untested, and Q2 alternates are not confirmed viable within 72 hours.
  - Why it blocks: substituting for ERP-dependent order, inventory and dispatch functions may not stand up within the window.
- **24–72h · Move 5 · Missing artifact (and missing authority).**
  - Source: Q1 is A at E0. There is no exit plan and no approver.
  - Why it blocks: if the outage escalates into a decision to exit a customer segment, lane or relationship, nobody owns the decision and no steps exist.

---

## 6) Top Blockers and Fixes

**1. No exit plan (Move 5, Q1: A, E0)**
- **Evidence gap:** No artifact and no owner.
- **Minimal fix (2 weeks):** Write a one-page exit skeleton covering legal, ops, data, people, comms and support, with a named owner role.
- **Proper fix (6–12 weeks):** A documented exit plan for Tier-1 relationships, validated in a tabletop.
- **Owner role:** COO (interim, pending executive designation).

**2. No trigger-based termination or unwind paths (Move 5, Q2: A, E0)**
- **Evidence gap:** Unknown at planning level.
- **Minimal fix (2 weeks):** Have counsel produce a high-level trigger and unwind summary for the five Tier-1 relationships, with redacted summaries only.
- **Proper fix (6–12 weeks):** Documented unwind paths, rehearsed in a tabletop.
- **Owner role:** General Counsel.

**3. No customer obligations and support plan (Move 5, Q3: A, E0)**
- **Evidence gap:** Obligations to about 300 customers are unmapped.
- **Minimal fix (2 weeks):** Build a top-customer obligations summary and a support contact plan.
- **Proper fix (6–12 weeks):** A documented support plan with scripts and a comms workflow.
- **Owner role:** Head of Sales or Customer Service.

**4. Data and people plan is verbal only (Move 5, Q4: B, E1)**
- **Evidence gap:** No artifact and no owner.
- **Minimal fix (2 weeks):** Convert the verbal plan into a written checklist with an owner role.
- **Proper fix (6–12 weeks):** Rehearsed responsibilities and steps.
- **Owner role:** CIO jointly with the HR Director.

**5. No approver named for market exit (Move 5, consistency check)**
- **Evidence gap:** Missing authority.
- **Minimal fix (2 weeks):** The board or executive committee designates an exit approver and a backup.
- **Proper fix (6–12 weeks):** Add the role to the authority matrix and log it in a drill.
- **Owner role:** CEO.

**6. Comms templates not pre-approved (Move 1, Q3: C, E2)**
- **Evidence gap:** No approval workflow and no test.
- **Minimal fix (2 weeks):** Pre-approve a ransomware holding statement for internal, customer and regulator audiences, routed through counsel.
- **Proper fix (6–12 weeks):** Pre-approved templates with workflow and owners, exercised in a drill.
- **Owner role:** Head of Communications.

**7. Stop authority never exercised (Move 1, Q1: C, E2)**
- **Evidence gap:** No exercise date, log or CAPA.
- **Minimal fix (2 weeks):** Walk through the authority matrix and confirm the Operations Director's backup.
- **Proper fix (6–12 weeks):** Exercise the delegated stop authority with a logged decision and a CAPA.
- **Owner role:** Operations Director.

**8. Treasury reroute not proven within 72 hours (Move 2, Q1 and Q4: C, E2)**
- **Evidence gap:** Pre-cleared only, not tested.
- **Minimal fix (2 weeks):** Map the ERP dependencies of the reroute path.
- **Proper fix (6–12 weeks):** A tested reroute with evidence, a log and a CAPA.
- **Owner role:** CFO, with the Treasurer as backup.

**9. Shutdown runbook and emergency access logging untested (Move 3, Q3 and Q4: C, E2)**
- **Evidence gap:** No E3 evidence.
- **Minimal fix (2 weeks):** Peer-review the runbook against an ERP-outage scenario and define go/no-go gates.
- **Proper fix (6–12 weeks):** Test the runbook and access logging with an audit trail and a CAPA.
- **Owner role:** CIO.

**10. Failover and alternates not proven viable within 72 hours (Move 4, Q2 and Q3: C, E2)**
- **Evidence gap:** Documented, not tested.
- **Minimal fix (2 weeks):** Confirm with each alternate what they can actually deliver within 72 hours.
- **Proper fix (6–12 weeks):** A failover test for ERP-dependent order and dispatch functions, with a log and a CAPA.
- **Owner role:** COO.

---

## 7) 30/60/90-Day Plan

### Workstream A: Build the Market Exit baseline (Move 5)

**Outcome:** Move 5 moves from Unknown to documented (E2), with a named approver.

**Tasks:**
- Designate an exit approver and a backup (Day 30).
- Draft an exit plan skeleton across legal, ops, data, people, comms and support (Day 30).
- Have counsel prepare a trigger and unwind summary for Tier-1 relationships (Day 60).
- Write up the customer obligations and support plan and the data and people checklist (Day 60).
- Validate all Move 5 artifacts in a tabletop (Day 90).

**Gates:**
- Approver named in the authority matrix.
- All four Q1–Q4 artifacts at E2.
- Tabletop log exists.

**Owner roles:** CEO (approver designation), COO, General Counsel, Head of Sales, CIO, HR Director.

**Stop rule:** Pause if counsel identifies a matter requiring legal determination, and route it to counsel before proceeding.

### Workstream B: Convert Moves 1–4 from E2 to E3 by exercise

**Outcome:** At least one E3 answer per move, which makes Medium confidence attainable.

**Tasks:**
- Run the 45-minute ERP-ransomware drill (Section 8) by Day 30.
- Open CAPAs and record the month/year and log location (Day 30).
- Test the Move 3 shutdown runbook and the Move 2 reroute path in a controlled exercise (Day 60).
- Test the Move 4 failover for order and dispatch functions (Day 60).
- Re-run the Fast Baseline to confirm E3 entries (Day 90).

**Gates:**
- Every claimed E3 has a month/year, a log and a CAPA.
- Re-scored consistency checks pass.

**Owner roles:** Operations Director, CFO, CIO, COO.

**Stop rule:** Halt any live test that risks production, safety or customer impact. Revert to tabletop instead.

### Workstream C: Ransomware comms and escalation readiness

**Outcome:** Pre-approved holding statements and an escalation path ready for a ransomware event.

**Tasks:**
- Pre-approve internal, customer and regulator holding templates (Day 30).
- Document the counsel and executive escalation path for criminal, sanctions and safety questions (Day 30).
- Add an approval workflow with owners and backups (Day 60).
- Exercise the workflow in the Workstream B drill (Day 90).

**Gates:**
- Templates signed off by counsel.
- Workflow timed in a drill.

**Owner roles:** Head of Communications, General Counsel, CISO or CIO.

**Stop rule:** Never publish statements that misstate facts. Stop and escalate if a statement's accuracy cannot be confirmed.

---

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Operations Director (stop)
- CFO and Treasurer (reroute)
- CIO (data switch)
- COO (substitution)
- Exit approver, or the CEO if none is designated
- General Counsel
- Head of Communications
- Scribe

**Agenda**
- **0–5 min:** Scenario brief. The ERP is encrypted, with an expected five-day outage, and the order portal is degraded.
- **5–15 min:** 0–6h decisions. What is paused, who authorizes it, which safety checks apply, and what the first holding statement says.
- **15–28 min:** 6–24h decisions. Which treasury rail, data posture and logistics or supplier path are chosen, what the gates are, and who signs off.
- **28–38 min:** 24–72h decisions. What is executed and monitored, and whether any exit or termination question arises.
- **38–45 min:** Hot wash and CAPA capture.

**Decisions to log**
- Stop decision and its approver.
- Reroute decision.
- Isolate or stop-cleanly decision.
- Substitution cutover.
- Holding statement approval.
- Exit or no-exit decision.
- Escalation-to-counsel decision.

**Evidence to capture**
- Timestamps and roles.
- Artifacts used, by type and location (no content).
- Gates passed or failed.
- Time-to-approval for comms.

**CAPA prompt**
"Where did we wait, guess, or lack an owner? For each, name one corrective action, an owner role and a due date."

---

## 9) Escalations

**ESCALATE.** Triggers are identified from the scenario as described.

- **Criminal:** A ransomware attack is a criminal act. Decisions on engaging law enforcement and handling a criminal extortion event need counsel and executive involvement.
- **Sanctions (conditional):** If any ransom payment were ever contemplated, potential sanctions exposure must go to specialist counsel. No sanctions determination is made here.
- **Physical safety (potential):** You warehouse specialty chemicals. If the ERP outage affects hazmat inventory, storage or handling information, safety must be confirmed by the HSE lead.
- **Not triggered on the figures provided:** Estimated impact (about USD 2m) is below USD 10m, and people affected (2,000 or fewer) is below 100,000. No regulator inquiry is indicated.

**Recommended escalation path**
1. Incident lead (CIO/CISO) and Operations Director.
2. CEO and General Counsel.
3. External counsel: cyber/criminal, plus sanctions specialist if payment is ever raised.
4. Board or risk committee.
5. HSE lead in parallel for safety.

**Questions for counsel**
- What notification or reporting duties may apply in our jurisdiction?
- How should law enforcement engagement be handled?
- What review is required before any payment decision?
- What constraints apply to customer and regulator statements?

---

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed. "Documented" reflects your claim of artifact type and owner role.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Nothing here is a legal, compliance or sanctions determination.
- **Scenario simplification:** A single five-day ERP outage is modelled. Cascading effects on the order portal, suppliers, logistics and safety are not fully represented.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run, and those artifacts are marked Unknown. Deepening is available on request.
- **Confidence vs. score:** Scores of 3 for Moves 1–4 carry Low confidence because nothing has been exercised in the last 12 months.
- **Move 5:** The score of 0 reflects insufficient data, not a measured inability.
- **Impact figures:** The USD and people figures are your estimates and have not been verified.
- **Not advice:** This is informational planning guidance only. It is not legal advice or certification.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 5, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 5 (Market exit): **Score 0 (Unknown/Insufficient data), Confidence Low.**

## Score

**Verdict: PASS.** The user supplied three of four Move 5 answers at A/E0 (Q1, Q2, Q3) and Q4 at B/E1. Under reference.md 8.2 that triggers the zero rule, so the expected score is 0 (Unknown/Insufficient data), and confidence is Low under Section 4. The packet reports exactly that in the Scorecard. Turn 2 restates the same values without change. All pass elements are met and no fail indicator appears.

---

Final Liability rests with the Human.
