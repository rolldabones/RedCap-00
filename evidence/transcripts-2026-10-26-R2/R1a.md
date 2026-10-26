# redcap-00-r2 R1a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:41 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R1: reference.md 8.1 "An exact half rounds down, the conservative direction: 2.5 → 2 and 3.5 → 3."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: an exact half (2.5) rounds down to 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: B, E2. Q2 Qualified alternates: B, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

## 1) Snapshot

- **Jurisdiction:** Unknown. Nothing in this packet is a legal or compliance determination.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers), followed by consistency checks (Section 5.2)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. User-estimated worst case is about USD 2m impact and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with 3 warehouses in one country, about 300 business customers and about 400 staff. Tier-1 assets are the cloud ERP, the house bank, 2 bulk suppliers, 1 logistics provider and the customer order portal.
- **Safety gate:** The user confirmed that no sensitive data was provided. Only summaries were received.

## 2) How Scoring Works

- **A–D pattern score:**
  - A=1: none, unknown or ad hoc
  - B=2: partial or untested
  - C=3: documented, owned, limited or no recent testing
  - D=4: tested in the last 12 months with logs and CAPA, with alternates viable within 72h
- **E0–E3 evidence score:**
  - E0=0: no evidence
  - E1=1: verbal only
  - E2=2: named artifact plus owner role
  - E3=3: exercised in the last 12 months with a log and at least one CAPA
- **Move score:**
  - The score is the mean of the move's pattern scores, rounded, with exact halves rounding down.
  - The score is 0 (Unknown) only if 3 or more of the 4 answers are A at E0.
- **Caps:**
  - If the evidence average is below 2, the score is capped at 2.
  - If the prerequisite question is answered A, the score is capped at 2.
  - The lowest value wins.
- **Confidence:**
  - High requires more than half of answers at E3.
  - Medium requires more than half at E2 or E3 and at least one E3.
  - Otherwise confidence is Low.
  - A failed consistency check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **2** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3 / Low**
- All four answers are C (mean 3.00). The evidence average is 2.00, which is not below 2. Q1 (stop authority) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passes: the approver is the Operations Director and artifacts sit in the quality document system. Nothing has been exercised in the last 12 months.

**Move 2 Treasury reroute: 3 / Low**
- All four answers are C (mean 3.00). The evidence average is 2.00. Q1 (alternate banks and rails) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passes: the approver is the CFO with the Treasurer as backup, and artifacts sit in the treasury system. Q4 "likely" means 72-hour execution has not been shown by exercise.

**Move 3 Data switchboard: 3 / Low**
- All four answers are C (mean 3.00). The evidence average is 2.00. Q1 (data flow map) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passes: the approver is the CIO and artifacts sit in the ITSM tool. The shutdown runbook and emergency access logging are documented but untested, which is the core risk in a ransomware scenario.

**Move 4 Substitution: 2 / Low**
- The answers are B, B, C, C (mean 2.50), which rounds down to 2. The evidence average is 2.00 and Q2 (qualified alternates) is B rather than A, so no cap applies. The score of 2 comes from the answers themselves, not from a cap.
- Confidence is Low because there are no E3 answers. The consistency check passes: the approver is the COO and artifacts sit in the procurement system. The SPOF list is partial, and alternates are possible but unqualified.

**Move 5 Market exit: 3 / Low**
- All four answers are C (mean 3.00). The evidence average is 2.00. Q1 (exit plan) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passes: the approver is the CEO and artifacts sit in the board portal. The exit plan has not been tested in a tabletop.

## 4) Evidence Index

Labels:
- **Documented** = the item was answered at E2.
- **Claimed** = the item was mentioned verbally with no artifact named.
- **Unknown** = the item was not asked in Fast Baseline or not provided.
- **Tested** = none in this run.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator communication templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path under conflict: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire trigger definitions: Documented
- 72-hour reroute execution assessment: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement (LC) playbook: Unknown
- Treasury authority and backup delegation: Claimed (the Treasurer backup was named, but no delegation artifact was identified)

**Move 3 Data switchboard**
- Tier-1 data flow map, including logs and telemetry: Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Tier-1 single-point-of-failure list (partial, unranked): Documented
- Alternates list (unqualified): Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

Moves 1, 2, 3 and 5 have all answers tied at C. For each of these, the breakpoint uses the tied answer most exposed in the ERP-ransomware scenario.

- **Move 1, Q3 Communications readiness (C)**
  - From answers, not exercised.
  - Time window: 0–6h.
  - What breaks: comms approval delay.
  - Why it blocks execution: Templates exist but are not pre-approved, so the first holding statement to customers and staff waits on drafting and sign-off while orders and shipments stall.
- **Move 2, Q4 Execute within 72 hours ("likely", C)**
  - From answers, not exercised.
  - Time window: 6–24h.
  - What breaks: operational infeasibility.
  - Why it blocks execution: Nobody has proven the reroute can run without ERP-generated payment and receivables data, so the CFO cannot confirm supplier and payroll-critical flows will settle inside 72 hours.
- **Move 3, Q3 Segmentation and shutdown runbook (C)**
  - From answers, not exercised.
  - Time window: 0–6h.
  - What breaks: missing gate.
  - Why it blocks execution: The isolation runbook has never been run, so the CIO lacks tested go/no-go gates for containing the outage without cutting Tier-1 connections needed for warehouse and safety operations.
- **Move 4, Q2 Qualified alternates (B)**
  - From answers, not exercised.
  - Time window: 6–24h.
  - What breaks: missing alternate.
  - Why it blocks execution: Alternates are possible but unqualified, so there is no viable substitute for bulk supply, logistics or manual order handling within 72 hours.
- **Move 5, Q2 Trigger-based termination and unwind paths (C)**
  - From answers, not exercised.
  - Time window: 24–72h.
  - What breaks: missing gate.
  - Why it blocks execution: The unwind paths are documented but not rehearsed and have no defined trigger thresholds, so the CEO cannot decide whether a prolonged outage warrants an exit from specific customer segments or contracts.

## 6) Top Blockers and Fixes

1. **Unqualified alternates (Move 4 Q2, B)**
   - Evidence gap: The list is E2 but contains no qualification status or 72-hour viability.
   - Minimal fix (2 weeks): Rank alternates for the 2 bulk suppliers and the logistics provider. Confirm 72-hour viability for the top one in each category.
   - Proper fix (6–12 weeks): Qualify at least one alternate per Tier-1 vendor, including onboarding readiness, and test one cutover.
   - Owner role: COO, with Head of Procurement.
2. **Partial, unranked SPOF list (Move 4 Q1, B)**
   - Evidence gap: The list does not rank or cover all Tier-1 items, including the ERP and order portal.
   - Minimal fix (2 weeks): Produce a ranked SPOF list for all 6 Tier-1 items.
   - Proper fix (6–12 weeks): Set a quarterly review cadence with a logged review record.
   - Owner role: COO.
3. **ERP failover and portability plan untested (Move 4 Q3, C)**
   - Evidence gap: There is no exercise log or CAPA.
   - Minimal fix (2 weeks): Hold a walkthrough of manual order-to-ship and order-to-cash fallback for 5 days without ERP.
   - Proper fix (6–12 weeks): Run a timed restore and manual-mode exercise, then log it and open CAPA.
   - Owner role: CIO, with COO.
4. **72-hour treasury execution unproven (Move 2 Q4, C "likely")**
   - Evidence gap: There is no exercise evidence.
   - Minimal fix (2 weeks): Hold a desk check of critical payments that can run without ERP data.
   - Proper fix (6–12 weeks): Run a live, logged reroute test of a low-value payment on the alternate rail, with CAPA.
   - Owner role: CFO, with Treasurer as backup.
5. **Alternate rails pre-cleared but untested (Move 2 Q1, C)**
   - Evidence gap: There is no test record.
   - Minimal fix (2 weeks): Confirm current access readiness and approval paths for the alternate rail.
   - Proper fix (6–12 weeks): Test the reroute path with evidence.
   - Owner role: Treasurer.
6. **Shutdown and segmentation runbook untested (Move 3 Q3, C)**
   - Evidence gap: There is no exercise log or CAPA.
   - Minimal fix (2 weeks): Hold a tabletop walkthrough of the isolation steps and gates for the ERP and order portal.
   - Proper fix (6–12 weeks): Run a controlled technical test on a non-production Tier-1 segment, logged with CAPA.
   - Owner role: CIO.
7. **Emergency access logging untested (Move 3 Q4, C)**
   - Evidence gap: No audit trail has been demonstrated.
   - Minimal fix (2 weeks): Confirm how the emergency access process is logged and who reviews the log.
   - Proper fix (6–12 weeks): Exercise the emergency access process and retain the audit trail as evidence.
   - Owner role: CIO, with Information Security lead.
8. **Comms templates not pre-approved (Move 1 Q3, C)**
   - Evidence gap: There is no approval workflow artifact.
   - Minimal fix (2 weeks): Pre-approve a holding statement for an ERP outage for staff, customers and suppliers.
   - Proper fix (6–12 weeks): Build an approval workflow with named owner roles and test it in a drill. Have counsel review any regulator templates.
   - Owner role: Operations Director, with Communications lead.
9. **Safety and continuity checklist untested (Move 1 Q2, C)**
   - Evidence gap: The checklist and rollback plan have no tested criteria.
   - Minimal fix (2 weeks): Add ERP-down checks for hazardous inventory visibility, safety documentation access and dangerous-goods shipping holds.
   - Proper fix (6–12 weeks): Run a warehouse drill with pass/fail criteria, logged with CAPA.
   - Owner role: Operations Director, with EHS lead.
10. **Exit and unwind paths not rehearsed (Move 5 Q1/Q2, C)**
    - Evidence gap: There is no tabletop or trigger thresholds.
    - Minimal fix (2 weeks): Define outage-duration triggers for segment or contract exit decisions.
    - Proper fix (6–12 weeks): Run an exit tabletop with legal, operations, data, people and comms roles, and log CAPA.
    - Owner role: CEO, with General Counsel.

## 7) 30/60/90-Day Plan

**Workstream 1: Qualified substitution (Move 4)**
- **Outcome:** Each Tier-1 vendor has a ranked SPOF entry and at least one alternate that can be viable within 72 hours.
- **Tasks:**
  - Days 0–30: Rank the SPOF list across all 6 Tier-1 items.
  - Days 0–30: Shortlist alternates for the bulk suppliers and the logistics provider.
  - Days 30–60: Complete qualification steps for the top alternate in each category.
  - Days 30–60: Map substitution rights for Tier-1 vendors at summary level.
  - Days 60–90: Run one logged cutover exercise.
- **Gates:**
  - Ranked SPOF list approved by the COO.
  - At least one alternate per category confirmed viable within 72 hours.
  - Cutover exercise logged, with at least 1 CAPA.
- **Owner roles:** COO, Head of Procurement.
- **Stop rule:** Pause the work and escalate to the CEO if an alternate is found to have hazardous-material handling or licensing constraints. Refer any such constraint to counsel.

**Workstream 2: ERP-outage exercise for pause and isolation (Moves 1 and 3)**
- **Outcome:** Moves 1 and 3 move from E2 to E3, with a dated log and CAPA.
- **Tasks:**
  - Days 0–30: Add ERP-down safety checks to the continuity checklist.
  - Days 0–30: Pre-approve the holding statement.
  - Days 30–60: Run the 45-minute drill in Section 8.
  - Days 30–60: Walk through the shutdown runbook.
  - Days 60–90: Test emergency access logging.
  - Days 60–90: Close at least one CAPA per move.
- **Gates:**
  - Drill log stored in the quality document system and the ITSM tool.
  - CAPA opened with an owner and due date.
- **Owner roles:** Operations Director, CIO, EHS lead.
- **Stop rule:** Stop any technical test that risks production or safety systems. Revert to tabletop only.

**Workstream 3: Treasury reroute and outage-exit triggers (Moves 2 and 5)**
- **Outcome:** 72-hour treasury execution is proven by exercise, and exit triggers are defined.
- **Tasks:**
  - Days 0–30: Run a desk check of critical payments that do not depend on ERP.
  - Days 30–60: Run a logged low-value reroute test.
  - Days 30–60: Define outage-duration exit triggers.
  - Days 60–90: Run an exit tabletop.
  - Days 60–90: Log CAPA.
- **Gates:**
  - Reroute test evidence filed in the treasury system.
  - Exit triggers approved by the CEO and filed in the board portal.
- **Owner roles:** CFO, Treasurer, CEO, General Counsel.
- **Stop rule:** Halt the work if any step touches ransom-payment planning or counterparties of uncertain status. Refer to counsel (see Section 9).

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Scribe
- Operations Director (stop authority)
- CFO and Treasurer
- CIO
- COO
- CEO
- EHS lead
- Communications lead
- Counsel (observer)

**Agenda**
- **0–5 min:** Scenario brief. The ERP is encrypted, with an estimated restore time of 5 days.
- **5–15 min:** 0–6h window.
  - What is paused (shipments, dangerous goods dispatch, order portal)?
  - Who authorizes the pause?
  - Which safety checks must pass?
  - What is the first holding statement?
- **15–25 min:** 6–24h window.
  - Which switch path is chosen: manual order mode, alternate rail, isolation posture or logistics changes?
  - Which gates must pass, and who signs off?
- **25–35 min:** 24–72h window.
  - What is executed and monitored?
  - What evidence is captured?
  - Does any exit trigger apply?
- **35–45 min:** Hotwash.
  - Map breakpoints by time window, move and what broke.
  - Assign CAPA.

**Decisions to log**
- Pause decision and approver role
- Isolation and shutdown decision (CIO)
- Treasury reroute decision (CFO)
- Substitution cutover decision (COO)
- Exit trigger decision (CEO)
- Holding statement approval

**Evidence to capture**
- Drill month and year
- Attendees by role
- Timestamped decision log
- Artifacts used and their system locations
- Steps where an artifact was missing or unusable
- Breakpoint list

**CAPA prompt**
"For each breakpoint, record the root cause, the corrective action, the owner role, the due date and how closure will be evidenced. Open at least one CAPA per move exercised."

Note: E3 credit requires a month/year within the last 12 months, a log, and at least one CAPA.

## 9) Escalations

**ESCALATE.** The scenario as described contains these triggers:

- **Criminal:** Ransomware is criminal activity. Ask counsel whether to involve law enforcement, and whether and how to preserve evidence.
- **Physical safety:**
  - An ERP outage at a specialty chemicals distributor may remove visibility of hazardous inventory, safety documentation and dangerous-goods shipping records.
  - Escalate to the EHS lead and the Operations Director for safe-pause decisions.
- **Sanctions (conditional):**
  - If any ransom payment or negotiation is contemplated, counsel must assess possible sanctions exposure.
  - This tool makes no sanctions determination and gives no payment guidance.

**Not triggered on the information provided:**
- No regulator inquiry was reported.
- Impact of about USD 2m is below USD 10m.
- No more than 2,000 people affected is below 100,000.

**Recommended path:**
- The CEO convenes the incident executive group (COO, CFO, CIO, Operations Director, EHS lead).
- Engage General Counsel or outside counsel immediately.
- Brief the board through the board portal.

**Questions for counsel (Jurisdiction: Unknown):**
- Which incident notification obligations may apply, for example data, sector, or chemical-safety obligations?
- What are the law enforcement engagement options?
- Are there constraints on ransom-related decisions?
- How do contractual notice obligations to customers and Tier-1 vendors apply?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported and may be optimistic.
- **No document validation:** No artifact was reviewed. "Documented" reflects the claimed artifact type and owner role only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so legal, notification and regulatory implications were not assessed.
- **Scenario simplification:** A single 5-day ERP outage was modeled. Combined events, such as a vendor failure during the outage, were not tested.
- **Fast Baseline only:** Q5–Q7 per move were not asked, and their artifacts are listed as Unknown.
- **No mini tabletop was run:** The Section 5 breakpoints come from the answers and are not exercised findings.
- **Confidence is Low on every move** because there is no E3 evidence. Scores of 3 mean documented, not proven.
- **Impact estimates** (about USD 2m, no more than 2,000 people) are user-supplied and unverified. Escalation thresholds depend on them.
- **This is informational only.** It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 2, Confidence Low.

## Score

**Verdict: PASS.** The answers B, B, C, C map to 2, 2, 3, 3, a mean of 2.5, which rounds down to 2 under reference.md 8.1. No cap lowers it further. The evidence average is 2.0, which is not below 2, and the Q2 prerequisite is B, not A. Confidence is Low because there are no E3 answers. The packet reports Score 2 and Low for Move 4, and the follow-up turn repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
