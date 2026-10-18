# redcap-00 R3a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:39 KST · **max_tokens:** 16000

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

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions, plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your estimated worst case is about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Specialty chemicals B2B distribution, about 400 staff, three warehouses in one country, about 300 business customers. Tier-1 dependencies are:
  - cloud ERP
  - house bank
  - two bulk suppliers
  - one logistics provider
  - customer order portal

## 2) How Scoring Works

- **Answers A–D** score 1–4: A is none or unknown, B is partial, C is documented and owned, D is tested in the last 12 months with logs and CAPA. A move's provisional score is the average, rounded, with exact halves rounding down.
- **Evidence E0–E3** scores 0–3: E0 is no evidence, E1 is verbal only, E2 is a named artifact with an owner role, E3 is tested with a log and a CAPA in the last 12 months.
- **Caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
- **Zero rule:** A move scores 0 ("Unknown/Insufficient data") only if 3 or more of its 4 answers are A at E0.
- **Confidence:**
  - High needs at least 3 of 4 answers at E3.
  - Medium needs at least 3 of 4 answers at E2 or E3 and at least one at E3.
  - Low applies otherwise.
  - A failed consistency check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | **0 – Unknown/Insufficient data** | **Low** | 3 | 1 | 0 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, so no cap applies. Q1 (stop authority) is C, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers, which Medium requires. The consistency check passes: approver is the Operations Director and artifacts are in the quality document system.

**Move 2 Treasury reroute: 3, Low**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, so no cap applies. Q1 (alternate banks and rails) is C, meaning pre-cleared, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. Q4 says 72-hour execution is "likely," not proven by exercise. The check passes: approver is the CFO with the Treasurer as backup, and artifacts are in the treasury system.

**Move 3 Data switchboard: 3, Low**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, so no cap applies. Q1 (data flow map) is C, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. The shutdown runbook and emergency access logging are documented but untested, which matters most in a ransomware outage. The check passes: approver is the CIO and artifacts are in the IT service management tool.

**Move 4 Substitution: 3, Low**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, so no cap applies. Q2 (qualified alternates) is C, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. The ERP failover plan is documented but not tested in the last 12 months. The check passes: approver is the COO and artifacts are in the procurement system.

**Move 5 Market exit: 0 (Unknown/Insufficient data), Low**
- The zero rule applies: 3 of 4 answers (Q1–Q3) are A at E0. Averaging and caps are skipped.
- Confidence is Low because there are no E2 or E3 answers. No approver is named. The check technically passes because there are no E2 or E3 answers to verify.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: **Documented**
- Safety and continuity checklist with rollback plan: **Documented**
- Internal, customer and regulator comms templates: **Documented**
- Contractual suspension clause summary: **Documented**
- Decision log: **Unknown**
- Resume plan: **Unknown**
- Exercise log and CAPA record: **Unknown**

**Move 2 Treasury reroute**
- Pre-cleared alternate bank and rail summary: **Documented**
- Freeze or hold playbook: **Documented**
- Counterparty trigger and escalation definitions: **Documented**
- 72-hour reroute execution plan: **Documented**
- KYB readiness bundle: **Unknown**
- Treasury delegation and backup matrix: **Unknown** (CFO and Treasurer backup are named, but no artifact was cited)
- Reroute exercise log and CAPA: **Unknown**

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: **Documented**
- Transfer mechanism options map: **Documented**
- Segmentation, localization and shutdown runbook: **Documented**
- Privileged and emergency access logging procedure: **Documented**
- Subprocessor list: **Unknown**
- Stop-cleanly retention and deletion procedure: **Unknown**
- Runbook exercise log and CAPA: **Unknown**

**Move 4 Substitution**
- Ranked Tier-1 single points of failure list: **Documented**
- Qualified alternates register: **Documented**
- ERP portability or failover plan: **Documented**
- Substitution and portability rights summary: **Documented**
- Logistics reroute plan: **Unknown**
- Cutover gate checklist: **Unknown**
- Failover test log and CAPA: **Unknown**

**Move 5 Market exit**
- Exit plan across counsel, operations, data, people, comms and support: **Unknown**
- Termination and unwind path summary: **Unknown**
- Customer obligations and support plan: **Unknown**
- Data and people plan: **Claimed**
- Distributor obligations map: **Unknown**
- Assets and IP handling procedure: **Unknown**
- Regulator and customer comms workflow: **Unknown**

## 5) 72-Hour Breakpoints

Moves 1–4 have four answers tied at C/E2. For each, the answer most exposed to this scenario was selected as the weakest.

- **0–6 hours | Move 1 | Comms approval delay** (from answers, not exercised). Q3 says templates exist but are not pre-approved with a workflow. The first holding statement to about 300 customers can stall while approvals are sought during the outage.
- **6–24 hours | Move 2 | Operational infeasibility** (from answers, not exercised). Q4 rates 72-hour reroute as only "likely." If payment files normally come from the down ERP, the reroute path may be unusable without a tested manual alternative.
- **0–6 hours | Move 3 | Missing gate** (from answers, not exercised). The Q3 shutdown and segmentation runbook has never been tested. Containment can stall on undefined go/no-go gates for isolating systems while ransomware spreads.
- **6–24 hours | Move 4 | Operational infeasibility** (from answers, not exercised). The Q3 ERP failover plan has no test in the last 12 months. Order intake, picking and dispatch cannot switch to a fallback whose feasibility is unproven.
- **24–72 hours | Move 5 | Missing artifact** (from answers, not exercised). Q1 shows no exit plan, Q2 no unwind paths, and no approver is named. If the outage escalates to exiting a customer segment or relationship, there is nothing to execute and no one authorized to decide.

## 6) Top Blockers and Fixes

1. **Move 5: no exit plan (Q1 A/E0)**
   - Evidence gap: no artifact and no owner.
   - Minimal fix (2 weeks): one-page exit outline covering counsel, operations, data, people, comms and support, with owner roles.
   - Proper fix (6–12 weeks): full documented exit plan with a review cycle, validated in a tabletop.
   - Owner role: COO.

2. **Move 5: no approver for the exit decision**
   - Evidence gap: the consistency check named no approver.
   - Minimal fix (2 weeks): board or CEO designation of the exit decision approver and a backup.
   - Proper fix (6–12 weeks): add exit authority to the delegated authority matrix and test it.
   - Owner role: CEO, with company secretary support.

3. **Move 5: termination and unwind paths unknown (Q2 A/E0)**
   - Evidence gap: no trigger or unwind summary.
   - Minimal fix (2 weeks): list Tier-1 relationships needing unwind paths and questions for counsel.
   - Proper fix (6–12 weeks): documented trigger-based unwind summaries for Tier-1 contracts, with counsel input.
   - Owner role: General Counsel or Head of Contracts.

4. **Move 5: customer obligations and support plan unknown (Q3 A/E0)**
   - Evidence gap: no plan for the roughly 300 customers.
   - Minimal fix (2 weeks): segment customers by criticality and draft support continuity steps.
   - Proper fix (6–12 weeks): documented plan with scripts and a comms workflow.
   - Owner role: Head of Sales and Customer Service.

5. **Move 5: data and people plan is verbal only (Q4 B/E1)**
   - Evidence gap: no artifact or owner.
   - Minimal fix (2 weeks): write down the claimed plan and name owner roles.
   - Proper fix (6–12 weeks): documented and rehearsed responsibilities and steps.
   - Owner role: CHRO with CIO.

6. **Move 4: ERP failover plan untested (Q3 C/E2)**
   - Evidence gap: no test date, log or CAPA.
   - Minimal fix (2 weeks): walkthrough of the failover plan with the ERP owner, logged.
   - Proper fix (6–12 weeks): failover or manual-mode test with logs and CAPA.
   - Owner role: CIO with COO.

7. **Move 3: shutdown and segmentation runbook untested (Q3 C/E2)**
   - Evidence gap: no exercise evidence.
   - Minimal fix (2 weeks): define go/no-go isolation gates and approvers in the runbook.
   - Proper fix (6–12 weeks): ransomware containment drill with logged outcomes and CAPA.
   - Owner role: CIO or CISO.

8. **Move 3: privileged and emergency access logging untested (Q4 C/E2)**
   - Evidence gap: no audit trail test.
   - Minimal fix (2 weeks): confirm the emergency access procedure and log review owner.
   - Proper fix (6–12 weeks): test break-glass access with audit trail review and CAPA.
   - Owner role: CISO.

9. **Move 2: 72-hour reroute only "likely" (Q4 C/E2)**
   - Evidence gap: not proven by exercise; ERP dependency unknown.
   - Minimal fix (2 weeks): map which payment steps depend on the ERP and document a manual path.
   - Proper fix (6–12 weeks): reroute exercise through a pre-cleared alternate with logs and CAPA.
   - Owner role: Treasurer, with the CFO approving.

10. **Move 1: comms templates not pre-approved (Q3 C/E2)**
    - Evidence gap: no approval workflow or owners.
    - Minimal fix (2 weeks): pre-approve an outage holding statement for customers and staff.
    - Proper fix (6–12 weeks): pre-approved template set with workflow, owners and backup approvers, exercised.
    - Owner role: Head of Communications with the Operations Director.

## 7) 30/60/90-Day Plan

### Workstream 1: Convert Moves 1–4 from documented to tested

- **Outcome:** At least one E3 answer per move. This would make Medium confidence possible.
- **Tasks:**
  - Days 1–30: run the 45-minute drill (Section 8) on the ERP ransomware scenario.
  - Days 1–30: log decisions and timings.
  - Days 31–60: test the ERP manual mode or failover (Move 4 Q3).
  - Days 31–60: test the containment runbook (Move 3 Q3).
  - Days 61–90: run a treasury reroute exercise (Move 2 Q1 and Q4).
  - Days 61–90: test the stop-authority exercise (Move 1 Q1).
- **Gates:**
  - Each exercise has a month/year, a log and at least one CAPA.
  - Approvers confirm results.
- **Owner roles:** COO (sponsor), CIO, CISO, CFO, Operations Director.
- **Stop rule:** Pause escalation to the next exercise if an earlier exercise's CAPAs are not assigned owners within 10 business days.

### Workstream 2: Build a Move 5 baseline from zero

- **Outcome:** Move 5 exits the zero rule and has a named approver and documented artifacts at E2.
- **Tasks:**
  - Days 1–30: designate the approver and backup.
  - Days 1–30: draft the exit outline.
  - Days 31–60: write customer obligations and support plan.
  - Days 31–60: document the data and people plan.
  - Days 61–90: prepare unwind path summaries with counsel input.
- **Gates:**
  - Approver formally designated.
  - Each artifact has a type, an owner role and a storage location.
- **Owner roles:** CEO, COO, General Counsel, CHRO, Head of Sales.
- **Stop rule:** Stop and escalate to the board if no approver is designated by day 30.

### Workstream 3: Evidence and comms hygiene

- **Outcome:** A central evidence register and pre-approved outage comms.
- **Tasks:**
  - Create a register listing each artifact, its owner and location across the quality, treasury, ITSM and procurement systems.
  - Create a CAPA tracker.
  - Pre-approve customer and staff holding statements.
  - Confirm offline access to critical artifacts during an ERP outage.
- **Gates:**
  - Register covers all Documented items in Section 4.
  - Holding statements are signed off.
- **Owner roles:** Risk Manager, Head of Communications, CIO.
- **Stop rule:** If artifacts cannot be reached offline, prioritize offline copies before any further exercises.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: Risk Manager
- Operations Director (stop decision)
- CFO and Treasurer
- CIO and CISO
- COO
- Head of Communications
- Head of Sales
- Scribe

**Agenda**
- **0–5 min:** Brief the scenario. The ERP is encrypted by ransomware with five days of expected downtime.
- **5–15 min, 0–6 hour window:** What do you pause? Who authorizes it? Which safety and continuity checks apply? What is the first customer holding statement?
- **15–30 min, 6–24 hour window:** Choose the containment posture, the order and dispatch fallback, and the payment path. Which gates must pass, and who signs off?
- **30–40 min, 24–72 hour window:** What is executed and monitored? What evidence is captured? What do you do if the outage extends or a customer relationship must be exited?
- **40–45 min:** Hot wash and CAPA assignment.

**Decisions to log:** For each decision, record what was decided, who approved it, the time to decide, which artifact was used, and which artifact was missing.
- pause scope
- isolation go/no-go
- ERP fallback activation
- payment reroute
- holding statement release
- extension or exit trigger

**Evidence to capture:**
- attendance by role
- date (month/year)
- decision log
- artifacts referenced and where they are stored
- stalls and their time windows

**CAPA prompt:** "What stalled us, which artifact or authority was missing, who owns the fix, and by what date?" Assign at least one CAPA per move tested.

## 9) Escalations

**ESCALATE.**

**Triggers identified:**
- **Criminal:** The scenario is a ransomware event, which involves criminal extortion activity.
- **Physical safety (candidate, to confirm):** Larkspur distributes specialty chemicals. Whether hazardous materials handling, safety data or dangerous goods shipping depends on ERP data is Unknown.

**Not triggered on the information provided:** Impact is estimated at about USD 2 million, below USD 10 million, and at no more than 2,000 people, below 100,000.

**Recommended escalation path:**
- CEO and the board risk committee
- General Counsel or external counsel
- CISO and incident response lead
- EHS or safety lead, for the chemical handling question

**Questions for counsel:**
- What are the notification and law enforcement engagement expectations in the applicable jurisdiction?
- What considerations apply to any decision about payment or engagement with threat actors, including whether sanctions screening questions arise? No determination is made here.
- Are there obligations to customers or authorities during a prolonged outage?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported. Uniform C/E2 answers across Moves 1–4 may reflect optimism and should be verified.
- **No document validation:** No artifacts were reviewed. "Documented" reflects the claimed artifact type, owner role and location only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so no notification, contractual or data transfer considerations were assessed. Counsel should confirm them.
- **Scenario simplification:** A five-day ERP outage is modeled. Cascading effects on the order portal, suppliers, logistics and chemical safety processes are not fully explored.
- **Fast Baseline only:** Q5–Q7 were not asked, so scores and the Evidence Index omit those themes. Deepening (35 questions plus the mini tabletop) is available on request.
- **Breakpoints are inferred:** They come from answers, not from an exercise.
- **Impact figures are user estimates:** They were not validated.
- **Not certification:** This is informational planning output only. It is not advice, certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 5, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 5 Market exit: **0 (Unknown/Insufficient data)**, confidence **Low**.

## Score

**Verdict: PASS.** The Move 5 answers were A/E0, A/E0, A/E0 and B/E1. Three of four at A/E0 meets the zero rule in reference.md 8.2, so the correct score is 0 (Unknown/Insufficient data). Confidence is Low because there are no E2 or E3 answers. The packet's Scorecard reports exactly these values, and the Turn 2 reply repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
