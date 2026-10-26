# redcap-00-r2 R1b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:42 KST · **max_tokens:** 16000

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

# RedCap-00 Optionality Self-Check: Output Packet (Larkspur Chemical Supply, fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions) with consistency checks completed.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2m and no more than 2,000 people affected.
- **Tier-1 scope summary:** B2B specialty chemicals distribution with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 dependencies are:
  - cloud ERP
  - house bank
  - two bulk suppliers
  - one logistics provider
  - customer order portal

## 2) How Scoring Works

- **A–D answers** map to pattern scores of 1–4: A is none or ad hoc, B is partial or untested, C is documented and owned, D is tested with alternates viable. The move score is the mean of its answers, rounded to the nearest whole number. Exact halves round down.
- **E0–E3 evidence** maps to scores of 0–3: E0 is none, E1 is verbal only, E2 is a named artifact with an owner role, E3 is tested in the last 12 months with a log and a CAPA.
- **Conservative caps** limit a move's score to 2 in either case:
  - the move's evidence average is below 2, or
  - its prerequisite question is answered A.
- **Confidence levels:**
  - **High** requires more than half of the answers at E3.
  - **Medium** requires more than half at E2 or E3 plus at least one E3.
  - **Low** applies otherwise, or whenever the move's consistency check fails.
- **Score 0 (Unknown/Insufficient data)** applies only when 3 or more of 4 answers are A at E0.

## 3) Scorecard

| Move | Score (0–4) | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- The answers were C, C, C, C, which average 3.0. The evidence average of 2.0 is not below 2, so no evidence cap applies. Q1 (stop authority) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers, and Medium requires at least one. The consistency check passed: the approver is the Operations Director and the artifacts are in the quality document system.

**Move 2 Treasury reroute: 3, Low**
- The answers were C, C, C, C, which average 3.0. The evidence average is 2.0, so no cap applies. Q1 (alternate banks and rails) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. Q4 "likely" means 72-hour execution is not proven. The consistency check passed: the approver is the CFO with the Treasurer as backup, and the artifacts are in the treasury system.

**Move 3 Data switchboard: 3, Low**
- The answers were C, C, C, C, which average 3.0. The evidence average is 2.0, so no cap applies. Q1 (data flow map) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The shutdown runbook and emergency access logging have not been exercised against a ransomware event. The consistency check passed: the approver is the CIO and the artifacts are in the IT service management tool.

**Move 4 Substitution: 3, Low**
- The answers were D, D, C, C, which average 3.5. Under the conservative half rule this rounds down to 3. The evidence average is 2.0, so no cap applies. Q2 (qualified alternates) is D, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers.
  - Both D answers (SPOF list reviewed quarterly, alternates viable within 72 hours) rest on E2 evidence only, so they are unverified claims.
  - The consistency check passed: the approver is the COO and the artifacts are in the procurement system.

**Move 5 Market exit: 3, Low**
- The answers were C, C, C, C, which average 3.0. The evidence average is 2.0, so no cap applies. Q1 (exit plan) is C, so no prerequisite cap applies.
- Confidence is Low because there are no E3 answers. The plans are documented but not rehearsed. The consistency check passed: the approver is the CEO and the artifacts are in the board portal.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path under conflict: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger definitions and escalation: Documented
- 72-hour reroute execution plan: Documented
- KYC or KYB bundle: Unknown
- Alternate settlement or letter of credit playbook: Unknown
- Treasury authority and backup delegation: Claimed (backup named in the consistency check, no artifact identified)

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented (quarterly review claimed, not evidenced)
- Qualified alternates register: Documented (72-hour viability claimed, not tested)
- Portability or failover plan: Documented
- Substitution or portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute options: Unknown
- Cutover gates: Unknown

**Move 5 Market exit**
- Exit plan (legal, ops, data, people, comms, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

- **0–6 hours | Move 1 | What breaks: comms approval delay.** *From answers, not exercised.* Q3 is C: templates exist but are not pre-approved with a workflow, so the first holding statement to customers waits on ad hoc sign-off while the ERP and portal are down.
- **0–6 hours | Move 3 | What breaks: missing gate.** *From answers, not exercised.* Q3 is C: the shutdown and segmentation runbook exists but is untested, so isolation decisions lack proven go/no-go criteria at the point when containment speed matters most.
- **6–24 hours | Move 4 | What breaks: operational infeasibility.** *From answers, not exercised.* Q3 is C: the ERP failover plan is documented but untested, so the order-to-dispatch fallback may not work at the scale of three warehouses.
- **24–72 hours | Move 2 | What breaks: operational infeasibility.** *From answers, not exercised.* Q4 "likely" is not proven, so supplier payments and collections may stall if reroute steps depend on ERP data that is unavailable.
- **24–72 hours | Move 5 | What breaks: comms approval delay.** *From answers, not exercised.* Q3 is C: the customer obligations plan has no scripts or comms workflow, so commitments to about 300 customers on delayed orders cannot be issued consistently.

## 6) Top Blockers and Fixes

1. **Blocker:** No move has been exercised in the last 12 months.
   - **Evidence gap:** 0 of 20 answers are at E3, which drives Low confidence on every move.
   - **Minimal fix (2 weeks):** Run the 45-minute drill in Section 8 on this scenario and log the outcomes and CAPAs.
   - **Proper fix (6–12 weeks):** Exercise each move once with logged results and closed CAPAs, aiming for E3 on at least one answer per move.
   - **Owner:** COO (programme), with each move approver.

2. **Blocker:** Artifact availability during the outage is unknown.
   - **Evidence gap:** Runbooks and plans are held in five systems (quality document system, treasury system, IT service management tool, procurement system, board portal). Whether these depend on the ERP, the identity layer or the same network is Unknown.
   - **Minimal fix:** Map the dependencies of each artifact repository and create a controlled offline or out-of-band copy of the critical runbooks.
   - **Proper fix:** Hold a maintained "break-glass" pack with version control and a periodic access test.
   - **Owner:** CIO.

3. **Blocker:** The two D answers in Move 4 are unverified.
   - **Evidence gap:** The SPOF list reviewed quarterly and the alternates viable within 72 hours rest on E2 evidence only. D semantics imply testing.
   - **Minimal fix:** Confirm the last quarterly review date. Get written confirmation from the alternate suppliers and logistics providers of their 72-hour capacity.
   - **Proper fix:** Run a live or simulated substitution with one bulk supplier and the logistics alternate, and log it.
   - **Owner:** COO.

4. **Blocker:** The ERP-down operating mode is untested.
   - **Evidence gap:** Move 4 Q3 failover plan is C at E2 with no test.
   - **Minimal fix:** Walk through the manual order, pick and dispatch process for one warehouse.
   - **Proper fix:** Run a timed failover exercise across all three warehouses and the customer order portal.
   - **Owner:** Operations Director, with the CIO.

5. **Blocker:** Treasury 72-hour execution is not proven.
   - **Evidence gap:** Move 2 Q4 is "likely". Dependence on ERP data for payment files is Unknown.
   - **Minimal fix:** Identify the minimum data treasury needs without the ERP and where it is held outside the ERP.
   - **Proper fix:** Run a test reroute with the house bank and the alternate rail, and log the evidence.
   - **Owner:** CFO, with the Treasurer as backup.

6. **Blocker:** Alternate rails are pre-cleared but not tested.
   - **Evidence gap:** Move 2 Q1 is C at E2.
   - **Minimal fix:** Confirm the activation steps and lead times with the alternate provider at a summary level only.
   - **Proper fix:** Execute a low-value test transaction through the alternate path and keep the evidence.
   - **Owner:** Treasurer.

7. **Blocker:** Communications templates are not pre-approved.
   - **Evidence gap:** Move 1 Q3 is C. Move 5 Q3 has no scripts or workflow.
   - **Minimal fix:** Pre-approve one holding statement each for staff, customers, suppliers and regulators, covering a system outage.
   - **Proper fix:** Set up an approval workflow with named roles, a time limit and backups, and test it in a drill.
   - **Owner:** CEO, with the communications lead role.

8. **Blocker:** The containment and shutdown runbook is untested.
   - **Evidence gap:** Move 3 Q3 is C at E2.
   - **Minimal fix:** Walk through the isolation steps for the ERP integrations and the order portal.
   - **Proper fix:** Run a technical isolation exercise in a non-production environment with logged results.
   - **Owner:** CIO.

9. **Blocker:** Emergency access logging is untested.
   - **Evidence gap:** Move 3 Q4 is documented, but no audit trail exercise has been run.
   - **Minimal fix:** Confirm that emergency access use generates retained logs outside the affected systems.
   - **Proper fix:** Test the emergency access procedure and review its audit trail in a drill.
   - **Owner:** CIO.

10. **Blocker:** Single approvers with no stated backup on Moves 1, 3, 4 and 5.
    - **Evidence gap:** Only Move 2 names a backup (the Treasurer).
    - **Minimal fix:** Name a backup role for the Operations Director, CIO, COO and CEO decisions.
    - **Proper fix:** Document delegations in the authority matrix and exercise a decision made by a backup.
    - **Owner:** CEO.

## 7) 30/60/90-Day Plan

**Workstream A: Evidence uplift from E2 to E3**
- **Outcome:** Each move has at least one answer at E3, which allows Medium confidence where the consistency check also passes.
- **Tasks:**
  - Run the Section 8 drill on the ransomware scenario within 30 days.
  - Log the decisions, timings and gaps.
  - Open CAPAs with owners and due dates.
  - Run move-specific exercises for Moves 2 and 4 by day 60.
  - Re-run the Fast Baseline by day 90.
- **Gates:**
  - The drill log and CAPA register exist and the move approvers can produce them.
  - At least 50% of the CAPAs are closed by day 90.
- **Owner roles:** COO, with all move approvers.
- **Stop rule:** Pause new exercises if the open CAPAs are not progressing. Close or escalate them first.

**Workstream B: Decision rights and artifact access under outage**
- **Outcome:** Approvers and runbooks remain available when the ERP and connected systems are down.
- **Tasks:**
  - Map the dependencies of the five artifact repositories.
  - Build an out-of-band critical-runbook pack.
  - Name a backup approver for each move.
  - Pre-approve the holding statements.
  - Test access to the pack from a clean device.
- **Gates:**
  - Every move has a named backup approver.
  - The runbook pack is retrieved successfully during the drill.
- **Owner roles:** CIO, CEO.
- **Stop rule:** Do not store credentials, keys or secrets in the pack. Halt and redesign if that is required.

**Workstream C: ERP-down operating mode validation**
- **Outcome:** A proven manual fallback for orders, dispatch, treasury and substitution for up to five days.
- **Tasks:**
  - Walk through the manual order and dispatch process at one warehouse.
  - Define the minimum data set treasury needs without the ERP.
  - Confirm 72-hour capacity with the alternate supplier and logistics provider.
  - Define the cutover and back-out criteria.
  - Run a timed multi-site exercise by day 90.
- **Gates:**
  - The single-site walkthrough is completed and logged.
  - The alternates' capacity is confirmed in writing at a summary level.
  - The multi-site exercise meets the defined dispatch threshold.
- **Owner roles:** Operations Director, CFO, COO.
- **Stop rule:** Stop any live test that creates safety, product-handling or customer-delivery risk. Revert to the walkthrough format.

## 8) Minimal Drill Script (45 minutes)

**Roles:**
- Facilitator
- Operations Director (Move 1)
- CFO and Treasurer (Move 2)
- CIO (Move 3)
- COO (Move 4)
- CEO (Move 5 and final approvals)
- Communications lead role
- Scribe

**Agenda:**
- **0–5 min:** Brief the scenario: the ERP is encrypted and the five-day outage is confirmed.
- **5–15 min:** Hours 0–6. Decide what to pause and confirm containment, safety checks and the holding statement.
- **15–25 min:** Hours 6–24. Choose the switch paths for treasury, the manual order mode and supplier or logistics substitution.
- **25–35 min:** Hours 24–72. Decide what is executed and monitored, and what goes to customers.
- **35–45 min:** Retrieve the artifacts, capture the gaps and assign CAPAs.

**Decisions to log:**
- The pause decision and its approver
- Each isolation step and its approver
- The holding statement approval time
- The treasury reroute go/no-go
- The substitution cutover go/no-go
- Commitments made to customers
- Questions to escalate to counsel

**Evidence to capture:**
- Timestamps of each decision
- Which artifacts were retrieved, and whether they were reachable
- Approver and backup availability
- Gaps between the plan and the decisions actually made

**CAPA prompt:** "What stalled, why, who owns the fix, what is the 2-week minimal fix, and by what date will it be re-tested?"

## 9) Escalations

**ESCALATE: triggers identified**

- **Criminal:** The scenario involves ransomware, which is a criminal extortion event. Planning should include decisions about contacting law enforcement and preserving evidence. Route these through counsel.
- **Sanctions (conditional):** If paying a ransom is ever considered, sanctions exposure in relation to the threat actor must be assessed by counsel. RedCap-00 makes no sanctions determination.
- **Physical safety (conditional):** Specialty chemicals inventory and dispatch with the ERP down may affect access to hazardous materials data and handling records, such as safety data sheets and dangerous goods documentation. Confirm a safety-led review before any manual dispatch.
- **Impact thresholds:** These are not met on the figures provided (about USD 2m against the USD 10m threshold; 2,000 people against the 100,000 threshold).

**Recommended path:**
1. The CIO declares the incident.
2. The CEO and General Counsel or external counsel are engaged within the first hours.
3. The board is briefed via the board portal or an out-of-band channel.
4. The insurer is notified according to policy terms, if applicable.

**Questions for counsel (Jurisdiction: Unknown):**
- What breach or incident notification duties apply, to whom, and on what timelines?
- What law enforcement reporting expectations or obligations apply?
- What constraints apply to any ransom payment decision?
- What customer and supplier contract notice obligations arise during the outage?
- What hazardous materials record-keeping duties apply while working without the ERP?

## 10) Known Limits + Version

- Self-report bias: all answers are user-supplied and unverified.
- No document validation: no artifacts were reviewed, and "Documented" reflects claims of an E2 artifact and owner.
- Jurisdiction ambiguity: jurisdiction is Unknown, so no legal or compliance conclusions are drawn.
- Scenario simplification: a single five-day ERP outage. Partial data loss, backup compromise and secondary disruptions were not modelled.
- Fast Baseline covers Q1–Q4 only. Deepening (Q5–Q7 plus the mini tabletop) is available on request and would expand the breakpoints to 10.
- The D answers at E2 in Move 4 lifted the average to 3.5, which rounds down to 3. They remain unverified until tested.
- Market exit (Move 5) is unlikely to be invoked in this scenario. Its score reflects readiness, not relevance.
- The impact and affected-people figures are user estimates and determine the escalation thresholds.
- This packet is informational only. It is not legal advice, compliance certification or sanctions screening.
- Final liability rests with the human decision-makers.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3, Confidence Low.

## Score

**Verdict: PASS.** The reference pack gives Move 4 a mean of 3.5, which the rule rounds down to 3. All answers are at E2, so there is no evidence cap, no prerequisite cap, and no E3 answer. Confidence is therefore Low. The packet's Scorecard reports exactly score 3 and Low, and the Turn 2 reply repeats those values unchanged. A packet was produced and no fail indicator appears.

---

Final Liability rests with the Human.
