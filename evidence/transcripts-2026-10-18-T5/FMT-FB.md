# redcap-00 FMT-FB

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:44 KST · **max_tokens:** 16000

**Rule:** tests.md section 1, format compliance checks, Fast Baseline (and R4: "5 breakpoints in Fast Baseline, 10 in Deepening"); input is the fictional user input published in example.md

**Pass condition:** The final Output Packet produced in the session meets every check in tests.md section 1 for Fast Baseline: (F1) exactly 10 sections with the exact headings of reference.md section 9 in order (Snapshot; How Scoring Works; Scorecard; Evidence Index; 72-Hour Breakpoints; Top Blockers and Fixes; 30/60/90-Day Plan; Minimal Drill Script (45 minutes); Escalations; Known Limits + Version); (F2) section 2 has 5 bullets or fewer; (F3) section 5 has exactly 5 bullets, one per move, each marked “from answers, not exercised”; (F4) section 6 has exactly 10 numbered items; (F5) section 10 ends with the exact footer string `RedCap-00 v1.2.0 | Evidence-capped scoring`.

## Transcript

### Turn 1, user

**Safety confirmation:** Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

**Intake.** Industry: marine hardware manufacturing (Kestrel Marine Fittings, a fictional company). Footprint: two plants, one in South Korea and one in Vietnam; sales to about 600 business customers in 14 countries. Model: B2B, made to order, about 1,100 staff. Tier-1: cloud-hosted ERP, house bank, one forging supplier, the main export port and freight forwarder, the customer order portal. Scenario: our cloud provider's primary region is down for seven days while the main export port is closed. Worst-case impact we estimate at about USD 4 million. Jurisdiction: not given.

**Fast Baseline answers.**

Move 1 Safe pause. Q1 Stop authority: C, E2 (authority matrix in the quality system, owner Plant Director). Q2 Safety and continuity checks: C, E2 (pause checklist with rollback plan, owner Plant Director). Q3 Communications: B, E1 (we draft as we go). Q4 Contractual suspension basis: B, E1 (legal looks case by case).

Move 2 Treasury reroute. Q1 Alternate banks and rails: B, E1 (a second bank is identified; no account opened). Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: D, E3 (March 2026 drill rerouted a supplier payment run through the house bank's secondary rail in 30 hours).

Move 3 Data switchboard. Q1 Tier-1 data flow map: A, E0. Q2 Transfer mechanism options: B, E1. Q3 Segmentation and shutdown runbook: C, E2 (runbook, owner IT Operations Lead). Q4 Privileged and emergency access logging: C, E2 (procedure, owner Information Security Manager).

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2 (ranked list, owner COO). Q2 Qualified alternates: C, E2 (second forging supplier qualified in 2025). Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: D, E3.

Move 5 Market exit. Q1 Exit plan: A, E0. Q2 Termination and unwind paths: A, E0. Q3 Customer obligations and support plan: A, E0. Q4 Data and people plan: B, E1.

**Consistency checks.** Move 1: approver Plant Director; artifacts in the quality document system; no E3 claims. Move 2: last exercise March 2026, drill log and a CAPA (open an account at the second bank) in the treasury system; approver CFO, Treasurer as backup. Move 3: approver CIO; artifacts in the IT service management tool. Move 4: approver COO; artifacts in the procurement system; for the Q4 E3 claim, legal reviewed the rights at some point, we do not know when, and there is no log or follow-up action. Move 5: no approver named; nothing documented.

### Turn 1, assistant (stop_reason end_turn)

Deepening mode (Q5–Q7 for each move plus the mini tabletop) is available if you want it. This packet reflects **Fast Baseline** only. It is informational only. It is not advice from counsel, not a certification and not sanctions screening.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline. Five moves, Q1–Q4 each, 20 answers, consistency checks recorded.
- **Scenario tested:** The cloud provider's primary region is down for 7 days while the main export port is closed. You estimate worst-case impact at about USD 4 million.
- **Tier-1 scope summary:** Kestrel Marine Fittings (fictional) makes B2B made-to-order marine hardware. It has about 1,100 staff, two plants (South Korea, Vietnam) and about 600 business customers in 14 countries. Tier-1 dependencies are:
  - cloud-hosted ERP
  - house bank
  - single forging supplier
  - main export port and freight forwarder
  - customer order portal

## 2) How Scoring Works

- **A–D answers** score A=1 (none, unknown, ad hoc), B=2 (partial, informal, untested), C=3 (documented, owned, little or no recent testing) and D=4 (tested in the last 12 months with logs and CAPA, alternates viable within 72 hours).
- **Evidence levels** score E0=0 (none), E1=1 (verbal), E2=2 (artifact type plus owner role) and E3=3 (tested, with month/year, log and CAPA).
- **Move score** is the mean of the A–D scores, rounded, with exact halves rounded down. A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Caps:**
  - If the move's evidence average is below 2, the score is capped at 2.
  - If the move's prerequisite question is answered A, the score is capped at 2.
- **Confidence levels:**
  - **High:** 3 or more E3 answers and the consistency check passes.
  - **Medium:** 3 or more answers at E2/E3, at least one E3, and the consistency check passes.
  - **Low:** everything else. A failed consistency check always forces Low.

## 3) Scorecard

**Move 1 Safe pause: Score 2 | Confidence Low | Evidence: E0 0, E1 2, E2 2, E3 0**
- The mean of 2.5 rounds down to 2. The evidence average of 1.5 is below 2, so the cap is also 2. Stop authority and the pause checklist with rollback plan are documented and owned by the Plant Director.
- Communications and the suspension basis are handled verbally and case by case. The consistency check passes (approver and artifact location named), but there are no E3 answers, so confidence is Low.

**Move 2 Treasury reroute: Score 3 | Confidence High | Evidence: E0 0, E1 1, E2 0, E3 3**
- The mean of 3.5 rounds down to 3. The evidence average is 2.5 and Q1 is B, so no cap applies. The March 2026 drill rerouted a supplier payment run in 30 hours, and a log and CAPA are held in the treasury system. The CFO approves, with the Treasurer as backup.
- The proven path runs through the house bank's own secondary rail. The second bank is identified only, with no account opened, so the CAPA is still open and the house-bank dependency remains.

**Move 3 Data switchboard: Score 2 | Confidence Low | Evidence: E0 1, E1 1, E2 2, E3 0**
- The mean of 2.25 rounds to 2. Two caps independently hold the score at 2: the evidence average of 1.25, and the prerequisite cap (Q1 Tier-1 data flow map answered A).
- The shutdown runbook (IT Operations Lead) and the access logging procedure (Information Security Manager) are documented. With the ERP and order portal hosted in the failed region, the missing data flow map is the central gap. There are no E3 answers, so confidence is Low.

**Move 4 Substitution: Score 3 | Confidence Low | Evidence: E0 0, E1 0, E2 3, E3 1**
- The mean of 3.25 rounds to 3. The evidence average is 2.25 and Q2 is C, so no cap applies. The ranked single-points-of-failure list, the qualified second forging supplier and the failover plan are held in the procurement system. The COO approves.
- The consistency check **fails**: the Q4 E3 claim has no month/year, no log and no CAPA, so confidence is Low. Reclassifying Q4 to E2 would not change the score, because the evidence average would be 2.0, which is not below 2.

**Move 5 Market exit: Score 0, Unknown/Insufficient data | Confidence Low | Evidence: E0 3, E1 1, E2 0, E3 0**
- The zero rule applies: 3 of the 4 answers are A at E0 (exit plan, unwind paths, customer support plan).
- No approver role is named. The only partial input is a verbal data and people plan (Q4: B, E1).

## 4) Evidence Index

Labels: Unknown = no evidence, Claimed = verbal only, Documented = artifact plus owner role, Tested = exercised with log and CAPA.

**Move 1 Safe pause**
| Artifact type | Label |
|---|---|
| Stop authority matrix | Documented |
| Pause checklist with rollback plan | Documented |
| Internal, customer and regulator comms templates | Claimed |
| Contractual suspension clause summary | Claimed |
| Pause decision log | Unknown |
| Resume plan | Unknown |
| Conflict escalation path | Unknown |

**Move 2 Treasury reroute**
| Artifact type | Label |
|---|---|
| Alternate bank/rail pre-clearance record | Claimed |
| Freeze or hold playbook | Tested |
| Counterparty tripwire definitions and escalation | Tested |
| Reroute drill log and CAPA (March 2026) | Tested |
| KYC/KYB bundle | Unknown |
| Alternate settlement or letter of credit playbook | Unknown |
| Treasury delegation and backup record | Unknown |

**Move 3 Data switchboard**
| Artifact type | Label |
|---|---|
| Tier-1 data flow map (including logs and telemetry) | Unknown |
| Transfer mechanism options map | Claimed |
| Segmentation and shutdown runbook | Documented |
| Privileged and emergency access logging procedure | Documented |
| Subprocessor list | Unknown |
| OT and critical access boundary procedure | Unknown |
| Stop-cleanly retention and deletion procedure | Unknown |

**Move 4 Substitution**
| Artifact type | Label |
|---|---|
| Ranked single-points-of-failure list | Documented |
| Alternate supplier qualification record | Documented |
| Portability and failover plan | Documented |
| Substitution and portability rights summary | Documented (Tested claim not substantiated) |
| Concentration limits | Unknown |
| Logistics reroute plan | Unknown |
| Cutover gate checklist | Unknown |

**Move 5 Market exit**
| Artifact type | Label |
|---|---|
| Cross-functional exit plan | Unknown |
| Termination and unwind path summary | Unknown |
| Customer obligations and support plan | Unknown |
| Data and people plan | Claimed |
| Distributor or JV obligations map | Unknown |
| Asset and IP handling procedure | Unknown |
| Regulator and customer comms workflow | Unknown |

## 5) 72-Hour Breakpoints

- **0–6 hours | Move 1 | Comms approval delay** (from answers, not exercised): The first holding statement is drafted from scratch (Q3: B, E1). Customers in 14 countries get no pause notice until text is written and approved during the outage.
- **6–24 hours | Move 2 | Missing alternate** (from answers, not exercised): The second bank has no account opened (Q1: B, E1). If the house bank or its secondary rail is impaired, there is no viable alternate path within 72 hours.
- **6–24 hours | Move 3 | Missing artifact** (from answers, not exercised): There is no Tier-1 data flow map (Q1: A, E0). The CIO cannot choose a data posture for the ERP and order portal without knowing which data, logs and integrations depend on the failed region.
- **6–24 hours | Move 4 | Missing alternate** (from answers, not exercised): The second forging supplier is qualified but not confirmed viable within 72 hours (Q2: C, E2). Its capacity, lead time and shipping route may not avoid the closed export port in time.
- **24–72 hours | Move 5 | Missing artifact (and missing authority)** (from answers, not exercised): There is no exit plan and no approver role (Q1: A, E0). If disruption extends beyond the scenario, there is no defined path or decision-maker for withdrawing from a market or lane.

## 6) Top Blockers and Fixes

1. **No Tier-1 data flow map (Move 3, Q1)**
   - Evidence gap: E0. This answer triggers the prerequisite cap.
   - Minimal fix (2 weeks): One-page map covering the ERP, order portal and their integrations, logs and telemetry, with the hosting region marked.
   - Proper fix (6–12 weeks): Full Tier-1 map, reviewed and versioned, linked to the shutdown runbook.
   - Owner role: CIO, with the IT Operations Lead.

2. **No exit plan and no approver (Move 5, Q1)**
   - Evidence gap: E0. No approver role is named.
   - Minimal fix (2 weeks): Name the exit approver role. Draft an exit plan skeleton covering ops, data, people, comms and support.
   - Proper fix (6–12 weeks): Documented exit plan, owned and tabletop-tested.
   - Owner role: CEO-designated executive sponsor (to be named).

3. **Termination and unwind paths unknown (Move 5, Q2)**
   - Evidence gap: E0.
   - Minimal fix (2 weeks): List Tier-1 customer, distributor and supplier relationships with high-level termination triggers.
   - Proper fix (6–12 weeks): Counsel-reviewed unwind summary.
   - Questions for counsel: Which termination triggers and notice periods apply per country? Which obligations survive exit?
   - Owner role: General Counsel.

4. **Customer obligations and support plan unknown (Move 5, Q3)**
   - Evidence gap: E0.
   - Minimal fix (2 weeks): Inventory open orders, warranty and support commitments for the top customers.
   - Proper fix (6–12 weeks): Documented support plan with scripts and a comms workflow.
   - Owner role: Head of Sales / Customer Service.

5. **Data and people plan partial (Move 5, Q4)**
   - Evidence gap: E1, verbal only.
   - Minimal fix (2 weeks): Write down the current understanding with a named owner role.
   - Proper fix (6–12 weeks): Documented plan with rehearsed responsibilities and steps.
   - Owner role: HR Director with the CIO.

6. **Second bank has no account; CAPA still open (Move 2, Q1)**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): Set a CAPA due date and start onboarding with the second bank.
   - Proper fix (6–12 weeks): Account pre-cleared, then a test reroute through the second bank, logged.
   - Owner role: Treasurer, approved by the CFO.

7. **Pause communications drafted as you go (Move 1, Q3)**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): Holding statement templates for internal, customer and regulator audiences covering both outage and port closure.
   - Proper fix (6–12 weeks): Pre-approved templates with workflow, owners and translations for the 14 countries.
   - Owner role: Communications Lead with the Plant Director.

8. **Contractual suspension basis handled case by case (Move 1, Q4)**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): Short summary of suspension and delay provisions for top Tier-1 contracts.
   - Proper fix (6–12 weeks): Provisions mapped to Tier-1 contracts with triggers and notice steps.
   - Questions for counsel: What notice is expected for delays caused by a port closure or provider outage, and on what timeline?
   - Owner role: General Counsel.

9. **Transfer mechanism options handled case by case (Move 3, Q2)**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): List candidate failover regions and the data categories that would move.
   - Proper fix (6–12 weeks): Options mapped per data category and reviewed by counsel. This involves no determinations by this tool.
   - Questions for counsel: Which options require review before data moves between regions or countries?
   - Owner role: CIO with General Counsel.

10. **Substitution rights "tested" claim unsubstantiated (Move 4, Q4)**
    - Evidence gap: No month/year, log or CAPA, so the consistency check fails.
    - Minimal fix (2 weeks): Treat the claim as Documented. Record the date of the last review, and open a CAPA to re-review the rights.
    - Proper fix (6–12 weeks): Exercise substitution rights in a tabletop with a log and CAPA, alongside the untested failover plan (Q3).
    - Owner role: COO with General Counsel.

## 7) 30/60/90-Day Plan

**Workstream A: Cloud outage data switchboard (Moves 3 and 1)**
- **Outcome:** Within 6–24 hours of a region outage, the CIO can choose a data posture for the ERP and order portal using documented artifacts.
- **Tasks:**
  - Day 30: Tier-1 data flow map draft.
  - Day 30: Holding statement templates.
  - Day 60: Transfer options mapped and questions sent to counsel.
  - Day 60: Runbook linked to the map.
  - Day 90: Tabletop with the shutdown runbook, logged, with a CAPA opened.
- **Gates:**
  - Map reviewed by the CIO.
  - Counsel responses received.
  - Exercise log and CAPA filed in the IT service management tool.
- **Owner roles:** CIO, IT Operations Lead, Information Security Manager, Communications Lead.
- **Stop rule:** If the map is not approved by day 45, pause the remaining tasks and escalate to the executive team.

**Workstream B: Exit readiness from zero (Move 5)**
- **Outcome:** Move 5 leaves Unknown status, with a named approver and documented core artifacts.
- **Tasks:**
  - Day 30: Name the approver role.
  - Day 30: Exit plan skeleton.
  - Day 60: Unwind summary.
  - Day 60: Customer support plan.
  - Day 90: Documented data and people plan.
  - Day 90: Exit tabletop.
- **Gates:**
  - Approver role recorded.
  - At least 3 of 4 Fast Baseline artifacts reach Documented.
- **Owner roles:** Executive sponsor (to be named), General Counsel, Head of Sales / Customer Service, HR Director.
- **Stop rule:** If no approver role is named by day 30, stop and escalate to the CEO.

**Workstream C: Evidence hardening for treasury and substitution (Moves 2 and 4)**
- **Outcome:** Alternates that are tested and viable within 72 hours, with clean E3 records.
- **Tasks:**
  - Day 30: Second-bank onboarding started.
  - Day 30: Substitution rights review dated and logged.
  - Day 60: Second forging supplier confirmed for 72-hour viability, including a shipping route that avoids the main port.
  - Day 90: Test reroute through the second bank.
  - Day 90: Failover tabletop.
- **Gates:**
  - Second-bank account pre-cleared.
  - Drill logs and CAPAs filed in the treasury and procurement systems.
- **Owner roles:** CFO, Treasurer, COO, General Counsel.
- **Stop rule:** If second-bank onboarding stalls beyond 60 days, escalate to the CFO for an alternative-provider decision.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Scribe
- Plant Directors (both plants)
- CFO and Treasurer
- CIO and IT Operations Lead
- Information Security Manager
- COO
- General Counsel
- Communications Lead
- Head of Sales / Customer Service

**Agenda**
- **0–5 min:** Scenario brief. The cloud primary region is down (ERP and portal unavailable) and the main export port is closed for 7 days.
- **5–15 min:** First 0–6 hours. Decide what to pause, who authorizes it, and what the first holding statement says.
- **15–28 min:** 6–24 hours. Choose the switch paths: data posture, forging supplier, payment rail and shipping route.
- **28–40 min:** 24–72 hours. Decide what is executed and monitored, and whether exit questions arise.
- **40–45 min:** Hot wash and CAPA assignment.

**Decisions to log**
- Pause scope and approver
- Holding statement approval time
- Data posture choice
- Supplier and shipping route switch
- Payment rail choice
- Any exit trigger discussion

**Evidence to capture**
- Timestamped decision log
- Artifacts actually opened (or found missing)
- Approver names by role
- Elapsed time per decision
- Participant list by role

**CAPA prompt**
For each stall, record: what blocked, which artifact or authority was missing, the fix owner role, and the due date. File the record in the relevant system so the move's next E3 claim has a month/year, a log and a CAPA.

## 9) Escalations

No escalation triggers identified from provided information.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are as you reported them.
- **No document validation:** No artifact was reviewed. The labels reflect your descriptions only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Korea, Vietnam and 14 customer countries may impose different requirements, so confirm with counsel.
- **Scenario simplification:** Two concurrent disruptions were assessed from answers only. No tabletop was run.
- **Fast Baseline coverage:** Q5–Q7 for each move were not asked. Logistics reroute, concentration limits and the KYC/KYB bundle remain unassessed.
- **Time-sensitive E3 status:** Move 2's E3 status relies on the March 2026 drill and lapses 12 months after it unless the drill is repeated.
- **Treasury evidence scope:** One drill was used as the exercise record for all three of Move 2's E3 answers.
- **Escalation thresholds:** The impact estimate (about USD 4 million) and the number of people affected are below the escalation thresholds. Re-check if the estimate grows beyond USD 10 million.
- **Not assessed:** Export controls or sanctions exposure for products, markets or counterparties. If relevant, raise it with counsel.
- **Scores are planning indicators only:** They are not certifications or determinations of any kind.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 2, assistant (stop_reason end_turn)

Packet complete.

## Score

**Verdict: FAIL.** F1, F3, F4 and F5 are met, and none of the listed fail indicators appear. F2 fails on a strict count: section 2 has 10 bullet items, 5 top-level plus 5 nested, against the cap of 5. Partial compliance is a FAIL, so the case fails. This rests on counting nested bullets, and a scorer who counts only top-level bullets would pass it.

---

Final Liability rests with the Human.
