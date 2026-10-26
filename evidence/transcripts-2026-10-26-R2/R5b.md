# redcap-00-r2 R5b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:42 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R5: reference.md 4 "Raising the evidence level of any answer never lowers confidence."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: a profile stronger on every axis is also Medium, not Low as under the old majority wording

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: D, E3. Q2 Qualified alternates: D, E3. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Optionality Self-Check: Output Packet

## 1) Snapshot

- **Jurisdiction:** Unknown. No legal or compliance determinations are made.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days.
- **Tier-1 scope summary:**
  - Larkspur Chemical Supply (fictional), specialty chemicals B2B distribution
  - Three warehouses in one country, about 300 business customers, about 400 staff
  - Tier-1 systems and vendors: cloud ERP, house bank, two bulk suppliers, one logistics provider, customer order portal
  - Your estimate: about USD 2m worst-case impact and no more than 2,000 people affected. Both are below the escalation thresholds (USD 10m and 100,000 people).

## 2) How Scoring Works

- **A–D pattern scores (A=1, B=2, C=3, D=4):** A is none or unknown, B is partial or informal, C is documented and owned, D is tested in the last 12 months with logs and CAPA. The move's provisional score is the average of its answers, and exact halves round down (3.5 → 3).
- **Evidence levels (E0=0, E1=1, E2=2, E3=3):** E0 is no evidence, E1 is verbal only, E2 is a named artifact with an owner role, and E3 is tested within 12 months with a log and CAPA.
- **Conservative caps:** A move's score is capped at 2 if its evidence average is below 2, or if its prerequisite question is answered A.
  - A move scores 0 (Unknown/Insufficient data) only if more than half of its answers are A at E0.
- **Confidence:**
  - High: more than half the answers at E3.
  - Medium: more than half at E2 or E3, plus at least one E3.
  - Low: otherwise.
  - Both High and Medium also require the move's consistency check to pass.
- **Consistency check:** Any E3 answer needs a dated exercise within 12 months, a log and a CAPA. Any E2 or E3 answer needs a named approver role and artifact location. If the check fails, confidence drops to Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 3 | Low | 0 | 0 | 4 | 0 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Medium | 0 | 0 | 2 | 2 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (3, Low)**
- All four answers are C at E2, so the average is 3.0. The evidence average is 2.0, so the cap does not apply, and Q1 is not A, so there is no prerequisite cap.
- Confidence is Low because there are no E3 answers. The consistency check passes (approver: Operations Director; artifacts in the quality document system), but the stop authority and pause checklist have never been exercised.

**Move 2: Treasury reroute (3, Low)**
- All four answers are C at E2, so the average is 3.0 with no caps. Alternate rails are pre-cleared (Q1 C), so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. Your 72-hour execution answer is "likely" (Q4 C), not proven by exercise. The check passes (approver: CFO, Treasurer as backup; artifacts in the treasury system).

**Move 3: Data switchboard (3, Low)**
- All four answers are C at E2, so the average is 3.0 with no caps. The data flow map is documented (Q1 C), so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers. The segmentation and shutdown runbook and the emergency access logging are untested, which matters most in a ransomware scenario. The check passes (approver: CIO; artifacts in the ITSM tool).

**Move 4: Substitution (3, Medium)**
- The answers (D, D, C, C) average 3.5, which rounds down to 3. The evidence average is 2.5, so there is no cap, and Q2 is D, so there is no prerequisite cap.
- Confidence is Medium:
  - All four answers are E2 or E3, including two at E3.
  - Two of four E3 answers is not more than half, so High is not reached.
  - The check passes: the April 2026 drill is within 12 months, with a drill log and a CAPA in the risk system, and the COO is the approver.

**Move 5: Market exit (3, Low)**
- All four answers are C at E2, so the average is 3.0 with no caps. The exit plan is documented (Q1 C), so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers and the exit plan has never had a tabletop test. The check passes (approver: CEO; artifacts in the board portal).

## 4) Evidence Index

Labels: Unknown (not supplied), Claimed (E1), Documented (E2), Tested (E3). The items are artifact categories only.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Pause safety and continuity checklist with rollback plan: Documented
- Holding-statement templates (internal, customer, regulator): Documented
- Contract suspension clause summary: Documented
- Decision log: Unknown
- Resume plan and gates: Unknown
- Escalation path under conflict: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail register (pre-cleared): Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury delegation and backup schedule: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options summary (no determinations): Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging procedure: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4: Substitution**
- Ranked Tier-1 single-point-of-failure list: Tested
- Qualified alternates register: Tested
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Drill log and CAPA record (April 2026): Tested
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5: Market exit**
- Exit plan (legal, ops, data, people, comms, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

Moves 1, 2, 3 and 5 had all answers tied at C/E2. The breakpoint for each was chosen as the answer most exposed in a five-day ERP outage.

- **Move 1, 0–6 hours, comms approval delay:** Communications readiness is C (templates exist but are not pre-approved). The first holding statement to customers and staff would wait on ad hoc sign-off while orders and shipments stall. *(from answers, not exercised)*
- **Move 2, 6–24 hours, operational infeasibility:** Execution within 72 hours is C ("likely", not proven). Alternate rails are pre-cleared but have never been used under outage conditions, so payments to suppliers and the logistics provider may not move when needed. *(from answers, not exercised)*
- **Move 3, 0–6 hours, operational infeasibility:** The segmentation and shutdown runbook is C (exists, untested). An untested containment sequence during live ransomware may fail or isolate the wrong systems, including the order portal's links to the ERP. *(from answers, not exercised)*
- **Move 4, 6–24 hours, missing gate:** The portability or failover plan is C/E2 (documented, not tested in the last 12 months). The April 2026 drill tested alternates and the SPOF list, not ERP failover, so no proven gate confirms a cutover is safe to execute. *(from answers, not exercised)*
- **Move 5, 24–72 hours, missing gate:** Termination and unwind paths are C (documented, not rehearsed). If the outage forces exit from a customer segment or supplier relationship, untested triggers and notices would stall the decision at board level. *(from answers, not exercised)*

## 6) Top Blockers and Fixes

1. **Stop authority never exercised (Move 1 Q1)**
   - **Evidence gap:** E2 only; no logged delegated use.
   - **Minimal fix (2 weeks):** Confirm the authority matrix covers ERP-down conditions and name backups.
   - **Proper fix (6–12 weeks):** Exercise the delegated stop in a drill with a timestamped log and CAPA.
   - **Owner:** Operations Director
2. **Holding statements not pre-approved (Move 1 Q3)**
   - **Evidence gap:** Templates exist, but there is no approval workflow.
   - **Minimal fix:** Pre-approve outage holding statements for staff, customers and suppliers.
   - **Proper fix:** Build an approval workflow with named approvers and backups, then test it in a drill.
   - **Owner:** Communications Lead, with Operations Director
3. **Suspension basis not mapped to Tier-1 contracts (Move 1 Q4)**
   - **Evidence gap:** Clause summary only; no trigger or notice mapping.
   - **Minimal fix:** List the Tier-1 counterparties (two suppliers, logistics provider, ERP vendor) and the notice owner for each.
   - **Proper fix:** Map triggers and notice steps per Tier-1 contract, with questions for counsel.
   - **Owner:** Legal/Contracts Lead
4. **Alternate rails never tested (Move 2 Q1)**
   - **Evidence gap:** Pre-cleared, but no reroute evidence.
   - **Minimal fix:** Confirm the reroute steps work without ERP-generated payment files.
   - **Proper fix:** Run a controlled test reroute and log the outcome and CAPA.
   - **Owner:** Treasurer
5. **72-hour execution unproven (Move 2 Q4)**
   - **Evidence gap:** "Likely" is not evidence.
   - **Minimal fix:** Walk through the 72-hour treasury timeline with the CFO and Treasurer.
   - **Proper fix:** Run a timed treasury exercise under a simulated ERP outage and record it at E3.
   - **Owner:** CFO
6. **Shutdown runbook untested (Move 3 Q3)**
   - **Evidence gap:** E2 runbook with no exercise record.
   - **Minimal fix:** Review the runbook against the ERP and order portal dependencies.
   - **Proper fix:** Run a technical tabletop or isolated simulation, then log it and open a CAPA.
   - **Owner:** CIO
7. **Emergency access logging untested (Move 3 Q4)**
   - **Evidence gap:** Documented, with no audit-trail test.
   - **Minimal fix:** Confirm break-glass logging works if the ERP and identity services are degraded.
   - **Proper fix:** Test the emergency access procedure end to end and retain the audit evidence.
   - **Owner:** IT Security Lead
8. **ERP failover plan untested (Move 4 Q3)**
   - **Evidence gap:** The April 2026 drill did not cover failover.
   - **Minimal fix:** Define manual order-to-ship and invoicing fallback steps for a five-day outage.
   - **Proper fix:** Test failover or manual operations in the next drill, with a log and CAPA.
   - **Owner:** COO, with CIO
9. **Substitution rights only summarized (Move 4 Q4)**
   - **Evidence gap:** Not mapped per Tier-1 vendor.
   - **Minimal fix:** Flag which Tier-1 vendor summaries cover substitution or portability.
   - **Proper fix:** Map the rights per Tier-1 vendor and refer open questions to counsel.
   - **Owner:** Procurement Lead
10. **Exit and customer support plans unrehearsed (Move 5 Q1–Q3)**
    - **Evidence gap:** E2 only; no tabletop.
    - **Minimal fix:** Brief the board on exit triggers and the customer support plan owners.
    - **Proper fix:** Run a tabletop on exit and unwind, then log it and open a CAPA.
    - **Owner:** CEO, with Commercial Director

## 7) 30/60/90-Day Plan

**Workstream 1: Ransomware pause and containment (Moves 1 and 3)**
- **Outcome:** The stop authority, holding statements, shutdown runbook and emergency access are exercised and recorded at E3.
- **Tasks:**
  - (30 days) Pre-approve the holding statements.
  - (30 days) Name backups in the authority matrix.
  - (60 days) Run the 45-minute drill (Section 8) on the ERP ransomware scenario.
  - (60 days) Test break-glass access logging.
  - (90 days) Close the drill CAPAs and re-score Moves 1 and 3.
- **Gates:**
  - The drill log is stored in the quality document system and the ITSM tool.
  - At least one CAPA is opened per move.
- **Owner roles:** Operations Director, CIO, IT Security Lead, Communications Lead
- **Stop rule:** Pause the workstream if the drill would touch production systems without a CIO-approved isolation plan.

**Workstream 2: Treasury and operations continuity (Moves 2 and 4)**
- **Outcome:** Treasury reroute and ERP failover or manual operations are proven within 72 hours.
- **Tasks:**
  - (30 days) Document payment execution without ERP outputs.
  - (30 days) Define the manual order-to-ship fallback.
  - (60 days) Run a controlled reroute test.
  - (60 days) Exercise the failover plan.
  - (90 days) Map substitution rights per Tier-1 vendor.
- **Gates:**
  - The reroute test is logged, with a CAPA, in the treasury system.
  - The failover exercise is logged in the risk system.
  - The CFO and COO sign off.
- **Owner roles:** CFO, Treasurer, COO, Procurement Lead
- **Stop rule:** Stop any live payment test if counterparty or reconciliation controls cannot be confirmed in advance.

**Workstream 3: Contract and exit readiness (Moves 1 Q4 and 5)**
- **Outcome:** Contract triggers and notices are mapped and the exit plan is tabletop-tested.
- **Tasks:**
  - (30 days) List the Tier-1 contracts and notice owners.
  - (60 days) Map suspension and termination triggers, with questions for counsel.
  - (60 days) Run an exit and unwind tabletop.
  - (90 days) Update the customer support plan from the CAPAs.
- **Gates:**
  - Counsel review of the open questions is complete.
  - The tabletop log is in the board portal.
- **Owner roles:** CEO, Legal/Contracts Lead, Commercial Director
- **Stop rule:** Stop the workstream if mapping would require sharing non-public contract text outside approved legal channels.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (Risk Lead)
- Operations Director (stop authority)
- CIO and IT Security Lead
- CFO and Treasurer
- COO
- Communications Lead
- Scribe

**Agenda**
- **0–5 minutes:** Scenario injection. The ERP is encrypted, the order portal is degraded, and restoration is estimated at five days.
- **5–15 minutes:** What is paused, who authorizes it, which safety checks must pass, and which holding statement goes out.
- **15–30 minutes:** Which path is chosen:
  - Containment and data posture
  - Treasury reroute
  - Manual order fulfilment and logistics
- **30–40 minutes:** What gates must pass and who signs off for execution through 72 hours.
- **40–45 minutes:** Capture the breakpoints and assign CAPAs.

**Decisions to log**
- Pause decision and approver
- Holding statement release
- Containment and shutdown scope
- Payment reroute go or no-go
- Manual-operations cutover
- Escalation to counsel or executives

**Evidence to capture**
- Timestamped decision log
- Approver roles
- Artifacts referenced, with their locations
- Gaps found
- Time each decision took against target

**CAPA prompt**
- For each stall: "What failed (authority, artifact, alternate, gate, comms, feasibility)? Who owns the fix? What is the due date? What evidence will close it?"

## 9) Escalations

The financial (about USD 2m) and population (no more than 2,000) thresholds are not met. Some triggers are inherent to the scenario:

- **ESCALATE: criminal matter.** Ransomware is a criminal act. Escalate to the CEO, General Counsel or external counsel, and the CIO. Ask counsel about law-enforcement engagement and evidence preservation.
- **ESCALATE (conditional): sanctions.** If ransom payment is ever considered, refer it to counsel before any action. This tool makes no sanctions determination.
- **ESCALATE (conditional): physical safety.** If the outage impairs hazardous-materials handling, safety data access or storage segregation at the warehouses, escalate to the Operations Director and the EHS lead immediately.
- **Question for counsel (jurisdiction Unknown):** Do any breach, regulator or customer notification obligations apply? Treat any regulator contact as an ESCALATE trigger.

**Recommended path:** Incident lead → CIO/COO → CEO → General Counsel or external counsel → Board chair, if criminal, sanctions or safety triggers are confirmed.

## 10) Known Limits + Version

- **Self-report bias:** The answers and evidence levels are as reported and have not been verified.
- **No document validation:** No artifacts were reviewed. E2 and E3 labels rest on the role and location claims you supplied.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so no legal, compliance or notification conclusions are drawn.
- **Scenario simplification:** A single five-day ERP outage does not cover cascading failures such as the cloud provider, house bank or logistics provider failing at the same time.
- **Fast Baseline only:** Q5–Q7 per move and the mini tabletop were not run, so those artifacts are listed as Unknown and the breakpoints were not exercised.
- **Move 4 limit:** Its Medium confidence rests on one drill (April 2026), which did not cover failover (Q3) or substitution rights (Q4).
- **Impact estimates:** The USD 2m and 2,000-person estimates are yours. If they are exceeded, the escalation status changes.
- **Not certification:** This is informational only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: **Score 3, Confidence Medium**

## Score

**Verdict: PASS.** The packet was produced in Turn 1 and reports Move 4 as score 3 with confidence Medium. Both values match the reference rules recomputed independently. The pattern average of 3.5 rounds down to 3. No cap applies. Confidence is Medium because 2 of 4 E3 answers is not more than half, all 4 answers are at E2 or E3, and the consistency check passes. Turn 2 repeats the same values without change. No fail indicator appears.

---

Final Liability rests with the Human.
