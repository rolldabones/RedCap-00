# redcap-00-r1 Test-B

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:28 KST · **max_tokens:** 16000

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

## 1) Snapshot

- **Jurisdiction:** Unknown
- **Mode:** Fast Baseline (20 questions plus consistency checks)
- **Scenario tested:** A ransomware outage takes the cloud ERP down for five days. Your estimate is about USD 2 million worst-case impact and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) distributes specialty chemicals B2B. It has 3 warehouses in one country, about 300 business customers and about 400 staff. Tier-1 dependencies are the cloud ERP, the house bank, 2 bulk suppliers, 1 logistics provider and the customer order portal.

## 2) How Scoring Works

- **Answer levels:** Each answer is A–D, scored 1–4. A means none or person-dependent, B partial or untested, C documented and owned, and D tested in the last 12 months with logs and CAPA.
- **Evidence levels:** Each answer also carries an evidence level, scored 0–3. E0 means none, E1 verbal only, E2 a named artifact with an owner role, and E3 tested within 12 months with a log and a CAPA.
- **Provisional score:** The mean of a move's answer scores, rounded. An exact half rounds down.
- **Caps:** A move scores 0 (Unknown) only if 3 or more of its 4 answers are A at E0. The score is capped at 2 if the move's evidence average is below 2. It is also capped at 2 if the move's prerequisite question is answered A.
- **Confidence:** High needs more than half the answers at E3 and a passed consistency check. Medium needs more than half at E2 or E3, at least one E3, and a passed check. Everything else is Low, and a failed check forces Low.

## 3) Scorecard

| Move | Score | Confidence | #E0 | #E1 | #E2 | #E3 |
|---|---|---|---|---|---|---|
| 1 Safe pause | 3 | Low | 0 | 0 | 4 | 0 |
| 2 Treasury reroute | 2 | High | 1 | 0 | 0 | 3 |
| 3 Data switchboard | 3 | Low | 0 | 0 | 4 | 0 |
| 4 Substitution | 3 | Low | 0 | 0 | 4 | 0 |
| 5 Market exit | 3 | Low | 0 | 0 | 4 | 0 |

**Move 1 Safe pause: 3, Low**
- All four answers are C at E2, so the mean is 3.0. The evidence average is 2.0, which is not below 2, so no evidence cap applies. Q1 is C, so there is no prerequisite cap. Final score: 3.
- Confidence is Low because there are no E3 answers, and Medium requires at least one. The consistency check passes: the approver is the Operations Director and the artifacts are in the quality document system.

**Move 2 Treasury reroute: 2, High**
- The answers are A, D, D, D, giving a mean of 3.25 and a provisional score of 3. The evidence average is 2.25, so no evidence cap applies. Q1 (alternate banks and rails) is A, so the prerequisite cap applies. Final score: 2.
- Confidence is High because 3 of 4 answers are at E3. The check passes: the April 2026 drill is within 12 months, and a log and a CAPA are recorded. The approver is the CFO with the Treasurer as backup, and the artifacts are in the treasury system.
  - **Caution:** Q4 says execution within 72 hours is proven by exercise, yet Q1 says there is no alternate bank or rail. The High rating reflects your evidence for hold and tripwire capability, not for a reroute path.

**Move 3 Data switchboard: 3, Low**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is 2.0. Q1 is C. No caps apply. Final score: 3.
- Confidence is Low because there are no E3 answers. The check passes: the approver is the CIO and the artifacts are in the IT service management tool.

**Move 4 Substitution: 3, Low**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is 2.0. The prerequisite question, Q2 (qualified alternates), is C. No caps apply. Final score: 3.
- Confidence is Low because there are no E3 answers. The check passes: the approver is the COO and the artifacts are in the procurement system.

**Move 5 Market exit: 3, Low**
- All four answers are C at E2, so the mean is 3.0 and the evidence average is 2.0. Q1 is C. No caps apply. Final score: 3.
- Confidence is Low because there are no E3 answers. The check passes: the approver is the CEO and the artifacts are in the board portal.

## 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist: Documented
- Rollback plan: Documented
- Communications templates (internal, customer, regulator): Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Safe-pause drill log and CAPA: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail register: Unknown
- Freeze or hold playbook: Tested
- Counterparty tripwire definitions and escalation: Tested
- 72-hour execution drill log (April 2026): Tested
- Drill CAPA record: Tested
- Treasury authority and backup delegation: Claimed
- KYC or KYB bundle: Unknown
- Alternate settlement playbook: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map: Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Retention and deletion procedure: Unknown

**Move 4 Substitution**
- Tier-1 single-point-of-failure ranked list: Documented
- Qualified alternates register: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Documented
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates and evidence pack: Unknown

**Move 5 Market exit**
- Exit plan: Documented
- Termination and unwind summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligations map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

## 5) 72-Hour Breakpoints

For Moves 1, 3, 4 and 5, all four answers tie at C/E2. In each case the bullet uses the tied answer most relevant to the scenario.

- **0–6 h | Move 1 | Comms approval delay** *(from answers, not exercised)*. Q3 templates exist but are not pre-approved and have no approval workflow. The first holding statement to customers and staff would wait on ad hoc sign-off while the ERP is down.
- **6–24 h | Move 2 | Missing alternate** *(from answers, not exercised)*. Q1 shows no alternate bank or rail. If house-bank access is suspended or held during the incident, there is no pre-cleared path to keep payables and receivables flowing.
- **0–6 h | Move 3 | Operational infeasibility** *(from answers, not exercised)*. The Q3 segmentation and shutdown runbook has never been tested. Containment of the ERP and connected systems, such as the order portal, may not run as written under live ransomware conditions.
- **6–24 h | Move 4 | Operational infeasibility** *(from answers, not exercised)*. The Q3 failover plan is documented but untested. Manual order-to-cash and dispatch without the ERP across three warehouses has not been shown to work at volume.
- **24–72 h | Move 5 | Comms approval delay** *(from answers, not exercised)*. The Q3 customer obligations plan exists, but scripts and a comms workflow are not ready. Customer service for about 300 accounts would improvise during a multi-day outage.

## 6) Top Blockers and Fixes

1. **No alternate bank or rail** (Move 2, Q1 = A/E0)
   - **Evidence gap:** No register, no owner, no record.
   - **Minimal fix (2 weeks):** Shortlist 1–2 alternate institutions and rails. Name an owner.
   - **Proper fix (6–12 weeks):** Pre-clear one alternate. Test a reroute and log it with a CAPA.
   - **Owner role:** Treasurer

2. **Unclear scope of the 72-hour treasury drill** (Move 2, Q4 D/E3 conflicts with Q1 A/E0)
   - **Evidence gap:** It is unclear what the April 2026 drill exercised if no alternate rail exists.
   - **Minimal fix (2 weeks):** Review the drill log and record its scope, for example "hold or freeze in house bank only."
   - **Proper fix (6–12 weeks):** Re-scope the next drill to include an actual reroute.
   - **Owner role:** CFO, with the risk function

3. **Untested segmentation and shutdown runbook** (Move 3, Q3 C/E2)
   - **Evidence gap:** No test date, log or CAPA.
   - **Minimal fix (2 weeks):** Walk through the runbook against the ERP and portal dependencies. Confirm a copy is available offline.
   - **Proper fix (6–12 weeks):** Run a technical containment exercise with a log and CAPA.
   - **Owner role:** CIO, with security lead

4. **Untested privileged and emergency access logging** (Move 3, Q4 C/E2)
   - **Evidence gap:** No proof that logs survive a compromise or are reviewable.
   - **Minimal fix (2 weeks):** Confirm the log retention location is separate from the ERP environment.
   - **Proper fix (6–12 weeks):** Test break-glass access end to end with an audit trail.
   - **Owner role:** Security lead

5. **Untested ERP failover and manual operations** (Move 4, Q3 C/E2)
   - **Evidence gap:** No test showing manual order, picking and dispatch work for 5 days.
   - **Minimal fix (2 weeks):** Pre-print manual forms. Define a minimum viable order list for priority customers.
   - **Proper fix (6–12 weeks):** Run a one-warehouse manual-mode drill with throughput metrics and a CAPA.
   - **Owner role:** COO

6. **Alternates not proven viable within 72 hours** (Move 4, Q2 C/E2)
   - **Evidence gap:** Alternates are "identified and qualified" but not shown to be contractually and operationally ready within 72 hours.
   - **Minimal fix (2 weeks):** Confirm a 72-hour activation path with the alternate logistics provider and suppliers.
   - **Proper fix (6–12 weeks):** Hold standby arrangements and run a test order through an alternate.
   - **Owner role:** Head of Procurement

7. **Stop authority never exercised** (Move 1, Q1 C/E2)
   - **Evidence gap:** The matrix exists, but delegation under outage conditions has not been demonstrated.
   - **Minimal fix (2 weeks):** Confirm deputies and an out-of-band contact method for the Operations Director.
   - **Proper fix (6–12 weeks):** Exercise the delegation in a tabletop and log the decisions.
   - **Owner role:** Operations Director

8. **Untested safety checks and rollback for chemical operations** (Move 1, Q2 C/E2)
   - **Evidence gap:** No proof that hazmat inventory and safety data stay accessible without the ERP.
   - **Minimal fix (2 weeks):** Confirm an offline copy of the hazardous-material inventory and safety data per warehouse.
   - **Proper fix (6–12 weeks):** Test the checklist and rollback plan in a drill with safety criteria.
   - **Owner role:** Environment, Health and Safety Manager

9. **Comms templates not pre-approved; customer scripts not ready** (Move 1 Q3 and Move 5 Q3, both C/E2)
   - **Evidence gap:** No approval workflow or named approvers.
   - **Minimal fix (2 weeks):** Pre-approve one holding statement each for staff, customers and suppliers.
   - **Proper fix (6–12 weeks):** Build an approval workflow and customer-service scripts, then rehearse them.
   - **Owner role:** Head of Communications, with Customer Service Lead

10. **Contract bases summarized but not mapped to Tier-1 contracts** (Move 1 Q4, Move 4 Q4, Move 5 Q2, all C/E2)
    - **Evidence gap:** No trigger-and-notice mapping for the ERP vendor, bank, suppliers and logistics provider.
    - **Minimal fix (2 weeks):** List Tier-1 notice obligations and deadlines in planning-level form, for counsel to review.
    - **Proper fix (6–12 weeks):** Have counsel validate the trigger and notice map for all Tier-1 agreements.
    - **Owner role:** General Counsel

## 7) 30/60/90-Day Plan

**Workstream A: Treasury alternate path (Move 2)**
- **Outcome:** One pre-cleared alternate rail, with a reroute tested within 90 days.
- **Tasks:**
  - Days 0–30: Confirm the scope of the April 2026 drill. Shortlist alternates.
  - Days 31–60: Begin onboarding and assemble a KYB bundle.
  - Days 61–90: Run a reroute drill and log it with a CAPA.
  - Throughout: Confirm the Treasurer can act as backup without ERP access.
- **Gates:**
  - Alternate pre-cleared, with a named owner.
  - Drill log and CAPA filed in the risk system.
- **Owner roles:** CFO (accountable), Treasurer (responsible)
- **Stop rule:** Pause and escalate to the CFO if onboarding needs non-public data the program cannot safely handle, or if counsel flags a jurisdictional question.

**Workstream B: ERP-down containment and manual operations (Moves 3 and 4)**
- **Outcome:** Tested containment and a tested manual mode for one warehouse.
- **Tasks:**
  - Confirm offline availability of runbooks and of artifacts held in the ITSM tool, quality system and procurement system.
  - Run a runbook walkthrough.
  - Run a break-glass access test.
  - Run a manual-mode drill at one warehouse.
  - Confirm 72-hour activation with the alternate logistics provider.
- **Gates:**
  - Runbooks retrievable without the ERP or corporate identity systems.
  - Manual-mode drill meets a throughput target set by the COO.
  - CAPA opened for every gap found.
- **Owner roles:** CIO, Security lead, COO, Head of Procurement
- **Stop rule:** Halt any live test that creates safety or customer-delivery risk. Revert to tabletop format.

**Workstream C: Convert E2 to E3 through exercises and pre-approvals (Moves 1, 5 and cross-move)**
- **Outcome:** At least one E3 answer per move, which allows confidence to rise to Medium, and pre-approved comms.
- **Tasks:**
  - Run the 45-minute drill in Section 8 by day 30.
  - Pre-approve holding statements.
  - Test the hazmat safety checklist offline.
  - Start counsel-led contract trigger mapping.
  - Re-run this self-check at day 90.
- **Gates:**
  - Drill log and CAPA recorded for each move exercised.
  - Comms templates approved by named roles.
- **Owner roles:** Operations Director, EHS Manager, Head of Communications, General Counsel
- **Stop rule:** If the drill reveals a physical-safety gap, stop the plan sequence and escalate to the COO and EHS Manager before continuing.

## 8) Minimal Drill Script (45 minutes)

**Roles**
- Facilitator (risk function)
- Operations Director (stop authority)
- CFO and Treasurer
- CIO and Security lead
- COO
- EHS Manager
- Head of Communications
- General Counsel
- Scribe

**Agenda**
- **0–5 min:** Inject. The ERP is encrypted, the order portal is down, and the outage is expected to last 5 days.
- **5–15 min (hours 0–6):**
  - What is paused, and who authorizes the pause?
  - Can hazmat safety data be accessed offline?
  - What is the first holding statement?
- **15–25 min (hours 6–24):**
  - Manual-mode decision.
  - Treasury posture if house-bank access is held.
  - Logistics activation.
- **25–35 min (hours 24–72):**
  - What is executed and monitored?
  - Customer-service handling.
  - Supplier and contract notices, as questions for counsel.
- **35–45 min:** Gaps, CAPA assignment and owners.

**Decisions to log**
- Pause scope and approver
- Containment action and approver
- Manual-mode go or no-go
- Treasury hold or reroute
- Holding-statement approval
- Escalation to counsel and executives

**Evidence to capture**
- Timestamped decision log
- Attendee roles
- Which artifacts were retrieved, and whether each was available offline
- Time to each decision

**CAPA prompt**
For each stall, record:
- What blocked us?
- Which artifact or authority was missing?
- What is the minimal fix, who owns it, and by what date?
- What evidence will show it is closed?

## 9) Escalations

**ESCALATE.** Triggers identified from the scenario as described. These are planning flags, not legal or sanctions determinations.

- **Criminal:** A ransomware scenario involves suspected criminal activity.
  - **Questions for counsel:** When and how should law enforcement be engaged? What evidence should be preserved?
- **Physical safety:** An ERP outage at chemical warehouses may weaken hazmat inventory tracking, access to safety data and dispatch controls.
  - **Questions for the EHS Manager and counsel:** What are the safe-operation thresholds? When should a site pause?
- **Sanctions (conditional):** Any consideration of a ransom payment raises sanctions questions.
  - **Question for counsel:** What must be reviewed before any payment decision is made? RedCap-00 makes no determination on this.
- **Regulator inquiry (possible, Unknown):** Incident notification duties depend on jurisdiction, which is Unknown.
  - **Questions for counsel:** Which notification obligations may apply? What are the deadlines?

The financial and population thresholds are **not** met: about USD 2 million is below USD 10 million, and 2,000 people is below 100,000.

**Recommended path:**
1. CEO and board chair.
2. General Counsel, plus external counsel experienced in cyber incidents.
3. CIO and Security lead.
4. EHS Manager for any site-safety pause decision.

## 10) Known Limits + Version

- **Self-report bias:** All answers and evidence levels are self-declared.
- **No document validation:** No artifact was reviewed. "Documented" and "Tested" labels reflect your claims only.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification, contract and sanctions questions are framed for counsel only.
- **Scenario simplification:** A single ERP outage was modeled. Combined events, such as data exfiltration or bank-side holds, are not scored.
- **Fast Baseline only:** Q5–Q7 and the mini tabletop were not run. Artifacts covered by those questions are listed as Unknown.
- **Move 2 tension:** The High confidence rating is rule-based. The conflict between Q1 and Q4 needs human review of the scope of the April 2026 drill.
- **Artifact availability:** Whether artifacts can be reached during a ransomware event (in the ITSM tool, quality system, procurement system and board portal) is Unknown.
- **Impact estimates:** The USD 2 million and 2,000-person figures are your estimates and were not verified.
- **Not legal advice:** This is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 2, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 2 Treasury reroute: score 2, confidence High.

## Score

**Verdict: PASS.** The Move 2 score of 2 and confidence of High match the values recomputed from the reference pack. The prerequisite cap (Q1 = A) lowers the provisional score of 3 to 2. The evidence-average cap does not apply, and the zero rule does not apply. Confidence is High because 3 of 4 answers are E3 and the consistency check passes. The Output Packet was produced in Turn 1, and Turn 2 repeats the same values unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
