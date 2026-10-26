# redcap-00-r1 R1a

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:28 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R1: reference.md 8.1 "An exact half rounds down, the conservative direction: 2.5 → 2 and 3.5 → 3."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 2 and confidence Low, and no later turn changes either value. Expected value computed in tests.md: an exact half (2.5) rounds down to 2

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: B, E2. Q2 Qualified alternates: B, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E2.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; no E3 claims. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

**Pre-packet note:** Safety confirmation and intake are received, and Fast Baseline (20 answers) and the consistency checks for all 5 moves are complete. Deepening (Q5–Q7 for each move plus the mini tabletop) is available if you want it later. Since you selected Fast Baseline, the packet follows.

---

## 1) Snapshot

- **Jurisdiction:** Unknown.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 answers).
- **Scenario tested:** A ransomware outage takes the cloud ERP down for 5 days. The estimated worst-case impact is about USD 2m, with no more than 2,000 people affected. The outage runs longer than the 72-hour execution window.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) distributes specialty chemicals B2B. It has 3 warehouses in one country, about 300 business customers and about 400 staff. The Tier-1 dependencies are the cloud ERP, the house bank, two bulk suppliers, one logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answers:** Each answer is scored A=1 (none or ad hoc), B=2 (partial or untested), C=3 (documented and owned, not recently tested) or D=4 (tested in the last 12 months, with logs, CAPA and viable alternates).
- **Evidence:** Each answer is also scored for evidence: E0=0 (none), E1=1 (verbal), E2=2 (named artifact plus owner role) or E3=3 (exercised in the last 12 months, with a log and a CAPA).
- **Move score:** The move score is the mean of its answer scores. An exact half rounds down. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Caps:** A move is capped at 2 if its evidence average is below 2. It is also capped at 2 if its prerequisite question is answered A.
- **Confidence:** High needs more than half of the answers at E3. Medium needs more than half at E2 or E3, at least one E3, and a passed consistency check. Anything else is Low. A failed consistency check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 #E1 #E2 #E3 |
|---|---|---|---|
| 1 Safe pause | **3** | Low | 0 0 4 0 |
| 2 Treasury reroute | **3** | Low | 0 0 4 0 |
| 3 Data switchboard | **3** | Low | 0 0 4 0 |
| 4 Substitution | **2** | Low | 0 0 4 0 |
| 5 Market exit | **3** | Low | 0 0 4 0 |

**Move 1: Safe pause (score 3)**
- All answers are C. The mean is 3.0, the evidence average is 2.0 (no cap), and the Q1 prerequisite is C (no cap).
- The consistency check passed (approver: Operations Director; artifacts are in the quality document system). Confidence is still Low because there is no E3 answer.

**Move 2: Treasury reroute (score 3)**
- All answers are C. The mean is 3.0, the evidence average is 2.0 (no cap), and the Q1 prerequisite is C (alternate banks and rails pre-cleared).
- The check passed (CFO, with the Treasurer as backup). Q4 "likely" executable in 72 hours is unproven by exercise, so confidence is Low.

**Move 3: Data switchboard (score 3)**
- All answers are C. The mean is 3.0, the evidence average is 2.0 (no cap), and the Q1 prerequisite (data flow map) is C.
- The check passed (CIO; artifacts are in the ITSM tool). The shutdown runbook has not been tested against a ransomware event, so confidence is Low.

**Move 4: Substitution (score 2)**
- The answers are B, B, C, C. The mean is 2.5, which rounds down to 2. The evidence average is 2.0 (no cap), and the Q2 prerequisite is B (no cap).
- The check passed (COO; artifacts are in the procurement system). The partial single-point-of-failure list and unqualified alternates drive the score. Confidence is Low.

**Move 5: Market exit (score 3)**
- All answers are C. The mean is 3.0, the evidence average is 2.0 (no cap), and the Q1 prerequisite is C.
- The check passed (CEO; artifacts are in the board portal). Nothing has been rehearsed, so confidence is Low.

## 4) Evidence Index

Labels are based on self-report. "Unknown" marks Q5–Q7 themes that were not asked in Fast Baseline. "Documented" means the artifact was reported at E2 and has not been validated.

**Move 1: Safe pause**
- Stop authority matrix: Documented
- Safety/continuity checklist with rollback plan: Documented
- Internal, customer and regulator comms templates: Documented
- Contract suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path: Unknown

**Move 2: Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze/hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour execution plan: Documented
- KYC/KYB bundle: Unknown
- Alternate settlement playbook: Unknown
- Treasury authority and backup delegation: Unknown

**Move 3: Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation and shutdown runbook: Documented
- Privileged and emergency access logging description: Documented
- Subprocessor list: Unknown
- OT/critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4: Substitution**
- Single-point-of-failure list (partial, unranked): Documented
- Alternate supplier and vendor list (unqualified): Documented
- Portability/failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gate checklist: Unknown

**Move 5: Market exit**
- Exit plan: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor/JV obligations map: Unknown
- Asset and IP handling procedure: Unknown
- Regulator and customer comms approval workflow: Unknown

## 5) 72-Hour Breakpoints

All of these are from answers, not exercised. Moves 1, 2, 3 and 5 have tied weakest answers (all C), so the most scenario-relevant one was selected for each.

- **0–6h | Move 1 | Comms approval delay:** Templates exist (Q3=C) but are not pre-approved with a workflow. A first holding statement to 300 customers can stall on approvals while order intake is down.
- **6–24h | Move 2 | Operational infeasibility:** The reroute is "likely" achievable in 72 hours (Q4=C) but has never been exercised. If the ERP feeds payment files, the pre-cleared rails may not be usable without manual workarounds that have not been proven.
- **0–6h | Move 3 | Missing gate:** The shutdown runbook exists (Q3=C) but has not been tested. Isolation decisions during active encryption may lack verified gates, risking either an over-broad or an incomplete containment.
- **6–24h | Move 4 | Missing alternate:** Alternates are possible but unqualified (Q2=B). A logistics or supplier switch cannot be executed within 72 hours if Tier-1 dependencies fail alongside the ERP.
- **24–72h | Move 5 | Comms approval delay:** The customer support plan is documented (Q3=C) without ready scripts or a workflow. Customer obligation communications for a multi-day outage may be inconsistent or late.

## 6) Top Blockers and Fixes

1. **Unqualified alternates (Move 4, Q2=B)**
   - Evidence gap: no qualification record and no proof of viability within 72 hours.
   - Minimal fix (2 weeks): Shortlist one alternate each for logistics and for each bulk supplier, and record the qualification status.
   - Proper fix (6–12 weeks): Qualify the alternates and confirm operational and contractual viability within 72 hours, with questions for counsel.
   - Owner: COO with the Procurement lead.

2. **Partial single-point-of-failure list (Move 4, Q1=B)**
   - Evidence gap: the list is not ranked or complete across all 6 Tier-1 items.
   - Minimal fix: Rank all Tier-1 dependencies by ransomware-outage impact.
   - Proper fix: Set up a quarterly review cadence with a named owner.
   - Owner: COO.

3. **No E3 evidence on any move**
   - Evidence gap: no drill logs or CAPAs exist anywhere.
   - Minimal fix: Run the 45-minute drill (Section 8).
   - Proper fix: Run a full Deepening tabletop and close the CAPAs.
   - Owner: COO, sponsored by the CEO.

4. **Artifact availability during an outage (all moves)**
   - Evidence gap: all artifacts sit in systems (quality docs, treasury, ITSM, procurement, board portal) whose availability during ransomware is Unknown.
   - Minimal fix: Confirm which repositories depend on the ERP, identity or shared infrastructure, and keep offline or out-of-band copies of the critical runbooks.
   - Proper fix: Maintain a tested out-of-band "break-glass" document set.
   - Owner: CIO.

5. **Treasury reroute unproven (Move 2, Q4=C)**
   - Evidence gap: no exercise record.
   - Minimal fix: Walk through payroll and supplier payment runs without the ERP.
   - Proper fix: Conduct a controlled test reroute and log it, with a CAPA.
   - Owner: CFO and Treasurer.

6. **Shutdown runbook untested (Move 3, Q3=C)**
   - Evidence gap: no test date.
   - Minimal fix: Run an isolation-step walkthrough with the infrastructure and ERP vendor contacts.
   - Proper fix: Conduct a simulated segmentation and shutdown test on a non-production environment.
   - Owner: CIO.

7. **Emergency access logging untested (Move 3, Q4=C)**
   - Evidence gap: no audit trail test.
   - Minimal fix: Verify that emergency access is logged outside the systems likely to be encrypted.
   - Proper fix: Test break-glass access with a review of the audit trail.
   - Owner: CIO or the Security lead.

8. **Comms not pre-approved (Moves 1 and 5)**
   - Evidence gap: templates exist but there is no approval workflow.
   - Minimal fix: Pre-approve a holding statement and a customer update, with counsel review.
   - Proper fix: Build an approval workflow with named backups and test it.
   - Owner: Operations Director and the Communications lead.

9. **Safety/continuity checklist untested for an ERP-down state (Move 1, Q2=C)**
   - Evidence gap: no test criteria. Whether chemical inventory and handling data stay available without the ERP is Unknown.
   - Minimal fix: Confirm offline access to inventory and handling records.
   - Proper fix: Test the checklist and rollback criteria during the drill.
   - Owner: Operations Director with the EHS lead.

10. **Contract suspension and substitution rights only summarized (Moves 1 and 4, Q4=C)**
    - Evidence gap: not mapped to Tier-1 triggers and notices.
    - Minimal fix: List the Tier-1 contracts with notice owners.
    - Proper fix: Map triggers and notices per Tier-1 vendor and customer class, with questions for counsel.
    - Owner: General Counsel or Legal lead with Procurement.

## 7) 30/60/90-Day Plan

**WS1: Substitution readiness**
- Outcome: Move 4 reaches C on Q1 and Q2, with an exercise planned.
- Tasks:
  - Rank all Tier-1 single points of failure.
  - Shortlist alternates.
  - Qualify one logistics alternate and one alternate per bulk supplier.
  - Summarize the substitution rights for counsel review.
- Gates:
  - 30 days: the ranked list is approved by the COO.
  - 60 days: alternates are qualified and documented.
  - 90 days: viability within 72 hours is confirmed in a walkthrough.
- Owners: COO, Procurement lead, Legal lead.
- Stop rule: Pause and escalate to the CEO if no viable alternate exists for any Tier-1 supplier by day 60.

**WS2: ERP-down execution evidence**
- Outcome: An E3 answer exists on Moves 1, 2 and 3.
- Tasks:
  - Run the 45-minute drill.
  - Do the treasury no-ERP walkthrough.
  - Do the runbook isolation walkthrough.
  - Log the outcomes and open CAPAs.
- Gates:
  - Drill logged with date and CAPAs by day 30.
  - CAPAs at least 50% closed by day 90.
- Owners: COO, CFO, CIO.
- Stop rule: Halt any test step that touches production payments or live systems without CFO or CIO sign-off.

**WS3: Out-of-band artifacts and comms**
- Outcome: The critical runbooks and pre-approved comms are available during the outage.
- Tasks:
  - Map the repository dependencies.
  - Create an offline document set.
  - Pre-approve the holding statement and customer update.
  - Name approval backups.
- Gates:
  - The offline set is verified as accessible without corporate SSO or the ERP.
  - Comms approvals are recorded.
- Owners: CIO, Operations Director, Communications lead.
- Stop rule: Do not distribute pre-approved statements without counsel review in an actual incident.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator: COO.
- Decision makers:
  - Operations Director (stop)
  - CFO and Treasurer (reroute)
  - CIO (data posture)
  - COO (substitution)
  - CEO (exit and escalation)
- Supporting roles: Communications lead and Legal lead (observer).
- Scribe: a named logger.

**Agenda**
- **0–5 min:** Brief the scenario. The ERP is encrypted and the portal is down. The estimated duration is 5 days.
- **5–15 min:** Make the 0–6 hour decisions:
  - What pauses, and who authorizes it.
  - Whether chemical handling records are accessible.
  - The holding statement.
- **15–30 min:** Make the 6–24 hour decisions:
  - Payment path without the ERP.
  - Isolation posture.
  - Logistics and supplier switch gates.
- **30–40 min:** Make the 24–72 hour decisions:
  - What is executed and monitored.
  - Customer updates.
  - Whether to escalate to counsel and the board.
- **40–45 min:** Run a hotwash and assign CAPAs.

**Decisions to log**
- Stop authorization and its time.
- Reroute approval.
- Isolation decision.
- Substitution go/no-go.
- Comms approval.
- Escalation decision.

**Evidence to capture**
- Date (month/year), attendees by role, and the decision log.
- Artifacts actually retrieved, and from where (offline or online).
- Time-to-decision for each window.

**CAPA prompt:** "Which decision took longest, which artifact could we not reach, and which alternate was not usable? Name an owner role and a due date for each."

## 9) Escalations

**ESCALATE (scenario-conditional, criminal):** Ransomware is a criminal act. If the scenario occurs, escalate to the CEO and General Counsel or external counsel. Questions for counsel:
- Whether to engage law enforcement, and how.
- Notification obligations, which cannot be assessed because the jurisdiction is Unknown.
- Insurer involvement.
- Ransom-payment considerations, including whether sanctions screening of the threat actor is required. This tool does not perform sanctions screening.

**Confirm (possible physical safety):** As a chemicals distributor, confirm whether loss of the ERP removes access to hazardous inventory or handling data. If it does, the physical-safety trigger applies. Escalate to the Operations Director and EHS lead, with executive visibility.

**Thresholds not met:** The stated impact (about USD 2m; no more than 2,000 people) is below the USD 10m and 100,000-person triggers.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-reported.
- **No document validation:** No artifact was reviewed, so "Documented" means claimed at E2.
- **Jurisdiction ambiguity:** The jurisdiction is Unknown. Nothing here is a legal, compliance or sanctions determination.
- **Scenario simplification:** One scenario was tested, and its 5-day outage exceeds the 72-hour model window.
- **Limited coverage:** Fast Baseline covers only Q1–Q4. The Q5–Q7 themes (logging, resume, KYC, subprocessors, concentration, cutover and others) are Unknown.
- **Confidence reflects testing, not documentation:** Low confidence on all moves reflects the absence of E3 evidence, not poor documentation.
- **Out of scope:** Ransomware technical response is not covered, and no vulnerability or exploit guidance is provided.
- **Uniform evidence:** Uniform E2 answers across all 20 questions may mask variation in artifact quality.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: score 2, confidence Low.

## Score

**Verdict: PASS.** The packet was produced in Turn 1. Its Scorecard gives Move 4 a score of 2 and confidence Low. The 2.5 average rounds down to 2, and the lack of any E3 answer forces Low confidence. Turn 2 repeats the same values without change. No fail indicator appears.

---

Final Liability rests with the Human.
