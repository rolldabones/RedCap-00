# redcap-00-r2 Test-A

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:41 KST · **max_tokens:** 16000

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

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (20 questions plus the consistency checks)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. User-estimated worst case is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Footprint: specialty chemicals B2B distribution, three warehouses in one country, about 300 business customers, about 400 staff.
  - Tier-1 operations, systems and vendors: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers A–D** map to pattern scores 1–4:
  - A is none or ad hoc.
  - B is partial.
  - C is documented and owned.
  - D is tested in the last 12 months with logs and CAPA.
  - Each move's score is the average of its answers, rounded, with exact halves rounding down.
- **Evidence E0–E3** maps to evidence scores 0–3:
  - E0 is no evidence.
  - E1 is verbal only.
  - E2 is a named artifact with an owner role.
  - E3 is tested, logged and has a CAPA.
- **Caps:**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If a move's prerequisite question is answered A, its score is capped at 2.
  - A score of 0 (Unknown) applies only when 3 or more of the 4 answers are A at E0.
- **Confidence:**
  - High needs 3 or more of 4 answers at E3.
  - Medium needs 3 or more at E2/E3, including at least one E3.
  - Everything else is Low.
- **Consistency checks:** These cover the exercise date, log and CAPA for E3 answers, the approver role and the artifact location. A failed check forces Low confidence.

## 3) Scorecard

**Move 1: Safe pause**
- **Score:** 2
- **Confidence:** Low
- **Evidence distribution:** #E0 1, #E1 2, #E2 0, #E3 1
- **Rationale:**
  - All four answers are D, giving a provisional score of 4. The evidence average is 1.25 (from 1, 1, 0 and 3), which is below 2, so the score is capped at 2. The prerequisite (Q1 = D) is not triggered.
  - The consistency check passes:
    - Approver: Operations Director.
    - Artifact location: quality document system.
    - Exercise: April 2026, with a log and CAPA.
  - Only 1 of 4 answers is at E2/E3, so confidence is Low. Three D claims rest on E0/E1. This conflicts with the D definition, which requires testing with logs and CAPA.

**Move 2: Treasury reroute**
- **Score:** 3
- **Confidence:** Low
- **Evidence distribution:** #E0 0, #E1 0, #E2 4, #E3 0
- **Rationale:**
  - Four C answers give a provisional score of 3. The evidence average is exactly 2.00, so the cap does not apply. The prerequisite (Q1 = C) is not triggered.
  - The consistency check passes (approver: CFO, with the Treasurer as backup; artifact location: treasury system). With no E3 answer, confidence cannot reach Medium. The 72-hour reroute is "likely," not proven.

**Move 3: Data switchboard**
- **Score:** 3
- **Confidence:** Low
- **Evidence distribution:** #E0 0, #E1 0, #E2 4, #E3 0
- **Rationale:**
  - Four C answers give a provisional score of 3. The evidence average is 2.00, so no cap applies. The prerequisite (Q1 data flow map = C) is not triggered.
  - The consistency check passes (approver: CIO; artifact location: IT service management tool). The shutdown runbook and emergency access logging are documented but untested, which matters directly in a ransomware scenario.

**Move 4: Substitution**
- **Score:** 3
- **Confidence:** Low
- **Evidence distribution:** #E0 0, #E1 0, #E2 4, #E3 0
- **Rationale:**
  - Four C answers give a provisional score of 3. The evidence average is 2.00, so no cap applies. The prerequisite (Q2 qualified alternates = C) is not triggered.
  - The consistency check passes (approver: COO; artifact location: procurement system). The alternates are qualified but not shown to be viable within 72 hours. The ERP failover plan is untested.

**Move 5: Market exit**
- **Score:** 3
- **Confidence:** Low
- **Evidence distribution:** #E0 0, #E1 0, #E2 4, #E3 0
- **Rationale:**
  - Four C answers give a provisional score of 3. The evidence average is 2.00, so no cap applies. The prerequisite (Q1 exit plan = C) is not triggered.
  - The consistency check passes (approver: CEO; artifact location: board portal). The plans are documented but none is rehearsed. Customer scripts and the comms workflow are not confirmed ready.

**Board read:** Safe pause is the move with the strongest self-ratings (all D), yet it has the lowest score because evidence does not back the claims. Every move is at Low confidence because no move other than Move 1 has any tested evidence.

## 4) Evidence Index

Labels: Unknown = E0 or not asked; Claimed = E1; Documented = E2; Tested = E3.

**Move 1: Safe pause**

| Artifact type | Label |
|---|---|
| Stop authority matrix | Claimed |
| Safety and continuity checklist with rollback plan | Claimed |
| Communications templates (internal, customer, regulator) | Unknown |
| Contractual suspension clause summary | Tested (April 2026) |
| Drill log and CAPA record | Tested (April 2026) |
| Pause decision log | Unknown |
| Resume plan | Unknown |

**Move 2: Treasury reroute**

| Artifact type | Label |
|---|---|
| Alternate banks and rails register | Documented |
| Freeze/hold playbook | Documented |
| Counterparty tripwire definitions and escalation | Documented |
| 72-hour reroute execution plan | Documented |
| KYC/KYB bundle | Unknown |
| Treasury authority and backup delegation | Unknown |
| Reroute exercise log | Unknown |

**Move 3: Data switchboard**

| Artifact type | Label |
|---|---|
| Tier-1 data flow map (including logs and telemetry) | Documented |
| Transfer mechanism options map | Documented |
| Segmentation, localization and shutdown runbook | Documented |
| Privileged and emergency access logging control description | Documented |
| Subprocessor list | Unknown |
| OT/critical access boundary procedure | Unknown |
| Retention and deletion procedure | Unknown |

**Move 4: Substitution**

| Artifact type | Label |
|---|---|
| Ranked Tier-1 single-point-of-failure list | Documented |
| Alternate qualification records | Documented |
| Portability/failover plan (including ERP) | Documented |
| Substitution/portability rights summary | Documented |
| Concentration limits | Unknown |
| Logistics reroute plan | Unknown |
| Cutover gate criteria | Unknown |

**Move 5: Market exit**

| Artifact type | Label |
|---|---|
| Exit plan (legal, ops, data, people, comms, support) | Documented |
| Termination and unwind path summary | Documented |
| Customer obligations and support plan | Documented |
| Data and people plan | Documented |
| Distributor/JV obligations map | Unknown |
| Assets and IP handling procedure | Unknown |
| Regulator and customer comms workflow | Unknown |

## 5) 72-Hour Breakpoints

*All five breakpoints are from answers, not exercised. For Moves 2–5, all answers tie at C/E2. The weakest answer was chosen as the one with the largest gap to a 72-hour-viable, tested state.*

- **0–6 hours | Move 1 | Missing artifact (from answers, not exercised):** Communications readiness (Q3) is claimed as D at E0, so there is no named template and no owner. **Why it blocks:** The first holding statement to staff, about 300 customers and any regulator cannot go out on time without a pre-approved template.
- **6–24 hours | Move 2 | Operational infeasibility (from answers, not exercised):** Execute within 72 hours (Q4) is rated "likely" (C) and has never been exercised. **Why it blocks:** With the ERP down, payment files and approvals may depend on ERP data, so the reroute path may fail when first tried.
- **0–6 hours | Move 3 | Missing gate (from answers, not exercised):** The segmentation and shutdown runbook (Q3) is documented but untested. **Why it blocks:** Containment steps with no tested go/no-go gates risk either spreading the infection or making an unnecessarily broad shutdown in the first hours.
- **6–24 hours | Move 4 | Missing alternate (from answers, not exercised):** Qualified alternates (Q2) are rated C, not "viable within 72 hours." **Why it blocks:** A qualified alternate that cannot be activated within the outage window gives no relief during the five-day ERP loss.
- **24–72 hours | Move 5 | Comms approval delay (from answers, not exercised):** The customer obligations and support plan (Q3) is documented, but scripts and the comms workflow are not confirmed ready. **Why it blocks:** Customer-facing commitments on delays or unwind stall while wording and approvals are drafted from scratch.

## 6) Top Blockers and Fixes

1. **No pause communications template (Move 1, Q3)**
   - **Evidence gap:** D claimed at E0; no artifact and no owner.
   - **Minimal fix (2 weeks):** Draft holding statements for staff, customers and regulator, and assign an owner.
   - **Proper fix (6–12 weeks):** Pre-approve the templates with a workflow and exercise them in a drill.
   - **Owner role:** Head of Communications, with the Operations Director.
2. **Stop authority is verbal only (Move 1, Q1)**
   - **Evidence gap:** D claimed at E1; no named matrix.
   - **Minimal fix (2 weeks):** Document a stop authority matrix with primary and backup roles per warehouse.
   - **Proper fix (6–12 weeks):** Exercise the delegated stop in a drill, then log the decision and record a CAPA.
   - **Owner role:** Operations Director.
3. **Safety and continuity checks are verbal only (Move 1, Q2)**
   - **Evidence gap:** D claimed at E1. This is critical for chemical handling while the ERP is down.
   - **Minimal fix (2 weeks):** Document an offline hazmat handling checklist and rollback plan, including paper or offline access to storage and compatibility data.
   - **Proper fix (6–12 weeks):** Test the checklist at one warehouse and add go/no-go criteria.
   - **Owner role:** EHS Manager.
4. **Treasury reroute is unproven within 72 hours (Move 2, Q1 and Q4)**
   - **Evidence gap:** E2 only; no exercise log.
   - **Minimal fix (2 weeks):** Confirm each pre-cleared rail can be operated without ERP outputs, then list the manual dependencies.
   - **Proper fix (6–12 weeks):** Run a reroute exercise with a small test transaction, then log it and record a CAPA.
   - **Owner role:** Treasurer.
5. **Freeze/hold playbook is untested (Move 2, Q2)**
   - **Evidence gap:** E2 only; roles and comms not exercised.
   - **Minimal fix (2 weeks):** Add a role call-tree and a bank notification checklist to the playbook.
   - **Proper fix (6–12 weeks):** Tabletop the playbook alongside the ransomware scenario and record a CAPA.
   - **Owner role:** CFO.
6. **Shutdown and segmentation runbook is untested (Move 3, Q3)**
   - **Evidence gap:** E2 only.
   - **Minimal fix (2 weeks):** Add explicit containment gates and decision owners to the runbook.
   - **Proper fix (6–12 weeks):** Run a technical simulation on a non-production segment, then log it and record a CAPA.
   - **Owner role:** CIO, with the IT Security Lead.
7. **Emergency access logging is untested (Move 3, Q4)**
   - **Evidence gap:** E2 only; no audit trail shown from an exercise.
   - **Minimal fix (2 weeks):** Confirm the break-glass logging is stored outside the ERP and cloud tenant blast radius.
   - **Proper fix (6–12 weeks):** Test a break-glass event end to end and review the audit trail.
   - **Owner role:** IT Security Lead.
8. **ERP failover is untested and alternates are not viable within 72 hours (Move 4, Q2 and Q3)**
   - **Evidence gap:** E2 only.
   - **Minimal fix (2 weeks):** Define a manual or offline order-to-ship fallback for five days, covering orders, picking and dispatch.
   - **Proper fix (6–12 weeks):** Test the fallback at one warehouse with the logistics provider and record a CAPA.
   - **Owner role:** COO.
9. **Substitution rights are summarized but not mapped (Move 4, Q4)**
   - **Evidence gap:** E2 summary only; triggers not mapped to the Tier-1 vendors.
   - **Minimal fix (2 weeks):** List the questions for counsel on substitution rights for the ERP, the bulk suppliers and logistics.
   - **Proper fix (6–12 weeks):** Have counsel-reviewed rights mapped for each Tier-1 vendor, with notice triggers.
   - **Owner role:** Head of Procurement, with General Counsel.
10. **Customer support scripts are not ready (Move 5, Q3)**
    - **Evidence gap:** E2 plan only; no scripts or workflow.
    - **Minimal fix (2 weeks):** Draft customer service scripts for order delays and portal outage.
    - **Proper fix (6–12 weeks):** Set up a script approval workflow and rehearse it with the customer service team.
    - **Owner role:** Head of Customer Service.

## 7) 30/60/90-Day Plan

**Workstream 1: Make Move 1 claims evidential**
- **Outcome:** Stop authority, safety checks and comms reach at least E2, and the Move 1 cap is lifted.
- **Tasks:**
  - By day 30: Document the stop authority matrix with backups.
  - By day 30: Document the offline hazmat checklist and rollback plan.
  - By day 30: Draft holding statement templates.
  - By day 60: Pre-approve the templates and define the workflow.
  - By day 90: Run a pause drill and log the decision and CAPA.
- **Gates:**
  - Every Move 1 answer has a named artifact and owner role.
  - The Move 1 evidence average is 2 or higher.
- **Owner roles:** Operations Director, EHS Manager, Head of Communications.
- **Stop rule:** Pause the workstream if the drill reveals a physical safety gap, and escalate it before continuing.

**Workstream 2: ERP-outage exercise for Moves 2–4**
- **Outcome:** At least one E3 answer each in Moves 2, 3 and 4, making Medium confidence reachable.
- **Tasks:**
  - By day 30: Map ERP dependencies for treasury, containment and order-to-ship.
  - By day 60: Run a tabletop of the five-day outage covering reroute, shutdown and failover.
  - By day 60: Run a technical test of break-glass logging.
  - By day 90: Run a limited live test of the manual order-to-ship fallback at one site.
  - By day 90: Record a CAPA for each failure.
- **Gates:**
  - The exercise is dated, with a log stored in the risk system.
  - A CAPA is opened for each move tested.
- **Owner roles:** CFO, Treasurer, CIO, IT Security Lead, COO.
- **Stop rule:** Halt any live test that risks production payments, customer data or warehouse safety.

**Workstream 3: Customer and exit comms readiness (Move 5)**
- **Outcome:** Customer scripts and an approval workflow are ready, and the exit and unwind path has been rehearsed once.
- **Tasks:**
  - By day 30: Draft customer delay and outage scripts.
  - By day 60: Prepare questions for counsel on termination and unwind triggers.
  - By day 60: Define the approval workflow.
  - By day 90: Run a one-hour exit tabletop with the board.
- **Gates:**
  - The scripts are approved by named roles.
  - The tabletop is logged and has a CAPA.
- **Owner roles:** CEO, Head of Customer Service, General Counsel.
- **Stop rule:** Stop if any comms would require a legal determination, and route it to counsel first.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk Manager)
- Operations Director (stop authority)
- CFO and Treasurer
- CIO and IT Security Lead
- COO
- Head of Communications
- EHS Manager
- Scribe

**Agenda**

| Time | Item |
|---|---|
| 0–5 min | Scenario brief: the ERP is encrypted, day 1 of 5. |
| 5–15 min | 0–6 hour window: what is paused, who authorizes it, safety checks, first holding statement. |
| 15–30 min | 6–24 hour window: treasury rail, containment posture, order-to-ship fallback, sign-offs. |
| 30–40 min | 24–72 hour window: what is executed, monitored and captured; customer comms. |
| 40–45 min | Hot wash and CAPA assignment. |

**Decisions to log**
- Pause decision and its authorizer
- Containment and shutdown scope
- Treasury reroute go or no-go
- Fallback activation
- Holding statement approval

Log each decision with a timestamp and the role that made it.

**Evidence to capture**
- Decision log
- Artifacts referenced (by type and location)
- Time taken to locate each artifact
- Gaps where no artifact existed

**CAPA prompt:** "Which decision took longest or had no artifact? What is the single fix, who owns it, and by when?"

## 9) Escalations

**ESCALATE.** The scenario is a planning exercise, but these triggers apply to it.

- **Criminal:** Ransomware is criminal activity. **Path:** Pre-plan the CEO, General Counsel and CIO decision on law enforcement engagement, with counsel advising on any notification obligations. Counsel should ask whether cyber insurance terms affect notification or response.
- **Sanctions consideration:** Any ransom payment decision could raise sanctions questions about the recipient. This packet makes no sanctions determination. **Path:** General Counsel, with specialist external counsel, before any payment discussion. The board should pre-agree its decision rights on ransom payment.
- **Physical safety:** The company distributes hazardous chemicals while ERP-held handling and storage data may be unavailable. **Path:** The Operations Director and EHS Manager confirm offline safety data access. The CEO is informed if warehouse operations cannot be run safely.

The financial threshold (above USD 10 million) and the people threshold (above 100,000) are not triggered based on the user's estimates of about USD 2 million and about 2,000 people.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are user-reported. Move 1's D answers at E0/E1 illustrate the inflation risk.
- **No document validation:** No artifacts were reviewed, and labels reflect claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Notification, data and contract questions need counsel in the relevant jurisdiction(s).
- **Scenario simplification:** A single five-day ERP outage does not cover concurrent failures, such as the bank, a supplier or the portal failing at the same time.
- **Fast Baseline depth:** Q5–Q7 were not asked, so related artifacts show as Unknown, and no tabletop was run.
- **Exercise recency:** The April 2026 E3 claim was treated as within 12 months of the v1.2.0 reference date. Confirm this against the actual assessment date.
- **Impact estimates:** The impact figures are user estimates and were not validated.
- **Not legal advice:** This packet is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 1, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 1 Safe pause: Score 2, Confidence Low.

## Score

**Verdict: PASS.** The scorecard matches an independent recomputation from the reference pack: Move 1 scores 2 (evidence-average cap) with Low confidence. The Output Packet was produced in turn 1, and turn 2 repeated the same values without change. No fail indicator appears.

---

Final Liability rests with the Human.
