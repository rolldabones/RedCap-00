# redcap-00-r2 Test-E

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:41 KST · **max_tokens:** 16000

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

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, plus consistency checks). Deepening (Q5–Q7 per move plus the mini tabletop) was not run and is available on request.
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. Estimated worst-case impact is about USD 2m, affecting 2,000 people or fewer.
- **Tier-1 scope summary:** Specialty chemicals B2B distributor, about 400 staff, 3 warehouses in one country, about 300 business customers. Tier-1 dependencies:
  - cloud ERP
  - house bank
  - 2 bulk suppliers
  - 1 logistics provider
  - customer order portal

## 2) How Scoring Works

- **Answers A–D:** Each answer maps to a pattern score: A=1 (none, unknown, ad hoc), B=2 (partial, informal), C=3 (documented, owned, not recently tested), D=4 (tested in the last 12 months with logs and CAPA, with viable alternates). The move score is the mean, rounded to the nearest whole number, with exact halves rounding down.
- **Evidence E0–E3:** E0=0 (none), E1=1 (verbal), E2=2 (named artifact and owner role), E3=3 (exercised in the last 12 months with a log and a CAPA).
- **Caps:**
  - If the move's evidence average is below 2, the score is capped at 2.
  - If the move's prerequisite question is answered A, the score is capped at 2.
- **Zero rule:** A score of 0 (Unknown/Insufficient data) applies only when more than half of a move's answers are A at E0.
- **Confidence:**
  - High: more than half the answers at E3 and the consistency check passes.
  - Medium: more than half at E2 or E3, at least one E3, and the check passes.
  - Low: otherwise.
  - A failed consistency check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 | Consistency check |
|---|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 | 0 | 4 | 0 | Pass |
| 2 Treasury reroute | **4** | Low | 0 | 0 | 0 | 4 | **Fail** |
| 3 Data switchboard | **3** | Low | 0 | 0 | 4 | 0 | Pass |
| 4 Substitution | **3** | Low | 0 | 0 | 4 | 0 | Pass |
| 5 Market exit | **3** | Low | 0 | 0 | 4 | 0 | Pass |

**Move 1: Safe pause (3, Low)**
- All four answers are C/E2, so the provisional score is 3. The evidence average is 2.00, which is not below 2, so no cap applies. The prerequisite (Q1 = C) is met. The Operations Director is the approver, and the artifacts sit in the quality document system.
- Confidence is Low because there are no E3 answers. Nothing about the pause, including stop authority and holding statements, has been exercised.

**Move 2: Treasury reroute (4, Low)**
- All four answers are D/E3, so the provisional score is 4. The evidence average is 3.00, so no caps apply. The score is therefore 4 as recorded.
- The consistency check **fails**: you report that none of the E3 claims has a date, a log or a CAPA. Confidence is forced to Low. Under the strict definitions, these answers do not meet D or E3. If you re-record them to match what you can show (likely C/E2), this move would score 3. **Treat the 4 as unverified.**

**Move 3: Data switchboard (3, Low)**
- All four answers are C/E2, so the provisional score is 3. No caps apply, and the prerequisite (Q1 = C) is met. The CIO is the approver, and the artifacts sit in the IT service management tool.
- Confidence is Low because there are no E3 answers. The shutdown and segmentation runbook and the emergency access logging are documented but not exercised. This is the central capability in a ransomware scenario.

**Move 4: Substitution (3, Low)**
- All four answers are C/E2, so the provisional score is 3. No caps apply, and the prerequisite (Q2 = C) is met. The COO is the approver, and the artifacts sit in the procurement system.
- Confidence is Low because there are no E3 answers. The alternates are "identified and qualified" but not shown to be viable within 72 hours. The ERP failover plan has not been tested.

**Move 5: Market exit (3, Low)**
- All four answers are C/E2, so the provisional score is 3. No caps apply, and the prerequisite (Q1 = C) is met. The CEO is the approver, and the artifacts sit in the board portal.
- Confidence is Low because there are no E3 answers. The exit and unwind plans are documented but not rehearsed in a tabletop.

## 4) Evidence Index

Labels describe artifact categories only, not their content.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Comms templates (internal, customer, regulator): Documented
- Contract suspension clause summary: Documented
- Pause decision log: Unknown
- Pause drill record and CAPA: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail list: Documented
- Freeze/hold playbook: Documented
- Counterparty tripwire definitions: Documented
- Reroute test record: Claimed
- Exercise log: Unknown (you report none recorded)
- CAPA record: Unknown (you report none recorded)
- Treasury authority and backup matrix: Documented (CFO, with Treasurer as backup)

**Move 3: Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options summary: Documented
- Segmentation/shutdown runbook: Documented
- Privileged/emergency access logging description: Documented
- Subprocessor list: Unknown
- Runbook test record and CAPA: Unknown

**Move 4: Substitution**
- Tier-1 single points of failure list: Documented
- Qualified alternates register: Documented
- ERP portability/failover plan: Documented
- Substitution rights summary: Documented
- 72-hour viability evidence for alternates: Unknown
- Failover test record and CAPA: Unknown

**Move 5: Market exit**
- Exit plan: Documented
- Termination/unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Exit tabletop record: Unknown

## 5) 72-Hour Breakpoints

Every bullet below comes from your answers and has not been exercised.

1. **0–6 hours | Move 1 | comms approval delay.** The communications templates (Q3 = C) are not pre-approved and have no workflow. The first holding statement to customers and staff therefore waits on drafting and sign-off while orders and deliveries are paused. *All four answers are tied at C/E2; this one was chosen as most exposed in this scenario.*
2. **6–24 hours | Move 2 | missing artifact.** The claim of 72-hour execution (Q4 = D) has no exercise log or date. The reroute path cannot be relied on, or shown to the bank, when payment runs fail without the ERP. *Weakest answer by verification status.*
3. **0–6 hours | Move 3 | missing gate.** The segmentation and shutdown runbook (Q3 = C) has never been tested. Containment and isolation decisions have no validated go/no-go gates, so they stall or are improvised while ransomware may still be spreading. *Tied at C/E2; most exposed in this scenario.*
4. **6–24 hours | Move 4 | missing alternate.** The qualified alternates (Q2 = C) are not proven viable within 72 hours, and the ERP failover plan is untested. Manual or alternate order-to-dispatch for 300 customers may not be workable before stock and delivery commitments lapse. *Tied at C/E2; most exposed in this scenario.*
5. **24–72 hours | Move 5 | missing artifact.** The customer obligations and support plan (Q3 = C) is documented in the board portal, but the customer obligation data likely sits in the ERP that is down. If a customer or segment exit or suspension is considered, the obligations cannot be confirmed. *Tied at C/E2; most exposed in this scenario.*

## 6) Top Blockers and Fixes

1. **Treasury "tested" claims cannot be shown.**
   - Gap: E3 claims with no date, log or CAPA.
   - Minimal fix (2 weeks): Re-record the Move 2 answers to the evidence you can actually show, and schedule a reroute walkthrough.
   - Proper fix (6–12 weeks): Run a logged reroute exercise with the alternate bank and rail, open CAPAs, and file the records in the treasury system.
   - Owner: CFO, with Treasurer delegated.
2. **Payments depend on the ERP during an outage.**
   - Gap: No evidence that a manual or out-of-ERP payment process has been exercised.
   - Minimal fix: Document the minimum viable manual payment run (critical payees and approvals) as a checklist.
   - Proper fix: Test it in a drill with dual approval and a log.
   - Owner: Treasurer.
3. **Shutdown and segmentation runbook untested.**
   - Gap: C/E2 only, with no exercise record.
   - Minimal fix: Hold a desk check of the runbook with IT and the ERP vendor contact role, and confirm decision gates.
   - Proper fix: Run a technical containment exercise with a log and CAPA.
   - Owner: CIO.
4. **Emergency access logging not validated.**
   - Gap: Documented but never exercised.
   - Minimal fix: Confirm that the break-glass procedure and log retention survive an ERP and identity outage.
   - Proper fix: Test break-glass with audit trail review.
   - Owner: CIO, with the IT security lead.
5. **ERP failover and manual operations untested.**
   - Gap: The Q3 failover plan is C/E2.
   - Minimal fix: Define 5-day manual operating procedures for order intake, picking and dispatch, and pre-stage offline customer, product and safety data extracts.
   - Proper fix: Run a timed manual-operations exercise at one warehouse.
   - Owner: COO.
6. **Alternates not proven viable within 72 hours.**
   - Gap: Q2 is "qualified", which is not the same as 72-hour viable.
   - Minimal fix: For each bulk supplier and the logistics provider, confirm the activation steps and lead time for the alternate.
   - Proper fix: Do a contractual and operational readiness check, with a dry-run order through the alternate.
   - Owner: COO, with the Procurement Lead.
7. **Comms templates not pre-approved.**
   - Gap: Templates exist, with no approval workflow evidenced.
   - Minimal fix: Pre-approve outage holding statements (staff, customer, supplier) and name approvers with backups.
   - Proper fix: Exercise the approval workflow under time pressure, with log and CAPA.
   - Owner: Operations Director, with the Communications Lead.
8. **Stop authority never exercised.**
   - Gap: Authority matrix only (E2).
   - Minimal fix: Confirm the delegate for the Operations Director and the conditions for using it.
   - Proper fix: Exercise a logged pause decision in a drill.
   - Owner: Operations Director.
9. **Customer obligation data inaccessible without the ERP.**
   - Gap: Plan location (board portal) and data location (ERP) are split.
   - Minimal fix: Maintain an offline summary of Tier-1 customer obligation categories.
   - Proper fix: Map and test retrieval during an ERP-down drill.
   - Owner: CEO, with the Commercial Director.
10. **No E3 evidence anywhere.**
    - Gap: Confidence is Low on all 5 moves.
    - Minimal fix: Run the 45-minute drill in Section 8 and log it.
    - Proper fix: Set an annual exercise calendar covering all 5 moves, with CAPA tracking.
    - Owner: CEO, with the Risk or Resilience Lead.

## 7) 30/60/90-Day Plan

**Workstream A: Ransomware containment and ERP-down operations (Moves 1, 3, 4)**
- **Outcome:** Larkspur can contain the incident, pause safely and run minimum operations for 5 days without the ERP, with evidence at E3.
- **Tasks:**
  - Days 0–30: Desk-check the shutdown runbook and the break-glass procedure.
  - Days 0–30: Draft manual operating procedures for order, pick and dispatch.
  - Days 30–60: Pre-stage offline extracts of customer, product and safety data.
  - Days 30–60: Confirm the delegates for the Operations Director and the CIO.
  - Days 60–90: Run a timed ERP-down exercise at one warehouse, with log and CAPA.
- **Gates:**
  - Day 30: Runbook gates and delegates are documented.
  - Day 60: Offline extracts are verified as retrievable.
  - Day 90: The exercise is logged and the CAPAs are opened.
- **Owner roles:** CIO (lead), Operations Director, COO.
- **Stop rule:** Pause any exercise step that could affect live safety-critical handling of hazardous materials. Proceed only after the Operations Director confirms safety checks.

**Workstream B: Treasury evidence reset (Move 2)**
- **Outcome:** Move 2 answers reflect verifiable evidence, and the reroute is exercised.
- **Tasks:**
  - Re-record the Q1–Q4 answers against the strict definitions.
  - Write the manual payment-run checklist.
  - Confirm alternate rail activation steps.
  - Run a logged reroute exercise.
  - Open CAPAs and file the records.
- **Gates:**
  - Day 30: Re-scored answers are accepted by the CFO.
  - Day 90: The exercise log and CAPA exist.
- **Owner roles:** CFO (lead), Treasurer.
- **Stop rule:** Do not move real funds as part of the test without CFO approval and bank coordination.

**Workstream C: Comms and governance (Moves 1, 5)**
- **Outcome:** Pre-approved holding statements, a tested approval workflow and a rehearsed escalation path.
- **Tasks:**
  - Pre-approve the outage templates.
  - Name approvers with backups.
  - Build an offline obligations summary.
  - Brief the board on scores and confidence.
- **Gates:**
  - Day 30: Templates are approved.
  - Day 60: The workflow is exercised in the Section 8 drill.
- **Owner roles:** CEO (lead), Operations Director, Communications Lead.
- **Stop rule:** Stop if any template's statements cannot be verified as accurate. Comms must stay factual and non-deceptive.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk or Resilience Lead)
- Decision approvers: Operations Director, CFO, CIO, COO, CEO
- Scribe/logger
- Communications Lead
- Observer (Internal Audit, optional)

**Agenda**
- 0–5 minutes: Inject. The ERP is encrypted at 06:00, the portal is down, and the outage is expected to last 5 days.
- 5–15 minutes, the 0–6 hour window:
  - What is paused and who authorizes it?
  - What containment gates apply (CIO)?
  - Which safety checks apply to hazardous stock?
  - Read out and approve the first holding statement.
- 15–28 minutes, the 6–24 hour window:
  - Choose the payment path, the manual operations posture, and supplier and logistics alternates.
  - Name the approvers.
- 28–40 minutes, the 24–72 hour window:
  - What is executed and monitored?
  - Is any customer suspension or exit considered?
  - What evidence is captured?
- 40–45 minutes: Hot wash and CAPA capture.

**Decisions to log** (record time, decision, approver role and artifact used for each)
- Pause decision
- Containment and segmentation decision
- Payment path
- Alternate activation
- Holding statement approval
- Escalation to counsel

**Evidence to capture**
- Attendance by role
- Timestamped decision log
- Artifacts referenced, and whether they could be found without the ERP
- Stalls observed

**CAPA prompt:** For each stall, state:
- What blocked the decision or action
- Which artifact or authority was missing
- The fix, owner role and due date
- How closure will be evidenced

## 9) Escalations

**ESCALATE.** Triggers identified from the scenario as provided:

- **Criminal matter:** Ransomware is a criminal act by its nature. If this scenario materializes, involve counsel and assess law enforcement engagement.
- **Potential sanctions exposure (conditional):** If any ransom payment or negotiation is ever considered, it may raise sanctions questions. This packet makes no sanctions determination. The question must go to counsel before any action.
- **Potential physical safety (conditional):** Specialty chemicals handling, and access to safety data or hazmat tracking during an ERP outage, may create physical safety risk. Confirm this with the Operations Director and the safety lead.
- **Thresholds not met:** The financial and people thresholds are not triggered on your estimates (about USD 2m, which is below USD 10m; 2,000 or fewer people, which is below 100,000).

**Recommended path:** Incident lead (CIO) → CEO → General Counsel or external counsel. Counsel advises on law enforcement, notification and sanctions questions. Brief the board via the CEO.

**Questions for counsel (Jurisdiction: Unknown):**
- Which notification obligations might apply?
- What is the position on ransom payment?
- Do contract suspension notices to customers or suppliers need review?

## 10) Known Limits + Version

- **Self-report bias:** All answers are self-reported. Move 2 shows claims exceeding the evidence the organization can produce.
- **No document validation:** No artifacts were reviewed. "Documented" labels reflect your statements only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown. No legal, compliance or notification conclusions are drawn.
- **Scenario simplification:** A single 5-day ERP outage. Data exfiltration, outages of more than one Tier-1 system at once, and supplier-side incidents are not modelled.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run. The breakpoints are not exercised.
- **Move 2 score:** The score of 4 follows the deterministic method on the answers as recorded. It is unverified, and re-recording would likely yield 3.
- **Tie-break:** Ties among equally weak answers were broken by exposure to this scenario, which is a judgement call.
- **Scope of service:** This is informational planning output, not legal advice, compliance certification or sanctions screening.

`RedCap-00 v1.2.0 | Evidence-capped scoring`

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 2, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 2 Treasury reroute: **Score 4, Confidence Low**

## Score

**Verdict: PASS.** All four Move 2 answers are D/E3, so the provisional score is 4. The evidence average is 3.0, so the evidence-average cap does not apply, and Q1 is D, so the prerequisite cap does not apply. The user reported that the E3 claims have no month/year, log or CAPA, so the consistency check fails and confidence drops to Low. The packet shows exactly 4 and Low, and Turn 2 repeats them unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
