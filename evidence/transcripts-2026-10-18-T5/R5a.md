# redcap-00 R5a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:40 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R5: reference.md 4 "Medium: not High; more than half of the answers at E2 or E3, at least one answer at E3, and the move’s consistency check passes"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: baseline profile: Medium

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: D, E3.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Optionality Self-Check: Output Packet

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2m and no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Larkspur Chemical Supply (fictional), a B2B specialty chemicals distributor
  - About 400 staff, three warehouses in one country, about 300 business customers
  - Tier-1 assets: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal

## 2) How Scoring Works

- **A–D pattern score:** A=1 (none, ad hoc or person-dependent), B=2 (partial or untested), C=3 (documented, owned, limited testing) and D=4 (tested in the last 12 months with logs and CAPA). Each move's score is the mean of its answers, rounded, with exact halves rounding down.
- **Evidence:** E0=0 (none), E1=1 (verbal only), E2=2 (named artifact plus owner role) and E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
  - A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Confidence:**
  - High requires more than half of answers at E3.
  - Medium requires more than half at E2 or E3 and at least one E3.
  - Everything else is Low.
- **Consistency check:** If a move's check (exercise date, approver role, artifact location) fails, its confidence drops to Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Medium | 0 | 0 | 3 | 1 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C at E2. The average of 3.0 triggers no cap, because the evidence average is 2.0 and the prerequisite (stop authority) is answered C.
- Confidence is Low because there is no E3 answer. The pause, rollback and holding statement are documented but have not been exercised. The consistency check passes (Operations Director; quality document system).

**Move 2: Treasury reroute (3, Low)**
- All four answers are C at E2. The alternate bank and rail are pre-cleared, so the prerequisite is met. The evidence average of 2.0 triggers no cap.
- "Execute within 72 hours" is rated "likely," not proven. With no E3 answer, confidence is Low. The consistency check passes (CFO, with the Treasurer as backup; treasury system).

**Move 3: Data switchboard (3, Low)**
- All four answers are C at E2. A Tier-1 data flow map exists, so the prerequisite is met. No cap applies.
- The shutdown runbook and the emergency access logging have not been exercised, and both are central to a ransomware response. With no E3 answer, confidence is Low. The consistency check passes (CIO; IT service management tool).

**Move 4: Substitution (3, Medium)**
- Answers are C, C, C, D. The average of 3.25 rounds to 3. The evidence average of 2.25 triggers no cap, and qualified alternates are answered C, so the prerequisite is met.
- Confidence is Medium because all four answers are at E2 or E3, one answer is at E3, and the check passes:
  - The substitution rights drill in April 2026 has a log and a CAPA in the risk system.
  - The approver is the COO, and artifacts are in the procurement system.
  - The ERP failover plan itself has not been tested.

**Move 5: Market exit (3, Low)**
- All four answers are C at E2. A documented exit plan exists, so the prerequisite is met. No cap applies.
- With no E3 answer, confidence is Low. The consistency check passes (CEO; board portal). This move is of limited relevance to a five-day ERP outage, but customer support under disruption overlaps with this scenario.

## 4) Evidence Index

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan and gates: Unknown
- Escalation path under conflict: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour execution plan: Documented
- KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury delegation and backup matrix: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Unknown
- OT and critical access boundary procedure: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4: Substitution**
- Tier-1 single points of failure ranked list: Documented
- Alternate supplier and vendor qualification records: Documented
- Portability and failover plan (including ERP): Documented
- Substitution and portability rights map for Tier-1 vendors: Tested
- Drill log and CAPA record (April 2026): Tested
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5: Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

All four answers in Moves 1, 2, 3 and 5 are tied at C/E2. In each of those moves, and among Move 4's three tied C/E2 answers, the answer most relevant to the ransomware scenario was selected as the weakest.

- **0–6 hours | Move 1 | Missing gate** (Q2, safety and continuity checks: C/E2; from answers, not exercised): The checklist and rollback plan lack tested pass/fail criteria. Pausing dispatch of chemical orders without ERP visibility depends on untested judgment about what is safe to hold or release.
- **6–24 hours | Move 2 | Operational infeasibility** (Q4, execute within 72 hours: rated "likely," C/E2; from answers, not exercised): The reroute has never been run end to end. With the ERP down, payment files, approvals and reconciliation may not be producible in time to protect supplier payments and payroll.
- **0–6 hours | Move 3 | Missing gate** (Q3, segmentation and shutdown runbook: C/E2; from answers, not exercised): The runbook is untested and stored in the IT service management tool, which may itself be affected. Containment steps could stall before they start.
- **6–24 hours | Move 4 | Missing alternate** (Q3, portability and failover plan: C/E2; from answers, not exercised): The ERP failover plan is documented but not tested. Substitution rights are proven, but no working fallback for order processing is proven within the window.
- **24–72 hours | Moves 5 and 1 | Comms approval delay** (Move 5 Q3, customer obligations and support plan: C/E2; from answers, not exercised): The support plan lacks ready scripts and a comms workflow. Messaging to about 300 business customers on delayed orders may wait on ad hoc approvals.

## 6) Top Blockers and Fixes

1. **Blocker:** The Move 1 rollback and continuity checks are untested.
   - **Evidence gap:** E2 only; no tested criteria.
   - **Minimal fix (2 weeks):** Add explicit pass/fail criteria to the checklist for holding or releasing hazardous goods without ERP data.
   - **Proper fix (6–12 weeks):** Exercise the checklist in a tabletop, then log the outcome and open a CAPA.
   - **Owner role:** Operations Director

2. **Blocker:** Move 1 comms templates are not pre-approved.
   - **Evidence gap:** C/E2; no approval workflow.
   - **Minimal fix (2 weeks):** Pre-approve one internal holding statement and one customer holding statement for an ERP outage.
   - **Proper fix (6–12 weeks):** Build an approval workflow with named owners and backups, and rehearse it.
   - **Owner role:** Head of Communications, with the Operations Director

3. **Blocker:** Stop authority is documented but has never been exercised.
   - **Evidence gap:** No delegated exercise is logged.
   - **Minimal fix (2 weeks):** Confirm deputies for the Operations Director and keep a printed authority matrix at each warehouse.
   - **Proper fix (6–12 weeks):** Exercise a delegated stop in a drill and record it in a decision log.
   - **Owner role:** Operations Director

4. **Blocker:** The 72-hour treasury reroute is unproven.
   - **Evidence gap:** "Likely," at E2.
   - **Minimal fix (2 weeks):** Walk through the steps to run critical payments without ERP-generated files.
   - **Proper fix (6–12 weeks):** Run a low-value test through the pre-cleared alternate rail, logged with a CAPA.
   - **Owner role:** Treasurer, with CFO approval

5. **Blocker:** Freeze and hold steps and counterparty triggers have never been exercised together.
   - **Evidence gap:** Each is at E2; no joint exercise.
   - **Minimal fix (2 weeks):** Map which triggers lead to which hold actions in a one-page decision tree.
   - **Proper fix (6–12 weeks):** Include both in the treasury tabletop, with the escalation steps logged.
   - **Owner role:** CFO

6. **Blocker:** The shutdown and segmentation runbook is untested and held only in the IT service management tool.
   - **Evidence gap:** E2; may be inaccessible in an outage.
   - **Minimal fix (2 weeks):** Keep an offline or printed copy of the runbook with the CIO and the on-call lead.
   - **Proper fix (6–12 weeks):** Exercise segmentation and shutdown in a simulation, logged with a CAPA.
   - **Owner role:** CIO

7. **Blocker:** Privileged and emergency access logging is untested.
   - **Evidence gap:** C/E2; no audit trail exercise.
   - **Minimal fix (2 weeks):** Confirm that the emergency access procedure and log location survive an ERP compromise.
   - **Proper fix (6–12 weeks):** Exercise break-glass access and review the resulting audit trail.
   - **Owner role:** CIO, with the IT Security Lead

8. **Blocker:** The ERP failover and portability plan is untested.
   - **Evidence gap:** C/E2; only substitution rights are at E3.
   - **Minimal fix (2 weeks):** Define a manual order-to-dispatch fallback (forms, stock lists, priorities) for five days.
   - **Proper fix (6–12 weeks):** Test the failover or manual fallback at one warehouse, logged with a CAPA.
   - **Owner role:** COO, with the CIO

9. **Blocker:** Alternates are qualified but not proven viable within 72 hours.
   - **Evidence gap:** Q2 is C/E2.
   - **Minimal fix (2 weeks):** Confirm lead times and contact paths for the alternate bulk supplier and logistics provider.
   - **Proper fix (6–12 weeks):** Run a cutover simulation that shows 72-hour viability, extending the April 2026 drill.
   - **Owner role:** COO, with the Head of Procurement

10. **Blocker:** The Move 5 customer support and data/people plans are unrehearsed.
    - **Evidence gap:** C/E2; no scripts or workflow.
    - **Minimal fix (2 weeks):** Draft customer service scripts for order delays and a priority-customer list kept outside the ERP.
    - **Proper fix (6–12 weeks):** Rehearse the scripts and workflow, and assign responsibility for the data and people steps.
    - **Owner role:** Head of Customer Service, with CEO sponsorship

## 7) 30/60/90-Day Plan

**Workstream 1: Outage containment and safe pause (Moves 1 and 3)**
- **Outcome:** The pause and shutdown runbooks are moved from E2 to E3 with offline access.
- **Tasks:**
  - Days 0–30: Create offline copies of the stop authority matrix, safety checklist and shutdown runbook.
  - Days 0–30: Add pass/fail criteria for hazardous goods hold and release.
  - Days 30–60: Pre-approve holding statements.
  - Days 30–60: Run the 45-minute drill (Section 8).
  - Days 60–90: Close the CAPAs from the drill.
- **Gates:**
  - Offline artifacts are confirmed at all three warehouses.
  - The drill log and at least one CAPA are recorded in the risk system.
- **Owner roles:** Operations Director and CIO
- **Stop rule:** Pause the workstream and escalate to the COO if the drill shows that the stop authority cannot be exercised without ERP access.

**Workstream 2: Cash continuity without ERP (Move 2)**
- **Outcome:** The 72-hour reroute is proven by exercise.
- **Tasks:**
  - Days 0–30: Map the critical payments (suppliers, payroll, logistics) and the manual payment file steps.
  - Days 0–30: Build the trigger-to-hold decision tree.
  - Days 30–60: Run a low-value test on the alternate rail.
  - Days 60–90: Hold a treasury tabletop with the backup approver.
- **Gates:**
  - The test reroute is logged with a month/year and a CAPA.
  - The Treasurer completes the steps as backup approver.
- **Owner roles:** CFO and Treasurer
- **Stop rule:** Halt the live test if any bank requires steps that are not pre-cleared, and refer the matter to the CFO and counsel.

**Workstream 3: ERP failover and supplier substitution (Moves 4 and 5)**
- **Outcome:** A tested manual or failover path for order processing, and alternates shown to be viable within 72 hours.
- **Tasks:**
  - Days 0–30: Define the manual order-to-dispatch fallback.
  - Days 0–30: Confirm alternate supplier and logistics lead times.
  - Days 30–60: Pilot the fallback at one warehouse.
  - Days 60–90: Run a cutover simulation and rehearse customer scripts.
- **Gates:**
  - The pilot is completed with a log and a CAPA.
  - Customer scripts are approved through a defined workflow.
- **Owner roles:** COO, CIO and Head of Customer Service
- **Stop rule:** Stop the pilot if manual processing compromises dangerous goods documentation, and revert to a safe pause under Move 1.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk Lead)
- Operations Director (stop authority)
- CIO (containment)
- CFO and Treasurer (cash)
- COO (substitution)
- Head of Communications
- Head of Customer Service
- Scribe

**Agenda**
- **0–5 min:** Inject. The ERP has been unavailable since 06:00 because of ransomware, and the order portal is unable to sync.
- **5–15 min (0–6 hour window):** Decide what is paused, who authorizes it, which safety checks must pass and the holding statement.
- **15–25 min (6–24 hour window):** Choose the switch paths: manual order fallback, payment reroute, alternate supplier or logistics, and data containment posture.
- **25–35 min (24–72 hour window):** Decide what is executed, what is monitored and how customers are updated.
- **35–45 min:** Hot debrief and CAPA capture.

**Decisions to log**
- The stop decision and the approver
- The containment and shutdown decision
- The payment reroute decision
- The substitution cutover decision
- The customer comms release decision

Log each with a timestamp and role.

**Evidence to capture**
- Time to reach each approver
- Whether offline artifacts were accessible
- Gaps in checklists
- Comms approval time
- Payment steps that could not be completed without the ERP

**CAPA prompt**
- "Which decision took longest or could not be made, why, and what single change (artifact, authority, alternate or gate) would remove that stall within 30 days?"
- Assign an owner role and a due date for each CAPA.

## 9) Escalations

**ESCALATE.** The criminal trigger is identified from the scenario. Conditional items to confirm are listed below.

- **Criminal (triggered):** A ransomware attack is a criminal act.
  - Recommended path: incident lead (CIO) to CEO, then the board risk committee, with external counsel engaged early.
  - Questions for counsel:
    - Whether, when and how to engage law enforcement
    - How to preserve evidence
- **Sanctions (conditional, question for counsel):** If any ransom payment or contact with the attackers is contemplated, refer it to counsel before any action. Counsel would need to assess possible sanctions exposure. No determination is made here.
- **Physical safety (conditional):** If the ERP outage removes access to hazardous materials inventory, safety data sheets or dangerous goods shipping records, escalate to the Operations Director and the safety lead immediately.
- **Regulator inquiry (not indicated):** Possible notification obligations depend on the jurisdiction, which is Unknown. This is a question for counsel.
- **Financial and people thresholds:** Not met. The user estimates about USD 2m and no more than 2,000 people, below USD 10m and 100,000.

## 10) Known Limits + Version

- **Self-report bias:** All answers are self-assessed. The uniform C/E2 pattern across 19 of 20 answers should be spot-checked by an independent reviewer.
- **No document validation:** No artifacts were reviewed. The "Documented" and "Tested" labels reflect claims only.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown. Notification, data transfer and contractual questions require counsel.
- **Scenario simplification:** A five-day single-system outage understates the risk if ransomware spreads to the quality, treasury, ITSM or procurement systems where the artifacts are held.
- **E3 recency assumption:** The assessment date was not supplied. Move 4's April 2026 drill is treated as within 12 months, and it would no longer count after April 2027.
- **Limited coverage:** Fast Baseline covers Q1–Q4 only. Q5–Q7 and the mini tabletop, which make up Deepening, were not run, so the breakpoints are from answers and have not been exercised.
- **Planning signals only:** The scores are planning signals, not certification or assurance of any kind.
- **No screening:** No sanctions or export-control screening was performed.
- **Impact estimates are unverified:** The USD 2m and 2,000-person figures are user estimates.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Medium

## Score

**Verdict: PASS.** The packet was produced in Turn 1 and the Move 4 values were not changed afterward. The scorecard gives Move 4 score 3 and confidence Medium. Recomputing from the reference pack rules gives the same values. The mean pattern score is 3.25, which rounds to 3. No evidence-average cap or prerequisite cap applies. Confidence is Medium because there is not a majority at E3, there is a majority at E2 or E3, there is at least one E3, and the consistency check passes. Turn 2 repeats 3 and Medium unchanged, and no fail indicator appears.

---

Final Liability rests with the Human.
