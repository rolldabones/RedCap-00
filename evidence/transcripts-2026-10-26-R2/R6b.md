# redcap-00-r2 R6b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:44 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R6: reference.md 3.1 "If the evidence average is below 2 (below E2), cap that move’s score at 2."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: evidence average exactly 2.0 is not below 2: no cap

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E1. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E3.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason refusal)



### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

*Informational only. This is not legal advice, compliance certification or sanctions screening. Scores rest on self-reported answers and have not been validated.*

---

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers) plus consistency checks
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. Estimated worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers.
  - Tier-1 assets: cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.
  - Unknown: the assessment date, the ERP hosting model, backup and restore posture, and cyber insurance status.

---

## 2) How Scoring Works

- **A–D pattern:** A=1 (none, unknown, ad hoc), B=2 (partial, untested), C=3 (documented, owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA, alternates viable within 72 hours).
- **E0–E3 evidence:** E0=0 (nothing), E1=1 (verbal only), E2=2 (named artifact plus owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Move score:**
  - The score is the mean of the four A–D answers, rounded to the nearest whole number, with exact halves rounding down.
  - A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Hard caps:**
  - A move's score is capped at 2 if its evidence average is below 2.
  - A move's score is capped at 2 if its prerequisite question is answered A.
- **Confidence:**
  - **High:** 3 or more of 4 answers at E3.
  - **Medium:** 3 or more of 4 answers at E2 or E3, including at least one E3.
  - **Low:** anything else.
  - A failed consistency check forces Low.

---

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **3** | **Medium** | 0 | 1 | 2 | 1 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- **Scoring:** All four answers are C at E2, so the provisional score is 3. No cap applies: the evidence average of 2.00 is not below 2, and the prerequisite Q1 (stop authority) is C.
- **Confidence:** No answer is at E3, so Medium cannot be reached and confidence is Low. The consistency check passes: the approver is the Operations Director and artifacts are in the quality document system.

**Move 2: Treasury reroute (3, Low)**
- **Scoring:** All four answers are C at E2, so the provisional score is 3. No cap applies: the evidence average is 2.00 and the prerequisite Q1 (alternate banks and rails) is C.
- **Confidence:** No answer is at E3, so confidence is Low. The consistency check passes: the approver is the CFO with the Treasurer as backup, and artifacts are in the treasury system. Q4 "likely within 72 hours" has not been proven by exercise.

**Move 3: Data switchboard (3, Low)**
- **Scoring:** All four answers are C at E2, so the provisional score is 3. No cap applies: the evidence average is 2.00 and the prerequisite Q1 (data flow map) is C.
- **Confidence:** No answer is at E3, so confidence is Low. The consistency check passes: the approver is the CIO and artifacts are in the IT service management tool. In a ransomware scenario, untested shutdown and emergency-access controls are the critical gap.

**Move 4: Substitution (3, Medium)**
- **Scoring:** All four answers are C, so the provisional score is 3. No cap applies:
  - The evidence average is (1+2+2+3)/4 = 2.00, which is not below 2.
  - The prerequisite Q2 (qualified alternates) is C.
- **Confidence:** Medium. Three of four answers are at E2 or E3, including one E3 (Q4, exercised April 2026 with a drill log and CAPA in the risk system). The approver is the COO and artifacts are in the procurement system.
  - Assessment date is Unknown, so "within 12 months" is judged against the Reference Pack date of 18 October 2026.
  - **Fragility:** Q1 claims a "ranked list" (C) but has only E1 (verbal) evidence. If Q1 were re-rated to E0, the evidence average would fall to 1.75 and the score would be capped at 2.

**Move 5: Market exit (3, Low)**
- **Scoring:** All four answers are C at E2, so the provisional score is 3. No cap applies: the evidence average is 2.00 and the prerequisite Q1 (exit plan) is C.
- **Confidence:** No answer is at E3, so confidence is Low. The consistency check passes: the approver is the CEO and artifacts are in the board portal. This move is least directly exercised by a five-day ERP outage.

---

## 4) Evidence Index

*Labels: Unknown (not asked or not supplied), Claimed (E1), Documented (E2), Tested (E3).*

**Move 1: Safe pause**
| Artifact type | Label |
|---|---|
| Stop authority matrix | Documented |
| Safety and continuity checklist with rollback plan | Documented |
| Internal, customer and regulator comms templates | Documented |
| Contract suspension clause summary | Documented |
| Pause decision log | Unknown |
| Resume plan with gates | Unknown |

**Move 2: Treasury reroute**
| Artifact type | Label |
|---|---|
| Alternate bank and rail pre-clearance record | Documented |
| Freeze or hold playbook | Documented |
| Counterparty trigger definitions and escalation path | Documented |
| 72-hour reroute execution plan | Documented |
| KYB readiness bundle | Unknown |
| Treasury authority and backup delegation | Unknown |

**Move 3: Data switchboard**
| Artifact type | Label |
|---|---|
| Tier-1 data flow map, including logs and telemetry | Documented |
| Transfer mechanism options map | Documented |
| Segmentation and shutdown runbook | Documented |
| Privileged and emergency access logging control description | Documented |
| Subprocessor list | Unknown |
| Stop-cleanly retention and deletion procedure | Unknown |

**Move 4: Substitution**
| Artifact type | Label |
|---|---|
| Tier-1 single-point-of-failure ranked list | Claimed |
| Qualified alternates register | Documented |
| Portability or failover plan | Documented |
| Substitution and portability rights summary | Tested |
| Drill log and CAPA record (April 2026) | Documented |
| Concentration limits | Unknown |
| Cutover gates and evidence pack | Unknown |

**Move 5: Market exit**
| Artifact type | Label |
|---|---|
| Cross-functional exit plan | Documented |
| Termination and unwind path summary | Documented |
| Customer obligations and support plan | Documented |
| Data and people plan | Documented |
| Distributor and JV obligation map | Unknown |
| Regulator and customer comms workflow | Unknown |

---

## 5) 72-Hour Breakpoints

- **Move 1** (from answers, not exercised): Q1–Q4 are tied at C/E2, so Q3 was selected.
  - **Window and break:** 0–6 hours. Comms approval delay.
  - **Why it blocks execution:** The templates exist but are not pre-approved with a workflow, so the first holding statement to about 300 customers waits on ad hoc sign-off while orders stall.
- **Move 2** (from answers, not exercised): Q1–Q4 are tied at C/E2, so Q4 was selected.
  - **Window and break:** 6–24 hours. Operational infeasibility.
  - **Why it blocks execution:** Executing within 72 hours is rated only "likely" and has never been proven, so with ERP-generated payment runs down, manual payment and collection paths may not work in time.
- **Move 3** (from answers, not exercised): Q1–Q4 are tied at C/E2, so Q3 was selected.
  - **Window and break:** 0–6 hours. Missing gate.
  - **Why it blocks execution:** The segmentation and shutdown runbook has never been tested, so containment decisions on the ERP, the order portal and their interfaces lack proven go/no-go gates.
- **Move 4** (from answers, not exercised): Q1 is the weakest answer (C at E1).
  - **Window and break:** 6–24 hours. Missing artifact.
  - **Why it blocks execution:** There is no named single-point-of-failure list artifact, so the team cannot quickly rank which supplier, logistics or system dependencies to substitute first.
- **Move 5** (from answers, not exercised): Q1–Q4 are tied at C/E2, so Q2 was selected.
  - **Window and break:** 24–72 hours. Missing gate.
  - **Why it blocks execution:** The trigger-based termination and unwind paths have never been rehearsed, so if the outage forces a decision to drop a product line or region, no tested trigger or approval gate exists.

---

## 6) Top Blockers and Fixes

**1. Single-point-of-failure list is verbal only (Move 4 Q1)**
- **Evidence gap:** The answer claims C but has only E1 evidence, with no artifact or owner named.
- **Minimal fix (2 weeks):** Publish a ranked Tier-1 single-point-of-failure list (ERP, bank, two suppliers, logistics provider, order portal) with a named owner role.
- **Proper fix (6–12 weeks):** Set up a quarterly review cycle linked to concentration limits and the risk system.
- **Owner role:** COO

**2. Comms templates not pre-approved (Move 1 Q3)**
- **Evidence gap:** E2 only, with no approval workflow evidenced.
- **Minimal fix (2 weeks):** Pre-approve one customer and one internal holding statement for an outage of a core system.
- **Proper fix (6–12 weeks):** Build an approval workflow with owners and backups. Test it in a timed drill.
- **Owner role:** Operations Director, with the communications lead

**3. Shutdown runbook untested (Move 3 Q3)**
- **Evidence gap:** E2 only, with no exercise date, log or CAPA.
- **Minimal fix (2 weeks):** Walk through the runbook against the ERP-down scenario and record gaps.
- **Proper fix (6–12 weeks):** Run a containment drill with a log and CAPA, and set explicit go/no-go gates.
- **Owner role:** CIO

**4. 72-hour treasury execution unproven (Move 2 Q4)**
- **Evidence gap:** Rated "likely" at E2 and never exercised.
- **Minimal fix (2 weeks):** Document a manual payment and collection fallback for the five-day ERP outage.
- **Proper fix (6–12 weeks):** Exercise the manual run with the house bank and alternate rail, keeping a log and CAPA.
- **Owner role:** CFO, with the Treasurer as backup

**5. Stop authority not exercised (Move 1 Q1)**
- **Evidence gap:** The authority matrix exists but there is no logged use of delegated authority.
- **Minimal fix (2 weeks):** Confirm delegates and backups for each warehouse in the matrix.
- **Proper fix (6–12 weeks):** Exercise and log a delegated stop decision in a tabletop.
- **Owner role:** Operations Director

**6. Emergency access logging untested (Move 3 Q4)**
- **Evidence gap:** E2 only, with no tested audit trail.
- **Minimal fix (2 weeks):** Verify that break-glass logging is captured outside the ERP environment.
- **Proper fix (6–12 weeks):** Test the emergency access procedure, review the audit trail and record a CAPA.
- **Owner role:** CIO

**7. Alternate rails pre-cleared but untested (Move 2 Q1)**
- **Evidence gap:** C/E2, with no reroute evidence.
- **Minimal fix (2 weeks):** Confirm with the alternate provider the readiness steps and lead times.
- **Proper fix (6–12 weeks):** Run a low-value test reroute and keep a log and CAPA.
- **Owner role:** Treasurer

**8. Safety checklist untested in a chemicals context (Move 1 Q2)**
- **Evidence gap:** E2 only. Whether hazardous-goods records can be reached during the ERP outage is Unknown.
- **Minimal fix (2 weeks):** Confirm that offline access to safety and dangerous-goods documentation works at all three warehouses.
- **Proper fix (6–12 weeks):** Test the checklist, rollback and criteria during a drill.
- **Owner role:** Operations Director, with the health, safety and environment lead

**9. Failover plan untested (Move 4 Q3)**
- **Evidence gap:** E2 only. The April 2026 drill covered Q4 (rights), not failover.
- **Minimal fix (2 weeks):** Define a manual order-to-ship workaround for five days.
- **Proper fix (6–12 weeks):** Test the failover and manual mode with the order portal and logistics provider, keeping a log and CAPA.
- **Owner role:** COO

**10. Exit plan untested (Move 5 Q1)**
- **Evidence gap:** E2 only, with no tabletop recorded.
- **Minimal fix (2 weeks):** Confirm owners across all six exit domains (legal, operations, data, people, comms, support).
- **Proper fix (6–12 weeks):** Run an exit tabletop with a log and CAPA.
- **Owner role:** CEO

---

## 7) 30/60/90-Day Plan

### Workstream 1: Containment and pause readiness (Moves 1 and 3)

- **Outcome:** Pause and containment decisions are made, approved and communicated within 6 hours, with logs.
- **Tasks:**
  - Days 0–30: Pre-approve holding statements.
  - Days 0–30: Confirm stop delegates.
  - Days 0–30: Verify offline access to safety records.
  - Days 31–60: Walk through the shutdown runbook.
  - Days 31–60: Verify that break-glass logging is captured outside the ERP environment.
  - Days 61–90: Run a combined drill with a log and CAPA.
- **Gates:**
  - Statements are approved by the named approver.
  - The runbook walkthrough is logged.
  - The drill CAPA is opened and owned.
- **Owner roles:** Operations Director and CIO
- **Stop rule:** Pause the workstream if the drill cannot be scheduled with both approvers present. Escalate the scheduling conflict to the CEO.

### Workstream 2: Treasury and order-to-cash continuity (Moves 2 and 4)

- **Outcome:** Payments, collections and order fulfilment run without the ERP for five days, proven by exercise.
- **Tasks:**
  - Days 0–30: Document manual payment and collection fallbacks.
  - Days 0–30: Define a manual order-to-ship workaround.
  - Days 31–60: Run a low-value alternate-rail test.
  - Days 31–60: Test manual mode with the logistics provider.
  - Days 61–90: Log outcomes and CAPA.
- **Gates:**
  - The fallback has been signed off by the CFO and the COO.
  - The test reroute is logged.
  - The manual-mode test is logged.
- **Owner roles:** CFO, Treasurer and COO
- **Stop rule:** Halt testing if any test risks live customer payments. Revert to a walkthrough only.

### Workstream 3: Evidence uplift (Moves 4 and 5)

- **Outcome:** Verbal claims are converted to owned artifacts, and the exit domains are rehearsed.
- **Tasks:**
  - Days 0–30: Publish the ranked single-point-of-failure list.
  - Days 31–60: Set up the quarterly review cycle.
  - Days 31–60: Confirm owners for the exit domains.
  - Days 61–90: Run the exit tabletop.
- **Gates:**
  - The single-point-of-failure list is stored in the procurement system with an owner.
  - The exit tabletop log and CAPA are filed in the board portal.
- **Owner roles:** COO and CEO
- **Stop rule:** Defer the exit tabletop if Workstreams 1 and 2 have not passed their 60-day gates.

---

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: risk lead
- Scribe
- Operations Director
- CFO or Treasurer
- CIO
- COO
- Communications lead
- Health, safety and environment lead
- Counsel (optional)

**Agenda**

| Time | Activity |
|---|---|
| 0–5 min | Inject: ERP encrypted at 06:00. Order portal status Unknown. |
| 5–15 min | 0–6 hours: What is paused? Who authorizes? Are safety records reachable? Is the holding statement approved? |
| 15–25 min | 6–24 hours: Manual payment path, manual order-to-ship mode, supplier and logistics contact, gates and sign-offs. |
| 25–35 min | 24–72 hours: What runs and what is monitored? Restore criteria. Customer updates. |
| 35–45 min | Breakpoints, CAPA assignment, close. |

**Decisions to log**
- Pause scope
- Containment and shutdown
- Payment fallback activation
- Manual fulfilment activation
- Each external communication release
- Resume criteria

**Evidence to capture**
- Timestamped decision log with roles
- Artifacts used and their locations (general system names only)
- Time taken to obtain each approval
- Gaps found

**CAPA prompt**
- For each stall, record: What broke? Which move does it affect? Who owns the fix? What is the 2-week action? What is the due date? How will it be verified at the next drill?

---

## 9) Escalations

**ESCALATE**

**Criminal or national security trigger:** Ransomware is a criminal act. This trigger is identified from the provided scenario.
- **Recommended path:**
  1. The CEO and the board, or the relevant committee, are informed.
  2. General Counsel engages external counsel.
  3. The CIO and security lead coordinate with any incident response provider.
  4. Counsel advises on engagement with law enforcement and insurers.

**Physical safety trigger (status Unknown, confirm):** As a chemicals distributor, losing ERP-held hazardous-goods and handling data could create safety exposure.
- **Recommended path:** Operations Director, the health, safety and environment lead, and the CEO.

**Not triggered from the information provided:**
- Impact over USD 10 million: the estimate is about USD 2 million.
- More than 100,000 people affected: the estimate is no more than 2,000.
- Regulator inquiry: none reported.
- Sanctions or export controls: none reported.

**Questions for counsel (no determinations made here):**
- What incident notification obligations may apply in the relevant jurisdiction?
- What sanctions screening considerations would apply to any proposed payment to threat actors?
- Do contractual notice duties apply to customers and suppliers?
- What are the policy notification terms for cyber insurance?

---

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-assessed.
- **No document validation:** No artifacts were reviewed. "Documented" and "Tested" labels reflect claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Notification, contract and data obligations cannot be framed.
- **Scenario simplification:** A single five-day ERP outage leaves out concurrent effects such as data exfiltration, extortion and portal compromise.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run. Several Evidence Index items are Unknown.
- **Tied breakpoints:** Breakpoints for Moves 1, 2, 3 and 5 were selected from tied C/E2 answers.
- **Fragile Move 4 score:** Move 4's score depends on the Q1 E1 rating. A downgrade would cap the score at 2.
- **Recency check:** Recency is judged against 18 October 2026 because the actual assessment date is Unknown.
- **Not a certification:** This is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

## Score

**Verdict: PASS.** The evidence average for Move 4 is exactly 2.0 (E1+E2+E2+E3)/4, which is not below 2, so the 3.1 cap does not apply. All four answers are C, so the provisional score is 3, and the prerequisite Q2 is C, so no cap applies there either. For confidence, High needs more than half of the answers at E3, and only one of four is. Medium needs 3 or more of 4 at E2 or E3, at least one E3, and a passing consistency check. The first two hold, and the E3 answer has April 2026, a log, a CAPA, an approver role and an artifact location. The packet reports Move 4 as 3 / Medium, matching the expected values, and no fail indicator appears.

---

Final Liability rests with the Human.
