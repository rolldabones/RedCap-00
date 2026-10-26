# redcap-00-r1 FMT-FB

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:34 KST · **max_tokens:** 16000

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

Fast Baseline packet below. Deepening (Q5–Q7 for each move plus the 72-hour mini tabletop) is available if you want it. It would produce 10 tabletop-derived breakpoints and fill the Unknown items in the Evidence Index.

---

## 1) Snapshot

- **Jurisdiction:** Unknown. Footprint is plants in South Korea and Vietnam, with sales into 14 countries. No governing jurisdiction was supplied.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks).
- **Scenario tested:** The cloud provider's primary region is down for 7 days while the main export port is closed. The organisation's own worst-case estimate is about USD 4m.
- **Tier-1 scope summary:**
  - Cloud-hosted ERP
  - Customer order portal
  - House bank
  - Single forging supplier
  - Main export port and freight forwarder
  - Two plants (South Korea, Vietnam), about 1,100 staff, about 600 B2B customers, made-to-order.

## 2) How Scoring Works

- **Answers (A–D):** Each answer scores A=1 (none or unknown) up to D=4 (tested in the last 12 months with logs and CAPA). The move score is the mean, rounded, and exact halves round down.
- **Evidence (E0–E3):** E0 means no evidence and scores 0. E1 means verbal only and scores 1. E2 means a named artifact with an owner role and scores 2. E3 means tested in the last 12 months with a log and a CAPA, and scores 3.
- **Caps:**
  - A move with an evidence average below 2 is capped at 2.
  - A move whose prerequisite question is answered A is capped at 2.
  - The final score is the lowest of the provisional score and any cap.
- **Zero rule:** If 3 or more of a move's 4 answers are A at E0, the move scores 0 and is reported as Unknown/Insufficient data.
- **Confidence:**
  - High needs more than half of answers at E3 and a passed consistency check.
  - Medium needs more than half at E2/E3, at least one E3, and a passed check.
  - Otherwise confidence is Low. A failed consistency check forces Low.

## 3) Scorecard

**Move 1: Safe pause. Score 2 | Confidence Low | E0:0 E1:2 E2:2 E3:0**
- Answers C, C, B, B give a mean of 2.5, which rounds down to 2. The evidence average is 1.5, so the cap of 2 applies. Q1 is C, so there is no prerequisite cap.
- Stop authority and the pause checklist are documented and owned by the Plant Director. Communications and the suspension basis are improvised, and there is no E3, so confidence is Low. The consistency check passed.

**Move 2: Treasury reroute. Score 3 | Confidence High | E0:0 E1:1 E2:0 E3:3**
- Answers B, D, D, D give a mean of 3.5, which rounds down to 3. The evidence average is 2.5, so there is no cap. Q1 is B, so there is no prerequisite cap.
- Three of four answers are E3, backed by the March 2026 drill with a log, a CAPA, the CFO as approver and the treasury system as location. However, the proven path ran through the house bank's own secondary rail. The second bank has no account opened, which is the open CAPA.

**Move 3: Data switchboard. Score 2 | Confidence Low | E0:1 E1:1 E2:2 E3:0**
- Answers A, B, C, C give a mean of 2.25, which rounds to 2. The evidence average is 1.25, so the cap of 2 applies. Q1 is A, so the prerequisite cap of 2 also applies.
- There is no Tier-1 data flow map, so the effect of the region outage on ERP, portal, logs and telemetry cannot be traced. The runbook and access logging are documented but untested. There is no E3, so confidence is Low. The check passed (CIO as approver, IT service management tool as location).

**Move 4: Substitution. Score 3 | Confidence Low | E0:0 E1:0 E2:3 E3:1**
- Answers C, C, C, D give a mean of 3.25, which rounds to 3. The evidence average is 2.25, so there is no cap. Q2 is C, so there is no prerequisite cap.
- The consistency check **failed**. The Q4 E3 claim has no month/year, no log and no CAPA, so confidence is downgraded to Low. If Q4 were re-rated to E1, the evidence average would be 1.75 and the score would fall to 2.
  - The qualified alternate covers the forging supplier only.
  - No port, forwarder or cloud-region alternate is evidenced, and these are central to this scenario.

**Move 5: Market exit. Score 0 (Unknown/Insufficient data) | Confidence Low | E0:3 E1:1 E2:0 E3:0**
- The zero rule applies: Q1–Q3 are A at E0 (3 of 4).
- No approver is named and nothing is documented. The data and people plan is verbal only.

## 4) Evidence Index

**Move 1: Safe pause**
- Stop authority matrix: **Documented**
- Pause checklist with rollback plan: **Documented**
- Communications templates (internal, customer, regulator): **Claimed**
- Contract suspension clause summary: **Claimed**
- Pause decision log: **Unknown**
- Resume plan with gates: **Unknown**
- Escalation path under conflict: **Unknown**

**Move 2: Treasury reroute**
- Alternate bank and rail record: **Claimed**
- Freeze or hold playbook: **Tested**
- Counterparty tripwire definitions: **Tested**
- Reroute drill log and CAPA record (March 2026): **Tested**
- KYC/KYB bundle: **Unknown**
- Letters of credit or alternate settlement playbook: **Unknown**
- Treasury authority and backup delegation record: **Unknown** (approver roles were named; the artifact was not assessed)

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): **Unknown**
- Transfer mechanism options summary: **Claimed**
- Segmentation, localization and shutdown runbook: **Documented**
- Privileged and emergency access logging procedure: **Documented**
- Subprocessor list: **Unknown**
- OT or critical access boundary procedure: **Unknown**
- Retention and deletion procedure: **Unknown**

**Move 4: Substitution**
- Tier-1 single-points-of-failure ranked list: **Documented**
- Alternate supplier qualification record (forging, 2025): **Documented**
- Portability or failover plan: **Documented**
- Substitution and portability rights summary: **Claimed** (E3 asserted; date, log and CAPA missing)
- Concentration limits: **Unknown**
- Logistics reroute options: **Unknown**
- Cutover gates and evidence pack: **Unknown**

**Move 5: Market exit**
- Exit plan (legal, ops, data, people, comms, support): **Unknown**
- Termination and unwind path summary: **Unknown**
- Customer obligations and support plan: **Unknown**
- Data and people plan: **Claimed**
- Distributor or JV obligations map: **Unknown**
- Assets and IP handling procedure: **Unknown**
- Regulator and customer communications workflow: **Unknown**

## 5) 72-Hour Breakpoints

- **0–6h | Move 1 | Comms approval delay** (from answers, not exercised): The first holding statement to about 600 customers must be drafted from scratch (Q3 B/E1). This delays notice while the ERP and portal are dark and orders cannot be confirmed.
- **0–6h | Move 3 | Missing artifact** (from answers, not exercised): No Tier-1 data flow map exists (Q1 A/E0). The team cannot quickly tell which ERP, portal, log and telemetry flows depend on the failed region, so it cannot choose a switch or clean-stop posture.
- **6–24h | Move 2 | Missing alternate** (from answers, not exercised): The second bank is identified but has no account (Q1 B/E1). If house-bank access or ERP-driven payment files are disrupted, there is no independent rail ready within 72 hours.
- **6–24h | Move 4 | Operational infeasibility** (from answers, not exercised): The portability and failover plan is documented but untested (Q3 C/E2), and no alternate port or forwarder is evidenced. The ERP failover and export lane switch may fail when first attempted.
- **24–72h | Move 5 | Missing artifact** (from answers, not exercised): There is no exit plan and no named approver (Q1 A/E0). If the disruption forces withdrawal from a lane or market, nobody has the authority or the steps to unwind customer and contract obligations.

## 6) Top Blockers and Fixes

1. **No Tier-1 data flow map (Move 3, Q1).**
   - Evidence gap: E0, with no artifact or owner.
   - Minimal fix (2 weeks): Produce a one-page map of ERP, portal, logs and telemetry, showing region dependencies.
   - Proper fix (6–12 weeks): Maintain a full map with a review cadence, linked to the shutdown runbook.
   - Owner: CIO, delegated to the IT Operations Lead.

2. **No exit plan or approver (Move 5, Q1).**
   - Evidence gap: E0, with no approver.
   - Minimal fix (2 weeks): Name the exit approver role and draft a skeleton plan covering legal, ops, data, people, comms and support.
   - Proper fix (6–12 weeks): Complete the documented exit plan and run a tabletop on one market.
   - Owner: CEO to designate (proposed: COO).

3. **Customer obligations and support plan unknown (Move 5, Q3).**
   - Evidence gap: E0.
   - Minimal fix (2 weeks): List obligation types for the top customers by revenue, as a summary only.
   - Proper fix (6–12 weeks): Document the support plan with scripts and a comms workflow.
   - Owner: Head of Sales or Customer Service.

4. **Termination and unwind paths unknown (Move 5, Q2).**
   - Evidence gap: E0.
   - Minimal fix (2 weeks): Prepare questions for counsel on termination triggers in Tier-1 customer and supplier relationships across the operating countries.
   - Proper fix (6–12 weeks): Produce a documented high-level unwind path per Tier-1 relationship.
   - Owner: General Counsel.

5. **Communications improvised (Move 1, Q3).**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): Draft internal, customer and regulator holding-statement templates.
   - Proper fix (6–12 weeks): Pre-approve the templates with a defined workflow and owners, then test them in a drill.
   - Owner: Head of Communications.

6. **Suspension basis case-by-case (Move 1, Q4).**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): Commission a clause summary for Tier-1 contracts. As a question for counsel, ask which suspension or notice mechanisms exist, without making determinations.
   - Proper fix (6–12 weeks): Map suspension triggers and notices to the Tier-1 contracts.
   - Owner: General Counsel.

7. **No account at the second bank (Move 2, Q1).**
   - Evidence gap: E1. The CAPA is already open.
   - Minimal fix (2 weeks): Set a CAPA due date and start onboarding.
   - Proper fix (6–12 weeks): Pre-clear the second bank and test a reroute through it.
   - Owner: Treasurer, with the CFO as approver.

8. **Transfer mechanism options case-by-case (Move 3, Q2).**
   - Evidence gap: E1.
   - Minimal fix (2 weeks): List the cross-border flows. As a question for counsel, ask which transfer mechanism options could apply if data moves to another cloud region, without making determinations.
   - Proper fix (6–12 weeks): Map the options per Tier-1 flow.
   - Owner: Privacy/Data Protection Lead, with counsel.

9. **Unverified E3 on substitution rights (Move 4, Q4).**
   - Evidence gap: The E3 claim has no date, log or CAPA, so the consistency check failed.
   - Minimal fix (2 weeks): Locate the legal review artifact and record its date and owner.
   - Proper fix (6–12 weeks): Map rights for Tier-1 vendors (cloud, forwarder, forging), exercise them in a drill and log a CAPA.
   - Owner: Head of Procurement, with General Counsel.

10. **Failover plan untested and no logistics alternates evidenced (Move 4, Q3).**
    - Evidence gap: E2 only. The plan is documented but has not been exercised.
    - Minimal fix (2 weeks): Hold a desk-check of ERP and portal failover steps, and list alternate ports and forwarders.
    - Proper fix (6–12 weeks): Run a failover test with a log and CAPA, and qualify one alternate port and forwarder lane.
    - Owners: CIO and COO.

## 7) 30/60/90-Day Plan

**Workstream A: Data and cloud switchboard**
- **Outcome:** The organisation can decide to switch or cleanly stop the ERP and portal within 6 hours.
- **Tasks:**
  - 30 days: Produce the Tier-1 data flow map.
  - 30 days: Prepare the transfer-options question list for counsel.
  - 60 days: Map the data flows to the shutdown runbook.
  - 60 days: Desk-check the failover plan.
  - 90 days: Run a logged failover test with a CAPA.
- **Gates:**
  - The map is signed off by the CIO.
  - The failover test log and CAPA are stored in the IT service management tool.
- **Owners:** CIO, IT Operations Lead, Information Security Manager, Privacy Lead.
- **Stop rule:** If the failover test shows the plan is infeasible within 72 hours, stop and escalate the redesign to the COO and CIO. Do not report the plan as viable.

**Workstream B: Pause, comms and contract readiness**
- **Outcome:** A safe pause comes with a pre-approved holding statement and a known suspension basis.
- **Tasks:**
  - 30 days: Draft the three communications templates.
  - 30 days: Request the clause summary from counsel.
  - 60 days: Approve the template workflow.
  - 60 days: Map suspension triggers to Tier-1 contracts.
  - 90 days: Run the 45-minute drill (section 8).
- **Gates:**
  - The templates are approved by named owners.
  - The drill log and at least one CAPA exist.
- **Owners:** Plant Director, Head of Communications, General Counsel.
- **Stop rule:** If counsel cannot provide a clause summary within 60 days, record this as an open gap. Do not publish any assumed suspension basis.

**Workstream C: Exit, evidence hygiene and alternates**
- **Outcome:** Market exit is no longer Unknown, every E3 claim is verifiable, and independent alternates exist.
- **Tasks:**
  - 30 days: Name the exit approver.
  - 30 days: Verify or downgrade the Move 4 Q4 claim.
  - 30 days: Set the due date for the second-bank CAPA.
  - 60 days: Draft the exit plan skeleton and customer obligations summary.
  - 90 days: Qualify an alternate port and forwarder.
  - 90 days: Run an exit tabletop.
- **Gates:**
  - The exit approver is named in writing.
  - The second-bank account status is confirmed.
  - Each E3 claim has a date, log and CAPA.
- **Owners:** CEO (designation), COO, CFO and Treasurer, Head of Procurement.
- **Stop rule:** Any claim that cannot be evidenced by day 90 is re-rated downward in the next self-check.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Logkeeper
- Plant Director
- CFO or Treasurer
- CIO or IT Operations Lead
- COO
- General Counsel representative
- Head of Communications
- Customer Service lead
- Observer (internal audit)

**Agenda**
- **0–5 min:** Brief the scenario. The primary cloud region is down and the ERP and portal are dark.
- **5–15 min:** Decide whether to pause production or order intake, and who authorises it. Draft the holding statement.
- **15–25 min:** Add a second inject: the export port is closed. Choose the lane and forwarder path, and the payment path if ERP payment files are unavailable.
- **25–35 min:** Add a third inject: on day 3 the outage continues and key customers escalate. Decide whether to switch or cleanly stop the data posture, and whether any lane or market withdrawal is considered.
- **35–45 min:** Debrief, open CAPAs and assign owners.

**Decisions to log**
- Pause decision and approver
- Holding statement approval
- Payment path
- Data posture
- Logistics lane
- Customer commitments
- Exit consideration (approver gap)

**Evidence to capture**
- Timestamps
- Approver roles
- Artifacts used, by type and location
- Artifacts found missing
- Time to each decision

**CAPA prompt:** "Which decision stalled longest, which artifact or authority was missing, who owns the fix, and by what date?"

## 9) Escalations

No escalation triggers identified from provided information.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed. Labels reflect claims as stated.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. Multi-country operations (South Korea, Vietnam, 14 sales countries) mean legal mechanisms need counsel review. Nothing here is a legal or compliance determination.
- **Scenario simplification:** The scenario combines a 7-day cloud region outage with a port closure. Knock-on effects are not modelled, such as forging supplier delays or effects on the bank's systems.
- **Fast Baseline only:** Q5–Q7 were not asked for any move, so related artifacts show as Unknown and the tabletop was not run.
- **Recency of E3:** Recency was judged against the Reference Pack date (October 2026).
- **Unverified E3 sensitivity:** The Move 4 score rests on an E3 claim that failed its consistency check.
- **Escalation thresholds:** Escalation was assessed only against the stated USD 4m impact and the stated scope. Re-check if the impact estimate exceeds USD 10m, or if sanctions, export control, regulator or safety issues arise.
- **Not a screening:** This is not sanctions screening, export-control review or compliance certification.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 2, assistant (stop_reason end_turn)

Packet complete.

## Score

**Verdict: PASS.** All five format checks hold on the Turn 1 packet: 10 correctly titled sections in order, 5 top-level bullets in section 2, exactly 5 section 5 breakpoints each carrying the required marker, 10 numbered blockers, and the exact footer as the last line of section 10. No fail indicator appears. The only real ambiguity is whether nested bullets in section 2 count toward its limit, and I counted top-level bullets consistently across F2 and F4.

---

Final Liability rests with the Human.
