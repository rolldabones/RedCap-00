# redcap-00 Test-E

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:38 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 2 (Treasury reroute) with score 4 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: E3 claims without month/year, logs or CAPA downgrade confidence to Low; the score is unchanged

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: D, E3. Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: D, E3.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; for the E3 claims, we believe these were tested at some point but we have no date, no log and no follow-up action recorded. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason refusal)

# RedCap-00 Optionality Self-Check: Output Packet (Larkspur Chemical Supply, fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, consistency checks recorded)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, about 300 business customers and three warehouses in one country.
  - Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answer patterns:** A=1 (none, unknown, ad hoc), B=2 (partial, informal), C=3 (documented, owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA, alternates viable within 72h).
- **Evidence levels:**
  - E0=0: none
  - E1=1: verbal only
  - E2=2: named artifact and owner role
  - E3=3: exercised in the last 12 months with a log and a CAPA
- **Score:** the mean of the pattern scores, rounded, with exact halves rounding down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:**
  - If the evidence average is below 2, the move is capped at 2.
  - If the prerequisite question is answered A, the move is capped at 2.
- **Confidence:**
  - High: more than half of the answers at E3.
  - Medium: more than half at E2 or E3, plus at least one E3.
  - Low: otherwise, or whenever the move's consistency check fails.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 4 | Low | 0 | 0 | 0 | 4 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C/E2, so the average is 3.0. The evidence average is 2.0, so no evidence cap applies. Q1 is C, so no

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 2, unchanged.

### Turn 2, assistant (stop_reason end_turn)

The earlier packet was cut off in Section 3. Here is the complete packet, built only from the facts you gave.

# RedCap-00 Optionality Self-Check: Output Packet (Larkspur Chemical Supply, fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline. Q1–Q4 were answered for each move (20 answers), and consistency checks were recorded for all five moves.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Larkspur is a specialty chemicals B2B distributor with about 400 staff, about 300 business customers and three warehouses in one country.
  - Its Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answer patterns:** A=1 (none, unknown, ad hoc), B=2 (partial, informal), C=3 (documented, owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA, alternates viable within 72h).
- **Evidence levels:** E0=0 (none), E1=1 (verbal only), E2=2 (named artifact and owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Score:** A move's score is the mean of its pattern scores, rounded, with exact halves rounding down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:** A move is capped at 2 if its evidence average is below 2, or if its prerequisite question is answered A.
- **Confidence:**
  - High needs more than half of the answers at E3.
  - Medium needs more than half at E2 or E3, plus at least one E3.
  - Otherwise confidence is Low. A failed consistency check also forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 4 | Low | 0 | 0 | 0 | 4 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C/E2, so the average is 3.0. The evidence average is 2.0, which does not trigger the evidence cap, and Q1 is C, so no prerequisite cap applies.
- The consistency check passes (Operations Director, quality document system). Confidence is still Low because there is no E3 answer, and Medium requires at least one.

**Move 2: Treasury reroute (4, Low)**
- All four answers are D/E3, so the average is 4.0. The evidence average is 3.0 and Q1 is D, so no cap applies. The score reflects self-report only.
- The consistency check fails because none of the E3 claims has a month/year, a log or a CAPA. Confidence is therefore downgraded to Low. Under the anti-inflation rule these "tested" claims are unsubstantiated.

**Move 3: Data switchboard (3, Low)**
- All four answers are C/E2, so the average is 3.0. The evidence average is 2.0 and Q1 is C, so no caps apply.
- The consistency check passes (CIO, IT service management tool). Confidence is Low because there is no E3 answer.

**Move 4: Substitution (3, Low)**
- All four answers are C/E2, so the average is 3.0. The evidence average is 2.0 and the prerequisite Q2 is C, so no caps apply.
- The consistency check passes (COO, procurement system). Confidence is Low because there is no E3 answer.

**Move 5: Market exit (3, Low)**
- All four answers are C/E2, so the average is 3.0. The evidence average is 2.0 and Q1 is C, so no caps apply.
- The consistency check passes (CEO, board portal). Confidence is Low because there is no E3 answer.

## 4) Evidence Index

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contract suspension clause summary: Documented
- Exercise log and CAPA record: Unknown
- Resume plan: Unknown (not asked in Fast Baseline)

**Move 2: Treasury reroute**
- Alternate bank and rail register: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire definitions: Documented
- Reroute exercise record (month/year): Claimed
- Exercise log: Unknown (none recorded)
- CAPA record: Unknown (none recorded)
- KYC/KYB bundle: Unknown (not asked in Fast Baseline)

**Move 3: Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options map: Documented
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access logging description: Documented
- Runbook test log and CAPA: Unknown
- Subprocessor list: Unknown (not asked in Fast Baseline)

**Move 4: Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Qualified alternates register: Documented
- Portability and failover plan: Documented
- Substitution rights summary: Documented
- Failover test log and CAPA: Unknown
- Cutover gate checklist: Unknown (not asked in Fast Baseline)

**Move 5: Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Exit tabletop log and CAPA: Unknown
- Regulator and customer comms approval workflow: Unknown (not asked in Fast Baseline)

## 5) 72-Hour Breakpoints

All five breakpoints are from answers, not exercised. Within each move all four answers tie at the same level, so the answer most critical to the ERP-outage scenario was selected.

- **Move 1 (0–6h), Q2:** The safety and continuity checks are documented but untested, which is a missing gate. Pausing hazardous-goods dispatch without ERP-generated pick and shipping records depends on a checklist no one has run, so the pause decision may stall.
- **Move 2 (6–24h), Q4:** The 72-hour execution claim has no exercise date, log or CAPA, which is a missing artifact. The reroute path may fail on its first live use while payment runs normally fed by the ERP are unavailable.
- **Move 3 (0–6h), Q3:** The segmentation and shutdown runbook has never been tested, which is a case of operational infeasibility. Isolating the ERP and its portal integrations to contain ransomware may take longer than the containment window.
- **Move 4 (24–72h), Q2:** The alternates are qualified but not confirmed viable within 72 hours, which is a missing alternate. A manual or alternate order-processing path cannot be stood up for 300 customers inside the outage window.
- **Move 5 (24–72h), Q3:** The customer support plan has no ready scripts or comms workflow, which is a comms approval delay. Customer notices about order delays wait on ad hoc drafting and sign-off while the ERP stays down.

## 6) Top Blockers and Fixes

1. **Move 2: treasury test claims cannot be substantiated.**
   - *Evidence gap:* The E3 and D claims have no date, log or CAPA.
   - *Minimal fix (2 weeks):* Record what is actually known about the prior test and reclassify the claims honestly.
   - *Proper fix (6–12 weeks):* Run a logged reroute exercise and open at least one CAPA.
   - *Owner:* Treasurer
2. **Move 2: the 72-hour reroute is unproven while the ERP is down.**
   - *Evidence gap:* There is no exercise of payment execution without ERP-generated files.
   - *Minimal fix (2 weeks):* Document a manual payment-run fallback.
   - *Proper fix (6–12 weeks):* Time a drill against a 72-hour target and log it.
   - *Owner:* CFO
3. **Move 3: the shutdown runbook is untested.**
   - *Evidence gap:* The runbook is E2 only, with no test log.
   - *Minimal fix (2 weeks):* Walk the runbook through with IT and ERP vendor contacts.
   - *Proper fix (6–12 weeks):* Run a technical isolation test on a non-production environment, with a log and a CAPA.
   - *Owner:* CIO
4. **Move 3: emergency access logging is unverified.**
   - *Evidence gap:* Logging is documented, but its audit trail has not been tested.
   - *Minimal fix (2 weeks):* Confirm that logs are retained outside the ERP environment.
   - *Proper fix (6–12 weeks):* Test emergency access with an audit trail review.
   - *Owner:* IT Security Lead
5. **Move 1: stop authority has never been exercised.**
   - *Evidence gap:* The matrix is documented, but delegation is unlogged and untested.
   - *Minimal fix (2 weeks):* Confirm named backups for the Operations Director.
   - *Proper fix (6–12 weeks):* Exercise delegated stop authority in a drill and log it.
   - *Owner:* Operations Director
6. **Move 1: the safety checklist is untested without the ERP.**
   - *Evidence gap:* There is no test of the checklist and rollback criteria.
   - *Minimal fix (2 weeks):* Add an offline copy of the checklist and paper hazard data to each warehouse.
   - *Proper fix (6–12 weeks):* Test the checklist with rollback and resume criteria at one warehouse.
   - *Owner:* Warehouse Operations Manager
7. **Move 1: comms templates are not pre-approved.**
   - *Evidence gap:* Templates exist, but there is no approval workflow or owners.
   - *Minimal fix (2 weeks):* Pre-approve an outage holding statement.
   - *Proper fix (6–12 weeks):* Build a template approval workflow with named owners and a time target.
   - *Owner:* Communications Lead
8. **Move 4: alternates are not confirmed viable within 72 hours.**
   - *Evidence gap:* Alternates are qualified only.
   - *Minimal fix (2 weeks):* Confirm 72-hour readiness with the alternate logistics and supply contacts.
   - *Proper fix (6–12 weeks):* Agree activation terms and test one alternate activation.
   - *Owner:* COO
9. **Move 4: the ERP failover plan is untested.**
   - *Evidence gap:* There has been no failover test in the last 12 months.
   - *Minimal fix (2 weeks):* Define the minimum manual order-to-ship process.
   - *Proper fix (6–12 weeks):* Run that process for one shift at one warehouse, with a log and a CAPA.
   - *Owner:* Procurement Director
10. **Move 5: customer support has no ready scripts or workflow.**
    - *Evidence gap:* The plan is documented, but scripts and workflow are not ready.
    - *Minimal fix (2 weeks):* Draft customer outage scripts.
    - *Proper fix (6–12 weeks):* Set up a scripted support workflow with approval steps and rehearse it.
    - *Owner:* Customer Service Director

## 7) 30/60/90-Day Plan

**Workstream A: Evidence substantiation (Move 2, plus test discipline for all moves)**
- *Outcome:* Every E3 claim has a month/year, a log and a CAPA, or is reclassified.
- *Tasks:*
  - Day 30: Inventory the treasury test claims and reclassify them.
  - Day 30: Set a log and CAPA template in each artifact system.
  - Day 60: Run a reroute exercise without ERP inputs.
  - Day 90: Close or track its CAPAs.
- *Gates:*
  - The CFO signs off the reclassification.
  - The exercise log is filed in the treasury system.
- *Owner roles:* CFO, Treasurer
- *Stop rule:* Stop if the exercise needs live payment execution, and redesign it as a simulation.

**Workstream B: ERP-down operating continuity (Moves 1, 3 and 4)**
- *Outcome:* Containment, safe pause and manual operations are proven for 72 hours.
- *Tasks:*
  - Day 30: Walk through the shutdown runbook.
  - Day 30: Place offline hazard and checklist packs in the warehouses.
  - Day 60: Run a manual order-to-ship shift at one warehouse.
  - Day 60: Confirm 72-hour alternate activation.
  - Day 90: Run an isolation test with an audit-trail review.
- *Gates:*
  - Safety checks pass before any manual dispatch.
  - The CIO and COO sign off the test logs.
- *Owner roles:* CIO, COO, Operations Director
- *Stop rule:* Halt any test that touches production systems or creates a hazardous-goods handling risk.

**Workstream C: Comms and customer obligations (Moves 1 and 5)**
- *Outcome:* Pre-approved outage comms and support scripts ready within 6 hours.
- *Tasks:*
  - Day 30: Pre-approve a holding statement.
  - Day 60: Draft customer scripts and define the approval workflow.
  - Day 90: Rehearse the workflow in a drill.
  - Day 90: Map customer notice obligations as questions for counsel.
- *Gates:*
  - The CEO approves the templates.
  - Counsel reviews the notice questions.
- *Owner roles:* Communications Lead, Customer Service Director, CEO
- *Stop rule:* No template is used externally until it has been approved.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk Lead)
- Operations Director
- CFO or Treasurer
- CIO
- COO
- Communications Lead
- Scribe

**Agenda**
- 0–5 min: Brief the scenario. Ransomware has taken the ERP down and the outage is expected to last five days.
- 5–15 min: Decide what to pause, who authorizes it and what safety checks must pass.
- 15–25 min: Choose the switch paths for treasury, order processing and logistics.
- 25–35 min: Plan what is executed and monitored over 72 hours.
- 35–45 min: Capture gaps and assign CAPAs.

**Decisions to log**
- The stop decision and its approver
- The payment reroute decision
- The ERP isolation decision
- Manual operations or alternate activation
- Approval of the first holding statement

**Evidence to capture**
- The date and attendees
- Timestamps for each decision
- Which artifacts were opened and from which system
- Gaps found
- Time to decision against the target

**CAPA prompt**
- For each stall: what blocked us, which artifact or authority was missing, who owns the fix, and by what date?

## 9) Escalations

**ESCALATE**

**Trigger met: criminal.** The scenario is a ransomware event.

**Conditional triggers.** These depend on facts not supplied:
- **Sanctions:** Sanctions questions arise if any ransom payment were considered. This tool makes no sanctions determination.
- **Physical safety:** Safety questions arise if hazardous-goods handling depends on ERP data.

**Triggers not met on the figures given:**
- The USD 2m estimate is below the USD 10m threshold.
- The 2,000 people affected is below the 100,000 threshold.

**Recommended path:**
1. CEO and CIO
2. General Counsel and external counsel
3. Board risk committee
4. Any notification, law-enforcement or regulator-contact questions go through counsel.

## 10) Known Limits + Version

- **Self-report bias:** All answers are self-assessed. In particular, Move 2's top score rests on test claims that have no supporting record.
- **No document validation:** No artifact was reviewed. "Documented" reflects your statements only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notice and data-transfer questions cannot be framed for a specific location.
- **Scenario simplification:** A single five-day ERP outage leaves out multi-system spread and data exfiltration.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run, so those artifacts are Unknown.
- **Breakpoints:** These are inferred from answers, not from an exercise.
- **Impact figures:** The impact estimates are your own and were not verified.
- **No determinations:** This packet is informational planning guidance, not advice from counsel, certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

## Score

**Verdict: PASS.** The pass condition requires Move 2 at score 4 and confidence Low in the final packet, with no later change. The final packet gives Move 2 as 4 and Low, which matches the expected value from the reference rules: all D/E3 answers give score 4 and no cap, and the E3 claims lacking date, log and CAPA fail the consistency check and force Low confidence. No fail indicator appears.

---

Final Liability rests with the Human.
