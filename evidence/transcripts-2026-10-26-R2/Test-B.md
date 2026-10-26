# redcap-00-r2 Test-B

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:41 KST · **max_tokens:** 16000

**Rule:** tests.md section 2, cap enforcement. reference.md section 3: "If the evidence average is below 2 (below E2), cap that move’s score at 2." / "Each move has one prerequisite question. If that question is answered A, cap the move’s score at 2."; section 8.1: "An exact half rounds down"; section 4 confidence rules

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 2 (Treasury reroute) with score 2 and confidence High, and no later turn changes either value. Expected value computed in tests.md: no alternate bank or rail (Q1 A) caps Move 2 at 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: A, E0. Q2 Freeze or hold playbook: D, E3. Q3 Counterparty tripwires: D, E3. Q4 Execute within 72 hours: D, E3.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E2. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions) plus consistency checks.
- **Scenario tested:** Ransomware outage takes the cloud ERP down for five days. You estimate worst-case impact at about USD 2 million and no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distribution
  - About 400 staff
  - Three warehouses in one country
  - About 300 business customers
  - Tier-1 dependencies: cloud ERP, house bank, two bulk suppliers, one logistics provider, customer order portal

## 2) How Scoring Works

- **Answers A–D map to scores 1–4:**
  - A (1) = none, unknown or ad hoc.
  - B (2) = partial or untested.
  - C (3) = documented and owned, with limited or no recent testing.
  - D (4) = tested in the last 12 months with logs and a CAPA (follow-up action).
  - The move average is rounded, with exact halves rounding down.
- **Evidence levels E0–E3 score 0–3:**
  - E0 = none.
  - E1 = verbal only.
  - E2 = named artifact plus owner role.
  - E3 = tested within 12 months, with a log and a CAPA.
- **Caps** (the final score is the lowest applicable value):
  - A move whose evidence average is below 2 is capped at 2.
  - A move whose prerequisite question is answered A is capped at 2.
- **Zero rule:**
  - A move scores 0 ("Unknown/Insufficient data") only if more than half of its answers are A at E0.
  - That means 3 or more of 4 answers in this mode.
- **Confidence:**
  - High = more than half of answers at E3.
  - Medium = more than half at E2 or E3, with at least one E3.
  - Low = otherwise, or whenever the move's consistency check fails.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 2 | High | 1 | 0 | 0 | 3 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1: Safe pause (Score 3, Low)**
- **Score:** All four answers are C/E2, so the provisional score is 3. The evidence average is 2.00, so the evidence cap does not apply. The prerequisite (Q1) is C, so no prerequisite cap applies.
- **Confidence:** The consistency check passes (Operations Director as approver; quality document system as location). Confidence is still Low because there are no E3 answers, so stop authority and the checklists are documented but unexercised.

**Move 2: Treasury reroute (Score 2, High)**
- **Score:** The provisional average is 3.25, which rounds to 3. The evidence average is 2.25, so the evidence cap does not apply. However, the prerequisite Q1 (alternate banks and rails) is A/E0, which caps the score at 2.
- **Confidence:** Confidence is High because three of four answers are E3. The check also passes: exercised April 2026, with a drill log and a CAPA in the risk system, the CFO as approver and the Treasurer as backup.
  - High confidence describes the evidence, not readiness.
  - Q4 says 72-hour execution is "proven by exercise" while Q1 reports no alternate bank. Confirm what path the April 2026 drill actually rerouted to.

**Move 3: Data switchboard (Score 3, Low)**
- **Score:** All four answers are C/E2, giving a provisional score of 3. Neither the evidence cap nor the prerequisite cap applies (Q1 data flow map is C).
- **Confidence:** The check passes (CIO as approver; IT service management tool as location). Confidence is Low because there is no E3 answer.
  - The artifact location may itself be unavailable during a ransomware event. Whether it is unaffected is Unknown.

**Move 4: Substitution (Score 3, Low)**
- **Score:** All four answers are C/E2, giving a provisional score of 3. Neither cap applies (prerequisite Q2 qualified alternates is C).
- **Confidence:** The check passes (COO as approver; procurement system as location). Confidence is Low because there is no E3 answer.
  - "Qualified" alternates are not yet shown to be viable within 72 hours, which is the D standard.
  - The failover plan is untested.

**Move 5: Market exit (Score 3, Low)**
- **Score:** All four answers are C/E2, giving a provisional score of 3. Neither cap applies (prerequisite Q1 exit plan is C).
- **Confidence:** The check passes (CEO as approver; board portal as location). Confidence is Low because there is no E3 answer, so the exit and customer plans are documented but not rehearsed.

## 4) Evidence Index

Each artifact type is labeled with one of four evidence labels:

- **Unknown:** not assessed in Fast Baseline (Q5–Q7), or E0.
- **Claimed:** E1, or named verbally only.
- **Documented:** E2.
- **Tested:** E3.

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator communication templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail list: Unknown
- Freeze or hold playbook: Tested
- Counterparty tripwire definitions: Tested
- 72-hour reroute drill record with CAPA: Tested
- KYC/KYB bundle: Unknown
- Letter of credit and alternate settlement playbook: Unknown
- Treasury authority delegation with backup: Claimed (CFO approver and Treasurer backup were named in the consistency check; Q7 was not assessed)

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4 Substitution**
- Ranked Tier-1 single-point-of-failure list: Documented
- Alternate qualification records: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gate checklist: Unknown

**Move 5 Market exit**
- Exit plan (legal, operations, data, people, communications, support): Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer communications templates with approval workflow: Unknown

## 5) 72-Hour Breakpoints

Moves 1, 3, 4 and 5 have four tied C/E2 answers. For each, the answer most exposed in this scenario was selected.

- **0–6 hours | Move 1 (Q3 Communications readiness, C/E2) | Comms approval delay** (from answers, not exercised)
  - The templates exist but are not pre-approved with a workflow. The first holding statement to 300 customers can therefore stall on approvals while orders and deliveries are paused.
- **6–24 hours | Move 2 (Q1 Alternate banks and rails, A/E0) | Missing alternate** (from answers, not exercised)
  - No alternate bank or rail is identified. If the house bank holds or restricts flows during the incident, there is no path for supplier payments or customer receipts.
- **0–6 hours | Move 3 (Q3 Segmentation and shutdown runbook, C/E2) | Missing artifact** (from answers, not exercised)
  - The runbook is untested, and it is stored in the IT service management tool, whose availability during a ransomware event is Unknown. Containment steps may not be retrievable when they are needed.
- **24–72 hours | Move 4 (Q3 Portability or failover plan, C/E2) | Operational infeasibility** (from answers, not exercised)
  - The ERP failover and manual-operations plan has not been tested. Warehouse picking, dispatch and invoicing may not run for five days without the ERP.
- **24–72 hours | Move 5 (Q3 Customer obligations and support plan, C/E2) | Operational infeasibility** (from answers, not exercised)
  - The support plan is not rehearsed, and its dependence on ERP-held customer and order data is Unknown. Meeting customer obligations during the outage may not be possible.

## 6) Top Blockers and Fixes

1. **No alternate bank or rail (Move 2, Q1)**
   - **Evidence gap:** A/E0; no artifact and no owner.
   - **Minimal fix (2 weeks):** Shortlist candidate alternate banks and rails and assign an owner.
   - **Proper fix (6–12 weeks):** Pre-clear at least one alternate, then exercise a reroute to it with a log and a CAPA.
   - **Owner role:** Treasurer, with CFO approval.

2. **Reroute evidence does not reconcile (Move 2, Q4 D/E3 against Q1 A/E0)**
   - **Evidence gap:** The April 2026 drill record does not show which alternate path was exercised.
   - **Minimal fix (2 weeks):** Review the drill log and record the exercised path and its scope.
   - **Proper fix (6–12 weeks):** Re-baseline the Q1 and Q4 answers and re-run the drill against a genuine alternate.
   - **Owner role:** Treasurer, with Risk Manager.

3. **Stop authority is documented but never exercised (Move 1, Q1)**
   - **Evidence gap:** E2 only; no exercise date, log or CAPA.
   - **Minimal fix (2 weeks):** Confirm delegates and alternates in the authority matrix, and keep an offline copy.
   - **Proper fix (6–12 weeks):** Exercise a pause decision in a tabletop, then log the outcome and open a CAPA.
   - **Owner role:** Operations Director.

4. **Communication templates are not pre-approved (Move 1, Q3)**
   - **Evidence gap:** C/E2; no approval workflow evidenced.
   - **Minimal fix (2 weeks):** Pre-draft an outage holding statement and name the approvers.
   - **Proper fix (6–12 weeks):** Set up a pre-approved template set with a workflow and backup approvers, and test it.
   - **Owner role:** Communications lead, with Operations Director.

5. **Shutdown runbook is untested and possibly unreachable (Move 3, Q3)**
   - **Evidence gap:** E2; the storage location may be affected by the incident.
   - **Minimal fix (2 weeks):** Create an offline or out-of-band copy of the runbook and contact lists.
   - **Proper fix (6–12 weeks):** Test segmentation and shutdown on a Tier-1 system, with a log and a CAPA.
   - **Owner role:** CIO.

6. **Emergency access logging is untested (Move 3, Q4)**
   - **Evidence gap:** E2; no tested audit trail.
   - **Minimal fix (2 weeks):** Verify that break-glass access is logged somewhere independent of the ERP.
   - **Proper fix (6–12 weeks):** Run a drill with an audit trail review and record a CAPA.
   - **Owner role:** CIO, with the Information Security lead.

7. **ERP failover and manual-operations plan is untested (Move 4, Q3)**
   - **Evidence gap:** E2; not tested in the last 12 months.
   - **Minimal fix (2 weeks):** Confirm that manual order, pick and dispatch forms exist offline at all three warehouses.
   - **Proper fix (6–12 weeks):** Run a one-shift manual-operations drill per warehouse, with logs and a CAPA.
   - **Owner role:** COO.

8. **Alternates are qualified, but 72-hour viability is not evidenced (Move 4, Q2)**
   - **Evidence gap:** C/E2; does not meet the D standard.
   - **Minimal fix (2 weeks):** For each bulk supplier and the logistics provider, record whether the alternate could be activated within 72 hours.
   - **Proper fix (6–12 weeks):** Pre-arrange activation steps and confirm 72-hour viability in an exercise.
   - **Owner role:** Procurement Director, with COO.

9. **Customer support plan is not rehearsed (Move 5, Q3)**
   - **Evidence gap:** E2; its dependency on ERP data is Unknown.
   - **Minimal fix (2 weeks):** Keep an offline extract of Tier-1 customer contacts and open orders, with no personal data in this tool.
   - **Proper fix (6–12 weeks):** Rehearse scripts and a communications workflow for an outage longer than 72 hours.
   - **Owner role:** Customer Service Director.

10. **Contract summaries are not mapped to Tier-1 triggers (Move 1, Q4; Move 4, Q4)**
    - **Evidence gap:** C/E2 summaries only, with no Tier-1 trigger or notice mapping.
    - **Minimal fix (2 weeks):** List the Tier-1 contracts and the planning questions for counsel on suspension, notice and substitution.
    - **Proper fix (6–12 weeks):** Have counsel review and map triggers and notices for each Tier-1 contract, at planning level and with no determinations here.
    - **Owner role:** General Counsel, with Procurement.

## 7) 30/60/90-Day Plan

**Workstream A: Treasury alternate path (Move 2)**

- **Outcome:** At least one alternate bank or rail is pre-cleared, and a reroute to it has been exercised.
- **Tasks:**
  - **By day 30:** Reconcile the April 2026 drill scope (Blocker 2) and shortlist alternates.
  - **By day 60:** Pre-clear one alternate and confirm that KYC/KYB bundle readiness is assessed.
  - **By day 90:** Exercise the reroute, log it and open a CAPA.
  - Update the Q1 and Q4 answers with new evidence.
- **Gates:**
  - An alternate is named and owned (day 30).
  - The alternate is pre-cleared (day 60).
  - The drill log and CAPA exist (day 90).
- **Owner roles:** Treasurer (lead), CFO (approver), Risk Manager.
- **Stop rule:** If no alternate is pre-cleared by day 60, escalate to the CEO and pause the remaining tasks until a decision is made.

**Workstream B: Ransomware-ready pause and manual operations (Moves 1, 3, 4)**

- **Outcome:** Larkspur can pause, contain and operate manually for five days without the ERP.
- **Tasks:**
  - **By day 30:** Put offline copies of the authority matrix, shutdown runbook, contact lists and manual operations forms in place.
  - **By day 30:** Verify that emergency access logging is independent of the ERP.
  - **By day 60:** Record 72-hour viability for the alternates of both bulk suppliers and the logistics provider.
  - **By day 90:** Run a manual-operations drill at one warehouse and a shutdown test on one Tier-1 system.
- **Gates:**
  - Offline artifacts are confirmed retrievable without the ITSM tool (day 30).
  - Drill logs exist and CAPAs are opened (day 90).
- **Owner roles:** COO (lead), CIO, Operations Director, Procurement Director.
- **Stop rule:** If any drill shows a safety or continuity checklist gap, stop the drill and fix the checklist before re-running it.

**Workstream C: Communications and evidence uplift (Moves 1, 5; all moves)**

- **Outcome:** Approved outage communications exist, and each move has at least one E3 answer.
- **Tasks:**
  - **By day 30:** Pre-draft the holding statement and name the approvers.
  - **By day 60:** Build the approval workflow with backups and prepare the planning questions for counsel (Blocker 10).
  - **By day 90:** Run the 45-minute drill (Section 8) and re-score in Deepening mode.
- **Gates:**
  - Templates are approved (day 60).
  - The drill is logged with CAPAs (day 90).
  - The re-score is completed (day 90).
- **Owner roles:** Communications lead, Customer Service Director, General Counsel, CEO (approver).
- **Stop rule:** If counsel input is not available by day 60, proceed with internal templates marked "pending counsel review" and do not issue regulator-facing drafts.

## 8) Minimal Drill Script (45 minutes)

- **Roles:**
  - Facilitator (Risk Manager)
  - Operations Director
  - CFO and Treasurer
  - CIO
  - COO
  - Procurement Director
  - Customer Service Director
  - Communications lead
  - Scribe
- **Agenda:**
  - **0–5 minutes:** Scenario brief. The ERP is encrypted on day one, recovery is expected in five days and the order portal is unavailable.
  - **5–15 minutes:** Decide what to pause and who authorizes it. Retrieve the authority matrix and shutdown runbook without the ERP or the ITSM tool.
  - **15–25 minutes:** Treasury. Decide how supplier payments and customer receipts continue if the house bank restricts flows.
  - **25–35 minutes:** Manual operations and alternates. Decide which bulk supplier or logistics alternates you would activate, and through what gates.
  - **35–42 minutes:** Customer communications. Approve the first holding statement and the update at the 72-hour mark.
  - **42–45 minutes:** Capture CAPAs.
- **Decisions to log:**
  - Pause decision and approver
  - Containment and shutdown decision
  - Treasury path chosen
  - Alternates activated or deferred
  - Holding statement approval time
  - Questions for counsel and executive escalation
- **Evidence to capture:**
  - Timestamps
  - Approver roles
  - Artifacts retrieved, and whether each was available offline
  - Gates checked
  - Stalls observed
- **CAPA prompt:** "Which decision took longest or could not be made, what artifact or authority was missing, who owns the fix, and by what date?"

## 9) Escalations

**ESCALATE.** Triggers identified from the information you provided:

- **Criminal:** Ransomware is a criminal extortion event.
  - **Planning questions for counsel:** law enforcement engagement, evidence preservation, and the incident's notification posture.
- **Sanctions (questions for counsel only; no determination made):** Any consideration of ransom payment may raise sanctions questions about the counterparties involved.
  - This tool does not assess or advise on payment.
  - Refer any such question to counsel and the board.
- **Physical safety:** For a specialty chemicals distributor, an ERP outage may affect access to hazardous-materials handling, storage and shipping documentation.
  - Safety checks must gate any pause, resume or manual shipping decision.

**Not triggered from your stated estimates:** impact above USD 10 million (you estimate about USD 2 million), more than 100,000 people affected (you estimate no more than 2,000), and regulator inquiry (none stated).

**Recommended escalation path:**

1. The incident lead (CIO and Operations Director) notifies the CEO and General Counsel within the 0–6 hour window.
2. General Counsel engages external counsel on criminal, notification and sanctions-related questions for the relevant jurisdiction, which is currently Unknown.
3. The CEO briefs the board chair.
4. The EHS or Safety lead confirms hazardous-materials controls before any operational restart.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported and were not verified.
- **No document validation:** No artifacts were reviewed. "Documented" and "Tested" reflect your claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so no legal, notification or compliance conclusions are drawn.
- **Scenario simplification:** A single five-day ERP outage does not model concurrent failures such as bank, supplier or portal outages, or data exfiltration.
- **Fast Baseline only:** Q5–Q7 were not assessed for any move, so those artifacts show as Unknown and no tabletop was run. Deepening mode is available on request.
- **Unresolved inconsistency:** Move 2's High confidence coexists with its prerequisite cap. The Q1 and Q4 relationship should be reconciled before relying on that move.
- **Artifact availability:** It is Unknown whether the artifact locations (ITSM tool, procurement system, quality document system) remain reachable during ransomware.
- **Impact estimates:** These are your figures. If impact exceeds USD 10 million or 100,000 people, additional escalation triggers apply.
- **Scope of this output:** It is informational planning output only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 2, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 2 Treasury reroute: Score 2, Confidence High.

## Score

**Verdict: PASS.** The Scorecard reports Move 2 at score 2 and confidence High. Both values match an independent recomputation: the prerequisite cap from Q1=A lowers the provisional 3 to 2, and 3 of 4 E3 answers with a passing consistency check gives High. Turn 2 repeats the same values unchanged, and no fail indicator appears.

---

Final Liability rests with the Human.
