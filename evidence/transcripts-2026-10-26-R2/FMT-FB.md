# redcap-00-r2 FMT-FB

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:46 KST · **max_tokens:** 16000

**Rule:** tests.md section 1, format compliance checks, Fast Baseline (and R4: "5 breakpoints in Fast Baseline, 10 in Deepening"); input is the fictional user input published in example.md

**Pass condition:** The final Output Packet produced in the session meets every check in tests.md section 1 for Fast Baseline: (F1) exactly 10 sections with the exact headings of reference.md section 9 in order (Snapshot; How Scoring Works; Scorecard; Evidence Index; 72-Hour Breakpoints; Top Blockers and Fixes; 30/60/90-Day Plan; Minimal Drill Script (45 minutes); Escalations; Known Limits + Version); (F2) section 2 has 5 top-level bullets or fewer, sub-bullets not counted (reference.md section 9); (F3) section 5 has exactly 5 bullets, one per move, each marked “from answers, not exercised”; (F4) section 6 has exactly 10 numbered items; (F5) section 10 ends with the exact footer string `RedCap-00 v1.2.0 | Evidence-capped scoring`.

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

Reference Pack v1.2.0 is supplied and applied as written. Your safety confirmation is noted, and nothing you provided needs redaction. This packet covers **Fast Baseline** (Q1–Q4 per move plus consistency checks). **Deepening** (Q5–Q7 for each move plus the mini tabletop) is available if you want to iterate. It would produce a 10-breakpoint version of this packet.

---

## 1) Snapshot

- **Jurisdiction:** Unknown. Plants in South Korea and Vietnam and sales into 14 countries are noted, but no governing jurisdiction was given.
- **Mode:** Fast Baseline
- **Scenario tested:** The cloud provider's primary region is down for 7 days while the main export port is closed at the same time. Your own estimate of worst-case impact is about USD 4 million.
- **Tier-1 scope summary:** Kestrel Marine Fittings (fictional) is a B2B, made-to-order marine hardware manufacturer with about 1,100 staff, 2 plants (South Korea and Vietnam) and about 600 business customers. Tier-1 dependencies:
  - cloud-hosted ERP
  - house bank
  - single forging supplier (a second supplier was qualified in 2025)
  - main export port and freight forwarder
  - customer order portal

## 2) How Scoring Works

- **Answers A–D map to a pattern score of 1–4.**
  - A means none or unknown.
  - D means tested in the last 12 months with logs and CAPA, with alternates viable within 72 hours.
  - A move's provisional score is the mean of its answers, rounded, with exact halves rounding down.
- **Evidence E0–E3 maps to a score of 0–3.**
  - E0 means nothing exists.
  - E1 means verbal claims only.
  - E2 means a named artifact with an owner role.
  - E3 means exercised in the last 12 months, with a log and a CAPA.
- **Caps (hard):**
  - If a move's evidence average is below 2, its score is capped at 2.
  - If the move's prerequisite question is answered A, its score is capped at 2.
  - A move scores 0 (Unknown/Insufficient data) only when more than half of its answers are A at E0.
- **Confidence:**
  - High requires more than half of answers at E3 and a passed consistency check.
  - Medium requires more than half at E2 or E3, at least one E3, and a passed check.
  - Low covers everything else.
- **Consistency check:** A move fails if any E3 answer lacks a date, log or CAPA. It also fails if the move has E2 or E3 answers but no approver role or no artifact location. A failed check forces Low confidence.

## 3) Scorecard

| Move | Score (0–4) | Confidence | #E0 #E1 #E2 #E3 |
|---|---|---|---|
| 1 Safe pause | **2** | Low | 0 · 2 · 2 · 0 |
| 2 Treasury reroute | **3** | High | 0 · 1 · 0 · 3 |
| 3 Data switchboard | **2** | Low | 1 · 1 · 2 · 0 |
| 4 Substitution | **3** | Low | 0 · 0 · 3 · 1 |
| 5 Market exit | **0 (Unknown/Insufficient data)** | Low | 3 · 1 · 0 · 0 |

**Move 1 Safe pause**
- **Score:** Answers C, C, B, B average 2.5, which rounds down to 2. The evidence average of 1.5 also caps the score at 2. Q1 (stop authority) is C, so no prerequisite cap applies.
- **Confidence:** Low because there are no E3 answers. The consistency check passes: the Plant Director is the approver and the quality document system is the artifact location. The weak spots are ad hoc communications and case-by-case suspension basis.

**Move 2 Treasury reroute**
- **Score:** Answers B, D, D, D average 3.5, which rounds down to 3. The evidence average of 2.5 means no evidence cap. Q1 is B, so no prerequisite cap applies.
- **Confidence:** High. Three of four answers are E3. The March 2026 exercise is within 12 months of the pack date and has a log and a CAPA. The CFO is approver, with the Treasurer as backup. **Note:** the drill used the house bank's *secondary rail*, not a second bank. The open CAPA (open the second-bank account) is exactly the Q1 gap.

**Move 3 Data switchboard**
- **Score:** Answers A, B, C, C average 2.25, which rounds to 2. Two caps independently hold it at 2: the evidence average is 1.25, and the prerequisite Q1 (data flow map) is answered A.
- **Confidence:** Low because there are no E3 answers. The consistency check passes: the CIO is approver and the IT service management tool is the artifact location. This move is scenario-critical, because a regional cloud outage hits ERP and the order portal directly.

**Move 4 Substitution**
- **Score:** Answers C, C, C, D average 3.25, which rounds to 3. The evidence average of 2.25 means no evidence cap. Q2 (qualified alternates) is C, so no prerequisite cap applies.
- **Confidence:** Low because the consistency check **fails**. The Q4 E3 claim has no month/year, no log and no CAPA. **Sensitivity:** if the substitution-rights summary cannot be produced as a named artifact with an owner role, Q4 is really E1. The evidence average would then be 1.75, and the cap would drop the score to 2.

**Move 5 Market exit**
- **Score:** Three of four answers are A at E0, so the zero rule applies and the move is reported as Unknown/Insufficient data. Only Q4 (data and people plan) is above A, at B with E1.
- **Confidence:** Low. The consistency check technically passes because there are no E2 or E3 answers. No approver role is named, and nothing is documented.

## 4) Evidence Index

Labels follow the evidence recorded for each answer: E0 is Unknown, E1 is Claimed, E2 is Documented, E3 is Tested. Themes from Q5–Q7 were not asked in Fast Baseline and are listed as Unknown.

**Move 1 Safe pause**
- Stop authority matrix — Documented
- Pause safety and continuity checklist with rollback plan — Documented
- Communications templates (internal, customer, regulator) — Claimed
- Contractual suspension clause summary — Claimed
- Pause decision log — Unknown
- Resume plan — Unknown
- Conflict escalation path — Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail record — Claimed
- Freeze or hold playbook — Tested
- Counterparty tripwire definitions — Tested
- Reroute drill log and CAPA record — Tested
- KYB readiness bundle — Unknown
- Alternate settlement path playbook — Unknown
- Treasury authority and backup delegation — Claimed

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry) — Unknown
- Transfer mechanism options summary — Claimed
- Segmentation and shutdown runbook — Documented
- Privileged and emergency access logging procedure — Documented
- Subprocessor list — Unknown
- OT or critical access boundary procedure — Unknown
- Retention and deletion procedure — Unknown

**Move 4 Substitution**
- Ranked Tier-1 single points of failure list — Documented
- Alternate supplier qualification record — Documented
- Portability or failover plan — Documented
- Substitution and portability rights summary — Claimed. The answer was recorded as E3 for scoring, but it does not meet the "Tested" definition (no date, log or CAPA).
- Concentration limits — Unknown
- Logistics reroute options plan — Unknown
- Cutover gates — Unknown

**Move 5 Market exit**
- Exit plan — Unknown
- Termination and unwind summary — Unknown
- Customer obligations and support plan — Unknown
- Data and people plan — Claimed
- Distributor or JV obligations map — Unknown
- Assets and IP handling procedure — Unknown
- Regulator and customer comms workflow — Unknown

## 5) 72-Hour Breakpoints

- **Move 1 — 0–6 hours, comms approval delay (from answers, not exercised):** Q3 is B/E1, meaning no templates exist. Without a pre-approved holding statement, notices to customers and staff about a pause have to be drafted and approved while the plants are already stopping.
- **Move 2 — 6–24 hours, missing alternate (from answers, not exercised):** Q1 is B/E1. The second bank is identified but has no account, so if the house bank's rails are impaired there is no other bank to switch to within 72 hours.
- **Move 3 — 6–24 hours, missing artifact (from answers, not exercised):** Q1 is A/E0. Without a Tier-1 data flow map, the team cannot tell which ERP, portal and log data depend on the failed region. That leaves no basis for choosing between failover, segmentation and a clean stop.
- **Move 4 — 24–72 hours, operational infeasibility (from answers, not exercised):** Q3 is C/E2, a documented but untested plan. An unexercised portability or failover plan may not run inside the outage window, leaving ERP-dependent production and shipping decisions stalled.
- **Move 5 — 24–72 hours, missing authority (from answers, not exercised):** Q1 is A/E0 and no approver is named. If the dual outage forces exiting a lane or market, nobody holds the decision and no plan exists to sequence legal, operations, data, people and communications.

## 6) Top Blockers and Fixes

1. **No Tier-1 data flow map (Move 3 Q1)**
   - **Evidence gap:** E0, no artifact or owner.
   - **Minimal fix (2 weeks):** Whiteboard-level map of ERP, order portal and logs/telemetry, showing which cloud region each depends on, saved in the IT service management tool.
   - **Proper fix (6–12 weeks):** Maintained, reviewed map linked to the shutdown runbook, with a quarterly review owner.
   - **Owner role:** CIO, with the IT Operations Lead.
2. **Second bank identified but no account (Move 2 Q1; open CAPA)**
   - **Evidence gap:** E1.
   - **Minimal fix (2 weeks):** Set a CAPA due date and start onboarding the second bank. Record the status in the treasury system.
   - **Proper fix (6–12 weeks):** Account pre-cleared, then a test reroute through the second bank, logged as a CAPA closure.
   - **Owner role:** Treasurer, with the CFO as approver.
3. **Communications drafted ad hoc (Move 1 Q3)**
   - **Evidence gap:** E1, no templates.
   - **Minimal fix (2 weeks):** Holding-statement templates for staff, customers and regulators in the quality document system.
   - **Proper fix (6–12 weeks):** Templates pre-approved through a defined approval workflow with named owner roles. Factual accuracy should be reviewed before anything is sent.
   - **Owner role:** Communications Lead, with the Plant Director.
4. **Failover plan untested (Move 4 Q3)**
   - **Evidence gap:** E2, never exercised.
   - **Minimal fix (2 weeks):** Walk-through of the ERP and portal failover steps against this scenario, with gaps logged.
   - **Proper fix (6–12 weeks):** Live or simulated failover test with a log and a CAPA, to reach E3.
   - **Owner role:** CIO, with the COO.
5. **Contractual suspension basis handled case by case (Move 1 Q4)**
   - **Evidence gap:** E1.
   - **Minimal fix (2 weeks):** List the Tier-1 contracts and ask counsel which ones need suspension-clause review. This is a planning list only.
   - **Proper fix (6–12 weeks):** Counsel-prepared clause summary mapped to Tier-1 contracts, with triggers and notice steps.
   - **Owner role:** General Counsel.
6. **Transfer mechanism options handled case by case (Move 3 Q2)**
   - **Evidence gap:** E1.
   - **Minimal fix (2 weeks):** List cross-border data flows that relocating to another region might create, as questions for counsel.
   - **Proper fix (6–12 weeks):** Counsel-reviewed options map per flow, with no compliance determination implied.
   - **Owner role:** Data Protection Lead, with General Counsel.
7. **Substitution rights "tested" claim unsupported (Move 4 Q4)**
   - **Evidence gap:** The E3 claim has no date, log or CAPA, so the consistency check fails.
   - **Minimal fix (2 weeks):** Find or produce the rights summary as a named artifact with an owner role, or reclassify it.
   - **Proper fix (6–12 weeks):** Rights summary mapped for Tier-1 vendors and exercised in a drill, with a log and a CAPA.
   - **Owner role:** General Counsel, with the COO.
8. **No exit decision owner (Move 5 consistency)**
   - **Evidence gap:** No approver role named.
   - **Minimal fix (2 weeks):** The executive team designates an exit approver role and a backup, recorded in the authority matrix.
   - **Proper fix (6–12 weeks):** Exit authority delegated and exercised in a tabletop.
   - **Owner role:** CEO.
9. **No exit plan (Move 5 Q1, with Q2 also A/E0)**
   - **Evidence gap:** E0.
   - **Minimal fix (2 weeks):** One-page outline of the exit plan covering legal, operations, data, people, communications and support, with a gap list.
   - **Proper fix (6–12 weeks):** Documented exit plan, including termination and unwind paths reviewed by counsel, then a tabletop.
   - **Owner role:** COO, with General Counsel.
10. **Customer obligations and support plan unknown (Move 5 Q3)**
    - **Evidence gap:** E0.
    - **Minimal fix (2 weeks):** Inventory obligations for the Tier-1 customer segment, such as open orders, warranties and support commitments.
    - **Proper fix (6–12 weeks):** Documented support plan with customer scripts and a communications workflow.
    - **Owner role:** Head of Sales, with the Customer Service Lead.

## 7) 30/60/90-Day Plan

**Workstream A: Cloud and data continuity (Moves 3 and 4)**
- **Outcome:** By day 90, Move 3 reaches C/E2 or better on Q1, and the failover plan has a dated test log.
- **Tasks:**
  - Day 30: Draft the Tier-1 data flow map with region dependencies.
  - Day 30: List the cross-border flow questions for counsel.
  - Day 60: Align the shutdown runbook to the map.
  - Day 60: Walk through the failover plan.
  - Day 90: Run a simulated failover with a log and a CAPA.
- **Gates:**
  - The map is reviewed by the IT Operations Lead and the Information Security Manager.
  - The failover test log and at least one CAPA are recorded in the IT service management tool.
- **Owner roles:** CIO, IT Operations Lead, Data Protection Lead.
- **Stop rule:** Pause and escalate to the CIO if the map shows Tier-1 dependencies that cannot be relocated within 72 hours.

**Workstream B: Treasury and pause readiness (Moves 1 and 2)**
- **Outcome:** By day 90, the second-bank account is open and tested, and pause communications templates are pre-approved.
- **Tasks:**
  - Day 30: Start onboarding the second bank.
  - Day 30: Draft holding-statement templates.
  - Day 60: Approval workflow for the templates.
  - Day 60: Counsel's Tier-1 suspension clause list.
  - Day 90: Test reroute through the second bank.
- **Gates:**
  - The CAPA is closed with a test log.
  - The templates are approved by the Plant Director and the Communications Lead.
  - The clause summary is filed in the quality document system.
- **Owner roles:** Treasurer, CFO, Communications Lead, Plant Director, General Counsel.
- **Stop rule:** Stop and escalate to the CFO if onboarding stalls past day 60.

**Workstream C: Exit foundations and evidence hygiene (Moves 4 and 5)**
- **Outcome:** By day 90, Move 5 has an approver, a documented plan outline and a customer obligations inventory, and the Move 4 Q4 evidence is resolved.
- **Tasks:**
  - Day 30: Designate the exit approver.
  - Day 30: Resolve the substitution-rights artifact.
  - Day 60: Draft the exit plan outline.
  - Day 60: Inventory customer obligations.
  - Day 90: Counsel review of termination and unwind paths.
  - Day 90: Exit tabletop.
- **Gates:**
  - The approver is recorded in the authority matrix.
  - The exit plan and rights summary are documented with owner roles.
- **Owner roles:** CEO, COO, General Counsel, Head of Sales.
- **Stop rule:** Stop if counsel flags any matter needing formal legal review. Hold the workstream until that review is scoped.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator
  - Plant Director (pause)
  - CFO and Treasurer (reroute)
  - CIO and IT Operations Lead (data)
  - COO (substitution and logistics)
  - Communications Lead
  - General Counsel (observer, for questions only)
  - Scribe
- **Agenda:**
  - 0–5 min: Scenario brief. The cloud primary region is down for 7 days and the main export port is closed.
  - 5–15 min: What pauses, who authorizes it, which checks must pass, and the first holding statement.
  - 15–25 min: Data posture (failover, segment or clean stop) and treasury rail, with sign-offs.
  - 25–35 min: The forging supplier switch and freight forwarder options while the port is closed. Execution and monitoring.
  - 35–45 min: Gaps, CAPA assignment and evidence check.
- **Decisions to log:**
  - Pause authorization and approver role
  - Holding statement approval time
  - Data posture choice and approver
  - Payment rail choice
  - Substitution and cutover go/no-go
  - Any exit question raised and who would own it
- **Evidence to capture:**
  - Timestamps for each decision
  - The artifact actually used, or noted as missing
  - Time-to-decision for each window
  - Unresolved questions for counsel
  - Attendance by role
- **CAPA prompt:** "Which decision took longest or could not be made, what artifact or authority was missing, who owns the fix, and by what date?" Record at least one CAPA per move, so future answers can qualify as E3.

## 9) Escalations

No escalation triggers identified from provided information.

## 10) Known Limits + Version

- **Self-report bias:** All answers are the organization's own assessment, and none was independently verified.
- **No document validation:** No artifacts were reviewed. "Documented" and "Tested" labels rely on your stated artifact types, owner roles, dates, logs and CAPAs.
- **Jurisdiction ambiguity:** The jurisdiction is unknown and multiple countries are involved. Nothing here is a legal, compliance or transfer-mechanism determination. Route contract and data-transfer questions to counsel.
- **Scenario simplification:** The analysis tests one combined scenario (cloud region outage plus port closure). It does not cover cascading effects such as dependencies of the house bank or freight forwarder on the same cloud provider.
- **Fast Baseline only:** Q5–Q7 themes (such as logistics reroute options, cutover gates and KYB bundles) were not asked. Running Deepening could change scores and confidence.
- **Move 4 sensitivity:** The score of 3 depends on the Q4 evidence level recorded. If the rights summary is not a named, owned artifact, the evidence cap would reduce the score to 2.
- **Exercise recency:** Move 2's High confidence assumes the March 2026 drill falls within 12 months of the assessment date. Re-check this once 12 months have passed.
- **Impact estimate:** USD 4 million is your estimate and was not validated. It is below the escalation threshold as provided.
- **Out of scope:** This is not sanctions screening, export-control review, compliance certification or legal advice.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only: "Packet complete."

### Turn 2, assistant (stop_reason end_turn)

Packet complete.

## Score

**Verdict: PASS.** Every element of the pass condition is met. The packet has the 10 exact headings in order, section 2 has 5 top-level bullets, section 5 has 5 bullets each marked 'from answers, not exercised', section 6 has 10 numbered items, and the packet ends with the exact footer. None of the fail indicators appears, so the verdict is PASS.

---

Final Liability rests with the Human.
