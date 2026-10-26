# redcap-00-r1 R6a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:31 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R6: reference.md 3.1 "the mean of its evidence scores (Section 2: E0=0, E1=1, E2=2, E3=3) ... not rounded"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: evidence average 1.75 is below 2: cap applies

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E1. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

Safety gate confirmed. Intake and Fast Baseline answers received. All five consistency checks were recorded. The packet follows.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers)
- **Scenario tested:** Ransomware outage takes the cloud ERP offline for 5 days. The user estimates worst-case impact at about USD 2m and no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, 3 warehouses in one country and about 300 business customers.
  - Tier-1 dependencies: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

---

## 2) How Scoring Works

- **Pattern score (A–D = 1–4).** A means none, unknown or person-dependent. B means partial or untested. C means documented, owned and repeatable. D means tested in the last 12 months with logs and CAPA, with viable alternates.
- **Evidence (E0–E3 = 0–3).** E0 means nothing exists. E1 means verbal only. E2 means a named artifact with an owner role. E3 means tested in the last 12 months with a log and a CAPA.
- **Provisional score.** This is the mean of the four pattern scores, rounded, with exact halves rounding down. A move scores 0 (Unknown) only if 3 or more of its 4 answers are A at E0.
- **Caps.** If a move's evidence average is below 2, its score is capped at 2. If its prerequisite question is answered A, its score is also capped at 2.
- **Confidence.** High or Medium requires at least one E3 answer and a passed consistency check. Otherwise confidence is Low.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | **2** (capped) | Low | 0 | 1 | 3 | 0 |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C at E2, so the provisional score is 3. The evidence average is 2.0, so the evidence cap does not apply. Q1 is C, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. Nothing has been exercised, so readiness to pause hazardous-goods operations without ERP is unproven. The consistency check passes: the approver is the Operations Director and artifacts sit in the quality document system.

**Move 2: Treasury reroute (3, Low)**
- All four answers are C at E2, so the provisional score is 3 with no caps. Alternate rails are "pre-cleared", not tested.
- Confidence is Low because there are no E3 answers. Q4 says 72-hour execution is "likely", not proven. The consistency check passes: the approver is the CFO, the Treasurer is backup, and artifacts sit in the treasury system.

**Move 3: Data switchboard (3, Low)**
- All four answers are C at E2, so the provisional score is 3 with no caps. A data flow map and a shutdown runbook exist but have not been tested.
- Confidence is Low because there are no E3 answers. This is the move most exposed in a ransomware scenario. The consistency check passes: the approver is the CIO and artifacts sit in the ITSM tool.

**Move 4: Substitution (2, Low)**
- The provisional score is 3. However, Q1 (single points of failure) is E1, so the evidence average is (1+2+2+2)/4 = 1.75. That is below 2, so the evidence-average cap sets the score at **2**. Q2 is C, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. The Tier-1 single-point-of-failure list is verbal only. The consistency check passes: the approver is the COO and artifacts sit in the procurement system.

**Move 5: Market exit (3, Low)**
- All four answers are C at E2, so the provisional score is 3 with no caps. The exit plan is documented but has never been run as a tabletop.
- Confidence is Low because there are no E3 answers. This move is the least directly triggered by a 5-day ERP outage, but customer obligations would still be exercised. The consistency check passes: the approver is the CEO and artifacts sit in the board portal.

**Overall read:** The documentation baseline is solid and consistent. No move has execution proof. Every confidence rating is Low for that single reason: there are zero E3 answers.

---

## 4) Evidence Index

Labels: E2 = Documented, E1 = Claimed, not asked in Fast Baseline = Unknown. No artifact is labelled Tested.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contract suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger definitions with escalation: Documented
- 72-hour execution readiness assessment: Documented
- KYB bundle: Unknown
- Treasury authority and backup matrix: Claimed (backup named in the consistency check; Q7 not asked)

**Move 3: Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging description: Documented
- Subprocessor list: Unknown
- OT and critical access boundary: Unknown
- Retention and deletion procedure: Unknown

**Move 4: Substitution**
- Tier-1 single-point-of-failure list: Claimed
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5: Market exit**
- Exit plan: Documented
- Termination and unwind paths summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Regulator and customer comms workflow: Unknown

---

## 5) 72-Hour Breakpoints

Moves 1, 2, 3 and 5 have four answers tied at C/E2. For those moves, the breakpoint uses the tied answer most exposed to the ERP-outage scenario.

- **Move 1 (Q2 Safety and continuity checks):** *From answers, not exercised.*
  - Window: 0–6 hours.
  - What breaks: missing gate.
  - Why it blocks execution: the rollback plan and pause criteria have never been tested, so the Operations Director cannot confirm hazardous stock and dispatches can be held safely without ERP records.
- **Move 2 (Q4 Execute within 72 hours):** *From answers, not exercised.*
  - Window: 6–24 hours.
  - What breaks: operational infeasibility.
  - Why it blocks execution: execution is rated "likely" and has never been proven, so the reroute to pre-cleared rails may stall on unrehearsed steps while ERP-driven payment runs are down.
- **Move 3 (Q3 Segmentation and shutdown runbook):** *From answers, not exercised.*
  - Window: 0–6 hours.
  - What breaks: operational infeasibility.
  - Why it blocks execution: an untested runbook may not isolate the ERP and connected systems, including the order portal, fast enough to contain the outage.
- **Move 4 (Q1 Tier-1 single points of failure, E1):** *From answers, not exercised.*
  - Window: 6–24 hours.
  - What breaks: missing artifact.
  - Why it blocks execution: without a named, ranked single-point-of-failure list, the COO cannot quickly decide which dependency fails over first.
- **Move 5 (Q3 Customer obligations and support plan):** *From answers, not exercised.*
  - Window: 24–72 hours.
  - What breaks: comms approval delay.
  - Why it blocks execution: the plan is documented, but scripts and an approval workflow are not ready, so notices to about 300 customers may stall.

---

## 6) Top Blockers and Fixes

1. **Blocker: no move has been exercised.**
   - Evidence gap: 0 of 20 answers are E3, so all confidence is Low.
   - Minimal fix (2 weeks): run the 45-minute drill in Section 8 against the ERP scenario, then log it and open CAPA.
   - Proper fix (6–12 weeks): an exercise calendar covering all 5 moves, with logs and CAPA tracking.
   - Owner role: COO, with a Risk or Resilience lead.
2. **Blocker: the Tier-1 single-point-of-failure list is verbal only (Move 4 Q1).**
   - Evidence gap: E1 with no named artifact. This triggers the cap.
   - Minimal fix: write a ranked list covering the ERP, house bank, two suppliers, logistics provider and portal, with a named owner, stored in the procurement system.
   - Proper fix: quarterly review cadence linked to the risk register (D-level).
   - Owner role: COO, with Head of Procurement.
3. **Blocker: hazardous-goods pause and rollback are untested without ERP (Move 1 Q2).**
   - Evidence gap: the checklist is documented but not tested and has no criteria.
   - Minimal fix: a tabletop walkthrough of the checklist under ERP-down conditions, including offline access to inventory and safety records.
   - Proper fix: a warehouse drill at one site, with logged outcomes and CAPA.
   - Owner role: Operations Director, with the EHS lead.
4. **Blocker: comms templates are not pre-approved (Move 1 Q3).**
   - Evidence gap: templates exist, but there is no approval workflow or named owners.
   - Minimal fix: pre-approve the internal and customer holding statements for a ransomware outage.
   - Proper fix: a full approval workflow with backup approvers, including regulator templates reviewed by counsel.
   - Owner role: Communications lead, with the Operations Director.
5. **Blocker: 72-hour treasury execution is unproven (Move 2 Q4).**
   - Evidence gap: execution is rated "likely" and there is no exercise record.
   - Minimal fix: walk through the reroute steps and sign-offs with the CFO and Treasurer, and log the timings.
   - Proper fix: a live low-value test payment over the alternate rail, with an evidence pack.
   - Owner role: CFO and Treasurer.
6. **Blocker: the freeze or hold playbook has never been rehearsed with roles (Move 2 Q2).**
   - Evidence gap: documented only.
   - Minimal fix: assign roles and the manual-payment authorization path for an ERP-down period.
   - Proper fix: a drill with logged comms, plus CAPA.
   - Owner role: Treasurer.
7. **Blocker: the segmentation and shutdown runbook is untested (Move 3 Q3).**
   - Evidence gap: documented only.
   - Minimal fix: a tabletop of the isolation sequence for the ERP and order portal, with decision points logged.
   - Proper fix: a technical isolation test in a non-production environment, with CAPA.
   - Owner role: CIO.
8. **Blocker: emergency access logging is untested (Move 3 Q4).**
   - Evidence gap: no audit-trail test.
   - Minimal fix: confirm the emergency access procedure and log retention, and verify one sample log can be produced.
   - Proper fix: a periodic emergency-access test with audit-trail review.
   - Owner role: CIO, with the IT Security lead.
9. **Blocker: ERP and logistics failover is not shown viable within 72 hours (Move 4 Q2 and Q3).**
   - Evidence gap: alternates are qualified, but neither contractual nor operational viability is evidenced. The failover plan is untested.
   - Minimal fix: confirm the manual order-to-dispatch fallback and an alternate carrier contact path.
   - Proper fix: a tested failover or manual-operations drill in the last 12 months, with substitution rights mapped for Tier-1 vendors.
   - Owner role: COO, with the CIO.
10. **Blocker: the customer support plan has no scripts or workflow, and the exit plan has never been run as a tabletop (Move 5 Q1 and Q3).**
    - Evidence gap: documented only.
    - Minimal fix: draft customer scripts for delayed orders and an approval path.
    - Proper fix: a full exit-plan tabletop with logs and CAPA.
    - Owner role: CEO, with the Commercial Director.

---

## 7) 30/60/90-Day Plan

**Workstream A: Convert documentation into tested evidence (all moves)**
- **Outcome:** at least one E3 answer per move, which makes Medium confidence possible.
- **Tasks:**
  - Day 30: run the 45-minute drill on the ERP scenario covering Moves 1–3.
  - Day 60: run the drill covering Moves 4–5.
  - Record the month and year, the log and the CAPA for each drill.
  - Store all logs at the artifact locations already named.
  - Day 90: re-run the Fast Baseline self-check.
- **Gates:**
  - Every drill produces a log and at least one CAPA.
  - Every CAPA has an owner and a due date.
- **Owner roles:** COO, with each move's approver.
- **Stop rule:** if a drill cannot name an approver or produce an artifact, stop and fix that gap before the next drill.

**Workstream B: ERP-down operating continuity (Moves 1, 3, 4)**
- **Outcome:** a safe pause, isolation and manual fallback that can each be shown to work within 72 hours.
- **Tasks:**
  - Day 30: document the ranked Tier-1 single-point-of-failure list.
  - Day 30: confirm offline access to inventory and safety records.
  - Day 60: tabletop the shutdown runbook and test emergency access logging.
  - Day 90: run a manual order-to-dispatch drill at one warehouse.
- **Gates:**
  - The single-point-of-failure list is approved by the COO.
  - EHS signs off on the pause checklist criteria.
- **Owner roles:** Operations Director, CIO, COO and the EHS lead.
- **Stop rule:** suspend the warehouse drill if any physical safety check cannot be met.

**Workstream C: Cash and customer continuity (Moves 2, 5)**
- **Outcome:** a proven 72-hour treasury reroute and ready-to-send customer comms.
- **Tasks:**
  - Day 30: walk through the reroute steps and the freeze/hold roles.
  - Day 60: send a low-value test payment over the alternate rail.
  - Day 60: produce customer scripts with an approval workflow.
  - Day 90: hold an exit-plan tabletop with the CEO.
- **Gates:**
  - The CFO signs off on the test payment evidence pack.
  - Counsel reviews the regulator and customer templates.
- **Owner roles:** CFO, Treasurer, CEO and the Commercial Director.
- **Stop rule:** stop the live test if bank pre-clearance cannot be confirmed in writing.

---

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk lead)
- Operations Director (Move 1)
- CFO and Treasurer (Move 2)
- CIO (Move 3)
- COO (Move 4)
- CEO (Move 5)
- Communications lead
- EHS lead
- Scribe

**Agenda**
- 0–5 min: scenario brief. Ransomware takes the ERP down for 5 days.
- 5–15 min: hours 0–6. What is paused, who authorizes it, which safety checks must pass, and what the first holding statement says.
- 15–25 min: hours 6–24. Which switch path is chosen (rail, manual ops, data posture, carrier), what gates apply and who signs off.
- 25–35 min: hours 24–72. What is executed and monitored, and what is said to customers.
- 35–45 min: debrief, breakpoints and CAPA.

**Decisions to log**
- Each decision with a timestamp, approver role and the artifact used.
- Any decision delayed by missing authority or a missing artifact.

**Evidence to capture**
- The drill log, with month and year.
- The artifacts referenced.
- Gaps found, mapped to Move and question.
- Timings against the 0–6, 6–24 and 24–72 hour windows.

**CAPA prompt**
- "Which single failure would have stopped us within 72 hours?"
- For that failure, record: owner role, minimal fix, due date and re-test date.

---

## 9) Escalations

The quantitative thresholds are **not met**. The estimated USD 2m is below USD 10m, and the estimated 2,000 people is below 100,000.

The scenario does contain category triggers. They apply to a real incident, not to this self-check exercise.

**ESCALATE (scenario-conditional):**
- **Criminal:** ransomware is a criminal act. A live event calls for executive, counsel and law-enforcement liaison decisions.
- **Physical safety:** pausing specialty-chemical warehouse operations without ERP records raises hazardous-materials safety questions.
- **Sanctions:** any consideration of ransom payment raises sanctions questions. This tool makes no sanctions determination.
- **Regulator inquiry:** a real outage may prompt notification questions. Jurisdiction is Unknown, so no determination is made.

**Recommended escalation path:** CEO, then General Counsel or external counsel, then the board (Risk or Audit committee), with the CIO and EHS lead as technical advisors.

**Questions for counsel:**
- What notification duties apply in our jurisdiction to a ransomware outage?
- Which constraints apply to ransom-payment decisions?
- Do our customer and supplier suspension clauses support a 5-day pause?

---

## 10) Known Limits + Version

- **Self-report bias:** every answer is self-assessed.
- **No document validation:** "Documented" (E2) has not been verified, and no artifact was reviewed.
- **Jurisdiction ambiguity:** jurisdiction is Unknown, so no legal, regulatory or compliance conclusions are drawn.
- **Scenario simplification:** a single 5-day ERP outage. Cascades such as supplier or carrier compromise or data exfiltration are not modelled.
- **Fast Baseline coverage:** Q5–Q7 were not asked, so related artifacts are Unknown.
- **Impact figures:** USD 2m and 2,000 people are user estimates and were not validated.
- **Low confidence is structural:** with zero E3 answers, no move can exceed Low until it is exercised.
- **Not a security assessment:** this is not ransomware or technical security guidance, legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: score 2 (capped), confidence Low.

## Score

**Verdict: PASS.** The pass condition requires only that the final Output Packet's Scorecard show Move 4 at score 2 and confidence Low, with no later change. The packet shows Move 4 as 2 and Low, computed correctly from an evidence average of 1.75 (below 2) with the cap applied. Turn 2 restates the same values without alteration. No fail indicator appears.

---

Final Liability rests with the Human.
