# redcap-00 R6a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-18 10:41 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R6: reference.md 3.1 "the mean of its evidence scores (Section 2: E0=0, E1=1, E2=2, E3=3) ... not rounded"

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: evidence average 1.75 is below 2: cap applies

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E1. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# RedCap-00 Output Packet: Larkspur Chemical Supply (fictional)

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers, consistency checks recorded).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Self-estimated worst-case impact is about USD 2 million, with no more than 2,000 people affected.
- **Tier-1 scope summary:**
  - Specialty chemicals B2B distributor with about 400 staff, three warehouses in one country and about 300 business customers.
  - Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers A–D map to 1–4.** A means none, unknown or ad hoc. B means partial or informal. C means documented, owned and repeatable but not recently tested. D means tested in the last 12 months with logs and CAPA, with viable alternates.
- **Evidence levels map to 0–3.** E0 means no evidence. E1 means verbal only. E2 means a named artifact with an owner role. E3 means exercised in the last 12 months with a log and a CAPA.
- **Provisional score.** The mean of the four answers is rounded to the nearest whole number, with exact halves rounding down. A score of 0 (Unknown/Insufficient data) applies only if 3 or more of the 4 answers are A at E0.
- **Caps.** A move whose evidence average is below E2 is capped at 2. A move whose prerequisite question is answered A is also capped at 2.
- **Confidence.** High requires more than half of answers at E3. Medium requires more than half at E2 or E3, with at least one E3. Both require the consistency check to pass. Otherwise confidence is Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | **3** | **Low** | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | **3** | **Low** | 0 | 0 | 4 | 0 |
| 3 Data switchboard | **3** | **Low** | 0 | 0 | 4 | 0 |
| 4 Substitution | **2** (capped) | **Low** | 0 | 1 | 3 | 0 |
| 5 Market exit | **3** | **Low** | 0 | 0 | 4 | 0 |

**Move 1: Safe pause**
- All four answers are C, giving a provisional score of 3. The evidence average is exactly 2.0, so the evidence cap does not apply. Q1 is not A, so the prerequisite cap does not apply.
- Confidence is Low because there are no E3 answers, so neither High nor Medium is reachable. The consistency check passed (approver: Operations Director; artifacts in the quality document system).

**Move 2: Treasury reroute**
- All four answers are C, giving a provisional score of 3. The evidence average is 2.0, and Q1 (alternate banks and rails) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passed (approver: CFO with Treasurer as backup; artifacts in the treasury system).

**Move 3: Data switchboard**
- All four answers are C, giving a provisional score of 3. The evidence average is 2.0, and Q1 (data flow map) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passed (approver: CIO; artifacts in the IT service management tool).

**Move 4: Substitution**
- The provisional score is 3, but the evidence average is (1+2+2+2)/4 = 1.75, which is below E2. **The move is therefore capped at 2.** Q2 (qualified alternates) is C, so the prerequisite cap does not apply.
- Q1 claims a ranked single-point-of-failure list (C) but at E1 (verbal only, no named artifact or owner). That mismatch is what triggers the cap. Confidence is Low because there are no E3 answers. The consistency check passed (approver: COO; artifacts in the procurement system).

**Move 5: Market exit**
- All four answers are C, giving a provisional score of 3. The evidence average is 2.0, and Q1 (exit plan) is C, so no cap applies.
- Confidence is Low because there are no E3 answers. The consistency check passed (approver: CEO; artifacts in the board portal).

## 4) Evidence Index

*These are artifact categories only, not content.*

**Move 1: Safe pause**
- Stop authority matrix: **Documented**
- Safety and continuity checklist with rollback plan: **Documented**
- Internal, customer and regulator communication templates: **Documented**
- Contractual suspension clause summary: **Documented**
- Decision log: **Unknown**
- Resume plan: **Unknown**
- Exercise log and CAPA record: **Unknown**

**Move 2: Treasury reroute**
- Alternate bank and rail register (pre-cleared): **Documented**
- Freeze or hold playbook: **Documented**
- Counterparty trigger and escalation definitions: **Documented**
- 72-hour execution plan: **Documented**
- KYC/KYB bundle: **Unknown**
- Treasury delegation and backup record: **Unknown**
- Exercise log and CAPA record: **Unknown**

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): **Documented**
- Transfer mechanism options map: **Documented**
- Segmentation, localization and shutdown runbook: **Documented**
- Privileged and emergency access logging description: **Documented**
- Subprocessor list: **Unknown**
- Stop-cleanly retention and deletion procedure: **Unknown**
- Exercise log and CAPA record: **Unknown**

**Move 4: Substitution**
- Ranked Tier-1 single-point-of-failure list: **Claimed**
- Qualified alternates register: **Documented**
- Portability or failover plan: **Documented**
- Substitution and portability rights summary: **Documented**
- Logistics reroute plan: **Unknown**
- Cutover gate checklist: **Unknown**
- Exercise log and CAPA record: **Unknown**

**Move 5: Market exit**
- Exit plan (ops, data, people, comms, support): **Documented**
- Termination and unwind path summary: **Documented**
- Customer obligations and support plan: **Documented**
- Data and people plan: **Documented**
- Distributor/JV obligations map: **Unknown**
- Regulator and customer comms approval workflow: **Unknown**
- Tabletop log and CAPA record: **Unknown**

## 5) 72-Hour Breakpoints

1. **0–6 hours | Move 1 | Comms approval delay.** Customer and regulator templates exist but are not pre-approved with a workflow (Q3 = C, not D), so the first holding statement to about 300 customers stalls in drafting and sign-off while orders fail. *(From answers, not exercised.)*
2. **6–24 hours | Move 2 | Operational infeasibility.** Ability to execute the reroute within 72 hours is rated "likely," not "proven by exercise" (Q4 = C), so whether payments can actually be released and collected without ERP data is untested at the point the switch decision is due. *(From answers, not exercised.)*
3. **0–6 hours | Move 3 | Operational infeasibility.** The segmentation and shutdown runbook exists but has not been tested (Q3 = C), so containment steps in a live ransomware event may fail or take longer than planned. *(From answers, not exercised.)*
4. **6–24 hours | Move 4 | Missing artifact.** The ranked single-point-of-failure list is verbal only (Q1 at E1), so the team cannot quickly confirm which suppliers, lanes and systems to substitute first while the ERP is down. *(From answers, not exercised.)*
5. **24–72 hours | Move 5 | Missing gate.** The exit plan is documented but has never been run as a tabletop (Q1 = C), so the decision gates for unwinding affected customer or partner commitments are unvalidated if the outage extends. *(From answers, not exercised.)*

## 6) Top Blockers and Fixes

**1. Single-point-of-failure list is verbal only (Move 4, Q1)**
- **Evidence gap:** E1. No named artifact or owner role, which caps Move 4 at 2.
- **Minimal fix (2 weeks):** Write the ranked Tier-1 list (ERP, house bank, two suppliers, logistics provider, order portal), assign an owner role and store it in the procurement system.
- **Proper fix (6–12 weeks):** Review it quarterly with ranking criteria and link each entry to its alternate and failover plan.
- **Owner role:** COO

**2. Ransomware containment runbook untested (Move 3, Q3)**
- **Evidence gap:** E2 only. No month/year, log or CAPA.
- **Minimal fix (2 weeks):** Walk through the runbook against the ERP-outage scenario and record the gaps found.
- **Proper fix (6–12 weeks):** Run a technical simulation with logged outcomes and an opened CAPA to reach E3.
- **Owner role:** CIO

**3. Emergency access logging not tested (Move 3, Q4)**
- **Evidence gap:** Documented but not exercised. The audit trail during the outage is unproven.
- **Minimal fix (2 weeks):** Confirm the emergency access procedure and where its logs are kept if the ERP is unavailable.
- **Proper fix (6–12 weeks):** Test emergency access with audit-trail review and a CAPA.
- **Owner role:** CIO

**4. Comms templates not pre-approved (Move 1, Q3)**
- **Evidence gap:** C/E2. No approval workflow or named owners per template.
- **Minimal fix (2 weeks):** Pre-approve a customer holding statement and an internal notice for an ERP outage, and name the sign-off roles.
- **Proper fix (6–12 weeks):** Build an approval workflow with backups and counsel review of regulator-facing templates.
- **Owner role:** Operations Director, with a communications lead

**5. Continuity checklist and rollback untested for manual operation (Move 1, Q2)**
- **Evidence gap:** No test. It is Unknown whether the warehouses can pick, ship and track hazardous goods without the ERP.
- **Minimal fix (2 weeks):** Confirm that the offline or manual fallback steps and the safety checks are listed in the checklist.
- **Proper fix (6–12 weeks):** Drill manual operation at one warehouse, with logs and a CAPA.
- **Owner role:** Operations Director

**6. 72-hour treasury execution "likely," not proven (Move 2, Q4)**
- **Evidence gap:** C/E2. There is no exercise evidence.
- **Minimal fix (2 weeks):** Map payment runs and collections that depend on ERP data and define manual alternatives.
- **Proper fix (6–12 weeks):** Run a reroute exercise with timestamps and a CAPA.
- **Owner role:** CFO

**7. Alternate rails pre-cleared but untested (Move 2, Q1)**
- **Evidence gap:** Viability within 72 hours is unproven.
- **Minimal fix (2 weeks):** Confirm the pre-clearance status and activation steps with the alternate provider at a summary level only.
- **Proper fix (6–12 weeks):** Run a low-value test of the reroute path with evidence retained.
- **Owner role:** Treasurer

**8. Alternates and failover plan not proven viable within 72 hours (Move 4, Q2–Q3)**
- **Evidence gap:** C/E2. The plans are not tested in the last 12 months.
- **Minimal fix (2 weeks):** For each Tier-1 dependency, record the time-to-activate and the activation contact role.
- **Proper fix (6–12 weeks):** Test the ERP failover or restore and one supplier or logistics substitution, with logs and a CAPA.
- **Owner role:** COO and CIO

**9. Single approver for Moves 1, 3, 4 and 5**
- **Evidence gap:** The consistency checks named one approver each. Backups were named only for Move 2.
- **Minimal fix (2 weeks):** Name a backup approver role for each move and record it in the authority matrix.
- **Proper fix (6–12 weeks):** Exercise the delegation in a drill and log it.
- **Owner role:** CEO

**10. Artifact accessibility during the outage**
- **Evidence gap:** Artifacts sit in the quality document system, treasury system, IT service management tool, procurement system and board portal. It is Unknown whether these stay available if the ERP environment is compromised.
- **Minimal fix (2 weeks):** Confirm each system's dependency on the ERP and identity infrastructure, and keep an offline copy of the critical runbooks.
- **Proper fix (6–12 weeks):** Set up a tested "break-glass" evidence pack that is accessible without the primary systems.
- **Owner role:** CIO

## 7) 30/60/90-Day Plan

**Workstream A: Evidence uplift and Move 4 cap removal**
- **Outcome:** Move 4 evidence average at or above E2, and every Tier-1 dependency linked to a documented alternate with a time-to-activate.
- **Tasks:**
  - Days 0–30: Document the ranked single-point-of-failure list.
  - Days 0–30: Assign owner roles and storage locations.
  - Days 30–60: Add time-to-activate for each alternate.
  - Days 30–60: Link substitution rights summaries to each Tier-1 vendor.
  - Days 60–90: Set up a quarterly review cadence.
- **Gates:**
  - The list exists as a named artifact with an owner role.
  - Each Tier-1 entry has an alternate and an activation time recorded.
- **Owner roles:** COO, Procurement Lead, CIO
- **Stop rule:** Pause if any alternate cannot be confirmed as viable within 72 hours. Record it as a gap rather than claiming it.

**Workstream B: Ransomware exercise program (E2 to E3)**
- **Outcome:** At least one E3 answer each in Moves 1, 2 and 3 within 90 days, with logs and CAPAs.
- **Tasks:**
  - Days 0–30: Run the 45-minute drill (Section 8).
  - Days 30–60: Test the containment runbook and emergency access logging.
  - Days 30–60: Run a manual warehouse operations drill at one site.
  - Days 60–90: Run a treasury reroute exercise.
  - Days 60–90: Track CAPAs to closure.
- **Gates:**
  - Each exercise has a dated log and at least one CAPA.
  - CAPA owners are named, with due dates.
- **Owner roles:** CIO, Operations Director, CFO
- **Stop rule:** Stop any live test that risks production, safety or customer data. Revert to tabletop format.

**Workstream C: Authority, comms and artifact access**
- **Outcome:** Backup approvers for all five moves, pre-approved outage comms, and critical artifacts accessible without primary systems.
- **Tasks:**
  - Days 0–30: Name backup approvers.
  - Days 0–30: Pre-approve the customer holding statement.
  - Days 30–60: Map artifact systems' dependencies on the ERP and identity infrastructure.
  - Days 30–60: Create an offline evidence pack.
  - Days 60–90: Exercise the delegation and comms workflow.
- **Gates:**
  - The authority matrix shows a primary and a backup for every move.
  - The offline pack is retrieved successfully in the drill.
- **Owner roles:** CEO, Operations Director, CIO, communications lead
- **Stop rule:** Stop and route to counsel any comms template that makes regulator-facing commitments before review.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator
- Operations Director (Move 1 approver)
- CFO and Treasurer (Move 2)
- CIO (Move 3)
- COO (Move 4)
- CEO (Move 5 and overall)
- Communications lead
- Scribe

**Agenda**

| Time | Phase | Focus |
|---|---|---|
| 0–5 min | Brief | ERP encrypted, five-day outage assumed. Ground rules: no sensitive data. |
| 5–15 min | 0–6 hours | What pauses? Who authorizes? Which safety checks apply to hazardous goods in transit and storage? Draft the first holding statement. |
| 15–25 min | 6–24 hours | Choose the switch paths: payment rail, manual order intake vs. portal, logistics handoff, data containment posture. |
| 25–35 min | 24–72 hours | Decide what is executed, what is monitored and what evidence is captured. |
| 35–45 min | Hot wash | Breakpoints and CAPAs. |

**Decisions to log**
- Pause scope and approver
- Containment action and approver
- Treasury reroute go/no-go
- First substitution activated
- Customer comms release time
- Escalation to counsel and executives (time and role)

**Evidence to capture**
- Timestamps
- Roles present
- Artifacts actually retrieved, and from where
- Artifacts that could not be retrieved
- Decisions made versus deferred

**CAPA prompt**
- "Which step stalled longest, which artifact or authority was missing, who owns the fix, and by what date?"
- Open at least one CAPA per move tested.

## 9) Escalations

**ESCALATE**

1. **Criminal activity (ransomware).** The scenario is a criminal cyberattack.
   - **Path:** CEO and board chair, with General Counsel or outside counsel, CIO/CISO and the cyber insurer contact role.
   - **Questions for counsel:** Law enforcement engagement, notification obligations in the relevant jurisdiction (Unknown) and preservation of evidence.
2. **Sanctions considerations if ransom payment is ever considered.** No determination is made here.
   - **Path:** Route any payment discussion to counsel before any action.
   - **Questions for counsel:** Sanctions screening of the threat actor and payment restrictions.
3. **Potential physical safety (conditional).** It is Unknown whether hazardous-goods tracking, safety data access or shipment documentation depends on the ERP.
   - **Path:** If it does, escalate to the Operations Director and the safety lead immediately in the 0–6 hour window.

**Not triggered from the information provided**
- **Impact thresholds:** USD 2 million is below USD 10 million, and 2,000 people is below 100,000.
- **Regulator inquiry:** Unknown.
- **Export controls:** Unknown.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifacts were reviewed, and "Documented" labels reflect claims of E2.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification and reporting questions are left to counsel.
- **Scenario simplification:** One ransomware outage of fixed duration is assumed. Concurrent failures (bank, supplier, portal) are not modelled.
- **Fast Baseline coverage:** Q5–Q7 themes were not assessed and appear as Unknown in the Evidence Index.
- **Breakpoints:** These are inferred from answers, not from an exercise.
- **Impact estimates:** Impact and people-affected figures are user estimates and were not verified.
- **Confidence:** Low confidence on all moves reflects the absence of any E3 evidence, not a judgement of document quality.
- **Not advice or certification:** This packet is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 2 (capped), Confidence Low.

## Score

**Verdict: PASS.** The packet was produced in Turn 1. Move 4's evidence average is 1.75 (E1, E2, E2, E2), below 2, so the cap to 2 applies. The provisional score is 3 and Q2 is not A, so no prerequisite cap applies. The consistency check passes, but there are no E3 answers, so confidence is Low. The packet reports score 2 and Low. Turn 2 repeats these values unchanged, and no fail indicator appears.

---

Final Liability rests with the Human.
