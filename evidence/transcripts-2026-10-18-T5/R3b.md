# redcap-00 R3b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:39 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R3: reference.md 8.2 "This is the only route to a score of 0 and the only case in which a move’s score is reported as Unknown/Insufficient data."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 1 (Safe pause) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: weak evidence short of the zero rule is capped at 2 and is not reported as Unknown

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E1. Q2 Safety and continuity checks: C, E1. Q3 Communications readiness: C, E1. Q4 Contractual suspension basis: C, E1.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: no approver named; nothing documented. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, consistency checks recorded)
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers. Tier-1 is the cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** A–D map to pattern scores 1–4. A = none/unknown/ad hoc, B = partial/informal, C = documented and owned but not recently tested, D = tested in the last 12 months with logs and CAPA.
- **Evidence:** E0 = none (0), E1 = verbal only (1), E2 = documented artifact plus owner role (2), E3 = tested in the last 12 months with a log and a CAPA (3).
- **Provisional score:** This is the mean of the four pattern scores, rounded, with exact halves rounding down. A move scores 0 (Unknown) only if 3 or more of its 4 answers are A at E0.
- **Caps:** If a move's evidence average is below 2, its score is capped at 2. If its prerequisite question is answered A, its score is also capped at 2. The final score is the lowest result.
- **Confidence:** High requires more than half of answers at E3. Medium requires more than half at E2 or E3 plus at least one E3. Anything else is Low, and a failed consistency check forces Low.

## 3) Scorecard

**Move 1: Safe pause — Score 2 | Confidence Low | #E0 0 #E1 4 #E2 0 #E3 0**
- All four answers are C, so the provisional score is 3. The evidence average is 1.00, which is below 2, so the evidence-average cap sets the score at 2. Q1 (prerequisite) is C, so no prerequisite cap applies.
- There are no E2 or E3 answers, so the consistency check passes by default. Confidence is still Low under Section 4. You reported no approver named and nothing documented, which matches the E1 ratings.

**Move 2: Treasury reroute — Score 3 | Confidence Low | #E0 0 #E1 0 #E2 4 #E3 0**
- All four answers are C, so the provisional score is 3. The evidence average is 2.00, which is not below 2, and Q1 (prerequisite) is C, so no cap applies.
- The consistency check passes: the CFO is approver, the Treasurer is backup, and artifacts are in the treasury system. With no E3 answer, Medium is not reached, so confidence is Low.

**Move 3: Data switchboard — Score 3 | Confidence Low | #E0 0 #E1 0 #E2 4 #E3 0**
- All four answers are C, so the provisional score is 3. The evidence average is 2.00 and Q1 (prerequisite) is C, so no cap applies.
- The consistency check passes: the CIO is approver and artifacts are in the IT service management tool. With no E3 answer, confidence is Low.

**Move 4: Substitution — Score 3 | Confidence Low | #E0 0 #E1 0 #E2 4 #E3 0**
- All four answers are C, so the provisional score is 3. The evidence average is 2.00 and Q2 (prerequisite) is C, so no cap applies.
- The consistency check passes: the COO is approver and artifacts are in the procurement system. With no E3 answer, confidence is Low.

**Move 5: Market exit — Score 3 | Confidence Low | #E0 0 #E1 0 #E2 4 #E3 0**
- All four answers are C, so the provisional score is 3. The evidence average is 2.00 and Q1 (prerequisite) is C, so no cap applies.
- The consistency check passes: the CEO is approver and artifacts are in the board portal. With no E3 answer, confidence is Low.

## 4) Evidence Index

**Move 1: Safe pause**

| Artifact type | Label |
|---|---|
| Stop authority matrix | Claimed |
| Safety and continuity checklist | Claimed |
| Rollback plan | Claimed |
| Communications templates (internal, customer, regulator) | Claimed |
| Contractual suspension clause summary | Claimed |
| Decision log | Unknown |
| Resume plan | Unknown |
| Escalation path | Unknown |

**Move 2: Treasury reroute**

| Artifact type | Label |
|---|---|
| Alternate bank and rail pre-clearance record | Documented |
| Freeze or hold playbook | Documented |
| Counterparty trigger and escalation definitions | Documented |
| 72-hour reroute execution plan | Documented |
| KYC/KYB bundle | Unknown |
| Letters of credit or alternate settlement playbook | Unknown |
| Treasury authority and backup delegation | Claimed (approver and backup named; artifact not assessed) |
| Reroute exercise log and CAPA | Unknown |

**Move 3: Data switchboard**

| Artifact type | Label |
|---|---|
| Tier-1 data flow map (including logs and telemetry) | Documented |
| Transfer mechanism options map | Documented |
| Segmentation, localization and shutdown runbook | Documented |
| Privileged and emergency access logging control description | Documented |
| Subprocessor list | Unknown |
| OT or critical access boundary procedure | Unknown |
| Stop-cleanly retention and deletion procedure | Unknown |
| Runbook exercise log and CAPA | Unknown |

**Move 4: Substitution**

| Artifact type | Label |
|---|---|
| Ranked Tier-1 single-points-of-failure list | Documented |
| Qualified alternates register | Documented |
| Portability or failover plan | Documented |
| Substitution or portability rights summary | Documented |
| Concentration limits | Unknown |
| Logistics reroute plan | Unknown |
| Cutover gate checklist and evidence pack | Unknown |

**Move 5: Market exit**

| Artifact type | Label |
|---|---|
| Exit plan (ops, data, people, comms, support) | Documented |
| Termination and unwind path summary | Documented |
| Customer obligations and support plan | Documented |
| Data and people plan | Documented |
| Distributor or JV obligations map | Unknown |
| Assets and IP handling procedure | Unknown |
| Regulator and customer comms workflow | Unknown |

## 5) 72-Hour Breakpoints

Each move's four answers are tied at C. The weakest answer was selected by its relevance to the ERP ransomware scenario.

- **0–6 h | Move 1 | Missing authority** (from Q1 Stop authority clarity, C at E1; from answers, not exercised): No approver can be named and no authority matrix artifact exists, so no one can confirm who orders a pause of warehouse dispatch or order intake in the first hours.
- **6–24 h | Move 2 | Operational infeasibility** (from Q4 Execute within 72 hours, "likely" at E2; from answers, not exercised): The reroute path is pre-cleared but has never been exercised, so it is unproven whether payments can move without ERP-generated payment data.
- **0–6 h | Move 3 | Operational infeasibility** (from Q3 Segmentation, localization, shutdown runbook, C at E2; from answers, not exercised): The shutdown and segmentation runbook has never been run, so containment steps may stall or conflict with portal and ERP dependencies under time pressure.
- **6–24 h | Move 4 | Missing alternate** (from Q3 Portability or failover plan, C at E2; from answers, not exercised): The ERP failover plan is documented but untested, so it is unknown whether order, inventory and dispatch can run on an alternate path within 72 hours.
- **24–72 h | Move 5 | Comms approval delay** (from Q3 Customer obligations and support plan, C at E2; from answers, not exercised): The support plan exists, but there are no pre-approved scripts or comms workflow (the D criteria), so customer messaging across about 300 accounts may queue for approval.

## 6) Top Blockers and Fixes

1. **Blocker:** Stop authority is undocumented and no approver is named (Move 1, Q1).
   - **Evidence gap:** E1 only; no artifact and no owner role.
   - **Minimal fix (2 weeks):** Name the pause approver and a backup, and record them in a one-page authority matrix.
   - **Proper fix (6–12 weeks):** Ratify a delegated authority matrix covering dispatch, intake and portal pause, then exercise and log it.
   - **Owner role:** COO with CEO sign-off.

2. **Blocker:** The safety and continuity checklist is verbal only (Move 1, Q2).
   - **Evidence gap:** E1; no checklist or rollback artifact.
   - **Minimal fix (2 weeks):** Write down the pause safety checks for hazardous storage and handling while the ERP is unavailable.
   - **Proper fix (6–12 weeks):** Build a checklist plus rollback plan with criteria and test it in a drill.
   - **Owner role:** EHS lead or Warehouse Operations Head.

3. **Blocker:** Communications templates are claimed but not shown to exist (Move 1, Q3).
   - **Evidence gap:** E1; no artifact location.
   - **Minimal fix (2 weeks):** Draft internal, customer and regulator holding statements and store them in a named system.
   - **Proper fix (6–12 weeks):** Pre-approve the templates with a named workflow and owners.
   - **Owner role:** Head of Communications.

4. **Blocker:** The contractual suspension basis is verbal only (Move 1, Q4).
   - **Evidence gap:** E1; no clause summary artifact.
   - **Minimal fix (2 weeks):** Prepare a redacted summary of suspension and notice triggers for the Tier-1 customer and supplier contract types.
   - **Proper fix (6–12 weeks):** Map triggers and notices to each Tier-1 contract with counsel input.
   - **Owner role:** General Counsel or Contracts Manager.

5. **Blocker:** The treasury reroute has never been exercised (Move 2, Q1 and Q4).
   - **Evidence gap:** E2 with no E3; the 72-hour feasibility is only "likely."
   - **Minimal fix (2 weeks):** Run a desk check of a reroute that does not rely on ERP payment files, and log it.
   - **Proper fix (6–12 weeks):** Run a full reroute exercise with logs and CAPA.
   - **Owner role:** Treasurer, with the CFO approving.

6. **Blocker:** The freeze or hold playbook and counterparty triggers are untested (Move 2, Q2 and Q3).
   - **Evidence gap:** E2; no roles drill and no exercised escalation.
   - **Minimal fix (2 weeks):** Walk through the playbook with named roles and record the gaps found.
   - **Proper fix (6–12 weeks):** Monitor the triggers and exercise the escalation path with CAPA.
   - **Owner role:** Treasurer.

7. **Blocker:** The shutdown and segmentation runbook is untested (Move 3, Q3).
   - **Evidence gap:** E2; no exercise log.
   - **Minimal fix (2 weeks):** Run a tabletop walkthrough of the ERP and portal isolation steps.
   - **Proper fix (6–12 weeks):** Run a technical test on a non-production Tier-1 environment with logged outcomes and CAPA.
   - **Owner role:** CIO or IT Security Lead.

8. **Blocker:** Emergency access logging is documented but not proven (Move 3, Q4).
   - **Evidence gap:** E2; no tested audit trail.
   - **Minimal fix (2 weeks):** Confirm that emergency access records can be produced on request, and log the check.
   - **Proper fix (6–12 weeks):** Test break-glass access with an audit trail review and CAPA.
   - **Owner role:** IT Security Lead.

9. **Blocker:** The ERP failover plan and qualified alternates are unproven within 72 hours (Move 4, Q2 and Q3).
   - **Evidence gap:** E2; failover not tested in the last 12 months.
   - **Minimal fix (2 weeks):** Define a manual or offline order-to-dispatch fallback and confirm the alternates are reachable.
   - **Proper fix (6–12 weeks):** Run a failover exercise with logged outcomes, and confirm the alternates are viable within 72 hours.
   - **Owner role:** COO with the CIO.

10. **Blocker:** The customer support and exit plans have never been rehearsed (Move 5, Q1 and Q3).
    - **Evidence gap:** E2; no scripts, workflow or tabletop.
    - **Minimal fix (2 weeks):** Draft customer outage scripts tied to the documented support plan.
    - **Proper fix (6–12 weeks):** Run an exit and support tabletop with logged decisions and CAPA.
    - **Owner role:** Head of Customer Service with the CEO.

## 7) 30/60/90-Day Plan

**Workstream 1: Safe pause from verbal to documented (Move 1)**
- **Outcome:** All Move 1 answers reach E2, with a named approver and artifact location.
- **Tasks:**
  - Days 0–30: name the pause approver and a backup.
  - Days 0–30: produce the authority matrix.
  - Days 0–30: write the hazardous-materials safety checklist and rollback plan.
  - Days 31–60: draft and file the comms templates.
  - Days 31–60: complete the suspension trigger summary with counsel input.
  - Days 61–90: walk through the full pause sequence.
- **Gates:**
  - The approver role is named and the artifact location is recorded.
  - All four artifacts are retrievable within 15 minutes.
- **Owner roles:** COO, EHS lead, Head of Communications, General Counsel.
- **Stop rule:** Pause the workstream and escalate to the CEO if no approver is named by day 30.

**Workstream 2: Evidence-to-E3 exercise program (Moves 2–4)**
- **Outcome:** At least one E3 answer each for Moves 2, 3 and 4, which opens the path to Medium confidence.
- **Tasks:**
  - Days 0–30: schedule the ERP ransomware tabletop.
  - Days 31–60: run the treasury reroute desk test.
  - Days 31–60: run the shutdown runbook walkthrough.
  - Days 61–90: run the ERP failover exercise.
  - Days 61–90: record the date, log and CAPA for each exercise.
- **Gates:**
  - Each exercise has a month/year, a stored log and at least one CAPA.
  - CAPAs are assigned to owner roles with due dates.
- **Owner roles:** CFO and Treasurer, CIO and IT Security Lead, COO.
- **Stop rule:** Do not claim E3 for any move whose exercise lacks a log or a CAPA.

**Workstream 3: Customer and stakeholder comms readiness (Moves 1 and 5)**
- **Outcome:** Pre-approved outage and support communications with a named approval workflow.
- **Tasks:**
  - Days 0–30: inventory the customer obligation categories.
  - Days 31–60: draft outage scripts and set the approval workflow and owners.
  - Days 61–90: run a 30-minute comms rehearsal and log the results.
- **Gates:**
  - Approvers are named for customer and regulator messaging.
  - Comms rehearsal timings are logged.
- **Owner roles:** Head of Communications, Head of Customer Service, CEO.
- **Stop rule:** Do not release templates until the approval workflow owners are recorded.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- CEO or crisis lead
- COO (pause and substitution)
- CFO and Treasurer
- CIO and IT Security Lead
- EHS lead
- Head of Communications
- Customer Service lead
- Scribe

**Agenda**
- **0–5 min:** Brief the scenario. The ERP is encrypted and expected to be down for five days.
- **5–15 min:** Decide what to pause, who authorizes it, which safety checks apply and what the first holding statement says.
- **15–25 min:** Choose the switch paths: payment rail, ERP fallback, data containment posture and logistics.
- **25–35 min:** Set the execution and monitoring plan for days 1–3 and identify the evidence to capture.
- **35–45 min:** List gaps, assign CAPAs and confirm owners.

**Decisions to log**
- The pause decision and its approver.
- The safety checks passed.
- The holding statement approval.
- The reroute approval.
- The containment or shutdown decision.
- Fallback activation.
- Customer notice timing.

**Evidence to capture**
- A timestamped decision log.
- The artifact used for each decision, with its location.
- The time to locate each artifact.
- Any decisions blocked and the reasons.

**CAPA prompt**
- For each stall, record what was missing (authority, artifact, alternate, gate or comms approval).
- Record the minimal fix, the owner role and the due date.
- Record the date for re-testing.

## 9) Escalations

**ESCALATE.** The following triggers come from the scenario described:

- **Criminal: ransomware attack.** This is planning guidance only. Executive and counsel questions include:
  - When and how should law enforcement be engaged?
  - What evidence must be preserved?
  - What notification duties may apply in your (Unknown) jurisdiction?
- **Sanctions (potential): any ransom payment consideration.** No sanctions determination is made here. Refer any payment question to counsel before any decision, and include it in the Move 2 approval path (CFO and CEO).
- **Physical safety (potential): hazardous chemical storage and dispatch operating without the ERP.** This affects inventory location, handling records and dispatch controls. Engage the EHS lead immediately.

**Recommended path:** CEO or crisis lead, then General Counsel or external counsel, then CIO and IT Security Lead plus the EHS lead, then board notice as counsel advises.

The financial (about USD 2 million) and people (no more than 2,000) estimates are below the escalation thresholds.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-declared.
- **No document validation:** No artifacts were reviewed, so "Documented" reflects claims of artifact plus owner role only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification and contract questions need counsel review.
- **Scenario simplification:** A single five-day ERP outage does not model cascading failures at the portal, bank or suppliers.
- **Partial coverage:** Fast Baseline covers Q1–Q4 only. Q5–Q7 themes are shown as Unknown in the Evidence Index.
- **Tie-breaking:** Each move had uniform C answers, so the breakpoints were selected by scenario relevance.
- **Confidence ceiling:** No E3 evidence was reported anywhere, so confidence cannot exceed Low until exercises are logged with CAPA.
- **Impact estimates:** These are user-supplied and unverified.
- **Scope:** This packet is informational. It is not a sanctions screening or a certification of any kind.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: Score 2, Confidence Low

## Score

**Verdict: PASS.** The Turn 1 Scorecard gives Move 1 a score of 2 with Low confidence. That matches the deterministic computation: provisional score 3, capped at 2 by the evidence-average rule, with the zero rule not triggered. Move 1 is not reported as Unknown. Turn 2 repeats the same values unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
