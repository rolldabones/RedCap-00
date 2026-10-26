# redcap-00-r2 Test-C

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:40 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 3 (Data switchboard) with score 2 and confidence High, and no later turn changes either value. Expected value computed in tests.md: no Tier-1 data flow map (Q1 A) caps Move 3 at 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: A, E0. Q2 Transfer mechanism options identified: D, E3. Q3 Segmentation, localization, shutdown runbook: D, E3. Q4 Privileged and emergency access logging: D, E3.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (20 questions plus consistency checks).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your estimated worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distribution, about 400 staff, three warehouses in one country, about 300 business customers.
  - Tier-1 dependencies:
    - cloud ERP
    - house bank
    - two bulk suppliers
    - one logistics provider
    - customer order portal

## 2) How Scoring Works

- **Pattern scores:** Each answer maps to a pattern score: A=1 (none, unknown or ad hoc), B=2 (partial or untested), C=3 (documented, owned, repeatable), D=4 (tested in the last 12 months with logs and CAPA). The move's average is rounded, and exact halves round down.
- **Evidence levels:** E0=0 means no evidence. E1=1 means verbal only. E2=2 means a named artifact and a named owner role. E3=3 means exercised within 12 months, with a log and a CAPA.
- **Caps:**
  - A move whose evidence average is below 2 is capped at 2.
  - A move whose prerequisite question is answered A is also capped at 2.
  - The final score is the lower of the provisional score and any applicable cap.
- **Zero rule:** A move scores 0 (Unknown/Insufficient data) only if 3 or more of its 4 answers are A at E0.
- **Confidence:**
  - High needs at least 3 of 4 answers at E3 and a passed consistency check.
  - Medium needs at least 3 of 4 answers at E2 or E3, at least one E3, and a passed check.
  - Otherwise confidence is Low. A failed consistency check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **2** | **High** | 1 | 0 | 0 | 3 |
| 4 Substitution | **3** | **Low** | 0 | 0 | 4 | 0 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- The provisional score is 3 (all C). The evidence average of 2.0 is not below 2, and the prerequisite Q1 is C, so no cap applies.
- Confidence is Low because there is no E3 answer, so Medium is not reachable. The consistency check passes (approver Operations Director; artifacts in the quality document system).

**Move 2 Treasury reroute: 3, Low**
- The provisional score is 3 (all C), with an evidence average of 2.0. The prerequisite Q1 (alternate banks and rails) is C, so no cap applies.
- Confidence is Low because there is no E3 answer. The "Execute within 72 hours" answer is "likely", not proven by exercise. The consistency check passes (CFO, with the Treasurer as backup; artifacts in the treasury system).

**Move 3 Data switchboard: 2, High**
- The provisional average is (1+4+4+4)/4 = 3.25, which rounds to 3. The zero rule does not apply because only 1 of 4 answers is A at E0. The evidence average is 2.25, so there is no evidence cap. However, the prerequisite Q1 (Tier-1 data flow map) is A, so the move is **capped at 2**.
- Confidence is High because 3 of 4 answers are at E3. The consistency check passes: the April 2026 exercise has a drill log and a CAPA, the approver is the CIO, and the artifacts are in the IT service management tool. High confidence here means confidence in the weakness. The tested runbooks run without a map of what they protect.

**Move 4 Substitution: 3, Low**
- The provisional score is 3 (all C), with an evidence average of 2.0. The prerequisite Q2 (qualified alternates) is C, so no cap applies.
- Confidence is Low because there is no E3 answer. The alternates are qualified but not shown to be viable within 72 hours, which would be the D standard. The consistency check passes (COO; procurement system).

**Move 5 Market exit: 3, Low**
- The provisional score is 3 (all C), with an evidence average of 2.0. The prerequisite Q1 (exit plan) is C, so no cap applies.
- Confidence is Low because there is no E3 answer and the exit plan has not been tested in a tabletop. The consistency check passes (CEO; board portal).

## 4) Evidence Index

Artifact types are categories only. A label of Unknown means the item was not asked in Fast Baseline or no evidence was given.

**Move 1 Safe pause**
- Stop-authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan with gates: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty tripwire and escalation definitions: Documented
- 72-hour execution plan: Documented
- KYC/KYB bundle: Unknown
- Treasury authority and backup delegation: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Unknown
- Transfer mechanism options map: Tested
- Segmentation, localization and shutdown runbook: Tested
- Privileged and emergency access logging: Tested
- Drill log (April 2026): Tested
- CAPA record in the risk system: Documented
- Subprocessor list: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Alternate qualification records: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5 Market exit**
- Exit plan (legal, ops, data, people, comms, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor and JV obligations map: Unknown
- Regulator and customer comms approval workflow: Unknown

## 5) 72-Hour Breakpoints

All answers in Moves 1, 2, 4 and 5 are tied at C/E2. For those moves, the bullet uses the answer most exposed under the ERP-ransomware scenario.

- **0–6h | Move 1 | Comms approval delay** (from answers, not exercised). The Q3 comms templates exist but are not pre-approved and have no workflow. The first holding statement to about 300 customers and other stakeholders cannot go out until someone drafts and approves it during the outage.
- **6–24h | Move 2 | Missing gate** (from answers, not exercised). The Q1 alternate rails are pre-cleared but have never been tested. With the ERP down, nobody has proven that payment instructions can be produced and released through the alternate path, so the reroute decision has no pass/fail gate.
- **6–24h | Move 3 | Missing artifact** (from answers, not exercised). There is no Tier-1 data flow map (Q1 is A/E0). The CIO cannot confirm which flows, logs and telemetry the tested shutdown or segmentation runbook must cover, so choosing a data posture becomes guesswork.
- **6–24h | Move 4 | Missing alternate** (from answers, not exercised). The Q2 alternates are qualified but not shown to be contractually and operationally viable within 72 hours. Order-taking or fulfilment substitution for the ERP or portal may not be executable inside the window.
- **24–72h | Move 5 | Missing gate** (from answers, not exercised). The Q1 exit plan is documented but has never been tabletop-tested. If prolonged disruption forces an exit or unwind decision on a segment or lane, the CEO has no rehearsed go/no-go criteria.

## 6) Top Blockers and Fixes

1. **No Tier-1 data flow map (Move 3 Q1)**
   - Evidence gap: A/E0, with no artifact and no owner.
   - Minimal fix (2 weeks): Draw a one-page map of ERP, portal, bank, supplier and logistics data flows, including logs and telemetry, with a named owner.
   - Proper fix (6–12 weeks): Build a reviewed, versioned map linked to the shutdown runbook and the CMDB, with a quarterly review cycle.
   - Owner role: CIO, with the data owner.

2. **72-hour treasury execution unproven (Move 2 Q4)**
   - Evidence gap: "Likely" at E2; no exercise.
   - Minimal fix (2 weeks): Run a desk walkthrough of payroll and supplier payments with the ERP unavailable.
   - Proper fix (6–12 weeks): Run a live low-value test through the alternate path, then log it and open a CAPA.
   - Owner role: CFO and Treasurer.

3. **Alternate rails untested (Move 2 Q1)**
   - Evidence gap: Pre-cleared but with no test evidence.
   - Minimal fix (2 weeks): Confirm with the alternate provider, at summary level, the onboarding status and the manual instruction path.
   - Proper fix (6–12 weeks): Run a tested reroute with a dated log and a CAPA.
   - Owner role: Treasurer.

4. **Alternates not proven viable within 72 hours (Move 4 Q2)**
   - Evidence gap: Qualified only, at E2.
   - Minimal fix (2 weeks): Rate each Tier-1 alternate (suppliers, logistics, manual order channel) on "viable within 72 hours: yes, no or unknown".
   - Proper fix (6–12 weeks): Close the contractual and operational gaps and verify them in a drill.
   - Owner role: COO, with the Procurement Lead.

5. **ERP failover or manual-operations plan untested (Move 4 Q3)**
   - Evidence gap: Documented, with no test in the last 12 months.
   - Minimal fix (2 weeks): Hold a tabletop of five-day manual order-to-ship operations at one warehouse.
   - Proper fix (6–12 weeks): Run a timed manual-mode drill across all three warehouses, with logs and a CAPA.
   - Owner role: COO and CIO.

6. **Comms templates not pre-approved (Move 1 Q3)**
   - Evidence gap: C/E2, with no approval workflow.
   - Minimal fix (2 weeks): Pre-approve a holding statement for the ransomware or outage scenario and name its approvers.
   - Proper fix (6–12 weeks): Set up an approval workflow with backups and a timed sign-off test.
   - Owner role: Communications Lead, with counsel review.

7. **Stop authority not exercised (Move 1 Q1)**
   - Evidence gap: The matrix is documented, but no delegated use has been logged.
   - Minimal fix (2 weeks): Confirm delegates and backups for each warehouse.
   - Proper fix (6–12 weeks): Exercise and log a stop decision in a drill.
   - Owner role: Operations Director.

8. **Continuity and safety checklist untested (Move 1 Q2)**
   - Evidence gap: Documented rollback plan with no test or criteria.
   - Minimal fix (2 weeks): Add explicit checks for chemical storage and handling continuity when the ERP is unavailable, such as offline access to hazard documentation and inventory locations.
   - Proper fix (6–12 weeks): Test the checklist with pass/fail criteria at all three sites.
   - Owner role: Operations Director, with the EHS Lead.

9. **Contract rights only summarized (Move 4 Q4)**
   - Evidence gap: Not mapped to Tier-1 vendors.
   - Minimal fix (2 weeks): Build a redacted summary table of substitution and portability rights for the ERP, bank, suppliers and logistics provider.
   - Proper fix (6–12 weeks): Map triggers and notice steps for each Tier-1 vendor, with counsel review.
   - Owner role: Procurement Lead, with counsel.

10. **Exit plan untested (Move 5 Q1)**
    - Evidence gap: Documented, with no tabletop.
    - Minimal fix (2 weeks): Define go/no-go triggers for exiting a lane, segment or vendor.
    - Proper fix (6–12 weeks): Run an exit tabletop with a log and a CAPA.
    - Owner role: CEO, with the Strategy or Legal Lead.

## 7) 30/60/90-Day Plan

**Workstream 1: Data map and ERP-down operations (Moves 3 and 4)**
- **Outcome:** A data flow map linked to the tested runbooks, and a proven five-day manual operating mode.
- **Tasks:**
  - Days 0–30: Draft the Tier-1 data flow map and assign an owner.
  - Days 0–30: Close or verify the April 2026 drill CAPA.
  - Days 31–60: Link the map to the shutdown and segmentation runbook.
  - Days 31–60: Hold a manual order-to-ship tabletop.
  - Days 61–90: Run a timed manual-mode drill at one site, with logs.
- **Gates:**
  - The map is reviewed and signed off by the CIO.
  - The manual-mode drill meets its defined throughput and safety criteria.
- **Owner roles:** CIO, COO, data owner.
- **Stop rule:** Pause expansion to other sites if the single-site drill fails a safety criterion. Fix it first.

**Workstream 2: Treasury and supplier alternates proven within 72 hours (Moves 2 and 4)**
- **Outcome:** Alternate rails and Tier-1 alternates evidenced as viable within 72 hours.
- **Tasks:**
  - Rate each alternate as viable within 72 hours: yes, no or unknown.
  - Run a payments walkthrough with the ERP down.
  - Run a live low-value reroute test.
  - Summarize substitution rights for each Tier-1 vendor.
  - Log the results and open CAPAs.
- **Gates:**
  - The test completes with a dated log.
  - Each Tier-1 dependency has at least one alternate rated "viable within 72 hours".
- **Owner roles:** CFO, Treasurer, COO, Procurement Lead.
- **Stop rule:** Halt the live test if the provider or counsel raises any concern. Revert to the desk exercise.

**Workstream 3: Pause, comms and exit decision readiness (Moves 1 and 5)**
- **Outcome:** Pre-approved comms and exercised stop and exit decisions.
- **Tasks:**
  - Pre-approve the outage holding statement.
  - Name delegates and backups for the stop decision.
  - Add chemical-safety continuity checks to the checklist.
  - Hold an exit-trigger tabletop.
- **Gates:**
  - The comms sign-off is completed within the target time in a test.
  - Both the stop and exit decisions are logged, with CAPAs.
- **Owner roles:** Operations Director, CEO, Communications Lead, EHS Lead.
- **Stop rule:** Do not publish any external statement without counsel review.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator
  - Operations Director (stop)
  - CFO or Treasurer (reroute)
  - CIO (data posture)
  - COO (substitution)
  - CEO (exit and escalation)
  - Communications Lead
  - Scribe
- **Agenda:**
  - 0–5 min: Scenario brief. Ransomware takes the ERP down for an estimated five days.
  - 5–15 min, 0–6h window: Decide what to pause, who authorizes it, which safety checks apply, and the first holding statement.
  - 15–30 min, 6–24h window: Choose the data posture without a flow map, the payment rail, and whether to switch to manual orders or an alternate supplier or logistics path.
  - 30–40 min, 24–72h window: Decide what is executed and monitored, and whether an exit or unwind trigger is reached.
  - 40–45 min: Capture the CAPAs.
- **Decisions to log:**
  - stop decision and its approver
  - holding statement approval time
  - rail choice
  - data posture
  - substitution cutover
  - exit or escalation call
- **Evidence to capture:**
  - timestamps
  - approver roles
  - artifacts consulted (category and location only)
  - gaps found
  - any decision made without an artifact
- **CAPA prompt:** "Which decision stalled, which missing artifact or authority caused it, who owns the fix, and by what date?"

## 9) Escalations

**ESCALATE (scenario-based: criminal).** The tested scenario is ransomware, which is a criminal act. Your stated figures (about USD 2 million and no more than 2,000 people) are below the financial and population thresholds, but the criminal-act trigger applies independently.

**Recommended path:** Incident lead (CIO) → CEO and General Counsel → external counsel and the board risk committee. Agree in advance who decides whether to engage law enforcement or report externally.

**Questions for counsel (no determinations made here):**
- Which notification or reporting obligations may apply, given that the jurisdiction is unknown?
- How should any ransom-payment question be handled? This includes sanctions screening of threat actors, which this tool does not perform.
- Do any products handled carry export-control or hazardous-materials obligations affected by an ERP outage?
- What physical-safety reporting is needed if chemical storage or handling controls depend on ERP data?

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed. "Documented" and "Tested" reflect your statements only.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown, so nothing here is legal advice or a compliance determination.
- **Scenario simplification:** A single five-day ERP outage scenario was used. Data exfiltration, extortion and concurrent supplier failure were not modeled.
- **Exercise recency assumption:** The Move 3 April 2026 exercise was treated as within 12 months relative to the Reference Pack date (October 2026). Confirm this against the actual assessment date.
- **Mode limitation:** Fast Baseline covers Q1–Q4 only. Breakpoints come from answers, not a tabletop. Deepening (Q5–Q7 and the mini tabletop) is available on request.
- **Not sanctions screening:** This is not sanctions screening or a security assessment of the ransomware threat.
- **Your own estimates:** The impact figures are your own estimates and were not validated.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 3, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 3 Data switchboard: Score 2, Confidence High

## Score

**Verdict: PASS.** Under the reference pack, Move 3 has Q1 = A/E0 and Q2-Q4 = D/E3. The prerequisite cap holds the provisional score of 3 down to 2, and 3 of 4 E3 answers with a passing consistency check (April 2026 exercise, log and CAPA named, approver CIO, artifact location named) give High confidence. The packet reports 2 and High, and Turn 2 repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
