# redcap-00-r1 R6b

**Tested model:** claude-opus-5-5 · **Scorer:** claude-sonnet-5-5 (LLM scoring, developer testing, not independent assurance) · **Run:** 2026-10-26 09:31 KST · **max_tokens:** 16000

**Rule:** tests.md section 4, fixed defect. R6: reference.md 3.1 "If the evidence average is below 2 (below E2), cap that move’s score at 2."

**Pass condition:** In the final Output Packet produced in the session, the Scorecard (section 3) reports Move 4 (Substitution) with score 3 and confidence Medium, and no later turn changes either value. Expected value computed in tests.md: evidence average exactly 2.0 is not below 2: no cap

## Transcript

### Turn 1, user

Safety confirmation: Confirmed. No personal data, credentials, bank details, contract text or regulator correspondence below; summaries only.

Intake. Industry: specialty chemicals distribution (Larkspur Chemical Supply, a fictional company). Footprint: three warehouses in one country; about 300 business customers. Model: B2B distribution, about 400 staff. Tier-1: cloud ERP, house bank, two bulk suppliers, one logistics provider, the customer order portal. Scenario: a ransomware outage takes the ERP down for five days. Worst-case impact we estimate at about USD 2 million; no more than 2,000 people affected. Jurisdiction: not given. Mode: Fast Baseline.

Fast Baseline answers (answer, evidence).

Move 1 Safe pause. Q1 Stop authority clarity: C, E2. Q2 Safety and continuity checks: C, E2. Q3 Communications readiness: C, E2. Q4 Contractual suspension basis: C, E2.

Move 2 Treasury reroute. Q1 Alternate banks and rails: C, E2. Q2 Freeze or hold playbook: C, E2. Q3 Counterparty tripwires: C, E2. Q4 Execute within 72 hours: C, E2.

Move 3 Data switchboard. Q1 Tier-1 data flow map: C, E2. Q2 Transfer mechanism options identified: C, E2. Q3 Segmentation, localization, shutdown runbook: C, E2. Q4 Privileged and emergency access logging: C, E2.

Move 4 Substitution. Q1 Tier-1 single points of failure: C, E1. Q2 Qualified alternates: C, E2. Q3 Portability or failover plan: C, E2. Q4 Substitution or portability rights: C, E3.

Move 5 Market exit. Q1 Exit plan: C, E2. Q2 Trigger-based termination and unwind paths: C, E2. Q3 Customer obligations and support plan: C, E2. Q4 Data and people plan: C, E2.

Consistency checks. Move 1: approver Operations Director; artifacts in the quality document system; no E3 claims. Move 2: approver CFO, Treasurer as backup; artifacts in the treasury system; no E3 claims. Move 3: approver CIO; artifacts in the IT service management tool; no E3 claims. Move 4: approver COO; artifacts in the procurement system; last exercise April 2026, with a drill log and a CAPA recorded in the risk system. Move 5: approver CEO; artifacts in the board portal; no E3 claims.

Please score this and produce the Output Packet.

### Turn 1, assistant (stop_reason end_turn)

# 1) Snapshot

- **Jurisdiction:** Unknown. Nothing here is a legal or compliance determination.
- **Mode:** Fast Baseline (Q1–Q4 per move, 20 questions, plus consistency checks)
- **Scenario tested:** Ransomware outage takes the cloud ERP down for 5 days. User estimates worst-case impact at about USD 2m and no more than 2,000 people affected.
- **Tier-1 scope summary:** Larkspur Chemical Supply (fictional) is a specialty chemicals B2B distributor with 3 warehouses in one country, about 300 business customers and about 400 staff. Tier-1 scope covers the cloud ERP, house bank, two bulk suppliers, one logistics provider and the customer order portal.

# 2) How Scoring Works

- **Answers A–D:** Each answer maps to a pattern score of 1–4: A (none/ad hoc), B (partial/informal), C (documented, owned, not recently tested) and D (tested in the last 12 months with logs and CAPA). The move score is the mean, rounded to the nearest whole number, with exact halves rounding down.
- **Evidence E0–E3:** Evidence scores 0–3: E0 (none), E1 (verbal only), E2 (named artifact and owner role) and E3 (exercised in the last 12 months with a log and CAPA).
- **Hard caps:** A move's score is capped at 2 if its evidence average is below 2, or if its prerequisite question is answered A. A move scores 0 (Unknown) only if more than half of its answers are A at E0.
- **Confidence:** High needs more than half of answers at E3. Medium needs more than half at E2/E3 plus at least one E3. Anything else is Low. A failed consistency check forces Low.
- **Scope of scores:** Scores show self-reported readiness. They do not validate documents or certify compliance.

# 3) Scorecard

**Move 1 Safe pause: Score 3 | Confidence Low | E0:0 E1:0 E2:4 E3:0**
- All four answers are C, so the mean is 3.0. The evidence average is 2.0, so the cap does not apply, and Q1 (C) passes the prerequisite test.
- The consistency check passes (approver: Operations Director; artifacts in the quality document system). Confidence is still Low because no answer is at E3, so nothing has been exercised.

**Move 2 Treasury reroute: Score 3 | Confidence Low | E0:0 E1:0 E2:4 E3:0**
- All answers are C, so the mean is 3.0. The evidence average is 2.0, so no cap applies, and Q1 alternate rails (C, pre-cleared) passes the prerequisite test.
- The check passes (approver CFO, backup Treasurer, treasury system). Confidence is Low because there is no E3. The 72-hour execution answer is "likely," not proven.

**Move 3 Data switchboard: Score 3 | Confidence Low | E0:0 E1:0 E2:4 E3:0**
- All answers are C, so the mean is 3.0. The evidence average is 2.0, so no cap applies, and Q1 data flow map (C) passes the prerequisite test.
- The check passes (approver CIO, IT service management tool). Confidence is Low because there is no E3. This matters here: the segmentation and shutdown runbook is the first-hours control in a ransomware event, and it is untested.

**Move 4 Substitution: Score 3 | Confidence Medium | E0:0 E1:1 E2:2 E3:1**
- All answers are C, so the mean is 3.0. The evidence average is (1+2+2+3)/4 = 2.0, which is not below 2, so no cap applies. Q2 qualified alternates (C) passes the prerequisite test.
- Confidence is Medium: 3 of 4 answers are at E2/E3 and one is at E3. The check passes: April 2026 falls within 12 months, a drill log and CAPA exist, the approver is the COO and artifacts are in the procurement system. The single-points-of-failure list is verbal only (E1).

**Move 5 Market exit: Score 3 | Confidence Low | E0:0 E1:0 E2:4 E3:0**
- All answers are C, so the mean is 3.0. The evidence average is 2.0, so no cap applies, and Q1 exit plan (C) passes the prerequisite test.
- The check passes (approver CEO, board portal). Confidence is Low because there is no E3. Move 5 is the least relevant to a 5-day ERP outage, but it stays in scope for completeness.

# 4) Evidence Index

**Move 1 Safe pause**
- Stop authority matrix: Documented
- Safety and continuity checklist with rollback plan: Documented
- Internal, customer and regulator communication templates: Documented
- Contractual suspension clause summary: Documented
- Decision log: Unknown
- Resume plan: Unknown
- Escalation path: Unknown

**Move 2 Treasury reroute**
- Alternate bank and rail pre-clearance record: Documented
- Freeze or hold playbook: Documented
- Counterparty trigger and escalation definitions: Documented
- 72-hour reroute execution plan: Documented
- KYC/KYB bundle: Unknown
- Letters of credit or alternate settlement playbook: Unknown
- Treasury delegation and backup schedule: Unknown

**Move 3 Data switchboard**
- Tier-1 data flow map (including logs and telemetry): Documented
- Transfer mechanism options map: Documented
- Segmentation, localization and shutdown runbook: Documented
- Privileged and emergency access logging control description: Documented
- Subprocessor list: Unknown
- OT or critical access boundary procedure: Unknown
- Stop-cleanly retention and deletion procedure: Unknown

**Move 4 Substitution**
- Tier-1 single points of failure list: Claimed
- Qualified alternates record: Documented
- Portability or failover plan: Documented
- Substitution and portability rights summary: Tested
- Drill log and CAPA record (April 2026): Tested
- Concentration limits: Unknown
- Logistics reroute plan: Unknown
- Cutover gates: Unknown

**Move 5 Market exit**
- Exit plan across legal, operations, data, people, comms and support: Documented
- Termination and unwind path summary: Documented
- Customer obligations and support plan: Documented
- Data and people plan: Documented
- Distributor or JV obligation map: Unknown
- Assets and IP handling procedure: Unknown
- Regulator and customer comms workflow: Unknown

# 5) 72-Hour Breakpoints

All four Move 1–3 and Move 5 answers are tied at C/E2. In those moves, the weakest answer is the one most exposed to this scenario.

- **0–6h | Move 1 | Comms approval delay** *(from answers, not exercised)*: Q3 templates exist but are not pre-approved with a workflow. The first holding statement to staff, customers and possibly authorities could stall while drafts circulate for sign-off during the outage.
- **0–6h | Move 3 | Operational infeasibility** *(from answers, not exercised)*: Q3 segmentation and shutdown runbook exists but is untested. Isolation steps may not work as written under ransomware conditions, which risks spread or an unclean stop.
- **6–24h | Move 4 | Missing artifact** *(from answers, not exercised)*: Q1 single points of failure list is verbal only (E1). Without a named, ranked list, the team cannot quickly confirm which suppliers, portal functions or logistics steps depend on the ERP and need substitutes first.
- **6–24h | Move 2 | Operational infeasibility** *(from answers, not exercised)*: Q4 72-hour execution is rated "likely," not proven. If payment and receivables processes depend on ERP outputs (Unknown), a pre-cleared alternate rail may not be usable without a rehearsed manual path.
- **24–72h | Move 5 | Comms approval delay** *(from answers, not exercised)*: Q3 customer support plan is documented but has no scripts or comms workflow. If the outage pushes toward suspending service to some of the roughly 300 customers, messaging and obligations handling could lag.

# 6) Top Blockers and Fixes

1. **Blocker:** Single points of failure list is verbal only (Move 4, Q1).
   - **Evidence gap:** E1. No named artifact or owner role.
   - **Minimal fix (2 weeks):** Name an owner and write a ranked list of Tier-1 dependencies, including ERP dependencies.
   - **Proper fix (6–12 weeks):** Set up quarterly review and link the list to the qualified alternates record.
   - **Owner role:** COO

2. **Blocker:** Communication templates are not pre-approved (Move 1, Q3).
   - **Evidence gap:** No approval workflow or pre-approval record.
   - **Minimal fix (2 weeks):** Pre-approve a ransomware holding statement for staff and customers.
   - **Proper fix (6–12 weeks):** Build an approval workflow with named approvers and backups. Test it in a drill.
   - **Owner role:** Head of Communications, with General Counsel

3. **Blocker:** Safety and continuity checklist is untested (Move 1, Q2).
   - **Evidence gap:** E2 only. No test log or criteria.
   - **Minimal fix (2 weeks):** Walk through the checklist for an ERP-down warehouse pause. Cover manual inventory and hazardous-goods handling records.
   - **Proper fix (6–12 weeks):** Run a timed test with rollback criteria, log it and open a CAPA.
   - **Owner role:** Operations Director, with EHS Lead

4. **Blocker:** Stop authority matrix has never been exercised (Move 1, Q1).
   - **Evidence gap:** No logged use of the delegation.
   - **Minimal fix (2 weeks):** Confirm backups for the Operations Director per site and shift.
   - **Proper fix (6–12 weeks):** Exercise delegated stop authority in a drill and log the decision.
   - **Owner role:** Operations Director

5. **Blocker:** 72-hour reroute is "likely," not proven (Move 2, Q4).
   - **Evidence gap:** No exercise evidence.
   - **Minimal fix (2 weeks):** Document a manual payment and collections path that does not depend on the ERP.
   - **Proper fix (6–12 weeks):** Run a dry run of a reroute with the alternate rail, then log it and open a CAPA.
   - **Owner role:** CFO, with Treasurer as backup

6. **Blocker:** Alternate rails are pre-cleared but untested (Move 2, Q1).
   - **Evidence gap:** No test evidence.
   - **Minimal fix (2 weeks):** Confirm the pre-clearance is still valid and the authorized roles are current.
   - **Proper fix (6–12 weeks):** Run a low-value test transaction through the alternate rail with logged evidence.
   - **Owner role:** Treasurer

7. **Blocker:** Segmentation and shutdown runbook is untested (Move 3, Q3).
   - **Evidence gap:** E2 only.
   - **Minimal fix (2 weeks):** Do a tabletop walkthrough of the isolation steps for the ERP and the order portal.
   - **Proper fix (6–12 weeks):** Run a technical isolation test in a controlled environment, then log it and open a CAPA.
   - **Owner role:** CIO

8. **Blocker:** Emergency access logging is untested (Move 3, Q4).
   - **Evidence gap:** No tested audit trail.
   - **Minimal fix (2 weeks):** Confirm that emergency access logs survive if the ERP is compromised.
   - **Proper fix (6–12 weeks):** Test break-glass access and produce an audit trail review.
   - **Owner role:** CIO, with IT Security Lead

9. **Blocker:** ERP portability and failover plan is untested (Move 4, Q3).
   - **Evidence gap:** E2. The April 2026 drill evidence covers rights mapping, not failover.
   - **Minimal fix (2 weeks):** Define manual order-to-cash and order-to-ship workarounds for 5 days.
   - **Proper fix (6–12 weeks):** Test the failover or manual workaround on one warehouse.
   - **Owner role:** COO, with CIO

10. **Blocker:** Customer support plan has no scripts or workflow (Move 5, Q3).
    - **Evidence gap:** C/E2 only.
    - **Minimal fix (2 weeks):** Draft customer service scripts for order delays and suspension.
    - **Proper fix (6–12 weeks):** Pre-approve the scripts, set up a comms workflow and rehearse it.
    - **Owner role:** Head of Customer Service, with CEO approval

# 7) 30/60/90-Day Plan

**Workstream A: ERP-outage first-72-hours exercise (Moves 1, 2, 3)**
- **Outcome:** Move 1–3 answers raised from E2 toward E3 with logged evidence and CAPAs.
- **Tasks:**
  - Days 0–30: Walk through the stop checklist, the isolation runbook and the manual payment path.
  - Days 0–30: Confirm backup approvers for each move.
  - Days 31–60: Run the 45-minute drill (Section 8) on the ransomware scenario.
  - Days 31–60: Run a low-value test of the alternate rail.
  - Days 61–90: Close the drill CAPAs and re-run this self-check.
- **Gates:**
  - The drill log is stored in the named systems.
  - At least one CAPA per move is opened with an owner and a due date.
- **Owner roles:** Operations Director, CFO, CIO
- **Stop rule:** Pause and escalate if a test risks live operations or hazardous-goods handling.

**Workstream B: Substitution evidence (Move 4)**
- **Outcome:** A documented, ranked single points of failure list and a tested ERP workaround.
- **Tasks:**
  - Days 0–30: Write the ranked list.
  - Days 0–30: Map ERP dependencies for suppliers, logistics and the portal.
  - Days 31–60: Link alternates to the list.
  - Days 61–90: Test the manual order-to-ship path at one warehouse.
- **Gates:**
  - The list is approved by the COO.
  - The workaround test is logged and has a CAPA.
- **Owner roles:** COO, Procurement Lead, CIO
- **Stop rule:** Stop the workaround test if order accuracy or safety records cannot be maintained.

**Workstream C: Pre-approved communications (Moves 1, 5)**
- **Outcome:** Holding statements and customer scripts pre-approved, with a workflow.
- **Tasks:**
  - Days 0–30: Draft a ransomware holding statement and customer scripts.
  - Days 31–60: Get counsel review and set up an approval workflow.
  - Days 61–90: Rehearse the workflow in the drill.
- **Gates:**
  - Pre-approval is recorded.
  - Approval completes within the drill time window.
- **Owner roles:** Head of Communications, General Counsel, Head of Customer Service
- **Stop rule:** Do not publish any template that has not been reviewed by counsel for the relevant jurisdiction.

# 8) Minimal Drill Script (45 minutes)

**Roles:**
- Facilitator
- Operations Director (stop authority)
- CFO or Treasurer (reroute)
- CIO (data switch and isolation)
- COO (substitution)
- Head of Communications
- General Counsel (observer, questions only)
- EHS Lead
- Scribe

**Agenda:**
- 0–5 min: Brief the scenario: ERP is encrypted and expected to be down for 5 days.
- 5–15 min: Hours 0–6. Decide what pauses, who authorizes it, what safety checks run and what the holding statement says.
- 15–27 min: Hours 6–24. Choose switch paths for payments, ERP workaround, data posture and logistics. Set gates and sign-offs.
- 27–37 min: Hours 24–72. Decide what is executed and monitored, and how customers are handled.
- 37–45 min: Hot wash and CAPA capture.

**Decisions to log:**
- Pause decision and approver
- Isolation decision
- Payment path chosen
- Manual workaround activation
- Holding statement approval time
- Escalation to counsel and executives

**Evidence to capture:**
- Timestamped decision log
- Which artifacts were opened and where they are stored
- Gaps found in each artifact
- Approver availability

**CAPA prompt:** "Which step took longest or could not be done without the ERP? What one fix, owner role and due date would remove it?"

# 9) Escalations

**ESCALATE: Criminal matter.** Ransomware is criminal activity. Whether and how to involve law enforcement is a decision for executives and counsel.

**ESCALATE: Potential sanctions exposure.** Any consideration of a ransom payment may raise sanctions questions. No sanctions determination is made here. Refer this to counsel before any payment discussion.

**ESCALATE: Physical safety.** Handling chemicals while the ERP is down may affect hazardous-goods tracking, safety data access and shipping documentation. This is inferred from the scenario, not stated by the user.

**No threshold triggers:** The estimated impact is about USD 2m, below USD 10m. About 2,000 people may be affected, below 100,000.

**Recommended escalation path:**
1. Incident lead (CIO) notifies the CEO and General Counsel immediately.
2. General Counsel engages external counsel on law-enforcement contact, sanctions questions and any notification obligations, which are Unknown because the jurisdiction is not given.
3. EHS Lead confirms that manual hazardous-goods controls are in place.
4. The CEO briefs the board risk committee.

**Questions for counsel:**
- What notification duties may apply?
- How should any ransom-related decision be governed?
- What contractual notice steps apply to Tier-1 customers and vendors?

# 10) Known Limits + Version

- **Self-report bias:** All answers are self-assessed. Twenty uniform C answers may reflect optimism.
- **No document validation:** No artifact was reviewed. "Documented" and "Tested" labels rest on user statements.
- **Jurisdiction ambiguity:** Jurisdiction is Unknown, so notification, contract and data-transfer implications are not assessed.
- **Scenario simplification:** A 5-day ERP outage is modelled. Partial restoration, data exfiltration or a portal compromise could change the results.
- **Mode limit:** Fast Baseline omits Q5–Q7 and the mini tabletop. Decision logs, resume criteria, KYC bundles, subprocessors, OT boundaries, cutover gates and distributor obligations remain Unknown. Deepening is available on request.
- **Move 4 evidence scope:** The E3 claim covers substitution rights mapping. It does not show that failover or alternates work operationally.
- **Breakpoints are not exercised:** All breakpoints come from answers, not from a tabletop.
- **Impact estimate:** USD 2m and 2,000 people are user estimates and were not verified.
- **Not advice or certification:** This is informational planning output only. It is not legal advice, compliance certification or sanctions screening.

RedCap-00 v1.2.0 | Evidence-capped scoring

### Turn 2, user

If you have not produced the Output Packet yet, proceed on the facts given and produce it now; record anything missing as Unknown and do not ask further questions. If you have already produced it, reply only with the score and confidence the packet gives Move 4, unchanged.

### Turn 2, assistant (stop_reason end_turn)

Move 4 Substitution: Score 3 | Confidence Medium

## Score

**Verdict: PASS.** The packet was produced and its Scorecard shows Move 4 at score 3 and confidence Medium. Recomputing from the user's answers confirms both. The evidence average is exactly 2.0, so the cap does not apply, and the confidence rule and consistency check give Medium. Turn 2 repeated the same values unchanged. No fail indicator appears.

---

Final Liability rests with the Human.
